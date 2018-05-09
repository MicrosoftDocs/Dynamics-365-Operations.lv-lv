--- 
title: "Konteinerizēšanas iestatīšana"
description: "Šajā procedūrā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā Noliktavas vadība."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4e7a2fde65c8dba8b16c5a87eae0ec2bbebc3388
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="42ebc-103">Konteinerizēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="42ebc-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42ebc-104">Šajā procedūrā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā Noliktavas vadība.</span><span class="sxs-lookup"><span data-stu-id="42ebc-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="42ebc-105">Automatizētā konteinerizēšanas izveido konteinerus un izdošanas darbu kravām, kad kopums ir apstrādāts un darba rindas var sadalīt daudzumos, kas atbilst konteineriem.</span><span class="sxs-lookup"><span data-stu-id="42ebc-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="42ebc-106">Tas palīdz noliktavas darbiniekiem izdot krājumus tieši uz izvēlēto konteineru.</span><span class="sxs-lookup"><span data-stu-id="42ebc-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="42ebc-107">Salīdzinot ar manuālo iepakošanas procesu, uzdevumus, piemēram, konteinera izveide, krājumu piešķiršana vai konteineru slēgšana automatizē sistēma.</span><span class="sxs-lookup"><span data-stu-id="42ebc-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="42ebc-108">Šī procedūra izmanto USMF demonstrācijas uzņēmumu, un to veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="42ebc-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="42ebc-109">Iestatiet kopuma veidni</span><span class="sxs-lookup"><span data-stu-id="42ebc-109">Set up a wave template</span></span>
1. <span data-ttu-id="42ebc-110">Dodieties uz Noliktavas vadība > Iestatīšana > Kopumi > Kopumu veidnes.</span><span class="sxs-lookup"><span data-stu-id="42ebc-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="42ebc-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-111">Click New.</span></span>
3. <span data-ttu-id="42ebc-112">Ierakstiet vērtību laukā Kopuma veidnes nosaukums.</span><span class="sxs-lookup"><span data-stu-id="42ebc-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="42ebc-113">Laukā Kopuma veidnes apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="42ebc-114">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="42ebc-115">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="42ebc-116">Izvērsiet sadaļu Metodes.</span><span class="sxs-lookup"><span data-stu-id="42ebc-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="42ebc-117">Atlasīto metožu rūtī tiek uzskaitītas atlasītā kopuma veidnes veida metodes.</span><span class="sxs-lookup"><span data-stu-id="42ebc-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="42ebc-118">Kopuma veidnei ir jāietver konteinerizēšanas metode.</span><span class="sxs-lookup"><span data-stu-id="42ebc-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="42ebc-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="42ebc-120">Laukā Kopuma darbības kods, ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="42ebc-121">Ievadiet kopuma darbības kodu pievienotajai metodei, kas var būt jebkurš kods.</span><span class="sxs-lookup"><span data-stu-id="42ebc-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="42ebc-122">Ir iespējams pievienot metodi vairāk nekā vienu reizi, un piešķirt dažādus kopuma darbību kodus.</span><span class="sxs-lookup"><span data-stu-id="42ebc-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="42ebc-123">Lai to izdarītu, kopuma procesa metodes lapā atlasiet Atkārtojams šai metodei.</span><span class="sxs-lookup"><span data-stu-id="42ebc-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="42ebc-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="42ebc-124">Click Save.</span></span>
11. <span data-ttu-id="42ebc-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="42ebc-126">Konteinera tipa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="42ebc-126">Set up a container type</span></span>
1. <span data-ttu-id="42ebc-127">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru veidi.</span><span class="sxs-lookup"><span data-stu-id="42ebc-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="42ebc-128">Jūs varat definēt konteinerus lapā Konteineru veidi.</span><span class="sxs-lookup"><span data-stu-id="42ebc-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="42ebc-129">Jūs varat konfigurēt konteineru fiziskās dimensijas, ieskaitot taras svaru, maksimālo svaru, maksimālo tilpumu, garumu, platumu un augstumu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="42ebc-130">Šajā piemērā, mums ir trīs dažādu izmēru kastes.</span><span class="sxs-lookup"><span data-stu-id="42ebc-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="42ebc-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-131">Click New.</span></span>
3. <span data-ttu-id="42ebc-132">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="42ebc-133">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="42ebc-134">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="42ebc-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="42ebc-135">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="42ebc-136">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="42ebc-137">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="42ebc-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="42ebc-138">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="42ebc-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="42ebc-139">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="42ebc-140">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="42ebc-140">Click Save.</span></span>
12. <span data-ttu-id="42ebc-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-141">Click New.</span></span>
13. <span data-ttu-id="42ebc-142">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="42ebc-143">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="42ebc-144">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="42ebc-145">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="42ebc-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="42ebc-146">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="42ebc-147">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="42ebc-148">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="42ebc-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="42ebc-149">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="42ebc-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="42ebc-150">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="42ebc-150">Click Save.</span></span>
22. <span data-ttu-id="42ebc-151">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-151">Click New.</span></span>
23. <span data-ttu-id="42ebc-152">Laukā Konteinera veida kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="42ebc-153">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="42ebc-154">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="42ebc-155">Ievadiet skaitli laukā Maksimālais svars.</span><span class="sxs-lookup"><span data-stu-id="42ebc-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="42ebc-156">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="42ebc-157">Laukā Garums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="42ebc-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="42ebc-158">Ievadiet skaitli laukā Platums.</span><span class="sxs-lookup"><span data-stu-id="42ebc-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="42ebc-159">Ievadiet skaitli laukā Augstums.</span><span class="sxs-lookup"><span data-stu-id="42ebc-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="42ebc-160">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="42ebc-160">Click Save.</span></span>
32. <span data-ttu-id="42ebc-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="42ebc-162">Konteineru grupas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="42ebc-162">Set up a container group</span></span>
1. <span data-ttu-id="42ebc-163">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru grupas.</span><span class="sxs-lookup"><span data-stu-id="42ebc-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="42ebc-164">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-164">Click New.</span></span>
    * <span data-ttu-id="42ebc-165">Varat iestatīt konteineru tipu loģiskās grupas.</span><span class="sxs-lookup"><span data-stu-id="42ebc-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="42ebc-166">Katrai grupai jūs varat norādīt secību, kādā konteineri tiek iepakoti, kā arī katra konteinera aizpildes vērtību procentos.</span><span class="sxs-lookup"><span data-stu-id="42ebc-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="42ebc-167">Krājuma izmēru dimensijas tiek izmantotas, lai noteiktu, vai krājumu varēs ievietot konteinerā.</span><span class="sxs-lookup"><span data-stu-id="42ebc-167">The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="42ebc-168">Tiek izmantots konteiners, kas ir vistuvāk krājuma izmēru dimensijām.</span><span class="sxs-lookup"><span data-stu-id="42ebc-168">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="42ebc-169">Ja vienā grupā ir vairāki konteineru tipi, ieteicams izveidot secību pēc lieluma, lai lielākais konteiners būtu pirmais, šīs secības 1. numurs, un vismazākais konteiners būtu pēdējais.</span><span class="sxs-lookup"><span data-stu-id="42ebc-169">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="42ebc-170">Laukā Konteinera grupas ID, ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-170">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="42ebc-171">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-171">In the Description field, type a value.</span></span>
