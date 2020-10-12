---
title: Krājuma konsolidācija – novietojuma izmantojums
description: Šajā tēmā ir sniegta informācija par funkcionalitāti, kas noliktavu pārvaldniekiem atvieglo iespēju skatīt un filtrēt noliktavas novietojumu tilpuma izmantojumu. Pārvaldnieki var atlasīt novietojumus un izveidot krājumu pārvietošanas darbu tieši no lapas Krājuma konsolidācija, lai konsolidētu krājumus, un tādējādi labāk izmantotu noliktavas telpu.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5e4172a8d3f82e6eeb8868aac87abd183a94c088
ms.sourcegitcommit: 14b554b43b9d86152ef27fdde6141589bcaf1161
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/16/2020
ms.locfileid: "3598789"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="1bab9-104">Krājuma konsolidācija – novietojuma izmantojums</span><span class="sxs-lookup"><span data-stu-id="1bab9-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1bab9-105">Šajā tēmā ir sniegta informācija par funkcionalitāti, kas noliktavu pārvaldniekiem atvieglo iespēju skatīt un filtrēt noliktavas novietojumu tilpuma izmantojumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="1bab9-106">Pārvaldnieki var atlasīt novietojumus un izveidot krājumu pārvietošanas darbu tieši no lapas **Krājuma konsolidācija**, lai konsolidētu krājumus, un tādējādi labāk izmantotu noliktavas telpu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="1bab9-107">Līdzekļu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="1bab9-107">Turn on the features</span></span>

<span data-ttu-id="1bab9-108">Lai varētu izmantot šajā tēmā aprakstītos līdzekļus, tie ir jāieslēdz jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="1bab9-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="1bab9-109">Administratori var izmantot darbvietu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai pārbaudītu līdzekļu statusu un tos ieslēgtu, ja tas nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="1bab9-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="1bab9-110">Ieslēdziet abus šos līdzekļus, tādā secībā, kādā tie ir norādīti.</span><span class="sxs-lookup"><span data-stu-id="1bab9-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="1bab9-111">(Abi līdzekļi ir paredzēti modulim **Noliktavas pārvaldība**.)</span><span class="sxs-lookup"><span data-stu-id="1bab9-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="1bab9-112">Noliktavas vietas statuss</span><span class="sxs-lookup"><span data-stu-id="1bab9-112">Warehouse location status</span></span>
2. <span data-ttu-id="1bab9-113">Krājumu konsolidācijas novietojuma utilizācija</span><span class="sxs-lookup"><span data-stu-id="1bab9-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="1bab9-114">Noliktavas vietas statuss</span><span class="sxs-lookup"><span data-stu-id="1bab9-114">Warehouse location status</span></span>

