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
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713498"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Uzsāktā karantīnas pasūtījuma daudzums netiek atjaunināts, ja pasūtījums ir sadalīts

KB numurs: 4613113

## <a name="symptoms"></a>Simptomi

Veidojot karantīnas pasūtījumu un mēģinot to sadalīt, pasūtījuma daudzums netiek atjaunināts uz atlikušo daudzumu pēc sadalīšanas.

## <a name="resolution"></a>Novēršana

Sistēma nemaina sākotnējo daudzumu no karantīnas pasūtījuma, lai nodrošinātu, ka varat izsekot sākotnējam daudzumam, kas tika izveidots šim karantīnas pasūtījumam. Tomēr sistēma izseko daudzumu, kas ir sadalīts no karantīnas pasūtījuma. Lai to paveiktu, tā izmanto datu bāzes lauku ar nosaukumu `QuantityThatHasSplitIntoOtherQuarantineOrders`. Tomēr šis lauks nav redzams lietotāja interfeisā (user interface — UI).
