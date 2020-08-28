---
title: Iegādes lodziņa modulis
description: Šajā tēmā tiek stāstīts par iegādes lodziņa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fe5c1eb5808ef778aeda29442fa884556671296
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686674"
---
# <a name="buy-box-module"></a><span data-ttu-id="6d934-103">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6d934-104">Šajā tēmā tiek stāstīts par iegādes lodziņa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6d934-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6d934-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="6d934-105">Overview</span></span>

<span data-ttu-id="6d934-106">Termins *iegādes lodziņš* tipiski tiek attiecināts uz preces informācijas lapas apgabalu, kas ir “virs ieloces” un kurā ir ietverta visa svarīgākā informācija, kas nepieciešama preces pirkuma veikšanai.</span><span class="sxs-lookup"><span data-stu-id="6d934-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="6d934-107">(Apgabals, kas ir “virs ieloces”, ir redzams, kad lapa tiek ielādēta pirmo reizi, lai lietotājiem skatīšanai nebūtu jāritina uz leju.)</span><span class="sxs-lookup"><span data-stu-id="6d934-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="6d934-108">Iegādes lodziņa modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu visus moduļus, kas parādīti preces informācijas lapas iegādes lodziņā.</span><span class="sxs-lookup"><span data-stu-id="6d934-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="6d934-109">Preces informācijas lapas vietrādī URL ir ietverta preces ID.</span><span class="sxs-lookup"><span data-stu-id="6d934-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="6d934-110">Visa informācija, kas nepieciešama iegādes lodziņa moduļa atveidošanai, tiek atvasināta no šīs preces ID.</span><span class="sxs-lookup"><span data-stu-id="6d934-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="6d934-111">Ja preces ID nav norādīts, iegādes lodziņa modulis netiks pareizi atveidots lapā.</span><span class="sxs-lookup"><span data-stu-id="6d934-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="6d934-112">Tāpēc iegādes loga moduli var izmantot tikai lapās, kurās ir preces konteksts.</span><span class="sxs-lookup"><span data-stu-id="6d934-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="6d934-113">Lai to izmantotu lapā, kurā nav preces konteksta (piemēram, mājaslapa vai mārketinga lapa), jāveic papildu pielāgojumi.</span><span class="sxs-lookup"><span data-stu-id="6d934-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="6d934-114">Attēlā zemāk redzams iegādes lodziņa moduļa piemērs preces informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="6d934-114">The following image shows an example of a buy box module on a product details page.</span></span>

