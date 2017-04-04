---
title: "Izmantot klientu maksājumu, lai atrisinātu vairākus rēķinus, kas aptver vairāku atlaižu periodus"
description: "Šajā rakstā ir izskaidrots, kā vairāki rēķini tiek apmaksāti, ja katram rēķinam var piemērot termiņatlaidi. Šajā rakstā aprakstītajā scenārijā galvenā uzmanība pievērsta termiņatlaidēm, kas tiek piemērotas atkarībā no maksājuma veikšanas laika."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6fd78a587d70ec371861084ac9f76b439c821a8f
ms.lasthandoff: 03/31/2017


---

# <a name="use-a-customer-payment-to-settle-multiple-invoices-that-span-multiple-discount-periods"></a>Izmantot klientu maksājumu, lai atrisinātu vairākus rēķinus, kas aptver vairāku atlaižu periodus

Šajā rakstā ir izskaidrots, kā vairāki rēķini tiek apmaksāti, ja katram rēķinam var piemērot termiņatlaidi. Šajā rakstā aprakstītajā scenārijā galvenā uzmanība pievērsta termiņatlaidēm, kas tiek piemērotas atkarībā no maksājuma veikšanas laika.

Fabrikam pārdod preces klientam 4032. Fabrikam piedāvā 1 procentu termiņatlaide, ja rēķins ir apmaksāts 14 dienu laikā. Fabrikam piedāvā arī termiņatlaides daļējiem maksājumiem. Settement parametrus, kas atrodas **Accounts receivable parameters** lapā.

## <a name="invoices"></a>Rēķini
Debitoram 4032 ir trīs rēķini, kuru kopsumma ir 3000,00.

-   Rēķinu FTI-10040, 1000,00, tika ierakstīts 15. maijs. Šis rēķins ir piemērota termiņatlaide, 1 procents, ja tā ir samaksāta 14 dienu laikā.
-   25. jūnijā tika ievadīts rēķina FTI-10041, 1000,00. Šis rēķins ir piemērota termiņatlaide, 1 procents, ja tā ir samaksāta 14 dienu laikā.
-   25. jūnijā tika ievadīts rēķina FTI-10042, 1000,00. Šis rēķins ir piemērota 2 procentu termiņatlaide, ja tas izmaksā piecu dienu un 1 procentu atlaidi, ja tā ir samaksāta 14 dienu laikā.

## <a name="settle-all-invoices-on-june-29"></a>Visu rēķinu apmaksa 29. jūnijā
Ja Ārnijs izveido maksājumu žurnālu, lai pilnībā apmaksātu šos rēķinus 29. jūnijā, maksājuma summa ir 2970,00. Visu atlaižu kopsumma ir 30,00. Ārnijs izveido maksājumu debitoram 4032 un pēc tam atver lapu **Transakciju nosegšana**. Lapā **Transakciju nosegšana** Ārnijs atzīmē visas trīs rēķinu rindas segšanai.

-   Rēķina FTI-10040 apmaksas summa ir 1000,00. Netiek lietota termiņatlaide.
-   Rēķina FTI-10041 apmaksas summa ir 990,00. Tiek lietota termiņatlaide 1 procenta vai 10,00 apmērā.
-   Rēķina FTI-10042 apmaksas summa ir 980,00. Tiek lietota termiņatlaide 2 procentu vai 20,00 apmērā.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Atlasīts                 | Parastais            | FTI-10040 | 4032    | 15.05.2015 | 15.06.2015 | 10040   | 1000,00                             |                                       | USD      | 1000,00         |
| Atlasīts                 | Parastais            | FTI-10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1000,00                             |                                       | USD      | 990,00           |
| Atlasīts un iezīmēts | Parastais            | FTI-10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1000,00                             |                                       | USD      | 980,00           |

Pēc maksājuma grāmatošanas debitora bilance ir 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Visu rēķinu apmaksa 1. jūlijā
Ja Ārnijs izveido maksājumu žurnālu, lai pilnībā apmaksātu šos rēķinus 1. jūlijā, maksājuma summa ir 2980,00. Ārnijs izveido maksājumu debitoram 4032 un pēc tam atver lapu **Transakciju nosegšana**. Lapā **Transakciju nosegšana** Ārnijs atzīmē visas trīs rēķinu rindas segšanai.

