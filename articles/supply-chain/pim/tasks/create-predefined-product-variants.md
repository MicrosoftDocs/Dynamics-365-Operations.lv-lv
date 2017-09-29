--- 
title: "Iepriekš definētu preces variantu izveide"
description: "Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: c49d25004b19084276404cf887188e89200afa32
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2017

---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="25733-103">Iepriekš definētu preces variantu izveide</span><span class="sxs-lookup"><span data-stu-id="25733-103">Create predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25733-104">Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="25733-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="25733-105">Demonstrācijas uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="25733-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="25733-106">Preces šablona izveide</span><span class="sxs-lookup"><span data-stu-id="25733-106">Create a product master</span></span>
1. <span data-ttu-id="25733-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Preces šabloni.</span><span class="sxs-lookup"><span data-stu-id="25733-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="25733-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="25733-108">Click New.</span></span>
3. <span data-ttu-id="25733-109">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="25733-110">Manuāla preces numura ievadīšana ir nepieciešama tikai tad, ja preces numura laukā nebija iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="25733-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="25733-111">Citiem vārdiem sakot, izlaidiet šo soli, ja attiecīgajā laukā ir iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="25733-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="25733-112">Laukā Preces nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="25733-113">Laukā Preces dimensijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="25733-114">Atlasiet preces dimensijas grupu SizeCol (izmērs un krāsa).</span><span class="sxs-lookup"><span data-stu-id="25733-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="25733-115">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="25733-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="25733-116">Pievienot preces dimensijas</span><span class="sxs-lookup"><span data-stu-id="25733-116">Add product dimensions</span></span>
1. <span data-ttu-id="25733-117">Noklikšķiniet uz Preces dimensijas.</span><span class="sxs-lookup"><span data-stu-id="25733-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="25733-118">Šajā piemērā parādīts, kā manuāli ievadīt preču dimensijas.</span><span class="sxs-lookup"><span data-stu-id="25733-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="25733-119">Jūs varat arī atlasīt izmēru, krāsu un stilu grupu, kurā ietilpst preces dimensiju vērtības, ko vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="25733-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="25733-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="25733-120">Click New.</span></span>
3. <span data-ttu-id="25733-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="25733-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="25733-122">Laukā Izmērs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="25733-123">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="25733-124">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="25733-124">Click New.</span></span>
7. <span data-ttu-id="25733-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="25733-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="25733-126">Laukā Izmērs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="25733-127">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="25733-128">Noklikšķiniet uz cilnes Krāsas.</span><span class="sxs-lookup"><span data-stu-id="25733-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="25733-129">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="25733-129">Click New.</span></span>
12. <span data-ttu-id="25733-130">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="25733-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="25733-131">Laukā Krāsa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="25733-132">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="25733-133">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="25733-133">Click New.</span></span>
16. <span data-ttu-id="25733-134">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="25733-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="25733-135">Laukā Krāsa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="25733-136">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25733-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="25733-137">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="25733-137">Click Save.</span></span>
20. <span data-ttu-id="25733-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="25733-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="25733-139">Ģenerēt preces variantus</span><span class="sxs-lookup"><span data-stu-id="25733-139">Generate product variants</span></span>
1. <span data-ttu-id="25733-140">Noklikšķiniet uz Preces varianti.</span><span class="sxs-lookup"><span data-stu-id="25733-140">Click Product variants.</span></span>
2. <span data-ttu-id="25733-141">Noklikšķiniet uz Variantu ieteikumi.</span><span class="sxs-lookup"><span data-stu-id="25733-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="25733-142">Noklikšķiniet uz Atlasīt visu.</span><span class="sxs-lookup"><span data-stu-id="25733-142">Click Select all.</span></span>
    * <span data-ttu-id="25733-143">Šajā piemērā ir atlasīti visi iespējamie varianti.</span><span class="sxs-lookup"><span data-stu-id="25733-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="25733-144">Ja variantu izveidei tiks izmantota tikai iespējamo preces dimensiju kombināciju apakškopa, varat atlasīt atsevišķus ierakstus.</span><span class="sxs-lookup"><span data-stu-id="25733-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="25733-145">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="25733-145">Click Create.</span></span>
    * <span data-ttu-id="25733-146">Jūs varat ģenerēt aprakstus visiem variantiem, pamatojoties uz preču dimensiju vērtību kombināciju.</span><span class="sxs-lookup"><span data-stu-id="25733-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="25733-147">Apraksti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="25733-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="25733-148">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="25733-148">Click Save.</span></span>


