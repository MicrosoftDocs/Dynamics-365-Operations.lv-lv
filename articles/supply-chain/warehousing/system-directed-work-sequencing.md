---
title: Sistēmas noteikta darbu secība
description: Šajā tēmā ir sniegta informācija par sistēmas noteiktu darbu secību. Šī funkcija sniedz iespēju kārtot un filtrēt darba pasūtījumus, kurus sistēma sniedz lietotājiem izpildei. Tas noder scenārijos, kad ir nepieciešami papildu kritēriji, lai virzītu noliktavas izdošanas procesu.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7db884a5cd62e1f44a2a86316fde6bf2d11a3376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239138"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="2a685-105">Sistēmas noteikta darbu secība</span><span class="sxs-lookup"><span data-stu-id="2a685-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a685-106">Sistēmas noteikta darbu secība ļauj kārtot un filtrēt darba pasūtījumus, kurus sistēma piedāvā lietotājiem izpildei.</span><span class="sxs-lookup"><span data-stu-id="2a685-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="2a685-107">Tas noder scenārijos, kad ir nepieciešami papildu kritēriji (piemēram, nosūtīšanas laiks, izdošanas zona, vietas profils vai dažādu kritēriju kombinācija), lai virzītu noliktavas izdošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="2a685-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="2a685-108">Šī funkcionalitāte paplašina pašreizējo sistēmas virzīto izdošanas funkcionalitāti, pievienojot sistēmas virzītu vaicājumu secību, kur lietotāji var iestatīt secību un vienu vai vairākus vaicājumus, kas novērtēs visus izveidotos darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="2a685-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="2a685-109">Tiks saglabāti un parādīti tikai tie darba pasūtījumi, kas atbilst mobilās ierīces izvēlnes vienuma iestatīšanā norādītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="2a685-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="2a685-110">Tāpēc šī funkcionalitāte ļauj veikt tālāku noliktavas izdošanas procesu optimizāciju, jo tajā tiek identificēti darba pasūtījumi, kas atbilst norādītajiem kritērijiem, tie tiek piešķirti pareizajam mobilās ierīces izvēlnes vienumam un pēc tam parādīti darbiniekam, pamatojoties uz noteiktu prasmju kopu, izdošanas aprīkojumu vai citām prasībām.</span><span class="sxs-lookup"><span data-stu-id="2a685-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="2a685-111">Ja ir nepieciešami atšķirīgi kritēriji, ir jāizmanto vairāki mobilās ierīces izvēlnes vienumi.</span><span class="sxs-lookup"><span data-stu-id="2a685-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="2a685-112">Ieslēdziet līdzekli Organizācijas līmeņa sistēmas noteikta darba secība</span><span class="sxs-lookup"><span data-stu-id="2a685-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="2a685-113">Lai varētu izmantot līdzekli Sistēmas noteikta darba secība, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="2a685-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="2a685-114">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="2a685-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2a685-115">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="2a685-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2a685-116">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="2a685-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2a685-117">**Līdzekļa nosaukums:** *Organizācijas līmeņa sistēmas noteikta darba secība*</span><span class="sxs-lookup"><span data-stu-id="2a685-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="2a685-118">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="2a685-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="2a685-119">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="2a685-119">Make demo data available</span></span>

