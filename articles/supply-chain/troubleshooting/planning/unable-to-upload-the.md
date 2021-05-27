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
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="8bbcd-103">Jūs nevarat atjaunināt prognozētās vienības izmaksas, kad importējat pieprasījuma apjoma prognozes ierakstus</span><span class="sxs-lookup"><span data-stu-id="8bbcd-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="8bbcd-104">KB numurs: 4614109</span><span class="sxs-lookup"><span data-stu-id="8bbcd-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="8bbcd-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="8bbcd-105">Symptoms</span></span>

<span data-ttu-id="8bbcd-106">Kad izmantojat datu elementus, lai importētu pieprasījuma prognozes ierakstus, esošo ierakstu **Prognozētās vienības izmaksu** vērtība netiek atjaunināta, lai tā atbilstu importētajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="8bbcd-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="8bbcd-107">Iemesls</span><span class="sxs-lookup"><span data-stu-id="8bbcd-107">Cause</span></span>

<span data-ttu-id="8bbcd-108">**Prognozētās vienības izmaksas** ir tikai lasāms lauks.</span><span class="sxs-lookup"><span data-stu-id="8bbcd-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="8bbcd-109">Vērtība tiek pamatota uz preces vienības izmaksām, un to nevar iestatīt tieši, izmantojot importu.</span><span class="sxs-lookup"><span data-stu-id="8bbcd-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="8bbcd-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="8bbcd-110">Resolution</span></span>

<span data-ttu-id="8bbcd-111">Tā kā lauks ir tikai lasāms, tam nevar importēt vērtības.</span><span class="sxs-lookup"><span data-stu-id="8bbcd-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="8bbcd-112">Vērtība tiks aprēķināta saskaņā ar esošo biznesa loģiku.</span><span class="sxs-lookup"><span data-stu-id="8bbcd-112">The value will be calculated according to the existing business logic.</span></span>