<span data-ttu-id="1bab9-115">Līdzeklis *Noliktavas novietojuma statuss* pievieno četrus jaunus laukus lapai **Novietojumi**, lai izsekotu papildu informācijai par pašreizējo novietojuma stāvokli:</span><span class="sxs-lookup"><span data-stu-id="1bab9-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="1bab9-116">**Krājuma numurs** — pašlaik novietojumā esošais krājums.</span><span class="sxs-lookup"><span data-stu-id="1bab9-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="1bab9-117">Ja novietojumā ir vairāki krājumi, šis lauks būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="1bab9-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="1bab9-118">**Pēdējās aktivitātes datums un laiks** — pēdējā noliktavas darījuma laikspiedols, kas tika veikts saistībā ar novietojumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="1bab9-119">**Vecumstruktūras datums** — datums, kad noliktavā tika ievietots krājums novietojumā.</span><span class="sxs-lookup"><span data-stu-id="1bab9-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="1bab9-120">Datums tiek aprēķināts, pamatojoties uz noliktavas vienības vecumstruktūras datumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="1bab9-121">Lai arī šis datums ir precīzs novietojumiem, kurus var izsekot pēc noliktavas vienības, tas var nebūt precīzs novietojumiem, kurus nevar izsekot pēc noliktavas vienības.</span><span class="sxs-lookup"><span data-stu-id="1bab9-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="1bab9-122">**Novietojuma statuss** — novietojuma statuss.</span><span class="sxs-lookup"><span data-stu-id="1bab9-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="1bab9-123">Ir pieejamas četras vērtības:</span><span class="sxs-lookup"><span data-stu-id="1bab9-123">Four values are available:</span></span>

    - <span data-ttu-id="1bab9-124">**Nav noteikts** – novietojuma profils neizseko statusu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="1bab9-125">Tāpēc pašreizējais statuss ir nezināms.</span><span class="sxs-lookup"><span data-stu-id="1bab9-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="1bab9-126">**Tukšs**– novietojumā pašlaik nav neviena krājuma.</span><span class="sxs-lookup"><span data-stu-id="1bab9-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="1bab9-127">**Izdošana** – izejošās darbības ir veiktas attiecībā pret novietojumu, kopš tas pēdējoreiz bija tukšs.</span><span class="sxs-lookup"><span data-stu-id="1bab9-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="1bab9-128">**Glabāšana** – ir veiktas tikai ienākošās transakcijas, jo pēdējoreiz novietojums bija tukšs.</span><span class="sxs-lookup"><span data-stu-id="1bab9-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="1bab9-129">Šie lauki sniedz noliktavas pārvaldniekiem iespēju iegūt labāku pārskatu par noliktavas novietojumu statusu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="1bab9-130">Tāpat tie ļauj veikt detalizētāku pārskatu veidošanu un filtrēšanu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="1bab9-131">Krājuma konsolidācijas un novietojuma izmantojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1bab9-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="1bab9-132">Šajā sadaļā ir aprakstīts, kā sagatavot sistēmu, lai izmantotu krājuma konsolidāciju un novietojuma izmantojumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="1bab9-133">Procedūrās tiek izmantoti vērtību paraugi no standarta demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="1bab9-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="1bab9-134">Ja plānojat strādāt ar scenārija piemēru, kas ir sniegts tālāk šajā tēmā, atlasiet **USMF** juridisko personu (kurā ir standarta demonstrācijas dati) un izveidojiet katru šajā sadaļā aprakstīto ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="1bab9-135">Ja neplānojat strādāt ar scenārija piemēru, šeit sniegtās vērtības var uzskatīt par tādu iestatīšanas veidu piemēriem, kas ir jāpabeidz, lai izmantotu līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="1bab9-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="1bab9-136">Izlaistā prece</span><span class="sxs-lookup"><span data-stu-id="1bab9-136">Released product</span></span>

1. <span data-ttu-id="1bab9-137">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1bab9-138">Laukā **Krājuma kods** atlasiet *M9201* un atveriet informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="1bab9-139">Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Fiziskās dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="1bab9-140">Lapā **Fiziskās dimensijas** darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="1bab9-141">Režģim tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="1bab9-141">A new line is added to the grid.</span></span> <span data-ttu-id="1bab9-142">Lauks **Krājuma kods** ir priekšiestatīts.</span><span class="sxs-lookup"><span data-stu-id="1bab9-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="1bab9-143">Laukā **Vienība** atlasiet *katra*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="1bab9-144">Atlikušie rindas lauki tiek iestatīti automātiski.</span><span class="sxs-lookup"><span data-stu-id="1bab9-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="1bab9-145">Atlasiet **Saglabāt** un aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="1bab9-146">Novietojuma profils</span><span class="sxs-lookup"><span data-stu-id="1bab9-146">Location profile</span></span>

1. <span data-ttu-id="1bab9-147">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="1bab9-148">Novietojuma profilu sarakstā atlasiet **FLOOR-05**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="1bab9-149">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="1bab9-150">Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, vai abas šīs opcijas ir iestatītas uz *Jā*:</span><span class="sxs-lookup"><span data-stu-id="1bab9-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="1bab9-151">Iespējot krājumu vietā</span><span class="sxs-lookup"><span data-stu-id="1bab9-151">Enable item in location</span></span>
    - <span data-ttu-id="1bab9-152">Iespējot vietas statusu</span><span class="sxs-lookup"><span data-stu-id="1bab9-152">Enable location status</span></span>

