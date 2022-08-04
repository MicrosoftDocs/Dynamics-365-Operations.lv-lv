---
title: Integrācija ar trešās puses ražošanas izpildes sistēmām
description: Šajā rakstā skaidrots, kā jūs varat Dynamics 365 Supply Chain Management integrēt Microsoft ar trešās puses ražošanas izpildes sistēmu (LES).
author: johanhoffmann
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 46f6db3dd9942131b379216e6fffe5551d6c8fc3
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068037"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integrācija ar trešās puses ražošanas izpildes sistēmām

[!include [banner](../includes/banner.md)]

Dažas ražošanas organizācijas, kas izmanto Microsoft vietējo Dynamics 365 Supply Chain Management funkcionalitāti sistēmā Dynamics 365, lai kontrolētu savas ražošanas darbības mašīnām, aprīkojumam un personālam. Tomēr citas ražošanas organizācijas, it īpaši tās, kurām ir papildu ražošanas vajadzības, tās vietā izmantojiet trešās puses ražošanas izpildes sistēmu (MES). Organizācijas var izvēlēties trešās puses MES risinājumu, jo, piemēram, tas ir īpaši pielāgots vertikālajai nozarei.

Integrētajā risinājumā datu apmaiņa ir pilnībā automatizēta un notiek tuvu reālam laikam. Tāpēc dati tiek saglabāti abās sistēmās un nav nepieciešama manuāla datu ievade. Piemēram, kad materiālu patēriņš ir reģistrēts MES, integrācija nodrošina, ka tāds pats patēriņš tiek reģistrēts arī Dynamics 365. Tāpēc līdz šim krājuma ieraksti ir pieejami citiem svarīgiem procesiem, piemēram, plānošanai un pārdošanai.

Risinājums atvieglo un ātrāku Piegādes ķēžu pārvaldības lietotāju integrāciju ar trešās puses MES. Tā piedāvā šādas funkcijas:

