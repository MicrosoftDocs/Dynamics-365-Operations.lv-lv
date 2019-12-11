---
title: Satura bagātinātā bloka modulis
description: Šajā tēmā tiek stāstīts par satura bagātinātā bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785425"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="7178b-103">Satura bagātinātā bloka modulis</span><span class="sxs-lookup"><span data-stu-id="7178b-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7178b-104">Šajā tēmā tiek stāstīts par satura bagātinātā bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7178b-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7178b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="7178b-105">Overview</span></span>

<span data-ttu-id="7178b-106">Satura bagātinātā bloka modulis ir īpašs konteiners, kurā var ievietot vienu vai vairākus satura bagātinātā bloka elementus.</span><span class="sxs-lookup"><span data-stu-id="7178b-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="7178b-107">Satura bagātinātā bloka moduļi tiek izmantoti lapas teksta saturam.</span><span class="sxs-lookup"><span data-stu-id="7178b-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="7178b-108">Tas var būt gan informatīvs, gan reklāmas saturs.</span><span class="sxs-lookup"><span data-stu-id="7178b-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="7178b-109">Satura bagātinātā bloka moduļus vada dati no satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="7178b-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="7178b-110">Tas ir savrups moduļi, kas nav atkarīgi no lapas konteksta vai jebkādiem citiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="7178b-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="7178b-111">Satura bagātinātā bloka moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="7178b-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="7178b-112">Satura bagātināta bloka moduļus var izmantot šādi.</span><span class="sxs-lookup"><span data-stu-id="7178b-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="7178b-113">Lai preces informācijas lapā rādītu preces līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="7178b-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="7178b-114">Informācijas nolūkiem jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="7178b-114">For informational purposes on any page.</span></span> <span data-ttu-id="7178b-115">Piemēram, tie var izskaidrot lojalitātes programmu priekšrocības, aprakstīt nosūtīšanas un atgriešanas politiku, atbildēt uz bieži uzdotajiem jautājumiem vai nodrošināt saturu "par mums".</span><span class="sxs-lookup"><span data-stu-id="7178b-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="7178b-116">Pievienot pielāgotus ziņojumus preces informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="7178b-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="7178b-117">(piemēram, “brīva piegāde pasūtījumiem virs 50 $”).</span><span class="sxs-lookup"><span data-stu-id="7178b-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="7178b-118">Atrunām un kontaktinformācijai par preču detalizētas informācijas lapām, groza lapām, izrakstīšanās lapām un citām lapām (piemēram, “Piegāde un atgriešana saskaņā ar veikala politikām”).</span><span class="sxs-lookup"><span data-stu-id="7178b-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="7178b-119">Satura bagātinātā bloka moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="7178b-119">Content rich block module properties</span></span>

| <span data-ttu-id="7178b-120">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="7178b-120">Property name</span></span>     | <span data-ttu-id="7178b-121">Vērtība</span><span class="sxs-lookup"><span data-stu-id="7178b-121">Value</span></span>                                 | <span data-ttu-id="7178b-122">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="7178b-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="7178b-123">Kolonnu skaits</span><span class="sxs-lookup"><span data-stu-id="7178b-123">Number of columns</span></span> | <span data-ttu-id="7178b-124">Skaitlis no **1** līdz **4**</span><span class="sxs-lookup"><span data-stu-id="7178b-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="7178b-125">Kolonnu skaits satura bagātinātajā blokā.</span><span class="sxs-lookup"><span data-stu-id="7178b-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="7178b-126">Tur var būt līdz četrām kolonnām.</span><span class="sxs-lookup"><span data-stu-id="7178b-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="7178b-127">Platums</span><span class="sxs-lookup"><span data-stu-id="7178b-127">Width</span></span>             | <span data-ttu-id="7178b-128">**Ietilpināt konteinerā** vai **Aizpildīt ekrānu**</span><span class="sxs-lookup"><span data-stu-id="7178b-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="7178b-129">Ja vērtība ir iestatīta uz **Ietilpināt konteinerā**, tad elementi konteinerā tiek ierobežoti ar konteinera platumu.</span><span class="sxs-lookup"><span data-stu-id="7178b-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="7178b-130">Ja vērtība ir iestatīta uz **Aizpildīt ekrānu**, elementi neaprobežojas ar konteinera platumu, bet var pāriet pilnekrāna režīmā.</span><span class="sxs-lookup"><span data-stu-id="7178b-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="7178b-131">Varat mainīt vērtību, lai sasniegtu vēlamo izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="7178b-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="7178b-132">Satura bagātinātā bloka elementa moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="7178b-132">Content rich block item module properties</span></span>

