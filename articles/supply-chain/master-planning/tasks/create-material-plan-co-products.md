---
title: Izveidot materiālu plānu līdzproduktiem
description: Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148082"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="d4382-103">Izveidot materiālu plānu līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="d4382-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4382-104">Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="d4382-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="d4382-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="d4382-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="d4382-106">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="d4382-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="d4382-107">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="d4382-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="d4382-108">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="d4382-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="d4382-109">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="d4382-109">Click New.</span></span>
4. <span data-ttu-id="d4382-110">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="d4382-110">Click Sales order.</span></span>
5. <span data-ttu-id="d4382-111">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4382-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="d4382-112">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="d4382-112">Example: US-001</span></span>  
6. <span data-ttu-id="d4382-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4382-113">Click OK.</span></span>
7. <span data-ttu-id="d4382-114">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4382-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d4382-115">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="d4382-115">Example: P6003</span></span>  
8. <span data-ttu-id="d4382-116">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d4382-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d4382-117">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="d4382-117">Example: 50000</span></span>  
9. <span data-ttu-id="d4382-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d4382-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="d4382-119">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="d4382-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="d4382-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4382-120">Close the page.</span></span>
2. <span data-ttu-id="d4382-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4382-121">Close the page.</span></span>
3. <span data-ttu-id="d4382-122">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="d4382-122">Click Master planning.</span></span>
4. <span data-ttu-id="d4382-123">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4382-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d4382-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4382-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d4382-125">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="d4382-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="d4382-126">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="d4382-126">Click Run.</span></span>
7. <span data-ttu-id="d4382-127">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="d4382-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="d4382-128">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="d4382-128">Click Filter.</span></span>
9. <span data-ttu-id="d4382-129">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="d4382-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="d4382-130">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4382-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="d4382-131">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="d4382-131">Example: P6003</span></span>  
11. <span data-ttu-id="d4382-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4382-132">Click OK.</span></span>
12. <span data-ttu-id="d4382-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4382-133">Click OK.</span></span>
13. <span data-ttu-id="d4382-134">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="d4382-134">Click Planned orders.</span></span>
14. <span data-ttu-id="d4382-135">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d4382-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d4382-136">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="d4382-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="d4382-137">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d4382-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="d4382-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d4382-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d4382-139">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="d4382-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="d4382-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4382-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="d4382-141">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="d4382-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="d4382-142">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4382-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d4382-143">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="d4382-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="d4382-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4382-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="d4382-145">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="d4382-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="d4382-146">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="d4382-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="d4382-147">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="d4382-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="d4382-148">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="d4382-148">Click New.</span></span>
4. <span data-ttu-id="d4382-149">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="d4382-149">Click Sales order.</span></span>
5. <span data-ttu-id="d4382-150">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4382-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="d4382-151">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="d4382-151">Example: US-001</span></span>  
6. <span data-ttu-id="d4382-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4382-152">Click OK.</span></span>
7. <span data-ttu-id="d4382-153">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4382-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d4382-154">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="d4382-154">Example: P6003</span></span>  
8. <span data-ttu-id="d4382-155">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d4382-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d4382-156">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="d4382-156">Example: 50000</span></span>  
9. <span data-ttu-id="d4382-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d4382-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="d4382-158">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="d4382-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="d4382-159">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4382-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="d4382-160">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4382-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d4382-161">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="d4382-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="d4382-162">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="d4382-162">Click Run.</span></span>
4. <span data-ttu-id="d4382-163">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="d4382-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="d4382-164">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="d4382-164">Click Filter.</span></span>
6. <span data-ttu-id="d4382-165">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="d4382-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="d4382-166">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4382-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="d4382-167">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="d4382-167">Example: P6003</span></span>  
8. <span data-ttu-id="d4382-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4382-168">Click OK.</span></span>
9. <span data-ttu-id="d4382-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4382-169">Click OK.</span></span>
10. <span data-ttu-id="d4382-170">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="d4382-170">Click Planned orders.</span></span>
11. <span data-ttu-id="d4382-171">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d4382-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d4382-172">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="d4382-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="d4382-173">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d4382-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="d4382-174">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d4382-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d4382-175">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="d4382-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="d4382-176">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4382-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d4382-177">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="d4382-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="d4382-178">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4382-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d4382-179">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="d4382-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="d4382-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4382-180">Close the page.</span></span>
17. <span data-ttu-id="d4382-181">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="d4382-181">Click Master planning.</span></span>
18. <span data-ttu-id="d4382-182">Doties uz Vispārējā plānošana > Iestatīšana > Vispārējas plānošanas parametri.</span><span class="sxs-lookup"><span data-stu-id="d4382-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="d4382-183">Laukā Atspējot visus plānošanas procesus atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="d4382-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="d4382-184">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4382-184">Close the page.</span></span>

