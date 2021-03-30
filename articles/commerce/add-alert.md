---
title: Veicināšanas reklāmkarogu modulis
description: Šajā tēmā aplūkoti Promo banner moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206587"
---
# <a name="promo-banner-module"></a><span data-ttu-id="86f82-103">Akcijas reklāmkaroga modulis</span><span class="sxs-lookup"><span data-stu-id="86f82-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86f82-104">Šajā tēmā aplūkoti Promo banner moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86f82-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="86f82-105">Veicināšanas reklāmlogu moduļi tiek izmantoti, lai lapā rādītu iekļautos informatīvos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="86f82-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="86f82-106">Tos var izmantot, lai visā vietnē rādītu veicināšanas pasākumus, kas tiek rādīti visās e-komercijas vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="86f82-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="86f82-107">Veicināšanas reklāmlogu moduļi atbalsta teksta ziņojumu un saiti.</span><span class="sxs-lookup"><span data-stu-id="86f82-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="86f82-108">Ja vairāki ziņojumi ir pievienoti veicināšanas reklāmlogu modulim, tas kļūst par rotējošu karuseļa reklāmkarogu, kas ļaus klientiem pārlūkot visus ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="86f82-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="86f82-109">Veicināšanas reklāmlogu moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="86f82-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="86f82-110">Lietojuma piemēri veicināšanas reklāmlogiem e-Commerce sistēmā</span><span class="sxs-lookup"><span data-stu-id="86f82-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="86f82-111">Veicināšanas reklāmlogus var izmantot vietnes galvenē, lai parādītu veicināšanas pasākumus vai ziņojumus visā vietnē, kā tas ir tālāk esošajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="86f82-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="86f82-112">“Ikgadējā pārdošana beidzas pēc 10 dienām”</span><span class="sxs-lookup"><span data-stu-id="86f82-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="86f82-113">“Labi ietaupiet ar skolas sākuma izpārdošanu.</span><span class="sxs-lookup"><span data-stu-id="86f82-113">"Save big with back to school sale.</span></span> <span data-ttu-id="86f82-114">Iepērcieties tūlīt.”</span><span class="sxs-lookup"><span data-stu-id="86f82-114">Shop Now."</span></span>

<span data-ttu-id="86f82-115">"Veikals Pateicības dienas IZPĀRDOŠANAi!"</span><span class="sxs-lookup"><span data-stu-id="86f82-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="86f82-116">Attēlā zemāk ir parādīts veicināšanas reklāmkaroga piemērs.</span><span class="sxs-lookup"><span data-stu-id="86f82-116">The following image shows an example of a promo banner.</span></span>

