---
title: Noliktavu slotu veidošana
description: Šajā tēmā ir sniegta informācija par noliktavu slotu veidošanu. Noliktavu slotu veidošana sniedz iespēju konsolidēt pieprasījumu pēc krājuma un mērvienības no pasūtījumiem ar statusu Pasūtīts, Rezervēts vai Izlaists. Tas palīdz noliktavu vadītājiem pārdomāti plānot izdošanas novietojumus, pirms viņi izlaiž pasūtījumus noliktavā un izveido izdošanas darbu.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017418"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="27c30-105">Noliktavu slotu veidošana</span><span class="sxs-lookup"><span data-stu-id="27c30-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27c30-106">Noliktavu slotu veidošana sniedz iespēju konsolidēt pieprasījumu pēc krājuma un mērvienības no pasūtījumiem ar statusu *Pasūtīts* , *Rezervēts* vai *Izlaists*.</span><span class="sxs-lookup"><span data-stu-id="27c30-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="27c30-107">Pēc tam ģenerēto pieprasījumu var lietot novietojumiem, kas tiks izmantoti izdošanai, pamatojoties uz daudzumu, vienību, fiziskām dimensijām, fiksētiem novietojumiem un citām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="27c30-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="27c30-108">Kad slotu veidošanas plāns ir gatavs, var izveidot papildināšanas darbu, lai katram novietojumam piegādātu atbilstošu krājumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="27c30-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="27c30-109">Šī funkcija palīdz noliktavu vadītājiem pārdomāti plānot izdošanas novietojumus, pirms viņi izlaiž pasūtījumus noliktavā un izveido izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="27c30-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="27c30-110">Līdzekļa Noliktavu slotu veidošana ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="27c30-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="27c30-111">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="27c30-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="27c30-112">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="27c30-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="27c30-113">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="27c30-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="27c30-114">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="27c30-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="27c30-115">**Līdzekļa nosaukums:** *noliktavu slotu veidošanas līdzeklis*</span><span class="sxs-lookup"><span data-stu-id="27c30-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="27c30-116">Noliktavu slotu veidošanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="27c30-116">Set up warehouse slotting</span></span>

<span data-ttu-id="27c30-117">Lai izmantotu noliktavu slotu veidošanu, sistēmā ir jāiestata tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="27c30-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="27c30-118">Mērvienību pakāpju izveide slotu veidošanai</span><span class="sxs-lookup"><span data-stu-id="27c30-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="27c30-119">Mērvienību pakāpes ļauj slotu veidošanas nolūkā kopā grupēt vairākas mērvienības.</span><span class="sxs-lookup"><span data-stu-id="27c30-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="27c30-120">Piemēram, ja no tā paša kastu izdošanas apgabala tiek izdotas vairāku lielumu kastes, visiem lielumiem var izveidot vienu līmeni.</span><span class="sxs-lookup"><span data-stu-id="27c30-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="27c30-121">**Katrai mērvienībai, kas būs pakāpes daļa, ir jāizveido rinda.**</span><span class="sxs-lookup"><span data-stu-id="27c30-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="27c30-122">Atveriet **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Slotu veidošanas mērvienību pakāpes**.</span><span class="sxs-lookup"><span data-stu-id="27c30-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="27c30-123">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="27c30-123">Select **New**.</span></span>
1. <span data-ttu-id="27c30-124">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="27c30-125">**Mērvienības pakāpe:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="27c30-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="27c30-126">**Apraksts:** *katra kastes palete*</span><span class="sxs-lookup"><span data-stu-id="27c30-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="27c30-127">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="27c30-127">Select **Save**.</span></span>
1. <span data-ttu-id="27c30-128">Kopsavilkuma cilnē **Mērvienība** atlasiet **Jauns** , lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="27c30-129">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27c30-130">**Vienība:** *kaste*</span><span class="sxs-lookup"><span data-stu-id="27c30-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="27c30-131">**Apraksts:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="27c30-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="27c30-132">Saglabājot izmaiņas, tas tiks automātiski aizpildīts.</span><span class="sxs-lookup"><span data-stu-id="27c30-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="27c30-133">**Vienības klase:** *daudzums*</span><span class="sxs-lookup"><span data-stu-id="27c30-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="27c30-134">Atlasiet **Jauns** , lai režģim pievienotu otru rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="27c30-135">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27c30-136">**Vienība:** *ea*</span><span class="sxs-lookup"><span data-stu-id="27c30-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="27c30-137">**Apraksts:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="27c30-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="27c30-138">Saglabājot izmaiņas, tas tiks automātiski aizpildīts.</span><span class="sxs-lookup"><span data-stu-id="27c30-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="27c30-139">**Vienības klase:** *daudzums*</span><span class="sxs-lookup"><span data-stu-id="27c30-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="27c30-140">Atlasiet **Jauns** , lai režģim pievienotu trešo rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="27c30-141">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27c30-142">**Vienība:** *PL*</span><span class="sxs-lookup"><span data-stu-id="27c30-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="27c30-143">**Apraksts:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="27c30-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="27c30-144">Saglabājot izmaiņas, tas tiks automātiski aizpildīts.</span><span class="sxs-lookup"><span data-stu-id="27c30-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="27c30-145">**Vienības klase:** *daudzums*</span><span class="sxs-lookup"><span data-stu-id="27c30-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="27c30-146">Atlasiet **Saglabāt** , lai saglabātu pakāpi.</span><span class="sxs-lookup"><span data-stu-id="27c30-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="27c30-147">Slotu veidošanas direktīvas koda izveide</span><span class="sxs-lookup"><span data-stu-id="27c30-147">Create a directive code for slotting</span></span>

