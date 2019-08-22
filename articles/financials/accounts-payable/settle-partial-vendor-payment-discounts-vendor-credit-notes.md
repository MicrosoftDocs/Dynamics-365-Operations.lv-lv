---
title: Tāda daļēja kreditora maksājuma segšana, kam ir atlaides kreditora kredītrēķiniem
description: Šajā rakstā ir izklāstīts scenārijs, kur kredītrēķins tiek nosegts pret rēķinu.
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
ms.search.scope: Core, Operations
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 923ab0305ac75c1156984c7a6d051f036479a16d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834515"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Tāda daļēja kreditora maksājuma segšana, kam ir atlaides kreditora kredītrēķiniem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izklāstīts scenārijs, kur kredītrēķins tiek nosegts pret rēķinu.

Uzņēmumam Fabrikam kreditori piešķir termiņatlaides kredīta notām. Kreditors 3050 ļauj uzņēmumam Fabrikam piemērot 1 % termiņatlaidi, ja rēķins tiek apmaksāts 14 dienu laikā.

## <a name="invoice-and-credit-memo"></a>Rēķins un kredītrēķins
Eiprila 29. jūnijā izveido kreditoram 3050 rēķinu par summu 1000,00. 2. jūlijā viņa izveido kredītrēķinu par summu 200,00. No lapas **Kreditori** Eiprila atver lapu **Transakciju nosegšana**. Viņa var izmantot lapu **Transakciju nosegšana**, lai atzīmētu nosegšanai gan kredītrēķinu, gan rēķinu. Kredītrēķinam tiek aprēķināta atlaide 2,00. Tādējādi kopējā kredītrēķina summa tiek samazināta līdz 198,00.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts                 | Parastais            | Inv-10070 | 3050    | 29.06.2015 | 29.07.2015 | 10070   | –1000,00                      | USD      | –990,00          |
| Atlasīts un iezīmēts | Parastais            | CR-10070  | 3050    | 02.07.2015  | 29.07.2015 |         | 200,00                         | USD      | 198,00           |

Kredītrēķina atlaides informācija ir redzama lapas **Nosegt atvērtās transakcijas** apakšdaļā.

|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 13.07.2015 |
| Termiņatlaides summa         | 2,00      |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | 2,00      |

Eiprila noklikšķina uz **Grāmatot**. Pēc tam viņa pārskata pabeigto nosegšanu. Eiprila redz, ka tika piemērota kredīrēķina summa 198,00, kā arī atlaides summa 2,00. Tādējādi kopsumma ir 200,00.

| Atzīmēt                     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins  | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Atlasīts un iezīmēts | Parastais            | Inv-10070 | 3050    | 29.06.2015 | 29.07.2015 | 10070    | –1000,00                      | USD      | –200,00          |
| Atlasīts                 | Parastais            | CR-10070  | 3050    | 02.07.2015  | 29.07.2015 | CR-10070 | 200,00                         | USD      | 198,00           |

Eiprila var pārskatīt kreditoru darbības lapā **Kreditoru darbības**, atlasot kreditoru lapā **Visi kreditori**un pēc tam darbību rūtī noklikšķinot uz **Darbības**. Šajā lapā Eiprila redz, ka rēķina bilances ir –800,00. Viņa arī redz kredītrēķinu par summu 198,00 un atlaides summu 2,00.

| Dokuments    | Darījuma veids | Datums      | Rēķins | Summa transakcijas valūtas debetā | Summa transakcijas valūtas kredītā | Bilance | Valūta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10070  | Rēķins          | 29.06.2015 | 10070   |                                      | 1000,00                              | –800,00 | USD      |
| Inv-10071  |                  | 02.07.2015  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| DISC-10071 |  Termiņatlaide   | 02.07.2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| DISC-10071 |  Termiņatlaide   | 02.07.2015  |         |                                      | 2,00                                  | 0,00    | USD      |





