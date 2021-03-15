---
title: Krājumu pieejamība duālajā ierakstā
description: Šajā tēmā ir sniegta informācija par to, kā pārbaudīt krājumu pieejamību duālajā ierakstā.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839553"
---
# <a name="inventory-availability-in-dual-write"></a>Krājumu pieejamība duālajā ierakstā

[!include [banner](../../includes/banner.md)]

Izmantojot krājumu pieejamību, varat pārbaudīt krājumus pirms preču pievienošanas lapā **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** programmā Microsoft Dynamics 365 Sales. Piemēram, krājumu pārbaude un izpildes datuma noteikšana ir galvenais uzdevums procesā [no potenciālā klienta līdz skaidrai naudai](dual-write-prospect-to-cash.md).

Ja nav pietiekami daudz krājumu, varat aplēst piegādes datumu, pamatojoties uz prognozēto krājumu saņemšanas un izsniegšanas plūsmām. Varat arī pārbaudīt preces pieejams solīšanai (ATP) informāciju, kur varat atrast ATP daudzumu iepriekš definētā laika periodā.

## <a name="on-hand-inventory"></a>Rīcībā esošie krājumi

Dynamics 365 Sales **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** lapu galvenē ir pievienota jauna poga **Rīcībā esošie krājumi**. Atlasot šo pogu, parādās dialoglodziņš, kur varat norādīt uzņēmumu un preci, kurai vēlaties pārbaudīt rīcībā esošos krājumus. Šis dialoglodziņš parāda to pašu informāciju, ko [rīcībā esošie krājumi](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialoglodziņā tiek atgriezta informācija par krājumiem no Dynamics 365 Supply Chain Management. Šajā informācijā ir iekļauti tālāk norādītie daudzumi:

- Rīcībā esošais daudzums
- Rezervētais rīcībā esošais daudzums
- Pieejamais rīcībā esošais daudzums
- Pasūtītais daudzums
- Pasūtījumā iekļautais daudzums
- Rezervētais pasūtītais daudzums
- Kopējais pieejamais daudzums

## <a name="atp-information"></a>ATP informācija

Programmā Sales ir pievienota jauna **ATP informācija**, kas ir pievienota rindas precēm **Piedāvājumu**, **Pasūtījumu** un **Rēķinu** lapās. Atlasot šo pogu, parādās dialoglodziņš, kur varat norādīt uzņēmumu, preci, krājuma atrašanās vietu, krājuma noliktavu un krājumu daudzumu. Šim dialoglodziņam ir tie paši iestatījumi, kas aprakstīti [Pasūtījumu solīšanā](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialoglodziņā tiek atgriezta ATP informācija no Supply Chain Management. Šajā informācijā ir iekļauti tālāk norādītie daudzumi:

- ATP daudzums
- Ieejas plūsmas daudzums
- Izejas plūsmas daudzums
- Rīcībā esošais daudzums

## <a name="how-it-works"></a>Kā tas darbojas

Atlasot pogu **Rīcībā esošie krājumi** lapā **Piedāvājumi**, **Pasūtījumi** vai **Rēķini**, **Rīcībā esošo krājumu API** tiek veikts tiešais duālās rakstīšanas izsaukums. API aprēķina dotās preces rīcībā esošos krājumus. Rezultāts tiek glabāts tabulās **InventCDSInventoryOnHandRequestEntity** un **InventCDSInventoryOnHandEntryEntity**, tad to ieraksta programmā Dataverse duālā ieraksta formā. Lai lietotu šo funkcionalitāti, ir jāpalaiž šādas duālās rakstīšanas kartes. Izlaist sākotnējo sinhronizāciju, kad palaižat kartes.

- CDS rīcībā esošo krājumu ieraksti (msdyn_inventoryonhandentries)
- CDS rīcībā esošo krājumu pieprasījumi (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Veidnes
Rīcībā esošo krājumu datu atklāšanai ir pieejamas šādas veidnes.

Finance and Operations programmas | Customer engagement programma | Apraksts 
---|---|---
[CDS krājumu rīcībā esošie ieraksti](#145) | msdyn_inventoryonhandentries |
[CDS krājumu rīcībā esošie pieprasījumi](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>CDS rīcībā esošo krājumu ieraksti (msdyn_inventoryonhandentries)

Šī veidne sinhronizē datus starp Finance and Operations programmām un Dataverse.

Finance and Operations lauks | Kartes veids | Lauks Customer engagement | Noklusētā vērtība
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>CDS rīcībā esošo krājumu pieprasījumi (msdyn_inventoryonhandrequests)

Šī veidne sinhronizē datus starp Finance and Operations programmām un Dataverse.

Finance and Operations lauks | Kartes veids | Lauks Customer engagement | Noklusētā vērtība
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]