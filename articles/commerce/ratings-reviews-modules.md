---
title: Vērtējumu un apskatu moduļi
description: Šī tēma ietver vērtējumu un apskatu moduļus, kas tiek izmantoti preču informācijas lapās programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: dee9a6a7e2a5278f069958ce00689b1beb9b1bd7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792151"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="717cb-103">Vērtējumu un apskatu moduļi</span><span class="sxs-lookup"><span data-stu-id="717cb-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="717cb-104">Šī tēma ietver vērtējumu un apskatu moduļus, kas tiek izmantoti preču informācijas lapās (PDP) programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="717cb-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="717cb-105">Vērtējumi un atsauksmes par e-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, kā arī tas ir mehānisms, ka iegūt klientu atsauksmes par precēm.</span><span class="sxs-lookup"><span data-stu-id="717cb-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="717cb-106">Vērtējumi tiek parādīti preču saraksta lapās, kategoriju saraksta lapās, meklēšanas rezultātu lapās un citās vietņu lapās.</span><span class="sxs-lookup"><span data-stu-id="717cb-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="717cb-107">Vērtējumu histogrammas un atsauksmes par precēm tiek rādīti preču papildinformācijas lapās.</span><span class="sxs-lookup"><span data-stu-id="717cb-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="717cb-108">Izmantojot pogu **Uzrakstīt atsauksmi**, klienti iesniedz vērtējumus un atsauksmes par preci.</span><span class="sxs-lookup"><span data-stu-id="717cb-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="717cb-109">Šos PDP līdzekļus kontrolē vērtējumu un apskatu moduļi.</span><span class="sxs-lookup"><span data-stu-id="717cb-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="717cb-110">Vērtējumu un atsauksmju moduļi preču papildinformācijas lapās (PDP)</span><span class="sxs-lookup"><span data-stu-id="717cb-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="717cb-111">Trīs moduļi rāda vērtējumus un atsauksmes preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="717cb-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="717cb-112">Atsauksmes moduļa rakstīšana</span><span class="sxs-lookup"><span data-stu-id="717cb-112">Write review module</span></span>
- <span data-ttu-id="717cb-113">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-113">Product reviews list module</span></span>
- <span data-ttu-id="717cb-114">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-114">Ratings histogram module</span></span>
 
<span data-ttu-id="717cb-115">Tālāk redzamajā attēlā atspoguļots, kā izskatās vērtējumi un atsauksmes preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="717cb-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Vērtējumu un atsauksmju moduļi preču papildinformācijas lapā (PDP)](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="717cb-117">Lai iegūtu informāciju par to, kā optimizēt PDP veidnes un izkārtojumus, lai varētu koplietot konfigurācijas vērtēšanas un atsauksmju moduļiem starp vairākām PDP jūsu E-komercijas vietnē, skatiet tēmu [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="717cb-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="717cb-118">Nākamajā attēlā ir parādīts, kā dialoglodziņā **Pievienot moduli** tiek atspoguļoti vērtējumi un atsauksmes programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="717cb-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="717cb-119">![Dialoglodziņš Moduļa pievienošana](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="717cb-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="717cb-120">Atsauksmes rakstīšanas modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-120">Write review module</span></span>

<span data-ttu-id="717cb-121">Atsauksmes rakstīšanas modulis ietver pogu **Rakstīt atsauksmi**, kas ļauj lietotājiem pierakstīties, piešķirt vērtējumu un uzrakstīt atsauksmi par preci.</span><span class="sxs-lookup"><span data-stu-id="717cb-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="717cb-122">Šis modulis arī ļauj lietotājiem rediģēt viņu iepriekš iesniegto vērtējumu vai atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="717cb-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="717cb-123">Šis modulis parasti tiek parādīts virs vērtējumu histogrammas un preces atsauksmju saraksta moduļiem preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="717cb-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="717cb-124">Nākamajā attēlā parādīts dialoglodziņš **Rakstīt atsauksmi**, kas tiek parādīts, klientam atlasot **Rakstīt atsauksmi**.</span><span class="sxs-lookup"><span data-stu-id="717cb-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="717cb-125">Klients var izmantot šo dialoglodziņu, lai iesniegtu vērtējumu un atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="717cb-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="717cb-126">![Dialoglodziņš atsauksmes rakstīšanai](media/rnr-eCommerce-write-review-module.png) Nākamajā tabulā ir parādīts atsauksmes rakstīšanas moduļa rekvizīts, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="717cb-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="717cb-127">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="717cb-127">Property name</span></span> | <span data-ttu-id="717cb-128">Vērtība</span><span class="sxs-lookup"><span data-stu-id="717cb-128">Value</span></span>        | <span data-ttu-id="717cb-129">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="717cb-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="717cb-130">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="717cb-130">Name</span></span>          | <span data-ttu-id="717cb-131">Atsauksmes rakstīšana</span><span class="sxs-lookup"><span data-stu-id="717cb-131">Write review</span></span> | <span data-ttu-id="717cb-132">Atsauksmes rakstīšanas moduļa nosaukums.</span><span class="sxs-lookup"><span data-stu-id="717cb-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="717cb-133">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-133">Ratings histogram module</span></span>

