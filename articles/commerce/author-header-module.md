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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885482"
---
# <a name="header-module"></a><span data-ttu-id="90b1f-103">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="90b1f-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="90b1f-104">Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="90b1f-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="90b1f-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="90b1f-105">Overview</span></span>

<span data-ttu-id="90b1f-106">Virsraksta modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu visus moduļus, kas tiks rādīti lapas galvenē.</span><span class="sxs-lookup"><span data-stu-id="90b1f-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="90b1f-107">Piemēram, tas var ietvert jūsu vietnes logotipu, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē un meklēšanas joslu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="90b1f-108">Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (tas ir, darbvirsmas ierīcei vai mobilajai ierīcei).</span><span class="sxs-lookup"><span data-stu-id="90b1f-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="90b1f-109">Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).</span><span class="sxs-lookup"><span data-stu-id="90b1f-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="90b1f-110">Galvenes rekvizīti</span><span class="sxs-lookup"><span data-stu-id="90b1f-110">Properties of a header</span></span>

<span data-ttu-id="90b1f-111">Tāpat kā vispārējie konteineri, galvenes modulis atbalsta **virsraksta** un **platuma** rekvizītu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="90b1f-112">Virsraksta modulim ir vairāki sloti.</span><span class="sxs-lookup"><span data-stu-id="90b1f-112">A header module has multiple slots.</span></span> <span data-ttu-id="90b1f-113">Piemēram, sloti ir informācijas ziņojumam, navigācijas izvēlnei, logotipam, meklēšanas joslai, groza ikonai, vēlmju saraksta ikonai un konta informācijai.</span><span class="sxs-lookup"><span data-stu-id="90b1f-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="90b1f-114">Katrs slots atbalsta noteiktu moduļu kopu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="90b1f-115">Galvenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="90b1f-115">Modules that are available in a header module</span></span>