| <span data-ttu-id="7178b-133">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="7178b-133">Property name</span></span> | <span data-ttu-id="7178b-134">Vērtība</span><span class="sxs-lookup"><span data-stu-id="7178b-134">Value</span></span>          | <span data-ttu-id="7178b-135">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7178b-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="7178b-136">Rindkopa</span><span class="sxs-lookup"><span data-stu-id="7178b-136">Paragraph</span></span>     | <span data-ttu-id="7178b-137">Rindkopas teksts</span><span class="sxs-lookup"><span data-stu-id="7178b-137">Paragraph text</span></span> | <span data-ttu-id="7178b-138">Teksts, kas pievienots katram saturam bagātinātajam bloka elementam.</span><span class="sxs-lookup"><span data-stu-id="7178b-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="7178b-139">Tiek atbalstītas dažas pamata bagātināta teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts.</span><span class="sxs-lookup"><span data-stu-id="7178b-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="7178b-140">Satura bagātinātā bloka moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="7178b-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="7178b-141">Lai pievienotu satura bagātinātā bloka moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="7178b-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7178b-142">Izveidojiet lapas veidni ar nosaukumu **Satura veidne**.</span><span class="sxs-lookup"><span data-stu-id="7178b-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="7178b-143">Noklusējuma lapas **Galvenajā** slotā pievienojiet satura bagātinātā bloka moduli.</span><span class="sxs-lookup"><span data-stu-id="7178b-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="7178b-144">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="7178b-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="7178b-145">Izmantojiet jūsu tikko izveidoto satura veidni, lai izveidotu lapu ar nosaukumu **Satura lapa**.</span><span class="sxs-lookup"><span data-stu-id="7178b-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="7178b-146">Jaunās lapas **Galvenajā** slotā pievienojiet satura bagātinātā bloka moduli.</span><span class="sxs-lookup"><span data-stu-id="7178b-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="7178b-147">Satura bagātinātā bloka moduļa rekvizītos iestatiet kolonnu skaitu uz **2**.</span><span class="sxs-lookup"><span data-stu-id="7178b-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="7178b-148">Satura bagātinātā bloka modulī atlasiet **Pievienot moduli**un pievienojiet satura bagātinātā bloka elementu (piemēram, **elements1**).</span><span class="sxs-lookup"><span data-stu-id="7178b-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="7178b-149">Jaunajā satura bagātinātā bloka elementā pievienojiet rindkopas tekstu.</span><span class="sxs-lookup"><span data-stu-id="7178b-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="7178b-150">Satura bagātinātā bloka modulī atlasiet **Pievienot moduli**un pievienojiet satura bagātinātā bloka elementu (piemēram, **elements2**).</span><span class="sxs-lookup"><span data-stu-id="7178b-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="7178b-151">Jaunajā satura bagātinātā bloka elementā pievienojiet rindkopas tekstu.</span><span class="sxs-lookup"><span data-stu-id="7178b-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="7178b-152">Saglabājiet lapu un priekšskatiet izmaiņas</span><span class="sxs-lookup"><span data-stu-id="7178b-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="7178b-153">Divu kolonnu skatā ir jāredz divi bagātināta teksta bloki.</span><span class="sxs-lookup"><span data-stu-id="7178b-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="7178b-154">Pārbaudiet lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="7178b-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="7178b-155">Ja pievienojat trešo satura bagātinātā bloka elementu, tas tiks novietots zem diviem iepriekš pievienotajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="7178b-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="7178b-156">Mainot kolonnu skaitu un elementus konteinerā, varat iegūt dažādus izkārtojumus teksta saturam.</span><span class="sxs-lookup"><span data-stu-id="7178b-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7178b-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7178b-157">Additional resources</span></span>

[<span data-ttu-id="7178b-158">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="7178b-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7178b-159">Brīdinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="7178b-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="7178b-160">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="7178b-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="7178b-161">Satura izvietojuma modulis</span><span class="sxs-lookup"><span data-stu-id="7178b-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="7178b-162">Līdzekļa modulis</span><span class="sxs-lookup"><span data-stu-id="7178b-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="7178b-163">Centrālais modulis</span><span class="sxs-lookup"><span data-stu-id="7178b-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="7178b-164">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="7178b-164">Video player module</span></span>](add-video-player.md)

