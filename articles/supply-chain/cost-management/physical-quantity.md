---
title: "Krājumu objekta vērtības"
description: "Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4aec6e70325c7e4d00e6070293a1ab0c719e420b
ms.contentlocale: lv-lv
ms.lasthandoff: 07/18/2017

---

# <a name="inventory-object-values"></a><span data-ttu-id="37af6-103">Krājumu objekta vērtības</span><span class="sxs-lookup"><span data-stu-id="37af6-103">Inventory object values</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="37af6-104">Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="37af6-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="37af6-105">Jaunā funkcija, kuras nosaukums ir **fiziskais daudzums** ļauj jums apskatīt noteikta krājuma objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="37af6-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="37af6-106">Izmaksu objekts norāda elementa līmeni, kurā tiek veikta krājumu uzskaite.</span><span class="sxs-lookup"><span data-stu-id="37af6-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="37af6-107">Plašāku informāciju par izmaksu objektiem skatiet sadaļā [Izmaksu objekti](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="37af6-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="37af6-108">Lai skatītu noteikta krājumu objekta vērtības, lapā **Izmaksu objekts** noklikšķiniet uz vienuma **Fiziskais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="37af6-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="37af6-109">Krājumu objekta vērtība tiek aprēķināta tālāk norādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="37af6-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="37af6-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span><span class="sxs-lookup"><span data-stu-id="37af6-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="37af6-111">Nākamajā piemērā ir parādīts, kā tiek aprēķinātas krājumu objekta un izmaksu objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="37af6-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="37af6-112">Krājumam A ir reģistrēti divi preču saņemšanas notikumi:</span><span class="sxs-lookup"><span data-stu-id="37af6-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="37af6-113">1. preces saņemšana: daudzums = 100 gab., summa = $ 1000,00, vieta = 1, noliktava = 11, partijas Nr.</span><span class="sxs-lookup"><span data-stu-id="37af6-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="37af6-114">= B1</span><span class="sxs-lookup"><span data-stu-id="37af6-114">= B1</span></span>
-   <span data-ttu-id="37af6-115">2. preces saņemšana: daudzums = 50 gab., summa = $ 800,00, vieta = 1, noliktava = 11, partijas Nr.</span><span class="sxs-lookup"><span data-stu-id="37af6-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="37af6-116">= B2</span><span class="sxs-lookup"><span data-stu-id="37af6-116">= B2</span></span>

