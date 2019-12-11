---
title: Līdzekļa modulis
description: Šajā tēmā tiek stāstīts par līdzekļu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785289"
---
# <a name="feature-module"></a><span data-ttu-id="a5d15-103">Līdzekļa modulis</span><span class="sxs-lookup"><span data-stu-id="a5d15-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a5d15-104">Šajā tēmā tiek stāstīts par līdzekļu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a5d15-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a5d15-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="a5d15-105">Overview</span></span>

<span data-ttu-id="a5d15-106">Līdzekļa modulis tiek izmantots, lai reklamētu preces vai veicināšanas pasākumus, izmantojot attēlu un teksta kombināciju.</span><span class="sxs-lookup"><span data-stu-id="a5d15-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="a5d15-107">Piemēram, mazumtirgotājs var pievienot līdzekļa moduli preces informācijas lapai, lai izceltu preces līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="a5d15-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="a5d15-108">Līdzekļa moduli vada dati no satura pārvaldība sistēmas (CMS).</span><span class="sxs-lookup"><span data-stu-id="a5d15-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="a5d15-109">Tas ir savrups modulis, kas nav atkarīgs no citiem moduļiem lapā.</span><span class="sxs-lookup"><span data-stu-id="a5d15-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="a5d15-110">Līdzekļa moduli var ievietot jebkurā vietnes lapā, kur mazumtirgotājs vēlas kaut ko pārdot vai reklamēt (piemēram, preces, pārdošanu vai līdzekļus).</span><span class="sxs-lookup"><span data-stu-id="a5d15-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="a5d15-111">Līdzekļu moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="a5d15-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="a5d15-112">Līdzekļa moduli var izmantot šādās lapās.</span><span class="sxs-lookup"><span data-stu-id="a5d15-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="a5d15-113">Preces informācijas lapa preces līdzekļu rādīšanai</span><span class="sxs-lookup"><span data-stu-id="a5d15-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="a5d15-114">Sākumlapa preču reklamēšanai</span><span class="sxs-lookup"><span data-stu-id="a5d15-114">The home page, to promote products</span></span>
- <span data-ttu-id="a5d15-115">Kategorijas lapa preču kategorijas izcelšanai</span><span class="sxs-lookup"><span data-stu-id="a5d15-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="a5d15-116">Līdzekļa moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="a5d15-116">Feature module properties</span></span>

