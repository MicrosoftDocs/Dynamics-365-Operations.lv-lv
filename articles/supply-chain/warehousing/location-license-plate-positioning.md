---
title: Novietojuma noliktavas vienības pozīcija
description: Noliktavas vienības novietojuma pozīcija ļauj skatīt, kur noliktavas vienība atrodas vairākpalešu novietojumā, piemēram, vietā, kur izmanto dubultdziļus palešu plauktus.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6810753c10d03999c38a6163687effd771076c15
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530056"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="e1bb9-103">Novietojuma noliktavas vienības pozīcija</span><span class="sxs-lookup"><span data-stu-id="e1bb9-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1bb9-104">Noliktavas vienības novietojuma pozīcija ļauj skatīt, kur noliktavas vienība atrodas vairākpalešu novietojumā, piemēram, vietā, kur izmanto dubultdziļus palešu plauktus.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="e1bb9-105">Līdzeklis pievieno secības numuru katrai noliktavas vienībai, kas tiek ievietota glabāšanas vietā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="e1bb9-106">Secības numurs tiek izmantots, lai sakārtotu noliktavas vienības glabāšanas vietā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="e1bb9-107">Tāpēc šis līdzeklis pārdomāti atbalsta scenārijus, kuros klienti izmanto gravitācijas plauktu sistēmu, kā arī izdošanas nolūkos tiem ir jāzina, kura noliktavas vienība ir priekšējā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="e1bb9-108">Šī tēma iepazīstina ar scenāriju, kas parāda, kā iestatīt un izmantot līdzekli.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="e1bb9-109">Novietojuma noliktavas vienības pozīcijas līdzekļa ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="e1bb9-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="e1bb9-110">Lai varētu izmantot noliktavas vienības novietojuma pozīciju, līdzeklim ir jābūt iespējotam sistēmā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="e1bb9-111">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e1bb9-112">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e1bb9-113">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e1bb9-114">**Līdzekļa nosaukums:** *Novietojuma noliktavas vienības pozīcija*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e1bb9-115">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="e1bb9-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="e1bb9-116">Padarīt pieejamus datu paraugus</span><span class="sxs-lookup"><span data-stu-id="e1bb9-116">Make sample data available</span></span>

<span data-ttu-id="e1bb9-117">Lai strādātu ar šo scenāriju, izmantojot šeit piedāvātās vērtības, ir jāstrādā ar sistēmu, kurā ir instalēti datu paraugi.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="e1bb9-118">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="e1bb9-119">Iestatīt līdzekli šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="e1bb9-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="e1bb9-120">Izpildiet šādas procedūras, lai iestatītu līdzekli *Novietojuma noliktavas vienības pozīcija* scenārijam šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="e1bb9-121">Atrašanās vietu profili</span><span class="sxs-lookup"><span data-stu-id="e1bb9-121">Location profiles</span></span>

<span data-ttu-id="e1bb9-122">Līdzeklim ir jābūt iespējotam novietojuma profilā katrai atrašanās vietai, kurā tas tiks izmantots.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="e1bb9-123">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="e1bb9-124">Novietojuma profilu saraksta kreisajā rūtī atlasiet **LIELAPJOMA-06**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="e1bb9-125">Kopsavilkuma cilnē **Vispārīgi** līdzeklis ir pievienojis divas jaunas opcijas.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="e1bb9-126">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-126">Set the following values:</span></span>

    - <span data-ttu-id="e1bb9-127">**Iespējot noliktavas vienības pozīciju:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="e1bb9-128">Kad šī opcija ir iestatīta uz *Jā*, noliktavas vienības pozīcija tiek uzturēta noliktavas vienībām šajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="e1bb9-129">**Rādīt mobilās ierīces LP pozīciju:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="e1bb9-130">Kad šī opcija ir iestatīta uz *Jā*, noliktavas vienības pozīcija tiek rādīta mobilās ierīces lietotājiem korekcijas un inventarizācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="e1bb9-131">Opcijas iestatījumu var mainīt tikai tad, kad līdzeklis ir ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="e1bb9-132">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="e1bb9-133">Vietas direktīvas</span><span class="sxs-lookup"><span data-stu-id="e1bb9-133">Location directives</span></span>

