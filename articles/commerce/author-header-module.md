---
title: Galvenes modulis
description: Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 99457b2c98eae0ddd898f852630d690140a5a4c5
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817014"
---
# <a name="header-module"></a><span data-ttu-id="2c512-103">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="2c512-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2c512-104">Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c512-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2c512-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="2c512-105">Overview</span></span>

<span data-ttu-id="2c512-106">Pakalpojumā Dynamics 365 Commerce, lapas galvene ir konfigurēta kā lapas fragments, kas ietver galveni, promo reklāmkarogu un sīkfailu piekrišanas moduļus.</span><span class="sxs-lookup"><span data-stu-id="2c512-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="2c512-107">Galvenes modulī ir iekļauts vietnes logotips, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē, groza ikonas modulis, vēlmju simbols, pierakstīšanās opcijas un meklēšanas josla.</span><span class="sxs-lookup"><span data-stu-id="2c512-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="2c512-108">Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (citiem vārdiem sakot, darbvirsmas ierīcei vai mobilajai ierīcei).</span><span class="sxs-lookup"><span data-stu-id="2c512-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="2c512-109">Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).</span><span class="sxs-lookup"><span data-stu-id="2c512-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="2c512-110">Attēlā zemāk redzams galvenes moduļa piemērs sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="2c512-110">The following image shows an example of a header module on a home page.</span></span>

