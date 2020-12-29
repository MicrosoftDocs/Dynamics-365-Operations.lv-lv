---
title: Noliktavas iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt noliktavu, ko izmantot kopā ar jaunu kanālu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414042"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="82763-103">Noliktavas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="82763-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="82763-104">Šajā tēmā ir aprakstīts, kā iestatīt noliktavu, ko izmantot kopā ar jaunu kanālu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="82763-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="82763-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="82763-105">Overview</span></span>

<span data-ttu-id="82763-106">Katram Commerce kanālam ir nepieciešama konfigurēta noliktava, kas saistīta ar to.</span><span class="sxs-lookup"><span data-stu-id="82763-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="82763-107">Šīs procedūras nodrošina minimālo konfigurāciju, kas nepieciešama, lai iestatītu noliktavu Commerce kanālam.</span><span class="sxs-lookup"><span data-stu-id="82763-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="82763-108">Lai iegūtu vairāk informācijas par noliktavas iestatījumiem, lūdzu, skatiet sadaļu [Noliktavas pārvaldības pārskats](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="82763-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="82763-109">Noliktavas vietas konfigurācija</span><span class="sxs-lookup"><span data-stu-id="82763-109">Configure a warehouse site</span></span>

<span data-ttu-id="82763-110">Pirms noliktavas iestatīšanas ir jākonfigurē noliktavas vieta.</span><span class="sxs-lookup"><span data-stu-id="82763-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="82763-111">Lai konfigurētu noliktavas vietu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="82763-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="82763-112">Navigācijas rūtī pārejiet uz **Moduļi \> Retail un Commerce \> Kanāla iestatīšana \> Vietas**.</span><span class="sxs-lookup"><span data-stu-id="82763-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="82763-113">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="82763-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="82763-114">Laukā **Vieta** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="82763-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="82763-115">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="82763-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="82763-116">Sadaļā **Vispārīgi** iestatiet atbilstošu **Laika joslu**.</span><span class="sxs-lookup"><span data-stu-id="82763-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="82763-117">Laukā **Adreses** ievadiet adresi.</span><span class="sxs-lookup"><span data-stu-id="82763-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="82763-118">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="82763-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="82763-119">Tālāk redzamajā attēlā ir parādīts noliktavas vietas piemērs.</span><span class="sxs-lookup"><span data-stu-id="82763-119">The following image shows an example warehouse site.</span></span>

![Noliktavas vietas piemērs](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="82763-121">Noliktavas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="82763-121">Set up a warehouse</span></span>

<span data-ttu-id="82763-122">Lai iestatītu noliktavu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="82763-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="82763-123">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="82763-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="82763-124">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="82763-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="82763-125">Laukā **Noliktavas** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="82763-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="82763-126">Ja šī ir 1:1 kartēšana veikalam, apsveriet iespēju izmantot veikala nosaukumu vai reģionālā sadales centra nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="82763-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="82763-127">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="82763-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="82763-128">Nolaižamajā sarakstā **Vieta** atlasiet iepriekš izveidoto noliktavas vietu.</span><span class="sxs-lookup"><span data-stu-id="82763-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="82763-129">Laukā **Veids** atlasiet **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="82763-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="82763-130">Ja vēlaties iestatīt **Karantīnas noliktavu**, vispirms ir jāizpilda šīs darbības, lai izveidotu papildu noliktavu, kur **Veids** ir iestatīts uz **Karantīna**.</span><span class="sxs-lookup"><span data-stu-id="82763-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="82763-131">Ja vēlaties iestatīt **Tranzīta noliktavu**, vispirms ir jāizpilda šīs darbības, lai izveidotu papildu noliktavu, kur **Veids** ir iestatīts uz **Tranzīts**.</span><span class="sxs-lookup"><span data-stu-id="82763-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="82763-132">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="82763-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="82763-133">Iestatīt krājumu ailes</span><span class="sxs-lookup"><span data-stu-id="82763-133">Set up inventory aisles</span></span>

<span data-ttu-id="82763-134">Lai iestatītu aiļu dimensijas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="82763-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="82763-135">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Atrašanās vietas iestatīšana \> Krājumu ailes**.</span><span class="sxs-lookup"><span data-stu-id="82763-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="82763-136">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="82763-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="82763-137">Nolaižamajā sarakstā **Noliktava** atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="82763-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="82763-138">Laukā **Aile** ievadiet nosaukumu (piemēram, Noklus.).</span><span class="sxs-lookup"><span data-stu-id="82763-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="82763-139">Laukā **Nosaukums** ievadiet nosaukumu (piemēram, Noklusējuma aile).</span><span class="sxs-lookup"><span data-stu-id="82763-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="82763-140">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="82763-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="82763-141">Iestatīt noliktavas krājumu vietas</span><span class="sxs-lookup"><span data-stu-id="82763-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="82763-142">Lai iestatītu noliktavas krājumu vietas standarta, bojātiem un atgrieztajiem krājumiem, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="82763-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="82763-143">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="82763-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="82763-144">Atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="82763-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="82763-145">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="82763-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="82763-146">Darbības rūtī atlasiet **Noliktava** un pēc tam atlasiet **Krājuma atrašanās vieta**.</span><span class="sxs-lookup"><span data-stu-id="82763-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="82763-147">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="82763-147">On the action pane, select **New**.</span></span> <span data-ttu-id="82763-148">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="82763-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="82763-149">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="82763-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="82763-150">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="82763-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="82763-151">Lodziņā **Vieta** ievadiet noliktavas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="82763-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="82763-152">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="82763-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="82763-153">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="82763-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="82763-154">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="82763-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="82763-155">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="82763-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="82763-156">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="82763-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="82763-157">Lodziņā **Vieta** ievadiet “Bojāts”.</span><span class="sxs-lookup"><span data-stu-id="82763-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="82763-158">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="82763-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="82763-159">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="82763-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="82763-160">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="82763-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="82763-161">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="82763-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="82763-162">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="82763-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="82763-163">Lodziņā **Vieta** ievadiet “Atgrieztās preces”.</span><span class="sxs-lookup"><span data-stu-id="82763-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="82763-164">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="82763-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="82763-165">Tālāk esošajā attēlā redzams Sanfrancisko noliktavas krājumu vietas iestatījums.</span><span class="sxs-lookup"><span data-stu-id="82763-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Krājumu novietojuma iestatījumu piemērs](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="82763-167">Noliktavas iestatīšanas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="82763-167">Complete warehouse setup</span></span>

<span data-ttu-id="82763-168">Lai pabeigtu noliktavas iestatīšanu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="82763-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="82763-169">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="82763-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="82763-170">Atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="82763-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="82763-171">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="82763-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="82763-172">Sadaļā **Krājumu un noliktavas vadības modulis** veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="82763-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="82763-173">Iestatiet **Noklusējuma saņemšanas vieta** uz iepriekš izveidoto noklusējuma atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="82763-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="82763-174">Atlasiet **Noklusējuma izejas vieta** uz iepriekš izveidoto noklusējuma atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="82763-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="82763-175">Sadaļā **Adreses** ievadiet noliktavas adresi.</span><span class="sxs-lookup"><span data-stu-id="82763-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="82763-176">Sadaļā **Mazumtirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="82763-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="82763-177">Lodziņā **Noklusējuma atgriešanas vieta** ievadiet iepriekš izveidoto atgriešanas vietu.</span><span class="sxs-lookup"><span data-stu-id="82763-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="82763-178">Iestatiet **Veikals** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="82763-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="82763-179">Iestatiet **Svars** uz **1,00**.</span><span class="sxs-lookup"><span data-stu-id="82763-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="82763-180">Lodziņā **Noliktavas dimensijas** ievadiet iepriekš izveidoto noklusējuma vietu.</span><span class="sxs-lookup"><span data-stu-id="82763-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="82763-181">Sadaļā **Noliktava** iestatiet **Fiziskie negatīvie krājumi** uz **Jā** .</span><span class="sxs-lookup"><span data-stu-id="82763-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="82763-182">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="82763-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="82763-183">Tālāk esošajā attēlā ir parādīta detalizēta informācija par konfigurēto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="82763-183">The following image shows details for a configured warehouse.</span></span>

![Konfigurētas noliktavas piemērs](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="82763-185">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="82763-185">Additional resources</span></span>

[<span data-ttu-id="82763-186">Noliktavas pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="82763-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="82763-187">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="82763-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="82763-188">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="82763-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="82763-189">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="82763-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="82763-190">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="82763-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="82763-191">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="82763-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





