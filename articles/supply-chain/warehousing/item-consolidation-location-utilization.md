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
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6edabc51981d8935672b44e53b453cfbaca9031b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004656"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="f287f-104">Krājuma konsolidācija – novietojuma izmantojums</span><span class="sxs-lookup"><span data-stu-id="f287f-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f287f-105">Šajā tēmā ir sniegta informācija par funkcionalitāti, kas noliktavu pārvaldniekiem atvieglo iespēju skatīt un filtrēt noliktavas novietojumu tilpuma izmantojumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="f287f-106">Pārvaldnieki var atlasīt novietojumus un izveidot krājumu pārvietošanas darbu tieši no lapas **Krājuma konsolidācija**, lai konsolidētu krājumus, un tādējādi labāk izmantotu noliktavas telpu.</span><span class="sxs-lookup"><span data-stu-id="f287f-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="f287f-107">Līdzekļu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="f287f-107">Turn on the features</span></span>

<span data-ttu-id="f287f-108">Lai varētu izmantot šajā tēmā aprakstītos līdzekļus, tie ir jāieslēdz jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="f287f-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="f287f-109">Administratori var izmantot darbvietu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai pārbaudītu līdzekļu statusu un tos ieslēgtu, ja tas nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="f287f-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="f287f-110">Ieslēdziet abus šos līdzekļus, tādā secībā, kādā tie ir norādīti.</span><span class="sxs-lookup"><span data-stu-id="f287f-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="f287f-111">(Abi līdzekļi ir paredzēti modulim **Noliktavas pārvaldība**.)</span><span class="sxs-lookup"><span data-stu-id="f287f-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="f287f-112">Noliktavas vietas statuss</span><span class="sxs-lookup"><span data-stu-id="f287f-112">Warehouse location status</span></span>
2. <span data-ttu-id="f287f-113">Krājumu konsolidācijas novietojuma utilizācija</span><span class="sxs-lookup"><span data-stu-id="f287f-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="f287f-114">Noliktavas vietas statuss</span><span class="sxs-lookup"><span data-stu-id="f287f-114">Warehouse location status</span></span>

<span data-ttu-id="f287f-115">Līdzeklis *Noliktavas novietojuma statuss* pievieno četrus jaunus laukus lapai **Novietojumi**, lai izsekotu papildu informācijai par pašreizējo novietojuma stāvokli:</span><span class="sxs-lookup"><span data-stu-id="f287f-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="f287f-116">**Krājuma numurs** — pašlaik novietojumā esošais krājums.</span><span class="sxs-lookup"><span data-stu-id="f287f-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="f287f-117">Ja novietojumā ir vairāki krājumi, šis lauks būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="f287f-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="f287f-118">**Pēdējās aktivitātes datums un laiks** — pēdējā noliktavas darījuma laikspiedols, kas tika veikts saistībā ar novietojumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="f287f-119">**Vecumstruktūras datums** — datums, kad noliktavā tika ievietots krājums novietojumā.</span><span class="sxs-lookup"><span data-stu-id="f287f-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="f287f-120">Datums tiek aprēķināts, pamatojoties uz noliktavas vienības vecumstruktūras datumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="f287f-121">Lai arī šis datums ir precīzs novietojumiem, kurus var izsekot pēc noliktavas vienības, tas var nebūt precīzs novietojumiem, kurus nevar izsekot pēc noliktavas vienības.</span><span class="sxs-lookup"><span data-stu-id="f287f-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="f287f-122">**Novietojuma statuss** — novietojuma statuss.</span><span class="sxs-lookup"><span data-stu-id="f287f-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="f287f-123">Ir pieejamas četras vērtības:</span><span class="sxs-lookup"><span data-stu-id="f287f-123">Four values are available:</span></span>

    - <span data-ttu-id="f287f-124">**Nav noteikts** – novietojuma profils neizseko statusu.</span><span class="sxs-lookup"><span data-stu-id="f287f-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="f287f-125">Tāpēc pašreizējais statuss ir nezināms.</span><span class="sxs-lookup"><span data-stu-id="f287f-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="f287f-126">**Tukšs**– novietojumā pašlaik nav neviena krājuma.</span><span class="sxs-lookup"><span data-stu-id="f287f-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="f287f-127">**Izdošana** – izejošās darbības ir veiktas attiecībā pret novietojumu, kopš tas pēdējoreiz bija tukšs.</span><span class="sxs-lookup"><span data-stu-id="f287f-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="f287f-128">**Glabāšana** – ir veiktas tikai ienākošās transakcijas, jo pēdējoreiz novietojums bija tukšs.</span><span class="sxs-lookup"><span data-stu-id="f287f-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="f287f-129">Šie lauki sniedz noliktavas pārvaldniekiem iespēju iegūt labāku pārskatu par noliktavas novietojumu statusu.</span><span class="sxs-lookup"><span data-stu-id="f287f-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="f287f-130">Tāpat tie ļauj veikt detalizētāku pārskatu veidošanu un filtrēšanu.</span><span class="sxs-lookup"><span data-stu-id="f287f-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="f287f-131">Krājuma konsolidācijas un novietojuma izmantojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f287f-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="f287f-132">Šajā sadaļā ir aprakstīts, kā sagatavot sistēmu, lai izmantotu krājuma konsolidāciju un novietojuma izmantojumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="f287f-133">Procedūrās tiek izmantoti vērtību paraugi no standarta demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="f287f-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="f287f-134">Ja plānojat strādāt ar scenārija piemēru, kas ir sniegts tālāk šajā tēmā, atlasiet **USMF** juridisko personu (kurā ir standarta demonstrācijas dati) un izveidojiet katru šajā sadaļā aprakstīto ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f287f-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="f287f-135">Ja neplānojat strādāt ar scenārija piemēru, šeit sniegtās vērtības var uzskatīt par tādu iestatīšanas veidu piemēriem, kas ir jāpabeidz, lai izmantotu līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="f287f-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="f287f-136">Izlaistā prece</span><span class="sxs-lookup"><span data-stu-id="f287f-136">Released product</span></span>

