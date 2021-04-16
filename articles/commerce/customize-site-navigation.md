---
title: Vietnes navigācijas pielāgošana
description: Šajā tēmā aprakstīts, kā izveidot pielāgotu tiešsaistes navigācijas hierarhiju, lai organizētu produktus pārlūkošanai Microsoft Dynamics 365 Commerce vietnē.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799353"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="8e79b-103">Vietnes navigācijas pielāgošana</span><span class="sxs-lookup"><span data-stu-id="8e79b-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e79b-104">Šajā tēmā aprakstīts, kā izveidot pielāgotu tiešsaistes navigācijas hierarhiju, lai organizētu produktus pārlūkošanai Microsoft Dynamics 365 Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="8e79b-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="8e79b-105">Tiešsaistes veikala skatlogs parasti ļauj klientiem atklāt un pārlūkot preces, pārvietojoties pa preču kategorijām.</span><span class="sxs-lookup"><span data-stu-id="8e79b-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="8e79b-106">Šo iespēju parasti nodrošina cilnes lapas augšpusē vai navigācijas josla kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="8e79b-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="8e79b-107">Dynamics 365 Commerce varat izveidot un pārvaldīt savas kategoriju navigācijas hierarhijas struktūru un preces, kas ir iekļautas dažādās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="8e79b-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="8e79b-108">Kanālu navigācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="8e79b-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="8e79b-109">Lai izveidotu kanālu navigācijas hierarhiju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="8e79b-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="8e79b-110">Pārejiet uz **Mazumtirdzniecība un komercija \> Preces un kategorijas \> Kategorija un preču pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="8e79b-111">Atlasiet **Kategorijas hierarhijas** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="8e79b-112">Piešķiriet hierarhijai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8e79b-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e79b-113">Izveidotā augšējā kategorija ir saknes kategorijas mezgls.</span><span class="sxs-lookup"><span data-stu-id="8e79b-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="8e79b-114">Tā netiks parādīta jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="8e79b-114">It won't be shown on your site.</span></span> <span data-ttu-id="8e79b-115">Lai izveidotu kategoriju hierarhiju, kur jūsu vietnē tiek parādīts viens augšējā līmeņa mezgls, izveidojiet kategoriju un piešķiriet tai nosaukumu kā saknes apakškategorijai.</span><span class="sxs-lookup"><span data-stu-id="8e79b-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="8e79b-116">Atlasiet **Jauns kategorijas mezgls** un piešķiriet kategorijai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8e79b-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="8e79b-117">Turpiniet veidot nepieciešamās dvīņu un apakškategorijas.</span><span class="sxs-lookup"><span data-stu-id="8e79b-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="8e79b-118">Tagad varat piešķirt preces katrai kategorijai, ko izveidojāt zem augšējā līmeņa kategorijas.</span><span class="sxs-lookup"><span data-stu-id="8e79b-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="8e79b-119">Kategoriju secības pielāgošana</span><span class="sxs-lookup"><span data-stu-id="8e79b-119">Customize the order of categories</span></span>

<span data-ttu-id="8e79b-120">Pēc noklusējuma jūsu definētās kategorijas jūsu vietnē parādīsies alfabētiskā secībā.</span><span class="sxs-lookup"><span data-stu-id="8e79b-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="8e79b-121">Tomēr varat arī pielāgot kategoriju rādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="8e79b-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="8e79b-122">Kategoriju hierarhijas tipa piešķiršana</span><span class="sxs-lookup"><span data-stu-id="8e79b-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="8e79b-123">Pārejiet uz **Mazumtirdzniecība un komercija \> Preces un kategorijas \> Kategorija un preču pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="8e79b-124">Atlasiet **Kategorijas hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="8e79b-125">Darbību rūts cilnē **Kategoriju hierarhija** grupā **Iestatīt** atlasiet **Saistītās hierarhijas veids**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="8e79b-126">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-126">Select **New**.</span></span>
1. <span data-ttu-id="8e79b-127">Laukā **Kategoriju hierarhijas veids** atlasiet **Kanālu navigācijas hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="8e79b-128">Laukā **Kategoriju hierarhija** atlasiet iepriekš izveidoto kanāla navigācijas hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="8e79b-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="8e79b-129">Jaunu vai atjauninātu navigācijas hierarhiju publicēšana</span><span class="sxs-lookup"><span data-stu-id="8e79b-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="8e79b-130">Lai navigācijas hierarhiju padarītu pieejamu jūsu tiešsaistes veikala skatlogam, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="8e79b-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="8e79b-131">Pārejiet uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preču īpašības**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="8e79b-132">Kokā kreisajā pusē atlasiet jūsu tiešsaistes veikalu.</span><span class="sxs-lookup"><span data-stu-id="8e79b-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="8e79b-133">Atlasiet **Publicēt kanāla atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="8e79b-134">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="8e79b-135">Sarakstā atrodiet un atlasiet **Darbs 1040**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="8e79b-136">Atlasiet **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="8e79b-136">Select **Run now**.</span></span>
1. <span data-ttu-id="8e79b-137">Atkārtojiet 5. un 6. darbību darbiem 1070 un 1150.</span><span class="sxs-lookup"><span data-stu-id="8e79b-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="8e79b-138">Kategoriju parādīšana jūsu vietnē</span><span class="sxs-lookup"><span data-stu-id="8e79b-138">Show categories on your site</span></span>

