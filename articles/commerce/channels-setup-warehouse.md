---
title: Noliktavas iestatīšana
description: Šajā tēmā aprakstīts, kā iestatīt noliktavu, kuru izmantot ar jauno kanālu risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800499"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="6057c-103">Noliktavas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6057c-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6057c-104">Šajā tēmā aprakstīts, kā iestatīt noliktavu, kuru izmantot ar jauno kanālu risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6057c-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6057c-105">Katram Commerce kanālam ir nepieciešama konfigurēta noliktava, kas saistīta ar to.</span><span class="sxs-lookup"><span data-stu-id="6057c-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="6057c-106">Šīs procedūras nodrošina minimālo konfigurāciju, kas nepieciešama, lai iestatītu noliktavu Commerce kanālam.</span><span class="sxs-lookup"><span data-stu-id="6057c-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="6057c-107">Lai iegūtu vairāk informācijas par noliktavas iestatījumiem, lūdzu, skatiet sadaļu [Noliktavas pārvaldības pārskats](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6057c-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="6057c-108">Noliktavas vietas konfigurācija</span><span class="sxs-lookup"><span data-stu-id="6057c-108">Configure a warehouse site</span></span>

<span data-ttu-id="6057c-109">Pirms noliktavas iestatīšanas ir jākonfigurē noliktavas vieta.</span><span class="sxs-lookup"><span data-stu-id="6057c-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="6057c-110">Lai konfigurētu noliktavas vietu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="6057c-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="6057c-111">Navigācijas rūtī pārejiet uz **Moduļi \> Retail un Commerce \> Kanāla iestatīšana \> Vietas**.</span><span class="sxs-lookup"><span data-stu-id="6057c-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="6057c-112">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6057c-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6057c-113">Laukā **Vieta** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="6057c-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="6057c-114">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="6057c-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="6057c-115">Sadaļā **Vispārīgi** iestatiet atbilstošu **Laika joslu**.</span><span class="sxs-lookup"><span data-stu-id="6057c-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="6057c-116">Laukā **Adreses** ievadiet adresi.</span><span class="sxs-lookup"><span data-stu-id="6057c-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="6057c-117">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6057c-118">Tālāk redzamajā attēlā ir parādīts noliktavas vietas piemērs.</span><span class="sxs-lookup"><span data-stu-id="6057c-118">The following image shows an example warehouse site.</span></span>

