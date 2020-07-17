---
title: Novietojuma produkta dimensiju sajaukšana
description: Šajā tēmā ir sniegta informācija par novietojuma produktu dimensiju jaukšanu. Šī novietojuma profila funkcionalitāte palīdz uzlabot novietojumu pārvaldību, izmantojot produkta variantus vai produktus ar dimensijām, piemēram, modes industrijā. Tas ļauj jums izlemt, vai konfigurācijas, krāsas, stilus un izmērus var kombinēt noteiktam novietojuma profilam, vai arī tikai vienu no šīm dimensijām, vai to kombināciju var pievienot tam pašam novietojumam.
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
ms.openlocfilehash: 968777b918d59b810a189139fbf4d6fee1b5d3f5
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529987"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="518a0-105">Novietojuma produkta dimensiju sajaukšana</span><span class="sxs-lookup"><span data-stu-id="518a0-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="518a0-106">Novietojuma produkta dimensiju kombinēšana ir novietojuma profila funkcionalitāte, kas palīdz uzlabot novietojumu pārvaldību, izmantojot produkta variantus vai produktus ar dimensijām, piemēram, modes industrijā.</span><span class="sxs-lookup"><span data-stu-id="518a0-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="518a0-107">Tas ļauj jums izlemt, vai konfigurācijas, krāsas, stilus un izmērus var kombinēt noteiktam novietojuma profilam, vai arī tikai vienu no šīm dimensijām, vai to kombināciju var pievienot tam pašam novietojumam.</span><span class="sxs-lookup"><span data-stu-id="518a0-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="518a0-108">Ieslēdziet Novietojuma produkta dimensiju jaukšanas iespēju</span><span class="sxs-lookup"><span data-stu-id="518a0-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="518a0-109">Pirms izmantot novietojuma produktu dimensiju jaukšanu, funkcijai ir jābūt iespējotai sistēmā.</span><span class="sxs-lookup"><span data-stu-id="518a0-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="518a0-110">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="518a0-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="518a0-111">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="518a0-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="518a0-112">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="518a0-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="518a0-113">**Funkcijas nosaukums:** *Novietojuma produktu dimensiju jaukšana*</span><span class="sxs-lookup"><span data-stu-id="518a0-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="518a0-114">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="518a0-114">Setup</span></span>

