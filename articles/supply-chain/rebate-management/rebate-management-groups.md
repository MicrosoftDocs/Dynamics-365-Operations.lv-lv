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
ms.openlocfilehash: c9e1cadae97bd8f0dea270deaa1a8e09bb28eb4b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020487"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="8663a-104">Atlaižu pārvaldības grupas</span><span class="sxs-lookup"><span data-stu-id="8663a-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8663a-105">Atlaižu un ieturējumu aprēķinus var vadīt pa grupām.</span><span class="sxs-lookup"><span data-stu-id="8663a-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="8663a-106">Atlaižu pārvaldības grupas var izveidot debitoriem, kreditoriem un krājumiem.</span><span class="sxs-lookup"><span data-stu-id="8663a-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="8663a-107">Tos var pievienot šablona ierakstam.</span><span class="sxs-lookup"><span data-stu-id="8663a-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="8663a-108">Atlaižu pārvaldības debitoru grupas</span><span class="sxs-lookup"><span data-stu-id="8663a-108">Rebate management customer groups</span></span>

<span data-ttu-id="8663a-109">Aprēķins klientu grupai bieži tiek izveidots uzņēmumu ķēdei, piemēram, lielveikalu ķēdei vai franšīzes uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="8663a-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="8663a-110">Šis aprēķina veids parasti ir saistīts ar atlaidi.</span><span class="sxs-lookup"><span data-stu-id="8663a-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="8663a-111">Ieturējums bieži tiek aprēķināts, neņemot vērā, kam tika pārdots kvalificētais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="8663a-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="8663a-112">Taču ir izņēmumi.</span><span class="sxs-lookup"><span data-stu-id="8663a-112">However, there are exceptions.</span></span> <span data-ttu-id="8663a-113">Piemēram, licenciāts var izveidot ieturējumu shēmu, kurā debitoru grupa A saņems 4 procentus, bet debitoru grupa B saņems tikai 3 procentus.</span><span class="sxs-lookup"><span data-stu-id="8663a-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="8663a-114">Iestatīt debitoru grupas</span><span class="sxs-lookup"><span data-stu-id="8663a-114">Set up customer groups</span></span>

<span data-ttu-id="8663a-115">Lai strādātu ar Atlaižu pārvaldības klientu grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatīšana \> Debitoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="8663a-116">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="8663a-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="8663a-117">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="8663a-118">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8663a-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="8663a-119">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="8663a-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="8663a-120">Pārvaldīt debitoru grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="8663a-120">Manage customer group assignments</span></span>

<span data-ttu-id="8663a-121">Katrs klients var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="8663a-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="8663a-122">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai klientu saraksta.</span><span class="sxs-lookup"><span data-stu-id="8663a-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="8663a-123">Lai skatītu, pievienotu vai noņemtu atlasītās grupas debitorus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="8663a-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="8663a-124">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Klientu grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="8663a-125">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="8663a-125">Select the group to manage.</span></span>
1. <span data-ttu-id="8663a-126">Darbību rūtī atlasiet **Debitori**.</span><span class="sxs-lookup"><span data-stu-id="8663a-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="8663a-127">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to debitoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="8663a-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="8663a-128">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu debitoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="8663a-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8663a-129">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8663a-130">**Debitora konts** - atlasiet debitora konta ID.</span><span class="sxs-lookup"><span data-stu-id="8663a-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="8663a-131">**Nosaukums** – ievadiet debitora nosaukumu un/vai aprakstu.</span><span class="sxs-lookup"><span data-stu-id="8663a-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="8663a-132">Lai noņemtu debitoru no grupas, atlasiet klientu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="8663a-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="8663a-133">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam debitoram, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="8663a-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="8663a-134">Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="8663a-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="8663a-135">Atlasiet debitoru, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="8663a-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="8663a-136">Darbību rūtī cilnē **Debitori** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="8663a-137">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to debitoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="8663a-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="8663a-138">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu debitoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="8663a-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8663a-139">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8663a-140">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot debitoru.</span><span class="sxs-lookup"><span data-stu-id="8663a-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="8663a-141">**Apraksts** – ievadiet grupas aprakstu (piemēram, lai izskaidrotu, kāpēc debitors ir tās dalībnieks).</span><span class="sxs-lookup"><span data-stu-id="8663a-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="8663a-142">Lai noņemtu debitoru no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="8663a-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="8663a-143">Atlaižu pārvaldības kreditoru grupas</span><span class="sxs-lookup"><span data-stu-id="8663a-143">Rebate management vendor groups</span></span>

