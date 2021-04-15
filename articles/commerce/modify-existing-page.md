---
title: Esošās vietnes lapas modificēšana
description: Šajā tēmā ir aprakstīts, kā modificēt esošu vietnes lapu programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803733"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="0513e-103">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="0513e-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0513e-104">Šajā tēmā ir aprakstīts, kā modificēt esošu vietnes lapu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0513e-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0513e-105">Kad ir jāmodificē lapa, pirmā darbība ir tās atvēršana lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0513e-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="0513e-106">Dodieties uz vietni, kas satur jūsu lapu, un tad lapu sarakstā atrodiet lapu, ko vēlaties.</span><span class="sxs-lookup"><span data-stu-id="0513e-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="0513e-107">Ja nevarat atrast lapu, varat izmantot autorēšanas rīka bagātīgās meklēšanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="0513e-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="0513e-108">Ierakstiet vai nu precīzu lapas nosaukumu, vai arī pirmos tā burtus un pēc tam zvaigznīti (\*).</span><span class="sxs-lookup"><span data-stu-id="0513e-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="0513e-109">Tiek parādīts filtrēts lapu saraksts.</span><span class="sxs-lookup"><span data-stu-id="0513e-109">A filtered list of pages appears.</span></span> <span data-ttu-id="0513e-110">Varat izmantot šo sarakstu, lai atrastu vēlamo lapu.</span><span class="sxs-lookup"><span data-stu-id="0513e-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="0513e-111">Kad esat atradis pareizo lapu, atlasiet lapas nosaukumu, lai atvērtu lapu lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0513e-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="0513e-112">Ja lapa ir redzama lapas inspektorā, varat atlasīt **Rediģēt** un pārbaudīt lapu, pirms atverat to lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0513e-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="0513e-113">Šādā veidā varat izrakstīt vairākas lapas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="0513e-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="0513e-114">Kad lapa ir atvērta lapas redaktorā, pārliecinieties, ka tā ir izrakstīta jums.</span><span class="sxs-lookup"><span data-stu-id="0513e-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="0513e-115">Autorēšanas rīka komandjosla ir dinamiska, kontekstjutīga un statusjutīga.</span><span class="sxs-lookup"><span data-stu-id="0513e-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="0513e-116">Tāpēc tā rāda tikai darbības, ko pašlaik varat veikt lapā.</span><span class="sxs-lookup"><span data-stu-id="0513e-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="0513e-117">Piemēram, ja lapa nav izrakstīta jums, pogas **Saglabāt** un **Pabeigt rediģēšanu** komandjoslā neparādās.</span><span class="sxs-lookup"><span data-stu-id="0513e-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="0513e-118">Loga labajā pusē tiek parādīts arī lapas stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="0513e-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="0513e-119">Ja lapa vēl nav izrakstīta jums, komandjoslā atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0513e-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="0513e-120">Komandjosla mainās, lai atspoguļotu lapas jauno stāvokli.</span><span class="sxs-lookup"><span data-stu-id="0513e-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="0513e-121">Jūs saņemsiet arī paziņojumu par to, ka lapa tika izrakstīta jums.</span><span class="sxs-lookup"><span data-stu-id="0513e-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="0513e-122">Nākamā darbība ir veikt savas faktiskās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0513e-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="0513e-123">Bieži, lai atrastu un atlasītu moduli, ko vēlaties mainīt, izmantosiet lapas strukturējuma koku kreisajā pusē, un pēc tam veiksiet izmaiņas rekvizītu rūtī labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="0513e-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="0513e-124">Tomēr dažkārt izmaiņas var ietvert modeļu vai fragmentu pievienošanu vai noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="0513e-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="0513e-125">Lai pievienotu fragmentu vai moduli, izmantojiet lapas strukturējuma koku, lai atrastu slotu, kuram vēlaties pievienot moduli vai fragmentu, un pēc tam atlasiet daudzpunktes pogu (**...**) šim slotam.</span><span class="sxs-lookup"><span data-stu-id="0513e-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="0513e-126">Tiek parādīta izvēlne, kurā ir iekļautas komandas moduļa vai fragmenta pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="0513e-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="0513e-127">Lai noņemtu moduli vai fragmentu, atrodiet un atlasiet to lapas strukturējuma kokā, atlasiet daudzpunktes pogu un pēc tam atlasiet komandu, lai dzēstu moduli vai fragmentu.</span><span class="sxs-lookup"><span data-stu-id="0513e-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="0513e-128">Varat arī apskatīt un rediģēt rekvizītus jebkuram modulim, kas ir redzams vizuālā lapu veidotāja priekšskatījumā, atlasot to tieši.</span><span class="sxs-lookup"><span data-stu-id="0513e-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="0513e-129">Kad esat beidzis veikt izmaiņas un priekšskatījis to sekas, lapa ir jāreģistrē, komandjoslā atlasot **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="0513e-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="0513e-130">Lai nekavējoties publicētu izmaiņas, komandjoslā atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="0513e-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="0513e-131">Jūsu modificētās lapas pēdējā reģistrētā versija ir publicēta un kļūst pieejama ārējiem lietotājiem, kuri skata jūsu vietni.</span><span class="sxs-lookup"><span data-stu-id="0513e-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="0513e-132">Piemērs: video mainīšana sākumlapā</span><span class="sxs-lookup"><span data-stu-id="0513e-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="0513e-133">Tālāk minētajā piemērā ir parādīts, kā modificēt sākumlapu, mainot videoklipu, kas parādās video atskaņotāja modulī.</span><span class="sxs-lookup"><span data-stu-id="0513e-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="0513e-134">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="0513e-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0513e-135">Navigācijas rūtī kreisajā pusē atlasiet **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="0513e-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="0513e-136">Atrodiet un atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="0513e-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="0513e-137">Komandjoslā atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0513e-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="0513e-138">Lapas strukturējumā atlasiet slotu **Galvenais**.</span><span class="sxs-lookup"><span data-stu-id="0513e-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="0513e-139">Zem slota **Galvenais** izvērsiet visus mainīgos konteinera moduļus.</span><span class="sxs-lookup"><span data-stu-id="0513e-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="0513e-140">Atrodiet un atlasiet video atskaņotāja moduli.</span><span class="sxs-lookup"><span data-stu-id="0513e-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="0513e-141">Rekvizītu rūts labajā pusē atlasiet rekvizītu **Video**.</span><span class="sxs-lookup"><span data-stu-id="0513e-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="0513e-142">Tiek parādīts līdzekļa atlasītājs.</span><span class="sxs-lookup"><span data-stu-id="0513e-142">The asset picker appears.</span></span>
1. <span data-ttu-id="0513e-143">Līdzekļu atlasītājā atlasiet pieejamo video līdzekli vai atlasiet **Augšupielādēt jaunu līdzekli**, lai augšupielādētu jaunu video līdzekli.</span><span class="sxs-lookup"><span data-stu-id="0513e-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="0513e-144">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0513e-144">Select **OK**.</span></span>
1. <span data-ttu-id="0513e-145">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="0513e-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0513e-146">Laukā **Komentāri** ievadiet **Mainīts video** un pēc tam atlasiet **Labi**,</span><span class="sxs-lookup"><span data-stu-id="0513e-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="0513e-147">Atlasiet **Priekšskatījums**, lai priekšskatītu atjaunināto lapu.</span><span class="sxs-lookup"><span data-stu-id="0513e-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="0513e-148">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="0513e-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="0513e-149">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="0513e-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0513e-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0513e-150">Additional resources</span></span>

[<span data-ttu-id="0513e-151">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="0513e-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0513e-152">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="0513e-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0513e-153">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="0513e-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0513e-154">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="0513e-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0513e-155">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="0513e-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0513e-156">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="0513e-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="0513e-157">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="0513e-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="0513e-158">Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem</span><span class="sxs-lookup"><span data-stu-id="0513e-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
