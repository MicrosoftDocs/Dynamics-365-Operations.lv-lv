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
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026718"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Vispārējā plānošana ģenerē fantoma precēm plānotos pasūtījumus

KB numurs: 4614729

## <a name="symptoms"></a>Simptomi

Plānotie pasūtījumi tiek ģenerēti fantoma precēm pēc tam, kad palaista vispārējā plānošana.

## <a name="resolution"></a>Novēršana

**Fantoma** opcijas iestatījums izlaistajām precēm nosaka noklusējuma rindas tipu materiālu komplektā (MK). Ja **Fantoma** opcija ir iestatīta uz *Jā*, sistēma joprojām izveidos plānotos pasūtījumus krājumam, bet **Tieši atvasinātās vajadzības** opcija katram plānotajam pasūtījumam tiks iestatīta uz *Jā*. Tāpēc plānoto ražošanas pasūtījumu nevar apstiprināt atsevišķi. Tā vietā tas vienmēr tiks automātiski iekļauts, kad pamata ražošanas pasūtījums ir apstiprināts. Turklāt plānotā fantoma pasūtījuma MK rindas tiek iekļautas pamata ražošanas pasūtījuma MK.
