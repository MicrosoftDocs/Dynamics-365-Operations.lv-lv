---
title: Izmaksu objekti
description: "Šajā rakstā ir sniegta informācija par izmaksu objektiem un paskaidrots, kā tiek uzkrātas izmaksas un daudzumi. Izmaksu objekts ir elements, kam ir uzkrātas izmaksas un daudzumi. Izmaksu objekta elements var būt prece vai preces varianti, piemēram, stila un krāsas varianti."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1a1c964a890c0c59a01700a6987bfbdfe5a17ccb
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="cost-objects"></a><span data-ttu-id="f48bd-105">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="f48bd-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f48bd-106">Šajā rakstā ir sniegta informācija par izmaksu objektiem un paskaidrots, kā tiek uzkrātas izmaksas un daudzumi.</span><span class="sxs-lookup"><span data-stu-id="f48bd-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="f48bd-107">Izmaksu objekts ir elements, kam ir uzkrātas izmaksas un daudzumi.</span><span class="sxs-lookup"><span data-stu-id="f48bd-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="f48bd-108">Izmaksu objekta elements var būt prece vai preces varianti, piemēram, stila un krāsas varianti.</span><span class="sxs-lookup"><span data-stu-id="f48bd-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="f48bd-109">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="f48bd-109">Cost objects</span></span>

<span data-ttu-id="f48bd-110">Sarakstā **Izmaksu objekti** ir parādīts saraksts ar visiem izmaksu objektiem, kas ir reģistrēti precei.</span><span class="sxs-lookup"><span data-stu-id="f48bd-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="f48bd-111">Izmaksu objektus nosaka dati no šādiem avotiem:</span><span class="sxs-lookup"><span data-stu-id="f48bd-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="f48bd-112">Produkts</span><span class="sxs-lookup"><span data-stu-id="f48bd-112">Product</span></span>
-   <span data-ttu-id="f48bd-113">Preces dimensijas grupa</span><span class="sxs-lookup"><span data-stu-id="f48bd-113">Product dimension group</span></span>
-   <span data-ttu-id="f48bd-114">Noliktavas dimensiju grupa</span><span class="sxs-lookup"><span data-stu-id="f48bd-114">Storage dimension group</span></span>
-   <span data-ttu-id="f48bd-115">Izsekošanas dimensijas grupa</span><span class="sxs-lookup"><span data-stu-id="f48bd-115">Tracking dimension group</span></span>