<span data-ttu-id="27c30-148">Atlasiet direktīvas kodu, ko saistīt ar veidni.</span><span class="sxs-lookup"><span data-stu-id="27c30-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="27c30-149">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Direktīvas kodi**.</span><span class="sxs-lookup"><span data-stu-id="27c30-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="27c30-150">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="27c30-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="27c30-151">Laukā **Direktīvas kods** ievadiet *Slotu veidošana*.</span><span class="sxs-lookup"><span data-stu-id="27c30-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="27c30-152">Laukā **Direktīvas apraksts** ievadiet *Slotu veidošana*.</span><span class="sxs-lookup"><span data-stu-id="27c30-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="27c30-153">Noliktavu slotu veidņu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="27c30-153">Set up slotting templates</span></span>

<span data-ttu-id="27c30-154">Ar katru slotu veidošanas veidni kontrolē, kā krājumi tiek piešķirti novietojumiem kādai konkrētai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="27c30-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="27c30-155">Katrā veidnē ir jābūt rindai, kas paredzēta katrai slotu veidošanas specifikācijai.</span><span class="sxs-lookup"><span data-stu-id="27c30-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="27c30-156">Izmantojiet šajā sadaļā pieejamās procedūras, lai iestatītu slotu veidošanas veidnes.</span><span class="sxs-lookup"><span data-stu-id="27c30-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="27c30-157">Atveriet **Noliktavas vadība \> Iestatīšana \> Papildināšana \> Slotu veidošanas veidnes**.</span><span class="sxs-lookup"><span data-stu-id="27c30-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="27c30-158">Atlasiet **Jauns** , lai izveidotu veidni.</span><span class="sxs-lookup"><span data-stu-id="27c30-158">Select **New** to create a template.</span></span>

