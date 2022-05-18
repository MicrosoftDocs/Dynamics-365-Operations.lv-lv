---
title: 125 procentu atlikuma bilances aprēķināšanas metode
description: Šajā tēmā sniegts pārskats par 125 procentu atlikumu bilances metodi.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 756048d1627731af2e1eb7a23a9dcc2756583526
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711581"
---
# <a name="125-percent-reducing-balance-depreciation"></a>125 procentu atlikuma bilances aprēķināšanas metode

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegts pārskats par 125 procentu atlikumu bilances metodi.

Iestatot pamatlīdzekļa nolietojuma tabulu un atlasot **125% atlikumu bilance** laukā **Metode**, lapā **Nolietojuma tabulas**, nolietojuma tabulai piešķirtā pamatlīdzekļa nolietojuma procenti ir vienādi visos nolietojuma periodos. Šī procentu likme tiek aprēķināta, pamatojoties uz pamatlīdzekļa lietošanas ilgumu. Piemēram, ja pamatlīdzekļa lietošanas ilgums ir pieci gadi, tiks aprēķināta procentu likme 25 procenti (125% ÷ 5).

Lai iestatītu 125 % atlikumu bilanci, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums**, lapā **Nolietojuma tabulas**. Laukā **Perioda biežums** pieejamās opcijas ir atkarīgas no vērtības, kas ir atlasīta laukā **Nolietojuma aprēķina gads**.

## <a name="select-a-depreciation-year"></a>Nolietojuma aprēķināšanas gada atlasīšana
Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**. Noklusējuma vērtība ir **Kalendārs**. 

Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**. Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.

### <a name="calendar"></a>Kalendārs

Laukā **Nolietojuma aprēķina gads** varat paturēt noklusējuma vērtību **Kalendārs**. 

Opcija **Kalendārs** nolietojuma bāzi atjaunina katru gadu 1. janvārī. Parasti nolietojuma bāze ir atlikusī vērtība mīnus lūžņu vērtība. Tālāk šajā tēmā redzamajos piemēros nolietojuma bāze ir aprēķinu kolonnas pirmās izteiksmes skaitītājs. 

Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Kalendārs**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** grāmato summu 31. decembrī.
-   **Reizi mēnesī** grāmato mēneša summu katra kalendārā mēneša beigās.
-   **Reizi ceturksnī** grāmato ceturkšņa summu katra kalendārā ceturkšņa beigās (31. martā, 30. jūnijā, 30. septembrī un 31. decembrī).
-   **Reizi pusgadā** — grāmato pusgada summu katrā kalendārajā pusgadā (30. jūnijā un 31. decembrī).
-   **Reizi dienā** — grāmato nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.

### <a name="fiscal"></a>Finanšu

Ja atlasāt lauka **Nolietojuma aprēķina gads** vērtību **Finanšu**, tad 125% regresīvais nolietojums tiek aprēķināts, pamatojoties uz finanšu gadu finanšu kalendāram, kas ir norādīts šai grāmatai, vai finanšu kalendāram, kas ir atlasīts lapā **Virsgrāmata**. Finanšu kalendāri tiek iestatīti lapā **Finanšu kalendāri**. 

Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā. Finanšu gads var būt garāks vai īsāks par 12 mēnešiem. Nolietojums tiek automātiski pielāgots katram periodam, un nākamā finanšu gada garumu nosaka periodu iestatījumi lapā **Finanšu kalendāri**. 

Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Finanšu**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** finanšu gada aprēķinātā nolietojuma kopsumma tiek iegrāmatota finanšu gada pēdējā datumā kā viena summa.
-   **Finanšu periods** — grāmato finanšu gadam aprēķinātā nolietojuma kopsummu. Šī summa tiek uzkrāta finanšu periodos, kas ir definēti lapā **Finanšu kalendāri**.

## <a name="example-of-125-reducing-balance-depreciation"></a>125% atlikumu bilances piemērs

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| Iegādes vērtība               | 11 000 |
| Lūžņu vērtība                  | 1000  |
| Nolietojuma bāze              | 10 000 |
| Lietošanas ilgums gados             | 5.      |
| Gada nolietojuma procenti | 25%    |

125 % atlikumu bilances metode dala 125 procentus ar lietošanas ilguma gadiem. Šie procenti tiek reizināti ar pamatlīdzekļa atlikušo vērtību, lai noteiktu gada nolietojuma summu.

| Periods | Ikgadējā nolietojuma summas aprēķins | Atlikusī vērtība                    | Atlikusī vērtība gada beigās |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| 1. gads | (11000 – 1000) × 25% = 2500                | (11000 – 2500) = 8500      | (11000 – 1000 – 2500) = 7500      |
| 2. gads | 7500 × 25% = 1875                           | (8500 – 1875) = 6625       | (7500 – 1875) = 5625               |
| 3. gads | 5625 × 25% = 1406,25                        | (6625 – 1406,25) = 5218,75 | (5625 – 1406,25) = 4218,75         |

> [!NOTE] 
> Kad summa, kas tiek aprēķināta, izmantojot 125% degresīvo nolietojuma aprēķināšanas metodi, kļūst mazāka par summu, kas rastos, lietojot lineāro metodi, atlikušā kalpošanas laika aprēķināšanai parasti notiek konversija uz lineāro metodi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
