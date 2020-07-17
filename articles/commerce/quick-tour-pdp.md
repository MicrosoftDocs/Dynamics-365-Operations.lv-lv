---
title: Preču papildinformācijas lapu pārskats
description: Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c53e74204fad2960dfba972a38c511df7d6672d8
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527543"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="0fea1-103">Preču papildinformācijas lapu pārskats</span><span class="sxs-lookup"><span data-stu-id="0fea1-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0fea1-104">Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0fea1-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0fea1-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="0fea1-105">Overview</span></span>

<span data-ttu-id="0fea1-106">PDP sniedz detalizētu informāciju par preci, un ļaujiet klientiem izvēlēties preces opcijas, piemēram, izmēru, stilu un krāsu.</span><span class="sxs-lookup"><span data-stu-id="0fea1-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="0fea1-107">PDP ir jāparāda visa preces informācija, kas klientam nepieciešama, lai pieņemtu lēmumu par pirkšanu.</span><span class="sxs-lookup"><span data-stu-id="0fea1-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="0fea1-108">Tālāk redzamajā attēlā parādīts PDP piemērs.</span><span class="sxs-lookup"><span data-stu-id="0fea1-108">The following illustration shows an example of a PDP.</span></span>

![Preces detalizētas informācijas lapas piemērs](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="0fea1-110">Galvenes un kājenes moduļi</span><span class="sxs-lookup"><span data-stu-id="0fea1-110">Header and footer modules</span></span>

<span data-ttu-id="0fea1-111">PDP augšpusē ir virsraksts, kas parāda visas preču kategorijas un citas lapas, kuras mazumtirgotājs vēlas, lai klienti pārlūkotu.</span><span class="sxs-lookup"><span data-stu-id="0fea1-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="0fea1-112">Lapas apakšpusē ir kājene, kas ietver ātras saites uz dažādām tēmām, kas varētu interesēt pircējus.</span><span class="sxs-lookup"><span data-stu-id="0fea1-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="0fea1-113">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="0fea1-113">Buy box module</span></span>

<span data-ttu-id="0fea1-114">Nozīmīgākais modulis PDP ir pirkšanas loga modulis, kas tiek parādīts kā pirmais vienums lapas galvenajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="0fea1-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="0fea1-115">Pirkšanas loga modulis parāda svarīgu informāciju par preci, piemēram, preces nosaukumu, preces aprakstu, preces cenu, preces attēlus un preces vērtējumu.</span><span class="sxs-lookup"><span data-stu-id="0fea1-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="0fea1-116">Iegādes lodziņa modulis ļauj klientam izvēlēties preces opcijas (piemēram, izmēru, stilu un krāsu) un pievienot preci grozam.</span><span class="sxs-lookup"><span data-stu-id="0fea1-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="0fea1-117">Tas arī ļauj klientam nopirkt preci tiešsaistē un saņemt to veikalā.</span><span class="sxs-lookup"><span data-stu-id="0fea1-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="0fea1-118">Modulis pirkšanai tiešsaistē un saņemšanai veikalā izmanto integrāciju ar Bing Maps programmas programmēšanas interfeisiem (API), lai atrastu tuvumā esošos veikalus vai veikalus citā vietā, ko norāda klients.</span><span class="sxs-lookup"><span data-stu-id="0fea1-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="0fea1-119">Iegādes lodziņa modulim ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="0fea1-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="0fea1-120">Šis ID tiek iegūts no lapas konteksta.</span><span class="sxs-lookup"><span data-stu-id="0fea1-120">This ID is derived from the page context.</span></span> <span data-ttu-id="0fea1-121">Ja iegādes lodziņa modulis ir pievienots lapai, kur lapas konteksts neietver preces ID, tas šo informāciju neatveidos pareizi.</span><span class="sxs-lookup"><span data-stu-id="0fea1-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="0fea1-122">Preces specifikāciju modulis</span><span class="sxs-lookup"><span data-stu-id="0fea1-122">Product specifications module</span></span>

<span data-ttu-id="0fea1-123">Preces specifikāciju modulis var tikt izmantots, lai parādītu papildu informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="0fea1-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="0fea1-124">Šī detalizētā informācija tiek ņemta no preces īpašībām programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="0fea1-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="0fea1-125">Preces specifikāciju modulis parāda katru īpašību, kur **redzams** rekvizīts ir iestatīts kā **patiess**.</span><span class="sxs-lookup"><span data-stu-id="0fea1-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="0fea1-126">Lai izgūtu preces īpašības, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="0fea1-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="0fea1-127">Ieteikumu modulis</span><span class="sxs-lookup"><span data-stu-id="0fea1-127">Recommendations module</span></span>

<span data-ttu-id="0fea1-128">Ieteikumu modulis ir svarīgs modulis PDP.</span><span class="sxs-lookup"><span data-stu-id="0fea1-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="0fea1-129">Kamēr klienti meklē preces, tiem jāsniedz vairāk preču opciju, lai klienti varētu atrast pareizo preci un veikt pirkumu.</span><span class="sxs-lookup"><span data-stu-id="0fea1-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="0fea1-130">Ieteikumi palīdz klientiem viegli atklāt saistīto saturu un turpināt iepirkties.</span><span class="sxs-lookup"><span data-stu-id="0fea1-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="0fea1-131">Ir pieejami dažādi ieteikumu sarakstu veidi.</span><span class="sxs-lookup"><span data-stu-id="0fea1-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="0fea1-132">Saraksts **Pircējiem patīk arī** ir balstīts uz mašīnmācību.</span><span class="sxs-lookup"><span data-stu-id="0fea1-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="0fea1-133">Lai sniegtu ieteikumus, tas izmanto citu klientu darījumu vēsturi.</span><span class="sxs-lookup"><span data-stu-id="0fea1-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="0fea1-134">Šo sarakstu ģenerē ieteikumu pakalpojums un tas līdzinās sarakstiem "Klientiem, kas iegādājušies šo, nopirka arī...".</span><span class="sxs-lookup"><span data-stu-id="0fea1-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="0fea1-135">Lai ģenerētu šo sarakstu, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="0fea1-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="0fea1-136">Sarakstu **Saistīts** precei ir iespējams konfigurēt programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="0fea1-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="0fea1-137">Piemēram, brūnai rokas ceļasomai no ādas saistītajā sarakstā var konfigurēt vairāk rokassomu, kas izgatavotas no ādas, vai paredzētas ceļošanai.</span><span class="sxs-lookup"><span data-stu-id="0fea1-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="0fea1-138">Citus saistīto sarakstu veidus, piemēram, **Piederumi** un **Vairāk līdzīgu preču** arī var konfigurēt programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="0fea1-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="0fea1-139">Lai ģenerētu šo sarakstu, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="0fea1-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="0fea1-140">Tāpēc, ja tas ir pievienots mājas lapai, kur lapas konteksts neietver preces ID, saraksts būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="0fea1-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="0fea1-141">Algoritmiski ģenerētie ieteikumu saraksti, piemēram, **Populārs**, **Vispirktākais** un **Jauns** var tikt izmantoti PDP.</span><span class="sxs-lookup"><span data-stu-id="0fea1-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="0fea1-142">Lai gan šie saraksti var nebūt tieši saistīti ar preci PDP, tas ir cits veids, kā palīdzēt klientiem atrast preces, kas varētu to interesēt.</span><span class="sxs-lookup"><span data-stu-id="0fea1-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="0fea1-143">Šiem sarakstu veidiem nav nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="0fea1-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="0fea1-144">Tie ir vispārēji saraksti, kas tiek ģenerēti, balstoties uz iepirkšanās paradumiem visā vietnē.</span><span class="sxs-lookup"><span data-stu-id="0fea1-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="0fea1-145">Rediģējamie saraksti ir manuāli pārraudzīti saraksti.</span><span class="sxs-lookup"><span data-stu-id="0fea1-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="0fea1-146">Piemēram, mazumtirgotājs var nolemt manuāli pārraudzīt to preču sarakstus, ko tas vēlas parādīt.</span><span class="sxs-lookup"><span data-stu-id="0fea1-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="0fea1-147">Vērtējumu un apskatu moduļi</span><span class="sxs-lookup"><span data-stu-id="0fea1-147">Ratings and reviews modules</span></span>

<span data-ttu-id="0fea1-148">Var izmantot trīs moduļus, lai parādītu un pievienotu pārskatus:</span><span class="sxs-lookup"><span data-stu-id="0fea1-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="0fea1-149">**Apskati** – Šis modulis parāda vērtējumus un apskatus, ko snieguši citi klienti.</span><span class="sxs-lookup"><span data-stu-id="0fea1-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="0fea1-150">Debitori var šķirot un filtrēt pārskatus.</span><span class="sxs-lookup"><span data-stu-id="0fea1-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="0fea1-151">Šis modulis ļauj arī klientiem atzinīgi vai negatīvi novērtēt apskatus, kā arī ziņot par problēmām.</span><span class="sxs-lookup"><span data-stu-id="0fea1-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="0fea1-152">**Rakstīt apskati** – Šis modulis ļauj klientiem rakstīt savus apskatus par preci.</span><span class="sxs-lookup"><span data-stu-id="0fea1-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="0fea1-153">**Vērtējumu histogramma** – šis modulis ietver histogrammu, kas parāda preces reitingu tendenci.</span><span class="sxs-lookup"><span data-stu-id="0fea1-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="0fea1-154">Papildinformāciju skatiet [Pārskats par vērtējumiem un apskatiem](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0fea1-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="0fea1-155">Mārketinga moduļi</span><span class="sxs-lookup"><span data-stu-id="0fea1-155">Marketing modules</span></span>

<span data-ttu-id="0fea1-156">Ja mārketinga saturs ir unikāls konkrētai precei, PDP var pievienot jebkuru mārketinga moduli.</span><span class="sxs-lookup"><span data-stu-id="0fea1-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="0fea1-157">Varat pievienot mārketinga moduļus PDP, izmantojot lapas "papildināšanu".</span><span class="sxs-lookup"><span data-stu-id="0fea1-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="0fea1-158">Plašāku informāciju skatiet [Preces lapas bagātināšana](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="0fea1-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0fea1-159">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0fea1-159">Additional resources</span></span>

[<span data-ttu-id="0fea1-160">Mājas lapas pārskats</span><span class="sxs-lookup"><span data-stu-id="0fea1-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="0fea1-161">Pārskats par grozu un norēķināšanās lapām</span><span class="sxs-lookup"><span data-stu-id="0fea1-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="0fea1-162">Konta pārvaldības lapu pārskats</span><span class="sxs-lookup"><span data-stu-id="0fea1-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="0fea1-163">Preces informācijas bagātināšanas lapa</span><span class="sxs-lookup"><span data-stu-id="0fea1-163">Enrich a product details page</span></span>](enrich-product-page.md)
