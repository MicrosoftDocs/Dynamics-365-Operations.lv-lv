---
title: Atlaižu pārvaldības grupas
description: Šajā tēmā ir aprakstīts, kā iestatīt Atlaižu pārvaldības grupas. Atlaižu pārvaldības grupas var izmantot atlaižu aprēķinos, un tās var pievienot šablona ierakstam.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920065"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="7d924-104">Atlaižu pārvaldības grupas</span><span class="sxs-lookup"><span data-stu-id="7d924-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d924-105">Atlaižu un ieturējumu aprēķinus var vadīt pa grupām.</span><span class="sxs-lookup"><span data-stu-id="7d924-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="7d924-106">Atlaižu pārvaldības grupas var izveidot debitoriem, kreditoriem un krājumiem.</span><span class="sxs-lookup"><span data-stu-id="7d924-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="7d924-107">Tos var pievienot šablona ierakstam.</span><span class="sxs-lookup"><span data-stu-id="7d924-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="7d924-108">Atlaižu pārvaldības debitoru grupas</span><span class="sxs-lookup"><span data-stu-id="7d924-108">Rebate management customer groups</span></span>

<span data-ttu-id="7d924-109">Aprēķins klientu grupai bieži tiek izveidots uzņēmumu ķēdei, piemēram, lielveikalu ķēdei vai franšīzes uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="7d924-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="7d924-110">Šis aprēķina veids parasti ir saistīts ar atlaidi.</span><span class="sxs-lookup"><span data-stu-id="7d924-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="7d924-111">Ieturējums bieži tiek aprēķināts, neņemot vērā, kam tika pārdots kvalificētais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="7d924-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="7d924-112">Taču ir izņēmumi.</span><span class="sxs-lookup"><span data-stu-id="7d924-112">However, there are exceptions.</span></span> <span data-ttu-id="7d924-113">Piemēram, licenciāts var izveidot ieturējumu shēmu, kurā debitoru grupa A saņems 4 procentus, bet debitoru grupa B saņems tikai 3 procentus.</span><span class="sxs-lookup"><span data-stu-id="7d924-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="7d924-114">Iestatīt debitoru grupas</span><span class="sxs-lookup"><span data-stu-id="7d924-114">Set up customer groups</span></span>

<span data-ttu-id="7d924-115">Lai strādātu ar Atlaižu pārvaldības klientu grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatīšana \> Debitoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="7d924-116">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="7d924-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="7d924-117">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="7d924-118">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7d924-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="7d924-119">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="7d924-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="7d924-120">Pārvaldīt debitoru grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="7d924-120">Manage customer group assignments</span></span>

<span data-ttu-id="7d924-121">Katrs klients var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="7d924-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="7d924-122">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai klientu saraksta.</span><span class="sxs-lookup"><span data-stu-id="7d924-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="7d924-123">Lai skatītu, pievienotu vai noņemtu atlasītās grupas debitorus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7d924-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="7d924-124">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Klientu grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="7d924-125">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="7d924-125">Select the group to manage.</span></span>
1. <span data-ttu-id="7d924-126">Darbību rūtī atlasiet **Debitori**.</span><span class="sxs-lookup"><span data-stu-id="7d924-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="7d924-127">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to debitoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7d924-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="7d924-128">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu debitoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7d924-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7d924-129">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7d924-130">**Debitora konts** - atlasiet debitora konta ID.</span><span class="sxs-lookup"><span data-stu-id="7d924-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="7d924-131">**Nosaukums** – ievadiet debitora nosaukumu un/vai aprakstu.</span><span class="sxs-lookup"><span data-stu-id="7d924-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="7d924-132">Lai noņemtu debitoru no grupas, atlasiet klientu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7d924-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="7d924-133">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam debitoram, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7d924-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="7d924-134">Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="7d924-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="7d924-135">Atlasiet debitoru, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="7d924-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="7d924-136">Darbību rūtī cilnē **Debitori** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="7d924-137">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to debitoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7d924-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="7d924-138">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu debitoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7d924-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7d924-139">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7d924-140">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot debitoru.</span><span class="sxs-lookup"><span data-stu-id="7d924-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="7d924-141">**Apraksts** – ievadiet grupas aprakstu (piemēram, lai izskaidrotu, kāpēc debitors ir tās dalībnieks).</span><span class="sxs-lookup"><span data-stu-id="7d924-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="7d924-142">Lai noņemtu debitoru no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7d924-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="7d924-143">Atlaižu pārvaldības kreditoru grupas</span><span class="sxs-lookup"><span data-stu-id="7d924-143">Rebate management vendor groups</span></span>

