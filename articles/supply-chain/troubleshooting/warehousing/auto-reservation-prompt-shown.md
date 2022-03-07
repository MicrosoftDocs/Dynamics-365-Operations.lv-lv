---
title: Pieejamajam krājumam tiek rādīts automātiskās rezervācijas vednis
description: Lietojot vienumu noliktavā, kurai nav iespējoti noliktavas procesi, tiek rādīts automātiskās rezervācijas vednis. Norādiet visus izmērus virs Atrašanās vietas.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477021"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Partijas numura automātiskās rezervācijas vednis tiek rādīts pat ar pieejamo krājumu

## <a name="symptoms"></a>Simptomi

Izmantojot krājumu, kam noliktavā nav iespējoti noliktavas procesi un ir iespējota automātiska rezervācija, rezervāciju hierarhiju *virs* rezervāciju hierarhijas, un ir iespējota automātiskā rezervācija, partijas numura automātiskās rezervēšanas uzvedne tiek parādīta pat tad, ja izdošanai ir pieejama tikai viena partija.

Tomēr, ja izmantojat to pašu krājumu noliktavā, kur ir iespējoti noliktavas procesi, netiek parādīta automātiskās rezervācijas uzvedne.

## <a name="resolution"></a>Novēršana

Ja rezervāciju hierarhija ir definēta kā *virs* vai *pārsniedz sēriju*, atsauces dimensija (**Partijas numurs** vai **Sērijas numurs**) vienmēr jānorāda pieprasījuma pasūtījumos. Noliktavas procesi, iespējams, var pabeigt informāciju, ja ir pieejams viens paketes vai sērijas numurs. Tomēr, tā kā noliktava nav iespējota noliktavas procesiem, lietotājam vienmēr ir jānorāda visas dimensijas virs **Novietojuma**.
