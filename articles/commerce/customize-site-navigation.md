---
title: Vietnes navigācijas pielāgošana
description: Šajā tēmā aprakstīts, kā izveidot pielāgotu tiešsaistes navigācijas hierarhiju, lai organizētu preces pārlūkošanai jūsu Microsoft Dynamics 365 Commerce vietnē.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 642cb5c145dec68631eb9ab27d926ba8ab75c59b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914914"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="b71bf-103">Vietnes navigācijas pielāgošana</span><span class="sxs-lookup"><span data-stu-id="b71bf-103">Customize site navigation</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b71bf-104">Šajā tēmā aprakstīts, kā izveidot pielāgotu tiešsaistes navigācijas hierarhiju, lai organizētu preces pārlūkošanai jūsu Microsoft Dynamics 365 Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="b71bf-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="b71bf-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="b71bf-105">Overview</span></span>

<span data-ttu-id="b71bf-106">Tiešsaistes veikala skatlogs parasti ļauj klientiem atklāt un pārlūkot preces, pārvietojoties pa preču kategorijām.</span><span class="sxs-lookup"><span data-stu-id="b71bf-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="b71bf-107">Šo iespēju parasti nodrošina cilnes lapas augšpusē vai navigācijas josla kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="b71bf-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="b71bf-108">Dynamics 365 Commerce varat izveidot un pārvaldīt savas kategoriju navigācijas hierarhijas struktūru un preces, kas ir iekļautas dažādās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="b71bf-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-retail-channel-navigation-hierarchy"></a><span data-ttu-id="b71bf-109">Mazumtirdzniecības kanāla navigācijas hierarhijas izveidošana</span><span class="sxs-lookup"><span data-stu-id="b71bf-109">Create a retail channel navigation hierarchy</span></span>

<span data-ttu-id="b71bf-110">Lai izveidotu mazumtirdzniecības kanāla navigācijas hierarhiju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="b71bf-110">To create a retail channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b71bf-111">Dodieties uz **Mazumtirdzniecība \> Preces un kategorijas \> Kategorija un preču pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-111">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="b71bf-112">Atlasiet **Kategorijas hierarhijas** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="b71bf-113">Piešķiriet hierarhijai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b71bf-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b71bf-114">Izveidotā augšējā kategorija ir saknes kategorijas mezgls.</span><span class="sxs-lookup"><span data-stu-id="b71bf-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="b71bf-115">Tā netiks parādīta jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="b71bf-115">It won't be shown on your site.</span></span> <span data-ttu-id="b71bf-116">Lai izveidotu kategoriju hierarhiju, kur jūsu vietnē tiek parādīts viens augšējā līmeņa mezgls, izveidojiet kategoriju un piešķiriet tai nosaukumu kā saknes apakškategorijai.</span><span class="sxs-lookup"><span data-stu-id="b71bf-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="b71bf-117">Atlasiet **Jauns kategorijas mezgls** un piešķiriet kategorijai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b71bf-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="b71bf-118">Turpiniet veidot nepieciešamās dvīņu un apakškategorijas.</span><span class="sxs-lookup"><span data-stu-id="b71bf-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="b71bf-119">Tagad varat piešķirt preces katrai kategorijai, ko izveidojāt zem augšējā līmeņa kategorijas.</span><span class="sxs-lookup"><span data-stu-id="b71bf-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="b71bf-120">Kategoriju secības pielāgošana</span><span class="sxs-lookup"><span data-stu-id="b71bf-120">Customize the order of categories</span></span>

<span data-ttu-id="b71bf-121">Pēc noklusējuma jūsu definētās kategorijas jūsu vietnē parādīsies alfabētiskā secībā.</span><span class="sxs-lookup"><span data-stu-id="b71bf-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="b71bf-122">Tomēr varat arī pielāgot kategoriju rādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="b71bf-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="b71bf-123">Kategoriju hierarhijas tipa piešķiršana</span><span class="sxs-lookup"><span data-stu-id="b71bf-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="b71bf-124">Dodieties uz **Mazumtirdzniecība \> Preces un kategorijas \> Kategorija un preču pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-124">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="b71bf-125">Atlasiet **Kategorijas hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="b71bf-126">Darbību rūts cilnē **Kategoriju hierarhija** grupā **Iestatīt** atlasiet **Saistītās hierarhijas veids**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="b71bf-127">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-127">Select **New**.</span></span>
1. <span data-ttu-id="b71bf-128">Laukā **Kategoriju hierarhijas veids** atlasiet **Mazumtirdzniecības kanāla navigācijas hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-128">In the **Category hierarchy type** field, select **Retail channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="b71bf-129">Laukā **Kategoriju hierarhija** atlasiet iepriekš izveidoto kanāla navigācijas hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="b71bf-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="b71bf-130">Jaunu vai atjauninātu navigācijas hierarhiju publicēšana</span><span class="sxs-lookup"><span data-stu-id="b71bf-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="b71bf-131">Lai navigācijas hierarhiju padarītu pieejamu jūsu tiešsaistes veikala skatlogam, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="b71bf-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="b71bf-132">Dodieties uz **Mazumtirdzniecība \> Kanāla iestatīšana \> Kanāla kategorijas un preses īpašības**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-132">Go to **Retail \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="b71bf-133">Kokā kreisajā pusē atlasiet jūsu tiešsaistes veikalu.</span><span class="sxs-lookup"><span data-stu-id="b71bf-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="b71bf-134">Atlasiet **Publicēt kanāla atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="b71bf-135">Atveriet sadaļu **Mazumtirdzniecība \> Mazumtirdzniecības IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-135">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b71bf-136">Sarakstā atrodiet un atlasiet **Darbs 1040**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="b71bf-137">Atlasiet **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="b71bf-137">Select **Run now**.</span></span>
1. <span data-ttu-id="b71bf-138">Atkārtojiet 5. un 6. darbību darbiem 1070 un 1150.</span><span class="sxs-lookup"><span data-stu-id="b71bf-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="b71bf-139">Kategoriju parādīšana jūsu vietnē</span><span class="sxs-lookup"><span data-stu-id="b71bf-139">Show categories on your site</span></span>

