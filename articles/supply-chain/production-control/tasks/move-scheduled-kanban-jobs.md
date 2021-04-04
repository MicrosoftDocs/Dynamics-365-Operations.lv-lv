---
title: Plānoto Kanban darbu pārvietošana
description: Šajā procedūrā parādīts, kā pārvietot plānotu procesu Kanban darbus uz citu periodu.
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b945cdfa3e013c213e718962499831df126f09b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259750"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="4a878-103">Plānoto Kanban darbu pārvietošana</span><span class="sxs-lookup"><span data-stu-id="4a878-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a878-104">Šajā procedūrā parādīts, kā pārvietot plānotu procesu Kanban darbus uz citu periodu.</span><span class="sxs-lookup"><span data-stu-id="4a878-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="4a878-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="4a878-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4a878-106">Šī procedūra ir paredzēta ražotnes vadītājam vai ražošanas plānotājam, kas strādā ar Kanban.</span><span class="sxs-lookup"><span data-stu-id="4a878-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="4a878-107">Atl. plānotos Kanban darbus.</span><span class="sxs-lookup"><span data-stu-id="4a878-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="4a878-108">Dod. uz sad. **Raž. kontr. > Kanban > Kanban darbu plān.**.</span><span class="sxs-lookup"><span data-stu-id="4a878-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="4a878-109">Laukā **Darba šūna** nokl. uz nolaiž. sar. pogas, lai atv. uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="4a878-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="4a878-110">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="4a878-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="4a878-111">Atlasiet darba šūnu 1250.</span><span class="sxs-lookup"><span data-stu-id="4a878-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="4a878-112">Noklikšķiniet uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="4a878-112">Click **Select**.</span></span> 

5. <span data-ttu-id="4a878-113">Laukā **Rādīt darba statusu** atlasiet **Plānots**.</span><span class="sxs-lookup"><span data-stu-id="4a878-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="4a878-114">Šādi darbu saraksts tiek filtrēts, lai parādītu tikai plānotos kanban darbus.</span><span class="sxs-lookup"><span data-stu-id="4a878-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="4a878-115">Pārv. Kanban darbus uz citu periodu.</span><span class="sxs-lookup"><span data-stu-id="4a878-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="4a878-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4a878-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="4a878-117">Atlasiet darbu ar statusu **Plānots darbs**, piemēram, darbu, kas laukā **Plānotais periods** plānots 2012. gada 20. decembrī.</span><span class="sxs-lookup"><span data-stu-id="4a878-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="4a878-118">Pēc tam pārvietojiet darbu uz iepriekšējo periodu.</span><span class="sxs-lookup"><span data-stu-id="4a878-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="4a878-119">Nokl. **Iepr. periods**.</span><span class="sxs-lookup"><span data-stu-id="4a878-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="4a878-120">Nokl. **Beigas**, lai darbu pārv. uz darbu sar. beigām un tas būtu pēd. darbs iepr. periodā.</span><span class="sxs-lookup"><span data-stu-id="4a878-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="4a878-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4a878-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="4a878-122">Atlasiet darbu ar statusu **Plānots darbs**, piemēram, darbu, kas laukā **Plānotais periods** plānots 2012. gada 18. decembrī.</span><span class="sxs-lookup"><span data-stu-id="4a878-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="4a878-123">Pēc tam pārvietojiet darbu uz nākamo periodu.</span><span class="sxs-lookup"><span data-stu-id="4a878-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="4a878-124">Nokl. **Nāk. per**.</span><span class="sxs-lookup"><span data-stu-id="4a878-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="4a878-125">Nokl. **Sākums**, lai darbu pārv. uz darbu sar. sākumu un tas būtu pirmais. darbs iepr. periodā.</span><span class="sxs-lookup"><span data-stu-id="4a878-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="4a878-126">Darba pārv. per. ietvaros.</span><span class="sxs-lookup"><span data-stu-id="4a878-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="4a878-127">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4a878-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="4a878-128">Atlasiet darbu ar statusu Plānots, piemēram, otro darbu, kas laukā **Plānotais periods** plānots 2012. gada 19. decembrī.</span><span class="sxs-lookup"><span data-stu-id="4a878-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="4a878-129">Pēc tam pārvietojiet darbu plānotajā periodā.</span><span class="sxs-lookup"><span data-stu-id="4a878-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="4a878-130">Nokl. **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="4a878-130">Click **Forward**.</span></span> <span data-ttu-id="4a878-131">Ņemiet vērā, ka darbs tiek pārvietots sarakstā par vienu rindu uz leju.</span><span class="sxs-lookup"><span data-stu-id="4a878-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="4a878-132">Nokl. **Atpakaļ**.</span><span class="sxs-lookup"><span data-stu-id="4a878-132">Click **Backward**.</span></span> <span data-ttu-id="4a878-133">Ņemiet vērā, ka darbs tiek pārvietots sarakstā par vienu rindu uz augšu.</span><span class="sxs-lookup"><span data-stu-id="4a878-133">Notice that the job is moved one line up on the list.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]