<span data-ttu-id="8e79b-139">Lai parādītu kategoriju hierarhiju jūsu tiešsaistes veikala skatlogā, jums veidnes vai fragmenta atbilstošā vietā jāpievieno navigācijas izvēlnes modulis.</span><span class="sxs-lookup"><span data-stu-id="8e79b-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="8e79b-140">Navigācijas izvēlnes modulis tiks parādīts navigācijas hierarhijā, ar nosacījumu, ka publicējāt savu navigācijas hierarhiju kanālā, ar kuru saistīta jūsu vietne.</span><span class="sxs-lookup"><span data-stu-id="8e79b-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="8e79b-141">Moduļa bibliotēkā iekļautais navigācijas izvēlnes modulis ļauj lietotājiem pārvietoties tikai uz kategorijām, kurām nav apakškategoriju.</span><span class="sxs-lookup"><span data-stu-id="8e79b-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="8e79b-142">Ja jūsu klientiem vajadzētu pārvietoties uz kategorijām, kurām ir apakškategorijas, navigācijas izvēlnes modulis ir jāpielāgo.</span><span class="sxs-lookup"><span data-stu-id="8e79b-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="8e79b-143">Pielāgoto navigācijas opciju pievienošana</span><span class="sxs-lookup"><span data-stu-id="8e79b-143">Add custom navigation options</span></span>

<span data-ttu-id="8e79b-144">Jūsu navigācijas izvēlnē varat pievienot navigācijas opcijas, kas nav daļa no preču kategoriju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="8e79b-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="8e79b-145">Piemēram, preču kategoriju saraksta beigās varat pievienot elementu **Sazinieties ar mums**, kas norāda uz jūsu vietnei izveidoto kontaktinformācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="8e79b-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="8e79b-146">Lai navigācijas izvēlnei pievienotu pielāgotās navigācijas opcijas, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="8e79b-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="8e79b-147">Veidnē vai fragmentā, ko vēlaties pielāgot, atlasiet navigācijas izvēlnes moduli.</span><span class="sxs-lookup"><span data-stu-id="8e79b-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="8e79b-148">Rekvizītu rūts cilnē **Dati** atlasiet **Pievienot elementu**, lai izveidotu jaunu satura pārvaldības sistēmas (CMS) navigācijas elementu.</span><span class="sxs-lookup"><span data-stu-id="8e79b-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="8e79b-149">Ievadiet saites tekstu un URL.</span><span class="sxs-lookup"><span data-stu-id="8e79b-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="8e79b-150">Atkārtojiet 2. un 3. darbību, lai pievienotu vairāk pielāgoto navigācijas opciju.</span><span class="sxs-lookup"><span data-stu-id="8e79b-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="8e79b-151">Kad esat pabeidzis, atlasiet **Saglabāt**, lai saglabātu veidni vai fragmentu, un pēc tam atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu.</span><span class="sxs-lookup"><span data-stu-id="8e79b-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e79b-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8e79b-152">Additional resources</span></span>

[<span data-ttu-id="8e79b-153">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="8e79b-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="8e79b-154">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="8e79b-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="8e79b-155">Darbs ar iepriekš iestatītiem izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="8e79b-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="8e79b-156">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="8e79b-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="8e79b-157">Darbs ar moduļiem</span><span class="sxs-lookup"><span data-stu-id="8e79b-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="8e79b-158">Lapas vietrāža URL izveide</span><span class="sxs-lookup"><span data-stu-id="8e79b-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="8e79b-159">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="8e79b-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
