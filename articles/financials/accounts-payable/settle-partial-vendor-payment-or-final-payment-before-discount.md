---
title: Daļēja kreditora maksājuma segšana un galīgā maksājuma segšana par pilnu summu pirms atlaides datuma
description: Šajā rakstā ir aprakstīts scenārijs, kurā tiek veikti daļēji maksājumi pēc kreditora rēķina un tiek pielāgota termiņatlaide.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6189d5de80a4b0b157797c1fdd072a8ee86857f3
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1508972"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Daļēja kreditora maksājuma segšana un galīgā maksājuma segšana par pilnu summu pirms atlaides datuma

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts scenārijs, kurā tiek veikti daļēji maksājumi pēc kreditora rēķina un tiek pielāgota termiņatlaide.

Fabrikam pērk preces no kreditora 3064. Kreditors dod Fabrikam 1 procenta termiņatlaidi, ja rēķins tiek apmaksāts 14 dienu laikā. Rēķini ir jāapmaksā 30 dienu laikā. Turklāt kreditors Fabrikam termiņatlaides ļauj saņemt arī par daļējiem maksājumiem. Nosegšanas parametri atrodas lapā **Kreditoru moduļa parametri**. 25. jūnijā Eiprila ievada rēķinu par summu 1000,00 kreditoram 3064.

## <a name="vendor-invoice-on-june-25"></a>Kreditora rēķins 25. jūnijā
25. jūnijā Eiprila ievada un grāmato rēķinu par summu 1000,00 kreditoram 3064. Eiprila var skatīt šo transakciju lapā **Debitoru transakcijas**.

| Dokuments   | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance   | Valūta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10010 | 25.06.2015 | 10010   |                                      | 1000,00                              | -1000,00 | USD      |

No lapas **Kreditori** Eiprila atver lapu **Transakciju nosegšana**. Viņa var izmantot lapu **Transakciju nosegšana**, lai skatītu termiņatlaižu datumus un summas. Izpildes datums ir 25. jūlijs un termiņatlaide -10,00 ir pieejama, ja rēķins tiek apmaksāts līdz 9. jūlijam.

| Atzīmēt | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Parastais            | Inv-10010 | 3064    | 25.06.2015 | 25.07.2015 | 10010   | 1000,00                       | USD      | 990,00           |

Atlaides informācija parādās lapas **Nosegt atvērtās darbības**apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015 |
| Termiņatlaides summa         | -10,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -10,00    |

Eiprila noklikšķina uz cilnes **Termiņatlaide**, lai apskatītu atlaides summu.

| Termiņatlaides datums | Termiņatlaides summa | Summa darījuma valūtā |
|--------------------|----------------------|--------------------------------|
| 09.07.2015           | 10,00                | 990,00                         |
| 25.07.2015          | 0,00                 | 1000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Daļējs maksājums 1. jūlijā, izmantojot lapu Transakciju nosegšana
Eiprila var izveidot maksājumu žurnālu šim maksājumam, atverot lapu **Maksājumu žurnāls** sadaļā Kreditori. Viņa izveido jaunu žurnālu un ievada rindu kreditoram 3064. Tad viņa atver lapu **Transakciju nosegšana**, lai varētu atzīmēt rēķinu nosegšanai. Eiprila atzīmē rēķinu un maina vērtību laukā **Nosedzamā summa** uz **-500,00**. Viņa redz, ka vērtība laukā **Termiņatlaides summa** ir **-10,00** pilnam rēķinam un ka vērtība **Ņemamā termiņatlaides summa** ir **-5,05**. Tāpēc Eiprila nosedz -505,05 no šī rēķina.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1000,00                       | USD      | -500,00          |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015 |
| Termiņatlaides summa         | -10,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -5,05     |

Eiprila vēlas nosegt precīzi pusi no rēķina. Tāpēc viņa maina vērtību laukā **Nosedzamā summa** uz **-495,00**. Kopējā nosegtā summa tagad ir 500,00. Šī summa iekļauj termiņatlaidi -5,00.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1000,00                       | USD      | -495,00          |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015 |
| Termiņatlaides summa         | -10,00    |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | -5,00     |

Eiprila aizver lapu **Transakciju nosegšana**. Žurnālā tiek izveidota maksājuma rinda summai 495,00, un pēc tam Eiprila iegrāmato žurnālu. Eiprila var pārskatīt kreditoru transakcijas lapā **Debitoru transakcijas**. Viņa redz rēķinam, ka ir bilance -500,00. Viņa redz arī maksājumu 495,00 apmērā un termiņatlaidi 5,00 apmērā.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Rēķins          | 25.06.2015 | 10010   |                                      | 1000,00                              | -500,00 | USD      |
| APP-10010  | Maksājums          | 01.07.2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Termiņatlaide    | 01.07.2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Atlikusī summa samaksāta 8. jūlijā
Eiprila apmaksā atlikušo rēķinu kreditoram 3064 8. jūlijā, kas ietilpst termiņatlaides periodā. Eiprila izveido maksājumu žurnālu 8. jūlijā un atzīmē transakciju nosegšanai. Viņa redz, ka nosedzamā summa ir 495,00. Vērtība laukā **Plānotā termiņatlaide** ir **-5,00**, jo atlaide 5,00 tika izmantota iepriekš.

|                         |        |
|-------------------------|--------|
| Kopā iezīmēts            | 495,00 |
| Plānotā termiņatlaide | -5,00  |

Informācija par iezīmēto transakciju parādās režģī laukā **Nosegt atvērtās darbības**.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1000,00                       | USD      | 495,00           |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/09/2015 |
| Termiņatlaides summa         | 10,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 5,00      |
| Ņemamā termiņatlaides summa | 5,00      |

Eiprila grāmato maksājumu žurnālu un pārskata kreditora transakcijas lapā **Kreditoru darbības**. Rēķina bilance tagad ir 0,00 un Eiprila redz divus maksājumus un divas termiņatlaides.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Rēķins          | 25.06.2015 | 10010   |                                      | 1000,00                              | 0,00    | USD      |
| APP-10010  |  Maksājums         | 01.07.2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Termiņatlaide    | 01.07.2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10011  | Maksājums          | 08.07.2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10011 | Termiņatlaide    | 7/8/2015  |         | 5,00                                 |                                       | 0,00    | USD      |





