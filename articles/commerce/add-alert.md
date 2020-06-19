---
title: Veicināšanas reklāmkarogu modulis
description: Šajā tēmā tiek stāstīts par veicināšanas reklāmlogu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: dae824cdbaaf56f85f125c5f36aaa56171bbd6bc
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411369"
---
# <a name="promo-banner-module"></a><span data-ttu-id="85e9b-103">Veicināšanas reklāmkarogu modulis</span><span class="sxs-lookup"><span data-stu-id="85e9b-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="85e9b-104">Šajā tēmā tiek stāstīts par veicināšanas reklāmlogu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="85e9b-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="85e9b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="85e9b-105">Overview</span></span>

<span data-ttu-id="85e9b-106">Veicināšanas reklāmlogu moduļi tiek izmantoti, lai lapā rādītu iekļautos informatīvos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="85e9b-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="85e9b-107">Tos var izmantot, lai visā vietnē rādītu veicināšanas pasākumus, kas tiek rādīti visās e-komercijas vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="85e9b-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="85e9b-108">Veicināšanas reklāmlogu moduļi atbalsta teksta ziņojumu un saiti.</span><span class="sxs-lookup"><span data-stu-id="85e9b-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="85e9b-109">Ja vairāki ziņojumi ir pievienoti veicināšanas reklāmlogu modulim, tas kļūst par rotējošu karuseļa reklāmkarogu, kas ļaus klientiem pārlūkot visus ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="85e9b-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="85e9b-110">Veicināšanas reklāmlogu moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="85e9b-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="85e9b-111">Lietojuma piemēri veicināšanas reklāmlogiem e-Commerce sistēmā</span><span class="sxs-lookup"><span data-stu-id="85e9b-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="85e9b-112">Veicināšanas reklāmlogus var izmantot vietnes galvenē, lai parādītu veicināšanas pasākumus vai ziņojumus visā vietnē, kā tas ir tālāk esošajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="85e9b-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="85e9b-113">“Ikgadējā pārdošana beidzas pēc 10 dienām”</span><span class="sxs-lookup"><span data-stu-id="85e9b-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="85e9b-114">“Labi ietaupiet ar skolas sākuma izpārdošanu.</span><span class="sxs-lookup"><span data-stu-id="85e9b-114">"Save big with back to school sale.</span></span> <span data-ttu-id="85e9b-115">Iepērcieties tūlīt.”</span><span class="sxs-lookup"><span data-stu-id="85e9b-115">Shop Now."</span></span>

<span data-ttu-id="85e9b-116">"Veikals Pateicības dienas IZPĀRDOŠANAi!"</span><span class="sxs-lookup"><span data-stu-id="85e9b-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="85e9b-117">Attēlā zemāk ir parādīts veicināšanas reklāmkaroga piemērs.</span><span class="sxs-lookup"><span data-stu-id="85e9b-117">The following image shows an example of a promo banner.</span></span>