<span data-ttu-id="518a0-115">Katram novietojumam ir jābūt ar to saistītam novietojuma profilam noliktavā, kas apraksta novietojuma parametrus.</span><span class="sxs-lookup"><span data-stu-id="518a0-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="518a0-116">Tāpēc visas vietas, kas izmanto vienu novietojuma profilu, pēc tā iestatīšanas varēs atļaut produktu dimensiju jaukšanu.</span><span class="sxs-lookup"><span data-stu-id="518a0-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="518a0-117">Konfigurējiet novietojuma profilus, lai atļautu produktu dimensiju jaukšanu</span><span class="sxs-lookup"><span data-stu-id="518a0-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="518a0-118">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.</span><span class="sxs-lookup"><span data-stu-id="518a0-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="518a0-119">Novietojuma profilu sarakstā atlasiet **LIELAPJOMA**.</span><span class="sxs-lookup"><span data-stu-id="518a0-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="518a0-120">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="518a0-121">Kopsavilkuma cilnē **Vispārēji** iestatiet **Iespējot novietojuma produktu dimensiju specifisku sajaukšanas** opciju uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="518a0-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="518a0-122">Varat iestatīt šo opciju kā *Jā* tikai tad, ja opcija **Atļaut jauktus elementus** ir iestatīta uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="518a0-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="518a0-123">Kopsavilkuma cilnē **Vispārēji** iestatiet opciju **Iespējot novietojuma produktu dimensiju specifisku jaukšanas** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="518a0-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="518a0-124">Šajā tēmā aprakstītajā scenārijā jaukšanu var veikt tikai produktiem ar dažāda **Izmēra** dimensijām.</span><span class="sxs-lookup"><span data-stu-id="518a0-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="518a0-125">Tomēr ir pieejamas arī citas iespējas.</span><span class="sxs-lookup"><span data-stu-id="518a0-125">However, other options are also available.</span></span>
1. <span data-ttu-id="518a0-126">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="518a0-127">Izveidojiet jaunu produktu šablonu un produktu variantus</span><span class="sxs-lookup"><span data-stu-id="518a0-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="518a0-128">Dodieties uz **Preču informācijas pārvaldība \> Produkts \> Produktu šabloni**.</span><span class="sxs-lookup"><span data-stu-id="518a0-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="518a0-129">Lai izveidotu produktu šablonu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="518a0-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="518a0-130">Dialoglodziņā **Jauns produkts** iestatiet sekojošus laukus:</span><span class="sxs-lookup"><span data-stu-id="518a0-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="518a0-131">**Produkta veids:** *Elements*</span><span class="sxs-lookup"><span data-stu-id="518a0-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="518a0-132">**Produkta apakštips:** *Produkta šablons*</span><span class="sxs-lookup"><span data-stu-id="518a0-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="518a0-133">**Produkta numurs:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="518a0-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="518a0-134">**Produkta nosaukums:** *B0001 Izmērs*</span><span class="sxs-lookup"><span data-stu-id="518a0-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="518a0-135">**Produkta dimensiju grupa:** *Izmērs*</span><span class="sxs-lookup"><span data-stu-id="518a0-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="518a0-136">**Konfigurēšanas tehnoloģija:** *Iepriekš noteikts variants*</span><span class="sxs-lookup"><span data-stu-id="518a0-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="518a0-137">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="518a0-137">Select **OK**.</span></span>
1. <span data-ttu-id="518a0-138">Lapā **Produkta detaļas**, kas atrodas kopsavilkuma cilnē **Vispārīgi**, iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="518a0-139">**Automātiski ģenerēt variantus:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="518a0-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="518a0-140">**Izmēru grupa:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="518a0-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="518a0-141">Lai skatītu iepriekš definētos variantus, darbību rūtī atlasiet **Produktu varianti**.</span><span class="sxs-lookup"><span data-stu-id="518a0-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="518a0-142">Parādās lapa **Produkta varianti** un ataino variantu sarakstu no izmēru grupas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="518a0-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="518a0-143">Nodot izpildei produktus USMF kompānijai</span><span class="sxs-lookup"><span data-stu-id="518a0-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="518a0-144">Darbību rūtī atlasiet **Nodot izpildei produktus**.</span><span class="sxs-lookup"><span data-stu-id="518a0-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="518a0-145">Lapā **Atlasīt publicējamos produktus** apstipriniet, ka produkta numurs *B0001* ir sarakstā, un pēc tam atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="518a0-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="518a0-146">Atlasiet **Tālāk**, lai apstiprinātu izpildei nododamos produktu variantus.</span><span class="sxs-lookup"><span data-stu-id="518a0-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="518a0-147">Lapā **Atlasīt uzņēmumus, lai nodotu tiem izpildei** atlasiet *USMF*, un pēc tam atlasiet **Tālāk**, lai apstiprinātu atlasi.</span><span class="sxs-lookup"><span data-stu-id="518a0-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="518a0-148">Lapā **Apstiprināt atlasi** atlasiet **Pabeigt**, lai pabeigtu nodošanu izpildei.</span><span class="sxs-lookup"><span data-stu-id="518a0-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="518a0-149">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="518a0-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="518a0-150">Atjaunināt izlaisto preci USMF uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="518a0-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="518a0-151">Pārliecinieties, ka esat pierakstīts **USMF** uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="518a0-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="518a0-152">Lai pabeigtu izlaistā produkta izveidi, atlasiet **Produktu informācijas pārvaldība \> Produkti \> Izlaistie produkti**.</span><span class="sxs-lookup"><span data-stu-id="518a0-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="518a0-153">Atrodiet un atlasiet elementu ar kodu *B0001*, lai atvērtu **Izdoto produktu informācijas** lapu.</span><span class="sxs-lookup"><span data-stu-id="518a0-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="518a0-154">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="518a0-155">Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, ka lauks **Elementu modeļu grupa** ir iestatīts kā *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="518a0-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="518a0-156">Darbību rūtī cilnes **Produkts** grupā **Iestatījumi**, atlasiet **Dimensiju grupas**.</span><span class="sxs-lookup"><span data-stu-id="518a0-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="518a0-157">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-157">Set the following values:</span></span>

    - <span data-ttu-id="518a0-158">**Noliktavas dimensiju grupa:** *Izstrādājumi*</span><span class="sxs-lookup"><span data-stu-id="518a0-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="518a0-159">**Izsekošanas dimensiju grupa:** *Nav*</span><span class="sxs-lookup"><span data-stu-id="518a0-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="518a0-160">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="518a0-160">Select **OK**.</span></span>
