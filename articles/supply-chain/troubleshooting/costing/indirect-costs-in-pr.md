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
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026712"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Procesa pārskata netiešās izmaksas ietver dzēstus ražošanas pasūtījumus

KB numurs: 4612748

## <a name="symptoms"></a>Simptomi

**Netiešās izmaksas procesā** pārskats sniedz informāciju par ražošanas pasūtījumiem, kas tika daļēji apstrādāti un vēlāk dzēsti.

## <a name="resolution"></a>Novēršana

Atsaucot ražošanas pasūtījumu, tiek atsauktas arī visi šī ražošanas pasūtījuma darījumi. Dzēšot ražošanas pasūtījumu, apakšgrāmatas tabulās un virsgrāmatā saglabājas visi ar to saistītie darījumi. Pārskati rādīs darījumus apakšgrāmatas tabulās. Konkrētam ražošanas pasūtījumam neto vērtībai jābūt 0,00.
