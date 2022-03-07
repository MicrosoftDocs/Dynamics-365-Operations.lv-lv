---
title: Vispārējā plānošana ģenerē fantoma precēm plānotos pasūtījumus
description: Plānotie pasūtījumi tiek ģenerēti fantoma precēm pēc tam, kad palaista vispārējā plānošana.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742008"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Vispārējā plānošana ģenerē fantoma precēm plānotos pasūtījumus

KB numurs: 4614729

## <a name="symptoms"></a>Simptomi

Plānotie pasūtījumi tiek ģenerēti fantoma precēm pēc tam, kad palaista vispārējā plānošana.

## <a name="resolution"></a>Novēršana

**Fantoma** opcijas iestatījums izlaistajām precēm nosaka noklusējuma rindas tipu materiālu komplektā (MK). Ja **Fantoma** opcija ir iestatīta uz *Jā*, sistēma joprojām izveidos plānotos pasūtījumus krājumam, bet **Tieši atvasinātās vajadzības** opcija katram plānotajam pasūtījumam tiks iestatīta uz *Jā*. Tāpēc plānoto ražošanas pasūtījumu nevar apstiprināt atsevišķi. Tā vietā tas vienmēr tiks automātiski iekļauts, kad pamata ražošanas pasūtījums ir apstiprināts. Turklāt plānotā fantoma pasūtījuma MK rindas tiek iekļautas pamata ražošanas pasūtījuma MK.