1. <span data-ttu-id="f287f-137">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="f287f-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f287f-138">Laukā **Krājuma kods** atlasiet *M9201* un atveriet informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="f287f-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="f287f-139">Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Fiziskās dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="f287f-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="f287f-140">Lapā **Fiziskās dimensijas** darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f287f-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="f287f-141">Režģim tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="f287f-141">A new line is added to the grid.</span></span> <span data-ttu-id="f287f-142">Lauks **Krājuma kods** ir priekšiestatīts.</span><span class="sxs-lookup"><span data-stu-id="f287f-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="f287f-143">Laukā **Vienība** atlasiet *katra*.</span><span class="sxs-lookup"><span data-stu-id="f287f-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="f287f-144">Atlikušie rindas lauki tiek iestatīti automātiski.</span><span class="sxs-lookup"><span data-stu-id="f287f-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="f287f-145">Atlasiet **Saglabāt** un aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="f287f-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="f287f-146">Novietojuma profils</span><span class="sxs-lookup"><span data-stu-id="f287f-146">Location profile</span></span>

1. <span data-ttu-id="f287f-147">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.</span><span class="sxs-lookup"><span data-stu-id="f287f-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="f287f-148">Novietojuma profilu sarakstā atlasiet **FLOOR-05**.</span><span class="sxs-lookup"><span data-stu-id="f287f-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="f287f-149">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="f287f-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f287f-150">Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, vai abas šīs opcijas ir iestatītas uz *Jā*:</span><span class="sxs-lookup"><span data-stu-id="f287f-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="f287f-151">Iespējot krājumu vietā</span><span class="sxs-lookup"><span data-stu-id="f287f-151">Enable item in location</span></span>
    - <span data-ttu-id="f287f-152">Iespējot vietas statusu</span><span class="sxs-lookup"><span data-stu-id="f287f-152">Enable location status</span></span>

