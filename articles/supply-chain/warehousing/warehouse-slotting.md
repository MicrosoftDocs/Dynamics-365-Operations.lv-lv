---
title: Noliktavu slotu veidošana
description: Šajā tēmā ir sniegta informācija par noliktavu slotu veidošanu. Noliktavu slotu veidošana sniedz iespēju konsolidēt pieprasījumu pēc krājuma un mērvienības no pasūtījumiem ar statusu Pasūtīts, Rezervēts vai Izlaists. Tas palīdz noliktavu vadītājiem pārdomāti plānot izdošanas novietojumus, pirms viņi izlaiž pasūtījumus noliktavā un izveido izdošanas darbu.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993757"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="eebfe-105">Noliktavu slotu veidošana</span><span class="sxs-lookup"><span data-stu-id="eebfe-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eebfe-106">Ir pieejami vairāki noliktavas slotu veidošanas līdzekļi, lai palīdzētu noliktavu vadītājiem pārdomāti plānot izdošanas novietojumus, pirms viņi izlaiž pasūtījumus noliktavā un izveido izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="eebfe-107">*Noliktavu slotu veidošanas līdzeklis* sniedz iespēju konsolidēt pieprasījumu pēc krājuma un mērvienības no pasūtījumiem ar statusu *Pasūtīts*, *Rezervēts* vai *Izlaists*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="eebfe-108">Pēc tam ģenerēto pieprasījumu var lietot novietojumiem, kas tiks izmantoti izdošanai, pamatojoties uz daudzumu, vienību, fiziskām dimensijām, fiksētiem novietojumiem un citām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="eebfe-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="eebfe-109">Kad slotu veidošanas plāns ir gatavs, var izveidot papildināšanas darbu, lai katram novietojumam piegādātu atbilstošu krājumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="eebfe-110">Līdzeklis *Noliktavas slotu veidošana pārsūtīšanas pasūtījumiem* sniedz iespēju noliktavas vadītājiem papildināt izdošanas vietas, pamatojoties uz pārsūtīšanas pasūtījumiem, kas vēl nav izlaisti uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="eebfe-111">Tas nodrošina, ka izdošanas vietas ietver visus krājumus, kas ir nepieciešami pārsūtīšanas pasūtījumiem pēc to izlaišanas uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="eebfe-112">Šim līdzeklim ir nepieciešams, lai tiktu ieslēgts arī līdzeklis *Noliktavas slotu veidošana*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="eebfe-113">Līdzeklis *Noliktavas slotu sadalījuma uzlabojumi* pievieno opciju veidnes rindām, ko izmanto līdzeklis *Noliktavas slotu veidošana*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="eebfe-114">Šī opcija sniedz sistēmai iespēju aplūkot esošos rīcībā esošos krājumus mērķa vietā.</span><span class="sxs-lookup"><span data-stu-id="eebfe-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="eebfe-115">Tāpēc slotu veidošanai var ģenerēt mazāk papildinājumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="eebfe-116">Līdzeklim *Noliktavas slotu sadalījuma uzlabojumi* ir nepieciešams, lai jūs ieslēgtu arī līdzekli *Noliktavas slotu veidošana*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="eebfe-117">To pēc izvēles var izmantot kopā ar līdzekli *Noliktavas slotu veidošana pārsūtīšanas pasūtījumiem*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="eebfe-118">Līdzekļu Noliktavu slotu veidošana ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="eebfe-119">Lai varētu izmantot šos līdzekļus, tie vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="eebfe-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="eebfe-120">Administratori var izmantot [līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļu statusu un tos ieslēgtu, ja tas nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="eebfe-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="eebfe-121">Ieslēgt tālāk minētos līdzekļus pēc vajadzības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="eebfe-122">Noliktavas slotu funkcija</span><span class="sxs-lookup"><span data-stu-id="eebfe-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="eebfe-123">Noliktavas slotu veidošana pārsūtīšanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="eebfe-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="eebfe-124">Līdzeklim *Noliktavas slotu veidošana* jābūt ieslēgtam pirms šā līdzekļa ieslēgšanas.</span><span class="sxs-lookup"><span data-stu-id="eebfe-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="eebfe-125">Noliktavas slotu veidošanas sadalījuma uzlabojumi</span><span class="sxs-lookup"><span data-stu-id="eebfe-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="eebfe-126">Līdzeklim *Noliktavas slotu veidošana* jābūt ieslēgtam pirms šā līdzekļa ieslēgšanas.</span><span class="sxs-lookup"><span data-stu-id="eebfe-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="eebfe-127">Noliktavu slotu veidošanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-127">Set up warehouse slotting</span></span>

<span data-ttu-id="eebfe-128">Lai izmantotu noliktavu slotu veidošanu, sistēmā ir jāiestata tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="eebfe-129">Slotu veidošanas mērvienību pakāpes</span><span class="sxs-lookup"><span data-stu-id="eebfe-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="eebfe-130">Direktīvu kodi</span><span class="sxs-lookup"><span data-stu-id="eebfe-130">Directive codes</span></span>
- <span data-ttu-id="eebfe-131">Slotu veidošanas veidnes</span><span class="sxs-lookup"><span data-stu-id="eebfe-131">Slotting templates</span></span>
- <span data-ttu-id="eebfe-132">Vietas direktīvas</span><span class="sxs-lookup"><span data-stu-id="eebfe-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="eebfe-133">Mērvienību pakāpju izveide slotu veidošanai</span><span class="sxs-lookup"><span data-stu-id="eebfe-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="eebfe-134">Mērvienību pakāpes ļauj slotu veidošanas nolūkā kopā grupēt vairākas mērvienības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="eebfe-135">Piemēram, ja no tā paša kastu izdošanas apgabala tiek izdotas vairāku lielumu kastes, visiem lielumiem var izveidot vienu līmeni.</span><span class="sxs-lookup"><span data-stu-id="eebfe-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="eebfe-136">**Katrai mērvienībai, kas būs pakāpes daļa, ir jāizveido rinda.**</span><span class="sxs-lookup"><span data-stu-id="eebfe-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="eebfe-137">Atveriet **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Slotu veidošanas mērvienību pakāpes**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="eebfe-138">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-138">Select **New**.</span></span>
1. <span data-ttu-id="eebfe-139">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="eebfe-140">**Mērvienības pakāpe:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="eebfe-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="eebfe-141">**Apraksts:** *katra kastes palete*</span><span class="sxs-lookup"><span data-stu-id="eebfe-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="eebfe-142">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-142">Select **Save**.</span></span>
1. <span data-ttu-id="eebfe-143">Kopsavilkuma cilnē **Mērvienība** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="eebfe-144">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-145">**Vienība:** *kaste*</span><span class="sxs-lookup"><span data-stu-id="eebfe-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="eebfe-146">**Apraksts:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="eebfe-147">Saglabājot izmaiņas, tas tiks automātiski aizpildīts.</span><span class="sxs-lookup"><span data-stu-id="eebfe-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="eebfe-148">**Vienības klase:** *daudzums*</span><span class="sxs-lookup"><span data-stu-id="eebfe-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="eebfe-149">Atlasiet **Jauns**, lai režģim pievienotu otru rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="eebfe-150">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-151">**Vienība:** *ea*</span><span class="sxs-lookup"><span data-stu-id="eebfe-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="eebfe-152">**Apraksts:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="eebfe-153">Saglabājot izmaiņas, tas tiks automātiski aizpildīts.</span><span class="sxs-lookup"><span data-stu-id="eebfe-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="eebfe-154">**Vienības klase:** *daudzums*</span><span class="sxs-lookup"><span data-stu-id="eebfe-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="eebfe-155">Atlasiet **Jauns**, lai režģim pievienotu trešo rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="eebfe-156">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-157">**Vienība:** *PL*</span><span class="sxs-lookup"><span data-stu-id="eebfe-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="eebfe-158">**Apraksts:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="eebfe-159">Saglabājot izmaiņas, tas tiks automātiski aizpildīts.</span><span class="sxs-lookup"><span data-stu-id="eebfe-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="eebfe-160">**Vienības klase:** *daudzums*</span><span class="sxs-lookup"><span data-stu-id="eebfe-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="eebfe-161">Atlasiet **Saglabāt**, lai saglabātu pakāpi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="eebfe-162">Slotu veidošanas direktīvas koda izveide</span><span class="sxs-lookup"><span data-stu-id="eebfe-162">Create a directive code for slotting</span></span>

<span data-ttu-id="eebfe-163">Atlasiet direktīvas kodu, ko saistīt ar veidni.</span><span class="sxs-lookup"><span data-stu-id="eebfe-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="eebfe-164">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Direktīvas kodi**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="eebfe-165">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eebfe-166">Laukā **Direktīvas kods** ievadiet *Slotu veidošana*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="eebfe-167">Laukā **Direktīvas apraksts** ievadiet *Slotu veidošana*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="eebfe-168">Noliktavu slotu veidņu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-168">Set up slotting templates</span></span>

<span data-ttu-id="eebfe-169">Ar katru slotu veidošanas veidni kontrolē, kā krājumi tiek piešķirti novietojumiem kādai konkrētai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="eebfe-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="eebfe-170">Katrā veidnē ir jābūt rindai, kas paredzēta katrai slotu veidošanas specifikācijai.</span><span class="sxs-lookup"><span data-stu-id="eebfe-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="eebfe-171">Izmantojiet šajā sadaļā pieejamās procedūras, lai iestatītu slotu veidošanas veidnes.</span><span class="sxs-lookup"><span data-stu-id="eebfe-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="eebfe-172">Atveriet **Noliktavas vadība \> Iestatīšana \> Papildināšana \> Slotu veidošanas veidnes**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="eebfe-173">Atlasiet **Jauns**, lai izveidotu veidni.</span><span class="sxs-lookup"><span data-stu-id="eebfe-173">Select **New** to create a template.</span></span>

<span data-ttu-id="eebfe-174">Pēc tam ir jāiestata veidnes galvene, slotu veidošanas specifikācijas un novietojumu direktīvas, kā tas ir izskaidrots nākamajās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="eebfe-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="eebfe-175">Slotu veidošanas pārsūtīšanas pasūtījumiem iestatījums līdzinās pārdošanas pasūtījumu slotu veidošanas iestatījumam, taču lauks **Pieprasījuma veids** tiek iestatīts uz *Pārsūtīšanas pasūtījumi*, nevis *Pārdošanas pasūtījums*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="eebfe-176">Pārdošanas pasūtījuma slotu veidošanas veidnes galvenes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="eebfe-177">Veidnes galvenē iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="eebfe-178">**Slotu veidošanas veidne:** _61_</span><span class="sxs-lookup"><span data-stu-id="eebfe-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="eebfe-179">**Apraksts:** _61_</span><span class="sxs-lookup"><span data-stu-id="eebfe-179">**Description:** _61_</span></span>
    - <span data-ttu-id="eebfe-180">**Pieprasījuma veids:** *pārdošanas pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="eebfe-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="eebfe-181">Pašlaik *Pārdošanas pasūtījumi* un *Pārsūtīšanas pasūtījumi* ir vienīgie pieprasījumu veidi, kas tiek atbalstīti.</span><span class="sxs-lookup"><span data-stu-id="eebfe-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="eebfe-182">Varat atlasīt *Pārsūtīšanas pasūtījumus* tikai tad, ja līdzeklis *Noliktavas slotu veidošana pārsūtīšanas pasūtījumiem* ir ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="eebfe-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="eebfe-183">**Pieprasījuma stratēģija:** _pasūtīts_</span><span class="sxs-lookup"><span data-stu-id="eebfe-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="eebfe-184">Šajā laukā ir pieejamas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="eebfe-185">**Pasūtīts** — pilnībā pasūtīts pārdošanas pasūtījuma daudzums ir uzskatāms par pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="eebfe-186">**Rezervēts** — par pieprasījumu ir uzskatāmi tikai rezervētie (fiziskie un pasūtītie) pārdošanas pasūtījuma rindas daudzumi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="eebfe-187">**Izlaists** – izlaistais daudzums ir jāuzskata par pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="eebfe-188">**Noliktava:** _61_</span><span class="sxs-lookup"><span data-stu-id="eebfe-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="eebfe-189">**Atļaut kopuma pieprasījumā izmantot nerezervētos daudzumus** — _Jā_</span><span class="sxs-lookup"><span data-stu-id="eebfe-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="eebfe-190">Varat arī norādīt vaicājumu, lai sašaurinātu novērtējamā pieprasījuma apjomu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="eebfe-191">Slotu veidošanas specifikāciju iestatīšana katrai veidnei</span><span class="sxs-lookup"><span data-stu-id="eebfe-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="eebfe-192">Katrai pārdošanas pasūtījuma veidnei, ko izveidojat, veiciet tālāk norādītās darbības, lai katrai slotu veidošanas specifikācijai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="eebfe-193">Kopsavilkuma cilnē **Detalizēta informācija par slotu veidošanas veidni** atlasiet **Jauns**, lai izveidotu veidnes rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="eebfe-194">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-195">**Secība:** _1_</span><span class="sxs-lookup"><span data-stu-id="eebfe-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="eebfe-196">**Apraksts:** _fiksēts novietojums_</span><span class="sxs-lookup"><span data-stu-id="eebfe-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="eebfe-197">**Minimālais daudzums:** _1_</span><span class="sxs-lookup"><span data-stu-id="eebfe-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="eebfe-198">Šajā laukā ir definēts rindai nepieciešamais minimālais pieprasījuma daudzums.</span><span class="sxs-lookup"><span data-stu-id="eebfe-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="eebfe-199">**Maksimālais daudzums:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="eebfe-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="eebfe-200">Šajā laukā ir definēts rindai derīgais maksimālais pieprasījuma daudzums.</span><span class="sxs-lookup"><span data-stu-id="eebfe-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="eebfe-201">**Vienība:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="eebfe-202">Šajā laukā ir definēta mērvienība, uz kuru attiecas minimālie un maksimālie daudzumi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="eebfe-203">**Mērvienības pakāpe:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="eebfe-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="eebfe-204">Šajā laukā ir definēts rindai derīgās pieprasījuma mērvienības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="eebfe-205">(Papildinformāciju skatiet sadaļā [Mērvienību pakāpju izveide slotu veidošanai](#unit-tiers) iepriekš šajā tēmā)</span><span class="sxs-lookup"><span data-stu-id="eebfe-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="eebfe-206">**Piešķirt slota kritēriju:** _apsvērt daudz._</span><span class="sxs-lookup"><span data-stu-id="eebfe-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="eebfe-207">Šajā laukā ir pieejamas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="eebfe-208">**Pieņemt, ka tukšs** — šī sistēma pieņems, ka visi novietojumi izdošanas apgabalā ir tukši un šajos novietojumos nepārbaudīs krājumus.</span><span class="sxs-lookup"><span data-stu-id="eebfe-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="eebfe-209">**Apsvērt daudz.**  — sistēma pārbaudīs novietojumus izdošanas apgabalā, meklējot krājumus, un izlaidīs visus novietojumus, kas nebūs tukši.</span><span class="sxs-lookup"><span data-stu-id="eebfe-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="eebfe-210">**Apsvērt rīcībā esošo** — sistēmai jāpārbauda, vai mērķa novietojums ietver nerezervētu daudzumu krājumam pieprasījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="eebfe-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="eebfe-211">Ja daudzums ir pietiekami liels, lai apmierinātu vismaz vienu pieprasījuma rindas vienību, ģenerētais slotu veidošanas plāna ieraksts tiek samazināts par pieejamo apjomu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="eebfe-212">Piemēram, ja pieprasījums ir 10 gadījumi un viens gadījums ir rīcībā esošs, tad izvietotais pieprasījums būs deviņi gadījumi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="eebfe-213">Ja pieprasījums ir 10 gadījumi un katrs gadījums ir rīcībā esošs, tad izvietotais pieprasījums būs 10 gadījumi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="eebfe-214">Šī vērtība ir pieejama tikai tad, kad ir ieslēgts līdzeklis *Noliktavas slotu veidošanas uzlabojumi*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="eebfe-215">**Direktīvas kods:** _slotu veidošana_</span><span class="sxs-lookup"><span data-stu-id="eebfe-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="eebfe-216">Šis lauks nosaka novietojuma direktīvu, kas tiek izmantota, lai atrastu papildināšana darba izdošanas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="eebfe-217">**Pārpildes novietojums:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="eebfe-218">Šis lauks definē novietojumu, kurā tiek novietoti krājumi, ja rindas apstrādes laikā daudzumam nevar atrast novietojumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="eebfe-219">**Atļaut palaišanu:** _Jā_</span><span class="sxs-lookup"><span data-stu-id="eebfe-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="eebfe-220">Ja šai opcijai ir iestatīta vērtība *Jā*, ja katram pieprasījumam nevar izveidot slotu, tiks izveidots kustības darbs, lai izņemtu krājumus no novietojumiem, kuros ir krājumi, bet nekam nav izveidoti sloti.</span><span class="sxs-lookup"><span data-stu-id="eebfe-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="eebfe-221">Pēc tam veidne atkal tiek palaista.</span><span class="sxs-lookup"><span data-stu-id="eebfe-221">The template is then run again.</span></span> <span data-ttu-id="eebfe-222">Šoreiz tā ignorē krājumus novietojumos.</span><span class="sxs-lookup"><span data-stu-id="eebfe-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="eebfe-223">Šī funkcija darbojas vislabāk, ja laukam **Piešķirt slota kritēriju** ir iestatīta vērtība _Apsvērt daudz_.</span><span class="sxs-lookup"><span data-stu-id="eebfe-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="eebfe-224">**Fiksēta novietojuma lietojums:** _tikai produktam paredzēti fiksēti novietojumi_</span><span class="sxs-lookup"><span data-stu-id="eebfe-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="eebfe-225">Šajā laukā ir pieejamas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="eebfe-226">**Fiksēti un nefiksēti novietojumi** — sistēmai nevajadzētu būt ierobežojumam izmantot tikai fiksētus novietojumus.</span><span class="sxs-lookup"><span data-stu-id="eebfe-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="eebfe-227">**Tikai produktam paredzēti fiksēti novietojumi** — sistēmai vajadzētu izveidot slotus tikai uz novietojumiem, kas ir produktam paredzēti fiksēti novietojumi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="eebfe-228">**Tikai produkta variantam paredzēti fiksēti novietojumi** — sistēmai vajadzētu izveidot slotus tikai uz novietojumiem, kas ir produkta variantam paredzēti fiksēti novietojumi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="eebfe-229">Ja slotu veidošanas veidne satur vismaz vienu rindu, kurā lauks **Piešķirt slota kritēriju** ir iestatīts kā *Apsvērt rīcībā esošo*, atļaut papildinājumus vairs nav atļauts nevienai veidnes rindai.</span><span class="sxs-lookup"><span data-stu-id="eebfe-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="eebfe-230">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-230">Select **Save**.</span></span>
1. <span data-ttu-id="eebfe-231">Atlasiet **Jauns**, lai izveidotu otro veidnes rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="eebfe-232">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-233">**Secība:** _2_</span><span class="sxs-lookup"><span data-stu-id="eebfe-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="eebfe-234">**Apraksts:** _Cits_</span><span class="sxs-lookup"><span data-stu-id="eebfe-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="eebfe-235">**Minimālais daudz.:** _1_</span><span class="sxs-lookup"><span data-stu-id="eebfe-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="eebfe-236">**Maksimālais daudz.:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="eebfe-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="eebfe-237">**Vienība:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="eebfe-238">**Mērvienības pakāpe:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="eebfe-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="eebfe-239">**Piešķirt slota kritēriju:** _apsvērt daudz._</span><span class="sxs-lookup"><span data-stu-id="eebfe-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="eebfe-240">**Direktīvas kods:** _slotu veidošana_</span><span class="sxs-lookup"><span data-stu-id="eebfe-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="eebfe-241">**Pārpildes novietojums:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="eebfe-242">**Atļaut palaišanu:** _Jā_</span><span class="sxs-lookup"><span data-stu-id="eebfe-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="eebfe-243">**Izmantot fiksētus novietojumus:** _fiksēti un nefiksēti novietojumi_</span><span class="sxs-lookup"><span data-stu-id="eebfe-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="eebfe-244">Otrajai rindai paredzētajā vaicājumā norādiet kritērijus, kas tiks izmantoti, lai noteiktu, kuriem novietojumiem šai rindai var izveidot pieprasījuma slotu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="eebfe-245">Atlasiet rindu, kur laukam **Secība** ir iestatīta vērtība *2*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="eebfe-246">Atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="eebfe-247">Cilnē **Diapazons** atlasiet **Pievienot**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="eebfe-248">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-249">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="eebfe-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="eebfe-250">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="eebfe-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="eebfe-251">**Lauks:** *Atrašanās vietas profila ID*</span><span class="sxs-lookup"><span data-stu-id="eebfe-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="eebfe-252">**Kritēriji:** *Pick-06* (atlasiet dubulto pluszīmi \[**++**\] laukā, lai izvērstu sarakstu, un pēc tam atlasiet *Pick-06* - *6. izdošanas vieta*).</span><span class="sxs-lookup"><span data-stu-id="eebfe-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="eebfe-253">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="eebfe-254">Iestatīt novietojuma direktīvas</span><span class="sxs-lookup"><span data-stu-id="eebfe-254">Set up location directives</span></span>

<span data-ttu-id="eebfe-255">Lai atbalstītu slotu veidošanas izdošanas, ir jāiestata vismaz viena novietojuma direktīva.</span><span class="sxs-lookup"><span data-stu-id="eebfe-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="eebfe-256">Izmantojiet šajā sadaļā pieejamās procedūras, lai izveidotu jaunu *papildināšanas novietojuma direktīvu* slotu veidošanas izdošanas gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="eebfe-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="eebfe-257">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="eebfe-258">Kreisajā rūtī, laukā **Darba pasūtījuma veids** atlasiet *Papildināšana*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="eebfe-259">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eebfe-260">Jaunās novietojuma direktīvas galvenes laukā **Nosaukums** ievadiet *61. slotu veidošanas izdošana*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="eebfe-261">Laukā **Kārtas numurs** akceptējiet noklusējuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="eebfe-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="eebfe-262">Novietojuma direktīvas kopsavilkuma cilnes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="eebfe-263">Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="eebfe-264">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="eebfe-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="eebfe-265">**Darba veids:** _Izdošana_</span><span class="sxs-lookup"><span data-stu-id="eebfe-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="eebfe-266">**Vieta:** _6_</span><span class="sxs-lookup"><span data-stu-id="eebfe-266">**Site:** _6_</span></span>
    - <span data-ttu-id="eebfe-267">**Noliktava:** _61_</span><span class="sxs-lookup"><span data-stu-id="eebfe-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="eebfe-268">**Direktīvas kods:** _slotu veidošana_</span><span class="sxs-lookup"><span data-stu-id="eebfe-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="eebfe-269">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="eebfe-270">Rindu kopsavilkuma cilnes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="eebfe-271">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, lai izveidotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="eebfe-272">Jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="eebfe-273">**No daudzuma:** _0_</span><span class="sxs-lookup"><span data-stu-id="eebfe-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="eebfe-274">**Līdz daudzumam:** _1 000 000_</span><span class="sxs-lookup"><span data-stu-id="eebfe-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="eebfe-275">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="eebfe-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="eebfe-276">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="eebfe-277">Novietojuma direktīvas darbību kopsavilkuma cilnes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="eebfe-278">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai izveidotu rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="eebfe-279">Jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-279">On the new line, set the following values.</span></span> <span data-ttu-id="eebfe-280">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="eebfe-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="eebfe-281">**Kārtas numurs:** akceptējiet noklusējuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="eebfe-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="eebfe-282">**Nosaukums:** _lielapjoma_</span><span class="sxs-lookup"><span data-stu-id="eebfe-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="eebfe-283">**Stratēģija:** _Nav_</span><span class="sxs-lookup"><span data-stu-id="eebfe-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="eebfe-284">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="eebfe-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="eebfe-285">Atlasiet **Saglabāt**, lai padarītu pieejamu pogu **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="eebfe-286">Rediģēt vaicājumu</span><span class="sxs-lookup"><span data-stu-id="eebfe-286">Edit the query</span></span>

1. <span data-ttu-id="eebfe-287">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="eebfe-288">Cilnē **Diapazons** atlasiet **Pievienot**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="eebfe-289">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-290">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="eebfe-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="eebfe-291">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="eebfe-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="eebfe-292">**Lauks:** *Zonas ID*</span><span class="sxs-lookup"><span data-stu-id="eebfe-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="eebfe-293">**Kritēriji:** *lielapjoma* (atlasiet dubulto pluszīmi \[**++**\] laukā, lai izvērstu sarakstu, un pēc tam atlasiet *Lielapjoma*.)</span><span class="sxs-lookup"><span data-stu-id="eebfe-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="eebfe-294">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="eebfe-295">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="eebfe-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="eebfe-296">Scenārija iestatīšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-296">Set up the scenario</span></span>

<span data-ttu-id="eebfe-297">Šim scenārijam izmantojiet iebūvēto datu paraugu un izveidojiet ierakstus, kas ir raksturoti šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="eebfe-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="eebfe-298">USMF datu parauga izmantošana</span><span class="sxs-lookup"><span data-stu-id="eebfe-298">Use the USMF sample data</span></span>

<span data-ttu-id="eebfe-299">Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="eebfe-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="eebfe-300">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="eebfe-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="eebfe-301">Pieprasījuma izveide</span><span class="sxs-lookup"><span data-stu-id="eebfe-301">Create demand</span></span>

<span data-ttu-id="eebfe-302">Izpildiet šīs darbības, lai izveidotu pieprasījumu, kuram lietosit slotu veidošanu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="eebfe-303">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="eebfe-304">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="eebfe-305">Dialoglodziņā **Pārdošanas pasūtījuma izveide** **klienta konta** laukā atlasiet _US-007_.</span><span class="sxs-lookup"><span data-stu-id="eebfe-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="eebfe-306">Laukā **Noliktava** atlasiet _61_.</span><span class="sxs-lookup"><span data-stu-id="eebfe-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="eebfe-307">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-307">Select **OK**.</span></span>
1. <span data-ttu-id="eebfe-308">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="eebfe-308">The new sales order is opened.</span></span> <span data-ttu-id="eebfe-309">Tajā ir ietverta tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="eebfe-310">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="eebfe-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-311">**Krājums:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="eebfe-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="eebfe-312">**Daudzums:** _20_</span><span class="sxs-lookup"><span data-stu-id="eebfe-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="eebfe-313">Atlasiet **Pievienot rindu**, lai pievienotu jaunu rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="eebfe-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="eebfe-314">**Krājums:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="eebfe-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="eebfe-315">**Daudzums:** _8_</span><span class="sxs-lookup"><span data-stu-id="eebfe-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="eebfe-316">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-316">Select **Save**.</span></span>
1. <span data-ttu-id="eebfe-317">Atlasiet **Jauns**, lai izveidotu otro pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="eebfe-318">Dialoglodziņā **Pārdošanas pasūtījuma izveide** **klienta konta** laukā atlasiet _US-008_.</span><span class="sxs-lookup"><span data-stu-id="eebfe-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="eebfe-319">Laukā **Noliktava** atlasiet _61_.</span><span class="sxs-lookup"><span data-stu-id="eebfe-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="eebfe-320">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="eebfe-320">The new sales order is opened.</span></span> <span data-ttu-id="eebfe-321">Tajā ir ietverta tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="eebfe-322">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="eebfe-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="eebfe-323">**Krājums:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="eebfe-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="eebfe-324">**Daudzums:** _1_</span><span class="sxs-lookup"><span data-stu-id="eebfe-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="eebfe-325">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="eebfe-326">Tipiska slotu veidošanas scenārija apskate</span><span class="sxs-lookup"><span data-stu-id="eebfe-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="eebfe-327">Kad visi priekšnosacījuma elementi ir ieviesti, kā tas tika izklāstīts iepriekšējā sadaļā, jūs esat gatavs izmēģināt līdzekli, izpildot katru šajā sadaļā norādīto uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="eebfe-328">Ģenerēt pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="eebfe-328">Generate demand</span></span>

1. <span data-ttu-id="eebfe-329">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Slotu veidošanas veidnes** un atlasiet slotu veidošanas veidni, ko izveidojāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="eebfe-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="eebfe-330">Darbību rūtī atlasiet **Ģenerēt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="eebfe-331">Šī komanda novērtē visu pieprasījumu, kas atrodas sistēmā un atbilst slotu veidošanas veidnes vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="eebfe-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="eebfe-332">Pēc tam kopējais pieprasījums no visiem pasūtījumiem tiek konsolidēts vienā rindā katram daudzumam/mērvienībai.</span><span class="sxs-lookup"><span data-stu-id="eebfe-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="eebfe-333">Kad process ir pabeigts, tiek parādīts informācijas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="eebfe-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="eebfe-334">Slotu veidošanas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="eebfe-334">Slotting demand</span></span>

<span data-ttu-id="eebfe-335">*Slotu veidošanas pieprasījums* parāda pieprasījuma ģenerēšanas rezultātus, pamatojoties uz slotu veidošanas veidnes iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="eebfe-336">Darbību rūtī atlasiet **Slotu veidošanas pieprasījums**, lai skatītu rezultātus no komandas **Ģenerēt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="eebfe-337">Slotu veidošanas pieprasījumā esošās rindas var rediģēt.</span><span class="sxs-lookup"><span data-stu-id="eebfe-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="eebfe-338">Varat dzēst rindu, pievienot jaunu rindu vai rediģēt detalizētu informāciju par rindu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="eebfe-339">Pieprasījumu varat rediģēt manuāli vai to importēt no ārējās sistēmas, izmantojot datu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="eebfe-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="eebfe-340">Viss, kas būs iekļauts slotu veidošanas pieprasījumā, tiks izmantots nākamajā darbībā neatkarīgi no izcelsmes vietas.</span><span class="sxs-lookup"><span data-stu-id="eebfe-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="eebfe-341">Atrast pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="eebfe-341">Locate demand</span></span>

<span data-ttu-id="eebfe-342">Pēc pieprasījuma ģenerēšanas izmantojiet komandu **Meklēt pieprasījumu**, lai ģenerētu *slotu veidošanas plānu*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="eebfe-343">Darbību rūtī atlasiet **Meklēt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="eebfe-344">Tiek izpildīts slotu veidošanas process.</span><span class="sxs-lookup"><span data-stu-id="eebfe-344">The slotting process runs.</span></span> <span data-ttu-id="eebfe-345">Kad process ir pabeigts, tiek parādīts informācijas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="eebfe-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="eebfe-346">Slotu veidošanas plāns</span><span class="sxs-lookup"><span data-stu-id="eebfe-346">Slotting plan</span></span>

<span data-ttu-id="eebfe-347">Slotu veidošanas plāns rāda novietojumu, kuram tika piešķirts katrs krājums/daudzums, vai tika izmantota pārpilde, izveidots palaišanas darbs un vai tika izmantota veidnes rinda.</span><span class="sxs-lookup"><span data-stu-id="eebfe-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="eebfe-348">*Visi pieprasījumi, kuriem nevar izveidot slotu, ir izcelti sarkanā krāsā.*</span><span class="sxs-lookup"><span data-stu-id="eebfe-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="eebfe-349">Darbību rūtī atlasiet **Slotu veidošanas plāns**, lai skatītu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="eebfe-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="eebfe-350">Tagad procesi **Ģenerēt pieprasījumu**, **Izvietot pieprasījumu** un **Palaist papildināšanu** darbojas smilškastē.</span><span class="sxs-lookup"><span data-stu-id="eebfe-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="eebfe-351">(Šie procesi ir pieejami no Darbību rūts lapā **Slotu veidošanas veidnes**.)</span><span class="sxs-lookup"><span data-stu-id="eebfe-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="eebfe-352">Procesi **Ģenerēt pieprasījumu**, **Izvietot pieprasījumu** un **Palaist papildināšanu** ir aprīkoti ar slēdzeni, lai nodrošinātu, ka tos nevar aktivizēt vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="eebfe-353">Pretējā gadījumā izmantotie dati var tikt dzēsti.</span><span class="sxs-lookup"><span data-stu-id="eebfe-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="eebfe-354">Procesi **Ģenerēt pieprasījumu** un **Izvietot pieprasījumu** parāda brīdinājumu, ja izpilde neģenerēja ierakstus vai ja ierakstos trūkst informācijas.</span><span class="sxs-lookup"><span data-stu-id="eebfe-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="eebfe-355">Kad atlasāt **Slotu veidošanas plāns**, lapas darbību rūtī nav pogu **Jauns** **Rediģēt** vai **Dzēst**, jo datu avotu nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="eebfe-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="eebfe-356">Kad atlasāt **Palaist papildināšanu**, sistēma validē atlasīto slota veidni un procesus.</span><span class="sxs-lookup"><span data-stu-id="eebfe-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="eebfe-357">Papildināšana izveide</span><span class="sxs-lookup"><span data-stu-id="eebfe-357">Create replenishment</span></span>

<span data-ttu-id="eebfe-358">Pēc slotu veidošanas plāna izveides ir jāizveido *papildināšanas darbs*, pamatojoties uz plānu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="eebfe-359">Darbību rūtī atlasiet **Palaist papildināšanu**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="eebfe-360">Kad process ir pabeigts, tiek parādīts informācijas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="eebfe-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="eebfe-361">Šis ziņojums norāda galveņu skaitu, kas tika izveidotas darba būvējuma ID.</span><span class="sxs-lookup"><span data-stu-id="eebfe-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="eebfe-362">Novietojuma direktīvas, kas tiks izmantotas, ir identificētas, pamatojoties uz katrā veidnes rindā norādīto direktīvas kodu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="eebfe-363">Padomi</span><span class="sxs-lookup"><span data-stu-id="eebfe-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="eebfe-364">Automātiskas slotu veidošanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="eebfe-364">Set up automatic slotting</span></span>

<span data-ttu-id="eebfe-365">Kad visi nepieciešamie elementi ir ieviesti, varat izpildīt tālāk norādītās darbības, lai iestatītu slotu veidošanas automātisku izpildi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="eebfe-366">Dodieties uz **Noliktavas pārvaldība \> Papildināšana \> Izpildīt slotu veidošanu**.</span><span class="sxs-lookup"><span data-stu-id="eebfe-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="eebfe-367">Norādiet izpildāmās slotu veidošanas darbības.</span><span class="sxs-lookup"><span data-stu-id="eebfe-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="eebfe-368">Atlasiet vienu vai vairākas no tālāk norādītajām slotu veidošanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="eebfe-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="eebfe-369">Ģenerēt pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="eebfe-369">Generate demand</span></span>
    - <span data-ttu-id="eebfe-370">Atrast pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="eebfe-370">Locate demand</span></span>
    - <span data-ttu-id="eebfe-371">Izveidot papildināšanas darbu</span><span class="sxs-lookup"><span data-stu-id="eebfe-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="eebfe-372">Slotu veidošanas darbības ir progresīvas.</span><span class="sxs-lookup"><span data-stu-id="eebfe-372">The slotting steps are progressive.</span></span> <span data-ttu-id="eebfe-373">Ja vēlaties atlasīt *Meklēt pieprasījumu*, vispirms ir jāatlasa *Ģenerēt pieprasījumu*.</span><span class="sxs-lookup"><span data-stu-id="eebfe-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="eebfe-374">Norādiet, kura slotu veidošanas veidne ir jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="eebfe-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="eebfe-375">Ja vēlaties, varat iestatīt automātisku periodiskuma izpildi.</span><span class="sxs-lookup"><span data-stu-id="eebfe-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="eebfe-376">Scenārijā iekļautajiem uzdevumiem **neiestatiet** automātisku slotu veidošanu.</span><span class="sxs-lookup"><span data-stu-id="eebfe-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
