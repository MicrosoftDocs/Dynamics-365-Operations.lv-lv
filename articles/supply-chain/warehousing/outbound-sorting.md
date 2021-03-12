---
title: Izejošā kārtošana
description: Šajā tēmā ir sniegta informācija par izejošo kārtošanu. Šī funkcionalitāte ļauj vieglāk apstrādāt mazus konteinerus un palīdz noliktavas darbiniekiem labāk plānot un organizēt palešu skaitu kravas automašīnā.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2b0049269b69c0777420b3ecd9b1f649c4a1ab11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963414"
---
# <a name="outbound-sorting"></a><span data-ttu-id="13bab-104">Izejošā kārtošana</span><span class="sxs-lookup"><span data-stu-id="13bab-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13bab-105">Šī funkcionalitāte ļauj vieglāk apstrādāt mazus konteinerus un palīdz noliktavas darbiniekiem labāk plānot un organizēt palešu skaitu kravas automašīnā.</span><span class="sxs-lookup"><span data-stu-id="13bab-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="13bab-106">Izmantojot izejošo kārtošanu, varat kārtot iepakotos konteinerus pareizajā paletē pēc tam, kad tie bijuši iepakošanas stacijā.</span><span class="sxs-lookup"><span data-stu-id="13bab-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="13bab-107">Varat veidot arī iepakošanas hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="13bab-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="13bab-108">Šī funkcionalitāte ļauj veidot paletes no konteineriem, kas iepakoti, izmantojot iepakošanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="13bab-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="13bab-109">Konteiners netiek sūtīts uz galējo nosūtīšanas vietu, kā tas ir sākotnējā iepakošanas plūsmā.</span><span class="sxs-lookup"><span data-stu-id="13bab-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="13bab-110">Tā vietā darbinieki var slēgt konteineru un pārvietot to uz kārtošanas veida vietu.</span><span class="sxs-lookup"><span data-stu-id="13bab-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="13bab-111">Pēc tam konteinerus var kārtot pozīcijās, kur katrā no tām ir noliktavas vienība (LP).</span><span class="sxs-lookup"><span data-stu-id="13bab-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="13bab-112">Kad konteineri ir sašķiroti, var izveidot darbu, lai nosūtītu visu LP uz galējo nosūtīšanas doku vai sagatavošanas vietām, balstoties uz novietojuma direktīvām vai jūsu vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="13bab-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="13bab-113">Turklāt kārtošanas pozīcijas slēgšanas darbība var nekavējoties pārvietot krājumus uz galīgo nosūtīšanas vietu un izdot to pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="13bab-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="13bab-114">Ieslēgt līdzekli Izejošā kārtošana</span><span class="sxs-lookup"><span data-stu-id="13bab-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="13bab-115">Lai varētu izmantot līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="13bab-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="13bab-116">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="13bab-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="13bab-117">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="13bab-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="13bab-118">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="13bab-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="13bab-119">**Līdzekļa nosaukums:** *Izejošā kārtošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="13bab-120">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="13bab-120">Setup</span></span>

<span data-ttu-id="13bab-121">Šim scenārijam ir jāizmanto standarta **USMF** demonstrācijas dati un noliktava *62*.</span><span class="sxs-lookup"><span data-stu-id="13bab-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="13bab-122">Kā arī ir jāpabeidz iestatīšana, kas aprakstīta nākamajās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="13bab-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="13bab-123">Iestatiet kopuma veidni</span><span class="sxs-lookup"><span data-stu-id="13bab-123">Set up a wave template</span></span>

<span data-ttu-id="13bab-124">Šis iestatījums automātiski apstrādā kopumu un izveido darbu, kad rinda tiek nodotas izpildei noliktavā.</span><span class="sxs-lookup"><span data-stu-id="13bab-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="13bab-125">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="13bab-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="13bab-126">Veidņu sarakstā atlasiet **62. noliktava**.</span><span class="sxs-lookup"><span data-stu-id="13bab-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="13bab-127">Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, ka opcija **Apstrādāt kopumu, to pārvietojot uz noliktavu** ir iestatīts uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="13bab-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="13bab-128">Darbinieka iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-128">Set up a worker</span></span>

<span data-ttu-id="13bab-129">Iepakošanas stacija tiek uzskatīta par atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="13bab-129">The packing station is considered a location.</span></span> <span data-ttu-id="13bab-130">Noliktavas darbinieki, kuri piesakās iepakošanas stacijā, redz un strādā tikai ar sūtījumiem un konteineriem, kas ir paredzēti noteiktai iepakošanas vietai.</span><span class="sxs-lookup"><span data-stu-id="13bab-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="13bab-131">Lietotājs, kurš piesakās Microsoft Dynamics 365, ir jāiestata kā darbinieks Noliktavas pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="13bab-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="13bab-132">Ja lietotāja vārds neparādās darba lietotāju sarakstā, izmantojiet nākamo procedūru, lai to pievienotu.</span><span class="sxs-lookup"><span data-stu-id="13bab-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="13bab-133">Šīs darbības pieņem, ka lietotājs jau ir sistēmā un ir saistīts ar darbinieku vai nodarbināto modulī **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="13bab-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="13bab-134">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.</span><span class="sxs-lookup"><span data-stu-id="13bab-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="13bab-135">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-135">Select **New**.</span></span>
1. <span data-ttu-id="13bab-136">Laukā **Nodarbinātais** atlasiet mērķa lietotāju darbinieku sarakstā.</span><span class="sxs-lookup"><span data-stu-id="13bab-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="13bab-137">Atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-137">Select **Select**.</span></span>
1. <span data-ttu-id="13bab-138">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="13bab-139">Kopsavilkuma cilnē **Lietotāji** atlasiet **Jauns**, lai izveidotu mobilās ierīces kontu, un iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="13bab-140">**Lietotāja ID:** ievadiet unikālu ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="13bab-141">**Lietotājvārds:** ievadiet ID nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="13bab-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="13bab-142">**Noklusējuma noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="13bab-143">**Izvēlnes nosaukums:** *Galvenā*</span><span class="sxs-lookup"><span data-stu-id="13bab-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="13bab-144">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="13bab-145">Tiek parādīts dialoglodziņš **Iestatīt paroli**, kur varat izveidot vienkāršu paroli, ko lietotājs var izmantot, lai pieteiktos mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="13bab-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="13bab-146">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-146">Set the following values:</span></span>

    - <span data-ttu-id="13bab-147">**Parole:** ievadiet vienkāršu paroli.</span><span class="sxs-lookup"><span data-stu-id="13bab-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="13bab-148">**Apstiprināt paroli:** vēlreiz ievadiet to pašu paroli.</span><span class="sxs-lookup"><span data-stu-id="13bab-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="13bab-149">Atlasiet **Iestatīt paroli**.</span><span class="sxs-lookup"><span data-stu-id="13bab-149">Select **Set password**.</span></span>

    <span data-ttu-id="13bab-150">Paziņojums darbību centrā informē, ka jūsu izveidotajam lietotājam ir iestatīta parole.</span><span class="sxs-lookup"><span data-stu-id="13bab-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="13bab-151">Novietojuma veida izveide</span><span class="sxs-lookup"><span data-stu-id="13bab-151">Create a location type</span></span>

