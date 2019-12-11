---
title: Brīdinājuma modulis
description: Šajā tēmā ir ietverti brīdinājumu moduļi un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785356"
---
# <a name="alert-module"></a><span data-ttu-id="31760-103">Brīdinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="31760-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="31760-104">Šajā tēmā ir ietverti brīdinājumu moduļi un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="31760-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31760-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="31760-105">Overview</span></span>

<span data-ttu-id="31760-106">Brīdinājuma modulis tiek izmantots, lai lapā rādītu iekļautos informatīvos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="31760-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="31760-107">Brīdinājumu moduļi atbalsta teksta ziņojumu un saiti.</span><span class="sxs-lookup"><span data-stu-id="31760-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="31760-108">Tos var izmantot, lai visā vietnē rādītu veicināšanas pasākumus, kas tiek rādīti visās e-komercijas vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="31760-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="31760-109">Brīdinājumu moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="31760-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="31760-110">Brīdinājumu moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="31760-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="31760-111">Brīdinājumu moduļus var izmantot vietnes galvenē, lai norādītu vietnes veicināšanas pasākumus un ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="31760-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="31760-112">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="31760-112">Here are some examples:</span></span>

<span data-ttu-id="31760-113">“Ikgadējā pārdošana beidzas pēc 10 dienām”</span><span class="sxs-lookup"><span data-stu-id="31760-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="31760-114">“Labi ietaupiet ar skolas sākuma izpārdošanu.</span><span class="sxs-lookup"><span data-stu-id="31760-114">"Save big with back to school sale.</span></span> <span data-ttu-id="31760-115">Iepērcieties tūlīt.”</span><span class="sxs-lookup"><span data-stu-id="31760-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="31760-116">Brīdinājuma moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="31760-116">Alert module properties</span></span>

| <span data-ttu-id="31760-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="31760-117">Property name</span></span>  | <span data-ttu-id="31760-118">Vērtība</span><span class="sxs-lookup"><span data-stu-id="31760-118">Value</span></span>                              | <span data-ttu-id="31760-119">Apraksts</span><span class="sxs-lookup"><span data-stu-id="31760-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="31760-120">Teksts</span><span class="sxs-lookup"><span data-stu-id="31760-120">Text</span></span>           | <span data-ttu-id="31760-121">Teksts</span><span class="sxs-lookup"><span data-stu-id="31760-121">Text</span></span>                               | <span data-ttu-id="31760-122">Brīdinājuma modulī redzamais teksta ziņojums.</span><span class="sxs-lookup"><span data-stu-id="31760-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="31760-123">Teksta līdzinājums</span><span class="sxs-lookup"><span data-stu-id="31760-123">Text alignment</span></span> | <span data-ttu-id="31760-124">**Pa labi**, **Pa kreisi** vai **Centrā**</span><span class="sxs-lookup"><span data-stu-id="31760-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="31760-125">Vērtība, kas nosaka, kā brīdinājuma modulī tiek līdzināts teksts.</span><span class="sxs-lookup"><span data-stu-id="31760-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="31760-126">Noraidīt brīdinājumu</span><span class="sxs-lookup"><span data-stu-id="31760-126">Dismiss alert</span></span>  | <span data-ttu-id="31760-127">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="31760-127">**True** or **False**</span></span>              | <span data-ttu-id="31760-128">Ja vērtība ir iestatīta uz **Patiess**, klients var noraidīt brīdinājumu.</span><span class="sxs-lookup"><span data-stu-id="31760-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="31760-129">Saistīt</span><span class="sxs-lookup"><span data-stu-id="31760-129">Link</span></span>           | <span data-ttu-id="31760-130">URL</span><span class="sxs-lookup"><span data-stu-id="31760-130">URL</span></span>                                | <span data-ttu-id="31760-131">Vietrādis URL neobligātai vietnei.</span><span class="sxs-lookup"><span data-stu-id="31760-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="31760-132">Brīdinājuma moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="31760-132">Add an alert module to a page</span></span> 

<span data-ttu-id="31760-133">Lai pievienotu brīdinājuma moduli lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="31760-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="31760-134">Izveidojiet lapas veidni ar nosaukumu **brīdinājuma veidne**.</span><span class="sxs-lookup"><span data-stu-id="31760-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="31760-135">Noklusējuma lapas **Galvenajā** slotā pievienojiet brīdinājuma moduli.</span><span class="sxs-lookup"><span data-stu-id="31760-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="31760-136">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="31760-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="31760-137">Izmantojiet jūsu tikko izveidoto brīdinājuma veidni, lai izveidotu lapu ar nosaukumu **brīdinājuma lapa**.</span><span class="sxs-lookup"><span data-stu-id="31760-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="31760-138">Jaunās lapas **Galvenajā** slotā pievienojiet brīdinājuma moduli.</span><span class="sxs-lookup"><span data-stu-id="31760-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="31760-139">Brīdinājuma moduļa iestatījumos ievadiet brīdinājuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="31760-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="31760-140">Var rediģēt pārējos rekvizītus, ja vēlaties tālāk pielāgot brīdinājuma moduli.</span><span class="sxs-lookup"><span data-stu-id="31760-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="31760-141">Saglabājiet un priekšskatiet lapu.</span><span class="sxs-lookup"><span data-stu-id="31760-141">Save and preview the page.</span></span> <span data-ttu-id="31760-142">Lapas augšdaļā ieraudzīsiet brīdinājumu ar jūsu pievienoto tekstu.</span><span class="sxs-lookup"><span data-stu-id="31760-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="31760-143">Pārbaudiet lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="31760-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="31760-144">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="31760-144">Additional resources</span></span>

[<span data-ttu-id="31760-145">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="31760-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="31760-146">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="31760-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="31760-147">Bagātinātā satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="31760-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="31760-148">Satura izvietojuma modulis</span><span class="sxs-lookup"><span data-stu-id="31760-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="31760-149">Līdzekļa modulis</span><span class="sxs-lookup"><span data-stu-id="31760-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="31760-150">Centrālais modulis</span><span class="sxs-lookup"><span data-stu-id="31760-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="31760-151">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="31760-151">Video player module</span></span>](add-video-player.md)
