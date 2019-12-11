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
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770485"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="e1626-103">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e1626-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e1626-104">Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1626-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e1626-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="e1626-105">Overview</span></span>

<span data-ttu-id="e1626-106">Vērtējumi un atsauksmes par E-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, parādot ko citi klienti domā par šīm precēm.</span><span class="sxs-lookup"><span data-stu-id="e1626-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="e1626-107">E-komercijas tīmekļa vietnēm vērtējumi un atsauksmes ir arī mehānisms klientu atsauksmju apkopošanai par precēm.</span><span class="sxs-lookup"><span data-stu-id="e1626-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="e1626-108">Vērtējumi tiek parādīti preču saraksta lapās, kategoriju saraksta lapās, meklēšanas rezultātu lapās un citās vietņu lapās.</span><span class="sxs-lookup"><span data-stu-id="e1626-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="e1626-109">Vērtējumu histogrammas un atsauksmes par precēm tiek rādīti preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="e1626-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="e1626-110">Izmantojot pogu **Uzrakstīt atsauksmi**, klienti iesniedz vērtējumus un atsauksmes par preci.</span><span class="sxs-lookup"><span data-stu-id="e1626-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="e1626-111">Vērtējumu un atsauksmju moduļi preču papildinformācijas lapās (PDP)</span><span class="sxs-lookup"><span data-stu-id="e1626-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="e1626-112">Trīs moduļi rāda vērtējumus un atsauksmes preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="e1626-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="e1626-113">Atsauksmes moduļa rakstīšana</span><span class="sxs-lookup"><span data-stu-id="e1626-113">Write review module</span></span>
- <span data-ttu-id="e1626-114">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="e1626-114">Product reviews list module</span></span>
- <span data-ttu-id="e1626-115">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="e1626-115">Ratings histogram module</span></span>
 
<span data-ttu-id="e1626-116">Tālāk redzamajā attēlā atspoguļots, kā izskatās vērtējumi un atsauksmes preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="e1626-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Vērtējumu un atsauksmju moduļi preču papildinformācijas lapā (PDP)](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="e1626-118">Lai iegūtu informāciju par to, kā optimizēt PDP veidnes un izkārtojumus, lai varētu koplietot konfigurācijas vērtēšanas un atsauksmju moduļiem starp vairākām PDP jūsu E-komercijas vietnē, skatiet tēmu [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e1626-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="e1626-119">Nākamajā attēlā ir parādīts, kā dialoglodziņā **Pievienot moduli** tiek atspoguļoti vērtējumi un atsauksmes programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1626-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Dialoglodziņš Moduļa pievienošana](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="e1626-121">Atsauksmes rakstīšanas modulis</span><span class="sxs-lookup"><span data-stu-id="e1626-121">Write review module</span></span>

<span data-ttu-id="e1626-122">Atsauksmes rakstīšanas modulis ietver pogu **Rakstīt atsauksmi**, kas ļauj lietotājiem pierakstīties, piešķirt vērtējumu un uzrakstīt atsauksmi par preci.</span><span class="sxs-lookup"><span data-stu-id="e1626-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="e1626-123">Šis modulis arī ļauj lietotājiem rediģēt viņu iepriekš iesniegto vērtējumu vai atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="e1626-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="e1626-124">Šis modulis parasti tiek parādīts virs vērtējumu histogrammas un preces atsauksmju saraksta moduļiem preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="e1626-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="e1626-125">Nākamajā attēlā parādīts dialoglodziņš **Rakstīt atsauksmi**, kas tiek parādīts, klientam atlasot **Rakstīt atsauksmi**.</span><span class="sxs-lookup"><span data-stu-id="e1626-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="e1626-126">Klients var izmantot šo dialoglodziņu, lai iesniegtu vērtējumu un atsauksmi.</span><span class="sxs-lookup"><span data-stu-id="e1626-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Dialoglodziņš Rakstīt atsauksmi](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="e1626-128">Nākamajā tabulā ir parādīts atsauksmes rakstīšanas moduļa rekvizīts, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="e1626-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="e1626-129">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="e1626-129">Property name</span></span> | <span data-ttu-id="e1626-130">Vērtība</span><span class="sxs-lookup"><span data-stu-id="e1626-130">Value</span></span>        | <span data-ttu-id="e1626-131">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="e1626-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="e1626-132">Vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="e1626-132">Name</span></span>          | <span data-ttu-id="e1626-133">Atsauksmes rakstīšana</span><span class="sxs-lookup"><span data-stu-id="e1626-133">Write review</span></span> | <span data-ttu-id="e1626-134">Atsauksmes rakstīšanas moduļa nosaukums.</span><span class="sxs-lookup"><span data-stu-id="e1626-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="e1626-135">Vērtējumu histogrammas modulis</span><span class="sxs-lookup"><span data-stu-id="e1626-135">Ratings histogram module</span></span>

