---
title: Krājumu objekta vērtības
description: Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52f39c18888b94b533743f546554d5cd1b2d56df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832254"
---
# <a name="inventory-object-values"></a><span data-ttu-id="a0135-103">Krājumu objekta vērtības</span><span class="sxs-lookup"><span data-stu-id="a0135-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0135-104">Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="a0135-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="a0135-105">Jaunā funkcija, kuras nosaukums ir **fiziskais daudzums** ļauj jums apskatīt noteikta krājuma objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="a0135-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="a0135-106">Izmaksu objekts norāda elementa līmeni, kurā tiek veikta krājumu uzskaite.</span><span class="sxs-lookup"><span data-stu-id="a0135-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="a0135-107">Plašāku informāciju par izmaksu objektiem skatiet sadaļā [Izmaksu objekti](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="a0135-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="a0135-108">Lai skatītu noteikta krājumu objekta vērtības, lapā **Izmaksu objekts** noklikšķiniet uz vienuma **Fiziskais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="a0135-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="a0135-109">Krājumu objekta vērtība tiek aprēķināta tālāk norādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="a0135-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="a0135-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span><span class="sxs-lookup"><span data-stu-id="a0135-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="a0135-111">Nākamajā piemērā ir parādīts, kā tiek aprēķinātas krājumu objekta un izmaksu objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="a0135-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="a0135-112">Krājumam A ir reģistrēti divi preču saņemšanas notikumi:</span><span class="sxs-lookup"><span data-stu-id="a0135-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="a0135-113">1. preces saņemšana: daudzums = 100 gab., summa = $ 1000,00, vieta = 1, noliktava = 11, partijas Nr.</span><span class="sxs-lookup"><span data-stu-id="a0135-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="a0135-114">= B1</span><span class="sxs-lookup"><span data-stu-id="a0135-114">= B1</span></span>
-   <span data-ttu-id="a0135-115">2. preces saņemšana: daudzums = 50 gab., summa = $ 800,00, vieta = 1, noliktava = 11, partijas Nr.</span><span class="sxs-lookup"><span data-stu-id="a0135-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="a0135-116">= B2</span><span class="sxs-lookup"><span data-stu-id="a0135-116">= B2</span></span>

