---
title: Esošās vietnes lapas modificēšana
description: Šajā tēmā ir aprakstīts, kā modificēt esošu vietnes lapu Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 50373d3681e269bf6164b2a425bbafebdd93d64f
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945701"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="0bbfb-103">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="0bbfb-103">Modify an existing site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0bbfb-104">Šajā tēmā ir aprakstīts, kā modificēt esošu vietnes lapu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0bbfb-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="0bbfb-105">Overview</span></span>

<span data-ttu-id="0bbfb-106">Kad ir jāmodificē lapa, pirmā darbība ir tās atvēršana lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="0bbfb-107">Dodieties uz vietni, kas satur jūsu lapu, un tad lapu sarakstā atrodiet lapu, ko vēlaties.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="0bbfb-108">Ja nevarat atrast lapu, varat izmantot autorēšanas rīka bagātīgās meklēšanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="0bbfb-109">Ierakstiet vai nu precīzu lapas nosaukumu, vai arī pirmos tā burtus un pēc tam zvaigznīti (\*).</span><span class="sxs-lookup"><span data-stu-id="0bbfb-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="0bbfb-110">Tiek parādīts filtrēts lapu saraksts.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-110">A filtered list of pages appears.</span></span> <span data-ttu-id="0bbfb-111">Varat izmantot šo sarakstu, lai atrastu vēlamo lapu.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="0bbfb-112">Kad esat atradis pareizo lapu, atlasiet lapas nosaukumu, lai atvērtu lapu lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="0bbfb-113">Ja lapa ir redzama lapas inspektorā, varat to atlasīt un izrakstīt, pirms atverat to lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-113">If your page is visible in the page inspector, you can select it and check it out before you open it in the page editor.</span></span> <span data-ttu-id="0bbfb-114">Šādā veidā varat izrakstīt vairākas lapas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="0bbfb-115">Kad lapa ir atvērta lapas redaktorā, pārliecinieties, ka tā ir izrakstīta jums.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="0bbfb-116">Autorēšanas rīka komandjosla ir dinamiska, kontekstjutīga un statusjutīga.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="0bbfb-117">Tāpēc tā rāda tikai darbības, ko pašlaik varat veikt lapā.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-117">Therefore, it shows only the actions that you can curently perform on the page.</span></span> <span data-ttu-id="0bbfb-118">Piemēram, ja lapa nav izrakstīta jums, pogas **Saglabāt** un **Reģistrēt** komandjoslā neparādās.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-118">For example, if the page isn't checked out to you, the **Save** and **Check in** buttons don't appear on the command bar.</span></span> <span data-ttu-id="0bbfb-119">Loga labajā pusē tiek parādīts arī lapas stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="0bbfb-120">Ja lapa vēl nav izrakstīta jums, komandjoslā atlasiet **Izrakstīt**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-120">If the page isn't already checked out to you, select **Check out** on the command bar.</span></span> <span data-ttu-id="0bbfb-121">Komandjosla mainās, lai atspoguļotu lapas jauno stāvokli.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="0bbfb-122">Jūs saņemsiet arī paziņojumu par to, ka lapa tika izrakstīta jums.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="0bbfb-123">Nākamā darbība ir veikt savas faktiskās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="0bbfb-124">Bieži, lai atrastu un atlasītu moduli, ko vēlaties mainīt, izmantosiet lapas strukturējuma koku kreisajā pusē, un pēc tam veiksiet izmaiņas rekvizītu rūtī labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="0bbfb-125">Tomēr dažkārt izmaiņas var ietvert modeļu vai fragmentu pievienošanu vai noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="0bbfb-126">Lai pievienotu fragmentu vai moduli, izmantojiet lapas strukturējuma koku, lai atrastu slotu, kuram vēlaties pievienot moduli vai fragmentu, un pēc tam atlasiet daudzpunktes pogu (**...**) šim slotam.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="0bbfb-127">Tiek parādīta izvēlne, kurā ir iekļautas komandas moduļa vai fragmenta pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="0bbfb-128">Lai noņemtu moduli vai fragmentu, atrodiet un atlasiet to lapas strukturējuma kokā, atlasiet daudzpunktes pogu un pēc tam atlasiet komandu, lai dzēstu moduli vai fragmentu.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="0bbfb-129">Varat arī apskatīt un rediģēt rekvizītus jebkuram modulim, kas ir redzams priekšskatījumā "redzat to, ko iegūstat" (WYSIWYG), atlasot to tieši.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="0bbfb-130">Kad esat beidzis veikt izmaiņas un priekšskatījis to sekas, lapa ir jāreģistrē, komandjoslā atlasot **Reģistrēt**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Check in** on the command bar.</span></span> 

<span data-ttu-id="0bbfb-131">Lai nekavējoties publicētu izmaiņas, komandjoslā atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="0bbfb-132">Jūsu modificētās lapas pēdējā reģistrētā versija ir publicēta un kļūst pieejama ārējiem lietotājiem, kuri skata jūsu vietni.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="0bbfb-133">Piemērs: video mainīšana sākumlapā</span><span class="sxs-lookup"><span data-stu-id="0bbfb-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="0bbfb-134">Tālāk minētajā piemērā ir parādīts, kā modificēt sākumlapu, mainot videoklipu, kas parādās video atskaņotāja modulī.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="0bbfb-135">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="0bbfb-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0bbfb-136">Navigācijas rūtī kreisajā pusē atlasiet **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="0bbfb-137">Atrodiet un atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="0bbfb-138">Komandjoslā atlasiet **Izrakstīt**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-138">On the command bar, select **Check Out**.</span></span>
1. <span data-ttu-id="0bbfb-139">Lapas strukturējumā atlasiet slotu **Galvenais**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="0bbfb-140">Zem slota **Galvenais** izvērsiet visus mainīgos konteinera moduļus.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="0bbfb-141">Atrodiet un atlasiet video atskaņotāja moduli.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="0bbfb-142">Rekvizītu rūts labajā pusē atlasiet rekvizītu **Video**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="0bbfb-143">Tiek parādīts līdzekļa atlasītājs.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-143">The asset picker appears.</span></span>
1. <span data-ttu-id="0bbfb-144">Līdzekļu atlasītājā atlasiet pieejamo video līdzekli vai atlasiet **Augšupielādēt jaunu līdzekli**, lai augšupielādētu jaunu video līdzekli.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="0bbfb-145">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-145">Select **OK**.</span></span>
1. <span data-ttu-id="0bbfb-146">Atlasiet **Saglabāt** un pēc tam **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-146">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="0bbfb-147">Laukā **Komentāri** ievadiet **Mainīts video** un pēc tam atlasiet **Labi**,</span><span class="sxs-lookup"><span data-stu-id="0bbfb-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="0bbfb-148">Atlasiet **Priekšskatījums**, lai priekšskatītu atjaunināto lapu.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="0bbfb-149">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="0bbfb-150">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="0bbfb-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bbfb-151">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0bbfb-151">Additional resources</span></span>

[<span data-ttu-id="0bbfb-152">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="0bbfb-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0bbfb-153">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="0bbfb-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0bbfb-154">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="0bbfb-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0bbfb-155">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="0bbfb-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0bbfb-156">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="0bbfb-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0bbfb-157">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="0bbfb-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="0bbfb-158">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="0bbfb-158">Verify page content accessibility</span></span>](verify-accessibility.md)
