---
title: Vispārējā plānošana pārsniedz pieejamo noslodzi
description: Vispārējai plānošanai nav jāievēro noslodzes ierobežojumi, un tā plānošana ir lielāka par pieejamo noslodzi
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476998"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Vispārējā plānošana pārsniedz pieejamo noslodzi

## <a name="symptoms"></a>Simptomi

Vispārējai plānošanai nav jāievēro noslodzes ierobežojumi, un tā plānošana ir lielāka par pieejamo noslodzi.

Kad izmantojat operāciju plānošanu, kur ir ierobežota noslodze un kur maršruts norāda vajadzību kopumu gan resursu grupai, gan atsevišķiem resursiem, ir neliela iespēja rezervēt vairāk, jo algoritms apstiprina noslodzes konfliktus. Šī rezervēšana var notikt, kad izmantojat palīgus, lai veiktu vispārējo plānošanu. Tas visdrīzāk var notikt, ja ir daudz darbu ar relatīvi īsu izpildlaiku.

## <a name="resolution"></a>Novēršana

Ja ir svarīgi, lai operāciju plānošana netiktu pārgrāmatota, ieslēdzot opciju **Precīza ierobežota noslodzes operāciju plānošanai** opciju lapā **Vispārējās plānošanas plānošana**. Šī opcija nav pieejama pēc noklusējuma. Tas ir manuāli jāpievieno lapai, izmantojot personalizēšanas līdzekļus. Kad izmantojat šo opciju, plānošana darbosies lēnāk, jo nav paralēlās apstrādes.
