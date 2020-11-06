---
title: Galvenes modulis
description: Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52069af5ca2211473d4a096ad850b5be1290bba1
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055454"
---
# <a name="header-module"></a><span data-ttu-id="96fe0-103">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="96fe0-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96fe0-104">Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="96fe0-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="96fe0-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="96fe0-105">Overview</span></span>

<span data-ttu-id="96fe0-106">Pakalpojumā Dynamics 365 Commerce, lapas galvene ir konfigurēta kā lapas fragments, kas ietver galveni, promo reklāmkarogu un sīkfailu piekrišanas moduļus.</span><span class="sxs-lookup"><span data-stu-id="96fe0-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="96fe0-107">Galvenes modulī ir iekļauts vietnes logotips, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē, groza ikonas modulis, vēlmju simbols, pierakstīšanās opcijas un meklēšanas josla.</span><span class="sxs-lookup"><span data-stu-id="96fe0-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="96fe0-108">Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (citiem vārdiem sakot, darbvirsmas ierīcei vai mobilajai ierīcei).</span><span class="sxs-lookup"><span data-stu-id="96fe0-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="96fe0-109">Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni* ).</span><span class="sxs-lookup"><span data-stu-id="96fe0-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu* ).</span></span>

<span data-ttu-id="96fe0-110">Attēlā zemāk redzams galvenes moduļa piemērs sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="96fe0-110">The following image shows an example of a header module on a home page.</span></span>

