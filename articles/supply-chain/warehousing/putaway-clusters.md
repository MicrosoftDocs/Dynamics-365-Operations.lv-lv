---
title: Izvietošanas klasteri
description: Izvietošanas klasteri piedāvā veidu, kā vienlaicīgi izvēlēties vairākas numura zīmes un pēc tam lietot tās izvietošanai dažādās atrašanās vietās. Tie var būt ļoti noderīgi mazumtirdzniecības uzņēmumiem, kur numura zīmes parasti nav pilnas noliktavas paletes.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a330ddccbd17c92443232fc8488e36a59235773
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512334"
---
# <a name="putaway-clusters"></a><span data-ttu-id="541ff-104">Izvietošanas klasteri</span><span class="sxs-lookup"><span data-stu-id="541ff-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="541ff-105">Izvietošanas klasteri piedāvā veidu, kā vienlaicīgi izvēlēties vairākas numura zīmes un pēc tam lietot tās izvietošanai dažādās atrašanās vietās.</span><span class="sxs-lookup"><span data-stu-id="541ff-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="541ff-106">Šis process bieži tiek saukts par *nodošanas-saņemšanas maršrutu*.</span><span class="sxs-lookup"><span data-stu-id="541ff-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="541ff-107">Izvietošanas klasteri var būt ļoti noderīgi mazumtirdzniecības uzņēmumiem, kur numura zīmes parasti nav pilnas noliktavas paletes.</span><span class="sxs-lookup"><span data-stu-id="541ff-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="541ff-108">Ieslēgt līdzekli klasteru izvietošana</span><span class="sxs-lookup"><span data-stu-id="541ff-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="541ff-109">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="541ff-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="541ff-110">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="541ff-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="541ff-111">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="541ff-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="541ff-112">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="541ff-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="541ff-113">**Līdzekļa nosaukums:** *Klasteru izvietošanas līdzeklis*</span><span class="sxs-lookup"><span data-stu-id="541ff-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="541ff-114">Piemēra scenārija iestatījumi</span><span class="sxs-lookup"><span data-stu-id="541ff-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="541ff-115">Klastera profili</span><span class="sxs-lookup"><span data-stu-id="541ff-115">Cluster profiles</span></span>

