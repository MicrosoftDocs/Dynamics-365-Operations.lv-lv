---
title: Vērtējumu un apskatu moduļi
description: Šī tēma ietver vērtējumu un apskatu moduļus, kas tiek izmantoti preču informācijas lapās programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 26658ebdbc70613baf30c344664133b9cf5911ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243773"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="a87ae-103">Vērtējumu un apskatu moduļi</span><span class="sxs-lookup"><span data-stu-id="a87ae-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a87ae-104">Šī tēma ietver vērtējumu un apskatu moduļus, kas tiek izmantoti preču informācijas lapās (PDP) programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a87ae-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a87ae-105">Vērtējumi un atsauksmes par e-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, kā arī tas ir mehānisms, ka iegūt klientu atsauksmes par precēm.</span><span class="sxs-lookup"><span data-stu-id="a87ae-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="a87ae-106">Vērtējumi tiek parādīti preču saraksta lapās, kategoriju saraksta lapās, meklēšanas rezultātu lapās un citās vietņu lapās.</span><span class="sxs-lookup"><span data-stu-id="a87ae-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="a87ae-107">Vērtējumu histogrammas un atsauksmes par precēm tiek rādīti preču papildinformācijas lapās.</span><span class="sxs-lookup"><span data-stu-id="a87ae-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="a87ae-108">Izmantojot pogu **Uzrakstīt atsauksmi**, klienti iesniedz vērtējumus un atsauksmes par preci.</span><span class="sxs-lookup"><span data-stu-id="a87ae-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="a87ae-109">Šos PDP līdzekļus kontrolē vērtējumu un apskatu moduļi.</span><span class="sxs-lookup"><span data-stu-id="a87ae-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="a87ae-110">Vērtējumu un atsauksmju moduļi preču papildinformācijas lapās (PDP)</span><span class="sxs-lookup"><span data-stu-id="a87ae-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="a87ae-111">Trīs moduļi rāda vērtējumus un atsauksmes preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="a87ae-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="a87ae-112">Atsauksmes moduļa rakstīšana</span><span class="sxs-lookup"><span data-stu-id="a87ae-112">Write review module</span></span>
- <span data-ttu-id="a87ae-113">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-113">Product reviews list module</span></span>
- <span data-ttu-id="a87ae-114">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-114">Ratings histogram module</span></span>
 
<span data-ttu-id="a87ae-115">Tālāk redzamajā attēlā atspoguļots, kā izskatās vērtējumi un atsauksmes preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="a87ae-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Vērtējumu un atsauksmju moduļi preču papildinformācijas lapā (PDP)](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="a87ae-117">Lai iegūtu informāciju par to, kā optimizēt PDP veidnes un izkārtojumus, lai varētu koplietot konfigurācijas vērtēšanas un atsauksmju moduļiem starp vairākām PDP jūsu E-komercijas vietnē, skatiet tēmu [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a87ae-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="a87ae-118">Nākamajā attēlā ir parādīts, kā dialoglodziņā **Pievienot moduli** tiek atspoguļoti vērtējumi un atsauksmes programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a87ae-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="a87ae-119">![Dialoglodziņš Moduļa pievienošana](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="a87ae-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="a87ae-120">Atsauksmes rakstīšanas modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-120">Write review module</span></span>

<span data-ttu-id="a87ae-121">Atsauksmes rakstīšanas modulis ietver pogu **Rakstīt atsauksmi**, kas ļauj lietotājiem pierakstīties, piešķirt vērtējumu un uzrakstīt atsauksmi par preci.</span><span class="sxs-lookup"><span data-stu-id="a87ae-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="a87ae-122">Šis modulis arī ļauj lietotājiem rediģēt viņu iepriekš iesniegto vērtējumu vai atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="a87ae-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="a87ae-123">Šis modulis parasti tiek parādīts virs vērtējumu histogrammas un preces atsauksmju saraksta moduļiem preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="a87ae-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="a87ae-124">Nākamajā attēlā parādīts dialoglodziņš **Rakstīt atsauksmi**, kas tiek parādīts, klientam atlasot **Rakstīt atsauksmi**.</span><span class="sxs-lookup"><span data-stu-id="a87ae-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="a87ae-125">Klients var izmantot šo dialoglodziņu, lai iesniegtu vērtējumu un atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="a87ae-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="a87ae-126">![Dialoglodziņš atsauksmes rakstīšanai](media/rnr-eCommerce-write-review-module.png) Nākamajā tabulā ir parādīts atsauksmes rakstīšanas moduļa rekvizīts, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="a87ae-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="a87ae-127">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="a87ae-127">Property name</span></span> | <span data-ttu-id="a87ae-128">Vērtība</span><span class="sxs-lookup"><span data-stu-id="a87ae-128">Value</span></span>        | <span data-ttu-id="a87ae-129">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="a87ae-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="a87ae-130">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="a87ae-130">Name</span></span>          | <span data-ttu-id="a87ae-131">Atsauksmes rakstīšana</span><span class="sxs-lookup"><span data-stu-id="a87ae-131">Write review</span></span> | <span data-ttu-id="a87ae-132">Atsauksmes rakstīšanas moduļa nosaukums.</span><span class="sxs-lookup"><span data-stu-id="a87ae-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="a87ae-133">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-133">Ratings histogram module</span></span>

