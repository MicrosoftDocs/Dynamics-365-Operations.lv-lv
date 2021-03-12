---
title: Plānošana ar negatīviem rīcībā esošajiem daudzumiem
description: Šajā tēmā izskaidrots, kā, lietojot plānošanas optimizāciju, tiek apstrādāts negatīvs rīcībā esošais daudzums.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72ed2ba42c6233461743492fe6776f376195ada6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983470"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="0f9e5-103">Plānošana ar negatīviem rīcībā esošajiem daudzumiem</span><span class="sxs-lookup"><span data-stu-id="0f9e5-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f9e5-104">Ja sistēma rāda negatīvu apkopotu rīcībā esošo daudzumu, plānošanas programma apstrādā daudzumu kā 0 (nulli), lai palīdzētu izvairīties no pasūtījuma apjoma pārsniegšanas.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="0f9e5-105">Lūk, kā šī funkcionalitāte darbojas:</span><span class="sxs-lookup"><span data-stu-id="0f9e5-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="0f9e5-106">Plānošanas optimizācijas funkcija apkopo rīcībā esošos daudzumus pie viszemākā vajadzību dimensiju līmeņa.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="0f9e5-107">(Piemēram, ja *novietojums* nav vajadzības dimensija, plānošanas optimizācijas apkopo rīcībā esošos daudzumus *noliktavas* līmenī.)</span><span class="sxs-lookup"><span data-stu-id="0f9e5-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="0f9e5-108">Ja kopējais rīcībā esošais daudzums vajadzību dimensiju zemākajā līmenī ir negatīvs, sistēma pieņem, ka rīcībā esošais daudzums patiesībā ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="0f9e5-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f9e5-109">Plānošanas sistēma var būt tikai tik precīza, cik precīzi ir ievades dati.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="0f9e5-110">Ja ievades dati ir neprecīzi, tad negatīvie rīcībā esošie ieraksti norādīs, ka krājumu informācija programmā Microsoft Dynamics 365 Supply Chain Management nav sinhronizēta ar reālo pasauli.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="0f9e5-111">Tāpēc plānošanas rezultāts būs kļūdains.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="0f9e5-112">Lai iegūtu precīzu plānošanas rezultātu, ir jāsamazina to ierakstu skaits, kuros tiek rādīts negatīvais rīcībā esošais daudzums.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="0f9e5-113">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="0f9e5-113">Example 1</span></span>

<span data-ttu-id="0f9e5-114">13. noliktava ir konfigurēta šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="0f9e5-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="0f9e5-115">**Vajadzību kods:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="0f9e5-116">**Minimālais:** 15 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="0f9e5-117">**Maksimālais** : 25 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="0f9e5-118">Zemākais seguma dimensiju līmenis ir *noliktava*, un šādi rīcībā esošie daudzumi tiek ierakstīti *vietas* līmenī:</span><span class="sxs-lookup"><span data-stu-id="0f9e5-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="0f9e5-119">**1. objekts, 13. noliktava, 1. vieta** 20 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="0f9e5-120">**1. objekts, 13. noliktava, 2. vieta:** &minus;8 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="0f9e5-121">Tāpēc kopējais rīcībā esošais daudzums 13. noliktavai ir 12 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="0f9e5-122">(= 20 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-122">(= 20 pcs.</span></span> <span data-ttu-id="0f9e5-123">&minus; = 8 gab.).</span><span class="sxs-lookup"><span data-stu-id="0f9e5-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="0f9e5-124">Šādā gadījumā plānošanas programma izmanto kopējo rīcībā esošo daudzumu, kas ir 12 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="0f9e5-125">13. noliktavai.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-125">for warehouse 13.</span></span>

<span data-ttu-id="0f9e5-126">Rezultāts tiek plānots 13 gab. pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="0f9e5-127">(= 25 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-127">(= 25 pcs.</span></span> <span data-ttu-id="0f9e5-128">&minus;12 gab.), lai uzpildītu 13. noliktavu no 12 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="0f9e5-129">uz 25 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="0f9e5-130">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="0f9e5-130">Example 2</span></span>

<span data-ttu-id="0f9e5-131">13. noliktava ir konfigurēta šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="0f9e5-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="0f9e5-132">**Vajadzību kods:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="0f9e5-133">**Minimālais:** 15 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="0f9e5-134">**Maksimālais** : 25 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="0f9e5-135">Zemākais seguma dimensiju līmenis ir *noliktava*, un šādi rīcībā esošie daudzumi tiek ierakstīti *vietas* līmenī:</span><span class="sxs-lookup"><span data-stu-id="0f9e5-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="0f9e5-136">**1. objekts, 13. noliktava, 1. vieta** 4 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="0f9e5-137">**1. objekts, 13. noliktava, 2. vieta:** &minus;8 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="0f9e5-138">Tāpēc kopējais rīcībā esošais daudzums 13. noliktavai ir &minus;4 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="0f9e5-139">(= 4 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-139">(= 4 pcs.</span></span> <span data-ttu-id="0f9e5-140">&minus; = 8 gab.).</span><span class="sxs-lookup"><span data-stu-id="0f9e5-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="0f9e5-141">Citiem vārdiem sakot, tas ir mazāks par 0 (nulli).</span><span class="sxs-lookup"><span data-stu-id="0f9e5-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="0f9e5-142">Šajā gadījumā plānošanas programma pieņem, ka rīcībā esošais daudzums 13. noliktavā ir 0 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="0f9e5-143">nevis &minus;4 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="0f9e5-144">Rezultāts tiek plānots 25 gab. pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="0f9e5-145">(= 25 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-145">(= 25 pcs.</span></span> <span data-ttu-id="0f9e5-146">&minus;0 gab.), lai uzpildītu 13. noliktavu no 0 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="0f9e5-147">uz 25 gab.</span><span class="sxs-lookup"><span data-stu-id="0f9e5-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="0f9e5-148">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="0f9e5-148">Related resources</span></span>

[<span data-ttu-id="0f9e5-149">Plānošanas optimizācijas apskats</span><span class="sxs-lookup"><span data-stu-id="0f9e5-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="0f9e5-150">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="0f9e5-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="0f9e5-151">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="0f9e5-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="0f9e5-152">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="0f9e5-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="0f9e5-153">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="0f9e5-153">Cancel a planning job</span></span>](cancel-planning-job.md)
