---
title: Izveidot materiālu plānu līdzproduktiem
description: Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982213"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="09617-103">Izveidot materiālu plānu līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="09617-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09617-104">Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="09617-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="09617-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="09617-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="09617-106">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="09617-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="09617-107">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="09617-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="09617-108">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="09617-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="09617-109">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="09617-109">Click New.</span></span>
4. <span data-ttu-id="09617-110">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="09617-110">Click Sales order.</span></span>
5. <span data-ttu-id="09617-111">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="09617-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="09617-112">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="09617-112">Example: US-001</span></span>  
6. <span data-ttu-id="09617-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="09617-113">Click OK.</span></span>
7. <span data-ttu-id="09617-114">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="09617-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="09617-115">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="09617-115">Example: P6003</span></span>  
8. <span data-ttu-id="09617-116">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="09617-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="09617-117">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="09617-117">Example: 50000</span></span>  
9. <span data-ttu-id="09617-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="09617-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="09617-119">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="09617-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="09617-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="09617-120">Close the page.</span></span>
2. <span data-ttu-id="09617-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="09617-121">Close the page.</span></span>
3. <span data-ttu-id="09617-122">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="09617-122">Click Master planning.</span></span>
4. <span data-ttu-id="09617-123">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="09617-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="09617-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="09617-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="09617-125">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="09617-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="09617-126">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="09617-126">Click Run.</span></span>
7. <span data-ttu-id="09617-127">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="09617-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="09617-128">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="09617-128">Click Filter.</span></span>
9. <span data-ttu-id="09617-129">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="09617-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="09617-130">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="09617-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="09617-131">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="09617-131">Example: P6003</span></span>  
11. <span data-ttu-id="09617-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="09617-132">Click OK.</span></span>
12. <span data-ttu-id="09617-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="09617-133">Click OK.</span></span>
13. <span data-ttu-id="09617-134">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="09617-134">Click Planned orders.</span></span>
14. <span data-ttu-id="09617-135">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="09617-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="09617-136">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="09617-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="09617-137">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="09617-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="09617-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="09617-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="09617-139">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="09617-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="09617-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="09617-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="09617-141">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="09617-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="09617-142">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="09617-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="09617-143">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="09617-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="09617-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="09617-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="09617-145">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="09617-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="09617-146">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="09617-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="09617-147">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="09617-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="09617-148">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="09617-148">Click New.</span></span>
4. <span data-ttu-id="09617-149">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="09617-149">Click Sales order.</span></span>
5. <span data-ttu-id="09617-150">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="09617-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="09617-151">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="09617-151">Example: US-001</span></span>  
6. <span data-ttu-id="09617-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="09617-152">Click OK.</span></span>
7. <span data-ttu-id="09617-153">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="09617-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="09617-154">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="09617-154">Example: P6003</span></span>  
8. <span data-ttu-id="09617-155">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="09617-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="09617-156">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="09617-156">Example: 50000</span></span>  
9. <span data-ttu-id="09617-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="09617-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="09617-158">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="09617-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="09617-159">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="09617-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="09617-160">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="09617-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="09617-161">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="09617-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="09617-162">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="09617-162">Click Run.</span></span>
4. <span data-ttu-id="09617-163">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="09617-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="09617-164">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="09617-164">Click Filter.</span></span>
6. <span data-ttu-id="09617-165">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="09617-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="09617-166">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="09617-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="09617-167">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="09617-167">Example: P6003</span></span>  
8. <span data-ttu-id="09617-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="09617-168">Click OK.</span></span>
9. <span data-ttu-id="09617-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="09617-169">Click OK.</span></span>
10. <span data-ttu-id="09617-170">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="09617-170">Click Planned orders.</span></span>
11. <span data-ttu-id="09617-171">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="09617-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="09617-172">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="09617-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="09617-173">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="09617-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="09617-174">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="09617-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="09617-175">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="09617-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="09617-176">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="09617-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="09617-177">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="09617-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="09617-178">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="09617-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="09617-179">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="09617-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="09617-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="09617-180">Close the page.</span></span>
17. <span data-ttu-id="09617-181">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="09617-181">Click Master planning.</span></span>
18. <span data-ttu-id="09617-182">Doties uz Vispārējā plānošana > Iestatīšana > Vispārējas plānošanas parametri.</span><span class="sxs-lookup"><span data-stu-id="09617-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="09617-183">Laukā Atspējot visus plānošanas procesus atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="09617-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="09617-184">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="09617-184">Close the page.</span></span>

