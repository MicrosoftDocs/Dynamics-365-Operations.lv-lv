---
title: "Pamatlīdzekļu vērtības modeļa un nolietojuma grāmatas sapludināšana"
description: "Iepriekšējos laidienos, pastāvēja divi vērtēšanas jēdzieni - vērtību modeļus un nolietojuma grāmatas pamatlīdzekļiem. Programmā Microsoft Dynamics 365 atbrīvošanas operāciju 1611, vērtības modeļa funkcionalitāti un nolietojuma grāmatu funkcionalitāte sapludināti vienotā koncepcija, kas ir pazīstams kā grāmatu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6c8c005c7f5ede54ce0b6c8114cac69e2551d467
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Pamatlīdzekļu vērtības modeļa un nolietojuma grāmatas sapludināšana

Iepriekšējos laidienos, pastāvēja divi vērtēšanas jēdzieni - vērtību modeļus un nolietojuma grāmatas pamatlīdzekļiem. Programmā Microsoft Dynamics 365 atbrīvošanas operāciju 1611, vērtības modeļa funkcionalitāti un nolietojuma grāmatu funkcionalitāte sapludināti vienotā koncepcija, kas ir pazīstams kā grāmatu.

Jauna grāmatas funkcionalitāte ir balstīta uz iepriekšējās vērtības modeļa funkcionalitāti, bet ietver arī visas funkcionalitātes, kas iepriekš tika nodrošinātas tikai nolietojuma grāmatām. [![Grāmatu kā apvienojas ar vērtības modeli un nolietojuma grāmatu funkcionalitāte](./media/fixed-assets.png)](./media/fixed-assets.png) sapludināšanu, tāpēc tagad varat izmantot vienotu kopumu lapas, Uzziņas un pārskatus visiem pamatlīdzekļu procesiem. Tabulas šajā tēmā apraksta nolietojuma grāmatu un vērtības modeļu iepriekšējo funkcionalitāti, kopā ar jauno funkcionalitāti grāmatām.

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


