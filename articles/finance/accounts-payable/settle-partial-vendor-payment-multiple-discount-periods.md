---
title: Daļēju kreditora maksājumu nosegšana, kam ir vairāki atlaižu periodi
description: Šajā rakstā ir aprakstīts scenārijs, kurā tiek veikti vairāki daļējie maksājumi kreditoram, kas piedāvā vairākas termiņatlaides.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56e2b3a8dadd824fa0170a1db19fffeaecb47775
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827870"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Daļēju kreditora maksājumu nosegšana, kam ir vairāki atlaižu periodi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts scenārijs, kurā tiek veikti vairāki daļējie maksājumi kreditoram, kas piedāvā vairākas termiņatlaides. 

Kreditors 3054 piedāvā uzņēmumam Fabrikam termiņatlaidi 2 procentu apmērā, ja rēķins tiek apmaksāts piecu dienu laikā, un termiņatlaidi 1 procenta apmērā, ja rēķins tiek apmaksāts 14 dienu laikā.

## <a name="invoice"></a>Rēķins
Eiprila 28. jūnijā izveido kreditoram 3054 rēķinu par summu 1000,00. Eiprila var skatīt šo transakciju lapā **Debitoru transakcijas**.

| Dokuments   | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance   | Valūta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10060 | 28.06.2015 | 10060   |                                      | 1000,00                              | –1000,00 | USD      |

Šim rēķinam ir pieejami tālāk norādītie termiņatlaides datumi un summas.

| Termiņatlaides datums | Termiņatlaides summa | Summa darījuma valūtā |
|--------------------|----------------------|--------------------------------|
| 03.07.2015           | 20,00                | 980,00                         |
| 12.07.2015          | 10,00                | 990,00                         |
| 25.07.2015          | 0,00                 | 1000,00                       |

## <a name="payment-on-july-2"></a>Maksājums 2. jūlijā
2. jūlijā Eiprila vēlas samaksāt summu 300,00 par šo rēķinu. Viņa izveido vienreizēju maksājumu, izmantojot moduļa Kreditoru parādi lapu **Maksājumu žurnāls**. Viņa pievieno rindu kreditoram 3054 un ievada maksājuma summu **300,00**. Pēc tam Eiprila atver lapu **Transakciju nosegšana**, lai varētu iezīmēt apmaksājamo rēķinu. Viņa atjaunina lauka **Nosedzamā summa** vērtību uz **300,00** un pamana, ka lauka **Ņemamā termiņatlaides summa** vērtība tiek mainīta uz **6,12**. Tā kā šis maksājums tiek veikts pirmajā atlaides periodā, tiek lietota atlaide 2 procentu apmēra.

| Atzīmēt | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Parastais            | Inv-10060 | 3054    | 28.06.2015 | 28.07.2015 | 10060   | 1000,00                       | USD      | 300,00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības** apakšdaļā.

| Lauks                        | Vērtība     |
|------------------------------|-----------|
| Termiņatlaides datums           | 02.07.2015 |
| Termiņatlaides summa         | -20,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | –6,12     |

Tā kā ir pieejama termiņatlaide, Eiprila vēlas mainīt maksājuma summu, lai kopējā segtā summa būtu 300,00 gan maksājumam, gan termiņatlaidei. Viņa maina lauka **Nosedzamā summa** vērtību uz **294,00** un pamana, ka lauka **Ņemamā termiņatlaides summa** vērtība tiek mainīta uz **6,00**.

| Atzīmēt | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Parastais            | Inv-10060 | 3054    | 28.06.2015 | 28.07.2015 | 10060   | 1000,00                       | USD      | 294,00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības** apakšdaļā.

| Lauks                        | Vērtība     |
|------------------------------|-----------|
| Termiņatlaides datums           | 02.07.2015 |
| Termiņatlaides summa         | -20,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | –6,00     |

Eiprila grāmato maksājumu. Viņa var skatīt transakcijas lapā **Debitoru darbības**. Viņa redz, ka rēķinam ir lietota summa 300,00. Šajā summā ir iekļauta termiņatlaide 6,00 ampērā. Tāpēc atlikusī bilance ir 700,00.

| Dokuments    | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28.06.2015 | 10060   |                                      | 1000,00                              | –700,00 | USD      |
| APP-10060  | 02.07.2015  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 02.07.2015  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Maksājums 8. jūlijā
8. jūlijā Eiprila veic papildu maksājumu par rēķinu. Lai ievadītu summu, viņa atver lapu **Transakciju nosegšana** un pēc tam noklikšķina uz cilnes **Termiņatlaide**. Viņa redz abu pieejamo termiņatlaižu datumus un summas. Tā kā šis maksājums tiek veikts otrajā atlaides periodā, ir pieejama atlaide 1 procenta vai 5,00 apmērā. Šī summa tiek aprēķināta kā puse no 1 procenta atlaides summai 1000,00 vai puse no 10,00.

| Termiņatlaides datums | Termiņatlaides summa | Summa darījuma valūtā |
|--------------------|----------------------|--------------------------------|
| 03.07.2015           | 20,00                | 680,00                         |
| 12.07.2015          | 10,00                | 690,00                         |
| 25.07.2015          | 0,00                 | 700,00                         |

Eiprila izlemj maksāt summu 495,00 un saņemt termiņatlaidi 5,00 apmērā. Tāpēc kopējā segtā summa ir 500,00.

| Atzīmēt | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Parastais            | Inv-10060 | 3054    | 28.06.2015 | 28.07.2015 | 10060   | 1000,00                       | USD      | 495,00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības** apakšdaļā.

| Lauks                        | Vērtība     |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2015 |
| Termiņatlaides summa         | -10,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | –6,00     |
| Ņemamā termiņatlaides summa | -5,00     |

Lapā **Kreditoru darbības** Eiprila redz, ka jaunā bilance ir 200,00.

| Dokuments    | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28.06.2015 | 10060   |                                      | 1000,00                              | –200,00 | USD      |
| APP-10060  | 02.07.2015  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 02.07.2015  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 12.07.2015 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 12.07.2015 |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Maksājums 20. jūlijā
20. jūlijā Eiprila izveido beidzamo maksājumu 200,00 apmērā. Netiek lietota nekāda atlaide, jo maksājums tiek veikts pēc abiem atlaižu periodiem. Rēķina bilance ir 0,00.

| Dokuments    | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28.06.2015 | 10060   |                                      | 1000,00                              | –200,00 | USD      |
| APP-10060  | 02.07.2015  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 02.07.2015  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 12.07.2015 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 12.07.2015 |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10062  | 20.07.2015 |         | 200,00                               |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]