-   Rēķina FTI-10040 apmaksas summa ir 1000,00. Netiek lietota termiņatlaide.
-   Rēķina FTI-10041 apmaksas summa ir 990,00. Tiek lietota termiņatlaide 1 procenta vai 10,00 apmērā.
-   Rēķina FTI-10042 apmaksas summa ir 990,00. Tiek lietota termiņatlaide 1 procenta vai 10,00 apmērā. Lai gan 1. jūlijs ir pēc perioda, kad ir pieejama atlaide 2 procentu apmērā, tas joprojām ir periodā, kad ir pieejama atlaide 1 procenta apmērā.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Atlasīts                 | Parastais            | FTI-10040 | 4032    | 15.05.2015 | 15.06.2015 | 10040   | 1000,00                             |                                       | USD      | 1000,00         |
| Atlasīts                 | Parastais            | FTI-10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1000,00                             |                                       | USD      | 990,00           |
| Atlasīts un iezīmēts | Parastais            | FTI-10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Daļēja segšana 29. jūnijā
Debitors 4032 var maksāt daļēju summu, piemēram, puse no katra rēķina summas. Ārnijs izveido maksājumu debitoram 4032 un pēc tam atver lapu **Transakciju nosegšana**. Lapā **Transakciju nosegšana** Ārnijs atzīmē visas trīs rēķinu rindas segšanai. Katrā rindā viņš ievada sedzamo summu, pamatojoties uz debitora sniegtajiem norādījumiem. Kad Ārnijs atlasa rindu, viņš redz šīs rindas atlaides summu un izmantoto termiņatlaides summu. Tā kā debitors apmaksā pusi no rēķina summas, Ārnijs redz, ka rēķina FTI-10042 lauka **Termiņatlaides summa** vērtība ir **20,00**, bet lauka **Paņemta termiņatlaides summa** vērtība ir **10,00**. Maksājuma summa ir 1485,00.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Atlasīts                 | Parastais            | FTI-10040 | 4032    | 15.05.2015 | 15.06.2015 | 10040   | 1000,00                             |                                       | USD      | 500,00           |
| Atlasīts                 | Parastais            | FTI-10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1000,00                             |                                       | USD      | 495,00           |
| Atlasīts un iezīmēts | Parastais            | FTI-10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1000,00                             |                                       | USD      | 490,00           |

Arnie arī manuāli ievadiet maksājuma summu 1,485.00, pirms viņš atver **norēķiniem par darījumiem** lapā. Ja Arnie manuāli ievada maksājuma summu un pēc tam atzīmē visas trīs darbības, bet viņš nav koriģētu vērtību **apjoms, lai nokārtotu** lauks katrai darbībai, viņš saņem šādu ziņojumu, aizverot lappusi:

> Iezīmēto darbību kopsumma atšķiras no žurnāla summas. Mainīt žurnāla summu?

Ja Ārnijs vēlas, lai maksājuma summa būtu tikai 1485,00, viņš noklikšķina uz **Nē** un pēc tam grāmato žurnālu. Transakcijas tiek segtas tālāk norādītajā veidā.

1.  Rēķins FTI-10040 tiek pilnībā apmaksāts par summu 1000,00, jo tas tika ievadīts 15. maijā un ir vecākais rēķins. Netiek lietota termiņatlaide. Atlikusī maksājuma transakcijas summa ir 485,00.
2.  Rēķins FTI-10041 netiek apmaksāts vispār. Rēķini FTI-10041 un FTI-10042 tika ievadīti vienā datumā. Taču rēķinam FTI-10041 ir pieejama atlaide 1 procenta apmērā, bet rēķinam FTI-10042 ir pieejama atlaide 2 procentu apmērā. Tā kā rēķinam FTI-10042 ir pieejama lielāka atlaide, atlikusī summa 485,00 tiek izmantota rēķina FTI-10042 apmaksai.
3.  Rēķins FTI-10042 tiek apmaksāts par atlikušo summu 485,00. Fabrikam piedāvā daļējas atlaides. Šajā gadījumā atlaide ir 9,90 (= 485,00 ÷ 0,98 × 0,02). Summa (485,00) tiek dalīta ar 0,98, jo pastāv atlaide 2 procentu apmērā (tāpēc debitors maksā 98 procentus no rēķina summas). Pēc tam rezultāts tiek reizināts ar atlaides procentuālo vērtību jeb 2 procentiem. Maksājuma summa 485,00 un atlaides summa 9,90 kopā veido summu 494,90. Sākotnējā rēķina summa bija 1000,00. Tāpēc transakcijas bilance ir 505,10 (= 1000,00 – 494,90).

Arnijs apskata informāciju lapā **Debitoru darbības**.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance  | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Rēķins          | 15.05.2015 | 10040   | 1000,00                             |                                       | 0,00     | USD      |
| FTI-10041  | Rēķins          | 25.06.2015 | 10041   | 1000,00                             |                                       | 1000,00 | USD      |
| FTI-10042  | Rēķins          | 25.06.2015 | 10042   | 1000,00                             |                                       | 505,10   | USD      |
| ARP-10040  | Maksājums          | 29.06.2015 |         |                                      | 1485,00                              | 0,00     | USD      |
| DISC-10040 | Termiņatlaide    | 29.06.2015 |         |                                      | 9,90                                  | 0,00     | USD      |