<span data-ttu-id="7d924-144">Aprēķins kreditoru grupai bieži tiek izveidots piegādes punktu grupai.</span><span class="sxs-lookup"><span data-stu-id="7d924-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="7d924-145">Šis aprēķina veids parasti ir saistīts ar atlaidi.</span><span class="sxs-lookup"><span data-stu-id="7d924-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="7d924-146">Kreditoru grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7d924-146">Set up vendor groups</span></span>

<span data-ttu-id="7d924-147">Lai strādātu ar Atlaižu pārvaldības kreditoru grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Kreditoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="7d924-148">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="7d924-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="7d924-149">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="7d924-150">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7d924-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="7d924-151">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="7d924-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="7d924-152">Pārvaldīt kreditoru grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="7d924-152">Manage vendor group assignments</span></span>

<span data-ttu-id="7d924-153">Katrs kreditors var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="7d924-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="7d924-154">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai kreditoru saraksta.</span><span class="sxs-lookup"><span data-stu-id="7d924-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="7d924-155">Lai skatītu, pievienotu vai noņemtu atlasītās grupas kreditorus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7d924-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="7d924-156">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Kreditoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="7d924-157">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="7d924-157">Select the group to manage.</span></span>
1. <span data-ttu-id="7d924-158">Darbību rūtī atlasiet **Kreditori**.</span><span class="sxs-lookup"><span data-stu-id="7d924-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="7d924-159">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to kreditoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7d924-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="7d924-160">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu kreditoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7d924-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7d924-161">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7d924-162">**Kreditora konts** - atlasiet kreditora konta ID.</span><span class="sxs-lookup"><span data-stu-id="7d924-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="7d924-163">**Nosaukums** – ievadiet kreditora nosaukumu un/vai aprakstu.</span><span class="sxs-lookup"><span data-stu-id="7d924-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="7d924-164">Lai noņemtu kreditoru no grupas, atlasiet klientu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7d924-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="7d924-165">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam kreditoram, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7d924-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="7d924-166">Dodieties uz **Kreditori \> Kreditori \> Visi kreditori**.</span><span class="sxs-lookup"><span data-stu-id="7d924-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="7d924-167">Atlasiet kreditoru, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="7d924-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="7d924-168">Darbību rūtī cilnē **Kreditori** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="7d924-169">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to kreditoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7d924-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="7d924-170">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu kreditoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7d924-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7d924-171">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7d924-172">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot kreditoru.</span><span class="sxs-lookup"><span data-stu-id="7d924-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="7d924-173">**Apraksts** – ievadiet grupas aprakstu (piemēram, lai izskaidrotu, kāpēc kreditors ir tās dalībnieks).</span><span class="sxs-lookup"><span data-stu-id="7d924-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="7d924-174">Lai noņemtu kreditoru no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7d924-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="7d924-175">Krājumu atlaižu grupas</span><span class="sxs-lookup"><span data-stu-id="7d924-175">Item rebate groups</span></span>

<span data-ttu-id="7d924-176">Grupējot krājumus, jums ir lielāka elastība, aprēķinot atlaides un ieturējumus.</span><span class="sxs-lookup"><span data-stu-id="7d924-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="7d924-177">Šī pieeja bieži vien ir efektīvāks veids, kā iestatīt atlaides un atskaitījumus debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="7d924-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="7d924-178">Iestatīt krājumu grupas</span><span class="sxs-lookup"><span data-stu-id="7d924-178">Set up item groups</span></span>

<span data-ttu-id="7d924-179">Lai strādātu ar Atlaižu pārvaldības krājumu grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="7d924-180">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="7d924-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="7d924-181">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="7d924-182">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7d924-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="7d924-183">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="7d924-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="7d924-184">Pārvaldīt krājumu grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="7d924-184">Manage item group assignments</span></span>

