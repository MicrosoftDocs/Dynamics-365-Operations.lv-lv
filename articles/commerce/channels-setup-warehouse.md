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
ms.openlocfilehash: fe785e3bfd503193a588958ae5df0d1c0fdb9e52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002316"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="17d96-103">Noliktavas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="17d96-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="17d96-104">Šajā tēmā ir aprakstīts, kā iestatīt noliktavu, ko izmantot kopā ar jaunu kanālu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="17d96-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="17d96-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="17d96-105">Overview</span></span>

<span data-ttu-id="17d96-106">Katram Commerce kanālam ir nepieciešama konfigurēta noliktava, kas saistīta ar to.</span><span class="sxs-lookup"><span data-stu-id="17d96-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="17d96-107">Šīs procedūras nodrošina minimālo konfigurāciju, kas nepieciešama, lai iestatītu noliktavu Commerce kanālam.</span><span class="sxs-lookup"><span data-stu-id="17d96-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="17d96-108">Lai iegūtu vairāk informācijas par noliktavas iestatījumiem, lūdzu, skatiet sadaļu [Noliktavas pārvaldības pārskats](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span><span class="sxs-lookup"><span data-stu-id="17d96-108">For more information regarding warehouse setup, please see the [Warehouse management overview](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="17d96-109">Noliktavas vietas konfigurācija</span><span class="sxs-lookup"><span data-stu-id="17d96-109">Configure a warehouse site</span></span>

<span data-ttu-id="17d96-110">Pirms noliktavas iestatīšanas ir jākonfigurē noliktavas vieta.</span><span class="sxs-lookup"><span data-stu-id="17d96-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="17d96-111">Lai konfigurētu noliktavas vietu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="17d96-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="17d96-112">Navigācijas rūtī pārejiet uz **Moduļi \> Retail un Commerce \> Kanāla iestatīšana \> Vietas**.</span><span class="sxs-lookup"><span data-stu-id="17d96-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="17d96-113">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17d96-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="17d96-114">Laukā **Vieta** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="17d96-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="17d96-115">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="17d96-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="17d96-116">Sadaļā **Vispārīgi** iestatiet atbilstošu **Laika joslu**.</span><span class="sxs-lookup"><span data-stu-id="17d96-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="17d96-117">Laukā **Adreses** ievadiet adresi.</span><span class="sxs-lookup"><span data-stu-id="17d96-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="17d96-118">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="17d96-119">Tālāk redzamajā attēlā ir parādīts noliktavas vietas piemērs.</span><span class="sxs-lookup"><span data-stu-id="17d96-119">The following image shows an example warehouse site.</span></span>

![Noliktavas vietas piemērs](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="17d96-121">Noliktavas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="17d96-121">Set up a warehouse</span></span>

<span data-ttu-id="17d96-122">Lai iestatītu noliktavu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="17d96-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="17d96-123">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="17d96-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="17d96-124">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17d96-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="17d96-125">Laukā **Noliktavas** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="17d96-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="17d96-126">Ja šī ir 1:1 kartēšana mazumtirdzniecības veikalam, apsveriet iespēju izmantot veikala nosaukumu vai reģionālā sadales centra nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="17d96-126">If this is a 1:1 mapping to a retail store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="17d96-127">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="17d96-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="17d96-128">Nolaižamajā sarakstā **Vieta** atlasiet iepriekš izveidoto noliktavas vietu.</span><span class="sxs-lookup"><span data-stu-id="17d96-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="17d96-129">Laukā **Veids** atlasiet **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="17d96-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="17d96-130">Ja vēlaties iestatīt **Karantīnas noliktavu**, vispirms ir jāizpilda šīs darbības, lai izveidotu papildu noliktavu, kur **Veids** ir iestatīts uz **Karantīna**.</span><span class="sxs-lookup"><span data-stu-id="17d96-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="17d96-131">Ja vēlaties iestatīt **Tranzīta noliktavu**, vispirms ir jāizpilda šīs darbības, lai izveidotu papildu noliktavu, kur **Veids** ir iestatīts uz **Tranzīts**.</span><span class="sxs-lookup"><span data-stu-id="17d96-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="17d96-132">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="17d96-133">Iestatīt krājumu ailes</span><span class="sxs-lookup"><span data-stu-id="17d96-133">Set up inventory aisles</span></span>

<span data-ttu-id="17d96-134">Lai iestatītu aiļu dimensijas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="17d96-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="17d96-135">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Atrašanās vietas iestatīšana \> Krājumu ailes**.</span><span class="sxs-lookup"><span data-stu-id="17d96-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="17d96-136">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17d96-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="17d96-137">Nolaižamajā sarakstā **Noliktava** atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="17d96-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="17d96-138">Laukā **Aile** ievadiet nosaukumu (piemēram, Noklus.).</span><span class="sxs-lookup"><span data-stu-id="17d96-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="17d96-139">Laukā **Nosaukums** ievadiet nosaukumu (piemēram, Noklusējuma aile).</span><span class="sxs-lookup"><span data-stu-id="17d96-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="17d96-140">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="17d96-141">Iestatīt noliktavas krājumu vietas</span><span class="sxs-lookup"><span data-stu-id="17d96-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="17d96-142">Lai iestatītu noliktavas krājumu vietas standarta, bojātiem un atgrieztajiem krājumiem, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="17d96-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="17d96-143">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="17d96-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="17d96-144">Atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="17d96-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="17d96-145">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="17d96-146">Darbības rūtī atlasiet **Noliktava** un pēc tam atlasiet **Krājuma atrašanās vieta**.</span><span class="sxs-lookup"><span data-stu-id="17d96-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="17d96-147">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17d96-147">On the action pane, select **New**.</span></span> <span data-ttu-id="17d96-148">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="17d96-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="17d96-149">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="17d96-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="17d96-150">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="17d96-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="17d96-151">Lodziņā **Vieta** ievadiet noliktavas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="17d96-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="17d96-152">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="17d96-153">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17d96-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="17d96-154">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="17d96-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="17d96-155">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="17d96-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="17d96-156">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="17d96-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="17d96-157">Lodziņā **Vieta** ievadiet “Bojāts”.</span><span class="sxs-lookup"><span data-stu-id="17d96-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="17d96-158">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="17d96-159">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17d96-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="17d96-160">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="17d96-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="17d96-161">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="17d96-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="17d96-162">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="17d96-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="17d96-163">Lodziņā **Vieta** ievadiet “Atgrieztās preces”.</span><span class="sxs-lookup"><span data-stu-id="17d96-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="17d96-164">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="17d96-165">Tālāk esošajā attēlā redzams Sanfrancisko noliktavas krājumu vietas iestatījums.</span><span class="sxs-lookup"><span data-stu-id="17d96-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Krājumu novietojuma iestatījumu piemērs](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="17d96-167">Noliktavas iestatīšanas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="17d96-167">Complete warehouse setup</span></span>

<span data-ttu-id="17d96-168">Lai pabeigtu noliktavas iestatīšanu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="17d96-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="17d96-169">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="17d96-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="17d96-170">Atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="17d96-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="17d96-171">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="17d96-172">Sadaļā **Krājumu un noliktavas vadības modulis** veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="17d96-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="17d96-173">Iestatiet **Noklusējuma saņemšanas vieta** uz iepriekš izveidoto noklusējuma atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="17d96-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="17d96-174">Atlasiet **Noklusējuma izejas vieta** uz iepriekš izveidoto noklusējuma atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="17d96-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="17d96-175">Sadaļā **Adreses** ievadiet noliktavas adresi.</span><span class="sxs-lookup"><span data-stu-id="17d96-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="17d96-176">Sadaļā **Mazumtirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="17d96-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="17d96-177">Lodziņā **Noklusējuma atgriešanas vieta** ievadiet iepriekš izveidoto atgriešanas vietu.</span><span class="sxs-lookup"><span data-stu-id="17d96-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="17d96-178">Iestatiet **Veikals** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="17d96-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="17d96-179">Iestatiet **Svars** uz **1,00**.</span><span class="sxs-lookup"><span data-stu-id="17d96-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="17d96-180">Lodziņā **Noliktavas dimensijas** ievadiet iepriekš izveidoto noklusējuma vietu.</span><span class="sxs-lookup"><span data-stu-id="17d96-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="17d96-181">Sadaļā **Noliktava** iestatiet **Fiziskie negatīvie krājumi** uz **Jā** .</span><span class="sxs-lookup"><span data-stu-id="17d96-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="17d96-182">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17d96-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="17d96-183">Tālāk esošajā attēlā ir parādīta detalizēta informācija par konfigurēto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="17d96-183">The following image shows details for a configured warehouse.</span></span>

![Konfigurētas noliktavas piemērs](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="17d96-185">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="17d96-185">Additional resources</span></span>

[<span data-ttu-id="17d96-186">Noliktavas pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="17d96-186">Warehouse management overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[<span data-ttu-id="17d96-187">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="17d96-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="17d96-188">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="17d96-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="17d96-189">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="17d96-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="17d96-190">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="17d96-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="17d96-191">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="17d96-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





