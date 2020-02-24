---
title: Vērtējumu un atsauksmju konfigurēšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002201"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="68080-103">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="68080-103">Configure ratings and reviews</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="68080-104">Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68080-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="68080-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="68080-105">Overview</span></span>

<span data-ttu-id="68080-106">Vērtējumi un atsauksmes par E-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, parādot ko citi klienti domā par šīm precēm.</span><span class="sxs-lookup"><span data-stu-id="68080-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="68080-107">E-komercijas tīmekļa vietnēm vērtējumi un atsauksmes ir arī mehānisms klientu atsauksmju apkopošanai par precēm.</span><span class="sxs-lookup"><span data-stu-id="68080-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="68080-108">Vērtējumi tiek parādīti preču saraksta lapās, kategoriju saraksta lapās, meklēšanas rezultātu lapās un citās vietņu lapās.</span><span class="sxs-lookup"><span data-stu-id="68080-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="68080-109">Vērtējumu histogrammas un atsauksmes par precēm tiek rādīti preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="68080-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="68080-110">Izmantojot pogu **Uzrakstīt atsauksmi**, klienti iesniedz vērtējumus un atsauksmes par preci.</span><span class="sxs-lookup"><span data-stu-id="68080-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="68080-111">Vērtējumu un atsauksmju moduļi preču papildinformācijas lapās (PDP)</span><span class="sxs-lookup"><span data-stu-id="68080-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="68080-112">Trīs moduļi rāda vērtējumus un atsauksmes preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="68080-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="68080-113">Atsauksmes moduļa rakstīšana</span><span class="sxs-lookup"><span data-stu-id="68080-113">Write review module</span></span>
- <span data-ttu-id="68080-114">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="68080-114">Product reviews list module</span></span>
- <span data-ttu-id="68080-115">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="68080-115">Ratings histogram module</span></span>
 
