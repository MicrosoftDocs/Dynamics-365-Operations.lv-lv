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
ms.openlocfilehash: 8917c9b265bc3df19517f052e28fb7644057cb46
ms.sourcegitcommit: 19f0e69a131e9e4ff680eac13efa51b04ad55a38
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/22/2022
ms.locfileid: "8330705"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integrācija ar trešās puses ražošanas izpildes sistēmām

[!include [banner](../includes/banner.md)]

Dažas ražošanas organizācijas, kas izmanto Microsoft Dynamics 365 Supply Chain Management, izmanto Dynamics 365 vietējo funkcionalitāti, lai kontrolētu savas ražošanas darbības mašīnām, iekārtām un personālam. Tomēr citas ražošanas organizācijas, jo īpaši tās, kurām ir uzlabotas ražošanas prasības, tā vietā izmanto trešās puses ražošanas izpildes sistēmu (MES). Organizācijas var izvēlēties trešās puses MES risinājumu, jo, piemēram, tas ir īpaši pielāgots to vertikālajai nozarei.

Integrētajā risinājumā datu apmaiņa ir pilnībā automatizēta un notiek gandrīz reālā laikā. Tāpēc dati tiek uzturēti aktuāli abās sistēmās, un nav nepieciešama manuāla datu ievadīšana. Piemēram, ja materiālu patēriņš ir reģistrēts TES, integrācija nodrošina, ka tāds pats patēriņš tiek reģistrēts arī dynamics 365. Tāpēc jaunākie krājumu ieraksti ir pieejami citiem svarīgiem procesiem, piemēram, plānošanai un pārdošanai.

Risinājums padara piegādes ķēdes pārvaldības lietotājiem ātrāku, vieglāku un lētāku integrāciju ar trešo pušu TES. Tas piedāvā šādas funkcijas:

