---
title: Karuseļa modulis
description: Šajā tēmā tiek stāstīts par karuseļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785241"
---
# <a name="carousel-module"></a><span data-ttu-id="aacff-103">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="aacff-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="aacff-104">Šajā tēmā tiek stāstīts par karuseļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aacff-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aacff-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="aacff-105">Overview</span></span>

<span data-ttu-id="aacff-106">Karuseļa modulis tiek izmantots, lai izvietotu vairākus reklāmas elementus karuselī, ko klienti var pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="aacff-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="aacff-107">Tas ir īpašs konteinera modulis, kas vieso citus moduļus.</span><span class="sxs-lookup"><span data-stu-id="aacff-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="aacff-108">Piemēram, mazumtirgotājs var izmantot karuseļa moduli sākumlapā, lai parādītu vairākas jaunas preces vai veicināšanas pasākumus.</span><span class="sxs-lookup"><span data-stu-id="aacff-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="aacff-109">Karuseļa modulī varat pievienot centrālos un funkciju moduļus.</span><span class="sxs-lookup"><span data-stu-id="aacff-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="aacff-110">Karuseļa moduļa rekvizīti nosaka, kā šie moduļi tiek atveidoti.</span><span class="sxs-lookup"><span data-stu-id="aacff-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="aacff-111">Karuseļa moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="aacff-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="aacff-112">Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="aacff-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="aacff-113">Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots preču informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="aacff-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="aacff-114">Karuseli var izmantot jebkurā mārketinga lapā, lai reklamētu vairākus veicināšanas pasākumus vai preces.</span><span class="sxs-lookup"><span data-stu-id="aacff-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="aacff-115">Karuseļa moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="aacff-115">Carousel module properties</span></span>

| <span data-ttu-id="aacff-116">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="aacff-116">Property name</span></span>             | <span data-ttu-id="aacff-117">Vērtība</span><span class="sxs-lookup"><span data-stu-id="aacff-117">Value</span></span>                                | <span data-ttu-id="aacff-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="aacff-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="aacff-119">Automātiskā atskaņošana</span><span class="sxs-lookup"><span data-stu-id="aacff-119">Autoplay</span></span>                  | <span data-ttu-id="aacff-120">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="aacff-120">**True** or **False**</span></span>                | <span data-ttu-id="aacff-121">Ja vērtība ir iestatīta uz **Patiess**, pāreja starp elementiem karuselī tiek veikta automātiski.</span><span class="sxs-lookup"><span data-stu-id="aacff-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="aacff-122">Ja vērtība ir iestatīta uz **Nepatiess**, pāreja netiek veikta, ja vien klients neizmanto tastatūru vai peli, lai pārvietotos no viena elementa uz nākamo.</span><span class="sxs-lookup"><span data-stu-id="aacff-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="aacff-123"> Slaidu pārejas intervāls</span><span class="sxs-lookup"><span data-stu-id="aacff-123">Slide transition interval</span></span> | <span data-ttu-id="aacff-124">Vērtība sekundēs</span><span class="sxs-lookup"><span data-stu-id="aacff-124">A value in seconds</span></span>                   | <span data-ttu-id="aacff-125">Intervāls pārejām starp elementiem.</span><span class="sxs-lookup"><span data-stu-id="aacff-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="aacff-126">Pārejas animācija</span><span class="sxs-lookup"><span data-stu-id="aacff-126">Transition animation</span></span>      | <span data-ttu-id="aacff-127">**Slīdināt** vai **Izbalēt**</span><span class="sxs-lookup"><span data-stu-id="aacff-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="aacff-128">Pārejas efekts.</span><span class="sxs-lookup"><span data-stu-id="aacff-128">The transition effect.</span></span> |
| <span data-ttu-id="aacff-129">Platums</span><span class="sxs-lookup"><span data-stu-id="aacff-129">Width</span></span>                     | <span data-ttu-id="aacff-130">**Ietilpināt konteinerā** vai **Pilnekrāna režīms**</span><span class="sxs-lookup"><span data-stu-id="aacff-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="aacff-131">Ja vērtība ir iestatīta uz **Ietilpināt konteinerā**, tad elementi karuselī tiek ierobežoti ar karuseļa platumu.</span><span class="sxs-lookup"><span data-stu-id="aacff-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="aacff-132">Ja vērtība ir iestatīta uz **Aizpildīt ekrānu**, elementi neaprobežojas ar karuseļa platumu, bet var pāriet pilnekrāna režīmā.</span><span class="sxs-lookup"><span data-stu-id="aacff-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="aacff-133">Varat mainīt vērtību, lai sasniegtu vēlamo izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="aacff-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="aacff-134">Karuseļa moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="aacff-134">Add a carousel module to a page</span></span>

