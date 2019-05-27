---
title: Krājumu objekta vērtības
description: Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e92c7889b11208c4d2b48eb279a104a7c226f904
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547863"
---
# <a name="inventory-object-values"></a><span data-ttu-id="41bb0-103">Krājumu objekta vērtības</span><span class="sxs-lookup"><span data-stu-id="41bb0-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41bb0-104">Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="41bb0-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="41bb0-105">Jaunā funkcija, kuras nosaukums ir **fiziskais daudzums** ļauj jums apskatīt noteikta krājuma objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="41bb0-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="41bb0-106">Izmaksu objekts norāda elementa līmeni, kurā tiek veikta krājumu uzskaite.</span><span class="sxs-lookup"><span data-stu-id="41bb0-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="41bb0-107">Plašāku informāciju par izmaksu objektiem skatiet sadaļā [Izmaksu objekti](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="41bb0-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="41bb0-108">Lai skatītu noteikta krājumu objekta vērtības, lapā **Izmaksu objekts** noklikšķiniet uz vienuma **Fiziskais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="41bb0-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="41bb0-109">Krājumu objekta vērtība tiek aprēķināta tālāk norādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="41bb0-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="41bb0-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span><span class="sxs-lookup"><span data-stu-id="41bb0-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="41bb0-111">Nākamajā piemērā ir parādīts, kā tiek aprēķinātas krājumu objekta un izmaksu objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="41bb0-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="41bb0-112">Krājumam A ir reģistrēti divi preču saņemšanas notikumi:</span><span class="sxs-lookup"><span data-stu-id="41bb0-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="41bb0-113">1. preces saņemšana: daudzums = 100 gab., summa = $ 1000,00, vieta = 1, noliktava = 11, partijas Nr.</span><span class="sxs-lookup"><span data-stu-id="41bb0-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="41bb0-114">= B1</span><span class="sxs-lookup"><span data-stu-id="41bb0-114">= B1</span></span>
-   <span data-ttu-id="41bb0-115">2. preces saņemšana: daudzums = 50 gab., summa = $ 800,00, vieta = 1, noliktava = 11, partijas Nr.</span><span class="sxs-lookup"><span data-stu-id="41bb0-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="41bb0-116">= B2</span><span class="sxs-lookup"><span data-stu-id="41bb0-116">= B2</span></span>