1. <span data-ttu-id="e1bb9-134">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="e1bb9-135">Kreisajā rūtī pārliecinieties, ka lauks **Darba pasūtījuma veids** ir iestatīts uz *Pārdošanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="e1bb9-136">Novietojuma direktīvu sarakstā atlasiet **61 SO izdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="e1bb9-137">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e1bb9-138">Kopsavilkuma cilnē **Rindas** atlasiet rindu ar **Secības numura** vērtību *2*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="e1bb9-139">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet rindu ar **Nosaukums** vērtību *Izdot mazāk par paleti* (tai ir jābūt vienīgajai rindai), un mainiet tās **Secības numura** vērtību uz *2*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="e1bb9-140">Virs režģa atlasiet **Jauns**, lai jaunai novietojuma direktīvas darbībai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="e1bb9-141">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1bb9-142">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="e1bb9-143">**Nosaukums:** *Izdošanas pozīcija 1*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="e1bb9-144">Turpinot atlasīt jaunāko rindu, atlasiet **Rediģēt vaicājumu** virs režģa.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="e1bb9-145">Vaicājumu redaktorā atlasiet cilni **Savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="e1bb9-146">Izvērsiet **Novietojumi** tabulas savienojumu, lai parādītu savienojumu ar **Krājumu dimensijas** tabulu.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="e1bb9-147">Izvērsiet **Krājumu dimensijas** tabulas savienojumu, lai parādītu savienojumu ar **Rīcībā esošie krājumi** tabulu.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="e1bb9-148">Atlasiet **Krājumu dimensijas** un pēc tam atlasiet **Pievienot tabulas savienojumu**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="e1bb9-149">Tabulu sarakstā, kas tiek parādīts kolonnā **Relācija**, atlasiet **Noliktavas vienība (Noliktavas vienība)**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="e1bb9-150">Pēc tam atlasiet **Atlasīt**, lai pievienotu **Noliktavas vienību** tabulas savienojumam **Krājumu dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="e1bb9-151">Kamēr **Noliktavas vienība** joprojām ir atlasīta, atlasiet **Pievienot tabulas savienojumu**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="e1bb9-152">Tabulu sarakstā, kas tiek parādīts kolonnā **Relācija**, atlasiet **Novietojuma noliktavas vienības pozīcija (Noliktavas vienība)**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="e1bb9-153">Pēc tam atlasiet **Atlasīt**, lai pievienotu **Novietojuma noliktavas vienības pozīcija** tabulas savienojumam **Krājumu dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="e1bb9-154">![Tabulas savienojums](media/LpTableJoin.png "Tabulas savienojums")</span><span class="sxs-lookup"><span data-stu-id="e1bb9-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="e1bb9-155">Atlasiet **Labi**, lai apstiprinātu atjauninātās savienotās tabulas un aizvērtu vaicājumu redaktoru.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="e1bb9-156">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** vēlreiz atlasiet **Rediģēt vaicājumu**, lai atkārtoti atvērtu vaicājumu redaktoru.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="e1bb9-157">Cilnē **Diapazons** atlasiet **Pievienot**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="e1bb9-158">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e1bb9-159">**Tabula:** *Novietojuma noliktavas vienības pozīcija*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="e1bb9-160">**Atveidotā tabula:** *Novietojuma noliktavas vienības pozīcija*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="e1bb9-161">**Lauks:** *LP pozīcija*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="e1bb9-162">**Kritēriji:** *1*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="e1bb9-163">![Jauns diapazons](media/LpPositionCriteria.png "Jauns diapazons")</span><span class="sxs-lookup"><span data-stu-id="e1bb9-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="e1bb9-164">Atlasiet **Labi**, lai apstiprinātu izmaiņas un aizvērtu vaicājumu redaktoru.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="e1bb9-165">Iestatīt datu paraugus šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="e1bb9-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="e1bb9-166">Scenārijā lietotājam ir jāpiesakās noliktavas mobilajā programmā, izmantojot darbinieku, kurš ir iestatīts veikt darbu *61* noliktavā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="e1bb9-167">Lietotājam ir jāveic arī darbības.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-167">The user must also complete transactions.</span></span>

<span data-ttu-id="e1bb9-168">Tā kā līdzeklis *Novietojuma noliktavas vienības pozīcija* pievieno jaunu identifikatoru noliktavas vienības pozīcijām, tad vispirms ir jāizveido daži dati, lai atbalstītu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="e1bb9-169">Pirmās atrašanās vietas inventarizācija</span><span class="sxs-lookup"><span data-stu-id="e1bb9-169">Spot-count the first location</span></span>

