---
title: Jaunas vietnes lapas pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot jaunu vietnes lapu programmā Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: b0f1e290526c25aa6e6300c65e24044a325bee53
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413996"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="db184-103">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="db184-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="db184-104">Šajā tēmā ir aprakstīts, kā pievienot jaunu vietnes lapu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="db184-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="db184-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="db184-105">Overview</span></span>

<span data-ttu-id="db184-106">Pēc tam, kad esat izveidojis veidnes un fragmentus jūsu vietnei, nākamais solis ir izveidot lapas, kas tās izmanto.</span><span class="sxs-lookup"><span data-stu-id="db184-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="db184-107">Lai sāktu darbu, jāatlasa veidne vai izkārtojums, lapas nosaukums un lapas vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="db184-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="db184-108">Veidne vai izkārtojums</span><span class="sxs-lookup"><span data-stu-id="db184-108">Template or layout</span></span>

<span data-ttu-id="db184-109">Jaunajai lapai varat izmantot veidni vai izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="db184-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="db184-110">Papildinformāciju skatiet tēmā [Veidņu un izkārtojumu apskats](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="db184-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="db184-111">Lapas nosaukums</span><span class="sxs-lookup"><span data-stu-id="db184-111">Page name</span></span>

<span data-ttu-id="db184-112">Lapas nosaukumam ir jābūt unikālam jūsu lapā.</span><span class="sxs-lookup"><span data-stu-id="db184-112">The page name must be unique to your page.</span></span> <span data-ttu-id="db184-113">Tam jābūt aprakstošam, lai to viegli varētu atrast un citiem cilvēkiem būtu skaidrs, kam paredzēta šī lapa.</span><span class="sxs-lookup"><span data-stu-id="db184-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="db184-114">Uzmanīgi izvēlieties lapas nosaukumu, jo to vēlāk nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="db184-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="db184-115">Lapas URL</span><span class="sxs-lookup"><span data-stu-id="db184-115">Page URL</span></span>

<span data-ttu-id="db184-116">Jums var būt opcija ievadīt vietrādi URL savai jaunai lapai.</span><span class="sxs-lookup"><span data-stu-id="db184-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="db184-117">Veidojot lapu, varat ievadīt virkni, kas tiks izmantota pilnīga vietrāža URL izveidei.</span><span class="sxs-lookup"><span data-stu-id="db184-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="db184-118">Šī virkne ir zināma kā relatīvais vietrādis URL vai URL rinda.</span><span class="sxs-lookup"><span data-stu-id="db184-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="db184-119">Tiek ģenerēts pilnīgs vietrādis URL, pamatojoties uz URL rindu, un tam ir piešķirta jaunā lapa.</span><span class="sxs-lookup"><span data-stu-id="db184-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="db184-120">Varat vēlāk mainīt URL rindu pirms lapas publicēšanas.</span><span class="sxs-lookup"><span data-stu-id="db184-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="db184-121">Papildinformāciju skatiet tēmā [Lapas vietrāža URL izveide](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="db184-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="db184-122">Dynamics 365 Commerce atdala vietrāžus URL un saturu.</span><span class="sxs-lookup"><span data-stu-id="db184-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="db184-123">Citiem vārdiem, var izveidot lapu, kas nav saistīta ar vietrādi URL, un var izveidot vietrādi URL, kas nav saistīts ar lapu.</span><span class="sxs-lookup"><span data-stu-id="db184-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="db184-124">Tāpēc satura pārnešanu var veikt vietrādim URL, tam nav nepieciešama dīkstāve un ir vieglāk pārvaldīt pārvirzīšanu.</span><span class="sxs-lookup"><span data-stu-id="db184-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="db184-125">Jaunas lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="db184-125">Add a new page</span></span>

<span data-ttu-id="db184-126">Lai vietnei pievienotu jaunu vietnes lapu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="db184-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="db184-127">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="db184-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="db184-128">Atlasiet **Jauna lapa**.</span><span class="sxs-lookup"><span data-stu-id="db184-128">Select **New Page**.</span></span>
1. <span data-ttu-id="db184-129">Dialoglodziņā **Jauna lapa** atlasiet veidni un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db184-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="db184-130">Laukā **Lapas nosaukums** ievadiet lapas nosaukumu (piemēram, **Mana jauna lapa**).</span><span class="sxs-lookup"><span data-stu-id="db184-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="db184-131">Laukā **URL** ievadiet virkni (URL rinda), lai pabeigtu vietrādi URL (piemēram, **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="db184-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="db184-132">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db184-132">Select **OK**.</span></span> <span data-ttu-id="db184-133">Tiek atvērts lapas redaktors.</span><span class="sxs-lookup"><span data-stu-id="db184-133">The page editor appears.</span></span> <span data-ttu-id="db184-134">Ievērojiet, ka galvene un kājene tiek automātiski pievienoti lapai, pamatojoties uz jūsu atlasīto veidni.</span><span class="sxs-lookup"><span data-stu-id="db184-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="db184-135">Lapas strukturējumā atlasiet slotu **Galvenais**, atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="db184-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="db184-136">Atlasiet **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db184-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="db184-137">Atlasiet daudzpunktes pogu **Mainīgs konteiners** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="db184-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="db184-138">Atlasiet **Bagātināta satura bloks** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db184-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="db184-139">Atlasiet **Bagātinātā satura bloks**, atlasiet daudzpunktes pogu un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="db184-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="db184-140">Atlasiet **Bagātinātā satura bloka elements** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db184-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="db184-141">Rekvizītu rūtī pa labi atlasiet **Rindkopa** un pēc tam laukā ievadiet **Mans testa teksts**.</span><span class="sxs-lookup"><span data-stu-id="db184-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="db184-142">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="db184-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="db184-143">Laukā **Komentāri** ievadiet **Pievienota jauna lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db184-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="db184-144">Atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="db184-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="db184-145">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="db184-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="db184-146">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="db184-146">Select **Publish**.</span></span>
1. <span data-ttu-id="db184-147">Navigācijas ceļā (atpakaļceļš) atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="db184-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="db184-148">Navigācijas rūtī kreisajā pusē atlasiet **Vietrāži URL**.</span><span class="sxs-lookup"><span data-stu-id="db184-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="db184-149">Sarakstā atrodiet un atlasiet savu vietrādi URL (**mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="db184-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="db184-150">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="db184-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db184-151">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="db184-151">Additional resources</span></span>

[<span data-ttu-id="db184-152">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="db184-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="db184-153">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="db184-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="db184-154">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="db184-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="db184-155">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="db184-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="db184-156">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="db184-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="db184-157">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="db184-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="db184-158">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="db184-158">Verify page content accessibility</span></span>](verify-accessibility.md)
