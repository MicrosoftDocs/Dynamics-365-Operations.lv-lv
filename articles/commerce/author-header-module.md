---
title: Galvenes modulis
description: Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261448"
---
# <a name="header-module"></a><span data-ttu-id="1762e-103">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1762e-104">Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā izveidot lapas galvenes programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1762e-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1762e-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="1762e-105">Overview</span></span>

<span data-ttu-id="1762e-106">Programmā Dynamics 365 Commerce lapas galvene ietver vairākus moduļus, piemēram, galveni, navigācijas izvēlni, meklēšanu, veicināšanas reklāmkarogu un sīkfailu piekrišanas moduļus.</span><span class="sxs-lookup"><span data-stu-id="1762e-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="1762e-107">Galvenes modulī ir iekļauts vietnes logotips, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē, groza simbols, vēlmju simbols, pierakstīšanās opcijas un meklēšanas josla.</span><span class="sxs-lookup"><span data-stu-id="1762e-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="1762e-108">Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (citiem vārdiem sakot, darbvirsmas ierīcei vai mobilajai ierīcei).</span><span class="sxs-lookup"><span data-stu-id="1762e-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="1762e-109">Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).</span><span class="sxs-lookup"><span data-stu-id="1762e-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="1762e-110">Galvenes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="1762e-110">Properties of a header module</span></span>

<span data-ttu-id="1762e-111">Galvenes modulis atbalsta šādus rekvizītus: **Logotipa attēls**, **Logotipa saite** un **Mana konta saites**.</span><span class="sxs-lookup"><span data-stu-id="1762e-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="1762e-112">Rekvizīti **Logotipa attēls** un **Logotipa saites** tiek izmantoti, lai definētu logotipu lapā.</span><span class="sxs-lookup"><span data-stu-id="1762e-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="1762e-113">Plašāku informāciju skatiet sadaļā [Logotipa pievienošana](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="1762e-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="1762e-114">Rekvizīts **Mana konta saites** var tikt izmantots, lai definētu konta lapas, kuras vietnes īpašnieks vēlas parādīt tiešās saites virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="1762e-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="1762e-115">Galvenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="1762e-115">Modules that are available in a header module</span></span>

<span data-ttu-id="1762e-116">Šādus moduļus var izmantot galvenes modulī.</span><span class="sxs-lookup"><span data-stu-id="1762e-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="1762e-117">**Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites.</span><span class="sxs-lookup"><span data-stu-id="1762e-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="1762e-118">Kanāla navigācijas hierarhiju var konfigurēt programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1762e-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1762e-119">Navigācijas izvēlnē ir rekvizīts **Navigācijas avots**, kas tiek izmantots, lai norādītu Retail Server navigācijas izvēlnes vienumus un statiskos izvēlnes elementus kā avotu.</span><span class="sxs-lookup"><span data-stu-id="1762e-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="1762e-120">Ja statiskie izvēlnes elementi ir norādīti kā avots, var tikt nodrošinātas relatīvas saites ar citām lapām vietnē.</span><span class="sxs-lookup"><span data-stu-id="1762e-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="1762e-121">Konfigurētie elementi tiek parādīti kā galvenes navigācija.</span><span class="sxs-lookup"><span data-stu-id="1762e-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="1762e-122">**Meklēšana** — meklēšanas modulis ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="1762e-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="1762e-123">Noklusējuma meklēšanas lapas URL un meklēšanas vaicājuma parametri ir jānorāda sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="1762e-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="1762e-124">Meklēšanas modulim ir rekvizīti, kas ļauj izlaist meklēšanas pogu vai etiķeti pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="1762e-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="1762e-125">Meklēšanas modulis atbalsta arī automātiskās ieteikšanas opcijas, piemēram, preci, atslēgvārdu un kategoriju meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="1762e-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="1762e-126">**Groza ikona** — groza ikonu modulis attēlo groza ikonu, kas parāda preču skaitu grozā jebkurā laikā.</span><span class="sxs-lookup"><span data-stu-id="1762e-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="1762e-127">Plašāku informāciju skatiet [Groza ikonas modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="1762e-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="1762e-128">Lapas galvenes moduļa izveide</span><span class="sxs-lookup"><span data-stu-id="1762e-128">Create a header module for a page</span></span>

<span data-ttu-id="1762e-129">Lai izveidotu galvenes moduli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="1762e-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="1762e-130">Izveidojiet fragmentu ar nosaukumu **Galvenes fragments** un pievienojiet tam konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="1762e-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="1762e-131">Konteinera moduļa rekvizītu rūtī iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="1762e-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="1762e-132">Pievienojiet konteinera modulim veicināšanas reklāmkarogu un sīkfailu piekrišanas moduļus.</span><span class="sxs-lookup"><span data-stu-id="1762e-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="1762e-133">Pievienojiet fragmentam citu konteinera moduli un iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="1762e-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="1762e-134">Pievienojiet galvenes moduli otrajam konteineru modulim.</span><span class="sxs-lookup"><span data-stu-id="1762e-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="1762e-135">Galvenes moduļa slotā **Navigācijas izvēlne** pievienojiet navigācijas izvēlnes moduli.</span><span class="sxs-lookup"><span data-stu-id="1762e-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="1762e-136">Navigācijas izvēlnes moduļa rekvizītu rūtī konfigurējiet navigācijas izvēlnes moduļa rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="1762e-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="1762e-137">Galvenes moduļa slotā **Meklēšana** pievienojiet meklēšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="1762e-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="1762e-138">Meklēšanas moduļa rekvizītu rūtī konfigurējiet meklēšanas moduļa rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="1762e-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="1762e-139">Galvenes moduļa **Groza ikonas** slotā pievienojiet groza ikonu moduli.</span><span class="sxs-lookup"><span data-stu-id="1762e-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="1762e-140">Groza ikonas moduļa rekvizītu rūtī konfigurējiet groza ikonas moduļa rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="1762e-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="1762e-141">Ja vēlaties, lai groza ikona rādītu mini grozu, kad atrodaties virs tā, atlasiet **Patiess** opcijai **Parādīt mini grozu**.</span><span class="sxs-lookup"><span data-stu-id="1762e-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="1762e-142">Saglabājiet lapas fragmentu, pabeidziet to rediģēt un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="1762e-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="1762e-143">Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.</span><span class="sxs-lookup"><span data-stu-id="1762e-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="1762e-144">Noklusējuma lapas slotā **Galvenais** pievienojiet galvenes lapas fragmentu, kas ietver galvenes moduli.</span><span class="sxs-lookup"><span data-stu-id="1762e-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="1762e-145">Saglabājiet veidni, pabeidziet to rediģēt un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="1762e-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1762e-146">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1762e-146">Additional resources</span></span>

[<span data-ttu-id="1762e-147">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="1762e-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1762e-148">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1762e-149">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1762e-150">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1762e-151">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="1762e-152">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1762e-153">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1762e-154">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1762e-155">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="1762e-155">Footer module</span></span>](author-footer-module.md)
