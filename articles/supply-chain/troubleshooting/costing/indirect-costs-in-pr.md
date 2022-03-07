---
title: Procesa pārskata netiešās izmaksas ietver dzēstus ražošanas pasūtījumus
description: Netiešās izmaksas procesā pārskats sniedz informāciju par ražošanas pasūtījumiem, kas tika daļēji apstrādāti un vēlāk dzēsti.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751773"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Procesa pārskata netiešās izmaksas ietver dzēstus ražošanas pasūtījumus

KB numurs: 4612748

## <a name="symptoms"></a>Simptomi

**Netiešās izmaksas procesā** pārskats sniedz informāciju par ražošanas pasūtījumiem, kas tika daļēji apstrādāti un vēlāk dzēsti.

## <a name="resolution"></a>Novēršana

Atsaucot ražošanas pasūtījumu, tiek atsauktas arī visi šī ražošanas pasūtījuma darījumi. Dzēšot ražošanas pasūtījumu, apakšgrāmatas tabulās un virsgrāmatā saglabājas visi ar to saistītie darījumi. Pārskati rādīs darījumus apakšgrāmatas tabulās. Konkrētam ražošanas pasūtījumam neto vērtībai jābūt 0,00.
