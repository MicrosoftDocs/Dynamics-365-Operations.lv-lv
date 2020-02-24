---
title: Teksta bloka modulis
description: Šajā tēmā tiek stāstīts par teksta bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025601"
---
# <a name="text-block-module"></a><span data-ttu-id="e4262-103">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="e4262-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e4262-104">Šajā tēmā tiek stāstīts par teksta bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4262-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e4262-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="e4262-105">Overview</span></span>

<span data-ttu-id="e4262-106">Teksta bloka modulis ir modulis, kas tiek izmantots teksta satura pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="e4262-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="e4262-107">Tas var būt gan informatīvs, gan reklāmas saturs.</span><span class="sxs-lookup"><span data-stu-id="e4262-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="e4262-108">Teksta bloka moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="e4262-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="e4262-109">Tas ir savrups moduļi, kas nav atkarīgi no lapas konteksta vai jebkādiem citiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="e4262-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="e4262-110">Teksta bloka moduļu piemēri pakalpojumā e-Commerce</span><span class="sxs-lookup"><span data-stu-id="e4262-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="e4262-111">Teksta bloka moduļus var izmantot šādi.</span><span class="sxs-lookup"><span data-stu-id="e4262-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="e4262-112">Lai preces informācijas lapā rādītu preces līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="e4262-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="e4262-113">Informācijas nolūkiem jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="e4262-113">For informational purposes on any page.</span></span> <span data-ttu-id="e4262-114">Piemēram, tie var izskaidrot lojalitātes programmu priekšrocības, aprakstīt nosūtīšanas un atgriešanas politiku, atbildēt uz bieži uzdotajiem jautājumiem vai nodrošināt saturu "par mums".</span><span class="sxs-lookup"><span data-stu-id="e4262-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="e4262-115">Pievienot pielāgotus ziņojumus preces informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="e4262-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="e4262-116">(piemēram, “brīva piegāde pasūtījumiem virs 50 $”).</span><span class="sxs-lookup"><span data-stu-id="e4262-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="e4262-117">Atrunām un kontaktinformācijai par preču detalizētas informācijas lapām, groza lapām, izrakstīšanās lapām un citām lapām (piemēram, “Piegāde un atgriešana saskaņā ar veikala politikām”).</span><span class="sxs-lookup"><span data-stu-id="e4262-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="e4262-118">Teksta bloka moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="e4262-118">Text block module properties</span></span>

| <span data-ttu-id="e4262-119">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="e4262-119">Property name</span></span>     | <span data-ttu-id="e4262-120">Value</span><span class="sxs-lookup"><span data-stu-id="e4262-120">Value</span></span>                                            | <span data-ttu-id="e4262-121">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e4262-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="e4262-122">Bagātināts teksts</span><span class="sxs-lookup"><span data-stu-id="e4262-122">Rich text</span></span>         | <span data-ttu-id="e4262-123">Bagātināts teksts</span><span class="sxs-lookup"><span data-stu-id="e4262-123">Rich text</span></span>                                        | <span data-ttu-id="e4262-124">Rindkopas teksts.</span><span class="sxs-lookup"><span data-stu-id="e4262-124">Paragraph text.</span></span> <span data-ttu-id="e4262-125">Tiek atbalstītas dažas pamata bagātināta teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts.</span><span class="sxs-lookup"><span data-stu-id="e4262-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="e4262-126">Pielāgotās klases nosaukums</span><span class="sxs-lookup"><span data-stu-id="e4262-126">Custom class name</span></span> | <span data-ttu-id="e4262-127">Kaskadētās stila lapas (CSS) klases nosaukums</span><span class="sxs-lookup"><span data-stu-id="e4262-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="e4262-128">Tās pielāgotās CSS klases nosaukums, ko izstrādātājs sniedz, lai formatētu šo moduli.</span><span class="sxs-lookup"><span data-stu-id="e4262-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="e4262-129">Klases nosaukumam ir jābūt definētam dizaina pakotnē.</span><span class="sxs-lookup"><span data-stu-id="e4262-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="e4262-130">Fontu lielums</span><span class="sxs-lookup"><span data-stu-id="e4262-130">Font size</span></span>         | <span data-ttu-id="e4262-131">**Mazs**, **Vidējs**, **Liels** vai **X-liels**</span><span class="sxs-lookup"><span data-stu-id="e4262-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="e4262-132">Satura fonta lielums.</span><span class="sxs-lookup"><span data-stu-id="e4262-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="e4262-133">Teksta bloka moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="e4262-133">Add a text block module to a page</span></span>

<span data-ttu-id="e4262-134">Lai pievienotu teksta bloka moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="e4262-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e4262-135">Izveidojiet lapas veidni ar nosaukumu **Satura veidne**.</span><span class="sxs-lookup"><span data-stu-id="e4262-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="e4262-136">Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.</span><span class="sxs-lookup"><span data-stu-id="e4262-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="e4262-137">Pabeidziet rediģēt veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="e4262-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="e4262-138">Izmantojiet jūsu tikko izveidoto satura veidni, lai izveidotu lapu ar nosaukumu **Satura lapa**.</span><span class="sxs-lookup"><span data-stu-id="e4262-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="e4262-139">Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="e4262-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="e4262-140">Konteinera moduļa rekvizītu rūtī iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="e4262-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="e4262-141">Pievienojiet teksta bloka moduli konteinera modulim.</span><span class="sxs-lookup"><span data-stu-id="e4262-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="e4262-142">Teksta bloka moduļa rekvizītu rūtī pievienojiet tekstu laukā **Bagātinātais teksts**.</span><span class="sxs-lookup"><span data-stu-id="e4262-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="e4262-143">Pabeidziet rediģēt lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="e4262-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4262-144">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e4262-144">Additional resources</span></span>

[<span data-ttu-id="e4262-145">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="e4262-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e4262-146">Veicināšanas reklāmkarogu modulis</span><span class="sxs-lookup"><span data-stu-id="e4262-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="e4262-147">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="e4262-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e4262-148">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="e4262-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="e4262-149">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="e4262-149">Video player module</span></span>](add-video-player.md)