<span data-ttu-id="8663a-144">Aprēķins kreditoru grupai bieži tiek izveidots piegādes punktu grupai.</span><span class="sxs-lookup"><span data-stu-id="8663a-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="8663a-145">Šis aprēķina veids parasti ir saistīts ar atlaidi.</span><span class="sxs-lookup"><span data-stu-id="8663a-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="8663a-146">Kreditoru grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8663a-146">Set up vendor groups</span></span>

<span data-ttu-id="8663a-147">Lai strādātu ar Atlaižu pārvaldības kreditoru grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Kreditoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="8663a-148">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="8663a-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="8663a-149">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="8663a-150">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8663a-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="8663a-151">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="8663a-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="8663a-152">Pārvaldīt kreditoru grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="8663a-152">Manage vendor group assignments</span></span>

<span data-ttu-id="8663a-153">Katrs kreditors var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="8663a-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="8663a-154">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai kreditoru saraksta.</span><span class="sxs-lookup"><span data-stu-id="8663a-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="8663a-155">Lai skatītu, pievienotu vai noņemtu atlasītās grupas kreditorus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="8663a-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="8663a-156">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Kreditoru grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="8663a-157">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="8663a-157">Select the group to manage.</span></span>
1. <span data-ttu-id="8663a-158">Darbību rūtī atlasiet **Kreditori**.</span><span class="sxs-lookup"><span data-stu-id="8663a-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="8663a-159">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to kreditoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="8663a-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="8663a-160">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu kreditoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="8663a-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8663a-161">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8663a-162">**Kreditora konts** - atlasiet kreditora konta ID.</span><span class="sxs-lookup"><span data-stu-id="8663a-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="8663a-163">**Nosaukums** – ievadiet kreditora nosaukumu un/vai aprakstu.</span><span class="sxs-lookup"><span data-stu-id="8663a-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="8663a-164">Lai noņemtu kreditoru no grupas, atlasiet klientu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="8663a-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="8663a-165">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam kreditoram, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="8663a-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="8663a-166">Dodieties uz **Kreditori \> Kreditori \> Visi kreditori**.</span><span class="sxs-lookup"><span data-stu-id="8663a-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="8663a-167">Atlasiet kreditoru, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="8663a-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="8663a-168">Darbību rūtī cilnē **Kreditori** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="8663a-169">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to kreditoru saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="8663a-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="8663a-170">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu kreditoru, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="8663a-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8663a-171">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8663a-172">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot kreditoru.</span><span class="sxs-lookup"><span data-stu-id="8663a-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="8663a-173">**Apraksts** – ievadiet grupas aprakstu (piemēram, lai izskaidrotu, kāpēc kreditors ir tās dalībnieks).</span><span class="sxs-lookup"><span data-stu-id="8663a-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="8663a-174">Lai noņemtu kreditoru no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="8663a-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="8663a-175">Krājumu atlaižu grupas</span><span class="sxs-lookup"><span data-stu-id="8663a-175">Item rebate groups</span></span>

<span data-ttu-id="8663a-176">Grupējot krājumus, jums ir lielāka elastība, aprēķinot atlaides un ieturējumus.</span><span class="sxs-lookup"><span data-stu-id="8663a-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="8663a-177">Šī pieeja bieži vien ir efektīvāks veids, kā iestatīt atlaides un atskaitījumus debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="8663a-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="8663a-178">Iestatīt krājumu grupas</span><span class="sxs-lookup"><span data-stu-id="8663a-178">Set up item groups</span></span>

<span data-ttu-id="8663a-179">Lai strādātu ar Atlaižu pārvaldības krājumu grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="8663a-180">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas.</span><span class="sxs-lookup"><span data-stu-id="8663a-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="8663a-181">Katrai grupai iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="8663a-182">**Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8663a-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="8663a-183">**Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.</span><span class="sxs-lookup"><span data-stu-id="8663a-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="8663a-184">Pārvaldīt krājumu grupu piešķires</span><span class="sxs-lookup"><span data-stu-id="8663a-184">Manage item group assignments</span></span>

