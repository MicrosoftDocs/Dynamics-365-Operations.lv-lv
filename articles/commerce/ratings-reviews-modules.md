---
title: Vērtējumu un apskatu moduļi
description: Šī tēma ietver vērtējumu un apskatu moduļus, kas tiek izmantoti preču informācijas lapās Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: ee2a2a781537b592fb5f80ce424a7331c4e21d41
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071878"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="6e0d2-103">Vērtējumu un apskatu moduļi</span><span class="sxs-lookup"><span data-stu-id="6e0d2-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6e0d2-104">Šī tēma ietver vērtējumu un apskatu moduļus, kas tiek izmantoti preču informācijas lapās (PDP) Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6e0d2-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="6e0d2-105">Overview</span></span>

<span data-ttu-id="6e0d2-106">Vērtējumi un atsauksmes par e-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, kā arī tas ir mehānisms, ka iegūt klientu atsauksmes par precēm.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="6e0d2-107">Vērtējumi tiek parādīti preču saraksta lapās, kategoriju saraksta lapās, meklēšanas rezultātu lapās un citās vietņu lapās.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="6e0d2-108">Vērtējumu histogrammas un atsauksmes par precēm tiek rādīti preču papildinformācijas lapās.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="6e0d2-109">Izmantojot pogu **Uzrakstīt atsauksmi**, klienti iesniedz vērtējumus un atsauksmes par preci.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="6e0d2-110">Šos PDP līdzekļus kontrolē vērtējumu un apskatu moduļi.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="6e0d2-111">Vērtējumu un atsauksmju moduļi preču papildinformācijas lapās (PDP)</span><span class="sxs-lookup"><span data-stu-id="6e0d2-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="6e0d2-112">Trīs moduļi rāda vērtējumus un atsauksmes preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="6e0d2-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="6e0d2-113">Atsauksmes moduļa rakstīšana</span><span class="sxs-lookup"><span data-stu-id="6e0d2-113">Write review module</span></span>
- <span data-ttu-id="6e0d2-114">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-114">Product reviews list module</span></span>
- <span data-ttu-id="6e0d2-115">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-115">Ratings histogram module</span></span>
 
<span data-ttu-id="6e0d2-116">Tālāk redzamajā attēlā atspoguļots, kā izskatās vērtējumi un atsauksmes preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="6e0d2-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Vērtējumu un atsauksmju moduļi preču papildinformācijas lapā (PDP)](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="6e0d2-118">Lai iegūtu informāciju par to, kā optimizēt PDP veidnes un izkārtojumus, lai varētu koplietot konfigurācijas vērtēšanas un atsauksmju moduļiem starp vairākām PDP jūsu E-komercijas vietnē, skatiet tēmu [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6e0d2-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="6e0d2-119">Nākamajā attēlā ir parādīts, kā dialoglodziņā **Pievienot moduli** tiek atspoguļoti vērtējumi un atsauksmes programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="6e0d2-120">![Dialoglodziņš Moduļa pievienošana](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="6e0d2-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="6e0d2-121">Atsauksmes rakstīšanas modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-121">Write review module</span></span>

<span data-ttu-id="6e0d2-122">Atsauksmes rakstīšanas modulis ietver pogu **Rakstīt atsauksmi**, kas ļauj lietotājiem pierakstīties, piešķirt vērtējumu un uzrakstīt atsauksmi par preci.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="6e0d2-123">Šis modulis arī ļauj lietotājiem rediģēt viņu iepriekš iesniegto vērtējumu vai atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="6e0d2-124">Šis modulis parasti tiek parādīts virs vērtējumu histogrammas un preces atsauksmju saraksta moduļiem preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="6e0d2-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="6e0d2-125">Nākamajā attēlā parādīts dialoglodziņš **Rakstīt atsauksmi**, kas tiek parādīts, klientam atlasot **Rakstīt atsauksmi**.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="6e0d2-126">Klients var izmantot šo dialoglodziņu, lai iesniegtu vērtējumu un atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="6e0d2-127">![Dialoglodziņš atsauksmes rakstīšanai](media/rnr-eCommerce-write-review-module.png) Nākamajā tabulā ir parādīts atsauksmes rakstīšanas moduļa rekvizīts, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="6e0d2-128">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="6e0d2-128">Property name</span></span> | <span data-ttu-id="6e0d2-129">Vērtība</span><span class="sxs-lookup"><span data-stu-id="6e0d2-129">Value</span></span>        | <span data-ttu-id="6e0d2-130">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="6e0d2-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="6e0d2-131">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="6e0d2-131">Name</span></span>          | <span data-ttu-id="6e0d2-132">Atsauksmes rakstīšana</span><span class="sxs-lookup"><span data-stu-id="6e0d2-132">Write review</span></span> | <span data-ttu-id="6e0d2-133">Atsauksmes rakstīšanas moduļa nosaukums.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="6e0d2-134">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-134">Ratings histogram module</span></span>

