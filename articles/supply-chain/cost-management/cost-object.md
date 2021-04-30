---
title: Izmaksu objekti
description: Šajā rakstā ir sniegta informācija par izmaksu objektiem un paskaidrots, kā tiek uzkrātas izmaksas un daudzumi. Izmaksu objekts ir elements, kam ir uzkrātas izmaksas un daudzumi. Izmaksu objekta elements var būt prece vai preces varianti, piemēram, stila un krāsas varianti.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6829f24b8efa29b39f5ed742d8ca99e09bcef01
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910357"
---
# <a name="cost-objects"></a><span data-ttu-id="cf191-105">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="cf191-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf191-106">Šajā rakstā ir sniegta informācija par izmaksu objektiem un paskaidrots, kā tiek uzkrātas izmaksas un daudzumi.</span><span class="sxs-lookup"><span data-stu-id="cf191-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="cf191-107">Izmaksu objekts ir elements, kam ir uzkrātas izmaksas un daudzumi.</span><span class="sxs-lookup"><span data-stu-id="cf191-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="cf191-108">Izmaksu objekta elements var būt prece vai preces varianti, piemēram, stila un krāsas varianti.</span><span class="sxs-lookup"><span data-stu-id="cf191-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="cf191-109">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="cf191-109">Cost objects</span></span>

<span data-ttu-id="cf191-110">Sarakstā **Izmaksu objekti** ir parādīts saraksts ar visiem izmaksu objektiem, kas ir reģistrēti precei.</span><span class="sxs-lookup"><span data-stu-id="cf191-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="cf191-111">Izmaksu objektus nosaka dati no šādiem avotiem:</span><span class="sxs-lookup"><span data-stu-id="cf191-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="cf191-112">Produkts</span><span class="sxs-lookup"><span data-stu-id="cf191-112">Product</span></span>
-   <span data-ttu-id="cf191-113">Preces dimensijas grupa</span><span class="sxs-lookup"><span data-stu-id="cf191-113">Product dimension group</span></span>
-   <span data-ttu-id="cf191-114">Noliktavas dimensiju grupa</span><span class="sxs-lookup"><span data-stu-id="cf191-114">Storage dimension group</span></span>
-   <span data-ttu-id="cf191-115">Izsekošanas dimensijas grupa</span><span class="sxs-lookup"><span data-stu-id="cf191-115">Tracking dimension group</span></span>

