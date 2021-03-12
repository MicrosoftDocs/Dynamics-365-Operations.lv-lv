---
title: Daļēja maksājuma segšana pirms atlaižu piemērošanas datuma ar gala maksājumu pēc atlaižu piemērošanas datuma
description: Šajā rakstā ir aprakstīta debitoru rēķinu segšanas maksājumu ietekme. Scenārija aprakstā galvenā uzmanība pievērsta izmaiņām, kas rodas apakšgrāmatā, nevis virsgrāmatā.
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
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad922bc6c9378078012b7a838909e4074b48f263
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979068"
---
# <a name="settle-partial-payment-before-discount-date-with-final-payment-after-discount-date"></a>Daļēja maksājuma segšana pirms atlaižu piemērošanas datuma ar gala maksājumu pēc atlaižu piemērošanas datuma

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīta debitoru rēķinu segšanas maksājumu ietekme. Scenārija aprakstā galvenā uzmanība pievērsta izmaiņām, kas rodas apakšgrāmatā, nevis virsgrāmatā.

Fabrikam pārdod preces debitoram 4027. Fabrikam piedāvā termiņatlaidi 1 procenta apmērā, ja rēķins tiek apmaksāts 14 dienu laikā. Rēķini ir jāapmaksā 30 dienu laikā. Fabrikam piedāvā arī termiņatlaides daļējiem maksājumiem. Nosegšanas parametri atrodas lapā **Debitoru moduļa parametri**.

## <a name="invoice"></a>Rēķins
Arnis debitoram 4027 izrakstīto rēķinu par summu 1000,00 ievada un grāmato 25. jūnijā. Arnis var skatīt šo rēķinu, izmantojot pogu **Transakcijas** lapā **Debitori**.

| Dokuments   | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance  | Valūta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | Rēķins          | 25.06.2015. | 10020   | 1000,00                             |                                       | 1000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Daļēja apmaksa pirms termiņatlaides datuma
2. jūlijā klients 4027 veic daļēju rēķina apmaksu: 297,00. Maksājums ir piemērots termiņatlaidei, jo Fabrikam piedāvā termiņatlaides daļējiem maksājumiem, un daļējais maksājums ir veikts pirms termiņatlaides datuma. Tādēļ klients 4027 saņem 3,00 lielu termiņatlaidi. Arnijs reģistrē debitora 4027 maksājumu, izmantojot maksājumu žurnālu. Pēc tam Arnijs atver lapu **Transakciju nosegšana**, lai varētu atzīmēt nosedzamo rēķinu.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10020 | 4027    | 25.06.2015. | 25.07.2015. | 10020   | 1000,00                             | USD      | 297,00           |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā. Ja nemainīsit vērtību **Nosedzamā summa** uz 297,00, parādītās vērtības **Termiņatlaides summa** būs atšķirīgas. Tomēr, grāmatojot maksājumu, 3,00 tiks apstrādāti kā termiņatlaide, jo nosegšana automātiski pielāgos vērtību **Nosedzamā summa**.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015 |
| Termiņatlaides summa         | 10,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | 3,00      |

Arnijs grāmato šo maksājumu. Tagad rēķina bilance ir 700,00. Debitors var redzēt šādas darbības.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Rēķins          | 25.06.2015. | 10020   | 1000,00                             |                                       | 700,00  | USD      |
| ARP-10020  |  Maksājums         | 01.07.2015.  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |  Termiņatlaide   | 01.07.2015.  |         |                                      | 3,00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Atlikusī apmaksa pēc termiņatlaides datuma
Atlikušo rēķinu klients 4027 apmaksā 11. jūlijā, kas ir pēc termiņatlaides perioda. Lapas **Transakciju nosegšana** laukā **Plānotā termiņatlaide** netiek rādīta nekāda atlaides summa, un vērtība laukā **Termiņatlaides summa** ir **0,00**. Kad klients 4027 samaksā atlikušo summu 700,00, netiek saņemta nekāda papildu atlaide.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Atlasīts | Parastais            | FTI-10020 | 4027    | 25.06.2015. | 25.07.2015. | 10020   | 700,00                               | USD      | 700,00           |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015. |
| Termiņatlaides summa         | 0,00      |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 3,00      |
| Ņemamā termiņatlaides summa | 0,00      |

Ja Arnijs maina vērtību laukā **Izmantot termiņatlaidi** uz **Vienmēr**, iestatījums **Aprēķināt termiņatlaides daļējiem maksājumiem** tiek ignorēts, un tiek saņemta termiņatlaide. Maksājuma summa mainās uz 693,00, un termiņatlaide ir atlikušie 7,00.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Atlasīts | Vienmēr            | FTI-10020 | 4027    | 25.06.2015. | 25.07.2015. | 10020   | 700,00                               |                                       | USD      | 693,00           |

Atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 09.07.2015. |
| Termiņatlaides summa         | 7,00      |
| Izmantot termiņatlaidi            | Vienmēr    |
| Paņemta termiņatlaides summa          | 3,00      |
| Ņemamā termiņatlaides summa | 7,00      |

Arnijs maina vērtību laukā **Izmantot termiņatlaidi** atpakaļ uz **Parasta**, jo viņš neļauj šim debitoram saņemt atlikušo termiņatlaidi 7,00. Pēc tam Arnijs grāmato maksājumu. Kad Arnijs atver lapu **Debitoru darbības**, viņš redz, ka rēķina bilance ir 0,00. Viņš arī redz, ka pastāv divi maksājumi. Viens maksājums ir par 297,00, un tam ir 3,00 termiņatlaide, un otrs maksājums ir 700,00.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Rēķins          | 25.06.2015. | 10020   | 1000,00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 01.07.2015.  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |                  | 01.07.2015.  |         |                                      | 3,00                                  | 0,00    | USD      |
| ARP-10021  |                  | 11.07.2015. |         |                                      | 700,00                                | 0,00    | USD      |





