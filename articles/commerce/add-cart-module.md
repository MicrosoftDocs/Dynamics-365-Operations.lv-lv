---
title: Groza modulis
description: Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025440"
---
# <a name="cart-module"></a><span data-ttu-id="30146-103">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="30146-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="30146-104">Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="30146-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30146-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="30146-105">Overview</span></span>

<span data-ttu-id="30146-106">Groza modulis tiek izmantots, lai parādītu krājumus, kas ir pievienoti grozam, pirms debitors turpina ar norēķināšanos.</span><span class="sxs-lookup"><span data-stu-id="30146-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="30146-107">Piemēram, tas ietver visus elementus, kas tika pievienoti grozam un pasūtījuma kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="30146-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="30146-108">Tas ļauj debitoram arī lietot vai noņemt veicināšanas kodus.</span><span class="sxs-lookup"><span data-stu-id="30146-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="30146-109">Groza modulis atbalsta pierakstīšanās un viesa norēķinu.</span><span class="sxs-lookup"><span data-stu-id="30146-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="30146-110">Tas atbalsta arī saiti **Atgriezties pie iepirkšanās**.</span><span class="sxs-lookup"><span data-stu-id="30146-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="30146-111">Jūs varat konfigurēt maršrutu šo saiti sadaļā **Vietnes iestatījumi \> Paplašinājumi \> Maršruti**.</span><span class="sxs-lookup"><span data-stu-id="30146-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="30146-112">Groza modulis atveido datus, pamatojoties uz groza ID.</span><span class="sxs-lookup"><span data-stu-id="30146-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="30146-113">Groza ID ir pārlūkprogrammas sīkfails, kas ir pieejams visā vietnē.</span><span class="sxs-lookup"><span data-stu-id="30146-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="30146-114">Groza moduļa rekvizīti un sloti</span><span class="sxs-lookup"><span data-stu-id="30146-114">Cart module properties and slots</span></span>

<span data-ttu-id="30146-115">Groza modulim ir rekvizīts **Virsraksts**, ko var iestatīt vērtībām, piemēram, **Iepirkumu grozs** un **Preces jūsu grozā**.</span><span class="sxs-lookup"><span data-stu-id="30146-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="30146-116">Moduļi, ko var izmantot groza modulī</span><span class="sxs-lookup"><span data-stu-id="30146-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="30146-117">**Teksta bloks** — šis modulis atbalsta pielāgotu ziņojumapmaiņu iepirkumu groza modulī.</span><span class="sxs-lookup"><span data-stu-id="30146-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="30146-118">Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS).</span><span class="sxs-lookup"><span data-stu-id="30146-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="30146-119">Var pievienot jebkuru ziņojumu, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="30146-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="30146-120">**Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci.</span><span class="sxs-lookup"><span data-stu-id="30146-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="30146-121">Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus.</span><span class="sxs-lookup"><span data-stu-id="30146-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="30146-122">Veikalu atlasīšanas modulis ir integrēts ar Bing karšu ģeokodēšanas lietojumprogrammas programmēšanas interfeisu (API), lai atrašanās vietu pārveidotu platumā un garumā.</span><span class="sxs-lookup"><span data-stu-id="30146-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="30146-123">Nepieciešama Bing karšu API atslēga, un tā ir jāpievieno lapā Mazumtirdzniecības kopīgie parametri pakalpojumā Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="30146-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="30146-124">Šis modulis atbalsta divus rekvizītus — **Meklēšanas rādiuss** un **Pakalpojuma noteikumu saite**.</span><span class="sxs-lookup"><span data-stu-id="30146-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="30146-125">Rekvizīts **Meklēšanas rādiuss** nosaka meklēšanas rādiusu veikaliem jūdzēs.</span><span class="sxs-lookup"><span data-stu-id="30146-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="30146-126">Ja nav norādīta vērtība, tiek izmantots noklusētais meklēšanas rādiuss, kas ir 50 km.</span><span class="sxs-lookup"><span data-stu-id="30146-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="30146-127">Ja tiek izmantotas Bing kartes vai jebkurš ārējs pakalpojums, rekvizīts **Pakalpojuma noteikumu saite** var tikt izmantots, lai nodrošinātu saiti uz pakalpojuma noteikumiem.</span><span class="sxs-lookup"><span data-stu-id="30146-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="30146-128">Bing karšu pakalpojumam ir nepieciešama saite uz pakalpojuma noteikumiem.</span><span class="sxs-lookup"><span data-stu-id="30146-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="30146-129">Groza moduļa iestatījumi</span><span class="sxs-lookup"><span data-stu-id="30146-129">Cart module settings</span></span>

