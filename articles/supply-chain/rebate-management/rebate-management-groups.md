---
title: Atlaižu pārvaldības grupas
description: Šajā tēmā ir aprakstīts, kā iestatīt Atlaižu pārvaldības grupas. Atlaižu pārvaldības grupas var izmantot atlaižu aprēķinos, un tās var pievienot šablona ierakstam.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271081"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="7823f-104">Atlaižu pārvaldības grupas</span><span class="sxs-lookup"><span data-stu-id="7823f-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7823f-105">Atlaižu pārvaldības aprēķinus var vadīt pa grupām.</span><span class="sxs-lookup"><span data-stu-id="7823f-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="7823f-106">Atlaižu pārvaldības grupas var izveidot debitoriem, kreditoriem un krājumiem.</span><span class="sxs-lookup"><span data-stu-id="7823f-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="7823f-107">Tos var pievienot šablona ierakstam.</span><span class="sxs-lookup"><span data-stu-id="7823f-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="7823f-108">Atlaižu pārvaldības debitoru grupas</span><span class="sxs-lookup"><span data-stu-id="7823f-108">Rebate management customer groups</span></span>

<span data-ttu-id="7823f-109">Aprēķins klientu grupai bieži tiek izveidots uzņēmumu ķēdei, piemēram, lielveikalu ķēdei vai franšīzes uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="7823f-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="7823f-110">Šis aprēķina veids parasti ir saistīts ar atlaidi.</span><span class="sxs-lookup"><span data-stu-id="7823f-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="7823f-111">Ieturējums bieži tiek aprēķināts, neņemot vērā, kam tika pārdots kvalificētais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="7823f-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="7823f-112">Taču ir izņēmumi.</span><span class="sxs-lookup"><span data-stu-id="7823f-112">However, there are exceptions.</span></span> <span data-ttu-id="7823f-113">Piemēram, licenciāts var izveidot ieturējumu shēmu, kurā debitoru grupa A saņems 4 procentus, bet debitoru grupa B saņems tikai 3 procentus.</span><span class="sxs-lookup"><span data-stu-id="7823f-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="7823f-114">Iestatīt debitoru grupas</span><span class="sxs-lookup"><span data-stu-id="7823f-114">Set up customer groups</span></span>

<span data-ttu-id="7823f-115">Lai strādātu ar Atlaižu pārvaldības klientu grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatīšana \> Debitoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="7823f-116">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="7823f-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="7823f-117">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7823f-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="7823f-118">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7823f-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="7823f-119">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="7823f-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="7823f-120">Pārvaldīt debitoru grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="7823f-120">Manage customer group assignments</span></span>

<span data-ttu-id="7823f-121">Katrs klients var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="7823f-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="7823f-122">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai klientu saraksta.</span><span class="sxs-lookup"><span data-stu-id="7823f-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="7823f-123">Lai skatītu, pievienotu vai noņemtu atlasītās grupas debitorus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7823f-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="7823f-124">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Klientu grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="7823f-125">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="7823f-125">Select the group to manage.</span></span>
1. <span data-ttu-id="7823f-126">Darbību rūtī atlasiet **Debitori**.</span><span class="sxs-lookup"><span data-stu-id="7823f-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="7823f-127">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to debitoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7823f-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="7823f-128">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu debitoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7823f-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7823f-129">Jaunajā rindā iestatiet šādu lauku:</span><span class="sxs-lookup"><span data-stu-id="7823f-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="7823f-130">**Debitora konts** - atlasiet debitora konta ID.</span><span class="sxs-lookup"><span data-stu-id="7823f-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="7823f-131">Lai noņemtu debitoru no grupas, atlasiet klientu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7823f-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="7823f-132">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam debitoram, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7823f-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="7823f-133">Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="7823f-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="7823f-134">Atlasiet debitoru, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="7823f-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="7823f-135">Darbību rūtī cilnē **Debitori** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="7823f-136">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to debitoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7823f-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="7823f-137">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu debitoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7823f-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7823f-138">Jaunajā rindā iestatiet šādu lauku:</span><span class="sxs-lookup"><span data-stu-id="7823f-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="7823f-139">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot debitoru.</span><span class="sxs-lookup"><span data-stu-id="7823f-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="7823f-140">Lai noņemtu debitoru no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7823f-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="7823f-141">Atlaižu pārvaldības kreditoru grupas</span><span class="sxs-lookup"><span data-stu-id="7823f-141">Rebate management vendor groups</span></span>

