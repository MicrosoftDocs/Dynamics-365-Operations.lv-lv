---
title: Atceļot piegādes atgādinājumu, pirkuma pasūtījums tiek pārvirzīts uz statusu Apstiprināts
description: Ja tiek atcelts piegādes pasūtījuma piegādes atgādinājums, esot ieslēgtais izmaiņu pārvaldībai, pirkuma pasūtījuma statuss tiek nomainīts uz Apstiprināts
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476996"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Atceļot piegādes atgādinājumu, pirkuma pasūtījums tiek pārvirzīts uz statusu Apstiprināts

## <a name="symptoms"></a>Simptomi

Pirkšanas pasūtījums, kas pakļauts izmaiņu pārvaldībai, ja vienīgā pieprasītā izmaiņa ir nosūtīšanas atlikuma atcelšana vienai vai vairākām rindām, tiks tieši pārsūtīts uz statusu *Apstiprināts*, kad tas tiks apstiprināts un žurnāls netiks izveidots.

## <a name="resolution"></a>Novēršana

Nosūtīšanas atlikuma atcelšana neietekmē apstiprinājumu žurnāla saturu. Šī funkcionalitāte jāizmanto, kad rinda ir daļēji saņemta un atlikusī kvalitāte ir jāatceļ procesa posmā pēc tam, kad ar kreditoru ir apstiprināts pirkšanas pasūtījums.

Ja tas jāatspoguļo pirkšanas pasūtījuma apstiprinājumā, daudzums ir jākoriģē pirkšanas pasūtījuma rindā, lai apstiprinājums tiktu pieprasīts. Pretējā gadījumā, ja rindā nekas nav saņemts, daudzumu var noņemt. Šādā gadījumā būs nepieciešams atkārtots apstiprinājums.