1. <span data-ttu-id="1bab9-153">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1bab9-154">Ja opcijas **Iespējot krājumu novietojumā** un **Iespējot novietojuma statusu** jau ir iestatītas uz *Jā*, pārejiet pie instrukciju 10. darbības, lai iestatītu kopsavilkuma cilni **Dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="1bab9-155">Ja opcijas jau nav iestatītas uz *Jā*, tad pēc to manuālas iestatīšanas, palaidiet konsekvences pārbaudi modulim **Noliktavas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="1bab9-156">Šādā gadījumā turpiniet ar nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="1bab9-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="1bab9-157">Lai palaistu konsekvences pārbaudi, dodieties uz **Sistēmas administrēšana \> Periodiskie uzdevumi \> Datu bāze \> Konsekvences pārbaude**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="1bab9-158">Dialoglodziņā **Konsekvences pārbaude** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1bab9-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1bab9-159">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="1bab9-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="1bab9-160">**Pārbaudīt/Labot:** *Pārbaudīt*</span><span class="sxs-lookup"><span data-stu-id="1bab9-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="1bab9-161">**No datuma:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="1bab9-162">**Noliktavas novietojuma statusa konsekvences pārbaude:** atzīmējiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="1bab9-163">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="1bab9-164">Kad konsekvences pārbaude ir pabeigta, tiek saņemts paziņojums.</span><span class="sxs-lookup"><span data-stu-id="1bab9-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="1bab9-165">Atveriet [darbību centru](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications), lai skatītu ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="1bab9-166">Atlasiet **Ziņojuma informācija**, lai skatītu informāciju.</span><span class="sxs-lookup"><span data-stu-id="1bab9-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="1bab9-167">Ja konsekvences pārbaudes ziņojums norāda, “Novietojumam XXXX konstatēta nepareiza novietojuma statusa informācija noliktavā XX”, konsekvences pārbaude ir jāpalaiž vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="1bab9-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="1bab9-168">Šoreiz lauku **Pārbaudīt/Labot** iestatiet uz *Labot kļūdu*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="1bab9-169">Skatiet ziņojumus, lai pārliecinātos, vai nav atrastas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="1bab9-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="1bab9-170">Pabeidziet novietojuma profila iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="1bab9-171">Atgriezieties sadaļā **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma profili**, atlasiet novietojuma profilu **FLOOR-05**, un pēc tam darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="1bab9-172">Kopsavilkuma cilnē **Dimensijas** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1bab9-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="1bab9-173">**Tilpuma izmantojuma procentuālā vērtība:** *100*</span><span class="sxs-lookup"><span data-stu-id="1bab9-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="1bab9-174">**Krājumu novietojumam izmantotā tilpuma metode:** *izmantot novietojumu tilpumu*</span><span class="sxs-lookup"><span data-stu-id="1bab9-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="1bab9-175">**Faktiskais novietojuma augstums:** *10*</span><span class="sxs-lookup"><span data-stu-id="1bab9-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="1bab9-176">**Faktiskais novietojuma platums:** *10*</span><span class="sxs-lookup"><span data-stu-id="1bab9-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="1bab9-177">**Faktiskais novietojuma dziļums:** *10*</span><span class="sxs-lookup"><span data-stu-id="1bab9-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="1bab9-178">**Maksimālais svars:** *100*</span><span class="sxs-lookup"><span data-stu-id="1bab9-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="1bab9-179">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="1bab9-180">Mobilās ierīces izvēlnes vienumi</span><span class="sxs-lookup"><span data-stu-id="1bab9-180">Mobile device menu items</span></span>

1. <span data-ttu-id="1bab9-181">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="1bab9-182">Darbību rūtī atlasiet **Jauns**, lai izveidotu kārtošanas izvēlnes elementu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="1bab9-183">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1bab9-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="1bab9-184">**Izvēlnes elementa nosaukums:** *Koriģēt ienākošo*</span><span class="sxs-lookup"><span data-stu-id="1bab9-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="1bab9-185">**Nosaukums:** *Koriģēt ienākošo*</span><span class="sxs-lookup"><span data-stu-id="1bab9-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="1bab9-186">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="1bab9-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="1bab9-187">**Izmantot esošo darbu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="1bab9-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="1bab9-188">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1bab9-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="1bab9-189">**Darba izveides process:** *Ienākošā korekcija*</span><span class="sxs-lookup"><span data-stu-id="1bab9-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="1bab9-190">**Krājumu korekciju veidi:** *Koriģēt ienākošo*</span><span class="sxs-lookup"><span data-stu-id="1bab9-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="1bab9-191">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="1bab9-192">Mobilās ierīces izvēlne</span><span class="sxs-lookup"><span data-stu-id="1bab9-192">Mobile device menu</span></span>