<span data-ttu-id="7823f-142">Aprēķins kreditoru grupai bieži tiek izveidots piegādes punktu grupai.</span><span class="sxs-lookup"><span data-stu-id="7823f-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="7823f-143">Šis aprēķina veids parasti ir saistīts ar atlaidi.</span><span class="sxs-lookup"><span data-stu-id="7823f-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="7823f-144">Kreditoru grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7823f-144">Set up vendor groups</span></span>

<span data-ttu-id="7823f-145">Lai strādātu ar Atlaižu pārvaldības kreditoru grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Kreditoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="7823f-146">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="7823f-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="7823f-147">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7823f-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="7823f-148">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7823f-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="7823f-149">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="7823f-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="7823f-150">Pārvaldīt kreditoru grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="7823f-150">Manage vendor group assignments</span></span>

<span data-ttu-id="7823f-151">Katrs kreditors var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="7823f-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="7823f-152">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai kreditoru saraksta.</span><span class="sxs-lookup"><span data-stu-id="7823f-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="7823f-153">Lai skatītu, pievienotu vai noņemtu atlasītās grupas kreditorus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7823f-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="7823f-154">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Kreditoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="7823f-155">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="7823f-155">Select the group to manage.</span></span>
1. <span data-ttu-id="7823f-156">Darbību rūtī atlasiet **Kreditori**.</span><span class="sxs-lookup"><span data-stu-id="7823f-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="7823f-157">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to kreditoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7823f-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="7823f-158">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu kreditoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7823f-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7823f-159">Jaunajā rindā iestatiet šādu lauku:</span><span class="sxs-lookup"><span data-stu-id="7823f-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="7823f-160">**Kreditora konts** - atlasiet kreditora konta ID.</span><span class="sxs-lookup"><span data-stu-id="7823f-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="7823f-161">Lai noņemtu kreditoru no grupas, atlasiet klientu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7823f-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="7823f-162">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam kreditoram, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7823f-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="7823f-163">Dodieties uz **Kreditori \> Kreditori \> Visi kreditori**.</span><span class="sxs-lookup"><span data-stu-id="7823f-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="7823f-164">Atlasiet kreditoru, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="7823f-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="7823f-165">Darbību rūtī cilnē **Kreditori** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="7823f-166">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to kreditoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7823f-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="7823f-167">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu kreditoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7823f-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7823f-168">Jaunajā rindā iestatiet šādu lauku:</span><span class="sxs-lookup"><span data-stu-id="7823f-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="7823f-169">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot kreditoru.</span><span class="sxs-lookup"><span data-stu-id="7823f-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="7823f-170">Lai noņemtu kreditoru no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7823f-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="7823f-171">Krājumu atlaižu grupas</span><span class="sxs-lookup"><span data-stu-id="7823f-171">Item rebate groups</span></span>

<span data-ttu-id="7823f-172">Grupējot krājumus, jums ir lielāka elastība, aprēķinot atlaides un ieturējumus.</span><span class="sxs-lookup"><span data-stu-id="7823f-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="7823f-173">Šī pieeja bieži vien ir efektīvāks veids, kā iestatīt atlaides un atskaitījumus debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="7823f-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="7823f-174">Iestatīt krājumu grupas</span><span class="sxs-lookup"><span data-stu-id="7823f-174">Set up item groups</span></span>

<span data-ttu-id="7823f-175">Lai strādātu ar Atlaižu pārvaldības krājumu grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="7823f-176">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="7823f-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="7823f-177">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7823f-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="7823f-178">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7823f-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="7823f-179">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="7823f-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="7823f-180">Pārvaldīt krājumu grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="7823f-180">Manage item group assignments</span></span>

