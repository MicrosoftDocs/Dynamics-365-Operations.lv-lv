---
title: Groza modulis
description: Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: 33db06ecfa2a8fa93cde3c4f1b31d6b30bfd0c34
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/07/2020
ms.locfileid: "4414207"
---
# <a name="cart-module"></a><span data-ttu-id="b8027-103">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8027-104">Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b8027-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b8027-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="b8027-105">Overview</span></span>

<span data-ttu-id="b8027-106">Groza modulis parāda krājumus, kas ir pievienoti grozam, pirms debitors turpina ar norēķināšanos.</span><span class="sxs-lookup"><span data-stu-id="b8027-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="b8027-107">Modulis arī parāda pasūtījuma kopsavilkumu un ļauj klientam piemērot vai noņemt veicināšanas kodus.</span><span class="sxs-lookup"><span data-stu-id="b8027-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="b8027-108">Groza modulis atbalsta pierakstīšanās un viesa norēķinu.</span><span class="sxs-lookup"><span data-stu-id="b8027-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="b8027-109">Tas atbalsta arī saiti **Atgriezties pie iepirkšanās**.</span><span class="sxs-lookup"><span data-stu-id="b8027-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="b8027-110">Jūs varat konfigurēt maršrutu šo saiti sadaļā **Vietnes iestatījumi \> Paplašinājumi \> Maršruti**.</span><span class="sxs-lookup"><span data-stu-id="b8027-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="b8027-111">Groza modulis atveido datus, pamatojoties uz groza ID, kas ir visā vietnē pieejama pārlūka sīkdatne.</span><span class="sxs-lookup"><span data-stu-id="b8027-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="b8027-112">Attēlā zemāk redzams groza lapas piemērs Fabrikam vietnē.</span><span class="sxs-lookup"><span data-stu-id="b8027-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Groza moduļa piemērs Fabrikam vietnē](./media/cart2.PNG)

<span data-ttu-id="b8027-114">Attēlā zemāk redzams groza lapas piemērs Fabrikam vietnē.</span><span class="sxs-lookup"><span data-stu-id="b8027-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="b8027-115">Šajā piemērā ir norādīta papildmaksa par rindas krājumu.</span><span class="sxs-lookup"><span data-stu-id="b8027-115">In this example, there is a handling fee for a line item.</span></span>

