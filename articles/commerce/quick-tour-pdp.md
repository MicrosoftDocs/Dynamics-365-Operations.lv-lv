---
title: Preču papildinformācijas lapu pārskats
description: Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792223"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="1343b-103">Preču papildinformācijas lapu pārskats</span><span class="sxs-lookup"><span data-stu-id="1343b-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1343b-104">Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1343b-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1343b-105">PDP sniedz detalizētu informāciju par preci, un ļaujiet klientiem izvēlēties preces opcijas, piemēram, izmēru, stilu un krāsu.</span><span class="sxs-lookup"><span data-stu-id="1343b-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="1343b-106">PDP ir jāparāda visa preces informācija, kas klientam nepieciešama, lai pieņemtu lēmumu par pirkšanu.</span><span class="sxs-lookup"><span data-stu-id="1343b-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="1343b-107">Tālāk redzamajā attēlā parādīts PDP piemērs.</span><span class="sxs-lookup"><span data-stu-id="1343b-107">The following illustration shows an example of a PDP.</span></span>

![Preces detalizētas informācijas lapas piemērs](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="1343b-109">Galvenes un kājenes moduļi</span><span class="sxs-lookup"><span data-stu-id="1343b-109">Header and footer modules</span></span>

<span data-ttu-id="1343b-110">PDP augšpusē ir virsraksts, kas parāda visas preču kategorijas un citas lapas, kuras mazumtirgotājs vēlas, lai klienti pārlūkotu.</span><span class="sxs-lookup"><span data-stu-id="1343b-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="1343b-111">Lapas apakšpusē ir kājene, kas ietver ātras saites uz dažādām tēmām, kas varētu interesēt pircējus.</span><span class="sxs-lookup"><span data-stu-id="1343b-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="1343b-112">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="1343b-112">Buy box module</span></span>

<span data-ttu-id="1343b-113">Nozīmīgākais modulis PDP ir pirkšanas loga modulis, kas tiek parādīts kā pirmais vienums lapas galvenajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="1343b-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="1343b-114">Pirkšanas loga modulis parāda svarīgu informāciju par preci, piemēram, preces nosaukumu, preces aprakstu, preces cenu, preces attēlus un preces vērtējumu.</span><span class="sxs-lookup"><span data-stu-id="1343b-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="1343b-115">Iegādes lodziņa modulis ļauj klientam izvēlēties preces opcijas (piemēram, izmēru, stilu un krāsu) un pievienot preci grozam.</span><span class="sxs-lookup"><span data-stu-id="1343b-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="1343b-116">Tas arī ļauj klientam nopirkt preci tiešsaistē un saņemt to veikalā.</span><span class="sxs-lookup"><span data-stu-id="1343b-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="1343b-117">Modulis pirkšanai tiešsaistē un saņemšanai veikalā izmanto integrāciju ar Bing Maps programmas programmēšanas interfeisiem (API), lai atrastu tuvumā esošos veikalus vai veikalus citā vietā, ko norāda klients.</span><span class="sxs-lookup"><span data-stu-id="1343b-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="1343b-118">Iegādes lodziņa modulim ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="1343b-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="1343b-119">Šis ID tiek iegūts no lapas konteksta.</span><span class="sxs-lookup"><span data-stu-id="1343b-119">This ID is derived from the page context.</span></span> <span data-ttu-id="1343b-120">Ja iegādes lodziņa modulis ir pievienots lapai, kur lapas konteksts neietver preces ID, tas šo informāciju neatveidos pareizi.</span><span class="sxs-lookup"><span data-stu-id="1343b-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="1343b-121">Preces specifikāciju modulis</span><span class="sxs-lookup"><span data-stu-id="1343b-121">Product specifications module</span></span>

<span data-ttu-id="1343b-122">Preces specifikāciju modulis var tikt izmantots, lai parādītu papildu informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="1343b-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="1343b-123">Šī detalizētā informācija tiek ņemta no preces īpašībām programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="1343b-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="1343b-124">Preces specifikāciju modulis parāda katru īpašību, kur **redzams** rekvizīts ir iestatīts kā **patiess**.</span><span class="sxs-lookup"><span data-stu-id="1343b-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="1343b-125">Lai izgūtu preces īpašības, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="1343b-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="1343b-126">Ieteikumu modulis</span><span class="sxs-lookup"><span data-stu-id="1343b-126">Recommendations module</span></span>

<span data-ttu-id="1343b-127">Ieteikumu modulis ir svarīgs modulis PDP.</span><span class="sxs-lookup"><span data-stu-id="1343b-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="1343b-128">Kamēr klienti meklē preces, tiem jāsniedz vairāk preču opciju, lai klienti varētu atrast pareizo preci un veikt pirkumu.</span><span class="sxs-lookup"><span data-stu-id="1343b-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="1343b-129">Ieteikumi palīdz klientiem viegli atklāt saistīto saturu un turpināt iepirkties.</span><span class="sxs-lookup"><span data-stu-id="1343b-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="1343b-130">Ir pieejami dažādi ieteikumu sarakstu veidi.</span><span class="sxs-lookup"><span data-stu-id="1343b-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="1343b-131">Saraksts **Pircējiem patīk arī** ir balstīts uz mašīnmācību.</span><span class="sxs-lookup"><span data-stu-id="1343b-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="1343b-132">Lai sniegtu ieteikumus, tas izmanto citu klientu darījumu vēsturi.</span><span class="sxs-lookup"><span data-stu-id="1343b-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="1343b-133">Šo sarakstu ģenerē ieteikumu pakalpojums un tas līdzinās sarakstiem "Klientiem, kas iegādājušies šo, nopirka arī...".</span><span class="sxs-lookup"><span data-stu-id="1343b-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="1343b-134">Lai ģenerētu šo sarakstu, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="1343b-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="1343b-135">Sarakstu **Saistīts** precei ir iespējams konfigurēt programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="1343b-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="1343b-136">Piemēram, brūnai rokas ceļasomai no ādas saistītajā sarakstā var konfigurēt vairāk rokassomu, kas izgatavotas no ādas, vai paredzētas ceļošanai.</span><span class="sxs-lookup"><span data-stu-id="1343b-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="1343b-137">Citus saistīto sarakstu veidus, piemēram, **Piederumi** un **Vairāk līdzīgu preču** arī var konfigurēt programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="1343b-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="1343b-138">Lai ģenerētu šo sarakstu, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="1343b-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="1343b-139">Tāpēc, ja tas ir pievienots mājas lapai, kur lapas konteksts neietver preces ID, saraksts būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="1343b-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="1343b-140">Algoritmiski ģenerētie ieteikumu saraksti, piemēram, **Populārs**, **Vispirktākais** un **Jauns** var tikt izmantoti PDP.</span><span class="sxs-lookup"><span data-stu-id="1343b-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="1343b-141">Lai gan šie saraksti var nebūt tieši saistīti ar preci PDP, tas ir cits veids, kā palīdzēt klientiem atrast preces, kas varētu to interesēt.</span><span class="sxs-lookup"><span data-stu-id="1343b-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="1343b-142">Šiem sarakstu veidiem nav nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="1343b-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="1343b-143">Tie ir vispārēji saraksti, kas tiek ģenerēti, balstoties uz iepirkšanās paradumiem visā vietnē.</span><span class="sxs-lookup"><span data-stu-id="1343b-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="1343b-144">Rediģējamie saraksti ir manuāli pārraudzīti saraksti.</span><span class="sxs-lookup"><span data-stu-id="1343b-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="1343b-145">Piemēram, mazumtirgotājs var nolemt manuāli pārraudzīt to preču sarakstus, ko tas vēlas parādīt.</span><span class="sxs-lookup"><span data-stu-id="1343b-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="1343b-146">Vērtējumu un apskatu moduļi</span><span class="sxs-lookup"><span data-stu-id="1343b-146">Ratings and reviews modules</span></span>

<span data-ttu-id="1343b-147">Var izmantot trīs moduļus, lai parādītu un pievienotu pārskatus:</span><span class="sxs-lookup"><span data-stu-id="1343b-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="1343b-148">**Apskati** – Šis modulis parāda vērtējumus un apskatus, ko snieguši citi klienti.</span><span class="sxs-lookup"><span data-stu-id="1343b-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="1343b-149">Debitori var šķirot un filtrēt pārskatus.</span><span class="sxs-lookup"><span data-stu-id="1343b-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="1343b-150">Šis modulis ļauj arī klientiem atzinīgi vai negatīvi novērtēt apskatus, kā arī ziņot par problēmām.</span><span class="sxs-lookup"><span data-stu-id="1343b-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="1343b-151">**Rakstīt apskati** – Šis modulis ļauj klientiem rakstīt savus apskatus par preci.</span><span class="sxs-lookup"><span data-stu-id="1343b-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="1343b-152">**Vērtējumu histogramma** – šis modulis ietver histogrammu, kas parāda preces reitingu tendenci.</span><span class="sxs-lookup"><span data-stu-id="1343b-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="1343b-153">Papildinformāciju skatiet [Pārskats par vērtējumiem un apskatiem](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1343b-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="1343b-154">Mārketinga moduļi</span><span class="sxs-lookup"><span data-stu-id="1343b-154">Marketing modules</span></span>

<span data-ttu-id="1343b-155">Ja mārketinga saturs ir unikāls konkrētai precei, PDP var pievienot jebkuru mārketinga moduli.</span><span class="sxs-lookup"><span data-stu-id="1343b-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="1343b-156">Varat pievienot mārketinga moduļus PDP, izmantojot lapas "papildināšanu".</span><span class="sxs-lookup"><span data-stu-id="1343b-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="1343b-157">Plašāku informāciju skatiet [Preces lapas bagātināšana](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="1343b-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1343b-158">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1343b-158">Additional resources</span></span>

[<span data-ttu-id="1343b-159">Mājas lapas pārskats</span><span class="sxs-lookup"><span data-stu-id="1343b-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="1343b-160">Pārskats par grozu un norēķināšanās lapām</span><span class="sxs-lookup"><span data-stu-id="1343b-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="1343b-161">Konta pārvaldības lapu pārskats</span><span class="sxs-lookup"><span data-stu-id="1343b-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="1343b-162">Preces informācijas bagātināšanas lapa</span><span class="sxs-lookup"><span data-stu-id="1343b-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