5. <span data-ttu-id="42ebc-172">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-172">Click New.</span></span>
6. <span data-ttu-id="42ebc-173">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-173">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="42ebc-174">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-174">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="42ebc-175">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-175">Click New.</span></span>
9. <span data-ttu-id="42ebc-176">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-176">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="42ebc-177">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-177">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="42ebc-178">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-178">Click New.</span></span>
12. <span data-ttu-id="42ebc-179">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-179">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="42ebc-180">Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-180">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="42ebc-181">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="42ebc-181">Click Save.</span></span>
15. <span data-ttu-id="42ebc-182">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-182">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="42ebc-183">Konteinera būvējuma veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="42ebc-183">Set up a container build template</span></span>
1. <span data-ttu-id="42ebc-184">Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteinera būvējuma veidnes.</span><span class="sxs-lookup"><span data-stu-id="42ebc-184">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="42ebc-185">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-185">Click New.</span></span>
    * <span data-ttu-id="42ebc-186">Konteinera būvējuma veidne ir balstīta uz to, kuri konteinerizēšanas procesi tiek veikti.</span><span class="sxs-lookup"><span data-stu-id="42ebc-186">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="42ebc-187">Katra konteinera būvējuma veidne nosaka vienu konteinerizēšanas procesu, kas tiks izmantots kopuma veidnē.</span><span class="sxs-lookup"><span data-stu-id="42ebc-187">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="42ebc-188">Opcija Rediģēt vaicājumu ļauj definēt nosacījumus, kuros tiks apstrādāta atlasītā veidne.</span><span class="sxs-lookup"><span data-stu-id="42ebc-188">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="42ebc-189">Piemēram, jūs varat palaist konteinerizēšanu tikai noteiktiem debitoriem, produktiem vai noliktavām, vai jūs veidnei varat pievienot atbilstošus vaicājuma diapazonus.</span><span class="sxs-lookup"><span data-stu-id="42ebc-189">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="42ebc-190">Lauks Kopuma darbību kods ir kā konteinera būvējuma veidne tiek saistīta ar darbībām kopuma veidnē.</span><span class="sxs-lookup"><span data-stu-id="42ebc-190">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="42ebc-191">Izpildot kopumu, tā nosaka, kura konteinera būvējuma veidne(-s) tiek izmantota, lai uzsāktu konteinerizēšanu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-191">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="42ebc-192">Lauks Bāzes vaicājuma veids nosaka, ko iepakot un uz ko balstīt filtra vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-192">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="42ebc-193">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="42ebc-193">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="42ebc-194">Laukā Konteinera veidnes ID, ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-194">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="42ebc-195">Laukā Konteinera grupas ID, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-195">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="42ebc-196">Laukā Kopuma darbības kods, ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-196">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="42ebc-197">Atzīmējiet izvēles rūtiņu Atļaut izdošanu sadali.</span><span class="sxs-lookup"><span data-stu-id="42ebc-197">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="42ebc-198">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="42ebc-198">Click Save.</span></span>