<span data-ttu-id="37af6-117">Šajā tabulā ir parādīts aprēķinu rezultāts izmaksu objektam.</span><span class="sxs-lookup"><span data-stu-id="37af6-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="37af6-118">Rezultātu var skatīt lapā **Izmaksu objekts**.</span><span class="sxs-lookup"><span data-stu-id="37af6-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37af6-119">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="37af6-119">Object type</span></span></th>
<th><span data-ttu-id="37af6-120">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="37af6-120">Item number</span></span></th>
<th><span data-ttu-id="37af6-121">Vieta</span><span class="sxs-lookup"><span data-stu-id="37af6-121">Site</span></span></th>
<th><span data-ttu-id="37af6-122">Daudzums</span><span class="sxs-lookup"><span data-stu-id="37af6-122">Quantity</span></span></th>
<th><span data-ttu-id="37af6-123">Krājumu uzskaites vienība</span><span class="sxs-lookup"><span data-stu-id="37af6-123">Inventory unit</span></span></th>
<th><span data-ttu-id="37af6-124">Vērtība</span><span class="sxs-lookup"><span data-stu-id="37af6-124">Value</span></span></th>
<th><span data-ttu-id="37af6-125">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="37af6-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37af6-126">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="37af6-126">Cost object</span></span></td>
<td><span data-ttu-id="37af6-127">A</span><span class="sxs-lookup"><span data-stu-id="37af6-127">A</span></span></td>
<td><span data-ttu-id="37af6-128">1</span><span class="sxs-lookup"><span data-stu-id="37af6-128">1</span></span></td>
<td><span data-ttu-id="37af6-129">150</span><span class="sxs-lookup"><span data-stu-id="37af6-129">150</span></span></td>
<td><span data-ttu-id="37af6-130">Gab.</span><span class="sxs-lookup"><span data-stu-id="37af6-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="37af6-131">$ 1800,00</span><span class="sxs-lookup"><span data-stu-id="37af6-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="37af6-132">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="37af6-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="37af6-133">Šajā tabulā ir parādīts aprēķinu rezultāts krājumu objektam.</span><span class="sxs-lookup"><span data-stu-id="37af6-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="37af6-134">Rezultātu var skatīt noklikšķinot uz **Fiziskais daudzums** lapā **Izmaksu objekts**.</span><span class="sxs-lookup"><span data-stu-id="37af6-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37af6-135">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="37af6-135">Object type</span></span></th>
<th><span data-ttu-id="37af6-136">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="37af6-136">Item number</span></span></th>
<th><span data-ttu-id="37af6-137">Vieta</span><span class="sxs-lookup"><span data-stu-id="37af6-137">Site</span></span></th>
<th><span data-ttu-id="37af6-138">Noliktava</span><span class="sxs-lookup"><span data-stu-id="37af6-138">Warehouse</span></span></th>
<th><span data-ttu-id="37af6-139">Paketes Nr.</span><span class="sxs-lookup"><span data-stu-id="37af6-139">Batch No.</span></span></th>
<th><span data-ttu-id="37af6-140">Daudzums</span><span class="sxs-lookup"><span data-stu-id="37af6-140">Quantity</span></span></th>
<th><span data-ttu-id="37af6-141">Krājumu uzskaites vienība</span><span class="sxs-lookup"><span data-stu-id="37af6-141">Inventory unit</span></span></th>
<th><span data-ttu-id="37af6-142">Vērtība</span><span class="sxs-lookup"><span data-stu-id="37af6-142">Value</span></span></th>
<th><span data-ttu-id="37af6-143">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="37af6-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37af6-144">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="37af6-144">Inventory object</span></span></td>
<td><span data-ttu-id="37af6-145">A</span><span class="sxs-lookup"><span data-stu-id="37af6-145">A</span></span></td>
<td><span data-ttu-id="37af6-146">1</span><span class="sxs-lookup"><span data-stu-id="37af6-146">1</span></span></td>
<td><span data-ttu-id="37af6-147">11.</span><span class="sxs-lookup"><span data-stu-id="37af6-147">11</span></span></td>
<td><span data-ttu-id="37af6-148">B1</span><span class="sxs-lookup"><span data-stu-id="37af6-148">B1</span></span></td>
<td><span data-ttu-id="37af6-149">100</span><span class="sxs-lookup"><span data-stu-id="37af6-149">100</span></span></td>
<td><span data-ttu-id="37af6-150">Gab.</span><span class="sxs-lookup"><span data-stu-id="37af6-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="37af6-151">$ 1200,00</span><span class="sxs-lookup"><span data-stu-id="37af6-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="37af6-152">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="37af6-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37af6-153">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="37af6-153">Inventory object</span></span></td>
<td><span data-ttu-id="37af6-154">A</span><span class="sxs-lookup"><span data-stu-id="37af6-154">A</span></span></td>
<td><span data-ttu-id="37af6-155">1.</span><span class="sxs-lookup"><span data-stu-id="37af6-155">1</span></span></td>
<td><span data-ttu-id="37af6-156">11.</span><span class="sxs-lookup"><span data-stu-id="37af6-156">11</span></span></td>
<td><span data-ttu-id="37af6-157">B2</span><span class="sxs-lookup"><span data-stu-id="37af6-157">B2</span></span></td>
<td><span data-ttu-id="37af6-158">50</span><span class="sxs-lookup"><span data-stu-id="37af6-158">50</span></span></td>
<td><span data-ttu-id="37af6-159">Gab.</span><span class="sxs-lookup"><span data-stu-id="37af6-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="37af6-160">$ 600,00</span><span class="sxs-lookup"><span data-stu-id="37af6-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="37af6-161">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="37af6-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="37af6-162">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="37af6-162">See also</span></span>
--------

[<span data-ttu-id="37af6-163">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="37af6-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="37af6-164">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="37af6-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="37af6-165">Jaunumi un izmaiņas</span><span class="sxs-lookup"><span data-stu-id="37af6-165">What's new and changed</span></span>](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)




