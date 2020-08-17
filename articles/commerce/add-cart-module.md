---
title: Groza modulis
description: Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621040"
---
# <a name="cart-module"></a><span data-ttu-id="82e14-103">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="82e14-104">Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="82e14-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="82e14-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="82e14-105">Overview</span></span>

<span data-ttu-id="82e14-106">Groza modulis parāda krājumus, kas ir pievienoti grozam, pirms debitors turpina ar norēķināšanos.</span><span class="sxs-lookup"><span data-stu-id="82e14-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="82e14-107">Modulis arī parāda pasūtījuma kopsavilkumu un ļauj klientam piemērot vai noņemt veicināšanas kodus.</span><span class="sxs-lookup"><span data-stu-id="82e14-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="82e14-108">Groza modulis atbalsta pierakstīšanās un viesa norēķinu.</span><span class="sxs-lookup"><span data-stu-id="82e14-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="82e14-109">Tas atbalsta arī saiti **Atgriezties pie iepirkšanās**.</span><span class="sxs-lookup"><span data-stu-id="82e14-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="82e14-110">Jūs varat konfigurēt maršrutu šo saiti sadaļā **Vietnes iestatījumi \> Paplašinājumi \> Maršruti**.</span><span class="sxs-lookup"><span data-stu-id="82e14-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="82e14-111">Groza modulis atveido datus, pamatojoties uz groza ID, kas ir visā vietnē pieejama pārlūka sīkdatne.</span><span class="sxs-lookup"><span data-stu-id="82e14-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="82e14-112">Attēlā zemāk redzams groza lapas piemērs Fabrikam vietnē.</span><span class="sxs-lookup"><span data-stu-id="82e14-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Groza moduļa piemērs](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="82e14-114">Groza moduļa rekvizīti un sloti</span><span class="sxs-lookup"><span data-stu-id="82e14-114">Cart module properties and slots</span></span>

<span data-ttu-id="82e14-115">Groza modulim ir rekvizīts **Virsraksts**, ko var iestatīt vērtībām, piemēram, **Iepirkumu grozs** un **Preces jūsu grozā**.</span><span class="sxs-lookup"><span data-stu-id="82e14-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="82e14-116">Moduļi, ko var izmantot groza modulī</span><span class="sxs-lookup"><span data-stu-id="82e14-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="82e14-117">**Teksta bloks** — šis modulis atbalsta pielāgotu ziņojumapmaiņu iepirkumu groza modulī.</span><span class="sxs-lookup"><span data-stu-id="82e14-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="82e14-118">Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS).</span><span class="sxs-lookup"><span data-stu-id="82e14-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="82e14-119">Var pievienot jebkuru ziņojumu, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="82e14-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="82e14-120">**Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci.</span><span class="sxs-lookup"><span data-stu-id="82e14-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="82e14-121">Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus.</span><span class="sxs-lookup"><span data-stu-id="82e14-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="82e14-122">Plašāku informāciju par šo moduli skatiet [Veikala atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="82e14-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="82e14-123">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="82e14-123">Module properties</span></span>

<span data-ttu-id="82e14-124">Groza moduļa iestatījumiem ir šādi iestatījumi, kurus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="82e14-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="82e14-125">**Maksimālais daudzums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam.</span><span class="sxs-lookup"><span data-stu-id="82e14-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="82e14-126">Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.</span><span class="sxs-lookup"><span data-stu-id="82e14-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="82e14-127">**Krājumi** — papildinformāciju par to, kā lietot krājumu iestatījumus, skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="82e14-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="82e14-128">**Atgriezties pie iepirkšanās** — šis rekvizīts tiek izmantots, lai norādītu maršrutu saitei **Atgriezties pie iepirkšanās**.</span><span class="sxs-lookup"><span data-stu-id="82e14-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="82e14-129">Maršrutu var konfigurēt vietnes līmenī, ļaujot mazumtirgotājiem aizvest debitoru uz sākumlapu vai jebkuru citu vietnes lapu.</span><span class="sxs-lookup"><span data-stu-id="82e14-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="82e14-130">Commerce Scale Unit mijiedarbība</span><span class="sxs-lookup"><span data-stu-id="82e14-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="82e14-131">Groza modulis izgūst preču informāciju, izmantojot Commerce Scale Unit API.</span><span class="sxs-lookup"><span data-stu-id="82e14-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="82e14-132">Groza ID no pārlūka sīkfaila tiek izmantots, lai izgūtu visu informāciju par preci no Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="82e14-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="82e14-133">Groza moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="82e14-133">Add a cart module to a page</span></span>

<span data-ttu-id="82e14-134">Lai pievienotu groza moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="82e14-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="82e14-135">Dodieties uz **Lapas fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.</span><span class="sxs-lookup"><span data-stu-id="82e14-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="82e14-136">Dialoglodziņā **Jaunas lapas fragments** atlasiet moduli **Grozs**.</span><span class="sxs-lookup"><span data-stu-id="82e14-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="82e14-137">Sadaļā **Lapas fragmenta nosaukums** ievadiet nosaukumu **Groza fragments** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="82e14-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="82e14-138">Atlasiet slotu **Grozs**.</span><span class="sxs-lookup"><span data-stu-id="82e14-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="82e14-139">Rekvizītu rūts labajā pusē atlasiet zīmuļa simbolu, ievadiet virsraksta tekstu laukā un pēc tam atlasiet atzīmes simbolu.</span><span class="sxs-lookup"><span data-stu-id="82e14-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="82e14-140">Slotā **Grozs** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="82e14-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="82e14-141">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veikalu atlasītājs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="82e14-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="82e14-142">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="82e14-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="82e14-143">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="82e14-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="82e14-144">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="82e14-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="82e14-145">Struktūras kokā atlasiet slotu **Pamatteksts**, atlasiet daudzpunktess (**...**) un pēc tam atlasiet **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="82e14-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="82e14-146">Dialoglodziņā **Atlasīt lapas fragmentu** atlasiet fragmentu **Groza fragments** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="82e14-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="82e14-147">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="82e14-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="82e14-148">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="82e14-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="82e14-149">Dialoglodziņā **Izvēlēties veidni** atlasiet iepriekš izveidoto veidni, ievadiet lapas nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="82e14-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="82e14-150">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="82e14-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="82e14-151">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="82e14-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82e14-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="82e14-152">Additional resources</span></span>

[<span data-ttu-id="82e14-153">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="82e14-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="82e14-154">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="82e14-155">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="82e14-156">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="82e14-157">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="82e14-158">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="82e14-159">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="82e14-160">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="82e14-161">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="82e14-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="82e14-162">Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem</span><span class="sxs-lookup"><span data-stu-id="82e14-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
