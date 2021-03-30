---
title: Galvenes modulis
description: Šajā tēmā aplūkoti galvenes moduļi un aprakstīta lapu galveņu izveide risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 569fb5ac3d30be30044ef9b928ecf1f6dde20aab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211428"
---
# <a name="header-module"></a><span data-ttu-id="19a73-103">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="19a73-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="19a73-104">Šajā tēmā aplūkoti galvenes moduļi un aprakstīta lapu galveņu izveide risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="19a73-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="19a73-105">Pakalpojumā Dynamics 365 Commerce, lapas galvene ir konfigurēta kā lapas fragments, kas ietver galveni, promo reklāmkarogu un sīkfailu piekrišanas moduļus.</span><span class="sxs-lookup"><span data-stu-id="19a73-105">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="19a73-106">Galvenes modulī ir iekļauts vietnes logotips, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē, groza ikonas modulis, vēlmju simbols, pierakstīšanās opcijas un meklēšanas josla.</span><span class="sxs-lookup"><span data-stu-id="19a73-106">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="19a73-107">Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (citiem vārdiem sakot, darbvirsmas ierīcei vai mobilajai ierīcei).</span><span class="sxs-lookup"><span data-stu-id="19a73-107">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="19a73-108">Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).</span><span class="sxs-lookup"><span data-stu-id="19a73-108">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="19a73-109">Attēlā zemāk redzams galvenes moduļa piemērs sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="19a73-109">The following image shows an example of a header module on a home page.</span></span>

