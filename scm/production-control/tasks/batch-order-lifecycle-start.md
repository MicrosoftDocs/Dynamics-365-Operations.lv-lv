--- 
title: "Partijas pasūtījuma dzīves cikls no izveidošanas līdz sākšanai"
description: "Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 418bf29aff3ff03455b4be150409fc9b55e965c9
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="3cf96-103">Partijas pasūtījuma dzīves cikls no izveidošanas līdz sākšanai</span><span class="sxs-lookup"><span data-stu-id="3cf96-103">Batch order lifecycle from create to start</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3cf96-104">Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa.</span><span class="sxs-lookup"><span data-stu-id="3cf96-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="3cf96-105">No izveides, izmaksu novērtējuma un ražošanas darbu plānošanas līdz faktiskajam partijas pasūtījuma sākumam.</span><span class="sxs-lookup"><span data-stu-id="3cf96-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="3cf96-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="3cf96-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="3cf96-107">Lai veiktu procedūras izpildi ar citu datu kopu, ir nepieciešama izlaista prece ar aktīvu formulu un maršruta versiju.</span><span class="sxs-lookup"><span data-stu-id="3cf96-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="3cf96-108">Partijas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="3cf96-108">Create a batch order</span></span>
1. <span data-ttu-id="3cf96-109">Dodieties uz Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="3cf96-109">Go to All production orders.</span></span>
2. <span data-ttu-id="3cf96-110">Noklikšķiniet uz Jauns partijas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="3cf96-110">Click New batch order.</span></span>
3. <span data-ttu-id="3cf96-111">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3cf96-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="3cf96-112">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="3cf96-112">Click Create.</span></span>
5. <span data-ttu-id="3cf96-113">Izmantojiet ātro filtru, lai filtrētu pēc lauka Ražošana ar vērtību “b”.</span><span class="sxs-lookup"><span data-stu-id="3cf96-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="3cf96-114">Ražošanas formulas un paredzamo līdzproduktu skatīšana</span><span class="sxs-lookup"><span data-stu-id="3cf96-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="3cf96-115">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="3cf96-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="3cf96-116">Noklikšķiniet uz Formula.</span><span class="sxs-lookup"><span data-stu-id="3cf96-116">Click Formula.</span></span>
3. <span data-ttu-id="3cf96-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-117">Close the page.</span></span>
4. <span data-ttu-id="3cf96-118">Nokliksķiniet uz Līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="3cf96-118">Click Co-products.</span></span>
5. <span data-ttu-id="3cf96-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="3cf96-120">Partijas pasūtījuma novērtējums</span><span class="sxs-lookup"><span data-stu-id="3cf96-120">Estimate the batch order</span></span>
1. <span data-ttu-id="3cf96-121">Noklikšķiniet uz Novērtējums.</span><span class="sxs-lookup"><span data-stu-id="3cf96-121">Click Estimate.</span></span>
2. <span data-ttu-id="3cf96-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3cf96-122">Click OK.</span></span>
3. <span data-ttu-id="3cf96-123">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="3cf96-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="3cf96-124">Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-124">Click View calculation details.</span></span>
5. <span data-ttu-id="3cf96-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="3cf96-126">Partijas pasūtījuma izlaišana</span><span class="sxs-lookup"><span data-stu-id="3cf96-126">Release the batch order</span></span>
1. <span data-ttu-id="3cf96-127">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="3cf96-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="3cf96-128">Noklikšķiniet uz Nodot izpildei.</span><span class="sxs-lookup"><span data-stu-id="3cf96-128">Click Release.</span></span>
3. <span data-ttu-id="3cf96-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3cf96-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="3cf96-130">Ražošanas darbu plānošana</span><span class="sxs-lookup"><span data-stu-id="3cf96-130">Schedule production jobs</span></span>
1. <span data-ttu-id="3cf96-131">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="3cf96-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="3cf96-132">Noklikšķiniet uz Plānot darbus.</span><span class="sxs-lookup"><span data-stu-id="3cf96-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="3cf96-133">Laukā Ierobežota noslodze atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="3cf96-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="3cf96-134">Laukā Ierobežots materiāls atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="3cf96-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="3cf96-135">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="3cf96-135">Click OK.</span></span>
6. <span data-ttu-id="3cf96-136">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="3cf96-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="3cf96-137">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="3cf96-137">Click All jobs.</span></span>
8. <span data-ttu-id="3cf96-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="3cf96-139">Partijas pasūtījuma uzsākšana</span><span class="sxs-lookup"><span data-stu-id="3cf96-139">Start the batch order</span></span>
1. <span data-ttu-id="3cf96-140">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="3cf96-140">Click Start.</span></span>
2. <span data-ttu-id="3cf96-141">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="3cf96-141">Click the General tab.</span></span>
3. <span data-ttu-id="3cf96-142">Laukā Grāmatot izdošanas sarakstu tagad atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="3cf96-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="3cf96-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3cf96-143">Click OK.</span></span>
5. <span data-ttu-id="3cf96-144">Darbību rūtī noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="3cf96-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="3cf96-145">Noklikšķiniet uz Izdošanas saraksts.</span><span class="sxs-lookup"><span data-stu-id="3cf96-145">Click Picking list.</span></span>
7. <span data-ttu-id="3cf96-146">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3cf96-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3cf96-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-147">Close the page.</span></span>
9. <span data-ttu-id="3cf96-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-148">Close the page.</span></span>
10. <span data-ttu-id="3cf96-149">Noklikšķiniet uz Maršruta karte.</span><span class="sxs-lookup"><span data-stu-id="3cf96-149">Click Route card.</span></span>
11. <span data-ttu-id="3cf96-150">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3cf96-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="3cf96-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-151">Close the page.</span></span>
13. <span data-ttu-id="3cf96-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3cf96-152">Close the page.</span></span>


