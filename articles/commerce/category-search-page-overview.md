---
title: Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas pārskats
description: Šajā tēmā ir sniegts pārskats par noklusējuma kategorijas ielādes lapu un meklēšanas rezultātu lapu programmā Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e85449c10fa4a768a144ce423a77bd1fc2c94352
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527472"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a><span data-ttu-id="8f5de-103">Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas pārskats</span><span class="sxs-lookup"><span data-stu-id="8f5de-103">Default category landing page and search results page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8f5de-104">Šajā tēmā ir sniegts pārskats par noklusējuma kategorijas ielādes lapu un meklēšanas rezultātu lapu programmā Microsoft Dynamics 365 Commerce E-komercija.</span><span class="sxs-lookup"><span data-stu-id="8f5de-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="8f5de-105">Noklusējuma kategorijas ielādes lapa</span><span class="sxs-lookup"><span data-stu-id="8f5de-105">Default category landing page</span></span>

<span data-ttu-id="8f5de-106">Noklusējuma kategorijas ielādes lapa ir lapa, uz kuru parasti tiek novirzīti vietnes lietotāji, kad viņi atlasa kategoriju navigācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="8f5de-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="8f5de-107">Kategorijas lapa ļauj jums pārlūkot, un jūs varat arī kārtot un attīrīt kategorizētās preces.</span><span class="sxs-lookup"><span data-stu-id="8f5de-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Noklusējuma kategorijas ielādes lapa](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="8f5de-109">Lapas augšdaļā ir virsraksts, kas parāda visas preču kategorijas un citas lapas, kurām ir kategorizēts tirdzniecības vadītājs.</span><span class="sxs-lookup"><span data-stu-id="8f5de-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="8f5de-110">Konfigurācija tiek veikta kā kanāla navigācijas hierarhijas konfigurācijas sastāvdaļa.</span><span class="sxs-lookup"><span data-stu-id="8f5de-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="8f5de-111">Lapas apakšdaļā ir kājene, kas ietver ātras saites uz dažādām tēmām, kas varētu interesēt pircēju.</span><span class="sxs-lookup"><span data-stu-id="8f5de-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="8f5de-112">Kategorijai ir svarīgi šādi komponenti.</span><span class="sxs-lookup"><span data-stu-id="8f5de-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="8f5de-113">**Preču izvietošanas elementi** parāda preces, ko tirdzniecības vadītājs ir definējis kategorijā kā navigācijas hierarhijas konfigurācijas sastāvdaļu.</span><span class="sxs-lookup"><span data-stu-id="8f5de-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="8f5de-114">**Rafinētāji un izvēles kopsavilkums** ir filtri, kas sniedz uzskaitījumu un ko var izmantot krājumu precizēšanai.</span><span class="sxs-lookup"><span data-stu-id="8f5de-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="8f5de-115">Tirdzniecības vadītājs tos konfigurē kā daļu no metadatu konfigurācijas, kas ir saistīti ar kanāla kategorijām un preču atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="8f5de-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="8f5de-116">**Kārtošanas opcijas** izmanto vietņu apmeklētāji, lai šķirotu preces.</span><span class="sxs-lookup"><span data-stu-id="8f5de-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="8f5de-117">Pēc noklusējuma ir pieejamas šādas kārtošanas opcijas.</span><span class="sxs-lookup"><span data-stu-id="8f5de-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="8f5de-118">Cena – no zemas līdz augstai</span><span class="sxs-lookup"><span data-stu-id="8f5de-118">Price – low to high</span></span>
    - <span data-ttu-id="8f5de-119">Cena – no zemas līdz augstai</span><span class="sxs-lookup"><span data-stu-id="8f5de-119">Price – high to low</span></span>
    - <span data-ttu-id="8f5de-120">Preces nosaukums – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="8f5de-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="8f5de-121">Preces nosaukums – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="8f5de-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="8f5de-122">Vērtējumi – no zema līdz augstam</span><span class="sxs-lookup"><span data-stu-id="8f5de-122">Ratings – low to high</span></span>
    - <span data-ttu-id="8f5de-123">Vērtējumi – no zema līdz augstam</span><span class="sxs-lookup"><span data-stu-id="8f5de-123">Ratings – high to low</span></span>

- <span data-ttu-id="8f5de-124">**Lappušu numerācija** ļauj vietnes apmeklētājiem pāriet no vienas lapas ar kategorizētā produkta rezultātiem uz citu lapu.</span><span class="sxs-lookup"><span data-stu-id="8f5de-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="8f5de-125">**Kopējais skaits** nodrošina kopējo preču skaitu, kas definēts kategorijā.</span><span class="sxs-lookup"><span data-stu-id="8f5de-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="8f5de-126">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="8f5de-126">Enrich a category landing page</span></span>

<span data-ttu-id="8f5de-127">Ja vēlaties, lai kategorijas ielādes lapai būtu vairāk pielāgota pieredze noteiktai kategorijai, varat “bagātināt” kategorijas ielādes lapu šai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="8f5de-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="8f5de-128">Piemēram, varat pievienot mārketinga video un dažas kategorijas stāstījumus, lai piesaistītu pircēju uzmanību.</span><span class="sxs-lookup"><span data-stu-id="8f5de-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="8f5de-129">Plašāku informāciju skatiet tēmā [Kategorijas ielādes lapas bagātināšana](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="8f5de-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Bagātināta kategorijas ielādes lapa](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="8f5de-131">Automātiskās piedāvāšanas un meklēšanas rezultātu lapas</span><span class="sxs-lookup"><span data-stu-id="8f5de-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="8f5de-132">Vietnes lietotāji var apskatīt vietni, atverot kategoriju no navigācijas hierarhijas vai meklēšanas laukā ievadot meklējamo terminu.</span><span class="sxs-lookup"><span data-stu-id="8f5de-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="8f5de-133">Tiklīdz lietotāji sāk ievadīt vārdus meklēšanas laukā, viņiem tiek sniegta visaptveroša automātiskās piedāvāšanas funkcionalitāte, kas piedāvā meklēšanas terminus.</span><span class="sxs-lookup"><span data-stu-id="8f5de-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="8f5de-134">Piedāvājam dažus piedāvājumu tipus, kas var tikt rādīti.</span><span class="sxs-lookup"><span data-stu-id="8f5de-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="8f5de-135">**Atslēgvārdi** tiek izmantoti, lai atrastu elementus visās precēs, kas ir pievienotas kanālam.</span><span class="sxs-lookup"><span data-stu-id="8f5de-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="8f5de-136">**Preces** sniedz tiešas saites uz preču informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="8f5de-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="8f5de-137">**Atlasītie kategorijas meklēšanas ieteikumi** uzskaita dažādas kategorijas un ļauj lietotājiem meklēt atslēgvārdu noteiktā kategorijā.</span><span class="sxs-lookup"><span data-stu-id="8f5de-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Visaptveroša automātiskā piedāvāšana](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="8f5de-139">Kad lietotāji atlasa vienu no atslēgvārdiem vai atlasītajiem kategoriju meklēšanas ieteikumiem, vai ja nav ieteikumu meklētajam terminam, kas tiek ievadīts, viņi tiek novirzīti uz meklēšanas rezultātu lapu.</span><span class="sxs-lookup"><span data-stu-id="8f5de-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="8f5de-140">Pēc tam lietotāji var pārlūkot, kārtot un precizēt meklēšanas rezultātu sarakstu, lai atrastu vēlamo elementu.</span><span class="sxs-lookup"><span data-stu-id="8f5de-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Meklēšanas ielāde](./media/SearchLanding.png)

<span data-ttu-id="8f5de-142">Meklēšanas rezultātu lapai ir svarīgi šādi komponenti.</span><span class="sxs-lookup"><span data-stu-id="8f5de-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="8f5de-143">**Preču izvietošanas elementi** parāda preces lietotāja meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="8f5de-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="8f5de-144">Pēc noklusējuma šie elementi tiek kārtoti pēc mākoņa darbinātā meklēšanas atbilstības rādītāja lietotāja meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="8f5de-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="8f5de-145">**Rafinētāji un izvēles kopsavilkums** ir filtri, kas sniedz uzskaitījumu un ko var izmantot krājumu precizēšanai.</span><span class="sxs-lookup"><span data-stu-id="8f5de-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="8f5de-146">Tirdzniecības vadītājs tos konfigurē kā metadatu “kanāla kategorijas un preču atribūti” konfigurācijas daļu.</span><span class="sxs-lookup"><span data-stu-id="8f5de-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="8f5de-147">**Kārtošanas opcijas** izmanto vietņu apmeklētāji, lai šķirotu preces.</span><span class="sxs-lookup"><span data-stu-id="8f5de-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="8f5de-148">Pēc noklusējuma ir pieejamas šādas kārtošanas opcijas.</span><span class="sxs-lookup"><span data-stu-id="8f5de-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="8f5de-149">Cena – no zemas līdz augstai</span><span class="sxs-lookup"><span data-stu-id="8f5de-149">Price – low to high</span></span>
    - <span data-ttu-id="8f5de-150">Cena – no zemas līdz augstai</span><span class="sxs-lookup"><span data-stu-id="8f5de-150">Price – high to low</span></span>
    - <span data-ttu-id="8f5de-151">Preces nosaukums – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="8f5de-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="8f5de-152">Preces nosaukums – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="8f5de-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="8f5de-153">Vērtējumi – no zema līdz augstam</span><span class="sxs-lookup"><span data-stu-id="8f5de-153">Ratings – low to high</span></span>
    - <span data-ttu-id="8f5de-154">Vērtējumi – no zema līdz augstam</span><span class="sxs-lookup"><span data-stu-id="8f5de-154">Ratings – high to low</span></span>
    - <span data-ttu-id="8f5de-155">Noklusējuma vērtība</span><span class="sxs-lookup"><span data-stu-id="8f5de-155">Default</span></span>

- <span data-ttu-id="8f5de-156">**Lappušu numerācija** ļauj vietnes apmeklētājiem pāriet no vienas lapas ar kategorizētā produkta rezultātiem uz citu lapu.</span><span class="sxs-lookup"><span data-stu-id="8f5de-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="8f5de-157">**Kopējais skaits** nodrošina kopējo preču skaitu, kas definēts kategorijā un kas atbilst meklēšanas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="8f5de-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

>[!NOTE]
><span data-ttu-id="8f5de-158">Mākoņa darbinātas meklēšanas iespējas ir pieejamas, sākot ar versiju 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="8f5de-158">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="8f5de-159">Pārliecinieties, vai sadaļas **Commerce parametri > Konfigurācijas parametri** ievadne “ProductSearch.UseAzureSearch ir iestatīta kā “true””.</span><span class="sxs-lookup"><span data-stu-id="8f5de-159">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="8f5de-160">![Mākoņa darbinātas meklēšanas konfigurācijas parametri](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="8f5de-160">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f5de-161">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8f5de-161">Additional resources</span></span>

[<span data-ttu-id="8f5de-162">Mākoņa darbināts meklēšanas pārskats</span><span class="sxs-lookup"><span data-stu-id="8f5de-162">Cloud-powered search overview</span></span>](cloud-powered-search-overview.md)

[<span data-ttu-id="8f5de-163">Mājas lapas pārskats</span><span class="sxs-lookup"><span data-stu-id="8f5de-163">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="8f5de-164">Preču papildinformācijas lapu apskats</span><span class="sxs-lookup"><span data-stu-id="8f5de-164">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="8f5de-165">Pārskats par grozu un norēķināšanās lapām</span><span class="sxs-lookup"><span data-stu-id="8f5de-165">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="8f5de-166">Konta pārvaldības lapu pārskats</span><span class="sxs-lookup"><span data-stu-id="8f5de-166">Account management pages overview</span></span>](quick-tour-account-management.md)

