---
title: E-komercijas vietnes izveide
description: Šajā tēmā aprakstīti uzdevumi, kas ir saistīti ar jaunas E-komercijas vietnes izveidi programmā Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945839"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="a1ea0-103">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="a1ea0-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a1ea0-104">Šajā tēmā aprakstīti uzdevumi, kas ir saistīti ar jaunas E-komercijas vietnes izveidi programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a1ea0-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="a1ea0-105">Overview</span></span>

<span data-ttu-id="a1ea0-106">Lai sāktu attīstīt savu E-komercijas vietni, vispirms ir jāizveido jauna vietne vietnes autorēšanas vidē.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="a1ea0-107">Pirms varat izveidot jaunu vietni, jāizveido vismaz viens tiešsaistes veikals programmā Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="a1ea0-108">Savas vietnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a1ea0-108">Set up your site</span></span>

<span data-ttu-id="a1ea0-109">Vietnes iestatīšanai izpildiet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="a1ea0-110">Portālā Microsoft Lifecycle Services (LCS) atlasiet saiti vietnes autorēšanas videi.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="a1ea0-111">Vietnes autorēšanas sākumlapā atlasiet **Jauna vietne**.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="a1ea0-112">Dialoglodziņā **Jauna vietne** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="a1ea0-113">Lauks</span><span class="sxs-lookup"><span data-stu-id="a1ea0-113">Field</span></span>                               | <span data-ttu-id="a1ea0-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a1ea0-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="a1ea0-115">Vietnes nosaukums</span><span class="sxs-lookup"><span data-stu-id="a1ea0-115">Site name</span></span>                           | <span data-ttu-id="a1ea0-116">Ievadiet parādāmo nosaukumu, kas jāizmanto vietnei vietnes autorēšanas vidē.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="a1ea0-117">Šis nosaukums ir redzams tikai autorēšanas vidē, un tas netiks rādīts klientiem.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="a1ea0-118">Vietnes administratora drošības grupa</span><span class="sxs-lookup"><span data-stu-id="a1ea0-118">Site administrator's security group</span></span> | <span data-ttu-id="a1ea0-119">Norādiet Microsoft Azure Active Directory (Azure AD) drošības grupu, kas pārvalda lietotājus, kuriem ir šīs vietnes administratora loma.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="a1ea0-120">Noklusējuma kanāls (pārvaldības struktūrvienības numurs)</span><span class="sxs-lookup"><span data-stu-id="a1ea0-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="a1ea0-121">Atlasiet tiešsaistes veikalu, kuram vietne kalpos kā tīmekļa vitrīna.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="a1ea0-122">Ja vēlaties, lai E-komercijas vietne atbalsta vairākus tiešsaistes veikalus, tad pēc vietnes iestatīšanas ir jāsaista veikali ar savu vietni, izvēloties **Vietnes iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="a1ea0-123">Noklusējuma valoda</span><span class="sxs-lookup"><span data-stu-id="a1ea0-123">Default language</span></span>                            | <span data-ttu-id="a1ea0-124">Norādiet noklusējuma valodu šim tiešsaistes veikalam un tirgum.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="a1ea0-125">Tiešsaistes veikals var atbalstīt vairākas valodas.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-125">An online store can support multiple languages.</span></span> <span data-ttu-id="a1ea0-126">Ja vēlaties atbalstīt vairākas valodas šim tiešsaistes veikalam vai citam tiešsaistes veikalam, tad pēc vietnes iestatīšanas varat konfigurēt šo atbalstu, izvēloties **Vietnes iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="a1ea0-127">Domēns</span><span class="sxs-lookup"><span data-stu-id="a1ea0-127">Domain</span></span>                              | <span data-ttu-id="a1ea0-128">Atlasiet domēna nosaukumu, kas būs šī tiešsaistes veikala domēns.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="a1ea0-129">Ja neesat konfigurējis nevienu domēnu pakalpojumā LCS, varat atstāt šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="a1ea0-130">Pēc tam, kad jūsu domēns ir konfigurēts pakalpojumā LCS, tas ir jāpievieno tiešsaistes veikalam, izvēloties **Vietnes iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="a1ea0-131">Ceļš</span><span class="sxs-lookup"><span data-stu-id="a1ea0-131">Path</span></span>                              | <span data-ttu-id="a1ea0-132">Ja jūsu vietne atbalsta vairāk nekā vienu valodu dotajam domēna vārdam, izmantojiet ceļa lauku, lai izveidotu unikālu vietnes URL šim domēnam un valodu kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="a1ea0-133">Ja valoda, ko norādījāt laukā **Noklusējuma valodā**, ir vienīgā valoda, ko atbalstīsiet šim domēnam, vai arī turpmāk būs noklusējuma valoda, pēc tam, kad būsiet lokalizējuši savu vietni citās valodās, iesakām atstāt šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="a1ea0-134">Pēc vietnes izveides varat pārbaudīt, vai tā ir saistīta ar jūsu tiešsaistes veikalu, atlasot cilni **Preces**. Jābūt redzamam preču klāstam, kas tika piešķirts tiešsaistes veikalam.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="a1ea0-135">Lai piekļūtu piešķirtajām precēm pēc kategorijas, varat arī izmantot nolaižamo izvēlni lapas augšējā kreisajā malā.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1ea0-136">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a1ea0-136">Additional resources</span></span>

[<span data-ttu-id="a1ea0-137">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a1ea0-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a1ea0-138">Jaunas e-komercijas vietnes izvietošana</span><span class="sxs-lookup"><span data-stu-id="a1ea0-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a1ea0-139">Tiešsaistes vietnes saistīšana ar kanālu</span><span class="sxs-lookup"><span data-stu-id="a1ea0-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a1ea0-140">robots.txt failu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="a1ea0-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a1ea0-141">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="a1ea0-141">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a1ea0-142">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="a1ea0-142">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a1ea0-143">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="a1ea0-143">Enable location-based store detection</span></span>](enable-store-detection.md)