<span data-ttu-id="f48bd-116">**Piezīme.** Izmaksu objekts norāda tikai tādu izmaksu elementu, kura tips ir **Tiešie materiāli**.</span><span class="sxs-lookup"><span data-stu-id="f48bd-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="f48bd-117">Izmaksu objekts atšķiras no krājumu objekta ar to, kā izmaksu objektu nosaka krājumu dimensijas, kas atlasītas finanšu krājumiem.</span><span class="sxs-lookup"><span data-stu-id="f48bd-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="f48bd-118">Piemēram, krājumam ir šāda konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="f48bd-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="f48bd-119">**Vieta:** Fiziskie krājumi = Jā, Finanšu krājumi = Jā</span><span class="sxs-lookup"><span data-stu-id="f48bd-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="f48bd-120">**Noliktava:** Fiziskie krājumi = Jā, Finanšu krājumi = Nē</span><span class="sxs-lookup"><span data-stu-id="f48bd-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="f48bd-121">**Partijas Nr.:** Fiziskie krājumi = Jā, Finanšu krājumi = Nē</span><span class="sxs-lookup"><span data-stu-id="f48bd-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="f48bd-122">Šajā tabulā ir parādīts, kas ir izmaksu objekts un kas ir krājumu objekts.</span><span class="sxs-lookup"><span data-stu-id="f48bd-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="f48bd-123">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="f48bd-123">Object type</span></span>      | <span data-ttu-id="f48bd-124">Krājuma kods</span><span class="sxs-lookup"><span data-stu-id="f48bd-124">Item number</span></span> | <span data-ttu-id="f48bd-125">Vieta</span><span class="sxs-lookup"><span data-stu-id="f48bd-125">Site</span></span> | <span data-ttu-id="f48bd-126">Noliktava</span><span class="sxs-lookup"><span data-stu-id="f48bd-126">Warehouse</span></span> | <span data-ttu-id="f48bd-127">Paketes Nr.</span><span class="sxs-lookup"><span data-stu-id="f48bd-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="f48bd-128">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="f48bd-128">Cost object</span></span>      | <span data-ttu-id="f48bd-129">x</span><span class="sxs-lookup"><span data-stu-id="f48bd-129">x</span></span>           | <span data-ttu-id="f48bd-130">x</span><span class="sxs-lookup"><span data-stu-id="f48bd-130">x</span></span>    |           |           |
| <span data-ttu-id="f48bd-131">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="f48bd-131">Inventory object</span></span> | <span data-ttu-id="f48bd-132">x</span><span class="sxs-lookup"><span data-stu-id="f48bd-132">x</span></span>           | <span data-ttu-id="f48bd-133">x</span><span class="sxs-lookup"><span data-stu-id="f48bd-133">x</span></span>    |  <span data-ttu-id="f48bd-134">x</span><span class="sxs-lookup"><span data-stu-id="f48bd-134">x</span></span>        | <span data-ttu-id="f48bd-135">x</span><span class="sxs-lookup"><span data-stu-id="f48bd-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="f48bd-136">Izmaksu un daudzumu uzkrāšana</span><span class="sxs-lookup"><span data-stu-id="f48bd-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="f48bd-137">Vērtība laukā **Vērtība** ir šādu vērtību summa:</span><span class="sxs-lookup"><span data-stu-id="f48bd-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="f48bd-138">Fiziskā izmaksu summa</span><span class="sxs-lookup"><span data-stu-id="f48bd-138">Physical cost amount</span></span>
    -   <span data-ttu-id="f48bd-139">Beigu izmaksu summa</span><span class="sxs-lookup"><span data-stu-id="f48bd-139">Financial cost amount</span></span>
    -   <span data-ttu-id="f48bd-140">Korekcijas</span><span class="sxs-lookup"><span data-stu-id="f48bd-140">Adjustments</span></span>
-   <span data-ttu-id="f48bd-141">Vērtība laukā **Daudzums** ir šādu vērtību summa:</span><span class="sxs-lookup"><span data-stu-id="f48bd-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="f48bd-142">Saņemts</span><span class="sxs-lookup"><span data-stu-id="f48bd-142">Received</span></span>
    -   <span data-ttu-id="f48bd-143">Atskaitīts</span><span class="sxs-lookup"><span data-stu-id="f48bd-143">Deducted</span></span>
    -   <span data-ttu-id="f48bd-144">Grāmatotais daudzums</span><span class="sxs-lookup"><span data-stu-id="f48bd-144">Posted quantity</span></span>
-   <span data-ttu-id="f48bd-145">Vērtība laukā **Vidējās vienības izmaksas** tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="f48bd-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="f48bd-146">Vērtība tiek aprēķināta, dalot vērtību laukā **Vērtība** ar vērtību laukā **Daudzums**.</span><span class="sxs-lookup"><span data-stu-id="f48bd-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="f48bd-147">**Piezīme.** Parametrs **Iekļaut fizisko vērtību** neietekmē iepriekšējos aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="f48bd-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="f48bd-148">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="f48bd-148">See also</span></span>
--------

[<span data-ttu-id="f48bd-149">Preces dimensiju grupa</span><span class="sxs-lookup"><span data-stu-id="f48bd-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="f48bd-150">Noliktavas dimensiju grupa</span><span class="sxs-lookup"><span data-stu-id="f48bd-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="f48bd-151">Izsekošanas dimensiju grupa</span><span class="sxs-lookup"><span data-stu-id="f48bd-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="f48bd-152">Jaunumi un izmaiņas</span><span class="sxs-lookup"><span data-stu-id="f48bd-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="f48bd-153">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="f48bd-153">Cost entries</span></span>](cost-entries.md)




