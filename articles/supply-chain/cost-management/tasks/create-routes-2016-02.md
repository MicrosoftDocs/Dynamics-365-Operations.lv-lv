--- 
title: "Maršrutu izveide (tikai 2016. gada februāris)"
description: "Šī uzdevuma mērķis ir pabeigtas preces un daļēji pabeigtas preces ražošanas maršrutu izveide."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6949c729f474e5ea4aea8ad1cca6ae127cf4d652
ms.openlocfilehash: e3df21705c5b417a4541ba2e76528be63f1f531d
ms.contentlocale: lv-lv
ms.lasthandoff: 03/27/2018

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="66c18-103">Maršrutu izveide (tikai 2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="66c18-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66c18-104">Šī uzdevuma mērķis ir pabeigtas preces un daļēji pabeigtas preces ražošanas maršrutu izveide.</span><span class="sxs-lookup"><span data-stu-id="66c18-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="66c18-105">Tas ir MK aprēķina sērijas piektais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="66c18-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="66c18-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="66c18-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="66c18-107">Izveidot maršrutu daļēji pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="66c18-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="66c18-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="66c18-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="66c18-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="66c18-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="66c18-110">Atlasiet vienuma numuru BOM_2.</span><span class="sxs-lookup"><span data-stu-id="66c18-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="66c18-111">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="66c18-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="66c18-112">Noklikšķiniet uz Maršruts.</span><span class="sxs-lookup"><span data-stu-id="66c18-112">Click Route.</span></span>
5. <span data-ttu-id="66c18-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66c18-113">Click New.</span></span>
6. <span data-ttu-id="66c18-114">Noklikšķiniet uz Maršruts un maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="66c18-114">Click Route and route version.</span></span>
7. <span data-ttu-id="66c18-115">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="66c18-116">Šajā piemērā ierakstiet vērtību ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="66c18-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="66c18-117">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="66c18-118">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="66c18-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="66c18-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="66c18-119">Click OK.</span></span>
10. <span data-ttu-id="66c18-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66c18-120">Click New.</span></span>
11. <span data-ttu-id="66c18-121">Laukā Operācija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="66c18-122">Šajā piemērā atlasiet vienumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="66c18-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="66c18-123">Laukā Izpildes laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="66c18-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="66c18-124">Piemēram, ievadiet 1.</span><span class="sxs-lookup"><span data-stu-id="66c18-124">For example, type 1.</span></span> <span data-ttu-id="66c18-125">Izpildes laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="66c18-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="66c18-126">Laukā Maršruta grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="66c18-127">Šajā piemērā atlasiet vērtību Std.</span><span class="sxs-lookup"><span data-stu-id="66c18-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="66c18-128">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="66c18-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="66c18-129">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="66c18-130">Šajā piemērā atlasiet vienumu Montāža.</span><span class="sxs-lookup"><span data-stu-id="66c18-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="66c18-131">Noklikšķiniet uz cilnes Reizes.</span><span class="sxs-lookup"><span data-stu-id="66c18-131">Click the Times tab.</span></span>
17. <span data-ttu-id="66c18-132">Laukā Uzstādīšanas laiks ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="66c18-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="66c18-133">Šajā piemērā ierakstiet vērtību 1.</span><span class="sxs-lookup"><span data-stu-id="66c18-133">For this example, type 1.</span></span> <span data-ttu-id="66c18-134">Uzstādīšanas laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="66c18-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="66c18-135">Darbību rūtī noklikšķiniet uz Maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="66c18-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="66c18-136">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="66c18-136">Click Approve.</span></span>
20. <span data-ttu-id="66c18-137">Laukā Vai vēlaties arī apstiprināt šo maršrutu? atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="66c18-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="66c18-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="66c18-138">Click OK.</span></span>
22. <span data-ttu-id="66c18-139">Darbību rūtī noklikšķiniet uz Maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="66c18-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="66c18-140">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="66c18-140">Click Activate.</span></span>
24. <span data-ttu-id="66c18-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="66c18-141">Close the page.</span></span>
25. <span data-ttu-id="66c18-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="66c18-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="66c18-143">Izveidot maršrutu pabeigtai precei</span><span class="sxs-lookup"><span data-stu-id="66c18-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="66c18-144">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="66c18-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="66c18-145">Atlasiet vienuma numuru BOM_1.</span><span class="sxs-lookup"><span data-stu-id="66c18-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="66c18-146">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="66c18-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="66c18-147">Noklikšķiniet uz Maršruts.</span><span class="sxs-lookup"><span data-stu-id="66c18-147">Click Route.</span></span>
4. <span data-ttu-id="66c18-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66c18-148">Click New.</span></span>
5. <span data-ttu-id="66c18-149">Noklikšķiniet uz Maršruts un maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="66c18-149">Click Route and route version.</span></span>
6. <span data-ttu-id="66c18-150">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="66c18-151">Šajā piemērā ierakstiet vērtību ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="66c18-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="66c18-152">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="66c18-153">Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="66c18-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="66c18-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="66c18-154">Click OK.</span></span>
9. <span data-ttu-id="66c18-155">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66c18-155">Click New.</span></span>
10. <span data-ttu-id="66c18-156">Laukā Operācija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="66c18-157">Šajā piemērā atlasiet vienumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="66c18-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="66c18-158">Laukā Izpildes laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="66c18-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="66c18-159">Šajā piemērā ierakstiet vērtību 1.</span><span class="sxs-lookup"><span data-stu-id="66c18-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="66c18-160">Laukā Maršruta grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="66c18-161">Šajā piemērā atlasiet vērtību Std.</span><span class="sxs-lookup"><span data-stu-id="66c18-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="66c18-162">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="66c18-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="66c18-163">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66c18-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="66c18-164">Šajā piemērā atlasiet vienumu Iepakošana.</span><span class="sxs-lookup"><span data-stu-id="66c18-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="66c18-165">Noklikšķiniet uz cilnes Reizes.</span><span class="sxs-lookup"><span data-stu-id="66c18-165">Click the Times tab.</span></span>
16. <span data-ttu-id="66c18-166">Laukā Uzstādīšanas laiks ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="66c18-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="66c18-167">Šajā piemērā ierakstiet vērtību 1.</span><span class="sxs-lookup"><span data-stu-id="66c18-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="66c18-168">Darbību rūtī noklikšķiniet uz Maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="66c18-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="66c18-169">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="66c18-169">Click Approve.</span></span>
19. <span data-ttu-id="66c18-170">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="66c18-170">Click OK.</span></span>
20. <span data-ttu-id="66c18-171">Darbību rūtī noklikšķiniet uz Maršruta versija.</span><span class="sxs-lookup"><span data-stu-id="66c18-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="66c18-172">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="66c18-172">Click Activate.</span></span>
22. <span data-ttu-id="66c18-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="66c18-173">Close the page.</span></span>
23. <span data-ttu-id="66c18-174">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="66c18-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="66c18-175">Iespējot uzstādīšanas laika automātisku patēriņu</span><span class="sxs-lookup"><span data-stu-id="66c18-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="66c18-176">Doties uz Ražošanas kontrole > Iestatīšana > Maršruti > Maršrutu grupas.</span><span class="sxs-lookup"><span data-stu-id="66c18-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="66c18-177">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="66c18-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66c18-178">Sarakstā atlasiet vērtību Std.</span><span class="sxs-lookup"><span data-stu-id="66c18-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="66c18-179">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="66c18-179">Click Edit.</span></span>
4. <span data-ttu-id="66c18-180">Laukā Uzstādīšanas laiks atlasiet vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="66c18-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="66c18-181">Uzstādīšanas laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="66c18-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="66c18-182">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="66c18-182">Click Save.</span></span>
6. <span data-ttu-id="66c18-183">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="66c18-183">Close the page.</span></span>