<span data-ttu-id="a87ae-134">Vērtējumu histogrammas modulis parāda vērtējumu histogrammu.</span><span class="sxs-lookup"><span data-stu-id="a87ae-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="a87ae-135">Šis modulis parasti tiek parādīts starp atsauksmes rakstīšanas moduli un preces atsauksmju saraksta moduli preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="a87ae-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="a87ae-136">Vērtējumu histogrammas modulim nav nepieciešama konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="a87ae-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="a87ae-137">Jums tikai jāpievieno modulis PDP veidnē.</span><span class="sxs-lookup"><span data-stu-id="a87ae-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="a87ae-138">Nākamajās ilustrācijās parādīts, kā izskatās PDP veidne programmā Dynamics 365 Commerce, kad vērtējumu un atsauksmju moduļi ir konfigurēti rādīšanai preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="a87ae-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="a87ae-139">![PDP veidne, kad vērtējumi un atsauksmes ir konfigurētas rādīšanai preču papildinformācijas lapās (PDP).](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="a87ae-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="a87ae-140">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-140">Product reviews list module</span></span>

<span data-ttu-id="a87ae-141">Atsauksmju par precēm saraksta modulī tiek rādīts preces atsauksmju saraksts kopā ar kārtošanas, filtrēšanas un lappušu numerācijas opcijām.</span><span class="sxs-lookup"><span data-stu-id="a87ae-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="a87ae-142">Šis modulis parasti parādās pēc vērtējumu histogrammas moduļa preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="a87ae-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="a87ae-143">Nākamajā tabulā ir parādīts preces atsauksmju saraksta moduļa rekvizīti, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="a87ae-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="a87ae-144">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="a87ae-144">Property name</span></span>              | <span data-ttu-id="a87ae-145">Vērtība</span><span class="sxs-lookup"><span data-stu-id="a87ae-145">Value</span></span> | <span data-ttu-id="a87ae-146">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="a87ae-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="a87ae-147">Katrā lapā parādītās atsauksmes</span><span class="sxs-lookup"><span data-stu-id="a87ae-147">Reviews shown on each page</span></span> | <span data-ttu-id="a87ae-148">10.</span><span class="sxs-lookup"><span data-stu-id="a87ae-148">10</span></span>    | <span data-ttu-id="a87ae-149">Atsauksmju skaits, kas vienlaicīgi jārāda preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="a87ae-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="a87ae-150">Lai lietotāji varētu pārvietoties pa atsauksmju lapām, ir iekļautas pogas **Nākamais** un **Iepriekšējais**.</span><span class="sxs-lookup"><span data-stu-id="a87ae-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="a87ae-151">Vērtējumu histogramma — kopsavilkuma skats</span><span class="sxs-lookup"><span data-stu-id="a87ae-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="a87ae-152">Preces atsauksmju saraksta modulī ir ietverts slots, kur varat pievienot vērtēšanas histogrammas moduli.</span><span class="sxs-lookup"><span data-stu-id="a87ae-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="a87ae-153">Nākamajā attēlā ir parādīts, kā var pievienot vērtēšanas histogrammas moduli preces atsauksmju saraksta modulī programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a87ae-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Vērtējumu histogrammas moduļa pievienošana preces atsauksmju saraksta modulī](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="a87ae-155">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a87ae-155">Additional resources</span></span>

[<span data-ttu-id="a87ae-156">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="a87ae-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a87ae-157">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a87ae-158">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a87ae-159">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a87ae-160">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a87ae-161">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a87ae-162">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="a87ae-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]