1. <span data-ttu-id="13bab-152">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma veidi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="13bab-153">Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojuma veidu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="13bab-154">**Novietojuma veids:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="13bab-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="13bab-155">**Apraksts:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="13bab-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="13bab-156">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="13bab-157">Noliktavas pārvaldības parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="13bab-158">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="13bab-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="13bab-159">Cilnē **Vispārīgi**, kopsavilkuma cilnē **Novietojuma veidi** iestatiet lauku **Kārtošanas novietojuma veids** uz *SORT*.</span><span class="sxs-lookup"><span data-stu-id="13bab-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="13bab-160">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="13bab-161">Novietojuma profila iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-161">Set up a location profile</span></span>

1. <span data-ttu-id="13bab-162">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.</span><span class="sxs-lookup"><span data-stu-id="13bab-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="13bab-163">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-164">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="13bab-165">**Novietojuma profila ID:** *Sorting*</span><span class="sxs-lookup"><span data-stu-id="13bab-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="13bab-166">**Nosaukums:** *Kārtošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="13bab-167">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-168">**Novietojuma formāts:** *ASRB* (aile-statīvs-plaukts-nodalījums)</span><span class="sxs-lookup"><span data-stu-id="13bab-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="13bab-169">**Novietojuma veids:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="13bab-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="13bab-170">**Izmantot noliktavas vienības izsekošanu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="13bab-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="13bab-171">**Atļaut jauktus krājumus:** *Jā* (iestatot šo opciju uz *Jā*, opcija **Atļaut jauktu krājumu partijas** tiek automātiski iestatīta uz *Jā*, un to nevar mainīt atsevišķi.)</span><span class="sxs-lookup"><span data-stu-id="13bab-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="13bab-172">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="13bab-173">Novietojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-173">Set up a location</span></span>

1. <span data-ttu-id="13bab-174">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojums**.</span><span class="sxs-lookup"><span data-stu-id="13bab-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="13bab-175">Virsrakstā noņemiet atzīmi izvēles rūtiņai **Ģenerēt novietojuma kontrolciparus**.</span><span class="sxs-lookup"><span data-stu-id="13bab-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="13bab-176">Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojumu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="13bab-177">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="13bab-178">**Novietojums:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="13bab-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="13bab-179">**Novietojuma profila ID:** *SORTING*</span><span class="sxs-lookup"><span data-stu-id="13bab-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="13bab-180">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="13bab-181">Izejošās kārtošanas veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="13bab-182">Izejošās kārtošanas veidne nosaka, vai darbs ir izveidots no kārtošanas vietas un vai kārtošana tiek veikta manuāli vai automātiski.</span><span class="sxs-lookup"><span data-stu-id="13bab-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="13bab-183">Šim scenārijam ir jāizveido izejošās kārtošanas veidne, lai pēc iepakošanas stacijas, veidotu paletes.</span><span class="sxs-lookup"><span data-stu-id="13bab-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="13bab-184">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Izejošās kārtošanas veidne**.</span><span class="sxs-lookup"><span data-stu-id="13bab-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="13bab-185">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-186">Jaunās veidnes galvenē iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="13bab-187">**Izejošās kārtošanas veidnes ID:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="13bab-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="13bab-188">**Apraksts:** *Automātiska darba izveide*</span><span class="sxs-lookup"><span data-stu-id="13bab-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="13bab-189">**Izejošās kārtošanas veidnes veids:** *Konteiners*</span><span class="sxs-lookup"><span data-stu-id="13bab-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="13bab-190">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="13bab-191">**Novietojums:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="13bab-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="13bab-192">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-193">**Kārtošanas pārbaude:** *Pozīcijas skenēšana*.</span><span class="sxs-lookup"><span data-stu-id="13bab-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="13bab-194">**Izveidot darbu slēgtai pozīcijai:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="13bab-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="13bab-195">Ja šī opcija ir iestatīta uz *Jā*, kad pozīcija tiek slēgta, tiks izveidots darbs, lai pārvietotu krājumus uz galējo nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="13bab-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="13bab-196">Ja tā ir iestatīta uz *Nē*, krājumi tiks nekavējoties izdoti pasūtījumam, kad pozīcija tiks slēgta.</span><span class="sxs-lookup"><span data-stu-id="13bab-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="13bab-197">**Pozīcijas piešķiršana:** *Automātiski*</span><span class="sxs-lookup"><span data-stu-id="13bab-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="13bab-198">Ja šajā laukā ir iestatīts *Manuāli*, lietotājam vienmēr jānorāda, kurā pozīcijā krājumi ir jākārto.</span><span class="sxs-lookup"><span data-stu-id="13bab-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="13bab-199">Ja tajā ir iestatīts *Automātiski*, sistēma automātiski novirzīs krājumus uz pozīciju, kad vien iespējams, pamatojoties uz kārtošanas veidnes pārtraukumiem.</span><span class="sxs-lookup"><span data-stu-id="13bab-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="13bab-200">Atlasiet **Saglabāt**, lai darbību rūtī padarītu pieejamu pogu **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="13bab-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="13bab-201">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="13bab-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="13bab-202">Vaicājumu redaktora cilnē **Kārtošana** pievienojiet rindu, kurai ir šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="13bab-203">**Tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="13bab-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="13bab-204">**Atvasinātā tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="13bab-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="13bab-205">**Lauks:** *Pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="13bab-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="13bab-206">Kad vērtības ir atlasītas, iespējams, tiks parādīts šāds ziņojums: “Lauks Pārvadātāja pakalpojums nav indeksa lauks.</span><span class="sxs-lookup"><span data-stu-id="13bab-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="13bab-207">Vai šim vēlaties pievienot kārtošanu?”</span><span class="sxs-lookup"><span data-stu-id="13bab-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="13bab-208">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="13bab-208">Select **Yes**.</span></span>

    - <span data-ttu-id="13bab-209">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="13bab-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="13bab-210">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-210">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-211">Var tikt parādīts šāds ziņojums: “Grupēšana tiks atiestatīta, vai turpināt?”</span><span class="sxs-lookup"><span data-stu-id="13bab-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="13bab-212">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="13bab-212">Select **Yes**.</span></span>

    <span data-ttu-id="13bab-213">Tagad darbību rūtī ir pieejama poga **Izejošās kārtošanas veidnes pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="13bab-214">Darbību rūtī atlasiet **Izejošās kārtošanas veidnes pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="13bab-215">Dialoglodziņā **Izejošās kārtošanas kritēriji** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="13bab-216">**Atsauces tabulas nosaukums:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="13bab-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="13bab-217">**Atsauces lauka nosaukums:** *Pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="13bab-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="13bab-218">**Grupēt pēc lauka:** atzīmējiet šo izvēles rūtiņu, lai grupētu sūtījumus pēc pārvadātāja pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="13bab-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="13bab-219">Atlasiet **Labi**, lai iestatījumus saglabātu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="13bab-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="13bab-220">Konteineru iepakošanas politiku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-220">Set up container packing policies</span></span>

