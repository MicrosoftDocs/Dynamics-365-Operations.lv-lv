---
title: Viena maksājuma lietošana, lai nosegtu rēķinus ar vairākiem atlaižu periodiem
description: Šajā rakstā ir izskaidrots, kā vairāki rēķini tiek apmaksāti, ja katram rēķinam var piemērot termiņatlaidi. Šajā rakstā aprakstītajā scenārijā galvenā uzmanība pievērsta termiņatlaidēm, kas tiek piemērotas atkarībā no maksājuma veikšanas laika.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bf321a5b0511295f2500f10cdffa9ff6f043bff
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780271"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Viena maksājuma lietošana, lai nosegtu rēķinus ar vairākiem atlaižu periodiem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā vairāki rēķini tiek apmaksāti, ja katram rēķinam var piemērot termiņatlaidi. Šajā rakstā aprakstītajā scenārijā galvenā uzmanība pievērsta termiņatlaidēm, kas tiek piemērotas atkarībā no maksājuma veikšanas laika.

Fabrikam pārdod preces debitoram 4032. Fabrikam piedāvā termiņatlaidi 1 procenta apmērā, ja rēķins tiek apmaksāts 14 dienu laikā. Fabrikam piedāvā arī termiņatlaides daļējiem maksājumiem. Nosegšanas parametri atrodas lapā **Debitoru moduļa parametri**.

## <a name="invoices"></a>Rēķini
Debitoram 4032 ir trīs rēķini, kuru kopsumma ir 3000,00.

-   Rēķins FTI-10040 par summu 1000,00 tika ievadīts 15. maijā. Šis rēķins ir piemērots termiņatlaides saņemšanai 1 procenta apmērā, ja tas tiek apmaksāts 14 dienu laikā.
-   Rēķins FTI-10041 par summu 1000,00 tika ievadīts 25. jūnijā. Šis rēķins ir piemērots termiņatlaides saņemšanai 1 procenta apmērā, ja tas tiek apmaksāts 14 dienu laikā.
-   Rēķins FTI-10042 par summu 1000,00 tika ievadīts 25. jūnijā. Šis rēķins ir piemērots termiņatlaides saņemšanai 2 procentu apmērā, ja tas tiek apmaksāts piecu dienu laikā, un 1 procenta apmērā, ja tas tiek apmaksāts 14 dienu laikā.

## <a name="settle-all-invoices-on-june-29"></a>Visu rēķinu apmaksa 29. jūnijā
Ja Ārnijs izveido maksājumu žurnālu, lai pilnībā apmaksātu šos rēķinus 29. jūnijā, maksājuma summa ir 2970,00. Visu atlaižu kopsumma ir 30,00. Ārnijs izveido maksājumu debitoram 4032 un pēc tam atver lapu **Transakciju nosegšana**. Lapā **Transakciju nosegšana** Ārnijs atzīmē visas trīs rēķinu rindas segšanai.

-   Rēķina FTI-10040 apmaksas summa ir 1000,00. Netiek lietota termiņatlaide.
-   Rēķina FTI-10041 apmaksas summa ir 990,00. Tiek lietota termiņatlaide 1 procenta vai 10,00 apmērā.
-   Rēķina FTI-10042 apmaksas summa ir 980,00. Tiek lietota termiņatlaide 2 procentu vai 20,00 apmērā.

| Atzīmēt | Izmantot termiņatlaidi | Dokuments   | Konts | Datums   | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|------|----------|-----------|---------|-----------|-----------|---------|---------------------|---------------------|----------|------------------|
| Atlasīts     | Parastais      | FTI-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00  |                    | USD      | 1,000.00         |
| Atlasīts     | Parastais      | FTI-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00  |                    | USD      | 990.00           |
| Atlasīts un iezīmēts | Parastais      | FTI-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00    |              | USD      | 980.00           |

Pēc maksājuma grāmatošanas debitora bilance ir 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Visu rēķinu apmaksa 1. jūlijā
Ja Ārnijs izveido maksājumu žurnālu, lai pilnībā apmaksātu šos rēķinus 1. jūlijā, maksājuma summa ir 2980,00. Ārnijs izveido maksājumu debitoram 4032 un pēc tam atver lapu **Transakciju nosegšana**. Lapā **Transakciju nosegšana** Ārnijs atzīmē visas trīs rēķinu rindas segšanai.

-   Rēķina FTI-10040 apmaksas summa ir 1000,00. Netiek lietota termiņatlaide.
-   Rēķina FTI-10041 apmaksas summa ir 990,00. Tiek lietota termiņatlaide 1 procenta vai 10,00 apmērā.
-   Rēķina FTI-10042 apmaksas summa ir 990,00. Tiek lietota termiņatlaide 1 procenta vai 10,00 apmērā. Lai gan 1. jūlijs ir pēc perioda, kad ir pieejama atlaide 2 procentu apmērā, tas joprojām ir periodā, kad ir pieejama atlaide 1 procenta apmērā.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|----------|---------|-----------|---------|-----------|-----------|---------|--------------------|------------------|----------|------------------|
| Atlasīts         | Parastais            | FTI-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00         |                | USD      | 1,000.00         |
| Atlasīts                 | Parastais            | FTI-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00  |               | USD      | 990.00           |
| Atlasīts un iezīmēts | Parastais            | FTI-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00  |             | USD      | 990.00           |

