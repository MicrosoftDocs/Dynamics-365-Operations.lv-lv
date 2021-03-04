---
title: Daļēju debitora maksājumu nosegšana, kam ir vairāki atlaižu periodi
description: Šajā rakstā ir izskaidrots, kā tiek nosegti daļēji debitora maksājumi, ja ir vairāki atlaižu periodi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f4d5178aeb3294fd3b40815bb294a7f2ff08b71
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445486"
---
# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Daļēju debitora maksājumu nosegšana, kam ir vairāki atlaižu periodi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā tiek nosegti daļēji debitora maksājumi, ja ir vairāki atlaižu periodi.

Fabrikam piedāvā debitoram 4031 divus termiņatlaides periodus. Debitors saņem 2 procentu termiņatlaidi, ja rēķins tiek apmaksāts piecu dienu laikā un 1 procenta termiņatlaidi, ja rēķins tiek apmaksāts 14 dienu laikā. Fabrikam piedāvā arī termiņatlaides daļējiem maksājumiem. Nosegšanas parametri atrodas lapā **Debitoru moduļa parametri**.

## <a name="invoice"></a>Rēķins
Arnis debitoram 4031 izrakstīto rēķinu par summu 1000,00 ievada un grāmato 25. jūnijā. Kad viņš pārskata rēķina termiņatlaides, Arnis redz, ka debitors 4031 saņem atlaidi 20,00, ja rēķins tiek apmaksāts līdz 30. jūnijam. Ja rēķins tiek apmaksāts līdz 9. jūlijam, debitors saņem atlaidi 10,00.

| Termiņatlaides datums | Termiņatlaides summa | Summa darījuma valūtā |
|--------------------|----------------------|--------------------------------|
| 30.06.2015          | 20,00                | 980,00                         |
| 09.07.2015           | 10,00                | 990,00                         |
| 25.07.2015          | 0,00                 | 1000,00                       |

Arnijs varat apskatīt šo transakciju lapā **Debitoru darbības**.

| Dokuments   | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance  | Valūta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Rēķins          | 25.06.2015 | 10030   | 1000,00                             |                                       | 1000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Daļēja apmaksa pirms termiņatlaides datuma
28. jūnijā debitors 4031 veic daļēju maksājumu 294,00 apmērā. Tā kā 28. jūnijs ietilpst pirmajā termiņatlaides periodā, debitors izmanto 6,00 atlaidi. Lapā **Transakciju nosegšana** vērtība **Termiņatlaides summa** ir 20,00 un vērtība **Ņemamā termiņatlaides summa** ir 6,00.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10030 | 4031    | 25.06.2015 | 25.07.2015 | 10030   | 1000,00                       | USD      | 294,00           |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā. Ja nemainīsiet vērtību **Nosedzamā summa** uz **294,00**, vērtības **Termiņatlaides summa**, kas tiks rādītas, atšķirsies. Tomēr 6,00 tiks ņemti kā termiņatlaide, grāmatojot maksājumu, jo nosegšana automātiski pielāgo vērtību **Nosedzamā summa**.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 30.06.2015 |
| Termiņatlaides summa         | 20,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | 6,00      |

Pēc tam Arnijs grāmato maksājumu, rēķina bilance ir 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Daļēja apmaksa pirms otrā termiņatlaides datuma
8. jūlijā debitors maksā pārējo rēķina summu. Tiek ņemta 7,00 atlaide (1 procents), jo maksājums tika veikts otrajā termiņatlaides periodā.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10030 | 4031    | 25.06.2015 | 25.07.2015 | 10030   | 700,00                               |                                       | USD      | 693,00           |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015 |
| Termiņatlaides summa         | 30,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 6,00      |
| Ņemamā termiņatlaides summa | 7,00      |

Rēķina bilance tagad ir 0,00. Arnijs apskata informāciju lapā **Debitoru darbības**.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Rēķins          | 25.06.2015 | 10030   | 1000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Maksājums         | 28.06.2015 |         |                                      | 294,00                                | 0,00    | USD      |
| DISC-10030 |  Termiņatlaide   | 28.06.2015 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Maksājums         | 08.07.2015  |         |                                      | 693,00                                | 0,00    | USD      |
| DISC-1031  |  Termiņatlaide   | 08.07.2015  |         |                                      | 7,00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]