1. <span data-ttu-id="13bab-221">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Konteineri \> Konteineru iepakošanas politikas**.</span><span class="sxs-lookup"><span data-stu-id="13bab-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="13bab-222">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-223">Jaunās politikas galvenē iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="13bab-224">**Konteineru iepakošanas politika:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="13bab-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="13bab-225">**Apraksts:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="13bab-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="13bab-226">Kopsavilkuma cilnē **Pārskats** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-227">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="13bab-228">**Kārtošanas noklusējuma novietojums:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="13bab-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="13bab-229">**Svara vienība:** *kg*</span><span class="sxs-lookup"><span data-stu-id="13bab-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="13bab-230">**Konteineru slēgšanas politika:** *Automātiska izlaide*</span><span class="sxs-lookup"><span data-stu-id="13bab-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="13bab-231">**Konteineru izlaides politika:** *Piešķirt konteineru izejošās kārtošanas pozīcijai*</span><span class="sxs-lookup"><span data-stu-id="13bab-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="13bab-232">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="13bab-233">Iepakošanas profilu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-233">Set up packing profiles</span></span>

<span data-ttu-id="13bab-234">Izveidojiet jaunu iepakošanas profilu, kas tiks izmantots kopā ar kārtošanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="13bab-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="13bab-235">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Iepakošanas profili**.</span><span class="sxs-lookup"><span data-stu-id="13bab-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="13bab-236">Darbību rūtī atlasiet **Jauns**, lai izveidotu rindu, un iestatiet tai šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="13bab-237">**Iepakošanas profila ID:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="13bab-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="13bab-238">**Apraksts:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="13bab-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="13bab-239">**Konteineru iepakošanas politika:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="13bab-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="13bab-240">**Konteinera ID režīms:** *Automātiski*</span><span class="sxs-lookup"><span data-stu-id="13bab-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="13bab-241">**Konteinera veids:** *Kaste - liela*</span><span class="sxs-lookup"><span data-stu-id="13bab-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="13bab-242">**Konteinera slēgšanas laikā automātiski izveidot konteineru:** notīrīts (= *Nē*)</span><span class="sxs-lookup"><span data-stu-id="13bab-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="13bab-243">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="13bab-244">Darba klašu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-244">Set up work classes</span></span>

<span data-ttu-id="13bab-245">Iestatiet darba klasi, kas tiks izmantota kopā ar kārtošanu.</span><span class="sxs-lookup"><span data-stu-id="13bab-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="13bab-246">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="13bab-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="13bab-247">Darbību rūtī atlasiet **Jauns**, lai izveidotu kārtošanas darba klasi, un iestatiet tai šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="13bab-248">**Darba klases ID:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="13bab-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="13bab-249">**Apraksts:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="13bab-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="13bab-250">**Darba pasūtījuma veids:** *Kārtotu krājumu izdošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="13bab-251">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="13bab-252">Mobilās ierīces izvēlnes vienumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="13bab-253">Jaunas paletes izvēlnes vienuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="13bab-254">Izveidojiet mobilās ierīces izvēlnes vienumu, lai veidotu paletes kārtošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="13bab-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="13bab-255">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="13bab-256">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-257">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="13bab-258">**Izvēlnes vienuma nosaukums:** *Paletes izveide*</span><span class="sxs-lookup"><span data-stu-id="13bab-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="13bab-259">**Nosaukums:** *Paletes izveide*</span><span class="sxs-lookup"><span data-stu-id="13bab-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="13bab-260">**Režīms:** *Netiešs*</span><span class="sxs-lookup"><span data-stu-id="13bab-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="13bab-261">**Izmantot esošo darbu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="13bab-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="13bab-262">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-263">**Aktivitātes kods:** *Izejošā kārtošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="13bab-264">Kad šis lauks ir iestatīts uz *Izejošā kārtošana*, tiek parādīts lauks **Izejošās kārtošanas veidnes ID**.</span><span class="sxs-lookup"><span data-stu-id="13bab-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="13bab-265">**Procesu ceļveža izmantošana:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="13bab-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="13bab-266">Kad lauks **Aktivitātes kods** ir iestatīts uz *Izejošā kārtošana*, šī opcija tiek automātiski iestatīta uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="13bab-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="13bab-267">**Izejošās kārtošanas veidnes ID:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="13bab-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="13bab-268">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="13bab-269">Jaunas iekraušanas izvēlnes vienuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-269">Set up a new loading menu item</span></span>

<span data-ttu-id="13bab-270">Izveidojiet izvēlnes vienumu, kas ļauj lietotājiem pārvietot sakārtotās krājuma vienības uz nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="13bab-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="13bab-271">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="13bab-272">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-273">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="13bab-274">**Izvēlnes vienuma nosaukums:** *Load from Sorting*</span><span class="sxs-lookup"><span data-stu-id="13bab-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="13bab-275">**Nosaukums:** *Ielādēt no kārtošanas*</span><span class="sxs-lookup"><span data-stu-id="13bab-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="13bab-276">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="13bab-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="13bab-277">**Izmantot esošo darbu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="13bab-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="13bab-278">Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Noteicējs:** uz *Lietotāja noteikts*.</span><span class="sxs-lookup"><span data-stu-id="13bab-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="13bab-279">Kopsavilkuma cilnē **Darba klases** atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="13bab-280">**Darba klases ID:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="13bab-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="13bab-281">**Darba pasūtījuma veids:** *Kārtotu krājumu izdošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="13bab-282">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="13bab-283">Mobilās ierīces izvēlnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13bab-283">Set up the mobile device menu</span></span>

<span data-ttu-id="13bab-284">Tagad mobilās ierīces izvēlnei ir jāpievieno jauni izvēlnes vienumi.</span><span class="sxs-lookup"><span data-stu-id="13bab-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="13bab-285">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="13bab-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="13bab-286">Atlasiet izvēlni **Izejošais**.</span><span class="sxs-lookup"><span data-stu-id="13bab-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="13bab-287">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="13bab-288">Kolonnā **Pieejamās izvēlnes un izvēļņu elementi** meklējiet un atlasiet **Paletes izveide**.</span><span class="sxs-lookup"><span data-stu-id="13bab-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="13bab-289">Atlasiet bultiņas pa labi pogu, lai pārvietotu **Paletes izveide** uz kolonnu **Izvēlnes struktūra**.</span><span class="sxs-lookup"><span data-stu-id="13bab-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="13bab-290">Izmantojiet bultiņas uz augšu un uz leju, lai izvēlnes vienumu **Paletes izveide** novietotu vēlamajā pozīcijā mobilās ierīces izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="13bab-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="13bab-291">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-291">Select **Save**.</span></span>
1. <span data-ttu-id="13bab-292">Atkārtojiet šo procedūru, lai pievienotu izvēlnes vienumu **Ielādēt no kārtošanas** izvēlnei **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="13bab-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="13bab-293">Iestatīt novietojuma direktīvas</span><span class="sxs-lookup"><span data-stu-id="13bab-293">Set up location directives</span></span>