1. <span data-ttu-id="f287f-153">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f287f-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f287f-154">Ja opcijas **Iespējot krājumu novietojumā** un **Iespējot novietojuma statusu** jau ir iestatītas uz *Jā*, pārejiet pie instrukciju 10. darbības, lai iestatītu kopsavilkuma cilni **Dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="f287f-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="f287f-155">Ja opcijas jau nav iestatītas uz *Jā*, tad pēc to manuālas iestatīšanas, palaidiet konsekvences pārbaudi modulim **Noliktavas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="f287f-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="f287f-156">Šādā gadījumā turpiniet ar nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="f287f-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="f287f-157">Lai palaistu konsekvences pārbaudi, dodieties uz **Sistēmas administrēšana \> Periodiskie uzdevumi \> Datu bāze \> Konsekvences pārbaude**.</span><span class="sxs-lookup"><span data-stu-id="f287f-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="f287f-158">Dialoglodziņā **Konsekvences pārbaude** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="f287f-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f287f-159">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="f287f-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="f287f-160">**Pārbaudīt/Labot:** *Pārbaudīt*</span><span class="sxs-lookup"><span data-stu-id="f287f-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="f287f-161">**No datuma:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="f287f-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="f287f-162">**Noliktavas novietojuma statusa konsekvences pārbaude:** atzīmējiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="f287f-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="f287f-163">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f287f-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="f287f-164">Kad konsekvences pārbaude ir pabeigta, tiek saņemts paziņojums.</span><span class="sxs-lookup"><span data-stu-id="f287f-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="f287f-165">Atveriet [darbību centru](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications), lai skatītu ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="f287f-166">Atlasiet **Ziņojuma informācija**, lai skatītu informāciju.</span><span class="sxs-lookup"><span data-stu-id="f287f-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="f287f-167">Ja konsekvences pārbaudes ziņojums norāda, “Novietojumam XXXX konstatēta nepareiza novietojuma statusa informācija noliktavā XX”, konsekvences pārbaude ir jāpalaiž vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="f287f-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="f287f-168">Šoreiz lauku **Pārbaudīt/Labot** iestatiet uz *Labot kļūdu*.</span><span class="sxs-lookup"><span data-stu-id="f287f-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="f287f-169">Skatiet ziņojumus, lai pārliecinātos, vai nav atrastas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="f287f-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="f287f-170">Pabeidziet novietojuma profila iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="f287f-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="f287f-171">Atgriezieties sadaļā **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma profili**, atlasiet novietojuma profilu **FLOOR-05**, un pēc tam darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="f287f-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f287f-172">Kopsavilkuma cilnē **Dimensijas** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="f287f-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f287f-173">**Tilpuma izmantojuma procentuālā vērtība:** *100*</span><span class="sxs-lookup"><span data-stu-id="f287f-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="f287f-174">**Krājumu novietojumam izmantotā tilpuma metode:** *izmantot novietojumu tilpumu*</span><span class="sxs-lookup"><span data-stu-id="f287f-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="f287f-175">**Faktiskais novietojuma augstums:** *10*</span><span class="sxs-lookup"><span data-stu-id="f287f-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="f287f-176">**Faktiskais novietojuma platums:** *10*</span><span class="sxs-lookup"><span data-stu-id="f287f-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="f287f-177">**Faktiskais novietojuma dziļums:** *10*</span><span class="sxs-lookup"><span data-stu-id="f287f-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="f287f-178">**Maksimālais svars:** *100*</span><span class="sxs-lookup"><span data-stu-id="f287f-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="f287f-179">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f287f-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="f287f-180">Mobilās ierīces izvēlnes vienumi</span><span class="sxs-lookup"><span data-stu-id="f287f-180">Mobile device menu items</span></span>

1. <span data-ttu-id="f287f-181">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="f287f-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="f287f-182">Darbību rūtī atlasiet **Jauns**, lai izveidotu kārtošanas izvēlnes elementu.</span><span class="sxs-lookup"><span data-stu-id="f287f-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="f287f-183">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="f287f-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="f287f-184">**Izvēlnes elementa nosaukums:** *Koriģēt ienākošo*</span><span class="sxs-lookup"><span data-stu-id="f287f-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="f287f-185">**Nosaukums:** *Koriģēt ienākošo*</span><span class="sxs-lookup"><span data-stu-id="f287f-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="f287f-186">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="f287f-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="f287f-187">**Izmantot esošo darbu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="f287f-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="f287f-188">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="f287f-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f287f-189">**Darba izveides process:** *Ienākošā korekcija*</span><span class="sxs-lookup"><span data-stu-id="f287f-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="f287f-190">**Krājumu korekciju veidi:** *Koriģēt ienākošo*</span><span class="sxs-lookup"><span data-stu-id="f287f-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="f287f-191">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f287f-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="f287f-192">Mobilās ierīces izvēlne</span><span class="sxs-lookup"><span data-stu-id="f287f-192">Mobile device menu</span></span>

1. <span data-ttu-id="f287f-193">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="f287f-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="f287f-194">Izvēļņu sarakstā atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="f287f-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="f287f-195">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="f287f-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f287f-196">Sarakstā **Pieejamās izvēlnes un izvēļņu elementi** atrodiet un atlasiet izvēlnes elementu **Koriģēt ienākošo**.</span><span class="sxs-lookup"><span data-stu-id="f287f-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="f287f-197">Atlasiet bultiņas pa labi pogu, lai pārvietotu **Koriģēt ienākošo** uz sarakstu **Izvēlnes struktūra**.</span><span class="sxs-lookup"><span data-stu-id="f287f-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="f287f-198">Šādā veidā jūs pievienojat jauno izvēlnes elementu atlasītajai izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="f287f-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="f287f-199">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f287f-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="f287f-200">Kustības veidi</span><span class="sxs-lookup"><span data-stu-id="f287f-200">Movement types</span></span>

