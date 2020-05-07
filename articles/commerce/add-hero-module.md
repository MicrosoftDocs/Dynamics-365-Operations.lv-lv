---
title: Satura bloka modulis
description: Šajā tēmā tiek stāstīts par satura bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: daf9193a7fdc3b57defbb3250ae902f6eb6ee6c4
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269686"
---
# <a name="content-block-module"></a><span data-ttu-id="0671a-103">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="0671a-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0671a-104">Šajā tēmā tiek stāstīts par satura bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0671a-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0671a-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="0671a-105">Overview</span></span>

<span data-ttu-id="0671a-106">Satura bloka modulis tiek izmantots, lai reklamētu preces vai veicināšanas pasākumus, izmantojot attēlu un teksta kombināciju.</span><span class="sxs-lookup"><span data-stu-id="0671a-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="0671a-107">Piemēram, mazumtirgotājs var pievienot satura bloka moduli e-Commerce sākumlapai, lai reklamētu jaunu preci un piesaistītu klientu uzmanību.</span><span class="sxs-lookup"><span data-stu-id="0671a-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="0671a-108">Satura bloka moduli vada dati no satura pārvaldība sistēmas (CMS).</span><span class="sxs-lookup"><span data-stu-id="0671a-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="0671a-109">Tas ir savrups modulis, kas nav atkarīgs no citiem moduļiem lapā.</span><span class="sxs-lookup"><span data-stu-id="0671a-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="0671a-110">Satura bloka moduli var ievietot jebkurā vietnes lapā, kur mazumtirgotājs vēlas kaut ko pārdot vai reklamēt (piemēram, preces, pārdošanu vai līdzekļus).</span><span class="sxs-lookup"><span data-stu-id="0671a-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="0671a-111">Satura bloka moduļa piemēri e-Commerce</span><span class="sxs-lookup"><span data-stu-id="0671a-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="0671a-112">Satura bloka moduli var izmantot e-Commerce vietnes sākumlapā, lai izceltu veicināšanas pasākumus un jaunās preces.</span><span class="sxs-lookup"><span data-stu-id="0671a-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="0671a-113">Satura bloka modulis var tikt izmantots preces informācijas lapā, lai parādītu informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="0671a-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="0671a-114">Vairākus satura bloka moduļus var ievietot karuseļa modulī, lai izceltu vairākas preces vai veicināšanas pasākumus.</span><span class="sxs-lookup"><span data-stu-id="0671a-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="0671a-115">Satura bloku moduļi un tēmas</span><span class="sxs-lookup"><span data-stu-id="0671a-115">Content block modules and themes</span></span>

<span data-ttu-id="0671a-116">Satura bloku moduļi var atbalstīt dažādus izkārtojumus un stilus, kas balstīti uz tēmu.</span><span class="sxs-lookup"><span data-stu-id="0671a-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="0671a-117">Piemēram, Fabrikam tēma atbalsta trīs izkārtojuma variācijas satura bloka modulī: varonis, funkcija un mozaīka.</span><span class="sxs-lookup"><span data-stu-id="0671a-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="0671a-118">Varoņa izkārtojumā tiek rādīts fonā esošs attēls ar teksta pārklājumu.</span><span class="sxs-lookup"><span data-stu-id="0671a-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="0671a-119">Funkciju izkārtojumā attēls un teksts ir redzams līdzās.</span><span class="sxs-lookup"><span data-stu-id="0671a-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="0671a-120">Mozaīkas izkārtojums atļauj vairākus satura blokus mozaīkas formātā.</span><span class="sxs-lookup"><span data-stu-id="0671a-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="0671a-121">Turklāt dizainā var būt dažādi rekvizīti katram izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="0671a-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="0671a-122">Dizaina izstrādātājs var veidot vairāk izkārtojumu ar vairāk stiliem, izmantojot satura bloka moduli.</span><span class="sxs-lookup"><span data-stu-id="0671a-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="0671a-123">Tālāk esošajā attēlā redzams satura bloka moduļa piemērs ar varonis izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="0671a-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Hero moduļa piemērs](./media/Hero.PNG)