1. <span data-ttu-id="e1bb9-170">Atveriet noliktavas mobilo programmu un piesakieties noliktavā *61*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="e1bb9-171">Doties uz **Krājumi \> Inventarizācija uz vietas**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="e1bb9-172">Lapā **Inventarizācija uz vietas** iestatiet lauku **Atrašanās vieta** uz *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="e1bb9-173">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-173">Select **OK**.</span></span>

    <span data-ttu-id="e1bb9-174">Lapā tiek parādītas jūsu ievadītās atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-174">The page shows the location that you entered.</span></span> <span data-ttu-id="e1bb9-175">Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”</span><span class="sxs-lookup"><span data-stu-id="e1bb9-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="e1bb9-176">Atlasiet **Atsvaidzināt**, lai atrašanās vietai pievienotu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="e1bb9-177">Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu**, atlasiet lauku **Krājums** un pēc tam ievadiet vērtību *A0001*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="e1bb9-178">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-178">Select **OK**.</span></span>
1. <span data-ttu-id="e1bb9-179">Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu**, atlasiet lauku **LP** un pēc tam ievadiet vērtību *LP1001* (vai citu unikālu noliktavas vienības identifikatoru pēc savas izvēles).</span><span class="sxs-lookup"><span data-stu-id="e1bb9-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="e1bb9-180">Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu** parādīta **1. noliktavas vienības pozīcija**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="e1bb9-181">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-181">Select **OK**.</span></span>

    <span data-ttu-id="e1bb9-182">Norādiet krājuma daudzumu, kas tika uzskaitīts noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="e1bb9-183">Iestatiet lauku **Daudz.** uz *10*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="e1bb9-184">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-184">Select **OK**.</span></span>

    <span data-ttu-id="e1bb9-185">Lapā tiek parādītas jūsu ievadītās atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-185">The page shows the location that you entered.</span></span> <span data-ttu-id="e1bb9-186">Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”</span><span class="sxs-lookup"><span data-stu-id="e1bb9-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="e1bb9-187">Atlasiet **Atsvaidzināt**, lai atrašanās vietai pievienotu citu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="e1bb9-188">Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu**, atlasiet lauku **Krājums** un pēc tam ievadiet vērtību *A0002*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="e1bb9-189">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-189">Select **OK**.</span></span>
1. <span data-ttu-id="e1bb9-190">Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu** atlasiet lauku **LP** un pēc tam ievadiet vērtību *LP1002* (vai citu unikālu noliktavas vienības identifikatoru pēc savas izvēles, nodrošinot, ka tas atšķiras no iepriekš norādītā).</span><span class="sxs-lookup"><span data-stu-id="e1bb9-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="e1bb9-191">Mainiet noliktavas vienības pozīciju, iestatot lauku **LP pozīcija** uz *2*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="e1bb9-192">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-192">Select **OK**.</span></span>
1. <span data-ttu-id="e1bb9-193">Norādiet krājuma daudzumu, kas tika uzskaitīts noliktavas vienībai, iestatot lauku **Daudz.** uz *10*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="e1bb9-194">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-194">Select **OK**.</span></span>

    <span data-ttu-id="e1bb9-195">Lapā tiek parādītas jūsu ievadītās atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-195">The page shows the location that you entered.</span></span> <span data-ttu-id="e1bb9-196">Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”</span><span class="sxs-lookup"><span data-stu-id="e1bb9-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="e1bb9-197">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-197">Select **OK**.</span></span>

<span data-ttu-id="e1bb9-198">Darbs tagad ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="e1bb9-199">Otrās atrašanās vietas inventarizācija</span><span class="sxs-lookup"><span data-stu-id="e1bb9-199">Spot-count the second location</span></span>

1. <span data-ttu-id="e1bb9-200">Lapā **Inventarizācija uz vietas** iestatiet lauku **Atrašanās vieta** uz *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="e1bb9-201">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-201">Select **OK**.</span></span>

    <span data-ttu-id="e1bb9-202">Lapā tiek parādītas jūsu ievadītās atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-202">The page shows the location that you entered.</span></span> <span data-ttu-id="e1bb9-203">Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”</span><span class="sxs-lookup"><span data-stu-id="e1bb9-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="e1bb9-204">Atlasiet **Atsvaidzināt**, lai atrašanās vietai pievienotu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="e1bb9-205">Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu**, atlasiet lauku **Krājums** un pēc tam ievadiet vērtību *A0002*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="e1bb9-206">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-206">Select **OK**.</span></span>
