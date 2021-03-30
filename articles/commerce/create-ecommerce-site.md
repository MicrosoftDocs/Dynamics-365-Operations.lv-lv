---
title: E-komercijas vietnes izveide
description: Šajā tēmā ir aprakstītas darbības un informācija, kas nepieciešama, lai vietņu veidotājā Dynamics 365 Commerce izveidotu jaunu e-komercijas vietni.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 465154ef7209547481c8598d5eaefb434359b1fd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207986"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="fd929-103">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="fd929-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd929-104">Šajā tēmā ir aprakstītas darbības un informācija, kas nepieciešama, lai vietņu veidotājā Dynamics 365 Commerce izveidotu jaunu e-komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="fd929-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="fd929-105">Licencējot Dynamics 365 Commerce iespējas, vietnes veidotājam tiks nodrošināta sākuma vieta, kuru varat izmantot kā pamatu savai vietnei.</span><span class="sxs-lookup"><span data-stu-id="fd929-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="fd929-106">Tomēr, vēloties sākt no jauna vai vēloties izveidot otru vietni, jums vietnes autorēšanas vidē būs jāizveido jauna vietne.</span><span class="sxs-lookup"><span data-stu-id="fd929-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="fd929-107">Savas vietnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="fd929-107">Set up your site</span></span>

<span data-ttu-id="fd929-108">Vietnes iestatīšanai izpildiet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="fd929-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="fd929-109">Atveriet vietņu veidotāja vidi.</span><span class="sxs-lookup"><span data-stu-id="fd929-109">Open the site builder environment.</span></span> <span data-ttu-id="fd929-110">Saiti uz vietņu veidotāju var atrast pakalpojumos Microsoft Lifecycle Services (LCS), kas atrodas Commerce paredzētajā vides līdzekļu lapā.</span><span class="sxs-lookup"><span data-stu-id="fd929-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="fd929-111">Vietnes autorēšanas sākumlapā atlasiet **Jauna vietne**.</span><span class="sxs-lookup"><span data-stu-id="fd929-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="fd929-112">Dialoglodziņā **Jauna vietne** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="fd929-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="fd929-113">Lauks</span><span class="sxs-lookup"><span data-stu-id="fd929-113">Field</span></span>                               | <span data-ttu-id="fd929-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fd929-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="fd929-115">Vietnes nosaukums</span><span class="sxs-lookup"><span data-stu-id="fd929-115">Site name</span></span>                           | <span data-ttu-id="fd929-116">Ievadiet parādāmo nosaukumu, kas jāizmanto vietnei vietnes autorēšanas vidē.</span><span class="sxs-lookup"><span data-stu-id="fd929-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="fd929-117">Šis nosaukums ir redzams tikai autorēšanas vidē, un tas netiks rādīts klientiem.</span><span class="sxs-lookup"><span data-stu-id="fd929-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="fd929-118">Vietnes administratora drošības grupa</span><span class="sxs-lookup"><span data-stu-id="fd929-118">Site administrator's security group</span></span> | <span data-ttu-id="fd929-119">Norādiet Microsoft Azure Active Directory (Azure AD) drošības grupu, kas pārvalda lietotājus, kuriem ir šīs vietnes administratora loma.</span><span class="sxs-lookup"><span data-stu-id="fd929-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="fd929-120">Noklusējuma kanāls (pārvaldības struktūrvienības numurs)</span><span class="sxs-lookup"><span data-stu-id="fd929-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="fd929-121">Atlasiet tiešsaistes veikalu, kuram vietne kalpos kā tīmekļa vitrīna.</span><span class="sxs-lookup"><span data-stu-id="fd929-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="fd929-122">Ja vēlaties, lai e-komercijas vietne atbalsta vairākus tiešsaistes veikalus, tad pēc vietnes iestatīšanas ir jāsaista veikali ar savu vietni, izvēloties **Vietnes iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="fd929-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="fd929-123">Noklusējuma valoda</span><span class="sxs-lookup"><span data-stu-id="fd929-123">Default language</span></span>                            | <span data-ttu-id="fd929-124">Norādiet noklusējuma valodu šim tiešsaistes veikalam un tirgum.</span><span class="sxs-lookup"><span data-stu-id="fd929-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="fd929-125">Tiešsaistes veikals var atbalstīt vairākas valodas.</span><span class="sxs-lookup"><span data-stu-id="fd929-125">An online store can support multiple languages.</span></span> <span data-ttu-id="fd929-126">Ja vēlaties atbalstīt vairākas valodas šim tiešsaistes veikalam vai citam tiešsaistes veikalam, tad pēc vietnes iestatīšanas varat konfigurēt šo atbalstu, izvēloties **Vietnes iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="fd929-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="fd929-127">Domēns</span><span class="sxs-lookup"><span data-stu-id="fd929-127">Domain</span></span>                              | <span data-ttu-id="fd929-128">Atlasiet domēna nosaukumu, kas būs šī tiešsaistes veikala domēns.</span><span class="sxs-lookup"><span data-stu-id="fd929-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="fd929-129">Ja neesat konfigurējis nevienu domēnu pakalpojumā LCS, varat atstāt šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="fd929-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="fd929-130">Pēc tam, kad jūsu domēns ir konfigurēts pakalpojumā LCS, tas ir jāpievieno tiešsaistes veikalam, izvēloties **Vietnes iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="fd929-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="fd929-131">Ceļš</span><span class="sxs-lookup"><span data-stu-id="fd929-131">Path</span></span>                              | <span data-ttu-id="fd929-132">Ja jūsu vietne atbalsta vairāk nekā vienu valodu dotajam domēna vārdam, izmantojiet ceļa lauku, lai izveidotu unikālu vietnes URL šim domēnam un valodu kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="fd929-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="fd929-133">Ja valoda, ko norādījāt laukā **Noklusējuma valodā**, ir vienīgā valoda, ko atbalstīsiet šim domēnam, vai arī turpmāk būs noklusējuma valoda, pēc tam, kad būsiet lokalizējuši savu vietni citās valodās, iesakām atstāt šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="fd929-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="fd929-134">Pēc vietnes izveides varat pārbaudīt, vai tā ir saistīta ar jūsu tiešsaistes veikalu, atlasot cilni **Preces**. Jābūt redzamam preču klāstam, kas tika piešķirts tiešsaistes veikalam.</span><span class="sxs-lookup"><span data-stu-id="fd929-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="fd929-135">Lai piekļūtu piešķirtajām precēm pēc kategorijas, varat arī izmantot nolaižamo izvēlni lapas augšējā kreisajā malā.</span><span class="sxs-lookup"><span data-stu-id="fd929-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd929-136">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fd929-136">Additional resources</span></span>

[<span data-ttu-id="fd929-137">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="fd929-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fd929-138">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="fd929-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="fd929-139">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="fd929-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="fd929-140">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="fd929-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="fd929-141">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="fd929-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="fd929-142">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="fd929-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="fd929-143">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="fd929-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="fd929-144">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="fd929-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="fd929-145">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="fd929-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="fd929-146">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="fd929-146">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]