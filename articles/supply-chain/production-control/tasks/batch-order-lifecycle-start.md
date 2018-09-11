--- 
title: "Partijas pasūtījuma dzīves cikls no izveidošanas līdz sākšanai"
description: "Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: b04960c0f92e8871e0de99b4ebb0c69e1225d21c
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="e7921-103">Partijas pasūtījuma dzīves cikls no izveidošanas līdz sākšanai</span><span class="sxs-lookup"><span data-stu-id="e7921-103">Batch order lifecycle from create to start</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7921-104">Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa.</span><span class="sxs-lookup"><span data-stu-id="e7921-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="e7921-105">No izveides, izmaksu novērtējuma un ražošanas darbu plānošanas līdz faktiskajam partijas pasūtījuma sākumam.</span><span class="sxs-lookup"><span data-stu-id="e7921-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="e7921-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e7921-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="e7921-107">Lai veiktu procedūras izpildi ar citu datu kopu, ir nepieciešama izlaista prece ar aktīvu formulu un maršruta versiju.</span><span class="sxs-lookup"><span data-stu-id="e7921-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="e7921-108">Partijas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="e7921-108">Create a batch order</span></span>
1. <span data-ttu-id="e7921-109">Dodieties uz Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e7921-109">Go to All production orders.</span></span>
2. <span data-ttu-id="e7921-110">Noklikšķiniet uz Jauns partijas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e7921-110">Click New batch order.</span></span>
3. <span data-ttu-id="e7921-111">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e7921-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="e7921-112">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="e7921-112">Click Create.</span></span>
5. <span data-ttu-id="e7921-113">Izmantojiet ātro filtru, lai filtrētu pēc lauka Ražošana ar vērtību “b”.</span><span class="sxs-lookup"><span data-stu-id="e7921-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="e7921-114">Ražošanas formulas un paredzamo līdzproduktu skatīšana</span><span class="sxs-lookup"><span data-stu-id="e7921-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="e7921-115">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e7921-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="e7921-116">Noklikšķiniet uz Formula.</span><span class="sxs-lookup"><span data-stu-id="e7921-116">Click Formula.</span></span>
3. <span data-ttu-id="e7921-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7921-117">Close the page.</span></span>
4. <span data-ttu-id="e7921-118">Nokliksķiniet uz Līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="e7921-118">Click Co-products.</span></span>
5. <span data-ttu-id="e7921-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7921-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="e7921-120">Partijas pasūtījuma novērtējums</span><span class="sxs-lookup"><span data-stu-id="e7921-120">Estimate the batch order</span></span>
1. <span data-ttu-id="e7921-121">Noklikšķiniet uz Novērtējums.</span><span class="sxs-lookup"><span data-stu-id="e7921-121">Click Estimate.</span></span>
2. <span data-ttu-id="e7921-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e7921-122">Click OK.</span></span>
3. <span data-ttu-id="e7921-123">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e7921-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="e7921-124">Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="e7921-124">Click View calculation details.</span></span>
5. <span data-ttu-id="e7921-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7921-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="e7921-126">Partijas pasūtījuma izlaišana</span><span class="sxs-lookup"><span data-stu-id="e7921-126">Release the batch order</span></span>
1. <span data-ttu-id="e7921-127">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e7921-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="e7921-128">Noklikšķiniet uz Nodot izpildei.</span><span class="sxs-lookup"><span data-stu-id="e7921-128">Click Release.</span></span>
3. <span data-ttu-id="e7921-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e7921-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="e7921-130">Ražošanas darbu plānošana</span><span class="sxs-lookup"><span data-stu-id="e7921-130">Schedule production jobs</span></span>
1. <span data-ttu-id="e7921-131">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="e7921-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="e7921-132">Noklikšķiniet uz Plānot darbus.</span><span class="sxs-lookup"><span data-stu-id="e7921-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="e7921-133">Laukā Ierobežota noslodze atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="e7921-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="e7921-134">Laukā Ierobežots materiāls atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="e7921-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="e7921-135">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="e7921-135">Click OK.</span></span>
6. <span data-ttu-id="e7921-136">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e7921-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="e7921-137">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="e7921-137">Click All jobs.</span></span>
8. <span data-ttu-id="e7921-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7921-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="e7921-139">Partijas pasūtījuma uzsākšana</span><span class="sxs-lookup"><span data-stu-id="e7921-139">Start the batch order</span></span>
1. <span data-ttu-id="e7921-140">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="e7921-140">Click Start.</span></span>
2. <span data-ttu-id="e7921-141">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="e7921-141">Click the General tab.</span></span>
3. <span data-ttu-id="e7921-142">Laukā Grāmatot izdošanas sarakstu tagad atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="e7921-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="e7921-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e7921-143">Click OK.</span></span>
5. <span data-ttu-id="e7921-144">Darbību rūtī noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="e7921-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="e7921-145">Noklikšķiniet uz Izdošanas saraksts.</span><span class="sxs-lookup"><span data-stu-id="e7921-145">Click Picking list.</span></span>
7. <span data-ttu-id="e7921-146">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e7921-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e7921-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7921-147">Close the page.</span></span>
9. <span data-ttu-id="e7921-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7921-148">Close the page.</span></span>
10. <span data-ttu-id="e7921-149">Noklikšķiniet uz Maršruta karte.</span><span class="sxs-lookup"><span data-stu-id="e7921-149">Click Route card.</span></span>
11. <span data-ttu-id="e7921-150">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e7921-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e7921-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7921-151">Close the page.</span></span>
13. <span data-ttu-id="e7921-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7921-152">Close the page.</span></span>