<span data-ttu-id="541ff-116">Izvietošanas klastera profils nosaka, kur krājums nonāks, pamatojoties uz novietojumu, kas ir piešķirts krājumam saņemšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="541ff-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="541ff-117">Ja ir nepieciešami dažādi klasteri, katram mobilās ierīces izvēlnes vienumam jāizveido cits izvietošanas klasters.</span><span class="sxs-lookup"><span data-stu-id="541ff-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="541ff-118">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilā ierīce \> Klastera profili**.</span><span class="sxs-lookup"><span data-stu-id="541ff-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="541ff-119">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="541ff-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="541ff-120">**Galvenes** skatā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="541ff-121">**Izvietošanas klastera profila ID:** *Klasteru izvietošana*</span><span class="sxs-lookup"><span data-stu-id="541ff-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="541ff-122">**Izvietošanas klastera profila ID nosaukums:** *Klasteru izvietošana*</span><span class="sxs-lookup"><span data-stu-id="541ff-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="541ff-123">**Klastera veids:** *izvietošana*</span><span class="sxs-lookup"><span data-stu-id="541ff-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="541ff-124">**Kārtas numurs:** akceptējiet noklusējuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="541ff-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="541ff-125">Atlasiet **Saglabāt**, lai padarītu pieejamus nepieciešamos laukus kopsavilkuma cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="541ff-126">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="541ff-127">**Klastera piešķiršanas laiks:** *Saņemšanas brīdī*</span><span class="sxs-lookup"><span data-stu-id="541ff-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="541ff-128">Šis lauks nosaka, vai izvietošanas klasteris ir jāpiešķir uzreiz pēc krājuma saņemšanas vai arī tas ir jākārto vēlāk.</span><span class="sxs-lookup"><span data-stu-id="541ff-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="541ff-129">**Klastera piešķiršanas kārtula:** *Manuāla*</span><span class="sxs-lookup"><span data-stu-id="541ff-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="541ff-130">Vai sistēmai ir automātiski jānosaka klastera piešķiršana, vai lietotājs to dara manuāli?</span><span class="sxs-lookup"><span data-stu-id="541ff-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="541ff-131">**Direktīvas kods:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="541ff-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="541ff-132">**Izvietošanas klastera atrašana:** *Kvīts*</span><span class="sxs-lookup"><span data-stu-id="541ff-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="541ff-133">Ir pieejamas šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-133">The following values are available:</span></span>

        - <span data-ttu-id="541ff-134">**Kvīts** - atrašanās vieta ir nekavējoties atrasta kvīts saņemšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="541ff-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="541ff-135">**Klastera aizvēršana** - atrašanās vieta ir atrasta, kad klasteris ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="541ff-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="541ff-136">**Lietotājs ir novirzīts** – atrašanās vieta tiek atrasta, kad numura zīme tiek saņemta no izvietošanas klastera.</span><span class="sxs-lookup"><span data-stu-id="541ff-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="541ff-137">Šādā gadījumā vieta netiek norādīta, kad tiek izveidots izvietošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="541ff-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="541ff-138">Izvietošanas laikā lietotājam ir jāskenē numura zīme vai darba ID, lai sāktu izvietošanas darbību.</span><span class="sxs-lookup"><span data-stu-id="541ff-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="541ff-139">Pēc tam sistēma atkal atrod izvietošanas vietu un paziņo lietotājam, kur novietot saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="541ff-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="541ff-140">**Izvietošanas klasteris katram lietotājam:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="541ff-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="541ff-141">Šis lauks nosaka, vai katram klasterim ir jābūt unikālam katram lietotājam, kad klasteri tiek piešķirti automātiski.</span><span class="sxs-lookup"><span data-stu-id="541ff-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="541ff-142">Tas ir pieejams tikai tad, ja **Klastera piešķiršanas kārtulas** lauks ir iestatīts uz *Automātisks*.</span><span class="sxs-lookup"><span data-stu-id="541ff-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="541ff-143">**Vienības ierobežojums:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="541ff-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="541ff-144">Šis lauks nosaka vienību, kas jāsaņem, lai profils būtu derīgs.</span><span class="sxs-lookup"><span data-stu-id="541ff-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="541ff-145">Ja tas ir atstāts tukšs, visas vienības ir derīgas.</span><span class="sxs-lookup"><span data-stu-id="541ff-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="541ff-146">**Darba vienības pārtraukums:** *Individuāls*</span><span class="sxs-lookup"><span data-stu-id="541ff-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="541ff-147">Šis lauks nosaka, vai visi krājumi ir jākonsolidē (izmantojot klastera ID un numura zīmi) uz vienas numura zīmes, kad klasteris ir slēgts, un vai tas ir jānovieto atstatus kā viena numura zīme vai atsevišķi uz saņemtajām numura plāksnēm.</span><span class="sxs-lookup"><span data-stu-id="541ff-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="541ff-148">Šis lauks nav pieejams, ja **Izvietošanas klastera atrašanas** lauks ir iestatīts uz *Kvīts*.</span><span class="sxs-lookup"><span data-stu-id="541ff-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="541ff-149">**Klasteris turpina pastāvēt kā pamata numura zīme:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="541ff-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="541ff-150">Ja šī opcija ir iestatīta uz *Jā*, kad izvietošanas solis ir pabeigts, klastera ID kļūs par pamata numura zīmi, un visi klastera ID vienumi tiks saistīti ar šo pamata numura zīmi.</span><span class="sxs-lookup"><span data-stu-id="541ff-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="541ff-151">Kopsavilkuma cilnē **Klastera šķirošana** varat definēt izvietošanas šķirošanas kritērijus.</span><span class="sxs-lookup"><span data-stu-id="541ff-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="541ff-152">Rīkjoslā atlasiet **Jauns**, lai pievienotu rindu, un tad iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="541ff-153">**Kārtas numurs:** akceptējiet noklusējuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="541ff-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="541ff-154">**Lauka nosaukums:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="541ff-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="541ff-155">Šis lauks nosaka lauku, kas šai rindai jāizmanto kā kārtošanas kritērijs.</span><span class="sxs-lookup"><span data-stu-id="541ff-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="541ff-156">**Kārtošana:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="541ff-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="541ff-157">Šis lauks nosaka, vai kārtošanai vajadzētu tikt veiktai augošā vai dilstošā secībā.</span><span class="sxs-lookup"><span data-stu-id="541ff-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="541ff-158">Kopsavilkuma cilnē **Klastera darba veidne** rīkjoslā atlasiet **Jauns**, lai pievienotu rindu, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="541ff-159">**Darba pasūtījuma tips:** *Pirkšanas pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="541ff-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="541ff-160">**Darba veidne:** *61 PP Direct*</span><span class="sxs-lookup"><span data-stu-id="541ff-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="541ff-161">Darbības rūtī atlasiet **Saglabāt** un pēc tam atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="541ff-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="541ff-162">**Klastera izvietošanas** dialoglodziņā cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu otru rindu vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="541ff-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="541ff-163">Pēc tam atjauniniet vaicājumu rindas, kā tas ir norādīts tabulā.</span><span class="sxs-lookup"><span data-stu-id="541ff-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="541ff-164">Tabula</span><span class="sxs-lookup"><span data-stu-id="541ff-164">Table</span></span> | <span data-ttu-id="541ff-165">Atveidotā tabula</span><span class="sxs-lookup"><span data-stu-id="541ff-165">Derived table</span></span> | <span data-ttu-id="541ff-166">Lauks</span><span class="sxs-lookup"><span data-stu-id="541ff-166">Field</span></span> | <span data-ttu-id="541ff-167">Kritēriji</span><span class="sxs-lookup"><span data-stu-id="541ff-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="541ff-168">Ir spēkā</span><span class="sxs-lookup"><span data-stu-id="541ff-168">Work</span></span> | <span data-ttu-id="541ff-169">Ir spēkā</span><span class="sxs-lookup"><span data-stu-id="541ff-169">Work</span></span> | <span data-ttu-id="541ff-170">Noliktava</span><span class="sxs-lookup"><span data-stu-id="541ff-170">Warehouse</span></span> | <span data-ttu-id="541ff-171">*61*</span><span class="sxs-lookup"><span data-stu-id="541ff-171">*61*</span></span> |
    | <span data-ttu-id="541ff-172">Ir spēkā</span><span class="sxs-lookup"><span data-stu-id="541ff-172">Work</span></span> | <span data-ttu-id="541ff-173">Ir spēkā</span><span class="sxs-lookup"><span data-stu-id="541ff-173">Work</span></span> | <span data-ttu-id="541ff-174">Darba ID</span><span class="sxs-lookup"><span data-stu-id="541ff-174">Work ID</span></span> | <span data-ttu-id="541ff-175">Atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="541ff-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="541ff-176">Atlasiet **Labi**, lai saglabātu vaicājumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="541ff-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="541ff-177">Darbības rūtī atlasiet **Saglabāt** un aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="541ff-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="541ff-178">Klastera profila lauki, kas parādās pelēkoti, kad opcija **Ģenerēt klastera ID** ir iestatīta uz *Jā*, nav pieejami, un netiks ņemti vērā, ja tiek izmantots šis līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="541ff-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="541ff-179">Mobilās ierīces izvēlnes vienumi</span><span class="sxs-lookup"><span data-stu-id="541ff-179">Mobile device menu items</span></span>