1. <span data-ttu-id="518a0-161">Darbību rūtī cilnes **Produkts** grupā **Iestatījumi** atlasiet **Rezervācijas hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="518a0-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="518a0-162">Iestatiet lauku **Rezervācijas hierarhija** pēc *Noklusējuma*, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="518a0-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="518a0-163">Kopsavilkuma cilnes **Vispārīgi** sadaļā **Administrācija** ievērojiet, ka atlases ir atjauninātas.</span><span class="sxs-lookup"><span data-stu-id="518a0-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="518a0-164">Kopsavilkuma cilnē **Pirkumi** laukā **Cena** ievadiet *10*.</span><span class="sxs-lookup"><span data-stu-id="518a0-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="518a0-165">Kopsavilkuma cilnes **Pārvaldīt izmaksas** laukā **Elementu grupa** ievadiet *Audio*.</span><span class="sxs-lookup"><span data-stu-id="518a0-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="518a0-166">Kopsavilkuma cilnē **Pirkumi** laukā **Cena** ievadiet *10*.</span><span class="sxs-lookup"><span data-stu-id="518a0-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="518a0-167">Kopsavilkuma cilnes **Noliktava** laukā **Vienības secības grupas ID** ievadiet *ea*.</span><span class="sxs-lookup"><span data-stu-id="518a0-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="518a0-168">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="518a0-169">Novietojuma direktīvas izveide</span><span class="sxs-lookup"><span data-stu-id="518a0-169">Create a location directive</span></span>