<span data-ttu-id="8663a-185">Katrs krājums var piederēt jebkuram Atlaižu pārvaldības grupu skaitam.</span><span class="sxs-lookup"><span data-stu-id="8663a-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="8663a-186">Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai krājumu saraksta.</span><span class="sxs-lookup"><span data-stu-id="8663a-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="8663a-187">Varat arī pievienot krājumus, pamatojoties uz kategoriju hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="8663a-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="8663a-188">Lai skatītu, pievienotu vai noņemtu atlasītās grupas krājumus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="8663a-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="8663a-189">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="8663a-190">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="8663a-190">Select the group to manage.</span></span>
1. <span data-ttu-id="8663a-191">Darbību rūtī atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="8663a-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="8663a-192">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to krājumu saraksts, kuri jau ir atlasītās grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="8663a-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="8663a-193">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu krājumu, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="8663a-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8663a-194">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8663a-195">**Kreditora konts** - atlasiet krājuma konta ID.</span><span class="sxs-lookup"><span data-stu-id="8663a-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="8663a-196">**Preces nosaukums** – ievadiet krājuma nosaukumu un/vai aprakstu.</span><span class="sxs-lookup"><span data-stu-id="8663a-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="8663a-197">Lai noņemtu krājumu no grupas, atlasiet krājumu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="8663a-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="8663a-198">Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam krājumam, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="8663a-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="8663a-199">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="8663a-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8663a-200">Atlasiet krājumu, ar kuru jāstrādā.</span><span class="sxs-lookup"><span data-stu-id="8663a-200">Select the item to work with.</span></span>
1. <span data-ttu-id="8663a-201">Darbību rūtī cilnē **Preces** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="8663a-202">Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to grupu saraksts, kuriem jau pieder atlasītais krājums.</span><span class="sxs-lookup"><span data-stu-id="8663a-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="8663a-203">Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu krājumu, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="8663a-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8663a-204">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="8663a-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8663a-205">**Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot krājumu.</span><span class="sxs-lookup"><span data-stu-id="8663a-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="8663a-206">**Apraksts** – ievadiet grupas aprakstu (piemēram, lai izskaidrotu, kāpēc krājums ir tās dalībnieks).</span><span class="sxs-lookup"><span data-stu-id="8663a-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="8663a-207">Lai noņemtu krājumu no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="8663a-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="8663a-208">Lai grupai pievienotu krājumus, pamatojoties uz kategoriju hierarhiju, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="8663a-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="8663a-209">Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.</span><span class="sxs-lookup"><span data-stu-id="8663a-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="8663a-210">Atlasiet pārvaldāmo grupu.</span><span class="sxs-lookup"><span data-stu-id="8663a-210">Select the group to manage.</span></span>
1. <span data-ttu-id="8663a-211">Darbību rūtī atlasiet **Pievienot krājumus**.</span><span class="sxs-lookup"><span data-stu-id="8663a-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="8663a-212">Dialoglodziņa **Pievienot krājumus** laukā **Kategoriju hierarhija** atlasiet augstākā līmeņa kategoriju.</span><span class="sxs-lookup"><span data-stu-id="8663a-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="8663a-213">Krājumu hierarhija tiek atvērta kreisajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="8663a-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="8663a-214">Atlasiet meklējamo hierarhijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="8663a-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="8663a-215">Krājumi no atlasītā hierarhijas un hierarhijas līmeņa tagad ir uzskaitīti labajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="8663a-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="8663a-216">Lai strādātu ar rūti, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="8663a-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="8663a-217">Atzīmējiet katra pievienojamā krājuma izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="8663a-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="8663a-218">Atzīmējiet izvēles rūtiņu režģa galvenē, lai atlasītu visus uzskaitītos krājumus.</span><span class="sxs-lookup"><span data-stu-id="8663a-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="8663a-219">Atlasiet pogu **Rādīt atlasīto**, lai filtrētu režģi tā, lai tajā būtu redzami tikai līdz šim atlasītie krājumi.</span><span class="sxs-lookup"><span data-stu-id="8663a-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="8663a-220">Lai atgrieztos pilnajā sarakstā, vēlreiz atlasiet pogu.</span><span class="sxs-lookup"><span data-stu-id="8663a-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="8663a-221">Atlasiet **Labi**, lai atlasītajai grupai lietotu vienumu atlasi.</span><span class="sxs-lookup"><span data-stu-id="8663a-221">Select **OK** to apply your item selection to the selected group.</span></span>
