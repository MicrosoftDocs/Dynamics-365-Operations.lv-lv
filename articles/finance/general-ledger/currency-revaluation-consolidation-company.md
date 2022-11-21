---
title: Valūtas pārvērtēšana konsolidācijas uzņēmumā
description: Šajā rakstā ir aprakstīts, kā pārvērtēt valūtu konsolidācijas uzņēmumā.
author: aprilolson
ms.date: 10/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c05ef0d4d05d5113d3b858dafe49ee9c1c7211d9
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779667"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Valūtas pārvērtēšana konsolidācijas uzņēmumā

[!include [banner](../includes/banner.md)]

Veicot datu konsolidāciju no vienas norēķinu valūtas uz citu, joprojām jāpalaiž valūtas pārvērtēšana, ja ir izmaiņas valūtas maiņas kursos, lai jūsu konta bilances tiktu pareizi pārvērtētas. Sākotnēji konsolidējot datus, izmantojiet cilni **Valūtas pārrēķināšana**, lai atlasītu sākotnējos maiņas kursus, pārrēķināšanai konsolidācijas procesa laikā. Pēc jaunā valūtas maiņas kursa ievadīšanas (piemēram, nākamajā mēnesī), nepieciešams pārvērtēt kontu bilances. Nerealizētā peļņa vai zaudējumi pēc tam tiek attiecīgi atjaunināta, pamatojoties uz jauno valūtas maiņas kursu un datumu. Šajā piemērā tiek parādīti uzskaites ieraksti, kas tiek izveidoti procesa laikā.

## <a name="company-setup"></a>Uzņēmuma iestatīšana
-   **Avota/strādājošs uzņēmums (USMF)** – ASV dolāri (USD) tiek izmantoti kā uzskaites un pārskata valūta.
-   **Konsolidēts uzņēmums (CON)** – eiro (EUR) tiek izmantoti kā uzskaites un pārskata valūta.
    -   **Realizētā peļņa** – Virsgrāmatas konts 801500
    -   **Realizētie zaudējumi** – Virsgrāmatas konts 801600
    -   **Nerealizētā peļņa** – Virsgrāmatas konts 801600
    -   **Nerealizētie zaudējumi** – Virsgrāmatas konts 801400

## <a name="original-transactions"></a>Sākotnējās darbības
### <a name="cash-receipt-transactions-in-usmf"></a>Kases ieņēmumu darbības USMF

| Datums       | Virsgrāmatas konts               | Valūta | Apjoms |
|------------|------------------------------|----------|--------|
| 10/11/2020 | 110110 – Skaidra nauda                | USD      | 500    |
| 10/11/2020 | 130100 – Debitoru parādi | USD      | -500   |

## <a name="exchange-rates"></a>Valūtu maiņas kursi

| No valūtas | Uz valūtu | Sākuma datums | Maiņas kurss |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 10/1/2020  | 200           |
| EUR           | USD         | 11/1/2020  | 150           |
| EUR           | USD         | 12/1/2017  | 100           |

## <a name="perform-the-consolidation-for-october-2020"></a>Veikt konsolidāciju par 2020. gada oktobri
### <a name="balances-in-the-consolidation-company"></a>Bilances konsolidētajā uzņēmumā

| Virsgrāmatas konts | Valūta | Summa | Aprēķins    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50%  |
| 130100         | EUR      | -250   | -500 USD × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-november-30-2020"></a>Veikt valūtas pārvērtēšanu kontiem no 2020. gada 1. oktobra līdz 2020. gada 30. novembrim
### <a name="balances-in-the-consolidation-company"></a>Bilances konsolidētajā uzņēmumā

| Virsgrāmatas konts | Valūta | Summa  | Aprēķins                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333,33  | Oriģinālā summa 500 × 66,6667%  |
| 130100         | EUR      | -333,33 | Oriģinālā summa -500 × 66,6667% |
| 801400         | EUR      | 83,33   | 333,33 – 250                       |
| 801600         | EUR      | -83,33  | -333,33 – (-250)                   |

Jūs redzēsiet papildu darbības pārskata valūtas summām.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-december-31-2020"></a>Veikt valūtas pārvērtēšanu kontiem no 2020. gada 1. oktobra līdz 2020. gada 31. decembrim
### <a name="balances-in-the-consolidation-company"></a>Bilances konsolidētajā uzņēmumā

| Virsgrāmatas konts | Valūta | Summa  | Aprēķins                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Oriģinālā summa 500 × 1                           |
| 130100         | EUR      | -500,00 | Oriģinālā summa -500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333,33 = 166.67 166,67 + 83,33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