<span data-ttu-id="cf191-116">**Piezīme.** Izmaksu objekts norāda tikai tādu izmaksu elementu, kura tips ir **Tiešie materiāli**.</span><span class="sxs-lookup"><span data-stu-id="cf191-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="cf191-117">Izmaksu objekts atšķiras no krājumu objekta ar to, kā izmaksu objektu nosaka krājumu dimensijas, kas atlasītas finanšu krājumiem.</span><span class="sxs-lookup"><span data-stu-id="cf191-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="cf191-118">Piemēram, krājumam ir šāda konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="cf191-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="cf191-119">**Vieta:** Fiziskie krājumi = Jā, Finanšu krājumi = Jā</span><span class="sxs-lookup"><span data-stu-id="cf191-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="cf191-120">**Noliktava:** Fiziskie krājumi = Jā, Finanšu krājumi = Nē</span><span class="sxs-lookup"><span data-stu-id="cf191-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="cf191-121">**Partijas Nr.:** Fiziskie krājumi = Jā, Finanšu krājumi = Nē</span><span class="sxs-lookup"><span data-stu-id="cf191-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="cf191-122">Šajā tabulā ir parādīts, kas ir izmaksu objekts un kas ir krājumu objekts.</span><span class="sxs-lookup"><span data-stu-id="cf191-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="cf191-123">Objekta veids</span><span class="sxs-lookup"><span data-stu-id="cf191-123">Object type</span></span>      | <span data-ttu-id="cf191-124">Krājuma numurs</span><span class="sxs-lookup"><span data-stu-id="cf191-124">Item number</span></span> | <span data-ttu-id="cf191-125">Vieta</span><span class="sxs-lookup"><span data-stu-id="cf191-125">Site</span></span> | <span data-ttu-id="cf191-126">Noliktava</span><span class="sxs-lookup"><span data-stu-id="cf191-126">Warehouse</span></span> | <span data-ttu-id="cf191-127">Paketes Nr.</span><span class="sxs-lookup"><span data-stu-id="cf191-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="cf191-128">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="cf191-128">Cost object</span></span>      | <span data-ttu-id="cf191-129">x</span><span class="sxs-lookup"><span data-stu-id="cf191-129">x</span></span>           | <span data-ttu-id="cf191-130">x</span><span class="sxs-lookup"><span data-stu-id="cf191-130">x</span></span>    |           |           |
| <span data-ttu-id="cf191-131">Krājumu objekts</span><span class="sxs-lookup"><span data-stu-id="cf191-131">Inventory object</span></span> | <span data-ttu-id="cf191-132">x</span><span class="sxs-lookup"><span data-stu-id="cf191-132">x</span></span>           | <span data-ttu-id="cf191-133">x</span><span class="sxs-lookup"><span data-stu-id="cf191-133">x</span></span>    |  <span data-ttu-id="cf191-134">x</span><span class="sxs-lookup"><span data-stu-id="cf191-134">x</span></span>        | <span data-ttu-id="cf191-135">x</span><span class="sxs-lookup"><span data-stu-id="cf191-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="cf191-136">Izmaksu un daudzumu uzkrāšana</span><span class="sxs-lookup"><span data-stu-id="cf191-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="cf191-137">Vērtība laukā **Vērtība** ir šādu vērtību summa:</span><span class="sxs-lookup"><span data-stu-id="cf191-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="cf191-138">Fiziskā izmaksu summa</span><span class="sxs-lookup"><span data-stu-id="cf191-138">Physical cost amount</span></span>
    -   <span data-ttu-id="cf191-139">Beigu izmaksu summa</span><span class="sxs-lookup"><span data-stu-id="cf191-139">Financial cost amount</span></span>
    -   <span data-ttu-id="cf191-140">Korekcijas</span><span class="sxs-lookup"><span data-stu-id="cf191-140">Adjustments</span></span>
-   <span data-ttu-id="cf191-141">Vērtība laukā **Daudzums** ir šādu vērtību summa:</span><span class="sxs-lookup"><span data-stu-id="cf191-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="cf191-142">Saņemts</span><span class="sxs-lookup"><span data-stu-id="cf191-142">Received</span></span>
    -   <span data-ttu-id="cf191-143">Atskaitīts</span><span class="sxs-lookup"><span data-stu-id="cf191-143">Deducted</span></span>
    -   <span data-ttu-id="cf191-144">Grāmatotais daudzums</span><span class="sxs-lookup"><span data-stu-id="cf191-144">Posted quantity</span></span>
-   <span data-ttu-id="cf191-145">Vērtība laukā **Vidējās vienības izmaksas** tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="cf191-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="cf191-146">Vērtība tiek aprēķināta, dalot vērtību laukā **Vērtība** ar vērtību laukā **Daudzums**.</span><span class="sxs-lookup"><span data-stu-id="cf191-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="cf191-147">**Piezīme.** Parametrs **Iekļaut fizisko vērtību** neietekmē iepriekšējos aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="cf191-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="cf191-148">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cf191-148">Additional resources</span></span>
--------

[<span data-ttu-id="cf191-149">Preces dimensijas grupa</span><span class="sxs-lookup"><span data-stu-id="cf191-149">Product dimension group</span></span>](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[<span data-ttu-id="cf191-150">Noliktavas dimensiju grupa</span><span class="sxs-lookup"><span data-stu-id="cf191-150">Storage dimension group</span></span>](/dynamicsax-2012//storage-dimension-groups-form)

[<span data-ttu-id="cf191-151">Izsekošanas dimensiju grupa</span><span class="sxs-lookup"><span data-stu-id="cf191-151">Tracking dimension group</span></span>](/dynamicsax-2012//tracking-dimension-groups-form)

[<span data-ttu-id="cf191-152">Jaunumi un izmaiņas</span><span class="sxs-lookup"><span data-stu-id="cf191-152">What's new or changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="cf191-153">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="cf191-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]