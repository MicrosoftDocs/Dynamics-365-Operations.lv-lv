---
title: Iepriekš definētu preces variantu izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d07a090dbd41eb17e8d604887435bbb8b07e8d9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966934"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="843aa-103">Iepriekš definētu preces variantu izveide</span><span class="sxs-lookup"><span data-stu-id="843aa-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="843aa-104">Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="843aa-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="843aa-105">Demonstrācijas uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="843aa-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="843aa-106">Preces šablona izveide</span><span class="sxs-lookup"><span data-stu-id="843aa-106">Create a product master</span></span>
1. <span data-ttu-id="843aa-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Preces šabloni.</span><span class="sxs-lookup"><span data-stu-id="843aa-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="843aa-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="843aa-108">Click New.</span></span>
3. <span data-ttu-id="843aa-109">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="843aa-110">Manuāla preces numura ievadīšana ir nepieciešama tikai tad, ja preces numura laukā nebija iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="843aa-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="843aa-111">Citiem vārdiem sakot, izlaidiet šo soli, ja attiecīgajā laukā ir iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="843aa-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="843aa-112">Laukā Preces nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="843aa-113">Laukā Preces dimensijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="843aa-114">Atlasiet preces dimensijas grupu SizeCol (izmērs un krāsa).</span><span class="sxs-lookup"><span data-stu-id="843aa-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="843aa-115">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="843aa-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="843aa-116">Pievienot preces dimensijas</span><span class="sxs-lookup"><span data-stu-id="843aa-116">Add product dimensions</span></span>
1. <span data-ttu-id="843aa-117">Noklikšķiniet uz Preces dimensijas.</span><span class="sxs-lookup"><span data-stu-id="843aa-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="843aa-118">Šajā piemērā parādīts, kā manuāli ievadīt preču dimensijas.</span><span class="sxs-lookup"><span data-stu-id="843aa-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="843aa-119">Jūs varat arī atlasīt izmēru, krāsu un stilu grupu, kurā ietilpst preces dimensiju vērtības, ko vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="843aa-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="843aa-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="843aa-120">Click New.</span></span>
3. <span data-ttu-id="843aa-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="843aa-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="843aa-122">Laukā Izmērs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="843aa-123">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="843aa-124">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="843aa-124">Click New.</span></span>
7. <span data-ttu-id="843aa-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="843aa-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="843aa-126">Laukā Izmērs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="843aa-127">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="843aa-128">Noklikšķiniet uz cilnes Krāsas.</span><span class="sxs-lookup"><span data-stu-id="843aa-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="843aa-129">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="843aa-129">Click New.</span></span>
12. <span data-ttu-id="843aa-130">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="843aa-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="843aa-131">Laukā Krāsa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="843aa-132">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="843aa-133">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="843aa-133">Click New.</span></span>
16. <span data-ttu-id="843aa-134">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="843aa-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="843aa-135">Laukā Krāsa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="843aa-136">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="843aa-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="843aa-137">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="843aa-137">Click Save.</span></span>
20. <span data-ttu-id="843aa-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="843aa-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="843aa-139">Ģenerēt preces variantus</span><span class="sxs-lookup"><span data-stu-id="843aa-139">Generate product variants</span></span>
1. <span data-ttu-id="843aa-140">Noklikšķiniet uz Preces varianti.</span><span class="sxs-lookup"><span data-stu-id="843aa-140">Click Product variants.</span></span>
2. <span data-ttu-id="843aa-141">Noklikšķiniet uz Variantu ieteikumi.</span><span class="sxs-lookup"><span data-stu-id="843aa-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="843aa-142">Noklikšķiniet uz Atlasīt visu.</span><span class="sxs-lookup"><span data-stu-id="843aa-142">Click Select all.</span></span>
    * <span data-ttu-id="843aa-143">Šajā piemērā ir atlasīti visi iespējamie varianti.</span><span class="sxs-lookup"><span data-stu-id="843aa-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="843aa-144">Ja variantu izveidei tiks izmantota tikai iespējamo preces dimensiju kombināciju apakškopa, varat atlasīt atsevišķus ierakstus.</span><span class="sxs-lookup"><span data-stu-id="843aa-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="843aa-145">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="843aa-145">Click Create.</span></span>
    * <span data-ttu-id="843aa-146">Jūs varat ģenerēt aprakstus visiem variantiem, pamatojoties uz preču dimensiju vērtību kombināciju.</span><span class="sxs-lookup"><span data-stu-id="843aa-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="843aa-147">Apraksti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="843aa-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="843aa-148">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="843aa-148">Click Save.</span></span>

