---
title: Tiešā piegāde nevar apstrādāt WMS iespējotai noliktavai
description: Ja noliktavai ir iespējots WMS, tā neatbalsta tiešo piegādi. Lai lietotu tiešo piegādi, ir jāatlasa ne-WMS elements un noliktava.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477036"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Tiešā piegāde nevar apstrādāt WMS iespējotai noliktavai

## <a name="symptoms"></a>Simptomi

Ja elements tiek pievienots pārdošanas rindai tiešai piegādei no noliktavas, kurai ir iespējota noliktavas pārvaldība (WMS), jūs saņemsit šādu kļūdas ziņojumu, kad pārdošanas rinda tiks atjaunināta:

> Tiešo piegādi nevar apstrādāt procesam noliktavai 1%, jo tai ir iespējota noliktavas pārvaldība. Norādiet citu noliktavu, kurai nav iespējota noliktavas pārvaldība.

## <a name="resolution"></a>Novēršana

Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums. Pašlaik WMS neatbalsta tiešo piegādi. Tāpēc, lai izmantotu tiešo piegādi, jāatlasa WMS krājums un noliktava.