<span data-ttu-id="13bab-294">*Novietojuma direktīvas* ir nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai.</span><span class="sxs-lookup"><span data-stu-id="13bab-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="13bab-295">Tagad ir jāizveido kārtula, lai pārvaldītu kārtošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="13bab-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="13bab-296">Iestatīt vienu SKU direktīvu</span><span class="sxs-lookup"><span data-stu-id="13bab-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="13bab-297">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="13bab-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="13bab-298">Kreisajā rūtī mainiet lauka **Darba pasūtījuma veids** vērtību uz *Kārtotu krājumu izdošana*.</span><span class="sxs-lookup"><span data-stu-id="13bab-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="13bab-299">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-300">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="13bab-301">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="13bab-302">**Nosaukums:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="13bab-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="13bab-303">Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-304">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="13bab-305">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="13bab-305">**Site:** *6*</span></span>
    - <span data-ttu-id="13bab-306">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="13bab-307">**Vairākas SKU:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="13bab-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="13bab-308">Atlasiet **Saglabāt**, lai padarītu pieejamu rīkjoslu kopsavilkuma cilnē **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="13bab-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="13bab-309">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, un pēc tam jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="13bab-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="13bab-310">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="13bab-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="13bab-311">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="13bab-312">**No:** *0*</span><span class="sxs-lookup"><span data-stu-id="13bab-312">**From:** *0*</span></span>
    - <span data-ttu-id="13bab-313">**Līdz:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="13bab-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="13bab-314">Atlasiet **Saglabāt**, lai padarītu pieejamu rīkjoslu kopsavilkuma cilnē **Novietojuma direktīvu darbības**.</span><span class="sxs-lookup"><span data-stu-id="13bab-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="13bab-315">Kopsavilkuma cilnē **Novietojuma direktīvu darbības** atlasiet **Jauns**, un pēc tam jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="13bab-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="13bab-316">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="13bab-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="13bab-317">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="13bab-318">**Nosaukums:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="13bab-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="13bab-319">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-319">Select **Save**.</span></span>
1. <span data-ttu-id="13bab-320">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="13bab-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="13bab-321">Vaicājumu redaktora cilnē **Diapazons** sameklējiet rindu, kurā lauks **Lauks** ir iestatīts uz *Novietojums*.</span><span class="sxs-lookup"><span data-stu-id="13bab-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="13bab-322">Iestatiet lauku **Kritēriji** šai rindai uz *Angāra durvis*.</span><span class="sxs-lookup"><span data-stu-id="13bab-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="13bab-323">Atlasiet **Labi**, lai saglabātu iestatījumus un aizvērtu vaicājumu redaktoru.</span><span class="sxs-lookup"><span data-stu-id="13bab-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="13bab-324">Iestatīt vairākas SKU direktīvas</span><span class="sxs-lookup"><span data-stu-id="13bab-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="13bab-325">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="13bab-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="13bab-326">Kreisajā rūtī mainiet lauka **Darba pasūtījuma veids** vērtību uz *Kārtotu krājumu izdošana*.</span><span class="sxs-lookup"><span data-stu-id="13bab-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="13bab-327">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-328">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="13bab-329">**Secība:** *2*</span><span class="sxs-lookup"><span data-stu-id="13bab-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="13bab-330">**Nosaukums:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="13bab-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="13bab-331">Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-332">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="13bab-333">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="13bab-333">**Site:** *6*</span></span>
    - <span data-ttu-id="13bab-334">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="13bab-335">**Vairākas SKU:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="13bab-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="13bab-336">Atlasiet **Saglabāt**, lai padarītu pieejamu rīkjoslu kopsavilkuma cilnē **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="13bab-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="13bab-337">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, un pēc tam jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="13bab-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="13bab-338">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="13bab-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="13bab-339">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="13bab-340">**No:** *0*</span><span class="sxs-lookup"><span data-stu-id="13bab-340">**From:** *0*</span></span>
    - <span data-ttu-id="13bab-341">**Līdz:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="13bab-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="13bab-342">Atlasiet **Saglabāt**, lai padarītu pieejamu rīkjoslu kopsavilkuma cilnē **Novietojuma direktīvu darbības**.</span><span class="sxs-lookup"><span data-stu-id="13bab-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="13bab-343">Kopsavilkuma cilnē **Novietojuma direktīvu darbības** atlasiet **Jauns**, un pēc tam jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="13bab-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="13bab-344">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="13bab-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="13bab-345">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="13bab-346">**Nosaukums:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="13bab-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="13bab-347">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-347">Select **Save**.</span></span>
1. <span data-ttu-id="13bab-348">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="13bab-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="13bab-349">Vaicājumu redaktora cilnē **Diapazons** sameklējiet rindu, kurā lauks **Lauks** ir iestatīts uz *Novietojums*.</span><span class="sxs-lookup"><span data-stu-id="13bab-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="13bab-350">Iestatiet lauku **Kritēriji** šai rindai uz *Angāra durvis*.</span><span class="sxs-lookup"><span data-stu-id="13bab-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="13bab-351">Atlasiet **Labi**, lai saglabātu iestatījumus un aizvērtu vaicājumu redaktoru.</span><span class="sxs-lookup"><span data-stu-id="13bab-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="13bab-352">Iestatīt darba veidnes</span><span class="sxs-lookup"><span data-stu-id="13bab-352">Set up work templates</span></span>

1. <span data-ttu-id="13bab-353">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="13bab-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="13bab-354">Mainiet lauka **Darba pasūtījuma veids** vērtību uz *Kārtotu krājumu izdošana*.</span><span class="sxs-lookup"><span data-stu-id="13bab-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="13bab-355">Lai izveidotu darba veidni, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="13bab-356">Cilnē **Pārskats** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="13bab-357">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="13bab-358">**Darba veidne:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="13bab-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="13bab-359">**Darba veidnes apraksts:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="13bab-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="13bab-360">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Darba veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="13bab-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="13bab-361">Kopsavilkuma cilnē **Darba veidnes informācija** atlasiet **Jauns**, lai pievienotu rindu, un pēc tam iestatiet tai šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="13bab-362">**Darba veids:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="13bab-363">**Darba klases ID:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="13bab-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="13bab-364">Vēlreiz atlasiet **Jauns**, lai pievienotu otro rindu, un tad iestatiet tai šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="13bab-365">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="13bab-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="13bab-366">**Darba klases ID:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="13bab-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="13bab-367">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="13bab-368">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="13bab-368">Scenario</span></span>

<span data-ttu-id="13bab-369">Šis scenārijs simulē situāciju, kad iepakotie konteineri tiek automātiski kārtoti dažādām pozīcijām (paletēm) pēc iepakošanas stacijas, atkarībā no sūtījuma pārvadātāja pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="13bab-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="13bab-370">Pēc tam, kad visi noslodzes krājumi ir iepakoti un sakārtoti pēc adreses, paletes tiks pārvietotas uz angāra durvīm.</span><span class="sxs-lookup"><span data-stu-id="13bab-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="13bab-371">Pārdošanas pasūtījuma un izdošanas darba izveide</span><span class="sxs-lookup"><span data-stu-id="13bab-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="13bab-372">1. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="13bab-372">Create sales order 1</span></span>

1. <span data-ttu-id="13bab-373">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="13bab-374">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-375">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="13bab-376">**Debitora konts:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="13bab-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="13bab-377">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="13bab-378">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="13bab-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="13bab-379">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="13bab-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="13bab-380">Pārejiet uz skatu **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="13bab-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="13bab-381">Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="13bab-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="13bab-382">**Sūtījuma pārvadātājs:** *Kravas lidmašīnas*</span><span class="sxs-lookup"><span data-stu-id="13bab-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="13bab-383">**Pārvadātāja pakalpojums:** *Gaisa*</span><span class="sxs-lookup"><span data-stu-id="13bab-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="13bab-384">Pārejiet uz skatu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="13bab-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="13bab-385">Ja jauna, tukša rinda netiek automātiski pievienota režģim, kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai to pievienotu.</span><span class="sxs-lookup"><span data-stu-id="13bab-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="13bab-386">Jaunajā pasūtījuma rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="13bab-387">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="13bab-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="13bab-388">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="13bab-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="13bab-389">Kamēr jaunā pasūtījuma rinda joprojām ir atlasīta, kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**, izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="13bab-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="13bab-390">Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="13bab-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="13bab-391">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="13bab-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="13bab-392">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="13bab-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="13bab-393">Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums.</span><span class="sxs-lookup"><span data-stu-id="13bab-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="13bab-394">Pierakstiet kopuma ID un sūtījuma ID numurus.</span><span class="sxs-lookup"><span data-stu-id="13bab-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="13bab-395">2. pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="13bab-395">Sales order 2</span></span>

