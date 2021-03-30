---
title: Vērtējumu un atsauksmju konfigurēšana
description: Šajā tēmā aprakstīts, kā konfigurēt e-komercijas vietni, lai klientiem rādītu vērtējumus un atsauksmes risinājumā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 130c80c1d68c7fb207a4fa073fe2b0476cbdd409
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220538"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="0e92a-103">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0e92a-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e92a-104">Šajā tēmā aprakstīts, kā konfigurēt e-komercijas vietni, lai klientiem rādītu vērtējumus un atsauksmes risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e92a-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0e92a-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="0e92a-105">Overview</span></span>

<span data-ttu-id="0e92a-106">Vērtējumi un atsauksmes par e-komercijas tīmekļa vietnēm palīdz klientiem uzzināt par precēm, pirms viņi nolemj veikt pirkumu, parādot ko citi klienti domā par šīm precēm.</span><span class="sxs-lookup"><span data-stu-id="0e92a-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="0e92a-107">E-komercijas tīmekļa vietnēm vērtējumi un atsauksmes ir arī mehānisms klientu atsauksmju apkopošanai par precēm.</span><span class="sxs-lookup"><span data-stu-id="0e92a-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="0e92a-108">Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai</span><span class="sxs-lookup"><span data-stu-id="0e92a-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="0e92a-109">Konfigurācijas vērtības vērtējumiem un atsauksmēm, piemēram, īrnieka ID, atsauksmes teksta garums un atsauksmes nosaukuma garums tiek konfigurēti vietnes līmenī.</span><span class="sxs-lookup"><span data-stu-id="0e92a-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="0e92a-110">Lai konfigurētu vietni vērtējumu un atsauksmju rādīšanai, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="0e92a-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="0e92a-111">Dodieties uz **Sākums \> Vietnes**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="0e92a-112">Atlasiet vietnes nosaukumu</span><span class="sxs-lookup"><span data-stu-id="0e92a-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="0e92a-113">Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="0e92a-114">Laukā **Rediģēt teksta maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes tekstam (piemēram, **1000**).</span><span class="sxs-lookup"><span data-stu-id="0e92a-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="0e92a-115">Laukā **Rediģēt nosaukuma maksimālo garumu** ievadiet maksimālo rakstzīmju skaitu atsauksmes nosaukumam (piemēram, **55**).</span><span class="sxs-lookup"><span data-stu-id="0e92a-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="0e92a-116">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="0e92a-117">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e92a-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Vietnes konfigurēšana vērtējumu un atsauksmju rādīšanai](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="0e92a-119">Preču vērtējuma saistīšana ar PDP sadaļu Atsauksmes</span><span class="sxs-lookup"><span data-stu-id="0e92a-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="0e92a-120">Preces vērtējums tiek parādīts zem produkta nosaukuma preču papildinformācijas lapas (PDP) augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="0e92a-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="0e92a-121">Preces vērtējumu var konfigurēt tā, lai tas būtu saistīts ar tās pašas PDP sadaļu **Atsauksmes**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="0e92a-122">Lai saistītu preces vērtējumu ar PDP sadaļu **Atsauksmes**, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0e92a-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="0e92a-123">Atveriet PDP veidni.</span><span class="sxs-lookup"><span data-stu-id="0e92a-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="0e92a-124">Dodieties uz **Iegādes lodziņa konteinera moduļa iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="0e92a-125">Sadaļā **Iegādes lodziņš** atlasiet **Preču vērtējumi** un pēc tam atzīmējiet izvēles rūtiņu **Saistīt klikšķi ar pilnu atsauksmju moduli**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="0e92a-126">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e92a-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Preces vērtējuma saistīšana ar PDP sadaļu Atsauksmes](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="0e92a-128">Saites konfigurēšana konfidencialitātes un politikas lapai</span><span class="sxs-lookup"><span data-stu-id="0e92a-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="0e92a-129">Lai konfigurētu saiti konfidencialitātes un politikas lapai, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="0e92a-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="0e92a-130">Dodieties uz **Sākums \> Vietnes**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="0e92a-131">Atlasiet vietnes nosaukumu</span><span class="sxs-lookup"><span data-stu-id="0e92a-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="0e92a-132">Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="0e92a-133">Cilnē **Maršruti** zem **RNR konfidencialitāte un politika** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="0e92a-134">Ja saite jau ir ievadīta un jūs vēlaties to aizstāt, atlasiet saiti.</span><span class="sxs-lookup"><span data-stu-id="0e92a-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="0e92a-135">Dialoglodziņā **Pievienot saiti** atlasiet saiti konfidencialitātes un politikas lapai un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="0e92a-136">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="0e92a-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="0e92a-137">Nākamajā attēlā ir redzams, kā šī konfigurācija izskatās programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e92a-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Saites konfigurēšana konfidencialitātes un politikas lapai](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="0e92a-139">Konfigurējiet vērtējumu un pārskata moduļus preces detalizētas informācijas lapās</span><span class="sxs-lookup"><span data-stu-id="0e92a-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="0e92a-140">Informāciju par vērtējumu un apskatu konfigurēšanu preču detalizētas informācijas lapā skatiet sadaļā [Vērtējumu un apskatu moduļi](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="0e92a-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e92a-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0e92a-141">Additional resources</span></span>

[<span data-ttu-id="0e92a-142">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="0e92a-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="0e92a-143">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="0e92a-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="0e92a-144">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="0e92a-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="0e92a-145">Konfigurējiet vērtējumu un pārskata moduļus preces detalizētas informācijas lapās</span><span class="sxs-lookup"><span data-stu-id="0e92a-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="0e92a-146">Preču vērtējumu sinhronizācija Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="0e92a-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]