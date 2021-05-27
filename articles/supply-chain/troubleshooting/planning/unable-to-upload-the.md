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
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026715"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Jūs nevarat atjaunināt prognozētās vienības izmaksas, kad importējat pieprasījuma apjoma prognozes ierakstus

KB numurs: 4614109

## <a name="symptoms"></a>Simptomi

Kad izmantojat datu elementus, lai importētu pieprasījuma prognozes ierakstus, esošo ierakstu **Prognozētās vienības izmaksu** vērtība netiek atjaunināta, lai tā atbilstu importētajiem datiem.

## <a name="cause"></a>Iemesls

**Prognozētās vienības izmaksas** ir tikai lasāms lauks. Vērtība tiek pamatota uz preces vienības izmaksām, un to nevar iestatīt tieši, izmantojot importu.

## <a name="resolution"></a>Novēršana

Tā kā lauks ir tikai lasāms, tam nevar importēt vērtības. Vērtība tiks aprēķināta saskaņā ar esošo biznesa loģiku.
