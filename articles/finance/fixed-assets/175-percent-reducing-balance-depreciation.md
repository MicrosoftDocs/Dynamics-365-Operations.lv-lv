---
title: 175 procentu degresīvā nolietojuma aprēķināšanas metode
description: Šajā rakstā ir sniegts pārskats par 175 procentu atlikumu bilances nolietojuma metodi.
author: moaamer
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68c10a1fe221731f7304fc0da92ed314b66dc13f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870196"
---
# <a name="175-percent-reducing-balance-depreciation"></a>175 procentu degresīvā nolietojuma aprēķināšanas metode

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par 175 procentu atlikumu bilances nolietojuma metodi.

Ja iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt lauka **Metode** vērtību **175% atlikumu bilance** lapā **Nolietojuma tabulas**, pamatlīdzekļiem, kam ir piešķirta šī nolietojuma tabula, tiek izmantota vienāda nolietojuma procentu likme katrā nolietojuma periodā. 

Lai iestatītu 175 % atlikumu bilanci, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums**, lapā **Nolietojuma tabulas**. Laukā **Perioda biežums** pieejamās opcijas ir atkarīgas no vērtības, kas ir atlasīta laukā **Nolietojuma aprēķina gads**.

## <a name="select-a-depreciation-year"></a>Nolietojuma aprēķināšanas gada atlasīšana
Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**. Noklusējuma vērtība ir **Kalendārs**. 

Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**. Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.

### <a name="calendar"></a>Kalendārs

Laukā **Nolietojuma aprēķina gads** varat paturēt noklusējuma vērtību **Kalendārs**. 

Opcija **Kalendārs** nolietojuma bāzi atjaunina katru gadu 1. janvārī. Parasti nolietojuma bāze ir atlikusī vērtība mīnus lūžņu vērtība. Tālāk piemēros šī raksta gadījumā nolietojuma bāze ir aprēķinu pirmās izteiksmes skaitītājs aprēķina kolonnā. 

Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Kalendārs**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** grāmato summu 31. decembrī.
-   **Reizi mēnesī** grāmato mēneša summu katra kalendārā mēneša beigās.
-   **Reizi ceturksnī** grāmato ceturkšņa summu katra kalendārā ceturkšņa beigās (31. martā, 30. jūnijā, 30. septembrī un 31. decembrī).
-   **Reizi pusgadā** — grāmato pusgada summu katrā kalendārajā pusgadā (30. jūnijā un 31. decembrī).
-   **Reizi dienā** — grāmato nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.

### <a name="fiscal"></a>Finanšu

Ja atlasāt lauka **Nolietojuma aprēķina gads** vērtību **Finanšu**, tad 175% regresīvā nolietojuma bilance tiek aprēķināta, pamatojoties uz finanšu gadu finanšu kalendāram, kas ir norādīts šai grāmatai, vai finanšu kalendāram, kas ir atlasīts lapā **Virsgrāmata**. Finanšu kalendāri tiek iestatīti lapā **Finanšu kalendāri**. Papildinformāciju skatiet rakstā [Finanšu kalendāri, finanšu gadi un periodi](../budgeting/fiscal-calendars-fiscal-years-periods.md).

Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā. Finanšu gads var būt garāks vai īsāks par 12 mēnešiem. Nolietojums tiek automātiski pielāgots katram periodam, un nākamā finanšu gada garumu nosaka periodu iestatījumi lapā **Finanšu kalendāri**. 

Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Finanšu**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** — grāmato nolietojuma kopsummu, kas finanšu gadam tiek aprēķināta attiecīgā finanšu gada pēdējā datumā.
-   **Finanšu periods** — aprēķina finanšu gadam aprēķināto nolietojuma kopsummu. Šī summa tiek uzkrāta finanšu periodos, kas ir definēti lapā **Finanšu kalendāri**.

## <a name="example-of-175-reducing-balance-depreciation"></a>Atlikuma samazinošā nolietojuma par 175% piemērs

| Lauks                          | Vērtība  |
|--------------------------------|--------|
| Iegādes vērtība               | 11,000 |
| Lūžņu vērtība                  | 1000  |
| Nolietojuma bāze              | 10 000 |
| Lietošanas ilgums gados             | 5.      |
| Gada nolietojuma procenti | 35%    |

Izmantojot 175% degresīvā nolietojuma aprēķināšanas metodi, 175 procenti tiek dalīti ar lietošanas ilgumu gados. Šie procenti tiek reizināti ar pamatlīdzekļa atlikušo vērtību, lai noteiktu gada nolietojuma summu.

| Periods | Ikgadējā nolietojuma summas aprēķins | Atlikusī vērtība                  | Atlikusī vērtība gada beigās |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| 1. gads | (11 000 – 1000) × 35% = 3500                | 11 000 – 3500 = 7500      | 11 000 – 1000 – 3500 = 6500        |
| 2. gads | 6500 × 35% = 2275                           | 7500 – 2275 = 5225       | 6500 – 2275 = 4225                 |
| 3. gads | 4225 × 35% = 1478,75                        | 5225 – 1478,75 = 3746,25 | 4225 – 1478,75 = 2746,25           |

> [!NOTE] 
> Kad summa, kas tiek aprēķināta, izmantojot 175% degresīvo nolietojuma aprēķināšanas metodi, kļūst mazāka par summu, kas rastos, lietojot lineāro metodi, atlikušā kalpošanas laika aprēķināšanai parasti notiek konversija uz lineāro metodi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