## <a name="partial-settlement-on-june-29"></a>Daļēja segšana 29. jūnijā
Debitors 4032 var maksāt daļēju summu, piemēram, puse no katra rēķina summas. Ārnijs izveido maksājumu debitoram 4032 un pēc tam atver lapu **Transakciju nosegšana**. Lapā **Transakciju nosegšana** Ārnijs atzīmē visas trīs rēķinu rindas segšanai. Katrā rindā Ārnijs ievada sedzamo summu, pamatojoties uz debitora sniegtajiem norādījumiem. Kad Ārnijs atlasa rindu, viņš redz šīs rindas atlaides summu un izmantoto termiņatlaides summu. Tā kā debitors apmaksā pusi no rēķina summas, Ārnijs redz, ka rēķina FTI-10042 lauka **Termiņatlaides summa** vērtība ir **20,00**, bet lauka **Paņemta termiņatlaides summa** vērtība ir **10,00**. Maksājuma summa ir 1485,00.

| Atzīmēt   | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|-------------|-------------------|-----------|---------|-----------|-----------|---------|-----------|------------------|----------|------------------|
| Atlasīts   | Parastais       | FTI-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00        |               | USD      | 500.00           |
| Atlasīts                 | Parastais            | FTI-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00     |     | USD      | 495,00           |
| Atlasīts un iezīmēts | Parastais            | FTI-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00     |         | USD      | 490,00           |

Ārnijs var arī manuāli ievadīt maksājuma summu 1485,00, pirms viņš **Nosegt transakcijas** lapas atvēršanas. Ja Ārnijs maksājuma summu ievada manuāli un pēc tam atzīmē visas trīs transakcijas, bet nekoriģē katras transakcijas lauka **Nosedzamā summa** vērtību, tad viņš, aizverot lapu, saņem tālāk norādīto ziņojumu.

> Iezīmēto darbību kopsumma atšķiras no žurnāla summas. Mainīt žurnāla summu?

Ja Ārnijs vēlas, lai maksājuma summa būtu tikai 1485,00, viņš noklikšķina uz **Nē** un pēc tam grāmato žurnālu. Transakcijas tiek segtas tālāk norādītajā veidā.

1.  Rēķins FTI-10040 tiek pilnībā apmaksāts par summu 1000,00, jo tas tika ievadīts 15. maijā un ir vecākais rēķins. Netiek lietota termiņatlaide. Atlikusī maksājuma transakcijas summa ir 485,00.
2.  Rēķins FTI-10041 netiek apmaksāts vispār. Rēķini FTI-10041 un FTI-10042 tika ievadīti vienā datumā. Taču rēķinam FTI-10041 ir pieejama atlaide 1 procenta apmērā, bet rēķinam FTI-10042 ir pieejama atlaide 2 procentu apmērā. Tā kā rēķinam FTI-10042 ir pieejama lielāka atlaide, atlikusī summa 485,00 tiek izmantota rēķina FTI-10042 apmaksai.
3.  Rēķins FTI-10042 tiek apmaksāts par atlikušo summu 485,00. Fabrikam piedāvā daļējas atlaides. Šajā gadījumā atlaide ir 9,90 (= 485,00 ÷ 0,98 × 0,02). Summa (485,00) tiek dalīta ar 0,98, jo pastāv atlaide 2 procentu apmērā (tāpēc debitors maksā 98 procentus no rēķina summas). Pēc tam rezultāts tiek reizināts ar atlaides procentuālo vērtību jeb 2 procentiem. Maksājuma summa 485,00 un atlaides summa 9,90 kopā veido summu 494,90. Sākotnējā rēķina summa bija 1000,00. Tāpēc transakcijas bilance ir 505,10 (= 1000,00 – 494,90).

Arnijs apskata informāciju lapā **Debitoru darbības**.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance  | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Rēķins          | 5/15/2020 | 10040   | 1,000.00                             |                                       | 0,00     | USD      |
| FTI-10041  | Rēķins          | 6/25/2020 | 10041   | 1,000.00                             |                                       | 1,000.00 | USD      |
| FTI-10042  | Rēķins          | 6/25/2020 | 10042   | 1,000.00                             |                                       | 505,10   | USD      |
| ARP-10040  | Maksājums          | 6/29/2020 |         |                                      | 1485,00                              | 0,00     | USD      |
| DISC-10040 | Termiņatlaide    | 6/29/2020 |         |                                      | 9,90                                  | 0,00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