1. <span data-ttu-id="13bab-396">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="13bab-397">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13bab-398">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="13bab-399">**Debitora konts:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="13bab-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="13bab-400">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="13bab-401">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="13bab-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="13bab-402">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="13bab-402">The new sales order is opened.</span></span> <span data-ttu-id="13bab-403">Tam ir jāietver jauna, tukša rinda režģī kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="13bab-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="13bab-404">Šajā pasūtījuma rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="13bab-405">**Krājums:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="13bab-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="13bab-406">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="13bab-407">Kopsavilkuma cilnē **Rindas informācija**, cilnē **Piegāde** iestatiet lauku **Piegādes režīms** uz *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="13bab-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="13bab-408">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, un pēc tam otrajā pasūtījuma rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="13bab-409">**Krājums:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="13bab-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="13bab-410">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="13bab-411">Kopsavilkuma cilnē **Rindas informācija**, cilnē **Piegāde** mainiet vērtību laukam **Piegādes režīms** uz *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="13bab-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="13bab-412">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet pirmo pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="13bab-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="13bab-413">Tad izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="13bab-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="13bab-414">Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="13bab-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="13bab-415">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="13bab-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="13bab-416">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="13bab-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="13bab-417">Tad izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="13bab-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="13bab-418">Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="13bab-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="13bab-419">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="13bab-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="13bab-420">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="13bab-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="13bab-421">Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums.</span><span class="sxs-lookup"><span data-stu-id="13bab-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="13bab-422">Ievērojiet, ka ir izveidoti divi kopuma ID numuri un divi sūtījuma ID numuri, viens katram piegādes režīmam pārdošanas pasūtījumu rindām.</span><span class="sxs-lookup"><span data-stu-id="13bab-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="13bab-423">Darba ID iegūšana no darba informācijas</span><span class="sxs-lookup"><span data-stu-id="13bab-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="13bab-424">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="13bab-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="13bab-425">Lapā tiek rādīti no pārdošanas pasūtījumiem izveidotie darba ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="13bab-426">Izmantojiet kopuma ID un sūtījuma ID no izveidotajiem pārdošanas pasūtījumiem, lai atrastu darba ID katram kopumam un sūtījumam.</span><span class="sxs-lookup"><span data-stu-id="13bab-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="13bab-427">Pierakstiet šos darba ID, jo tie būs vajadzīgi nākamajās darbībās.</span><span class="sxs-lookup"><span data-stu-id="13bab-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="13bab-428">Ievērojiet, ka otrajam pārdošanas pasūtījumam ir izveidoti divi darba ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="13bab-429">Ja dažādi krājumi tiek izdoti no dažādām vietām, tiek ģenerēti atsevišķi darba ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="13bab-430">Krājumu izdošana pārdošanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="13bab-430">Pick items for the sales orders</span></span>