![Groza moduļa piemērs ar apstrādes komisiju rindas krājumam](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="b8027-117">Groza moduļa rekvizīti un sloti</span><span class="sxs-lookup"><span data-stu-id="b8027-117">Cart module properties and slots</span></span>

| <span data-ttu-id="b8027-118">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="b8027-118">Property</span></span> | <span data-ttu-id="b8027-119">Vērtības</span><span class="sxs-lookup"><span data-stu-id="b8027-119">Values</span></span> | <span data-ttu-id="b8027-120">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b8027-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b8027-121">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="b8027-121">Heading</span></span> | <span data-ttu-id="b8027-122">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="b8027-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b8027-123">Groza virsraksts, piemēram, "Iepirkumu soma", vai "Preces jūsu grozā".</span><span class="sxs-lookup"><span data-stu-id="b8027-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="b8027-124">Rādīt “Nav krājumā” kļūdas</span><span class="sxs-lookup"><span data-stu-id="b8027-124">Show out of stock errors</span></span> | <span data-ttu-id="b8027-125">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="b8027-125">**True** or **False**</span></span> | <span data-ttu-id="b8027-126">Ja šis rekvizīts ir iestatīts kā **Patiess**, groza lapā būs redzamas ar krājumu saistītas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="b8027-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="b8027-127">Ieteicams iestatīt šo rekvizītu kā **Patiess**, ja vietnē tiek lietotas krājumu pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="b8027-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="b8027-128">Rādīt rindu vienību piegādes izmaksas</span><span class="sxs-lookup"><span data-stu-id="b8027-128">Show shipping charges for line items</span></span> | <span data-ttu-id="b8027-129">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="b8027-129">**True** or **False**</span></span> | <span data-ttu-id="b8027-130">Ja šis rekvizīts ir iestatīts kā **Patiess**, groza rindas krājumi rādīs piegādes izmaksas, ja šī informācija ir pieejama.</span><span class="sxs-lookup"><span data-stu-id="b8027-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="b8027-131">Šis līdzeklis netiek atbalstīts Fabrikam tēmā, jo lietotāji atlasa piegādi tikai izrakstīšanās plūsmā.</span><span class="sxs-lookup"><span data-stu-id="b8027-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="b8027-132">Tomēr šo līdzekli var ieslēgt citās darbplūsmās, ja tas ir piemērojams.</span><span class="sxs-lookup"><span data-stu-id="b8027-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="b8027-133">Moduļi, ko var izmantot groza modulī</span><span class="sxs-lookup"><span data-stu-id="b8027-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="b8027-134">**Teksta bloks** — šis modulis atbalsta pielāgotu ziņojumapmaiņu iepirkumu groza modulī.</span><span class="sxs-lookup"><span data-stu-id="b8027-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="b8027-135">Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS).</span><span class="sxs-lookup"><span data-stu-id="b8027-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="b8027-136">Var pievienot jebkuru ziņojumu, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="b8027-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="b8027-137">**Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci.</span><span class="sxs-lookup"><span data-stu-id="b8027-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="b8027-138">Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus.</span><span class="sxs-lookup"><span data-stu-id="b8027-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="b8027-139">Plašāku informāciju par šo moduli skatiet [Veikala atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="b8027-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="b8027-140">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="b8027-140">Module properties</span></span>

<span data-ttu-id="b8027-141">Groza moduļa iestatījumiem ir šādi iestatījumi, kurus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="b8027-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="b8027-142">**Maksimālais daudzums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam.</span><span class="sxs-lookup"><span data-stu-id="b8027-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="b8027-143">Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.</span><span class="sxs-lookup"><span data-stu-id="b8027-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="b8027-144">**Krājumi** — papildinformāciju par to, kā lietot krājumu iestatījumus, skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="b8027-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="b8027-145">**Atgriezties pie iepirkšanās** — šis rekvizīts tiek izmantots, lai norādītu maršrutu saitei **Atgriezties pie iepirkšanās**.</span><span class="sxs-lookup"><span data-stu-id="b8027-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="b8027-146">Maršrutu var konfigurēt vietnes līmenī, ļaujot mazumtirgotājiem aizvest debitoru uz sākumlapu vai jebkuru citu vietnes lapu.</span><span class="sxs-lookup"><span data-stu-id="b8027-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8027-147">Dynamics 365 Commerce 10.0.14 laidienā un vēlākos laidienos preces grozā tiek apkopotas, pamatojoties uz iestatījumiem, kas definēti tiešsaistes funkcionalitātes profilā tiešsaistes veikalam programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b8027-147">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="b8027-148">Papildinformāciju par to, kā izveidot tiešsaistes funkcionalitātes profilu un iestatīt rekvizītus, kas nepieciešami apkopošanai, skatiet sadaļā [Tiešsaistes funkcionalitātes profila izveide](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="b8027-148">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="b8027-149">Commerce Scale Unit mijiedarbība</span><span class="sxs-lookup"><span data-stu-id="b8027-149">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="b8027-150">Groza modulis izgūst preču informāciju, izmantojot Commerce Scale Unit API.</span><span class="sxs-lookup"><span data-stu-id="b8027-150">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="b8027-151">Groza ID no pārlūka sīkfaila tiek izmantots, lai izgūtu visu informāciju par preci no Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="b8027-151">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="b8027-152">Groza moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="b8027-152">Add a cart module to a page</span></span>

<span data-ttu-id="b8027-153">Lai pievienotu groza moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="b8027-153">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b8027-154">Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.</span><span class="sxs-lookup"><span data-stu-id="b8027-154">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b8027-155">Dialoglodziņā **Jauns fragments** atlasiet moduli **Grozs**.</span><span class="sxs-lookup"><span data-stu-id="b8027-155">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="b8027-156">Sadaļā **Fragmenta nosaukums** ievadiet nosaukumu **Groza fragments** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b8027-156">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="b8027-157">Atlasiet slotu **Grozs**.</span><span class="sxs-lookup"><span data-stu-id="b8027-157">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="b8027-158">Rekvizītu rūts labajā pusē atlasiet zīmuļa simbolu, ievadiet virsraksta tekstu laukā un pēc tam atlasiet atzīmes simbolu.</span><span class="sxs-lookup"><span data-stu-id="b8027-158">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="b8027-159">Slotā **Grozs** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="b8027-159">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b8027-160">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veikalu atlasītājs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b8027-160">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b8027-161">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="b8027-161">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b8027-162">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="b8027-162">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b8027-163">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b8027-163">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="b8027-164">Struktūras kokā atlasiet slotu **Pamatteksts**, atlasiet daudzpunktess (**...**), un pēc tam atlasiet **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="b8027-164">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="b8027-165">Dialoglodziņā **Atlasīt fragmentu** atlasiet fragmentu **Groza fragments** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b8027-165">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b8027-166">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="b8027-166">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b8027-167">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="b8027-167">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b8027-168">Dialoglodziņā **Izvēlēties veidni** atlasiet iepriekš izveidoto veidni, ievadiet lapas nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b8027-168">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="b8027-169">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="b8027-169">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="b8027-170">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="b8027-170">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8027-171">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b8027-171">Additional resources</span></span>

[<span data-ttu-id="b8027-172">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-172">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b8027-173">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-173">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b8027-174">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-174">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b8027-175">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-175">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b8027-176">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-176">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b8027-177">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-177">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b8027-178">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-178">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b8027-179">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="b8027-179">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="b8027-180">Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem</span><span class="sxs-lookup"><span data-stu-id="b8027-180">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="b8027-181">Izveidot tiešsaistes funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="b8027-181">Create an online functionality profile</span></span>](online-functionality-profile.md)
