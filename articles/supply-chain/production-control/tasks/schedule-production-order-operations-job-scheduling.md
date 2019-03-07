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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2019
ms.locfileid: "352463"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="843a5-103">Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu</span><span class="sxs-lookup"><span data-stu-id="843a5-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="843a5-104">Šajā procedūrā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="843a5-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="843a5-105">Ar operāciju plānošanu netiek izveidots neviens darbs, bet darbi tiek izveidoti ar darbu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="843a5-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="843a5-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="843a5-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="843a5-107">Šī procedūra ir paredzēta ražošanas vadītājam, ražošanas plānotājam vai ražotnes vadītājam, kas strādā diskrētās ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="843a5-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="843a5-108">Ražošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="843a5-108">Create a production order</span></span>
1. <span data-ttu-id="843a5-109">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="843a5-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="843a5-110">Noklikšķiniet uz Jauns ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="843a5-110">Click New production order.</span></span>
3. <span data-ttu-id="843a5-111">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843a5-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="843a5-112">Atlasiet krājuma kodu D0001.</span><span class="sxs-lookup"><span data-stu-id="843a5-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="843a5-113">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="843a5-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="843a5-114">Ieplānot operācijas ražošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="843a5-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="843a5-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="843a5-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="843a5-116">Atlasiet ražošanas pasūtījumu, kuru tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="843a5-116">Select the production order that you have just created.</span></span> <span data-ttu-id="843a5-117">Tam vajadzētu atrasties saraksta augšgalā.</span><span class="sxs-lookup"><span data-stu-id="843a5-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="843a5-118">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="843a5-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="843a5-119">Noklikšķiniet uz Plānot operācijas.</span><span class="sxs-lookup"><span data-stu-id="843a5-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="843a5-120">Laukā Plānošanas virziens atlasiet “No plānošanas datuma uz priekšu”.</span><span class="sxs-lookup"><span data-stu-id="843a5-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="843a5-121">Laukā Plānošanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="843a5-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="843a5-122">Atlasiet kādu nākotnes datumu, piemēram, vienu nedēļu pēc šodienas.</span><span class="sxs-lookup"><span data-stu-id="843a5-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="843a5-123">Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="843a5-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="843a5-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="843a5-124">Click OK.</span></span>
7. <span data-ttu-id="843a5-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="843a5-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="843a5-126">Ņemiet vērā, ka statuss tiek mainīts uz Plānots.</span><span class="sxs-lookup"><span data-stu-id="843a5-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="843a5-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="843a5-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="843a5-128">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="843a5-128">Click All jobs.</span></span>
    * <span data-ttu-id="843a5-129">Ņemiet vērā, ka darbi tiek izveidoti ar operāciju plānošanu.</span><span class="sxs-lookup"><span data-stu-id="843a5-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="843a5-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="843a5-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="843a5-131">Ieplānot darbus ražošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="843a5-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="843a5-132">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="843a5-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="843a5-133">Noklikšķiniet uz Plānot darbus.</span><span class="sxs-lookup"><span data-stu-id="843a5-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="843a5-134">Laukā Plānošanas virziens atlasiet “No plānošanas datuma uz priekšu”.</span><span class="sxs-lookup"><span data-stu-id="843a5-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="843a5-135">Laukā Plānošanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="843a5-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="843a5-136">Atlasiet kādu datumu nākotnē, piemēram, vienu nedēļu pēc šodienas.</span><span class="sxs-lookup"><span data-stu-id="843a5-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="843a5-137">Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="843a5-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="843a5-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="843a5-138">Click OK.</span></span>
6. <span data-ttu-id="843a5-139">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="843a5-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="843a5-140">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="843a5-140">Click All jobs.</span></span>
    * <span data-ttu-id="843a5-141">Ņemiet vērā, ka, pamatojoties uz aktīvo maršrutu, ar darbu plānošanu tiek izveidoti 5 darbi.</span><span class="sxs-lookup"><span data-stu-id="843a5-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

