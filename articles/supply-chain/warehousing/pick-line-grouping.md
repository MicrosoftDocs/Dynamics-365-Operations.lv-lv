---
title: Izdošanas rindu grupēšana
description: Šajā tēmā ir sniegts pārskats par izdošanas rindu grupēšanu.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906272"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="dede4-103">Izdošanas rindu grupēšana</span><span class="sxs-lookup"><span data-stu-id="dede4-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dede4-104">Izdošanas rindu grupēšanā vairākas darba rindas, kurām ir viens un tas pats vienums un novietojums, var apvienot vienā savākšanas programmā, kas lietotājam tiek uzrādīta mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="dede4-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="dede4-105">Tādējādi noliktavas darbinieki var saņemt visefektīvākos iespējamos norādījumus, bet tiek uzturēta arī nepieciešamā darba līniju nodalīšana sistēmā (piemēram, dažādiem konteineriem un pasūtījumiem).</span><span class="sxs-lookup"><span data-stu-id="dede4-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="dede4-106">Izdošanas rindu grupēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="dede4-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="dede4-107">Mobilās ierīces izvēlnes elementa izveide</span><span class="sxs-lookup"><span data-stu-id="dede4-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="dede4-108">Dodieties uz **Noliktavas pārvaldība \>Iestatījumi \>Mobilās ierīces \>Mobilās ierīces izvēlnes vienumi** un izveidojiet jaunu izvēlnes vienumu ar nosaukumu **Pārdošanas grupas rindas izdošana — lietotāja norādīts**.</span><span class="sxs-lookup"><span data-stu-id="dede4-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="dede4-109">Sadaļā **Mobilās ierīces izvēlnes vienumi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="dede4-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="dede4-110">Laukā **izvēlnes elementa nosaukums** ievadiet **Pārdošanas izdošana - grupas rinda**.</span><span class="sxs-lookup"><span data-stu-id="dede4-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="dede4-111">Laukā **Nosaukums** ievadiet **Pārdošanas izdošana - grupas rinda**.</span><span class="sxs-lookup"><span data-stu-id="dede4-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="dede4-112">Laukā **Režīms** atlasiet **Darba**.</span><span class="sxs-lookup"><span data-stu-id="dede4-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="dede4-113">Iestatiet opciju **Izmantot esošo darbu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="dede4-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="dede4-114">Kopsavilkuma cilnē **Vispārīgi** jūs varat iestatīt šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="dede4-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="dede4-115">Laukā **Noteica** atlasiet **Noteica lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="dede4-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="dede4-116">Iestatiet opciju **Ģenerēt pozīcijas unikālo noliktavas vienības identifikatoru** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="dede4-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="dede4-117">Atlasiet opcijas **Grupas izdošana** iestatījumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="dede4-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="dede4-118">Kopsavilkuma cilnē **Darba klases** veiciet šīs darbības, lai konfigurētu mobilās ierīces izvēlnes vienumam derīgās darba klases:</span><span class="sxs-lookup"><span data-stu-id="dede4-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="dede4-119">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="dede4-119">Select **New**.</span></span>
    2. <span data-ttu-id="dede4-120">Laukā **Darba klases ID** atlasiet **Pārdošana** vai **SO izdošana**atkarībā no noliktavas, kuru izmantosiet.</span><span class="sxs-lookup"><span data-stu-id="dede4-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="dede4-121">Laukā **Darba pasūtījuma veids** atlasiet **Pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="dede4-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="dede4-122">Mobilās ierīces izvēlnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="dede4-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="dede4-123">Dodieties uz **Noliktavas vadība \> Iestatīšana \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="dede4-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="dede4-124">Pievienojiet tikko izveidoto izvēlnes vienumu vēlamajai izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="dede4-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="dede4-125">Darba veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="dede4-125">Set up a work template</span></span>

