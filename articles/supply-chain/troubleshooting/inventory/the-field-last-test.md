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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742032"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Pēdējā pārbaudītā datuma lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi

KB numurs: 4612803

## <a name="symptoms"></a>Simptomi

**Pēdējā pārbaudītā datuma** lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi.

## <a name="resolution"></a>Novēršana

Sistēma darbojas kā paredzēts. Pēdējais pārbaudītais datums nav saistīts ar kvalitātes pārbaudes pasūtījumiem. Tajā tiek glabāts datums, kad pabeigtās preces tikušas pirmo reizi iegādātas vai saražotas. Šis datums tiek izmantots, lai aprēķinātu glabāšanas laika izziņas datumu.
