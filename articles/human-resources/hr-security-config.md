---
title: Drošības konfigurācijas koncepcijas virtuālo tabulu integrācijām
description: Šajā rakstā ir izskaidrota arhitektūra integrācijas veidošanai starp Microsoft Dynamics 365 Human Resources un citām sistēmām.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759729"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Drošības konfigurācijas koncepcijas virtuālo tabulu integrācijām

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīta arhitektūra virtuālo tabulu (entītiju) izmantošanai [Microsoft Dataverse,](/dev-itpro/power-platform/virtual-entities-overview) lai izveidotu integrāciju starp Dynamics 365 Human Resources trešo pušu sistēmu. Raksta uzmanības centrā ir drošības konfigurācija un autentifikācijas un autorizācijas aspekti, kas nepieciešami starp sistēmas robežām, lai izveidotu funkcionālu, drošu sistēmu.

## <a name="prerequisite-reference-articles"></a>Priekšnosacījumu atsauces raksti

Šajos rakstos ir sniegta plašāka informācija par šī raksta jēdzieniem:

- [Virtuālo elementu pārskats](/dev-itpro/power-platform/virtual-entities-overview)
- [Darba sākšana ar virtuālajām tabulām (entītijām)](/developer/data-platform/virtual-entities/get-started-ve)
- [Vairāku nomnieku starpserveru autentifikācijas izmantošana (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Izmantojiet OAuth autentifikāciju ar Microsoft Dataverse (Dataverse)](/developer/data-platform/authenticate-oauth)
- [OAuth 2.0 klienta akreditācijas datu plūsma Microsoft identitātes platformā](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Autentifikācija un autorizācija](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Arhitektūra 

Šajā arhitektūras diagrammā ir parādīti galvenie jēdzieni, kas ir iesaistīti integrācijā, kurā tiek izmantotas virtuālās tabulas (entītijas).

![Uz virtuālo galdu balstīta integrācija.](./media/Hosts.jpg)

Tālāk ir sniegts skaidrojums par dažiem elementiem iepriekšējā diagrammā.

- **Microsoft — Microsoft** vieso un klientu vārdā darbina dažādus Dynamics 365 produktus.

    - **Azure Active Directory(Azure AD) nomnieks C** — nomnieks Azure AD, kas pieder korporācijai Microsoft. Dynamics 365 lietojumprogrammas ir reģistrētas nomniekā.

- **Integrējošais partneris**

    - **Integrējoša sistēma — sistēma, kas tiek integrēta** ar Dynamics 365. Tā var būt algu sistēma vai jebkura sistēma, kas paļaujas uz dynamics 365 saglabātajiem datiem.
    - **Adapteris** — programmatūra vai pakalpojums, kas atbild par mijiedarbību gan ar Dynamics 365, gan integrējošo sistēmu.

        > [!NOTE]
        > Ja adapteris ir paredzēts lietošanai vairākiem Dynamics 365 debitoriem, tiek sagaidīts, ka tas tiks reģistrēts kā vairāktenantu lietojumprogramma pakalpojumā Azure AD.

    - **Azure AD nomnieks A** — nomnieks Azure AD, kas pieder integrējošajam partnerim. Tas ir nomnieks, kurā adaptera lietojumprogrammas ID ir reģistrēts.

- **Savstarpējs klients** – klients Dynamics 365 Human Resources, kas ievieš un integrē partnera risinājumu.

    - **Dynamics 365 Finance vai Human Resources — klientam specifiska Dynamics 365 Finance vai Human Resources** instance, kas satur integrējošajai sistēmai nepieciešamos klienta datus.
    - **Dataverse**- Klientam raksturīga Dataverse vide, kas ir saistīta ar Finance vai Cilvēkresursiem. Dataverse nodrošina tīmekļa API mijiedarbībai ar Dynamics 365 datiem.
    - **Azure AD nomnieks B** – klienta nomnieks Azure AD. Tas darbojas kā identitātes nodrošinātājs (autorizācijas serveris) un izsniedz marķierus, kas pilnvaro zvanītājus zvanīt uz klienta Dataverse instanci.

## <a name="basic-request-flow"></a>Pamata pieprasījuma plūsma

Šajā sadaļā ir aprakstīta vienkārša pieprasījuma, kas ir iesaistīts integrācijā, pamatplūsma. Tajā ir atsauce uz arhitektūras diagrammu iepriekš šajā rakstā.

Tipiskam pieprasījumam ir nepieciešams, lai adapteris vaicātu Dynamics 365 datiem un pēc tam saglabātu un sinhronizētu šos datus ar integrējošo sistēmu.

1. Adapteris izsauc Dataverse tīmekļa API, lai vaicātu par atbilstošiem datiem.

    > [!NOTE]
    > Autentifikācija ir priekšnoteikums, un marķiera iegūšana ir būtiska procesa daļa. Autentifikācija tiks aprakstīta [sadaļā Autentifikācija un autorizācija sistēmas robežās](#authentication-and-authorization-at-system-boundaries).

    Šis aicinājums tiek veikts, Dataverse izmantojot tīmekļa API, lai vaicātu par lietojumprogrammas datiem, kas tiek parādīti, izmantojot virtuālo tabulu. (Sk. "2. Sākotnējā sinhronizācija" un "3. Delta Sync" diagrammā.)

2. Dataverse apstrādā pieprasījumu, veicot vaicājumus virtuālajā tabulā, izmantojot virtuālās entītijas spraudni ("Virtuālās tabulas starpniekserveris" diagrammā). Pieprasījums Dataverse tiek pārsūtīts finanšu vai cilvēkresursu virtuālās entītijas pakalpojumam, lai vaicātu par datiem, kas fiziski tiek glabāti finanšu vai cilvēkresursu datu bāzē.
3. Pakalpojums Finanses vai Cilvēkresursu virtuālā entītija pārvērš pieprasījumu pret virtuālo entītiju vaicājumā pret finanšu vai cilvēkresursu entītiju, kas atbalsta virtuālo Dataverse entītiju. Dati tiek izgūti no datu bāzes, pārvērsti atpakaļ entītijas attēlojumā Dataverse un atgriezti zvanītājam.
4. Adapteris pabeidz visu nepieciešamo kartēšanu un datu tulkošanu un zvana uz integrējošo sistēmu, lai saglabātu datus integrējošās sistēmas datu bāzē. (Sk. "4. Saglabāt datus" diagrammā.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Autentifikācija un autorizācija sistēmas robežās

*Autentifikācija* apstiprina, ka lietotāja vai lietojumprogrammas identitāte ir pierādīta, un apstiprina, ka lietotājs vai lietojumprogramma ir tas, par ko viņi saka, ka viņi ir. *Autorizācija* piešķir lietotājam vai lietojumprogrammai tiesības piekļūt noteiktām lietojumprogrammas līmeņa atļaujām. Papildinformāciju skatiet sadaļā [Autentifikācija salīdzinājumā ar autorizāciju](/azure/active-directory/develop/authentication-vs-authorization).

Lielākā daļa starpsistēmu izsaukumu arhitektūras diagrammā iepriekš šajā rakstā ietver adapteri. Adapterim ir jāautentificējas, lai veiktu šādus zvanus:

- Aicinājums uz Dataverse
- Aicinājums uz integrējošo sistēmu

Apskatiet sistēmas robežas diagrammā. Katrs tīmekļa pieprasījums starp sistēmām ir jāautentificē, un pirms datu atgriešanas zvanītājam ir jānokārto lietojumprogrammas līmeņa autorizācijas pārbaudes. Pieprasījumam pret Dynamics 365 virtuālo tabulu, ko atbalsta programma Finance vai Human Resources, autentifikācijas un autorizācijas pārbaudes tiek īstenotas tālāk norādītajās sistēmas robežās.

- Zvans starp adapteri un Dataverse tīmekļa API (OData) galapunktu
- Zvans starp virtuālās entītijas spraudni un finanšu vai cilvēkresursu virtuālās Dataverse entītijas pakalpojumu

Abos gadījumos vispirms tiek veiktas autentifikācijas pārbaudes. Pēc tam tiek veiktas lietojumprogrammas līmeņa autorizācijas pārbaudes, lai pārliecinātos, vai autentificētajam lietotājam vai lietojumprogrammai ir pareizās lietojumprogrammas līmeņa atļaujas, lai izgūtu pieprasītos datus.

Zvana Dataverse autentifikācija tiek apstrādāta, izmantojot uzrādītāja marķieri, kas tīmekļa pieprasījumā ir jāiekļauj kā HTTP galvene.Dataverse Adapterim ir jāsaņem marķieris no nomnieka B Azure AD instances. (Sk. "1. Get Token" diagrammā.) Azure AD darbojas kā identitātes nodrošinātājs autentifikācijas plūsmā.

Adapteris autentificējas, norādot savu lietojumprogrammas identitāti (neslepens, kā reģistrēts nomniekā Azure AD A) un lietojumprogrammas noslēpumu vai sertifikātu, kas ir tikai adaptera lietojumprogrammai.

Pēc tam, kad lietotājs vai lietojumprogramma ir autentificēta, lai veiktu zvanus Dataverse, Dataverse autorizācijas pārbaudes tiek veiktas pret katru pieprasījumu. Šīs pārbaudes nodrošina, ka zvanītājam (adaptera lietojumprogrammas identitātei, kas diagrammā ir apzīmēta kā """\<guid A\>) ir atbilstošas lietojumprogrammas atļaujas. Lietojumprogrammas līmeņa autorizācija tiek pārvaldīta Dataverse, izmantojot lietojumprogrammas lietotāju, kas pārstāv adaptera lietojumprogrammas ID. Lietojumprogrammas līmeņa atļaujas tiek pārvaldītas, piešķirot piekļuvi noteiktām Dataverse definētām lietojumprogrammu lomām. Šīs lomas nodrošina lietojumprogrammai detalizētas atļaujas.

Detalizētākus norādījumus skatiet sadaļā [Vairāku nomnieku starpserveru autentifikācijas](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication) izmantošana.

Ja Dataverse lietojumprogrammas atļauju pārbaudes līmenī ir nokārtotas, spraudnis Virtuālā entītija veic zvanu uz virtuālās entītijas pakalpojuma galapunktu finanšu vai cilvēkresursu vidē. Lai veiktu šo zvanu, tiek izmantota starpserveru (S2S) autentifikācija. Tas izmanto identitāti un noslēpumu, kas ir konfigurēts Finance and Operations virtuālā datu avota konfigurācijas ierakstā.

![Finance and Operations virtuālā datu avota konfigurācijas ieraksts smilškastes vidē.](./media/sandbox.jpg)

Papildinformāciju skatiet sadaļā [Virtuālo entītiju Dataverse konfigurēšana](/dev-itpro/power-platform/admin-reference).

Zvans no virtuālās Dataverse entītijas spraudņa uz programmu Finance vai Human Resources ietver adaptera identitāti sākotnējam zvanam no Dataverse adaptera (identitāte, kas arhitektūras diagrammā ir apzīmēta kā "\<guid A\>"). Ja virtuālās entītijas datu avots ir pareizi konfigurēts un S2S autentifikācijas pārbaudes ir nokārtotas, virtuālās entītijas pakalpojums programmatūrā Finance vai Human Resources izpildīs vaicājumu sākotnējā zvanītāja (adaptera, \<guid A\>) kontekstā. Lietojumprogrammu atļauju pārbaudes (autorizācija) finanšu vai cilvēkresursu līmenī tiks veiktas, lai nodrošinātu, ka adapterim ir atļaujas, kas nepieciešamas, lai piekļūtu vaicājuma pieprasītajiem datu elementiem.

Finanšu un cilvēkresursu drošība tiek pārvaldīta šādos veidos:

1. Kartējot adaptera identitāti (\<guid A\>) uz konkrētu finanšu vai cilvēkresursu lietotāju. Šī kartēšana tiek veikta **Azure Active Directory lietojumprogrammu** lapā. Papildinformāciju skatiet sadaļā [Ārējās lietojumprogrammas reģistrēšana](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Piešķirot finanšu vai cilvēkresursu lietotājam atbilstošas lietojumprogrammas līmeņa lomas, pienākumus un atļaujas. Papildinformāciju skatiet sadaļā [Uz lomām balstīta drošība](/dev-itpro/sysadmin/role-based-security).

Ja adaptera lietojumprogrammai (\<guid A\>) ir piešķirtas atļaujas, kas nepieciešamas, lai piekļūtu pieprasītajiem datiem, notiek šādi notikumi:

1. Vaicājums tiek izpildīts.
2. Dati tiek tulkoti atpakaļ uz entītijas Dataverse lapu.
3. Dati tiek atgriezti adapterī.

> [!IMPORTANT]
> Izstrādes laikā adapteri var palaist, izmantojot finanšu vai cilvēkresursu lietotāju, kuram ir administratora loma. Tomēr ražošanas vidē adapteri nekad nedrīkst palaist ar administratora atļaujām.

## <a name="key-takeaways"></a>Galvenās atziņas

Tālāk ir norādīti daži svarīgi virtuālās tabulas vai entītijas arhitektūras aspekti.

- Drošības konfigurācija virtuālajām tabulām, kuras atbalsta personāla vadība, tiek pārvaldīta sadaļā Personāla vadība.
- Klientam ("Savstarpējais klients" arhitektūras diagrammā iepriekš šajā rakstā) ir pilnīga kontrole pār to, kādas privilēģijas tiek piešķirtas integrējošā adaptera identitātei (diagrammā apzīmēta kā "\<guid A\>").
- Klients ir atbildīgs par pareizu personāla vides drošības konfigurāciju. Integrējošajam partnerim, kurš izveido adapteri, ir jāsniedz norādījumi par adapterim nepieciešamajām atļaujām.
