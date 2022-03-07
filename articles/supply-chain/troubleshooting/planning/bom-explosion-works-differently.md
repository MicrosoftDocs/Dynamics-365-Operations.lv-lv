---
title: MK izvēršana darbojas atšķirīgi apstiprinātajiem un aptuvenajiem ražošanas pasūtījumiem
description: Materiālu komplekta izvēršana darbojas atšķirīgi apstiprinātiem ražošanas pasūtījumiem un aptuvenajiem ražošanas pasūtījumiem, kuri attiecas uz manuāli izveidotu darbu
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
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476981"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>MK izvēršana darbojas atšķirīgi apstiprinātajiem un aptuvenajiem ražošanas pasūtījumiem

## <a name="symptoms"></a>Simptomi

Kad ražošanas pasūtījums ir apstiprināts, krājumi netiek izvērsti, kad tiek izvērsti materiālu komplekti (MK). Tomēr, kad manuāli veidojat darba pasūtījumu un pēc tam novērtējat ražošanas pasūtījumu, krājumi tiek izvērsti.

### <a name="resolution"></a>Novēršana

Izvērsums, kas rodas, kad ražošanas pasūtījums ir apstiprināts, norādīs uz plānoto pasūtījumu, bet neparādās, ka šajā gadījumā plānotais pasūtījums pašlaik ir apstiprināts. Tomēr, ja ražošanas pasūtījums ir novērtēts, izvērsums tiek izraisīts no nodotā ražošanas pasūtījuma, kur nepastāv plānotais pasūtījums.
