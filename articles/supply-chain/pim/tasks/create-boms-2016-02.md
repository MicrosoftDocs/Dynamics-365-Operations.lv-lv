---
title: Izveidot MK (2016. gada februāris)
description: Šajā uzdevumā uzmanība ir vērsta uz materiālu komplekta struktūras izveidošanu pabeigtai precei un daļēji pabeigtai precei.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568562"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="a7cc2-103">Izveidot MK (2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="a7cc2-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7cc2-104">Šajā uzdevumā uzmanība ir vērsta uz materiālu komplekta struktūras izveidošanu pabeigtai precei un daļēji pabeigtai precei.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="a7cc2-105">Tas ir MK aprēķina sērijas ceturtais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="a7cc2-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="a7cc2-107">Izveidot MK daļēji pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="a7cc2-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="a7cc2-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a7cc2-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a7cc2-110">Atlasiet vienuma numuru BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="a7cc2-111">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="a7cc2-112">Noklikšķiniet uz MK versijas.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-112">Click BOM versions.</span></span>
5. <span data-ttu-id="a7cc2-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-113">Click New.</span></span>
6. <span data-ttu-id="a7cc2-114">Noklikšķiniet uz MK un MK versija.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="a7cc2-115">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a7cc2-116">Ierakstiet, piemēram, BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="a7cc2-117">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a7cc2-118">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="a7cc2-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-119">Click OK.</span></span>
10. <span data-ttu-id="a7cc2-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-120">Click New.</span></span>
11. <span data-ttu-id="a7cc2-121">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a7cc2-122">Šajā piemērā ierakstiet vērtību ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="a7cc2-123">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a7cc2-124">Šajā piemērā ievadiet vai atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="a7cc2-125">Noklikšķiniet uz Virsraksts.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-125">Click Header.</span></span>
14. <span data-ttu-id="a7cc2-126">Noklikšķiniet uz Apstiprināt, lai apstiprinātu materiālu komplektus.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="a7cc2-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-127">Click OK.</span></span>
16. <span data-ttu-id="a7cc2-128">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-128">Click Approve.</span></span>
    * <span data-ttu-id="a7cc2-129">Poga Apstiprināt atrodas sadaļas MK versijas rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="a7cc2-130">Ja tā nav redzama, noklikšķiniet uz lapas Materiālu komplekti galvenes labajā augšējā pusē, lai parādītu vienumu Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="a7cc2-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-131">Click OK.</span></span>
18. <span data-ttu-id="a7cc2-132">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-132">Click Activate.</span></span>
19. <span data-ttu-id="a7cc2-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-133">Close the page.</span></span>
20. <span data-ttu-id="a7cc2-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-134">Close the page.</span></span>
21. <span data-ttu-id="a7cc2-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="a7cc2-136">Izveidot MK pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="a7cc2-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="a7cc2-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a7cc2-138">Atlasiet vienuma numuru BOM_1.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="a7cc2-139">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="a7cc2-140">Noklikšķiniet uz MK versijas.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-140">Click BOM versions.</span></span>
4. <span data-ttu-id="a7cc2-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-141">Click New.</span></span>
5. <span data-ttu-id="a7cc2-142">Noklikšķiniet uz MK un MK versija.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="a7cc2-143">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a7cc2-144">Ierakstiet, piemēram, BOM_1.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="a7cc2-145">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a7cc2-146">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="a7cc2-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-147">Click OK.</span></span>
9. <span data-ttu-id="a7cc2-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-148">Click New.</span></span>
10. <span data-ttu-id="a7cc2-149">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a7cc2-150">Šajā piemērā ierakstiet vērtību ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="a7cc2-151">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a7cc2-152">Šajā piemērā atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="a7cc2-153">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-153">Click New.</span></span>
13. <span data-ttu-id="a7cc2-154">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a7cc2-155">Šajā piemērā ierakstiet vērtību ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="a7cc2-156">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a7cc2-157">Šajā piemērā ievadiet vai atlasiet vērtību 11.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="a7cc2-158">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-158">Click New.</span></span>
16. <span data-ttu-id="a7cc2-159">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a7cc2-160">Šajā piemērā ierakstiet vērtību BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="a7cc2-161">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="a7cc2-162">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a7cc2-163">Šajā piemērā ievadiet vai atlasiet 11. noliktavu.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="a7cc2-164">Noklikšķiniet uz Virsraksts.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-164">Click Header.</span></span>
20. <span data-ttu-id="a7cc2-165">Noklikšķiniet uz Apstiprināt, lai apstiprinātu materiālu komplektus.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="a7cc2-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-166">Click OK.</span></span>
22. <span data-ttu-id="a7cc2-167">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-167">Click Approve.</span></span>
    * <span data-ttu-id="a7cc2-168">Poga Apstiprināt atrodas sadaļas MK versijas rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="a7cc2-169">Ja tā nav redzama, noklikšķiniet uz lapas Materiālu komplekti galvenes labajā augšējā pusē, lai parādītu vienumu Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="a7cc2-170">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-170">Click OK.</span></span>
24. <span data-ttu-id="a7cc2-171">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-171">Click Activate.</span></span>
25. <span data-ttu-id="a7cc2-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-172">Close the page.</span></span>
26. <span data-ttu-id="a7cc2-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-173">Close the page.</span></span>
27. <span data-ttu-id="a7cc2-174">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7cc2-174">Close the page.</span></span>

