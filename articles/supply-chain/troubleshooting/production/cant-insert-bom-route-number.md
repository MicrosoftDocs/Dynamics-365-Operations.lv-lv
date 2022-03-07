---
title: Nevar ievadīt BOM aktīvo versiju un maršrutēšanas numurus
description: Ja noklusējuma vieta un noliktava jau ir definēta atlasītājam produktam, jūs netiksit lūgti ievadīt BOM aktīvo versiju un maršrutēšanas numurus.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476937"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Izveidojot jaunu produkta pasūtījumu, nevar ievadīt materiālu komplektu (BOM) un maršrutu

## <a name="symptoms"></a>Simptomi

Kad izveidojat jaunu ražošanas pasūtījumu, pēc krājuma numura ievadīšanas **Vietnes** un **Noliktavas** lauki tiek automātiski iestatīti uz noklusējuma vietu un noliktavu, kas tiek definēta lapā **Noklusējuma pasūtījuma iestatījumi** pabeigtām precēm. Turklāt aktīvais BOM numurs un maršrutēšanas numurs tiek ievadīti automātiski, tāpēc jūs nesaņemsit šādu ziņojumu, kurā tiktu lūgts ievietot šīs vērtības:

> Vai ievietot aktīvo versiju materiālu komplektam un maršrutam?

## <a name="resolution"></a>Novēršana

Jums netiek lūgts ievadīt BOM un maršrutēšanas numurus, ja atlasāt preci, kuras vieta un noliktava jau ir norādīta lapā **Noklusējuma pasūtījuma iestatījumi**. Jūs tiekat brīdināts tikai tad, ja šīs vērtības nav definētas atlasītajā precē.