<span data-ttu-id="717cb-134">Vērtējumu histogrammas modulis parāda vērtējumu histogrammu.</span><span class="sxs-lookup"><span data-stu-id="717cb-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="717cb-135">Šis modulis parasti tiek parādīts starp atsauksmes rakstīšanas moduli un preces atsauksmju saraksta moduli preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="717cb-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="717cb-136">Vērtējumu histogrammas modulim nav nepieciešama konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="717cb-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="717cb-137">Jums tikai jāpievieno modulis PDP veidnē.</span><span class="sxs-lookup"><span data-stu-id="717cb-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="717cb-138">Nākamajās ilustrācijās parādīts, kā izskatās PDP veidne programmā Dynamics 365 Commerce, kad vērtējumu un atsauksmju moduļi ir konfigurēti rādīšanai preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="717cb-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="717cb-139">![PDP veidne, kad vērtējumi un atsauksmes ir konfigurētas rādīšanai preču papildinformācijas lapās (PDP).](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="717cb-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="717cb-140">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-140">Product reviews list module</span></span>

<span data-ttu-id="717cb-141">Atsauksmju par precēm saraksta modulī tiek rādīts preces atsauksmju saraksts kopā ar kārtošanas, filtrēšanas un lappušu numerācijas opcijām.</span><span class="sxs-lookup"><span data-stu-id="717cb-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="717cb-142">Šis modulis parasti parādās pēc vērtējumu histogrammas moduļa preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="717cb-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="717cb-143">Nākamajā tabulā ir parādīts preces atsauksmju saraksta moduļa rekvizīti, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="717cb-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="717cb-144">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="717cb-144">Property name</span></span>              | <span data-ttu-id="717cb-145">Vērtība</span><span class="sxs-lookup"><span data-stu-id="717cb-145">Value</span></span> | <span data-ttu-id="717cb-146">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="717cb-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="717cb-147">Katrā lapā parādītās atsauksmes</span><span class="sxs-lookup"><span data-stu-id="717cb-147">Reviews shown on each page</span></span> | <span data-ttu-id="717cb-148">10.</span><span class="sxs-lookup"><span data-stu-id="717cb-148">10</span></span>    | <span data-ttu-id="717cb-149">Atsauksmju skaits, kas vienlaicīgi jārāda preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="717cb-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="717cb-150">Lai lietotāji varētu pārvietoties pa atsauksmju lapām, ir iekļautas pogas **Nākamais** un **Iepriekšējais**.</span><span class="sxs-lookup"><span data-stu-id="717cb-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="717cb-151">Vērtējumu histogramma — kopsavilkuma skats</span><span class="sxs-lookup"><span data-stu-id="717cb-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="717cb-152">Preces atsauksmju saraksta modulī ir ietverts slots, kur varat pievienot vērtēšanas histogrammas moduli.</span><span class="sxs-lookup"><span data-stu-id="717cb-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="717cb-153">Nākamajā attēlā ir parādīts, kā var pievienot vērtēšanas histogrammas moduli preces atsauksmju saraksta modulī programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="717cb-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Vērtējumu histogrammas moduļa pievienošana preces atsauksmju saraksta modulī](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="717cb-155">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="717cb-155">Additional resources</span></span>

[<span data-ttu-id="717cb-156">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="717cb-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="717cb-157">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="717cb-158">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="717cb-159">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="717cb-160">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="717cb-161">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="717cb-162">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="717cb-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]