<span data-ttu-id="30146-130">Groza moduļiem ir šādi iestatījumi, kurus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="30146-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="30146-131">**Maksimālais daudzums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam.</span><span class="sxs-lookup"><span data-stu-id="30146-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="30146-132">Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.</span><span class="sxs-lookup"><span data-stu-id="30146-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="30146-133">**Krājumu pārbaude** — ja vērtība ir iestatīta uz **Patiess**, prece tiek pievienota grozam tikai pēc tam, kad iegādes lodziņa modulis apstiprina, ka šī prece ir krājumos.</span><span class="sxs-lookup"><span data-stu-id="30146-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="30146-134">Šī krājuma pārbaude tiek veikta gan gadījumam, kad prece tiks nosūtīta, gan gadījumam, kur prece tiks saņemta veikalā.</span><span class="sxs-lookup"><span data-stu-id="30146-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="30146-135">Ja vērtība ir iestatīta uz **Nepatiess**, krājumu pārbaude netiek veikta pirms preces pievienošanas grozam un pasūtījuma veikšanas.</span><span class="sxs-lookup"><span data-stu-id="30146-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="30146-136">**Krājumu buferis** — šis rekvizīts tiek izmantots, lai norādītu krājuma bufera numuru.</span><span class="sxs-lookup"><span data-stu-id="30146-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="30146-137">Krājumi tiek uzturēti reālajā laikā, un situācijā, kad daudzi klienti veic pasūtījumus, var būt sarežģīti uzturēt precīzu krājumu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="30146-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="30146-138">Kad ir veikta krājuma pārbaude, ja krājumi ir mazāki par buferā esošo daudzumu, tiek uzskatīts, ka prece vairs nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="30146-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="30146-139">Tāpēc, kad pārdošana notiek ātri, izmantojot vairākus kanālus, un krājumu uzskaite nav pilnībā sinhronizēta, pastāv mazāks risks, ka tiks pārdota prece, kas vairs nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="30146-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="30146-140">**Atgriezties pie iepirkšanās** — šis rekvizīts tiek izmantots, lai norādītu maršrutu saitei **Atgriezties pie iepirkšanās**.</span><span class="sxs-lookup"><span data-stu-id="30146-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="30146-141">Šo maršrutu var konfigurēt vietnes līmenī.</span><span class="sxs-lookup"><span data-stu-id="30146-141">This route can be configured at the site level.</span></span> <span data-ttu-id="30146-142">Šī konfigurācija ļauj mazumtirgotājiem novirzīt klientu uz sākumlapu vai jebkuru citu vietnes lapu.</span><span class="sxs-lookup"><span data-stu-id="30146-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="30146-143">Commerce Scale Unit mijiedarbība</span><span class="sxs-lookup"><span data-stu-id="30146-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="30146-144">Groza modulis izgūst preču informāciju, izmantojot Commerce Scale Unit API.</span><span class="sxs-lookup"><span data-stu-id="30146-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="30146-145">Groza ID no pārlūka sīkfaila tiek izmantots, lai izgūtu visu informāciju par preci no Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="30146-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="30146-146">Groza moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="30146-146">Add a cart module to a page</span></span>

<span data-ttu-id="30146-147">Lai pievienotu groza moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="30146-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="30146-148">Izveidojiet fragmentu ar nosaukumu **Groza fragments** un pievienojiet tam groza moduli.</span><span class="sxs-lookup"><span data-stu-id="30146-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="30146-149">Pievienojiet virsrakstu groza modulim.</span><span class="sxs-lookup"><span data-stu-id="30146-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="30146-150">Pievienojiet veikala atlasītāja moduli groza modulim.</span><span class="sxs-lookup"><span data-stu-id="30146-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="30146-151">Saglabājiet lapas fragmentu, pabeidziet to rediģēt un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="30146-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="30146-152">Izveidojiet veidni ar nosaukumu **Groza veidne** un pievienojiet groza fragmentu, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="30146-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="30146-153">Saglabājiet veidni, pabeidziet to rediģēt un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="30146-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="30146-154">Izveidojiet lapu, kas izmanto jauno veidni.</span><span class="sxs-lookup"><span data-stu-id="30146-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="30146-155">Saglabājiet un priekšskatiet lapu.</span><span class="sxs-lookup"><span data-stu-id="30146-155">Save and preview the page.</span></span>
1. <span data-ttu-id="30146-156">Pabeidziet rediģēt lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="30146-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30146-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="30146-157">Additional resources</span></span>

[<span data-ttu-id="30146-158">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="30146-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="30146-159">Container modulis</span><span class="sxs-lookup"><span data-stu-id="30146-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="30146-160">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="30146-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="30146-161">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="30146-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="30146-162">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="30146-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="30146-163">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="30146-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="30146-164">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="30146-164">Footer module</span></span>](author-footer-module.md)
