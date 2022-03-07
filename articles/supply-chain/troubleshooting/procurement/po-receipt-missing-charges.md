---
title: Pirkuma pasūtījuma kvīts neietver visas maksas
description: Pirkuma pasūtījuma kvīts neietver visas maksas
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
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476942"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Pirkuma pasūtījuma kvīts neietver visas maksas

## <a name="symptoms"></a>Simptomi

Saņemot pirkuma pasūtījumu kvītī nav iekļautas visas maksas.

### <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Lapā **Sagādes un avotu parametri** cilnē **Piegāde** pārliecinieties, vai opcija **Produktu ieejas plūsmas maksu ģenerēšana** ir iestatīta uz *Jā*.
1. Izveidojiet pirkšanas pasūtījumu, kurā ietvertas maksas.
1. Apstipriniet pirkšanas pasūtījumu.
1. Saņemiet pirkšanas pasūtījumu.
1. Apskatiet kvīts kopsummu un salīdziniet to ar prognozēto kopsummu.
1. Ievērojiet, ka pirkšanas pasūtījuma kvītī nav ietvertas visas maksas.

## <a name="resolution"></a>Novēršana

Risinājums ir atkarīgs no veida, kādā ir iestatītas papildmaksas. Lai iegūtu informāciju par to, kā iestatīt papildmaksas, kas atbilst jūsu prasībām, skatiet šo emuāra ierakstu: [Papildmaksu grāmatošana produktu ieejas plūsmas laikā](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