<span data-ttu-id="0671a-125">Tālāk esošajā attēlā redzams satura bloka moduļa piemērs ar funkcijas izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="0671a-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Līdzekļu moduļu piemēri](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="0671a-127">Satura bloka moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="0671a-127">Content block module properties</span></span>

| <span data-ttu-id="0671a-128">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="0671a-128">Property name</span></span>  | <span data-ttu-id="0671a-129">Vērtības</span><span class="sxs-lookup"><span data-stu-id="0671a-129">Values</span></span> | <span data-ttu-id="0671a-130">Apraksts</span><span class="sxs-lookup"><span data-stu-id="0671a-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0671a-131">Attēls</span><span class="sxs-lookup"><span data-stu-id="0671a-131">Image</span></span>          | <span data-ttu-id="0671a-132">Attēla fails</span><span class="sxs-lookup"><span data-stu-id="0671a-132">Image file</span></span> | <span data-ttu-id="0671a-133">Attēlu var izmantot, lai rādītu preci vai veicināšanas pasākumu.</span><span class="sxs-lookup"><span data-stu-id="0671a-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="0671a-134">Attēlu var augšupielādēt attēlu galerijā vai arī var izmantot esošu attēlu.</span><span class="sxs-lookup"><span data-stu-id="0671a-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="0671a-135">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="0671a-135">Heading</span></span>        | <span data-ttu-id="0671a-136">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="0671a-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0671a-137">Katram centrālajam modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="0671a-137">Every hero module can have a heading.</span></span> <span data-ttu-id="0671a-138">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="0671a-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0671a-139">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="0671a-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0671a-140">Rindkopa</span><span class="sxs-lookup"><span data-stu-id="0671a-140">Paragraph</span></span>      | <span data-ttu-id="0671a-141">Rindkopas teksts</span><span class="sxs-lookup"><span data-stu-id="0671a-141">Paragraph text</span></span> | <span data-ttu-id="0671a-142">Centrālie moduļi atbalsta rindkopu tekstu bagātinātā teksta formātā.</span><span class="sxs-lookup"><span data-stu-id="0671a-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="0671a-143">Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts, kā arī hipersaites.</span><span class="sxs-lookup"><span data-stu-id="0671a-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="0671a-144">Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām.</span><span class="sxs-lookup"><span data-stu-id="0671a-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="0671a-145">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0671a-145">Link</span></span>           | <span data-ttu-id="0671a-146">Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē**</span><span class="sxs-lookup"><span data-stu-id="0671a-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="0671a-147">Centrālie moduļi atbalsta vienu vai vairākas saites “aicinājums uz darbību”.</span><span class="sxs-lookup"><span data-stu-id="0671a-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="0671a-148">Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete.</span><span class="sxs-lookup"><span data-stu-id="0671a-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="0671a-149">ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="0671a-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="0671a-150">Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē.</span><span class="sxs-lookup"><span data-stu-id="0671a-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="0671a-151">Satura bloka moduļa rekvizīti, kas pakļauti Fabrikam motīvam</span><span class="sxs-lookup"><span data-stu-id="0671a-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="0671a-152">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="0671a-152">Property name</span></span>  | <span data-ttu-id="0671a-153">Vērtības</span><span class="sxs-lookup"><span data-stu-id="0671a-153">Values</span></span> | <span data-ttu-id="0671a-154">Apraksts</span><span class="sxs-lookup"><span data-stu-id="0671a-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0671a-155">Teksta izvietojums</span><span class="sxs-lookup"><span data-stu-id="0671a-155">Text placement</span></span> | <span data-ttu-id="0671a-156">**Pa kreisi**, **Pa labi**, **Pa vidu**</span><span class="sxs-lookup"><span data-stu-id="0671a-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="0671a-157">Šis rekvizīts nosaka teksta novietojumu attiecībā pret attēlu.</span><span class="sxs-lookup"><span data-stu-id="0671a-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="0671a-158">Tas attiecas tikai uz varoņa izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="0671a-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="0671a-159">Teksta motīvs</span><span class="sxs-lookup"><span data-stu-id="0671a-159">Text theme</span></span>     | <span data-ttu-id="0671a-160">**Gaišs** vai **Tumšs**</span><span class="sxs-lookup"><span data-stu-id="0671a-160">**Light** or **Dark**</span></span> | <span data-ttu-id="0671a-161">Teksta krāsu shēmu var definēt, pamatojoties uz fona attēlu.</span><span class="sxs-lookup"><span data-stu-id="0671a-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="0671a-162">Piemēram, ja attēlam ir tumšs fons, var lietot gaismas dizainu, lai tekstu padarītu redzamāku un panāktu atbilstību krāsu kontrasta koeficientu pieejamībai.</span><span class="sxs-lookup"><span data-stu-id="0671a-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="0671a-163">Tas attiecas tikai uz varoņa izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="0671a-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="0671a-164">Attēla izvietojums</span><span class="sxs-lookup"><span data-stu-id="0671a-164">Image placement</span></span>       | <span data-ttu-id="0671a-165">**Pa kreisi**, **Pa labi**</span><span class="sxs-lookup"><span data-stu-id="0671a-165">**Left**,  **Right**</span></span> | <span data-ttu-id="0671a-166">Šis rekvizīts norāda, vai attēlam jāatrodas pa kreisi vai pa labi no teksta.</span><span class="sxs-lookup"><span data-stu-id="0671a-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="0671a-167">Tas attiecas tikai uz funkciju izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="0671a-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="0671a-168">Satura bloka moduļa pievienošana jaunā lapā</span><span class="sxs-lookup"><span data-stu-id="0671a-168">Add a content block module to a new page</span></span>

