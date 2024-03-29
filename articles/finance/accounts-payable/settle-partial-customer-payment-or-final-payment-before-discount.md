---
title: Daļēja un gala maksājumu pilnā apmērā segšana pirms atlaižu piemērošanas datuma
description: Šajā rakstā ir aprakstīti scenāriji, kas izskaidro, kā reģistrēt daļējus debitora maksājumus un termiņatlaides termiņā aprēķināt termiņatlaides.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
ms.openlocfilehash: a8da366b1e770ea649603ae85d4acc5e377ed9fb
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780250"
---
# <a name="settle-partial-and-final-payments-in-full-before-the-discount-date"></a>Daļēja un gala maksājumu pilnā apmērā segšana pirms atlaižu piemērošanas datuma

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti scenāriji, kas izskaidro, kā reģistrēt daļējus debitora maksājumus un termiņatlaides termiņā aprēķināt termiņatlaides.

Fabrikam pārdod preces debitoram 4028. Fabrikam piedāvā termiņatlaidi 1 procenta apmērā, ja rēķins tiek apmaksāts 14 dienu laikā. Rēķini ir jāapmaksā 30 dienu laikā. Fabrikam piedāvā arī termiņatlaides daļējiem maksājumiem. Nosegšanas parametri atrodas lapā **Debitoru moduļa parametri**.

## <a name="customer-invoice"></a>Debitora rēķins
Arnis debitoram 4028 izrakstīto rēķinu par summu 1000,00 ievada un grāmato 25. jūnijā. Arnijs varat apskatīt šo transakciju lapā **Debitoru darbības**.

| Dokuments   | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance  | Valūta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Rēķins          | 6/25/2020 | 10010   | 1,000.00                             |                                       | 1,000.00 | USD      |

Izmantojot lapu **Debitors** vai **Debitora transakcijas**, Arnis var atvērt lapu **Veikt transakcijas**, lai skatītu uz rēķinu attiecināto termiņatlaižu datumus un summas. Rēķina apmaksas datums ir 25. jūlijs, un termiņatlaide par summu 10,00 ir pieejama tad, ja rēķins tiek apmaksāts līdz 9. jūlijam.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10010 | 4028    | 6/25/2020 | 7/25/2020 | 10010   | 1,000.00                       | USD      | 990.00           |

Atlaides dati ir redzami atzīmēta rēķina lapas **Veikt transakcijas** apakšā.

|    &nbsp;                    |  &nbsp;   |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/09/2020 |
| Termiņatlaides summa         | 10,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | 10,00     |

Lai redzētu atlaides summu, Arnis noklikšķina uz cilnes **Termiņatlaide**.

| Termiņatlaides datums | Termiņatlaides summa | Summa darījuma valūtā |
|--------------------|----------------------|--------------------------------|
| 7/9/2020           | 10,00                | 990.00                         |
| 7/25/2020          | 0,00                 | 1,000.00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Daļējs maksājums, izmantojot lapu Debitora maksājumu ievadīšana
Debitors 4028 veic maksājumu par summu 500,00 1. jūlijā. Lai ievadītu šo maksājumu, Arnis nenoklikšķina uz vienuma **Rindas**. Tā vietā Arnijs izveido jaunu maksājumu žurnālu, lai reģistrētu maksājumu, un pēc tam atver lapu **Ievadīt debitora maksājumus**. Arnijs ievada maksājuma datus un atzīmē rēķinu, kā ievadītu. Ievadot summu **500,00**, viņi ievada arī summu **500,00** lauka **Apmaksājamā summa** režģī. Tā kā uzņēmums Fabrikam piedāvā termiņatlaidi daļējiem maksājumiem, Arnijs redz, ka spēkā stājas arī daļējā termiņatlaide par summu 5,05. Atlaide aprēķināta šādi: 500,00 ÷ 0,99 × 0,01 = 5,05. (Šajā aprēķinā summa 500,00 tiek dalīta ar 0,99, jo ir spēkā atlaide 1 procenta apmērā. Līdz ar to debitors apmaksā 99 procentus no rēķina summas. Rezultāts pēc tam tiek reizināts ar atlaides procentuālo summu, kas ir 1 procents vai 0,01. Ja debitoram ir piešķirta pilna atlaide par summu 10,00, nosedzamā summa ir 990,00.) Atlaides dati ir redzami režģī lapas **Ievadīt debitora maksājumus** apakšā.

