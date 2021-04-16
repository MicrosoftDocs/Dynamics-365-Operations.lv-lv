---
title: Preces numuru nomenklatūras izveide konfigurētiem preces variantiem
description: Šajā procedūrā parādīts, kā iestatīt preces numura nomenklatūru konfigurētiem preču variantiem, un kā to var piesaistīt konfigurējamam preces šablonam.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f342831d95f9988f9bb7807bac986e43cb317e0f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820013"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="0a05c-103">Preces numuru nomenklatūras izveide konfigurētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="0a05c-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a05c-104">Šajā procedūrā parādīts, kā iestatīt preces numura nomenklatūru konfigurētiem preču variantiem, un kā to var piesaistīt konfigurējamam preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="0a05c-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="0a05c-105">Šajā procedūrā ir parādīts, kā jūs varat izveidot konfigurācijas nomenklatūru preces konfigurācijas modeļa komponentam.</span><span class="sxs-lookup"><span data-stu-id="0a05c-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="0a05c-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="0a05c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0a05c-107">Jauna preces numura nomenklatūra tiek piešķirta D0004 preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="0a05c-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="0a05c-108">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="0a05c-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="0a05c-109">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="0a05c-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="0a05c-110">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="0a05c-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="0a05c-111">Noklikšķiniet uz Preču nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="0a05c-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="0a05c-112">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="0a05c-112">Click New.</span></span>
4. <span data-ttu-id="0a05c-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a05c-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0a05c-114">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a05c-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="0a05c-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-115">Click Add.</span></span>
7. <span data-ttu-id="0a05c-116">Noklikšķiniet uz Preces šablona numurs.</span><span class="sxs-lookup"><span data-stu-id="0a05c-116">Click Product master number.</span></span>
8. <span data-ttu-id="0a05c-117">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-117">Click Add.</span></span>
9. <span data-ttu-id="0a05c-118">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="0a05c-118">Click Text constant.</span></span>
10. <span data-ttu-id="0a05c-119">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="0a05c-120">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="0a05c-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="0a05c-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-121">Click Add.</span></span>
13. <span data-ttu-id="0a05c-122">Noklikšķiniet uz Konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="0a05c-122">Click Configuration.</span></span>
14. <span data-ttu-id="0a05c-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="0a05c-124">Piešķirt preces numura nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="0a05c-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="0a05c-125">Noklikšķiniet uz Preču šabloni.</span><span class="sxs-lookup"><span data-stu-id="0a05c-125">Click Product masters.</span></span>
2. <span data-ttu-id="0a05c-126">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="0a05c-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0a05c-127">Piemēram, filtrējiet pēc preces numura lauka, izmantojot vērtību 'D'.</span><span class="sxs-lookup"><span data-stu-id="0a05c-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="0a05c-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0a05c-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0a05c-129">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0a05c-129">Click Edit.</span></span>
5. <span data-ttu-id="0a05c-130">Atlasiet Jā laukā Izmantot nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="0a05c-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="0a05c-131">Laukā Preces varianta numura nomenklatūra ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a05c-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="0a05c-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-132">Close the page.</span></span>
8. <span data-ttu-id="0a05c-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="0a05c-134">Izveidot nomenklatūru preces konfigurācijas modeļa komponentam</span><span class="sxs-lookup"><span data-stu-id="0a05c-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="0a05c-135">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="0a05c-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="0a05c-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0a05c-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0a05c-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0a05c-138">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0a05c-138">Click Edit.</span></span>
5. <span data-ttu-id="0a05c-139">Atlasiet Jā laukā Izmantot konfigurācijas nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="0a05c-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="0a05c-140">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-140">Click Add.</span></span>
7. <span data-ttu-id="0a05c-141">Noklikšķiniet uz Atribūta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0a05c-141">Click Attribute value.</span></span>
8. <span data-ttu-id="0a05c-142">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0a05c-143">Laukā Atribūts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a05c-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="0a05c-144">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-144">Click Add.</span></span>
11. <span data-ttu-id="0a05c-145">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="0a05c-145">Click Text constant.</span></span>
12. <span data-ttu-id="0a05c-146">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="0a05c-147">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="0a05c-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="0a05c-148">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-148">Click Add.</span></span>
15. <span data-ttu-id="0a05c-149">Noklikšķiniet uz Atribūta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0a05c-149">Click Attribute value.</span></span>
16. <span data-ttu-id="0a05c-150">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="0a05c-151">Laukā Atribūts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a05c-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="0a05c-152">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-152">Click Add.</span></span>
19. <span data-ttu-id="0a05c-153">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="0a05c-153">Click Text constant.</span></span>
20. <span data-ttu-id="0a05c-154">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="0a05c-155">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="0a05c-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="0a05c-156">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-156">Click Add.</span></span>
23. <span data-ttu-id="0a05c-157">Noklikšķiniet uz Atribūta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0a05c-157">Click Attribute value.</span></span>
24. <span data-ttu-id="0a05c-158">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="0a05c-159">Laukā Atribūts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a05c-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="0a05c-160">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-160">Click Add.</span></span>
27. <span data-ttu-id="0a05c-161">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="0a05c-161">Click Text constant.</span></span>
28. <span data-ttu-id="0a05c-162">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="0a05c-163">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="0a05c-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="0a05c-164">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-164">Click Add.</span></span>
31. <span data-ttu-id="0a05c-165">Noklikšķiniet uz Atribūta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0a05c-165">Click Attribute value.</span></span>
32. <span data-ttu-id="0a05c-166">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="0a05c-167">Laukā Atribūts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a05c-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="0a05c-168">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-168">Click Add.</span></span>
35. <span data-ttu-id="0a05c-169">Noklikšķiniet uz Teksta konstante.</span><span class="sxs-lookup"><span data-stu-id="0a05c-169">Click Text constant.</span></span>
36. <span data-ttu-id="0a05c-170">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="0a05c-171">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="0a05c-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="0a05c-172">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0a05c-172">Click Add.</span></span>
39. <span data-ttu-id="0a05c-173">Noklikšķiniet uz Numuru sērijas vērtība.</span><span class="sxs-lookup"><span data-stu-id="0a05c-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="0a05c-174">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="0a05c-175">Laukā Numuru sērija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a05c-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="0a05c-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-176">Close the page.</span></span>
43. <span data-ttu-id="0a05c-177">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-177">Close the page.</span></span>
44. <span data-ttu-id="0a05c-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0a05c-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]