<span data-ttu-id="7823f-181">Katrs krājums var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="7823f-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="7823f-182">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai krājumu saraksta.</span><span class="sxs-lookup"><span data-stu-id="7823f-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="7823f-183">Varat arī pievienot krājumus, pamatojoties uz kategoriju hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="7823f-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="7823f-184">Lai skatītu, pievienotu vai noņemtu atlasītās grupas krājumus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7823f-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="7823f-185">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="7823f-186">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="7823f-186">Select the group to manage.</span></span>
1. <span data-ttu-id="7823f-187">Darbību rūtī atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="7823f-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="7823f-188">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to krājumu saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7823f-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="7823f-189">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu krājumu, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7823f-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7823f-190">Jaunajā rindā iestatiet šādu lauku:</span><span class="sxs-lookup"><span data-stu-id="7823f-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="7823f-191">**Kreditora konts** - atlasiet krājuma konta ID.</span><span class="sxs-lookup"><span data-stu-id="7823f-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="7823f-192">Lai noņemtu krājumu no grupas, atlasiet krājumu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7823f-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="7823f-193">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam krājumam, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7823f-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="7823f-194">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="7823f-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7823f-195">Atlasiet krājumu, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="7823f-195">Select the item to work with.</span></span>
1. <span data-ttu-id="7823f-196">Darbību rūtī cilnē **Preces** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="7823f-197">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to grupu saraksts, kuriem jau pieder atlasītais krājums.</span><span class="sxs-lookup"><span data-stu-id="7823f-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="7823f-198">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu krājumu, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7823f-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7823f-199">Jaunajā rindā iestatiet šādu lauku:</span><span class="sxs-lookup"><span data-stu-id="7823f-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="7823f-200">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot krājumu.</span><span class="sxs-lookup"><span data-stu-id="7823f-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="7823f-201">Lai noņemtu krājumu no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7823f-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="7823f-202">Lai grupai pievienotu krājumus, pamatojoties uz kategoriju hierarhiju, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7823f-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7823f-203">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="7823f-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="7823f-204">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="7823f-204">Select the group to manage.</span></span>
1. <span data-ttu-id="7823f-205">Darbību rūtī atlasiet **Pievienot krājumus**.</span><span class="sxs-lookup"><span data-stu-id="7823f-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="7823f-206">Dialoglodziņa **Pievienot krājumus** laukā **Kategoriju hierarhija** atlasiet augstākā līmeņa kategoriju.</span><span class="sxs-lookup"><span data-stu-id="7823f-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="7823f-207">Krājumu hierarhija tiek atvērta kreisajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="7823f-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="7823f-208">Atlasiet meklējamo hierarhijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="7823f-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="7823f-209">Krājumi no atlasītā hierarhijas un hierarhijas līmeņa tagad ir uzskaitīti labajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="7823f-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="7823f-210">Lai strādātu ar rūti, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="7823f-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="7823f-211">Atzīmējiet katra pievienojamā krājuma izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="7823f-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="7823f-212">Atzīmējiet izvēles rūtiņu režģa galvenē, lai atlasītu visus uzskaitītos krājumus.</span><span class="sxs-lookup"><span data-stu-id="7823f-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="7823f-213">Atlasiet pogu **Rādīt atlasīto**, lai filtrētu režģi tā, lai tajā būtu redzami tikai līdz šim atlasītie krājumi.</span><span class="sxs-lookup"><span data-stu-id="7823f-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="7823f-214">Lai atgrieztos pilnajā sarakstā, vēlreiz atlasiet pogu.</span><span class="sxs-lookup"><span data-stu-id="7823f-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="7823f-215">Atlasiet **Labi**, lai atlasītajai grupai lietotu vienumu atlasi.</span><span class="sxs-lookup"><span data-stu-id="7823f-215">Select **OK** to apply your item selection to the selected group.</span></span>