<span data-ttu-id="27c30-159">Pēc tam ir jāiestata veidnes galvene, slotu veidošanas specifikācijas un novietojumu direktīvas, kā tas ir izskaidrots nākamajās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="27c30-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="27c30-160">Slotu veidošanas galvenes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="27c30-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="27c30-161">Veidnes galvenē iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="27c30-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="27c30-162">**Slotu veidošanas veidne:** _61_</span><span class="sxs-lookup"><span data-stu-id="27c30-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="27c30-163">**Apraksts:** _61_</span><span class="sxs-lookup"><span data-stu-id="27c30-163">**Description:** _61_</span></span>
    - <span data-ttu-id="27c30-164">**Pieprasījuma veids:** *pārdošanas pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="27c30-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="27c30-165">Pašlaik vienīgais atbalstītais pieprasījuma veids ir *Pārdošanas pasūtījums*.</span><span class="sxs-lookup"><span data-stu-id="27c30-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="27c30-166">**Pieprasījuma stratēģija:** _pasūtīts_</span><span class="sxs-lookup"><span data-stu-id="27c30-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="27c30-167">Šajā laukā ir pieejamas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="27c30-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="27c30-168">**Pasūtīts**  — pilnībā pasūtīts pārdošanas pasūtījuma daudzums ir uzskatāms par pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="27c30-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="27c30-169">**Rezervēts**  — par pieprasījumu ir uzskatāmi tikai rezervētie (fiziskie un pasūtītie) pārdošanas pasūtījuma rindas daudzumi.</span><span class="sxs-lookup"><span data-stu-id="27c30-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="27c30-170">**Noliktava:** _61_</span><span class="sxs-lookup"><span data-stu-id="27c30-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="27c30-171">**Atļaut kopuma pieprasījumā izmantot nerezervētos daudzumus**  — _Jā_</span><span class="sxs-lookup"><span data-stu-id="27c30-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="27c30-172">Varat arī norādīt vaicājumu, lai sašaurinātu novērtējamā pieprasījuma apjomu.</span><span class="sxs-lookup"><span data-stu-id="27c30-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="27c30-173">Slotu veidošanas specifikāciju iestatīšana katrai veidnei</span><span class="sxs-lookup"><span data-stu-id="27c30-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="27c30-174">Katrai veidnei, ko izveidojat, veiciet tālāk norādītās darbības, lai katrai slotu veidošanas specifikācijai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="27c30-175">Kopsavilkuma cilnē **Detalizēta informācija par slotu veidošanas veidni** atlasiet **Jauns** , lai izveidotu veidnes rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="27c30-176">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27c30-177">**Secība:** _1_</span><span class="sxs-lookup"><span data-stu-id="27c30-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="27c30-178">**Apraksts:** _fiksēts novietojums_</span><span class="sxs-lookup"><span data-stu-id="27c30-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="27c30-179">**Minimālais daudzums:** _1_</span><span class="sxs-lookup"><span data-stu-id="27c30-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="27c30-180">Šajā laukā ir definēts rindai nepieciešamais minimālais pieprasījuma daudzums.</span><span class="sxs-lookup"><span data-stu-id="27c30-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="27c30-181">**Maksimālais daudzums:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="27c30-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="27c30-182">Šajā laukā ir definēts rindai derīgais maksimālais pieprasījuma daudzums.</span><span class="sxs-lookup"><span data-stu-id="27c30-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="27c30-183">**Vienība:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="27c30-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="27c30-184">Šajā laukā ir definēta mērvienība, uz kuru attiecas minimālie un maksimālie daudzumi.</span><span class="sxs-lookup"><span data-stu-id="27c30-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="27c30-185">**Mērvienības pakāpe:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="27c30-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="27c30-186">Šajā laukā ir definēts rindai derīgās pieprasījuma mērvienības.</span><span class="sxs-lookup"><span data-stu-id="27c30-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="27c30-187">(Papildinformāciju skatiet sadaļā [Mērvienību pakāpju izveide slotu veidošanai](#unit-tiers) iepriekš šajā tēmā)</span><span class="sxs-lookup"><span data-stu-id="27c30-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="27c30-188">**Piešķirt slota kritēriju:** _apsvērt daudz._</span><span class="sxs-lookup"><span data-stu-id="27c30-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="27c30-189">Šajā laukā ir pieejamas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="27c30-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="27c30-190">**Pieņemt, ka tukšs**  — šī sistēma pieņems, ka visi novietojumi izdošanas apgabalā ir tukši un šajos novietojumos nepārbaudīs krājumus.</span><span class="sxs-lookup"><span data-stu-id="27c30-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="27c30-191">**Apsvērt daudz.**  — sistēma pārbaudīs novietojumus izdošanas apgabalā, meklējot krājumus, un izlaidīs visus novietojumus, kas nebūs tukši.</span><span class="sxs-lookup"><span data-stu-id="27c30-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="27c30-192">**Direktīvas kods:** _slotu veidošana_</span><span class="sxs-lookup"><span data-stu-id="27c30-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="27c30-193">Šis lauks nosaka novietojuma direktīvu, kas tiek izmantota, lai atrastu papildināšana darba izdošanas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="27c30-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="27c30-194">**Pārpildes novietojums:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="27c30-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="27c30-195">Šis lauks definē novietojumu, kurā tiek novietoti krājumi, ja rindas apstrādes laikā daudzumam nevar atrast novietojumu.</span><span class="sxs-lookup"><span data-stu-id="27c30-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="27c30-196">**Atļaut palaišanu:** _Jā_</span><span class="sxs-lookup"><span data-stu-id="27c30-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="27c30-197">Ja šai opcijai ir iestatīta vērtība *Jā* , ja katram pieprasījumam nevar izveidot slotu, tiks izveidots kustības darbs, lai izņemtu krājumus no novietojumiem, kuros ir krājumi, bet nekam nav izveidoti sloti.</span><span class="sxs-lookup"><span data-stu-id="27c30-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="27c30-198">Pēc tam veidne atkal tiek palaista.</span><span class="sxs-lookup"><span data-stu-id="27c30-198">The template is then run again.</span></span> <span data-ttu-id="27c30-199">Šoreiz tā ignorē krājumus novietojumos.</span><span class="sxs-lookup"><span data-stu-id="27c30-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="27c30-200">Šī funkcija darbojas vislabāk, ja laukam **Piešķirt slota kritēriju** ir iestatīta vērtība _Apsvērt daudz_.</span><span class="sxs-lookup"><span data-stu-id="27c30-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="27c30-201">**Fiksēta novietojuma lietojums:** _tikai produktam paredzēti fiksēti novietojumi_</span><span class="sxs-lookup"><span data-stu-id="27c30-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="27c30-202">Šajā laukā ir pieejamas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="27c30-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="27c30-203">**Fiksēti un nefiksēti novietojumi**  — sistēmai nevajadzētu būt ierobežojumam izmantot tikai fiksētus novietojumus.</span><span class="sxs-lookup"><span data-stu-id="27c30-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="27c30-204">**Tikai produktam paredzēti fiksēti novietojumi**  — sistēmai vajadzētu izveidot slotus tikai uz novietojumiem, kas ir produktam paredzēti fiksēti novietojumi.</span><span class="sxs-lookup"><span data-stu-id="27c30-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="27c30-205">**Tikai produkta variantam paredzēti fiksēti novietojumi**  — sistēmai vajadzētu izveidot slotus tikai uz novietojumiem, kas ir produkta variantam paredzēti fiksēti novietojumi.</span><span class="sxs-lookup"><span data-stu-id="27c30-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="27c30-206">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="27c30-206">Select **Save**.</span></span>