![Noliktavas vietas piemērs](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="6057c-120">Noliktavas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6057c-120">Set up a warehouse</span></span>

<span data-ttu-id="6057c-121">Lai iestatītu noliktavu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="6057c-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="6057c-122">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="6057c-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6057c-123">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6057c-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6057c-124">Laukā **Noliktavas** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6057c-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="6057c-125">Ja šī ir 1:1 kartēšana veikalam, apsveriet iespēju izmantot veikala nosaukumu vai reģionālā sadales centra nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6057c-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="6057c-126">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="6057c-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="6057c-127">Nolaižamajā sarakstā **Vieta** atlasiet iepriekš izveidoto noliktavas vietu.</span><span class="sxs-lookup"><span data-stu-id="6057c-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="6057c-128">Laukā **Veids** atlasiet **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="6057c-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="6057c-129">Ja vēlaties iestatīt **Karantīnas noliktavu**, vispirms ir jāizpilda šīs darbības, lai izveidotu papildu noliktavu, kur **Veids** ir iestatīts uz **Karantīna**.</span><span class="sxs-lookup"><span data-stu-id="6057c-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="6057c-130">Ja vēlaties iestatīt **Tranzīta noliktavu**, vispirms ir jāizpilda šīs darbības, lai izveidotu papildu noliktavu, kur **Veids** ir iestatīts uz **Tranzīts**.</span><span class="sxs-lookup"><span data-stu-id="6057c-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="6057c-131">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="6057c-132">Iestatīt krājumu ailes</span><span class="sxs-lookup"><span data-stu-id="6057c-132">Set up inventory aisles</span></span>

<span data-ttu-id="6057c-133">Lai iestatītu aiļu dimensijas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="6057c-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="6057c-134">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Atrašanās vietas iestatīšana \> Krājumu ailes**.</span><span class="sxs-lookup"><span data-stu-id="6057c-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="6057c-135">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6057c-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6057c-136">Nolaižamajā sarakstā **Noliktava** atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="6057c-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="6057c-137">Laukā **Aile** ievadiet nosaukumu (piemēram, Noklus.).</span><span class="sxs-lookup"><span data-stu-id="6057c-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="6057c-138">Laukā **Nosaukums** ievadiet nosaukumu (piemēram, Noklusējuma aile).</span><span class="sxs-lookup"><span data-stu-id="6057c-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="6057c-139">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="6057c-140">Iestatīt noliktavas krājumu vietas</span><span class="sxs-lookup"><span data-stu-id="6057c-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="6057c-141">Lai iestatītu noliktavas krājumu vietas standarta, bojātiem un atgrieztajiem krājumiem, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="6057c-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="6057c-142">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="6057c-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6057c-143">Atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="6057c-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="6057c-144">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="6057c-145">Darbības rūtī atlasiet **Noliktava** un pēc tam atlasiet **Krājuma atrašanās vieta**.</span><span class="sxs-lookup"><span data-stu-id="6057c-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="6057c-146">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6057c-146">On the action pane, select **New**.</span></span> <span data-ttu-id="6057c-147">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="6057c-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6057c-148">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6057c-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="6057c-149">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="6057c-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6057c-150">Lodziņā **Vieta** ievadiet noliktavas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6057c-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="6057c-151">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="6057c-152">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6057c-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="6057c-153">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="6057c-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6057c-154">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6057c-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="6057c-155">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="6057c-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6057c-156">Lodziņā **Vieta** ievadiet “Bojāts”.</span><span class="sxs-lookup"><span data-stu-id="6057c-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="6057c-157">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="6057c-158">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6057c-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="6057c-159">Nolaižamajam sarakstam **Noliktava** noklusējums ir jāpiešķir jaunajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="6057c-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6057c-160">Lodziņā **Aile** ievadiet iepriekš norādītās ailes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6057c-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="6057c-161">Iestatiet **Manuālā atjaunināšana** uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="6057c-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6057c-162">Lodziņā **Vieta** ievadiet “Atgrieztās preces”.</span><span class="sxs-lookup"><span data-stu-id="6057c-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="6057c-163">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="6057c-164">Tālāk esošajā attēlā redzams Sanfrancisko noliktavas krājumu vietas iestatījums.</span><span class="sxs-lookup"><span data-stu-id="6057c-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Krājumu novietojuma iestatījumu piemērs](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="6057c-166">Noliktavas iestatīšanas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="6057c-166">Complete warehouse setup</span></span>

<span data-ttu-id="6057c-167">Lai pabeigtu noliktavas iestatīšanu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="6057c-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="6057c-168">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="6057c-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6057c-169">Atlasiet iepriekš izveidoto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="6057c-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="6057c-170">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="6057c-171">Sadaļā **Krājumu un noliktavas vadības modulis** veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="6057c-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="6057c-172">Iestatiet **Noklusējuma saņemšanas vieta** uz iepriekš izveidoto noklusējuma atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="6057c-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="6057c-173">Atlasiet **Noklusējuma izejas vieta** uz iepriekš izveidoto noklusējuma atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="6057c-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="6057c-174">Sadaļā **Adreses** ievadiet noliktavas adresi.</span><span class="sxs-lookup"><span data-stu-id="6057c-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="6057c-175">Sadaļā **Mazumtirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="6057c-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="6057c-176">Lodziņā **Noklusējuma atgriešanas vieta** ievadiet iepriekš izveidoto atgriešanas vietu.</span><span class="sxs-lookup"><span data-stu-id="6057c-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="6057c-177">Iestatiet **Veikals** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="6057c-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="6057c-178">Iestatiet **Svars** uz **1,00**.</span><span class="sxs-lookup"><span data-stu-id="6057c-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="6057c-179">Lodziņā **Noliktavas dimensijas** ievadiet iepriekš izveidoto noklusējuma vietu.</span><span class="sxs-lookup"><span data-stu-id="6057c-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="6057c-180">Sadaļā **Noliktava** iestatiet **Fiziskie negatīvie krājumi** uz **Jā** .</span><span class="sxs-lookup"><span data-stu-id="6057c-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="6057c-181">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6057c-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6057c-182">Tālāk esošajā attēlā ir parādīta detalizēta informācija par konfigurēto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="6057c-182">The following image shows details for a configured warehouse.</span></span>

![Konfigurētas noliktavas piemērs](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="6057c-184">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6057c-184">Additional resources</span></span>

[<span data-ttu-id="6057c-185">Noliktavas pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="6057c-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6057c-186">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="6057c-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6057c-187">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="6057c-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6057c-188">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6057c-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="6057c-189">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6057c-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="6057c-190">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6057c-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
