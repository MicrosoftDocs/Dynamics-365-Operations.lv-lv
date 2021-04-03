---
title: Krājumu objekta vērtības
description: Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: f14248ffa8f9f5a460b090ca5754442cd50bf45a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263546"
---
# <a name="inventory-object-values"></a><span data-ttu-id="1556c-103">Krājumu objekta vērtības</span><span class="sxs-lookup"><span data-stu-id="1556c-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1556c-104">Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="1556c-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="1556c-105">Jaunā funkcija, kuras nosaukums ir **fiziskais daudzums** ļauj jums apskatīt noteikta krājuma objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="1556c-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="1556c-106">Izmaksu objekts norāda elementa līmeni, kurā tiek veikta krājumu uzskaite.</span><span class="sxs-lookup"><span data-stu-id="1556c-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="1556c-107">Plašāku informāciju par izmaksu objektiem skatiet sadaļā [Izmaksu objekti](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="1556c-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="1556c-108">Lai skatītu noteikta krājumu objekta vērtības, lapā **Izmaksu objekts** noklikšķiniet uz vienuma **Fiziskais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="1556c-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="1556c-109">Krājumu objekta vērtība tiek aprēķināta tālāk norādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="1556c-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="1556c-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span><span class="sxs-lookup"><span data-stu-id="1556c-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="1556c-111">Nākamajā piemērā ir parādīts, kā tiek aprēķinātas krājumu objekta un izmaksu objekta vērtības.</span><span class="sxs-lookup"><span data-stu-id="1556c-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="1556c-112">Krājumam A ir reģistrēti divi preču saņemšanas notikumi:</span><span class="sxs-lookup"><span data-stu-id="1556c-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="1556c-113">1. preces saņemšana: daudzums = 100 gab., summa = $ 1000,00, vieta = 1, noliktava = 11, partijas Nr.</span><span class="sxs-lookup"><span data-stu-id="1556c-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="1556c-114">= B1</span><span class="sxs-lookup"><span data-stu-id="1556c-114">= B1</span></span>
-   <span data-ttu-id="1556c-115">2. preces saņemšana: daudzums = 50 gab., summa = $ 800,00, vieta = 1, noliktava = 11, partijas Nr.</span><span class="sxs-lookup"><span data-stu-id="1556c-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="1556c-116">= B2</span><span class="sxs-lookup"><span data-stu-id="1556c-116">= B2</span></span>