1. <span data-ttu-id="27c30-207">Atlasiet **Jauns** , lai izveidotu otro veidnes rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="27c30-208">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27c30-209">**Secība:** _2_</span><span class="sxs-lookup"><span data-stu-id="27c30-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="27c30-210">**Apraksts:** _Cits_</span><span class="sxs-lookup"><span data-stu-id="27c30-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="27c30-211">**Minimālais daudz.:** _1_</span><span class="sxs-lookup"><span data-stu-id="27c30-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="27c30-212">**Maksimālais daudz.:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="27c30-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="27c30-213">**Vienība:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="27c30-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="27c30-214">**Mērvienības pakāpe:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="27c30-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="27c30-215">**Piešķirt slota kritēriju:** _apsvērt daudz._</span><span class="sxs-lookup"><span data-stu-id="27c30-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="27c30-216">**Direktīvas kods:** _slotu veidošana_</span><span class="sxs-lookup"><span data-stu-id="27c30-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="27c30-217">**Pārpildes novietojums:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="27c30-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="27c30-218">**Atļaut palaišanu:** _Jā_</span><span class="sxs-lookup"><span data-stu-id="27c30-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="27c30-219">**Izmantot fiksētus novietojumus:** _fiksēti un nefiksēti novietojumi_</span><span class="sxs-lookup"><span data-stu-id="27c30-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="27c30-220">Otrajai rindai paredzētajā vaicājumā norādiet kritērijus, kas tiks izmantoti, lai noteiktu, kuriem novietojumiem šai rindai var izveidot pieprasījuma slotu.</span><span class="sxs-lookup"><span data-stu-id="27c30-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="27c30-221">Atlasiet rindu, kur laukam **Secība** ir iestatīta vērtība  *2*.</span><span class="sxs-lookup"><span data-stu-id="27c30-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="27c30-222">Atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="27c30-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="27c30-223">Cilnē **Diapazons** atlasiet **Pievienot** , lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="27c30-224">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27c30-225">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="27c30-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="27c30-226">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="27c30-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="27c30-227">**Lauks:** *Atrašanās vietas profila ID*</span><span class="sxs-lookup"><span data-stu-id="27c30-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="27c30-228">**Kritēriji:** *Pick-06* (atlasiet dubulto pluszīmi \[**++**\] laukā, lai izvērstu sarakstu, un pēc tam atlasiet *Pick-06* - *6. izdošanas vieta* ).</span><span class="sxs-lookup"><span data-stu-id="27c30-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="27c30-229">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="27c30-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="27c30-230">Iestatīt novietojuma direktīvas</span><span class="sxs-lookup"><span data-stu-id="27c30-230">Set up location directives</span></span>

