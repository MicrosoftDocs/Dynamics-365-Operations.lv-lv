---
title: Valūtas pārvērtēšana konsolidācijas uzņēmumā
description: Šajā tēmā ir aprakstīts, kā konsolidētā uzņēmumā pārvērtēt valūtu.
author: roschlom
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c901d5ccd8c8b2146daa49752b7d8b70bbfca722
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818420"
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

| Datums       | Virsgrāmatas konts               | Valūta | Summa |
|------------|------------------------------|----------|--------|
| 11.10.2015 | 110110 – Skaidra nauda                | USD      | 500    |
| 11.10.2015 | 130100 – Debitoru parādi | USD      | -500   |

## <a name="exchange-rates"></a>Valūtu maiņas kursi

| No valūtas | Uz valūtu | Sākuma datums | Valūtas kurss |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 01.10.2015  | 200           |
| EUR           | USD         | 01.11.2015  | 150           |
| EUR           | USD         | 01.12.2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>Veikt konsolidāciju par 2015. gada oktobri
### <a name="balances-in-the-consolidation-company"></a>Bilances konsolidētajā uzņēmumā

| Virsgrāmatas konts | Valūta | Summa | Aprēķins    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50%  |
| 130100         | EUR      | -250   | -500 USD × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 30. novembrim
### <a name="balances-in-the-consolidation-company"></a>Bilances konsolidētajā uzņēmumā

| Virsgrāmatas konts | Valūta | Summa  | Aprēķins                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333,33  | Oriģinālā summa 500 × 66,6667%  |
| 130100         | EUR      | -333,33 | Oriģinālā summa -500 × 66,6667% |
| 801400         | EUR      | 83,33   | 333,33 – 250                       |
| 801600         | EUR      | -83,33  | -333,33 – (-250)                   |

Jūs redzēsiet papildu darbības pārskata valūtas summām.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Veikt valūtas pārvērtēšanu kontiem no 2015. gada 1. oktobra līdz 2015. gada 31. decembrim
### <a name="balances-in-the-consolidation-company"></a>Bilances konsolidētajā uzņēmumā

| Virsgrāmatas konts | Valūta | Summa  | Aprēķins                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Oriģinālā summa 500 × 1                           |
| 130100         | EUR      | -500,00 | Oriģinālā summa -500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333,33 = 166.67 166,67 + 83,33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]