<span data-ttu-id="90b1f-116">Šādus moduļus var izmantot galvenes modulī.</span><span class="sxs-lookup"><span data-stu-id="90b1f-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="90b1f-117">**Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites.</span><span class="sxs-lookup"><span data-stu-id="90b1f-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="90b1f-118">Kanāla navigācijas hierarhiju var konfigurēt programmā Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="90b1f-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="90b1f-119">Konfigurētie elementi tiek parādīti kā galvenes navigācija.</span><span class="sxs-lookup"><span data-stu-id="90b1f-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="90b1f-120">Turklāt var tikt konfigurētas statiskas navigācijas saites, un var tikt nodrošinātas relatīvas saites uz citām lapām E-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="90b1f-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="90b1f-121">Galveni var līdzināt pa kreisi, pa labi vai centrēt.</span><span class="sxs-lookup"><span data-stu-id="90b1f-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="90b1f-122">**Groza ikona** — groza ikona ir īpaša ikona, kas apzīmē grozu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="90b1f-123">Tā tiek parādīta virsrakstā un norāda elementu skaitu grozā.</span><span class="sxs-lookup"><span data-stu-id="90b1f-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="90b1f-124">Saite uz groza lapu jāpievieno groza ikonai, lai klientus varētu novirzīt uz groza lapu, kad viņi mijiedarbojas ar ikonu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="90b1f-125">**Vēlmju saraksta ikona** — virsrakstā ir parādīta vēlmju saraksta ikona, un tā norāda elementu skaitu, kas pievienoti klienta vēlmju sarakstam.</span><span class="sxs-lookup"><span data-stu-id="90b1f-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="90b1f-126">Šai ikonai ir jāpievieno saite uz vēlmju sarakstu, lai klientus var novirzīt uz vēlmju saraksta lapu, kad viņi mijiedarbojas ar ikonu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="90b1f-127">**Pierakstīšanās modulis** – pierakstīšanās modulis ir redzams virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="90b1f-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="90b1f-128">Tas ļauj klientiem vai nu pierakstīties savā kontā, vai reģistrējieties kontam.</span><span class="sxs-lookup"><span data-stu-id="90b1f-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="90b1f-129">Ja klients jau ir pierakstījies, moduli var konfigurēt, lai rādītu saites uz konta lapu, pasūtījuma vēstures lapu vai citu lapu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="90b1f-130">**Logotipa modulis** — šis modulis rāda logotipu, kas apzīmē mazumtirgotāju un zīmolu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="90b1f-131">Tas ir attēls, kuram ir saite.</span><span class="sxs-lookup"><span data-stu-id="90b1f-131">It's an image that has a link.</span></span> <span data-ttu-id="90b1f-132">Parasti saite ir konfigurēta tā, ka tā varētu novirzīt uz sākumlapu, tāpēc klienti var ātri atgriezties sākumlapā no jebkuras vietnes lapas.</span><span class="sxs-lookup"><span data-stu-id="90b1f-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="90b1f-133">**Brīdinājums** — galvenē tiek parādīts brīdinājums, un tas tiek izmantots, lai atspoguļotu iekļauto ziņojumu, kas attiecas uz visām vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="90b1f-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="90b1f-134">Piemēram, brīdinājumā var tikt parādīts ziņojums “Ikgadējā izpārdošana beidzas pēc 10 dienām”.</span><span class="sxs-lookup"><span data-stu-id="90b1f-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="90b1f-135">**Meklēšanas josla** — meklēšanas josla ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai.</span><span class="sxs-lookup"><span data-stu-id="90b1f-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="90b1f-136">Modulim jābūt konfigurētam ar meklēšanas rezultātu lapas vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="90b1f-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="90b1f-137">Vaicājuma virknes parametru var konfigurēt (noklusējuma vērtība ir **“q”**).</span><span class="sxs-lookup"><span data-stu-id="90b1f-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="90b1f-138">Meklēšanas joslai ir automātiskās piedāvāšanas slots, kurā ir jāpievieno automātiskās piedāvāšanas modulis.</span><span class="sxs-lookup"><span data-stu-id="90b1f-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="90b1f-139">**Automātiskā piedāvāšana** – automātiskās piedāvāšanas modulis rāda automātiski piedāvātos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="90b1f-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="90b1f-140">Šie rezultāti var būt atslēgvārdi, preces vai kategorijas, kur ir atrasts meklējamais termins.</span><span class="sxs-lookup"><span data-stu-id="90b1f-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="90b1f-141">Galvenes moduļa izveide</span><span class="sxs-lookup"><span data-stu-id="90b1f-141">Create a header module</span></span>

<span data-ttu-id="90b1f-142">Lai izveidotu galvenes moduli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="90b1f-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="90b1f-143">Izveidojiet lapas fragmentu, kas ietver galvenes moduli.</span><span class="sxs-lookup"><span data-stu-id="90b1f-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="90b1f-144">Pievienojiet moduļus slotiem virsrakstu modulī.</span><span class="sxs-lookup"><span data-stu-id="90b1f-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="90b1f-145">Atjauniniet katra moduļa iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="90b1f-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="90b1f-146">Saglabājiet lapas fragmentu.</span><span class="sxs-lookup"><span data-stu-id="90b1f-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="90b1f-147">Pārbaudiet lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="90b1f-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="90b1f-148">Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.</span><span class="sxs-lookup"><span data-stu-id="90b1f-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="90b1f-149">Noklusējuma lapā lapas fragmentu, kas ietver virsraksta moduli, pievienojiet galvenei, kas atrodas galvenajā slotā.</span><span class="sxs-lookup"><span data-stu-id="90b1f-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="90b1f-150">Saglabājiet veidni.</span><span class="sxs-lookup"><span data-stu-id="90b1f-150">Save the template.</span></span> 
1. <span data-ttu-id="90b1f-151">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="90b1f-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90b1f-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="90b1f-152">Additional resources</span></span>

[<span data-ttu-id="90b1f-153">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="90b1f-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="90b1f-154">Container modulis</span><span class="sxs-lookup"><span data-stu-id="90b1f-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="90b1f-155">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="90b1f-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="90b1f-156">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="90b1f-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="90b1f-157">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="90b1f-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="90b1f-158">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="90b1f-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="90b1f-159">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="90b1f-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="90b1f-160">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="90b1f-160">Footer module</span></span>](author-footer-module.md)
