---
title: "SEPA tiešā debeta mandāta iestatīšana"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA tiešā debeta mandāta iestatīšana



Vienotās eiro maksājumu zonas (Single Euro Payment Area — SEPA) tiešais debets kreditoram ļauj iekasēt līdzekļus no debitora bankas konta ar nosacījumu, ka debitors kreditoram ir piešķīris parakstītu mandātu. Debitora parakstītais mandāts pilnvaro kreditoru iekasēt maksājumu un klienta bankai sniedz norādījumus par iekasējamās summas izmaksāšanu. Šajā tēmā ir organizēta parādīt procesu iestatīšanai SEPA tiešā debeta pilnvarojumu.

## <a name="prerequisites"></a>Priekšnosacījumi
Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.

| Kategorija       | Priekšnosacījums                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valsts/reģions | Juridiskās personas primārajai adresei ir jābūt šādās valstīs/reģionos: Austrija, Beļģija, Vācija, Spānija, Francija, Itālija vai Nīderlande. |

1. Iestatiet numuru sēriju, lai tiešā debeta pilnvarojumu katra tiešā debeta pilnvarojumu ir jābūt unikālam numuram. Lai tiešā debeta mandātiem izveidotu numuru sēriju, izmantojiet lapu **Numuru sērijas**. Šis identifikators ir jāizmanto, lai tiešā debeta mandātu sistēmai piešķirtu numuru sēriju lapā **Debitoru moduļa parametri**.

2. Iestatiet kontu saņemamajiem parametriem tiešā debeta pilnvarojumu izmantot **Accounts receivable parameters** lapu, lai iestatītu parametrus tiešā debeta pilnvarojumu. Lai iestatītu parametrus, no **tiešā debeta** cilni, cik jums nepieciešams mainīt noklusētos parametrus. Tad, **numuru sērijas** cilni, atjaunināt **tiešā debeta pilnvarojumu ID** lauku ar numuru sēriju, kuru izveidojāt.

3. Maksājumu veidu iestatīšana par tiešā debeta pilnvaras, jums ir jāuzstāda maksāšanas tiešā debeta pilnvarojumu. Šo maksāšanas metodi jūs izmantojat, lai veidotu vaicājumus par rēķiniem, kam izveidot tiešā debeta maksājumus. Lai iestatītu maksāšanas metodi, izmantojiet lapu **Maksāšanas metodes**. Lai iestatītu maksāšanas metodi tiešā debeta mandātiem, jums ir jāizpilda šādas papildu darbības maksāšanas metodei:

-   Laukā **Maksājuma tips** atlasiet **Elektronisks maksājums**.
-   Pēc izvēles: Ja jums gaidīt, visiem klientiem ir vairākas pilnvaras, jo **periods** lauku, atlasiet **rēķina**. Katram rēķinam tiks izveidota atsevišķa maksājuma un katru maksājumu izmantos pilnvaras, kas ir norādīts rēķina.
-   Atlasiet opciju **Pieprasīt mandātu**, lai izveidotu maksājumus, izmantojot tiešā debeta mandātus. Opcija **Pieprasīt mandātu** ir pieejama tikai tad, ja laukā **Maksājuma tips** atlasāt vērtību **Elektronisks maksājums**.

Sk. arī [tiešā debeta pārskats](sepa-direct-debit-overview.md) 

