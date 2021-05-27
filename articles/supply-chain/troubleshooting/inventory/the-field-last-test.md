---
title: Pēdējā pārbaudītā datuma lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi
description: Pēdējā pārbaudītā datuma lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026722"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Pēdējā pārbaudītā datuma lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi

KB numurs: 4612803

## <a name="symptoms"></a>Simptomi

**Pēdējā pārbaudītā datuma** lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi.

## <a name="resolution"></a>Novēršana

Sistēma darbojas kā paredzēts. Pēdējais pārbaudītais datums nav saistīts ar kvalitātes pārbaudes pasūtījumiem. Tajā tiek glabāts datums, kad pabeigtās preces tikušas pirmo reizi iegādātas vai saražotas. Šis datums tiek izmantots, lai aprēķinātu glabāšanas laika izziņas datumu.