1. <span data-ttu-id="518a0-170">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="518a0-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="518a0-171">Kreisajā rūtī, laukā **Darba pasūtījuma veids** atlasiet *Pirkuma pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="518a0-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="518a0-172">Sarakstā atlasiet novietojuma direktīvu ar nosaukumu *24 PO Direct*.</span><span class="sxs-lookup"><span data-stu-id="518a0-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="518a0-173">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="518a0-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="518a0-174">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="518a0-175">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="518a0-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="518a0-176">Jaunajai rindai jābūt pirms iepriekš esošās rindas.</span><span class="sxs-lookup"><span data-stu-id="518a0-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="518a0-177">Lai veiktu izmaiņas, izmantojiet rīkjoslas pogas **Pārvietot uz augšu** un **Pārvietot uz leju** vai mainiet esošās rindas **Secības numura** vērtību uz *2*.</span><span class="sxs-lookup"><span data-stu-id="518a0-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="518a0-178">**Nosaukums:** *Likt uz LIELAPJOMA novietojuma profila*</span><span class="sxs-lookup"><span data-stu-id="518a0-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="518a0-179">**Fiksēta novietojuma lietojums:** *Fiksētas un nefiksētas vietas*</span><span class="sxs-lookup"><span data-stu-id="518a0-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="518a0-180">**Atļaut negatīvu uzkrājumu:** *Nodzēst šo izvēles rūtiņu (=Nē)*</span><span class="sxs-lookup"><span data-stu-id="518a0-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="518a0-181">**Pakete aktivizēta:** *Nodzēst šo izvēles rūtiņu (=Nē)*</span><span class="sxs-lookup"><span data-stu-id="518a0-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="518a0-182">**Stratēģija:** *Nav*</span><span class="sxs-lookup"><span data-stu-id="518a0-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="518a0-183">Turpinot atlasīt jaunāko rindu, atlasiet **Rediģēt vaicājumu** virs režģa.</span><span class="sxs-lookup"><span data-stu-id="518a0-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="518a0-184">Vaicājuma redaktora dialoglodziņā cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu režģim.</span><span class="sxs-lookup"><span data-stu-id="518a0-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="518a0-185">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="518a0-186">**Tabula:** *Atrašanās vietas*</span><span class="sxs-lookup"><span data-stu-id="518a0-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="518a0-187">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="518a0-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="518a0-188">**Lauks:** *Atrašanās vietas profila ID*</span><span class="sxs-lookup"><span data-stu-id="518a0-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="518a0-189">**Kritēriji:** *LIELAPJOMA*</span><span class="sxs-lookup"><span data-stu-id="518a0-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="518a0-190">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="518a0-190">Select **OK**.</span></span>
1. <span data-ttu-id="518a0-191">Darbības rūts lapā **Atrašanās vietas direktīvas** atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="518a0-192">Ja izmantojat *Konsolidācijas* atrašanās vietas stratēģiju kopsavilkuma cilnes **Atrašanās vietu direktīvu darbības** laukā **Stratēģija**, tiks ignorēti kopsavilkuma cilnes **Atļautā produkta dimensiju jaukšana** lauka **Atrašanās vietu profili** iestatījumi, un elementi tiks ievietoti turpat, pat ja iestatījumi neļauj veikt šo darbību.</span><span class="sxs-lookup"><span data-stu-id="518a0-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="518a0-193">Mobilās ierīces izvēlnes elementa izveide</span><span class="sxs-lookup"><span data-stu-id="518a0-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="518a0-194">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="518a0-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="518a0-195">Darbības rūtī atlasiet **Jauns**, lai izveidotu izvēlnes elementu, ko izmantot kārtošanai.</span><span class="sxs-lookup"><span data-stu-id="518a0-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="518a0-196">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="518a0-197">**Izvēlnes elementa nosaukums:** *PO rindas saņemšana*</span><span class="sxs-lookup"><span data-stu-id="518a0-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="518a0-198">**Nosaukums:** *PO rindas saņemšana*</span><span class="sxs-lookup"><span data-stu-id="518a0-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="518a0-199">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="518a0-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="518a0-200">**Izmantot esošo darbu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="518a0-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="518a0-201">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="518a0-202">**Darba izveides process:** *Pirkšanas pasūtījuma rindas saņemšana un nosūtīšana*</span><span class="sxs-lookup"><span data-stu-id="518a0-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="518a0-203">**Ģenerēt numura zīmi:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="518a0-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="518a0-204">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="518a0-205">Konfigurēt mobilās ierīces izvēlni</span><span class="sxs-lookup"><span data-stu-id="518a0-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="518a0-206">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="518a0-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="518a0-207">Novietojuma profilu sarakstā atlasiet **Ienākošie**.</span><span class="sxs-lookup"><span data-stu-id="518a0-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="518a0-208">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="518a0-209">Sarakstā **Pieejamās izvēlnes un izvēlņu elementi** atrodiet un atlasiet **PO rindas saņemšanas** izvēlnes elementu.</span><span class="sxs-lookup"><span data-stu-id="518a0-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="518a0-210">Atlasiet labo bultiņu, lai pārvietotu **PO rindas saņemšanas** izvēlnes elementu **Izvēlņu struktūras** sarakstā.</span><span class="sxs-lookup"><span data-stu-id="518a0-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="518a0-211">Šādā veidā jūs pievienojiet savu jauno izvēlnes elementu atlasītajai izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="518a0-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="518a0-212">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="518a0-213">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="518a0-213">Scenario</span></span>

<span data-ttu-id="518a0-214">Šis demonstrācijas scenārijs parāda, kā divi dažādi produkta varianti var tikt ievietoti vienā un tajā pašā vietā, kad novietojuma profilā nav atļauti jaukti elementi, bet ir iespējota *Novietojuma produktu dimensiju jaukšanas* funkcija.</span><span class="sxs-lookup"><span data-stu-id="518a0-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="518a0-215">Šādā gadījumā jūs izmantosiet **Izmēra** variantu kā kritēriju.</span><span class="sxs-lookup"><span data-stu-id="518a0-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="518a0-216">Pirms sākat, pārliecinieties, ka noliktavā *24* ir tukšas atrašanās vietas, kas izmanto *LIELAPJOMA* atrašanās vietas profilu.</span><span class="sxs-lookup"><span data-stu-id="518a0-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="518a0-217">Pirkuma pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="518a0-217">Create a purchase order</span></span>

