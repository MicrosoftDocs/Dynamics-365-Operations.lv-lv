---
title: Jūs nevarat atjaunināt prognozētās vienības izmaksas, kad importējat pieprasījuma apjoma prognozes ierakstus
description: Kad izmantojat datu elementus, lai importētu pieprasījuma prognozes ierakstus, esošo ierakstu izmaksu cena netiek atjaunināta, lai tā atbilstu importētajiem datiem.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765374"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Jūs nevarat atjaunināt prognozētās vienības izmaksas, kad importējat pieprasījuma apjoma prognozes ierakstus

KB numurs: 4614109

## <a name="symptoms"></a>Simptomi

Kad izmantojat datu elementus, lai importētu pieprasījuma prognozes ierakstus, esošo ierakstu **Prognozētās vienības izmaksu** vērtība netiek atjaunināta, lai tā atbilstu importētajiem datiem.

## <a name="cause"></a>Iemesls

**Prognozētās vienības izmaksas** ir tikai lasāms lauks. Vērtība tiek pamatota uz preces vienības izmaksām, un to nevar iestatīt tieši, izmantojot importu.

## <a name="resolution"></a>Novēršana

Tā kā lauks ir tikai lasāms, tam nevar importēt vērtības. Vērtība tiks aprēķināta saskaņā ar esošo biznesa loģiku.