<span data-ttu-id="13bab-431">Pabeidziet izveidoto darbu, izmantojot mobilo ierīci, lai pārvietotu krājumus uz iepakošanas staciju.</span><span class="sxs-lookup"><span data-stu-id="13bab-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="13bab-432">Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).</span><span class="sxs-lookup"><span data-stu-id="13bab-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="13bab-433">Galvenajā izvēlnē atlasiet **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="13bab-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="13bab-434">Izvēlnē **Izejošs** atlasiet **Pārdošanas izdošana**.</span><span class="sxs-lookup"><span data-stu-id="13bab-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="13bab-435">Laukā **ID** ievadiet darba ID, kas tika izveidots 1. pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="13bab-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="13bab-436">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-436">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-437">Lapā **Pārdošanas pasūtījumi - izdošana**, ievadiet mērķa LP, kas tika izveidots 1. pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="13bab-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="13bab-438">Ievērojiet, ka tiek rādīta izdošanas vieta (*bulk-001*), krājums (*A0001*) un daudzums (*2 gab.*).</span><span class="sxs-lookup"><span data-stu-id="13bab-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="13bab-439">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-439">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-440">Pārskatiet informāciju lapā **Pārdošanas pasūtījumi - izvietošana**.</span><span class="sxs-lookup"><span data-stu-id="13bab-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="13bab-441">Laukam **Vieta** ir jānorāda, ka izdotie krājumi ir jānosūta uz atrašanās vietu *Iepakot*.</span><span class="sxs-lookup"><span data-stu-id="13bab-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="13bab-442">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-442">Select **OK**.</span></span>

    <span data-ttu-id="13bab-443">Lapā **Skenēt darba ID / noliktavas vienības ID** tiek saņemts ziņojums “Darbs pabeigts”, norādot, ka darba ID no 1. pārdošanas pasūtījuma ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="13bab-444">Tagad tiks izdots 2. pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="13bab-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="13bab-445">Laukā **ID** ievadiet darba ID, kas tika izveidots 2. pārdošanas pasūtījumam, kur 1. rindai ir krājums *A0001*.</span><span class="sxs-lookup"><span data-stu-id="13bab-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="13bab-446">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-446">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-447">Lapā **Pārdošanas pasūtījumi - izdošana** ievadiet mērķa LP.</span><span class="sxs-lookup"><span data-stu-id="13bab-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="13bab-448">Ievērojiet, ka tiek rādīta izdošanas vieta (*bulk-001*), krājums (*A0001*) un daudzums (*1 gab.*).</span><span class="sxs-lookup"><span data-stu-id="13bab-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="13bab-449">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-449">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-450">Pārskatiet informāciju lapā **Pārdošanas pasūtījumi - izvietošana**.</span><span class="sxs-lookup"><span data-stu-id="13bab-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="13bab-451">Laukam **Vieta** ir jānorāda, ka izdotie krājumi ir jānosūta uz atrašanās vietu *Iepakot*.</span><span class="sxs-lookup"><span data-stu-id="13bab-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="13bab-452">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-452">Select **OK**.</span></span>

    <span data-ttu-id="13bab-453">Lapā **Skenēt darba ID / noliktavas vienības ID** tiek saņemts ziņojums “Darbs pabeigts”.</span><span class="sxs-lookup"><span data-stu-id="13bab-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="13bab-454">Šis ziņojums norāda, ka 2. pārdošanas pasūtījuma 1. rindas darba ID ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="13bab-455">Laukā **ID** ievadiet darba ID, kas tika izveidots 2. pārdošanas pasūtījumam, kur 2. rindai ir krājums *A0002*.</span><span class="sxs-lookup"><span data-stu-id="13bab-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="13bab-456">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-456">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-457">Lapā **Pārdošanas pasūtījumi - izdošana** ievadiet mērķa LP.</span><span class="sxs-lookup"><span data-stu-id="13bab-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="13bab-458">Ievērojiet, ka tiek rādīta izdošanas vieta (*bulk-002*), krājums (*A0001*) un daudzums (*1 gab.*).</span><span class="sxs-lookup"><span data-stu-id="13bab-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="13bab-459">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-459">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-460">Pārskatiet informāciju lapā **Pārdošanas pasūtījumi - izvietošana**.</span><span class="sxs-lookup"><span data-stu-id="13bab-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="13bab-461">Laukam **Vieta** ir jānorāda, ka izdotie krājumi ir jānosūta uz atrašanās vietu *Iepakot*.</span><span class="sxs-lookup"><span data-stu-id="13bab-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="13bab-462">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-462">Select **OK**.</span></span>

    <span data-ttu-id="13bab-463">Lapā **Skenēt darba ID / noliktavas vienības ID** tiek saņemts ziņojums “Darbs pabeigts”.</span><span class="sxs-lookup"><span data-stu-id="13bab-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="13bab-464">Šis ziņojums norāda, ka 2. pārdošanas pasūtījuma 2. rindas darba ID ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="13bab-465">Pārdošanas pasūtījumu iepakošana konteineros</span><span class="sxs-lookup"><span data-stu-id="13bab-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="13bab-466">1. pārdošanas pasūtījuma iepakošana konteineros</span><span class="sxs-lookup"><span data-stu-id="13bab-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="13bab-467">Dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Iepakot**.</span><span class="sxs-lookup"><span data-stu-id="13bab-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="13bab-468">Tiek parādīts dialoglodziņš **Atlasīt iepakošanas staciju**.</span><span class="sxs-lookup"><span data-stu-id="13bab-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="13bab-469">Pēc noklusējuma lauks **Darbinieks** ir jāiestata uz tā darbinieka vārda, ko iestatījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="13bab-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="13bab-470">Iestatiet šādas vērtības, lai skatītu un strādātu ar sūtījumiem un konteineriem, kas ir paredzēti noteiktai iepakošanas vietai:</span><span class="sxs-lookup"><span data-stu-id="13bab-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="13bab-471">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="13bab-471">**Site:** *6*</span></span>
    - <span data-ttu-id="13bab-472">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="13bab-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="13bab-473">**Atrašanās vieta:** *Pakotne*</span><span class="sxs-lookup"><span data-stu-id="13bab-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="13bab-474">**Iepakošanas profila ID:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="13bab-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="13bab-475">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="13bab-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="13bab-476">Lapas **Pakotne** laukā **Noliktavas vienība vai sūtījums**, ievadiet mērķa LP 1. pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="13bab-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="13bab-477">Pēc tam atlasiet klaviatūras taustiņu **Cilne** vai **Ievadīt**, lai izietu no lauka.</span><span class="sxs-lookup"><span data-stu-id="13bab-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="13bab-478">Darbību rūtī atlasiet **Jauns konteiners**.</span><span class="sxs-lookup"><span data-stu-id="13bab-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="13bab-479">Pieņemiet visus noklusējuma iestatījumus un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="13bab-480">Pierakstiet konteinera ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="13bab-481">Kopsavilkuma cilnē **Krājuma iepakošana** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-482">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="13bab-483">**Identifikators:** krājums *A0001*</span><span class="sxs-lookup"><span data-stu-id="13bab-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="13bab-484">Darbību rūtī atlasiet **Slēgt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="13bab-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="13bab-485">Dialoglodziņā **Slēgt konteineru** atlasiet **Iegūt sistēmas svaru**, lai sistēma atjauninātu lauku **Bruto svars**.</span><span class="sxs-lookup"><span data-stu-id="13bab-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="13bab-486">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-486">Select **OK**.</span></span> <span data-ttu-id="13bab-487">Konteiners ir pārvietots uz novietni *SORT* un ir gatavs kārtošanai.</span><span class="sxs-lookup"><span data-stu-id="13bab-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="13bab-488">Izveidojiet otru konteineru, lai pievienotu otro krājumu, no LP 1. pārdošanas pasūtījuma uz jauno konteineru.</span><span class="sxs-lookup"><span data-stu-id="13bab-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="13bab-489">Darbību rūtī atlasiet **Jauns konteiners**.</span><span class="sxs-lookup"><span data-stu-id="13bab-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="13bab-490">Pieņemiet visus noklusējuma iestatījumus un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="13bab-491">Pierakstiet konteinera ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="13bab-492">Kopsavilkuma cilnē **Krājuma iepakošana** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-493">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="13bab-494">**Identifikators:** krājums *A0001*</span><span class="sxs-lookup"><span data-stu-id="13bab-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="13bab-495">Darbību rūtī atlasiet **Slēgt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="13bab-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="13bab-496">Dialoglodziņā **Slēgt konteineru** atlasiet **Iegūt sistēmas svaru**, lai sistēma atjauninātu lauku **Bruto svars**.</span><span class="sxs-lookup"><span data-stu-id="13bab-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="13bab-497">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-497">Select **OK**.</span></span> <span data-ttu-id="13bab-498">Konteiners ir pārvietots uz novietni *SORT* un ir gatavs kārtošanai.</span><span class="sxs-lookup"><span data-stu-id="13bab-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="13bab-499">2. pārdošanas pasūtījuma iepakošana konteineros</span><span class="sxs-lookup"><span data-stu-id="13bab-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="13bab-500">Lapas **Pakotne** laukā **Noliktavas vienība vai sūtījums**, ievadiet mērķa LP 2. pārdošanas pasūtījuma 1. rindai.</span><span class="sxs-lookup"><span data-stu-id="13bab-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="13bab-501">Pēc tam atlasiet klaviatūras taustiņu **Cilne** vai **Ievadīt**, lai izietu no lauka.</span><span class="sxs-lookup"><span data-stu-id="13bab-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="13bab-502">Darbību rūtī atlasiet **Jauns konteiners**.</span><span class="sxs-lookup"><span data-stu-id="13bab-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="13bab-503">Pieņemiet visus noklusējuma iestatījumus un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="13bab-504">Pierakstiet konteinera ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="13bab-505">Kopsavilkuma cilnē **Krājuma iepakošana** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-506">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="13bab-507">**Identifikators:** krājums *A0001*</span><span class="sxs-lookup"><span data-stu-id="13bab-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="13bab-508">Darbību rūtī atlasiet **Slēgt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="13bab-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="13bab-509">Dialoglodziņā **Slēgt konteineru** atlasiet **Iegūt sistēmas svaru**, lai sistēma atjauninātu lauku **Bruto svars**.</span><span class="sxs-lookup"><span data-stu-id="13bab-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="13bab-510">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-510">Select **OK**.</span></span> <span data-ttu-id="13bab-511">Konteiners ir pārvietots uz novietni *SORT* un ir gatavs kārtošanai.</span><span class="sxs-lookup"><span data-stu-id="13bab-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="13bab-512">Laukā **Noliktavas vienība vai sūtījums**, ievadiet mērķa LP 2. pārdošanas pasūtījuma 2. rindai.</span><span class="sxs-lookup"><span data-stu-id="13bab-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="13bab-513">Pēc tam atlasiet klaviatūras taustiņu **Cilne** vai **Ievadīt**, lai izietu no lauka.</span><span class="sxs-lookup"><span data-stu-id="13bab-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="13bab-514">Darbību rūtī atlasiet **Jauns konteiners**.</span><span class="sxs-lookup"><span data-stu-id="13bab-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="13bab-515">Pieņemiet visus noklusējuma iestatījumus un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="13bab-516">Pierakstiet konteinera ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="13bab-517">Kopsavilkuma cilnē **Krājuma iepakošana** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="13bab-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="13bab-518">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="13bab-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="13bab-519">**Identifikatora lauks:** krājums *A0002*</span><span class="sxs-lookup"><span data-stu-id="13bab-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="13bab-520">Darbību rūtī atlasiet **Slēgt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="13bab-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="13bab-521">Dialoglodziņā **Slēgt konteineru** atlasiet **Iegūt sistēmas svaru**, lai sistēma atjauninātu lauku **Bruto svars**.</span><span class="sxs-lookup"><span data-stu-id="13bab-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="13bab-522">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-522">Select **OK**.</span></span> <span data-ttu-id="13bab-523">Konteiners ir pārvietots uz novietni *SORT* un ir gatavs kārtošanai.</span><span class="sxs-lookup"><span data-stu-id="13bab-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="13bab-524">Lai skatītu konteineru informāciju, dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Konteineri** un meklējiet konteineru ID, kas tika izveidoti iepakošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="13bab-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="13bab-525">Konteineru kārtošana</span><span class="sxs-lookup"><span data-stu-id="13bab-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13bab-526">Kad piekļūstat izvēlnes vienumam **Paletes izveide** mobilajā programmā, lai veiktu izejošo kārtošanu, tiks parādīta poga, kas ir apzīmēta kā **Pilns**.</span><span class="sxs-lookup"><span data-stu-id="13bab-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="13bab-527">*Nelietojiet pogu **Pilns**, lai kārtotu vai slēgtu pozīciju.*</span><span class="sxs-lookup"><span data-stu-id="13bab-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="13bab-528">Poga **Pilns** tiek nodrošināta pēc noklusējuma, un to nevar atspējot vai noņemt no lapas.</span><span class="sxs-lookup"><span data-stu-id="13bab-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="13bab-529">To nelieto funkcijai *Izejošā kārtošana*.</span><span class="sxs-lookup"><span data-stu-id="13bab-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="13bab-530">Pirmā konteinera kārtošana</span><span class="sxs-lookup"><span data-stu-id="13bab-530">Sort the first container</span></span>

