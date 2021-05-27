---
title: Tieši atvasinātie apstiprinātie pasūtījumi tiek apstrādāti, izmantojot pārskatīšanas darbplūsmu
description: Tieši atvasinātie apstiprinātie pasūtījumi tiek apstrādāti, izmantojot darbplūsmu ar Pārskatīšanas statusu.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026719"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Tieši atvasinātie apstiprinātie pasūtījumi tiek apstrādāti, izmantojot pārskatīšanas darbplūsmu

KB numurs: 4612450

## <a name="symptoms"></a>Simptomi

Tieši atvasinātie apstiprinātie pasūtījumi tiek apstrādāti, izmantojot darbplūsmu ar *Pārskatīšanas* statusu.

## <a name="resolution"></a>Novēršana

Kad ir iespējota gadījuma izmaiņu izsekošana, *Pārskatīšanas* statuss tiek piešķirts apstiprinātiem atvasinātiem pasūtījumiem (pakārtotie pirkšanas pasūtījumi). Tādēļ, ja pirkšanas pasūtījums ir atvasināts (pakārtots pirkšanas pasūtījums), tas tiek iesniegts tikai darbplūsmai. Ja pirkšanas pasūtījums ir apstiprināts plānotais pirkšanas pasūtījums, tas tiek automātiski apstiprināts, lai nodrošinātu, ka plānošanas programma neveido jaunus plānotos pasūtījumus, kamēr pirkšanas pasūtījumam joprojām ir statuss *Melnraksts*.