<span data-ttu-id="27c30-231">Lai atbalstītu slotu veidošanas izdošanas, ir jāiestata vismaz viena novietojuma direktīva.</span><span class="sxs-lookup"><span data-stu-id="27c30-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="27c30-232">Izmantojiet šajā sadaļā pieejamās procedūras, lai izveidotu jaunu *papildināšanas novietojuma direktīvu* slotu veidošanas izdošanas gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="27c30-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="27c30-233">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="27c30-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="27c30-234">Kreisajā rūtī, laukā **Darba pasūtījuma veids** atlasiet *Papildināšana*.</span><span class="sxs-lookup"><span data-stu-id="27c30-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="27c30-235">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="27c30-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="27c30-236">Jaunās novietojuma direktīvas galvenes laukā **Nosaukums** ievadiet *61. slotu veidošanas izdošana*.</span><span class="sxs-lookup"><span data-stu-id="27c30-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="27c30-237">Novietojuma direktīvas kopsavilkuma cilnes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="27c30-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="27c30-238">Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="27c30-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="27c30-239">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="27c30-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="27c30-240">**Darba veids:** _Izdošana_</span><span class="sxs-lookup"><span data-stu-id="27c30-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="27c30-241">**Vieta:** _6_</span><span class="sxs-lookup"><span data-stu-id="27c30-241">**Site:** _6_</span></span>
    - <span data-ttu-id="27c30-242">**Noliktava:** _61_</span><span class="sxs-lookup"><span data-stu-id="27c30-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="27c30-243">**Direktīvas kods:** _slotu veidošana_</span><span class="sxs-lookup"><span data-stu-id="27c30-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="27c30-244">Atlasiet **Saglabāt** , lai padarītu pieejamu kopsavilkuma cilni **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="27c30-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="27c30-245">Rindu kopsavilkuma cilnes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="27c30-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="27c30-246">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns** , lai izveidotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="27c30-247">Jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="27c30-247">On the new line, set the following values.</span></span> <span data-ttu-id="27c30-248">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="27c30-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="27c30-249">**No daudzuma:** _0_</span><span class="sxs-lookup"><span data-stu-id="27c30-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="27c30-250">**Līdz daudzumam:** _1 000 000_</span><span class="sxs-lookup"><span data-stu-id="27c30-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="27c30-251">Atlasiet **Saglabāt** , lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.</span><span class="sxs-lookup"><span data-stu-id="27c30-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="27c30-252">Novietojuma direktīvas darbību kopsavilkuma cilnes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="27c30-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="27c30-253">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns** , lai izveidotu rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="27c30-254">Jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="27c30-254">On the new line, set the following values.</span></span> <span data-ttu-id="27c30-255">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="27c30-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="27c30-256">**Nosaukums:** _lielapjoma_</span><span class="sxs-lookup"><span data-stu-id="27c30-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="27c30-257">**Stratēģija:** _Nav_</span><span class="sxs-lookup"><span data-stu-id="27c30-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="27c30-258">Atlasiet **Saglabāt** , lai padarītu pieejamu pogu **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="27c30-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="27c30-259">Rediģēt vaicājumu</span><span class="sxs-lookup"><span data-stu-id="27c30-259">Edit the query</span></span>