<span data-ttu-id="b71bf-140">Lai parādītu kategoriju hierarhiju jūsu tiešsaistes veikala skatlogā, jums veidnes vai fragmenta atbilstošā vietā jāpievieno navigācijas izvēlnes modulis.</span><span class="sxs-lookup"><span data-stu-id="b71bf-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="b71bf-141">Navigācijas izvēlnes modulis tiks parādīts navigācijas hierarhijā, ar nosacījumu, ka publicējāt savu mazumtirdzniecības navigācijas hierarhiju kanālā, ar kuru saistīta jūsu vietne.</span><span class="sxs-lookup"><span data-stu-id="b71bf-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your retail navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="b71bf-142">Veikala sākuma komplektā iekļautais navigācijas izvēlnes modulis ļauj lietotājiem pārvietoties tikai uz kategorijām, kurām nav apakškategoriju.</span><span class="sxs-lookup"><span data-stu-id="b71bf-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="b71bf-143">Ja jūsu klientiem vajadzētu pārvietoties uz kategorijām, kurām ir apakškategorijas, navigācijas izvēlnes modulis ir jāpielāgo.</span><span class="sxs-lookup"><span data-stu-id="b71bf-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="b71bf-144">Pielāgoto navigācijas opciju pievienošana</span><span class="sxs-lookup"><span data-stu-id="b71bf-144">Add custom navigation options</span></span>

<span data-ttu-id="b71bf-145">Jūsu navigācijas izvēlnē varat pievienot navigācijas opcijas, kas nav daļa no preču kategoriju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="b71bf-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="b71bf-146">Piemēram, preču kategoriju saraksta beigās varat pievienot elementu **Sazinieties ar mums**, kas norāda uz jūsu vietnei izveidoto kontaktinformācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="b71bf-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="b71bf-147">Lai navigācijas izvēlnei pievienotu pielāgotās navigācijas opcijas, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="b71bf-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="b71bf-148">Veidnē vai fragmentā, ko vēlaties pielāgot, atlasiet navigācijas izvēlnes moduli.</span><span class="sxs-lookup"><span data-stu-id="b71bf-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="b71bf-149">Rekvizītu rūts cilnē **Dati** atlasiet **Pievienot elementu**, lai izveidotu jaunu satura pārvaldības sistēmas (CMS) navigācijas elementu.</span><span class="sxs-lookup"><span data-stu-id="b71bf-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="b71bf-150">Ievadiet saites tekstu un URL.</span><span class="sxs-lookup"><span data-stu-id="b71bf-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="b71bf-151">Atkārtojiet 2. un 3. darbību, lai pievienotu vairāk pielāgoto navigācijas opciju.</span><span class="sxs-lookup"><span data-stu-id="b71bf-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="b71bf-152">Kad esat pabeidzis, saglabājiet veidni vai fragmentu un reģistrējiet to.</span><span class="sxs-lookup"><span data-stu-id="b71bf-152">When you've finished, save the template or fragment, and check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b71bf-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b71bf-153">Additional resources</span></span>

[<span data-ttu-id="b71bf-154">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="b71bf-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="b71bf-155">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="b71bf-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="b71bf-156">Darbs ar iepriekš iestatītiem izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="b71bf-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="b71bf-157">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="b71bf-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="b71bf-158">Darbs ar moduļiem</span><span class="sxs-lookup"><span data-stu-id="b71bf-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="b71bf-159">Lapas vietrāža URL izveide</span><span class="sxs-lookup"><span data-stu-id="b71bf-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="b71bf-160">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="b71bf-160">Work with publish groups</span></span>](publish-groups.md)
