---
title: Krājumu vecumstruktūru pārskatu piemēri un loģika
description: Šajā tēmā sniegti daži piemēri, kas parāda, kā interpretēt Krājumu vecumstruktūru pārskata rezultātus.
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484534"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="236c7-103">Krājumu vecumstruktūru pārskatu piemēri un loģika</span><span class="sxs-lookup"><span data-stu-id="236c7-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="236c7-104">Šajā tēmā sniegti daži piemēri, kas parāda, kā interpretēt **Krājumu vecumstruktūru** pārskata rezultātus.</span><span class="sxs-lookup"><span data-stu-id="236c7-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="236c7-105">Šajā pārskatā ir iedalīti rīcībā esošie daudzumi un krājumu vērtības atlasītajam krājumam vai krājumu grupai vairākos perioda intervālos.</span><span class="sxs-lookup"><span data-stu-id="236c7-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="236c7-106">Šī tēma rāda arī pārskata iekšējo loģiku.</span><span class="sxs-lookup"><span data-stu-id="236c7-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="236c7-107">Šīs tēmas piemēri rāda rezultātus, kas ir sniegti standarta **Krājumu novecošanas** pārskatā.</span><span class="sxs-lookup"><span data-stu-id="236c7-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="236c7-108">Tomēr parasti ir ieteicams izmantot šī pārskata [Krājumu novecošanas pārskata krātuve](inventory-aging-report-storage.md) versiju, īpaši, ja ir daudz krājumu un noliktavu, kas jāapstrādā.</span><span class="sxs-lookup"><span data-stu-id="236c7-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="236c7-109">Krājumu novecošanas pārskata krātuve saglabā katru izveidoto pārskatu, parāda rezultātus kā interaktīvu lapu un diagrammu un ļauj eksportēt visu saglabāto pārskatu.</span><span class="sxs-lookup"><span data-stu-id="236c7-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="236c7-110">Šajos piemēros izmantotie parauga dati</span><span class="sxs-lookup"><span data-stu-id="236c7-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="236c7-111">Šīs tēmas piemēri ir balstīti uz parauga krājumu darbību datiem, kas aprakstīti šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="236c7-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="236c7-112">Noliktavas dimensiju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="236c7-112">Storage dimension setup</span></span>

<span data-ttu-id="236c7-113">Piemēra sistēmā ir ietverti šādi glabāšanas dimensiju iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="236c7-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="236c7-114">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="236c7-114">Name</span></span>      | <span data-ttu-id="236c7-115">Aktīva</span><span class="sxs-lookup"><span data-stu-id="236c7-115">Active</span></span> | <span data-ttu-id="236c7-116">Fizisks krājums</span><span class="sxs-lookup"><span data-stu-id="236c7-116">Physical inventory</span></span> | <span data-ttu-id="236c7-117">Finanšu krājumi</span><span class="sxs-lookup"><span data-stu-id="236c7-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="236c7-118">Vietne</span><span class="sxs-lookup"><span data-stu-id="236c7-118">Site</span></span>      | <span data-ttu-id="236c7-119">Jā</span><span class="sxs-lookup"><span data-stu-id="236c7-119">Yes</span></span>    | <span data-ttu-id="236c7-120">Jā</span><span class="sxs-lookup"><span data-stu-id="236c7-120">Yes</span></span>                | <span data-ttu-id="236c7-121">Jā</span><span class="sxs-lookup"><span data-stu-id="236c7-121">Yes</span></span>                 |
| <span data-ttu-id="236c7-122">Noliktava</span><span class="sxs-lookup"><span data-stu-id="236c7-122">Warehouse</span></span> | <span data-ttu-id="236c7-123">Jā</span><span class="sxs-lookup"><span data-stu-id="236c7-123">Yes</span></span>    | <span data-ttu-id="236c7-124">Jā</span><span class="sxs-lookup"><span data-stu-id="236c7-124">Yes</span></span>                | <span data-ttu-id="236c7-125">Nr.</span><span class="sxs-lookup"><span data-stu-id="236c7-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="236c7-126">Krājumu modelis</span><span class="sxs-lookup"><span data-stu-id="236c7-126">Inventory model</span></span>

