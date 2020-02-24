---
title: Veicināšanas reklāmkarogu modulis
description: Šajā tēmā tiek stāstīts par veicināšanas reklāmlogu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025624"
---
# <a name="promo-banner-module"></a><span data-ttu-id="d0516-103">Veicināšanas reklāmkarogu modulis</span><span class="sxs-lookup"><span data-stu-id="d0516-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d0516-104">Šajā tēmā tiek stāstīts par veicināšanas reklāmlogu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d0516-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d0516-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="d0516-105">Overview</span></span>

<span data-ttu-id="d0516-106">Veicināšanas reklāmlogu moduļi tiek izmantoti, lai lapā rādītu iekļautos informatīvos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="d0516-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="d0516-107">Tos var izmantot, lai visā vietnē rādītu veicināšanas pasākumus, kas tiek rādīti visās e-komercijas vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="d0516-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="d0516-108">Veicināšanas reklāmlogu moduļi atbalsta teksta ziņojumu un saiti.</span><span class="sxs-lookup"><span data-stu-id="d0516-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="d0516-109">Ja vairāki ziņojumi ir pievienoti veicināšanas reklāmlogu modulim, tas kļūst par rotējošu karuseļa reklāmkarogu, kas ļaus klientiem pārlūkot visus ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="d0516-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="d0516-110">Veicināšanas reklāmlogu moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="d0516-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="d0516-111">Lietojuma piemēri veicināšanas reklāmlogiem e-Commerce sistēmā</span><span class="sxs-lookup"><span data-stu-id="d0516-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="d0516-112">Veicināšanas reklāmlogus var izmantot vietnes galvenē, lai parādītu veicināšanas pasākumus vai ziņojumus visā vietnē, kā tas ir tālāk esošajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="d0516-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="d0516-113">“Ikgadējā pārdošana beidzas pēc 10 dienām”</span><span class="sxs-lookup"><span data-stu-id="d0516-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="d0516-114">“Labi ietaupiet ar skolas sākuma izpārdošanu.</span><span class="sxs-lookup"><span data-stu-id="d0516-114">"Save big with back to school sale.</span></span> <span data-ttu-id="d0516-115">Iepērcieties tūlīt.”</span><span class="sxs-lookup"><span data-stu-id="d0516-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="d0516-116">Veicināšanas reklāmkarogu moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d0516-116">Promo banner module properties</span></span>

