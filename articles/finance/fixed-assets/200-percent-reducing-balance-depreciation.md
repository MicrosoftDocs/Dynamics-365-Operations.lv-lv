---
title: 200 procentu atlikuma bilances aprēķināšanas metode
description: Šajā rakstā ir sniegts pārskats par 200 procentu atlikumu bilances metodi.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7abcf26f3e658e8a6f451f26240890d183547982
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870167"
---
# <a name="200-percent-reducing-balance-depreciation"></a>200 procentu atlikuma bilances aprēķināšanas metode

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par 200 procentu atlikumu bilances metodi.

Ja iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt lauka **Metode** vērtību **200% atlikumu bilance** lapā **Nolietojuma tabulas**, pamatlīdzekļiem, kam ir piešķirta šī nolietojuma tabula, tiek izmantota vienāda nolietojuma procentu likme katrā nolietojuma periodā. Procentu likme tiek aprēķināta, pamatojoties uz pamatlīdzekļa lietošanas ilgumu. Piemēram, ja pamatlīdzekļa lietošanas ilgums ir pieci gadi, tiek aprēķināta procentu likme 40 procenti (200% ÷ 5). 

Šī metode ir zināma kā dubultdegresīvā nolietojuma aprēķina metode.

Lai iestatītu 200 % atlikumu bilanci, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums**, lapā **Nolietojuma tabulas**. Laukā **Perioda biežums** pieejamās opcijas atšķiras atkarībā no vērtības, ko esat atlasījis laukā **Nolietojuma aprēķina gads**.

## <a name="select-a-depreciation-year"></a>Nolietojuma aprēķināšanas gada atlasīšana
Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**. Noklusējuma vērtība ir **Kalendārs**. 

Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**. Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.

### <a name="calendar"></a>Kalendārs

Laukā **Nolietojuma aprēķina gads** varat paturēt noklusējuma vērtību **Kalendārs**. 

Opcija **Kalendārs** nolietojuma bāzi atjaunina katru gadu 1. janvārī. Parasti nolietojums ir atlikusī vērtība mīnus lūžņu vērtība. Tālāk piemēros šī raksta gadījumā nolietojuma bāze ir aprēķinu pirmās izteiksmes skaitītājs aprēķina kolonnā. 

Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Kalendārs**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** grāmato summu 31. decembrī.
-   **Reizi mēnesī** grāmato mēneša summu katra kalendārā mēneša beigās.
-   **Reizi ceturksnī** grāmato ceturkšņa summu katra kalendārā ceturkšņa beigās (31. martā, 30. jūnijā, 30. septembrī un 31. decembrī).
-   **Reizi pusgadā** — grāmato pusgada summu katrā kalendārajā pusgadā (30. jūnijā un 31. decembrī).
-   **Reizi dienā** — grāmato nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.

### <a name="fiscal"></a>Finanšu

Ja atlasāt lauka **Nolietojuma aprēķina gads** vērtību **Finanšu**, tad 200 % regresīvā nolietojuma bilance tiek aprēķināta, pamatojoties uz finanšu gadu finanšu kalendāram, kas ir norādīts šai grāmatai, vai finanšu kalendāram, kas ir atlasīts lapā **Virsgrāmata**. Finanšu kalendāri tiek iestatīti lapā **Finanšu kalendāri**. 

Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā. Finanšu gads var būt garāks vai īsāks par 12 mēnešiem. Nolietojums tiek pielāgots katram periodam. Nākamā finanšu gada garumu nosaka periodu iestatījumi lapā **Finanšu kalendāri**. 

Ja ir atlasīta nolietojuma aprēķināšanas gada opcija **Finanšu**, laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** finanšu gada aprēķinātā nolietojuma kopsumma tiek iegrāmatota finanšu gada pēdējā datumā kā viena summa.
-   **Finanšu periods** — grāmato finanšu gadam aprēķinātā nolietojuma kopsummu. Šī summa tiek uzkrāta finanšu periodos, kas ir definēti lapā **Finanšu kalendāri**.

## <a name="example-of-200-reducing-balance-depreciation"></a>200% atlikumu bilances piemērs

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| Iegādes vērtība               | 11 000 |
| Lūžņu vērtība                  | 1000 |
| Nolietojuma bāze              | 10 000 |
| Lietošanas ilgums gados             | 5.      |
| Gada nolietojuma procenti | 40%    |

200 % atlikumu bilances metode dala 200 procentus ar lietošanas ilguma gadiem. Šie procenti tiek reizināti ar pamatlīdzekļa atlikušo vērtību, lai noteiktu gada nolietojuma summu.

| Periods | Ikgadējā nolietojuma summas aprēķins | Atlikusī vērtība             | Atlikusī vērtība gada beigās |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 1. gads | (11 000 – 1000) × 40% = 4000                | 11 000 – 4000 = 7000 | 11 000 – 1000 – 4000 = 6000        |
| 2. gads | 6000 × 40% = 2400                           | 7000 – 2400 = 4600  | 6000 – 2400 = 3600                 |
| 3. gads | 3600 × 40% = 1440                           | 4600 – 1440 = 3160  | 3600 – 1440 = 2160                 |

> [!NOTE] 
> Kad summa, kas tiek aprēķināta, izmantojot 200% degresīvo nolietojuma aprēķināšanas metodi, kļūst mazāka par summu, kas rastos, lietojot lineāro metodi, atlikušā kalpošanas laika aprēķināšanai parasti notiek konversija uz lineāro metodi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
