---
title: "Pamatlīdzekļu vērtības modeļa un nolietojuma grāmatas sapludināšana"
description: "Iepriekšējos laidienos pamatlīdzekļiem pastāvēja divi vērtēšanas jēdzieni — vērtības modeļi un nolietojuma grāmatas. Programmatūrā Microsoft Dynamics 365 for Operations (1611) vērtības modeļa funkcionalitāte un nolietojuma grāmatas funkcionalitāte ir apvienotas vienā jēdzienā, kas tiek saukts par grāmatu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7a5f833fd7a897d00f8232873c81736a8de65812
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Pamatlīdzekļu vērtības modeļa un nolietojuma grāmatas sapludināšana

[!include[banner](../includes/banner.md)]


Iepriekšējos laidienos pamatlīdzekļiem pastāvēja divi vērtēšanas jēdzieni — vērtības modeļi un nolietojuma grāmatas. Programmatūrā Microsoft Dynamics 365 for Operations (1611) vērtības modeļa funkcionalitāte un nolietojuma grāmatas funkcionalitāte ir apvienotas vienā jēdzienā, kas tiek saukts par grāmatu.

Jauna grāmatas funkcionalitāte ir balstīta uz iepriekšējās vērtības modeļa funkcionalitāti, bet ietver arī visas funkcionalitātes, kas iepriekš tika nodrošinātas tikai nolietojuma grāmatām. [![Grāmata, kurā ir apvienotas vērības modeļa un nolietojuma grāmatas funkcijas](./media/fixed-assets.png)](./media/fixed-assets.png) Šī funkciju apvienošana tagad sniedz iespēju izmantot vienu lapu, pieprasījumu un pārskatu kopu visiem pamatlīdzekļu procesiem. Tabulas šajā tēmā apraksta nolietojuma grāmatu un vērtības modeļu iepriekšējo funkcionalitāti, kopā ar jauno funkcionalitāti grāmatām.

## <a name="setup"></a>Iestatīšana
Pēc noklusējuma grāmatas grāmato gan virsgrāmatā (GL), gan pamatlīdzekļu apakšgrāmatā. Grāmatām ir jauna opcija **Grāmatot Virsgrāmatā**, kas ļauj atspējot grāmatošanu virsgrāmatā, un grāmatot tikai pamatlīdzekļu apakšgrāmatās. Šī funkcionalitāte ir līdzīga agrākai grāmatošanas uzvedībai nolietojuma grāmatām. Žurnālu nosaukumu iestatīšanai ir jaunu grāmatošanas slānis, ar nosaukumu Nav. Šis grāmatošanas līmenis tika pievienots īpaši pamatlīdzekļu darbībām. Lai grāmatotu darbības grāmatām, kas negrāmato Virsgrāmatā, jums ir jāizmanto žurnāla nosaukums, kura grāmatošanas slānis ir iestatīts uz **Nav**.

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | Nolietojuma grāmata               | Vērtības modelis                     | Grāmata (Jauna)                                              |
| Grāmatot virsgrāmatā                                   | Nekad                           | Vienmēr                          | Opcija grāmatot Virsgrāmatā                                |
| Grāmatošanas līmeņi                                   | Nav attiecināms                  | 3: Pašreizējais, Darbības un Nodoklis | 11: Pašreizējais, Darbības, Nodoklis, 7 pielāgoti slāņi un Nav |
| Žurnālu nosaukumi                                    | Nolietojuma grāmatas žurnāla nosaukumi | Virsgrāmata - Žurnālu nosaukumi              | Virsgrāmata - Žurnālu nosaukumi                                      |
| Atvasinātās grāmatas                                    | Nav atļauts                     | Atļauts                         | Atļauts                                                 |
| Nolietojuma profila ignorēšana līdzekļu līmenī | Atļauts                         | Nav atļauts                     | Atļauts                                                 |

## <a name="processes"></a>Procesi
Procesi tagad izmanto kopēju lapu. Daži procesi ir atļauti tikai tad, ja opcija **Grāmatot Virsgrāmatā** ir iestatīta uz **Nē** grāmatas iestatījumā.

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | Nolietojuma grāmata         | Vērtības modelis         | Grāmata (Jauna)                               |
| Darbības ieraksts              | Nolietojuma grāmatas žurnāls | Pamatlīdzekļu žurnāls | Pamatlīdzekļu žurnāls                      |
| Papildnolietojums             | Atļauts                   | Nav atļauts         | Atļauts                                  |
| Dzēst vēsturiskas darbības | Atļauts                   | Nav atļauts         | Atļauts, ja vien jūs grāmatojat Virsgrāmatā |
| Masveida atjaunināšana                    | Atļauts                   | Nav atļauts         | Atļauts, ja vien jūs grāmatojat Virsgrāmatā |

## <a name="inquiries-and-reports"></a>Pieprasījumi un pārskati
Pieprasījumos un pārskatos tiek atbalstītas visas grāmatas. Pārskati, kas nav iekļauti šajā tabulā iepriekš tika atbalstīti gan nolietojuma grāmatās, gan vērtību modeļos, un tagad turpinās atbalstīt visus grāmatu tipus. Lauks **Grāmatošanas slānis** arī tika pievienots pārskatiem, lai jūs varētu vieglāk identificēt darbību grāmatojumus.

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | Nolietojuma grāmata              | Vērtības modelis              | Grāmata (Jauna)               |
| Pieprasījumi                             | Nolietojuma grāmatas darbības | Pamatlīdzekļa darbības | Pamatlīdzekļa darbības |
| Pamatlīdzekļu perioda pārskats                 | Nav atļauts                    | Atļauts                  | Atļauts                  |
| Pamatlīdzekļu bāze                     | Atļauts                        | Nav atļauts              | Atļauts                  |
| Pamatlīdzekļu piemērojamība ceturkšņa pusē | Atļauts                        | Nav atļauts              | Atļauts                  |

## <a name="upgrade"></a>Jaunināt
Jaunināšanas process jūsu esošos iestatījumus un visas jūsu pastāvošās transakcijas pārvietos uz jaunās grāmatas struktūru. Vērtību modeļi saglabāsies pašreizējā stāvokli, kā grāmata, kas grāmato Virsgrāmatā. Tomēr nolietojuma grāmatas tiks pārvietotas uz grāmatu, kurai opcija **Grāmatot virsgrāmatā** ir iestatīta uz **Nē**. Nolietojuma grāmatas žurnāla nosaukumi tiks pārvietoti uz virsgrāmatas žurnāla nosaukumu, kura grāmatošanas slānis ir iestatīts uz **Nav**.




