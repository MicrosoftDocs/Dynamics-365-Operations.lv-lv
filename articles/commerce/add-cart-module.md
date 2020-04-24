---
title: Groza modulis
description: Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261425"
---
# <a name="cart-module"></a><span data-ttu-id="f0106-103">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f0106-104">Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0106-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f0106-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="f0106-105">Overview</span></span>

<span data-ttu-id="f0106-106">Groza modulis parāda krājumus, kas ir pievienoti grozam, pirms debitors turpina ar norēķināšanos.</span><span class="sxs-lookup"><span data-stu-id="f0106-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="f0106-107">Modulis arī parāda pasūtījuma kopsavilkumu un ļauj klientam piemērot vai noņemt veicināšanas kodus.</span><span class="sxs-lookup"><span data-stu-id="f0106-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="f0106-108">Groza modulis atbalsta pierakstīšanās un viesa norēķinu.</span><span class="sxs-lookup"><span data-stu-id="f0106-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="f0106-109">Tas atbalsta arī saiti **Atgriezties pie iepirkšanās**.</span><span class="sxs-lookup"><span data-stu-id="f0106-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="f0106-110">Jūs varat konfigurēt maršrutu šo saiti sadaļā **Vietnes iestatījumi \> Paplašinājumi \> Maršruti**.</span><span class="sxs-lookup"><span data-stu-id="f0106-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="f0106-111">Groza modulis veido datus, pamatojoties uz groza ID, kas ir visā vietnē pieejama pārlūka sīkdatne.</span><span class="sxs-lookup"><span data-stu-id="f0106-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="f0106-112">Groza moduļa rekvizīti un sloti</span><span class="sxs-lookup"><span data-stu-id="f0106-112">Cart module properties and slots</span></span>

<span data-ttu-id="f0106-113">Groza modulim ir rekvizīts **Virsraksts**, ko var iestatīt vērtībām, piemēram, **Iepirkumu grozs** un **Preces jūsu grozā**.</span><span class="sxs-lookup"><span data-stu-id="f0106-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="f0106-114">Moduļi, ko var izmantot groza modulī</span><span class="sxs-lookup"><span data-stu-id="f0106-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="f0106-115">**Teksta bloks** — šis modulis atbalsta pielāgotu ziņojumapmaiņu iepirkumu groza modulī.</span><span class="sxs-lookup"><span data-stu-id="f0106-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="f0106-116">Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS).</span><span class="sxs-lookup"><span data-stu-id="f0106-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="f0106-117">Var pievienot jebkuru ziņojumu, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="f0106-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="f0106-118">**Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci.</span><span class="sxs-lookup"><span data-stu-id="f0106-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="f0106-119">Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus.</span><span class="sxs-lookup"><span data-stu-id="f0106-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="f0106-120">Plašāku informāciju par šo moduli skatiet [Veikala atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="f0106-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="f0106-121">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="f0106-121">Module properties</span></span>

