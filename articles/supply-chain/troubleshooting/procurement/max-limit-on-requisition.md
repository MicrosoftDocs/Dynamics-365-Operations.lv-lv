---
title: Pirkuma līguma maksimālā robeža nedarbojas pirkuma pieprasījumā
description: Pirkuma līguma maksimālā robeža nedarbojas pirkuma pieprasījumā
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476962"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Pirkuma līguma maksimālā robeža nedarbojas pirkuma pieprasījumā

## <a name="symptoms"></a>Simptomi

Kad pirkšanas pieprasījums ir saistīts ar pirkšanas līgumu, pirkšanas līguma maksimālais ierobežojums nav spēkā pirkšanas pieprasījumā. Noklusējuma cenas informācija ir ievadīta pareizi, tomēr pirkšanas pieprasījumā nevar pasūtīt vairāk par pirkšanas līguma maksimālo ierobežojumu.

## <a name="resolution"></a>Novēršana

Šāda darbība ir paredzama. Tā kā pieprasījumi ne vienmēr tiek apstiprināti, daudzums vai summa pirkšanas līgumā nav jārezervē. Tādējādi netiks sasniegts pirkšanas līguma maksimālais ierobežojums.
