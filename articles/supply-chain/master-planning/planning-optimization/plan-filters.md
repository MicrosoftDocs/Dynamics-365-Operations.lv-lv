---
title: Izmantot filtrus plānam
description: Šajā tēmā izskaidrots, kā izmantot filtrus plānam, kad izmanto funkcionalitāti Plānošanas optimizācija.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774007"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="36451-103">Izmantot filtrus plānam</span><span class="sxs-lookup"><span data-stu-id="36451-103">Apply filters to a plan</span></span>

<span data-ttu-id="36451-104">Kad tiek izmantota plānošanas optimizācijas funkcionalitāte, var izmantot filtru plānam.</span><span class="sxs-lookup"><span data-stu-id="36451-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="36451-105">Plāna filtrs vienmēr tiks lietots vispārējās plānošanas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="36451-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="36451-106">Plāna filtrs ir noderīgs, ja vēlaties ierobežot plānu līdz noteiktai krājumu grupai, un pārliecināties, vai citi krājumi nav ietverti kā daļa no iegūtās vispārējās plānošanas.</span><span class="sxs-lookup"><span data-stu-id="36451-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="36451-107">Ja tiek lietots plāna filtrs un tiek lietots arī izpildlaika filtrs vispārējās plānošanas izpildes laikā, tikai abu filtru krustpunkts tiek iekļauts plānošanas darbībā.</span><span class="sxs-lookup"><span data-stu-id="36451-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="36451-108">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="36451-108">Example scenario</span></span>

<span data-ttu-id="36451-109">Ir iestatīts plāna filtrs, kas ietver krājumus A, B un C. Vispārējā plānošana tiek palaista vienam un tam pašam plānam, bet tiek piemēroti dažādi izpildlaika filtri:</span><span class="sxs-lookup"><span data-stu-id="36451-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="36451-110">**Izpildlaika filtrs, kas ietver krājumu D:** Netiek plānoti krājumi, jo starp plāna filtru un izpildlaika filtru nav krustpunkta.</span><span class="sxs-lookup"><span data-stu-id="36451-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="36451-111">**Izpildlaika filtrs, kas ietver krājumus A un D:** Plānošanas darbībā iekļauj tikai krājumu A, jo krājums D nav daļa no plāna filtra.</span><span class="sxs-lookup"><span data-stu-id="36451-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="36451-112">**Izpildlaika filtrs, kas ietver krājumu B:** Plānošanas darbībā iekļauj tikai krājumu B, un tiek paturēta iepriekšējais plānošanas izvade krājumam A.</span><span class="sxs-lookup"><span data-stu-id="36451-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="36451-113">**Izpildlaika filtrs, kas ietver visus elementus (tukšs filtrs):** Krājumi A, B un C tiek iekļauti plānošanas darbībā, un iepriekšējā plānošanas izvade A un B tiek pārrakstīta.</span><span class="sxs-lookup"><span data-stu-id="36451-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="36451-114">Jums vajadzētu izvairīties no plāna filtra iestatīšanas plānā, kas ir izvēlēts kā **Pašreizējais dinamiskais vispārējais plāns** **Vispārējās plānošanas parametru** lapā.</span><span class="sxs-lookup"><span data-stu-id="36451-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="36451-115">Pretējā gadījumā dinamiskā vispārējā plāna funkcionalitāte tiks ierobežota līdz filtrētajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="36451-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="36451-116">Piemēram, ja neto vajadzības tiek atjauninātas krājumam, kas nav daļa no plāna filtra, rezultāts netiks ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="36451-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="36451-117">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="36451-117">Related resources</span></span>

[<span data-ttu-id="36451-118">Plānošanas optimizācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="36451-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="36451-119">Darba sākšana ar Plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="36451-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="36451-120">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="36451-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="36451-121">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="36451-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="36451-122">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="36451-122">Cancel a planning job</span></span>](cancel-planning-job.md)
