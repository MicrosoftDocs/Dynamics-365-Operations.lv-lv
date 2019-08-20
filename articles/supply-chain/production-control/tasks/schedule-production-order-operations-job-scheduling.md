---
title: Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu
description: Šajā procedūrā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4932cfa472c34a16249b226aa4a07b8e5f528053
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838491"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="639e3-103">Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu</span><span class="sxs-lookup"><span data-stu-id="639e3-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="639e3-104">Šajā procedūrā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="639e3-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="639e3-105">Ar operāciju plānošanu netiek izveidots neviens darbs, bet darbi tiek izveidoti ar darbu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="639e3-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="639e3-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="639e3-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="639e3-107">Šī procedūra ir paredzēta ražošanas vadītājam, ražošanas plānotājam vai ražotnes vadītājam, kas strādā diskrētās ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="639e3-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="639e3-108">Ražošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="639e3-108">Create a production order</span></span>
1. <span data-ttu-id="639e3-109">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="639e3-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="639e3-110">Noklikšķiniet uz Jauns ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="639e3-110">Click New production order.</span></span>
3. <span data-ttu-id="639e3-111">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="639e3-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="639e3-112">Atlasiet krājuma kodu D0001.</span><span class="sxs-lookup"><span data-stu-id="639e3-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="639e3-113">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="639e3-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="639e3-114">Ieplānot operācijas ražošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="639e3-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="639e3-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="639e3-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="639e3-116">Atlasiet ražošanas pasūtījumu, kuru tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="639e3-116">Select the production order that you have just created.</span></span> <span data-ttu-id="639e3-117">Tam vajadzētu atrasties saraksta augšgalā.</span><span class="sxs-lookup"><span data-stu-id="639e3-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="639e3-118">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="639e3-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="639e3-119">Noklikšķiniet uz Plānot operācijas.</span><span class="sxs-lookup"><span data-stu-id="639e3-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="639e3-120">Laukā Plānošanas virziens atlasiet “No plānošanas datuma uz priekšu”.</span><span class="sxs-lookup"><span data-stu-id="639e3-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="639e3-121">Laukā Plānošanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="639e3-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="639e3-122">Atlasiet kādu nākotnes datumu, piemēram, vienu nedēļu pēc šodienas.</span><span class="sxs-lookup"><span data-stu-id="639e3-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="639e3-123">Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="639e3-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="639e3-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="639e3-124">Click OK.</span></span>
7. <span data-ttu-id="639e3-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="639e3-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="639e3-126">Ņemiet vērā, ka statuss tiek mainīts uz Plānots.</span><span class="sxs-lookup"><span data-stu-id="639e3-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="639e3-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="639e3-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="639e3-128">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="639e3-128">Click All jobs.</span></span>
    * <span data-ttu-id="639e3-129">Ņemiet vērā, ka darbi tiek izveidoti ar operāciju plānošanu.</span><span class="sxs-lookup"><span data-stu-id="639e3-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="639e3-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="639e3-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="639e3-131">Ieplānot darbus ražošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="639e3-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="639e3-132">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="639e3-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="639e3-133">Noklikšķiniet uz Plānot darbus.</span><span class="sxs-lookup"><span data-stu-id="639e3-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="639e3-134">Laukā Plānošanas virziens atlasiet “No plānošanas datuma uz priekšu”.</span><span class="sxs-lookup"><span data-stu-id="639e3-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="639e3-135">Laukā Plānošanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="639e3-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="639e3-136">Atlasiet kādu datumu nākotnē, piemēram, vienu nedēļu pēc šodienas.</span><span class="sxs-lookup"><span data-stu-id="639e3-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="639e3-137">Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="639e3-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="639e3-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="639e3-138">Click OK.</span></span>
6. <span data-ttu-id="639e3-139">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="639e3-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="639e3-140">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="639e3-140">Click All jobs.</span></span>
    * <span data-ttu-id="639e3-141">Ņemiet vērā, ka, pamatojoties uz aktīvo maršrutu, ar darbu plānošanu tiek izveidoti 5 darbi.</span><span class="sxs-lookup"><span data-stu-id="639e3-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

