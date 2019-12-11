---
title: Preču detalizētas informācijas lapu apskats
description: Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697869"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="83029-103">Preču detalizētas informācijas lapu apskats</span><span class="sxs-lookup"><span data-stu-id="83029-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="83029-104">Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="83029-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="83029-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="83029-105">Overview</span></span>

<span data-ttu-id="83029-106">PDP sniedz detalizētu informāciju par preci, un ļaujiet klientiem izvēlēties preces opcijas, piemēram, izmēru, stilu un krāsu.</span><span class="sxs-lookup"><span data-stu-id="83029-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="83029-107">PDP ir jāparāda visa preces informācija, kas klientam nepieciešama, lai pieņemtu lēmumu par pirkšanu.</span><span class="sxs-lookup"><span data-stu-id="83029-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="83029-108">Tālāk redzamajā attēlā parādīts PDP piemērs.</span><span class="sxs-lookup"><span data-stu-id="83029-108">The following illustration shows an example of a PDP.</span></span>

![Preces detalizētas informācijas lapas piemērs](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="83029-110">Galvenes un kājenes moduļi</span><span class="sxs-lookup"><span data-stu-id="83029-110">Header and footer modules</span></span>

<span data-ttu-id="83029-111">PDP augšpusē ir virsraksts, kas parāda visas preču kategorijas un citas lapas, kuras mazumtirgotājs vēlas, lai klienti pārlūkotu.</span><span class="sxs-lookup"><span data-stu-id="83029-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="83029-112">Lapas apakšpusē ir kājene, kas ietver ātras saites uz dažādām tēmām, kas varētu interesēt pircējus.</span><span class="sxs-lookup"><span data-stu-id="83029-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="83029-113">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="83029-113">Buy box module</span></span>

<span data-ttu-id="83029-114">Vissvarīgākais modulis PDP ir iegādes lodziņa modulis.</span><span class="sxs-lookup"><span data-stu-id="83029-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="83029-115">Tāpēc tas ir pirmais vienums lapas galvenajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="83029-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="83029-116">Iegādes lodziņa modulis ir konteinera modulis, un tas vieso vairākus moduļus, kas satur svarīgāko informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="83029-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="83029-117">Šī informācija ietver preces nosaukumu, preces attēlus, aprakstu, cenu un preces vērtējumus.</span><span class="sxs-lookup"><span data-stu-id="83029-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="83029-118">Iegādes lodziņa modulis ļauj klientam izvēlēties preces opcijas (piemēram, izmēru, stilu un krāsu) un pievienot preci grozam.</span><span class="sxs-lookup"><span data-stu-id="83029-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="83029-119">Tas arī ļauj klientam nopirkt preci tiešsaistē un saņemt to veikalā.</span><span class="sxs-lookup"><span data-stu-id="83029-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="83029-120">Modulis pirkšanai tiešsaistē un saņemšanai veikalā izmanto integrāciju ar Bing Maps programmas programmēšanas interfeisiem (API), lai atrastu tuvumā esošos veikalus vai veikalus citā vietā, ko norāda klients.</span><span class="sxs-lookup"><span data-stu-id="83029-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="83029-121">Iegādes lodziņa modulim ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="83029-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="83029-122">Šis ID tiek iegūts no lapas konteksta.</span><span class="sxs-lookup"><span data-stu-id="83029-122">This ID is derived from the page context.</span></span> <span data-ttu-id="83029-123">Ja iegādes lodziņa modulis ir pievienots lapai, kur lapas konteksts neietver preces ID, tas šo informāciju neatveidos pareizi.</span><span class="sxs-lookup"><span data-stu-id="83029-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="83029-124">Preces specifikāciju modulis</span><span class="sxs-lookup"><span data-stu-id="83029-124">Product specifications module</span></span>

<span data-ttu-id="83029-125">Preces specifikāciju modulis var tikt izmantots, lai parādītu papildu informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="83029-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="83029-126">Šī detalizētā informācija tiek ņemta no preces īpašībām Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="83029-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="83029-127">Preces specifikāciju modulis parāda katru īpašību, kur **redzams** rekvizīts ir iestatīts kā **patiess**.</span><span class="sxs-lookup"><span data-stu-id="83029-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="83029-128">Lai izgūtu preces īpašības, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="83029-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="83029-129">Ieteikumu modulis</span><span class="sxs-lookup"><span data-stu-id="83029-129">Recommendations module</span></span>

<span data-ttu-id="83029-130">Ieteikumu modulis ir svarīgs modulis PDP.</span><span class="sxs-lookup"><span data-stu-id="83029-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="83029-131">Kamēr klienti meklē preces, tiem jāsniedz vairāk preču opciju, lai klienti varētu atrast pareizo preci un veikt pirkumu.</span><span class="sxs-lookup"><span data-stu-id="83029-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="83029-132">Ieteikumi palīdz klientiem viegli atklāt saistīto saturu un turpināt iepirkties.</span><span class="sxs-lookup"><span data-stu-id="83029-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="83029-133">Ir pieejami dažādi ieteikumu sarakstu veidi.</span><span class="sxs-lookup"><span data-stu-id="83029-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="83029-134">Saraksts **Pircējiem patīk arī** ir balstīts uz mašīnmācību.</span><span class="sxs-lookup"><span data-stu-id="83029-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="83029-135">Lai sniegtu ieteikumus, tas izmanto citu klientu transakciju vēsturi.</span><span class="sxs-lookup"><span data-stu-id="83029-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="83029-136">Šo sarakstu ģenerē ieteikumu pakalpojums un tas līdzinās sarakstiem "Klientiem, kas iegādājušies šo, nopirka arī...".</span><span class="sxs-lookup"><span data-stu-id="83029-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="83029-137">Lai ģenerētu šo sarakstu, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="83029-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="83029-138">Sarakstu **Saistīts** precei ir iespējams konfigurēt Retail.</span><span class="sxs-lookup"><span data-stu-id="83029-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="83029-139">Piemēram, brūnai rokas ceļasomai no ādas saistītajā sarakstā var konfigurēt vairāk rokassomu, kas izgatavotas no ādas, vai paredzētas ceļošanai.</span><span class="sxs-lookup"><span data-stu-id="83029-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="83029-140">Citus saistīto sarakstu veidus, piemēram, **Piederumi** un **Vairāk kā šis** arī var konfigurēt Retail.</span><span class="sxs-lookup"><span data-stu-id="83029-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="83029-141">Lai ģenerētu šo sarakstu, ir nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="83029-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="83029-142">Tāpēc, ja tas ir pievienots sākumlapai, kur lapas konteksts neietver preces ID, saraksts būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="83029-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="83029-143">Algoritmiski ģenerētie ieteikumu saraksti, piemēram, **Populārs**, **Vispirktākais** un **Jauns** var tikt izmantoti PDP.</span><span class="sxs-lookup"><span data-stu-id="83029-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="83029-144">Lai gan šie saraksti var nebūt tieši saistīti ar preci PDP, tas ir cits veids, kā palīdzēt klientiem atrast preces, kas varētu to interesēt.</span><span class="sxs-lookup"><span data-stu-id="83029-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="83029-145">Šiem sarakstu veidiem nav nepieciešams preces ID.</span><span class="sxs-lookup"><span data-stu-id="83029-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="83029-146">Tie ir vispārēji saraksti, kas tiek ģenerēti, balstoties uz iepirkšanās paradumiem visā vietnē.</span><span class="sxs-lookup"><span data-stu-id="83029-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="83029-147">Redakcionālie saraksti ir manuāli pārraudzīti saraksti.</span><span class="sxs-lookup"><span data-stu-id="83029-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="83029-148">Piemēram, mazumtirgotājs var nolemt manuāli pārraudzīt to preču sarakstus, ko tas vēlas parādīt.</span><span class="sxs-lookup"><span data-stu-id="83029-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="83029-149">Vērtējumu un apskatu modulis</span><span class="sxs-lookup"><span data-stu-id="83029-149">Ratings and reviews module</span></span>

<span data-ttu-id="83029-150">Vērtējumu un apskatu modulis parāda vērtējumus un apskatus, ko snieguši citi klienti.</span><span class="sxs-lookup"><span data-stu-id="83029-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="83029-151">Tas arī ļauj klientam uzrakstīt pašam savu preces apskatu.</span><span class="sxs-lookup"><span data-stu-id="83029-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="83029-152">Turklāt tajā ir ietverta histogramma, kas parāda preces vērtējumu tendenci.</span><span class="sxs-lookup"><span data-stu-id="83029-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="83029-153">Papildinformāciju skatiet [Pārskats par vērtējumiem un apskatiem](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83029-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="83029-154">Mārketinga moduļi</span><span class="sxs-lookup"><span data-stu-id="83029-154">Marketing modules</span></span>

<span data-ttu-id="83029-155">Ja mārketinga saturs ir unikāls konkrētai precei, PDP var pievienot jebkuru mārketinga moduli.</span><span class="sxs-lookup"><span data-stu-id="83029-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="83029-156">Varat pievienot mārketinga moduļus PDP, izmantojot lapas "papildināšanu".</span><span class="sxs-lookup"><span data-stu-id="83029-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="83029-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="83029-157">Additional resources</span></span>

[<span data-ttu-id="83029-158">Sākumlapas pārskats</span><span class="sxs-lookup"><span data-stu-id="83029-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="83029-159">Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas apskats</span><span class="sxs-lookup"><span data-stu-id="83029-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="83029-160">Pārskats par grozu un norēķināšanās lapām</span><span class="sxs-lookup"><span data-stu-id="83029-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="83029-161">Pārskats par konta pārvaldības lapām</span><span class="sxs-lookup"><span data-stu-id="83029-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
