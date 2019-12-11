---
title: Centrālais modulis
description: Šī tēma ietver centrālos moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785398"
---
# <a name="hero-module"></a><span data-ttu-id="f4b7b-103">Centrālais modulis</span><span class="sxs-lookup"><span data-stu-id="f4b7b-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f4b7b-104">Šī tēma ietver centrālos moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f4b7b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="f4b7b-105">Overview</span></span>

<span data-ttu-id="f4b7b-106">Centrālais modulis tiek izmantots, lai reklamētu preces vai veicināšanas pasākumus, izmantojot attēlu un teksta kombināciju.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="f4b7b-107">Piemēram, mazumtirgotājs var pievienot centrālo moduli E-komercijas sākumlapai, lai reklamētu jaunu preci un piesaistītu klientu uzmanību.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="f4b7b-108">Centrālo moduli vada dati no satura pārvaldība sistēmas (CMS).</span><span class="sxs-lookup"><span data-stu-id="f4b7b-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="f4b7b-109">Tas ir savrups modulis, kas nav atkarīgs no citiem moduļiem lapā.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="f4b7b-110">Centrālo moduli var ievietot jebkurā vietnes lapā, kur mazumtirgotājs vēlas kaut ko pārdot vai reklamēt (piemēram, preces, pārdošanu vai līdzekļus).</span><span class="sxs-lookup"><span data-stu-id="f4b7b-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="f4b7b-111">Centrālo moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="f4b7b-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="f4b7b-112">Centrālo moduli var izmantot E-komercijas vietnes sākumlapā, lai izceltu veicināšanas pasākumus un jaunās preces.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="f4b7b-113">Centrālais modulis var tikt izmantots preces informācijas lapā, lai parādītu informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="f4b7b-114">Vairākus centrālos moduļus var ievietot karuseļa modulī, lai izceltu vairākas preces vai veicināšanas pasākumus.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="f4b7b-115">Centrālā moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="f4b7b-115">Hero module properties</span></span>

| <span data-ttu-id="f4b7b-116">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="f4b7b-116">Property name</span></span>  | <span data-ttu-id="f4b7b-117">Vērtības</span><span class="sxs-lookup"><span data-stu-id="f4b7b-117">Values</span></span> | <span data-ttu-id="f4b7b-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="f4b7b-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="f4b7b-119">Attēls</span><span class="sxs-lookup"><span data-stu-id="f4b7b-119">Image</span></span>          | <span data-ttu-id="f4b7b-120">Attēla fails</span><span class="sxs-lookup"><span data-stu-id="f4b7b-120">Image file</span></span> | <span data-ttu-id="f4b7b-121">Attēlu var izmantot, lai rādītu preci vai veicināšanas pasākumu.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="f4b7b-122">Attēlu var augšupielādēt attēlu galerijā vai arī var izmantot esošu attēlu.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="f4b7b-123">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="f4b7b-123">Heading</span></span>        | <span data-ttu-id="f4b7b-124">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="f4b7b-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="f4b7b-125">Katram centrālajam modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-125">Every hero module can have a heading.</span></span> <span data-ttu-id="f4b7b-126">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="f4b7b-127">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="f4b7b-128">Rindkopa</span><span class="sxs-lookup"><span data-stu-id="f4b7b-128">Paragraph</span></span>      | <span data-ttu-id="f4b7b-129">Rindkopas teksts</span><span class="sxs-lookup"><span data-stu-id="f4b7b-129">Paragraph text</span></span> | <span data-ttu-id="f4b7b-130">Centrālie moduļi atbalsta rindkopu tekstu bagātinātā teksta formātā.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="f4b7b-131">Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts, kā arī hipersaites.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="f4b7b-132">Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="f4b7b-133">Saistīt</span><span class="sxs-lookup"><span data-stu-id="f4b7b-133">Link</span></span>           | <span data-ttu-id="f4b7b-134">Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē**</span><span class="sxs-lookup"><span data-stu-id="f4b7b-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="f4b7b-135">Centrālie moduļi atbalsta vienu vai vairākas saites “aicinājums uz darbību”.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="f4b7b-136">Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="f4b7b-137">ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="f4b7b-138">Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="f4b7b-139">Teksta izvietojums</span><span class="sxs-lookup"><span data-stu-id="f4b7b-139">Text placement</span></span> | <span data-ttu-id="f4b7b-140">**Augšpusē pa kreisi**, **Augšpusē pa labi**, **Augšpusē centrā**, **Apakšpusē pa kreisi**, **Apakšpusē pa labi**, **Apakšpusē centrā**, **Centrā pa kreisi**, **Centrā pa labi** vai **Centrā**</span><span class="sxs-lookup"><span data-stu-id="f4b7b-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="f4b7b-141">Šis rekvizīts nosaka attēla novietojumu attiecībā pret tekstu.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="f4b7b-142">Piemēram, atlasot **Pa labi**, attēls tiek parādīts pa labi no teksta.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="f4b7b-143">Teksta motīvs</span><span class="sxs-lookup"><span data-stu-id="f4b7b-143">Text theme</span></span>     | <span data-ttu-id="f4b7b-144">**Gaišs** vai **Tumšs**</span><span class="sxs-lookup"><span data-stu-id="f4b7b-144">**Light** or **Dark**</span></span> | <span data-ttu-id="f4b7b-145">Teksta krāsu shēmu var definēt, pamatojoties uz fona attēlu.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="f4b7b-146">Piemēram, ja attēlam ir tumšs fons, var lietot gaismas dizainu, lai tekstu padarītu redzamāku un panāktu atbilstību krāsu kontrasta koeficientu pieejamībai.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="f4b7b-147">Gradients</span><span class="sxs-lookup"><span data-stu-id="f4b7b-147">Gradient</span></span>       | <span data-ttu-id="f4b7b-148">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="f4b7b-148">**True** or **False**</span></span> | <span data-ttu-id="f4b7b-149">Gradientu var lietot attēlam, lai nodrošinātu krāsu kontrasta attiecības pieejamības nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="f4b7b-150">Centrālā moduļa pievienošana jaunā lapā</span><span class="sxs-lookup"><span data-stu-id="f4b7b-150">Add a hero module to a new page</span></span>