<span data-ttu-id="236c7-127">Piemēra sistēmai izlaisto preču krājumu modelis ir *FIFO*, un **Izmaksu cenas** iestatījums krājumu modelim ir *Ietver fizisko vērtību*.</span><span class="sxs-lookup"><span data-stu-id="236c7-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="236c7-128">Krājumu transakcijas</span><span class="sxs-lookup"><span data-stu-id="236c7-128">Inventory transactions</span></span>

<span data-ttu-id="236c7-129">Piemēra sistēmā ir iekļautas šādas krājumu darbības izlaistam produktam ar krājuma numuru *1000*.</span><span class="sxs-lookup"><span data-stu-id="236c7-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="236c7-130">Atsauce</span><span class="sxs-lookup"><span data-stu-id="236c7-130">Reference</span></span>      | <span data-ttu-id="236c7-131">Vietne</span><span class="sxs-lookup"><span data-stu-id="236c7-131">Site</span></span> | <span data-ttu-id="236c7-132">Noliktava</span><span class="sxs-lookup"><span data-stu-id="236c7-132">Warehouse</span></span> | <span data-ttu-id="236c7-133">Pirkš.pas. ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="236c7-133">Receipt</span></span>   | <span data-ttu-id="236c7-134">Izsniegt</span><span class="sxs-lookup"><span data-stu-id="236c7-134">Issue</span></span> | <span data-ttu-id="236c7-135">Fiziskais datums</span><span class="sxs-lookup"><span data-stu-id="236c7-135">Physical date</span></span> | <span data-ttu-id="236c7-136">Finansiālais datums</span><span class="sxs-lookup"><span data-stu-id="236c7-136">Financial date</span></span> | <span data-ttu-id="236c7-137">Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-137">Quantity</span></span> | <span data-ttu-id="236c7-138">Izmaksu summa</span><span class="sxs-lookup"><span data-stu-id="236c7-138">Cost amount</span></span> | <span data-ttu-id="236c7-139">Fiziskā izmaksu summa</span><span class="sxs-lookup"><span data-stu-id="236c7-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="236c7-140">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="236c7-140">Purchase order</span></span> | <span data-ttu-id="236c7-141">1</span><span class="sxs-lookup"><span data-stu-id="236c7-141">1</span></span>    | <span data-ttu-id="236c7-142">11.</span><span class="sxs-lookup"><span data-stu-id="236c7-142">11</span></span>        | <span data-ttu-id="236c7-143">Nopirkts</span><span class="sxs-lookup"><span data-stu-id="236c7-143">Purchased</span></span> |       | <span data-ttu-id="236c7-144">15. marts</span><span class="sxs-lookup"><span data-stu-id="236c7-144">March 15</span></span>      | <span data-ttu-id="236c7-145">15. marts</span><span class="sxs-lookup"><span data-stu-id="236c7-145">March 15</span></span>       | <span data-ttu-id="236c7-146">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-146">10</span></span>       | <span data-ttu-id="236c7-147">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-147">1,000</span></span>       | <span data-ttu-id="236c7-148">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-148">1,000</span></span>                |
| <span data-ttu-id="236c7-149">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="236c7-149">Purchase order</span></span> | <span data-ttu-id="236c7-150">2</span><span class="sxs-lookup"><span data-stu-id="236c7-150">2</span></span>    | <span data-ttu-id="236c7-151">21</span><span class="sxs-lookup"><span data-stu-id="236c7-151">21</span></span>        | <span data-ttu-id="236c7-152">Nopirkts</span><span class="sxs-lookup"><span data-stu-id="236c7-152">Purchased</span></span> |       | <span data-ttu-id="236c7-153">15. marts</span><span class="sxs-lookup"><span data-stu-id="236c7-153">March 15</span></span>      | <span data-ttu-id="236c7-154">15. marts</span><span class="sxs-lookup"><span data-stu-id="236c7-154">March 15</span></span>       | <span data-ttu-id="236c7-155">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-155">10</span></span>       | <span data-ttu-id="236c7-156">2,000</span><span class="sxs-lookup"><span data-stu-id="236c7-156">2,000</span></span>       | <span data-ttu-id="236c7-157">2,000</span><span class="sxs-lookup"><span data-stu-id="236c7-157">2,000</span></span>                |
| <span data-ttu-id="236c7-158">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="236c7-158">Purchase order</span></span> | <span data-ttu-id="236c7-159">1</span><span class="sxs-lookup"><span data-stu-id="236c7-159">1</span></span>    | <span data-ttu-id="236c7-160">11.</span><span class="sxs-lookup"><span data-stu-id="236c7-160">11</span></span>        | <span data-ttu-id="236c7-161">Saņemts</span><span class="sxs-lookup"><span data-stu-id="236c7-161">Received</span></span>  |       | <span data-ttu-id="236c7-162">15. aprīlis</span><span class="sxs-lookup"><span data-stu-id="236c7-162">April 15</span></span>      |                | <span data-ttu-id="236c7-163">5</span><span class="sxs-lookup"><span data-stu-id="236c7-163">5</span></span>        |             | <span data-ttu-id="236c7-164">375</span><span class="sxs-lookup"><span data-stu-id="236c7-164">375</span></span>                  |
| <span data-ttu-id="236c7-165">Pārsūtīšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="236c7-165">Transfer order</span></span> | <span data-ttu-id="236c7-166">1</span><span class="sxs-lookup"><span data-stu-id="236c7-166">1</span></span>    | <span data-ttu-id="236c7-167">11.</span><span class="sxs-lookup"><span data-stu-id="236c7-167">11</span></span>        |           | <span data-ttu-id="236c7-168">Pārdots</span><span class="sxs-lookup"><span data-stu-id="236c7-168">Sold</span></span>  | <span data-ttu-id="236c7-169">2. maijs</span><span class="sxs-lookup"><span data-stu-id="236c7-169">May 2</span></span>         | <span data-ttu-id="236c7-170">2. maijs</span><span class="sxs-lookup"><span data-stu-id="236c7-170">May 2</span></span>          | <span data-ttu-id="236c7-171">-5</span><span class="sxs-lookup"><span data-stu-id="236c7-171">-5</span></span>       | <span data-ttu-id="236c7-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="236c7-172">-458.33</span></span>     | <span data-ttu-id="236c7-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="236c7-173">-458.33</span></span>              |
| <span data-ttu-id="236c7-174">Pārsūtīšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="236c7-174">Transfer order</span></span> | <span data-ttu-id="236c7-175">1</span><span class="sxs-lookup"><span data-stu-id="236c7-175">1</span></span>    | <span data-ttu-id="236c7-176">12.</span><span class="sxs-lookup"><span data-stu-id="236c7-176">12</span></span>        | <span data-ttu-id="236c7-177">Nopirkts</span><span class="sxs-lookup"><span data-stu-id="236c7-177">Purchased</span></span> |       | <span data-ttu-id="236c7-178">2. maijs</span><span class="sxs-lookup"><span data-stu-id="236c7-178">May 2</span></span>         | <span data-ttu-id="236c7-179">2. maijs</span><span class="sxs-lookup"><span data-stu-id="236c7-179">May 2</span></span>          | <span data-ttu-id="236c7-180">5</span><span class="sxs-lookup"><span data-stu-id="236c7-180">5</span></span>        | <span data-ttu-id="236c7-181">458.33</span><span class="sxs-lookup"><span data-stu-id="236c7-181">458.33</span></span>      | <span data-ttu-id="236c7-182">458.33</span><span class="sxs-lookup"><span data-stu-id="236c7-182">458.33</span></span>               |
| <span data-ttu-id="236c7-183">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="236c7-183">Sales order</span></span>    | <span data-ttu-id="236c7-184">1</span><span class="sxs-lookup"><span data-stu-id="236c7-184">1</span></span>    | <span data-ttu-id="236c7-185">12.</span><span class="sxs-lookup"><span data-stu-id="236c7-185">12</span></span>        |           | <span data-ttu-id="236c7-186">Pārdots</span><span class="sxs-lookup"><span data-stu-id="236c7-186">Sold</span></span>  | <span data-ttu-id="236c7-187">3. maijs</span><span class="sxs-lookup"><span data-stu-id="236c7-187">May 3</span></span>         | <span data-ttu-id="236c7-188">3. maijs</span><span class="sxs-lookup"><span data-stu-id="236c7-188">May 3</span></span>          | <span data-ttu-id="236c7-189">-1</span><span class="sxs-lookup"><span data-stu-id="236c7-189">-1</span></span>       | <span data-ttu-id="236c7-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="236c7-190">-91.67</span></span>      | <span data-ttu-id="236c7-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="236c7-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="236c7-192">Kā tiek aprēķināti katra perioda intervāla daudzumi un summas</span><span class="sxs-lookup"><span data-stu-id="236c7-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="236c7-193">Izmantojot datu paraugus, kas aprakstīti iepriekšējās sadaļās, varat palaist **Krājumu vecumstruktūras** pārskatu, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="236c7-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="236c7-194">**Datums:** *2020. gada 9. maijs*</span><span class="sxs-lookup"><span data-stu-id="236c7-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="236c7-195">**Vietne:** *Skatīt*</span><span class="sxs-lookup"><span data-stu-id="236c7-195">**Site:** *View*</span></span>
- <span data-ttu-id="236c7-196">**Noliktava:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="236c7-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="236c7-197">**Krājuma numurs:** *Kopā*</span><span class="sxs-lookup"><span data-stu-id="236c7-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="236c7-198">**vecumstruktūras periods:** Iestatiet šo lauku, lai ģenerētu mēneša intervālus.</span><span class="sxs-lookup"><span data-stu-id="236c7-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="236c7-199">Šādā gadījumā ģenerētā pārskata saturs būs līdzīgs šim piemēram.</span><span class="sxs-lookup"><span data-stu-id="236c7-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="236c7-200">Krājums</span><span class="sxs-lookup"><span data-stu-id="236c7-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-201">Vietne</span><span class="sxs-lookup"><span data-stu-id="236c7-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-202">Rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-203">Rīcībā esošā vērtība</span><span class="sxs-lookup"><span data-stu-id="236c7-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-204">Krājumu vērtības daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-205">Krājumu vērtība</span><span class="sxs-lookup"><span data-stu-id="236c7-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-206">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="236c7-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-207">8/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-208">30/04/2020 - 1/04/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-209">31/03/2020 - 1/03/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="236c7-210">P1: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-211">P1: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="236c7-212">P2: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-213">P2: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="236c7-214">P3: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-215">P3: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="236c7-216">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-216">1000</span></span></td>
    <td><span data-ttu-id="236c7-217">1</span><span class="sxs-lookup"><span data-stu-id="236c7-217">1</span></span></td>
    <td><span data-ttu-id="236c7-218">14.</span><span class="sxs-lookup"><span data-stu-id="236c7-218">14</span></span></td>
    <td><span data-ttu-id="236c7-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="236c7-219">1,283.33</span></span></td>
    <td><span data-ttu-id="236c7-220">14.</span><span class="sxs-lookup"><span data-stu-id="236c7-220">14</span></span></td>
    <td><span data-ttu-id="236c7-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="236c7-221">1,283.33</span></span></td>
    <td><span data-ttu-id="236c7-222">91.67</span><span class="sxs-lookup"><span data-stu-id="236c7-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-223">5.00</span><span class="sxs-lookup"><span data-stu-id="236c7-223">5.00</span></span></td>
    <td><span data-ttu-id="236c7-224">458.33</span><span class="sxs-lookup"><span data-stu-id="236c7-224">458.33</span></span></td>
    <td><span data-ttu-id="236c7-225">9.00</span><span class="sxs-lookup"><span data-stu-id="236c7-225">9.00</span></span></td>
    <td><span data-ttu-id="236c7-226">825.00</span><span class="sxs-lookup"><span data-stu-id="236c7-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="236c7-227">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-227">1000</span></span></td>
    <td><span data-ttu-id="236c7-228">2</span><span class="sxs-lookup"><span data-stu-id="236c7-228">2</span></span></td>
    <td><span data-ttu-id="236c7-229">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-229">10</span></span></td>
    <td><span data-ttu-id="236c7-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-230">2,000.00</span></span></td>
    <td><span data-ttu-id="236c7-231">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-231">10</span></span></td>
    <td><span data-ttu-id="236c7-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-232">2,000.00</span></span></td>
    <td><span data-ttu-id="236c7-233">200.00</span><span class="sxs-lookup"><span data-stu-id="236c7-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-234">10,00</span><span class="sxs-lookup"><span data-stu-id="236c7-234">10.00</span></span></td>
    <td><span data-ttu-id="236c7-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="236c7-236"><strong>1000 Kopsummas</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="236c7-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="236c7-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="236c7-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="236c7-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="236c7-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="236c7-243">Ievērojiet šajā piemēra pārskatā norādīto informāciju:</span><span class="sxs-lookup"><span data-stu-id="236c7-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="236c7-244">**Krājumu vērtības daudzums**, **Krājumu vērtība** un **Vidējās vienības izmaksu** vērtības, kas tiek rādītas pārskatā, ir finanšu krājumu dimensijas (šajā gadījumā **Vietnes**) vērtības.</span><span class="sxs-lookup"><span data-stu-id="236c7-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="236c7-245">Piemēram, 1. vietnei pārskats rāda sekojošo informāciju:</span><span class="sxs-lookup"><span data-stu-id="236c7-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="236c7-246">**Krājumu vērtības daudzuma** vērtība ir *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="236c7-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="236c7-247">**Krājumu vērtības** vērtība ir *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="236c7-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="236c7-248">**Vidējā vienības izmaksu** vērtība ir *91,67*.</span><span class="sxs-lookup"><span data-stu-id="236c7-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="236c7-249">**Rīcībā esošā vērtības** vērtība un **Summas** vērtība katrā perioda intervālā tiek aprēķināta, izmantojot **Vidējo vienības izmaksu** vērtību.</span><span class="sxs-lookup"><span data-stu-id="236c7-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="236c7-250">Pārskats nosaka rīcībā esošo daudzumu katram perioda intervālam, apkopojot visu saņemto krājumu daudzumu katram periodam.</span><span class="sxs-lookup"><span data-stu-id="236c7-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="236c7-251">Pēc tam tas piemēro principu “pirmais iekšā, pirmais ārā” (FIFO), lai atskaitītu kopējo izdoto daudzumu neatkarīgi no krājuma modeļa, kuru izmanto preces.</span><span class="sxs-lookup"><span data-stu-id="236c7-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="236c7-252">Palaižot vienu un to pašu pārskatu, bet šoreiz iestatot gan **Vietnes**, gan **Noliktavas** laukus uz *Skatīt*, jaunais pārskats būs līdzīgs šim piemēram.</span><span class="sxs-lookup"><span data-stu-id="236c7-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="236c7-253">Krājums</span><span class="sxs-lookup"><span data-stu-id="236c7-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-254">Vietne</span><span class="sxs-lookup"><span data-stu-id="236c7-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-255">Noliktava</span><span class="sxs-lookup"><span data-stu-id="236c7-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-256">Rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-257">Rīcībā esošā vērtība</span><span class="sxs-lookup"><span data-stu-id="236c7-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-258">Krājumu vērtības daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-259">Krājumu vērtība</span><span class="sxs-lookup"><span data-stu-id="236c7-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-260">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="236c7-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-261">8/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-262">30/04/2020 - 1/04/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-263">31/03/2020 - 1/03/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="236c7-264">P1: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-265">P1: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="236c7-266">P2: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-267">P2: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="236c7-268">P3: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-269">P3: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="236c7-270">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-270">1000</span></span></td>
    <td><span data-ttu-id="236c7-271">1</span><span class="sxs-lookup"><span data-stu-id="236c7-271">1</span></span></td>
    <td><span data-ttu-id="236c7-272">11.</span><span class="sxs-lookup"><span data-stu-id="236c7-272">11</span></span></td>
    <td><span data-ttu-id="236c7-273">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-273">10</span></span></td>
    <td><span data-ttu-id="236c7-274">916.67</span><span class="sxs-lookup"><span data-stu-id="236c7-274">916.67</span></span></td>
    <td><span data-ttu-id="236c7-275">14.</span><span class="sxs-lookup"><span data-stu-id="236c7-275">14</span></span></td>
    <td><span data-ttu-id="236c7-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="236c7-276">1,283.33</span></span></td>
    <td><span data-ttu-id="236c7-277">91.67</span><span class="sxs-lookup"><span data-stu-id="236c7-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-278">5.00</span><span class="sxs-lookup"><span data-stu-id="236c7-278">5.00</span></span></td>
    <td><span data-ttu-id="236c7-279">458.33</span><span class="sxs-lookup"><span data-stu-id="236c7-279">458.33</span></span></td>
    <td><span data-ttu-id="236c7-280">5.00</span><span class="sxs-lookup"><span data-stu-id="236c7-280">5.00</span></span></td>
    <td><span data-ttu-id="236c7-281">458.33</span><span class="sxs-lookup"><span data-stu-id="236c7-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="236c7-282">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-282">1000</span></span></td>
    <td><span data-ttu-id="236c7-283">1</span><span class="sxs-lookup"><span data-stu-id="236c7-283">1</span></span></td>
    <td><span data-ttu-id="236c7-284">12.</span><span class="sxs-lookup"><span data-stu-id="236c7-284">12</span></span></td>
    <td><span data-ttu-id="236c7-285">4.</span><span class="sxs-lookup"><span data-stu-id="236c7-285">4</span></span></td>
    <td><span data-ttu-id="236c7-286">366.67</span><span class="sxs-lookup"><span data-stu-id="236c7-286">366.67</span></span></td>
    <td><span data-ttu-id="236c7-287">14.</span><span class="sxs-lookup"><span data-stu-id="236c7-287">14</span></span></td>
    <td><span data-ttu-id="236c7-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="236c7-288">1,283.33</span></span></td>
    <td><span data-ttu-id="236c7-289">91.67</span><span class="sxs-lookup"><span data-stu-id="236c7-289">91.67</span></span></td>
    <td><span data-ttu-id="236c7-290">4.00</span><span class="sxs-lookup"><span data-stu-id="236c7-290">4.00</span></span></td>
    <td><span data-ttu-id="236c7-291">366.67</span><span class="sxs-lookup"><span data-stu-id="236c7-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="236c7-292">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-292">1000</span></span></td>
    <td><span data-ttu-id="236c7-293">2</span><span class="sxs-lookup"><span data-stu-id="236c7-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="236c7-294">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-294">10</span></span></td>
    <td><span data-ttu-id="236c7-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-295">2,000.00</span></span></td>
    <td><span data-ttu-id="236c7-296">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-296">10</span></span></td>
    <td><span data-ttu-id="236c7-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-297">2,000.00</span></span></td>
    <td><span data-ttu-id="236c7-298">200.00</span><span class="sxs-lookup"><span data-stu-id="236c7-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-299">10,00</span><span class="sxs-lookup"><span data-stu-id="236c7-299">10.00</span></span></td>
    <td><span data-ttu-id="236c7-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="236c7-301"><strong>1000 Kopsummas</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="236c7-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="236c7-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="236c7-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="236c7-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="236c7-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="236c7-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="236c7-310">Šoreiz 1. vietne ir sadalīta divās rindās — viena 11. noliktavai un otra 12. noliktavai.</span><span class="sxs-lookup"><span data-stu-id="236c7-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="236c7-311">Tomēr **Krājumu vērtības daudzums**, **Krājumu vērtība** un **Vidējās vienības izmaksu** vērtības ir vienādas, jo **Noliktava** nav finanšu krājumu dimensija.</span><span class="sxs-lookup"><span data-stu-id="236c7-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="236c7-312">Turklāt ņemiet vērā, ka 1. vietnes daudzuma sadale atšķiras.</span><span class="sxs-lookup"><span data-stu-id="236c7-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="236c7-313">Pirmajā jūsu veiktajā pārskatā sistēma ignorēja pārsūtīšanas pasūtījumu, kas notika vienā un tajā pašā vietā, un atskaitīja pārdošanas rēķina daudzumu no **31/03/2020-1/03/2020** perioda kopuma 1. vietnē.</span><span class="sxs-lookup"><span data-stu-id="236c7-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="236c7-314">Tomēr jaunajā pārskatā sistēma atņem pārdošanas rēķina daudzumu no **8/05/2020-1/05/2020** perioda intervāla 12. noliktavā.</span><span class="sxs-lookup"><span data-stu-id="236c7-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="236c7-315">Krājumu slēgšanas sekas</span><span class="sxs-lookup"><span data-stu-id="236c7-315">Effects of inventory closing</span></span>

