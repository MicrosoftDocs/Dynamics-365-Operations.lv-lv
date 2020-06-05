---
title: Veikala atlasītāja modulis
description: Šajā tēmā tiek stāstīts par veikala atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378212"
---
# <a name="store-selector-module"></a><span data-ttu-id="ff5b3-103">Veikala atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="ff5b3-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ff5b3-104">Šajā tēmā tiek stāstīts par veikala atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ff5b3-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ff5b3-105">Overview</span></span>

<span data-ttu-id="ff5b3-106">Veikala atlasītāja modulis tiek izmantots klienta scenārijā "pērk tiešsaistē, saņem veikalā" (BOPIS).</span><span class="sxs-lookup"><span data-stu-id="ff5b3-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="ff5b3-107">Tiek rādīts saraksts ar tiem veikaliem, kuros prece ir pieejama saņemšanai, kā arī veikala darba laiki un preču krājumi katram veikalam.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="ff5b3-108">Veikala atlasītāja modulim ir nepieciešams preces konteksts un meklēšanas vieta veikalu atrašanai.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="ff5b3-109">Ja nav meklēšanas vietas, tā pēc noklusējuma ir klienta pārlūka vieta, ja klients tam ir devis piekrišanu.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="ff5b3-110">Modulī ir ievades lodziņš, kas ļauj klientam ievadīt vietu (pasta indeksu vai pilsētu un rajonu), lai atrastu tuvumā esošos veikalus.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="ff5b3-111">Veikalu atlasīšanas modulis ir integrēts ar Bing karšu ģeokodēšanas lietojumprogrammas programmēšanas interfeisu (API), lai atrašanās vietu pārveidotu platumā un garumā.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="ff5b3-112">Nepieciešama Bing karšu API atslēga, un tā ir jāpievieno lapā Commerce kopīgie parametri pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ff5b3-113">Veikala atlasītāja moduli var pievienot pirkšanas kastes modulim preces informācijas lapā (PDP), lai parādītu veikalus, kuros prece ir pieejama saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="ff5b3-114">To var pievienot arī groza modulim.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-114">It can also be added to a cart module.</span></span> <span data-ttu-id="ff5b3-115">Veikala atlasītāja modulis pēc pievienošanas groza modulim rāda opcijas katras groza rindas elementam.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="ff5b3-116">Turklāt, izmantojot pielāgotu kodēšanu, šo moduli var pievienot citām lapām vai moduļiem, izmantojot paplašinājumus un pielāgojumus.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="ff5b3-117">Lai BOPIS scenārijs darbotos, precēm jābūt konfigurētām ar piegādes režīmu "saņem debitors".</span><span class="sxs-lookup"><span data-stu-id="ff5b3-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="ff5b3-118">Pretējā gadījumā modulis netiks uzrādīts attiecīgajās lapās.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="ff5b3-119">Plašāku informāciju par piegādes režīma konfigurēšanu skatiet rakstā [Piegādes veidu iestatīšana](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="ff5b3-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="ff5b3-120">Šajā attēlā redzams veikala atlasītāja moduļa piemērs, kas izmantots PDP.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Veikala atlasītāja moduļa piemērs](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="ff5b3-122">Veikala atlasītāja moduļa izmantošana e-komercijā</span><span class="sxs-lookup"><span data-stu-id="ff5b3-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="ff5b3-123">Veikala atlasītāja moduli var izmantot preces informācijas lapā (PDP), lai atrastu tuvumā esošus veikalus, kuros prece ir pieejama saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="ff5b3-124">Veikala atlasītāja moduli var izmantot groza lapā (PDP), lai atrastu tuvumā esošus veikalus, kuros grozs ir pieejama saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="ff5b3-125">Veikala atlasītāja moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="ff5b3-125">Store selector module properties</span></span>

| <span data-ttu-id="ff5b3-126">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="ff5b3-126">Property name</span></span>             | <span data-ttu-id="ff5b3-127">Vērtība</span><span class="sxs-lookup"><span data-stu-id="ff5b3-127">Value</span></span>                 | <span data-ttu-id="ff5b3-128">apraksts</span><span class="sxs-lookup"><span data-stu-id="ff5b3-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="ff5b3-129">Meklēšanas rādiuss</span><span class="sxs-lookup"><span data-stu-id="ff5b3-129">Search radius</span></span> | <span data-ttu-id="ff5b3-130">Skaits</span><span class="sxs-lookup"><span data-stu-id="ff5b3-130">Number</span></span> | <span data-ttu-id="ff5b3-131">Nosaka veikalu meklēšanas rādiusu jūdzēs.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="ff5b3-132">Ja nav norādīta vērtība, tiek izmantots noklusētais meklēšanas rādiuss, kas ir 50 jūdzes.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="ff5b3-133">Pakalpojuma noteikumi</span><span class="sxs-lookup"><span data-stu-id="ff5b3-133">Terms of Service</span></span> | <span data-ttu-id="ff5b3-134">Vietrādis URL</span><span class="sxs-lookup"><span data-stu-id="ff5b3-134">URL</span></span>    |  <span data-ttu-id="ff5b3-135">Bing karšu pakalpojumam nepieciešamā vietrāža URL pakalpojuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="ff5b3-136">Veikala atlasītāja moduļa pievienošana lapai</span><span class="sxs-lookup"><span data-stu-id="ff5b3-136">Add a store selector module to a page</span></span>

<span data-ttu-id="ff5b3-137">Veikala atlasītāja modulim ir nepieciešams preces konteksts, tāpēc to var izmantot tikai pirkšanas kastes un groza moduļos.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="ff5b3-138">Veikala atlasītāja moduļi nedarbojas ārpus šiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="ff5b3-139">Lai iegūtu informāciju par to, kā pievienot veikala atlasītāja moduli pirkšanas kastes modulim skatiet rakstu [Pirkšanas kastes modulis](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="ff5b3-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="ff5b3-140">Lai iegūtu informāciju par to, kā pievienot veikala atlasītāja moduli groza modulim skatiet rakstu [Groza modulis](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="ff5b3-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff5b3-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ff5b3-141">Additional resources</span></span>

[<span data-ttu-id="ff5b3-142">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="ff5b3-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ff5b3-143">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="ff5b3-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ff5b3-144">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="ff5b3-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ff5b3-145">Īss PDP apskats</span><span class="sxs-lookup"><span data-stu-id="ff5b3-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="ff5b3-146">Īss groza un norēķināšanās apskats</span><span class="sxs-lookup"><span data-stu-id="ff5b3-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="ff5b3-147">Iestatiet piegādes veidus</span><span class="sxs-lookup"><span data-stu-id="ff5b3-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="ff5b3-148">Bing karšu pārvaldība jūsu organizācijā</span><span class="sxs-lookup"><span data-stu-id="ff5b3-148">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)