1. <span data-ttu-id="27c30-260">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="27c30-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="27c30-261">Cilnē **Diapazons** atlasiet **Pievienot** , lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="27c30-262">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="27c30-263">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="27c30-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="27c30-264">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="27c30-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="27c30-265">**Lauks:** *Zonas ID*</span><span class="sxs-lookup"><span data-stu-id="27c30-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="27c30-266">**Kritēriji:** *lielapjoma* (atlasiet dubulto pluszīmi \[**++**\] laukā, lai izvērstu sarakstu, un pēc tam atlasiet *Lielapjoma*.)</span><span class="sxs-lookup"><span data-stu-id="27c30-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="27c30-267">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="27c30-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="27c30-268">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="27c30-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="27c30-269">Scenārija iestatīšana</span><span class="sxs-lookup"><span data-stu-id="27c30-269">Set up the scenario</span></span>

<span data-ttu-id="27c30-270">Šim scenārijam izmantojiet iebūvēto datu paraugu un izveidojiet ierakstus, kas ir raksturoti šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="27c30-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="27c30-271">USMF datu parauga izmantošana</span><span class="sxs-lookup"><span data-stu-id="27c30-271">Use the USMF sample data</span></span>

<span data-ttu-id="27c30-272">Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="27c30-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="27c30-273">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="27c30-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="27c30-274">Pieprasījuma izveide</span><span class="sxs-lookup"><span data-stu-id="27c30-274">Create demand</span></span>

<span data-ttu-id="27c30-275">Izpildiet šīs darbības, lai izveidotu pieprasījumu, kuram lietosit slotu veidošanu.</span><span class="sxs-lookup"><span data-stu-id="27c30-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="27c30-276">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="27c30-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="27c30-277">Atlasiet **Jauns** , lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="27c30-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="27c30-278">Dialoglodziņā **Pārdošanas pasūtījuma izveide** **klienta konta** laukā atlasiet _US-007_.</span><span class="sxs-lookup"><span data-stu-id="27c30-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="27c30-279">Laukā **Noliktava** atlasiet _61_.</span><span class="sxs-lookup"><span data-stu-id="27c30-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="27c30-280">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="27c30-280">Select **OK**.</span></span>
1. <span data-ttu-id="27c30-281">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="27c30-281">The new sales order is opened.</span></span> <span data-ttu-id="27c30-282">Tajā ir ietverta tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="27c30-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="27c30-283">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="27c30-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="27c30-284">**Krājums:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="27c30-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="27c30-285">**Daudzums:** _20_</span><span class="sxs-lookup"><span data-stu-id="27c30-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="27c30-286">Atlasiet **Pievienot rindu** , lai pievienotu jaunu rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="27c30-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="27c30-287">**Krājums:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="27c30-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="27c30-288">**Daudzums:** _8_</span><span class="sxs-lookup"><span data-stu-id="27c30-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="27c30-289">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="27c30-289">Select **Save**.</span></span>
1. <span data-ttu-id="27c30-290">Atlasiet **Jauns** , lai izveidotu otro pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="27c30-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="27c30-291">Dialoglodziņā **Pārdošanas pasūtījuma izveide** **klienta konta** laukā atlasiet _US-008_.</span><span class="sxs-lookup"><span data-stu-id="27c30-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="27c30-292">Laukā **Noliktava** atlasiet _61_.</span><span class="sxs-lookup"><span data-stu-id="27c30-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="27c30-293">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="27c30-293">The new sales order is opened.</span></span> <span data-ttu-id="27c30-294">Tajā ir ietverta tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="27c30-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="27c30-295">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="27c30-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="27c30-296">**Krājums:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="27c30-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="27c30-297">**Daudzums:** _1_</span><span class="sxs-lookup"><span data-stu-id="27c30-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="27c30-298">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="27c30-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="27c30-299">Tipiska slotu veidošanas scenārija apskate</span><span class="sxs-lookup"><span data-stu-id="27c30-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="27c30-300">Kad visi priekšnosacījuma elementi ir ieviesti, kā tas tika izklāstīts iepriekšējā sadaļā, jūs esat gatavs izmēģināt līdzekli, izpildot katru šajā sadaļā norādīto uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="27c30-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="27c30-301">Ģenerēt pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="27c30-301">Generate demand</span></span>