![Iegādes lodziņa moduļa piemērs](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="6d934-116">Iegādes lodziņa moduļa rekvizīti un sloti</span><span class="sxs-lookup"><span data-stu-id="6d934-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="6d934-117">Preces informācijas lapā iegādes lodziņš ir sadalīts divos reģionos: multivides reģions kreisajā pusē un satura reģions labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="6d934-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="6d934-118">Pēc noklusējuma multivides reģiona kolonnas platuma proporcija uz satura apgabala kolonnas platumu ir 2:1.</span><span class="sxs-lookup"><span data-stu-id="6d934-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="6d934-119">Mobilajās ierīcēs abi reģioni ir grupēti. Tādējādi viens reģions tiek parādīts zem cita reģiona.</span><span class="sxs-lookup"><span data-stu-id="6d934-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="6d934-120">Tēmas var izmantot, lai pielāgotu kolonnu platumus un salikšanas rangu.</span><span class="sxs-lookup"><span data-stu-id="6d934-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="6d934-121">Iegādes loga modulis atveido preces nosaukumu, aprakstu, cenu un vērtējumus.</span><span class="sxs-lookup"><span data-stu-id="6d934-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="6d934-122">Tas arī ļauj klientiem izvēlēties preces variantus, kuriem ir dažādas preces īpašības, piemēram, lielums, stils un krāsa.</span><span class="sxs-lookup"><span data-stu-id="6d934-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="6d934-123">Ja ir atlasīts preces variants, tad tiek atjaunināti citi rekvizīti iegādes lodziņā (piemēram, produkta apraksts un attēli), lai atspoguļotu informāciju par variantu.</span><span class="sxs-lookup"><span data-stu-id="6d934-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="6d934-124">Tiek nodrošināts daudzuma atlasītājs, lai klienti varētu norādīt pērkamo vienumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6d934-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="6d934-125">Maksimālo daudzumu, ko var iegādāties, var definēt vietnes iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="6d934-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="6d934-126">No iegādes loga klienti var veikt arī darbības, piemēram, pievienot preci grozam, pievienot produktu vēlmju sarakstam un izvēlēties saņemšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="6d934-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="6d934-127">Šīs darbības var veikt ar preci vai preces variantu.</span><span class="sxs-lookup"><span data-stu-id="6d934-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="6d934-128">Lai preci pievienotu vēlmju sarakstam, klientam jābūt reģistrētam sistēmā.</span><span class="sxs-lookup"><span data-stu-id="6d934-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="6d934-129">Tēmas var izmantot, lai noņemtu vai mainītu iegādes loga produktu rekvizītu un darbības kontroļu kārtību.</span><span class="sxs-lookup"><span data-stu-id="6d934-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="6d934-130">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="6d934-130">Module properties</span></span>

- <span data-ttu-id="6d934-131">**Galvenes etiķete** — šis rekvizīts definē galvenes etiķeti preces nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="6d934-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="6d934-132">Ja iegādes logs atrodas lapas augšā, šis rekvizīts ir jāiestata uz **h1**, lai atbilstu pieejamības standartiem.</span><span class="sxs-lookup"><span data-stu-id="6d934-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="6d934-133">Moduļi, ko var izmantot iegādes lodziņa modulī</span><span class="sxs-lookup"><span data-stu-id="6d934-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="6d934-134">**Multivides galerija** — šis modulis tiek izmantots, lai parādītu preču attēlus preču informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="6d934-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="6d934-135">Plašāku informāciju par šo moduli skatiet [Multivides galerijas modulis](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="6d934-135">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="6d934-136">**Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci.</span><span class="sxs-lookup"><span data-stu-id="6d934-136">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="6d934-137">Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus.</span><span class="sxs-lookup"><span data-stu-id="6d934-137">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="6d934-138">Plašāku informāciju par šo moduli skatiet [Veikalu atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="6d934-138">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="6d934-139">Iegādes lodziņa moduļa iestatījumi</span><span class="sxs-lookup"><span data-stu-id="6d934-139">Buy box module settings</span></span>

<span data-ttu-id="6d934-140">Iegādes lodziņa moduļa iestatījumus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-140">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="6d934-141">**Groza rindu daudzuma ierobežojums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam.</span><span class="sxs-lookup"><span data-stu-id="6d934-141">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="6d934-142">Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.</span><span class="sxs-lookup"><span data-stu-id="6d934-142">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="6d934-143">**Krājumi** — papildinformāciju par to, kā lietot krājumu iestatījumus, skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="6d934-143">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="6d934-144">**Pievienot grozam** — šis rekvizīts tiek izmantots, lai noteiktu uzvedību pēc krājuma pievienošanas grozam.</span><span class="sxs-lookup"><span data-stu-id="6d934-144">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="6d934-145">Iespējamās vērtības ir **Doties uz grozu**, **Nedoties uz grozu** un **Parādīt paziņojumus**.</span><span class="sxs-lookup"><span data-stu-id="6d934-145">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="6d934-146">Kad vērtība ir iestatīta uz **Doties uz grozu**, lietotāji pēc krājuma pievienošanas tiek nosūtīti uz groza lapu.</span><span class="sxs-lookup"><span data-stu-id="6d934-146">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="6d934-147">Kad vērtība ir iestatīta uz **Nedoties uz grozu**, lietotāji pēc krājuma pievienošanas netiek nosūtīti uz groza lapu.</span><span class="sxs-lookup"><span data-stu-id="6d934-147">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="6d934-148">Kad vērtība ir iestatīta **Rādīt paziņojumus**, lietotājiem tiek parādīts apstiprinājuma paziņojums un viņi turpināt pārlūkot preces informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="6d934-148">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="6d934-149">Attēlā zemāk redzams "pievienots grozam" apstiprinājuma paziņojuma piemērs Fabrikam vietnē.</span><span class="sxs-lookup"><span data-stu-id="6d934-149">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![Paziņojuma moduļa piemērs](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="6d934-151">Commerce Scale Unit mijiedarbība</span><span class="sxs-lookup"><span data-stu-id="6d934-151">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="6d934-152">Iegādes lodziņa modulis izgūst preču informāciju, izmantojot Commerce Scale Unit pieteikuma programmēšanas interfeisus (API).</span><span class="sxs-lookup"><span data-stu-id="6d934-152">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="6d934-153">Preces ID no preces informācijas lapas tiek izmantots visas informācijas izgūšanai.</span><span class="sxs-lookup"><span data-stu-id="6d934-153">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="6d934-154">Iegādes lodziņa moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="6d934-154">Add a buy box module to a page</span></span>

<span data-ttu-id="6d934-155">Lai pievienotu iegādes lodziņa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="6d934-155">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6d934-156">Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.</span><span class="sxs-lookup"><span data-stu-id="6d934-156">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="6d934-157">Dialoglodziņā **Jaunas lapas fragments** atlasiet moduli **Iegādes lodziņš**.</span><span class="sxs-lookup"><span data-stu-id="6d934-157">In the **New page fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="6d934-158">Sadaļā **Lapas fragmenta nosaukums** ievadiet nosaukumu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-158">Under **Page fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="6d934-159">Iegādes lodziņa moduļa slotā **Mediju galerija** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="6d934-159">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6d934-160">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Mediju galerija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-160">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6d934-161">Iegādes lodziņa moduļa slotā **Veikalu atlasītājs** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="6d934-161">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6d934-162">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veikalu atlasītājs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-162">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6d934-163">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="6d934-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6d934-164">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="6d934-164">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="6d934-165">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **PDP veidne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-165">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="6d934-166">Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="6d934-166">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6d934-167">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-167">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6d934-168">Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot lapas fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="6d934-168">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="6d934-169">Dialoglodziņā **Atlasīt lapas fragmentu** atlasiet iepriekš izveidoto fragmentu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-169">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="6d934-170">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="6d934-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6d934-171">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="6d934-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="6d934-172">Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **PDP veidne**.</span><span class="sxs-lookup"><span data-stu-id="6d934-172">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="6d934-173">Sadaļā **Lapas nosaukums** ievadiet **PDP lapa** pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-173">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="6d934-174">Jaunās lapas **Galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot lapas fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="6d934-174">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="6d934-175">Dialoglodziņā **Atlasīt lapas fragmentu** atlasiet iepriekš izveidoto fragmentu **Iegādes lodziņa fragments** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d934-175">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="6d934-176">Saglabājiet un priekšskatiet lapu.</span><span class="sxs-lookup"><span data-stu-id="6d934-176">Save and preview the page.</span></span> <span data-ttu-id="6d934-177">Pievienojiet **?productid=&lt;product id&gt;** vaicājuma virknes parametru priekšskatījuma lapas vietrādim URL.</span><span class="sxs-lookup"><span data-stu-id="6d934-177">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="6d934-178">Šādā veidā preces konteksts tiek izmantots priekšskatījuma lapas ielādei un atveidošanai.</span><span class="sxs-lookup"><span data-stu-id="6d934-178">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="6d934-179">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="6d934-179">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="6d934-180">Preču informācijas lapā ir jābūt redzamam iegādes lodziņam.</span><span class="sxs-lookup"><span data-stu-id="6d934-180">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d934-181">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6d934-181">Additional resources</span></span>

[<span data-ttu-id="6d934-182">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="6d934-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6d934-183">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-183">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="6d934-184">Multivides galerijas modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-184">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="6d934-185">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-185">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6d934-186">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6d934-187">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-187">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="6d934-188">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-188">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6d934-189">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-189">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6d934-190">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-190">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6d934-191">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="6d934-191">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="6d934-192">Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem</span><span class="sxs-lookup"><span data-stu-id="6d934-192">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