![Galvenes moduļa piemērs](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="19a73-111">Galvenes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="19a73-111">Properties of a header module</span></span>

<span data-ttu-id="19a73-112">Galvenes modulis atbalsta šādus rekvizītus: **Logotipa attēls**, **Logotipa saite** un **Mana konta saites**.</span><span class="sxs-lookup"><span data-stu-id="19a73-112">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="19a73-113">Rekvizīti **Logotipa attēls** un **Logotipa saites** tiek izmantoti, lai definētu logotipu lapā.</span><span class="sxs-lookup"><span data-stu-id="19a73-113">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="19a73-114">Plašāku informāciju skatiet sadaļā [Logotipa pievienošana](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="19a73-114">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="19a73-115">Rekvizīts **Mana konta saites** var tikt izmantots, lai definētu konta lapas, kuras vietnes īpašnieks vēlas parādīt tiešās saites virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="19a73-115">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="19a73-116">Galvenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="19a73-116">Modules that are available within a header module</span></span>

<span data-ttu-id="19a73-117">Šādus moduļus var izmantot galvenes modulī.</span><span class="sxs-lookup"><span data-stu-id="19a73-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="19a73-118">**Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites.</span><span class="sxs-lookup"><span data-stu-id="19a73-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="19a73-119">Papildinformāciju skatiet šeit: [Navigācijas izvēlnes modulis](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="19a73-119">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="19a73-120">**Meklēšana** — meklēšanas modulis ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="19a73-120">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="19a73-121">Noklusējuma meklēšanas lapas URL un meklēšanas vaicājuma parametri ir jānorāda sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-121">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="19a73-122">Meklēšanas modulim ir rekvizīti, kas ļauj izlaist meklēšanas pogu vai etiķeti pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="19a73-122">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="19a73-123">Meklēšanas modulis atbalsta arī automātiskās ieteikšanas opcijas, piemēram, preci, atslēgvārdu un kategoriju meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="19a73-123">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="19a73-124">**Groza ikona** — groza ikonu modulis attēlo groza ikonu, kas parāda preču skaitu grozā jebkurā laikā.</span><span class="sxs-lookup"><span data-stu-id="19a73-124">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="19a73-125">Plašāku informāciju skatiet [Groza ikonas modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="19a73-125">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="19a73-126">**Vietas atlasītājs** — vietas atlasītāja modulis ļauj lietotājiem pārlūkot dažādas iepriekšdefinētas vietas, ņemot vērā tirgu, reģionus un lokalizāciju.</span><span class="sxs-lookup"><span data-stu-id="19a73-126">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="19a73-127">Plašāku informāciju skatiet sadaļā [Vietas atlasītāja modulis](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="19a73-127">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="19a73-128">**Veikalu atlasītājs** — veikalu atlasītāja moduli var iekļaut galvenes moduļa veikalu atlasītāja slotā.</span><span class="sxs-lookup"><span data-stu-id="19a73-128">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="19a73-129">Tas ļauj lietotājiem pārlūkot un atrast tuvumā esošos veikalus.</span><span class="sxs-lookup"><span data-stu-id="19a73-129">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="19a73-130">Lietotāji var arī norādīt vēlamo veikalu.</span><span class="sxs-lookup"><span data-stu-id="19a73-130">Users can also specify a preferred store.</span></span> <span data-ttu-id="19a73-131">Šis veikals pēc tam būs redzams galvenē.</span><span class="sxs-lookup"><span data-stu-id="19a73-131">That store will then be shown in the header.</span></span> <span data-ttu-id="19a73-132">Kad veikalu atlasītāja modulis ir iekļauts galvenes modulī, tā rekvizītam **Režīms** jābūt iestatītam uz **Atrast veikalus**.</span><span class="sxs-lookup"><span data-stu-id="19a73-132">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="19a73-133">Plašāku informāciju skatiet sadaļā [Veikalu atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="19a73-133">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="19a73-134">Atbalsts groza ikonas moduļa izmantošanai galvenes moduļos ir pieejams Dynamics 365 Commerce 10.0.11 laidienā.</span><span class="sxs-lookup"><span data-stu-id="19a73-134">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="19a73-135">Atbalsts vietas atlasītāja moduļa izmantošanai galvenes moduļos ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.</span><span class="sxs-lookup"><span data-stu-id="19a73-135">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="19a73-136">Atbalsts veikalu atlasītāja moduļa izmantošanai galvenes moduļos ir pieejams Dynamics 365 Commerce 10.0.15 laidienā.</span><span class="sxs-lookup"><span data-stu-id="19a73-136">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="19a73-137">Lapas galvenes fragmenta izveide</span><span class="sxs-lookup"><span data-stu-id="19a73-137">Create a header fragment for a page</span></span>

<span data-ttu-id="19a73-138">Lai izveidotu galvenes fragmentu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="19a73-138">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="19a73-139">Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.</span><span class="sxs-lookup"><span data-stu-id="19a73-139">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="19a73-140">Dialoglodziņā **Jauns fragments** atlasiet moduli **Konteiners**, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-140">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="19a73-141">Atlasiet slotu **Noklusējuma konteiners** un pēc tam rekvizītu rūtī pa labi iestatiet rekvizītu **Platums** uz **Aizpildīt ekrānu**.</span><span class="sxs-lookup"><span data-stu-id="19a73-141">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="19a73-142">Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="19a73-142">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="19a73-143">Dialoglodziņā **Pievienot moduli** atlasiet moduļus **Sīkdatņu piekrišana**, **Galvene** un **Veicināšanas reklāmkarogs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-143">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="19a73-144">Moduļa **Veicināšanas reklāmkarogs** rekvizītu rūtī atlasiet **Pievienot ziņojumu** un pēc tam atlasiet **Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="19a73-144">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="19a73-145">Dialoglodziņā **Ziņojums** pievienojiet tekstu un saites reklāmas saturam un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-145">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="19a73-146">Moduļa **Sīkdatņu piekrišana** rekvizītu rūtī pievienojiet un konfigurējiet tekstu un saiti uz vietnes konfidencialitātes lapu.</span><span class="sxs-lookup"><span data-stu-id="19a73-146">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="19a73-147">Galvenes moduļa slotā **Navigācijas izvēlne** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="19a73-147">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="19a73-148">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Navigācijas izvēlne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-148">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="19a73-149">Navigācijas izvēlnes moduļa rekvizītu rūts sadaļā **Navigācijas izvēlnes avots** atlasiet **Mazumtirdzniecības serveris**.</span><span class="sxs-lookup"><span data-stu-id="19a73-149">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="19a73-150">Navigācijas izvēlnes moduļa rekvizītu rūts sadaļā **Statiski izvēlnes vienumi** atlasiet **Pievienot izvēlnes vienumu**, un pēc tam atlasiet **Izvēlnes elements**.</span><span class="sxs-lookup"><span data-stu-id="19a73-150">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="19a73-151">Dialoglodziņā **Izvēlnes vienums** sadaļā **Izvēlnes vienuma teksts** ievadiet "Kontaktpersona."</span><span class="sxs-lookup"><span data-stu-id="19a73-151">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="19a73-152">Dialoglodziņā **Izvēlnes vienums** sadaļā **Izvēlnes vienuma saites mērķis** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="19a73-152">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="19a73-153">Dialoglodziņā **Pievienot saiti** atlasiet URL saites "Kontaktpersonas" lapai un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-153">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="19a73-154">Dialoglodziņā **Izvēlnes vienums** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-154">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="19a73-155">Galvenes moduļa slotā **Meklēt** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="19a73-155">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="19a73-156">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēt** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-156">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="19a73-157">Meklēšanas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="19a73-157">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="19a73-158">Galvenes moduļa slotā **Groza ikona** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="19a73-158">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="19a73-159">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Groza ikona** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="19a73-159">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="19a73-160">Groza ikonas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="19a73-160">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="19a73-161">Ja vēlaties, lai groza ikona parāda groza kopsavilkumu (to sauc arī par mini grozu), kad lietotāji uz to norāda, atlasiet **Rādīt mini grozu**.</span><span class="sxs-lookup"><span data-stu-id="19a73-161">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="19a73-162">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="19a73-162">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="19a73-163">Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.</span><span class="sxs-lookup"><span data-stu-id="19a73-163">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="19a73-164">Moduļa **Noklusējuma lapa** slotā **Galvene** pievienojiet jūsu izveidoto kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="19a73-164">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="19a73-165">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="19a73-165">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19a73-166">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="19a73-166">Additional resources</span></span>

[<span data-ttu-id="19a73-167">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="19a73-167">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="19a73-168">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="19a73-168">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="19a73-169">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="19a73-169">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="19a73-170">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="19a73-170">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="19a73-171">Navigācijas izvēlnas modulis</span><span class="sxs-lookup"><span data-stu-id="19a73-171">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="19a73-172">Piekrišana sīkfailiem</span><span class="sxs-lookup"><span data-stu-id="19a73-172">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="19a73-173">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="19a73-173">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="19a73-174">Vietņu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="19a73-174">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="19a73-175">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="19a73-175">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]