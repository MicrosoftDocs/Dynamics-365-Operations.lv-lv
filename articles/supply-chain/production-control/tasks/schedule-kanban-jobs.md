---
title: Kanban darbu grafika izveide
description: Šajā procedūrā apskatīts Kanban darbu plānošanas process noteiktai darba šūnai.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5dc359309dd96d93a59fbfb6d0b0f64cfaddc5fa
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146587"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="8e827-103">Kanban darbu grafika izveide</span><span class="sxs-lookup"><span data-stu-id="8e827-103">Schedule kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e827-104">Šajā procedūrā apskatīts Kanban darbu plānošanas process noteiktai darba šūnai.</span><span class="sxs-lookup"><span data-stu-id="8e827-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="8e827-105">Šīs procedūras izveides priekšnosacījums ir procedūra "Sagatavot procesa Kanban darbu, kad materiāli nav pieejami".</span><span class="sxs-lookup"><span data-stu-id="8e827-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="8e827-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="8e827-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8e827-107">Šis uzdevums ir paredzēts ražotnes vadītājam un ražošanas plānotājam, kas strādā ar Kanban.</span><span class="sxs-lookup"><span data-stu-id="8e827-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="8e827-108">Kanban darbu atlase darba šūnai</span><span class="sxs-lookup"><span data-stu-id="8e827-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="8e827-109">Pārejiet uz sadaļu Ražošanas kontrole > Kanban > Kanban darbu plānošana.</span><span class="sxs-lookup"><span data-stu-id="8e827-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="8e827-110">Izvērsiet sadaļas Perioda noslodze papildinformāciju</span><span class="sxs-lookup"><span data-stu-id="8e827-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="8e827-111">Izvērsiet Kanban papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="8e827-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="8e827-112">Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8e827-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8e827-113">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="8e827-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8e827-114">Atlasiet darba šūnu 1250.</span><span class="sxs-lookup"><span data-stu-id="8e827-114">Select work cell 1250.</span></span> <span data-ttu-id="8e827-115">Šādi atfiltrēsiet skatu, lai parādītu tikai darbus šūnai 1250.</span><span class="sxs-lookup"><span data-stu-id="8e827-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="8e827-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8e827-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8e827-117">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="8e827-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="8e827-118">Kanban darbs ieplānošana pirmajā pieejamā periodā</span><span class="sxs-lookup"><span data-stu-id="8e827-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="8e827-119">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="8e827-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8e827-120">Atlasiet pirmo rindu sarakstā, kuras statuss ir Nav plānots.</span><span class="sxs-lookup"><span data-stu-id="8e827-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="8e827-121">Punktotā ikona laukā Darba statuss norāda, ka statuss ir Nav plānots.</span><span class="sxs-lookup"><span data-stu-id="8e827-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="8e827-122">Noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="8e827-122">Click Schedule.</span></span>
    * <span data-ttu-id="8e827-123">Šādi Kanban darbs tiks ieplānots pirmajā pieejamā periodā.</span><span class="sxs-lookup"><span data-stu-id="8e827-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="8e827-124">Ņemiet vērā, ka Kanban darbs tiek pārvietots uz saraksta beigām, jo tas ir pievienots periodam, kas sākas šodien.</span><span class="sxs-lookup"><span data-stu-id="8e827-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="8e827-125">Ja periods, kas sākas šodien, ir pilnībā rezervēts, darbs tiks pārvietots uz pirmo pieejamo periodu.</span><span class="sxs-lookup"><span data-stu-id="8e827-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="8e827-126">Divu Kanban darbu plānošana noteiktai dienai</span><span class="sxs-lookup"><span data-stu-id="8e827-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="8e827-127">Sarakstā atlasiet 1. rindu.</span><span class="sxs-lookup"><span data-stu-id="8e827-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="8e827-128">Vajadzētu būt redzamam, ka pirmās rindas vērtība laukā Darba statuss ir Nav plānots.</span><span class="sxs-lookup"><span data-stu-id="8e827-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="8e827-129">Sarakstā atlasiet 2. rindu.</span><span class="sxs-lookup"><span data-stu-id="8e827-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="8e827-130">Vajadzētu būt redzamam, ka otrās rindas vērtība laukā Darba statuss ir Nav plānots.</span><span class="sxs-lookup"><span data-stu-id="8e827-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="8e827-131">Tagad esat atlasījis pirmos divus darbus.</span><span class="sxs-lookup"><span data-stu-id="8e827-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="8e827-132">Noklikšķiniet uz Grafiks no datuma, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8e827-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="8e827-133">Atzīmējiet rūtiņu Ignorēt noslodzes nepietiekamības sekas vai noņemiet atzīmi.</span><span class="sxs-lookup"><span data-stu-id="8e827-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="8e827-134">Šī opcija ļauj ignorēt noklusējuma noslodzes nepietiekamības sekas.</span><span class="sxs-lookup"><span data-stu-id="8e827-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="8e827-135">Laukā Noslodzes nepietiekamības sekas atlasiet Pievienot pieprasītajam periodam.</span><span class="sxs-lookup"><span data-stu-id="8e827-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="8e827-136">Šī opcija nodrošina, ka darbs tiek pievienots pieprasītajā periodā neatkarīgi no tā, vai darba šūna ir pārslogota.</span><span class="sxs-lookup"><span data-stu-id="8e827-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="8e827-137">Noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="8e827-137">Click Schedule.</span></span>
    * <span data-ttu-id="8e827-138">Ņemiet vērā, ka abi darbi tiek pievienoti izvēlētajam periodam.</span><span class="sxs-lookup"><span data-stu-id="8e827-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="8e827-139">Sadaļā Perioda noslodze varat redzēt katra perioda slodzi.</span><span class="sxs-lookup"><span data-stu-id="8e827-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="8e827-140">Laukā Patēriņš parādīts šī perioda plānotais patēriņš.</span><span class="sxs-lookup"><span data-stu-id="8e827-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="8e827-141">Ja plānotais patēriņš ir lielāks par šajā periodā pieejamo noslodzi, tiks atlasīts pārslodzes patēriņš.</span><span class="sxs-lookup"><span data-stu-id="8e827-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

