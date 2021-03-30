---
title: Termiņatlaides ārpus termiņatlaides perioda piešķiršana
description: Šajā rakstā ir aprakstīti divi scenāriji, kas izskaidro, kā var piemērot termiņatlaidi arī tad, ja maksājums tiek veikts ārpus termiņatlaides perioda.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0df635e78fff1994b9a9e1abc99c67470852ad81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235865"
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
| Atlasīts | Vienmēr            | Rēķ.-10030 | 3052    | 6/28/2015          | 7/12/2015 | 10030   | -2000,00                      | USD      | -1980,00        |

Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2015 |
| Termiņatlaides summa         | -20,00    |
| Izmantot termiņatlaidi            | Vienmēr    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Datums, ko izmantot atlaižu aprēķināšanai = atlasītais datums
Ja gan rēķins, gan maksājums ir iegrāmatots, termiņatlaide vēl aizvien tiek piemērota, ja transakciju segšana tiek veikta lapā **Transakciju nosegšana**. Eiprila maina vērtību laukā **Atlaižu aprēķināšanai izmantojamais datums**, atzīmējot **Atlasītais datums**. Pēc tam viņa ievada datumu — 28. jūnijs, kas atbilst rēķina termiņatlaides periodam. Šis datums tiek izmantots, lai aprēķinātu transakcijas termiņatlaidi. Eiprila redz, ka pēc noklusējuma lapā **Atvērto transakciju segšana** tiek parādīta pilna atlaide par summu 20,00. Rēķina rindā ir redzams, ka nosedzamā summa ir 1980,00.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Termiņatlaides datums | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts un iezīmēts | Parastais            | Rēķ.-10030 | 3052    | 6/28/2015          | 7/12/2015 | 10030   | -2000,00                      | USD      | -1980,00        |
| Atlasīts                 | Parastais            | APST.-10030 | 3052    | 7/15/2015          | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā. Ir piemērota atlaide par summu 20,00, jo nosedzamā rēķina noklusējuma summa ir 1980,00.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2015 |
| Termiņatlaides summa         | -20,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -20,00    |

Eiprila atjaunina vērtību laukā **Nosedzamā summa**, ievadot **500,00**. Laukā **Piešķirtās termiņatlaides summa** tiek aprēķināta vērtība **5,05**.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts un iezīmēts | Parastais            | Rēķ.-10030 | 3052    | 6/28/2015 | 7/12/2015 | 10030   | 2000,00                       | USD      | -500,00          |
| Atlasīts                 | Parastais            | APST.-10030 | 3052    | 7/15/2015 | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā. Laukā **Piešķirtās termiņatlaides summa** ir redzama vērtība **5,05**, jo rēķina nosedzamā summa ir mainīta uz maksājuma summu 500,00.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2015 |
| Termiņatlaides summa         | -20,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]