<span data-ttu-id="0671a-169">Lai pievienotu centrālo moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="0671a-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0671a-170">Dodieties uz **Veidnes**un izveidojiet lapas veidni ar nosaukumu **Satura bloka veidne**.</span><span class="sxs-lookup"><span data-stu-id="0671a-170">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="0671a-171">Noklusētās lapas **Galvenajā** slotā pievienojiet centrālo moduli.</span><span class="sxs-lookup"><span data-stu-id="0671a-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="0671a-172">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="0671a-172">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0671a-173">Izmantojiet jūsu tikko izveidoto konteinera varoņa veidni, lai izveidotu lapu ar nosaukumu **Satura bloka lapa**.</span><span class="sxs-lookup"><span data-stu-id="0671a-173">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="0671a-174">Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="0671a-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0671a-175">Dialoglodziņā **Pievienot moduli** zem **Atlasīt moduļus** izvēlieties centrālio moduli un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0671a-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="0671a-176">Strukturējuma kokā pa kreisi atlasiet satura bloka moduli.</span><span class="sxs-lookup"><span data-stu-id="0671a-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="0671a-177">Rekvizītu rūts labajā pusē atlasiet **Pievienot attēlu**.</span><span class="sxs-lookup"><span data-stu-id="0671a-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="0671a-178">Pēc tam vai nu atlasiet esošu attēlu, vai augšupielādējiet jaunu attēlu.</span><span class="sxs-lookup"><span data-stu-id="0671a-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="0671a-179">Atlasiet **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="0671a-179">Select **Heading**.</span></span>
1. <span data-ttu-id="0671a-180">Dialoglodziņā **Virsraksts** pievienojiet virsraksta tekstu, atlasiet virsraksta līmeni un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0671a-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="0671a-181">Sadaļā **Bagātināts teksts** pievienojiet vēlamo tekstu.</span><span class="sxs-lookup"><span data-stu-id="0671a-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="0671a-182">Atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="0671a-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="0671a-183">Dialoglodziņā **Saite** pievienojiet saites tekstu, saites vietrādi URL un ARIA etiķeti saitei un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0671a-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="0671a-184">Atlasiet **Varonis** izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="0671a-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="0671a-185">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="0671a-185">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0671a-186">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="0671a-186">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="0671a-187">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0671a-187">Additional resources</span></span>

[<span data-ttu-id="0671a-188">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="0671a-188">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0671a-189">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="0671a-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="0671a-190">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="0671a-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="0671a-191">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="0671a-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="0671a-192">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="0671a-192">Video player module</span></span>](add-video-player.md)
