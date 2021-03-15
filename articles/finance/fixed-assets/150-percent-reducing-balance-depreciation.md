---
title: 150 procentu degresīvā nolietojuma aprēķināšanas metode
description: Šajā rakstā ir sniegts pārskats par 150 procentu degresīvās nolietojuma aprēķināšanas metodi.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc7fa705681c3f1fde96cabc430dad1dd0045b4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009322"
---
# <a name="150-percent-reducing-balance-depreciation"></a>150 procentu degresīvā nolietojuma aprēķināšanas metode

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par 150 procentu degresīvās nolietojuma aprēķināšanas metodi.

Ja iestatāt pamatlīdzekļa nolietojuma tabulu un atlasāt lauka **Metode** vērtību **150% atlikumu bilance** lapā **Nolietojuma tabulas**, pamatlīdzekļiem, kam ir piešķirta šī nolietojuma tabula, tiek izmantota vienāda nolietojuma procentu likme katrā nolietojuma periodā. Šī procentu likme tiek aprēķināta, pamatojoties uz pamatlīdzekļa lietošanas ilgumu. Piemēram, ja līdzekļa lietošanas ilgums ir pieci gadi, tiek aprēķināta procentu likme 30 procenti (150% ÷ 5). 

Lai iestatītu 150 % atlikumu bilanci, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums**, lapā **Nolietojuma tabulas**. Laukā **Perioda biežums** pieejamās opcijas ir atkarīgas no vērtības, kas ir atlasīta laukā **Nolietojuma aprēķina gads**.

## <a name="selection-of-depreciation-year"></a>Nolietojuma aprēķina gada atlase
Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**. 

Noklusējuma vērtība ir **Kalendārs**. Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**. Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.

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

Ja atlasāt lauka **Nolietojuma aprēķina gads** vērtību **Finanšu**, tad 150% regresīvā nolietojuma bilance tiek aprēķināta, pamatojoties uz finanšu gadu finanšu kalendāram, kas ir norādīts šai grāmatai, vai finanšu kalendāram, kas ir atlasīts lapā **Virsgrāmata**. Finanšu kalendāri tiek iestatīti lapā **Finanšu kalendāri**. 

Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā. Finanšu gads var būt garāks vai īsāks par 12 mēnešiem. Nolietojums tiek pielāgots katram periodam. Nākamā finanšu gada garumu nosaka periodu iestatījumi lapā **Finanšu kalendāri**. 

Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Finanšu**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** — grāmato nolietojuma kopsummu, kas finanšu gadam tiek aprēķināta attiecīgā finanšu gada pēdējā datumā.
-   **Finanšu periods** — grāmato finanšu gadam aprēķinātā nolietojuma kopsummu. Šī summa tiek uzkrāta finanšu periodos, kas ir definēti lapā **Finanšu kalendāri**.

## <a name="example-of-150-reducing-balance-depreciation"></a>150% atlikumu bilances piemērs

|                                |        |
|--------------------------------|--------|
| Iegādes vērtība               | 11 000 |
| Lūžņu vērtība                  | 1000  |
| Nolietojuma bāze              | 10 000 |
| Lietošanas ilgums gados             | 5.      |
| Gada nolietojuma procenti | 30%    |

150 % atlikumu bilances metode dala 150 procentus ar lietošanas ilguma gadiem. Šie procenti tiek reizināti ar pamatlīdzekļa atlikušo vērtību, lai noteiktu gada nolietojuma summu.

| Periods | Ikgadējā nolietojuma summas aprēķins | Atlikusī vērtība             | Atlikusī vērtība gada beigās |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 1. gads | (11 000 – 1000) × 30% = 3000                | 11 000 – 3000 = 8000 | 11 000 – 1000 – 3000 = 7000        |
| 2. gads | 7000 × 30% = 2100                           | 8000 – 2100 = 5900  | 7000 – 2100 = 4900                 |
| 3. gads | 4900 × 30% = 1470                           | 5900 – 1470 = 4430  | 4900 – 1470 = 3430                 |

> [!NOTE]
> Kad summa, kas tiek aprēķināta, izmantojot 150% degresīvo nolietojuma aprēķināšanas metodi, kļūst mazāka par summu, kas rastos, lietojot lineāro metodi, atlikušā kalpošanas laika aprēķināšanai parasti notiek konversija uz lineāro metodi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]