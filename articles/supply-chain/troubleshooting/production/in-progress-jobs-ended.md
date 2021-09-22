---
title: Izpildē esoši uzdevumi tiek beigti, kad tiek ziņots par pēdējā uzdevuma daļējo daudzumu
description: Lietojot uzdevuma kartītes ierīci, lai ziņotu par daļēju pēdējā ražošanas pasūtījuma uzdevuma daudzumu, visi iepriekšējie uzdevumi, kuriem notiek izpilde, tiek beigti.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477026"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Iepriekšējie izpildē esoši uzdevumi tiek beigti, kad tiek ziņots par pēdējā uzdevuma daļējo daudzumu

## <a name="symptoms"></a>Simptomi

Lietojot uzdevuma kartītes ierīci, lai ziņotu par daļēju pēdējā ražošanas pasūtījuma uzdevuma daudzumu, visi iepriekšējie šā pasūtījuma uzdevumi, kuriem notiek izpilde, tiek automātiski beigti.

## <a name="resolution"></a>Novēršana

Tas tiek darīts ar nolūku. Lapas **Ražošanas pasūtījuma noklusējuma vērtības** cilnē **Ziņot par pabeigšanu** ir opcija ar nosaukumu **Iezīmēt maršrutu**. Ja šī tēma ir iestatīta uz *Jā*, maršruta kartes žurnāls tiek grāmatots, kad darbinieks izmanto darba kartes ierīci vai darba kartes termināli, lai ziņotu par pēdējo operāciju. Šis žurnāls atzīmē visas operācijas kā pabeigtas un beidz visus ražošanas darbus. Ja opcija **Iezīmēt maršrutu** ir iestatīta uz *Jā*, sistēma neņem vērā darbinieka iestatīto uzdevuma statusu laikā, kad tika ziņots par pēdējo darbību. Sistēma arī neņem vērā, vai darbinieks ziņo par pilnīgu vai daļēju daudzumu.