<span data-ttu-id="236c7-316">Ja palaižat krājumu slēgšanu maijam un pēc tam vēlreiz palaižat iepriekšējo pārskatu, bet, iestatāt **Datuma** lauku uz *2020. gada 31. maiju*, jūs ievērosit šādus rezultātus:</span><span class="sxs-lookup"><span data-stu-id="236c7-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="236c7-317">**Krājumu vērtības** un **Vidējās vienības izmaksu** vērtības tiek atjauninātas.</span><span class="sxs-lookup"><span data-stu-id="236c7-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="236c7-318">**Rīcībā esošā vērtības** vērtība un visas **Summas** vērtības katrā perioda intervālā tiek attiecīgi atjauninātas.</span><span class="sxs-lookup"><span data-stu-id="236c7-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="236c7-319">Jaunais pārskats izskatīsies līdzīgi kā tālāk sniegtais piemērs.</span><span class="sxs-lookup"><span data-stu-id="236c7-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="236c7-320">Krājums</span><span class="sxs-lookup"><span data-stu-id="236c7-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-321">Vietne</span><span class="sxs-lookup"><span data-stu-id="236c7-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-322">Noliktava</span><span class="sxs-lookup"><span data-stu-id="236c7-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-323">Rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-324">Rīcībā esošā vērtība</span><span class="sxs-lookup"><span data-stu-id="236c7-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-325">Krājumu vērtības daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-326">Krājumu vērtība</span><span class="sxs-lookup"><span data-stu-id="236c7-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="236c7-327">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="236c7-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-328">31/05/2020 - 1/05/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-329">30/04/2020 - 1/04/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="236c7-330">31/03/2020 - 1/03/2020</span><span class="sxs-lookup"><span data-stu-id="236c7-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="236c7-331">P1: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-332">P1: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="236c7-333">P2: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-334">P2: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="236c7-335">P3: Daudzums</span><span class="sxs-lookup"><span data-stu-id="236c7-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="236c7-336">P3: Summa</span><span class="sxs-lookup"><span data-stu-id="236c7-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="236c7-337">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-337">1000</span></span></td>
    <td><span data-ttu-id="236c7-338">1</span><span class="sxs-lookup"><span data-stu-id="236c7-338">1</span></span></td>
    <td><span data-ttu-id="236c7-339">11.</span><span class="sxs-lookup"><span data-stu-id="236c7-339">11</span></span></td>
    <td><span data-ttu-id="236c7-340">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-340">10</span></span></td>
    <td><span data-ttu-id="236c7-341">910.70</span><span class="sxs-lookup"><span data-stu-id="236c7-341">910.70</span></span></td>
    <td><span data-ttu-id="236c7-342">14.</span><span class="sxs-lookup"><span data-stu-id="236c7-342">14</span></span></td>
    <td><span data-ttu-id="236c7-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="236c7-343">1,275.00</span></span></td>
    <td><span data-ttu-id="236c7-344">91.07</span><span class="sxs-lookup"><span data-stu-id="236c7-344">91.07</span></span></td>
    <td><span data-ttu-id="236c7-345">0.00</span><span class="sxs-lookup"><span data-stu-id="236c7-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="236c7-346">5.00</span><span class="sxs-lookup"><span data-stu-id="236c7-346">5.00</span></span></td>
    <td><span data-ttu-id="236c7-347">455.36</span><span class="sxs-lookup"><span data-stu-id="236c7-347">455.36</span></span></td>
    <td><span data-ttu-id="236c7-348">5.00</span><span class="sxs-lookup"><span data-stu-id="236c7-348">5.00</span></span></td>
    <td><span data-ttu-id="236c7-349">455.36</span><span class="sxs-lookup"><span data-stu-id="236c7-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="236c7-350">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-350">1000</span></span></td>
    <td><span data-ttu-id="236c7-351">1</span><span class="sxs-lookup"><span data-stu-id="236c7-351">1</span></span></td>
    <td><span data-ttu-id="236c7-352">12.</span><span class="sxs-lookup"><span data-stu-id="236c7-352">12</span></span></td>
    <td><span data-ttu-id="236c7-353">4.</span><span class="sxs-lookup"><span data-stu-id="236c7-353">4</span></span></td>
    <td><span data-ttu-id="236c7-354">364.29</span><span class="sxs-lookup"><span data-stu-id="236c7-354">364.29</span></span></td>
    <td><span data-ttu-id="236c7-355">14.</span><span class="sxs-lookup"><span data-stu-id="236c7-355">14</span></span></td>
    <td><span data-ttu-id="236c7-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="236c7-356">1,275.00</span></span></td>
    <td><span data-ttu-id="236c7-357">91.07</span><span class="sxs-lookup"><span data-stu-id="236c7-357">91.07</span></span></td>
    <td><span data-ttu-id="236c7-358">4.00</span><span class="sxs-lookup"><span data-stu-id="236c7-358">4.00</span></span></td>
    <td><span data-ttu-id="236c7-359">364.29</span><span class="sxs-lookup"><span data-stu-id="236c7-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="236c7-360">1000</span><span class="sxs-lookup"><span data-stu-id="236c7-360">1000</span></span></td>
    <td><span data-ttu-id="236c7-361">2</span><span class="sxs-lookup"><span data-stu-id="236c7-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="236c7-362">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-362">10</span></span></td>
    <td><span data-ttu-id="236c7-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-363">2,000.00</span></span></td>
    <td><span data-ttu-id="236c7-364">10.</span><span class="sxs-lookup"><span data-stu-id="236c7-364">10</span></span></td>
    <td><span data-ttu-id="236c7-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-365">2,000.00</span></span></td>
    <td><span data-ttu-id="236c7-366">200.00</span><span class="sxs-lookup"><span data-stu-id="236c7-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-367">10,00</span><span class="sxs-lookup"><span data-stu-id="236c7-367">10.00</span></span></td>
    <td><span data-ttu-id="236c7-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="236c7-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="236c7-369"><strong>1000 Kopsummas</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="236c7-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="236c7-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="236c7-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="236c7-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="236c7-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="236c7-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="236c7-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="236c7-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
