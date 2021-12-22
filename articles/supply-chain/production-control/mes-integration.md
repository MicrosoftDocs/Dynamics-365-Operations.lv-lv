---
title: Integrācija ar trešās puses ražošanas izpildes sistēmām
description: Šajā tēmā ir paskaidrots, kā varat integrēt Microsoft Dynamics 365 Supply Chain Management ar trešās puses ražošanas izpildes sistēmu (MES).
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 43814023474d44b8c95bae087c7b6a4d52d21471
ms.sourcegitcommit: 7cbd53617af179a0de74aae30c149edc95e86684
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2021
ms.locfileid: "7891930"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integrācija ar trešās puses ražošanas izpildes sistēmām

[!include [banner](../includes/banner.md)]

Dažas ražošanas organizācijas, kas izmanto Dynamics 365 Supply Chain Management Microsoft, izmanto dynamics 365 vietējo funkcionalitāti, lai kontrolētu iekārtu, iekārtu un personāla ražošanas darbības. Tomēr citas ražošanas organizācijas, jo īpaši tās, kurām ir uzlabotas ražošanas prasības, tā vietā izmanto trešās puses ražošanas izpildes sistēmu (MES). Organizācijas var izvēlēties trešās puses MES risinājumu, jo, piemēram, tas ir īpaši pielāgots to vertikālajai nozarei.

Integrētajā risinājumā datu apmaiņa ir pilnībā automatizēta un notiek gandrīz reālā laikā. Tāpēc dati tiek uzturēti aktuāli abās sistēmās, un manuāla datu ievade nav nepieciešama. Piemēram, ja materiālu patēriņš ir reģistrēts TES, integrācija nodrošina, ka tāds pats patēriņš tiek reģistrēts arī Dynamics 365. Tāpēc atjauninātie krājumu ieraksti ir pieejami citiem svarīgiem procesiem, piemēram, plānošanai un pārdošanai.

Risinājums piegādes ķēdes pārvaldības lietotājiem nodrošina ātrāku, vienkāršāku un lētāku integrāciju ar trešo pušu TES. Tā piedāvā šādas funkcijas:

