---
title: Jaunas vietnes lapas pievienošana
description: Šajā tēmā aprakstīts, kā pievienot jaunu vietnes lapu risinājumā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797555"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="20b24-103">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="20b24-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="20b24-104">Šajā tēmā aprakstīts, kā pievienot jaunu vietnes lapu risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="20b24-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="20b24-105">Pēc tam, kad esat izveidojis veidnes un fragmentus jūsu vietnei, nākamais solis ir izveidot lapas, kas tās izmanto.</span><span class="sxs-lookup"><span data-stu-id="20b24-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="20b24-106">Lai sāktu darbu, jāatlasa veidne vai izkārtojums, lapas nosaukums un lapas vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="20b24-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="20b24-107">Veidne vai izkārtojums</span><span class="sxs-lookup"><span data-stu-id="20b24-107">Template or layout</span></span>

<span data-ttu-id="20b24-108">Jaunajai lapai varat izmantot veidni vai izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="20b24-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="20b24-109">Papildinformāciju skatiet tēmā [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="20b24-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="20b24-110">Lapas nosaukums</span><span class="sxs-lookup"><span data-stu-id="20b24-110">Page name</span></span>

<span data-ttu-id="20b24-111">Lapas nosaukumam ir jābūt unikālam jūsu lapā.</span><span class="sxs-lookup"><span data-stu-id="20b24-111">The page name must be unique to your page.</span></span> <span data-ttu-id="20b24-112">Tam jābūt aprakstošam, lai to viegli varētu atrast un citiem cilvēkiem būtu skaidrs, kam paredzēta šī lapa.</span><span class="sxs-lookup"><span data-stu-id="20b24-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="20b24-113">Uzmanīgi izvēlieties lapas nosaukumu, jo to vēlāk nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="20b24-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="20b24-114">Lapas URL</span><span class="sxs-lookup"><span data-stu-id="20b24-114">Page URL</span></span>

<span data-ttu-id="20b24-115">Jums var būt opcija ievadīt vietrādi URL savai jaunai lapai.</span><span class="sxs-lookup"><span data-stu-id="20b24-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="20b24-116">Veidojot lapu, varat ievadīt virkni, kas tiks izmantota pilnīga vietrāža URL izveidei.</span><span class="sxs-lookup"><span data-stu-id="20b24-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="20b24-117">Šī virkne ir zināma kā relatīvais vietrādis URL vai URL rinda.</span><span class="sxs-lookup"><span data-stu-id="20b24-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="20b24-118">Tiek ģenerēts pilnīgs vietrādis URL, pamatojoties uz URL rindu, un tam ir piešķirta jaunā lapa.</span><span class="sxs-lookup"><span data-stu-id="20b24-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="20b24-119">Varat vēlāk mainīt URL rindu pirms lapas publicēšanas.</span><span class="sxs-lookup"><span data-stu-id="20b24-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="20b24-120">Papildinformāciju skatiet tēmā [Lapas vietrāža URL izveide](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="20b24-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="20b24-121">Dynamics 365 Commerce atdala vietrāžus URL un saturu.</span><span class="sxs-lookup"><span data-stu-id="20b24-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="20b24-122">Citiem vārdiem, var izveidot lapu, kas nav saistīta ar vietrādi URL, un var izveidot vietrādi URL, kas nav saistīts ar lapu.</span><span class="sxs-lookup"><span data-stu-id="20b24-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="20b24-123">Tāpēc satura pārnešanu var veikt vietrādim URL, tam nav nepieciešama dīkstāve un ir vieglāk pārvaldīt pārvirzīšanu.</span><span class="sxs-lookup"><span data-stu-id="20b24-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="20b24-124">Jaunas lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="20b24-124">Add a new page</span></span>

<span data-ttu-id="20b24-125">Lai vietnei pievienotu jaunu vietnes lapu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="20b24-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="20b24-126">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="20b24-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="20b24-127">Atlasiet **Jauna lapa**.</span><span class="sxs-lookup"><span data-stu-id="20b24-127">Select **New Page**.</span></span>
1. <span data-ttu-id="20b24-128">Dialoglodziņā **Jauna lapa** atlasiet veidni un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="20b24-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="20b24-129">Laukā **Lapas nosaukums** ievadiet lapas nosaukumu (piemēram, **Mana jauna lapa**).</span><span class="sxs-lookup"><span data-stu-id="20b24-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="20b24-130">Laukā **URL** ievadiet virkni (URL rinda), lai pabeigtu vietrādi URL (piemēram, **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="20b24-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="20b24-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="20b24-131">Select **OK**.</span></span> <span data-ttu-id="20b24-132">Tiek atvērts lapas redaktors.</span><span class="sxs-lookup"><span data-stu-id="20b24-132">The page editor appears.</span></span> <span data-ttu-id="20b24-133">Ievērojiet, ka galvene un kājene tiek automātiski pievienoti lapai, pamatojoties uz jūsu atlasīto veidni.</span><span class="sxs-lookup"><span data-stu-id="20b24-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="20b24-134">Lapas strukturējumā atlasiet slotu **Galvenais**, atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="20b24-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="20b24-135">Atlasiet **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="20b24-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="20b24-136">Atlasiet daudzpunktes pogu **Mainīgs konteiners** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="20b24-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="20b24-137">Atlasiet **Bagātināta satura bloks** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="20b24-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="20b24-138">Atlasiet **Bagātinātā satura bloks**, atlasiet daudzpunktes pogu un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="20b24-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="20b24-139">Atlasiet **Bagātinātā satura bloka elements** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="20b24-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="20b24-140">Rekvizītu rūtī pa labi atlasiet **Rindkopa** un pēc tam laukā ievadiet **Mans testa teksts**.</span><span class="sxs-lookup"><span data-stu-id="20b24-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="20b24-141">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="20b24-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="20b24-142">Laukā **Komentāri** ievadiet **Pievienota jauna lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="20b24-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="20b24-143">Atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="20b24-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="20b24-144">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="20b24-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="20b24-145">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="20b24-145">Select **Publish**.</span></span>
1. <span data-ttu-id="20b24-146">Navigācijas ceļā (atpakaļceļš) atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="20b24-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="20b24-147">Navigācijas rūtī kreisajā pusē atlasiet **Vietrāži URL**.</span><span class="sxs-lookup"><span data-stu-id="20b24-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="20b24-148">Sarakstā atrodiet un atlasiet savu vietrādi URL (**mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="20b24-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="20b24-149">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="20b24-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20b24-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="20b24-150">Additional resources</span></span>

[<span data-ttu-id="20b24-151">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="20b24-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="20b24-152">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="20b24-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="20b24-153">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="20b24-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="20b24-154">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="20b24-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="20b24-155">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="20b24-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="20b24-156">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="20b24-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="20b24-157">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="20b24-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="20b24-158">Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem</span><span class="sxs-lookup"><span data-stu-id="20b24-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
