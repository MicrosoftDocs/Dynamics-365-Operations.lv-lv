---
title: "Atlikušā lietošanas ilguma lineārā aprēķināšanas metode"
description: "Šajā rakstā ir sniegts pārskats par atlikušā lietošanas ilguma lineāro aprēķināšanas metodi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: 9b690b80f148e7ccecba19850bd78c81216d8658
ms.lasthandoff: 03/31/2017


---

# <a name="straight-line-life-remaining-depreciation"></a>Atlikušā lietošanas ilguma lineārā aprēķināšanas metode

Šajā rakstā ir sniegts pārskats par atlikušā lietošanas ilguma lineāro aprēķināšanas metodi.

Iestatot pamatlīdzekļa nolietojuma profilu un atlasot opciju **Lineārais lietošanas ilgums** laukā **Metode** lapā **Nolietojuma profili**, pamatlīdzekļu, kuriem ir piešķirts šis nolietojuma profils, nolietojums ir balstīts uz pamatlīdzekļa kopējo lietošanas ilgumu. Galvenokārt tas nozīmē, ka visiem nolietojuma periodiem ir viena nolietojuma summa. Lai iestatītu atlikušā lietošanas ilguma lineāro aprēķināšanas metodi, jāatlasa arī opcijas laukā **Nolietojuma aprēķina gads**, kā arī laukā **Perioda biežums** lapā **Nolietojuma tabulas**. Laukā **Perioda biežums** pieejamās opcijas ir atkarīgas no vērtības, kas ir atlasīta laukā **Nolietojuma aprēķina gads**.

## <a name="select-a-depreciation-year"></a>Nolietojuma aprēķināšanas gada atlasīšana
Lapā **Nolietojuma tabulas** laukā **Nolietojuma aprēķina gads** varat atlasīt **Kalendārs** vai **Finanšu**. Noklusējuma vērtība ir **Kalendārs**. Jūsu atlase nosaka, kādas opcijas ir pieejamas laukā **Periodu biežums**. Šis lauks nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā.

### <a name="calendar"></a>Kalendārs

Ja atlasāt **Kalendārs**, ***nolietojuma aprēķina gads*** laukā Intervāls no 1. janvāra līdz 31. decembris tiek pieņemts, ka, pat tad, ja finanšu kalendārs esat noteikts savādāk. Opcija **Kalendārs** nolietojuma bāzi atjaunina katru gadu 1. janvārī. Parasti nolietojuma bāze ir atlikusī vērtība mīnus lūžņu vērtība. Tālāk šajā tēmā redzamajos piemēros nolietojuma bāze ir aprēķinu kolonnas pirmās izteiksmes skaitītājs. Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Kalendārs**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** grāmato summu 31. decembrī.
-   **Reizi mēnesī** grāmato mēneša summu katra kalendārā mēneša beigās.
-   **Reizi ceturksnī** grāmato ceturkšņa summu katra kalendārā ceturkšņa beigās (31. martā, 30. jūnijā, 30. septembrī un 31. decembrī).
-   **Pusgada** grāmatojums par pusgada summu katra kalendārā pusgada beigās (30. jūnijs un 31. decembris),
-   **Reizi dienā** — grāmato nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.

Piemēram, ja atlasāt **Reizi gadā**, gada nolietojums tiek grāmatots tikai vienu reizi, katra gada 31. decembrī. Ja atlasāt **Reizi mēnesī**, ikmēneša nolietojums tiek grāmatots katru mēnesi kā divpadsmitā daļa no ikgadējās nolietojuma summas.

### <a name="fiscal"></a>Finanšu

Ja laukā **Nolietojuma aprēķina gads** atlasāt opciju **Finanšu**, tiek izmantota atlikušā lietošanas ilguma lineārā aprēķināšanas metode. Nolietojumu aprēķina, pamatojoties uz atlikušo finanšu gadu. Piemēram, finanšu gads 2015 1. jūlijs, līdz 2016. gada 30. jūnijā, nolietojuma aprēķins sākas 1. jūlijā. Finanšu gads var būt garāks vai īsāks par 12 mēnešiem. Nolietojums tiek pielāgots katram finanšu periodam. Nākamā finanšu gada garumu nosaka finanšu periodi, kas iestatīti lapā **Finanšu kalendāri**. Ja kā nolietojuma aprēķināšanas gadu atlasāt opciju **Finanšu**, tad laukā **Perioda biežums** ir pieejamas tālāk norādītās opcijas.

-   **Reizi gadā** finanšu gada aprēķinātā nolietojuma kopsumma tiek iegrāmatota finanšu gada pēdējā datumā kā viena summa.
-   **Finanšu periods** — aprēķina finanšu gadam aprēķināto nolietojuma kopsummu. Šī summa pēc tam tiek uzkrāta finanšu periodos, kas definēti lapā **Finanšu kalendāri** lapu finanšu kalendāram, kas ir norādīts grāmatai.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Nemainīta pamatlīdzekļa lineārā nolietojuma piemērs
Pamatlīdzeklim ir šādi raksturlielumi.

|                     |        |
|---------------------|--------|
| Iegādes vērtība    | 11 000 |
| Lūžņu vērtība       | 1000  |
| Nolietojuma bāze   | 10 000 |
| Lietošanas ilgums gados  | 5.      |
| Ikgada nolietojums | 2000  |

Nolietojuma summa ir tāda pati katru gadu: (Pirkšanas vērtība — Lūžņu vērtība) ÷ Lietošanas ilgums gados

| Periods | Ikgadējā nolietojuma summas aprēķins | Atlikusī vērtība gada beigās |
|--------|-----------------------------------------------|---------------------------------------|
| 1. gads | (11 000 – 1000) ÷ 5 = 2000                  | 9000                                 |
| 2. gads | (9 000 – 1000) ÷ 4 = 2000                   | 7000                                 |
| 3. gads | (7 000 – 1000) ÷ 3 = 2000                   | 5000                                 |
| 4. gads | (5 000 – 1000) ÷ 2 = 2000                   | 3000                                 |
| 5. gads | (3 000 – 1000) ÷ 1 = 2000                   | 1000                                 |