<span data-ttu-id="541ff-180">Šim līdzeklim ir pieejamas divas jaunas mobilās ierīces izvēlnes vienības.</span><span class="sxs-lookup"><span data-stu-id="541ff-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="541ff-181">Izvēlnes elements **Saņemt un kārtot klasteri** tiek lietots, lai sakārtotu saņemto krājumu izvietošanas klasterī pēc saņemšanas.</span><span class="sxs-lookup"><span data-stu-id="541ff-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="541ff-182">Izvēlnes vienums **Klastera izvietošana** tiek izmantots, lai pēc piešķiršanas izvietotu klasteri.</span><span class="sxs-lookup"><span data-stu-id="541ff-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="541ff-183">Saņemt un kārtot klasteri</span><span class="sxs-lookup"><span data-stu-id="541ff-183">Receive and sort cluster</span></span>

<span data-ttu-id="541ff-184">Izveidot jaunu mobilās ierīces izvēlnes elementu krājumu un šķirošanas saņemšanai klasterī.</span><span class="sxs-lookup"><span data-stu-id="541ff-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="541ff-185">Šis izvēlnes elements izveidos ienākošo darbu pēc krājumu saņemšanas, kas norāda, ka saņemšanas izvēlnes elements tiks izmantots izvietošanas klasteriem.</span><span class="sxs-lookup"><span data-stu-id="541ff-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="541ff-186">Izvēlnes elementu **Saņemt un kārtot klasteri** var izmantot ar šādiem saņemšanas izvēlnes elementiem:</span><span class="sxs-lookup"><span data-stu-id="541ff-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="541ff-187">Pirkšanas pasūtījuma rindas saņemšana</span><span class="sxs-lookup"><span data-stu-id="541ff-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="541ff-188">Pirkšanas pasūtījuma krājuma saņemšana</span><span class="sxs-lookup"><span data-stu-id="541ff-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="541ff-189">Kravas krājuma saņemšana</span><span class="sxs-lookup"><span data-stu-id="541ff-189">Load item receiving</span></span>

