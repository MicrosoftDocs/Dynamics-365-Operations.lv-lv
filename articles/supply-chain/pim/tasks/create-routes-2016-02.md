--- 
title: "Izveidot maršrutus (2016. gada februāris)"
description: "Šī uzdevuma mērķis ir pabeigtas preces un daļēji pabeigtas preces ražošanas maršrutu izveide."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.contentlocale: lv-lv
ms.lasthandoff: 09/17/2018

---
# <a name="create-routes-february-2016"></a><span data-ttu-id="807fa-103">Izveidot maršrutus (2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="807fa-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="807fa-104">Šī uzdevuma mērķis ir pabeigtas preces un daļēji pabeigtas preces ražošanas maršrutu izveide.</span><span class="sxs-lookup"><span data-stu-id="807fa-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="807fa-105">Tas ir MK aprēķina sērijas piektais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="807fa-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="807fa-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="807fa-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="807fa-107">Izveidot maršrutu daļēji pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="807fa-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="807fa-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="807fa-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="807fa-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="807fa-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="807fa-110">Atlasiet vienuma numuru BOM_2.</span><span class="sxs-lookup"><span data-stu-id="807fa-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="807fa-111">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="807fa-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="807fa-112">Noklikšķiniet uz Maršruts.</span><span class="sxs-lookup"><span data-stu-id="807fa-112">Click Route.</span></span>
5. <span data-ttu-id="807fa-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="807fa-113">Click New.</span></span>
6. <span data-ttu-id="807fa-114">Noklikšķiniet uz Maršruts un maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="807fa-114">Click Route and route version.</span></span>
7. <span data-ttu-id="807fa-115">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="807fa-116">Šajā piemērā ierakstiet vērtību ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="807fa-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="807fa-117">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="807fa-118">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="807fa-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="807fa-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="807fa-119">Click OK.</span></span>
10. <span data-ttu-id="807fa-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="807fa-120">Click New.</span></span>
11. <span data-ttu-id="807fa-121">Laukā Operācija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="807fa-122">Šajā piemērā atlasiet vienumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="807fa-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="807fa-123">Laukā Izpildes laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="807fa-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="807fa-124">Piemēram, ievadiet 1.</span><span class="sxs-lookup"><span data-stu-id="807fa-124">For example, type 1.</span></span> <span data-ttu-id="807fa-125">Izpildes laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="807fa-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="807fa-126">Laukā Maršruta grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="807fa-127">Šajā piemērā atlasiet vērtību Std.</span><span class="sxs-lookup"><span data-stu-id="807fa-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="807fa-128">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="807fa-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="807fa-129">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="807fa-130">Šajā piemērā atlasiet vienumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="807fa-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="807fa-131">Noklikšķiniet uz cilnes Reizes.</span><span class="sxs-lookup"><span data-stu-id="807fa-131">Click the Times tab.</span></span>
17. <span data-ttu-id="807fa-132">Laukā Uzstādīšanas laiks ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="807fa-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="807fa-133">Šajā piemērā ierakstiet vērtību 1.</span><span class="sxs-lookup"><span data-stu-id="807fa-133">For this example, type 1.</span></span> <span data-ttu-id="807fa-134">Uzstādīšanas laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="807fa-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="807fa-135">Darbību rūtī noklikšķiniet uz Maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="807fa-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="807fa-136">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="807fa-136">Click Approve.</span></span>
20. <span data-ttu-id="807fa-137">Laukā Vai vēlaties arī apstiprināt šo maršrutu? atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="807fa-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="807fa-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="807fa-138">Click OK.</span></span>
22. <span data-ttu-id="807fa-139">Darbību rūtī noklikšķiniet uz Maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="807fa-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="807fa-140">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="807fa-140">Click Activate.</span></span>
24. <span data-ttu-id="807fa-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="807fa-141">Close the page.</span></span>
25. <span data-ttu-id="807fa-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="807fa-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="807fa-143">Izveidot maršrutu pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="807fa-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="807fa-144">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="807fa-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="807fa-145">Atlasiet vienuma numuru BOM_1.</span><span class="sxs-lookup"><span data-stu-id="807fa-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="807fa-146">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="807fa-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="807fa-147">Noklikšķiniet uz Maršruts.</span><span class="sxs-lookup"><span data-stu-id="807fa-147">Click Route.</span></span>
4. <span data-ttu-id="807fa-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="807fa-148">Click New.</span></span>
5. <span data-ttu-id="807fa-149">Noklikšķiniet uz Maršruts un maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="807fa-149">Click Route and route version.</span></span>
6. <span data-ttu-id="807fa-150">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="807fa-151">Šajā piemērā ierakstiet vērtību ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="807fa-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="807fa-152">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="807fa-153">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="807fa-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="807fa-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="807fa-154">Click OK.</span></span>
9. <span data-ttu-id="807fa-155">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="807fa-155">Click New.</span></span>
10. <span data-ttu-id="807fa-156">Laukā Operācija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="807fa-157">Šajā piemērā atlasiet vienumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="807fa-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="807fa-158">Laukā Izpildes laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="807fa-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="807fa-159">Šajā piemērā ierakstiet vērtību 1.</span><span class="sxs-lookup"><span data-stu-id="807fa-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="807fa-160">Laukā Maršruta grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="807fa-161">Šajā piemērā atlasiet vērtību Std.</span><span class="sxs-lookup"><span data-stu-id="807fa-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="807fa-162">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="807fa-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="807fa-163">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="807fa-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="807fa-164">Šajā piemērā atlasiet vienumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="807fa-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="807fa-165">Noklikšķiniet uz cilnes Reizes.</span><span class="sxs-lookup"><span data-stu-id="807fa-165">Click the Times tab.</span></span>
16. <span data-ttu-id="807fa-166">Laukā Uzstādīšanas laiks ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="807fa-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="807fa-167">Šajā piemērā ierakstiet vērtību 1.</span><span class="sxs-lookup"><span data-stu-id="807fa-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="807fa-168">Darbību rūtī noklikšķiniet uz Maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="807fa-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="807fa-169">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="807fa-169">Click Approve.</span></span>
19. <span data-ttu-id="807fa-170">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="807fa-170">Click OK.</span></span>
20. <span data-ttu-id="807fa-171">Darbību rūtī noklikšķiniet uz Maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="807fa-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="807fa-172">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="807fa-172">Click Activate.</span></span>
22. <span data-ttu-id="807fa-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="807fa-173">Close the page.</span></span>
23. <span data-ttu-id="807fa-174">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="807fa-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="807fa-175">Iespējot uzstādīšanas laika automātisku patēriņu</span><span class="sxs-lookup"><span data-stu-id="807fa-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="807fa-176">Doties uz Ražošanas kontrole > Iestatīšana > Maršruti > Maršrutu grupas.</span><span class="sxs-lookup"><span data-stu-id="807fa-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="807fa-177">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="807fa-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="807fa-178">Sarakstā atlasiet vērtību Std.</span><span class="sxs-lookup"><span data-stu-id="807fa-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="807fa-179">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="807fa-179">Click Edit.</span></span>
4. <span data-ttu-id="807fa-180">Laukā Uzstādīšanas laiks atlasiet vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="807fa-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="807fa-181">Uzstādīšanas laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="807fa-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="807fa-182">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="807fa-182">Click Save.</span></span>
6. <span data-ttu-id="807fa-183">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="807fa-183">Close the page.</span></span>

