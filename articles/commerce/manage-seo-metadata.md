---
title: SEO metadatu pārvaldība
description: Šajā tēmā ir aprakstīts, kā pārvaldīt meklēšanas programmas optimizācijas (SEO) metadatus Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e7da7bf5c473746413e92babfa943f546b7724d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003468"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="2c14a-103">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="2c14a-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2c14a-104">Šajā tēmā ir aprakstīts, kā pārvaldīt meklēšanas programmas optimizācijas (SEO) metadatus Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c14a-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2c14a-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="2c14a-105">Overview</span></span>

<span data-ttu-id="2c14a-106">SEO metadatus vietnei var pārvaldīt, izmantojot vietnes kartes un lapas metadatus.</span><span class="sxs-lookup"><span data-stu-id="2c14a-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="2c14a-107">Vietnes kartes</span><span class="sxs-lookup"><span data-stu-id="2c14a-107">Site maps</span></span>

<span data-ttu-id="2c14a-108">Vietnes karte ir jūsu tīmekļa vietnes lapu mašīnlasāms saraksts XML formātā.</span><span class="sxs-lookup"><span data-stu-id="2c14a-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="2c14a-109">Tas paredzēts meklēšanas programmu lietošanai, lai tās varētu nodrošināt labākus meklēšanas rezultātus no jūsu vietnes.</span><span class="sxs-lookup"><span data-stu-id="2c14a-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="2c14a-110">Meklētājprogrammas var manuāli uzņemt vietnes kartes vai tās var publicēt robots.txt failā.</span><span class="sxs-lookup"><span data-stu-id="2c14a-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="2c14a-111">Dynamics 365 Commerce atbalsta automātisku vietnes karšu ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="2c14a-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="2c14a-112">Kad lapas tiek vai netiek publicētas, vietas kartes tiek automātiski atjauninātas.</span><span class="sxs-lookup"><span data-stu-id="2c14a-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="2c14a-113">Vietnes kartes ģenerēšanas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="2c14a-113">Turn on site map generation</span></span>

1. <span data-ttu-id="2c14a-114">Pierakstieties autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="2c14a-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="2c14a-115">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="2c14a-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2c14a-116">Navigācijas rūtī kreisajā pusē atlasiet **Lapas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="2c14a-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="2c14a-117">Pārliecinieties, vai ir ieslēgta opcija **Vietnes lapas iespējotas**.</span><span class="sxs-lookup"><span data-stu-id="2c14a-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="2c14a-118">Lapas metadati</span><span class="sxs-lookup"><span data-stu-id="2c14a-118">Page metadata</span></span>

<span data-ttu-id="2c14a-119">Dynamics 365 Commerce ļauj pārvaldīt SEO metadatus atsevišķām lapām.</span><span class="sxs-lookup"><span data-stu-id="2c14a-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="2c14a-120">Varat apskatīt un modificēt šo informāciju lapas konteinera sadaļā **SEO rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="2c14a-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="2c14a-121">Pašlaik tiek atbalstīti tālāk minētie SEO metadatu rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="2c14a-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="2c14a-122">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="2c14a-122">Title</span></span>
- <span data-ttu-id="2c14a-123">Apraksts</span><span class="sxs-lookup"><span data-stu-id="2c14a-123">Description</span></span>
- <span data-ttu-id="2c14a-124">SEO atslēgvārdi</span><span class="sxs-lookup"><span data-stu-id="2c14a-124">SEO keywords</span></span>
- <span data-ttu-id="2c14a-125">Aria etiķetes</span><span class="sxs-lookup"><span data-stu-id="2c14a-125">Aria labels</span></span>
- <span data-ttu-id="2c14a-126">noindex</span><span class="sxs-lookup"><span data-stu-id="2c14a-126">noindex</span></span>
- <span data-ttu-id="2c14a-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="2c14a-127">nofollow</span></span>
- <span data-ttu-id="2c14a-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="2c14a-128">noarchive</span></span>
- <span data-ttu-id="2c14a-129">nocache</span><span class="sxs-lookup"><span data-stu-id="2c14a-129">nocache</span></span>
- <span data-ttu-id="2c14a-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="2c14a-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="2c14a-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="2c14a-131">nosnippet</span></span>
- <span data-ttu-id="2c14a-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="2c14a-132">noImageIndex</span></span>
- <span data-ttu-id="2c14a-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="2c14a-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="2c14a-134">Lapas metadatu modificēšana</span><span class="sxs-lookup"><span data-stu-id="2c14a-134">Modify page metadata</span></span>

<span data-ttu-id="2c14a-135">Lai modificētu lapas metadatus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="2c14a-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="2c14a-136">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="2c14a-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2c14a-137">Navigācijas rūtī kreisajā pusē atlasiet **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="2c14a-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="2c14a-138">Atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="2c14a-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="2c14a-139">Darbību rūtī atlasiet **Izrakstīt**.</span><span class="sxs-lookup"><span data-stu-id="2c14a-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="2c14a-140">Rekvizītu rūts labajā pusē izvērsiet **Noklusējuma metaetiķetes**.</span><span class="sxs-lookup"><span data-stu-id="2c14a-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="2c14a-141">Lai pievienotu jaunu metaetiķeti, atlasiet **Pievienot** un pēc tam laukā ievadiet etiķeti.</span><span class="sxs-lookup"><span data-stu-id="2c14a-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="2c14a-142">Lai noņemtu esošu metaetiķeti, atlasiet miskastes simbolu pa labi no tās.</span><span class="sxs-lookup"><span data-stu-id="2c14a-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="2c14a-143">Atlasiet **Saglabāt** un pēc tam **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="2c14a-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="2c14a-144">Laukā **Komentāri** ievadiet **Atjauninātas metaetiķetes** un pēc tam atlasiet **Labi**,</span><span class="sxs-lookup"><span data-stu-id="2c14a-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="2c14a-145">Atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="2c14a-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="2c14a-146">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="2c14a-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="2c14a-147">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="2c14a-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c14a-148">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2c14a-148">Additional resources</span></span>

[<span data-ttu-id="2c14a-149">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="2c14a-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="2c14a-150">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="2c14a-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2c14a-151">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="2c14a-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2c14a-152">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="2c14a-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2c14a-153">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="2c14a-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="2c14a-154">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="2c14a-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="2c14a-155">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="2c14a-155">Verify page content accessibility</span></span>](verify-accessibility.md)