![Galvenes moduļa piemērs](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="96fe0-112">Galvenes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="96fe0-112">Properties of a header module</span></span>

<span data-ttu-id="96fe0-113">Galvenes modulis atbalsta šādus rekvizītus: **Logotipa attēls** , **Logotipa saite** un **Mana konta saites**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-113">A header module supports **Logo image** , **Logo link** , and **My account links** properties.</span></span> 

<span data-ttu-id="96fe0-114">Rekvizīti **Logotipa attēls** un **Logotipa saites** tiek izmantoti, lai definētu logotipu lapā.</span><span class="sxs-lookup"><span data-stu-id="96fe0-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="96fe0-115">Plašāku informāciju skatiet sadaļā [Logotipa pievienošana](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="96fe0-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="96fe0-116">Rekvizīts **Mana konta saites** var tikt izmantots, lai definētu konta lapas, kuras vietnes īpašnieks vēlas parādīt tiešās saites virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="96fe0-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="96fe0-117">Galvenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="96fe0-117">Modules that are available within a header module</span></span>

<span data-ttu-id="96fe0-118">Šādus moduļus var izmantot galvenes modulī.</span><span class="sxs-lookup"><span data-stu-id="96fe0-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="96fe0-119">**Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites.</span><span class="sxs-lookup"><span data-stu-id="96fe0-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="96fe0-120">Papildinformāciju skatiet šeit: [Navigācijas izvēlnes modulis](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="96fe0-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="96fe0-121">**Meklēšana** — meklēšanas modulis ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="96fe0-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="96fe0-122">Noklusējuma meklēšanas lapas URL un meklēšanas vaicājuma parametri ir jānorāda sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="96fe0-123">Meklēšanas modulim ir rekvizīti, kas ļauj izlaist meklēšanas pogu vai etiķeti pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="96fe0-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="96fe0-124">Meklēšanas modulis atbalsta arī automātiskās ieteikšanas opcijas, piemēram, preci, atslēgvārdu un kategoriju meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="96fe0-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="96fe0-125">**Groza ikona** — groza ikonu modulis attēlo groza ikonu, kas parāda preču skaitu grozā jebkurā laikā.</span><span class="sxs-lookup"><span data-stu-id="96fe0-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="96fe0-126">Plašāku informāciju skatiet [Groza ikonas modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="96fe0-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="96fe0-127">**Vietas atlasītājs** — vietas atlasītāja modulis ļauj lietotājiem pārlūkot dažādas iepriekšdefinētas vietas, ņemot vērā tirgu, reģionus un lokalizāciju.</span><span class="sxs-lookup"><span data-stu-id="96fe0-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="96fe0-128">Plašāku informāciju skatiet sadaļā [Vietas atlasītāja modulis](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="96fe0-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="96fe0-129">**Veikalu atlasītājs** — veikalu atlasītāja moduli var iekļaut galvenes moduļa veikalu atlasītāja slotā.</span><span class="sxs-lookup"><span data-stu-id="96fe0-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="96fe0-130">Tas ļauj lietotājiem pārlūkot un atrast tuvumā esošos veikalus.</span><span class="sxs-lookup"><span data-stu-id="96fe0-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="96fe0-131">Lietotāji var arī norādīt vēlamo veikalu.</span><span class="sxs-lookup"><span data-stu-id="96fe0-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="96fe0-132">Šis veikals pēc tam būs redzams galvenē.</span><span class="sxs-lookup"><span data-stu-id="96fe0-132">That store will then be shown in the header.</span></span> <span data-ttu-id="96fe0-133">Kad veikalu atlasītāja modulis ir iekļauts galvenes modulī, tā rekvizītam **Režīms** jābūt iestatītam uz **Atrast veikalus**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="96fe0-134">Plašāku informāciju skatiet sadaļā [Veikalu atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="96fe0-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="96fe0-135">Atbalsts groza ikonas moduļa izmantošanai galvenes moduļos ir pieejams Dynamics 365 Commerce 10.0.11 laidienā.</span><span class="sxs-lookup"><span data-stu-id="96fe0-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="96fe0-136">Atbalsts vietas atlasītāja moduļa izmantošanai galvenes moduļos ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.</span><span class="sxs-lookup"><span data-stu-id="96fe0-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="96fe0-137">Atbalsts veikalu atlasītāja moduļa izmantošanai galvenes moduļos ir pieejams Dynamics 365 Commerce 10.0.15 laidienā.</span><span class="sxs-lookup"><span data-stu-id="96fe0-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="96fe0-138">Lapas galvenes fragmenta izveide</span><span class="sxs-lookup"><span data-stu-id="96fe0-138">Create a header fragment for a page</span></span>

<span data-ttu-id="96fe0-139">Lai izveidotu galvenes fragmentu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="96fe0-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="96fe0-140">Dodieties uz **Fragmenti** un atlasiet **Jauns** , lai izveidotu jaunu fragmentu.</span><span class="sxs-lookup"><span data-stu-id="96fe0-140">Go to **Fragments** , and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="96fe0-141">Dialoglodziņā **Jauns fragments** atlasiet moduli **Konteiners** , ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="96fe0-142">Atlasiet slotu **Noklusējuma konteiners** un pēc tam rekvizītu rūtī pa labi iestatiet rekvizītu **Platums** uz **Aizpildīt ekrānu**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="96fe0-143">Slotā **Noklusējuma konteiners** atlasiet daudzpunkti ( **...** ) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-143">In the **Default container** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="96fe0-144">Dialoglodziņā **Pievienot moduli** atlasiet moduļus **Sīkdatņu piekrišana** , **Galvene** un **Veicināšanas reklāmkarogs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-144">In the **Add Module** dialog box, select the **Cookie consent** , **Header** , and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="96fe0-145">Moduļa **Veicināšanas reklāmkarogs** rekvizītu rūtī atlasiet **Pievienot ziņojumu** un pēc tam atlasiet **Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-145">In the properties pane of the **Promo banner** module, select **Add Message** , and then select **Message**.</span></span>
1. <span data-ttu-id="96fe0-146">Dialoglodziņā **Ziņojums** pievienojiet tekstu un saites reklāmas saturam un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="96fe0-147">Moduļa **Sīkdatņu piekrišana** rekvizītu rūtī pievienojiet un konfigurējiet tekstu un saiti uz vietnes konfidencialitātes lapu.</span><span class="sxs-lookup"><span data-stu-id="96fe0-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="96fe0-148">Galvenes moduļa slotā **Navigācijas izvēlne** slotā atlasiet daudzpunktes pogu ( **...** ) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-148">In the **Navigation menu** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="96fe0-149">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Navigācijas izvēlne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="96fe0-150">Navigācijas izvēlnes moduļa rekvizītu rūts sadaļā **Navigācijas izvēlnes avots** atlasiet **Mazumtirdzniecības serveris**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-150">In the property pane for the navigation menu module, under **Source for navigation menu** , select **Retail Server**.</span></span>
1. <span data-ttu-id="96fe0-151">Navigācijas izvēlnes moduļa rekvizītu rūts sadaļā **Statiski izvēlnes vienumi** atlasiet **Pievienot izvēlnes vienumu** , un pēc tam atlasiet **Izvēlnes elements**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-151">In the property pane for the navigation menu module, under **Static menu items** , select **Add Menu item** , and then select **Menu item**.</span></span> 
1. <span data-ttu-id="96fe0-152">Dialoglodziņā **Izvēlnes vienums** sadaļā **Izvēlnes vienuma teksts** ievadiet "Kontaktpersona."</span><span class="sxs-lookup"><span data-stu-id="96fe0-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="96fe0-153">Dialoglodziņā **Izvēlnes vienums** sadaļā **Izvēlnes vienuma saites mērķis** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="96fe0-154">Dialoglodziņā **Pievienot saiti** atlasiet URL saites "Kontaktpersonas" lapai un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="96fe0-155">Dialoglodziņā **Izvēlnes vienums** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="96fe0-156">Galvenes moduļa slotā **Meklēt** slotā atlasiet daudzpunktes pogu ( **...** ) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-156">In the **Search** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="96fe0-157">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēt** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="96fe0-158">Meklēšanas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="96fe0-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="96fe0-159">Galvenes moduļa slotā **Groza ikona** slotā atlasiet daudzpunktes pogu ( **...** ) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-159">In the **Cart icon** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="96fe0-160">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Groza ikona** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="96fe0-161">Groza ikonas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="96fe0-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="96fe0-162">Ja vēlaties, lai groza ikona parāda groza kopsavilkumu (to sauc arī par mini grozu), kad lietotāji uz to norāda, atlasiet **Rādīt mini grozu**.</span><span class="sxs-lookup"><span data-stu-id="96fe0-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="96fe0-163">Atlasiet **Saglabāt** , atlasiet **Pabeigt rediģēšanu** , lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt** , lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="96fe0-163">Select **Save** , select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="96fe0-164">Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.</span><span class="sxs-lookup"><span data-stu-id="96fe0-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="96fe0-165">Moduļa **Noklusējuma lapa** slotā **Galvene** pievienojiet jūsu izveidoto kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="96fe0-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="96fe0-166">Atlasiet **Saglabāt** , atlasiet **Pabeigt rediģēšanu** , lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt** , lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="96fe0-166">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96fe0-167">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="96fe0-167">Additional resources</span></span>

[<span data-ttu-id="96fe0-168">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="96fe0-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="96fe0-169">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="96fe0-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="96fe0-170">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="96fe0-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="96fe0-171">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="96fe0-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="96fe0-172">Navigācijas izvēlnas modulis</span><span class="sxs-lookup"><span data-stu-id="96fe0-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="96fe0-173">Piekrišana sīkfailiem</span><span class="sxs-lookup"><span data-stu-id="96fe0-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="96fe0-174">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="96fe0-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="96fe0-175">Vietņu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="96fe0-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="96fe0-176">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="96fe0-176">Store selector module</span></span>](store-selector.md)