<span data-ttu-id="518a0-218">Jūs izveidosiet pirkuma pasūtījumu, kam ir trīs rindas: divas rindas satur vienādu produkta numuru, bet dažādus **Izmēra** variantus, bet trešā rinda ir paredzēta citam produktam, kam nav variantu.</span><span class="sxs-lookup"><span data-stu-id="518a0-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="518a0-219">Dodieties uz **Kreditori \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="518a0-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="518a0-220">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="518a0-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="518a0-221">Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="518a0-222">**Tirgotāja konts:** *1001*</span><span class="sxs-lookup"><span data-stu-id="518a0-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="518a0-223">**Noliktava:** *24*</span><span class="sxs-lookup"><span data-stu-id="518a0-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="518a0-224">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="518a0-224">Select **OK**.</span></span>
1. <span data-ttu-id="518a0-225">Pirkuma pasūtījums ir izveidots, un kopsavilkuma cilnē **Pirkuma pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="518a0-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="518a0-226">Pierakstiet pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="518a0-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="518a0-227">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="518a0-228">**Elementa numurs:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="518a0-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="518a0-229">**Lielums** *L*</span><span class="sxs-lookup"><span data-stu-id="518a0-229">**Size** *L*</span></span>
    - <span data-ttu-id="518a0-230">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="518a0-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="518a0-231">Atlasiet **Pievienot rindu** virs režģa, lai pievienotu otro pirkuma pasūtījuma rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="518a0-232">**Elementa numurs:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="518a0-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="518a0-233">**Izmērs** *XL*</span><span class="sxs-lookup"><span data-stu-id="518a0-233">**Size** *XL*</span></span>
    - <span data-ttu-id="518a0-234">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="518a0-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="518a0-235">Atlasiet **Pievienot rindu**, lai pievienotu trešo pirkuma pasūtījuma rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="518a0-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="518a0-236">**Elementa numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="518a0-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="518a0-237">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="518a0-237">**Quantity:** *1*</span></span>

