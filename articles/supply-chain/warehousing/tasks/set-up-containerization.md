--- 
title: "Konteinerizēšanas iestatīšana"
description: "Šajā procedūrā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā Noliktavas vadība."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3f68251365ae34b7c4a2ce25b5b59275e856df55
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="9da11-103">Konteinerizēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9da11-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9da11-104">Šajā procedūrā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā Noliktavas vadība.</span><span class="sxs-lookup"><span data-stu-id="9da11-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="9da11-105">Automatizētā konteinerizēšanas izveido konteinerus un izdošanas darbu kravām, kad kopums ir apstrādāts un darba rindas var sadalīt daudzumos, kas atbilst konteineriem.</span><span class="sxs-lookup"><span data-stu-id="9da11-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="9da11-106">Tas palīdz noliktavas darbiniekiem izdot krājumus tieši uz izvēlēto konteineru.</span><span class="sxs-lookup"><span data-stu-id="9da11-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="9da11-107">Salīdzinot ar manuālo iepakošanas procesu, uzdevumus, piemēram, konteinera izveide, krājumu piešķiršana vai konteineru slēgšana automatizē sistēma.</span><span class="sxs-lookup"><span data-stu-id="9da11-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="9da11-108">Šī procedūra izmanto USMF demonstrācijas uzņēmumu, un to veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="9da11-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="9da11-109">Iestatiet kopuma veidni</span><span class="sxs-lookup"><span data-stu-id="9da11-109">Set up a wave template</span></span>
1. <span data-ttu-id="9da11-110">Dodieties uz Noliktavas vadība > Iestatīšana > Kopumi > Kopumu veidnes.</span><span class="sxs-lookup"><span data-stu-id="9da11-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="9da11-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-111">Click New.</span></span>
3. <span data-ttu-id="9da11-112">Ierakstiet vērtību laukā Kopuma veidnes nosaukums.</span><span class="sxs-lookup"><span data-stu-id="9da11-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="9da11-113">Laukā Kopuma veidnes apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="9da11-114">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="9da11-115">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="9da11-116">Izvērsiet sadaļu Metodes.</span><span class="sxs-lookup"><span data-stu-id="9da11-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="9da11-117">Atlasīto metožu rūtī tiek uzskaitītas atlasītā kopuma veidnes veida metodes.</span><span class="sxs-lookup"><span data-stu-id="9da11-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="9da11-118">Kopuma veidnei ir jāietver konteinerizēšanas metode.</span><span class="sxs-lookup"><span data-stu-id="9da11-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="9da11-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9da11-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="9da11-120">Laukā Kopuma darbības kods, ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="9da11-121">Ievadiet kopuma darbības kodu pievienotajai metodei, kas var būt jebkurš kods.</span><span class="sxs-lookup"><span data-stu-id="9da11-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="9da11-122">Ir iespējams pievienot metodi vairāk nekā vienu reizi, un piešķirt dažādus kopuma darbību kodus.</span><span class="sxs-lookup"><span data-stu-id="9da11-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="9da11-123">Lai to izdarītu, kopuma procesa metodes lapā atlasiet Atkārtojams šai metodei.</span><span class="sxs-lookup"><span data-stu-id="9da11-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="9da11-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9da11-124">Click Save.</span></span>
11. <span data-ttu-id="9da11-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9da11-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="9da11-126">Konteinera tipa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9da11-126">Set up a container type</span></span>
1. <span data-ttu-id="9da11-127">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru veidi.</span><span class="sxs-lookup"><span data-stu-id="9da11-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="9da11-128">Jūs varat definēt konteinerus lapā Konteineru veidi.</span><span class="sxs-lookup"><span data-stu-id="9da11-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="9da11-129">Jūs varat konfigurēt konteineru fiziskās dimensijas, ieskaitot taras svaru, maksimālo svaru, maksimālo tilpumu, garumu, platumu un augstumu.</span><span class="sxs-lookup"><span data-stu-id="9da11-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="9da11-130">Šajā piemērā, mums ir trīs dažādu izmēru kastes.</span><span class="sxs-lookup"><span data-stu-id="9da11-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="9da11-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-131">Click New.</span></span>
3. <span data-ttu-id="9da11-132">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="9da11-133">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="9da11-134">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="9da11-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="9da11-135">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="9da11-136">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="9da11-137">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="9da11-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="9da11-138">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="9da11-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="9da11-139">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="9da11-140">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9da11-140">Click Save.</span></span>
12. <span data-ttu-id="9da11-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-141">Click New.</span></span>
13. <span data-ttu-id="9da11-142">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="9da11-143">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="9da11-144">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="9da11-145">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="9da11-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="9da11-146">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="9da11-147">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="9da11-148">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="9da11-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="9da11-149">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="9da11-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="9da11-150">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9da11-150">Click Save.</span></span>
22. <span data-ttu-id="9da11-151">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-151">Click New.</span></span>
23. <span data-ttu-id="9da11-152">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="9da11-153">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="9da11-154">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="9da11-155">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="9da11-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="9da11-156">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="9da11-157">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9da11-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="9da11-158">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="9da11-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="9da11-159">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="9da11-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="9da11-160">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9da11-160">Click Save.</span></span>
32. <span data-ttu-id="9da11-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9da11-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="9da11-162">Konteineru grupas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9da11-162">Set up a container group</span></span>
1. <span data-ttu-id="9da11-163">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru grupas.</span><span class="sxs-lookup"><span data-stu-id="9da11-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="9da11-164">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-164">Click New.</span></span>
    * <span data-ttu-id="9da11-165">Varat iestatīt konteineru tipu loģiskās grupas.</span><span class="sxs-lookup"><span data-stu-id="9da11-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="9da11-166">Katrai grupai varat norādīt secību, kādā konteineri ir jāiepako, kā arī konteineru aizpildes procentus. Programma izmanto krājuma lieluma dimensijas, lai noteiktu, vai šis krājums ietilpst konteinerā.</span><span class="sxs-lookup"><span data-stu-id="9da11-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="9da11-167">Tiek izmantots konteiners, kas ir vistuvāk krājuma izmēru dimensijām.</span><span class="sxs-lookup"><span data-stu-id="9da11-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="9da11-168">Ja vienā grupā ir vairāki konteineru tipi, ieteicams izveidot secību pēc lieluma, lai lielākais konteiners būtu pirmais, šīs secības 1. numurs, un vismazākais konteiners būtu pēdējais.</span><span class="sxs-lookup"><span data-stu-id="9da11-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="9da11-169">Laukā Konteinera grupas ID, ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="9da11-170">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9da11-171">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-171">Click New.</span></span>
