---
title: Izveidot izejmateriālus (2016. gada februāris)
description: Šajā uzdevumā uzmanība ir vērsta uz pabeigtu un daļēji pabeigtu preču komponentu izveidošanu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e20abf8a1b211bff2bc73d1a36a1e5c917ffaab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844589"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="7fecc-103">Izveidot izejmateriālus (2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="7fecc-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fecc-104">Šajā uzdevumā uzmanība ir vērsta uz pabeigtu un daļēji pabeigtu preču komponentu izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="7fecc-105">Tas ir MK aprēķina sērijas trešais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="7fecc-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="7fecc-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="7fecc-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="7fecc-107">Izveidot pirmo materiālu</span><span class="sxs-lookup"><span data-stu-id="7fecc-107">Create the first material</span></span>
1. <span data-ttu-id="7fecc-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="7fecc-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7fecc-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7fecc-109">Click New.</span></span>
3. <span data-ttu-id="7fecc-110">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7fecc-111">Šajā piemērā ievadiet ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7fecc-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="7fecc-112">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-113">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="7fecc-113">Select STD.</span></span> <span data-ttu-id="7fecc-114">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="7fecc-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="7fecc-115">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-116">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="7fecc-116">For example, select Audio.</span></span> <span data-ttu-id="7fecc-117">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="7fecc-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="7fecc-118">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-119">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7fecc-119">Select SiteWH.</span></span> <span data-ttu-id="7fecc-120">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="7fecc-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="7fecc-121">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-122">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7fecc-123">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="7fecc-123">Select None.</span></span>  
8. <span data-ttu-id="7fecc-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7fecc-124">Click OK.</span></span>
9. <span data-ttu-id="7fecc-125">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="7fecc-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="7fecc-126">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="7fecc-126">Click Default order settings.</span></span>
11. <span data-ttu-id="7fecc-127">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-128">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7fecc-129">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-130">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7fecc-131">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-132">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="7fecc-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-133">Close the page.</span></span>
15. <span data-ttu-id="7fecc-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-134">Close the page.</span></span>
16. <span data-ttu-id="7fecc-135">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7fecc-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7fecc-136">Noklikšķiniet uz ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7fecc-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="7fecc-137">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="7fecc-138">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7fecc-139">Šajā piemērā ierakstiet vērtību M2.</span><span class="sxs-lookup"><span data-stu-id="7fecc-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="7fecc-140">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="7fecc-141">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="7fecc-141">Click Item price.</span></span>
21. <span data-ttu-id="7fecc-142">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7fecc-142">Click New.</span></span>
22. <span data-ttu-id="7fecc-143">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-144">Šajā piemērā atlasiet vērtību 10, kas ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="7fecc-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="7fecc-145">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-146">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="7fecc-147">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="7fecc-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7fecc-148">Šajā piemērā ierakstiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="7fecc-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="7fecc-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7fecc-149">Click Save.</span></span>
26. <span data-ttu-id="7fecc-150">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="7fecc-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-151">Close the page.</span></span>
28. <span data-ttu-id="7fecc-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="7fecc-153">Izveidot otro materiālu</span><span class="sxs-lookup"><span data-stu-id="7fecc-153">Create the second material</span></span>
1. <span data-ttu-id="7fecc-154">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7fecc-154">Click New.</span></span>
2. <span data-ttu-id="7fecc-155">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7fecc-156">Šajā piemērā ierakstiet vērtību ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7fecc-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="7fecc-157">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-158">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="7fecc-158">Select STD.</span></span> <span data-ttu-id="7fecc-159">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="7fecc-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7fecc-160">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-161">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="7fecc-161">For example, select Audio.</span></span> <span data-ttu-id="7fecc-162">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="7fecc-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7fecc-163">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-164">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7fecc-164">Select SiteWH.</span></span> <span data-ttu-id="7fecc-165">Šajā piemērā tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="7fecc-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="7fecc-166">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-167">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7fecc-168">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="7fecc-168">Select None.</span></span>  
7. <span data-ttu-id="7fecc-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7fecc-169">Click OK.</span></span>
8. <span data-ttu-id="7fecc-170">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="7fecc-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7fecc-171">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="7fecc-171">Click Default order settings.</span></span>
10. <span data-ttu-id="7fecc-172">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-173">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7fecc-174">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-175">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7fecc-176">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-177">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7fecc-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-178">Close the page.</span></span>
14. <span data-ttu-id="7fecc-179">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-179">Close the page.</span></span>
15. <span data-ttu-id="7fecc-180">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7fecc-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7fecc-181">Noklikšķiniet uz ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7fecc-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="7fecc-182">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7fecc-183">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7fecc-184">Šajā piemērā ierakstiet vērtību M2.</span><span class="sxs-lookup"><span data-stu-id="7fecc-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="7fecc-185">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7fecc-186">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="7fecc-186">Click Item price.</span></span>
20. <span data-ttu-id="7fecc-187">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7fecc-187">Click New.</span></span>
21. <span data-ttu-id="7fecc-188">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-189">Šajā piemērā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="7fecc-189">For this example, select 10.</span></span> <span data-ttu-id="7fecc-190">Šis ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="7fecc-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7fecc-191">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-192">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7fecc-193">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="7fecc-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7fecc-194">Demonstrācijas nolūkos ierakstiet 10.</span><span class="sxs-lookup"><span data-stu-id="7fecc-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="7fecc-195">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7fecc-195">Click Save.</span></span>
25. <span data-ttu-id="7fecc-196">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7fecc-197">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-197">Close the page.</span></span>
27. <span data-ttu-id="7fecc-198">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="7fecc-199">Izveidot trešo materiālu</span><span class="sxs-lookup"><span data-stu-id="7fecc-199">Create the third material</span></span>
1. <span data-ttu-id="7fecc-200">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7fecc-200">Click New.</span></span>
2. <span data-ttu-id="7fecc-201">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7fecc-202">Demonstrācijas nolūkos ierakstiet ITEM_C</span><span class="sxs-lookup"><span data-stu-id="7fecc-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="7fecc-203">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-204">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="7fecc-204">Select STD.</span></span> <span data-ttu-id="7fecc-205">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="7fecc-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7fecc-206">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-207">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="7fecc-207">For example, select Audio.</span></span> <span data-ttu-id="7fecc-208">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="7fecc-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7fecc-209">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-210">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7fecc-210">Select SiteWH.</span></span> <span data-ttu-id="7fecc-211">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="7fecc-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="7fecc-212">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-213">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7fecc-214">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="7fecc-214">Select None.</span></span>  
7. <span data-ttu-id="7fecc-215">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7fecc-215">Click OK.</span></span>
8. <span data-ttu-id="7fecc-216">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="7fecc-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7fecc-217">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="7fecc-217">Click Default order settings.</span></span>
10. <span data-ttu-id="7fecc-218">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-219">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7fecc-220">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-221">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7fecc-222">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-223">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7fecc-224">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-224">Close the page.</span></span>
14. <span data-ttu-id="7fecc-225">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-225">Close the page.</span></span>
15. <span data-ttu-id="7fecc-226">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7fecc-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7fecc-227">Noklikšķiniet uz ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="7fecc-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="7fecc-228">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7fecc-229">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7fecc-230">Šajā piemērā ierakstiet vērtību M1.</span><span class="sxs-lookup"><span data-stu-id="7fecc-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="7fecc-231">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7fecc-232">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="7fecc-232">Click Item price.</span></span>
20. <span data-ttu-id="7fecc-233">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7fecc-233">Click New.</span></span>
21. <span data-ttu-id="7fecc-234">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-235">Šajā piemērā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="7fecc-235">For this example, select 10.</span></span> <span data-ttu-id="7fecc-236">Šis ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="7fecc-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7fecc-237">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7fecc-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7fecc-238">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7fecc-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7fecc-239">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="7fecc-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7fecc-240">Šajā piemērā ierakstiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="7fecc-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="7fecc-241">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7fecc-241">Click Save.</span></span>
25. <span data-ttu-id="7fecc-242">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="7fecc-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7fecc-243">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-243">Close the page.</span></span>
27. <span data-ttu-id="7fecc-244">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7fecc-244">Close the page.</span></span>

