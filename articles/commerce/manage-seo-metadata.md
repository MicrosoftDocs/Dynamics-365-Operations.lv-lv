---
title: SEO metadatu pārvaldība
description: Šajā tēmā ir aprakstīts, kā pārvaldīt meklēšanas programmas optimizācijas (SEO) metadatus Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794215"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="0459c-103">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="0459c-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0459c-104">Šajā tēmā ir aprakstīts, kā pārvaldīt meklēšanas programmas optimizācijas (SEO) metadatus Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0459c-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0459c-105">SEO metadatus vietnei var pārvaldīt, izmantojot vietnes kartes un lapas metadatus.</span><span class="sxs-lookup"><span data-stu-id="0459c-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="0459c-106">Vietnes kartes</span><span class="sxs-lookup"><span data-stu-id="0459c-106">Site maps</span></span>

<span data-ttu-id="0459c-107">Vietnes karte ir jūsu tīmekļa vietnes lapu mašīnlasāms saraksts XML formātā.</span><span class="sxs-lookup"><span data-stu-id="0459c-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="0459c-108">Tas paredzēts meklēšanas programmu lietošanai, lai tās varētu nodrošināt labākus meklēšanas rezultātus no jūsu vietnes.</span><span class="sxs-lookup"><span data-stu-id="0459c-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="0459c-109">Meklētājprogrammas var manuāli uzņemt vietnes kartes vai tās var publicēt robots.txt failā.</span><span class="sxs-lookup"><span data-stu-id="0459c-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="0459c-110">Dynamics 365 Commerce atbalsta automātisku vietnes karšu ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="0459c-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="0459c-111">Kad lapas tiek vai netiek publicētas, vietas kartes tiek automātiski atjauninātas.</span><span class="sxs-lookup"><span data-stu-id="0459c-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="0459c-112">Vietnes kartes ģenerēšanas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="0459c-112">Turn on site map generation</span></span>

1. <span data-ttu-id="0459c-113">Pierakstieties autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="0459c-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="0459c-114">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="0459c-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0459c-115">Navigācijas rūtī kreisajā pusē atlasiet **Lapas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="0459c-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="0459c-116">Pārliecinieties, vai ir ieslēgta opcija **Vietnes lapas iespējotas**.</span><span class="sxs-lookup"><span data-stu-id="0459c-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="0459c-117">Lapas metadati</span><span class="sxs-lookup"><span data-stu-id="0459c-117">Page metadata</span></span>

<span data-ttu-id="0459c-118">Dynamics 365 Commerce ļauj pārvaldīt SEO metadatus atsevišķām lapām.</span><span class="sxs-lookup"><span data-stu-id="0459c-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="0459c-119">Varat apskatīt un modificēt šo informāciju lapas konteinera sadaļā **SEO rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="0459c-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="0459c-120">Pašlaik tiek atbalstīti tālāk minētie SEO metadatu rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="0459c-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="0459c-121">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="0459c-121">Title</span></span>
- <span data-ttu-id="0459c-122">Apraksts</span><span class="sxs-lookup"><span data-stu-id="0459c-122">Description</span></span>
- <span data-ttu-id="0459c-123">SEO atslēgvārdi</span><span class="sxs-lookup"><span data-stu-id="0459c-123">SEO keywords</span></span>
- <span data-ttu-id="0459c-124">Aria etiķetes</span><span class="sxs-lookup"><span data-stu-id="0459c-124">Aria labels</span></span>
- <span data-ttu-id="0459c-125">noindex</span><span class="sxs-lookup"><span data-stu-id="0459c-125">noindex</span></span>
- <span data-ttu-id="0459c-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="0459c-126">nofollow</span></span>
- <span data-ttu-id="0459c-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="0459c-127">noarchive</span></span>
- <span data-ttu-id="0459c-128">nocache</span><span class="sxs-lookup"><span data-stu-id="0459c-128">nocache</span></span>
- <span data-ttu-id="0459c-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="0459c-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="0459c-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="0459c-130">nosnippet</span></span>
- <span data-ttu-id="0459c-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="0459c-131">noImageIndex</span></span>
- <span data-ttu-id="0459c-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="0459c-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="0459c-133">Lapas metadatu modificēšana</span><span class="sxs-lookup"><span data-stu-id="0459c-133">Modify page metadata</span></span>

<span data-ttu-id="0459c-134">Lai modificētu lapas metadatus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="0459c-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="0459c-135">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="0459c-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0459c-136">Navigācijas rūtī kreisajā pusē atlasiet **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="0459c-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="0459c-137">Atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0459c-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="0459c-138">Komandjoslā atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0459c-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="0459c-139">Rekvizītu rūts labajā pusē izvērsiet **Noklusējuma metaetiķetes**.</span><span class="sxs-lookup"><span data-stu-id="0459c-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="0459c-140">Lai pievienotu jaunu metaetiķeti, atlasiet **Pievienot** un pēc tam laukā ievadiet etiķeti.</span><span class="sxs-lookup"><span data-stu-id="0459c-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="0459c-141">Lai noņemtu esošu metaetiķeti, atlasiet miskastes simbolu pa labi no tās.</span><span class="sxs-lookup"><span data-stu-id="0459c-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="0459c-142">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="0459c-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0459c-143">Laukā **Komentāri** ievadiet **Atjauninātas metaetiķetes** un pēc tam atlasiet **Labi**,</span><span class="sxs-lookup"><span data-stu-id="0459c-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="0459c-144">Atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="0459c-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="0459c-145">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="0459c-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="0459c-146">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="0459c-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0459c-147">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0459c-147">Additional resources</span></span>

[<span data-ttu-id="0459c-148">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="0459c-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="0459c-149">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="0459c-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0459c-150">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="0459c-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0459c-151">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="0459c-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0459c-152">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="0459c-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0459c-153">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="0459c-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="0459c-154">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="0459c-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="0459c-155">Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem</span><span class="sxs-lookup"><span data-stu-id="0459c-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
