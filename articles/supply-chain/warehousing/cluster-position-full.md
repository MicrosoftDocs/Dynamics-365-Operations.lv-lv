---
title: Klastera pozīcija pilna
description: Šajā tēmā ir sniegta informācija par līdzekli Pilna klastera pozīcija. Šis līdzeklis piedāvā alternatīvu stingrākai darba pārtraukuma noteikumu izpildei, ja tiek izmantota klasteru izdošana, jo tas pieļauj lielāku kļūdu robežu konteineru vai tvertņu tilpuma ierobežojumos.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3610725815b35609ee98b69b367db2945bbf166a
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433138"
---
# <a name="cluster-position-full"></a><span data-ttu-id="74814-104">Klastera pozīcija pilna</span><span class="sxs-lookup"><span data-stu-id="74814-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74814-105">Līdzeklis *Pilna klastera pozīcija* piedāvā alternatīvu stingrākai darba pārtraukuma noteikumu izpildei, ja tiek izmantota klasteru izdošana, jo tas pieļauj lielāku kļūdu robežu konteineru vai tvertņu tilpuma ierobežojumos.</span><span class="sxs-lookup"><span data-stu-id="74814-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="74814-106">Kopējā scenārijā ne visi darba pasūtījuma vienumi iekļaujas atlasītajā konteinerā.</span><span class="sxs-lookup"><span data-stu-id="74814-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="74814-107">Noliktavas darbiniekiem, kas veic klasteru izdošanu, šajā scenārijā ir dažas iespējas: viņiem ir vai nu jāsamainā konteineru uz lielāku, vai kopā ar vadītāju jāatrod citu risinājumu.</span><span class="sxs-lookup"><span data-stu-id="74814-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="74814-108">Šis līdzeklis ievieš iespēju darbināt pogu **Pilns** uz vienas no klastera darba vienībām.</span><span class="sxs-lookup"><span data-stu-id="74814-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="74814-109">Vecākās versijās šī opcija bija pieejama tikai regulārai pasūtījumu izdošanai, nevis klastera izdošanai.</span><span class="sxs-lookup"><span data-stu-id="74814-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="74814-110">Tomēr šis līdzeklis atšķiras no standarta pogas **Pilns** , jo tas atceļ atlikušo darbu.</span><span class="sxs-lookup"><span data-stu-id="74814-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="74814-111">Tas neliecina, ka lietotājs tam pašam klasterim pievieno vēl vienu nodalījumu, un tas automātiski nerada jaunu darbu.</span><span class="sxs-lookup"><span data-stu-id="74814-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="74814-112">Ieslēgt līdzekli Pilna klastera pozīcija</span><span class="sxs-lookup"><span data-stu-id="74814-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="74814-113">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="74814-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="74814-114">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="74814-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="74814-115">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="74814-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="74814-116">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="74814-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="74814-117">**Līdzekļa nosaukums:** *Pilna klastera pozīcija*</span><span class="sxs-lookup"><span data-stu-id="74814-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="74814-118">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="74814-118">Setup</span></span>

<span data-ttu-id="74814-119">Šajā sadaļā ir sniegti norādījumi, un piemērs, kas parāda, kā iestatīt un izmantot līdzekli *Pilna klastera pozīcija* .</span><span class="sxs-lookup"><span data-stu-id="74814-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="74814-120">Padarīt pieejamus datu paraugus</span><span class="sxs-lookup"><span data-stu-id="74814-120">Make sample data available</span></span>