| Ņemamā termiņatlaides summa | Paņemta termiņatlaides summa | Izmaksājamā summa |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Daļējais maksājums, izmantojot žurnāla rindas
Arnis neatver lapu **Ievadīt debitora maksājumus** maksājumu žurnālā, bet noklikšķina uz vienuma **Rindas**, lai ievadītu maksājumu. Tiek parādīts maksājumu žurnāls, kur Arnis var ievadīt debitora 4028 rindu. Pēc tam Arnijs atver lapu **Transakciju nosegšana**, lai varētu atzīmēt nosedzamo rēķinu. Arnis atzīmē rēķinu un laukā **Nosedzamā summa** ievada summu **500,00**. Arnijs tātad redz, ka laukā **Termiņatlaides summa** norādītā summa **10,00** attiecas uz visu rēķina summu, bet vērtība laukā **Piešķirtās termiņatlaides summa** ir **5,05**. Tāpēc Arnis šā rēķina nosegšanai norāda summu 505,05.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10010 | 4028    | 6/25/2020 | 7/25/2020 | 10010   | 1,000.00                       | USD      | 500.00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības** apakšdaļā.

|        &nbsp;                | &nbsp;    |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/09/2020 |
| Termiņatlaides summa         | 10,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | 5,05      |

Ja debitors vēlas nosegt tieši pusi no rēķina summas, viņš veic maksājumu par summu 495,00. Šajā gadījumā Arnis ievada summu **495,00** laukā **Nosedzamā summa**. Spēkā stājas arī termiņatlaide par summu 5,00, līdz ar to kopējā nosedzamā summa 500,00.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10010 | 4028    | 6/25/2020 | 7/25/2020 | 10010   | 1,000.00                       | USD      | 495,00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības** apakšdaļā.

|     &nbsp;                   | &nbsp;    |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/09/2020 |
| Termiņatlaides summa         | 10,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | 5,00      |

Arnis aizver lapu **Nosegt transakcijas**. Žurnālā tiek izveidota maksājuma rinda par summu 495,00, un pēc tam Arnis iegrāmato žurnālu. Debitora transakcijas Arnijs var pārskatīt lapā **Debitora transakcijas**. Šajā lapā Arnis redz, ka rēķina atlikusī summa ir 500,00. Arnijs arī redz, ka maksājuma summa ir 495,00 un atlaide ir 5,00.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Rēķins          | 6/25/2020 | 10010   | 1,000.00                             |                                       | 500.00  | USD      |
| ARP-10010  |  Maksājums         | 7/1/2020  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 |  Termiņatlaide   | 7/1/2020  |         |                                      | 5.00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Maksājums par atlikušo summu
Debitors 4028 veic maksājumu par atlikušo summu 495,00 apmērā 8. jūlijā, kas atbilst termiņatlaides periodam. Arnis 8. jūlijā izveido maksājumu žurnālu un atzīmē nosedzamo transakciju. Arnijs redz, ka nosedzamā summa ir 495,00. Laukā **Aprēķinātā termiņatlaide** ir norādīta summa **5,00**, jo iepriekš tika piešķirta atlaide par summu 5,00.

|   &nbsp;                | &nbsp; |
|-------------------------|--------|
| Kopā iezīmēts            | 495,00 |
| Plānotā termiņatlaide | 5,00   |

Informācija par iezīmēto transakciju parādās režģī laukā **Nosegt atvērtās darbības**.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10010 | 4028    | 6/25/2020 | 7/25/2020 | 10010   | 1,000.00                       | USD      | 495,00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības** apakšdaļā.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/09/2020 |
| Termiņatlaides summa         | 10,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 5,00      |
| Ņemamā termiņatlaides summa | 5,00      |

Arnis iegrāmato žurnālu un pārskata debitora transakcijas lapā **Debitora transakcijas**. Atlikusī rēķina summa tagad ir 0,00, un Arnis redz divus veiktos maksājumus divas piešķirtās termiņatlaides.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Rēķins          | 6/25/2020 | 10010   | 1,000.00                             |                                       | 0,00    | USD      |
| ARP-10010  | Maksājums          | 7/1/2020  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 | Termiņatlaide    | 7/1/2020  |         |                                      | 5.00                                  | 0,00    | USD      |
| ARP-10011  | Maksājums          | 7/8/2020  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10011 | Termiņatlaide    | 7/8/2020  |         |                                      | 5.00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