<span data-ttu-id="2a685-120">Lai strādātu ar scenāriju, izmantojot šajā tēmā norādītās vērtības, ir jāstrādā ar sistēmu, kurā ir instalēti standarta demonstrācijas dati.</span><span class="sxs-lookup"><span data-stu-id="2a685-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="2a685-121">Turklāt ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="2a685-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="2a685-122">Scenārijā tiek izmantota noliktava nr. *51* no demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="2a685-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a685-123">Pirms pasūtījumu izdošanas noliktavā pārliecinieties, vai izdošanas vietās ir pietiekami daudz krājumu visām precēm pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="2a685-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="2a685-124">Noklusējuma USMF datiem ir jāatbalsta šis scenārijs.</span><span class="sxs-lookup"><span data-stu-id="2a685-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="2a685-125">Ja neizmantojat demonstrācijas datus, pārskatiet **Novietojuma direktīvas** iestatījumu, lai uzzinātu, kuras izdošanas vietas tiek izmantotas pārdošanas pasūtījuma izdošanai.</span><span class="sxs-lookup"><span data-stu-id="2a685-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="2a685-126">Pielāgojot krājumus, varat izveidot manuālo kustību, izmantot papildināšanu vai jebkuru citu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="2a685-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="2a685-127">Mobilās ierīces izvēlnes vienuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="2a685-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="2a685-128">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="2a685-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2a685-129">Mobilās ierīces izvēlnes vienumu sarakstā atlasiet **Pārdošanas izdošana — Sistēma**.</span><span class="sxs-lookup"><span data-stu-id="2a685-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="2a685-130">Nepieciešamajam izvēlnes vienumam jau vajadzētu pastāvēt.</span><span class="sxs-lookup"><span data-stu-id="2a685-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="2a685-131">Apstipriniet tālāk minētos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="2a685-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="2a685-132">**Vispārīgās** kopsavilkuma cilnes laukā **Noteica:** ir jāiestata vērtība *Sistēmas noteikts*.</span><span class="sxs-lookup"><span data-stu-id="2a685-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="2a685-133">Kopsavilkuma cilnē **Darba klases** vajadzētu būt redzamiem tālāk norādītajiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="2a685-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="2a685-134">Darba klases ID</span><span class="sxs-lookup"><span data-stu-id="2a685-134">Work class ID</span></span> | <span data-ttu-id="2a685-135">Darba pasūtījuma veids</span><span class="sxs-lookup"><span data-stu-id="2a685-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="2a685-136">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="2a685-136">Sales</span></span> | <span data-ttu-id="2a685-137">Pārdošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="2a685-137">Sales orders</span></span> |
        | <span data-ttu-id="2a685-138">Pārdošanas pasūtījuma izdošana</span><span class="sxs-lookup"><span data-stu-id="2a685-138">SO Pick</span></span> | <span data-ttu-id="2a685-139">Pārdošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="2a685-139">Sales orders</span></span> |