| <span data-ttu-id="d0516-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="d0516-117">Property name</span></span>             | <span data-ttu-id="d0516-118">Value</span><span class="sxs-lookup"><span data-stu-id="d0516-118">Value</span></span>                              | <span data-ttu-id="d0516-119">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d0516-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="d0516-120">Reklāmkaroga ziņojumi</span><span class="sxs-lookup"><span data-stu-id="d0516-120">Banner messages</span></span>           | <span data-ttu-id="d0516-121">Teksts un saites</span><span class="sxs-lookup"><span data-stu-id="d0516-121">Text and links</span></span>                     | <span data-ttu-id="d0516-122">Teksta un saišu masīvs.</span><span class="sxs-lookup"><span data-stu-id="d0516-122">An array of text and links.</span></span> |
| <span data-ttu-id="d0516-123">Automātiskā atskaņošana</span><span class="sxs-lookup"><span data-stu-id="d0516-123">Autoplay</span></span>                  | <span data-ttu-id="d0516-124">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d0516-124">**True** or **False**</span></span>              | <span data-ttu-id="d0516-125">Vērtība, kas norāda, vai ziņojumi tiek automātiski iestatīti, ja ir konfigurēti vairāki ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="d0516-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="d0516-126"> Slaidu pārejas intervāls</span><span class="sxs-lookup"><span data-stu-id="d0516-126">Slide transition interval</span></span> | <span data-ttu-id="d0516-127">Milisekunžu skaits (ms)</span><span class="sxs-lookup"><span data-stu-id="d0516-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="d0516-128">Intervāls, ko izmanto, lai pārlūkotu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="d0516-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="d0516-129">Atļaut noraidīšanu</span><span class="sxs-lookup"><span data-stu-id="d0516-129">Allow dismiss</span></span>             | <span data-ttu-id="d0516-130">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d0516-130">**True** or **False**</span></span>              | <span data-ttu-id="d0516-131">Ja vērtība ir iestatīta uz **Patiess**, debitori var noraidīt brīdinājumu.</span><span class="sxs-lookup"><span data-stu-id="d0516-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="d0516-132">Rādīt karuseļveida ziņojumu</span><span class="sxs-lookup"><span data-stu-id="d0516-132">Show carousel flipper</span></span>     | <span data-ttu-id="d0516-133">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d0516-133">**True** or **False**</span></span>              | <span data-ttu-id="d0516-134">Vērtība, kas norāda, vai karuseļa paziņojumi ir jārāda, lai klienti varētu manuāli pārvietoties pa vairākiem reklāmkaroga vienumiem.</span><span class="sxs-lookup"><span data-stu-id="d0516-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="d0516-135">Teksta līdzinājums</span><span class="sxs-lookup"><span data-stu-id="d0516-135">Text alignment</span></span>            | <span data-ttu-id="d0516-136">**Pa labi**, **Pa kreisi** vai **Centrā**</span><span class="sxs-lookup"><span data-stu-id="d0516-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="d0516-137">Teksta līdzinājums veicināšanas reklāmkaroga modulī.</span><span class="sxs-lookup"><span data-stu-id="d0516-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="d0516-138">Saistīt</span><span class="sxs-lookup"><span data-stu-id="d0516-138">Link</span></span>                      | <span data-ttu-id="d0516-139">URL</span><span class="sxs-lookup"><span data-stu-id="d0516-139">A URL</span></span>                              | <span data-ttu-id="d0516-140">Vietrādis URL neobligātai vietnei.</span><span class="sxs-lookup"><span data-stu-id="d0516-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="d0516-141">Veicināšanas reklāmloga moduļa pievienošana jaunā lapā</span><span class="sxs-lookup"><span data-stu-id="d0516-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="d0516-142">Lai pievienotu veicināšanas reklāmloga moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="d0516-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d0516-143">Izveidojiet lapas veidni ar nosaukumu **Veicināšanas reklāmloga veidne**.</span><span class="sxs-lookup"><span data-stu-id="d0516-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="d0516-144">Sadaļā **Lapas struktūra** pievienojiet moduli **Noklusējuma lapa** slotam **Pamatteksts**.</span><span class="sxs-lookup"><span data-stu-id="d0516-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="d0516-145">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="d0516-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="d0516-146">Izmantojiet jūsu tikko izveidoto brīdinājuma veidni, lai izveidotu lapu ar nosaukumu **Veicināšanas reklāmloga lapa**.</span><span class="sxs-lookup"><span data-stu-id="d0516-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="d0516-147">Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="d0516-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="d0516-148">Rūtī pa labi iestatiet vērtību **Platums** sadaļai **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="d0516-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="d0516-149">Sadaļā **Lapas struktūra** pievienojiet veicināšanas reklāmkaroga moduli konteinera modulim.</span><span class="sxs-lookup"><span data-stu-id="d0516-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="d0516-150">Reklāmkaroga moduļa iestatījumos pievienojiet vienu vai vairākus reklāmkarogu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="d0516-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="d0516-151">Katrai ziņai var būt teksts kopā ar saiti.</span><span class="sxs-lookup"><span data-stu-id="d0516-151">Each message can have text together with a link.</span></span> <span data-ttu-id="d0516-152">Varat rediģēt pārējos rekvizītus, lai tālāk pielāgotu moduli.</span><span class="sxs-lookup"><span data-stu-id="d0516-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="d0516-153">Saglabājiet un priekšskatiet lapu.</span><span class="sxs-lookup"><span data-stu-id="d0516-153">Save and preview the page.</span></span> <span data-ttu-id="d0516-154">Lapas augšdaļā ieraudzīsiet brīdinājumu ar jūsu pievienoto tekstu.</span><span class="sxs-lookup"><span data-stu-id="d0516-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="d0516-155">Pabeidziet rediģēt lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="d0516-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="d0516-156">Veicināšanas reklāmlogs parasti tiek izmantots lapas galvenes slotā vai apakšvadītāja slotā.</span><span class="sxs-lookup"><span data-stu-id="d0516-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="d0516-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d0516-157">Additional resources</span></span>

[<span data-ttu-id="d0516-158">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="d0516-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d0516-159">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="d0516-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d0516-160">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="d0516-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d0516-161">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="d0516-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="d0516-162">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="d0516-162">Video player module</span></span>](add-video-player.md)