- Biznesa notikumi un interfeisi, kas atbalsta [galvenos ražošanas izpildes procesus](#processes-available-for-mes-integration)
- Centralizēts informācijas panelis, kur var izsekot notikumu apstrādes vēsturi un novērst problēmu un labot procesus, kas neizdodas

Šajā ilustrācijā parādīts tipisks biznesa notikumu, procesu un ziņojumu apkopojums, kas tiek apmainīts integrētā risinājumā.

![Tipisks integrācijas scenārijs.](media/3p-mes-scenario.png "Tipisks integrācijas scenārijs.")

## <a name="turn-on-the-mes-integration-feature"></a>Ieslēgt MES integrācijas līdzekli

Pirms šo funkciju iespējams izmantot, administratoram tas jāslēdz jūsu sistēmā kā aprakstīts šajā procedūrā.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
1. Pārliecinieties, vai laika **un apmeklētības licences** atslēga ir iespējota (parāda atzīmi). Šī licences atslēga ir nepieciešama, jo tā kontrolē ražošanas izpildes sistēmas funkcionalitāti un datus. Ja tā nav iespējota, veiciet šādas darbības:
    1. Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
    1. Licences konfigurācijas **lapā** atzīmējiet izvēles **rūtiņu Laiks un** apmeklētība.
    1. Izslēgt uzturēšanas režīmu, kā aprakstīts uzturēšanas [režīmā](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)
1. Dodieties uz sistēmas **administrēšanas \> darbalauku \> līdzekļu pārvaldību**.
1. Slēdziet funkciju, kas ir uzskaitīta šādā veidā (skatiet arī Līdzekļu [pārvaldības apskatu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)):
    - **Modulis:** *Ražošanas kontrole*
    - **Funkcionalitātes nosaukums:** *ražošanas izpildes sistēmas integrācija*

## <a name="processes-available-for-mes-integration"></a>MES integrācijai pieejamie procesi

Integrācijai jūs varat iespējot jebkurus vai visus tālāk norādītos procesus.

| Procesa Nosaukums | Apraksts |
|---|---|
| Nodot izpildei ražošanas pasūtījumus un ražošanas pasūtījuma statusa maiņas biznesa notikumus | Šis process nodrošina biznesa notikumu, ko MES var noklausīties, lai iegūtu informāciju par ražojamajiem ražošanas pasūtījumiem. Atsauces datus, kas ir saistīti ar ražošanas pasūtījumu, paredzēts koplietot no Piegādes ķēžu pārvaldības uz MES, izmantojot Atvērto datu protokolu (OData) vai datu elementus. |
| Sākt ražošanas pasūtījumu | Šis process nodrošina Piegādes ķēdes pārvaldību ar informāciju par ražošanas pasūtījumiem, kas tiek uzsākti, izmantojot MES. Tas nodrošina, ka abām sistēmām tiek atjauninātas visas ražošanas darbības. |
| Ziņot par saražoto vai norakstīto daudzumu | Šis process nodrošina Piegādes ķēdes pārvaldību ar informāciju par labiem un kļūdu daudzumiem, par kuriem ziņots par ražošanas darbu, izmantojot MES. Tas nodrošina, ka ražotnes supervizoriem ir ražošanas plāna progresa atjaunināta skatījums. |
| Ziņot par materiālu patēriņu | Šis process nodrošina Piegādes ķēdes pārvaldību ar informāciju no MES par patērēto materiālu daudzumu. Tas veido līdz šim pieejamos krājumu ierakstus citiem svarīgiem procesiem, piemēram, plānošanai un pārdošanai. |
| Operācijai patērētais pārskata laiks | Šis process nodrošina Piegādes ķēdes pārvaldību ar informāciju par laiku, kas tiek izmantots noteiktai operācijai. |
| Pārtraukt ražošanas pasūtījumu | Šis process informē Piegādes ķēdes pārvaldību, ka MES ir atjauninājis ražošanas pasūtījumu uz tā gala statusu *Pabeigts*. Šis statuss norāda, ka ražošanas pasūtījumā vairs netiks ražoti daudzumi. |

## <a name="monitor-incoming-messages"></a>Ienākošo ziņojumu pārraudzīšana

Lai uzraudzītu ienākošos ziņojumus sistēmai, atveriet lapu **Ražošanas izpildes sistēmu integrācija**. Tur varat skatīt, apstrādāt un novērst problēmas.

Visi ziņojumi konkrētam ražošanas pasūtījumam tiek apstrādāti tādā secībā, kādā tie tiek saņemti. Tomēr ziņojumus dažādiem ražošanas pasūtījumiem nevar apstrādāt saņemtā secībā, jo pakešuzdevumi tiek apstrādāti paralēli. Kļūmes gadījumā pakešuzdevums mēģinās apstrādāt katru ziņojumu trīs reizes, pirms iestatīs to uz Neizdevušos *statusu*.

## <a name="call-the-api"></a>Izsaukt API

Lai izsauktu MES integrācijas API, nosūtiet pieprasījumu `POST` uz šādu galapunkta URL:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Jūsu sūtītā pieprasījuma pamatteksts ir līdzīgs šim piemēram. Nomainiet vērtības `_companyId` uz un `_messageType` pēc `_messageContent` vajadzības. Lai iegūtu informāciju par dažādiem ziņojumu tipiem, ko API atbalsta un kā projektēt to saturu, skatiet nākamo sadaļu.

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

Šajā sadaļā ir aprakstīts katra tipa ziņojums, ar kuru var veikt apmaiņu, izmantojot MES integrācijas API.

### <a name="start-production-order-message"></a>Sākt ražošanas pasūtījuma ziņojumu

Sāktam *ražošanas pasūtījuma* ziņojumam ir `_messageType` vērtība `ProdProductionOrderStart`. Šajā tabulā redzami lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `StartedQuantity` | Neobligāti | Reāls |
| `StartedDate` | Neobligāti | Datums |
| `AutomaticBOMConsumptionRule` | Neobligāti | Uzskaitījums (FlushingPrincip \| vienmēr \|) |

### <a name="report-as-finished-message"></a>Ziņojums par pabeigšanu

Pabeidzamā *ziņojuma* vērtība `_messageType` ir `ProdProductionOrderReportFinished`. Šajā tabulā redzami lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `ReportFinishedLines` | Obligāts | Rindu saraksts (vismaz viens), no kurām viena satur nākamajā tabulā aprakstīto lietderīgo slodzi |

Šajā tabulā ir parādīti lauki, kurus katra rinda `ReportFinishedLines` ziņojuma sadaļā `ProdProductionOrderReportFinished` atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `LineNumber` | Neobligāti | Reāls |
| `ItemNumber` | Neobligāti | Virkne|
| `ProductionType` | Neobligāti | Uzskaitījums (MainItem \| formulas \|\| MK Co_Product \| By_Product \| nav), paplašināms |
| `ReportedErrorQuantity` | Neobligāti | Reāls|
| `ReportedGoodQuantity` | Neobligāti | Reāls|
| `ReportedErrorCatchWeightQuantity` | Neobligāti | Reāls |
| `ReportedGoodCatchWeightQuantity` | Neobligāti | Reāls |
| `AcceptError` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `ErrorCause` | Neobligāti | Uzskaitījums (Nav \| materiālu \| iekārtas \| OperatingStaff), paplašināms |
| `ExecutedDateTime` | Neobligāti | Datums un laiks |
| `ReportAsFinishedDate` | Neobligāti | Datums |
| `AutomaticBOMConsumptionRule` | Neobligāti | Uzskaitījums (FlushingPrincip \| vienmēr \|) |
| `AutomaticRouteConsumptionRule` | Neobligāti |Uzskaitījums (RouteDependent \| Never \|) |
| `RespectFlushingPrincipleDuringOverproduction` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `ProductionJournalNameId` | Neobligāti | Virkne |
| `PickingListProductionJournalNameId` | Neobligāti | Virkne|
| `RouteCardProductionJournalNameId` | Neobligāti | Virkne |
| `FromOperationNumber` | Neobligāti | Vesels skaitlis|
| `ToOperationNumber` | Neobligāti | Vesels skaitlis|
| `InventoryLotId` | Neobligāti | Virkne |
| `BaseValue` | Neobligāti | Virkne |
| `EndJob` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `EndPickingList` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `EndRouteCard` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `PostNow` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `AutoUpdate` | Neobligāti | Uzskaitījums (Jā \| Nē) |
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

12 paplašināmām dimensijām (`InventoryDimension1``InventoryDimension12` izmantojot) nepieciešama pielāgošana, un tās vienmēr netiek izmantotas. Papildinformāciju par tām skatiet sadaļā Jaunu [krājumu dimensiju pievienošana, izmantojot paplašinājumu](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Materiālu patēriņa (izdošanas saraksta) ziņojums

Materiālu patēriņa *(izdošanas saraksta) ziņojumam* vērtība `_messageType` ir `ProdProductionOrderPickingList`. Šajā tabulā redzami lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `JournalNameId` | Neobligāti | Virkne |
| `PickingListLines` | Obligāts | Rindu saraksts (vismaz viens), no kurām viena satur nākamajā tabulā aprakstīto lietderīgo slodzi |

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
| `IsConsumptionEnded` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `ErrorCause` | Neobligāti | Uzskaitījums (Nav \| materiālu \| iekārtas \| OperatingStaff), paplašināms |
| `InventoryLotId` | Neobligāti | Virkne |

### <a name="time-used-for-operation-route-card-message"></a>Operācijas (maršruta kartes) ziņojuma laiks

*Operācijas (maršruta kartes) ziņojumam izmantotais* laiks ir `_messageType` vērtība `ProdProductionOrderRouteCard`. Šajā tabulā redzami lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `JournalNameId` | Neobligāti | Virkne |
| `RouteCardLines` | Obligāts | Rindu saraksts (vismaz viens), no kurām viena satur nākamajā tabulā aprakstīto lietderīgo slodzi |

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
| `ErrorCause` | Neobligāti | Uzskaitījums (Nav \| materiālu \| iekārtas \| OperatingStaff), paplašināms |
| `OperationCompleted` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `BOMConsumption` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `ReportAsFinished` | Neobligāti | Uzskaitījums (Jā \| Nē) |

### <a name="end-production-order-message"></a>Pārtraukt ražošanas pasūtījuma ziņojumu

*Beigu ražošanas pasūtījuma ziņojumam* ir `_messageType` vērtība `ProdProductionOrderEnd`. Šajā tabulā redzami lauki, kurus šis ziņojums atbalsta.

| Lauka nosaukums | Statuss | Veids |
|---|---|---|
| `ProductionOrderNumber` | Obligāts | Virkne |
| `ExecutedDateTime` | Neobligāti | Datums un laiks |
| `EndedDate` | Neobligāti | Datums |
| `UseTimeAndAttendanceCost` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `AutoReportAsFinished` | Neobligāti | Uzskaitījums (Jā \| Nē) |
| `AutoUpdate` | Neobligāti | Uzskaitījums (Jā \| Nē) |

## <a name="other-production-information"></a>Cita informācija par ražošanu

Ziņojumi atbalsta darbības vai notikumus, kas notiek ražotnes jomā. Tos apstrādā, izmantojot šajā rakstā aprakstīto MES integrācijas struktūru. Dizainā ir pieņemts, ka cita atsauces informācija, ko koplietot ar MES (piemēram, ar preci saistīta informācija vai materiālu komplekts vai maršruts (ar tā specifiskiem iestatījumiem un konfigurācijas laikiem), kas tiek izmantoti noteiktā ražošanas pasūtījumā), [tiks](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#data-entities) izgūta no sistēmas, izmantojot datu elementus, izmantojot faila pārsūtīšanu vai OData.

## <a name="receive-feedback-about-the-state-of-a-message"></a>Saņemt atsauksmi par ziņojuma stāvokli

Kad MES ir nosūtījis ziņojumu Piegādes ķēžu pārvaldībai, iespējams, ka tas būs svarīgi Piegādes ķēžu pārvaldībai, lai atgrieztu atsauksmes par ziņojuma stāvokli. Šeit sniegti daži piemēri par gadījumiem, kad šī uzvedība var būt svarīga:

- Nav personas, kura būtu atbildīga par MES integrācijas pārzēšanu.
- Persona, kura ir atbildīga par MES integrācijas pārzinēšanu, vēlas tikt informēts ar e-pasta ziņojumu, ja ziņojums neizdodas, lai viņi zinātu, ka viņiem jāveic darbības.
- MES jārāda kļūdas ziņojums, lai informētu ražotnes operatoru vai paziņotu IT nodaļai, ka viņiem jārīkojas.
- MES jāpārrēķina pasūtījuma grafiks pēc tam, kad tas saņem kļūmes ziņojumu (piemēram, tāpēc, ka ražošanas pasūtījumu nevarēja startēt).

Šādos gadījumos varat izmantot standarta brīdinājuma funkcijas priekšrocības Piegādes ķēžu pārvaldībā. Papildinformāciju par to, kā darbojas standarta brīdinājumi, skatiet šādos resursos:

- Palīdzības dokuments: [Brīdinājumu apskats](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [brīdinājuma noteikuma opcijas finansēs un operācijās](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Piemēram, varat iestatīt šādus brīdinājumus, lai sniegtu atsauksmi par ziņojuma stāvokli:

- Izveidojiet biznesa notikumu ("Sūtīt ārēju"), kas tiek izmantots, ja ziņojums nav *izdevies*.
- Nosūtiet paziņojumu un e-pasta ziņojumu IT administratoram vai ražošanas stāvu pārvaldniekam.

