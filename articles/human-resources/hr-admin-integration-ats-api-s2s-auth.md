---
title: Servera-servera autentifikācija ATS integrācijas API
description: Šajā tēmā ir aprakstīts, kā iestatīt servera-servera autentifikāciju integrācijai ar Dynamics 365 Human Resources kandidātu izsekošanas sistēmas (ATS) integrācijas API.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aabe2cd9fd962c8f1c5bbf7fe911e7c6ceeae082f61fc4359aaf7bf197531eff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778083"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Servera-servera autentifikācija ATS integrācijas API

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā ir aprakstīts, kā iestatīt servera-servera autentifikāciju pieteikumu integrācijai ar Dynamics 365 Human Resources kandidātu izsekošanas sistēmas (ATS) integrācijas API. Ir daži drošības līmeņi, kas ir jāvalda pakalpojumu pamatdatiem, lai piekļūtu virtuālajai tabulai un ar to Microsoft Dataverse saistītajiem datiem. Lietotājam jābūt piešķirtai piekļuvei Dataverse virtuālajai tabulai Microsoft Power Platform un piekļuvei datiem programmā Dynamics 365 Human Resources.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Iespējojiet piekļuvi Dataverse virtuālām tabulām Power Platform

Pirmā darbība iespējo piekļuvi Dataverse virtuālajām tabulām Power Platform, ir iestatīt jūsu programmu autentifikācijai Power Platform attiecībā uz Dataverse virtuālās tabulas galapunktiem. Darbības, kas veicamas, lai to izdarītu, ir aprakstītas [Microsoft Dataverse izstrādātāju ceļvedī](/powerapps/developer/data-platform).

  - Viena nomnieka programmas reģistrācijām: [Izmantojiet viena nomnieka autentifikāciju no servera uz serveru](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Vairāku nomnieku programmas reģistrācijām: [Izmantojiet vairāku nomnieku autentifikāciju no servera uz serveru](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Drošības lomas izveide ATS integrācijām

Viena no darbībām pēc programmas lietotāja izveidošanas ir piešķirt lietotāju drošības lomai, kas nosaka piekļuvi programmai, galapunktiem būs. Šī ir 7. darbība [Programmas lietotāja izveidošanā](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) viena nomnieka programmas reģistrācijām un [Drošības lomas izveide](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) programmas lietotājam vairāku nomnieku reģistrācijām. 

Lomai, kurai piešķirat programmas lietotāju, ir jābūt piekļuvei datu elementiem, kas tiek izmantoti jūsu ATS integrācijai. Kastē nepastāv šāds vienums, tādēļ ir jāizveido jauna drošības loma. Jauno lomu var izveidot, ņemot vērā darbības, kas izklāstītas sadaļā [Drošības lomas izveide](/power-platform/admin/create-edit-security-role#create-a-security-role).

Jaunajai lomai ir jāpiešķir atbilstoša piekļuve vismaz tālāk minētajiem elementiem jaunās lomas cilnē **Pielāgotās entītijas**. Ievērojiet, ka var būt papildu entītijas, kuras var būt nepieciešams pievienot, ja integrācija izmanto plašākus lietojumprogrammas datus. Kad jaunā loma ir izveidota, to var piešķirt programmas lietotājam.

  - Pamatstrādnieks (mshr)
  - Kandidāts pieņemšanai darbā (mshr)
  - Sertifikāta kompetence (mshr)
  - Sertifikāta veids (mshr)
  - Uzņēmums
  - Atlīdzības darba funkcija (mshr)
  - Atlīdzības darba veids (mshr)
  - Valsts/reģioni (mshr)
  - Nodaļa (mshr)
  - Izglītības kompetence (mshr)
  - Izglītības pakāpe (mshr)
  - Izglītības disciplīnas (mshr)
  - Izglītības prasības (mshr)
  - Identifikācijas tips (mshr)
  - Identifikācijas veida (mshr)
  - Institūcija (mshr)
  - Izdevējiestāde (mshr)
  - Darba kompensācija (mshr)
  - Darbi (mshr)
  - Izglītības līmenis (mshr)
  - Puses kontaktpersonas (mshr)
  - Cilvēki (mshr)
  - Personu adreses (mshr)
  - Personas izvērtēšana (mshr)
  - Amata veids (mshr)
  - Pozīcija V2 (mshr)
  - Profesionālās pieredzes kompetence (mshr)
  - Novērtējuma līmenis (mshr)
  - Vērtēšanas modeļi (mshr)
  - Iemeslu kodi (mshr)
  - Darbā pieņemšanas pieprasījums (mshr)
  - Darbā pieņemšanas pieprasījuma atrašanās vieta (mshr)
  - Darbā pieņemšanas pieprasījuma amats (mshr)
  - Darbā pieņemšanas prasmes (mshr)
  - Izvērtēšanas tips (mshr)
  - Prasmju kompetence (mshr)
  - Prasmes (mshr)
  - Nosaukumi (mshr)
  - Veterāna statuss (mshr)
  - Strādnieks (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Programmas atļauju piešķiršana Human Resources datiem

Otrā darbība ir nodrošināt, ka programmai tiek piešķirtas atbilstošas atļaujas Human Resources datiem, saistot to ar lietotāju programmā Human Resources. Programmas lietotājam servera-servera izsaukumi, izmantojot Dataverse virtuālās tabulas, tiek veikti lietotāja (programmas) identitātes kontekstā Dataverse, kas tiek atsaukta no darbības. Pēc tam virtuālās tabulas adaptera pakalpojums meklē saistīto lietotāju Human Resources un palaiž vaicājumu šī lietotāja kontekstā. Tas nozīmē, ka lietotājam jābūt izveidotam Human Resources kontā ar pareizām lomām, lai nodrošinātu piekļuvi datiem, kas nepieciešamas integrācijas programmai.

Human Resources lietotājam būs jāpiešķir arī pareizās atļaujas datiem Human Resources datos. Loma **Personāla atlases programma** (HcmRecruitingIntegrator) ir pieejama ar privilēģijām primārajām entītijām, kas nepieciešamas integrēšanai personāla atlases datos. Šo lomu var piešķirt programmas lietotājam lapā **Lietotāji**, lai piešķirtu atbilstošu piekļuvi datiem. Papildinformāciju par Human Resources drošības lomām skatiet sadaļā [Uz lomām balstīta drošība](/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Iestatīt jaunu lietotāju ar atbilstošām atļaujām

La iestatītu jaunu lietotāju ar atbilstošām atļaujām, veiciet šīs darbības:

  1. Atveriet lapu **Lietotājs** Human Resources un atlasiet **Jauns**.
  2. Ievadiet jaunā programmas lietotāja **Lietotāja ID** un **Lietotājvārdu**. Piemēram, varat ievadīt "RecruitingIntegration".

      > [!NOTE]
      > Ja programmā nav Microsoft Azure Active Directory (Azure AD) lietotāja konta vai e-pasta adreses, varat lietotāja e-pasta adresē un nodrošinātāja laukos ievietot kaut ko tādu kā "RecruitingApp".

  3. Kopsavilkuma cilnē **Lietotāja lomas** atlasiet darbību **Piešķirt lomas**.
  4. Rūtī **Piešķirt lomas lietotājam** atlasiet **Personāla atlases programma** un atlasiet **Labi**.
  5. Saglabāt jauno lietotāja ierakstu.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Saistīt jauno Human Resources lietotāju ar programmu

Pēc lietotāja izveides programmā ir jāizveido ieraksts formā **Azure Active Directory Programmas**, lai saistītu programmu ar Human Resources lietotāju.

  1. Atveriet formu **Azure Active Directory Programmas** un atlasiet **Jauns**.
  2. Laukā **Klienta ID** ievadiet programmai izveidotā programmas lietotāja klienta ID.
  3. Laukā **Nosaukums** ievadiet integrējošās lietojumprogrammas nosaukumu.
  4. Laukā **Lietotāja ID** atlasiet jauno personāla vadības lietotāju, kas izveidots personāla atlases integrācijai.
  5. Saglabāt jauno ierakstu.

Tad lietojumprogrammai būs piekļuve Human Resources datiem, kas ir ierobežoti tikai ar datiem, kas nepieciešami programmas integrācijas atlasei.

## <a name="see-also"></a>Skatiet arī

[Kandidātu pieņemšana darbā](hr-personnel-recruit.md)<br>
[Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Izmantot Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>
[Opciju kopu izveide un atjaunināšana, izmantojot Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
