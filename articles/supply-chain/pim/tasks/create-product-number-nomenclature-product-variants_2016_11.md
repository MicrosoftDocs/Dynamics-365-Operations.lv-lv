---
title: Preces numuru nomenklatūras izveide konfigurētiem preces variantiem
description: Šajā procedūrā parādīts, kā iestatīt preces numura nomenklatūru konfigurētiem preču variantiem, un kā to var piesaistīt konfigurējamam preces šablonam.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f75d7e493255b9c09c10b121f388854861cb0fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432775"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="c9123-103">Preces numuru nomenklatūras izveide konfigurētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="c9123-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9123-104">Šajā procedūrā parādīts, kā iestatīt preces numura nomenklatūru konfigurētiem preču variantiem, un kā to var piesaistīt konfigurējamam preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="c9123-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="c9123-105">Šajā procedūrā ir parādīts, kā jūs varat izveidot konfigurācijas nomenklatūru preces konfigurācijas modeļa komponentam.</span><span class="sxs-lookup"><span data-stu-id="c9123-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="c9123-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="c9123-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c9123-107">Jauna preces numura nomenklatūra tiek piešķirta D0004 preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="c9123-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="c9123-108">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="c9123-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="c9123-109">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="c9123-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="c9123-110">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="c9123-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="c9123-111">Noklikšķiniet uz Preču nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="c9123-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="c9123-112">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="c9123-112">Click New.</span></span>
4. <span data-ttu-id="c9123-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c9123-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c9123-114">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c9123-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c9123-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-115">Click Add.</span></span>
7. <span data-ttu-id="c9123-116">Noklikšķiniet uz Preces šablona numurs.</span><span class="sxs-lookup"><span data-stu-id="c9123-116">Click Product master number.</span></span>
8. <span data-ttu-id="c9123-117">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-117">Click Add.</span></span>
9. <span data-ttu-id="c9123-118">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="c9123-118">Click Text constant.</span></span>
10. <span data-ttu-id="c9123-119">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="c9123-120">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="c9123-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="c9123-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-121">Click Add.</span></span>
13. <span data-ttu-id="c9123-122">Noklikšķiniet uz Konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="c9123-122">Click Configuration.</span></span>
14. <span data-ttu-id="c9123-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c9123-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="c9123-124">Piešķirt preces numura nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="c9123-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="c9123-125">Noklikšķiniet uz Preču šabloni.</span><span class="sxs-lookup"><span data-stu-id="c9123-125">Click Product masters.</span></span>
2. <span data-ttu-id="c9123-126">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="c9123-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c9123-127">Piemēram, filtrējiet pēc preces numura lauka, izmantojot vērtību 'D'.</span><span class="sxs-lookup"><span data-stu-id="c9123-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="c9123-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c9123-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c9123-129">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="c9123-129">Click Edit.</span></span>
5. <span data-ttu-id="c9123-130">Atlasiet Jā laukā Izmantot nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="c9123-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="c9123-131">Laukā Preces varianta numura nomenklatūra ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c9123-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="c9123-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c9123-132">Close the page.</span></span>
8. <span data-ttu-id="c9123-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c9123-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="c9123-134">Izveidot nomenklatūru preces konfigurācijas modeļa komponentam</span><span class="sxs-lookup"><span data-stu-id="c9123-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="c9123-135">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="c9123-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="c9123-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c9123-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c9123-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c9123-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c9123-138">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="c9123-138">Click Edit.</span></span>
5. <span data-ttu-id="c9123-139">Atlasiet Jā laukā Izmantot konfigurācijas nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="c9123-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="c9123-140">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-140">Click Add.</span></span>
7. <span data-ttu-id="c9123-141">Noklikšķiniet uz Atribūta vērtība.</span><span class="sxs-lookup"><span data-stu-id="c9123-141">Click Attribute value.</span></span>
8. <span data-ttu-id="c9123-142">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c9123-143">Laukā Atribūts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c9123-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="c9123-144">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-144">Click Add.</span></span>
11. <span data-ttu-id="c9123-145">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="c9123-145">Click Text constant.</span></span>
12. <span data-ttu-id="c9123-146">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c9123-147">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="c9123-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="c9123-148">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-148">Click Add.</span></span>
15. <span data-ttu-id="c9123-149">Noklikšķiniet uz Atribūta vērtība.</span><span class="sxs-lookup"><span data-stu-id="c9123-149">Click Attribute value.</span></span>
16. <span data-ttu-id="c9123-150">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="c9123-151">Laukā Atribūts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c9123-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="c9123-152">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-152">Click Add.</span></span>
19. <span data-ttu-id="c9123-153">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="c9123-153">Click Text constant.</span></span>
20. <span data-ttu-id="c9123-154">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="c9123-155">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="c9123-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="c9123-156">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-156">Click Add.</span></span>
23. <span data-ttu-id="c9123-157">Noklikšķiniet uz Atribūta vērtība.</span><span class="sxs-lookup"><span data-stu-id="c9123-157">Click Attribute value.</span></span>
24. <span data-ttu-id="c9123-158">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="c9123-159">Laukā Atribūts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c9123-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="c9123-160">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-160">Click Add.</span></span>
27. <span data-ttu-id="c9123-161">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="c9123-161">Click Text constant.</span></span>
28. <span data-ttu-id="c9123-162">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="c9123-163">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="c9123-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="c9123-164">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-164">Click Add.</span></span>
31. <span data-ttu-id="c9123-165">Noklikšķiniet uz Atribūta vērtība.</span><span class="sxs-lookup"><span data-stu-id="c9123-165">Click Attribute value.</span></span>
32. <span data-ttu-id="c9123-166">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="c9123-167">Laukā Atribūts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c9123-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="c9123-168">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-168">Click Add.</span></span>
35. <span data-ttu-id="c9123-169">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="c9123-169">Click Text constant.</span></span>
36. <span data-ttu-id="c9123-170">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="c9123-171">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="c9123-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="c9123-172">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9123-172">Click Add.</span></span>
39. <span data-ttu-id="c9123-173">Noklikšķiniet uz Numuru sērijas vērtība.</span><span class="sxs-lookup"><span data-stu-id="c9123-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="c9123-174">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c9123-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="c9123-175">Laukā Numuru sērija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c9123-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="c9123-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c9123-176">Close the page.</span></span>
43. <span data-ttu-id="c9123-177">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c9123-177">Close the page.</span></span>
44. <span data-ttu-id="c9123-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c9123-178">Close the page.</span></span>

