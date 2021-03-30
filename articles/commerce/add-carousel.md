---
title: Karuseļa modulis
description: Šajā tēmā aplūkoti Carousel moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 5333ecd7a1fe4f60684fa5f5bb3ac9f98efde6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206515"
---
# <a name="carousel-module"></a><span data-ttu-id="6dd79-103">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="6dd79-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6dd79-104">Šajā tēmā aplūkoti Carousel moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6dd79-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6dd79-105">Karuseļa modulis tiek izmantots, lai izvietotu vairākus veicināšanas elementus (ieskaitot bagātinātus attēlus) rotējošā karuseļa reklāmlogā, ko klienti var pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="6dd79-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="6dd79-106">Piemēram, mazumtirgotājs var izmantot karuseļa moduli sākumlapā, lai parādītu vairākas jaunas preces vai veicināšanas pasākumus.</span><span class="sxs-lookup"><span data-stu-id="6dd79-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="6dd79-107">Karuseļa modulī varat pievienot satura bloka moduļus.</span><span class="sxs-lookup"><span data-stu-id="6dd79-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="6dd79-108">Karuseļa moduļa rekvizīti nosaka, kā šie moduļi tiek atveidoti.</span><span class="sxs-lookup"><span data-stu-id="6dd79-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="6dd79-109">Karuseļa moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="6dd79-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="6dd79-110">Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="6dd79-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="6dd79-111">Karuselis, kurā ir vairāki reklāmas moduļi tajā, var tikt izmantots preču informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="6dd79-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="6dd79-112">Karuseli var izmantot jebkurā mārketinga lapā, lai reklamētu vairākus veicināšanas pasākumus vai preces.</span><span class="sxs-lookup"><span data-stu-id="6dd79-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="6dd79-113">Attēlā zemāk redzams piemērs karuseļa modulim, kas tiek izmantots sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="6dd79-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="6dd79-114">Šajā karuseļa modulī ir vairāki satura bloka elementi.</span><span class="sxs-lookup"><span data-stu-id="6dd79-114">This carousel module contains multiple content block items.</span></span>