<span data-ttu-id="f4b7b-151">Lai pievienotu centrālo moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f4b7b-152">Dodieties uz **Veidnes** un izveidojiet lapas veidni ar nosaukumu **centrālā veidne**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="f4b7b-153">Noklusētās lapas **Galvenajā** slotā pievienojiet centrālo moduli.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="f4b7b-154">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="f4b7b-155">Izmantojiet jūsu tikko izveidoto centrālo veidni, lai izveidotu lapu ar nosaukumu **centrālā lapa**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="f4b7b-156">Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4b7b-157">Dialoglodziņā **Pievienot moduli** zem **Atlasīt moduļus** izvēlieties centrālio moduli un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4b7b-158">Strukturējuma kokā pa kreisi atlasiet centrālo moduli.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="f4b7b-159">Rekvizītu rūts labajā pusē atlasiet **Pievienot attēlu**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="f4b7b-160">Pēc tam vai nu atlasiet esošu attēlu, vai augšupielādējiet jaunu attēlu.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="f4b7b-161">Atlasiet **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-161">Select **Heading**.</span></span>
1. <span data-ttu-id="f4b7b-162">Dialoglodziņā **Virsraksts** pievienojiet virsraksta tekstu, atlasiet virsraksta līmeni un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="f4b7b-163">Sadaļā **Bagātināts teksts** pievienojiet vēlamo tekstu.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="f4b7b-164">Atlasiet **Pievienot darbības saiti**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="f4b7b-165">Dialoglodziņā **Darbības saite** pievienojiet saites tekstu, saites vietrādi URL un ARIA etiķeti saitei un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="f4b7b-166">Lapas saglabāšana un savu izmaiņu priekšskatīšana</span><span class="sxs-lookup"><span data-stu-id="f4b7b-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="f4b7b-167">Pārbaudiet lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="f4b7b-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4b7b-168">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f4b7b-168">Additional resources</span></span>

[<span data-ttu-id="f4b7b-169">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="f4b7b-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f4b7b-170">Brīdinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="f4b7b-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="f4b7b-171">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="f4b7b-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="f4b7b-172">Bagātinātā satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="f4b7b-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f4b7b-173">Satura izvietojuma modulis</span><span class="sxs-lookup"><span data-stu-id="f4b7b-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="f4b7b-174">Līdzekļa modulis</span><span class="sxs-lookup"><span data-stu-id="f4b7b-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="f4b7b-175">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="f4b7b-175">Video player module</span></span>](add-video-player.md)