1. <span data-ttu-id="541ff-190">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="541ff-191">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="541ff-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="541ff-192">**Galvenes** skatā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="541ff-193">**Izvēlnes elementa nosaukums:** *Saņemt un kārtot klasteri*</span><span class="sxs-lookup"><span data-stu-id="541ff-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="541ff-194">**Virsraksts:** *Saņemt un kārtot klasteri*</span><span class="sxs-lookup"><span data-stu-id="541ff-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="541ff-195">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="541ff-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="541ff-196">**Izmantot esošo darbu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="541ff-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="541ff-197">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="541ff-198">**Darba izveides process:** *Pirkšanas pasūtījuma krājuma saņemšana*</span><span class="sxs-lookup"><span data-stu-id="541ff-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="541ff-199">**Ģenerēt numura zīmi:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="541ff-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="541ff-200">**Piešķirt izvietošanas klasteri:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="541ff-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="541ff-201">Opcija **Piešķirt izvietošanas klasteri** ir pieejama tikai vienas darbības *Darba izveides procesa* aktivitātes saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="541ff-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="541ff-202">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="541ff-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="541ff-203">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="541ff-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="541ff-204">Klastera izvietošana</span><span class="sxs-lookup"><span data-stu-id="541ff-204">Cluster putaway</span></span>

<span data-ttu-id="541ff-205">Izveidot jaunu mobilās ierīces izvēlnes elementu klastera izvietošanai pēc tā piešķiršanas.</span><span class="sxs-lookup"><span data-stu-id="541ff-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="541ff-206">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="541ff-207">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="541ff-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="541ff-208">**Galvenes** skatā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="541ff-209">**Izvēlnes vienuma nosaukums:** *Klastera izvietošana*</span><span class="sxs-lookup"><span data-stu-id="541ff-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="541ff-210">**Virsraksts:** *Klastera izvietošana*</span><span class="sxs-lookup"><span data-stu-id="541ff-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="541ff-211">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="541ff-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="541ff-212">**Izmantot esošo darbu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="541ff-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="541ff-213">Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Noteicējs:** uz *Klastera izvietošana*.</span><span class="sxs-lookup"><span data-stu-id="541ff-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="541ff-214">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="541ff-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="541ff-215">Kopsavilkuma cilnē **Darba klases** iestatiet šīs mobilās ierīces izvēlnes vienumam derīgo darba klasi:</span><span class="sxs-lookup"><span data-stu-id="541ff-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="541ff-216">**Darba klases ID:** *Pirkums*</span><span class="sxs-lookup"><span data-stu-id="541ff-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="541ff-217">**Darba pasūtījuma tips:** *Pirkšanas pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="541ff-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="541ff-218">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="541ff-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="541ff-219">Mobilās ierīces izvēlne</span><span class="sxs-lookup"><span data-stu-id="541ff-219">Mobile device menu</span></span>

