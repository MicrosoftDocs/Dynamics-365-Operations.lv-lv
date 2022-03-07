---
title: Atceltie pirkuma pasūtījumi parādās darbvietas melnrakstu sarakstā
description: Atceltie pirkuma pasūtījumi parādās Pirkuma pasūtījuma sagatavošanas darbvietas melnrakstu sarakstā
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477006"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Atceltie pirkuma pasūtījumi parādās darbvietas melnrakstu sarakstā

## <a name="symptoms"></a>Simptomi

Atceļot pirkšanas pasūtījumus, ar statusu *Apstiprināts*, atceltie pirkšanas pasūtījumi joprojām parādās **Pirkšanas pasūtījumu sagatavošanas** darbvietas pirkšanas pasūtījumu melnrakstu sarakstā.

## <a name="resolution"></a>Novēršana

Šī problēma rodas tikai tiem pirkšanas pasūtījumiem, kas ir pakļauti izmaiņu pārvaldībai. Tas notiek tāpēc, ka atcelšana tiek uzskatīta par izmaiņu, kas ir jāapstiprina. Apstiprinājumu sistēma var veikt automātiski. Atceltais pirkšanas pasūtījums ir jāiesniedz apstiprināšanas darbplūsmai, lai to varētu nosūtīt uz statusu *Apstiprināts*. Pēc tam pirkšanas pasūtījums vairs netiks rādīts **Pirkšanas pasūtījumu sagatavošanas** darbvietas pirkšanas pasūtījumu melnrakstu sarakstā.