1. <span data-ttu-id="e1bb9-207">Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu** atlasiet lauku **LP** un pēc tam ievadiet vērtību *LP1003* (vai citu unikālu noliktavas vienības identifikatoru pēc savas izvēles, nodrošinot, ka tas atšķiras no abiem iepriekšējā procedūrā norādītajiem).</span><span class="sxs-lookup"><span data-stu-id="e1bb9-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="e1bb9-208">Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu** parādīta **1. noliktavas vienības pozīcija**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="e1bb9-209">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-209">Select **OK**.</span></span>
1. <span data-ttu-id="e1bb9-210">Norādiet krājuma daudzumu, kas tika uzskaitīts noliktavas vienībai, iestatot lauku **Daudz.** uz *10*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="e1bb9-211">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-211">Select **OK**.</span></span>

    <span data-ttu-id="e1bb9-212">Lapā tiek parādītas jūsu ievadītās atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-212">The page shows the location that you entered.</span></span> <span data-ttu-id="e1bb9-213">Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”</span><span class="sxs-lookup"><span data-stu-id="e1bb9-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="e1bb9-214">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-214">Select **OK**.</span></span>

<span data-ttu-id="e1bb9-215">Darbs tagad ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="e1bb9-216">Detalizēta informācija par darbu</span><span class="sxs-lookup"><span data-stu-id="e1bb9-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="e1bb9-217">Inventarizācijas uz vietas no mobilās programmas veido cikla inventarizācijas darbu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="e1bb9-218">Darbam nepieciešams, lai inventarizācijas tiktu akceptētas, pirms tās tiek iegrāmatotas krājumos.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="e1bb9-219">Pierakstieties programmā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="e1bb9-220">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="e1bb9-221">Cilnē **Pārskats** meklējiet rindas ar šādām vērtībām:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="e1bb9-222">**Darba pasūtījuma veids:** *Cikla inventarizācija*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="e1bb9-223">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="e1bb9-224">**Darba statuss:** *Gaida pārskatīšanu*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="e1bb9-225">Šīm rindām ir jāizveido divi darba ID.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="e1bb9-226">Abām darba ID uzskaitēm ir jābūt pieņemtām.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="e1bb9-227">Režģī atlasiet pirmo darba ID *Cikla inventarizācija* darba pasūtījuma tipam.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="e1bb9-228">Darbību rūts cilnē **Darbs** grupā **Darbs** atlasiet **Cikla inventarizācija**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="e1bb9-229">Tiek rādītas divas rindas, pa vienai katrai krājuma un noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="e1bb9-230">Vērtībām **Inventarizācijas daudzums** laukos **Atrašanās vieta**, **Noliktavas vienība** un **Krājums** ir jāatbilst mobilajā ierīcē izveidotajiem uzskaites ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="e1bb9-231">Ja kāds no šiem laukiem nav redzams, darbību rūtī atlasiet **Parādīt dimensijas**, lai tās pievienotu režģim.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="e1bb9-232">Atlasiet abas rindas.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-232">Select both lines.</span></span>
1. <span data-ttu-id="e1bb9-233">Darbību rūtī atlasiet **Pieņemt uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="e1bb9-234">Tiek saņemts ziņojums “Grāmatošana – žurnāls”.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="e1bb9-235">Atlasiet **Ziņojuma informācija**, lai apskatītu grāmatotā žurnāla numuru.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="e1bb9-236">Aizveriet ziņojuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-236">Close the message details.</span></span>
1. <span data-ttu-id="e1bb9-237">Atsvaidziniet lapu **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="e1bb9-238">Pirmais darba ID ir aizvērts un vairs netiek rādīts.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="e1bb9-239">Lai skatītu slēgto darbu, atzīmējiet izvēles rūtiņu **Rādīt slēgto**, kas atrodas virs režģa.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="e1bb9-240">Tiek pieņemts darbs noliktavas vienībai *01A01R1S2B* vietā.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="e1bb9-241">Cilnē **Pārskats**, atlasiet otru darba ID darba pasūtījuma veidam *Cikla inventarizācija*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="e1bb9-242">Darbību rūts cilnē **Darbs** grupā **Darbs** atlasiet **Cikla inventarizācija**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="e1bb9-243">Tiek rādīta viena rinda krājumam un noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="e1bb9-244">Vērtībām **Inventarizācijas daudzums** laukos **Atrašanās vieta**, **Noliktavas vienība** un **Krājums** ir jāatbilst mobilajā ierīcē izveidotajiem uzskaites ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="e1bb9-245">Atlasiet rindu.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-245">Select the line.</span></span>
1. <span data-ttu-id="e1bb9-246">Darbību rūtī atlasiet **Pieņemt uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="e1bb9-247">Tiek saņemts ziņojums “Grāmatošana – žurnāls”.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="e1bb9-248">Atlasiet **Ziņojuma informācija**, lai apskatītu grāmatotā žurnāla numuru.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="e1bb9-249">Aizveriet ziņojuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-249">Close the message details.</span></span>
1. <span data-ttu-id="e1bb9-250">Atsvaidziniet lapu **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="e1bb9-251">Otrais darba ID ir aizvērts un vairs netiek rādīts.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="e1bb9-252">Lai skatītu slēgto darbu, atzīmējiet izvēles rūtiņu **Rādīt slēgto**, kas atrodas virs režģa.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="e1bb9-253">Rīcībā esošie krājumi pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="e1bb9-253">On-hand by location</span></span>