<span data-ttu-id="7d924-185">Katrs krājums var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="7d924-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="7d924-186">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai krājumu saraksta.</span><span class="sxs-lookup"><span data-stu-id="7d924-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="7d924-187">Varat arī pievienot krājumus, pamatojoties uz kategoriju hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="7d924-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="7d924-188">Lai skatītu, pievienotu vai noņemtu atlasītās grupas krājumus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7d924-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="7d924-189">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="7d924-190">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="7d924-190">Select the group to manage.</span></span>
1. <span data-ttu-id="7d924-191">Darbību rūtī atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="7d924-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="7d924-192">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to krājumu saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="7d924-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="7d924-193">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu krājumu, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7d924-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7d924-194">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7d924-195">**Kreditora konts** - atlasiet krājuma konta ID.</span><span class="sxs-lookup"><span data-stu-id="7d924-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="7d924-196">**Preces nosaukums** – ievadiet krājuma nosaukumu un/vai aprakstu.</span><span class="sxs-lookup"><span data-stu-id="7d924-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="7d924-197">Lai noņemtu krājumu no grupas, atlasiet krājumu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7d924-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="7d924-198">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam krājumam, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7d924-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="7d924-199">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="7d924-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7d924-200">Atlasiet krājumu, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="7d924-200">Select the item to work with.</span></span>
1. <span data-ttu-id="7d924-201">Darbību rūtī cilnē **Preces** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="7d924-202">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to grupu saraksts, kuriem jau pieder atlasītais krājums.</span><span class="sxs-lookup"><span data-stu-id="7d924-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="7d924-203">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu krājumu, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="7d924-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="7d924-204">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7d924-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="7d924-205">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot krājumu.</span><span class="sxs-lookup"><span data-stu-id="7d924-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="7d924-206">**Apraksts** – ievadiet grupas aprakstu (piemēram, lai izskaidrotu, kāpēc krājums ir tās dalībnieks).</span><span class="sxs-lookup"><span data-stu-id="7d924-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="7d924-207">Lai noņemtu krājumu no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7d924-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="7d924-208">Lai grupai pievienotu krājumus, pamatojoties uz kategoriju hierarhiju, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7d924-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7d924-209">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="7d924-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="7d924-210">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="7d924-210">Select the group to manage.</span></span>
1. <span data-ttu-id="7d924-211">Darbību rūtī atlasiet **Pievienot krājumus**.</span><span class="sxs-lookup"><span data-stu-id="7d924-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="7d924-212">Dialoglodziņa **Pievienot krājumus** laukā **Kategoriju hierarhija** atlasiet augstākā līmeņa kategoriju.</span><span class="sxs-lookup"><span data-stu-id="7d924-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="7d924-213">Krājumu hierarhija tiek atvērta kreisajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="7d924-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="7d924-214">Atlasiet meklējamo hierarhijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="7d924-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="7d924-215">Krājumi no atlasītā hierarhijas un hierarhijas līmeņa tagad ir uzskaitīti labajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="7d924-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="7d924-216">Lai strādātu ar rūti, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="7d924-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="7d924-217">Atzīmējiet katra pievienojamā krājuma izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="7d924-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="7d924-218">Atzīmējiet izvēles rūtiņu režģa galvenē, lai atlasītu visus uzskaitītos krājumus.</span><span class="sxs-lookup"><span data-stu-id="7d924-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="7d924-219">Atlasiet pogu **Rādīt atlasīto**, lai filtrētu režģi tā, lai tajā būtu redzami tikai līdz šim atlasītie krājumi.</span><span class="sxs-lookup"><span data-stu-id="7d924-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="7d924-220">Lai atgrieztos pilnajā sarakstā, vēlreiz atlasiet pogu.</span><span class="sxs-lookup"><span data-stu-id="7d924-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="7d924-221">Atlasiet **Labi**, lai atlasītajai grupai lietotu vienumu atlasi.</span><span class="sxs-lookup"><span data-stu-id="7d924-221">Select **OK** to apply your item selection to the selected group.</span></span>