<span data-ttu-id="e1626-136">Vērtējumu histogrammas modulis parāda vērtējumu histogrammu.</span><span class="sxs-lookup"><span data-stu-id="e1626-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="e1626-137">Šis modulis parasti tiek parādīts starp atsauksmes rakstīšanas moduli un preces atsauksmju saraksta moduli preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="e1626-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="e1626-138">Vērtējumu histogrammas modulim nav nepieciešama konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="e1626-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="e1626-139">Jums tikai jāpievieno modulis PDP veidnē.</span><span class="sxs-lookup"><span data-stu-id="e1626-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="e1626-140">Nākamajās ilustrācijās parādīts, kā izskatās PDP veidne programmā Dynamics 365 Commerce, kad vērtējumu un atsauksmju moduļi ir konfigurēti rādīšanai preču papildinformācijas lapās (PDP).</span><span class="sxs-lookup"><span data-stu-id="e1626-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP veidne, kad vērtējumi un atsauksmes ir konfigurētas rādīšanai preču papildinformācijas lapās (PDP).](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="e1626-142">Preču atsauksmju saraksta modulis</span><span class="sxs-lookup"><span data-stu-id="e1626-142">Product reviews list module</span></span>

<span data-ttu-id="e1626-143">Atsauksmju par precēm saraksta modulī tiek rādīts preces atsauksmju saraksts kopā ar kārtošanas, filtrēšanas un lappušu numerācijas opcijām.</span><span class="sxs-lookup"><span data-stu-id="e1626-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="e1626-144">Šis modulis parasti parādās pēc vērtējumu histogrammas moduļa preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="e1626-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="e1626-145">Nākamajā tabulā ir parādīts preces atsauksmju saraksta moduļa rekvizīti, kas jākonfigurē autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="e1626-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="e1626-146">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="e1626-146">Property name</span></span>              | <span data-ttu-id="e1626-147">Vērtība</span><span class="sxs-lookup"><span data-stu-id="e1626-147">Value</span></span> | <span data-ttu-id="e1626-148">Rekvizīta apraksts</span><span class="sxs-lookup"><span data-stu-id="e1626-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="e1626-149">Katrā lapā parādītās atsauksmes</span><span class="sxs-lookup"><span data-stu-id="e1626-149">Reviews shown on each page</span></span> | <span data-ttu-id="e1626-150">10.</span><span class="sxs-lookup"><span data-stu-id="e1626-150">10</span></span>    | <span data-ttu-id="e1626-151">Atsauksmju skaits, kas vienlaicīgi jārāda preču papildinformācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="e1626-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="e1626-152">Lai lietotāji varētu pārvietoties pa atsauksmju lapām, ir iekļautas pogas **Nākamais** un **Iepriekšējais**.</span><span class="sxs-lookup"><span data-stu-id="e1626-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="e1626-153">Vērtējumu histogramma — kopsavilkuma skats</span><span class="sxs-lookup"><span data-stu-id="e1626-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="e1626-154">Preces atsauksmju saraksta modulī ir ietverts slots, kur varat pievienot vērtēšanas histogrammas moduli.</span><span class="sxs-lookup"><span data-stu-id="e1626-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="e1626-155">Nākamajā attēlā ir parādīts, kā var pievienot vērtēšanas histogrammas moduli preces atsauksmju saraksta modulī programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1626-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Vērtējumu histogrammas moduļa pievienošana preces atsauksmju saraksta modulī](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="e1626-157">Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai</span><span class="sxs-lookup"><span data-stu-id="e1626-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="e1626-158">Konfigurācijas vērtības vērtējumiem un atsauksmēm, piemēram, īrnieka ID, atsauksmes teksta garums un atsauksmes nosaukuma garums tiek konfigurēti vietnes līmenī.</span><span class="sxs-lookup"><span data-stu-id="e1626-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="e1626-159">Lai konfigurētu vietni vērtējumu un atsauksmju rādīšanai, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="e1626-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="e1626-160">Dodieties uz **Sākums \> Vietnes**.</span><span class="sxs-lookup"><span data-stu-id="e1626-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="e1626-161">Atlasiet vietnes nosaukumu</span><span class="sxs-lookup"><span data-stu-id="e1626-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="e1626-162">Dodieties uz **Vietnes pārvaldība \>Paplašināmība**.</span><span class="sxs-lookup"><span data-stu-id="e1626-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="e1626-163">Laukā **Rediģēt teksta maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes tekstam (piemēram, **1000**).</span><span class="sxs-lookup"><span data-stu-id="e1626-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="e1626-164">Laukā **Rediģēt nosaukuma maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes nosaukumam (piemēram, **55**).</span><span class="sxs-lookup"><span data-stu-id="e1626-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="e1626-165">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="e1626-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="e1626-166">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1626-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="e1626-168">Preču vērtējuma saistīšana ar PDP sadaļu Atsauksmes</span><span class="sxs-lookup"><span data-stu-id="e1626-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="e1626-169">Preces vērtējums tiek parādīts zem produkta nosaukuma preču papildinformācijas lapas (PDP) augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="e1626-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="e1626-170">Preces vērtējumu var konfigurēt tā, lai tas būtu saistīts ar tās pašas PDP sadaļu **Atsauksmes**.</span><span class="sxs-lookup"><span data-stu-id="e1626-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="e1626-171">Lai saistītu preces vērtējumu ar PDP sadaļu **Atsauksmes**, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e1626-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="e1626-172">Atveriet PDP veidni.</span><span class="sxs-lookup"><span data-stu-id="e1626-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="e1626-173">Dodieties uz **Iegādes lodziņa konteinera moduļa iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e1626-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="e1626-174">Sadaļā **Iegādes lodziņš**atlasiet **Preču vērtējumi** un pēc tam atzīmējiet izvēles rūtiņu **Saistīt klikšķi ar pilnu atsauksmju moduli**.</span><span class="sxs-lookup"><span data-stu-id="e1626-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="e1626-175">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1626-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Preces vērtējuma saistīšana ar PDP sadaļu Atsauksmes](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="e1626-177">Saites konfigurēšana konfidencialitātes un politikas lapai</span><span class="sxs-lookup"><span data-stu-id="e1626-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="e1626-178">Lai konfigurētu saiti konfidencialitātes un politikas lapai, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="e1626-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="e1626-179">Dodieties uz **Sākums \> Vietnes**.</span><span class="sxs-lookup"><span data-stu-id="e1626-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="e1626-180">Atlasiet vietnes nosaukumu</span><span class="sxs-lookup"><span data-stu-id="e1626-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="e1626-181">Dodieties uz **Vietnes pārvaldība \>Paplašināmība**.</span><span class="sxs-lookup"><span data-stu-id="e1626-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="e1626-182">Cilnē **Maršruti** zem **RNR konfidencialitāte un politika** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="e1626-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="e1626-183">Ja saite jau ir ievadīta un jūs vēlaties to aizstāt, atlasiet saiti.</span><span class="sxs-lookup"><span data-stu-id="e1626-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="e1626-184">Dialoglodziņā **Pievienot saiti** atlasiet saiti konfidencialitātes un politikas lapai un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1626-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="e1626-185">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="e1626-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="e1626-186">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1626-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Saites konfigurēšana konfidencialitātes un politikas lapai](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="e1626-188">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e1626-188">Additional resources</span></span>

[<span data-ttu-id="e1626-189">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="e1626-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="e1626-190">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="e1626-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="e1626-191">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="e1626-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="e1626-192">Preču vērtējumu sinhronizācija Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="e1626-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
