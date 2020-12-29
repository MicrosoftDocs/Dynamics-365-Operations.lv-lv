---
title: Vērtējumu un atsauksmju konfigurēšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
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
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413952"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="c70b8-103">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c70b8-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c70b8-104">Šajā tēmā ir aprakstīts, kā konfigurēt E-komercijas vietni, lai rādītu klientu vērtējumus un atsauksmes programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c70b8-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c70b8-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="c70b8-105">Overview</span></span>

<span data-ttu-id="c70b8-106">Vērtējumi un atsauksmes par e-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, parādot ko citi klienti domā par šīm precēm.</span><span class="sxs-lookup"><span data-stu-id="c70b8-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="c70b8-107">E-komercijas tīmekļa vietnēm vērtējumi un atsauksmes ir arī mehānisms klientu atsauksmju apkopošanai par precēm.</span><span class="sxs-lookup"><span data-stu-id="c70b8-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="c70b8-108">Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai</span><span class="sxs-lookup"><span data-stu-id="c70b8-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="c70b8-109">Konfigurācijas vērtības vērtējumiem un atsauksmēm, piemēram, īrnieka ID, atsauksmes teksta garums un atsauksmes nosaukuma garums tiek konfigurēti vietnes līmenī.</span><span class="sxs-lookup"><span data-stu-id="c70b8-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="c70b8-110">Lai konfigurētu vietni vērtējumu un atsauksmju rādīšanai, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="c70b8-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="c70b8-111">Dodieties uz **Sākums \> Vietnes**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="c70b8-112">Atlasiet vietnes nosaukumu</span><span class="sxs-lookup"><span data-stu-id="c70b8-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="c70b8-113">Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="c70b8-114">Laukā **Rediģēt teksta maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes tekstam (piemēram, **1000**).</span><span class="sxs-lookup"><span data-stu-id="c70b8-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="c70b8-115">Laukā **Rediģēt nosaukuma maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes nosaukumam (piemēram, **55**).</span><span class="sxs-lookup"><span data-stu-id="c70b8-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="c70b8-116">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="c70b8-117">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c70b8-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="c70b8-119">Preču vērtējuma saistīšana ar PDP sadaļu Atsauksmes</span><span class="sxs-lookup"><span data-stu-id="c70b8-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="c70b8-120">Preces vērtējums tiek parādīts zem produkta nosaukuma preču papildinformācijas lapas (PDP) augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="c70b8-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="c70b8-121">Preces vērtējumu var konfigurēt tā, lai tas būtu saistīts ar tās pašas PDP sadaļu **Atsauksmes**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="c70b8-122">Lai saistītu preces vērtējumu ar PDP sadaļu **Atsauksmes**, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c70b8-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="c70b8-123">Atveriet PDP veidni.</span><span class="sxs-lookup"><span data-stu-id="c70b8-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="c70b8-124">Dodieties uz **Iegādes lodziņa konteinera moduļa iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="c70b8-125">Sadaļā **Iegādes lodziņš** atlasiet **Preču vērtējumi** un pēc tam atzīmējiet izvēles rūtiņu **Saistīt klikšķi ar pilnu atsauksmju moduli**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="c70b8-126">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c70b8-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Preces vērtējuma saistīšana ar PDP sadaļu Atsauksmes](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="c70b8-128">Saites konfigurēšana konfidencialitātes un politikas lapai</span><span class="sxs-lookup"><span data-stu-id="c70b8-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="c70b8-129">Lai konfigurētu saiti konfidencialitātes un politikas lapai, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="c70b8-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="c70b8-130">Dodieties uz **Sākums \> Vietnes**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="c70b8-131">Atlasiet vietnes nosaukumu</span><span class="sxs-lookup"><span data-stu-id="c70b8-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="c70b8-132">Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="c70b8-133">Cilnē **Maršruti** zem **RNR konfidencialitāte un politika** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="c70b8-134">Ja saite jau ir ievadīta un jūs vēlaties to aizstāt, atlasiet saiti.</span><span class="sxs-lookup"><span data-stu-id="c70b8-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="c70b8-135">Dialoglodziņā **Pievienot saiti** atlasiet saiti konfidencialitātes un politikas lapai un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="c70b8-136">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="c70b8-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="c70b8-137">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c70b8-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Saites konfigurēšana konfidencialitātes un politikas lapai](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="c70b8-139">Konfigurējiet vērtējumu un pārskata moduļus preces detalizētas informācijas lapās</span><span class="sxs-lookup"><span data-stu-id="c70b8-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="c70b8-140">Informāciju par vērtējumu un apskatu konfigurēšanu preču detalizētas informācijas lapā skatiet sadaļā [Vērtējumu un apskatu moduļi](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="c70b8-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c70b8-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c70b8-141">Additional resources</span></span>

[<span data-ttu-id="c70b8-142">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="c70b8-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="c70b8-143">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="c70b8-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="c70b8-144">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="c70b8-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="c70b8-145">Konfigurējiet vērtējumu un pārskata moduļus preces detalizētas informācijas lapās</span><span class="sxs-lookup"><span data-stu-id="c70b8-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="c70b8-146">Preču vērtējumu sinhronizācija Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="c70b8-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