<span data-ttu-id="541ff-220">Pievienojiet izvēlnes elementus, ko tikko izveidojāt mobilās programmas saņemšanas izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="541ff-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="541ff-221">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="541ff-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="541ff-222">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="541ff-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="541ff-223">Izvēlnes sarakstā atlasiet **Ienākošie**.</span><span class="sxs-lookup"><span data-stu-id="541ff-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="541ff-224">Sarakstā **Pieejamās izvēlnes un izvēļņu elementi** atrodiet un atlasiet izvēlnes elementu **Saņemt un kārtot klasteru**.</span><span class="sxs-lookup"><span data-stu-id="541ff-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="541ff-225">Atlasiet labo bultiņu, lai pārvietotu atlasītās izvēlnes elementu **Izvēlņu struktūras** sarakstā.</span><span class="sxs-lookup"><span data-stu-id="541ff-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="541ff-226">Izmantojiet pogu uz augšu vai uz leju, lai pārvietotu izvēlnes elementu vēlamajā pozīcijā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="541ff-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="541ff-227">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="541ff-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="541ff-228">Atkārtojiet soļus no 4. līdz 7., lai pievienotu atlikušos izvēlnes elementus:</span><span class="sxs-lookup"><span data-stu-id="541ff-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="541ff-229">Piešķirt klasteri</span><span class="sxs-lookup"><span data-stu-id="541ff-229">Assign cluster</span></span>
    - <span data-ttu-id="541ff-230">Klastera izvietošana</span><span class="sxs-lookup"><span data-stu-id="541ff-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="541ff-231">Piemērs</span><span class="sxs-lookup"><span data-stu-id="541ff-231">Example scenario</span></span>

<span data-ttu-id="541ff-232">Šis scenārijs simulē izvietošanas klastera apstrādi.</span><span class="sxs-lookup"><span data-stu-id="541ff-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="541ff-233">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="541ff-233">Create a purchase order</span></span>