1. <span data-ttu-id="2a685-140">Darbības rūtī atlasiet **Sistēmas noteikti darba secības vaicājumi**.</span><span class="sxs-lookup"><span data-stu-id="2a685-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="2a685-141">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="2a685-141">Select **Edit**.</span></span>
1. <span data-ttu-id="2a685-142">Izdzēsiet esošo rindu un pēc tam atlasiet **Jā**, lai apstiprinātu darbību.</span><span class="sxs-lookup"><span data-stu-id="2a685-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="2a685-143">Lai izveidotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2a685-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="2a685-144">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2a685-145">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="2a685-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2a685-146">**Apraksta lauks:** *Darba daudzums mazāks par 20 un dilstošs*</span><span class="sxs-lookup"><span data-stu-id="2a685-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="2a685-147">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2a685-147">Select **Save**.</span></span>
1. <span data-ttu-id="2a685-148">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="2a685-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="2a685-149">Cilnē **Savienojumi** izvērsiet savienojumu hierarhiju, lai parādītu tabulu **Darba rindas**.</span><span class="sxs-lookup"><span data-stu-id="2a685-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="2a685-150">Atlasiet tabulu savienojumu **Darba rindas**.</span><span class="sxs-lookup"><span data-stu-id="2a685-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="2a685-151">Atlasiet **Pievienot tabulu savienojumu**.</span><span class="sxs-lookup"><span data-stu-id="2a685-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="2a685-152">Tiks parādīts saraksts. Tajā atrodiet un atlasiet rindu, kurai ir tālāk norādītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="2a685-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="2a685-153">**Savienojuma režīms:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="2a685-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="2a685-154">**Relācija:** *vietas (vieta)*</span><span class="sxs-lookup"><span data-stu-id="2a685-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="2a685-155">Atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="2a685-155">Select **Select**.</span></span>

    <span data-ttu-id="2a685-156">Vietas ir pievienotas savienojumu tabulai.</span><span class="sxs-lookup"><span data-stu-id="2a685-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="2a685-157">Cilnē **Kārtošana** atlasiet **Pievienot**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="2a685-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="2a685-158">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2a685-159">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="2a685-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="2a685-160">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="2a685-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="2a685-161">**Lauks:** *Darba daudzums* (paradītajā ziņojumu lodziņā atlasiet **Jā**, lai šim laukam pievienotu kārtošanu.)</span><span class="sxs-lookup"><span data-stu-id="2a685-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="2a685-162">**Meklēšanas virziens:** *Dilstošā secībā*</span><span class="sxs-lookup"><span data-stu-id="2a685-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="2a685-163">Atlasiet cilni **Diapazons**.</span><span class="sxs-lookup"><span data-stu-id="2a685-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="2a685-164">Ja secībā ir jāiekļauj tikai noteikt darba kritēriji, tos varat norādīt cilnē **Diapazons**. Šajā piemērā jūs vēlaties iekļaut tikai to darbu, kur daudzums ir mazāks par 20 ea (viszemākā mērvienība).</span><span class="sxs-lookup"><span data-stu-id="2a685-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="2a685-165">Ņemiet vērā, ka dažas rindas jau ir iekļautas.</span><span class="sxs-lookup"><span data-stu-id="2a685-165">Notice that some lines are already included.</span></span> <span data-ttu-id="2a685-166">Šīs rindas nedrīkst noņemt.</span><span class="sxs-lookup"><span data-stu-id="2a685-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="2a685-167">Lai pievienotu rindu, atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="2a685-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="2a685-168">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2a685-169">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="2a685-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="2a685-170">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="2a685-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="2a685-171">**Lauks:** *Krājumu darba daudzums*</span><span class="sxs-lookup"><span data-stu-id="2a685-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="2a685-172">**Kritēriji:** *\<20* (mazāk par 20)</span><span class="sxs-lookup"><span data-stu-id="2a685-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="2a685-173">Lai pievienotu vēl vienu rindu, atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="2a685-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="2a685-174">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2a685-175">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="2a685-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="2a685-176">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="2a685-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="2a685-177">**Lauks:** *Darba veids*</span><span class="sxs-lookup"><span data-stu-id="2a685-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="2a685-178">**Kritēriji:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="2a685-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="2a685-179">Lai pievienotu vēl vienu rindu, atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="2a685-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="2a685-180">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2a685-181">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="2a685-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="2a685-182">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="2a685-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="2a685-183">**Lauks:** *Atrašanās vietas profila ID*</span><span class="sxs-lookup"><span data-stu-id="2a685-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="2a685-184">**Kritēriji:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="2a685-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="2a685-185">Vienuma *STAGE* priekšā noteikti pievienojiet izsaukuma zīmi (*!*).</span><span class="sxs-lookup"><span data-stu-id="2a685-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="2a685-186">Atlasiet **Labi**, lai saglabātu un aizvērtu vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="2a685-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="2a685-187">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2a685-187">Select **Save**.</span></span>
1. <span data-ttu-id="2a685-188">Aizveriet lapu, lai atgrieztos lapā **Mobilās ierīces izvēles vienumi**.</span><span class="sxs-lookup"><span data-stu-id="2a685-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="2a685-189">Šis iestatījums definē, kādi kritēriji tiks izmantoti, lai mobilās ierīces izvēlnes vienumā ievietotu piemēroto darbu.</span><span class="sxs-lookup"><span data-stu-id="2a685-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="2a685-190">Ja vaicājumam pievienosit vairākas kritēriju rindas, sistēma vispirms izmantos vaicājuma rindu ar viszemāko kārtas numuru.</span><span class="sxs-lookup"><span data-stu-id="2a685-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="2a685-191">Citiem vārdiem sakot, lietotājam vispirms tiks rādīts viss 1. kārtas numuram piemērotais darbs un pēc tam viss 2. kārtas numuram piemērotais darbs.</span><span class="sxs-lookup"><span data-stu-id="2a685-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="2a685-192">Tāpēc, ja kopā ir jāizmanto konkrēts diapazons un kārtošana, tie ir jānorāda tajā pašā sistēmas vadītajā darbu secības vaicājumā.</span><span class="sxs-lookup"><span data-stu-id="2a685-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="2a685-193">Ar šo iestatījumu tiks nolasīts visa veida darbs, kurā ir vismaz viena rinda ar daudzumu, kas mazāks par 20 ea.</span><span class="sxs-lookup"><span data-stu-id="2a685-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="2a685-194">Tāpēc, ja darbā ir rinda, kur daudzums ir precīzi 20 ea vai vairāk nekā 20 ea, tā būs derīga, pieņemot, ka darbā ir arī rinda, kuras daudzums ir mazāks par 20 ea.</span><span class="sxs-lookup"><span data-stu-id="2a685-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="2a685-195">Vietas direktīvas</span><span class="sxs-lookup"><span data-stu-id="2a685-195">Location directives</span></span>