<span data-ttu-id="68080-116">Tālāk redzamajā attēlā atspoguļots, kā izskatās vērtējumi un atsauksmes preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="68080-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Vērtējumu un atsauksmju moduļi preču papildinformācijas lapā (PDP)](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="68080-118">Lai iegūtu informāciju par to, kā optimizēt PDP veidnes un izkārtojumus, lai varētu koplietot konfigurācijas vērtēšanas un atsauksmju moduļiem starp vairākām PDP jūsu E-komercijas vietnē, skatiet tēmu [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="68080-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="68080-119">Nākamajā attēlā ir parādīts, kā dialoglodziņā **Pievienot moduli** tiek atspoguļoti vērtējumi un atsauksmes programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68080-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Dialoglodziņš Moduļa pievienošana](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="68080-121">Atsauksmes rakstīšanas modulis</span><span class="sxs-lookup"><span data-stu-id="68080-121">Write review module</span></span>

<span data-ttu-id="68080-122">Atsauksmes rakstīšanas modulis ietver pogu **Rakstīt atsauksmi**, kas ļauj lietotājiem pierakstīties, piešķirt vērtējumu un uzrakstīt atsauksmi par preci.</span><span class="sxs-lookup"><span data-stu-id="68080-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="68080-123">Šis modulis arī ļauj lietotājiem rediģēt viņu iepriekš iesniegto vērtējumu vai atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="68080-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="68080-124">Šis modulis parasti tiek parādīts virs vērtējumu histogrammas un preces atsauksmju saraksta moduļiem preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="68080-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="68080-125">Nākamajā attēlā parādīts dialoglodziņš **Rakstīt atsauksmi**, kas tiek parādīts, klientam atlasot **Rakstīt atsauksmi**.</span><span class="sxs-lookup"><span data-stu-id="68080-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="68080-126">Klients var izmantot šo dialoglodziņu, lai iesniegtu vērtējumu un atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="68080-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Dialoglodziņš Rakstīt atsauksmi](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="68080-128">Nākamajā tabulā ir parādīts atsauksmes rakstīšanas moduļa rekvizīts, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="68080-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="68080-129">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="68080-129">Property name</span></span> | <span data-ttu-id="68080-130">Vērtība</span><span class="sxs-lookup"><span data-stu-id="68080-130">Value</span></span>        | <span data-ttu-id="68080-131">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="68080-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="68080-132">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="68080-132">Name</span></span>          | <span data-ttu-id="68080-133">Atsauksmes rakstīšana</span><span class="sxs-lookup"><span data-stu-id="68080-133">Write review</span></span> | <span data-ttu-id="68080-134">Atsauksmes rakstīšanas moduļa nosaukums.</span><span class="sxs-lookup"><span data-stu-id="68080-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="68080-135">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="68080-135">Ratings histogram module</span></span>

<span data-ttu-id="68080-136">Vērtējumu histogrammas modulis parāda vērtējumu histogrammu.</span><span class="sxs-lookup"><span data-stu-id="68080-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="68080-137">Šis modulis parasti tiek parādīts starp atsauksmes rakstīšanas moduli un preces atsauksmju saraksta moduli preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="68080-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="68080-138">Vērtējumu histogrammas modulim nav nepieciešama konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="68080-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="68080-139">Jums tikai jāpievieno modulis PDP veidnē.</span><span class="sxs-lookup"><span data-stu-id="68080-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="68080-140">Nākamajās ilustrācijās parādīts, kā izskatās PDP veidne programmā Dynamics 365 Commerce, kad vērtējumu un atsauksmju moduļi ir konfigurēti rādīšanai preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="68080-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP veidne, kad vērtējumi un atsauksmes ir konfigurētas rādīšanai preču papildinformācijas lapās (PDP).](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="68080-142">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="68080-142">Product reviews list module</span></span>

<span data-ttu-id="68080-143">Atsauksmju par precēm saraksta modulī tiek rādīts preces atsauksmju saraksts kopā ar kārtošanas, filtrēšanas un lappušu numerācijas opcijām.</span><span class="sxs-lookup"><span data-stu-id="68080-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="68080-144">Šis modulis parasti parādās pēc vērtējumu histogrammas moduļa preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="68080-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="68080-145">Nākamajā tabulā ir parādīts preces atsauksmju saraksta moduļa rekvizīti, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="68080-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="68080-146">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="68080-146">Property name</span></span>              | <span data-ttu-id="68080-147">Vērtība</span><span class="sxs-lookup"><span data-stu-id="68080-147">Value</span></span> | <span data-ttu-id="68080-148">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="68080-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="68080-149">Katrā lapā parādītās atsauksmes</span><span class="sxs-lookup"><span data-stu-id="68080-149">Reviews shown on each page</span></span> | <span data-ttu-id="68080-150">10.</span><span class="sxs-lookup"><span data-stu-id="68080-150">10</span></span>    | <span data-ttu-id="68080-151">Atsauksmju skaits, kas vienlaicīgi jārāda preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="68080-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="68080-152">Lai lietotāji varētu pārvietoties pa atsauksmju lapām, ir iekļautas pogas **Nākamais** un **Iepriekšējais**.</span><span class="sxs-lookup"><span data-stu-id="68080-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="68080-153">Vērtējumu histogramma — kopsavilkuma skats</span><span class="sxs-lookup"><span data-stu-id="68080-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="68080-154">Preces atsauksmju saraksta modulī ir ietverts slots, kur varat pievienot vērtēšanas histogrammas moduli.</span><span class="sxs-lookup"><span data-stu-id="68080-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="68080-155">Nākamajā attēlā ir parādīts, kā var pievienot vērtēšanas histogrammas moduli preces atsauksmju saraksta modulī programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68080-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Vērtējumu histogrammas moduļa pievienošana preces atsauksmju saraksta modulī](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="68080-157">Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai</span><span class="sxs-lookup"><span data-stu-id="68080-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="68080-158">Konfigurācijas vērtības vērtējumiem un atsauksmēm, piemēram, īrnieka ID, atsauksmes teksta garums un atsauksmes nosaukuma garums tiek konfigurēti vietnes līmenī.</span><span class="sxs-lookup"><span data-stu-id="68080-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="68080-159">Lai konfigurētu vietni vērtējumu un atsauksmju rādīšanai, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="68080-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="68080-160">Dodieties uz **Sākums \> Vietnes**.</span><span class="sxs-lookup"><span data-stu-id="68080-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="68080-161">Atlasiet vietnes nosaukumu</span><span class="sxs-lookup"><span data-stu-id="68080-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="68080-162">Dodieties uz **Vietnes pārvaldība \>Paplašināmība**.</span><span class="sxs-lookup"><span data-stu-id="68080-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="68080-163">Laukā **Rediģēt teksta maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes tekstam (piemēram, **1000**).</span><span class="sxs-lookup"><span data-stu-id="68080-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="68080-164">Laukā **Rediģēt nosaukuma maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes nosaukumam (piemēram, **55**).</span><span class="sxs-lookup"><span data-stu-id="68080-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="68080-165">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="68080-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="68080-166">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68080-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="68080-168">Preču vērtējuma saistīšana ar PDP sadaļu Atsauksmes</span><span class="sxs-lookup"><span data-stu-id="68080-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="68080-169">Preces vērtējums tiek parādīts zem produkta nosaukuma preču papildinformācijas lapas (PDP) augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="68080-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="68080-170">Preces vērtējumu var konfigurēt tā, lai tas būtu saistīts ar tās pašas PDP sadaļu **Atsauksmes**.</span><span class="sxs-lookup"><span data-stu-id="68080-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="68080-171">Lai saistītu preces vērtējumu ar PDP sadaļu **Atsauksmes**, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="68080-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="68080-172">Atveriet PDP veidni.</span><span class="sxs-lookup"><span data-stu-id="68080-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="68080-173">Dodieties uz **Iegādes lodziņa konteinera moduļa iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="68080-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="68080-174">Sadaļā **Iegādes lodziņš**atlasiet **Preču vērtējumi** un pēc tam atzīmējiet izvēles rūtiņu **Saistīt klikšķi ar pilnu atsauksmju moduli**.</span><span class="sxs-lookup"><span data-stu-id="68080-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="68080-175">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68080-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Preces vērtējuma saistīšana ar PDP sadaļu Atsauksmes](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="68080-177">Saites konfigurēšana konfidencialitātes un politikas lapai</span><span class="sxs-lookup"><span data-stu-id="68080-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="68080-178">Lai konfigurētu saiti konfidencialitātes un politikas lapai, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="68080-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="68080-179">Dodieties uz **Sākums \> Vietnes**.</span><span class="sxs-lookup"><span data-stu-id="68080-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="68080-180">Atlasiet vietnes nosaukumu</span><span class="sxs-lookup"><span data-stu-id="68080-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="68080-181">Dodieties uz **Vietnes pārvaldība \>Paplašināmība**.</span><span class="sxs-lookup"><span data-stu-id="68080-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="68080-182">Cilnē **Maršruti** zem **RNR konfidencialitāte un politika** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="68080-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="68080-183">Ja saite jau ir ievadīta un jūs vēlaties to aizstāt, atlasiet saiti.</span><span class="sxs-lookup"><span data-stu-id="68080-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="68080-184">Dialoglodziņā **Pievienot saiti** atlasiet saiti konfidencialitātes un politikas lapai un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="68080-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="68080-185">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="68080-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="68080-186">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68080-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Saites konfigurēšana konfidencialitātes un politikas lapai](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="68080-188">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="68080-188">Additional resources</span></span>

[<span data-ttu-id="68080-189">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="68080-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="68080-190">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="68080-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="68080-191">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="68080-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="68080-192">Preču vērtējumu sinhronizācija Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="68080-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