1. <span data-ttu-id="541ff-234">Dodieties uz **Kreditori \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="541ff-235">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="541ff-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="541ff-236">Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="541ff-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="541ff-237">**Tirgotāja konts:** *1001*</span><span class="sxs-lookup"><span data-stu-id="541ff-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="541ff-238">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="541ff-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="541ff-239">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-239">Select **OK**.</span></span>

    <span data-ttu-id="541ff-240">Atveras lapa **Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="541ff-241">Lapā **Visi pirkšanas pasūtījumi**, kas atrodas kopsavilkuma cilnē **Pirkšanas pasūtījuma rindas**, izmantojiet pogu **Pievienot rindu**, lai pievienotu šādas rindas:</span><span class="sxs-lookup"><span data-stu-id="541ff-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="541ff-242">Pirkšanas pasūtījuma 1. rinda:</span><span class="sxs-lookup"><span data-stu-id="541ff-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="541ff-243">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="541ff-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="541ff-244">**Daudzums:** *10*</span><span class="sxs-lookup"><span data-stu-id="541ff-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="541ff-245">Pirkšanas pasūtījuma 2. rinda:</span><span class="sxs-lookup"><span data-stu-id="541ff-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="541ff-246">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="541ff-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="541ff-247">**Daudzums:** *20*</span><span class="sxs-lookup"><span data-stu-id="541ff-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="541ff-248">Pirkšanas pasūtījuma 3. rinda:</span><span class="sxs-lookup"><span data-stu-id="541ff-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="541ff-249">**Krājuma numurs:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="541ff-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="541ff-250">**Daudzums:** *30*</span><span class="sxs-lookup"><span data-stu-id="541ff-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="541ff-251">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="541ff-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="541ff-252">Pierakstiet pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="541ff-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="541ff-253">Saņemt krājumu un nodot to tālāk prom no mobilās ierīces</span><span class="sxs-lookup"><span data-stu-id="541ff-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="541ff-254">Saņemt un kārtot krājumus klasterī</span><span class="sxs-lookup"><span data-stu-id="541ff-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="541ff-255">Pierakstieties noliktavas lietotnē kā lietotājs, kurš ir iespējots noliktavā *61*.</span><span class="sxs-lookup"><span data-stu-id="541ff-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="541ff-256">Galvenajā izvēlnē atlasiet **Ienākošs**.</span><span class="sxs-lookup"><span data-stu-id="541ff-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="541ff-257">Izvēlnē **Ienākošie** atlasiet **Saņemt un kārtot klasteri**.</span><span class="sxs-lookup"><span data-stu-id="541ff-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="541ff-258">Laukā **Ponum** ievadiet savu pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="541ff-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="541ff-259">Atlasiet pogu **Labi** (atzīmes poga).</span><span class="sxs-lookup"><span data-stu-id="541ff-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="541ff-260">Atlasiet lauku **Krājums**, ievadiet krājuma numuru *A0001* un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="541ff-261">Atlasiet lauku **Daudzums**, ievadiet *10*, izmantojot ciparu tastatūru, un pēc tam atlasiet izvēles rūtiņas pogu.</span><span class="sxs-lookup"><span data-stu-id="541ff-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="541ff-262">Uzdevumu lapā **Daudzums** atlasiet **Labi** (izvēles rūtiņas poga), lai apstiprinātu ievadīto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="541ff-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="541ff-263">Uzdevumu lapā **Krājums** atlasiet **Labi**, lai apstiprinātu, ka krājums *A0001* tika ievadīts .</span><span class="sxs-lookup"><span data-stu-id="541ff-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="541ff-264">Atlasiet lauku **Klastera ID** un ievadiet vērtību, lai piešķirtu izveidoto klastera ID.</span><span class="sxs-lookup"><span data-stu-id="541ff-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="541ff-265">Šeit ievadītais ID tiks izmantots, kad tiek saņemti divi atlikušie pirkšanas pasūtījuma krājumi.</span><span class="sxs-lookup"><span data-stu-id="541ff-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="541ff-266">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-266">Select **OK**.</span></span>

    <span data-ttu-id="541ff-267">Parādās uzdevumu lapa **Ponum** un parādīts ziņojums "Darbs pabeigts".</span><span class="sxs-lookup"><span data-stu-id="541ff-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="541ff-268">Krājums *A0001* tagad ir saņemts *RECV* atrašanās vietā un piešķirts klastera ID, ko ievadījāt 10. solī.</span><span class="sxs-lookup"><span data-stu-id="541ff-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="541ff-269">Atkārtojiet 4. – 11. soli, lai saņemtu atlikušos divus krājumus no pirkšanas pasūtījuma, un piešķiriet tiem klastera ID:</span><span class="sxs-lookup"><span data-stu-id="541ff-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="541ff-270">Preces *A0002* daudzums *20*</span><span class="sxs-lookup"><span data-stu-id="541ff-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="541ff-271">Preces *M9215* daudzums *30*</span><span class="sxs-lookup"><span data-stu-id="541ff-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="541ff-272">Aizvērt klasteri</span><span class="sxs-lookup"><span data-stu-id="541ff-272">Close the cluster</span></span>

