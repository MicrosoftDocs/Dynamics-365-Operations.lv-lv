---
title: Izdošanas rindu grupēšana
description: Šajā tēmā ir sniegts pārskats par izdošanas rindu grupēšanu.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e70244d46ec2787fefdb097d0354af7910b55e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989722"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="8878e-103">Izdošanas rindu grupēšana</span><span class="sxs-lookup"><span data-stu-id="8878e-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8878e-104">Izdošanas rindu grupēšanā vairākas darba rindas, kurām ir viens un tas pats vienums un novietojums, var apvienot vienā savākšanas programmā, kas lietotājam tiek uzrādīta mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="8878e-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="8878e-105">Tādējādi noliktavas darbinieki var saņemt visefektīvākos iespējamos norādījumus, bet tiek uzturēta arī nepieciešamā darba līniju nodalīšana sistēmā (piemēram, dažādiem konteineriem un pasūtījumiem).</span><span class="sxs-lookup"><span data-stu-id="8878e-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="8878e-106">Darba izdošanas rindas pārskata līdzekļa ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="8878e-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="8878e-107">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="8878e-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="8878e-108">Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="8878e-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="8878e-109">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="8878e-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8878e-110">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="8878e-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="8878e-111">**Līdzekļa nosaukums:** *Izvēles rindu grupēšana*</span><span class="sxs-lookup"><span data-stu-id="8878e-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="8878e-112">Izdošanas rindu grupēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8878e-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="8878e-113">Mobilās ierīces izvēlnes elementa izveide</span><span class="sxs-lookup"><span data-stu-id="8878e-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="8878e-114">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="8878e-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="8878e-115">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8878e-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8878e-116">Laukā **Izvēlnes elementa nosaukums** ievadiet *Pārdošanas grupas rindu izdošana*.</span><span class="sxs-lookup"><span data-stu-id="8878e-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="8878e-117">Laukā **Nosaukums** ievadiet *Pārdošanas grupas rindas izdošana*.</span><span class="sxs-lookup"><span data-stu-id="8878e-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="8878e-118">Šis nosaukums tiks rādīts mobilās ierīces izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="8878e-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="8878e-119">Laukā **Režīms** atlasiet *Darbs*.</span><span class="sxs-lookup"><span data-stu-id="8878e-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="8878e-120">Iestatiet opciju **Izmantot esošo darbu** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="8878e-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="8878e-121">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="8878e-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8878e-122">Laukā **Noteica** atlasiet *Noteica lietotājs*.</span><span class="sxs-lookup"><span data-stu-id="8878e-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="8878e-123">Iestatiet opciju **Ģenerēt pozīcijas unikālo noliktavas vienības identifikatoru** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="8878e-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="8878e-124">Atlasiet opcijas **Grupas izdošana** iestatījumu *Jā*.</span><span class="sxs-lookup"><span data-stu-id="8878e-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="8878e-125">Pieņemiet noklusējuma vērtības atlikušajām funkcijām.</span><span class="sxs-lookup"><span data-stu-id="8878e-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="8878e-126">Kopsavilkuma cilnē Darba klases veiciet šīs darbības, lai konfigurētu mobilās ierīces izvēlnes vienumam derīgās darba klases:</span><span class="sxs-lookup"><span data-stu-id="8878e-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="8878e-127">Kopsavilkuma cilnē **Darba klases** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8878e-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="8878e-128">Laukā **Darba klases ID** atlasiet *Pārdošana* vai *SO izdošana* atkarībā no noliktavas, kuru izmantosiet.</span><span class="sxs-lookup"><span data-stu-id="8878e-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="8878e-129">Šim scenārijam atlasiet *SO izdošana*.</span><span class="sxs-lookup"><span data-stu-id="8878e-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="8878e-130">Galvenē iestatiet lauku **Darba pasūtījuma veids** uz *Pirkšanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="8878e-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="8878e-131">Mobilās ierīces izvēlnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8878e-131">Set up a mobile device menu</span></span>