<span data-ttu-id="a0135-117">Šajā tabulā ir parādīts aprēķinu rezultāts izmaksu objektam.</span><span class="sxs-lookup"><span data-stu-id="a0135-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="a0135-118">Rezultātu var skatīt lapā **Izmaksu objekts**.</span><span class="sxs-lookup"><span data-stu-id="a0135-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="a0135-119">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="a0135-119">Object type</span></span></th>
<th><span data-ttu-id="a0135-120">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="a0135-120">Item number</span></span></th>
<th><span data-ttu-id="a0135-121">Vieta</span><span class="sxs-lookup"><span data-stu-id="a0135-121">Site</span></span></th>
<th><span data-ttu-id="a0135-122">Daudzums</span><span class="sxs-lookup"><span data-stu-id="a0135-122">Quantity</span></span></th>
<th><span data-ttu-id="a0135-123">Krājumu uzskaites vienība</span><span class="sxs-lookup"><span data-stu-id="a0135-123">Inventory unit</span></span></th>
<th><span data-ttu-id="a0135-124">Vērtība</span><span class="sxs-lookup"><span data-stu-id="a0135-124">Value</span></span></th>
<th><span data-ttu-id="a0135-125">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="a0135-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0135-126">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="a0135-126">Cost object</span></span></td>
<td><span data-ttu-id="a0135-127">A</span><span class="sxs-lookup"><span data-stu-id="a0135-127">A</span></span></td>
<td><span data-ttu-id="a0135-128">1</span><span class="sxs-lookup"><span data-stu-id="a0135-128">1</span></span></td>
<td><span data-ttu-id="a0135-129">150</span><span class="sxs-lookup"><span data-stu-id="a0135-129">150</span></span></td>
<td><span data-ttu-id="a0135-130">Gab.</span><span class="sxs-lookup"><span data-stu-id="a0135-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="a0135-131">$ 1800,00</span><span class="sxs-lookup"><span data-stu-id="a0135-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="a0135-132">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="a0135-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0135-133">Šajā tabulā ir parādīts aprēķinu rezultāts krājumu objektam.</span><span class="sxs-lookup"><span data-stu-id="a0135-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="a0135-134">Rezultātu var skatīt noklikšķinot uz **Fiziskais daudzums** lapā **Izmaksu objekts**.</span><span class="sxs-lookup"><span data-stu-id="a0135-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="a0135-135">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="a0135-135">Object type</span></span></th>
<th><span data-ttu-id="a0135-136">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="a0135-136">Item number</span></span></th>
<th><span data-ttu-id="a0135-137">Vieta</span><span class="sxs-lookup"><span data-stu-id="a0135-137">Site</span></span></th>
<th><span data-ttu-id="a0135-138">Noliktava</span><span class="sxs-lookup"><span data-stu-id="a0135-138">Warehouse</span></span></th>
<th><span data-ttu-id="a0135-139">Paketes Nr.</span><span class="sxs-lookup"><span data-stu-id="a0135-139">Batch No.</span></span></th>
<th><span data-ttu-id="a0135-140">Daudzums</span><span class="sxs-lookup"><span data-stu-id="a0135-140">Quantity</span></span></th>
<th><span data-ttu-id="a0135-141">Krājumu uzskaites vienība</span><span class="sxs-lookup"><span data-stu-id="a0135-141">Inventory unit</span></span></th>
<th><span data-ttu-id="a0135-142">Vērtība</span><span class="sxs-lookup"><span data-stu-id="a0135-142">Value</span></span></th>
<th><span data-ttu-id="a0135-143">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="a0135-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0135-144">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="a0135-144">Inventory object</span></span></td>
<td><span data-ttu-id="a0135-145">A</span><span class="sxs-lookup"><span data-stu-id="a0135-145">A</span></span></td>
<td><span data-ttu-id="a0135-146">1</span><span class="sxs-lookup"><span data-stu-id="a0135-146">1</span></span></td>
<td><span data-ttu-id="a0135-147">11.</span><span class="sxs-lookup"><span data-stu-id="a0135-147">11</span></span></td>
<td><span data-ttu-id="a0135-148">B1</span><span class="sxs-lookup"><span data-stu-id="a0135-148">B1</span></span></td>
<td><span data-ttu-id="a0135-149">100</span><span class="sxs-lookup"><span data-stu-id="a0135-149">100</span></span></td>
<td><span data-ttu-id="a0135-150">Gab.</span><span class="sxs-lookup"><span data-stu-id="a0135-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="a0135-151">$ 1200,00</span><span class="sxs-lookup"><span data-stu-id="a0135-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="a0135-152">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="a0135-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0135-153">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="a0135-153">Inventory object</span></span></td>
<td><span data-ttu-id="a0135-154">A</span><span class="sxs-lookup"><span data-stu-id="a0135-154">A</span></span></td>
<td><span data-ttu-id="a0135-155">1</span><span class="sxs-lookup"><span data-stu-id="a0135-155">1</span></span></td>
<td><span data-ttu-id="a0135-156">11</span><span class="sxs-lookup"><span data-stu-id="a0135-156">11</span></span></td>
<td><span data-ttu-id="a0135-157">B2</span><span class="sxs-lookup"><span data-stu-id="a0135-157">B2</span></span></td>
<td><span data-ttu-id="a0135-158">50</span><span class="sxs-lookup"><span data-stu-id="a0135-158">50</span></span></td>
<td><span data-ttu-id="a0135-159">Gab.</span><span class="sxs-lookup"><span data-stu-id="a0135-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="a0135-160">$ 600,00</span><span class="sxs-lookup"><span data-stu-id="a0135-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="a0135-161">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="a0135-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="a0135-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a0135-162">Additional resources</span></span>
--------

[<span data-ttu-id="a0135-163">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="a0135-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="a0135-164">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="a0135-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="a0135-165">Jaunumi un izmaiņas</span><span class="sxs-lookup"><span data-stu-id="a0135-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]