<span data-ttu-id="541ff-273">Pirms krājumu var izvietot klasterī, klasteris ir jāslēdz.</span><span class="sxs-lookup"><span data-stu-id="541ff-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="541ff-274">Supply Chain Management dodieties uz **Noliktavas pārvaldība \> Darbs \> Izejošie \> Darba klasteri**.</span><span class="sxs-lookup"><span data-stu-id="541ff-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="541ff-275">Lapā **Darba klasteri** sadaļā **Darba klasteris** meklējiet lauku **Klastera ID**, ko ievadījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="541ff-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="541ff-276">Ja klasteris netiek norādīts, iespējams, tas jau ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="541ff-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="541ff-277">Lai noteiktu, vai klasteris tika slēgts, atzīmējiet izvēles rūtiņu **Rādīt slēgto darbu** un meklējiet klastera ID, ko ievadījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="541ff-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="541ff-278">Pēc tam izpildiet kādu no norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="541ff-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="541ff-279">Ja klasteris ir slēgts, izlaidiet atlikušos šīs procedūras soļus un pārejiet uz nākamo procedūru [Novietot klasteri tālāk](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="541ff-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="541ff-280">Ja klasteris nav slēgts, izpildiet atlikušos šīs procedūras soļus, lai manuāli aizvērtu klasteri.</span><span class="sxs-lookup"><span data-stu-id="541ff-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="541ff-281">Tad pārejiet uz nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="541ff-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="541ff-282">Sadaļā **Darba klasteris** atlasiet klastera ID, ko ievadījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="541ff-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="541ff-283">Darbību rūtī atlasiet **Slēgt klasteri**.</span><span class="sxs-lookup"><span data-stu-id="541ff-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="541ff-284">Pēc klastera slēgšanas tas vairs netiek parādīts sadaļā **Darba klasteris** (ja vien nav atzīmētā izvēles rūtiņa **Parādīt slēgto darbu**).</span><span class="sxs-lookup"><span data-stu-id="541ff-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="541ff-285">Klastera izvietošana</span><span class="sxs-lookup"><span data-stu-id="541ff-285">Put the cluster away</span></span>

1. <span data-ttu-id="541ff-286">Pierakstieties noliktavas lietotnē kā lietotājs, kurš ir iespējots noliktavā *61*.</span><span class="sxs-lookup"><span data-stu-id="541ff-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="541ff-287">Galvenajā izvēlnē atlasiet **Ienākošs**.</span><span class="sxs-lookup"><span data-stu-id="541ff-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="541ff-288">Izvēlnē **Ienākošie** atlasiet **Klastera izvietošana**.</span><span class="sxs-lookup"><span data-stu-id="541ff-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="541ff-289">Atlasiet **Klastera ID** un ievadiet klastera ID, ko iepriekš ievadījāt slēgtajam klasterim.</span><span class="sxs-lookup"><span data-stu-id="541ff-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="541ff-290">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-290">Select **OK**.</span></span>

    <span data-ttu-id="541ff-291">Tiek parādīta lapa **Klastera izvietošana: Izdot**.</span><span class="sxs-lookup"><span data-stu-id="541ff-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="541ff-292">Tas rāda klastera ID, izdošanas vietu, krājumus (tiks rādītas *Vairākas* vērtības) un kopējo daudzumu klasterī, kas ir jāizdod.</span><span class="sxs-lookup"><span data-stu-id="541ff-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="541ff-293">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="541ff-293">Select **OK**.</span></span>

    <span data-ttu-id="541ff-294">Tiek parādīta lapa **Klastera izvietošana: Izvietot**.</span><span class="sxs-lookup"><span data-stu-id="541ff-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="541ff-295">**Izvietot** instrukcijās tiek identificēts klastera ID, novietojums, krājumi, kopējais daudzums un numura zīmes ID krājumiem, kas saņemti klasterī.</span><span class="sxs-lookup"><span data-stu-id="541ff-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="541ff-296">Ir standarta opcijas, lai ignorētu vai izpildītu šo darbību.</span><span class="sxs-lookup"><span data-stu-id="541ff-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="541ff-297">![Klastera izvietošana: izvietot lapu](media/Cluster_putaway-Put.png "Klastera izvietošana: izvietot lapu")</span><span class="sxs-lookup"><span data-stu-id="541ff-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="541ff-298">Atlasiet **Labi**, lai apstiprinātu klastera izvietošanu.</span><span class="sxs-lookup"><span data-stu-id="541ff-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="541ff-299">Tiek parādīts ziņojums "Klasteris pabeigts".</span><span class="sxs-lookup"><span data-stu-id="541ff-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="541ff-300">Piezīmes un padomi</span><span class="sxs-lookup"><span data-stu-id="541ff-300">Notes and tips</span></span>

<span data-ttu-id="541ff-301">Gadījumos, kad klastera ID ir kļuvis par pamatnumura zīmi ligzdotai paletei, novietošanas pozīcija tiek norādīta automātiski, kad tiek skenēts klastera ID.</span><span class="sxs-lookup"><span data-stu-id="541ff-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="541ff-302">Neviena papildu numura zīme nedrīkst tikt skenēta, pat ja numura zīmes ģenerēšana ir iestatīta uz manuālu.</span><span class="sxs-lookup"><span data-stu-id="541ff-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>