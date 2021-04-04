---
title: Nosūtīšanas konteineri
description: Šajā tēmā ir aprakstīts, kā iestatīt nosūtīšanas konteinerus Kopējo izmaksu modulim.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500962"
---
# <a name="shipping-container-setup"></a>Nosūtīšanas konteinera iestatījumi

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt nosūtīšanas konteinerus **Kopējo izmaksu** modulim.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Konteinera veidu iestatīšana

Nosūtīšanas konteinera veidi nosaka nosūtīšanas konteineru tipus, kuri ir pieejami izmantošanai nosūtīšanas un reisu laikā.

Lai strādātu ar nosūtīšanas konteineru tipiem, dodieties uz **Kopējās izmaksas \> Konteineru iestatījumi \> Nosūtīšanas konteineru veidi**. Tur varat skatīt, pievienot un noņemt ierakstus saviem konteineru tipiem. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Nosūtīšanas konteinera veids | Ievadiet nosūtīšanas konteinera tipam unikālu ID nosaukumu/numuru. |
| Apraksts | Ievadiet nosūtīšanas konteinera tipa aprakstu. |
| Tilpums | Ievadiet maksimālo tilpumu, kas ir atļauts šī tipa nosūtīšanas konteineros. |
| Lielums | Ievadiet maksimālo svaru, kas ir atļauts šī tipa nosūtīšanas konteineros. |
| Atgriežams | Norādiet, vai šāda veida sūtījuma konteinerus var atgriezt kreditoram pēc tam, kad tie ir izmantoti reisa laikā. Ja šī opcija ir iestatīta kā *Jā*, šī tipa pārvadāšanas konteineru atgriešanai uz izcelsmes ostu var tikt piemērotas papildu izmaksas. |

## <a name="set-up-shipping-containers"></a>Nosūtīšanas konteineru iestatīšana

Jūs izmantojat nosūtīšanas konteinera ierakstus, lai identificētu katru konteineru, ko izmantojat reisu laikā. Kad izveidojat reisu, varat tam atlasīt īpašu konteineru visu šeit definēto nosūtīšanas konteinera ierakstu sarakstā. Šī funkcija ir īpaši noderīga, ja jūsu uzņēmumam pieder savi nosūtīšanas konteineri.

Jums nav jāievada nosūtīšanas konteineru numuri nosūtīšanas konteineriem, kas tiks izmantoti tikai vienu reizi. Tā vietā varat pievienot nosūtīšanas konteinera numuru, izveidojot reisu.

Nosūtīšanas konteinera ieraksti tiek izmantoti tikai sūtījuma izmaksām. Tās nav pieejamas standarta **Transportēšanas pārvaldības** modulī (TMS).

Lai strādātu ar nosūtīšanas konteineru tipiem, dodieties uz **Kopējās izmaksas \> Konteineru iestatījumi \> Nosūtīšanas konteineri**. Tur varat skatīt, pievienot un noņemt ierakstus saviem nosūtīšanas konteineriem. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Nosūtīšanas konteiners | Ievadiet nosūtīšanas konteinera tipam unikālu ID nosaukumu/numuru. |
| Nosūtīšanas konteinera veids | Atlasiet nosūtīšanas konteinera tipu. Papildinformāciju skatiet šīs tēmas iepriekšējā sadaļā [Nosūtīšanas konteineru tipu iestatīšana](#shipping-container-types). |

> [!NOTE]
> - Nosūtīšanas konteinera iestatīšana nav obligāta. Parasti to izmantosiet tikai tad, ja jūsu uzņēmumam pieder savi nosūtīšanas konteineri vai arī tie paši nosūtīšanas konteineri bieži tiek atkārtoti izmantoti.
> - Nosūtīšanas konteineru numuriem netiek aprēķināts neviens kontrolskaitlis.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Vienību tipu iestatīšana

Vienību tipi izveido papildu grupējumus un identifikācijas metodes nosūtīšanas konteineriem. Vienības tips parasti tiek izmantots, lai identificētu konteinera tipu, kurā preces tiek iepakotas, piemēram, paletēs vai tvertnēs. Vienības tipu var atlasīt, iestatot konteineru lapā **Visi pārvadāšanas konteineri**.

Vienību tipi tiek izmantoti tikai Kopējās izmaksās. Tie nav pieejami TMS.

Lai strādātu ar nosūtīšanas konteineru tipiem, dodieties uz **Kopējās izmaksas \> Konteineru iestatījumi \> Vienību tipi**. Tur varat skatīt, pievienot un noņemt ierakstus saviem vienību tipiem. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Vienības veids | Ievadiet vienības tipa unikālo ID nosaukumu/numuru. |
| Apraksts | Ievadiet vienības tipa aprakstu. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Refrižeratora tipu iestatīšana

Refrižeratoru tipi veido papildu nosūtīšanas konteineru grupēšanas un identifikācijas līdzekļus, parasti tie ir refrižeratora konteineri. Refrižeratora tipu var atlasīt, iestatot konteineru lapā **Visi nosūtīšanas konteineri**.

Lai strādātu ar nosūtīšanas konteineru tipiem, dodieties uz **Kopējās izmaksas \> Konteineru iestatījumi \> Refrižeratoru tipi**. Tur varat skatīt, pievienot un noņemt ierakstus saviem refrižeratoru tipiem. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Dzesēšanas veids | Ievadiet refrižeratora tipa unikālo ID nosaukumu/numuru. |
| Apraksts | Ievadiet refrižeratora tipa aprakstu. |
