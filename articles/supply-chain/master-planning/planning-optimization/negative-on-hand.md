---
title: Plānošana ar negatīviem rīcībā esošajiem daudzumiem
description: Šajā tēmā izskaidrots, kā, lietojot plānošanas optimizāciju, tiek apstrādāts negatīvs rīcībā esošais daudzums.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ca12d13f7318f649cb1dbc0f7c3cf56502c9d3ea
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077488"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="33634-103">Plānošana ar negatīviem rīcībā esošajiem daudzumiem</span><span class="sxs-lookup"><span data-stu-id="33634-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33634-104">Ja sistēma rāda negatīvu apkopotu rīcībā esošo daudzumu, plānošanas programma apstrādā daudzumu kā 0 (nulli), lai palīdzētu izvairīties no pasūtījuma apjoma pārsniegšanas.</span><span class="sxs-lookup"><span data-stu-id="33634-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="33634-105">Lūk, kā šī funkcionalitāte darbojas:</span><span class="sxs-lookup"><span data-stu-id="33634-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="33634-106">Plānošanas optimizācijas funkcija apkopo rīcībā esošos daudzumus pie viszemākā vajadzību dimensiju līmeņa.</span><span class="sxs-lookup"><span data-stu-id="33634-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="33634-107">(Piemēram, ja *novietojums* nav vajadzības dimensija, plānošanas optimizācijas apkopo rīcībā esošos daudzumus *noliktavas* līmenī.)</span><span class="sxs-lookup"><span data-stu-id="33634-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="33634-108">Ja kopējais rīcībā esošais daudzums vajadzību dimensiju zemākajā līmenī ir negatīvs, sistēma pieņem, ka rīcībā esošais daudzums patiesībā ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="33634-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33634-109">Plānošanas sistēma var būt tikai tik precīza, cik precīzi ir ievades dati.</span><span class="sxs-lookup"><span data-stu-id="33634-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="33634-110">Ja ievades dati ir neprecīzi, tad negatīvie rīcībā esošie ieraksti norādīs, ka krājumu informācija programmā Microsoft Dynamics 365 Supply Chain Management nav sinhronizēta ar reālo pasauli.</span><span class="sxs-lookup"><span data-stu-id="33634-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="33634-111">Tāpēc plānošanas rezultāts būs kļūdains.</span><span class="sxs-lookup"><span data-stu-id="33634-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="33634-112">Lai iegūtu precīzu plānošanas rezultātu, ir jāsamazina to ierakstu skaits, kuros tiek rādīts negatīvais rīcībā esošais daudzums.</span><span class="sxs-lookup"><span data-stu-id="33634-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="33634-113">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="33634-113">Example 1</span></span>

<span data-ttu-id="33634-114">13. noliktava ir konfigurēta šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="33634-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="33634-115">**Vajadzību kods:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="33634-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="33634-116">**Minimālais:** 15 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="33634-117">**Maksimālais** : 25 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="33634-118">Zemākais seguma dimensiju līmenis ir *noliktava*, un šādi rīcībā esošie daudzumi tiek ierakstīti *vietas* līmenī:</span><span class="sxs-lookup"><span data-stu-id="33634-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="33634-119">**1. objekts, 13. noliktava, 1. vieta** 20 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="33634-120">**1. objekts, 13. noliktava, 2. vieta:** &minus;8 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="33634-121">Tāpēc kopējais rīcībā esošais daudzums 13. noliktavai ir 12 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="33634-122">(= 20 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-122">(= 20 pcs.</span></span> <span data-ttu-id="33634-123">&minus; = 8 gab.).</span><span class="sxs-lookup"><span data-stu-id="33634-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="33634-124">Šādā gadījumā plānošanas programma izmanto kopējo rīcībā esošo daudzumu, kas ir 12 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="33634-125">13. noliktavai.</span><span class="sxs-lookup"><span data-stu-id="33634-125">for warehouse 13.</span></span>

<span data-ttu-id="33634-126">Rezultāts tiek plānots 13 gab. pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="33634-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="33634-127">(= 25 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-127">(= 25 pcs.</span></span> <span data-ttu-id="33634-128">&minus;12 gab.), lai uzpildītu 13. noliktavu no 12 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="33634-129">uz 25 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="33634-130">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="33634-130">Example 2</span></span>

<span data-ttu-id="33634-131">13. noliktava ir konfigurēta šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="33634-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="33634-132">**Vajadzību kods:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="33634-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="33634-133">**Minimālais:** 15 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="33634-134">**Maksimālais** : 25 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="33634-135">Zemākais seguma dimensiju līmenis ir *noliktava*, un šādi rīcībā esošie daudzumi tiek ierakstīti *vietas* līmenī:</span><span class="sxs-lookup"><span data-stu-id="33634-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="33634-136">**1. objekts, 13. noliktava, 1. vieta** 4 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="33634-137">**1. objekts, 13. noliktava, 2. vieta:** &minus;8 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="33634-138">Tāpēc kopējais rīcībā esošais daudzums 13. noliktavai ir &minus;4 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="33634-139">(= 4 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-139">(= 4 pcs.</span></span> <span data-ttu-id="33634-140">&minus; = 8 gab.).</span><span class="sxs-lookup"><span data-stu-id="33634-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="33634-141">Citiem vārdiem sakot, tas ir mazāks par 0 (nulli).</span><span class="sxs-lookup"><span data-stu-id="33634-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="33634-142">Šajā gadījumā plānošanas programma pieņem, ka rīcībā esošais daudzums 13. noliktavā ir 0 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="33634-143">nevis &minus;4 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="33634-144">Rezultāts tiek plānots 25 gab. pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="33634-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="33634-145">(= 25 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-145">(= 25 pcs.</span></span> <span data-ttu-id="33634-146">&minus;0 gab.), lai uzpildītu 13. noliktavu no 0 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="33634-147">uz 25 gab.</span><span class="sxs-lookup"><span data-stu-id="33634-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="33634-148">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="33634-148">Related resources</span></span>

[<span data-ttu-id="33634-149">Plānošanas optimizācijas apskats</span><span class="sxs-lookup"><span data-stu-id="33634-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="33634-150">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="33634-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="33634-151">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="33634-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="33634-152">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="33634-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="33634-153">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="33634-153">Cancel a planning job</span></span>](cancel-planning-job.md)