![Karuseļa moduļa piemērs](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="6dd79-116">Karuseļa moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="6dd79-116">Carousel module properties</span></span>

| <span data-ttu-id="6dd79-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="6dd79-117">Property name</span></span>             | <span data-ttu-id="6dd79-118">Vērtība</span><span class="sxs-lookup"><span data-stu-id="6dd79-118">Value</span></span>                 | <span data-ttu-id="6dd79-119">apraksts</span><span class="sxs-lookup"><span data-stu-id="6dd79-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="6dd79-120">Automātiskā atskaņošana</span><span class="sxs-lookup"><span data-stu-id="6dd79-120">Autoplay</span></span>                  | <span data-ttu-id="6dd79-121">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="6dd79-121">**True** or **False**</span></span> | <span data-ttu-id="6dd79-122">Ja vērtība ir iestatīta uz **Patiess**, pāreja starp elementiem karuselī tiek veikta automātiski.</span><span class="sxs-lookup"><span data-stu-id="6dd79-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="6dd79-123">Ja vērtība ir iestatīta uz **Nepatiess**, pāreja netiek veikta, ja vien klients neizmanto tastatūru vai peli, lai pārvietotos no viena elementa uz nākamo.</span><span class="sxs-lookup"><span data-stu-id="6dd79-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="6dd79-124">Slaidu pārejas intervāls</span><span class="sxs-lookup"><span data-stu-id="6dd79-124">Slide transition interval</span></span> | <span data-ttu-id="6dd79-125">Vērtība sekundēs</span><span class="sxs-lookup"><span data-stu-id="6dd79-125">A value in seconds</span></span>    | <span data-ttu-id="6dd79-126">Intervāls pārejām starp elementiem.</span><span class="sxs-lookup"><span data-stu-id="6dd79-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="6dd79-127">Pārejas veids</span><span class="sxs-lookup"><span data-stu-id="6dd79-127">Transition type</span></span>           | <span data-ttu-id="6dd79-128">**Slīdināt** vai **Izbalēt**</span><span class="sxs-lookup"><span data-stu-id="6dd79-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="6dd79-129">Pārejas efekts starp vienumiem.</span><span class="sxs-lookup"><span data-stu-id="6dd79-129">The transition effect between items.</span></span> |
| <span data-ttu-id="6dd79-130">Paslēpt karuseļa apvēršanas indikatoru</span><span class="sxs-lookup"><span data-stu-id="6dd79-130">Hide carousel flipper</span></span>     | <span data-ttu-id="6dd79-131">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="6dd79-131">**True** or **False**</span></span> | <span data-ttu-id="6dd79-132">Ja vērtība ir iestatīta uz **Patiess**, karuseļa ziņojums un secības indikators ir slēpts.</span><span class="sxs-lookup"><span data-stu-id="6dd79-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="6dd79-133">Atļaut karuseļa noraidīšanu</span><span class="sxs-lookup"><span data-stu-id="6dd79-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="6dd79-134">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="6dd79-134">**True** or **False**</span></span> | <span data-ttu-id="6dd79-135">Ja vērtība ir iestatīta uz **Patiess**, lietotāji var noraidīt karuseli.</span><span class="sxs-lookup"><span data-stu-id="6dd79-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="6dd79-136">Karuseļa moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="6dd79-136">Add a carousel module to a page</span></span>

<span data-ttu-id="6dd79-137">Lai pievienotu karuseļa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="6dd79-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6dd79-138">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="6dd79-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="6dd79-139">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Karuseļa veidni** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6dd79-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="6dd79-140">Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.</span><span class="sxs-lookup"><span data-stu-id="6dd79-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="6dd79-141">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="6dd79-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="6dd79-142">Izmantojiet jūsu tikko izveidoto karuseļa veidni lapas ar nosaukumu **Karuseļa lapa** izveidei.</span><span class="sxs-lookup"><span data-stu-id="6dd79-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="6dd79-143">Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="6dd79-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="6dd79-144">Rūtī pa labi iestatiet vērtību **Platums** sadaļai **Aizpildīt ekrānu**.</span><span class="sxs-lookup"><span data-stu-id="6dd79-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="6dd79-145">Sadaļā **Lapas struktūra** pievienojiet karuseļa moduli konteinera modulim.</span><span class="sxs-lookup"><span data-stu-id="6dd79-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="6dd79-146">Pievienojiet satura bloka moduli karuseļa modulim.</span><span class="sxs-lookup"><span data-stu-id="6dd79-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="6dd79-147">Iestatiet satura bloka moduļa rekvizītus, sniedzot **Virsraksts**, **Saite**, **Izkārtojums** un citus rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="6dd79-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="6dd79-148">Pievienojiet un konfigurējiet citu satura bloka moduli.</span><span class="sxs-lookup"><span data-stu-id="6dd79-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="6dd79-149">Iestatiet papildu rekvizītus karuseļa modulim, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="6dd79-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="6dd79-150">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="6dd79-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="6dd79-151">Lapā ir jāparāda karuselis, kurā ir divi moduļi (centrālais modulis un līdzekļa modulis).</span><span class="sxs-lookup"><span data-stu-id="6dd79-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="6dd79-152">Lai sasniegtu vēlamo efektu, varat mainīt papildus rekvizītus karuselim, centrālajam un līdzekļa modulim.</span><span class="sxs-lookup"><span data-stu-id="6dd79-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="6dd79-153">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="6dd79-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dd79-154">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6dd79-154">Additional resources</span></span>

[<span data-ttu-id="6dd79-155">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="6dd79-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6dd79-156">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="6dd79-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="6dd79-157">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="6dd79-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="6dd79-158">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="6dd79-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="6dd79-159">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="6dd79-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]