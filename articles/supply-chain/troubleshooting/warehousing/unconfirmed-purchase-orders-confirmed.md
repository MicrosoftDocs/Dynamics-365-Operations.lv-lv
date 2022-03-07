---
title: Produktu ieejas plūsmu uzdevumu atjaunināšana apstiprina neapstiprinātus pasūtījumus
description: Pēc produktu ieejas plūsmu atjaunināšanas sistēma apstiprina neapstiprinātos pasūtījumus, kuru statuss ir Reģistrēts. Uzziniet par līdzekli, kas noverš šo problēmu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476949"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Pēc atjaunināšanas produktu saņemšanas tiek apstiprināti neapstiprināti pirkšanas pasūtījumi

## <a name="symptoms"></a>Simptomi

Pēc tam, kad esat palaidis *Atjaunināt preču ieejas plūsmu* periodisko uzdevumu, sistēma automātiski apstiprina neapstiprinātos pirkšanas pasūtījumus, kuriem ir krājuma darbības statuss *Reģistrēts*.

## <a name="resolution"></a>Novēršana

Jauna ienākošo kravu apstrādes funkcija *Pārsniedzot kravas daudzumu* izlabo šo problēmu. Lai ieslēgtu šo funkciju, dodieties uz darbvietu [Līdzekļu pārvaldība](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) un ieslēdziet tālāk norādītos līdzekļus minētajā secībā:

1. Saistīt pirkšanas pasūtījuma krājumu transakcijas ar kravu
2. Noslodzes daudzumu pārmērīga saņemšana

Lai iegūtu papildu informāciju, skatiet [Reģistrēto preču daudzumu grāmatošana uz pirkšanas pasūtījumiem](/dynamics365/supply-chain/warehousing/inbound-load-handling).