<span data-ttu-id="6e0d2-135">Vērtējumu histogrammas modulis parāda vērtējumu histogrammu.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="6e0d2-136">Šis modulis parasti tiek parādīts starp atsauksmes rakstīšanas moduli un preces atsauksmju saraksta moduli preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="6e0d2-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="6e0d2-137">Vērtējumu histogrammas modulim nav nepieciešama konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="6e0d2-138">Jums tikai jāpievieno modulis PDP veidnē.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="6e0d2-139">Nākamajās ilustrācijās parādīts, kā izskatās PDP veidne programmā Dynamics 365 Commerce, kad vērtējumu un atsauksmju moduļi ir konfigurēti rādīšanai preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="6e0d2-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="6e0d2-140">![PDP veidne, kad vērtējumi un atsauksmes ir konfigurētas rādīšanai preču papildinformācijas lapās (PDP).](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="6e0d2-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="6e0d2-141">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-141">Product reviews list module</span></span>

<span data-ttu-id="6e0d2-142">Atsauksmju par precēm saraksta modulī tiek rādīts preces atsauksmju saraksts kopā ar kārtošanas, filtrēšanas un lappušu numerācijas opcijām.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="6e0d2-143">Šis modulis parasti parādās pēc vērtējumu histogrammas moduļa preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="6e0d2-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="6e0d2-144">Nākamajā tabulā ir parādīts preces atsauksmju saraksta moduļa rekvizīti, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="6e0d2-145">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="6e0d2-145">Property name</span></span>              | <span data-ttu-id="6e0d2-146">Vērtība</span><span class="sxs-lookup"><span data-stu-id="6e0d2-146">Value</span></span> | <span data-ttu-id="6e0d2-147">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="6e0d2-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="6e0d2-148">Katrā lapā parādītās atsauksmes</span><span class="sxs-lookup"><span data-stu-id="6e0d2-148">Reviews shown on each page</span></span> | <span data-ttu-id="6e0d2-149">10.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-149">10</span></span>    | <span data-ttu-id="6e0d2-150">Atsauksmju skaits, kas vienlaicīgi jārāda preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="6e0d2-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="6e0d2-151">Lai lietotāji varētu pārvietoties pa atsauksmju lapām, ir iekļautas pogas **Nākamais** un **Iepriekšējais**.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="6e0d2-152">Vērtējumu histogramma — kopsavilkuma skats</span><span class="sxs-lookup"><span data-stu-id="6e0d2-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="6e0d2-153">Preces atsauksmju saraksta modulī ir ietverts slots, kur varat pievienot vērtēšanas histogrammas moduli.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="6e0d2-154">Nākamajā attēlā ir parādīts, kā var pievienot vērtēšanas histogrammas moduli preces atsauksmju saraksta modulī programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e0d2-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Vērtējumu histogrammas moduļa pievienošana preces atsauksmju saraksta modulī](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="6e0d2-156">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6e0d2-156">Additional resources</span></span>

[<span data-ttu-id="6e0d2-157">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="6e0d2-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6e0d2-158">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6e0d2-159">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6e0d2-160">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6e0d2-161">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6e0d2-162">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6e0d2-163">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="6e0d2-163">Footer module</span></span>](author-footer-module.md)
