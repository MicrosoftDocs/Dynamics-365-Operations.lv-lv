---
title: Pagaidu maksājumu iestatīšana un apstrāde
description: Šajā rakstā skaidrots, kā iestatīt un apstrādāt pagaidu debitoru maksājumus. Pagaidu maksājums ir maksājums, kas tiek grāmatots Virsgrāmatā divos soļos.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f0609e333fb16ba189b6a971f88fbb5bf900fec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887982"
---
# <a name="set-up-and-process-bridged-payments"></a>Pagaidu maksājumu iestatīšana un apstrāde

[!include [banner](../includes/banner.md)]

Pagaidu maksājums ir maksājums, kas tiek grāmatots Virsgrāmatā divos soļos. Parasti šī pieeja tiek izmantota **, kad maksājuma metode ir iestatīta uz Banku**, un darbības bankas kontā jāgrāmato tikai tad, kad darbība ir dzēsta no bankas. Tomēr to var izmantot arī Virsgrāmatas kontam. Šajā gadījumā sistēma pārvirzīs summu no viena galvenā konta uz citu galveno kontu, kad pagaidu grāmatojums ir apstrādāts.

Jūs varat izveidot pagaidu maksājumus no Parādi kreditoriem vai Debitoru parādiem. Lai gan šajā rakstā skaidrots, kā konfigurēt pagaidu grāmatošanu debitoru parādiem, darbības kreditoru darbībām ir līdzīgas.

## <a name="set-up-bridging-posting"></a>Pagaidu grāmatošanas iestatīšana

Lai lietotu pagaidu grāmatošanu, jāiestata viena vai vairākas maksājuma metodes, lai tās izmantotu **pagaidu grāmatošanas** metodi. Pēc tam jāatlasa pagaidu konts.

1. Dodieties uz **debitoru &gt; parādu maksājumu &gt; iestatīšanas metodēm**.
2. Atlasiet esošu maksāšanas veidu, lai iespējotu pagaidu grāmatošanu. Vai arī izveidojiet jaunu maksāšanas metodi.
3. Atzīmējiet **izvēles rūtiņu Pagaidu** grāmatošana.
4. Laukā **Pagaidu konts atlasiet** galveno kontu, kurā grāmatot maksājumus, pirms tie tiek dzēsti bankas kontā.
5. Aizvērt lapu.

## <a name="process-and-transfer-bridging-posting"></a>Pagaidu grāmatošanas apstrāde un pārsūtīšana

Lai izveidotu un apstrādātu pagaidu grāmatojumu, sekojiet šiem soļiem.

1. Dodieties uz **Debitori &gt; Maksājumi &gt; Debitora maksājumu žurnāls**.
2. Atlasiet **Jauns**, lai izveidotu žurnālu.
3. Laukā **Nosaukums** atlasiet nosaukumu.
4. Pievienojiet rindas debitora maksājumu žurnālam un atlasiet maksājuma metodi, kas ir konfigurēta pagaidu grāmatošanai.
5. Grāmatot žurnālu. Darbības tiks grāmatotas galvenajā kontā, kurš atlasīts **iepriekšējās** procedūras laukā Pagaidu konts.

Kad darbības ir nodīztas bankai un vēlaties pārsūtīt maksājumu no pagaidu konta uz maksājuma kontu, kas norādīts maksājuma metodei, sekojiet šiem soļiem.

1. Dodieties uz **Virsgrāmata &gt; Žurnāla ieraksti &gt; Virsgrāmatas žurnāli**.
2. Atlasiet **Jauns**, lai izveidotu žurnālu.
3. Laukā **Nosaukums** atlasiet nosaukumu.
4. Atlasiet **Rindas,** lai atvērtu detalizēto informāciju par žurnālu.
5. Atlasiet **funkcijas, &gt; lai atlasītu pagaidu darbības**.
6. Atzīmējiet katru dzēsto maksājumu un pēc tam atlasiet **Pieņemt**.
7. Grāmatot žurnālu.
