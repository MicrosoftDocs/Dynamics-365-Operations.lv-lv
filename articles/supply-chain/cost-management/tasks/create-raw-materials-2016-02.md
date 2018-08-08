--- 
title: "Izejmateriālu izveide (tikai 2016. gada februāris)"
description: "Šajā uzdevumā uzmanība ir vērsta uz pabeigtu un daļēji pabeigtu preču komponentu izveidošanu."
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 869acddf6f7e9754bb4952176ded4b22c74eaffd
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="53679-103">Izejmateriālu izveide (tikai 2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="53679-103">Create raw materials (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53679-104">Šajā uzdevumā uzmanība ir vērsta uz pabeigtu un daļēji pabeigtu preču komponentu izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="53679-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="53679-105">Tas ir MK aprēķina sērijas trešais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="53679-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="53679-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="53679-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="53679-107">Izveidot pirmo materiālu</span><span class="sxs-lookup"><span data-stu-id="53679-107">Create the first material</span></span>
1. <span data-ttu-id="53679-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="53679-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="53679-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="53679-109">Click New.</span></span>
3. <span data-ttu-id="53679-110">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="53679-111">Šajā piemērā ievadiet ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="53679-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="53679-112">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-113">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="53679-113">Select STD.</span></span> <span data-ttu-id="53679-114">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="53679-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="53679-115">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-116">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="53679-116">For example, select Audio.</span></span> <span data-ttu-id="53679-117">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="53679-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="53679-118">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-119">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="53679-119">Select SiteWH.</span></span> <span data-ttu-id="53679-120">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="53679-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="53679-121">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-122">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="53679-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="53679-123">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="53679-123">Select None.</span></span>  
8. <span data-ttu-id="53679-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="53679-124">Click OK.</span></span>
9. <span data-ttu-id="53679-125">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="53679-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="53679-126">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="53679-126">Click Default order settings.</span></span>
11. <span data-ttu-id="53679-127">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-128">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="53679-129">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-130">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="53679-131">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-132">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="53679-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-133">Close the page.</span></span>
15. <span data-ttu-id="53679-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-134">Close the page.</span></span>
16. <span data-ttu-id="53679-135">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="53679-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="53679-136">Noklikšķiniet uz ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="53679-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="53679-137">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="53679-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="53679-138">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="53679-139">Šajā piemērā ierakstiet vērtību M2.</span><span class="sxs-lookup"><span data-stu-id="53679-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="53679-140">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="53679-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="53679-141">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="53679-141">Click Item price.</span></span>
21. <span data-ttu-id="53679-142">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="53679-142">Click New.</span></span>
22. <span data-ttu-id="53679-143">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-144">Šajā piemērā atlasiet vērtību 10, kas ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="53679-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="53679-145">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-146">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="53679-147">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="53679-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="53679-148">Šajā piemērā ierakstiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="53679-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="53679-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="53679-149">Click Save.</span></span>
26. <span data-ttu-id="53679-150">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="53679-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="53679-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-151">Close the page.</span></span>
28. <span data-ttu-id="53679-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="53679-153">Izveidot otro materiālu</span><span class="sxs-lookup"><span data-stu-id="53679-153">Create the second material</span></span>
1. <span data-ttu-id="53679-154">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="53679-154">Click New.</span></span>
2. <span data-ttu-id="53679-155">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="53679-156">Šajā piemērā ierakstiet vērtību ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="53679-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="53679-157">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-158">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="53679-158">Select STD.</span></span> <span data-ttu-id="53679-159">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="53679-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="53679-160">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-161">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="53679-161">For example, select Audio.</span></span> <span data-ttu-id="53679-162">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="53679-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="53679-163">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-164">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="53679-164">Select SiteWH.</span></span> <span data-ttu-id="53679-165">Šajā piemērā tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="53679-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="53679-166">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-167">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="53679-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="53679-168">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="53679-168">Select None.</span></span>  
7. <span data-ttu-id="53679-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="53679-169">Click OK.</span></span>
8. <span data-ttu-id="53679-170">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="53679-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="53679-171">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="53679-171">Click Default order settings.</span></span>
10. <span data-ttu-id="53679-172">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-173">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="53679-174">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-175">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="53679-176">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-177">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="53679-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-178">Close the page.</span></span>
14. <span data-ttu-id="53679-179">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-179">Close the page.</span></span>
15. <span data-ttu-id="53679-180">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="53679-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="53679-181">Noklikšķiniet uz ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="53679-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="53679-182">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="53679-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="53679-183">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="53679-184">Šajā piemērā ierakstiet vērtību M2.</span><span class="sxs-lookup"><span data-stu-id="53679-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="53679-185">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="53679-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="53679-186">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="53679-186">Click Item price.</span></span>
20. <span data-ttu-id="53679-187">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="53679-187">Click New.</span></span>
21. <span data-ttu-id="53679-188">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-189">Šajā piemērā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="53679-189">For this example, select 10.</span></span> <span data-ttu-id="53679-190">Šis ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="53679-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="53679-191">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-192">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="53679-193">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="53679-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="53679-194">Demonstrācijas nolūkos ierakstiet 10.</span><span class="sxs-lookup"><span data-stu-id="53679-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="53679-195">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="53679-195">Click Save.</span></span>
25. <span data-ttu-id="53679-196">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="53679-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="53679-197">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-197">Close the page.</span></span>
27. <span data-ttu-id="53679-198">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="53679-199">Izveidot trešo materiālu</span><span class="sxs-lookup"><span data-stu-id="53679-199">Create the third material</span></span>
1. <span data-ttu-id="53679-200">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="53679-200">Click New.</span></span>
2. <span data-ttu-id="53679-201">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="53679-202">Demonstrācijas nolūkos ierakstiet ITEM_C</span><span class="sxs-lookup"><span data-stu-id="53679-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="53679-203">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-204">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="53679-204">Select STD.</span></span> <span data-ttu-id="53679-205">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="53679-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="53679-206">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-207">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="53679-207">For example, select Audio.</span></span> <span data-ttu-id="53679-208">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="53679-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="53679-209">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-210">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="53679-210">Select SiteWH.</span></span> <span data-ttu-id="53679-211">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="53679-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="53679-212">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-213">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="53679-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="53679-214">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="53679-214">Select None.</span></span>  
7. <span data-ttu-id="53679-215">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="53679-215">Click OK.</span></span>
8. <span data-ttu-id="53679-216">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="53679-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="53679-217">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="53679-217">Click Default order settings.</span></span>
10. <span data-ttu-id="53679-218">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-219">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="53679-220">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-221">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="53679-222">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-223">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="53679-224">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-224">Close the page.</span></span>
14. <span data-ttu-id="53679-225">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-225">Close the page.</span></span>
15. <span data-ttu-id="53679-226">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="53679-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="53679-227">Noklikšķiniet uz ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="53679-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="53679-228">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="53679-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="53679-229">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="53679-230">Šajā piemērā ierakstiet vērtību M1.</span><span class="sxs-lookup"><span data-stu-id="53679-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="53679-231">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="53679-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="53679-232">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="53679-232">Click Item price.</span></span>
20. <span data-ttu-id="53679-233">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="53679-233">Click New.</span></span>
21. <span data-ttu-id="53679-234">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-235">Šajā piemērā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="53679-235">For this example, select 10.</span></span> <span data-ttu-id="53679-236">Šis ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="53679-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="53679-237">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53679-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="53679-238">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="53679-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="53679-239">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="53679-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="53679-240">Šajā piemērā ierakstiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="53679-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="53679-241">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="53679-241">Click Save.</span></span>
25. <span data-ttu-id="53679-242">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="53679-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="53679-243">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-243">Close the page.</span></span>
27. <span data-ttu-id="53679-244">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53679-244">Close the page.</span></span>