9. <span data-ttu-id="42ebc-199">Noklikšķiniet uz Konteineru kombinēšanas ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="42ebc-199">Click Container mixing constraints.</span></span>
    * <span data-ttu-id="42ebc-200">Kombinēšanas loģikas pārtraukumpunkti ļauj iestatīt noteikumus iepakošanas sadalījuma rindām konteineros.</span><span class="sxs-lookup"><span data-stu-id="42ebc-200">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="42ebc-201">Piemēram, ja pievienojat lauku Krājuma numurs, kad krājumi tiek piešķirti konteineriem, jauns konteineris tiks izveidots, parādoties jaunam krājuma kodam.</span><span class="sxs-lookup"><span data-stu-id="42ebc-201">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="42ebc-202">Tas novērsīs darbiniekus no iepakojuma sadalījuma rindām diviem dažādiem klientiem vienā konteinerā.</span><span class="sxs-lookup"><span data-stu-id="42ebc-202">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="42ebc-203">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="42ebc-203">Click New.</span></span>
11. <span data-ttu-id="42ebc-204">Laukā Tabula, atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="42ebc-204">In the Table field, select an option.</span></span>
12. <span data-ttu-id="42ebc-205">Laukā Atlasīt lauku, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42ebc-205">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="42ebc-206">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="42ebc-206">Click OK.</span></span>


