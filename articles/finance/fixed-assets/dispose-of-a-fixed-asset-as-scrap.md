---
title: Izslēgt pamatlīdzekļus kā norakstītos
description: Tēmā ir aprakstīts process, kurā tiek likvidētas transakcijas pamatlīdzeklim, kas noņemts kā brāķis.
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 413847d350ca6b2bdd6153a598ea5b3f34a33818
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826279"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Izslēgt pamatlīdzekļus kā norakstītos

[!include [banner](../includes/banner.md)]

Tēmā ir aprakstīts process, kurā tiek likvidētas transakcijas pamatlīdzeklim, kas noņemts kā brāķis. Transakciju veidi, kurus var likvidēt, ietver pamatlīdzekļa iegādi un uzkrātā nolietojuma transakcijas un citas pamatlīdzekļu transakcijas. Šo darbību likvidēšana ietekmē bilances kontus, piemēram, iegādes korekciju, nolietojuma korekciju, pārvērtēšanu, vērtības palielināšanu un vērtības samazināšanu.

| Darījums                                         | Debets (Dr.) | Kredīts (Kr.) |
|-----------------------------------------------------|-------------|--------------|
| Dr. Uzkrātais nolietojums.                        | X           |              |
| Kr. Pamatlīdzekļu peļņa/zaudējumi                          |             | X            |
| Dr. Pamatlīdzekļu peļņa/zaudējumi                          | X           |              |
| Kr. Pamatlīdzekļu ieguves konti                 |             | X            |
| Dr. Pamatlīdzekļu peļņa/zaudējumi (atlikusī vērtība \[NBV\]) | X           |              |
| Kr. Pamatlīdzekļu peļņa/zaudējumi (NBV)                    |             | X            |

> [!NOTE]
> Iesakām cieši sadarboties ar uzņēmuma galveno finanšu darbinieku (CFO) vai kontrolieri, lai identificētu pareizos kontus, kas jāizmanto katram transakcijas veidam, kā arī pārbaudīt, vai likvidēšanas process un transakcijas, ko tas ģenerē, atjauninā šos kontus pareizi.

Pirms pamatlīdzekļa likvidēsanas kā brāķa, ir jāizveido virsgrāmatas konts, kas ir saistīts ar pamatlīdzekļa iegādes vērtību, nolietojumu pašreizējam gadam, nolietojumu iepriekšējos gados un pamatlīdzekļa NBV. Pamatlīdzekļu transakciju veidi ir uzskaitīti **Pamatlīdzekļu grāmatošanas profila** lapā. Dodieties uz **Pamatlīdzekļi \> Iestatīšanas \> Pamatlīdzekļu grāmatošanas metodes** un pēc tam kopsavilkuma cilnē **Likvidēšana** atlasiet **Brāķis** laukā virs režģa. Sekojošajā attēlā ir redzams pamatlīdzekļu transakciju veidu saraksts **Pamatlīdzekļu grāmatošanas profile** lapā.


[![Pamatlīdzekļa likvidēšana kā brāķa, 1. attēls](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Šim piemēram, pamatlīdzeklis tika iegādāts 2018. gada 1. janvārī, un tas tiks likvidēts 2019. gada 31. martā.

- **Iegādes cena:** 24 000,00 ASV dolāri (USD)
- **Lietošanas ilgums:** Divi gadi
- **Nolietojuma metode:** lineārais lietošanas ilgums
- **Nolietojuma daudzums:** 1 000,00 USD mēnesī

Pamatlīdzekļa NBV tiek aprēķināts, izmantojot šādu formulu:

Atlikusī vērtība = Iegādes cena — Nolietojums

Šajā piemērā pamatlīdzeklis tika iegādāts un tika nolietots 15 mēnešu laikā no 2018. līdz 2019. gada martam. Tāpēc pamatlīdzekļa NBV ir 9 000,00 USD (24 000,00 USD – 15 000,00 USD).

[![Pamatlīdzekļa nolietojuma piemērs](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Lai izveidotu likvidēšanas žurnālu, atveriet **Pamatlīdzekļi \> Žurnāla ieraksti \> Pamatlīdzekļu žurnāls** un pēc tam Darbības rūtī atlasiet **Rindas**. Atlasiet **Likvidēšana— brāķis**, pēc tam atlasiet pamatlīdzekļa ID. Lai pilnībā likvidētu pamatlīdzekli, neievadiet vērtību laukā **Debets** vai laukā **Kredīts**.

[![Pamatlīdzekļu žurnāls](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Pamatlīdzekļa likvidēšanas transakcija brāķa dēļ maina pamatlīdzekļu grāmatas lauka vērtības šādos veidos:

- Sadaļā **Bilance** lauks **Statuss** tiek atjaunināts uz **Brāķēts**.
- Sadaļā **Izsniegšana** lauks **Likvidēšanas datums** tiek iestatīts uz datumu, kad pamatlīdzeklis tika norakstīts.

[![Detalizēta informācija par amatlīdzekļu žurnālu](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Sekojošajā attēlā ir redzama pamatlīdzekļa bilance.

[![Pamatlīdzekļu bilance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Sekojošajā attēlā ir redzams grāmatots dokuments.

[![Atlikusī vērtība](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]