---
title: Galvenes modulis
description: Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686626"
---
# <a name="header-module"></a><span data-ttu-id="df484-103">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="df484-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df484-104">Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="df484-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="df484-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="df484-105">Overview</span></span>

<span data-ttu-id="df484-106">Programmā Dynamics 365 Commerce lapas galvene ietver vairākus moduļus, piemēram, galveni, navigācijas izvēlni, meklēšanu, veicināšanas reklāmkarogu un sīkfailu piekrišanas moduļus.</span><span class="sxs-lookup"><span data-stu-id="df484-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="df484-107">Galvenes modulī ir iekļauts vietnes logotips, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē, groza simbols, vēlmju simbols, pierakstīšanās opcijas un meklēšanas josla.</span><span class="sxs-lookup"><span data-stu-id="df484-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="df484-108">Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (citiem vārdiem sakot, darbvirsmas ierīcei vai mobilajai ierīcei).</span><span class="sxs-lookup"><span data-stu-id="df484-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="df484-109">Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).</span><span class="sxs-lookup"><span data-stu-id="df484-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="df484-110">Attēlā zemāk redzams galvenes moduļa piemērs sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="df484-110">The following image shows an example of a header module on a home page.</span></span>

![Galvenes moduļa piemērs](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="df484-112">Galvenes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="df484-112">Properties of a header module</span></span>

<span data-ttu-id="df484-113">Galvenes modulis atbalsta šādus rekvizītus: **Logotipa attēls**, **Logotipa saite** un **Mana konta saites**.</span><span class="sxs-lookup"><span data-stu-id="df484-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="df484-114">Rekvizīti **Logotipa attēls** un **Logotipa saites** tiek izmantoti, lai definētu logotipu lapā.</span><span class="sxs-lookup"><span data-stu-id="df484-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="df484-115">Plašāku informāciju skatiet sadaļā [Logotipa pievienošana](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="df484-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="df484-116">Rekvizīts **Mana konta saites** var tikt izmantots, lai definētu konta lapas, kuras vietnes īpašnieks vēlas parādīt tiešās saites virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="df484-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="df484-117">Galvenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="df484-117">Modules that are available in a header module</span></span>

<span data-ttu-id="df484-118">Šādus moduļus var izmantot galvenes modulī.</span><span class="sxs-lookup"><span data-stu-id="df484-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="df484-119">**Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites.</span><span class="sxs-lookup"><span data-stu-id="df484-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="df484-120">Kanāla navigācijas hierarhiju var konfigurēt programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="df484-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="df484-121">Navigācijas izvēlnē ir rekvizīts **Navigācijas avots**, kas tiek izmantots, lai norādītu Retail Server navigācijas izvēlnes vienumus un statiskos izvēlnes elementus kā avotu.</span><span class="sxs-lookup"><span data-stu-id="df484-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="df484-122">Ja statiskie izvēlnes elementi ir norādīti kā avots, var tikt nodrošinātas relatīvas saites ar citām lapām vietnē.</span><span class="sxs-lookup"><span data-stu-id="df484-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="df484-123">Konfigurētie elementi tiek parādīti kā galvenes navigācija.</span><span class="sxs-lookup"><span data-stu-id="df484-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="df484-124">**Meklēšana** — meklēšanas modulis ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="df484-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="df484-125">Noklusējuma meklēšanas lapas URL un meklēšanas vaicājuma parametri ir jānorāda sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="df484-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="df484-126">Meklēšanas modulim ir rekvizīti, kas ļauj izlaist meklēšanas pogu vai etiķeti pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="df484-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="df484-127">Meklēšanas modulis atbalsta arī automātiskās ieteikšanas opcijas, piemēram, preci, atslēgvārdu un kategoriju meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="df484-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="df484-128">**Groza ikona** — groza ikonu modulis attēlo groza ikonu, kas parāda preču skaitu grozā jebkurā laikā.</span><span class="sxs-lookup"><span data-stu-id="df484-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="df484-129">Plašāku informāciju skatiet [Groza ikonas modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="df484-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="df484-130">Lapas galvenes moduļa izveide</span><span class="sxs-lookup"><span data-stu-id="df484-130">Create a header module for a page</span></span>

<span data-ttu-id="df484-131">Lai izveidotu galvenes moduli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="df484-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="df484-132">Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.</span><span class="sxs-lookup"><span data-stu-id="df484-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="df484-133">Dialoglodziņā **Jaunas lapas fragments** atlasiet moduli **Konteiners**, ievadiet lapas fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="df484-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="df484-134">Atlasiet slotu **Noklusējuma konteiners** un pēc tam rekvizītu rūtī pa labi iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="df484-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="df484-135">Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="df484-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="df484-136">Dialoglodziņā **Pievienot moduli** atlasiet moduļus **Veicināšanas reklāmkarogs** un **Sīkdatņu piekrišana** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="df484-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="df484-137">Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="df484-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="df484-138">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="df484-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="df484-139">Atlasiet slotu **Konteiners** un pēc tam rekvizītu rūtī pa labi iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="df484-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="df484-140">Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="df484-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="df484-141">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Galvene** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="df484-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="df484-142">Galvenes moduļa slotā **Navigācijas izvēlne** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="df484-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="df484-143">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Navigācijas izvēlne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="df484-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="df484-144">Navigācijas izvēlnes moduļa rekvizītu rūtī konfigurējiet navigācijas izvēlnes moduļa rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="df484-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="df484-145">Galvenes moduļa slotā **Meklēt** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="df484-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="df484-146">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēt** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="df484-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="df484-147">Meklēšanas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="df484-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="df484-148">Galvenes moduļa slotā **Groza ikona** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="df484-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="df484-149">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Groza ikona** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="df484-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="df484-150">Groza ikonas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="df484-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="df484-151">Ja vēlaties, lai groza ikona parāda groza kopsavilkumu (to sauc arī par mini grozu), kad lietotāji uz to norāda, atlasiet **Rādīt mini grozu**.</span><span class="sxs-lookup"><span data-stu-id="df484-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="df484-152">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="df484-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="df484-153">Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.</span><span class="sxs-lookup"><span data-stu-id="df484-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="df484-154">Moduļa **Noklusējuma lapa** slotā **Galvene** pievienojiet jūsu izveidoto kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="df484-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="df484-155">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="df484-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df484-156">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="df484-156">Additional resources</span></span>

[<span data-ttu-id="df484-157">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="df484-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="df484-158">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="df484-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="df484-159">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="df484-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="df484-160">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="df484-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="df484-161">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="df484-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="df484-162">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="df484-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="df484-163">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="df484-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="df484-164">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="df484-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="df484-165">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="df484-165">Footer module</span></span>](author-footer-module.md)
