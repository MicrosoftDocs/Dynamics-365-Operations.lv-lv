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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "351060"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="19e3f-103">Izveidot izejmateriālus (2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="19e3f-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19e3f-104">Šajā uzdevumā uzmanība ir vērsta uz pabeigtu un daļēji pabeigtu preču komponentu izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="19e3f-105">Tas ir MK aprēķina sērijas trešais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="19e3f-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="19e3f-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="19e3f-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="19e3f-107">Izveidot pirmo materiālu</span><span class="sxs-lookup"><span data-stu-id="19e3f-107">Create the first material</span></span>
1. <span data-ttu-id="19e3f-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="19e3f-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="19e3f-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="19e3f-109">Click New.</span></span>
3. <span data-ttu-id="19e3f-110">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="19e3f-111">Šajā piemērā ievadiet ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="19e3f-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="19e3f-112">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-113">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="19e3f-113">Select STD.</span></span> <span data-ttu-id="19e3f-114">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="19e3f-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="19e3f-115">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-116">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="19e3f-116">For example, select Audio.</span></span> <span data-ttu-id="19e3f-117">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="19e3f-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="19e3f-118">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-119">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="19e3f-119">Select SiteWH.</span></span> <span data-ttu-id="19e3f-120">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="19e3f-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="19e3f-121">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-122">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="19e3f-123">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="19e3f-123">Select None.</span></span>  
8. <span data-ttu-id="19e3f-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="19e3f-124">Click OK.</span></span>
9. <span data-ttu-id="19e3f-125">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="19e3f-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="19e3f-126">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="19e3f-126">Click Default order settings.</span></span>
11. <span data-ttu-id="19e3f-127">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-128">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="19e3f-129">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-130">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="19e3f-131">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-132">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="19e3f-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-133">Close the page.</span></span>
15. <span data-ttu-id="19e3f-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-134">Close the page.</span></span>
16. <span data-ttu-id="19e3f-135">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="19e3f-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="19e3f-136">Noklikšķiniet uz ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="19e3f-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="19e3f-137">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="19e3f-138">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="19e3f-139">Šajā piemērā ierakstiet vērtību M2.</span><span class="sxs-lookup"><span data-stu-id="19e3f-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="19e3f-140">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="19e3f-141">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="19e3f-141">Click Item price.</span></span>
21. <span data-ttu-id="19e3f-142">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="19e3f-142">Click New.</span></span>
22. <span data-ttu-id="19e3f-143">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-144">Šajā piemērā atlasiet vērtību 10, kas ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="19e3f-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="19e3f-145">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-146">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="19e3f-147">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="19e3f-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="19e3f-148">Šajā piemērā ierakstiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="19e3f-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="19e3f-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="19e3f-149">Click Save.</span></span>
26. <span data-ttu-id="19e3f-150">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="19e3f-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-151">Close the page.</span></span>
28. <span data-ttu-id="19e3f-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="19e3f-153">Izveidot otro materiālu</span><span class="sxs-lookup"><span data-stu-id="19e3f-153">Create the second material</span></span>
1. <span data-ttu-id="19e3f-154">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="19e3f-154">Click New.</span></span>
2. <span data-ttu-id="19e3f-155">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="19e3f-156">Šajā piemērā ierakstiet vērtību ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="19e3f-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="19e3f-157">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-158">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="19e3f-158">Select STD.</span></span> <span data-ttu-id="19e3f-159">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="19e3f-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="19e3f-160">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-161">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="19e3f-161">For example, select Audio.</span></span> <span data-ttu-id="19e3f-162">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="19e3f-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="19e3f-163">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-164">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="19e3f-164">Select SiteWH.</span></span> <span data-ttu-id="19e3f-165">Šajā piemērā tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="19e3f-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="19e3f-166">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-167">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="19e3f-168">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="19e3f-168">Select None.</span></span>  
7. <span data-ttu-id="19e3f-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="19e3f-169">Click OK.</span></span>
8. <span data-ttu-id="19e3f-170">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="19e3f-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="19e3f-171">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="19e3f-171">Click Default order settings.</span></span>
10. <span data-ttu-id="19e3f-172">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-173">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="19e3f-174">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-175">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="19e3f-176">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-177">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="19e3f-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-178">Close the page.</span></span>
14. <span data-ttu-id="19e3f-179">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-179">Close the page.</span></span>
15. <span data-ttu-id="19e3f-180">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="19e3f-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="19e3f-181">Noklikšķiniet uz ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="19e3f-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="19e3f-182">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="19e3f-183">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="19e3f-184">Šajā piemērā ierakstiet vērtību M2.</span><span class="sxs-lookup"><span data-stu-id="19e3f-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="19e3f-185">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="19e3f-186">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="19e3f-186">Click Item price.</span></span>
20. <span data-ttu-id="19e3f-187">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="19e3f-187">Click New.</span></span>
21. <span data-ttu-id="19e3f-188">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-189">Šajā piemērā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="19e3f-189">For this example, select 10.</span></span> <span data-ttu-id="19e3f-190">Šis ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="19e3f-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="19e3f-191">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-192">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="19e3f-193">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="19e3f-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="19e3f-194">Demonstrācijas nolūkos ierakstiet 10.</span><span class="sxs-lookup"><span data-stu-id="19e3f-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="19e3f-195">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="19e3f-195">Click Save.</span></span>
25. <span data-ttu-id="19e3f-196">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="19e3f-197">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-197">Close the page.</span></span>
27. <span data-ttu-id="19e3f-198">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="19e3f-199">Izveidot trešo materiālu</span><span class="sxs-lookup"><span data-stu-id="19e3f-199">Create the third material</span></span>
1. <span data-ttu-id="19e3f-200">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="19e3f-200">Click New.</span></span>
2. <span data-ttu-id="19e3f-201">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="19e3f-202">Demonstrācijas nolūkos ierakstiet ITEM_C</span><span class="sxs-lookup"><span data-stu-id="19e3f-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="19e3f-203">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-204">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="19e3f-204">Select STD.</span></span> <span data-ttu-id="19e3f-205">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="19e3f-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="19e3f-206">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-207">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="19e3f-207">For example, select Audio.</span></span> <span data-ttu-id="19e3f-208">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="19e3f-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="19e3f-209">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-210">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="19e3f-210">Select SiteWH.</span></span> <span data-ttu-id="19e3f-211">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="19e3f-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="19e3f-212">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-213">Šajā piemērā izsekošanas dimensijas netiks lietotas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="19e3f-214">Atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="19e3f-214">Select None.</span></span>  
7. <span data-ttu-id="19e3f-215">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="19e3f-215">Click OK.</span></span>
8. <span data-ttu-id="19e3f-216">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="19e3f-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="19e3f-217">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="19e3f-217">Click Default order settings.</span></span>
10. <span data-ttu-id="19e3f-218">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-219">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="19e3f-220">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-221">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="19e3f-222">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-223">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="19e3f-224">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-224">Close the page.</span></span>
14. <span data-ttu-id="19e3f-225">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-225">Close the page.</span></span>
15. <span data-ttu-id="19e3f-226">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="19e3f-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="19e3f-227">Noklikšķiniet uz ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="19e3f-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="19e3f-228">Izvērsiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="19e3f-229">Laukā Izmaksu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="19e3f-230">Šajā piemērā ierakstiet vērtību M1.</span><span class="sxs-lookup"><span data-stu-id="19e3f-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="19e3f-231">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="19e3f-232">Noklikšķiniet uz Krājuma cena.</span><span class="sxs-lookup"><span data-stu-id="19e3f-232">Click Item price.</span></span>
20. <span data-ttu-id="19e3f-233">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="19e3f-233">Click New.</span></span>
21. <span data-ttu-id="19e3f-234">Laukā Versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-235">Šajā piemērā atlasiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="19e3f-235">For this example, select 10.</span></span> <span data-ttu-id="19e3f-236">Šis ir Standarta izmaksu aprēķināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="19e3f-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="19e3f-237">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="19e3f-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="19e3f-238">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="19e3f-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="19e3f-239">Laukā Cena ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="19e3f-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="19e3f-240">Šajā piemērā ierakstiet vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="19e3f-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="19e3f-241">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="19e3f-241">Click Save.</span></span>
25. <span data-ttu-id="19e3f-242">Noklikšķiniet uz Aktivizēt gaidošās cenas.</span><span class="sxs-lookup"><span data-stu-id="19e3f-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="19e3f-243">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-243">Close the page.</span></span>
27. <span data-ttu-id="19e3f-244">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="19e3f-244">Close the page.</span></span>