<span data-ttu-id="2a685-196">Ja izmantojat noklusējuma Contoso datus, novietojuma direktīvas darbības vaicājumam nebūs nepieciešamas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="2a685-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="2a685-197">Tomēr, lai būtu drošs, ka novietojuma direktīvas nolasa pārdošanas pasūtījumos ietvertos vienumus, kad lietojat līdzekli vidē, kas nav Contoso, izveidojiet jaunu vietas direktīvu.</span><span class="sxs-lookup"><span data-stu-id="2a685-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="2a685-198">Lai demonstrācijas vidē pārbaudītu iestatījumus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="2a685-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="2a685-199">Dodieties uz **Noliktavas vadība** \> **Iestatīšana** \> **Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="2a685-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="2a685-200">Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="2a685-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="2a685-201">Atlasiet novietojuma direktīvu ar nosaukumu *51. izdošana*.</span><span class="sxs-lookup"><span data-stu-id="2a685-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="2a685-202">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** darbībai **Izdošana** atlasiet jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="2a685-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="2a685-203">Virs režģa atlasiet komandu **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="2a685-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="2a685-204">Pārskatiet vaicājumu **Diapazons**.</span><span class="sxs-lookup"><span data-stu-id="2a685-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="2a685-205">Atrodiet rindu, kurā laukam **Lauks** ir iestatīta vērtība *Novietojums*.</span><span class="sxs-lookup"><span data-stu-id="2a685-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="2a685-206">Pārbaudiet, vai lauks **Kritēriji** ir tukšs (vai tajā nav ierobežojumu).</span><span class="sxs-lookup"><span data-stu-id="2a685-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="2a685-207">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="2a685-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="2a685-208">Izveidojiet pārdošanas pasūtījuma izdošanas darbu</span><span class="sxs-lookup"><span data-stu-id="2a685-208">Create sales order picking work</span></span>

<span data-ttu-id="2a685-209">Pirms sistēmas vadītas izdošanas izpildes ir jāizveido izejošais darbs.</span><span class="sxs-lookup"><span data-stu-id="2a685-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="2a685-210">Šim scenārijam izveidojiet četrus pārdošanas pasūtījumus, kuru pamatā ir norādītie sistēmas vadītās darbu secības vaicājumi.</span><span class="sxs-lookup"><span data-stu-id="2a685-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="2a685-211">Katram pārdošanas pasūtījumam rezervējiet krājumu daudzumus.</span><span class="sxs-lookup"><span data-stu-id="2a685-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="2a685-212">Līdz ar to rezervēto krājumu nevar izņemt no noliktavas citiem pasūtījumiem, ja vien netiek atcelta šī krājuma rezervācija vai daļa no krājuma rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="2a685-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="2a685-213">Pēc tam izlaidiet noliktavā katru pārdošanas pasūtījumu, lai izveidotu izejošo darbu.</span><span class="sxs-lookup"><span data-stu-id="2a685-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="2a685-214">1. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="2a685-214">Sales order 1</span></span>

1. <span data-ttu-id="2a685-215">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="2a685-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2a685-216">Lai izveidotu 1. pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2a685-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="2a685-217">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2a685-218">Sadaļā **Klients** laukam **Klienta konts** iestatiet vērtību *US-004*.</span><span class="sxs-lookup"><span data-stu-id="2a685-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="2a685-219">Sadaļā **Vispārīgi** laukam **Noliktava** iestatiet vērtību *51*.</span><span class="sxs-lookup"><span data-stu-id="2a685-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="2a685-220">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2a685-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="2a685-221">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="2a685-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="2a685-222">Pievienojiet rindu jaunajam pārdošanas pasūtījumam un iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="2a685-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="2a685-223">**Krājuma numurs:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="2a685-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="2a685-224">**Daudzums:** *20*</span><span class="sxs-lookup"><span data-stu-id="2a685-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="2a685-225">Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="2a685-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="2a685-226">Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="2a685-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="2a685-227">Aizveriet lapu **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="2a685-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="2a685-228">Darbību rūts cilnē **Noliktava** atlasiet **Pārvietot uz noliktavu**, lai noliktavai izveidotu darbu.</span><span class="sxs-lookup"><span data-stu-id="2a685-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="2a685-229">Tiks saņemti informatīvi ziņojumi, kuros būs norādīts pārdošanas pasūtījumam izveidotais kopuma ID un sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="2a685-230">2. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="2a685-230">Sales order 2</span></span>

