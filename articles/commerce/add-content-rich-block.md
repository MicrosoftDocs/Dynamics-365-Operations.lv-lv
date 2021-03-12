---
title: Teksta bloka modulis
description: Šajā tēmā tiek stāstīts par teksta bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cad6a26ea1858d6afac33ef8eab10e16b404035b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980485"
---
# <a name="text-block-module"></a><span data-ttu-id="c7adc-103">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="c7adc-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7adc-104">Šajā tēmā tiek stāstīts par teksta bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7adc-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c7adc-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="c7adc-105">Overview</span></span>

<span data-ttu-id="c7adc-106">Teksta bloka modulis ir modulis, kas tiek izmantots teksta satura pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="c7adc-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="c7adc-107">Tas var būt gan informatīvs, gan reklāmas saturs.</span><span class="sxs-lookup"><span data-stu-id="c7adc-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="c7adc-108">Teksta bloka moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="c7adc-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="c7adc-109">Tas ir savrups moduļi, kas nav atkarīgi no lapas konteksta vai jebkādiem citiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="c7adc-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="c7adc-110">Teksta bloka moduļu piemēri pakalpojumā e-Commerce</span><span class="sxs-lookup"><span data-stu-id="c7adc-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="c7adc-111">Teksta bloka moduļus var izmantot šādi.</span><span class="sxs-lookup"><span data-stu-id="c7adc-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="c7adc-112">Lai preces informācijas lapā rādītu preces līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="c7adc-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="c7adc-113">Informācijas nolūkiem jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="c7adc-113">For informational purposes on any page.</span></span> <span data-ttu-id="c7adc-114">Piemēram, tie var izskaidrot lojalitātes programmu priekšrocības, aprakstīt nosūtīšanas un atgriešanas politiku, atbildēt uz bieži uzdotajiem jautājumiem vai nodrošināt saturu "par mums".</span><span class="sxs-lookup"><span data-stu-id="c7adc-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="c7adc-115">Pievienot pielāgotus ziņojumus preces informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="c7adc-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="c7adc-116">(piemēram, “brīva piegāde pasūtījumiem virs 50 $”).</span><span class="sxs-lookup"><span data-stu-id="c7adc-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="c7adc-117">Atrunām un kontaktinformācijai par preču detalizētas informācijas lapām, groza lapām, izrakstīšanās lapām un citām lapām (piemēram, “Piegāde un atgriešana saskaņā ar veikala politikām”).</span><span class="sxs-lookup"><span data-stu-id="c7adc-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="c7adc-118">Attēlā zemāk redzams piemērs teksta bloka modulim, kas tiek izmantots sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="c7adc-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Teksta bloka moduļa piemērs](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="c7adc-120">Teksta bloka moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="c7adc-120">Text block module properties</span></span>

| <span data-ttu-id="c7adc-121">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="c7adc-121">Property name</span></span>     | <span data-ttu-id="c7adc-122">Vērtība</span><span class="sxs-lookup"><span data-stu-id="c7adc-122">Value</span></span>                                            | <span data-ttu-id="c7adc-123">apraksts</span><span class="sxs-lookup"><span data-stu-id="c7adc-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="c7adc-124">Bagātināts teksts</span><span class="sxs-lookup"><span data-stu-id="c7adc-124">Rich text</span></span>         | <span data-ttu-id="c7adc-125">Bagātināts teksts</span><span class="sxs-lookup"><span data-stu-id="c7adc-125">Rich text</span></span>                                        | <span data-ttu-id="c7adc-126">Rindkopas teksts.</span><span class="sxs-lookup"><span data-stu-id="c7adc-126">Paragraph text.</span></span> <span data-ttu-id="c7adc-127">Tiek atbalstītas dažas pamata bagātināta teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts.</span><span class="sxs-lookup"><span data-stu-id="c7adc-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="c7adc-128">Pielāgotās klases nosaukums</span><span class="sxs-lookup"><span data-stu-id="c7adc-128">Custom class name</span></span> | <span data-ttu-id="c7adc-129">Kaskadētās stila lapas (CSS) klases nosaukums</span><span class="sxs-lookup"><span data-stu-id="c7adc-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="c7adc-130">Tās pielāgotās CSS klases nosaukums, ko izstrādātājs sniedz, lai formatētu šo moduli.</span><span class="sxs-lookup"><span data-stu-id="c7adc-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="c7adc-131">Klases nosaukumam ir jābūt definētam dizaina pakotnē.</span><span class="sxs-lookup"><span data-stu-id="c7adc-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="c7adc-132">Fontu lielums</span><span class="sxs-lookup"><span data-stu-id="c7adc-132">Font size</span></span>         | <span data-ttu-id="c7adc-133">**Mazs**, **Vidējs**, **Liels** vai **X-liels**</span><span class="sxs-lookup"><span data-stu-id="c7adc-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="c7adc-134">Satura fonta lielums.</span><span class="sxs-lookup"><span data-stu-id="c7adc-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="c7adc-135">Teksta bloka moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="c7adc-135">Add a text block module to a page</span></span>

<span data-ttu-id="c7adc-136">Lai pievienotu teksta bloka moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="c7adc-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c7adc-137">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="c7adc-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c7adc-138">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **Satura veidne**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="c7adc-139">Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c7adc-140">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c7adc-141">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="c7adc-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c7adc-142">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="c7adc-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c7adc-143">Dialoglodziņā **Izvēlēties veidni** atlasiet **Satura veidne**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="c7adc-144">Sadaļā **Lapas nosaukums** ievadiet **Satura lapa** pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c7adc-145">Jaunās lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c7adc-146">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c7adc-147">Konteinera moduļa rekvizītu rūtī iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="c7adc-148">Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c7adc-149">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Teksta bloks** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="c7adc-150">Teksta bloka moduļa rekvizītu rūtī pievienojiet tekstu laukā **Bagātinātais teksts**.</span><span class="sxs-lookup"><span data-stu-id="c7adc-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="c7adc-151">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="c7adc-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="c7adc-152">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="c7adc-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7adc-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c7adc-153">Additional resources</span></span>

[<span data-ttu-id="c7adc-154">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="c7adc-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c7adc-155">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="c7adc-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="c7adc-156">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="c7adc-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="c7adc-157">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="c7adc-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="c7adc-158">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="c7adc-158">Video player module</span></span>](add-video-player.md)

