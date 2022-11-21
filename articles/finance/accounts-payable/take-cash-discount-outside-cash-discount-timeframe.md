---
title: Termiņatlaides ārpus termiņatlaides perioda piešķiršana
description: Šajā rakstā ir aprakstīti divi scenāriji, kas izskaidro, kā var piemērot termiņatlaidi arī tad, ja maksājums tiek veikts ārpus termiņatlaides perioda.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26b1eb5e542acf7496d1a0cf7196716a5de75e4e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780265"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Termiņatlaides ārpus termiņatlaides perioda piešķiršana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti divi scenāriji, kas izskaidro, kā var piemērot termiņatlaidi arī tad, ja maksājums tiek veikts ārpus termiņatlaides perioda.

Eiprila 28. jūnijā izveido kreditoram 3052 rēķinu par summu 2000,00. Ja rēķins tiek apmaksāts 14 dienu laikā, rēķinam tiek piemērota termiņatlaide 1 procenta apmērā.

## <a name="use-cash-discount-option--always"></a>Izmantot termiņatlaides opciju = vienmēr.
Eiprila veic maksājumu 1. jūlijā, bet tas ir pēc atlaides datuma. Eiprila atver lapu **Transakciju nosegšana**, lai skatītu nosedzamās transakcijas. 

Eiprila atzīmē rēķinu kā apmaksājamu. Termiņatlaide netiek piemērota, jo maksājums tiek veikts pēc konkrētā atlaides datuma. Tomēr kreditors ir devis Eiprilai atļauju piemērot termiņatlaidi jebkurā gadījumā. Tāpēc Eiprila maina vērtību laukā **Izmantot termiņatlaidi**, atzīmējot **Vienmēr**.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Termiņatlaides datums | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Vienmēr            | Rēķ.-10030 | 3052    | 6/28/2020          | 7/12/2020 | 10030   | -2000,00                      | USD      | -1980,00        |

Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā.

| Lauks                        | Vērtība     |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2020 |
| Termiņatlaides summa         | -20,00    |
| Izmantot termiņatlaidi            | Vienmēr    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Datums, ko izmantot atlaižu aprēķināšanai = atlasītais datums
Ja gan rēķins, gan maksājums ir iegrāmatots, termiņatlaide vēl aizvien tiek piemērota, ja transakciju segšana tiek veikta lapā **Transakciju nosegšana**. Eiprila maina vērtību laukā **Atlaižu aprēķināšanai izmantojamais datums**, atzīmējot **Atlasītais datums**. Pēc tam viņa ievada datumu — 28. jūnijs, kas atbilst rēķina termiņatlaides periodam. Šis datums tiek izmantots, lai aprēķinātu transakcijas termiņatlaidi. Eiprila redz, ka pēc noklusējuma lapā **Atvērto transakciju segšana** tiek parādīta pilna atlaide par summu 20,00. Rēķina rindā ir redzams, ka nosedzamā summa ir 1980,00.

| Atzīmēt          | Izmantot termiņatlaidi | Dokuments   | Konts | Termiņatlaides datums | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|--------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts un iezīmēts | Parastais    | Rēķ.-10030 | 3052    | 6/28/2020         | 7/12/2020 | 10030   | -2000,00                      | USD      | -1980,00        |
| Atlasīts                 | Parastais    | APST.-10030 | 3052    | 7/15/2020          | 7/15/2020 |         | 500.00                         | USD      | 500.00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības** apakšdaļā. Ir piemērota atlaide par summu 20,00, jo nosedzamā rēķina noklusējuma summa ir 1980,00.

| Lauks                        | Vērtība     |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2020 |
| Termiņatlaides summa         | -20,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -20,00    |

Eiprila atjaunina vērtību laukā **Nosedzamā summa**, ievadot **500,00**. Laukā **Piešķirtās termiņatlaides summa** tiek aprēķināta vērtība **5,05**.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts un iezīmēts | Parastais            | Rēķ.-10030 | 3052    | 6/28/2020 | 7/12/2020 | 10030   | 2,000.00                       | USD      | -500,00          |
| Atlasīts                 | Parastais            | APST.-10030 | 3052    | 7/15/2020 | 7/15/2020 |         | 500.00                         | USD      | 500.00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības** apakšdaļā. Laukā **Piešķirtās termiņatlaides summa** ir redzama vērtība **5,05**, jo rēķina nosedzamā summa ir mainīta uz maksājuma summu 500,00.

| Lauks                        | Vērtība     |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2020 |
| Termiņatlaides summa         | -20,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
