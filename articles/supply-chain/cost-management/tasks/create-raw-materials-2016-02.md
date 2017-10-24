--- 
title: "Izejmateriālu izveide (tikai 2016. gada februāris)"
description: "Šajā uzdevumā uzmanība ir vērsta uz pabeigtu un daļēji pabeigtu preču komponentu izveidošanu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3d77dcc20fe7402af83dd724e7fef848977e5bf8
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="7816c-103">Izejmateriālu izveide (tikai 2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="7816c-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7816c-104">Šajā uzdevumā uzmanība ir vērsta uz pabeigtu un daļēji pabeigtu preču komponentu izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="7816c-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="7816c-105">Tas ir MK aprēķina sērijas trešais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="7816c-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="7816c-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="7816c-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="7816c-107">Izveidot pirmo materiālu</span><span class="sxs-lookup"><span data-stu-id="7816c-107">Create the first material</span></span>
1. <span data-ttu-id="7816c-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="7816c-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7816c-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7816c-109">Click New.</span></span>
3. <span data-ttu-id="7816c-110">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7816c-111">Šajā piemērā ievadiet ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7816c-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="7816c-112">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-113">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="7816c-113">Select STD.</span></span> <span data-ttu-id="7816c-114">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="7816c-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="7816c-115">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-116">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="7816c-116">For example, select Audio.</span></span> <span data-ttu-id="7816c-117">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="7816c-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="7816c-118">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-119">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7816c-119">Select SiteWH.</span></span> <span data-ttu-id="7816c-120">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="7816c-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="7816c-121">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-122">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="7816c-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7816c-123">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="7816c-123">Select None.</span></span>  
8. <span data-ttu-id="7816c-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7816c-124">Click OK.</span></span>
9. <span data-ttu-id="7816c-125">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="7816c-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="7816c-126">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="7816c-126">Click Default order settings.</span></span>
11. <span data-ttu-id="7816c-127">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-128">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7816c-129">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-130">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7816c-131">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-132">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="7816c-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-133">Close the page.</span></span>
15. <span data-ttu-id="7816c-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-134">Close the page.</span></span>
16. <span data-ttu-id="7816c-135">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7816c-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7816c-136">Noklikšķiniet uz ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7816c-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="7816c-137">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7816c-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="7816c-138">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7816c-139">Šajā piemērā ierakstiet vērtību M2.</span><span class="sxs-lookup"><span data-stu-id="7816c-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="7816c-140">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7816c-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="7816c-141">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="7816c-141">Click Item price.</span></span>
21. <span data-ttu-id="7816c-142">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7816c-142">Click New.</span></span>
22. <span data-ttu-id="7816c-143">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-144">Šajā piemērā atlasiet vērtību 10, kas ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="7816c-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="7816c-145">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-146">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="7816c-147">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="7816c-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7816c-148">Šajā piemērā ierakstiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="7816c-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="7816c-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7816c-149">Click Save.</span></span>
26. <span data-ttu-id="7816c-150">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="7816c-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="7816c-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-151">Close the page.</span></span>
28. <span data-ttu-id="7816c-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="7816c-153">Izveidot otro materiālu</span><span class="sxs-lookup"><span data-stu-id="7816c-153">Create the second material</span></span>
1. <span data-ttu-id="7816c-154">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7816c-154">Click New.</span></span>
2. <span data-ttu-id="7816c-155">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7816c-156">Šajā piemērā ierakstiet vērtību ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7816c-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="7816c-157">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-158">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="7816c-158">Select STD.</span></span> <span data-ttu-id="7816c-159">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="7816c-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7816c-160">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-161">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="7816c-161">For example, select Audio.</span></span> <span data-ttu-id="7816c-162">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="7816c-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7816c-163">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-164">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7816c-164">Select SiteWH.</span></span> <span data-ttu-id="7816c-165">Šajā piemērā tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="7816c-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="7816c-166">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-167">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="7816c-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7816c-168">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="7816c-168">Select None.</span></span>  
7. <span data-ttu-id="7816c-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7816c-169">Click OK.</span></span>
8. <span data-ttu-id="7816c-170">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="7816c-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7816c-171">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="7816c-171">Click Default order settings.</span></span>
10. <span data-ttu-id="7816c-172">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-173">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7816c-174">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-175">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7816c-176">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-177">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7816c-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-178">Close the page.</span></span>
14. <span data-ttu-id="7816c-179">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-179">Close the page.</span></span>
15. <span data-ttu-id="7816c-180">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7816c-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7816c-181">Noklikšķiniet uz ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7816c-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="7816c-182">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7816c-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7816c-183">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7816c-184">Šajā piemērā ierakstiet vērtību M2.</span><span class="sxs-lookup"><span data-stu-id="7816c-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="7816c-185">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7816c-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7816c-186">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="7816c-186">Click Item price.</span></span>
20. <span data-ttu-id="7816c-187">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7816c-187">Click New.</span></span>
21. <span data-ttu-id="7816c-188">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-189">Šajā piemērā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="7816c-189">For this example, select 10.</span></span> <span data-ttu-id="7816c-190">Šis ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="7816c-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7816c-191">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-192">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7816c-193">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="7816c-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7816c-194">Demonstrācijas nolūkos ierakstiet 10.</span><span class="sxs-lookup"><span data-stu-id="7816c-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="7816c-195">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7816c-195">Click Save.</span></span>
25. <span data-ttu-id="7816c-196">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="7816c-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7816c-197">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-197">Close the page.</span></span>
27. <span data-ttu-id="7816c-198">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="7816c-199">Izveidot trešo materiālu</span><span class="sxs-lookup"><span data-stu-id="7816c-199">Create the third material</span></span>
1. <span data-ttu-id="7816c-200">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7816c-200">Click New.</span></span>
2. <span data-ttu-id="7816c-201">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7816c-202">Demonstrācijas nolūkos ierakstiet ITEM_C</span><span class="sxs-lookup"><span data-stu-id="7816c-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="7816c-203">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-204">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="7816c-204">Select STD.</span></span> <span data-ttu-id="7816c-205">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="7816c-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7816c-206">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-207">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="7816c-207">For example, select Audio.</span></span> <span data-ttu-id="7816c-208">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="7816c-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7816c-209">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-210">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7816c-210">Select SiteWH.</span></span> <span data-ttu-id="7816c-211">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="7816c-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="7816c-212">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-213">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="7816c-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7816c-214">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="7816c-214">Select None.</span></span>  
7. <span data-ttu-id="7816c-215">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7816c-215">Click OK.</span></span>
8. <span data-ttu-id="7816c-216">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="7816c-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7816c-217">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="7816c-217">Click Default order settings.</span></span>
10. <span data-ttu-id="7816c-218">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-219">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7816c-220">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-221">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7816c-222">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-223">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7816c-224">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-224">Close the page.</span></span>
14. <span data-ttu-id="7816c-225">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-225">Close the page.</span></span>
15. <span data-ttu-id="7816c-226">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7816c-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7816c-227">Noklikšķiniet uz ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="7816c-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="7816c-228">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7816c-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7816c-229">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7816c-230">Šajā piemērā ierakstiet vērtību M1.</span><span class="sxs-lookup"><span data-stu-id="7816c-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="7816c-231">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7816c-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7816c-232">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="7816c-232">Click Item price.</span></span>
20. <span data-ttu-id="7816c-233">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7816c-233">Click New.</span></span>
21. <span data-ttu-id="7816c-234">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-235">Šajā piemērā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="7816c-235">For this example, select 10.</span></span> <span data-ttu-id="7816c-236">Šis ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="7816c-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7816c-237">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7816c-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7816c-238">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7816c-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7816c-239">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="7816c-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7816c-240">Šajā piemērā ierakstiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="7816c-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="7816c-241">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7816c-241">Click Save.</span></span>
25. <span data-ttu-id="7816c-242">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="7816c-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7816c-243">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-243">Close the page.</span></span>
27. <span data-ttu-id="7816c-244">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7816c-244">Close the page.</span></span>


