---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 24. marts)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 83f24dd6f094715f96666c3ae94faa4bdb97a652
ms.sourcegitcommit: fac1d519a85eab0c936b54e0a9247f6a11842871
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2020
ms.locfileid: "3177941"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 24. marts)

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3073. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta atsauces numuriem portālā Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Human Resources vides ierobežojumi tagad ir balstīti atjauninātajā licencēšanā (394595)

Ir mainīt limits vižu skaitam projektā pakalpojumos Lifecycle Services (LCS). Iepriekšējais ierobežojums bija divas vides. Ražošanas un smilškastes vides skaita ierobežojums, ko var izveidot programmai Human Resources pakalpojumā LCS, tagad ir balstīts atjauninātajā licencēšanā. Tagad ir iespējams izveidot tik daudz vides, cik nepieciešams, katram LCS projektam atkarībā no iegādāto licenču skaita. Jaunā licencēšana, kas atjaunināta 2020. gada 1. februārī, ļauj klientiem iegādāties papildu vides. Plašāku informāciju par licencēšanas prasībām papildu vidēm skatiet [Dynamics 365 licencēšanas rokasgrāmatā](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="platform-changes"></a>Platformas izmaiņas

- Pilnas lapas lietojumprogrammas (priekšskatījums) - Šī priekšskatījuma funkcija, kas paredz saglabāto skatu funkcijas iespējošanu, ļauj Power Apps un trešo pušu programmas pievienot kā pilnas lapas programmas, izmantojot informācijas paneli. 

- Saglabātie skati (priekšskatījums) — Šis priekšskatījuma līdzeklis iespējo saglabātos skatījumus, kas ir nozīmīgs personalizēšanas apakšsistēmas papildinājums. Šis līdzeklis ļauj lietotājiem iegūt vairākas nosauktas personalizācijas kopas uz lapu. Varat arī publicēt skatus uz drošības lomām.

- Optimizēta ¨ir viens no¨ filtrēšanas iespēja - Šī funkcija ļauj optimizētu "ir viens no" filtrēšanas iespēju, kas atvieglo vairāku filtru vērtību ievadīšanu. Tai ir vienkāršāks individuālo vai visu filtru vērtību noņemšanas mehānisms, kā arī filtra vērtību vizualizācija ir kompaktāka un intuitīvāka. 

- Ieteicamie lauki — Lietotājiem bieži ir jāpievieno lauki režģim vai lapai. Tas var būt sarežģīti ar tik daudziem pieejamiem laukiem. Tā vietā, lai meklētu pēc liela saraksta, šis līdzeklis ļauj sistēmai pāriet pāri ieteicamo lauku kopai, pamatojoties uz to, ko citi lietotāji visbiežāk pievieno līdzīgos scenārijos.

- Sticky noklusējuma darbības režģos - Šī funkcija nodrošina, ka noklusējuma darbība režģī tiek sasaistīta ar konkrētu kolonnu režģī neatkarīgi no tā, vai šī kolonna tiek pārvietota vai paslēpta.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>Nevar pielāgot atlikuma bilanci plānam bez uzkrājumiem, kas tika izveidots ar "vairāku atvaļinājumu veidu" funkciju (419635)

Ar šīm izmaiņām jūs varat pielāgot bilances atvaļinājumu plāniem, kas ir izveidotas ar priekšskatījuma Vairāku atvaļinājumu veidu (priekšskatījums) līdzekli, kas iespējots līdzekļu pārvaldībā.

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie priekšskatījuma līdzekļi kļuva pieejami 2020. gada 3. februārī:

- **Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi** – Papildu informāciju skatiet [Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Atvieglojumu pārvaldības priekšskatījums** — plašāku informāciju, ieskaitot zināmās problēmas, skatiet [Atvieglojumu pārvaldības apskatā](hr-benefits-management-overview.md).

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service risinājums tagad ir pieejams ar šādām izmaiņām:

| apraksts | Labot |
| --- | --- |
| **Darba/amata** elementa izmaiņas | <ul><li>**Kompensācijas reģions** pievienots</li>|
| **Darba amata dimensijas** pievienotais elements | <ul><li>**Finanšu dimensijas** pievienotas</li>
| **Darbinieka** elementa izmaiņas | <ul><li>**Vārdu secība** pievienota</li><li>**Darbi no mājām** pievienoti</li><li>**Valoda** pievienota</li><li>**Darba stāža datums** pievienots</li><li>**Gadadienas datums** pievienots</li><li>**Sākotnējais darbā pieņemšanas datums** pievienots</li></ul> |
| **Nodarbinātības** elementa izmaiņas | <ul><li>**Finanšu dimensijas** pievienotas</li><li>**Darba attiecību pārtraukšanas pamatojums** pievienots</li><li>**Beigu datums** pārdēvēts no **Pārejas datuma**</li><li>**Probācijas datums** pievienots</li></ul> |
| **Darbinieka adreses** elementa izmaiņas | <ul><li>**Adrese** pievienota</li><li>**1. adreses rinda**, **2. adreses rinda** un **3. adreses rinda** atzīmēta norakstīšanai</li></ul> |
| Jaunas mainīgās atlīdzības iestatījuma entitījas | <ul><li>**Atlīdzības mainīgā plāna tips**</li><li>**Atlīdzības mainīgā sistēma**</li><li>**Izmaksas noteikumi**</li><li>**Atlīdzības mainīgā plāna līmenis**</li></ul> |
| Jauna **Darbinieka kalendāra nodarbinātības** entitīja | <ul><li>**Darba kalendāra elements** pievienots</li></ul> |
| Jauna **Algas pozīcijas detalizētas informācijas** entitīja | <ul><li>**Algas pozīcijas detalizēta informācija** pievienota</li></ul> |
| Jauna **Nosaukuma** entitīja | <ul><li>**Nosaukums** pievienots</li></ul>Jaunā **Nosaukuma** entītija ir iekļauta Common Data Service, bet šajā laikā nav atsauces no **Darba amata** vai **Darba** vienībām. |

> [!NOTE]
> Finanšu dimensijas abām pozīcijām un nodarbinātībai nodrošina viena virziena integrēšanu personāla vadības resursu atjauninājumiem Common Data Service. Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Common Data Service uz personāla vadības resursiem.

Nākamo dažu nedēļu laikā šīs elementa izmaiņas būs pieejamas visās vidēs. Lai manuāli instalētu jaunāko Common Data Service risinājumu Personāla vadībai:

1.  Dodieties uz [Power Platform Administrēšanas centru](https://admin.powerplatform.microsoft.com).

2.  Atlasiet **Vides**.

3.  Sameklējiet vidi, ko vēlaties atjaunināt. Apkārtējai videi ir jāatbilst **Vides nosaukumam** **Common Data Service informācijas** sadaļā, kas atrodas sadaļā **Par** personāla vadības veidlapā.

4.  Atlasiet vidi, lai skatītu vides informāciju.

5.  Darbību joslas augšdaļā atlasiet pogu **Pārvaldīt risinājumus**. Tiks atvērts jauns pārlūkprogrammas logs un navigēs uz **Dynamics 365 administrēšanas centru** vides kontekstā.

6.  **Risinājumu** sarakstā atlasiet **Dynamics 365 Human Resources enkurs**.

7.  Atlasiet **Atjaunināt**, lai izmantotu jaunāko risinājumu.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint priekšskatījums dažās vidēs nedarbojas

Ja dokumenta priekšskatījums dokumentiem, kas saglabāti SharePoint programmā, nedarbojas, veiciet šādas darbības:

1. Pārbaudiet, vai administratora lietotāja kontam ir e-pasts, kas saistīts ar lietotāja ierakstu. Šo informāciju varat aplūkot lapā **Lietotājs**. Ja e-pasta ziņojums nav iestatīts, e-pasta ziņojums un nodrošinātājs ir jāpievieno, izmantojot OData Excel pievienojumprogrammu. Pēc noklusējuma e-pasta adrese nav atrodama Excel noformējumā. Jums vajadzēs rediģēt Excel noformējumu, pievienot visus laukus, piemērot un atsvaidzināt. Kad šīs darbības ir izpildītas, varat atjaunināt administratora kontu.

2. Pēc tam, kad administratora kontam ir saistītais e-pasta konts, piesakieties pakalpojumā Human Resources ar administratora akreditācijas datiem.

3. Lai sāktu dokumenta priekšskatījumu, piekļūstiet SharePoint pielikumam.

4. Piesakieties ar citu lietotāja kontu, kam ir piekļuve pielikumiem, un apstipriniet, ka priekšskatījums darbojas kā paredzēts.

## <a name="coming-soon"></a>Drīzumā

## <a name="new-production-release-cadence"></a>Jauns ražošanas laidiena ritms

No aprīļa Personāla vadības laidienu ritms mainīsies no iknedēļas atjauninājumiem uz atjauninājumiem reizi divās nedēļās. Lai nodrošinātu saskaņotību ar drošām izvietošanas praksēm, kā arī uzturētu augstus stabilitātes un uzticamības standartus pakalpojumā, pakalpojumu atjauninājumu izvietošanas process visiem reģioniem būs divu nedēļu izvēršana. Būs paredzēta papildu pārbaudes un uzraudzība, lai nodrošinātu veiksmīgu izvietošanu katrā procesa posmā. Lai iegūtu papildu informāciju par laidiena ritmu skatiet rakstu [Atjaunināšanas process](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Zināmās problēmas

## <a name="employment-detail-entity"></a>Nodarbinātības informācijas elements

**Nodarbinātības informācijas** entītija ir atjaunināta ar šādiem laukiem: **PayFrequency**, **Nodarbinātības kategorijas ID**, **Nodarbinātības veids**, **EmploymentType ID** un **Atvieglojumu nodarbinātības statuss**. Šo lauku iestatīšanas dati paļaujas uz atvieglojumu pārvaldību, kas ir iespējota Līdzekļu pārvaldībā. Šos laukus nedrīkst aizpildīt vai atjaunināt **Nodarbinātības informācijas** entītijā, jo importēšanas laikā radīsies kļūdas.