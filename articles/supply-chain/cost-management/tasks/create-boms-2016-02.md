---
title: MK izveide (tikai 2016. gada februāris)
description: Šajā uzdevumā uzmanība ir vērsta uz materiālu komplekta struktūras izveidošanu pabeigtai precei un daļēji pabeigtai precei.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f132a3865b180a74d328ebc76ca29b2fc8aee85f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563254"
---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="a09fa-103">MK izveide (tikai 2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="a09fa-103">Create BOMs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a09fa-104">Šajā uzdevumā uzmanība ir vērsta uz materiālu komplekta struktūras izveidošanu pabeigtai precei un daļēji pabeigtai precei.</span><span class="sxs-lookup"><span data-stu-id="a09fa-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="a09fa-105">Tas ir MK aprēķina sērijas ceturtais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="a09fa-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="a09fa-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="a09fa-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="a09fa-107">Izveidot MK daļēji pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="a09fa-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="a09fa-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="a09fa-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a09fa-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a09fa-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a09fa-110">Atlasiet vienuma numuru BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a09fa-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="a09fa-111">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="a09fa-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="a09fa-112">Noklikšķiniet uz MK versijas.</span><span class="sxs-lookup"><span data-stu-id="a09fa-112">Click BOM versions.</span></span>
5. <span data-ttu-id="a09fa-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a09fa-113">Click New.</span></span>
6. <span data-ttu-id="a09fa-114">Noklikšķiniet uz MK un MK versija.</span><span class="sxs-lookup"><span data-stu-id="a09fa-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="a09fa-115">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a09fa-116">Ierakstiet, piemēram, BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a09fa-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="a09fa-117">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a09fa-118">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="a09fa-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="a09fa-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a09fa-119">Click OK.</span></span>
10. <span data-ttu-id="a09fa-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a09fa-120">Click New.</span></span>
11. <span data-ttu-id="a09fa-121">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a09fa-122">Šajā piemērā ierakstiet vērtību ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="a09fa-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="a09fa-123">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a09fa-124">Šajā piemērā ievadiet vai atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="a09fa-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="a09fa-125">Noklikšķiniet uz Virsraksts.</span><span class="sxs-lookup"><span data-stu-id="a09fa-125">Click Header.</span></span>
14. <span data-ttu-id="a09fa-126">Noklikšķiniet uz Apstiprināt, lai apstiprinātu materiālu komplektus.</span><span class="sxs-lookup"><span data-stu-id="a09fa-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="a09fa-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a09fa-127">Click OK.</span></span>
16. <span data-ttu-id="a09fa-128">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a09fa-128">Click Approve.</span></span>
    * <span data-ttu-id="a09fa-129">Poga Apstiprināt atrodas sadaļas MK versijas rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="a09fa-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="a09fa-130">Ja tā nav redzama, noklikšķiniet uz lapas Materiālu komplekti galvenes labajā augšējā pusē, lai parādītu vienumu Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a09fa-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="a09fa-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a09fa-131">Click OK.</span></span>
18. <span data-ttu-id="a09fa-132">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="a09fa-132">Click Activate.</span></span>
19. <span data-ttu-id="a09fa-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a09fa-133">Close the page.</span></span>
20. <span data-ttu-id="a09fa-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a09fa-134">Close the page.</span></span>
21. <span data-ttu-id="a09fa-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a09fa-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="a09fa-136">Izveidot MK pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="a09fa-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="a09fa-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a09fa-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a09fa-138">Atlasiet vienuma numuru BOM_1.</span><span class="sxs-lookup"><span data-stu-id="a09fa-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="a09fa-139">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="a09fa-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="a09fa-140">Noklikšķiniet uz MK versijas.</span><span class="sxs-lookup"><span data-stu-id="a09fa-140">Click BOM versions.</span></span>
4. <span data-ttu-id="a09fa-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a09fa-141">Click New.</span></span>
5. <span data-ttu-id="a09fa-142">Noklikšķiniet uz MK un MK versija.</span><span class="sxs-lookup"><span data-stu-id="a09fa-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="a09fa-143">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a09fa-144">Ierakstiet, piemēram, BOM_1.</span><span class="sxs-lookup"><span data-stu-id="a09fa-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="a09fa-145">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a09fa-146">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="a09fa-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="a09fa-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a09fa-147">Click OK.</span></span>
9. <span data-ttu-id="a09fa-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a09fa-148">Click New.</span></span>
10. <span data-ttu-id="a09fa-149">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a09fa-150">Šajā piemērā ierakstiet vērtību ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="a09fa-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="a09fa-151">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a09fa-152">Šajā piemērā atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="a09fa-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="a09fa-153">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a09fa-153">Click New.</span></span>
13. <span data-ttu-id="a09fa-154">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a09fa-155">Šajā piemērā ierakstiet vērtību ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="a09fa-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="a09fa-156">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a09fa-157">Šajā piemērā ievadiet vai atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="a09fa-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="a09fa-158">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a09fa-158">Click New.</span></span>
16. <span data-ttu-id="a09fa-159">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a09fa-160">Šajā piemērā ierakstiet vērtību BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a09fa-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="a09fa-161">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a09fa-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="a09fa-162">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a09fa-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a09fa-163">Šajā piemērā ievadiet vai atlasiet 11. noliktavu.</span><span class="sxs-lookup"><span data-stu-id="a09fa-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="a09fa-164">Noklikšķiniet uz Virsraksts.</span><span class="sxs-lookup"><span data-stu-id="a09fa-164">Click Header.</span></span>
20. <span data-ttu-id="a09fa-165">Noklikšķiniet uz Apstiprināt, lai apstiprinātu materiālu komplektus.</span><span class="sxs-lookup"><span data-stu-id="a09fa-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="a09fa-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a09fa-166">Click OK.</span></span>
22. <span data-ttu-id="a09fa-167">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a09fa-167">Click Approve.</span></span>
    * <span data-ttu-id="a09fa-168">Poga Apstiprināt atrodas sadaļas MK versijas rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="a09fa-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="a09fa-169">Ja tā nav redzama, noklikšķiniet uz lapas Materiālu komplekti galvenes labajā augšējā pusē, lai parādītu vienumu Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a09fa-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="a09fa-170">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a09fa-170">Click OK.</span></span>
24. <span data-ttu-id="a09fa-171">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="a09fa-171">Click Activate.</span></span>
25. <span data-ttu-id="a09fa-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a09fa-172">Close the page.</span></span>
26. <span data-ttu-id="a09fa-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a09fa-173">Close the page.</span></span>
27. <span data-ttu-id="a09fa-174">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a09fa-174">Close the page.</span></span>