<span data-ttu-id="41bb0-117">Šajā tabulā ir parādīts aprēķinu rezultāts izmaksu objektam.</span><span class="sxs-lookup"><span data-stu-id="41bb0-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="41bb0-118">Rezultātu var skatīt lapā **Izmaksu objekts**.</span><span class="sxs-lookup"><span data-stu-id="41bb0-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="41bb0-119">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="41bb0-119">Object type</span></span></th>
<th><span data-ttu-id="41bb0-120">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="41bb0-120">Item number</span></span></th>
<th><span data-ttu-id="41bb0-121">Vieta</span><span class="sxs-lookup"><span data-stu-id="41bb0-121">Site</span></span></th>
<th><span data-ttu-id="41bb0-122">Daudzums</span><span class="sxs-lookup"><span data-stu-id="41bb0-122">Quantity</span></span></th>
<th><span data-ttu-id="41bb0-123">Krājumu uzskaites vienība</span><span class="sxs-lookup"><span data-stu-id="41bb0-123">Inventory unit</span></span></th>
<th><span data-ttu-id="41bb0-124">Vērtība</span><span class="sxs-lookup"><span data-stu-id="41bb0-124">Value</span></span></th>
<th><span data-ttu-id="41bb0-125">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="41bb0-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41bb0-126">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="41bb0-126">Cost object</span></span></td>
<td><span data-ttu-id="41bb0-127">A</span><span class="sxs-lookup"><span data-stu-id="41bb0-127">A</span></span></td>
<td><span data-ttu-id="41bb0-128">1</span><span class="sxs-lookup"><span data-stu-id="41bb0-128">1</span></span></td>
<td><span data-ttu-id="41bb0-129">150</span><span class="sxs-lookup"><span data-stu-id="41bb0-129">150</span></span></td>
<td><span data-ttu-id="41bb0-130">Gab.</span><span class="sxs-lookup"><span data-stu-id="41bb0-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="41bb0-131">$ 1800,00</span><span class="sxs-lookup"><span data-stu-id="41bb0-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="41bb0-132">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="41bb0-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41bb0-133">Šajā tabulā ir parādīts aprēķinu rezultāts krājumu objektam.</span><span class="sxs-lookup"><span data-stu-id="41bb0-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="41bb0-134">Rezultātu var skatīt noklikšķinot uz **Fiziskais daudzums** lapā **Izmaksu objekts**.</span><span class="sxs-lookup"><span data-stu-id="41bb0-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="41bb0-135">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="41bb0-135">Object type</span></span></th>
<th><span data-ttu-id="41bb0-136">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="41bb0-136">Item number</span></span></th>
<th><span data-ttu-id="41bb0-137">Vieta</span><span class="sxs-lookup"><span data-stu-id="41bb0-137">Site</span></span></th>
<th><span data-ttu-id="41bb0-138">Noliktava</span><span class="sxs-lookup"><span data-stu-id="41bb0-138">Warehouse</span></span></th>
<th><span data-ttu-id="41bb0-139">Paketes Nr.</span><span class="sxs-lookup"><span data-stu-id="41bb0-139">Batch No.</span></span></th>
<th><span data-ttu-id="41bb0-140">Daudzums</span><span class="sxs-lookup"><span data-stu-id="41bb0-140">Quantity</span></span></th>
<th><span data-ttu-id="41bb0-141">Krājumu uzskaites vienība</span><span class="sxs-lookup"><span data-stu-id="41bb0-141">Inventory unit</span></span></th>
<th><span data-ttu-id="41bb0-142">Vērtība</span><span class="sxs-lookup"><span data-stu-id="41bb0-142">Value</span></span></th>
<th><span data-ttu-id="41bb0-143">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="41bb0-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41bb0-144">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="41bb0-144">Inventory object</span></span></td>
<td><span data-ttu-id="41bb0-145">A</span><span class="sxs-lookup"><span data-stu-id="41bb0-145">A</span></span></td>
<td><span data-ttu-id="41bb0-146">1</span><span class="sxs-lookup"><span data-stu-id="41bb0-146">1</span></span></td>
<td><span data-ttu-id="41bb0-147">11.</span><span class="sxs-lookup"><span data-stu-id="41bb0-147">11</span></span></td>
<td><span data-ttu-id="41bb0-148">B1</span><span class="sxs-lookup"><span data-stu-id="41bb0-148">B1</span></span></td>
<td><span data-ttu-id="41bb0-149">100</span><span class="sxs-lookup"><span data-stu-id="41bb0-149">100</span></span></td>
<td><span data-ttu-id="41bb0-150">Gab.</span><span class="sxs-lookup"><span data-stu-id="41bb0-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="41bb0-151">$ 1200,00</span><span class="sxs-lookup"><span data-stu-id="41bb0-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="41bb0-152">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="41bb0-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41bb0-153">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="41bb0-153">Inventory object</span></span></td>
<td><span data-ttu-id="41bb0-154">A</span><span class="sxs-lookup"><span data-stu-id="41bb0-154">A</span></span></td>
<td><span data-ttu-id="41bb0-155">1</span><span class="sxs-lookup"><span data-stu-id="41bb0-155">1</span></span></td>
<td><span data-ttu-id="41bb0-156">11</span><span class="sxs-lookup"><span data-stu-id="41bb0-156">11</span></span></td>
<td><span data-ttu-id="41bb0-157">B2</span><span class="sxs-lookup"><span data-stu-id="41bb0-157">B2</span></span></td>
<td><span data-ttu-id="41bb0-158">50</span><span class="sxs-lookup"><span data-stu-id="41bb0-158">50</span></span></td>
<td><span data-ttu-id="41bb0-159">Gab.</span><span class="sxs-lookup"><span data-stu-id="41bb0-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="41bb0-160">$ 600,00</span><span class="sxs-lookup"><span data-stu-id="41bb0-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="41bb0-161">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="41bb0-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="41bb0-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="41bb0-162">Additional resources</span></span>
--------

[<span data-ttu-id="41bb0-163">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="41bb0-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="41bb0-164">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="41bb0-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="41bb0-165">Jaunumi un izmaiņas</span><span class="sxs-lookup"><span data-stu-id="41bb0-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



