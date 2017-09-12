--- 
title: "MK izveide (tikai 2016. gada februāris)"
description: "Šajā uzdevumā uzmanība ir vērsta uz materiālu komplekta struktūras izveidošanu pabeigtai precei un daļēji pabeigtai precei."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8ad4b0e230fb0f018355e486e3b898895a61f28
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="7d7a1-103">MK izveide (tikai 2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="7d7a1-103">Create BOMs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d7a1-104">Šajā uzdevumā uzmanība ir vērsta uz materiālu komplekta struktūras izveidošanu pabeigtai precei un daļēji pabeigtai precei.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="7d7a1-105">Tas ir MK aprēķina sērijas ceturtais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="7d7a1-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="7d7a1-107">Izveidot MK daļēji pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="7d7a1-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="7d7a1-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7d7a1-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7d7a1-110">Atlasiet vienuma numuru BOM_2.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="7d7a1-111">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="7d7a1-112">Noklikšķiniet uz MK versijas.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-112">Click BOM versions.</span></span>
5. <span data-ttu-id="7d7a1-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-113">Click New.</span></span>
6. <span data-ttu-id="7d7a1-114">Noklikšķiniet uz MK un MK versija.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="7d7a1-115">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7d7a1-116">Ierakstiet, piemēram, BOM_2.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="7d7a1-117">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7d7a1-118">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="7d7a1-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-119">Click OK.</span></span>
10. <span data-ttu-id="7d7a1-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-120">Click New.</span></span>
11. <span data-ttu-id="7d7a1-121">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7d7a1-122">Šajā piemērā ierakstiet vērtību ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="7d7a1-123">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7d7a1-124">Šajā piemērā ievadiet vai atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="7d7a1-125">Noklikšķiniet uz Virsraksts.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-125">Click Header.</span></span>
14. <span data-ttu-id="7d7a1-126">Noklikšķiniet uz Apstiprināt, lai apstiprinātu materiālu komplektus.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="7d7a1-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-127">Click OK.</span></span>
16. <span data-ttu-id="7d7a1-128">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-128">Click Approve.</span></span>
    * <span data-ttu-id="7d7a1-129">Poga Apstiprināt atrodas sadaļas MK versijas rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="7d7a1-130">Ja tā nav redzama, noklikšķiniet uz lapas Materiālu komplekti galvenes labajā augšējā pusē, lai parādītu vienumu Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="7d7a1-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-131">Click OK.</span></span>
18. <span data-ttu-id="7d7a1-132">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-132">Click Activate.</span></span>
19. <span data-ttu-id="7d7a1-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-133">Close the page.</span></span>
20. <span data-ttu-id="7d7a1-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-134">Close the page.</span></span>
21. <span data-ttu-id="7d7a1-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="7d7a1-136">Izveidot MK pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="7d7a1-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="7d7a1-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7d7a1-138">Atlasiet vienuma numuru BOM_1.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="7d7a1-139">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="7d7a1-140">Noklikšķiniet uz MK versijas.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-140">Click BOM versions.</span></span>
4. <span data-ttu-id="7d7a1-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-141">Click New.</span></span>
5. <span data-ttu-id="7d7a1-142">Noklikšķiniet uz MK un MK versija.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="7d7a1-143">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7d7a1-144">Ierakstiet, piemēram, BOM_1.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="7d7a1-145">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7d7a1-146">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="7d7a1-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-147">Click OK.</span></span>
9. <span data-ttu-id="7d7a1-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-148">Click New.</span></span>
10. <span data-ttu-id="7d7a1-149">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7d7a1-150">Šajā piemērā ierakstiet vērtību ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="7d7a1-151">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7d7a1-152">Šajā piemērā atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="7d7a1-153">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-153">Click New.</span></span>
13. <span data-ttu-id="7d7a1-154">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7d7a1-155">Šajā piemērā ierakstiet vērtību ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="7d7a1-156">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7d7a1-157">Šajā piemērā ievadiet vai atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="7d7a1-158">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-158">Click New.</span></span>
16. <span data-ttu-id="7d7a1-159">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7d7a1-160">Šajā piemērā ierakstiet vērtību BOM_2.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="7d7a1-161">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="7d7a1-162">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7d7a1-163">Šajā piemērā ievadiet vai atlasiet 11. noliktavu.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="7d7a1-164">Noklikšķiniet uz Virsraksts.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-164">Click Header.</span></span>
20. <span data-ttu-id="7d7a1-165">Noklikšķiniet uz Apstiprināt, lai apstiprinātu materiālu komplektus.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="7d7a1-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-166">Click OK.</span></span>
22. <span data-ttu-id="7d7a1-167">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-167">Click Approve.</span></span>
    * <span data-ttu-id="7d7a1-168">Poga Apstiprināt atrodas sadaļas MK versijas rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="7d7a1-169">Ja tā nav redzama, noklikšķiniet uz lapas Materiālu komplekti galvenes labajā augšējā pusē, lai parādītu vienumu Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="7d7a1-170">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-170">Click OK.</span></span>
24. <span data-ttu-id="7d7a1-171">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-171">Click Activate.</span></span>
25. <span data-ttu-id="7d7a1-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-172">Close the page.</span></span>
26. <span data-ttu-id="7d7a1-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-173">Close the page.</span></span>
27. <span data-ttu-id="7d7a1-174">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-174">Close the page.</span></span>


