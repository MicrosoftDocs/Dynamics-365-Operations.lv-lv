---
title: Izmantot filtrus plānam
description: Šajā tēmā izskaidrots, kā izmantot filtrus plānam, kad izmanto funkcionalitāti Plānošanas optimizācija.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0e65d04b7b5261ffe72e67ef5321967f7af0ca20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970385"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="d297c-103">Izmantot filtrus plānam</span><span class="sxs-lookup"><span data-stu-id="d297c-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d297c-104">Kad tiek izmantota plānošanas optimizācijas funkcionalitāte, var izmantot filtru plānam.</span><span class="sxs-lookup"><span data-stu-id="d297c-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="d297c-105">**Plāna filtrs**  vienmēr tiks lietots vispārējās plānošanas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="d297c-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="d297c-106">**Plāna filtrs** ir noderīgs, ja vēlaties ierobežot plānu līdz noteiktai krājumu grupai, un pārliecināties, vai citi krājumi nav ietverti kā daļa no iegūtās vispārējās plānošanas.</span><span class="sxs-lookup"><span data-stu-id="d297c-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="d297c-107">Ja tiek lietots **Plāna filtrs** un tiek lietots arī izpildlaika filtrs vispārējās plānošanas izpildes laikā, tikai abu filtru krustpunkts tiek iekļauts plānošanas darbībā.</span><span class="sxs-lookup"><span data-stu-id="d297c-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="d297c-108">**Plāna filtram** var piekļūt no **Vispārējiem plāniem**, kad tiek izmantota plānošanas optimizācija.</span><span class="sxs-lookup"><span data-stu-id="d297c-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="d297c-109">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="d297c-109">Example scenario</span></span>

<span data-ttu-id="d297c-110">Ir iestatīts plāna filtrs, kas ietver krājumus A, B un C. Vispārējā plānošana tiek palaista vienam un tam pašam plānam, bet tiek piemēroti dažādi izpildlaika filtri:</span><span class="sxs-lookup"><span data-stu-id="d297c-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="d297c-111">**Izpildlaika filtrs, kas ietver krājumu D:** Netiek plānoti krājumi, jo starp plāna filtru un izpildlaika filtru nav krustpunkta.</span><span class="sxs-lookup"><span data-stu-id="d297c-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="d297c-112">**Izpildlaika filtrs, kas ietver krājumus A un D:** Plānošanas darbībā iekļauj tikai krājumu A, jo krājums D nav daļa no plāna filtra.</span><span class="sxs-lookup"><span data-stu-id="d297c-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="d297c-113">**Izpildlaika filtrs, kas ietver krājumu B:** Plānošanas darbībā iekļauj tikai krājumu B, un tiek paturēta iepriekšējais plānošanas izvade krājumam A.</span><span class="sxs-lookup"><span data-stu-id="d297c-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="d297c-114">**Izpildlaika filtrs, kas ietver visus elementus (tukšs filtrs):** Krājumi A, B un C tiek iekļauti plānošanas darbībā, un iepriekšējā plānošanas izvade A un B tiek pārrakstīta.</span><span class="sxs-lookup"><span data-stu-id="d297c-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="d297c-115">Jums vajadzētu izvairīties no plāna filtra iestatīšanas plānā, kas ir izvēlēts kā **Pašreizējais dinamiskais vispārējais plāns** **Vispārējās plānošanas parametru** lapā.</span><span class="sxs-lookup"><span data-stu-id="d297c-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="d297c-116">Pretējā gadījumā dinamiskā vispārējā plāna funkcionalitāte tiks ierobežota līdz filtrētajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="d297c-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="d297c-117">Piemēram, ja neto vajadzības tiek atjauninātas krājumam, kas nav daļa no plāna filtra, rezultāts netiks ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="d297c-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="d297c-118">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="d297c-118">Related resources</span></span>

[<span data-ttu-id="d297c-119">Plānošanas optimizācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="d297c-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="d297c-120">Darba sākšana ar Plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="d297c-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="d297c-121">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="d297c-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="d297c-122">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="d297c-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="d297c-123">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="d297c-123">Cancel a planning job</span></span>](cancel-planning-job.md)
