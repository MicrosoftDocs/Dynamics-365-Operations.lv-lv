---
title: Karuseļa modulis
description: Šajā tēmā tiek stāstīts par karuseļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0b4ce8fdb7b598e55db59ddf5a99a0ba46eb6f91
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986008"
---
# <a name="carousel-module"></a><span data-ttu-id="627e3-103">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="627e3-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="627e3-104">Šajā tēmā tiek stāstīts par karuseļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="627e3-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="627e3-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="627e3-105">Overview</span></span>

<span data-ttu-id="627e3-106">Karuseļa modulis tiek izmantots, lai izvietotu vairākus veicināšanas elementus (ieskaitot bagātinātus attēlus) rotējošā karuseļa reklāmlogā, ko klienti var pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="627e3-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="627e3-107">Piemēram, mazumtirgotājs var izmantot karuseļa moduli sākumlapā, lai parādītu vairākas jaunas preces vai veicināšanas pasākumus.</span><span class="sxs-lookup"><span data-stu-id="627e3-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="627e3-108">Karuseļa modulī varat pievienot satura bloka moduļus.</span><span class="sxs-lookup"><span data-stu-id="627e3-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="627e3-109">Karuseļa moduļa rekvizīti nosaka, kā šie moduļi tiek atveidoti.</span><span class="sxs-lookup"><span data-stu-id="627e3-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="627e3-110">Karuseļa moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="627e3-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="627e3-111">Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="627e3-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="627e3-112">Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots preču informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="627e3-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="627e3-113">Karuseli var izmantot jebkurā mārketinga lapā, lai reklamētu vairākus veicināšanas pasākumus vai preces.</span><span class="sxs-lookup"><span data-stu-id="627e3-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="627e3-114">Attēlā zemāk redzams piemērs karuseļa modulim, kas tiek izmantots sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="627e3-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="627e3-115">Šajā karuseļa modulī ir vairāki satura bloka elementi.</span><span class="sxs-lookup"><span data-stu-id="627e3-115">This carousel module contains multiple content block items.</span></span>

![Karuseļa moduļa piemērs](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="627e3-117">Karuseļa moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="627e3-117">Carousel module properties</span></span>

| <span data-ttu-id="627e3-118">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="627e3-118">Property name</span></span>             | <span data-ttu-id="627e3-119">Vērtība</span><span class="sxs-lookup"><span data-stu-id="627e3-119">Value</span></span>                 | <span data-ttu-id="627e3-120">apraksts</span><span class="sxs-lookup"><span data-stu-id="627e3-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="627e3-121">Automātiskā atskaņošana</span><span class="sxs-lookup"><span data-stu-id="627e3-121">Autoplay</span></span>                  | <span data-ttu-id="627e3-122">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="627e3-122">**True** or **False**</span></span> | <span data-ttu-id="627e3-123">Ja vērtība ir iestatīta uz **Patiess**, pāreja starp elementiem karuselī tiek veikta automātiski.</span><span class="sxs-lookup"><span data-stu-id="627e3-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="627e3-124">Ja vērtība ir iestatīta uz **Nepatiess**, pāreja netiek veikta, ja vien klients neizmanto tastatūru vai peli, lai pārvietotos no viena elementa uz nākamo.</span><span class="sxs-lookup"><span data-stu-id="627e3-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="627e3-125">Slaidu pārejas intervāls</span><span class="sxs-lookup"><span data-stu-id="627e3-125">Slide transition interval</span></span> | <span data-ttu-id="627e3-126">Vērtība sekundēs</span><span class="sxs-lookup"><span data-stu-id="627e3-126">A value in seconds</span></span>    | <span data-ttu-id="627e3-127">Intervāls pārejām starp elementiem.</span><span class="sxs-lookup"><span data-stu-id="627e3-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="627e3-128">Pārejas veids</span><span class="sxs-lookup"><span data-stu-id="627e3-128">Transition type</span></span>           | <span data-ttu-id="627e3-129">**Slīdināt** vai **Izbalēt**</span><span class="sxs-lookup"><span data-stu-id="627e3-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="627e3-130">Pārejas efekts starp vienumiem.</span><span class="sxs-lookup"><span data-stu-id="627e3-130">The transition effect between items.</span></span> |
| <span data-ttu-id="627e3-131">Paslēpt karuseļa apvēršanas indikatoru</span><span class="sxs-lookup"><span data-stu-id="627e3-131">Hide carousel flipper</span></span>     | <span data-ttu-id="627e3-132">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="627e3-132">**True** or **False**</span></span> | <span data-ttu-id="627e3-133">Ja vērtība ir iestatīta uz **Patiess**, karuseļa ziņojums un secības indikators ir slēpts.</span><span class="sxs-lookup"><span data-stu-id="627e3-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="627e3-134">Atļaut karuseļa noraidīšanu</span><span class="sxs-lookup"><span data-stu-id="627e3-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="627e3-135">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="627e3-135">**True** or **False**</span></span> | <span data-ttu-id="627e3-136">Ja vērtība ir iestatīta uz **Patiess**, lietotāji var noraidīt karuseli.</span><span class="sxs-lookup"><span data-stu-id="627e3-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="627e3-137">Karuseļa moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="627e3-137">Add a carousel module to a page</span></span>

<span data-ttu-id="627e3-138">Lai pievienotu karuseļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="627e3-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="627e3-139">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="627e3-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="627e3-140">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Karuseļa veidni** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="627e3-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="627e3-141">Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.</span><span class="sxs-lookup"><span data-stu-id="627e3-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="627e3-142">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="627e3-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="627e3-143">Izmantojiet jūsu tikko izveidoto karuseļa veidni lapas ar nosaukumu **Karuseļa lapa** izveidei.</span><span class="sxs-lookup"><span data-stu-id="627e3-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="627e3-144">Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="627e3-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="627e3-145">Rūtī pa labi iestatiet vērtību **Platums** sadaļai **Aizpildīt ekrānu**.</span><span class="sxs-lookup"><span data-stu-id="627e3-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="627e3-146">Sadaļā **Lapas struktūra** pievienojiet karuseļa moduli konteinera modulim.</span><span class="sxs-lookup"><span data-stu-id="627e3-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="627e3-147">Pievienojiet satura bloka moduli karuseļa modulim.</span><span class="sxs-lookup"><span data-stu-id="627e3-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="627e3-148">Iestatiet satura bloka moduļa rekvizītus, sniedzot **Virsraksts**, **Saite**, **Izkārtojums** un citus rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="627e3-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="627e3-149">Pievienojiet un konfigurējiet citu satura bloka moduli.</span><span class="sxs-lookup"><span data-stu-id="627e3-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="627e3-150">Iestatiet papildu rekvizītus karuseļa modulim, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="627e3-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="627e3-151">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="627e3-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="627e3-152">Lapā ir jāparāda karuselis, kurā ir divi moduļi (centrālais modulis un līdzekļa modulis).</span><span class="sxs-lookup"><span data-stu-id="627e3-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="627e3-153">Lai sasniegtu vēlamo efektu, varat mainīt papildus rekvizītus karuselim, centrālajam un līdzekļa modulim.</span><span class="sxs-lookup"><span data-stu-id="627e3-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="627e3-154">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="627e3-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="627e3-155">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="627e3-155">Additional resources</span></span>

[<span data-ttu-id="627e3-156">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="627e3-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="627e3-157">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="627e3-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="627e3-158">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="627e3-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="627e3-159">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="627e3-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="627e3-160">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="627e3-160">Video player module</span></span>](add-video-player.md)