![Veicināšanas reklāmkaroga moduļa piemērs](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="86f82-118">Veicināšanas reklāmkarogu moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="86f82-118">Promo banner module properties</span></span>

| <span data-ttu-id="86f82-119">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="86f82-119">Property name</span></span>             | <span data-ttu-id="86f82-120">Vērtība</span><span class="sxs-lookup"><span data-stu-id="86f82-120">Value</span></span>                              | <span data-ttu-id="86f82-121">apraksts</span><span class="sxs-lookup"><span data-stu-id="86f82-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="86f82-122">Reklāmkaroga ziņojumi</span><span class="sxs-lookup"><span data-stu-id="86f82-122">Banner messages</span></span>           | <span data-ttu-id="86f82-123">Teksts un saites</span><span class="sxs-lookup"><span data-stu-id="86f82-123">Text and links</span></span>                     | <span data-ttu-id="86f82-124">Teksta un saišu masīvs.</span><span class="sxs-lookup"><span data-stu-id="86f82-124">An array of text and links.</span></span> |
| <span data-ttu-id="86f82-125">Automātiskā atskaņošana</span><span class="sxs-lookup"><span data-stu-id="86f82-125">Autoplay</span></span>                  | <span data-ttu-id="86f82-126">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="86f82-126">**True** or **False**</span></span>              | <span data-ttu-id="86f82-127">Vērtība, kas norāda, vai ziņojumi tiek automātiski iestatīti, ja ir konfigurēti vairāki ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="86f82-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="86f82-128">Slaidu pārejas intervāls</span><span class="sxs-lookup"><span data-stu-id="86f82-128">Slide transition interval</span></span> | <span data-ttu-id="86f82-129">Milisekunžu skaits (ms)</span><span class="sxs-lookup"><span data-stu-id="86f82-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="86f82-130">Intervāls, ko izmanto, lai pārlūkotu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="86f82-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="86f82-131">Atļaut noraidīšanu</span><span class="sxs-lookup"><span data-stu-id="86f82-131">Allow dismiss</span></span>             | <span data-ttu-id="86f82-132">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="86f82-132">**True** or **False**</span></span>              | <span data-ttu-id="86f82-133">Ja vērtība ir iestatīta uz **Patiess**, debitori var noraidīt brīdinājumu.</span><span class="sxs-lookup"><span data-stu-id="86f82-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="86f82-134">Rādīt karuseļveida ziņojumu</span><span class="sxs-lookup"><span data-stu-id="86f82-134">Show carousel flipper</span></span>     | <span data-ttu-id="86f82-135">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="86f82-135">**True** or **False**</span></span>              | <span data-ttu-id="86f82-136">Vērtība, kas norāda, vai karuseļa paziņojumi ir jārāda, lai klienti varētu manuāli pārvietoties pa vairākiem reklāmkaroga vienumiem.</span><span class="sxs-lookup"><span data-stu-id="86f82-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="86f82-137">Teksta līdzinājums</span><span class="sxs-lookup"><span data-stu-id="86f82-137">Text alignment</span></span>            | <span data-ttu-id="86f82-138">**Pa labi**, **Pa kreisi** vai **Centrā**</span><span class="sxs-lookup"><span data-stu-id="86f82-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="86f82-139">Teksta līdzinājums veicināšanas reklāmkaroga modulī.</span><span class="sxs-lookup"><span data-stu-id="86f82-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="86f82-140">Saistīt</span><span class="sxs-lookup"><span data-stu-id="86f82-140">Link</span></span>                      | <span data-ttu-id="86f82-141">URL</span><span class="sxs-lookup"><span data-stu-id="86f82-141">A URL</span></span>                              | <span data-ttu-id="86f82-142">Vietrādis URL neobligātai vietnei.</span><span class="sxs-lookup"><span data-stu-id="86f82-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="86f82-143">Veicināšanas reklāmloga moduļa pievienošana jaunā lapā</span><span class="sxs-lookup"><span data-stu-id="86f82-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="86f82-144">Lai pievienotu veicināšanas reklāmloga moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="86f82-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="86f82-145">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="86f82-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="86f82-146">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Veicināšanas reklāmkaroga veidni** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="86f82-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="86f82-147">Sadaļā **Lapas struktūra** pievienojiet moduli **Noklusējuma lapa** slotam **Pamatteksts**.</span><span class="sxs-lookup"><span data-stu-id="86f82-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="86f82-148">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="86f82-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="86f82-149">Izmantojiet jūsu tikko izveidoto brīdinājuma veidni, lai izveidotu lapu ar nosaukumu **Veicināšanas reklāmloga lapa**.</span><span class="sxs-lookup"><span data-stu-id="86f82-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="86f82-150">Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="86f82-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="86f82-151">Rūtī pa labi iestatiet vērtību **Platums** sadaļai **Aizpildīt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="86f82-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="86f82-152">Sadaļā **Lapas struktūra** pievienojiet veicināšanas reklāmkaroga moduli konteinera modulim.</span><span class="sxs-lookup"><span data-stu-id="86f82-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="86f82-153">Reklāmkaroga moduļa iestatījumos pievienojiet vienu vai vairākus reklāmkarogu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="86f82-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="86f82-154">Katrai ziņai var būt teksts kopā ar saiti.</span><span class="sxs-lookup"><span data-stu-id="86f82-154">Each message can have text together with a link.</span></span> <span data-ttu-id="86f82-155">Varat rediģēt pārējos rekvizītus, lai tālāk pielāgotu moduli.</span><span class="sxs-lookup"><span data-stu-id="86f82-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="86f82-156">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="86f82-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="86f82-157">Lapas augšdaļā ieraudzīsiet brīdinājumu ar jūsu pievienoto tekstu.</span><span class="sxs-lookup"><span data-stu-id="86f82-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="86f82-158">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="86f82-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="86f82-159">Veicināšanas reklāmlogs parasti tiek izmantots lapas galvenes slotā vai apakšvadītāja slotā.</span><span class="sxs-lookup"><span data-stu-id="86f82-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="86f82-160">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="86f82-160">Additional resources</span></span>

[<span data-ttu-id="86f82-161">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="86f82-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="86f82-162">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="86f82-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="86f82-163">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="86f82-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="86f82-164">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="86f82-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="86f82-165">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="86f82-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]