1. <span data-ttu-id="dede4-126">Doties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="dede4-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="dede4-127">Atrodiet darba veidni, kas jāizmanto ar šo funkciju.</span><span class="sxs-lookup"><span data-stu-id="dede4-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="dede4-128">Šajā piemērā atlasiet standarta **51 izdot posmam** Contoso darba veidni.</span><span class="sxs-lookup"><span data-stu-id="dede4-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="dede4-129">Izvēlnē atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="dede4-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="dede4-130">Cilnē **Kārtošana** atlasiet **Pievienot** un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="dede4-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="dede4-131">Laukā **Tabula** atlasiet **Pagaidu darba transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="dede4-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="dede4-132">Laukā **Atveidotā tabula** atlasiet **Pagaidu darba transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="dede4-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="dede4-133">Laukā **Lauks** atlasiet **Vienuma numurs**.</span><span class="sxs-lookup"><span data-stu-id="dede4-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="dede4-134">Laukā **Meklēšanas virziens** atlasiet **Augošā secībā**.</span><span class="sxs-lookup"><span data-stu-id="dede4-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="dede4-135">Lai izdošanas rindu grupēšanas funkcionalitāte darbotos, darba rindas ir jākārto pēc vienuma ID.</span><span class="sxs-lookup"><span data-stu-id="dede4-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="dede4-136">Ja rindas, kurām ir vienādi vienumi, netiek kārtotas viena pēc otras, tās netiks grupētas.</span><span class="sxs-lookup"><span data-stu-id="dede4-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="dede4-137">Paraugs</span><span class="sxs-lookup"><span data-stu-id="dede4-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="dede4-138">Izveidot izdošanas darbu</span><span class="sxs-lookup"><span data-stu-id="dede4-138">Create picking work</span></span>