1. <span data-ttu-id="1bab9-193">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="1bab9-194">Izvēļņu sarakstā atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="1bab9-195">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="1bab9-196">Sarakstā **Pieejamās izvēlnes un izvēļņu elementi** atrodiet un atlasiet izvēlnes elementu **Koriģēt ienākošo**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="1bab9-197">Atlasiet bultiņas pa labi pogu, lai pārvietotu **Koriģēt ienākošo** uz sarakstu **Izvēlnes struktūra**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="1bab9-198">Šādā veidā jūs pievienojat jauno izvēlnes elementu atlasītajai izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="1bab9-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="1bab9-199">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="1bab9-200">Kustības veidi</span><span class="sxs-lookup"><span data-stu-id="1bab9-200">Movement types</span></span>

1. <span data-ttu-id="1bab9-201">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Krājumi \> Kustības veidi**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="1bab9-202">Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1bab9-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="1bab9-203">**Kustības veida kods:** *CONSOLIDATE*</span><span class="sxs-lookup"><span data-stu-id="1bab9-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="1bab9-204">**Apraksts:** *Novietojumu konsolidēšana*</span><span class="sxs-lookup"><span data-stu-id="1bab9-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="1bab9-205">**Darba klases ID:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="1bab9-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="1bab9-206">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1bab9-207">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="1bab9-207">Example scenario</span></span>

<span data-ttu-id="1bab9-208">Šajā scenārijā tiek izmantota noliktavas programma mobilajā ierīcē, lai veiktu krājumu *ienākošo korekciju* diviem noliktavas novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="1bab9-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="1bab9-209">Krājumu pievienošana novietojumiem</span><span class="sxs-lookup"><span data-stu-id="1bab9-209">Add inventory to locations</span></span>

1. <span data-ttu-id="1bab9-210">Piesakieties mobilajā ierīcē kā lietotājs, kurš ir iestatīts noliktavai *51*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="1bab9-211">Dodieties uz **Krājumi \> Koriģēt ienākošo**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="1bab9-212">Tagad ievadiet pirmā novietojuma korekciju.</span><span class="sxs-lookup"><span data-stu-id="1bab9-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="1bab9-213">Uzdevumā **Ienākošā korekcija** atlasiet novietojumu, kuram veikt krājumu korekciju.</span><span class="sxs-lookup"><span data-stu-id="1bab9-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="1bab9-214">Laukā **LOC** atlasiet *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="1bab9-215">Apstipriniet novietojumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-215">Confirm the location.</span></span>
1. <span data-ttu-id="1bab9-216">Izveidojiet noliktavas vienības ID krājumam, kas tiks pievienots novietojumam.</span><span class="sxs-lookup"><span data-stu-id="1bab9-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="1bab9-217">Laukā **LP** ievadiet *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="1bab9-218">Apstipriniet noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="1bab9-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="1bab9-219">Ievadiet krājumu, kas tiks pievienots noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="1bab9-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="1bab9-220">Laukā **ITEM** ievadiet *M9201*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="1bab9-221">Apstipriniet krājumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-221">Confirm the item.</span></span>
1. <span data-ttu-id="1bab9-222">Ievadiet krājuma daudzumu, kas tiks pievienots.</span><span class="sxs-lookup"><span data-stu-id="1bab9-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="1bab9-223">Laukā **QTY** ievadiet *10*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="1bab9-224">Apstipriniet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-224">Confirm the quantity.</span></span>

    <span data-ttu-id="1bab9-225">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="1bab9-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="1bab9-226">Tagad ievadiet otrā novietojuma korekciju.</span><span class="sxs-lookup"><span data-stu-id="1bab9-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="1bab9-227">Uzdevumā **Ienākošā korekcija** atlasiet novietojumu, kuram veikt krājumu korekciju.</span><span class="sxs-lookup"><span data-stu-id="1bab9-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="1bab9-228">Laukā **LOC** atlasiet *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="1bab9-229">Apstipriniet novietojumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-229">Confirm the location.</span></span>
