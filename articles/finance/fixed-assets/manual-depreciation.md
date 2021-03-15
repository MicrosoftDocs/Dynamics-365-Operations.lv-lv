---
title: Manuāls nolietojuma aprēķins
description: Šajā rakstā ir sniegts pārskats par manuālo nolietojuma metodi.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 228e6c94042942a26793eb0bebc1186dd4767e7f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969033"
---
# <a name="manual-depreciation"></a>Manuāls nolietojuma aprēķins

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par manuālo nolietojuma metodi.

Kad iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt vērtību **Manuāls** laukā **Metode**, lapā **Nolietojuma tabulas**, šai nolietošanas tabulai piešķirto pamatlīdzekļu nolietojums tiek noteikts pēc procentuālā daudzuma, ko ievadāt katram kalendārā gada intervālam. Intervāli, kuriem iestatāt procentuālo daudzumu, tiek grāmatoti atbilstoši vērībai, kuru atlasāt laukā **Perioda biežums**, kopsavilkuma cilnē **Vispārīgi**, kura atrodas lapā **Nolietojuma tabulas**. Varat atlasīt šādas vērtības:

-   Reizi gadā
-   Reizi mēnesī
-   Reizi ceturksnī
-   Reizi pusgadā
-   Katru dienu

Pēc perioda biežuma atlasīšanas noklikšķiniet uz **Manuālie grafiki** un iestatiet procentuālo daudzumu katram grāmatošanas intervālam. Manuālie grafiki un grāmatošanas intervāli kopā nosaka nolietojuma summu, kā parādīts šajā rakstā tālāk iekļautajos piemēros. Manuālais nolietojums vienmēr tiek aprēķināts kā procenti no iegādes cenas. Attiecībā uz manuālo nolietojumu jūsu nolietojuma intervālos ievadītajiem procentuālajiem daudzumiem kopā nav jāveido 100 procenti. Manuāls nolietojums ir elastīga nolietojuma metode, ko bieži lieto, lai lapā **Grāmatas** definētu specifisku nolietojuma tabulu, piemēram, neregulāru nolietojumu specifiskiem mērķiem (piemēram, nodokļiem).

## <a name="examples"></a>Piemēri
Iegādes cena: 11 000,00 Plānotā lūžņu vērtība: 1000,00 Nākamajā tabulā ir parādīti intervāli un procentuālie daudzumi, ko iestatāt lapā **Pamatlīdzekļu nolietojuma aprēķina tabulas**.

| Intervāla numurs | Procenti |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

Nākamajā tabulā ir parādīts, ka nolietojums tiek aprēķināts katram intervālam.

|  Intervāla numurs | Ikgadējā nolietojuma summas aprēķins | Atlikusī vērtība intervāla beigās |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11 000 – 1000)× 10% = 1000                | 10 000 (11 000 – 1000)                   |
| 2                | (11 000 – 1000) × 50% = 5000                | 5000 (10 000 – 5000)                    |
| 3                | (11 000 – 1000) × 8% = 800                   | 4200 (5000 – 800)                       |

Ja laukā **Perioda biežums** atlasāt vērtību **Reizi mēnesī**, jūs iestatāt 12 manuālus grafika intervālus. Nākamajā tabulā ir parādītas nolietojuma summas pirmajiem diviem intervāliem.

| Intervāls | Nolietojuma summa            |
|----------|--------------------------------|
| Janvāris  | (11 000 – 1000)× 10% = 1000 |
| Februāris | (11 000 – 1000) × 50% = 5000 |

Ja atlasāt lauka <strong>Perioda biežums</strong> vērtību *<strong><em>Reizi pusgadā</em>* </strong>, tiek iestatīti divi manuālā grafika intervāli. Nākamajā tabulā ir parādītas nolietojuma summas šiem diviem intervāliem.

| Intervāls    | Nolietojuma summa            |
|-------------|--------------------------------|
| 30. jūnijs     | (11 000 – 1000)× 10% = 1000 |
| 31. decembris | (11 000 – 1000) × 50% = 5000 |

Intervālu procentuālo vērtību kopsummai nav jābūt 100. Taču, ja lapā **Pamatlīdzekļu nolietojuma aprēķina tabula** esošā lauka **Uzkrātie procenti** vērtība nav **100**, tiek parādīts attiecīgs ziņojums.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]