1. <span data-ttu-id="e1bb9-254">Dodieties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Rīcībā esošie krājumi pēc atrašanās vietas**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="e1bb9-255">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-255">Set the following values:</span></span>

    - <span data-ttu-id="e1bb9-256">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-256">**Site:** *6*</span></span>
    - <span data-ttu-id="e1bb9-257">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="e1bb9-258">**Atsvaidzināt vairākās atrašanās vietās:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="e1bb9-259">Ievērojiet, ka novietojumam *01A01R1S1B* ir divas noliktavas vienības:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="e1bb9-260">**A0001**, kur lauks **LP pozīcija** ir iestatīts uz *1*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="e1bb9-261">**A0002**, kur lauks **LP pozīcija** ir iestatīts uz *2*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="e1bb9-262">Ievērojiet, ka novietojumam *01A01R1S2B* ir viena noliktavas vienība:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="e1bb9-263">**A0002**, kur lauks **LP pozīcija** ir iestatīts uz *1*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="e1bb9-264">Pārdošanas pasūtījuma scenārijs</span><span class="sxs-lookup"><span data-stu-id="e1bb9-264">Sales order scenario</span></span>

<span data-ttu-id="e1bb9-265">Tagad, kad ir iestatīts līdzeklis *Novietojuma noliktavas vienības pozīcija* un krājumi ir nodrošināti, ir jāizveido pārdošanas pasūtījums, lai ģenerētu izdošanas darbu, kas novirzīs noliktavas darbinieku izdot krājumu *A0002* no krājumu novietojuma, kur paletes ID ir pozīcijā *1*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="e1bb9-266">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e1bb9-267">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e1bb9-268">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e1bb9-269">**Debitora konts:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="e1bb9-270">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="e1bb9-271">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-271">Select **OK**.</span></span>
1. <span data-ttu-id="e1bb9-272">Kopsavilkuma cilnes režģim **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="e1bb9-273">Šajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e1bb9-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="e1bb9-274">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="e1bb9-275">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="e1bb9-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="e1bb9-276">Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e1bb9-277">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="e1bb9-278">Aizveriet lapu **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="e1bb9-279">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e1bb9-280">Tiek saņemts informatīvs ziņojums, norādot pasūtījumam izveidoto kopuma ID un sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="e1bb9-281">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Noliktava** virs režģa, atlasiet **Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="e1bb9-282">Tiek parādīta lapa **Darbs**, un tā parāda darbu, kas tika izveidots pārdošanas rindai.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="e1bb9-283">Pierakstiet parādīto darba ID.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="e1bb9-284">Pārdošanas izdošanas scenārijs</span><span class="sxs-lookup"><span data-stu-id="e1bb9-284">Sales picking scenario</span></span>

1. <span data-ttu-id="e1bb9-285">Atveriet mobilo programmu un piesakieties noliktavā *61*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="e1bb9-286">Doties uz **Izejošs \> Pārdošanas izdošana**.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="e1bb9-287">Lapā **Skenēt darba ID / noliktavas vienības ID** atlasiet lauku **ID** un pēc tam ievadiet darba ID no pārdošanas rindas.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="e1bb9-288">Ņemiet vērā, ka izdošanas darbs jūs novirza izdot krājumu *A0002* no atrašanās vietas *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="e1bb9-289">Šī instrukcija tiek saņemta, jo krājums *A0002* atrodas noliktavas vienībā, kas ir novietojuma pozīcijā *1*.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="e1bb9-290">![1. pozīcijas novietojums](media/LocationLicensePlatePositioning.png "1. pozīcijas novietojums")</span><span class="sxs-lookup"><span data-stu-id="e1bb9-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="e1bb9-291">Ievadiet novietojuma izveidoto noliktavas vienības ID un pēc tam sekojiet uzvednēm, lai izdotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e1bb9-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>