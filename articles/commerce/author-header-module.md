---
title: Galvenes modulis
description: Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697279"
---
# <a name="header-module"></a><span data-ttu-id="97794-103">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="97794-103">Header module</span></span>

<span data-ttu-id="97794-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="97794-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="97794-105">Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97794-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97794-106">Pārskats</span><span class="sxs-lookup"><span data-stu-id="97794-106">Overview</span></span>

<span data-ttu-id="97794-107">Virsraksta modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu visus moduļus, kas tiks rādīti lapas galvenē.</span><span class="sxs-lookup"><span data-stu-id="97794-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="97794-108">Piemēram, tas var ietvert jūsu vietnes logotipu, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē un meklēšanas joslu.</span><span class="sxs-lookup"><span data-stu-id="97794-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="97794-109">Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (tas ir, darbvirsmas ierīcei vai mobilajai ierīcei).</span><span class="sxs-lookup"><span data-stu-id="97794-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="97794-110">Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).</span><span class="sxs-lookup"><span data-stu-id="97794-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="97794-111">Galvenes rekvizīti</span><span class="sxs-lookup"><span data-stu-id="97794-111">Properties of a header</span></span>

<span data-ttu-id="97794-112">Tāpat kā vispārējie konteineri, galvenes modulis atbalsta **virsraksta** un **platuma** rekvizītu.</span><span class="sxs-lookup"><span data-stu-id="97794-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="97794-113">Virsraksta modulim ir vairāki sloti.</span><span class="sxs-lookup"><span data-stu-id="97794-113">A header module has multiple slots.</span></span> <span data-ttu-id="97794-114">Piemēram, sloti ir informācijas ziņojumam, navigācijas izvēlnei, logotipam, meklēšanas joslai, groza ikonai, vēlmju saraksta ikonai un konta informācijai.</span><span class="sxs-lookup"><span data-stu-id="97794-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="97794-115">Katrs slots atbalsta noteiktu moduļu kopu.</span><span class="sxs-lookup"><span data-stu-id="97794-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="97794-116">Galvenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="97794-116">Modules that are available in a header module</span></span>