<span data-ttu-id="f0106-122">Groza moduļiem ir šādi iestatījumi, kurus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="f0106-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="f0106-123">**Maksimālais daudzums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam.</span><span class="sxs-lookup"><span data-stu-id="f0106-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="f0106-124">Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.</span><span class="sxs-lookup"><span data-stu-id="f0106-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="f0106-125">**Krājumu pārbaude** — ja vērtība ir iestatīta uz **Patiess**, prece tiek pievienota grozam tikai pēc tam, kad iegādes lodziņa modulis apstiprina, ka šī prece ir krājumos.</span><span class="sxs-lookup"><span data-stu-id="f0106-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="f0106-126">Šī krājuma pārbaude tiek veikta gadījumā, kad prece tiks nosūtīta, gan gadījumā, kad prece tiks saņemta veikalā.</span><span class="sxs-lookup"><span data-stu-id="f0106-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="f0106-127">Ja vērtība ir iestatīta uz **Nepatiess**, krājumu pārbaude netiek veikta pirms preces pievienošanas grozam un pasūtījuma veikšanas.</span><span class="sxs-lookup"><span data-stu-id="f0106-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="f0106-128">Lai iegūtu informāciju par to, kā konfigurēt krājumu iestatījumus aizmugurē, skatiet [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="f0106-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="f0106-129">**Krājumu buferis** — šis rekvizīts tiek izmantots, lai norādītu krājuma bufera numuru.</span><span class="sxs-lookup"><span data-stu-id="f0106-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="f0106-130">Krājumi tiek uzturēti reālajā laikā, un situācijā, kad daudzi klienti veic pasūtījumus, var būt sarežģīti uzturēt precīzu krājumu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="f0106-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="f0106-131">Kad ir veikta krājuma pārbaude, ja krājumi ir mazāki par buferā esošo daudzumu, tiek uzskatīts, ka prece vairs nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="f0106-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="f0106-132">Tāpēc, kad pārdošana notiek ātri, izmantojot vairākus kanālus, un krājumu uzskaite nav pilnībā sinhronizēta, pastāv mazāks risks, ka tiks pārdota prece, kas vairs nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="f0106-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="f0106-133">**Atgriezties pie iepirkšanās** — šis rekvizīts tiek izmantots, lai norādītu maršrutu saitei **Atgriezties pie iepirkšanās**.</span><span class="sxs-lookup"><span data-stu-id="f0106-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="f0106-134">Maršrutu var konfigurēt vietnes līmenī, ļaujot mazumtirgotājiem aizvest debitoru uz sākumlapu vai jebkuru citu vietnes lapu.</span><span class="sxs-lookup"><span data-stu-id="f0106-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="f0106-135">Commerce Scale Unit mijiedarbība</span><span class="sxs-lookup"><span data-stu-id="f0106-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="f0106-136">Groza modulis izgūst preču informāciju, izmantojot Commerce Scale Unit API.</span><span class="sxs-lookup"><span data-stu-id="f0106-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="f0106-137">Groza ID no pārlūka sīkfaila tiek izmantots, lai izgūtu visu informāciju par preci no Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="f0106-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="f0106-138">Groza moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="f0106-138">Add a cart module to a page</span></span>

<span data-ttu-id="f0106-139">Lai pievienotu groza moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="f0106-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f0106-140">Izveidojiet fragmentu ar nosaukumu **Groza fragments** un pievienojiet jaunajam fragmentam groza moduli.</span><span class="sxs-lookup"><span data-stu-id="f0106-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="f0106-141">Pievienojiet virsrakstu groza modulim.</span><span class="sxs-lookup"><span data-stu-id="f0106-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="f0106-142">Pievienojiet veikala atlasītāja moduli groza modulim.</span><span class="sxs-lookup"><span data-stu-id="f0106-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="f0106-143">Saglabājiet fragmentu, pabeidziet to rediģēt un publicējiet šo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f0106-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="f0106-144">Izveidojiet veidni ar nosaukumu **Groza veidne** un pievienojiet groza fragmentu, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="f0106-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="f0106-145">Saglabājiet veidni, pabeidziet to rediģēt un publicējiet šo veidni.</span><span class="sxs-lookup"><span data-stu-id="f0106-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="f0106-146">Izveidojiet lapu, kas izmanto jauno veidni.</span><span class="sxs-lookup"><span data-stu-id="f0106-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="f0106-147">Saglabājiet un priekšskatiet lapu.</span><span class="sxs-lookup"><span data-stu-id="f0106-147">Save and preview the page.</span></span>
1. <span data-ttu-id="f0106-148">Pabeidziet rediģēt lapu un šo lapu publicējiet.</span><span class="sxs-lookup"><span data-stu-id="f0106-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0106-149">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f0106-149">Additional resources</span></span>

[<span data-ttu-id="f0106-150">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="f0106-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f0106-151">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f0106-152">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="f0106-153">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f0106-154">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f0106-155">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f0106-156">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f0106-157">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f0106-158">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="f0106-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="f0106-159">Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem</span><span class="sxs-lookup"><span data-stu-id="f0106-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