6. <span data-ttu-id="9da11-172">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9da11-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="9da11-173">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="9da11-174">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-174">Click New.</span></span>
9. <span data-ttu-id="9da11-175">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9da11-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="9da11-176">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="9da11-177">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-177">Click New.</span></span>
12. <span data-ttu-id="9da11-178">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9da11-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="9da11-179">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="9da11-180">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9da11-180">Click Save.</span></span>
15. <span data-ttu-id="9da11-181">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9da11-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="9da11-182">Konteinera būvējuma veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9da11-182">Set up a container build template</span></span>
1. <span data-ttu-id="9da11-183">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteinera būvējuma veidnes.</span><span class="sxs-lookup"><span data-stu-id="9da11-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="9da11-184">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-184">Click New.</span></span>
    * <span data-ttu-id="9da11-185">Konteinera būvējuma veidne ir balstīta uz to, kuri konteinerizēšanas procesi tiek veikti.</span><span class="sxs-lookup"><span data-stu-id="9da11-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="9da11-186">Katra konteinera būvējuma veidne nosaka vienu konteinerizēšanas procesu, kas tiks izmantots kopuma veidnē.</span><span class="sxs-lookup"><span data-stu-id="9da11-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="9da11-187">Opcija Rediģēt vaicājumu ļauj definēt nosacījumus, kuros tiks apstrādāta atlasītā veidne.</span><span class="sxs-lookup"><span data-stu-id="9da11-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="9da11-188">Piemēram, jūs varat palaist konteinerizēšanu tikai noteiktiem debitoriem, produktiem vai noliktavām, vai jūs veidnei varat pievienot atbilstošus vaicājuma diapazonus.</span><span class="sxs-lookup"><span data-stu-id="9da11-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="9da11-189">Lauks Kopuma darbību kods ir kā konteinera būvējuma veidne tiek saistīta ar darbībām kopuma veidnē.</span><span class="sxs-lookup"><span data-stu-id="9da11-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="9da11-190">Izpildot kopumu, tā nosaka, kura konteinera būvējuma veidne(-s) tiek izmantota, lai uzsāktu konteinerizēšanu.</span><span class="sxs-lookup"><span data-stu-id="9da11-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="9da11-191">Lauks Bāzes vaicājuma veids nosaka, ko iepakot un uz ko balstīt filtra vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="9da11-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="9da11-192">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9da11-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9da11-193">Laukā Konteinera veidnes ID, ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="9da11-194">Laukā Konteinera grupas ID, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="9da11-195">Laukā Kopuma darbības kods, ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="9da11-196">Atzīmējiet izvēles rūtiņu Atļaut izdošanu sadali.</span><span class="sxs-lookup"><span data-stu-id="9da11-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="9da11-197">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9da11-197">Click Save.</span></span>
9. <span data-ttu-id="9da11-198">Noklikšķiniet uz Konteineru kombinēti ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="9da11-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="9da11-199">Kombinēšanas loģikas pārtraukumpunkti ļauj iestatīt noteikumus iepakošanas sadalījuma rindām konteineros.</span><span class="sxs-lookup"><span data-stu-id="9da11-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="9da11-200">Piemēram, ja pievienojat lauku Krājuma numurs, kad krājumi tiek piešķirti konteineriem, jauns konteineris tiks izveidots, parādoties jaunam krājuma kodam.</span><span class="sxs-lookup"><span data-stu-id="9da11-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="9da11-201">Tas novērsīs darbiniekus no iepakojuma sadalījuma rindām diviem dažādiem klientiem vienā konteinerā.</span><span class="sxs-lookup"><span data-stu-id="9da11-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="9da11-202">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9da11-202">Click New.</span></span>
11. <span data-ttu-id="9da11-203">Laukā Tabula, atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9da11-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="9da11-204">Laukā Atlasīt lauku, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9da11-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="9da11-205">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9da11-205">Click OK.</span></span>