<span data-ttu-id="518a0-238">1.Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="518a0-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="518a0-239">Saņemt pirkuma pasūtījumu rindas noliktavas lietotnē</span><span class="sxs-lookup"><span data-stu-id="518a0-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="518a0-240">Pierakstieties noliktavas lietotnē kā lietotājs, kurš ir iespējots noliktavā *24*.</span><span class="sxs-lookup"><span data-stu-id="518a0-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="518a0-241">Atlasiet izvēlni **Ienākošie**.</span><span class="sxs-lookup"><span data-stu-id="518a0-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="518a0-242">Atlasiet **PO rindas saņemšana**.</span><span class="sxs-lookup"><span data-stu-id="518a0-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="518a0-243">Atlasiet lauku **PONUM** un pēc tam ievadiet pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="518a0-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="518a0-244">Apstipriniet ievadni, atlasot apstiprināšanas pogu (✔) lapas apakšdaļā.</span><span class="sxs-lookup"><span data-stu-id="518a0-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="518a0-245">Ievadiet rindas numuru no pirkuma pasūtījuma, kas tiek saņemts.</span><span class="sxs-lookup"><span data-stu-id="518a0-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="518a0-246">Atlasiet lauku **LINENUM** un pēc tam izmantojiet ciparu tastatūru, lai ievadītu *1*.</span><span class="sxs-lookup"><span data-stu-id="518a0-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="518a0-247">Apstipriniet ievadīto.</span><span class="sxs-lookup"><span data-stu-id="518a0-247">Confirm your entry.</span></span>
1. <span data-ttu-id="518a0-248">Ievadiet saņemamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="518a0-248">Enter the quantity to receive.</span></span> <span data-ttu-id="518a0-249">Atlasiet plus zīmi (**+**) divas reizes, lai palielinātu lauka **Daudzums** vērtību par *2*.</span><span class="sxs-lookup"><span data-stu-id="518a0-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="518a0-250">Reģistrējiet savu ierakstu, lapas apakšdaļā atlasot pogu (✔), un pēc tam apstipriniet ievadni, vēlreiz atlasot pogu (✔).</span><span class="sxs-lookup"><span data-stu-id="518a0-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="518a0-251">Skatiet informāciju par lapu **Pirkuma pasūtījumiem: Ievietotie**.</span><span class="sxs-lookup"><span data-stu-id="518a0-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="518a0-252">Šajā lapā ir parādīts darbs, kas tika izveidots izvietošanai (1. darbs).</span><span class="sxs-lookup"><span data-stu-id="518a0-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="518a0-253">Tiek atainota atrašanās vieta, kur tiks izvietoti saņemtie pasūtījumi, numura zīme, elements, lielums un **PO rindas saņemšanas** uzdevumu skaits, ko tikko pabeidzāt.</span><span class="sxs-lookup"><span data-stu-id="518a0-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="518a0-254">Apstipriniet izvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="518a0-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="518a0-255">Pirkuma pasūtījuma 2.rindai atkārtojiet 4. – 11. soli.</span><span class="sxs-lookup"><span data-stu-id="518a0-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="518a0-256">Tomēr 8. solī norādiet daudzumu *1*.</span><span class="sxs-lookup"><span data-stu-id="518a0-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="518a0-257">Jauns izvietošanas darbs (2. darbs) ir izveidots tai pašai vietai kā 1. darbs.</span><span class="sxs-lookup"><span data-stu-id="518a0-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="518a0-258">Pirkuma pasūtījuma 2.rindai vēlreiz atkārtojiet 4. – 11. soli.</span><span class="sxs-lookup"><span data-stu-id="518a0-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="518a0-259">8. solī norādiet atlikušo daudzumu *1*.</span><span class="sxs-lookup"><span data-stu-id="518a0-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="518a0-260">Jauns izvietošanas darbs (3. darbs) ir izveidots tai pašai vietai kā 1. un 2. darbs.</span><span class="sxs-lookup"><span data-stu-id="518a0-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="518a0-261">Šī problēma rodas tāpēc, ka tiek izmantota *Konsolidētās* atrašanās vietas direktīvas stratēģija, un kopsavilkuma cilnes **Atļautā produkta dimensiju jaukšana** uz *LIELAPJOMA*, **Atrašanās vietas profiliem** iestatīšana ļauj mainīt **Izmēru** variantu, kombinējot ar atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="518a0-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="518a0-262">Pirkuma pasūtījuma 3.rindai atkārtojiet 4. – 11. soli.</span><span class="sxs-lookup"><span data-stu-id="518a0-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="518a0-263">8. solī norādiet daudzumu *1* elementam ar numuru *A0001*.</span><span class="sxs-lookup"><span data-stu-id="518a0-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="518a0-264">Jauns izvietošanas darbs (4. darbs) ir izveidots citai vietai nekā vieta, kas tiek izmantota pirkuma pasūtījuma 1. un 2. rindai.</span><span class="sxs-lookup"><span data-stu-id="518a0-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="518a0-265">Šī problēma rodas tāpēc, ka novietojuma profils nenodrošina jauktus produktus, bet tas ļauj sajaukt vienas preces šablona dimensijas.</span><span class="sxs-lookup"><span data-stu-id="518a0-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="518a0-266">Atlasiet pogu Izvēlne lapas augšmalā (dažreiz saukta par hamburgeru vai hamburgeru pogu) un pēc tam atlasiet **Atcelt**, lai izietu no **PO rindas saņemšanas**.</span><span class="sxs-lookup"><span data-stu-id="518a0-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="518a0-267">Varat atkārtot šo scenāriju, bet šoreiz iestatiet **Izmēru** - *Nē* atbilstoši kopsavilkuma cilnes sadaļā **Atļaut produktu dimensiju jaukšanu** uz *LIELAPJOMA*, **Atrašanās vietas profiliem**, lai neviens no preces dimensijām nevarētu sajaukt.</span><span class="sxs-lookup"><span data-stu-id="518a0-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="518a0-268">Šādā gadījumā, saņemot pirkuma pasūtījumu, katrs produktu variants tiks nosūtīts uz jaunu atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="518a0-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>
