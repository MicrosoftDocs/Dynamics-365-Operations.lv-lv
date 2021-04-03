---
title: Atlīdzību režģu iestatīšana
description: Atlīdzības režģi tiek izmantoti, lai definētu un uzturētu algu struktūras fiksētās atlīdzības plāniem.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7e68ec4d172ced7ac66837e9580971d22b23b5f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465754"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="e3407-103">Atlīdzību režģu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e3407-103">Set up compensation grids</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e3407-104">Atlīdzības režģi tiek izmantoti, lai definētu un uzturētu algu struktūras fiksētās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="e3407-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="e3407-105">Atlīdzības režģus var koplietot vairākiem plāniem vai kopēt, veidojot jaunu atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="e3407-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="e3407-106">Pirms atlīdzības režģa izveidošanas ir jāiestata Līmeņi un Atsauces punkti.</span><span class="sxs-lookup"><span data-stu-id="e3407-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="e3407-107">Šajā piemērā tiks izveidots jauns atlīdzības režģa pakāpes tips, izmantojot demonstrācijas datus līmeņiem un atskaites punktiem.</span><span class="sxs-lookup"><span data-stu-id="e3407-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="e3407-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e3407-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="e3407-109">Informāciju par atlīdzības režģi iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e3407-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="e3407-110">Pārejiet uz sadaļu Personāla vadība > Atlīdzība > Fiksēta atlīdzība > Atlīdzības režģi.</span><span class="sxs-lookup"><span data-stu-id="e3407-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="e3407-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e3407-111">Click New.</span></span>
3. <span data-ttu-id="e3407-112">Laukā Režģis ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="e3407-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e3407-114">Atlasiet opciju laukā Tips.</span><span class="sxs-lookup"><span data-stu-id="e3407-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="e3407-115">Ievadiet vai atlasiet vērtību laukā Atsauces iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="e3407-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="e3407-116">Laukā Valūta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="e3407-117">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="e3407-118">Laukā Spēkā stāšanās datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="e3407-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="e3407-119">Līmeņu pievienošana kompensācijas struktūrai</span><span class="sxs-lookup"><span data-stu-id="e3407-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="e3407-120">Noklikšķiniet uz Kompensācijas struktūra.</span><span class="sxs-lookup"><span data-stu-id="e3407-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="e3407-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e3407-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e3407-122">Laukā Līmenis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="e3407-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e3407-123">Click New.</span></span>
5. <span data-ttu-id="e3407-124">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e3407-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="e3407-125">Laukā Līmenis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="e3407-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e3407-126">Click New.</span></span>
8. <span data-ttu-id="e3407-127">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e3407-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e3407-128">Laukā Līmenis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="e3407-129">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e3407-129">Click New.</span></span>
11. <span data-ttu-id="e3407-130">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e3407-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="e3407-131">Laukā Līmenis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="e3407-132">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e3407-132">Click New.</span></span>
14. <span data-ttu-id="e3407-133">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e3407-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="e3407-134">Laukā Līmenis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3407-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="e3407-135">Kompensācijas struktūras aizpildīšana ar vērtībām</span><span class="sxs-lookup"><span data-stu-id="e3407-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="e3407-136">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e3407-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e3407-137">Šajā posmā katrā tabulas laukā var manuāli ievadīt atlīdzības vērtības vai arī var izmantot funkciju Masveida izmaiņas, lai vienkārši aizpildītu vairākus laukus un veiktu pamata aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="e3407-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="e3407-138">Noklikšķiniet Masveida izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="e3407-138">Click Mass change.</span></span>
    * <span data-ttu-id="e3407-139">Šim režģim vispirms tiks lietota pirmā līmeņa viduspunkta vērtība visiem tabulas laukiem.</span><span class="sxs-lookup"><span data-stu-id="e3407-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="e3407-140">Tas būs pamats atlīdzības matricai.</span><span class="sxs-lookup"><span data-stu-id="e3407-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="e3407-141">Laukā Korekcijas veids atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="e3407-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="e3407-142">Laukā Korekcijas summa ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e3407-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="e3407-143">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="e3407-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="e3407-144">Noklikšķiniet uz Lietot režģim.</span><span class="sxs-lookup"><span data-stu-id="e3407-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="e3407-145">Tagad izmantosim masveida izmaiņu funkciju, lai palielinātu summas katrā nākamajā līmenī par noteiktu procentuālo vērtību vai summu.</span><span class="sxs-lookup"><span data-stu-id="e3407-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="e3407-146">Šajā piemērā katrai pakāpei būs 12,5 % izplatība starp to viduspunktiem.</span><span class="sxs-lookup"><span data-stu-id="e3407-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="e3407-147">Laukā Korekcijas veids atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="e3407-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="e3407-148">Laukā Korekcijas summa ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e3407-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="e3407-149">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e3407-150">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e3407-151">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e3407-152">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="e3407-153">Noklikšķiniet uz Lietot režģim.</span><span class="sxs-lookup"><span data-stu-id="e3407-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="e3407-154">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="e3407-155">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="e3407-156">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="e3407-157">Noklikšķiniet uz Lietot režģim.</span><span class="sxs-lookup"><span data-stu-id="e3407-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="e3407-158">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="e3407-159">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="e3407-160">Noklikšķiniet uz Lietot režģim.</span><span class="sxs-lookup"><span data-stu-id="e3407-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="e3407-161">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3407-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="e3407-162">Noklikšķiniet uz Lietot režģim.</span><span class="sxs-lookup"><span data-stu-id="e3407-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="e3407-163">Tagad izmantosim masveida izmaiņu funkciju, lai koriģētu minimālo un maksimālo atsauces punktu katram līmenim.</span><span class="sxs-lookup"><span data-stu-id="e3407-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="e3407-164">Šajā piemērā tiks izmantota 50 % izplatība, tādējādi minimālais atsauces punkts tiks koriģēts par –20 % un maksimālais atsauces punkts tiks koriģēts pa +20 %.</span><span class="sxs-lookup"><span data-stu-id="e3407-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="e3407-165">Laukā Korekcijas summa ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e3407-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="e3407-166">Ievadiet vai atlasiet vērtību laukā Atsauces punkts.</span><span class="sxs-lookup"><span data-stu-id="e3407-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="e3407-167">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="e3407-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="e3407-168">Noklikšķiniet uz Lietot režģim.</span><span class="sxs-lookup"><span data-stu-id="e3407-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="e3407-169">Laukā Korekcijas summa ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e3407-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="e3407-170">Ievadiet vai atlasiet vērtību laukā Atsauces punkts.</span><span class="sxs-lookup"><span data-stu-id="e3407-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="e3407-171">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="e3407-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="e3407-172">Noklikšķiniet uz Lietot režģim.</span><span class="sxs-lookup"><span data-stu-id="e3407-172">Click Apply to grid.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]