1. <span data-ttu-id="2a685-231">Lai izveidotu 2. pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2a685-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="2a685-232">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2a685-233">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="2a685-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="2a685-234">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="2a685-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2a685-235">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2a685-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="2a685-236">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="2a685-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="2a685-237">Pievienojiet rindu jaunajam pārdošanas pasūtījumam un iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="2a685-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="2a685-238">**Krājuma numurs:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="2a685-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="2a685-239">**Daudzums:** *5*</span><span class="sxs-lookup"><span data-stu-id="2a685-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="2a685-240">Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="2a685-241">**Krājuma numurs:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="2a685-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="2a685-242">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="2a685-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="2a685-243">Rezervējiet krājumus abām rindām.</span><span class="sxs-lookup"><span data-stu-id="2a685-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="2a685-244">Izlaidiet pasūtījumu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="2a685-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="2a685-245">3. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="2a685-245">Sales order 3</span></span>

1. <span data-ttu-id="2a685-246">Lai izveidotu 3. pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2a685-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="2a685-247">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2a685-248">**Debitora konts:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="2a685-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="2a685-249">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="2a685-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2a685-250">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2a685-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="2a685-251">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="2a685-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="2a685-252">Pievienojiet rindu jaunajam pārdošanas pasūtījumam un iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="2a685-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="2a685-253">**Krājuma numurs:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="2a685-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="2a685-254">**Daudzums:** *7*</span><span class="sxs-lookup"><span data-stu-id="2a685-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="2a685-255">Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="2a685-256">**Krājuma numurs:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="2a685-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="2a685-257">**Daudzums:** *8*</span><span class="sxs-lookup"><span data-stu-id="2a685-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="2a685-258">Rezervējiet krājumus abām rindām.</span><span class="sxs-lookup"><span data-stu-id="2a685-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="2a685-259">Izlaidiet pasūtījumu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="2a685-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="2a685-260">4. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="2a685-260">Sales order 4</span></span>