1. <span data-ttu-id="13bab-531">Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).</span><span class="sxs-lookup"><span data-stu-id="13bab-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="13bab-532">Galvenajā izvēlnē atlasiet **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="13bab-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="13bab-533">Izvēlnē **Izejošs** atlasiet **Paletes izveide**.</span><span class="sxs-lookup"><span data-stu-id="13bab-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="13bab-534">Laukā **LP/Con** ievadiet pirmā konteinera ID, kas ir saistīts ar 1. pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="13bab-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="13bab-535">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-535">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-536">Tā kā pašlaik nav kārtošanas pozīciju, tā ir jānorāda.</span><span class="sxs-lookup"><span data-stu-id="13bab-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="13bab-537">Laukā **Kārtošanas pozīcijas ID** ievadiet *SP01*.</span><span class="sxs-lookup"><span data-stu-id="13bab-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="13bab-538">Tā kā neviena LP pašlaik nav saistīta ar kārtošanas pozīciju *SP01*, tā ir jānorāda.</span><span class="sxs-lookup"><span data-stu-id="13bab-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="13bab-539">Laukā **LP** ievadiet *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="13bab-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="13bab-540">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-540">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-541">Tā kā ir ieslēgta kārtošanas pozīcijas pārbaude, jums vēlreiz ir jāievada kārtošanas pozīcijas ID.</span><span class="sxs-lookup"><span data-stu-id="13bab-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="13bab-542">Laukā **Kārtošanas pozīcijas ID** ievadiet *SP01*.</span><span class="sxs-lookup"><span data-stu-id="13bab-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="13bab-543">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-543">Select **OK**.</span></span>

    <span data-ttu-id="13bab-544">Tiek saņemts ziņojums “Darbs pabeigts”.</span><span class="sxs-lookup"><span data-stu-id="13bab-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="13bab-545">Lai skatītu kārtošanas pozīciju un tajā iekļauto LP, dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Izejošās kārtošanas pozīciju piešķires**.</span><span class="sxs-lookup"><span data-stu-id="13bab-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="13bab-546">Lapā **Izejošās kārtošanas pozīciju piešķires** tiek parādītas visas šobrīd aktīvās kārtošanas pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="13bab-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="13bab-547">Lauks **Kārtošanas pozīcijas transakcijas** parāda ar katru kārtošanas pozīciju saistīto LP un konteinerus, kas ir kārtošanas pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="13bab-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="13bab-548">Ievērojiet, ka pašlaik pastāv viena kārtošanas pozīcija un ka kopsavilkuma cilne **Kārtošanas pozīcijas kritēriji** parāda kritērijus **Sūtījums – Pārvadātāja pakalpojums – Gaisa**.</span><span class="sxs-lookup"><span data-stu-id="13bab-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="13bab-549">Atlikušo konteineru kārtošana</span><span class="sxs-lookup"><span data-stu-id="13bab-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="13bab-550">Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).</span><span class="sxs-lookup"><span data-stu-id="13bab-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="13bab-551">Galvenajā izvēlnē atlasiet **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="13bab-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="13bab-552">Izvēlnē **Izejošs** atlasiet **Paletes izveide**.</span><span class="sxs-lookup"><span data-stu-id="13bab-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="13bab-553">Laukā **LP/Con** ievadiet otrā konteinera ID, kas ir saistīts ar 1. pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="13bab-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="13bab-554">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-554">Select **OK**.</span></span> <span data-ttu-id="13bab-555">Tā kā kārtošanas veidne ir iestatīta automātiskai kārtošanai un kārtošanas pozīcija ar atbilstošajiem kritērijiem jau pastāv, jūs automātiski tiekat novirzīts uz pareizo kārtošanas pozīciju.</span><span class="sxs-lookup"><span data-stu-id="13bab-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="13bab-556">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-556">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-557">Apstipriniet kārtošanas pozīcijas ID, norādot, ka krājumi ir pareizajā vietā.</span><span class="sxs-lookup"><span data-stu-id="13bab-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="13bab-558">Laukā **Kārtošanas pozīcijas ID** ievadiet *SP01*.</span><span class="sxs-lookup"><span data-stu-id="13bab-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="13bab-559">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-559">Select **OK**.</span></span>

    <span data-ttu-id="13bab-560">1. pārdošanas pasūtījuma otrā konteinera darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="13bab-561">Tagad tiks šķiroti atlikušie konteineri no 2. pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="13bab-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="13bab-562">Laukā **LP/Con** ievadiet konteinera ID no 2. pārdošanas pasūtījuma konteinera, kas satur krājumu *A0001*.</span><span class="sxs-lookup"><span data-stu-id="13bab-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="13bab-563">Tā kā pārvadātāja pakalpojums ir atšķirīgs, tiek parādīta uzvedne ievadīt jaunu kārtošanas pozīciju un piešķirt šai pozīcijai LP.</span><span class="sxs-lookup"><span data-stu-id="13bab-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="13bab-564">Izmantojiet kārtošanas pozīciju *SP02* un LP *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="13bab-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="13bab-565">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-565">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-566">Apstipriniet kārtošanas pozīciju, laukā **Kārtošanas pozīcijas ID** ievadot *SP02*.</span><span class="sxs-lookup"><span data-stu-id="13bab-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="13bab-567">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-567">Select **OK**.</span></span>

    <span data-ttu-id="13bab-568">Konteinera darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="13bab-569">Laukā **LP/Con** ievadiet konteinera ID 2. pārdošanas pasūtījuma atlikušajam konteineram, kas satur krājumu *A0002*.</span><span class="sxs-lookup"><span data-stu-id="13bab-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="13bab-570">Tā kā pārvadātāja pakalpojums ir tāds pats kā pārvadātāja pakalpojums 1. pārdošanas pasūtījumam, sistēma parāda esošo kārtošanas pozīciju ar atbilstošajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="13bab-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="13bab-571">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-571">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-572">Apstipriniet kārtošanas pozīciju, laukā **Kārtošanas pozīcijas ID** ievadot *SP01*.</span><span class="sxs-lookup"><span data-stu-id="13bab-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="13bab-573">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-573">Select **OK**.</span></span>

    <span data-ttu-id="13bab-574">Konteinera darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="13bab-575">Slēgt izejošās kārtošanas pozīcijas</span><span class="sxs-lookup"><span data-stu-id="13bab-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="13bab-576">Kad visi krājumi ir sakārtoti, pozīcija ir jāslēdz, lai varētu izveidot darbu.</span><span class="sxs-lookup"><span data-stu-id="13bab-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="13bab-577">Tiks izveidots kārtots krājumu izdošanas darbs, lai veiktu inventarizāciju angāra durvīm.</span><span class="sxs-lookup"><span data-stu-id="13bab-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="13bab-578">Pozīcijas slēgšana no mobilās ierīces</span><span class="sxs-lookup"><span data-stu-id="13bab-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="13bab-579">Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).</span><span class="sxs-lookup"><span data-stu-id="13bab-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="13bab-580">Galvenajā izvēlnē atlasiet **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="13bab-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="13bab-581">Izvēlnē **Izejošs** atlasiet **Paletes izveide**.</span><span class="sxs-lookup"><span data-stu-id="13bab-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="13bab-582">Laukā **LP/Con** ievadiet kārtotā konteinera ID kārtošanas pozīciju *SP01*.</span><span class="sxs-lookup"><span data-stu-id="13bab-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="13bab-583">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-583">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-584">Tiek parādīts šāds ziņojums: “Konteiners jau ir sakārtots pēc pozīcijas SP01.</span><span class="sxs-lookup"><span data-stu-id="13bab-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="13bab-585">Vai slēgt pozīciju?”</span><span class="sxs-lookup"><span data-stu-id="13bab-585">Close the position?"</span></span> <span data-ttu-id="13bab-586">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="13bab-586">Select **Close**.</span></span>

    <span data-ttu-id="13bab-587">Darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="13bab-588">Pozīcijas slēgšana no izejošās kārtošanas pozīcijas piešķirēm</span><span class="sxs-lookup"><span data-stu-id="13bab-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="13bab-589">Dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Izejošās kārtošanas pozīciju piešķires**.</span><span class="sxs-lookup"><span data-stu-id="13bab-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="13bab-590">Kreisajā kolonnā atlasiet **SP02**.</span><span class="sxs-lookup"><span data-stu-id="13bab-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="13bab-591">Šī izejošās kārtošanas pozīcijas rinda ir tā, kuru slēgsit.</span><span class="sxs-lookup"><span data-stu-id="13bab-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="13bab-592">Darbību rūtī atlasiet **Slēgt pozīciju**.</span><span class="sxs-lookup"><span data-stu-id="13bab-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="13bab-593">Kārtošanas pozīcijas ieraksts ir slēgts un vairs netiek rādīts.</span><span class="sxs-lookup"><span data-stu-id="13bab-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="13bab-594">Lai tiktu rādīti visi slēgtie pozīciju ieraksti, atzīmējiet izvēles rūtiņu **Rādīt slēgto**.</span><span class="sxs-lookup"><span data-stu-id="13bab-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="13bab-595">Kārtoto krājumu izdošana</span><span class="sxs-lookup"><span data-stu-id="13bab-595">Sorted inventory picking</span></span>

