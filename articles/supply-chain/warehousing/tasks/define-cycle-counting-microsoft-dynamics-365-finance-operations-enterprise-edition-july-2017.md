--- 
title: "Cikla inventarizācijas definēšana "
description: "Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5a95f63efe3d78dc371cacdc09734490a601b1b8
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="define-cycle-counting"></a><span data-ttu-id="a9a55-103">Cikla inventarizācijas definēšana </span><span class="sxs-lookup"><span data-stu-id="a9a55-103">Define cycle counting</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9a55-104">Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības.</span><span class="sxs-lookup"><span data-stu-id="a9a55-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="a9a55-105">Šajā uzdevuma ierakstā parādīts, kā iestatīt noklusēto inventarizācijas darba prioritāti, iespējot mobilās ierīces izvēlnes elementu, lai apstrādātu gan izdošanas un inventarizācijas operācijas, iespējot inventarizācijas robežvērtības trigeri, kad novietojums kļūs tukšs un iespējot cikla inventarizācijas plānu noteiktam krājumam noteiktā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="a9a55-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="a9a55-106">Parasti šos uzdevumus veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="a9a55-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="a9a55-107">Šo procedūru varat izmēģināt, izmantojot USMF demonstrācijas datu uzņēmumu vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="a9a55-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="a9a55-108">Inventarizācijas darba prioritātes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a9a55-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="a9a55-109">Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="a9a55-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="a9a55-110">Noklikšķiniet uz cilnes Cikla inventarizācija.</span><span class="sxs-lookup"><span data-stu-id="a9a55-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="a9a55-111">Laukā Cikla inventarizācijas noklusējuma darba prioritāte ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a9a55-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="a9a55-112">Šis solis maina cikla inventarizācijas darba prioritāti salīdzinājumā ar citiem darba veidiem noliktavā.</span><span class="sxs-lookup"><span data-stu-id="a9a55-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="a9a55-113">Ievadot skaitli, kas ir mazāks par citu darba veidu skaitu, jūs palielināsiet cikla inventarizācijas darba prioritāti.</span><span class="sxs-lookup"><span data-stu-id="a9a55-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="a9a55-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a9a55-114">Click Save.</span></span>
5. <span data-ttu-id="a9a55-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="a9a55-116">Mobilās ierīces iespējošana</span><span class="sxs-lookup"><span data-stu-id="a9a55-116">Enable the mobile device</span></span>
1. <span data-ttu-id="a9a55-117">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi.</span><span class="sxs-lookup"><span data-stu-id="a9a55-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="a9a55-118">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a9a55-118">Click New.</span></span>
3. <span data-ttu-id="a9a55-119">Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="a9a55-120">Laukā Virsraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="a9a55-121">Laukā Režīms atlasiet "Darbs".</span><span class="sxs-lookup"><span data-stu-id="a9a55-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="a9a55-122">Iestatiet opciju Izmantot esošo darbu uz Jā.</span><span class="sxs-lookup"><span data-stu-id="a9a55-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="a9a55-123">Iestatot šo opciju uz Jā, sistēma meklēs pašreizējo darbu, ja tiek izmantots mobilās ierīces izvēlnes elements.</span><span class="sxs-lookup"><span data-stu-id="a9a55-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="a9a55-124">Laukā Novirzītājs atlasiet vienumu "Sistēmas noteikts".</span><span class="sxs-lookup"><span data-stu-id="a9a55-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="a9a55-125">Ja ir atlasīts "System directed", noliktavas darbinieks tiks novirzīts uz atvērto darbu, kas atrodas definētajās darba klasēs.</span><span class="sxs-lookup"><span data-stu-id="a9a55-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="a9a55-126">(Mēs izveidosim šīs darba klases vēlāk.)</span><span class="sxs-lookup"><span data-stu-id="a9a55-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="a9a55-127">Izvērsiet vai sakļaujiet sadaļu Darba klases.</span><span class="sxs-lookup"><span data-stu-id="a9a55-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="a9a55-128">Tagad mēs izveidosim divas darba klases, kas tiks lietotas ar šo mobilās ierīces izvēlnes vienumu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="a9a55-129">Ja tiek izmantots izvēlnes vienums, šīm darba klasēm būs nepieciešams vaicājums, un lietotājam tiks parādīts darbs ar augstāko prioritāti.</span><span class="sxs-lookup"><span data-stu-id="a9a55-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="a9a55-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a9a55-130">Click New.</span></span>
10. <span data-ttu-id="a9a55-131">Laukā Darba klases ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="a9a55-132">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a9a55-132">Click New.</span></span>
12. <span data-ttu-id="a9a55-133">Laukā Darba klases ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="a9a55-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a9a55-134">Click Save.</span></span>
14. <span data-ttu-id="a9a55-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-135">Close the page.</span></span>
15. <span data-ttu-id="a9a55-136">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne.</span><span class="sxs-lookup"><span data-stu-id="a9a55-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="a9a55-137">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="a9a55-138">Kokā atlasiet "the menu item that you just created".</span><span class="sxs-lookup"><span data-stu-id="a9a55-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="a9a55-139">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="a9a55-139">Click Edit.</span></span>
19. <span data-ttu-id="a9a55-140">Noklikšķiniet uz bultiņas, lai šo izvēlnes elementu pievienotu izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="a9a55-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="a9a55-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a9a55-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="a9a55-142">Inventarizācijas sliekšņa izveide</span><span class="sxs-lookup"><span data-stu-id="a9a55-142">Create a counting threshold</span></span>
1. <span data-ttu-id="a9a55-143">Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas robežvērtības.</span><span class="sxs-lookup"><span data-stu-id="a9a55-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="a9a55-144">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a9a55-144">Click New.</span></span>
3. <span data-ttu-id="a9a55-145">Ierakstiet vērtību laukā Cikla inventarizācijas sliekšņa ID.</span><span class="sxs-lookup"><span data-stu-id="a9a55-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="a9a55-146">Iestatiet opciju Nekavējoties apstrādāt cikla inventarizāciju uz Jā.</span><span class="sxs-lookup"><span data-stu-id="a9a55-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="a9a55-147">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a9a55-148">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a9a55-148">Click Save.</span></span>
7. <span data-ttu-id="a9a55-149">Noklikšķiniet uz Atlasīt novietojumus.</span><span class="sxs-lookup"><span data-stu-id="a9a55-149">Click Select locations.</span></span>
8. <span data-ttu-id="a9a55-150">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a9a55-151">Laukā Kritēriji atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="a9a55-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a9a55-152">Click OK.</span></span>
11. <span data-ttu-id="a9a55-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="a9a55-154">Cikla inventarizācijas plāna izveide</span><span class="sxs-lookup"><span data-stu-id="a9a55-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="a9a55-155">Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas plāni.</span><span class="sxs-lookup"><span data-stu-id="a9a55-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="a9a55-156">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a9a55-156">Click New.</span></span>
3. <span data-ttu-id="a9a55-157">Ierakstiet vērtību laukā Cikla inventarizācijas plāna ID.</span><span class="sxs-lookup"><span data-stu-id="a9a55-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="a9a55-158">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a9a55-159">Laukā Maksimālais cikla inventarizāciju skaits ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a9a55-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="a9a55-160">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a9a55-160">Click Save.</span></span>
7. <span data-ttu-id="a9a55-161">Noklikšķiniet uz Atlasīt novietojumus.</span><span class="sxs-lookup"><span data-stu-id="a9a55-161">Click Select locations.</span></span>
8. <span data-ttu-id="a9a55-162">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a9a55-163">Laukā Kritēriji atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="a9a55-164">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a9a55-164">Click OK.</span></span>
11. <span data-ttu-id="a9a55-165">Laukā Dienu skaits starp cikla inventarizācijām ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a9a55-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="a9a55-166">Piemēram, ja laukā Dienu skaits starp cikla inventarizācijām iestatītā vērtība ir 5, cikla inventarizācijas darbs tiks izveidots ik pēc piecām dienām.</span><span class="sxs-lookup"><span data-stu-id="a9a55-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="a9a55-167">Tomēr, ja cikla inventarizācijas darbs tiek apstrādāts trešajā dienā, nākamais cikla inventarizācijas darbs tiks izveidots piecas dienas pēc tam, kad tika apstrādāta pēdējā cikla inventarizācija, t.i., 8. dienā.</span><span class="sxs-lookup"><span data-stu-id="a9a55-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="a9a55-168">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a9a55-168">Click Save.</span></span>
13. <span data-ttu-id="a9a55-169">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a9a55-169">Click New.</span></span>
14. <span data-ttu-id="a9a55-170">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="a9a55-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="a9a55-171">Kārtošana tiek veikta no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="a9a55-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="a9a55-172">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="a9a55-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="a9a55-173">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="a9a55-174">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="a9a55-175">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a9a55-175">Click Save.</span></span>
18. <span data-ttu-id="a9a55-176">Noklikšķiniet uz Definēt preces vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-176">Click Define product query.</span></span>
19. <span data-ttu-id="a9a55-177">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="a9a55-178">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a9a55-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="a9a55-179">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a9a55-179">Click OK.</span></span>
22. <span data-ttu-id="a9a55-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a9a55-180">Close the page.</span></span>


