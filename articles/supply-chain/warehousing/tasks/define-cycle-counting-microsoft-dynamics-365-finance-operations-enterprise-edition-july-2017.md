---
title: 'Cikla inventarizācijas definēšana '
description: Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571691"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="3b90c-103">Cikla inventarizācijas definēšana </span><span class="sxs-lookup"><span data-stu-id="3b90c-103">Define cycle counting</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3b90c-104">Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības.</span><span class="sxs-lookup"><span data-stu-id="3b90c-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="3b90c-105">Šajā uzdevuma ierakstā parādīts, kā iestatīt noklusēto inventarizācijas darba prioritāti, iespējot mobilās ierīces izvēlnes elementu, lai apstrādātu gan izdošanas un inventarizācijas operācijas, iespējot inventarizācijas robežvērtības trigeri, kad novietojums kļūs tukšs un iespējot cikla inventarizācijas plānu noteiktam krājumam noteiktā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="3b90c-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="3b90c-106">Parasti šos uzdevumus veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="3b90c-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="3b90c-107">Šo procedūru varat izmēģināt, izmantojot USMF demonstrācijas datu uzņēmumu vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="3b90c-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="3b90c-108">Inventarizācijas darba prioritātes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3b90c-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="3b90c-109">Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="3b90c-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="3b90c-110">Noklikšķiniet uz cilnes Cikla inventarizācija.</span><span class="sxs-lookup"><span data-stu-id="3b90c-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="3b90c-111">Laukā Cikla inventarizācijas noklusējuma darba prioritāte ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="3b90c-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="3b90c-112">Šis solis maina cikla inventarizācijas darba prioritāti salīdzinājumā ar citiem darba veidiem noliktavā.</span><span class="sxs-lookup"><span data-stu-id="3b90c-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="3b90c-113">Ievadot skaitli, kas ir mazāks par citu darba veidu skaitu, jūs palielināsiet cikla inventarizācijas darba prioritāti.</span><span class="sxs-lookup"><span data-stu-id="3b90c-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="3b90c-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3b90c-114">Click Save.</span></span>
5. <span data-ttu-id="3b90c-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="3b90c-116">Mobilās ierīces iespējošana</span><span class="sxs-lookup"><span data-stu-id="3b90c-116">Enable the mobile device</span></span>
1. <span data-ttu-id="3b90c-117">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi.</span><span class="sxs-lookup"><span data-stu-id="3b90c-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="3b90c-118">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3b90c-118">Click New.</span></span>
3. <span data-ttu-id="3b90c-119">Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="3b90c-120">Laukā Virsraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="3b90c-121">Laukā Režīms atlasiet "Darbs".</span><span class="sxs-lookup"><span data-stu-id="3b90c-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="3b90c-122">Iestatiet opciju Izmantot esošo darbu uz Jā.</span><span class="sxs-lookup"><span data-stu-id="3b90c-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="3b90c-123">Iestatot šo opciju uz Jā, sistēma meklēs pašreizējo darbu, ja tiek izmantots mobilās ierīces izvēlnes elements.</span><span class="sxs-lookup"><span data-stu-id="3b90c-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="3b90c-124">Laukā Novirzītājs atlasiet vienumu "Sistēmas noteikts".</span><span class="sxs-lookup"><span data-stu-id="3b90c-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="3b90c-125">Ja ir atlasīts "System directed", noliktavas darbinieks tiks novirzīts uz atvērto darbu, kas atrodas definētajās darba klasēs.</span><span class="sxs-lookup"><span data-stu-id="3b90c-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="3b90c-126">(Mēs izveidosim šīs darba klases vēlāk.)</span><span class="sxs-lookup"><span data-stu-id="3b90c-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="3b90c-127">Izvērsiet vai sakļaujiet sadaļu Darba klases.</span><span class="sxs-lookup"><span data-stu-id="3b90c-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="3b90c-128">Tagad mēs izveidosim divas darba klases, kas tiks lietotas ar šo mobilās ierīces izvēlnes vienumu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="3b90c-129">Ja tiek izmantots izvēlnes vienums, šīm darba klasēm būs nepieciešams vaicājums, un lietotājam tiks parādīts darbs ar augstāko prioritāti.</span><span class="sxs-lookup"><span data-stu-id="3b90c-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="3b90c-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3b90c-130">Click New.</span></span>
10. <span data-ttu-id="3b90c-131">Laukā Darba klases ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="3b90c-132">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3b90c-132">Click New.</span></span>
12. <span data-ttu-id="3b90c-133">Laukā Darba klases ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="3b90c-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3b90c-134">Click Save.</span></span>
14. <span data-ttu-id="3b90c-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-135">Close the page.</span></span>
15. <span data-ttu-id="3b90c-136">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne.</span><span class="sxs-lookup"><span data-stu-id="3b90c-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="3b90c-137">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="3b90c-138">Kokā atlasiet "the menu item that you just created".</span><span class="sxs-lookup"><span data-stu-id="3b90c-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="3b90c-139">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="3b90c-139">Click Edit.</span></span>
19. <span data-ttu-id="3b90c-140">Noklikšķiniet uz bultiņas, lai šo izvēlnes elementu pievienotu izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="3b90c-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="3b90c-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3b90c-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="3b90c-142">Inventarizācijas sliekšņa izveide</span><span class="sxs-lookup"><span data-stu-id="3b90c-142">Create a counting threshold</span></span>
1. <span data-ttu-id="3b90c-143">Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas robežvērtības.</span><span class="sxs-lookup"><span data-stu-id="3b90c-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="3b90c-144">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3b90c-144">Click New.</span></span>
3. <span data-ttu-id="3b90c-145">Ierakstiet vērtību laukā Cikla inventarizācijas sliekšņa ID.</span><span class="sxs-lookup"><span data-stu-id="3b90c-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="3b90c-146">Iestatiet opciju Nekavējoties apstrādāt cikla inventarizāciju uz Jā.</span><span class="sxs-lookup"><span data-stu-id="3b90c-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="3b90c-147">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="3b90c-148">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3b90c-148">Click Save.</span></span>
7. <span data-ttu-id="3b90c-149">Noklikšķiniet uz Atlasīt novietojumus.</span><span class="sxs-lookup"><span data-stu-id="3b90c-149">Click Select locations.</span></span>
8. <span data-ttu-id="3b90c-150">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3b90c-151">Laukā Kritēriji atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="3b90c-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3b90c-152">Click OK.</span></span>
11. <span data-ttu-id="3b90c-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="3b90c-154">Cikla inventarizācijas plāna izveide</span><span class="sxs-lookup"><span data-stu-id="3b90c-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="3b90c-155">Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas plāni.</span><span class="sxs-lookup"><span data-stu-id="3b90c-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="3b90c-156">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3b90c-156">Click New.</span></span>
3. <span data-ttu-id="3b90c-157">Ierakstiet vērtību laukā Cikla inventarizācijas plāna ID.</span><span class="sxs-lookup"><span data-stu-id="3b90c-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="3b90c-158">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3b90c-159">Laukā Maksimālais cikla inventarizāciju skaits ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="3b90c-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="3b90c-160">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3b90c-160">Click Save.</span></span>
7. <span data-ttu-id="3b90c-161">Noklikšķiniet uz Atlasīt novietojumus.</span><span class="sxs-lookup"><span data-stu-id="3b90c-161">Click Select locations.</span></span>
8. <span data-ttu-id="3b90c-162">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3b90c-163">Laukā Kritēriji atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="3b90c-164">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3b90c-164">Click OK.</span></span>
11. <span data-ttu-id="3b90c-165">Laukā Dienu skaits starp cikla inventarizācijām ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="3b90c-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="3b90c-166">Piemēram, ja laukā Dienu skaits starp cikla inventarizācijām iestatītā vērtība ir 5, cikla inventarizācijas darbs tiks izveidots ik pēc piecām dienām.</span><span class="sxs-lookup"><span data-stu-id="3b90c-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="3b90c-167">Tomēr, ja cikla inventarizācijas darbs tiek apstrādāts trešajā dienā, nākamais cikla inventarizācijas darbs tiks izveidots piecas dienas pēc tam, kad tika apstrādāta pēdējā cikla inventarizācija, t.i., 8. dienā.</span><span class="sxs-lookup"><span data-stu-id="3b90c-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="3b90c-168">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3b90c-168">Click Save.</span></span>
13. <span data-ttu-id="3b90c-169">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3b90c-169">Click New.</span></span>
14. <span data-ttu-id="3b90c-170">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="3b90c-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="3b90c-171">Kārtošana tiek veikta no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="3b90c-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="3b90c-172">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="3b90c-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="3b90c-173">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="3b90c-174">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="3b90c-175">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3b90c-175">Click Save.</span></span>
18. <span data-ttu-id="3b90c-176">Noklikšķiniet uz Definēt preces vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-176">Click Define product query.</span></span>
19. <span data-ttu-id="3b90c-177">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="3b90c-178">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3b90c-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="3b90c-179">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3b90c-179">Click OK.</span></span>
22. <span data-ttu-id="3b90c-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3b90c-180">Close the page.</span></span>

