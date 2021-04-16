---
title: Partijas pasūtījuma dzīves cikls no izveides līdz sākšanai
description: Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d9ed44c9e05ea815e78ae041234ad61f76d89d8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825042"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="e7e41-103">Partijas pasūtījuma dzīves cikls no izveides līdz sākšanai</span><span class="sxs-lookup"><span data-stu-id="e7e41-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7e41-104">Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa.</span><span class="sxs-lookup"><span data-stu-id="e7e41-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="e7e41-105">No izveides, izmaksu novērtējuma un ražošanas darbu plānošanas līdz faktiskajam partijas pasūtījuma sākumam.</span><span class="sxs-lookup"><span data-stu-id="e7e41-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="e7e41-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e7e41-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="e7e41-107">Lai veiktu procedūras izpildi ar citu datu kopu, ir nepieciešama izlaista prece ar aktīvu formulu un maršruta versiju.</span><span class="sxs-lookup"><span data-stu-id="e7e41-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="e7e41-108">Partijas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="e7e41-108">Create a batch order</span></span>
1. <span data-ttu-id="e7e41-109">Dodieties uz Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e7e41-109">Go to All production orders.</span></span>
2. <span data-ttu-id="e7e41-110">Noklikšķiniet uz Jauns partijas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e7e41-110">Click New batch order.</span></span>
3. <span data-ttu-id="e7e41-111">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e7e41-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="e7e41-112">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="e7e41-112">Click Create.</span></span>
5. <span data-ttu-id="e7e41-113">Izmantojiet ātro filtru, lai filtrētu pēc lauka Ražošana ar vērtību “b”.</span><span class="sxs-lookup"><span data-stu-id="e7e41-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="e7e41-114">Ražošanas formulas un paredzamo līdzproduktu skatīšana</span><span class="sxs-lookup"><span data-stu-id="e7e41-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="e7e41-115">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e7e41-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="e7e41-116">Noklikšķiniet uz Formula.</span><span class="sxs-lookup"><span data-stu-id="e7e41-116">Click Formula.</span></span>
3. <span data-ttu-id="e7e41-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-117">Close the page.</span></span>
4. <span data-ttu-id="e7e41-118">Nokliksķiniet uz Līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="e7e41-118">Click Co-products.</span></span>
5. <span data-ttu-id="e7e41-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="e7e41-120">Partijas pasūtījuma novērtējums</span><span class="sxs-lookup"><span data-stu-id="e7e41-120">Estimate the batch order</span></span>
1. <span data-ttu-id="e7e41-121">Noklikšķiniet uz Novērtējums.</span><span class="sxs-lookup"><span data-stu-id="e7e41-121">Click Estimate.</span></span>
2. <span data-ttu-id="e7e41-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e7e41-122">Click OK.</span></span>
3. <span data-ttu-id="e7e41-123">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e7e41-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="e7e41-124">Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-124">Click View calculation details.</span></span>
5. <span data-ttu-id="e7e41-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="e7e41-126">Partijas pasūtījuma izlaišana</span><span class="sxs-lookup"><span data-stu-id="e7e41-126">Release the batch order</span></span>
1. <span data-ttu-id="e7e41-127">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e7e41-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="e7e41-128">Noklikšķiniet uz Nodot izpildei.</span><span class="sxs-lookup"><span data-stu-id="e7e41-128">Click Release.</span></span>
3. <span data-ttu-id="e7e41-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e7e41-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="e7e41-130">Ražošanas darbu plānošana</span><span class="sxs-lookup"><span data-stu-id="e7e41-130">Schedule production jobs</span></span>
1. <span data-ttu-id="e7e41-131">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="e7e41-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="e7e41-132">Noklikšķiniet uz Plānot darbus.</span><span class="sxs-lookup"><span data-stu-id="e7e41-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="e7e41-133">Laukā Ierobežota noslodze atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="e7e41-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="e7e41-134">Laukā Ierobežots materiāls atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="e7e41-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="e7e41-135">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="e7e41-135">Click OK.</span></span>
6. <span data-ttu-id="e7e41-136">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e7e41-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="e7e41-137">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="e7e41-137">Click All jobs.</span></span>
8. <span data-ttu-id="e7e41-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="e7e41-139">Partijas pasūtījuma uzsākšana</span><span class="sxs-lookup"><span data-stu-id="e7e41-139">Start the batch order</span></span>
1. <span data-ttu-id="e7e41-140">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="e7e41-140">Click Start.</span></span>
2. <span data-ttu-id="e7e41-141">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="e7e41-141">Click the General tab.</span></span>
3. <span data-ttu-id="e7e41-142">Laukā Grāmatot izdošanas sarakstu tagad atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="e7e41-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="e7e41-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e7e41-143">Click OK.</span></span>
5. <span data-ttu-id="e7e41-144">Darbību rūtī noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="e7e41-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="e7e41-145">Noklikšķiniet uz Izdošanas saraksts.</span><span class="sxs-lookup"><span data-stu-id="e7e41-145">Click Picking list.</span></span>
7. <span data-ttu-id="e7e41-146">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e7e41-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e7e41-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-147">Close the page.</span></span>
9. <span data-ttu-id="e7e41-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-148">Close the page.</span></span>
10. <span data-ttu-id="e7e41-149">Noklikšķiniet uz Maršruta karte.</span><span class="sxs-lookup"><span data-stu-id="e7e41-149">Click Route card.</span></span>
11. <span data-ttu-id="e7e41-150">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e7e41-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e7e41-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-151">Close the page.</span></span>
13. <span data-ttu-id="e7e41-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e7e41-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]