1. <span data-ttu-id="1bab9-230">Izveidojiet noliktavas vienības ID krājumam, kas tiks pievienots novietojumam.</span><span class="sxs-lookup"><span data-stu-id="1bab9-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="1bab9-231">Laukā **LP** ievadiet *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="1bab9-232">Apstipriniet noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="1bab9-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="1bab9-233">Ievadiet krājumu, kas tiks pievienots noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="1bab9-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="1bab9-234">Laukā **ITEM** ievadiet *M9201*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="1bab9-235">Apstipriniet krājumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-235">Confirm the item.</span></span>
1. <span data-ttu-id="1bab9-236">Ievadiet krājuma daudzumu, kas tiks pievienots.</span><span class="sxs-lookup"><span data-stu-id="1bab9-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="1bab9-237">Laukā **QTY** ievadiet *15*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="1bab9-238">Apstipriniet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-238">Confirm the quantity.</span></span>

    <span data-ttu-id="1bab9-239">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="1bab9-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="1bab9-240">Atlasiet pogu Izvēlne (dažreiz saukta par hamburgeru vai hamburgera pogu) un pēc tam atlasiet **Atcelt**, lai izietu no uzdevuma **Ienākošā korekcija**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="1bab9-241">Novietojumu konsolidēšana</span><span class="sxs-lookup"><span data-stu-id="1bab9-241">Consolidate locations</span></span>

1. <span data-ttu-id="1bab9-242">Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Krājuma konsolidācija**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="1bab9-243">Galvenē atlasiet noliktavu, kurai veikt konsolidēšanu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="1bab9-244">Laukā **Noliktava** ievadiet *51*.</span><span class="sxs-lookup"><span data-stu-id="1bab9-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="1bab9-245">Katram novietojumam, kurā tika koriģēts krājums *M9201*, tiek parādīts ieraksts.</span><span class="sxs-lookup"><span data-stu-id="1bab9-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="1bab9-246">Kolonna **Izmantojuma procentuālā vērtība** rāda tilpuma izmantojumu katram novietojumam.</span><span class="sxs-lookup"><span data-stu-id="1bab9-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="1bab9-247">Lai konsolidētu krājumus, atlasiet visus konsolidējamos novietojumus, un pēc tam darbību rūtī atlasiet **Krājumu konsolidēšana**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="1bab9-248">Dialoglodziņā **Krājumu konsolidēšana** norādiet novietojumu un kustības veidu, kas jāizmanto, lai izveidotu krājumu pārvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="1bab9-249">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1bab9-249">Set the following values:</span></span>

    - <span data-ttu-id="1bab9-250">**Novietojums:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="1bab9-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="1bab9-251">**Kustības veida kods:** *CONSOLIDATE*</span><span class="sxs-lookup"><span data-stu-id="1bab9-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="1bab9-252">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-252">Select **OK**.</span></span>
1. <span data-ttu-id="1bab9-253">Tiks saņemts informatīvs ziņojums, kurā norādīts izveidotais pārvietošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="1bab9-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="1bab9-254">Pierakstiet pārvietošanas darba ID.</span><span class="sxs-lookup"><span data-stu-id="1bab9-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="1bab9-255">Pārvietošanas darba skatīšana</span><span class="sxs-lookup"><span data-stu-id="1bab9-255">View movement work</span></span>

1. <span data-ttu-id="1bab9-256">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="1bab9-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="1bab9-257">Skatiet izveidoto darbu.</span><span class="sxs-lookup"><span data-stu-id="1bab9-257">View the work that was created.</span></span> <span data-ttu-id="1bab9-258">Izmantojiet pārvietošanas darba ID no krājumu konsolidācijas, lai filtrētu vai meklētu darbu režģī.</span><span class="sxs-lookup"><span data-stu-id="1bab9-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="1bab9-259">Šajā scenārijā esošs novietojums, kurā bija krājumi, tika izmantots kā krājumu konsolidācijas novietojums.</span><span class="sxs-lookup"><span data-stu-id="1bab9-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="1bab9-260">Tādēļ tika izveidots tikai viens darba ID.</span><span class="sxs-lookup"><span data-stu-id="1bab9-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="1bab9-261">Sistēma izveido vienu darba ID katrai kustībai, kas ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="1bab9-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="1bab9-262">Ja norādāt novietojumu, kurā jau ir krājumi, tiek izveidots tikai viens darba ID.</span><span class="sxs-lookup"><span data-stu-id="1bab9-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="1bab9-263">Ja norādāt jaunu novietojumu, tiek izveidoti divi darba ID.</span><span class="sxs-lookup"><span data-stu-id="1bab9-263">If you specify a new location, two work IDs are created.</span></span>