1. <span data-ttu-id="2a685-261">Lai izveidotu 4. pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2a685-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="2a685-262">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2a685-263">**Debitora konts:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="2a685-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="2a685-264">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="2a685-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2a685-265">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2a685-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="2a685-266">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="2a685-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="2a685-267">Pievienojiet rindu jaunajam pārdošanas pasūtījumam un iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="2a685-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="2a685-268">**Krājuma numurs:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="2a685-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="2a685-269">**Daudzums:** *25*</span><span class="sxs-lookup"><span data-stu-id="2a685-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="2a685-270">Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="2a685-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="2a685-271">**Krājuma numurs:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="2a685-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="2a685-272">**Daudzums:** *10*</span><span class="sxs-lookup"><span data-stu-id="2a685-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="2a685-273">Rezervējiet krājumus abām rindām.</span><span class="sxs-lookup"><span data-stu-id="2a685-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="2a685-274">Izlaidiet pasūtījumu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="2a685-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="2a685-275">Darba ID iegūšana izveidotajam darbam</span><span class="sxs-lookup"><span data-stu-id="2a685-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="2a685-276">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="2a685-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="2a685-277">Laukā **Noliktava** veiciet filtrēšanu tā, lai darbs tiktu rādīts tikai noliktavai nr. *51*.</span><span class="sxs-lookup"><span data-stu-id="2a685-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="2a685-278">Ir jābūt izveidotiem četriem darba ID:</span><span class="sxs-lookup"><span data-stu-id="2a685-278">Four work IDs should have been created.</span></span> <span data-ttu-id="2a685-279">Pierakstiet katra pārdošanas pasūtījuma darba ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="2a685-280">Pārdošanas pasūtījuma ID</span><span class="sxs-lookup"><span data-stu-id="2a685-280">Sales order ID</span></span> | <span data-ttu-id="2a685-281">Darba ID</span><span class="sxs-lookup"><span data-stu-id="2a685-281">Work ID</span></span> | <span data-ttu-id="2a685-282">Darba daudzums</span><span class="sxs-lookup"><span data-stu-id="2a685-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="2a685-283">1. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="2a685-283">Sales Order 1</span></span> | <span data-ttu-id="2a685-284">1. darba ID</span><span class="sxs-lookup"><span data-stu-id="2a685-284">Work ID 1</span></span> | <span data-ttu-id="2a685-285">20 ea</span><span class="sxs-lookup"><span data-stu-id="2a685-285">20 ea</span></span> |
    | <span data-ttu-id="2a685-286">2. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="2a685-286">Sales Order 2</span></span> | <span data-ttu-id="2a685-287">2. darba ID</span><span class="sxs-lookup"><span data-stu-id="2a685-287">Work ID 2</span></span> | <span data-ttu-id="2a685-288">6 ea (abu rindu summa)</span><span class="sxs-lookup"><span data-stu-id="2a685-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="2a685-289">3. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="2a685-289">Sales Order 3</span></span> | <span data-ttu-id="2a685-290">3. darba ID</span><span class="sxs-lookup"><span data-stu-id="2a685-290">Work ID 3</span></span> | <span data-ttu-id="2a685-291">15 ea (abu rindu summa)</span><span class="sxs-lookup"><span data-stu-id="2a685-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="2a685-292">4. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="2a685-292">Sales Order 4</span></span> | <span data-ttu-id="2a685-293">4. darba ID</span><span class="sxs-lookup"><span data-stu-id="2a685-293">Work ID 4</span></span> | <span data-ttu-id="2a685-294">35 ea (abu rindu summa)</span><span class="sxs-lookup"><span data-stu-id="2a685-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="2a685-295">Pirms plūsmas izpildes mobilajā ierīcē pārliecinieties, vai tikko izveidotā darba noliktavas nr. *51* un darba pasūtījuma tipa *Pārdošanas pasūtījums* statuss ir *Atvērts*.</span><span class="sxs-lookup"><span data-stu-id="2a685-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="2a685-296">Pretējā gadījumā testa rezultāti var atšķirties, jo sistēmas tiešajā izdošanā tiks iekļauts viss piemērotais darbs.</span><span class="sxs-lookup"><span data-stu-id="2a685-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="2a685-297">Atveriet **Noliktavas pārvaldība \> Darbs \> Izejošs \> Atvērts pārdošanas darbs**.</span><span class="sxs-lookup"><span data-stu-id="2a685-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="2a685-298">Režģī **Atvērts pārdošanas darbs** laukā **Noliktava** veiciet filtrēšanu tā, lai darbs tiktu rādīts tikai noliktavai nr. *51*.</span><span class="sxs-lookup"><span data-stu-id="2a685-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="2a685-299">Pārliecinieties, vai tiek rādīti tikai iepriekš izveidotie četri darba ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="2a685-300">Aizveriet lapu **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="2a685-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="2a685-301">Mobilās ierīces plūsmas izpilde</span><span class="sxs-lookup"><span data-stu-id="2a685-301">Mobile device flow execution</span></span>

<span data-ttu-id="2a685-302">Ņemot vērā iestatījumu, sistēma rādīs lietotāja darbu, kas tiek kārtots no augstākās darba rindas daudzuma uz zemāko.</span><span class="sxs-lookup"><span data-stu-id="2a685-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="2a685-303">Daudzums katrā rindā būs mazāks par 20 ea.</span><span class="sxs-lookup"><span data-stu-id="2a685-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="2a685-304">Ņemiet vērā, ka ar šo iestatījumu tiks nolasīts visa veida darbs, kurā ir vismaz viena rinda ar daudzumu, kas mazāks par 20 ea.</span><span class="sxs-lookup"><span data-stu-id="2a685-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="2a685-305">Līdz ar to, ja darbam ir cita rinda, kuras daudzums ir tieši 20 ea vai vairāk par 20 ea, arī tā būs derīga.</span><span class="sxs-lookup"><span data-stu-id="2a685-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="2a685-306">Mobilā programma</span><span class="sxs-lookup"><span data-stu-id="2a685-306">Mobile app</span></span>