| <span data-ttu-id="a5d15-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="a5d15-117">Property name</span></span>     | <span data-ttu-id="a5d15-118">Vērtības</span><span class="sxs-lookup"><span data-stu-id="a5d15-118">Values</span></span> | <span data-ttu-id="a5d15-119">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a5d15-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="a5d15-120">Attēls</span><span class="sxs-lookup"><span data-stu-id="a5d15-120">Image</span></span>             | <span data-ttu-id="a5d15-121">Attēla fails</span><span class="sxs-lookup"><span data-stu-id="a5d15-121">Image file</span></span> | <span data-ttu-id="a5d15-122">Attēlu var izmantot, lai reklamētu preci vai veicināšanas pasākumu.</span><span class="sxs-lookup"><span data-stu-id="a5d15-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="a5d15-123">Attēlu var augšupielādēt attēlu galerijā vai arī var izmantot esošu attēlu.</span><span class="sxs-lookup"><span data-stu-id="a5d15-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="a5d15-124">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="a5d15-124">Heading</span></span>           | <span data-ttu-id="a5d15-125">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="a5d15-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="a5d15-126">Katram līdzekļu modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="a5d15-126">Every feature module can have a heading.</span></span> <span data-ttu-id="a5d15-127">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="a5d15-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="a5d15-128">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="a5d15-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="a5d15-129">Rindkopa</span><span class="sxs-lookup"><span data-stu-id="a5d15-129">Paragraph</span></span>         | <span data-ttu-id="a5d15-130">Rindkopas teksts</span><span class="sxs-lookup"><span data-stu-id="a5d15-130">Paragraph text</span></span> | <span data-ttu-id="a5d15-131">Līdzekļu moduļi atbalsta rindkopu tekstu bagātinātā teksta formātā.</span><span class="sxs-lookup"><span data-stu-id="a5d15-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="a5d15-132">Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts, kā arī hipersaites.</span><span class="sxs-lookup"><span data-stu-id="a5d15-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="a5d15-133">Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām.</span><span class="sxs-lookup"><span data-stu-id="a5d15-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="a5d15-134">Saistīt</span><span class="sxs-lookup"><span data-stu-id="a5d15-134">Link</span></span>              | <span data-ttu-id="a5d15-135">Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē**</span><span class="sxs-lookup"><span data-stu-id="a5d15-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="a5d15-136">Līdzekļu moduļi atbalsta vienu vai vairākas saites “Aicinājums uz darbību”.</span><span class="sxs-lookup"><span data-stu-id="a5d15-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="a5d15-137">Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete.</span><span class="sxs-lookup"><span data-stu-id="a5d15-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="a5d15-138">ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="a5d15-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="a5d15-139">Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē.</span><span class="sxs-lookup"><span data-stu-id="a5d15-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="a5d15-140">Attēla izvietojums</span><span class="sxs-lookup"><span data-stu-id="a5d15-140">Image placement</span></span>   | <span data-ttu-id="a5d15-141">**Pa labai**, **Pa kreisi**, **Augšā** vai **Apakšā**</span><span class="sxs-lookup"><span data-stu-id="a5d15-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="a5d15-142">Šis rekvizīts nosaka attēla novietojumu attiecībā pret tekstu.</span><span class="sxs-lookup"><span data-stu-id="a5d15-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="a5d15-143">Piemēram, atlasot **Pa labi**, attēls tiek parādīts pa labi no teksta.</span><span class="sxs-lookup"><span data-stu-id="a5d15-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="a5d15-144">Attēlu kolonnas lielums</span><span class="sxs-lookup"><span data-stu-id="a5d15-144">Image column size</span></span> | <span data-ttu-id="a5d15-145">Skaitlis no **1** līdz **12**</span><span class="sxs-lookup"><span data-stu-id="a5d15-145">A value from **1** through **12**</span></span> | <span data-ttu-id="a5d15-146">Šis rekvizīts nosaka attēla izmēru attiecībā pret tekstu.</span><span class="sxs-lookup"><span data-stu-id="a5d15-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="a5d15-147">Izmērs ir izteikts kā kolonnu skaits lapā.</span><span class="sxs-lookup"><span data-stu-id="a5d15-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="a5d15-148">Lapā ir 12 kolonnas.</span><span class="sxs-lookup"><span data-stu-id="a5d15-148">There are 12 columns on a page.</span></span> <span data-ttu-id="a5d15-149">Pēc noklusējuma attēlam un tekstam ir vienāds izmērs (sešas kolonnas katrai).</span><span class="sxs-lookup"><span data-stu-id="a5d15-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="a5d15-150">Tomēr izmērus var pielāgot pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="a5d15-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="a5d15-151">Līdzekļa moduļa pievienošana jaunā lapā</span><span class="sxs-lookup"><span data-stu-id="a5d15-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="a5d15-152">Lai pievienotu līdzekļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="a5d15-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a5d15-153">Dodieties uz **Veidnes**un izveidojiet lapas veidni ar nosaukumu **līdzekļa veidne**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="a5d15-154">Noklusējuma lapas **Galvenajā** slotā pievienojiet līdzekļa moduli.</span><span class="sxs-lookup"><span data-stu-id="a5d15-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="a5d15-155">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="a5d15-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="a5d15-156">Izmantojiet jūsu tikko izveidoto līdzekļa veidni, lai izveidotu lapu ar nosaukumu **līdzekļa lapa**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="a5d15-157">Noklusējuma lapas **Galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a5d15-158">Dialoglodziņā **Pievienot moduli** zem **Atlasīt moduļus** atlasiet līdzekļa moduli un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="a5d15-159">Strukturējuma kokā pa kreisi atlasiet līdzekļa moduli.</span><span class="sxs-lookup"><span data-stu-id="a5d15-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="a5d15-160">Rekvizītu rūts labajā pusē atlasiet **Pievienot attēlu**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="a5d15-161">Pēc tam vai nu atlasiet esošu attēlu, vai augšupielādējiet jaunu attēlu.</span><span class="sxs-lookup"><span data-stu-id="a5d15-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="a5d15-162">Atlasiet **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-162">Select **Heading**.</span></span>
1. <span data-ttu-id="a5d15-163">Dialoglodziņā **Virsraksts** pievienojiet virsraksta tekstu, atlasiet virsraksta līmeni un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="a5d15-164">Sadaļā **Bagātināts teksts** pievienojiet vēlamo tekstu.</span><span class="sxs-lookup"><span data-stu-id="a5d15-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="a5d15-165">Atlasiet **Pievienot darbības saiti**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="a5d15-166">Dialoglodziņā **Darbības saite** pievienojiet saites tekstu, saites vietrādi URL un ARIA etiķeti saitei un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a5d15-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="a5d15-167">Lapas saglabāšana un savu izmaiņu priekšskatīšana</span><span class="sxs-lookup"><span data-stu-id="a5d15-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="a5d15-168">Pārbaudiet lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="a5d15-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5d15-169">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a5d15-169">Additional resources</span></span>

[<span data-ttu-id="a5d15-170">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="a5d15-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a5d15-171">Brīdinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="a5d15-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="a5d15-172">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="a5d15-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a5d15-173">Bagātinātā satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="a5d15-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a5d15-174">Satura izvietojuma modulis</span><span class="sxs-lookup"><span data-stu-id="a5d15-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="a5d15-175">Centrālais modulis</span><span class="sxs-lookup"><span data-stu-id="a5d15-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="a5d15-176">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="a5d15-176">Video player module</span></span>](add-video-player.md)
