---
title: Uzsāktā karantīnas pasūtījuma daudzums netiek atjaunināts, ja pasūtījums ir sadalīts
description: Veidojot karantīnas pasūtījumu un mēģinot to sadalīt, pasūtījuma daudzums netiek atjaunināts uz sadalīto atlikušo daudzumu.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026724"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Uzsāktā karantīnas pasūtījuma daudzums netiek atjaunināts, ja pasūtījums ir sadalīts

KB numurs: 4613113

## <a name="symptoms"></a>Simptomi

Veidojot karantīnas pasūtījumu un mēģinot to sadalīt, pasūtījuma daudzums netiek atjaunināts uz atlikušo daudzumu pēc sadalīšanas.

## <a name="resolution"></a>Novēršana

Sistēma nemaina sākotnējo daudzumu no karantīnas pasūtījuma, lai nodrošinātu, ka varat izsekot sākotnējam daudzumam, kas tika izveidots šim karantīnas pasūtījumam. Tomēr sistēma izseko daudzumu, kas ir sadalīts no karantīnas pasūtījuma. Lai to paveiktu, tā izmanto datu bāzes lauku ar nosaukumu `QuantityThatHasSplitIntoOtherQuarantineOrders`. Tomēr šis lauks nav redzams lietotāja interfeisā (user interface — UI).