<span data-ttu-id="1556c-117">Šajā tabulā ir parādīts aprēķinu rezultāts izmaksu objektam.</span><span class="sxs-lookup"><span data-stu-id="1556c-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="1556c-118">Rezultātu var skatīt lapā **Izmaksu objekts**.</span><span class="sxs-lookup"><span data-stu-id="1556c-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="1556c-119">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="1556c-119">Object type</span></span></th>
<th><span data-ttu-id="1556c-120">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="1556c-120">Item number</span></span></th>
<th><span data-ttu-id="1556c-121">Vieta</span><span class="sxs-lookup"><span data-stu-id="1556c-121">Site</span></span></th>
<th><span data-ttu-id="1556c-122">Daudzums</span><span class="sxs-lookup"><span data-stu-id="1556c-122">Quantity</span></span></th>
<th><span data-ttu-id="1556c-123">Krājumu uzskaites vienība</span><span class="sxs-lookup"><span data-stu-id="1556c-123">Inventory unit</span></span></th>
<th><span data-ttu-id="1556c-124">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1556c-124">Value</span></span></th>
<th><span data-ttu-id="1556c-125">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="1556c-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1556c-126">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="1556c-126">Cost object</span></span></td>
<td><span data-ttu-id="1556c-127">A</span><span class="sxs-lookup"><span data-stu-id="1556c-127">A</span></span></td>
<td><span data-ttu-id="1556c-128">1</span><span class="sxs-lookup"><span data-stu-id="1556c-128">1</span></span></td>
<td><span data-ttu-id="1556c-129">150</span><span class="sxs-lookup"><span data-stu-id="1556c-129">150</span></span></td>
<td><span data-ttu-id="1556c-130">Gab.</span><span class="sxs-lookup"><span data-stu-id="1556c-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="1556c-131">$ 1800,00</span><span class="sxs-lookup"><span data-stu-id="1556c-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="1556c-132">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="1556c-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1556c-133">Šajā tabulā ir parādīts aprēķinu rezultāts krājumu objektam.</span><span class="sxs-lookup"><span data-stu-id="1556c-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="1556c-134">Rezultātu var skatīt noklikšķinot uz **Fiziskais daudzums** lapā **Izmaksu objekts**.</span><span class="sxs-lookup"><span data-stu-id="1556c-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="1556c-135">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="1556c-135">Object type</span></span></th>
<th><span data-ttu-id="1556c-136">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="1556c-136">Item number</span></span></th>
<th><span data-ttu-id="1556c-137">Vieta</span><span class="sxs-lookup"><span data-stu-id="1556c-137">Site</span></span></th>
<th><span data-ttu-id="1556c-138">Noliktava</span><span class="sxs-lookup"><span data-stu-id="1556c-138">Warehouse</span></span></th>
<th><span data-ttu-id="1556c-139">Paketes Nr.</span><span class="sxs-lookup"><span data-stu-id="1556c-139">Batch No.</span></span></th>
<th><span data-ttu-id="1556c-140">Daudzums</span><span class="sxs-lookup"><span data-stu-id="1556c-140">Quantity</span></span></th>
<th><span data-ttu-id="1556c-141">Krājumu uzskaites vienība</span><span class="sxs-lookup"><span data-stu-id="1556c-141">Inventory unit</span></span></th>
<th><span data-ttu-id="1556c-142">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1556c-142">Value</span></span></th>
<th><span data-ttu-id="1556c-143">Vidējās vienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="1556c-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1556c-144">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="1556c-144">Inventory object</span></span></td>
<td><span data-ttu-id="1556c-145">A</span><span class="sxs-lookup"><span data-stu-id="1556c-145">A</span></span></td>
<td><span data-ttu-id="1556c-146">1</span><span class="sxs-lookup"><span data-stu-id="1556c-146">1</span></span></td>
<td><span data-ttu-id="1556c-147">11.</span><span class="sxs-lookup"><span data-stu-id="1556c-147">11</span></span></td>
<td><span data-ttu-id="1556c-148">B1</span><span class="sxs-lookup"><span data-stu-id="1556c-148">B1</span></span></td>
<td><span data-ttu-id="1556c-149">100</span><span class="sxs-lookup"><span data-stu-id="1556c-149">100</span></span></td>
<td><span data-ttu-id="1556c-150">Gab.</span><span class="sxs-lookup"><span data-stu-id="1556c-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="1556c-151">$ 1200,00</span><span class="sxs-lookup"><span data-stu-id="1556c-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="1556c-152">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="1556c-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1556c-153">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="1556c-153">Inventory object</span></span></td>
<td><span data-ttu-id="1556c-154">A</span><span class="sxs-lookup"><span data-stu-id="1556c-154">A</span></span></td>
<td><span data-ttu-id="1556c-155">1</span><span class="sxs-lookup"><span data-stu-id="1556c-155">1</span></span></td>
<td><span data-ttu-id="1556c-156">11</span><span class="sxs-lookup"><span data-stu-id="1556c-156">11</span></span></td>
<td><span data-ttu-id="1556c-157">B2</span><span class="sxs-lookup"><span data-stu-id="1556c-157">B2</span></span></td>
<td><span data-ttu-id="1556c-158">50</span><span class="sxs-lookup"><span data-stu-id="1556c-158">50</span></span></td>
<td><span data-ttu-id="1556c-159">Gab.</span><span class="sxs-lookup"><span data-stu-id="1556c-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="1556c-160">$ 600,00</span><span class="sxs-lookup"><span data-stu-id="1556c-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="1556c-161">$ 12,00</span><span class="sxs-lookup"><span data-stu-id="1556c-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="1556c-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1556c-162">Additional resources</span></span>
--------

[<span data-ttu-id="1556c-163">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="1556c-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="1556c-164">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="1556c-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="1556c-165">Jaunumi un izmaiņas</span><span class="sxs-lookup"><span data-stu-id="1556c-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]