---
title: Darbību ikonu un nosaukumu piešķiršana Warehouse Management mobilajai programmai
description: Šajā tēmā ir aprakstīts, kā piešķirt darbību ikonas un virsrakstus jaunām vai pielāgotām uzdevumu plūsmām Warehouse Management mobilajai lietojumprogrammai.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049368"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Darbību ikonu un nosaukumu piešķiršana Warehouse Management mobilajai programmai

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā piešķirt darbību ikonas un virsrakstus jaunām vai pielāgotām uzdevumu plūsmām Warehouse Management mobilajai lietojumprogrammai.

Nākamajās ilustrācijās ir parādīts, kā darbību ikonas un virsraksti tiek parādīti Warehouse Management mobilajā lietojumprogrammā.

![Darbību ikonas un virsraksta piemērs Warehouse Management mobilajā lietojumprogrammā](media/step-icon-example.png "Darbību ikonas un virsraksta piemērs Warehouse Management mobilajā lietojumprogrammā")

## <a name="turn-on-this-feature-in-your-system"></a>Šī līdzekļa ieslēgšana sistēmā

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Lietotāja iestatījumi, ikonas un darbību nosaukumi jaunajai noliktavas programmai*

## <a name="standard-step-ids-classes-and-icons"></a>Standarta darbību ID, klases un ikonas

Katra darbība uzdevumu plūsmā tiek identificēta ar darbības ID, un katram darbības ID ir atbilstoša darbības klase. Darbības ikona un virsraksts ir norādīti katrā darbības klasē.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Darbību ID un darbības klases

Šajā tabulā ir uzskaitīti visi darbības ID, kas pašlaik ir pieejami, un tai atbilstoša darbības klase. Primārā ievades lauka kontroles nosaukums tiek izmantots kā darbības ID.

