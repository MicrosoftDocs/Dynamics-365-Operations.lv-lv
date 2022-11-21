---
title: Pagaidu maksājumu iestatīšana un apstrāde
description: Šajā rakstā ir paskaidrots, kā iestatīt un apstrādāt pagaidu debitoru maksājumus. Saīsinātais maksājums ir maksājums, kas tiek grāmatots virsgrāmatā, veicot divas darbības.
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
ms.openlocfilehash: bb563008f156e1bfa6e4e9a705e9170342719ce7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775173"
---
# <a name="set-up-and-process-bridged-payments"></a>Pagaidu maksājumu iestatīšana un apstrāde

[!include [banner](../includes/banner.md)]

Saīsinātais maksājums ir maksājums, kas tiek grāmatots virsgrāmatā, veicot divas darbības. Parasti šo pieeju izmanto, ja maksājuma veids ir iestatīts uz **Banku, un jums ir jāgrāmato darījumi bankas kontā tikai tad, kad darījums ir iztīrījis banku**. Tomēr varat to izmantot arī virsgrāmatas kontam. Šajā gadījumā, apstrādājot pagaidu grāmatošanu, summa tiks pārvietota no viena galvenā konta uz citu galveno kontu.

Varat izveidot saīsinātus maksājumus no kreditoriem vai debitoru parādiem. Lai gan šajā rakstā ir paskaidrots, kā konfigurēt pagaidu grāmatošanu debitoru parādiem, kreditoru parādu transakcijām atbilstošās darbības ir līdzīgas.

## <a name="set-up-bridging-posting"></a>Pagaidu publicēšanas iestatīšana

Lai izmantotu pagaidu grāmatošanu, jums ir jāiestata viens vai vairāki maksājuma veidi, lai tie izmantotu **pārejas grāmatošanas** metodi. Pēc tam jums ir jāizvēlas pagaidu konts.

1. Pārejiet uz sadaļu **Debitoru parādi &gt; Maksājumu iestatījumi &gt; Apmaksas veidi**.
2. Atlasiet esošu maksājuma veidu, lai iespējotu pagaidu grāmatošanu. Vai arī izveidojiet jaunu maksājuma veidu.
3. Atzīmējiet izvēles rūtiņu **Pagaidu ievietošana**.
4. Laukā Pagaidu **konts** atlasiet galveno kontu, kurā maksājumi ir jāgrāmato, pirms tie tiek ieskaitīti bankas kontā.
5. Aizvērt lapu.

## <a name="process-and-transfer-bridging-posting"></a>Pagaidu norīkošanas apstrāde un pārsūtīšana

Lai izveidotu un apstrādātu pagaidu publicēšanu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Debitori &gt; Maksājumi &gt; Debitora maksājumu žurnāls**.
2. Atlasiet **Jauns**, lai izveidotu žurnālu.
3. Laukā **Nosaukums** atlasiet nosaukumu.
4. Pievienojiet rindas debitoru maksājumu žurnālam un atlasiet maksāšanas metodi, kas ir konfigurēta pagaidu grāmatošanai.
5. Grāmatot žurnālu. Transakcijas tiks grāmatotas galvenajā kontā, kuru atlasījāt **iepriekšējās procedūras laukā Pārejas konts**.

Kad darījumi ir iztīrīti bankā un jūs vēlaties pārskaitīt maksājumu no pagaidu konta uz maksājumu kontu, kas norādīts maksājuma veidam, veiciet tālāk norādītās darbības.

1. Dodieties uz **Virsgrāmata &gt; Žurnāla ieraksti &gt; Virsgrāmatas žurnāli**.
2. Atlasiet **Jauns**, lai izveidotu žurnālu.
3. Laukā **Nosaukums** atlasiet nosaukumu.
4. Atlasiet **Rindas**, lai atvērtu detalizētu informāciju par žurnālu.
5. Atlasiet **Funkcijas &gt; Atlasiet saistītās transakcijas**.
6. Atzīmējiet katru notīrīto maksājumu un pēc tam atlasiet **Akceptēt**.
7. Grāmatot žurnālu.