1. <span data-ttu-id="27c30-302">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Slotu veidošanas veidnes** un atlasiet slotu veidošanas veidni, ko izveidojāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="27c30-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="27c30-303">Darbību rūtī atlasiet **Ģenerēt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="27c30-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="27c30-304">Šī komanda novērtē visu pieprasījumu, kas atrodas sistēmā un atbilst slotu veidošanas veidnes vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="27c30-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="27c30-305">Pēc tam kopējais pieprasījums no visiem pasūtījumiem tiek konsolidēts vienā rindā katram daudzumam/mērvienībai.</span><span class="sxs-lookup"><span data-stu-id="27c30-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="27c30-306">Kad process ir pabeigts, tiek parādīts informācijas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="27c30-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="27c30-307">Slotu veidošanas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="27c30-307">Slotting demand</span></span>

<span data-ttu-id="27c30-308">*Slotu veidošanas pieprasījums* parāda pieprasījuma ģenerēšanas rezultātus, pamatojoties uz slotu veidošanas veidnes iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="27c30-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="27c30-309">Darbību rūtī atlasiet **Slotu veidošanas pieprasījums** , lai skatītu rezultātus no komandas **Ģenerēt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="27c30-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="27c30-310">Slotu veidošanas pieprasījumā esošās rindas var rediģēt.</span><span class="sxs-lookup"><span data-stu-id="27c30-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="27c30-311">Varat dzēst rindu, pievienot jaunu rindu vai rediģēt detalizētu informāciju par rindu.</span><span class="sxs-lookup"><span data-stu-id="27c30-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="27c30-312">Pieprasījumu varat rediģēt manuāli vai to importēt no ārējās sistēmas, izmantojot datu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="27c30-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="27c30-313">Viss, kas būs iekļauts slotu veidošanas pieprasījumā, tiks izmantots nākamajā darbībā neatkarīgi no izcelsmes vietas.</span><span class="sxs-lookup"><span data-stu-id="27c30-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="27c30-314">Atrast pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="27c30-314">Locate demand</span></span>

<span data-ttu-id="27c30-315">Pēc pieprasījuma ģenerēšanas izmantojiet komandu **Meklēt pieprasījumu** , lai ģenerētu *slotu veidošanas plānu*.</span><span class="sxs-lookup"><span data-stu-id="27c30-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="27c30-316">Darbību rūtī atlasiet **Meklēt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="27c30-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="27c30-317">Tiek izpildīts slotu veidošanas process.</span><span class="sxs-lookup"><span data-stu-id="27c30-317">The slotting process runs.</span></span> <span data-ttu-id="27c30-318">Kad process ir pabeigts, tiek parādīts informācijas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="27c30-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="27c30-319">Slotu veidošanas plāns</span><span class="sxs-lookup"><span data-stu-id="27c30-319">Slotting plan</span></span>