<span data-ttu-id="aacff-135">Lai pievienotu karuseļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="aacff-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="aacff-136">Izveidojiet lapas veidni ar nosaukumu **karuseļa veidne**.</span><span class="sxs-lookup"><span data-stu-id="aacff-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="aacff-137">Noklusējuma lapas **Galvenajā** slotā pievienojiet karuseļa moduli.</span><span class="sxs-lookup"><span data-stu-id="aacff-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="aacff-138">Pievienojiet centrālo moduli karuseļa modulim.</span><span class="sxs-lookup"><span data-stu-id="aacff-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="aacff-139">Pievienojiet līdzekļa moduli karuseļa modulim.</span><span class="sxs-lookup"><span data-stu-id="aacff-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="aacff-140">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="aacff-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="aacff-141">Izmantojiet jūsu tikko izveidoto karuseļa veidni lapas ar nosaukumu **karuseļa lapa** izveidei.</span><span class="sxs-lookup"><span data-stu-id="aacff-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="aacff-142">Jaunās lapas **Galvenajā** slotā pievienojiet karuseļa moduli.</span><span class="sxs-lookup"><span data-stu-id="aacff-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="aacff-143">Iestatiet karuseļa moduļa rekvizītu **Platums**, lai **Aizpildītu ekrānu**.</span><span class="sxs-lookup"><span data-stu-id="aacff-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="aacff-144">Iestatiet rekvizītu **Pārejas animācija** uz **Slīdināt**.</span><span class="sxs-lookup"><span data-stu-id="aacff-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="aacff-145">Pievienojiet centrālo moduli karuseļa modulim.</span><span class="sxs-lookup"><span data-stu-id="aacff-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="aacff-146">Centrālajā modulī pievienojiet attēlu un virsrakstu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="aacff-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="aacff-147">Pievienojiet līdzekļa moduli karuseļa modulim.</span><span class="sxs-lookup"><span data-stu-id="aacff-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="aacff-148">Līdzekļa modulī pievienojiet attēlu, virsrakstu un teksta rindkopu.</span><span class="sxs-lookup"><span data-stu-id="aacff-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="aacff-149">Saglabājiet un priekšskatiet lapu.</span><span class="sxs-lookup"><span data-stu-id="aacff-149">Save and preview the page.</span></span> <span data-ttu-id="aacff-150">Lapā ir jāparāda karuselis, kurā ir divi moduļi (centrālais modulis un līdzekļa modulis).</span><span class="sxs-lookup"><span data-stu-id="aacff-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="aacff-151">Lai sasniegtu vēlamo efektu, varat mainīt papildus rekvizītus karuselim, centrālajam un līdzekļa modulim.</span><span class="sxs-lookup"><span data-stu-id="aacff-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="aacff-152">Pārbaudiet lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="aacff-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aacff-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="aacff-153">Additional resources</span></span>

[<span data-ttu-id="aacff-154">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="aacff-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aacff-155">Brīdinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="aacff-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="aacff-156">Bagātinātā satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="aacff-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="aacff-157">Satura izvietojuma modulis</span><span class="sxs-lookup"><span data-stu-id="aacff-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="aacff-158">Līdzekļa modulis</span><span class="sxs-lookup"><span data-stu-id="aacff-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="aacff-159">Centrālais modulis</span><span class="sxs-lookup"><span data-stu-id="aacff-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="aacff-160">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="aacff-160">Video player module</span></span>](add-video-player.md)
