---
title: Materiālu pārsūtīšana, izmantojot Kanban darbus
description: Šajā procedūrā parādīts, kā izpildīt Kanban atsaukšanas darbu, lai pārsūtītu materiālus.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2db7b9fb960beb5b4a851aabb9f28a0f9e3d3da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "367436"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="914d9-103">Materiālu pārsūtīšana, izmantojot Kanban darbus</span><span class="sxs-lookup"><span data-stu-id="914d9-103">Transfer materials with kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="914d9-104">Šajā procedūrā parādīts, kā izpildīt Kanban atsaukšanas darbu, lai pārsūtītu materiālus.</span><span class="sxs-lookup"><span data-stu-id="914d9-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="914d9-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="914d9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="914d9-106">Šī procedūra ir paredzēta noliktavas darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="914d9-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="914d9-107">Pārsūtīšanas darbu attēlošana</span><span class="sxs-lookup"><span data-stu-id="914d9-107">Display transfer jobs</span></span>
1. <span data-ttu-id="914d9-108">Pārejiet uz sadaļu Ražošanas kontrole > Kanban >Pārsūtīšanas darbu Kanban panelis.</span><span class="sxs-lookup"><span data-stu-id="914d9-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="914d9-109">Izvērsiet vai sakļaujiet sadaļu Filtri.</span><span class="sxs-lookup"><span data-stu-id="914d9-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="914d9-110">Sadaļā Filtri varat norādīt, kurus darbus vēlaties apskatīt, filtrējot pēc parametriem Ražošanas plūsma, Aktivitātes nosaukums, No noliktavas un atrašanās vietas un Uz noliktavu un atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="914d9-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="914d9-111">Laukā No noliktavas ierakstiet "11".</span><span class="sxs-lookup"><span data-stu-id="914d9-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="914d9-112">Laukā Uz atrašanās vietu ierakstiet "12".</span><span class="sxs-lookup"><span data-stu-id="914d9-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="914d9-113">Sākt pārvietošanas darbu</span><span class="sxs-lookup"><span data-stu-id="914d9-113">Start a transfer job</span></span>
1. <span data-ttu-id="914d9-114">Sarakstā noņemiet atlasi no atlasītās rindas, ja tāda ir.</span><span class="sxs-lookup"><span data-stu-id="914d9-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="914d9-115">Sarakstā atlasiet 4. rindu.</span><span class="sxs-lookup"><span data-stu-id="914d9-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="914d9-116">Atlasiet pirmo darbu ar statusu Nav plānots.</span><span class="sxs-lookup"><span data-stu-id="914d9-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="914d9-117">Pārliecinieties, ka šis ir vienīgais atlasītais darbs.</span><span class="sxs-lookup"><span data-stu-id="914d9-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="914d9-118">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="914d9-118">Click Start.</span></span>
    * <span data-ttu-id="914d9-119">Ņemiet vērā, ka ikona norāda, ka darbs ir sākts.</span><span class="sxs-lookup"><span data-stu-id="914d9-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="914d9-120">Atlasiet otro pārsūtīšanas darbu un mainiet daudzumu</span><span class="sxs-lookup"><span data-stu-id="914d9-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="914d9-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="914d9-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="914d9-122">Varat atlasīt vairākus darbus, bet tagad atlasiet 5. rindu.</span><span class="sxs-lookup"><span data-stu-id="914d9-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="914d9-123">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="914d9-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="914d9-124">Pārliecinieties, ka iepriekšējā soļa darbs ir vienīgais atlasītais.</span><span class="sxs-lookup"><span data-stu-id="914d9-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="914d9-125">Atceliet visu citu darbu atlasi.</span><span class="sxs-lookup"><span data-stu-id="914d9-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="914d9-126">Ievērojiet vērtību laukā Darba apjoms vēlākai atsaucei</span><span class="sxs-lookup"><span data-stu-id="914d9-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="914d9-127">Vienumam Darba apjoms iestatiet vērtību "30".</span><span class="sxs-lookup"><span data-stu-id="914d9-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="914d9-128">Ņemiet vērā brīdinājumu.</span><span class="sxs-lookup"><span data-stu-id="914d9-128">Notice the warning!</span></span> <span data-ttu-id="914d9-129">Jums nav atļauts pārsūtīt 30.</span><span class="sxs-lookup"><span data-stu-id="914d9-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="914d9-130">Saskaņā ar Kanban nosacījuma iestatījumu varat pārsūtīt tikai sākotnējo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="914d9-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="914d9-131">Lietojiet vērtību, ko iepriekš ievērojāt laukā Darba apjoms</span><span class="sxs-lookup"><span data-stu-id="914d9-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="914d9-132">Iestatiet darba daudzuma vērtību uz iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="914d9-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="914d9-133">Sāciet otro pārsūtīšanas darbu</span><span class="sxs-lookup"><span data-stu-id="914d9-133">Start the second transfer job</span></span>
1. <span data-ttu-id="914d9-134">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="914d9-134">Click Start.</span></span>
    * <span data-ttu-id="914d9-135">Šādi tiks uzsākta 5. rindas darba pārsūtīšana.</span><span class="sxs-lookup"><span data-stu-id="914d9-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="914d9-136">Pabeidziet abus pārvietošanas darbus</span><span class="sxs-lookup"><span data-stu-id="914d9-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="914d9-137">Sarakstā atlasiet 4. rindu.</span><span class="sxs-lookup"><span data-stu-id="914d9-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="914d9-138">Tagad ir atlasīti divi pārsūtīšanas darbi — 4. rindā un 5. rindā.</span><span class="sxs-lookup"><span data-stu-id="914d9-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="914d9-139">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="914d9-139">Click Complete.</span></span>
    * <span data-ttu-id="914d9-140">Šī darbība pabeigs abu darbu pārsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="914d9-140">This will complete the transfer of both jobs.</span></span>  

