---
title: Cikla inventarizācijas definēšana
description: Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0b94bcc1c33889f336541f3dd8ba4782fac0261
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238994"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="5b350-103">Cikla inventarizācijas definēšana</span><span class="sxs-lookup"><span data-stu-id="5b350-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b350-104">Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības.</span><span class="sxs-lookup"><span data-stu-id="5b350-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="5b350-105">Šajā uzdevuma ierakstā parādīts, kā iestatīt noklusēto inventarizācijas darba prioritāti, iespējot mobilās ierīces izvēlnes elementu, lai apstrādātu gan izdošanas un inventarizācijas operācijas, iespējot inventarizācijas robežvērtības trigeri, kad novietojums kļūs tukšs un iespējot cikla inventarizācijas plānu noteiktam krājumam noteiktā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="5b350-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="5b350-106">Parasti šos uzdevumus veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="5b350-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="5b350-107">Šo procedūru varat izmēģināt, izmantojot USMF demonstrācijas datu uzņēmumu vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="5b350-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="5b350-108">Inventarizācijas darba prioritātes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5b350-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="5b350-109">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana> Noliktavas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="5b350-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="5b350-110">Noklikšķiniet uz cilnes **Cikla inventarizācija**.</span><span class="sxs-lookup"><span data-stu-id="5b350-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="5b350-111">Ievadiet skaitli laukā **Noklusējuma cikla inventarizācijas darba prioritāte**.</span><span class="sxs-lookup"><span data-stu-id="5b350-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="5b350-112">Šis solis maina cikla inventarizācijas darba prioritāti salīdzinājumā ar citiem darba veidiem noliktavā.</span><span class="sxs-lookup"><span data-stu-id="5b350-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="5b350-113">Ievadot skaitli, kas ir mazāks par citu darba veidu skaitu, jūs palielināsiet cikla inventarizācijas darba prioritāti.</span><span class="sxs-lookup"><span data-stu-id="5b350-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="5b350-114">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b350-114">Click **Save**.</span></span>
5. <span data-ttu-id="5b350-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5b350-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="5b350-116">Mobilās ierīces iespējošana</span><span class="sxs-lookup"><span data-stu-id="5b350-116">Enable the mobile device</span></span>
1. <span data-ttu-id="5b350-117">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes elementi**.</span><span class="sxs-lookup"><span data-stu-id="5b350-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="5b350-118">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b350-118">Click **New**.</span></span>
3. <span data-ttu-id="5b350-119">Laukā **Izvēlnes vienuma nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5b350-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="5b350-120">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5b350-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="5b350-121">Laukā **Režīms** atlasiet “Darba”.</span><span class="sxs-lookup"><span data-stu-id="5b350-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="5b350-122">Iestatiet opciju **Izmantot esošo darbu** uz Jā.</span><span class="sxs-lookup"><span data-stu-id="5b350-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="5b350-123">Iestatot šo opciju uz Jā, sistēma meklēs pašreizējo darbu, ja tiek izmantots mobilās ierīces izvēlnes elements.</span><span class="sxs-lookup"><span data-stu-id="5b350-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="5b350-124">Laukā **Noteica:** atlasiet “Sistēmas noteikts”.</span><span class="sxs-lookup"><span data-stu-id="5b350-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="5b350-125">Ja ir atlasīts "System directed", noliktavas darbinieks tiks novirzīts uz atvērto darbu, kas atrodas definētajās darba klasēs.</span><span class="sxs-lookup"><span data-stu-id="5b350-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="5b350-126">(Mēs izveidosim šīs darba klases vēlāk.)</span><span class="sxs-lookup"><span data-stu-id="5b350-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="5b350-127">Izvērtiet fastTab **Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="5b350-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="5b350-128">Tagad mēs izveidosim divas darba klases, kas tiks lietotas ar šo mobilās ierīces izvēlnes vienumu.</span><span class="sxs-lookup"><span data-stu-id="5b350-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="5b350-129">Ja tiek izmantots izvēlnes vienums, šīm darba klasēm būs nepieciešams vaicājums, un lietotājam tiks parādīts darbs ar augstāko prioritāti.</span><span class="sxs-lookup"><span data-stu-id="5b350-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="5b350-130">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b350-130">Click **New**.</span></span>
10. <span data-ttu-id="5b350-131">Laukā **Darba klases ID** atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5b350-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="5b350-132">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b350-132">Click **New**.</span></span>
12. <span data-ttu-id="5b350-133">Laukā **Darba klases ID** atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5b350-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="5b350-134">**Darbību rūtī** noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b350-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="5b350-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5b350-135">Close the page.</span></span>
15. <span data-ttu-id="5b350-136">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas pārvaldība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="5b350-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="5b350-137">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5b350-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="5b350-138">Kokā atlasiet "the menu item that you just created".</span><span class="sxs-lookup"><span data-stu-id="5b350-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="5b350-139">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="5b350-139">Click **Edit**.</span></span>
19. <span data-ttu-id="5b350-140">Noklikšķiniet uz bultiņas, lai šo izvēlnes elementu pievienotu izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="5b350-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="5b350-141">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b350-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="5b350-142">Inventarizācijas sliekšņa izveide</span><span class="sxs-lookup"><span data-stu-id="5b350-142">Create a counting threshold</span></span>
1. <span data-ttu-id="5b350-143">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas pārvaldība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas sliekšņi**.</span><span class="sxs-lookup"><span data-stu-id="5b350-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="5b350-144">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b350-144">Click **New**.</span></span>
3. <span data-ttu-id="5b350-145">Ievadiet vērtību laukā **Cikla inventarizācijas sliekšņa ID**.</span><span class="sxs-lookup"><span data-stu-id="5b350-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="5b350-146">Iestatiet opciju **Nekavējoties apstrādāt cikla inventarizāciju** uz Jā.</span><span class="sxs-lookup"><span data-stu-id="5b350-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="5b350-147">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5b350-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="5b350-148">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b350-148">Click **Save**.</span></span>
7. <span data-ttu-id="5b350-149">Noklikšķiniet uz **Atlasīt atrašanās vietas**.</span><span class="sxs-lookup"><span data-stu-id="5b350-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="5b350-150">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5b350-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="5b350-151">Atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="5b350-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="5b350-152">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5b350-152">Click **OK**.</span></span>
11. <span data-ttu-id="5b350-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5b350-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="5b350-154">Cikla inventarizācijas plāna izveide</span><span class="sxs-lookup"><span data-stu-id="5b350-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="5b350-155">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas pārvaldība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas plāni**.</span><span class="sxs-lookup"><span data-stu-id="5b350-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="5b350-156">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b350-156">Click **New**.</span></span>
3. <span data-ttu-id="5b350-157">Ievadiet vērtību laukā **Cikla inventarizācijas plāna ID**.</span><span class="sxs-lookup"><span data-stu-id="5b350-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="5b350-158">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5b350-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="5b350-159">Ievadiet skaitli laukā **Maksimālais cikla inventarizāciju skaits**.</span><span class="sxs-lookup"><span data-stu-id="5b350-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="5b350-160">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b350-160">Click **Save**.</span></span>
7. <span data-ttu-id="5b350-161">Noklikšķiniet uz **Atlasīt atrašanās vietas**.</span><span class="sxs-lookup"><span data-stu-id="5b350-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="5b350-162">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5b350-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="5b350-163">Atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="5b350-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="5b350-164">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5b350-164">Click **OK**.</span></span>
11. <span data-ttu-id="5b350-165">Ievadiet skaitli laukā **Dienu skaits starp cikla inventarizācijām**.</span><span class="sxs-lookup"><span data-stu-id="5b350-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="5b350-166">Piemēram, ja lauks **Dienu skaits starp cikla inventarizācijām** ir iestatīts uz 5, cikla inventarizācijas darbs tiks veidots ik pēc piecām dienām.</span><span class="sxs-lookup"><span data-stu-id="5b350-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="5b350-167">Tomēr, ja cikla inventarizācijas darbs tiek apstrādāts trešajā dienā, nākamais cikla inventarizācijas darbs tiks izveidots piecas dienas pēc tam, kad tika apstrādāta pēdējā cikla inventarizācija, t.i., 8. dienā.</span><span class="sxs-lookup"><span data-stu-id="5b350-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="5b350-168">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b350-168">Click **Save**.</span></span>
13. <span data-ttu-id="5b350-169">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b350-169">Click **New**.</span></span>
14. <span data-ttu-id="5b350-170">Ievadiet skaitli laukā **Secības numurs**.</span><span class="sxs-lookup"><span data-stu-id="5b350-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="5b350-171">Kārtošana tiek veikta no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="5b350-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="5b350-172">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="5b350-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="5b350-173">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5b350-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="5b350-174">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5b350-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="5b350-175">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b350-175">Click **Save**.</span></span>
18. <span data-ttu-id="5b350-176">Noklikšķiniet uz vaicājuma **Definēt preces**.</span><span class="sxs-lookup"><span data-stu-id="5b350-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="5b350-177">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5b350-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="5b350-178">Ievadiet vai atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="5b350-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="5b350-179">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5b350-179">Click **OK**.</span></span>
22. <span data-ttu-id="5b350-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5b350-180">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]