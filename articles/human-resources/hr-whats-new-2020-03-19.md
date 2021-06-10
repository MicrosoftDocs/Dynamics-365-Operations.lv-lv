---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 19. marts)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 19. martu.
author: andreabichsel
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2882eca5c0823d413ca3242069c5ba47b985c2a8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051165"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 19. marts)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3014. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta atsauces numuriem portālā Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Human Resources vides ierobežojumi tagad ir balstīti atjauninātajā licencēšanā (394595)

Ir mainīt limits vižu skaitam projektā pakalpojumos Lifecycle Services (LCS). Iepriekšējais ierobežojums bija divas vides. Ražošanas un smilškastes vides skaita ierobežojums, ko var izveidot programmai Human Resources pakalpojumā LCS, tagad ir balstīts atjauninātajā licencēšanā. Tagad ir iespējams izveidot tik daudz vides, cik nepieciešams, katram LCS projektam atkarībā no iegādāto licenču skaita. Jaunā licencēšana, kas atjaunināta 2020. gada 1. februārī, ļauj klientiem iegādāties papildu vides. Plašāku informāciju par licencēšanas prasībām papildu vidēm skatiet [Dynamics 365 licencēšanas rokasgrāmatā](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Nodrošināt atlīdzības datu starpuzņēmumu apskati darbiniekiem un vadītājiem (403904)

**Līdzekļu pārvaldības** darbvietā aktivizējiet šo līdzekli. Lai iegūtu papildinformāciju, skatiet sadaļu [Priekšskatījuma līdzekļu iespējošana vai atspējošana](hr-admin-manage-features.md#enable-or-disable-preview-features).

Iespējojot šo līdzekli, vadītāji var redzēt tiešu un paplašinātu pārskatu atlīdzināšanu bez nepieciešamības pieteikties darba uzņēmumā. Pilna atlīdzības vēsture ir pieejama no jebkura pieteikta uzņēmuma, kura vadītājam ir piekļuve. Papildinformāciju skatiet sadaļā [Darbinieka un vadītāja pašapkalpošanās pārskats](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Iespējot globālās adrešu grāmatas sapludināšanas funkcionalitāti (427189)

Tagad varat sapludināt adrešu grāmatas dublikātus, atlasot ierakstu dublikātus un **Globālās adrešu grāmatas** lapā atlasot **Sapludināt**.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Nevar pielāgot atlikuma bilanci plānam bez uzkrājumiem, kas tika izveidots ar vairāku atvaļinājumu veidu funkciju (419635)

Tagad varat pielāgot bilances atvaļinājumu plāniem, kas tika izveidoti ar priekšskatījuma līdzekli **Vairāki atvaļinājumu veidi**, kas izveidots Līdzekļu pārvaldībā.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>Primārās pozīcijas lauks elementā WorkerPositionAssignmentEntity, kad darbinieks ir pārtraucis darbu (420774)

Darbiniekiem, kam ir izbeigta nodarbinātība, entitījā tiek parādīts primārais amats, kas bija aktīvs darba attiecību pārtraukšanas laikā. Attiecībā uz integrācijām darbinieka nodarbinātības amata piešķiršanai vairs netiks izveidots dublikāta ieraksts. 

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse risinājums tagad ir pieejams ar šādām izmaiņām:

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
| Jauna **Nosaukuma** entitīja | <ul><li>**Nosaukums** pievienots</li></ul>Jaunā **Nosaukuma** entītija ir iekļauta Dataverse, bet šajā laikā nav atsauces no **Darba amata** vai **Darba** vienībām. |

> [!NOTE]
> Finanšu dimensijas abām pozīcijām un nodarbinātībai nodrošina viena virziena integrēšanu personāla vadības resursu atjauninājumiem Dataverse. Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Dataverse uz personāla vadības resursiem.

Nākamo dažu nedēļu laikā šīs elementa izmaiņas būs pieejamas visās vidēs. Lai manuāli instalētu jaunāko Dataverse risinājumu Personāla vadībai:

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

### <a name="platform-update-33"></a>Platformas update 33

- Pilnas lapas lietojumprogrammas (priekšskatījums) - Šī priekšskatījuma funkcija, kas paredz saglabāto skatu funkcijas iespējošanu, ļauj Power Apps un trešo pušu programmas pievienot kā pilnas lapas programmas, izmantojot informācijas paneli.

- Saglabātie skati (priekšskatījums) — Šis priekšskatījuma līdzeklis iespējo saglabātos skatījumus, kas ir nozīmīgs personalizēšanas apakšsistēmas papildinājums. Šis līdzeklis ļauj lietotājiem iegūt vairākas nosauktas personalizācijas kopas uz lapu. Varat arī publicēt skatus uz drošības lomām.

- Optimizēta ¨ir viens no¨ filtrēšanas iespēja - Šī funkcija ļauj optimizētu "ir viens no" filtrēšanas iespēju, kas atvieglo vairāku filtru vērtību ievadīšanu. Tai ir vienkāršāks individuālo vai visu filtru vērtību noņemšanas mehānisms, kā arī filtra vērtību vizualizācija ir kompaktāka un intuitīvāka.

- Ieteicamie lauki — Lietotājiem bieži ir jāpievieno lauki režģim vai lapai. Tas var būt sarežģīti ar tik daudziem pieejamiem laukiem. Tā vietā, lai meklētu pēc liela saraksta, šis līdzeklis ļauj sistēmai pāriet pāri ieteicamo lauku kopai, pamatojoties uz to, ko citi lietotāji visbiežāk pievieno līdzīgos scenārijos.

- Sticky noklusējuma darbības režģos - Šī funkcija nodrošina, ka noklusējuma darbība režģī tiek sasaistīta ar konkrētu kolonnu režģī neatkarīgi no tā, vai šī kolonna tiek pārvietota vai paslēpta.

## <a name="new-production-release-cadence"></a>Jauns ražošanas laidiena ritms

No aprīļa Human Resources laidienu ritms mainīsies no iknedēļas atjauninājumiem uz atjauninājumiem reizi divās nedēļās. Tas nodrošinās saskaņošanu ar drošu izvietošanas praksi un uzturēs augstas stabilitātes un uzticamības standartus pakalpojumā. Mēs ieviešam papildu pārbaudes un uzraudzību, lai nodrošinātu veiksmīgu izvietošanu katrā procesa posmā. Lai iegūtu papildu informāciju par laidiena ritmu skatiet rakstu [Atjaunināšanas process](hr-admin-setup-update-process.md).

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie priekšskatījuma līdzekļi ir pieejami 2020. gada 3. februārī:

- **Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi** – Papildu informāciju skatiet [Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Atvieglojumu pārvaldības priekšskatījums** — plašāku informāciju, ieskaitot zināmās problēmas, skatiet [Atvieglojumu pārvaldības apskatā](hr-benefits-management-overview.md).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]