![Veicināšanas reklāmkaroga moduļa piemērs](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="85e9b-119">Veicināšanas reklāmkarogu moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="85e9b-119">Promo banner module properties</span></span>

| <span data-ttu-id="85e9b-120">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="85e9b-120">Property name</span></span>             | <span data-ttu-id="85e9b-121">Vērtība</span><span class="sxs-lookup"><span data-stu-id="85e9b-121">Value</span></span>                              | <span data-ttu-id="85e9b-122">apraksts</span><span class="sxs-lookup"><span data-stu-id="85e9b-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="85e9b-123">Reklāmkaroga ziņojumi</span><span class="sxs-lookup"><span data-stu-id="85e9b-123">Banner messages</span></span>           | <span data-ttu-id="85e9b-124">Teksts un saites</span><span class="sxs-lookup"><span data-stu-id="85e9b-124">Text and links</span></span>                     | <span data-ttu-id="85e9b-125">Teksta un saišu masīvs.</span><span class="sxs-lookup"><span data-stu-id="85e9b-125">An array of text and links.</span></span> |
| <span data-ttu-id="85e9b-126">Automātiskā atskaņošana</span><span class="sxs-lookup"><span data-stu-id="85e9b-126">Autoplay</span></span>                  | <span data-ttu-id="85e9b-127">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="85e9b-127">**True** or **False**</span></span>              | <span data-ttu-id="85e9b-128">Vērtība, kas norāda, vai ziņojumi tiek automātiski iestatīti, ja ir konfigurēti vairāki ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="85e9b-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="85e9b-129"> Slaidu pārejas intervāls</span><span class="sxs-lookup"><span data-stu-id="85e9b-129">Slide transition interval</span></span> | <span data-ttu-id="85e9b-130">Milisekunžu skaits (ms)</span><span class="sxs-lookup"><span data-stu-id="85e9b-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="85e9b-131">Intervāls, ko izmanto, lai pārlūkotu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="85e9b-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="85e9b-132">Atļaut noraidīšanu</span><span class="sxs-lookup"><span data-stu-id="85e9b-132">Allow dismiss</span></span>             | <span data-ttu-id="85e9b-133">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="85e9b-133">**True** or **False**</span></span>              | <span data-ttu-id="85e9b-134">Ja vērtība ir iestatīta uz **Patiess**, debitori var noraidīt brīdinājumu.</span><span class="sxs-lookup"><span data-stu-id="85e9b-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="85e9b-135">Rādīt karuseļveida ziņojumu</span><span class="sxs-lookup"><span data-stu-id="85e9b-135">Show carousel flipper</span></span>     | <span data-ttu-id="85e9b-136">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="85e9b-136">**True** or **False**</span></span>              | <span data-ttu-id="85e9b-137">Vērtība, kas norāda, vai karuseļa paziņojumi ir jārāda, lai klienti varētu manuāli pārvietoties pa vairākiem reklāmkaroga vienumiem.</span><span class="sxs-lookup"><span data-stu-id="85e9b-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="85e9b-138">Teksta līdzinājums</span><span class="sxs-lookup"><span data-stu-id="85e9b-138">Text alignment</span></span>            | <span data-ttu-id="85e9b-139">**Pa labi**, **Pa kreisi** vai **Centrā**</span><span class="sxs-lookup"><span data-stu-id="85e9b-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="85e9b-140">Teksta līdzinājums veicināšanas reklāmkaroga modulī.</span><span class="sxs-lookup"><span data-stu-id="85e9b-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="85e9b-141">Saistīt</span><span class="sxs-lookup"><span data-stu-id="85e9b-141">Link</span></span>                      | <span data-ttu-id="85e9b-142">URL</span><span class="sxs-lookup"><span data-stu-id="85e9b-142">A URL</span></span>                              | <span data-ttu-id="85e9b-143">Vietrādis URL neobligātai vietnei.</span><span class="sxs-lookup"><span data-stu-id="85e9b-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="85e9b-144">Veicināšanas reklāmloga moduļa pievienošana jaunā lapā</span><span class="sxs-lookup"><span data-stu-id="85e9b-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="85e9b-145">Lai pievienotu veicināšanas reklāmloga moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="85e9b-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="85e9b-146">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="85e9b-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="85e9b-147">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Veicināšanas reklāmkaroga veidni** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="85e9b-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="85e9b-148">Sadaļā **Lapas struktūra** pievienojiet moduli **Noklusējuma lapa** slotam **Pamatteksts**.</span><span class="sxs-lookup"><span data-stu-id="85e9b-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="85e9b-149">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="85e9b-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="85e9b-150">Izmantojiet jūsu tikko izveidoto brīdinājuma veidni, lai izveidotu lapu ar nosaukumu **Veicināšanas reklāmloga lapa**.</span><span class="sxs-lookup"><span data-stu-id="85e9b-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="85e9b-151">Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="85e9b-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="85e9b-152">Rūtī pa labi iestatiet vērtību **Platums** sadaļai **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="85e9b-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="85e9b-153">Sadaļā **Lapas struktūra** pievienojiet veicināšanas reklāmkaroga moduli konteinera modulim.</span><span class="sxs-lookup"><span data-stu-id="85e9b-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="85e9b-154">Reklāmkaroga moduļa iestatījumos pievienojiet vienu vai vairākus reklāmkarogu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="85e9b-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="85e9b-155">Katrai ziņai var būt teksts kopā ar saiti.</span><span class="sxs-lookup"><span data-stu-id="85e9b-155">Each message can have text together with a link.</span></span> <span data-ttu-id="85e9b-156">Varat rediģēt pārējos rekvizītus, lai tālāk pielāgotu moduli.</span><span class="sxs-lookup"><span data-stu-id="85e9b-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="85e9b-157">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="85e9b-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="85e9b-158">Lapas augšdaļā ieraudzīsiet brīdinājumu ar jūsu pievienoto tekstu.</span><span class="sxs-lookup"><span data-stu-id="85e9b-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="85e9b-159">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="85e9b-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="85e9b-160">Veicināšanas reklāmlogs parasti tiek izmantots lapas galvenes slotā vai apakšvadītāja slotā.</span><span class="sxs-lookup"><span data-stu-id="85e9b-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="85e9b-161">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="85e9b-161">Additional resources</span></span>

[<span data-ttu-id="85e9b-162">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="85e9b-162">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="85e9b-163">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="85e9b-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="85e9b-164">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="85e9b-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="85e9b-165">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="85e9b-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="85e9b-166">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="85e9b-166">Video player module</span></span>](add-video-player.md)