1. <span data-ttu-id="f287f-201">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Krājumi \> Kustības veidi**.</span><span class="sxs-lookup"><span data-stu-id="f287f-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="f287f-202">Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="f287f-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="f287f-203">**Kustības veida kods:** *CONSOLIDATE*</span><span class="sxs-lookup"><span data-stu-id="f287f-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="f287f-204">**Apraksts:** *Novietojumu konsolidēšana*</span><span class="sxs-lookup"><span data-stu-id="f287f-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="f287f-205">**Darba klases ID:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="f287f-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="f287f-206">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f287f-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f287f-207">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="f287f-207">Example scenario</span></span>

<span data-ttu-id="f287f-208">Šajā scenārijā tiek izmantota noliktavas programma mobilajā ierīcē, lai veiktu krājumu *ienākošo korekciju* diviem noliktavas novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="f287f-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="f287f-209">Krājumu pievienošana novietojumiem</span><span class="sxs-lookup"><span data-stu-id="f287f-209">Add inventory to locations</span></span>

1. <span data-ttu-id="f287f-210">Piesakieties mobilajā ierīcē kā lietotājs, kurš ir iestatīts noliktavai *51*.</span><span class="sxs-lookup"><span data-stu-id="f287f-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="f287f-211">Dodieties uz **Krājumi \> Koriģēt ienākošo**.</span><span class="sxs-lookup"><span data-stu-id="f287f-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="f287f-212">Tagad ievadiet pirmā novietojuma korekciju.</span><span class="sxs-lookup"><span data-stu-id="f287f-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="f287f-213">Uzdevumā **Ienākošā korekcija** atlasiet novietojumu, kuram veikt krājumu korekciju.</span><span class="sxs-lookup"><span data-stu-id="f287f-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="f287f-214">Laukā **LOC** atlasiet *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="f287f-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="f287f-215">Apstipriniet novietojumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-215">Confirm the location.</span></span>
1. <span data-ttu-id="f287f-216">Izveidojiet noliktavas vienības ID krājumam, kas tiks pievienots novietojumam.</span><span class="sxs-lookup"><span data-stu-id="f287f-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="f287f-217">Laukā **LP** ievadiet *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="f287f-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="f287f-218">Apstipriniet noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="f287f-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="f287f-219">Ievadiet krājumu, kas tiks pievienots noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="f287f-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="f287f-220">Laukā **ITEM** ievadiet *M9201*.</span><span class="sxs-lookup"><span data-stu-id="f287f-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="f287f-221">Apstipriniet krājumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-221">Confirm the item.</span></span>
1. <span data-ttu-id="f287f-222">Ievadiet krājuma daudzumu, kas tiks pievienots.</span><span class="sxs-lookup"><span data-stu-id="f287f-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="f287f-223">Laukā **QTY** ievadiet *10*.</span><span class="sxs-lookup"><span data-stu-id="f287f-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="f287f-224">Apstipriniet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-224">Confirm the quantity.</span></span>

    <span data-ttu-id="f287f-225">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="f287f-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="f287f-226">Tagad ievadiet otrā novietojuma korekciju.</span><span class="sxs-lookup"><span data-stu-id="f287f-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="f287f-227">Uzdevumā **Ienākošā korekcija** atlasiet novietojumu, kuram veikt krājumu korekciju.</span><span class="sxs-lookup"><span data-stu-id="f287f-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="f287f-228">Laukā **LOC** atlasiet *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="f287f-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="f287f-229">Apstipriniet novietojumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-229">Confirm the location.</span></span>