<span data-ttu-id="dede4-139">Pirms varēsiet iestatīt izdošanas rindas grupēšanu, ir jāizveido daži piemēroti izejošie darbi.</span><span class="sxs-lookup"><span data-stu-id="dede4-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="dede4-140">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="dede4-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="dede4-141">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="dede4-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="dede4-142">Laukā **Debitora konts** atlasiet jebkuru debitoru.</span><span class="sxs-lookup"><span data-stu-id="dede4-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="dede4-143">Kopsavilkuma cilnes **Vispārīgi** laukā **Noliktava** atlasiet **51**.</span><span class="sxs-lookup"><span data-stu-id="dede4-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="dede4-144">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="dede4-144">Then select **OK**.</span></span>
5. <span data-ttu-id="dede4-145">Sadaļā **Pārdošanas pasūtījuma rindas**pievienojiet šādas sešas rindas:</span><span class="sxs-lookup"><span data-stu-id="dede4-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="dede4-146">**1. rinda:** laukā **Krājuma numurs**, atlasiet **M9200**.</span><span class="sxs-lookup"><span data-stu-id="dede4-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="dede4-147">Laukā **Daudzums** ievadiet **3**.</span><span class="sxs-lookup"><span data-stu-id="dede4-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="dede4-148">**2. rinda:** laukā **Krājuma numurs**, atlasiet **M9201**.</span><span class="sxs-lookup"><span data-stu-id="dede4-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="dede4-149">Laukā **Daudzums** ievadiet **3**.</span><span class="sxs-lookup"><span data-stu-id="dede4-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="dede4-150">**3. rinda:** laukā **Krājuma numurs**, atlasiet **M9202**.</span><span class="sxs-lookup"><span data-stu-id="dede4-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="dede4-151">Laukā **Daudzums** ievadiet **2**.</span><span class="sxs-lookup"><span data-stu-id="dede4-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="dede4-152">**4. rinda:** laukā **Krājuma numurs**, atlasiet **M9200**.</span><span class="sxs-lookup"><span data-stu-id="dede4-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="dede4-153">Laukā **Daudzums** ievadiet **1**.</span><span class="sxs-lookup"><span data-stu-id="dede4-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="dede4-154">**5. rinda:** laukā **Krājuma numurs**, atlasiet **M9200**.</span><span class="sxs-lookup"><span data-stu-id="dede4-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="dede4-155">Laukā **Daudzums** ievadiet **3**.</span><span class="sxs-lookup"><span data-stu-id="dede4-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="dede4-156">**6. rinda:** laukā **Krājuma numurs**, atlasiet **M9202**.</span><span class="sxs-lookup"><span data-stu-id="dede4-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="dede4-157">Laukā **Daudzums** ievadiet **7**.</span><span class="sxs-lookup"><span data-stu-id="dede4-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="dede4-158">Šeit ir kopsavilkums par kopējiem daudzumiem katram krājumam:</span><span class="sxs-lookup"><span data-stu-id="dede4-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="dede4-159">**Krājums M9200:** 7 katram</span><span class="sxs-lookup"><span data-stu-id="dede4-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="dede4-160">**Krājums M9201:** 3 katram</span><span class="sxs-lookup"><span data-stu-id="dede4-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="dede4-161">**Krājums M9202:** 9 katram</span><span class="sxs-lookup"><span data-stu-id="dede4-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="dede4-162">Pirms pasūtījumu izdošanas noliktavā jāpārliecinās, vai savākšanas vietās ir pietiekami daudz krājumu visām precēm visos pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="dede4-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="dede4-163">Pārskatiet **Atrašanās vietas direktīvas** iestatījumu, lai noteiktu, kuras izdošanas vietas tiek izmantotas pārdošanas pasūtījuma izdošanai.</span><span class="sxs-lookup"><span data-stu-id="dede4-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="dede4-164">Rezervējiet krājumu un izdodiet to noliktavai.</span><span class="sxs-lookup"><span data-stu-id="dede4-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="dede4-165">Tiek izveidots darba ID, kuram ir sešas rindas.</span><span class="sxs-lookup"><span data-stu-id="dede4-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="dede4-166">Rindas tiek kārtotas pēc krājuma koda.</span><span class="sxs-lookup"><span data-stu-id="dede4-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="dede4-167">Mobilās ierīces plūsmas palaišana</span><span class="sxs-lookup"><span data-stu-id="dede4-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="dede4-168">Mobilajā ierīcē atlasiet izvēlni, kurā ir iekļauts jaunais mobilās ierīces izvēlnes vienums.</span><span class="sxs-lookup"><span data-stu-id="dede4-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="dede4-169">Atlasiet izvēlnes vienumu **Pārdošanas izdošana - Grupas rinda** un iniciējiet izdošanu.</span><span class="sxs-lookup"><span data-stu-id="dede4-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="dede4-170">Kad ir atlasīta izvēlne un ievadīts darba ID, tiek parādīta izdošanas darbība, kurā ir grupētas visas preču M9200 savākšanas rindas.</span><span class="sxs-lookup"><span data-stu-id="dede4-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="dede4-171">Jūs saņemat instrukciju, lai izvēlētos 7 katram no krājumiem M9200.</span><span class="sxs-lookup"><span data-stu-id="dede4-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="dede4-172">Apstipriniet izdošanas darbību.</span><span class="sxs-lookup"><span data-stu-id="dede4-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="dede4-173">Pārejiet uz darba procesa klienta ekrānu un ievērojiet, ka visas trīs savākšanas rindas krājumam M9200 tika slēgtas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="dede4-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="dede4-174">Uzrāda 4. darba līniju.</span><span class="sxs-lookup"><span data-stu-id="dede4-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="dede4-175">Apstipriniet izdošanas darbību.</span><span class="sxs-lookup"><span data-stu-id="dede4-175">Confirm the pick step.</span></span>

    <span data-ttu-id="dede4-176">Pēdējā izdošanas darbība mobilajā ierīcē apkopo pēdējās divas izdošanas rindas no darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="dede4-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="dede4-177">Pabeidziet izdošanas darbību pa 9 no katra krājuma M9202.</span><span class="sxs-lookup"><span data-stu-id="dede4-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="dede4-178">Apstipriniet nolikšanas darbību un visus papildu izdošanas/nolikšanas pārus, lai pabeigtu darbu.</span><span class="sxs-lookup"><span data-stu-id="dede4-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="dede4-179">Darba rindas var grupēt tikai tad, ja tās ir secīgas.</span><span class="sxs-lookup"><span data-stu-id="dede4-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="dede4-180">Šī funkcionalitāte netiek atbalstīta:</span><span class="sxs-lookup"><span data-stu-id="dede4-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="dede4-181">Pieļaujamā svara krājumi.</span><span class="sxs-lookup"><span data-stu-id="dede4-181">Catch-weight items.</span></span> <span data-ttu-id="dede4-182">Ja darbā ir kādi pieļaujamā svara krājumi, jūs pirms izdošanas uzsākšanas saņemsit kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="dede4-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="dede4-183">Vienību izdošana.</span><span class="sxs-lookup"><span data-stu-id="dede4-183">Piece picking.</span></span>
>    - <span data-ttu-id="dede4-184">Darba rindas, kurām ir nepabeigt papildināšanas darbi.</span><span class="sxs-lookup"><span data-stu-id="dede4-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="dede4-185">Pārizidošana.</span><span class="sxs-lookup"><span data-stu-id="dede4-185">Over-picking.</span></span>