<span data-ttu-id="8878e-132">Sekojiet šiem soļiem, lai pievienotu tikko izveidoto izvēlnes elementu **Nosūtīšanas** izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="8878e-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="8878e-133">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="8878e-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="8878e-134">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="8878e-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8878e-135">Saraksta rūtī ir redzamas visas esošās mobilās ierīces izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="8878e-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="8878e-136">Sarakstā atlasiet *Izejošie*.</span><span class="sxs-lookup"><span data-stu-id="8878e-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="8878e-137">Režģī **Pieejamās izvēlnes un izvēļņu elementi** meklējiet un atlasiet tikko izveidoto izvēlnes elementu *Pārdošanas grupas rindu izdošana*.</span><span class="sxs-lookup"><span data-stu-id="8878e-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="8878e-138">Atlasiet labo bultiņu, lai pārvietotu *PO rindas saņemšanas* izvēlnes elementu **Izvēlņu struktūras** sarakstā.</span><span class="sxs-lookup"><span data-stu-id="8878e-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="8878e-139">Izmantojiet pogu uz augšu vai uz leju, lai pārvietotu izvēlnes elementu vēlamajā pozīcijā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="8878e-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="8878e-140">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8878e-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="8878e-141">Darba veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8878e-141">Set up a work template</span></span>

1. <span data-ttu-id="8878e-142">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="8878e-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="8878e-143">Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="8878e-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="8878e-144">Režģī **Pārskats** atrodiet un atlasiet darba veidni, kas jāizmanto ar šo funkciju.</span><span class="sxs-lookup"><span data-stu-id="8878e-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="8878e-145">Šim scenārijam atlasiet *51 izdot stadijai* veidni.</span><span class="sxs-lookup"><span data-stu-id="8878e-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="8878e-146">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="8878e-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8878e-147">Vaicājuma dialoglodziņa cilnē **Kārtošana** atlasiet **Pievienot**, lai pievienotu rindu, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="8878e-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="8878e-148">Kolonnā **Tabula** atlasiet *Pagaidu darba transakcijas*.</span><span class="sxs-lookup"><span data-stu-id="8878e-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="8878e-149">Laukā **Atveidotā tabula** atlasiet *Pagaidu darba transakcijas*.</span><span class="sxs-lookup"><span data-stu-id="8878e-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="8878e-150">Kolonnā **Lauks** atlasiet *Vienuma numurs*.</span><span class="sxs-lookup"><span data-stu-id="8878e-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="8878e-151">Laukā **Meklēšanas virziens** atlasiet *Augošā secībā*.</span><span class="sxs-lookup"><span data-stu-id="8878e-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="8878e-152">Atlasiet **Labi**, lai iestatījumus saglabātu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8878e-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="8878e-153">Var tikt parādīts šāds ziņojums: “Grupēšana tiks atiestatīta, vai turpināt?”</span><span class="sxs-lookup"><span data-stu-id="8878e-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="8878e-154">Lai turpinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8878e-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8878e-155">Lai izdošanas rindu grupēšanas funkcionalitāte darbotos, darba rindas ir jākārto pēc vienuma ID.</span><span class="sxs-lookup"><span data-stu-id="8878e-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="8878e-156">Ja rindas, kurām ir vienādi vienumi, netiek kārtotas viena pēc otras, tās netiks grupētas.</span><span class="sxs-lookup"><span data-stu-id="8878e-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="8878e-157">Paraugs</span><span class="sxs-lookup"><span data-stu-id="8878e-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="8878e-158">Izveidot izdošanas darbu</span><span class="sxs-lookup"><span data-stu-id="8878e-158">Create picking work</span></span>

