---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 9. jūlijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b3eb53943546166eee845749a070ed2fca1a03b8
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023957"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 9. jūlijs)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Drīzumā risinājumā Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Darbu apstiprinājumu rādīšana sākumlapā

Apstiprinājumi tiek rādīti informācijas paneļa sadaļā **Apstiprinājumi**. Apstiprinātāji var pārskatīt savus apstiprinājumus sadaļā **Piešķirts jums**, kur ir norādīts darba ID, amata nosaukums, citi apstiprinātāji un datums, kad šis darbs tika piešķirts. Lietotāji, kuri iesniedz darbu apstiprināšanai, var pārskatīt savus darbus sadaļā **Jūsu pieprasījumi**, kur ir norādīti apstiprinātāji, kam šis iesniegtais darbs joprojām ir jāapstiprina.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Finance and Operations Platform update 28

Papildinformāciju par atjauninājumu Finance and Operations Platform update 28 skatiet rakstā [Priekšskatījuma līdzekļi Dynamics 365 Finance and Operations Platform update 28 (2019. gada jūlijs)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Elementu atbalsts pielāgotajiem laukiem Common Data Service 

Tālāk norādītie elementi atbalsta pielāgotus laukus. 

- **Atlīdzības fiksētā sistēma**
- **Atlīdzības atsauces punktu iestatīšana**
- **Atlīdzības atsauces punktu iestatīšanas līnija**
- **Algas ienākumu veida kods**
- **Apmaksas periods**
- **Fiksētas atlīdzības notikums**
- **Atlīdzību režģis**

Lai skatītu visus atjauninātos elementus programmā Talent, veiciet tālāk norādītās darbības.

1. Atlasiet **Sistēmas administrēšana**, atlasiet **Saites** un pēc tam atlasiet **Common Data Service konfigurācija**.
2. Atlasiet nolaižamo izvēlni **CDS elementa nosaukums**. Visi uzskaitītie elementi ir iekļauti jaunākajā versijā. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Pilns vārds, ko pievieno elementam Darbinieks Common Data Service

Elementam **Darbinieks** ir pievienots lauks **Pilns vārds**.

### <a name="full-time-equivalent-higher-than-10"></a>Pilna laika ekvivalents, kas lielāks par 1,0

Tagad tiek parādīts brīdinājums, ja pilna laika darbiniekam amatā tiek ievadīta vērtība, kas ir lielāka par 1,0. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Brīdinājums vairs netiek rādīts darbinieku lapā, ja nav nodarbinātības ar nākotnes datumu

Jūs vairs nesaņemsit ziņojumu, kas norāda, ka pastāv nākotnes darbs, naviģējot uz lapu **Darbinieks** no saraksta **Esošie darbinieki** darbvietā **Personāla vadība**. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Nevar dzēst biznesa procesu programmā Talent

Tagad varat dzēst biznesa procesu darbvietā **Biznesa process**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Atvaļinājuma bilance vairs nerāda nulli plāniem bez uzkrājumiem, izmantojot bilanci kā uzkrāšanas periodu

Plāni, kas ir iestatīti bez uzkrājumiem, tagad var rādīt bilanci.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Priekšskatījuma līdzekļi ir iespējoti tikai smilškastes instancēs

Kad nodrošināt jaunu Talent instanci, varat norādīt, vai šīs instances tips ir **Ražošana** vai **Smilškaste**. Instances, kuru tips ir **Smilškaste**, ļauj agri testēt jaunos līdzekļus. Visas esošās programmas Talent instances tiks atjauninātas uz instances tipu **Ražošana**. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu **Smilškaste**, sazinieties ar [atbalsta dienestu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), lai sāktu izmaiņu pieprasījumu.

Papildinformāciju par to, kā tiek publicētas izmaiņas, skatiet tēmā [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Atvaļinājumu tipu ierobežošana brīvā laika pieprasījumos

Organizācijas var piedāvāt darbiniekiem daudz dažādus atvaļinājumu tipus. Taču daži brīvā laika pieprasījumu atvaļinājumu tipi var nebūt piemēroti tam, lai tos iesniegtu darbinieki. Tā vietā šos atvaļinājumu tipus var pārvaldīt personāla vadība (HR). Šajā laidienā jūs varat konfigurēt, kuriem atvaļinājumu tipiem darbinieki var iesniegt brīvā laika pieprasījumus. 

## <a name="coming-soon-in-core-hr"></a>Drīzumā programmā Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Paplašinātas informācijas skatīšana par veiktspēju vadītāja patstāvīgi lietojamajā pakalpojumā

Jauna opcija ļaus vadītājiem apskatīt gan savas tiešās veiktspējas atskaites, gan izvērstās atskaites. Pašlaik rindu pārvaldnieki var piešķirt un atjaunināt veiktspējas mērķus un izdot jaunus pārskatus, kuru pārvaldīšanā ir jāpiedalās viņu darbiniekiem. Turklāt tiešie vadītāji un viņu darbinieki var uzturēt un atjaunināt veiktspējas žurnālus, lai palīdzētu nodrošināt, ka veiktspējas pārskatīšanas process norit raiti. Kad šīs izmaiņas būs ieviestas, papildus savām tiešajām atskaitēm pārvaldnieki varēs skatīt un uzturēt ar veiktspēju saistītu informāciju par savām izvērstajām atskaitēm. 

### <a name="entities-supporting-custom-fields"></a>Elementi, kas atbalsta pielāgotos laukus

Pielāgotajiem laukiem tiks iespējoti tālāk norādītie elementi Common Data Service. 

- **Atvaļinājuma tips**
- **Nodarbinātā bankas konts**
- **Darba kalendārs**