<span data-ttu-id="13bab-596">Pabeidziet kārtoto krājumu izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="13bab-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="13bab-597">Kad tas ir pabeigts, krājumi tiks izdoti pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="13bab-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="13bab-598">Šajā brīdī tiek lietoti visi pārējie noliktavas procesi.</span><span class="sxs-lookup"><span data-stu-id="13bab-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="13bab-599">Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).</span><span class="sxs-lookup"><span data-stu-id="13bab-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="13bab-600">Galvenajā izvēlnē atlasiet **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="13bab-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="13bab-601">Izvēlnē **Izejošs** atlasiet **Ielādēt no kārtošanas**.</span><span class="sxs-lookup"><span data-stu-id="13bab-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="13bab-602">Ievadiet mērķa LP ID no pirmās kārtošanas pozīcijas, *SP01*.</span><span class="sxs-lookup"><span data-stu-id="13bab-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="13bab-603">Iestatiet lauku **ID** uz *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="13bab-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="13bab-604">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-604">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-605">Lapā **Kārtoto krājumu izdošana: Izdot** tiek rādīts veicamais izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="13bab-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="13bab-606">Izdot no novietojuma *SORT* un mērķa LP *PLP01*, kam ir vairāki krājumi un daudzums ir *3*.</span><span class="sxs-lookup"><span data-stu-id="13bab-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="13bab-607">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-607">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-608">Lapā **Kārtoto krājumu izdošana: Izvietot** tiek rādīts veicamais izvietošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="13bab-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="13bab-609">Izvietot novietojumā *Baydoor* un mērķa LP *PLP01*, kam ir vairāki krājumi un daudzums ir *3*.</span><span class="sxs-lookup"><span data-stu-id="13bab-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="13bab-610">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-610">Select **OK**.</span></span>

    <span data-ttu-id="13bab-611">Darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-611">Work is completed.</span></span>

1. <span data-ttu-id="13bab-612">Ievadiet mērķa noliktavas vienības ID no otrās kārtošanas pozīcijas, *SP02*.</span><span class="sxs-lookup"><span data-stu-id="13bab-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="13bab-613">Iestatiet lauku **ID** uz *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="13bab-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="13bab-614">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-614">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-615">Lapā **Kārtoto krājumu izdošana: Izdot** tiek rādīts veicamais izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="13bab-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="13bab-616">Izdot no novietojuma *SORT* un mērķa LP *PLP02*, kam ir vairāki krājumi un daudzums ir *1*.</span><span class="sxs-lookup"><span data-stu-id="13bab-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="13bab-617">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-617">Select **OK**.</span></span>
1. <span data-ttu-id="13bab-618">Lapā **Kārtoto krājumu izdošana: Izvietot** tiek rādīts veicamais izvietošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="13bab-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="13bab-619">Izvietot novietojumā *Baydoor* un mērķa LP *PLP02*, kam ir vairāki krājumi un daudzums ir *1*.</span><span class="sxs-lookup"><span data-stu-id="13bab-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="13bab-620">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13bab-620">Select **OK**.</span></span>

    <span data-ttu-id="13bab-621">Darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="13bab-621">Work is completed.</span></span>

<span data-ttu-id="13bab-622">No šī brīža tiek lietoti visi pārējie noliktavas procesi.</span><span class="sxs-lookup"><span data-stu-id="13bab-622">From this point forward, all other warehouse processes apply.</span></span>