1. <span data-ttu-id="f287f-230">Izveidojiet noliktavas vienības ID krājumam, kas tiks pievienots novietojumam.</span><span class="sxs-lookup"><span data-stu-id="f287f-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="f287f-231">Laukā **LP** ievadiet *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="f287f-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="f287f-232">Apstipriniet noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="f287f-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="f287f-233">Ievadiet krājumu, kas tiks pievienots noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="f287f-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="f287f-234">Laukā **ITEM** ievadiet *M9201*.</span><span class="sxs-lookup"><span data-stu-id="f287f-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="f287f-235">Apstipriniet krājumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-235">Confirm the item.</span></span>
1. <span data-ttu-id="f287f-236">Ievadiet krājuma daudzumu, kas tiks pievienots.</span><span class="sxs-lookup"><span data-stu-id="f287f-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="f287f-237">Laukā **QTY** ievadiet *15*.</span><span class="sxs-lookup"><span data-stu-id="f287f-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="f287f-238">Apstipriniet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f287f-238">Confirm the quantity.</span></span>

    <span data-ttu-id="f287f-239">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="f287f-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="f287f-240">Atlasiet pogu Izvēlne (dažreiz saukta par hamburgeru vai hamburgera pogu) un pēc tam atlasiet **Atcelt**, lai izietu no uzdevuma **Ienākošā korekcija**.</span><span class="sxs-lookup"><span data-stu-id="f287f-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="f287f-241">Novietojumu konsolidēšana</span><span class="sxs-lookup"><span data-stu-id="f287f-241">Consolidate locations</span></span>

1. <span data-ttu-id="f287f-242">Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Krājuma konsolidācija**.</span><span class="sxs-lookup"><span data-stu-id="f287f-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="f287f-243">Galvenē atlasiet noliktavu, kurai veikt konsolidēšanu.</span><span class="sxs-lookup"><span data-stu-id="f287f-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="f287f-244">Laukā **Noliktava** ievadiet *51*.</span><span class="sxs-lookup"><span data-stu-id="f287f-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="f287f-245">Katram novietojumam, kurā tika koriģēts krājums *M9201*, tiek parādīts ieraksts.</span><span class="sxs-lookup"><span data-stu-id="f287f-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="f287f-246">Kolonna **Izmantojuma procentuālā vērtība** rāda tilpuma izmantojumu katram novietojumam.</span><span class="sxs-lookup"><span data-stu-id="f287f-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="f287f-247">Lai konsolidētu krājumus, atlasiet visus konsolidējamos novietojumus, un pēc tam darbību rūtī atlasiet **Krājumu konsolidēšana**.</span><span class="sxs-lookup"><span data-stu-id="f287f-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="f287f-248">Dialoglodziņā **Krājumu konsolidēšana** norādiet novietojumu un kustības veidu, kas jāizmanto, lai izveidotu krājumu pārvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="f287f-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="f287f-249">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="f287f-249">Set the following values:</span></span>

    - <span data-ttu-id="f287f-250">**Novietojums:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="f287f-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="f287f-251">**Kustības veida kods:** *CONSOLIDATE*</span><span class="sxs-lookup"><span data-stu-id="f287f-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="f287f-252">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f287f-252">Select **OK**.</span></span>
1. <span data-ttu-id="f287f-253">Tiks saņemts informatīvs ziņojums, kurā norādīts izveidotais pārvietošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="f287f-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="f287f-254">Pierakstiet pārvietošanas darba ID.</span><span class="sxs-lookup"><span data-stu-id="f287f-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="f287f-255">Pārvietošanas darba skatīšana</span><span class="sxs-lookup"><span data-stu-id="f287f-255">View movement work</span></span>

1. <span data-ttu-id="f287f-256">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="f287f-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="f287f-257">Skatiet izveidoto darbu.</span><span class="sxs-lookup"><span data-stu-id="f287f-257">View the work that was created.</span></span> <span data-ttu-id="f287f-258">Izmantojiet pārvietošanas darba ID no krājumu konsolidācijas, lai filtrētu vai meklētu darbu režģī.</span><span class="sxs-lookup"><span data-stu-id="f287f-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="f287f-259">Šajā scenārijā esošs novietojums, kurā bija krājumi, tika izmantots kā krājumu konsolidācijas novietojums.</span><span class="sxs-lookup"><span data-stu-id="f287f-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="f287f-260">Tādēļ tika izveidots tikai viens darba ID.</span><span class="sxs-lookup"><span data-stu-id="f287f-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="f287f-261">Sistēma izveido vienu darba ID katrai kustībai, kas ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="f287f-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="f287f-262">Ja norādāt novietojumu, kurā jau ir krājumi, tiek izveidots tikai viens darba ID.</span><span class="sxs-lookup"><span data-stu-id="f287f-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="f287f-263">Ja norādāt jaunu novietojumu, tiek izveidoti divi darba ID.</span><span class="sxs-lookup"><span data-stu-id="f287f-263">If you specify a new location, two work IDs are created.</span></span>
