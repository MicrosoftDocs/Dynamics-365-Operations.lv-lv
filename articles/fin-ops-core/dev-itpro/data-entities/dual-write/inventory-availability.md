---
title: Krājumu pieejamība duālajā ierakstā
description: Šajā rakstā ir sniegta informācija, kā pārbaudīt krājumu pieejamību dubultās rakstīšanas veidā.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 442486550d3a7c5132e26f663caaa7c2c02eeb6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289214"
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

Finance and Operations programmas | Customer engagement programmas     | Apraksts
---|---|---
[CDS krājumu rīcībā esošie ieraksti](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[CDS krājumu rīcībā esošie pieprasījumi](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