<span data-ttu-id="97794-117">Šādus moduļus var izmantot galvenes modulī.</span><span class="sxs-lookup"><span data-stu-id="97794-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="97794-118">**Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites.</span><span class="sxs-lookup"><span data-stu-id="97794-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="97794-119">Kanāla navigācijas hierarhiju var konfigurēt programmā Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="97794-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="97794-120">Konfigurētie elementi tiek parādīti kā galvenes navigācija.</span><span class="sxs-lookup"><span data-stu-id="97794-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="97794-121">Turklāt var tikt konfigurētas statiskas navigācijas saites, un var tikt nodrošinātas relatīvas saites uz citām lapām E-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="97794-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="97794-122">Galveni var līdzināt pa kreisi, pa labi vai centrēt.</span><span class="sxs-lookup"><span data-stu-id="97794-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="97794-123">**Groza ikona** — groza ikona ir īpaša ikona, kas apzīmē grozu.</span><span class="sxs-lookup"><span data-stu-id="97794-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="97794-124">Tā tiek parādīta virsrakstā un norāda elementu skaitu grozā.</span><span class="sxs-lookup"><span data-stu-id="97794-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="97794-125">Saite uz groza lapu jāpievieno groza ikonai, lai klientus varētu novirzīt uz groza lapu, kad viņi mijiedarbojas ar ikonu.</span><span class="sxs-lookup"><span data-stu-id="97794-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="97794-126">**Vēlmju saraksta ikona** — virsrakstā ir parādīta vēlmju saraksta ikona, un tā norāda elementu skaitu, kas pievienoti klienta vēlmju sarakstam.</span><span class="sxs-lookup"><span data-stu-id="97794-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="97794-127">Šai ikonai ir jāpievieno saite uz vēlmju sarakstu, lai klientus var novirzīt uz vēlmju saraksta lapu, kad viņi mijiedarbojas ar ikonu.</span><span class="sxs-lookup"><span data-stu-id="97794-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="97794-128">**Pierakstīšanās modulis** – pierakstīšanās modulis ir redzams virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="97794-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="97794-129">Tas ļauj klientiem vai nu pierakstīties savā kontā, vai reģistrējieties kontam.</span><span class="sxs-lookup"><span data-stu-id="97794-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="97794-130">Ja klients jau ir pierakstījies, moduli var konfigurēt, lai rādītu saites uz konta lapu, pasūtījuma vēstures lapu vai citu lapu.</span><span class="sxs-lookup"><span data-stu-id="97794-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="97794-131">**Logotipa modulis** — šis modulis rāda logotipu, kas apzīmē mazumtirgotāju un zīmolu.</span><span class="sxs-lookup"><span data-stu-id="97794-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="97794-132">Tas ir attēls, kuram ir saite.</span><span class="sxs-lookup"><span data-stu-id="97794-132">It's an image that has a link.</span></span> <span data-ttu-id="97794-133">Parasti saite ir konfigurēta tā, ka tā varētu novirzīt uz sākumlapu, tāpēc klienti var ātri atgriezties sākumlapā no jebkuras vietnes lapas.</span><span class="sxs-lookup"><span data-stu-id="97794-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="97794-134">**Brīdinājums** — galvenē tiek parādīts brīdinājums, un tas tiek izmantots, lai atspoguļotu iekļauto ziņojumu, kas attiecas uz visām vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="97794-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="97794-135">Piemēram, brīdinājumā var tikt parādīts ziņojums “Ikgadējā izpārdošana beidzas pēc 10 dienām”.</span><span class="sxs-lookup"><span data-stu-id="97794-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="97794-136">**Meklēšanas josla** — meklēšanas josla ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="97794-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="97794-137">Modulim jābūt konfigurētam ar meklēšanas rezultātu lapas vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="97794-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="97794-138">Vaicājuma virknes parametru var konfigurēt (noklusējuma vērtība ir **“q”**).</span><span class="sxs-lookup"><span data-stu-id="97794-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="97794-139">Meklēšanas joslai ir automātiskās piedāvāšanas slots, kurā ir jāpievieno automātiskās piedāvāšanas modulis.</span><span class="sxs-lookup"><span data-stu-id="97794-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="97794-140">**Automātiskā piedāvāšana** – automātiskās piedāvāšanas modulis rāda automātiski piedāvātos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="97794-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="97794-141">Šie rezultāti var būt atslēgvārdi, preces vai kategorijas, kur ir atrasts meklējamais termins.</span><span class="sxs-lookup"><span data-stu-id="97794-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="97794-142">Galvenes moduļa izveide</span><span class="sxs-lookup"><span data-stu-id="97794-142">Create a header module</span></span>

<span data-ttu-id="97794-143">Lai izveidotu galvenes moduli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="97794-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="97794-144">Izveidojiet lapas fragmentu, kas ietver galvenes moduli.</span><span class="sxs-lookup"><span data-stu-id="97794-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="97794-145">Pievienojiet moduļus slotiem virsrakstu modulī.</span><span class="sxs-lookup"><span data-stu-id="97794-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="97794-146">Atjauniniet katra moduļa iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="97794-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="97794-147">Saglabājiet lapas fragmentu.</span><span class="sxs-lookup"><span data-stu-id="97794-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="97794-148">Pārbaudiet lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="97794-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="97794-149">Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.</span><span class="sxs-lookup"><span data-stu-id="97794-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="97794-150">Noklusējuma lapā lapas fragmentu, kas ietver virsraksta moduli, pievienojiet galvenei, kas atrodas galvenajā slotā.</span><span class="sxs-lookup"><span data-stu-id="97794-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="97794-151">Saglabājiet veidni.</span><span class="sxs-lookup"><span data-stu-id="97794-151">Save the template.</span></span> 
1. <span data-ttu-id="97794-152">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="97794-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97794-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="97794-153">Additional resources</span></span>

[<span data-ttu-id="97794-154">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="97794-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="97794-155">Container modulis</span><span class="sxs-lookup"><span data-stu-id="97794-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="97794-156">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="97794-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="97794-157">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="97794-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="97794-158">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="97794-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="97794-159">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="97794-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="97794-160">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="97794-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="97794-161">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="97794-161">Footer module</span></span>](author-footer-module.md)
