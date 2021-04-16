---
title: Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu
description: Šajā tēmā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu.
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 883a68af78a9d91df089d30d8f1b3d7ba498d577
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841387"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="6410d-103">Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu</span><span class="sxs-lookup"><span data-stu-id="6410d-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6410d-104">Šajā tēmā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="6410d-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="6410d-105">Ar operāciju plānošanu netiek izveidots neviens darbs, bet darbi tiek izveidoti ar darbu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="6410d-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="6410d-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="6410d-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="6410d-107">Šī procedūra ir paredzēta ražošanas vadītājam, ražošanas plānotājam vai ražotnes vadītājam, kas strādā diskrētās ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="6410d-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="6410d-108">Ražošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="6410d-108">Create a production order</span></span>
1. <span data-ttu-id="6410d-109">Navigācijas rūtī atveriet **Moduļi > Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="6410d-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="6410d-110">Atlasiet **Jauns ražošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="6410d-110">Select **New production order**.</span></span>
3. <span data-ttu-id="6410d-111">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6410d-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="6410d-112">Atlasiet krājuma numuru **D0001**.</span><span class="sxs-lookup"><span data-stu-id="6410d-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="6410d-113">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="6410d-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="6410d-114">Ieplānot operācijas ražošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="6410d-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="6410d-115">Atzīmējiet jaunizveidoto rindu.</span><span class="sxs-lookup"><span data-stu-id="6410d-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="6410d-116">Darbības rūtī atlasiet **Ieplānot**.</span><span class="sxs-lookup"><span data-stu-id="6410d-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="6410d-117">Atlasiet **Ieplānot operācijas**.</span><span class="sxs-lookup"><span data-stu-id="6410d-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="6410d-118">Laukā **Plānošanas virziens** atlasiet **No plānošanas datuma uz priekšu**.</span><span class="sxs-lookup"><span data-stu-id="6410d-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="6410d-119">Laukā **Plānošanas datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="6410d-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="6410d-120">Atlasiet kādu nākotnes datumu, piemēram, vienu nedēļu pēc šodienas.</span><span class="sxs-lookup"><span data-stu-id="6410d-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="6410d-121">Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="6410d-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="6410d-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6410d-122">Select **OK**.</span></span>
7. <span data-ttu-id="6410d-123">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6410d-123">In the list, mark the selected row.</span></span> <span data-ttu-id="6410d-124">Ņemiet vērā, ka statuss tiek mainīts uz **Ieplānots**.</span><span class="sxs-lookup"><span data-stu-id="6410d-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="6410d-125">Atlasiet **Visi darbi**.</span><span class="sxs-lookup"><span data-stu-id="6410d-125">Select **All jobs**.</span></span> <span data-ttu-id="6410d-126">Ņemiet vērā, ka darbi tiek izveidoti ar operāciju plānošanu.</span><span class="sxs-lookup"><span data-stu-id="6410d-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="6410d-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6410d-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="6410d-128">Ieplānot darbus ražošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="6410d-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="6410d-129">Darbības rūtī atlasiet **Ieplānot**.</span><span class="sxs-lookup"><span data-stu-id="6410d-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="6410d-130">Atlasiet **Ieplānot darbus**.</span><span class="sxs-lookup"><span data-stu-id="6410d-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="6410d-131">Laukā **Plānošanas virziens** atlasiet **No plānošanas datuma uz priekšu**.</span><span class="sxs-lookup"><span data-stu-id="6410d-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="6410d-132">Laukā **Plānošanas datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="6410d-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="6410d-133">Atlasiet kādu datumu nākotnē, piemēram, vienu nedēļu pēc šodienas.</span><span class="sxs-lookup"><span data-stu-id="6410d-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="6410d-134">Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="6410d-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="6410d-135">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6410d-135">Select **OK**.</span></span>
6. <span data-ttu-id="6410d-136">Darbību rūtī atlasiet **Ražošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="6410d-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="6410d-137">Atlasiet **Visi darbi**.</span><span class="sxs-lookup"><span data-stu-id="6410d-137">Select **All jobs**.</span></span> <span data-ttu-id="6410d-138">Ņemiet vērā, ka, pamatojoties uz aktīvo maršrutu, ar darbu plānošanu tiek izveidoti 5 darbi.</span><span class="sxs-lookup"><span data-stu-id="6410d-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]