---
title: Plānotie pasūtījumi tiek ģenerēti noliktavas krājumiem ar ražošanas pasūtījumiem
description: Plānotie pasūtījumi tiek ģenerēti pat, ja jums krājumā ir vienības un tām jau pastāv ražošanas pasūtījumi
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
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477033"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Plānotie pasūtījumi tiek ģenerēti noliktavas krājumiem ar ražošanas pasūtījumiem

## <a name="symptoms"></a>Simptomi

Plānotie pasūtījumi tiek ģenerēti pat, ja jums krājumā ir vienības un tām jau pastāv ražošanas pasūtījumi.

## <a name="resolution"></a>Novēršana

Šo problēmu var novērst, palielinot **Pozitīvo dienu** vērtību attiecīgajām grupām lapā **Pārklājumu grupa**. Šī izmaiņa liks sistēmai noteikt, vai rīcībā esošie krājumi var tikt izmantoti pieprasījumam. Pēc tam krājumos esošām precēm netiks ģenerēts jauns plānotais pasūtījums.