<span data-ttu-id="27c30-320">Slotu veidošanas plāns rāda novietojumu, kuram tika piešķirts katrs krājums/daudzums, vai tika izmantota pārpilde, izveidots palaišanas darbs un vai tika izmantota veidnes rinda.</span><span class="sxs-lookup"><span data-stu-id="27c30-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="27c30-321">**Visi pieprasījumi, kuriem nevar izveidot slotu, ir izcelti sarkanā krāsā.**</span><span class="sxs-lookup"><span data-stu-id="27c30-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="27c30-322">Darbību rūtī atlasiet **Slotu veidošanas plāns** , lai skatītu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="27c30-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="27c30-323">Papildināšana izveide</span><span class="sxs-lookup"><span data-stu-id="27c30-323">Create replenishment</span></span>

<span data-ttu-id="27c30-324">Pēc slotu veidošanas plāna izveides ir jāizveido *papildināšanas darbs* , pamatojoties uz plānu.</span><span class="sxs-lookup"><span data-stu-id="27c30-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="27c30-325">Darbību rūtī atlasiet **Palaist papildināšanu**.</span><span class="sxs-lookup"><span data-stu-id="27c30-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="27c30-326">Kad process ir pabeigts, tiek parādīts informācijas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="27c30-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="27c30-327">Šis ziņojums norāda galveņu skaitu, kas tika izveidotas darba būvējuma ID.</span><span class="sxs-lookup"><span data-stu-id="27c30-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="27c30-328">Novietojuma direktīvas, kas tiks izmantotas, ir identificētas, pamatojoties uz katrā veidnes rindā norādīto direktīvas kodu.</span><span class="sxs-lookup"><span data-stu-id="27c30-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="27c30-329">Padomi</span><span class="sxs-lookup"><span data-stu-id="27c30-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="27c30-330">Automātiskas slotu veidošanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="27c30-330">Set up automatic slotting</span></span>

<span data-ttu-id="27c30-331">Kad visi nepieciešamie elementi ir ieviesti, varat izpildīt tālāk norādītās darbības, lai iestatītu slotu veidošanas automātisku izpildi.</span><span class="sxs-lookup"><span data-stu-id="27c30-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="27c30-332">Dodieties uz **Noliktavas pārvaldība \> Papildināšana \> Izpildīt slotu veidošanu**.</span><span class="sxs-lookup"><span data-stu-id="27c30-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="27c30-333">Norādiet izpildāmās slotu veidošanas darbības.</span><span class="sxs-lookup"><span data-stu-id="27c30-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="27c30-334">Atlasiet vienu vai vairākas no tālāk norādītajām slotu veidošanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="27c30-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="27c30-335">Ģenerēt pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="27c30-335">Generate demand</span></span>
    - <span data-ttu-id="27c30-336">Atrast pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="27c30-336">Locate demand</span></span>
    - <span data-ttu-id="27c30-337">Izveidot papildināšanas darbu</span><span class="sxs-lookup"><span data-stu-id="27c30-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="27c30-338">Slotu veidošanas darbības ir progresīvas.</span><span class="sxs-lookup"><span data-stu-id="27c30-338">The slotting steps are progressive.</span></span> <span data-ttu-id="27c30-339">Ja vēlaties atlasīt *Meklēt pieprasījumu* , vispirms ir jāatlasa *Ģenerēt pieprasījumu*.</span><span class="sxs-lookup"><span data-stu-id="27c30-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="27c30-340">Norādiet, kura slotu veidošanas veidne ir jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="27c30-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="27c30-341">Ja vēlaties, varat iestatīt automātisku periodiskuma izpildi.</span><span class="sxs-lookup"><span data-stu-id="27c30-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="27c30-342">Scenārijā iekļautajiem uzdevumiem **neiestatiet** automātisku slotu veidošanu.</span><span class="sxs-lookup"><span data-stu-id="27c30-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