<span data-ttu-id="74814-121">Lai, izmantojot šo [scenārija piemēru](#example-scenario), strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="74814-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="74814-122">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="74814-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="74814-123">Varat arī izmantot šo scenārija piemēru kā norādījumus darbam ar šo līdzekli ražošanas sistēmā.</span><span class="sxs-lookup"><span data-stu-id="74814-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="74814-124">Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības tiem iestatījumiem, kas šeit aprakstīti.</span><span class="sxs-lookup"><span data-stu-id="74814-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="74814-125">Klastera profili</span><span class="sxs-lookup"><span data-stu-id="74814-125">Cluster profiles</span></span>

<span data-ttu-id="74814-126">Ir jānorāda, vai klastera ID tiek ģenerēti automātiski, cik daudz pozīciju tiek izmantotas, kad klasteri tiek sadalīti, un kā izdošanas darbs ir sakārtots un pārbaudīts.</span><span class="sxs-lookup"><span data-stu-id="74814-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="74814-127">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilā ierīce \> Klastera profili**.</span><span class="sxs-lookup"><span data-stu-id="74814-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="74814-128">Saraksta rūtī atlasiet ierakstu **Izveidot klasteri**.</span><span class="sxs-lookup"><span data-stu-id="74814-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="74814-129">Kopsavilkuma cilnē **Vispārīgi** pārbaudiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="74814-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="74814-130">**Ģenerēt klastera ID:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="74814-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="74814-131">**Aktivizēt pozīcijas:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="74814-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="74814-132">**Pozīciju skaits:** *2*</span><span class="sxs-lookup"><span data-stu-id="74814-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="74814-133">**Pozīcijas nosaukums:** *Skaitlisks*</span><span class="sxs-lookup"><span data-stu-id="74814-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="74814-134">**Pārtraukt klasteri pie:** *Ievietot*</span><span class="sxs-lookup"><span data-stu-id="74814-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="74814-135">**Kārtošanas pārbaudes veids:** *Pozīcijas skenēšana*</span><span class="sxs-lookup"><span data-stu-id="74814-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="74814-136">Kopsavilkuma cilnē **Klastera šķirošana** .</span><span class="sxs-lookup"><span data-stu-id="74814-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="74814-137">Režģim ir jābūt tukšam (tas ir, tajā nedrīkst būt rindu).</span><span class="sxs-lookup"><span data-stu-id="74814-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="74814-138">Darbu veidnes</span><span class="sxs-lookup"><span data-stu-id="74814-138">Work templates</span></span>

<span data-ttu-id="74814-139">Ir jādefinē, kā ir izveidots klastera izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="74814-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="74814-140">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="74814-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="74814-141">Lapas augšmalā iestatiet lauku **Darba pasūtījuma veids** uz *Pārdošanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="74814-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="74814-142">Pārliecinieties, vai ir uzskaitītas šādas darba veidnes no demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="74814-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="74814-143">Ja tās nav pieejamas, scenāriju vairs nevarēs pabeigt.</span><span class="sxs-lookup"><span data-stu-id="74814-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="74814-144">61 SO stadija</span><span class="sxs-lookup"><span data-stu-id="74814-144">61 SO Stage</span></span>
    - <span data-ttu-id="74814-145">61 SO Klastera izdošana</span><span class="sxs-lookup"><span data-stu-id="74814-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="74814-146">Vietas direktīvas</span><span class="sxs-lookup"><span data-stu-id="74814-146">Location directives</span></span>

<span data-ttu-id="74814-147">Jānorāda, no kurienes vienumi tiek izdoti un kur tie tiek ievietoti.</span><span class="sxs-lookup"><span data-stu-id="74814-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="74814-148">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="74814-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="74814-149">Saraksta galvenē iestatiet lauku **Darba pasūtījuma veids** uz *Pārdošanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="74814-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="74814-150">Pārliecinieties, vai ir uzskaitītas šādas pārdošanas pasūtījumu direktīvas no demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="74814-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="74814-151">Ja tās nav pieejamas, scenāriju vairs nevarēs pabeigt.</span><span class="sxs-lookup"><span data-stu-id="74814-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="74814-152">61 Klastera izdošana</span><span class="sxs-lookup"><span data-stu-id="74814-152">61 Cluster pick</span></span>
    - <span data-ttu-id="74814-153">61 SO Izdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="74814-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="74814-154">Mobilās ierīces izvēlnes vienumi</span><span class="sxs-lookup"><span data-stu-id="74814-154">Mobile device menu items</span></span>

<span data-ttu-id="74814-155">Jākonfigurē mobilās ierīces izvēlnes vienumu, lai izmantotu esošu darbu, ko novirzījusi klastera izdošana.</span><span class="sxs-lookup"><span data-stu-id="74814-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="74814-156">Klastera izdošanai paredzētajā mobilās ierīces izvēlnes vienumā ir jābūt ieslēgtam parametram **Atļaut darba sadalīšanu**, un ir jāpievieno darba klase *SO Izdošana* .</span><span class="sxs-lookup"><span data-stu-id="74814-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="74814-157">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="74814-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="74814-158">Saraksta rūtī atlasiet ierakstu **Izveidot izdošanas klasteri** .</span><span class="sxs-lookup"><span data-stu-id="74814-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="74814-159">Darbības rūtī atlasiet **Rediģēt** .</span><span class="sxs-lookup"><span data-stu-id="74814-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="74814-160">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="74814-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="74814-161">**Noteic:** *Klastera izdošana*</span><span class="sxs-lookup"><span data-stu-id="74814-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="74814-162">**Ģenerēt numura zīmi:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="74814-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="74814-163">**Atļaut darba sadali** *Jā*</span><span class="sxs-lookup"><span data-stu-id="74814-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="74814-164">**Klastera profila ID:** *Klastera izveide*</span><span class="sxs-lookup"><span data-stu-id="74814-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="74814-165">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="74814-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="74814-166">Kopsavilkuma cilnē **Darba klases** pēc nepieciešamības pievienojiet šādas divas rindas:</span><span class="sxs-lookup"><span data-stu-id="74814-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="74814-167">1. rinda (parasti ir demonstrācijas datos):</span><span class="sxs-lookup"><span data-stu-id="74814-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="74814-168">**Darba klases ID:** *Pārdošana*</span><span class="sxs-lookup"><span data-stu-id="74814-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="74814-169">**Darba pasūtījuma veids:** *Pārdošanas pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="74814-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="74814-170">2. rinda (varbūt nav demonstrācijas datos):</span><span class="sxs-lookup"><span data-stu-id="74814-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="74814-171">**Darba klases ID:** *SO Izdošana*</span><span class="sxs-lookup"><span data-stu-id="74814-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="74814-172">**Darba pasūtījuma veids:** *Pārdošanas pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="74814-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="74814-173">Dodieties uz **Darba apstiprināšanas iestatījumi** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="74814-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="74814-174">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="74814-174">Select **Edit**.</span></span>
1. <span data-ttu-id="74814-175">Režģa rindā ievadiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="74814-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="74814-176">**Darba veids** - *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="74814-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="74814-177">**Preces apstiprinājums** - *Atzīmējiet izvēles rūtiņu*</span><span class="sxs-lookup"><span data-stu-id="74814-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="74814-178">Darbības rūtī atlasiet **Saglabāt** un aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="74814-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="74814-179">Izveidot izdošanas darbu</span><span class="sxs-lookup"><span data-stu-id="74814-179">Create picking work</span></span>

<span data-ttu-id="74814-180">Pirms klastera izdošanas sākšanas jāizveido daži izejošie darbi.</span><span class="sxs-lookup"><span data-stu-id="74814-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="74814-181">Iepriekš izveidotais klastera profils norāda divas klastera pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="74814-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="74814-182">Tādēļ pārdošanas pasūtījuma izdošanai jāizveido vismaz divi darba ID.</span><span class="sxs-lookup"><span data-stu-id="74814-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="74814-183">Šim scenārijam darbības tiks veiktas noliktavā *61*, un tās izmantos preces *L0101* un *T0100*.</span><span class="sxs-lookup"><span data-stu-id="74814-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="74814-184">Demonstrācijas datos jābūt pietiekamam šo vienumu rīcībā esošo krājumu daudzumam.</span><span class="sxs-lookup"><span data-stu-id="74814-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="74814-185">Pārliecinieties, vai jums ir pietiekami daudz krājumu, lai pabeigtu šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="74814-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="74814-186">1. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="74814-186">Create sales order 1</span></span>

1. <span data-ttu-id="74814-187">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="74814-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="74814-188">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu 1.</span><span class="sxs-lookup"><span data-stu-id="74814-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="74814-189">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="74814-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="74814-190">**Debitora konts:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="74814-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="74814-191">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="74814-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="74814-192">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="74814-192">Select **OK**.</span></span>
1. <span data-ttu-id="74814-193">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="74814-193">The new sales order is opened.</span></span> <span data-ttu-id="74814-194">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet rindu, kurai ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="74814-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="74814-195">**Krājuma numurs:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="74814-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="74814-196">**Daudzums:** *5*</span><span class="sxs-lookup"><span data-stu-id="74814-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="74814-197">Kopsavilkuma cilnē **Rindas detalizēta informācija** cilnē **Piegāde** iestatiet lauku **Apstiprināts nosūtīšanas datums** uz šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="74814-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="74814-198">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet otru rindu, kurai ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="74814-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="74814-199">**Krājuma numurs:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="74814-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="74814-200">**Daudzums:** *20*</span><span class="sxs-lookup"><span data-stu-id="74814-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="74814-201">Kopsavilkuma cilnē **Rindas detalizēta informācija** cilnē **Piegāde** iestatiet lauku **Apstiprināts nosūtīšanas datums** uz šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="74814-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="74814-202">Katrai rindai, ko tikko pievienojāt, veiciet šīs darbības, lai rezervētu krājumus:</span><span class="sxs-lookup"><span data-stu-id="74814-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="74814-203">Atlasiet rezervējamo rindu.</span><span class="sxs-lookup"><span data-stu-id="74814-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="74814-204">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="74814-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="74814-205">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="74814-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="74814-206">Aizveriet lapu **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="74814-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="74814-207">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="74814-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="74814-208">Kad izlaišana ir pabeigta, saņemsiet informatīvus ziņojumus, kas parāda izveidotos kopuma un noslodzes ID.</span><span class="sxs-lookup"><span data-stu-id="74814-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="74814-209">2. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="74814-209">Create sales order 2</span></span>

1. <span data-ttu-id="74814-210">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="74814-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="74814-211">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu 2.</span><span class="sxs-lookup"><span data-stu-id="74814-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="74814-212">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="74814-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="74814-213">**Debitora konts:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="74814-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="74814-214">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="74814-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="74814-215">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="74814-215">Select **OK**.</span></span>
1. <span data-ttu-id="74814-216">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="74814-216">The new sales order is opened.</span></span> <span data-ttu-id="74814-217">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet rindu, kurai ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="74814-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="74814-218">**Krājuma numurs:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="74814-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="74814-219">**Daudzums:** *20*</span><span class="sxs-lookup"><span data-stu-id="74814-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="74814-220">Kopsavilkuma cilnē **Rindas detalizēta informācija** cilnē **Piegāde** iestatiet lauku **Apstiprināts nosūtīšanas datums** uz šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="74814-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="74814-221">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet otru rindu, kurai ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="74814-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="74814-222">**Krājuma numurs:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="74814-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="74814-223">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="74814-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="74814-224">Kopsavilkuma cilnē **Rindas detalizēta informācija** cilnē **Piegāde** iestatiet lauku **Apstiprināts nosūtīšanas datums** uz šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="74814-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="74814-225">Katrai rindai, ko tikko pievienojāt, veiciet šīs darbības, lai rezervētu krājumus:</span><span class="sxs-lookup"><span data-stu-id="74814-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="74814-226">Atlasiet rezervējamo rindu.</span><span class="sxs-lookup"><span data-stu-id="74814-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="74814-227">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="74814-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="74814-228">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="74814-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="74814-229">Aizveriet lapu **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="74814-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="74814-230">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="74814-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="74814-231">Kad izlaišana ir pabeigta, saņemsiet informatīvus ziņojumus, kas parāda izveidotos kopuma un noslodzes ID.</span><span class="sxs-lookup"><span data-stu-id="74814-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="74814-232">Iegūt darba ID un unikālus noliktavas vienības identifikatorus</span><span class="sxs-lookup"><span data-stu-id="74814-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="74814-233">Ir jāizveido divi darba ID, katram no kuriem ir divas izdošanas rindas.</span><span class="sxs-lookup"><span data-stu-id="74814-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="74814-234">Sekojiet šiem soļiem, lai atrastu darba ID un unikālās noliktavas vienības piešķires.</span><span class="sxs-lookup"><span data-stu-id="74814-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="74814-235">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="74814-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="74814-236">Režģī **Pārskats** meklējiet abu tikko izveidoto pārdošanas pasūtījumu kolonnu **Pasūtījuma numurs** .</span><span class="sxs-lookup"><span data-stu-id="74814-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="74814-237">Katram pārdošanas pasūtījumam atzīmējiet atbilstošo darba ID.</span><span class="sxs-lookup"><span data-stu-id="74814-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="74814-238">Atlasiet rindu katram pārdošanas pasūtījumam, lai parādītu saistīto informāciju režģī **Rindas** .</span><span class="sxs-lookup"><span data-stu-id="74814-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="74814-239">Atzīmējiet vietu, no kuras tiks izdota katra vienība.</span><span class="sxs-lookup"><span data-stu-id="74814-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="74814-240">Dodieties uz **Krājumu vadība \> Uzziņas un atskaites \> Rīcībā esošie krājumu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="74814-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="74814-241">Darbību rūtī atlasiet **Dimensijas**, lai atvērtu dialoglodziņu **Dimensiju attēlojums** .</span><span class="sxs-lookup"><span data-stu-id="74814-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="74814-242">Pārliecinieties, vai ir atzīmētas izvēles rūtiņas **Numura zīme**, **Noliktava** un **Vienuma numurs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="74814-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="74814-243">Rūtī **Filtrs** iestatiet šādus filtrus:</span><span class="sxs-lookup"><span data-stu-id="74814-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="74814-244">**Vienuma numurs** – **ir viens no** – *L0101* un *T100*</span><span class="sxs-lookup"><span data-stu-id="74814-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="74814-245">**Noliktava** – **sākas ar** – *61*</span><span class="sxs-lookup"><span data-stu-id="74814-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="74814-246">Atzīmējiet paradītās **Vienuma numurs** vērtības.</span><span class="sxs-lookup"><span data-stu-id="74814-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="74814-247">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="74814-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="74814-248">Mobilās ierīces plūsmas izpilde – Darba apstiprinājuma iestatījums precei</span><span class="sxs-lookup"><span data-stu-id="74814-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="74814-249">Pierakstieties noliktavas programmā kā lietotājs noliktavā *61*.</span><span class="sxs-lookup"><span data-stu-id="74814-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="74814-250">Dodieties uz **Izejošie \> Izveidot klastera izdošanu**.</span><span class="sxs-lookup"><span data-stu-id="74814-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="74814-251">Tiek parādīta lapa **UZDEVUMS: Piešķirt darbu klasterim** .</span><span class="sxs-lookup"><span data-stu-id="74814-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="74814-252">Ievadiet 1. pārdošanas pasūtījuma darba ID, lai to piešķirtu klastera pozīcijai 1.</span><span class="sxs-lookup"><span data-stu-id="74814-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="74814-253">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="74814-254">Ievadiet 2. pārdošanas pasūtījuma darba ID, lai to piešķirtu klastera pozīcijai 2.</span><span class="sxs-lookup"><span data-stu-id="74814-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="74814-255">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="74814-256">Tiek parādīta lapa **UZDEVUMS: Klastera izdošanas izveide: Izdot** un tā parāda *Vienums L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="74814-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="74814-257">Tā kā klastera profils iestata pozīciju skaitu uz 2, sistēma automātiski novirza jūs uz pirmo konsolidēto izdošanu: divas paletes (PL) no vienuma *L0101*.</span><span class="sxs-lookup"><span data-stu-id="74814-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="74814-258">Šo darbību laikā jebkurā brīdī varat atlasīt cilni **Detalizēti** , lai apskatītu papildu informāciju par uzdevumu, piemēram, izdošanas vietu.</span><span class="sxs-lookup"><span data-stu-id="74814-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="74814-259">Iestatiet lauku **VIENĪBA** uz *L0101*.</span><span class="sxs-lookup"><span data-stu-id="74814-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="74814-260">Tas apstiprina vienuma numuru, kas ir nepieciešams šim izvēlnes vienumam (jūs konfigurējāt to agrāk, atlasot **Darba apstiprināšanas iestatījumi**  no lapas **Mobilās ierīces izvēlnes vienums** , kad izveidojāt šo izvēlnes vienumu).</span><span class="sxs-lookup"><span data-stu-id="74814-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="74814-261">Ievadiet unikālu noliktavas vienības identifikatoru, kas ir saistīts ar vienību izdotajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="74814-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="74814-262">Tiks izdotas divas paletes.</span><span class="sxs-lookup"><span data-stu-id="74814-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="74814-263">Iestatiet **LP** lauku uz *LP\_PICK\_01*.</span><span class="sxs-lookup"><span data-stu-id="74814-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="74814-264">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="74814-265">Tiek parādīta lapa **UZDEVUMS: Sakārtot: Klastera izdošanas izveide** .</span><span class="sxs-lookup"><span data-stu-id="74814-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="74814-266">Šeit divas izdotās paletes tiks šķirotas izdošanas pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="74814-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="74814-267">Šī pozīcija varētu būt tvertne vai konteiners, ko izmanto, lai atdalītu izdotos krājumus pēc pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="74814-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="74814-268">Skatiet informāciju, kas tiek rādīta krājumam (*L0101*) un daudzumam (*20* ea), kas tiks sašķirots pozīcijā 1 (pārdošanas pasūtījumam 1).</span><span class="sxs-lookup"><span data-stu-id="74814-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="74814-269">Iestatiet **POZICIJA NA** lauku uz *1*.</span><span class="sxs-lookup"><span data-stu-id="74814-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="74814-270">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="74814-271">Skatiet informāciju, kas tiek rādīta krājumam (*L0101*) un daudzumam (*20* ea), kas tiks sašķirots pozīcijā 2 (pārdošanas pasūtījumam 2).</span><span class="sxs-lookup"><span data-stu-id="74814-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="74814-272">Iestatiet **POZICIJA NA** lauku uz *2*.</span><span class="sxs-lookup"><span data-stu-id="74814-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="74814-273">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="74814-274">Tiek parādīta lapa **UZDEVUMS: Klastera izdošanas izveide: Izdot** un tā parāda *Vienums T0100 7 ea*.</span><span class="sxs-lookup"><span data-stu-id="74814-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="74814-275">Šādā gadījumā 1. pozīcija nevar akceptēt visu vienumu daudzumu, kas ir jāizdod, lai izpildītu 1. pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="74814-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="74814-276">Pozīcijai ir jābūt atzīmētai kā pilnai.</span><span class="sxs-lookup"><span data-stu-id="74814-276">A position must be marked as full.</span></span> <span data-ttu-id="74814-277">Šajā scenārijā jūs veiksiet daļēju otrā vienuma izdošanu.</span><span class="sxs-lookup"><span data-stu-id="74814-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="74814-278">Otrais vienums tiks daļēji izdots 1. pozīcijai, un tiks izveidots jauns darbs, lai izdotu atlikušo daudzumu pasūtījuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="74814-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="74814-279">Atlasiet pogu Izvēlne (dažreiz saukta par hamburgeru vai hamburgera pogu) un pēc tam atlasiet **Pilna pozīcija**.</span><span class="sxs-lookup"><span data-stu-id="74814-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="74814-280">Identificējiet pozīciju, kas ir pilna, un atlasiet *1*.</span><span class="sxs-lookup"><span data-stu-id="74814-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="74814-281">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="74814-282">Ievadiet izdošanas daudzumu, ko joprojām var izdot 1. pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="74814-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="74814-283">Sistēma var noteikt, kurš vienuma numurs tiek izdots.</span><span class="sxs-lookup"><span data-stu-id="74814-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="74814-284">Ievadiet *2*.</span><span class="sxs-lookup"><span data-stu-id="74814-284">Enter *2*.</span></span>
1. <span data-ttu-id="74814-285">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="74814-286">Apstipriniet vienuma nmuru, lai pabeigtu atlikušo vienumu izdošanu 2. pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="74814-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="74814-287">Iestatiet lauku **VIENĪBA** uz *T0100*.</span><span class="sxs-lookup"><span data-stu-id="74814-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="74814-288">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="74814-289">Ievadiet numura zīmi, no kuras tiek izdots vienums, iestatot, lauku **LP** uz *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="74814-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="74814-290">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="74814-291">Skatiet informāciju, kas tiek rādīta krājumam (*T0100*) un daudzumam (*2* ea), kas tiks sašķirots pozīcijā 2 (pārdošanas pasūtījumam 2).</span><span class="sxs-lookup"><span data-stu-id="74814-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="74814-292">Iestatiet **POZICIJA NA** lauku uz *2*.</span><span class="sxs-lookup"><span data-stu-id="74814-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="74814-293">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="74814-294">Skatiet informāciju, kas tiek rādīta krājumam (*T0100*) un daudzumam (*2* ea), kas tiks sašķirots pozīcijā 1 (pārdošanas pasūtījumam 1).</span><span class="sxs-lookup"><span data-stu-id="74814-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="74814-295">Iestatiet **POZICIJA NA** lauku uz *1*.</span><span class="sxs-lookup"><span data-stu-id="74814-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="74814-296">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="74814-297">Tiek parādīta lapa **UZDEVUMS: Klastera izdošanas izveide: Ievietot** .</span><span class="sxs-lookup"><span data-stu-id="74814-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="74814-298">Šajā scenārijā klastera izdošana ir pabeigta, un lietotājs ir novirzīts, lai izvietotu izdotos krājumus no 1. pozīcijas un 2. pozīcijas uz sagatavošanas vietu *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="74814-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="74814-299">Pārskatiet informāciju lapā.</span><span class="sxs-lookup"><span data-stu-id="74814-299">Review the information on the page.</span></span> <span data-ttu-id="74814-300">Tā parāda, ka kopējais daudzums *44* tiks izvietots uz sagatavošanas vietu.</span><span class="sxs-lookup"><span data-stu-id="74814-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="74814-301">Atlasiet **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="74814-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="74814-302">Tiek saņemts ziņojums "Klasteris pabeigts".</span><span class="sxs-lookup"><span data-stu-id="74814-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="74814-303">Tagad varat izmantot izvēlnes vienumu **Pārdošanas izdošana**, lai izdotu atlikušo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="74814-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="74814-304">Pēc tam varat izmantot izvēlnes vienumu **Pārdošanas iekraušana** , lai pārvietotu vienumus no sagatavošanas vietas uz iekraušanas doku.</span><span class="sxs-lookup"><span data-stu-id="74814-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>
