---
title: Nav iespējams atcelt atcelt pavadzīmi, kad tā ir grāmatota no pasūtījuma
description: Kad izdošanas un nosūtīšanas procesi ir iespējoti WMS, pavadzīmi nevar atcelt pēc tās grāmatošanas no pārdošanas pasūtījuma. Šajā lapā tiek piedāvāts risinājums.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477037"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Nav iespējams atcelt atcelt pavadzīmi, kad tā ir grāmatota no pārdošanas pasūtījuma

## <a name="symptoms"></a>Simptomi

Kad papildu noliktavas pārvaldībai (WMS) tiek iespējoti izdošanas un sūtīšanas procesi, nav iespējams atcelt pavadzīmi pēc tam, kad tā ir grāmatota no pārdošanas pasūtījuma.

## <a name="resolution"></a>Novēršana

Lai labotu grāmatotās pavadzīmes krājumiem, kas ir iespējoti WMS, grāmatošana ir jāveic no kravas, nevis tieši no pasūtījuma. Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.  

Kopumā pārdošanas pasūtījumu, kas ir izdots un sūtīts, izmantojot noliktavas pārvaldības procesus, var atjaunināt ar pavadzīmi no kravas vai sūtījuma un paša pārdošanas pasūtījuma dokumenta. Taču, ja ar pavadzīmi atjaunināt pārdošanas pasūtījumu no pārdošanas pasūtījuma dokumenta, pavadzīmes atcelšanu joprojām nevar veikt no kravas vai pārdošanas pasūtījuma. Tāpēc ieteicams izmantot pavadzīmes grāmatošanu no kravas. Šādā gadījumā tiks aktivizēta atgriešana, kas ir jāveic no kravas.
