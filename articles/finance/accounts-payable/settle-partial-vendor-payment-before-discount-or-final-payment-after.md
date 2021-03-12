---
title: Daļēja maksājuma segšana pirms atlaižu piemērošanas datuma un gala maksājumu pēc atlaižu piemērošanas datuma
description: Šajā rakstā ir izklāstīts scenārijs, kur tiek veikti vairāki daļēji maksājumi, daži no tiem — termiņatlaides periodā, un citi — ārpus termiņatlaides perioda.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a30bd1c032d27405c17388465eb813d6c87c270
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971982"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Daļēja maksājuma segšana pirms atlaižu piemērošanas datuma un gala maksājumu pēc atlaižu piemērošanas datuma

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izklāstīts scenārijs, kur tiek veikti vairāki daļēji maksājumi, daži no tiem — termiņatlaides periodā, un citi — ārpus termiņatlaides perioda.

Fabrikam iegādājas preces no kreditora 3057. Fabrikam saņem 1 procenta termiņatlaidi, ja rēķins tiek apmaksāts 14 dienu laikā. Rēķini ir jāapmaksā 30 dienu laikā. Turklāt kreditors Fabrikam termiņatlaides ļauj saņemt arī par daļējiem maksājumiem. Nosegšanas parametri atrodas lapā **Kreditoru moduļa parametri**.

## <a name="invoice-on-june-25"></a>Rēķins 25. jūnijā
25. jūnijā Eiprila ievada un grāmato rēķinu par summu 1000,00 kreditoram 3057. Eiprila var skatīt šo transakciju lapā **Debitoru transakcijas**.

| Dokuments   | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance   | Valūta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10020 | Rēķins          | 25.06.2015 | 10020   |                                      | 1000,00                              | –1000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Daļējs maksājums 2. jūlijā
2. jūlijā Eiprila vēlas nosegt 300,00 no šī rēķina. Maksājums ir piemērots atlaidei, jo Fabrikam saņem atlaides daļējiem maksājumiem. Tāpēc Eiprila maksā 297,00 un saņem 3,00 atlaidi. Viņa izveido maksājumu žurnālu un ievada rindu kreditoram 3057. Tad viņa atver lapu **Transakciju nosegšana**, lai varētu atzīmēt rēķinu nosegšanai.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | Inv-10020 | 3057    | 25.06.2015 | 25.07.2015 | 10020   | –1000,00                      | USD      | -297,00          |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015 |
| Termiņatlaides summa         | -10,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -3,00     |

Pēc tam Eiprila grāmato maksājumu. Tagad rēķina bilance ir 700,00. Eiprila var skatīt šo transakciju lapā **Debitoru transakcijas**.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rēķins          | 25.06.2015 | 10020   |                                      | 1000,00                              | –700,00 | USD      |
| APP-10020  | Maksājums          | 01.07.2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Termiņatlaide    | 01.07.2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Atlikušais maksājums 15. jūlijā, Izmantot termiņatlaidi = Parasts
Atlikušo rēķinu Eiprila apmaksā 15. jūlijā, kas ir pēc termiņatlaides perioda. Lapā **Nosegt atvērtās transakcijas** laukā **Plānotā termiņatlaide** netiek rādīta nekāda atlaides summa, un vērtība laukā **Termiņatlaides summa** ir **0,00**. Kad Eiprila samaksā atlikušo summu 700,00, netiek saņemta nekāda papildu atlaide.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | Inv-10020 | 3057    | 25.06.2015 | 25.07.2015 | 10020   | –700,00                        | USD      | –700,00          |

Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā. Eiprila var redzēt, ka viņa ir jau saņēmusi 3,00 atlaidi.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015 |
| Termiņatlaides summa         | 0,00      |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | -3,00     |
| Ņemamā termiņatlaides summa | 0,00      |

Pēc tam Eiprila grāmato maksājumu. Kad viņa atver lapu **Kreditoru transakcijas**, viņa redz, ka rēķina bilance ir 0,00. Viņa arī redz, ka pastāv divi maksājumi. Viens maksājums ir par 297,00, un tam ir 3,00 atlaide, un otrs maksājums ir par 700,00.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rēķins          | 25.06.2015 | 10020   |                                      | 1000,00                              | 0,00    | USD      |
| APP-10020  | Maksājums          | 01.07.2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Termiņatlaide    | 01.07.2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Maksājums          | 15.07.2015 |         | 700,00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Atlikušais maksājums 15. jūlijā, Izmantot termiņatlaidi = Vienmēr
Ja kreditors Eiprilai ļauj saņemt atlaidi, lai gan viņa maksā pēc atlaides datuma, vērtību laukā **Izmantot termiņatlaidi** viņa var mainīt uz **Vienmēr**. Iestatījums **Aprēķināt termiņatlaides daļējiem maksājumiem** tiek pārrakstīts, un atlaide tiek saņemta. Maksājuma summa ir 693,00, un atlaide ir atlikušie 7,00.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Atlasīts | Vienmēr            | Inv-10020 | 3057    | 25.06.2015 | 25.07.2015 | 10020   | 700,00                               |                                       | USD      | -693,00          |

Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015 |
| Termiņatlaides summa         | 7,00      |
| Izmantot termiņatlaidi            | Vienmēr    |
| Paņemta termiņatlaides summa          | -3,00     |
| Ņemamā termiņatlaides summa | -7,00     |

Pēc tam Eiprila grāmato maksājumu. Kad viņa atver lapu **Kreditoru transakcijas**, viņa redz, ka rēķina bilance ir 0,00. Viņa arī redz, ka pastāv divi maksājumi. Viens maksājums ir par 297,00, un tam ir 3,00 atlaide, un otrs maksājums ir par 693.00, un tam ir 7,00 atlaide.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Rēķins          | 25.06.2015 | 10020   |                                      | 1000,00                              | 0,00    | USD      |
| APP-10020  | Maksājums          | 01.07.2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Termiņatlaide    | 01.07.2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Maksājums          | 15.07.2015 |         | 693,00                               |                                       | 0,00    | USD      |
| DISC-10021 | Termiņatlaide    | 15.07.2015 |         | 7,00                                 |                                       | 0,00    | USD      |





