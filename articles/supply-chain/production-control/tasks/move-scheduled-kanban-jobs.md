--- 
title: "Plānoto Kanban darbu pārvietošana"
description: "Šajā procedūrā parādīts, kā pārvietot plānotu procesu Kanban darbus uz citu periodu."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ae6ea66f0e0ce03008882e59140ad7a0d89f0e30
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="912ef-103">Plānoto Kanban darbu pārvietošana</span><span class="sxs-lookup"><span data-stu-id="912ef-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="912ef-104">Šajā procedūrā parādīts, kā pārvietot plānotu procesu Kanban darbus uz citu periodu.</span><span class="sxs-lookup"><span data-stu-id="912ef-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="912ef-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="912ef-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="912ef-106">Šī procedūra ir paredzēta ražotnes vadītājam vai ražošanas plānotājam, kas strādā ar Kanban.</span><span class="sxs-lookup"><span data-stu-id="912ef-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="912ef-107">Atlasiet plānotos Kanban darbus</span><span class="sxs-lookup"><span data-stu-id="912ef-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="912ef-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="912ef-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="912ef-109">!MtCMR!Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="912ef-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="912ef-110">áçêìõý!</span><span class="sxs-lookup"><span data-stu-id="912ef-110">áçêìõý !</span></span>
3. <span data-ttu-id="912ef-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="912ef-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="912ef-112">Atlasiet darba šūnu 1250.</span><span class="sxs-lookup"><span data-stu-id="912ef-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="912ef-113">Klik på Select.</span><span class="sxs-lookup"><span data-stu-id="912ef-113">Klik på Select.</span></span>
5. <span data-ttu-id="912ef-114">Vælg 'Planlagt' i feltet Display job status.</span><span class="sxs-lookup"><span data-stu-id="912ef-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="912ef-115">Šādi darbu saraksts tiek filtrēts, lai parādītu tikai plānotos kanban darbus.</span><span class="sxs-lookup"><span data-stu-id="912ef-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="912ef-116">Kanban darbu pārvietošana uz citu periodu</span><span class="sxs-lookup"><span data-stu-id="912ef-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="912ef-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="912ef-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="912ef-118">Atlasiet darbu ar statusu Plānots, piemēram, darbu, kas laukā Plānotais periods plānots 2012. gada 20. decembrī.</span><span class="sxs-lookup"><span data-stu-id="912ef-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="912ef-119">Pēc tam pārvietojiet darbu uz iepriekšējo periodu.</span><span class="sxs-lookup"><span data-stu-id="912ef-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="912ef-120">Klik på Previous period.</span><span class="sxs-lookup"><span data-stu-id="912ef-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="912ef-121">Klik på End.</span><span class="sxs-lookup"><span data-stu-id="912ef-121">Klik på End.</span></span>
    * <span data-ttu-id="912ef-122">Šādi darbs tiks pārvietots uz darbu saraksta beigām, padarot to par pēdējo darbu iepriekšējā periodā.</span><span class="sxs-lookup"><span data-stu-id="912ef-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="912ef-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="912ef-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="912ef-124">Atlasiet darbu ar statusu Plānots, piemēram, darbu, kas laukā Plānotais periods plānots 2012. gada 18. decembrī.</span><span class="sxs-lookup"><span data-stu-id="912ef-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="912ef-125">Pēc tam pārvietojiet darbu uz nākamo periodu.</span><span class="sxs-lookup"><span data-stu-id="912ef-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="912ef-126">Klik på Next period.</span><span class="sxs-lookup"><span data-stu-id="912ef-126">Klik på Next period.</span></span>
6. <span data-ttu-id="912ef-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="912ef-127">Klik på Start.</span></span>
    * <span data-ttu-id="912ef-128">Šādi darbs tiks pārvietots uz darbu saraksta sākumu, padarot to par pirmo darbu iepriekšējā periodā.</span><span class="sxs-lookup"><span data-stu-id="912ef-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="912ef-129">Uzdevums: darba pārvietošana perioda ietvaros</span><span class="sxs-lookup"><span data-stu-id="912ef-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="912ef-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="912ef-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="912ef-131">Atlasiet darbu ar statusu Plānots, piemēram, otro darbu, kas laukā Plānotais periods plānots 2012. gada 19. decembrī.</span><span class="sxs-lookup"><span data-stu-id="912ef-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="912ef-132">Pēc tam pārvietojiet darbu plānotajā periodā.</span><span class="sxs-lookup"><span data-stu-id="912ef-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="912ef-133">Klik på Forward.</span><span class="sxs-lookup"><span data-stu-id="912ef-133">Klik på Forward.</span></span>
    * <span data-ttu-id="912ef-134">Ņemiet vērā, ka darbs tiek pārvietots sarakstā par vienu rindu uz leju.</span><span class="sxs-lookup"><span data-stu-id="912ef-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="912ef-135">Klik på Backward.</span><span class="sxs-lookup"><span data-stu-id="912ef-135">Klik på Backward.</span></span>
    * <span data-ttu-id="912ef-136">Ņemiet vērā, ka darbs tiek pārvietots sarakstā par vienu rindu uz augšu.</span><span class="sxs-lookup"><span data-stu-id="912ef-136">Notice that the job is moved one line up on the list.</span></span>  