- Biznesa notikumi un saskarnes, kas atbalsta [galvenos ražošanas izpildes procesus](#processes-available-for-mes-integration)
- Centralizēts informācijas panelis, kurā varat izsekot notikumu apstrādes vēsturi un novērst un novērst kļūmes procesus, kas neizdodas

Tālāk redzamajā attēlā ir parādīta tipiska biznesa notikumu, procesu un ziņojumu kolekcija, ar kuriem notiek apmaiņa integrētā risinājumā.

![Tipisks integrācijas scenārijs.](media/3p-mes-scenario.png "Tipisks integrācijas scenārijs.")

## <a name="turn-on-the-mes-integration-feature"></a>MES integrācijas līdzekļa ieslēgšana

Lai varētu izmantot šo līdzekli, administratoram tas ir jāieslēdz jūsu sistēmā, kā aprakstīts tālāk.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
1. Pārliecinieties, **vai ir aktivizēta atslēga Laika un apmeklētības** licence (tiek parādīta atzīme). Šī licences atslēga ir nepieciešama, jo tā kontrolē ražošanas izpildes sistēmas funkcionalitāti un datus. Ja tas nav iespējots, veiciet tālāk norādītās darbības.
    1. Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
    1. Lapā Licences konfigurācija **atzīmējiet** izvēles rūtiņu Laiks un apmeklētība **.**
    1. Tehniskās apkopes režīma izslēgšana, kā aprakstīts [apkopes režīmā](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)
1. Dodieties uz **sistēmas administrēšanas \> darbvietu \> līdzekļu pārvaldību**.
1. Ieslēdziet funkciju, kas ir norādīta tālāk norādītajā veidā (skatiet arī [līdzekļu pārvaldības pārskatu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)):
    - **Modulis:** *Ražošanas kontrole*
    - **Funkcijas nosaukums:** *Ražošanas izpildes sistēmas integrācija*

## <a name="processes-available-for-mes-integration"></a>MES integrācijai pieejamie procesi

Integrācijas procesam var iespējot jebkuru vai visus no šiem procesiem.

| Procesa Nosaukums | Apraksts |
|---|---|
| Nodot ražošanas pasūtījumus un ražošanas pasūtījuma statusa izmaiņu biznesa notikumus | Šis process nodrošina biznesa notikumu, ko TES var noklausīties, lai iegūtu informāciju par ražošanas pasūtījumiem, kas būtu jāsagatavo. Paredzams, ka atsauces dati, kas ir saistīti ar ražošanas pasūtījumu, tiks kopīgoti no piegādes ķēdes pārvaldības uz TES, izmantojot atvērto datu protokolu (OData) vai datu entītijas. |
| Sākt ražošanas pasūtījumu | Šis process nodrošina piegādes ķēdes pārvaldību ar informāciju par ražošanas pasūtījumiem, kas tiek sākti, izmantojot TES. Tas nodrošina, ka abām sistēmām ir atjaunināts pārskats par visām ražošanas darbībām. |
| Pārskats par saražoto vai norakstīto daudzumu | Šis process nodrošina piegādes ķēdes pārvaldību ar informāciju par labajiem un kļūdu daudzumiem, par kuriem tiek ziņots ražošanas darbā, izmantojot TES. Tas nodrošina, ka ražotnes uzraugiem ir aktuāls pārskats par ražošanas plāna norisi. |
| Ziņot par materiālu patēriņu | Šis process sniedz piegādes ķēdes pārvaldībai informāciju no TES par patērēto materiālu daudzumu. Tas veido atjauninātus krājumu ierakstus, kas pieejami citiem svarīgiem procesiem, piemēram, plānošanai un pārdošanai. |
| Atskaite par operācijai patērēto laiku | Šis process sniedz piegādes ķēdes pārvaldībai informāciju par laiku, kas tiek izmantots konkrētai operācijai. |
| Pārtraukt ražošanas pasūtījumu | Šis process informē piegādes ķēdes pārvaldību, ka TES ir atjauninājis ražošanas pasūtījumu līdz galīgajam statusam *Pabeigts*. Šis statuss norāda, ka ražošanas pasūtījumā vairs netiks saražoti daudzumi. |

## <a name="monitor-incoming-messages"></a>Ienākošo ziņojumu pārraudzība

Lai pārraudzītu sistēmā ienākošos ziņojumus, atveriet **ražošanas izpildes sistēmu integrācijas** lapu. Tur varat skatīt, apstrādāt un novērst problēmas.

## <a name="call-the-api"></a>Zvaniet uz API

Lai izsauktu MES integrācijas API, nosūtiet `POST` pieprasījumu uz šādu galapunkta URL:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Jūsu nosūtītā pieprasījuma pamattekstam ir jālīdzinās šim piemēram. Pēc vajadzības nomainiet vērtības `_companyId``_messageType``_messageContent`. Informāciju par dažādiem ziņojumu tipiem, ko api atbalsta, un to, kā noformēt to saturu, skatiet nākamajā sadaļā.

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

Šajā sadaļā aprakstīts katra veida ziņojums, ar kuru var apmainīties, izmantojot MES integrācijas API.

### <a name="start-production-order-message"></a>Sākt ražošanas pasūtījuma ziņojumu

*Sākuma ražošanas pasūtījuma* ziņojumam `_messageType` vērtība ir `ProdProductionOrderStart`. Šajā tabulā ir parādīti šī ziņojuma atbalstītie lauki.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `StartedQuantity` | Neobligāti | Reāls |
| `StartedDate` | Neobligāti | Datums |
| `AutomaticBOMConsumptionRule` | Neobligāti | Uzskaitījums (FlushingPrincip \| vienmēr \| nekad) |

### <a name="report-as-finished-message"></a>Ziņot par pabeigtu ziņojumu

Pabeigtam *ziņojumam*`_messageType` vērtība ir `ProdProductionOrderReportFinished`. Šajā tabulā ir parādīti šī ziņojuma atbalstītie lauki.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `ReportFinishedLines` | Obligāts | Rindu saraksts (vismaz viena), no kurām katrā ir nākamajā tabulā aprakstītā kravnesība |

Šajā tabulā ir parādīti lauki, kurus atbalsta katra ziņojuma sadaļas `ReportFinishedLines` rindiņa `ProdProductionOrderReportFinished`.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `LineNumber` | Neobligāti | Reāls |
| `ItemNumber` | Neobligāti | Virkne|
| `ProductionType` | Neobligāti | Uzskaitījums (MainItem \| Formula \| BOM \| Co_Product \| By_Product \| Nav), paplašināms |
| `ReportedErrorQuantity` | Neobligāti | Reāls|
| `ReportedGoodQuantity` | Neobligāti | Reāls|
| `ReportedErrorCatchWeightQuantity` | Neobligāti | Reāls |
| `ReportedGoodCatchWeightQuantity` | Neobligāti | Reāls |
| `AcceptError` | Neobligāti |Būla |
| `ErrorCause` | Neobligāti | Uzskaitījums (None \| Material \| Machine \| OperatingStaff), paplašināms |
| `ExecutedDateTime` | Neobligāti | Datums un laiks |
| `ReportAsFinishedDate` | Neobligāti | Datums |
| `AutomaticBOMConsumptionRule` | Neobligāti | Uzskaitījums (FlushingPrincip \| vienmēr \| nekad) |
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

12 paplašināmajām dimensijām (`InventoryDimension1` līdz `InventoryDimension12`) ir nepieciešama pielāgošana, un tās ne vienmēr tiek izmantotas. Papildinformāciju par tām skatiet sadaļā Jaunu [krājumu dimensiju pievienošana, izmantojot paplašinājumu](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Materiālu patēriņa (izdošanas saraksta) ziņojums

Materiālu patēriņa *(izdošanas saraksta) ziņojumam* vērtība `_messageType` ir `ProdProductionOrderPickingList`. Šajā tabulā ir parādīti šī ziņojuma atbalstītie lauki.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `JournalNameId` | Neobligāti | Virkne |
| `PickingListLines` | Obligāts | Rindu saraksts (vismaz viena), no kurām katrā ir nākamajā tabulā aprakstītā kravnesība |

Šajā tabulā ir parādīti lauki, kurus katra rinda `PickingListLines` ziņojuma sadaļā `ProdProductionOrderPickingList` atbalsta.

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
| `InventoryLotId` | Neobligāti | Virkne |

### <a name="time-used-for-operation-route-card-message"></a>Operācijas (maršruta kartes) ziņojuma laiks

*Operācijas (maršruta kartes) ziņojumam izmantotais* laiks ir `_messageType` vērtība `ProdProductionOrderRouteCard`. Šajā tabulā ir parādīti šī ziņojuma atbalstītie lauki.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `JournalNameId` | Neobligāti | Virkne |
| `RouteCardLines` | Obligāts | Rindu saraksts (vismaz viena), no kurām katrā ir nākamajā tabulā aprakstītā kravnesība |

Šajā tabulā ir parādīti lauki, kurus katra rinda `RouteCardLines` ziņojuma sadaļā `ProdProductionOrderRouteCard` atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `OperationNumber` | Obligāts | Vesels skaitlis |
| `OperationPriority` | Neobligāti | Uzskaitījums (primārais \| Secondary1 \| Secondary2 \| ... \| Sekundārais20) |
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
| `TaskType` | Neobligāti | Uzskaitījums (QueueBefore Iestatīšanas \|\| procesa pārklāšanās \| transports \|\| QueueAfter slogs \|) |
| `ErrorCause` | Neobligāti | Uzskaitījums (None \| Material \| Machine \| OperatingStaff), paplašināms |
| `OperationCompleted` | Neobligāti | Būla |
| `BOMConsumption` | Neobligāti | Būla |
| `ReportAsFinished` | Neobligāti | Būla |

### <a name="end-production-order-message"></a>Pārtraukt ražošanas pasūtījuma ziņojumu

*Beigu ražošanas pasūtījuma ziņojumam* ir `_messageType` vērtība `ProdProductionOrderEnd`. Šajā tabulā ir parādīti šī ziņojuma atbalstītie lauki.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `ExecutedDateTime` | Neobligāti | Datums un laiks |
| `EndedDate` | Neobligāti | Datums |
| `UseTimeAndAttendanceCost` | Neobligāti | Būla |
| `AutoReportAsFinished` | Neobligāti | Būla |
| `AutoUpdate` | Neobligāti | Būla |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Saņemt atsauksmi par ziņojuma stāvokli

Kad MES ir nosūtījis ziņojumu Piegādes ķēžu pārvaldībai, iespējams, ka tas būs svarīgi Piegādes ķēžu pārvaldībai, lai atgrieztu atsauksmes par ziņojuma stāvokli. Šeit sniegti daži piemēri par gadījumiem, kad šī uzvedība var būt svarīga:

- Nav personas, kura būtu atbildīga par MES integrācijas pārzēšanu.
- Persona, kura ir atbildīga par MES integrācijas pārzinēšanu, vēlas tikt informēts ar e-pasta ziņojumu, ja ziņojums neizdodas, lai viņi zinātu, ka viņiem jāveic darbības.
- MES jārāda kļūdas ziņojums, lai informētu ražotnes operatoru vai paziņotu IT nodaļai, ka viņiem jārīkojas.
- MES jāpārrēķina pasūtījuma grafiks pēc tam, kad tas saņem kļūmes ziņojumu (piemēram, tāpēc, ka ražošanas pasūtījumu nevarēja startēt).

Šādos gadījumos varat izmantot standarta brīdinājuma funkcijas priekšrocības Piegādes ķēžu pārvaldībā. Papildinformāciju par to, kā darbojas standarta brīdinājumi, skatiet šādos resursos:

- Palīdzības tēma: [brīdinājumu apskats](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: brīdinājumu noteikumu opcijas šeit: [Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Piemēram, varat iestatīt šādus brīdinājumus, lai sniegtu atsauksmi par ziņojuma stāvokli:

- Izveidojiet biznesa notikumu ("Sūtīt ārēju"), kas tiek izmantots, ja ziņojums nav *izdevies*.
- Nosūtiet paziņojumu un e-pasta ziņojumu IT administratoram vai ražošanas stāvu pārvaldniekam.
