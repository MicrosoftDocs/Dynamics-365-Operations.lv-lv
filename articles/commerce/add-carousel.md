---
title: Karuseļa modulis
description: Šajā tēmā tiek stāstīts par karuseļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269732"
---
# <a name="carousel-module"></a><span data-ttu-id="cfe31-103">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="cfe31-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cfe31-104">Šajā tēmā tiek stāstīts par karuseļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cfe31-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cfe31-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="cfe31-105">Overview</span></span>

<span data-ttu-id="cfe31-106">Karuseļa modulis tiek izmantots, lai izvietotu vairākus veicināšanas elementus (ieskaitot bagātinātus attēlus) rotējošā karuseļa reklāmlogā, ko klienti var pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="cfe31-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="cfe31-107">Piemēram, mazumtirgotājs var izmantot karuseļa moduli sākumlapā, lai parādītu vairākas jaunas preces vai veicināšanas pasākumus.</span><span class="sxs-lookup"><span data-stu-id="cfe31-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="cfe31-108">Karuseļa modulī varat pievienot satura bloka moduļus.</span><span class="sxs-lookup"><span data-stu-id="cfe31-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="cfe31-109">Karuseļa moduļa rekvizīti nosaka, kā šie moduļi tiek atveidoti.</span><span class="sxs-lookup"><span data-stu-id="cfe31-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="cfe31-110">Karuseļa moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="cfe31-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="cfe31-111">Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="cfe31-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="cfe31-112">Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots preču informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="cfe31-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="cfe31-113">Karuseli var izmantot jebkurā mārketinga lapā, lai reklamētu vairākus veicināšanas pasākumus vai preces.</span><span class="sxs-lookup"><span data-stu-id="cfe31-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="cfe31-114">Karuseļa moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="cfe31-114">Carousel module properties</span></span>

| <span data-ttu-id="cfe31-115">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="cfe31-115">Property name</span></span>             | <span data-ttu-id="cfe31-116">Vērtība</span><span class="sxs-lookup"><span data-stu-id="cfe31-116">Value</span></span>                 | <span data-ttu-id="cfe31-117">Apraksts</span><span class="sxs-lookup"><span data-stu-id="cfe31-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="cfe31-118">Automātiskā atskaņošana</span><span class="sxs-lookup"><span data-stu-id="cfe31-118">Autoplay</span></span>                  | <span data-ttu-id="cfe31-119">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="cfe31-119">**True** or **False**</span></span> | <span data-ttu-id="cfe31-120">Ja vērtība ir iestatīta uz **Patiess**, pāreja starp elementiem karuselī tiek veikta automātiski.</span><span class="sxs-lookup"><span data-stu-id="cfe31-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="cfe31-121">Ja vērtība ir iestatīta uz **Nepatiess**, pāreja netiek veikta, ja vien klients neizmanto tastatūru vai peli, lai pārvietotos no viena elementa uz nākamo.</span><span class="sxs-lookup"><span data-stu-id="cfe31-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="cfe31-122"> Slaidu pārejas intervāls</span><span class="sxs-lookup"><span data-stu-id="cfe31-122">Slide transition interval</span></span> | <span data-ttu-id="cfe31-123">Vērtība sekundēs</span><span class="sxs-lookup"><span data-stu-id="cfe31-123">A value in seconds</span></span>    | <span data-ttu-id="cfe31-124">Intervāls pārejām starp elementiem.</span><span class="sxs-lookup"><span data-stu-id="cfe31-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="cfe31-125">Pārejas veids</span><span class="sxs-lookup"><span data-stu-id="cfe31-125">Transition type</span></span>           | <span data-ttu-id="cfe31-126">**Slīdināt** vai **Izbalēt**</span><span class="sxs-lookup"><span data-stu-id="cfe31-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="cfe31-127">Pārejas efekts starp vienumiem.</span><span class="sxs-lookup"><span data-stu-id="cfe31-127">The transition effect between items.</span></span> |
| <span data-ttu-id="cfe31-128">Paslēpt karuseļa apvēršanas indikatoru</span><span class="sxs-lookup"><span data-stu-id="cfe31-128">Hide carousel flipper</span></span>     | <span data-ttu-id="cfe31-129">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="cfe31-129">**True** or **False**</span></span> | <span data-ttu-id="cfe31-130">Ja vērtība ir iestatīta uz **Patiess**, karuseļa ziņojums un secības indikators ir slēpts.</span><span class="sxs-lookup"><span data-stu-id="cfe31-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="cfe31-131">Atļaut karuseļa noraidīšanu</span><span class="sxs-lookup"><span data-stu-id="cfe31-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="cfe31-132">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="cfe31-132">**True** or **False**</span></span> | <span data-ttu-id="cfe31-133">Ja vērtība ir iestatīta uz **Patiess**, lietotāji var noraidīt karuseli.</span><span class="sxs-lookup"><span data-stu-id="cfe31-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="cfe31-134">Karuseļa moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="cfe31-134">Add a carousel module to a page</span></span>

<span data-ttu-id="cfe31-135">Lai pievienotu karuseļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="cfe31-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="cfe31-136">Atlasiet **Jauns**, lai izveidotu lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="cfe31-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="cfe31-137">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Karuseļa veidni** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cfe31-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="cfe31-138">Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.</span><span class="sxs-lookup"><span data-stu-id="cfe31-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="cfe31-139">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="cfe31-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="cfe31-140">Izmantojiet jūsu tikko izveidoto karuseļa veidni lapas ar nosaukumu **Karuseļa lapa** izveidei.</span><span class="sxs-lookup"><span data-stu-id="cfe31-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="cfe31-141">Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="cfe31-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="cfe31-142">Rūtī pa labi iestatiet vērtību **Platums** sadaļai **Aizpildīt ekrānu**.</span><span class="sxs-lookup"><span data-stu-id="cfe31-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="cfe31-143">Sadaļā **Lapas struktūra** pievienojiet karuseļa moduli konteinera modulim.</span><span class="sxs-lookup"><span data-stu-id="cfe31-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="cfe31-144">Pievienojiet satura bloka moduli karuseļa modulim.</span><span class="sxs-lookup"><span data-stu-id="cfe31-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="cfe31-145">Iestatiet satura bloka moduļa rekvizītus, sniedzot **Virsraksts**, **Saite**, **Izkārtojums** un citus rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="cfe31-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="cfe31-146">Pievienojiet un konfigurējiet citu satura bloka moduli.</span><span class="sxs-lookup"><span data-stu-id="cfe31-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="cfe31-147">Iestatiet papildu rekvizītus karuseļa modulim, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="cfe31-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="cfe31-148">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="cfe31-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="cfe31-149">Lapā ir jāparāda karuselis, kurā ir divi moduļi (centrālais modulis un līdzekļa modulis).</span><span class="sxs-lookup"><span data-stu-id="cfe31-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="cfe31-150">Lai sasniegtu vēlamo efektu, varat mainīt papildus rekvizītus karuselim, centrālajam un līdzekļa modulim.</span><span class="sxs-lookup"><span data-stu-id="cfe31-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="cfe31-151">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="cfe31-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfe31-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cfe31-152">Additional resources</span></span>

[<span data-ttu-id="cfe31-153">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="cfe31-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cfe31-154">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="cfe31-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="cfe31-155">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="cfe31-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="cfe31-156">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="cfe31-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="cfe31-157">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="cfe31-157">Video player module</span></span>](add-video-player.md)