1. <span data-ttu-id="2a685-307">Pierakstieties noliktavas programmā kā lietotājs noliktavā *51*.</span><span class="sxs-lookup"><span data-stu-id="2a685-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="2a685-308">Atveriet **Izejošs \> Pārdošanas izdošana – Sistēma**.</span><span class="sxs-lookup"><span data-stu-id="2a685-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="2a685-309">Tiek rādīts *4.*  darba ID izdošanas solis.</span><span class="sxs-lookup"><span data-stu-id="2a685-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="2a685-310">Šis darba ID tiek rādīts vispirms sistēmas noteikta vaicājuma pasūtījuma iestatīšanas dēļ, kur jūs norādījāt, ka darba secība ir jāveido, ņemot vērā darba rindu daudzumu dilstošā secībā.</span><span class="sxs-lookup"><span data-stu-id="2a685-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="2a685-311">Pabeidziet nepieciešamo izdošanu un novietojiet, lai aizvērtu darba ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="2a685-312">Pēc tam tiek rādīts *3.*  darba ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="2a685-313">Viena no tā darba rindām ir nākamā secībā, ņemot vērā darba rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="2a685-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="2a685-314">Pabeidziet izdošanu un novietojiet, lai aizvērtu darba ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="2a685-315">Pēc tam tiek rādīts *2.*  darba ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="2a685-316">Šī darba izdošanas rinda ir nākamā secībā.</span><span class="sxs-lookup"><span data-stu-id="2a685-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="2a685-317">Pabeidziet izdošanu un novietojiet, lai aizvērtu darba ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="2a685-318">Cits darbs jums vairs netiks rādīts.</span><span class="sxs-lookup"><span data-stu-id="2a685-318">No further work should be presented to you.</span></span> <span data-ttu-id="2a685-319">*1.*  darba ID šim mobilās ierīces izvēlnes vienumam nav piemērots, jo vaicājumā ir norādīts, ka darba galvenes tiek ņemtas vērā tikai tad, ja darba rindu daudzums ir mazāks par 20 ea.</span><span class="sxs-lookup"><span data-stu-id="2a685-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="2a685-320">Padomi</span><span class="sxs-lookup"><span data-stu-id="2a685-320">Tips</span></span>

<span data-ttu-id="2a685-321">Sistēmas norādītie darbu secības vaicājumi ir *iekļauti*.</span><span class="sxs-lookup"><span data-stu-id="2a685-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="2a685-322">Šo faktu ir svarīgi atcerēties dažiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="2a685-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="2a685-323">Piemēram, jūs vēlaties, lai konkrēts izvēlnes vienums apstrādā tikai to darbu, kur darba vienība ir *ea*, un jūs šo ierobežojumu norādāt vaicājuma cilnē **Diapazons**.</span><span class="sxs-lookup"><span data-stu-id="2a685-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="2a685-324">Šajā gadījumā darbiniekam tiks parādīts viss darbs, kur vismaz vienā darba rindā kādai darba vienībai būs iestatīts *ea*.</span><span class="sxs-lookup"><span data-stu-id="2a685-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="2a685-325">Tāpēc šajā darbā var būt ietverts arī darbs, kurā darba rindām būs cits darba vienības iestatījums, nevis *ea* (piemēram, *kaste* vai *palete*).</span><span class="sxs-lookup"><span data-stu-id="2a685-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="2a685-326">Vaicājums izslēgs tikai to darbu, kur nevienai darba rindai nebūs darba vienības ar iestatījumu *ea*.</span><span class="sxs-lookup"><span data-stu-id="2a685-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="2a685-327">Tāpēc šī scenārija piemērā vaicājumā bija iekļauts arī *4.*  darba ID.</span><span class="sxs-lookup"><span data-stu-id="2a685-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="2a685-328">Pēc tā izveidošanas tika pievienotas divas rindas: viena iestatījumam 25 ea un otra — 10 ea.</span><span class="sxs-lookup"><span data-stu-id="2a685-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="2a685-329">Darbs vienalga tika rādīts darbiniekam, jo vismaz vienā darba rindā iekļautais daudzums bija mazāks par 20 ea.</span><span class="sxs-lookup"><span data-stu-id="2a685-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="2a685-330">Atkarībā no scenārija varat novērst šādu norisi, izmantojot darba pārtraukumus.</span><span class="sxs-lookup"><span data-stu-id="2a685-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]