- Biznesa notikumi un saskarnes, kas atbalsta [galvenos ražošanas izpildes procesus](#processes-available-for-mes-integration)
- Centralizēts informācijas panelis, kurā var izsekot notikumu apstrādes vēsturei un novērst un novērst neizdoties procesus

Tālāk redzamajā attēlā ir parādīta tipiska biznesa notikumu, procesu un ziņojumu kolekcija, ar kuriem apmainās integrētā risinājumā.

![Tipisks integrācijas scenārijs.](media/3p-mes-scenario.png "Tipisks integrācijas scenārijs.")

## <a name="turn-on-the-mes-integration-feature"></a>TES integrācijas līdzekļa ieslēgšana

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Ražošanas kontrole*
- **Funkcijas nosaukums:** *Ražošanas izpildes sistēmas integrācija*

## <a name="processes-available-for-mes-integration"></a>TES integrācijai pieejamie procesi

Integrācijai var iespējot jebkuru vai visus tālāk norādītos procesus.

| Procesa Nosaukums | Apraksts |
|---|---|
| Nodot izpildei ražošanas pasūtījumus un ražošanas pasūtījuma statusu mainīt biznesa notikumus | Šis process nodrošina biznesa notikumu, ko TES var klausīties, lai iegūtu informāciju par ražošanas pasūtījumiem, kas būtu jāsagatavo. Atsauces datus, kas saistīti ar ražošanas pasūtījumu, paredzēts kopīgot no piegādes ķēdes pārvaldības uz TES, izmantojot atvērto datu protokolu (OData) vai datu entītijas. |
| Sākt ražošanas pasūtījumu | Šis process sniedz piegādes ķēdes pārvaldībai informāciju par ražošanas pasūtījumiem, kas tiek uzsākti, izmantojot TES. Tas nodrošina, ka abām sistēmām ir atjaunināts priekšstats par visām ražošanas darbībām. |
| Saražotais vai norakstītais daudzums | Šis process sniedz piegādes ķēdes vadībai informāciju par labajiem un kļūdu daudzumiem, kas tiek paziņoti ražošanas darbā, izmantojot TES. Tas nodrošina, ka ražotnes uzraugiem ir atjaunināts priekšstats par ražošanas plāna progresu. |
| Ziņot par materiālu patēriņu | Šis process sniedz piegādes ķēdes vadībai informāciju no TES par patērēto materiālu daudzumu. Tas padara atjauninātus krājumu ierakstus pieejamus citiem svarīgiem procesiem, piemēram, plānošanai un pārdošanai. |
| Pārskata laiks, kas patērēts operācijai | Šis process sniedz piegādes ķēdes pārvaldībai informāciju par laiku, kas tiek izmantots konkrētai operācijai. |
| Pārtraukt ražošanas pasūtījumu | Šis process informē piegādes ķēdes vadību, ka TES ir atjauninājusi ražošanas pasūtījumu līdz tā galīgajam statusam *Pabeigts*. Šis statuss norāda, ka ražošanas pasūtījumā vairs netiks saražoti daudzumi. |

## <a name="monitor-incoming-messages"></a>Ienākošo ziņojumu pārraudzība

Lai pārraudzītu sistēmā ienākošos ziņojumus, atveriet **ražošanas izpildes sistēmu integrācijas** lapu. Tur varat skatīt, apstrādāt un novērst problēmas.

## <a name="call-the-api"></a>Izsauciet API

Lai izsauktu MES integrācijas API, nosūtiet `POST` pieprasījumu uz šādu galapunkta URL:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Jūsu nosūtītā pieprasījuma pamattekstam vajadzētu līdzināties šim piemēram. Nomainiet `_companyId` vērtības `_messageType`, un pēc `_messageContent` vajadzības. Informāciju par dažādiem API atbalstītajiem ziņojumu tipiem un to satura noformēšanu skatiet nākamajā sadaļā.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API ziņojumu tipi un saturs

Šajā sadaļā ir aprakstīts katrs ziņojuma veids, ar kuru var apmainīties, izmantojot MES integrācijas API.

### <a name="start-production-order-message"></a>Sākt ražošanas pasūtījuma ziņojumu

Sākuma *ražošanas pasūtījuma* ziņojumam `_messageType` vērtība ir `ProdProductionOrderStart`. Šajā tabulā ir parādīti lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `StartedQuantity` | Neobligāti | Reāls |
| `StartedDate` | Neobligāti | Datums |
| `AutomaticBOMConsumptionRule` | Neobligāti | Uzskaitījums (FlushingPrincip \| always \| Never) |

### <a name="report-as-finished-message"></a>Ziņot kā pabeigtu ziņojumu

Pabeigtajam *ziņojumam vērtība ir*`_messageType``ProdProductionOrderReportFinished`. Šajā tabulā ir parādīti lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `ReportFinishedLines` | Obligāts | Rindu saraksts (vismaz viena), no kurām katrā ir nākamajā tabulā aprakstītā lietderīgā slodze |

Šajā tabulā ir parādīti lauki, kurus atbalsta katra `ReportFinishedLines` ziņojuma sadaļas `ProdProductionOrderReportFinished` rinda.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `LineNumber` | Neobligāti | Reāls |
| `ItemNumber` | Neobligāti | Virkne|
| `ProductionType` | Neobligāti | Uzskaitījums (MainItem \| formula BOM Co_Product By_Product \|\|\|\| None), paplašināms |
| `ReportedErrorQuantity` | Neobligāti | Reāls|
| `ReportedGoodQuantity` | Neobligāti | Reāls|
| `ReportedErrorCatchWeightQuantity` | Neobligāti | Reāls |
| `ReportedGoodCatchWeightQuantity` | Neobligāti | Reāls |
| `AcceptError` | Neobligāti |Būla |
| `ErrorCause` | Neobligāti | Uzskaitījums (None \| Material \| Machine \| OperatingStaff), paplašināms |
| `ExecutedDateTime` | Neobligāti | Datums un laiks |
| `ReportAsFinishedDate` | Neobligāti | Datums |
| `AutomaticBOMConsumptionRule` | Neobligāti | Uzskaitījums (FlushingPrincip \| always \| Never) |
| `AutomaticRouteConsumptionRule` | Neobligāti |Uzskaitījums (RouteDependent \| Always \| Never) |
| `RespectFlushingPrincipleDuringOverproduction` | Neobligāti | Būla |
| `ProductionJournalNameId` | Neobligāti | Virkne |
| `PickingListProductionJournalNameId` | Neobligāti | Virkne|
| `RouteCardProductionJournalNameId` | Neobligāti | Virkne |
| `FromOperationNumber` | Neobligāti | Vesels skaitlis|
| `ToOperationNumber` | Neobligāti | Vesels skaitlis|
| `InventoryLotId` | Neobligāti | Virkne |
| `BaseValue` | Neobligāti | Virkne |
| `EndJob` | Neobligāti | Būla |
| `EndPickingList` | Neobligāti | Būla |
| `EndRouteCard` | Neobligāti | Būla |
| `PostNow` | Neobligāti | Būla |
| `AutoUpdate` | Neobligāti | Būla |
| `ProductColorId` | Neobligāti | Virkne|
| `ProductConfigurationId` | Neobligāti | Virkne |
| `ProductSizeId` | Neobligāti | Virkne |
| `ProductStyleId` | Neobligāti | Virkne |
| `ProductVersionId` | Neobligāti | Virkne |
| `ItemBatchNumber` | Neobligāti | Virkne |
| `ProductSerialNumber` | Neobligāti | Virkne |
| `LicensePlateNumber` | Neobligāti | Virkne |
| `InventoryStatusId` | Neobligāti | Virkne |
| `ProductionWarehouseId` | Neobligāti | Virkne |
| `ProductionSiteId` | Neobligāti | Virkne |
| `ProductionWarehouseLocationId` | Neobligāti | Virkne |
| `InventoryDimension1` līdz `InventoryDimension12` | Neobligāti | Virkne |

12 paplašināmās dimensijas (`InventoryDimension1` līdz `InventoryDimension12`) ir jāpielāgo, un tās ne vienmēr tiek izmantotas. Plašāku informāciju par tiem skatiet [Add jaunu inventory dimensions through extension](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Materiālu patēriņa (izdošanas saraksta) ziņojums

Materiālu *patēriņa (izdošanas saraksta)* ziņojumam vērtība ir `_messageType``ProdProductionOrderPickingList`. Šajā tabulā ir parādīti lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `JournalNameId` | Neobligāti | Virkne |
| `PickingListLines` | Obligāts | Rindu saraksts (vismaz viena), no kurām katrā ir nākamajā tabulā aprakstītā lietderīgā slodze |

Šajā tabulā ir parādīti lauki, kurus atbalsta katra `PickingListLines` ziņojuma sadaļas `ProdProductionOrderPickingList` rinda.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ItemNumber` | Obligāts | Virkne |
| `ConsumptionBOMQuantity` | Neobligāti | Reāls |
| `ProposalBOMQuantity` | Neobligāti | Reāls |
| `ScrapBOMQuantity` | Neobligāti | Reāls |
| `BOMUnitSymbol` | Neobligāti | Virkne |
| `ConsumptionInventoryQuantity` | Neobligāti | Reāls |
| `ProposalInventoryQuantity` | Neobligāti | Reāls |
| `ConsumptionCatchWeightQuantity` | Neobligāti | Reāls |
| `ProposalCatchWeightQuantity` | Neobligāti | Reāls |
| `ConsumptionDate` | Neobligāti | Datums |
| `OperationNumber` | Neobligāti | Vesels skaitlis |
| `LineNumber` | Neobligāti | Reāls |
| `PositionNumber` | Neobligāti | Virkne |
| `IsConsumptionEnded` | Neobligāti | Būla |
| `ErrorCause` | Neobligāti | Uzskaitījums (None \| Material \| Machine \| OperatingStaff), paplašināms |

### <a name="time-used-for-operation-route-card-message"></a>Operācijas (maršruta kartes) ziņojumam izmantotais laiks

Operācijas *(maršruta kartes) ziņojumam izmantotajam laikam*`_messageType` vērtība ir `ProdProductionOrderRouteCard`. Šajā tabulā ir parādīti lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `JournalNameId` | Neobligāti | Virkne |
| `RouteCardLines` | Obligāts | Rindu saraksts (vismaz viena), no kurām katrā ir nākamajā tabulā aprakstītā lietderīgā slodze |

Šajā tabulā ir parādīti lauki, kurus atbalsta katra `RouteCardLines` ziņojuma sadaļas `ProdProductionOrderRouteCard` rinda.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `OperationNumber` | Obligāts | Vesels skaitlis |
| `OperationPriority` | Neobligāti | Uzskaitījums (Primary \| Secondary1 \| Secondary2 \| ... \| Sekundārais20) |
| `OperationId` | Neobligāti | Virkne |
| `OperationsResourceId` | Neobligāti | Virkne |
| `Worker` | Neobligāti | Virkne |
| `HoursRouteCostCategoryId` | Neobligāti | Virkne |
| `QuantityRouteCostCategoryId` | Neobligāti | Virkne |
| `HourlyRate` | Neobligāti | Reāls |
| `Hours` | Neobligāti | Reāls |
| `GoodQuantity` | Neobligāti | Reāls |
| `ErrorQuantity` | Neobligāti | Reāls |
| `CatchWeightGoodQuantity` | Neobligāti | Reāls |
| `CatchWeightErrorQuantity` | Neobligāti | Reāls |
| `QuantityPrice` | Neobligāti | Reāls |
| `ProcessingPercentage` | Neobligāti | Reāls |
| `ConsumptionDate` | Neobligāti | Datums |
| `TaskType` | Neobligāti | Uzskaitījums (QueueBefore \| setup process overlap transport \|\|\|\| queuePēc \| sloga) |
| `ErrorCause` | Neobligāti | Uzskaitījums (None \| Material \| Machine \| OperatingStaff), paplašināms |
| `OperationCompleted` | Neobligāti | Būla |
| `BOMConsumption` | Neobligāti | Būla |
| `ReportAsFinished` | Neobligāti | Būla |

### <a name="end-production-order-message"></a>Beigt ražošanas pasūtījuma ziņojumu

Beigu *ražošanas pasūtījuma* ziņojumam `_messageType` vērtība ir `ProdProductionOrderEnd`. Šajā tabulā ir parādīti lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `ExecutedDateTime` | Neobligāti | Datums un laiks |
| `EndedDate` | Neobligāti | Datums |
| `UseTimeAndAttendanceCost` | Neobligāti | Būla |
| `AutoReportAsFinished` | Neobligāti | Būla |
| `AutoUpdate` | Neobligāti | Būla |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Atsauksmju saņemšana par ziņojuma stāvokli

Pēc tam, kad TES ir nosūtījusi ziņojumu piegādes ķēdes pārvaldībai, piegādes ķēdes pārvaldībai varētu būt svarīgi atgriezt atsauksmes par ziņojuma stāvokli. Tālāk ir sniegti daži piemēri gadījumiem, kad šī darbība varētu būt svarīga.

- Nav nevienas personas, kas būtu atbildīga par PASTĀVĪGU TES integrācijas uzraudzību.
- Persona, kas ir atbildīga par TES integrācijas uzraudzību, vēlas saņemt paziņojumu pa e-pastu, ja ziņojums neizdodas, lai tā zinātu, ka tai ir jārīkojas.
- MES ir jāparāda kļūdas ziņojums, lai informētu ražotnes operatoru vai kādu no IT nodaļas darbinieku, ka viņiem ir jārīkojas.
- TES ir jāpārrēķina pasūtījumu grafiks pēc tam, kad tas ir saņēmis kļūmes ziņojumu (piemēram, tāpēc, ka neizdevās startēt ražošanas pasūtījumu).

Šādos gadījumos jūs varat izmantot standarta brīdinājuma funkciju piegādes ķēdes pārvaldībā. Informāciju par to, kā darbojas standarta brīdinājumi, skatiet šādos resursos:

- Palīdzības tēma: [Brīdinājumu pārskats](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [brīdinājuma noteikumu opcijas Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Piemēram, varat iestatīt šādus brīdinājumus, lai sniegtu atsauksmes par ziņojuma stāvokli:

- Izveidojiet biznesa notikumu ("Sūtīt ārēji"), kas tiek izmantots, ja ziņojums nav *izdevies*.
- Nosūtiet paziņojumu un e-pastu IT administratoram vai ražošanas stāvu pārvaldniekam.