<span data-ttu-id="8878e-159">Pirms varēsiet iestatīt izdošanas rindas grupēšanu, ir jāizveido daži piemēroti izejošie darbi.</span><span class="sxs-lookup"><span data-stu-id="8878e-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="8878e-160">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="8878e-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8878e-161">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="8878e-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="8878e-162">Laukā **Debitora konts** atlasiet *US-004*.</span><span class="sxs-lookup"><span data-stu-id="8878e-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="8878e-163">Kopsavilkuma cilnes **Vispārīgi** laukā **Noliktava** atlasiet *51*.</span><span class="sxs-lookup"><span data-stu-id="8878e-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="8878e-164">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8878e-164">Select **OK**.</span></span>
1. <span data-ttu-id="8878e-165">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet šādas sešas rindas:</span><span class="sxs-lookup"><span data-stu-id="8878e-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="8878e-166">**1. rinda:** laukā **Krājuma numurs**, atlasiet *M9200*.</span><span class="sxs-lookup"><span data-stu-id="8878e-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="8878e-167">Laukā **Daudzums** ievadiet *3*.</span><span class="sxs-lookup"><span data-stu-id="8878e-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="8878e-168">**2. rinda:** laukā **Krājuma numurs**, atlasiet *M9201*.</span><span class="sxs-lookup"><span data-stu-id="8878e-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="8878e-169">Laukā **Daudzums** ievadiet *3*.</span><span class="sxs-lookup"><span data-stu-id="8878e-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="8878e-170">**3. rinda:** laukā **Krājuma numurs**, atlasiet *M9202*.</span><span class="sxs-lookup"><span data-stu-id="8878e-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="8878e-171">Laukā **Daudzums** ievadiet *2*.</span><span class="sxs-lookup"><span data-stu-id="8878e-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="8878e-172">**4. rinda:** laukā **Krājuma numurs**, atlasiet *M9200*.</span><span class="sxs-lookup"><span data-stu-id="8878e-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="8878e-173">Laukā **Daudzums** ievadiet *1*.</span><span class="sxs-lookup"><span data-stu-id="8878e-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="8878e-174">**5. rinda:** laukā **Krājuma numurs**, atlasiet *M9200*.</span><span class="sxs-lookup"><span data-stu-id="8878e-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="8878e-175">Laukā **Daudzums** ievadiet *3*.</span><span class="sxs-lookup"><span data-stu-id="8878e-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="8878e-176">**6. rinda:** laukā **Krājuma numurs**, atlasiet *M9202*.</span><span class="sxs-lookup"><span data-stu-id="8878e-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="8878e-177">Laukā **Daudzums** ievadiet *7*.</span><span class="sxs-lookup"><span data-stu-id="8878e-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="8878e-178">Šeit ir kopsavilkums par kopējiem daudzumiem katram krājumam:</span><span class="sxs-lookup"><span data-stu-id="8878e-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="8878e-179">**Krājums M9200:** *7* katram</span><span class="sxs-lookup"><span data-stu-id="8878e-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="8878e-180">**Krājums M9201:** *3* katram</span><span class="sxs-lookup"><span data-stu-id="8878e-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="8878e-181">**Krājums M9202:** *9* katram</span><span class="sxs-lookup"><span data-stu-id="8878e-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="8878e-182">Pirms pasūtījumu izdošanas noliktavā jāpārliecinās, vai savākšanas vietās ir pietiekami daudz krājumu visām precēm visos pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="8878e-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="8878e-183">Pārskatiet **Atrašanās vietas direktīvas** iestatījumu, lai noteiktu, kuras izdošanas vietas tiek izmantotas pārdošanas pasūtījuma izdošanai.</span><span class="sxs-lookup"><span data-stu-id="8878e-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="8878e-184">Ja izmantojat Contoso demonstrācijas datu vidi *51.* noliktavai, apstipriniet, ka ir pieejami krājumi.</span><span class="sxs-lookup"><span data-stu-id="8878e-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="8878e-185">Tagad krājums ir jārezervē katrai rindai.</span><span class="sxs-lookup"><span data-stu-id="8878e-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="8878e-186">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet vienu no rezervējamajām rindām.</span><span class="sxs-lookup"><span data-stu-id="8878e-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="8878e-187">Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="8878e-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="8878e-188">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="8878e-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="8878e-189">Tad aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="8878e-189">Then close the page.</span></span>
1. <span data-ttu-id="8878e-190">Atlikušajām rindām, kas ir jārezervē, atkārtojiet 8. - 10. soli.</span><span class="sxs-lookup"><span data-stu-id="8878e-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="8878e-191">Atlasiet pārdošanas pasūtījumu, kuru tikko izlaidāt noliktavā.</span><span class="sxs-lookup"><span data-stu-id="8878e-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="8878e-192">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="8878e-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="8878e-193">Jūs saņemat ziņojumu, ka sūtījums un kopums ir izveidoti un ka kopums ir iesniegts palaišanai partijā.</span><span class="sxs-lookup"><span data-stu-id="8878e-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="8878e-194">Kad kopums un visi lejupstraumes darbi ir pabeigti, darbam ar sešām rindām tiek izveidots darba ID.</span><span class="sxs-lookup"><span data-stu-id="8878e-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="8878e-195">Rindas tiek kārtotas pēc krājuma koda.</span><span class="sxs-lookup"><span data-stu-id="8878e-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="8878e-196">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Visi darbi**, lai skatītu izveidoto darbu.</span><span class="sxs-lookup"><span data-stu-id="8878e-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="8878e-197">Atzīmējiet **Noslodzes ID** vērtību, lai to varētu izmantot nākamajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="8878e-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="8878e-198">Sākt izdošanu no mobilās ierīces</span><span class="sxs-lookup"><span data-stu-id="8878e-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="8878e-199">Piesakieties mobilajā ierīcē kā lietotājs, kurš ir iestatīts noliktavai *51*.</span><span class="sxs-lookup"><span data-stu-id="8878e-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="8878e-200">Mobilajā ierīcē atlasiet izvēlni, kurā ir iekļauts jaunais mobilās ierīces izvēlnes vienums.</span><span class="sxs-lookup"><span data-stu-id="8878e-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="8878e-201">Šim scenārijam atlasiet **Izejošie**.</span><span class="sxs-lookup"><span data-stu-id="8878e-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="8878e-202">Atlasiet izvēlnes vienumu **Pārdošanas grupas rindas izdošana** un iniciējiet izdošanu.</span><span class="sxs-lookup"><span data-stu-id="8878e-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="8878e-203">Ievadiet **Darba ID** vērtību, par kuru izdarījāt piezīmi iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="8878e-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="8878e-204">Vajadzētu redzēt izdošanas soli, kur visas krājuma *M9200* izdošanas rindas ir grupētas, un jums jāsaņem instrukcija izdot katrus *7* no *M9200* krājumiem.</span><span class="sxs-lookup"><span data-stu-id="8878e-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8878e-205">Mobilajā ierīcē izdošanas darbs trīs izdošanas darba rindām ir apkopots lietotāja vienā izdošanas solī.</span><span class="sxs-lookup"><span data-stu-id="8878e-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="8878e-206">Apstipriniet izdošanas darbību.</span><span class="sxs-lookup"><span data-stu-id="8878e-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="8878e-207">Pārejiet uz darba procesa klienta ekrānu un ievērojiet, ka visas trīs savākšanas rindas krājumam *M9200* tika slēgtas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="8878e-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="8878e-208">Atgriezieties mobilajā ierīcē un turpiniet izdot.</span><span class="sxs-lookup"><span data-stu-id="8878e-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="8878e-209">Ir jānorāda krājuma *M9201* 4. darba rinda.</span><span class="sxs-lookup"><span data-stu-id="8878e-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="8878e-210">Pasūtījumā bija tikai viena darba rinda, tāpēc nav ko uzkrāt.</span><span class="sxs-lookup"><span data-stu-id="8878e-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="8878e-211">Apstipriniet izdošanas darbību.</span><span class="sxs-lookup"><span data-stu-id="8878e-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="8878e-212">Pēdējā izdošanas darbība mobilajā ierīcē apkopo pēdējās divas izdošanas rindas no darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="8878e-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="8878e-213">Pabeidziet izdošanas darbību pa *9* no katra krājuma *M9202*.</span><span class="sxs-lookup"><span data-stu-id="8878e-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="8878e-214">Apstipriniet nolikšanas darbību un visus papildu izdošanas/nolikšanas pārus, lai pabeigtu darbu.</span><span class="sxs-lookup"><span data-stu-id="8878e-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="8878e-215">Darba rindas var grupēt tikai tad, ja tās ir secīgas.</span><span class="sxs-lookup"><span data-stu-id="8878e-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="8878e-216">Šī funkcionalitāte netiek atbalstīta:</span><span class="sxs-lookup"><span data-stu-id="8878e-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="8878e-217">Pieļaujamā svara krājumi</span><span class="sxs-lookup"><span data-stu-id="8878e-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="8878e-218">Ja darbā ir kādi pieļaujamā svara krājumi, jūs pirms izdošanas uzsākšanas saņemsit kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="8878e-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="8878e-219">Vienību izdošana</span><span class="sxs-lookup"><span data-stu-id="8878e-219">Piece picking</span></span>
>   - <span data-ttu-id="8878e-220">Darba rindas, kurām ir nepabeigti papildināšanas darbi</span><span class="sxs-lookup"><span data-stu-id="8878e-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="8878e-221">Pārizidošana</span><span class="sxs-lookup"><span data-stu-id="8878e-221">Over-picking</span></span>
>   - <span data-ttu-id="8878e-222">Saīsināta izdošana ar krājuma atkārtotu sadali</span><span class="sxs-lookup"><span data-stu-id="8878e-222">Short picking with item reallocation</span></span>