![Galvenes moduļa piemērs](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="2c512-112">Galvenes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="2c512-112">Properties of a header module</span></span>

<span data-ttu-id="2c512-113">Galvenes modulis atbalsta šādus rekvizītus: **Logotipa attēls**, **Logotipa saite** un **Mana konta saites**.</span><span class="sxs-lookup"><span data-stu-id="2c512-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="2c512-114">Rekvizīti **Logotipa attēls** un **Logotipa saites** tiek izmantoti, lai definētu logotipu lapā.</span><span class="sxs-lookup"><span data-stu-id="2c512-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="2c512-115">Plašāku informāciju skatiet sadaļā [Logotipa pievienošana](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="2c512-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="2c512-116">Rekvizīts **Mana konta saites** var tikt izmantots, lai definētu konta lapas, kuras vietnes īpašnieks vēlas parādīt tiešās saites virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="2c512-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="2c512-117">Galvenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="2c512-117">Modules that are available within a header module</span></span>

<span data-ttu-id="2c512-118">Šādus moduļus var izmantot galvenes modulī.</span><span class="sxs-lookup"><span data-stu-id="2c512-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="2c512-119">**Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites.</span><span class="sxs-lookup"><span data-stu-id="2c512-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="2c512-120">Papildinformāciju skatiet šeit: [Navigācijas izvēlnes modulis](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="2c512-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="2c512-121">**Meklēšana** — meklēšanas modulis ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="2c512-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="2c512-122">Noklusējuma meklēšanas lapas URL un meklēšanas vaicājuma parametri ir jānorāda sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="2c512-123">Meklēšanas modulim ir rekvizīti, kas ļauj izlaist meklēšanas pogu vai etiķeti pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="2c512-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="2c512-124">Meklēšanas modulis atbalsta arī automātiskās ieteikšanas opcijas, piemēram, preci, atslēgvārdu un kategoriju meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="2c512-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="2c512-125">**Groza ikona** — groza ikonu modulis attēlo groza ikonu, kas parāda preču skaitu grozā jebkurā laikā.</span><span class="sxs-lookup"><span data-stu-id="2c512-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="2c512-126">Plašāku informāciju skatiet [Groza ikonas modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="2c512-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="2c512-127">Lapas galvenes fragmenta izveide</span><span class="sxs-lookup"><span data-stu-id="2c512-127">Create a header fragment for a page</span></span>

<span data-ttu-id="2c512-128">Lai izveidotu galvenes fragmentu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="2c512-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="2c512-129">Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.</span><span class="sxs-lookup"><span data-stu-id="2c512-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="2c512-130">Dialoglodziņā **Jauns fragments** atlasiet moduli **Konteiners**, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2c512-131">Atlasiet slotu **Noklusējuma konteiners** un pēc tam rekvizītu rūtī pa labi iestatiet rekvizītu **Platums** uz **Aizpildīt ekrānu**.</span><span class="sxs-lookup"><span data-stu-id="2c512-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="2c512-132">Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="2c512-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2c512-133">Dialoglodziņā **Pievienot moduli** atlasiet moduļus **Sīkdatņu piekrišana**, **Galvene** un **Veicināšanas reklāmkarogs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="2c512-134">Moduļa **Veicināšanas reklāmkarogs** rekvizītu rūtī atlasiet **Pievienot ziņojumu** un pēc tam atlasiet **Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="2c512-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="2c512-135">Dialoglodziņā **Ziņojums** pievienojiet tekstu un saites reklāmas saturam un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="2c512-136">Moduļa **Sīkdatņu piekrišana** rekvizītu rūtī pievienojiet un konfigurējiet tekstu un saiti uz vietnes konfidencialitātes lapu.</span><span class="sxs-lookup"><span data-stu-id="2c512-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="2c512-137">Galvenes moduļa slotā **Navigācijas izvēlne** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="2c512-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2c512-138">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Navigācijas izvēlne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2c512-139">Navigācijas izvēlnes moduļa rekvizītu rūts sadaļā **Navigācijas izvēlnes avots** atlasiet **Mazumtirdzniecības serveris**.</span><span class="sxs-lookup"><span data-stu-id="2c512-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="2c512-140">Navigācijas izvēlnes moduļa rekvizītu rūts sadaļā **Statiski izvēlnes vienumi** atlasiet **Pievienot izvēlnes vienumu**, un pēc tam atlasiet **Izvēlnes elements**.</span><span class="sxs-lookup"><span data-stu-id="2c512-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="2c512-141">Dialoglodziņā **Izvēlnes vienums** sadaļā **Izvēlnes vienuma teksts** ievadiet "Kontaktpersona."</span><span class="sxs-lookup"><span data-stu-id="2c512-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="2c512-142">Dialoglodziņā **Izvēlnes vienums** sadaļā **Izvēlnes vienuma saites mērķis** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="2c512-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="2c512-143">Dialoglodziņā **Pievienot saiti** atlasiet URL saites "Kontaktpersonas" lapai un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="2c512-144">Dialoglodziņā **Izvēlnes vienums** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="2c512-145">Galvenes moduļa slotā **Meklēt** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="2c512-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2c512-146">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēt** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2c512-147">Meklēšanas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="2c512-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="2c512-148">Galvenes moduļa slotā **Groza ikona** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="2c512-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2c512-149">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Groza ikona** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c512-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2c512-150">Groza ikonas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="2c512-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="2c512-151">Ja vēlaties, lai groza ikona parāda groza kopsavilkumu (to sauc arī par mini grozu), kad lietotāji uz to norāda, atlasiet **Rādīt mini grozu**.</span><span class="sxs-lookup"><span data-stu-id="2c512-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="2c512-152">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="2c512-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="2c512-153">Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.</span><span class="sxs-lookup"><span data-stu-id="2c512-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="2c512-154">Moduļa **Noklusējuma lapa** slotā **Galvene** pievienojiet jūsu izveidoto kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="2c512-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="2c512-155">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="2c512-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c512-156">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2c512-156">Additional resources</span></span>

[<span data-ttu-id="2c512-157">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="2c512-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2c512-158">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="2c512-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2c512-159">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="2c512-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="2c512-160">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="2c512-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="2c512-161">Navigācijas izvēlnas modulis</span><span class="sxs-lookup"><span data-stu-id="2c512-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="2c512-162">Piekrišana sīkfailiem</span><span class="sxs-lookup"><span data-stu-id="2c512-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="2c512-163">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="2c512-163">Footer module</span></span>](author-footer-module.md)
