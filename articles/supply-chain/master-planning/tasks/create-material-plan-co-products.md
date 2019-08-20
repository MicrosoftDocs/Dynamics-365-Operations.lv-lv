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
ms.openlocfilehash: e59ff769685677b0970dbc7d4c9d4d2c1e5b63d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835962"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="fae06-103">Izveidot materiālu plānu līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="fae06-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fae06-104">Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="fae06-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="fae06-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="fae06-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="fae06-106">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="fae06-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="fae06-107">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="fae06-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="fae06-108">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="fae06-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="fae06-109">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="fae06-109">Click New.</span></span>
4. <span data-ttu-id="fae06-110">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="fae06-110">Click Sales order.</span></span>
5. <span data-ttu-id="fae06-111">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fae06-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="fae06-112">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="fae06-112">Example: US-001</span></span>  
6. <span data-ttu-id="fae06-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fae06-113">Click OK.</span></span>
7. <span data-ttu-id="fae06-114">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fae06-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fae06-115">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="fae06-115">Example: P6003</span></span>  
8. <span data-ttu-id="fae06-116">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="fae06-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="fae06-117">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="fae06-117">Example: 50000</span></span>  
9. <span data-ttu-id="fae06-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="fae06-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="fae06-119">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="fae06-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="fae06-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fae06-120">Close the page.</span></span>
2. <span data-ttu-id="fae06-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fae06-121">Close the page.</span></span>
3. <span data-ttu-id="fae06-122">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="fae06-122">Click Master planning.</span></span>
4. <span data-ttu-id="fae06-123">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="fae06-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fae06-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="fae06-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fae06-125">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="fae06-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="fae06-126">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="fae06-126">Click Run.</span></span>
7. <span data-ttu-id="fae06-127">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="fae06-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="fae06-128">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="fae06-128">Click Filter.</span></span>
9. <span data-ttu-id="fae06-129">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="fae06-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="fae06-130">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fae06-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="fae06-131">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="fae06-131">Example: P6003</span></span>  
11. <span data-ttu-id="fae06-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fae06-132">Click OK.</span></span>
12. <span data-ttu-id="fae06-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fae06-133">Click OK.</span></span>
13. <span data-ttu-id="fae06-134">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="fae06-134">Click Planned orders.</span></span>
14. <span data-ttu-id="fae06-135">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="fae06-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fae06-136">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="fae06-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="fae06-137">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="fae06-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="fae06-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="fae06-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fae06-139">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="fae06-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="fae06-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="fae06-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="fae06-141">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="fae06-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="fae06-142">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="fae06-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fae06-143">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="fae06-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="fae06-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fae06-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="fae06-145">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="fae06-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="fae06-146">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="fae06-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="fae06-147">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="fae06-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="fae06-148">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="fae06-148">Click New.</span></span>
4. <span data-ttu-id="fae06-149">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="fae06-149">Click Sales order.</span></span>
5. <span data-ttu-id="fae06-150">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fae06-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="fae06-151">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="fae06-151">Example: US-001</span></span>  
6. <span data-ttu-id="fae06-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fae06-152">Click OK.</span></span>
7. <span data-ttu-id="fae06-153">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fae06-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fae06-154">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="fae06-154">Example: P6003</span></span>  
8. <span data-ttu-id="fae06-155">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="fae06-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="fae06-156">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="fae06-156">Example: 50000</span></span>  
9. <span data-ttu-id="fae06-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="fae06-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="fae06-158">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="fae06-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="fae06-159">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="fae06-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="fae06-160">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="fae06-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fae06-161">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="fae06-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="fae06-162">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="fae06-162">Click Run.</span></span>
4. <span data-ttu-id="fae06-163">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="fae06-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="fae06-164">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="fae06-164">Click Filter.</span></span>
6. <span data-ttu-id="fae06-165">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="fae06-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="fae06-166">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fae06-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="fae06-167">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="fae06-167">Example: P6003</span></span>  
8. <span data-ttu-id="fae06-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fae06-168">Click OK.</span></span>
9. <span data-ttu-id="fae06-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fae06-169">Click OK.</span></span>
10. <span data-ttu-id="fae06-170">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="fae06-170">Click Planned orders.</span></span>
11. <span data-ttu-id="fae06-171">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="fae06-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fae06-172">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="fae06-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="fae06-173">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="fae06-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="fae06-174">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="fae06-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fae06-175">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="fae06-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="fae06-176">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="fae06-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="fae06-177">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="fae06-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="fae06-178">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="fae06-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fae06-179">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="fae06-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="fae06-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fae06-180">Close the page.</span></span>
17. <span data-ttu-id="fae06-181">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="fae06-181">Click Master planning.</span></span>
18. <span data-ttu-id="fae06-182">Doties uz Vispārējā plānošana > Iestatīšana > Vispārējas plānošanas parametri.</span><span class="sxs-lookup"><span data-stu-id="fae06-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="fae06-183">Laukā Atspējot visus plānošanas procesus atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="fae06-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="fae06-184">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fae06-184">Close the page.</span></span>