Piemēru, kurā parādīts, kā tiek lietoti šie darbības ID un klases, skatiet `WHSMobileAppStepInfoBuilder.stepId()` metodes ieviešanas sadaļā [Piemērs: Darbību ikonu un nosaukumu piešķiršana pielāgotajai plūsmai](#example) tālāk šajā tēmā.

| Darbības ID | Darbības klase |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Pārvadātājs | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Apstiprināšana | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Atgriešanas metode | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| PONum | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Saturs | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Izvietot | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Daudz. | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Lielums | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Pieejamās darbību ikonas

Sistēmā ir ietverta standarta darbību ikonu kolekcija, ko varat izmantot arī pielāgotajām darbībām. Šobrīd nevar augšupielādēt pielāgotās darbību ikonas. Tāpēc vienmēr jāatlasa viena no standarta darbību ikonām.

Šajā tabulā parādīta katra standarta darbības ikona, kas pašreiz ir pieejama, un tās nosaukums.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Par darbības ikonu"><br>Par programmu</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Pievienot numura zīmi vai krājuma darbības ikonu"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Partijas atgriešanas darbības ikona"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Pārvadātāja darbības ikona"><br>Pārvadātājs</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Pieļaujamā svara etiķetes darbības ikona"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Pieļaujamā svara etiķetes svara darbības ikona"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Kontrolcipara darbības ikona"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Ierakstīšanās vai izrakstīšanas ID darbības ikona"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Pakārtotās numura zīmes darbības ikona"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Klastera ID darbības ikona"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Klastera pozīcijas darbības ikona"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Konfigurācijas ID darbības ikona"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Konfigurētā lauka darbības ikona"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con vai LP darbības ikona"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsolidēt no numura zīmes ID darbības ikona"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsolidēt uz numura zīmes ID darbības ikona"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Konteinera tipa darbības ikona"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Uzskaites darbības ikona"><br>Inventarizācija</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Inventarizācijas iemesla koda darbības ikona"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Izcelsmes valsts koda darbības ikona"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Atgriešanas darbības ikona"><br>Atgriešanas metode</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Pabeigtā darbības ikona"><br>Pabeigts</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Transportlīdzekļa vadītāja reģistrēšanās apstiprinājuma darbības ikona"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Transportlīdzekļa vadītāja pierakstīšanās ID darbības ikona"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Transportlīdzekļa vadītāja izrakstīšanās ID darbības ikona"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Beigu datuma darbības ikona"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Lauka darbības ikona"><br>Lauks</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="No partijas atgriešanas darbības ikona"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="No krājumu statusa darbības ikona"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ID atribūta darbības ikona"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Krājumu partijas ID darbības ikona"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Krājumu krāsas ID darbības ikona"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Krājumu atrašanās vietas darbības ikona"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Krājumu sērijas ID darbības ikona"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Krājumu izmēra ID darbības ikona"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Krājumu statusa ID darbības ikona"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Krājumu stila ID darbības ikona"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Krājumu versijas ID darbības ikona"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Krājuma ID darbības ikona"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM konteinera ID darbības ikona"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM sūtījuma ID darbības ikona"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban kartes ID darbības ikona"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban vai kartes ID darbības ikona"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Numura zīmes ID darbības ikona"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Kravas ID darbības ikona"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Numura zīmes novietojuma pozīcijas darbības ikona"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Atrašanās vietas vai numura zīmes darbības ikona"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Atrašanās vietas vai numura zīmes pārbaudes darbības ikona"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Atrašanās vietas vai numura zīmes no darbības ikonas"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Atrašanās vieta vai numura zīme uz darbības ikona"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Ilgais process pabeigts darbības ikona"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP pārtraukuma pamata LP darbības ikona"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Apvienot konteinera ID darbības ikona"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Jauktas numura zīmes rindas numura darbības ikona"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Izejošā svara darbības ikona"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Īpašnieka darbības ikona"><br>Īpašnieks</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Pamata numura zīmes darbības ikona"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Lūdzu, apstipriniet darbības ikona"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Pirkšanas pasūtījuma rindas numura darbības ikona"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Pirkšanas pasūtījuma numura darbības ikona"><br>PONum</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Pozīcija pilna darbības ikona"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Satura darbības ikona"><br>Saturs</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Printera nosaukuma darbības ikona"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Preces ID darbības ikona"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Preces apstiprināšanas darbības ikona"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Izvietot darbības ikona"><br>Izvietot</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Izvietošanas klastera ID darbības ikona"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Daudzuma darbības ikona"><br>Daudz.</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Daudzuma pielāgošana izvietošanā darbības ikona"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Mazā daudzuma darbības ikona"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Daudzums, kas tiek patērēts darbības ikona"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Daudzums, kas tiek izvietots darbības ikona"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Daudzums, kas tiek izbrāķēts darbības ikona"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Daudzuma apstiprināšanas darbības ikona"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Ziņot, kad pabeigts gala darbs darbības ikona"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Saņemt novietojuma ID darbības ikona"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Noņemt konteinera ID darbības ikona"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA numura darbības ikona"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Atlasīt pasūtījumu darbības ikona"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Saīsinātās izdošanas iemesla darbības ikona"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Kārtot pozīcijas ID darbības ikona"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Mērķa numura zīmes ID darbības ikona"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Uz rindas numuru darbības ikona"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Uz atrašanās vietu darbības ikona"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Uz numuru darbības ikona"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Uz noliktavu darbības ikona"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Transporta kravas ID darbības ikona"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Kreditora partijas ID darbības ikona"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Kopuma etiķetes ID darbības ikona"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Kopuma etiķetes daudzuma darbības ikona"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Svara darbības ikona"><br>Lielums</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Svars, kas tiek patērēts darbības ikona"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS korekcijas tipa darbības ikona"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS saņemšanas izņēmuma darbības ikona"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS atrašanās vietas ID darbības ikona"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Darba ID darbības ikona"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Darba ID, lai atceltu darbības ikona"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Darba numura zīmes ID darbības ikona"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Darba numura zīmes ID izdošanas klastera darbības ikona"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Darba kopuma ID darbības ikona"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Zonas ID darbības ikona"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Piemērs: darbību ikonu un nosaukumu piešķiršana pielāgotajai plūsmai

Šajā piemērā skaidrots, kā iestatīt darbību ikonas un nosaukumus pielāgotai uzdevumu plūsmai. Scenārijs ir veidots no pielāgotas uzdevumu plūsmas piemēra, kas ir uzrādīta un detalizētāk aprakstīta tālāk aprakstītajā ziņā: [Noliktavas mobilās programmas pielāgošana](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Uzdevumu plūsma darbojas šādi:

1. Programmā tiek parādīta lapa, kurā darbiniekam tiek parādīta uzvedne ar aicinājumu norādīt konteinera ID (piemēram, skenējot svītrkodu).
1. Ja konteinera ID ir derīgs, programma atver jaunu lapu, kurā tiek parādīta uzvedne ar aicinājumu darbiniekam ievadīt svaru. (Ja konteinera ID nav derīgs, darbinieks tiek atgriezts pirmajā lapā.)
1. Kad darbinieks ievada derīgu svaru, sistēma saglabā svaru un atgriež darbinieku pirmajā lapā.

Šajā attēlā parādīta šī uzdevuma plūsma.

![Uzdevuma plūsmas diagramma](media/step-icons-example-task-flow.png "Uzdevuma plūsmas diagramma")

### <a name="create-a-step-class-for-the-container-input-page"></a>Izveidot darbības klasi konteinera ievades lapai

Konteinera ievades lapa ļauj darbiniekam skenēt vai ievadīt konteinera ID.

![Konteinera ievades lapa](media/step-icons-example-container-input.png "Konteinera ievades lapa")

Konteinera ievades lapā ir ievadītā lauka kontroles nosaukums `ContainerId`. Tā kā šis vadīklas nosaukums nav norādīts [darbības ID sarakstā](#step-ids-classes), jūs neatradīsiet esošu darbību, kas ir balstīta uz to. Tādēļ ir jāizveido darbības klase, kas pārstāv šo darbību. Tālāk ir minēts piemērs.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Darbības ikonas identifikators tiek saglabāts `defaultStepIcon` klases dalībniekā, un darbības nosaukums tiek saglabāts `defaultStepTitle` klases dalībniekā.

Lai piešķirtu darbības ikonu, iestatiet `defaultStepIcon` uz vienu no ikonu ID, kas uzskaitīti sadaļā [Pieejamās darbības ikonas](#step-icons) iepriekš šajā tēmā.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Izmantojiet standarta vai pielāgotu darbības ikonu un nosaukumu svara ievadei

Svara ievades lapa ļauj darbiniekam ievadīt svaru.

![Svara ievades lapa](media/step-icons-example-weight-input.png "Svara ievades lapa")

Svara ievades lapā ievades lauka kontroles nosaukums ir `Weight`, kas atrodas [darbības ID sarakstā](#step-ids-classes). Tādēļ, ja definētā darbības ikona un nosaukums `WHSMobileAppStepWeight` klasē jums ir pieņemami, šai darbībai nekas nav jāmaina.

Tomēr, ja šai darbībai vēlaties lietot citu ikonu vai nosaukumu, varat ignorēt `stepId()` metodi vai `stepInfo()` metodi veidotāja klasē. Katrai uzdevumu plūsmai ir savs darbību informācijas veidotājs.

#### <a name="override-the-stepid-method"></a>Ignorēt stepId() metodi

Šajā piemērā parādīts viens veids, kā modificēt veidotāja klasi, ignorējot `stepId()` metodi.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Izveidojiet darbības klasi `NewWeight` darbībai. Kodam ir jābūt līdzīgam kodam iepriekš parādītajā `ContainerId` piemērā.

#### <a name="override-the-stepinfo-method"></a>Ignorēt stepInfo() metodi

Šajā piemērā parādīts viens veids, kā modificēt veidotāja klasi, ignorējot `stepInfo()` metodi.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

Tad konstruējiet objektu `WHSMobileAppStepInfo` un tieši iestatiet ikonu un/vai nosaukumu.

## <a name="additional-resources"></a>Papildu resursi

- [Noliktavas pārvaldības mobilās programmas instalēšana un savienošana](install-configure-warehouse-management-app.md)
- [Mobilās ierīces lietotāja iestatījumi](mobile-device-user-settings.md)
