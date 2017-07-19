---
title: "SEPA tiešā debeta mandāta iestatīšana"
description: 
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ebf80efa32b21184a8effdde4d46c4d0d2179efd
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA tiešā debeta mandāta iestatīšana

[!include[banner](../includes/banner.md)]




Vienotās eiro maksājumu zonas (Single Euro Payment Area — SEPA) tiešais debets kreditoram ļauj iekasēt līdzekļus no debitora bankas konta ar nosacījumu, ka debitors kreditoram ir piešķīris parakstītu mandātu. Debitora parakstītais mandāts pilnvaro kreditoru iekasēt maksājumu un klienta bankai sniedz norādījumus par iekasējamās summas izmaksāšanu. Šī tēma ir sakārtota, lai parādītu SEPA tiešā debeta mandātu iestatīšanas procesu.

## <a name="prerequisites"></a>Priekšnosacījumi
Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.

| Kategorija       | Priekšnosacījums                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valsts/reģions | Juridiskās personas primārajai adresei ir jābūt šādās valstīs/reģionos: Austrija, Beļģija, Vācija, Spānija, Francija, Itālija vai Nīderlande. |

1. Numuru sērijas iestatīšana tiešā debeta mandātiem Katram tiešā debeta mandātam ir nepieciešams unikāls numurs. Lai tiešā debeta mandātiem izveidotu numuru sēriju, izmantojiet lapu **Numuru sērijas**. Šis identifikators ir jāizmanto, lai tiešā debeta mandātu sistēmai piešķirtu numuru sēriju lapā **Debitoru moduļa parametri**.

2. Debitoru parādu parametru iestatīšana tiešā debeta mandātiem Lai iestatītu parametrus tiešā debeta mandātiem, izmantojiet lapu **Debitoru moduļa parametri**. Lai iestatītu parametrus, cilnē **Tiešais debets** pēc nepieciešamības mainiet noklusējuma parametrus. Pēc tam cilnē **Numuru sērijas** lauku **Tiešā debeta mandāta ID** atjauniniet ar iepriekš iestatīto numuru sēriju.

3. Maksājumu metodes iestatīšana tiešā debeta mandātiem Jums jāiestata maksāšanas metode tiešā debeta mandātiem. Šo maksāšanas metodi jūs izmantojat, lai veidotu vaicājumus par rēķiniem, kam izveidot tiešā debeta maksājumus. Lai iestatītu maksāšanas metodi, izmantojiet lapu **Maksāšanas metodes**. Lai iestatītu maksāšanas metodi tiešā debeta mandātiem, jums ir jāizpilda šādas papildu darbības maksāšanas metodei:

-   Laukā **Maksājuma tips** atlasiet **Elektronisks maksājums**.
-   Neobligāti: ja plānojat, ka katram klientam būs vairāki mandāti, laukā **Periods** atlasiet vienumu **Rēķins**. Katram rēķinam tiks izveidots atsevišķs maksājums, un katrs maksājums izmantos mandātu, kas ir norādīts rēķinam.
-   Atlasiet opciju **Pieprasīt mandātu**, lai izveidotu maksājumus, izmantojot tiešā debeta mandātus. Opcija **Pieprasīt mandātu** ir pieejama tikai tad, ja laukā **Maksājuma tips** atlasāt vērtību **Elektronisks maksājums**.

Skatiet arī sadaļu [Tiešā debeta pārskats](sepa-direct-debit-overview.md) 



