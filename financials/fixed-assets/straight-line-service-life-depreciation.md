---
title: "Lineārā lietošanas ilguma nolietojums"
description: "Šajā rakstā ir sniegts pārskats par atlikušā lietošanas ilguma lineāro aprēķināšanas metodi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5ff3d87f610489608f0bebadd9bb4c9c5c727992
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="straight-line-service-life-depreciation"></a>Lineārā lietošanas ilguma nolietojums

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par atlikušā lietošanas ilguma lineāro aprēķināšanas metodi.

Iestatot pamatlīdzekļa nolietojuma profilu un lapas Nolietojuma profili laukā Metode atlasot opciju Lineārais lietošanas ilgums, pamatlīdzekļi, kuriem ir piešķirts šis nolietojuma profils, tiek uzskatīti par nolietotiem, pamatojoties uz pamatlīdzekļa kopējo lietošanas ilgumu. Galvenokārt tas nozīmē, ka visiem nolietojuma periodiem ir viena nolietojuma summa. 

Nolietojuma summas aprēķins starp lineāro atlikušo lietošanas ilgumu un lineāro lietošanas ilgumu atšķiras, ja pamatlīdzekļiem ir iegrāmatota korekcija. 

Lai iestatītu lineārā lietošanas ilguma nolietojumu, jāatlasa arī opcijas laukā Nolietojuma aprēķina gads, kā arī lapas Nolietojuma profili laukā Perioda biežums.

## <a name="select-a-depreciation-year"></a>Nolietojuma aprēķināšanas gada atlasīšana
Nolietojuma profilu lapas laukā Nolietojuma aprēķina gads varat atlasīt Kalendārs vai Finanšu. Atlase nosaka opcijas, kas pieejamas laukā Periodu biežums. Noklusējuma opcija ir Kalendārs.

### <a name="calendar"></a>Kalendārs

Atlasot opciju Kalendārs, tiks izmantots laika intervāls no 1. janvāra līdz 31. decembrim, pat ja ir atšķirīgi noteikts finanšu kalendārs. 

Opcija Kalendārs katra gada 1. janvārī atjaunina nolietojuma bāzi, kas parasti ir atlikusī vērtība mīnus lūžņu vērtība. Tālāk šajā tēmā redzamajos piemēros nolietojuma bāze ir aprēķinu kolonnas pirmās izteiksmes skaitītājs. 

Atlasot opciju Kalendārs, laukā Periodu biežums ir četras opcijas, kas nosaka nolietojuma uzkrājuma grāmatošanas datumus un summas kalendārā gada laikā:
-   Reizi gadā grāmato summu 31. decembrī.
-   ikmēneša grāmatojums par mēneša summu katra kalendārā mēneša beigās,
-   katra ceturkšņa grāmatojums par ceturkšņa summu katra kalendārā ceturkšņa beigās (31. marts, 30. jūnijs, 30. septembris un 31. decembris),
-   Pusgada grāmatojums par pusgada summu katra kalendārā pusgada beigās (30. jūnijs un 31. decembris),
-   ikdienas grāmatojums par nolietojuma summu ikdienas nolietojuma metodei, izmantojot vienu transakciju katrai dienai.

Piemēram, ja atlasāt Reizi gadā, gada nolietojums tiek grāmatots tikai vienu reizi, katra gada 31. decembrī. Ja atlasāt Reizi mēnesī, ikmēneša nolietojums tiek grāmatots katru mēnesi kā 1/12 daļa no ikgadējās nolietojuma summas.

### <a name="fiscal"></a>Finanšu

Ja laukā Nolietojuma aprēķina gads atlasāt opciju Finanšu, tiek izmantots lietošanas ilguma nolietojums. Tā tiek aprēķināta, pamatojoties uz finanšu gadu, ko definē finanšu kalendārs, kas norādīts grāmatai, vai ko definē finanšu kalendārs, kas atlasīts lapā Virsgrāmata. Finanšu kalendāri tiek iestatīti lapā Finanšu kalendāri.

Piemēram, finanšu gadam no 1. jūlija līdz 30. jūnijam nolietojuma aprēķins sākas 1. jūlijā. Finanšu gads var būt garāks vai īsāks par 12 mēnešiem. Nolietojums tiek automātiski pielāgots katram finanšu periodam. Nākamā finanšu gada garums tiek noteikts, pamatojoties uz finanšu periodiem, kurus iestatāt jauna finanšu gada izveidē formā Finanšu kalendāri. 

Atlasot opciju Finanšu, laukā Periodu biežums ir pieejamas šādas opcijas:
-   Reizi gadā: finanšu gadam aprēķinātā nolietojuma kopsumma tiek grāmatota kā viena summa finanšu gada pēdējā datumā.
-   Finanšu periods — aprēķina nolietojuma kopsummu finanšu gadā, kas sadalīts finanšu periodos, kuri katram finanšu gadam definēti formā Finanšu kalendāri.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Piemērs: nemainīta pamatlīdzekļa lineārais nolietojums
Pieņemsim, ka pamatlīdzeklim ir šādi raksturlielumi.

|                     |        |
|---------------------|--------|
| Iegādes vērtība    | 11 000 |
| Lūžņu vērtība       | 1000  |
| Nolietojuma bāze   | 10 000 |
| Lietošanas ilgums gados  | 5.      |
| Ikgada nolietojums | 2000  |

Katru gadu ir vienāda nolietojuma summa. (pirkšanas vērtība — likvidācijas vērtība)/lietošanas ilgums gados

| Periods | Ikgada nolietojuma summas aprēķins | Atlikusī vērtība gada beigās |
|--------|-------------------------------------------|---------------------------------------|
| 1. gads | (11 000 - 1000)/5 = 2000              | 9000                                 |
| 2. gads | (11 000 - 1000)/5 = 2000              | 7000                                 |
| 3. gads | (11 000 - 1000)/5 = 2000              | 5000                                 |
| 4. gads | (11 000 - 1000)/5 = 2000              | 3000                                 |
| 5. gads | (11 000 - 1000)/5 = 2000              | 1000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a> Piemērs: modificēta pamatlīdzekļa lineārais nolietojums

Pieņemsim, ka tam pašam pamatlīdzeklim 2. gadā tiek pievienota kapitālā izmaksa par summu 4000. 

Kapitālās izmaksas lietošanas ilgums ir tāds pats kā pamatlīdzeklim un sākas ar tā iegādes brīdi. Atlikusī vērtība paliek uz 5. gada beigām atbilstoši kapitālās izmaksas atlikušajai vērtībai. Nolietojums pa periodiem tiek aprēķināts šādi:

| Periods | Ikgada nolietojuma summas aprēķins | Atlikusī vērtība gada beigās |
|--------|-------------------------------------------|---------------------------------------|
| 1. gads | 10 000/5 = 2000                        | 11 000 - 2000 = 9000                |
| 2. gads | 4000 (iegādes pielāgošana)            | 9000 + 4000 = 13 000                 |
| 2. gads | 14 000/5 = 2800                        | 13 000 - 2800 = 10 200               |
| 3. gads | 14 000/5 = 2800                        | 10 200 - 2800 = 7400                |
| 4. gads | 14 000/5 = 2800                        | 7400 - 2800 = 4600                 |
| 5. gads | 14 000/5 = 2800                        | 4600 - 2800 = 1800                 |
| 6. gads | Atlikusī summa 800\*                           | 1800 - 800 = 1000                   |

\*Tā kā atlikusī summa ir mazāka par nolietojuma summu, tiek ņemta tikai atlikusī summa, kas mazāka par likvidācijas vērtību.






