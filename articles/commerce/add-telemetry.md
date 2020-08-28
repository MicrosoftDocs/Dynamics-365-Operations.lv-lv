---
title: Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju
description: Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686818"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="95963-103">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="95963-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95963-104">Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.</span><span class="sxs-lookup"><span data-stu-id="95963-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="95963-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="95963-105">Overview</span></span>

<span data-ttu-id="95963-106">Tīmekļa analīze ir svarīgs rīks, lai izprastu, kā jūsu klienti mijiedarbojas ar jūsu vietni, un pieņemtu lēmumus, kas palīdzēs optimizēt maksimālo pārveidošanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="95963-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="95963-107">Daudzas tīmekļa analīzes pakotnes ir pieejamas šo mērķu sasniegšanai, piemēram, Google Analytics, Clicker, Moz Analytics un KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="95963-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="95963-108">Lielākajai daļai tīmekļa analīzes pakotņu ir nepieciešams pievienot klienta puses skripta kodu HTML **\<head\>** elementā visām jūsu vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="95963-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="95963-109">Šajā tēmā instrukcijas attiecas arī uz citu pielāgotu klienta puses funkcionalitāti, ko programma Microsoft Dynamics 365 Commerce vispārēji nepiedāvā.</span><span class="sxs-lookup"><span data-stu-id="95963-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="95963-110">Atkārtoti izmantojama lapas fragmenta izveide jūsu skripta kodam</span><span class="sxs-lookup"><span data-stu-id="95963-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="95963-111">Lapas fragments ļauj atkārtoti izmantot iekļautos vai ārējos skripta kodus visās jūsu vietnes lapās neatkarīgi no veidnes, ko tās izmanto.</span><span class="sxs-lookup"><span data-stu-id="95963-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="95963-112">Atkārtoti izmantojama lapas fragmenta izveide jūsu iekļautā skripta kodam</span><span class="sxs-lookup"><span data-stu-id="95963-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="95963-113">Lai izveidotu atkārtoti izmantojamu lapas fragmentu jūsu iekļautajam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="95963-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="95963-114">Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="95963-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="95963-115">Dialoglodziņā **Jauns lapas fragments** atlasiet **Iekļauts skripts**.</span><span class="sxs-lookup"><span data-stu-id="95963-115">In the **New page fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="95963-116">Sadaļā **Lapas fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="95963-116">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="95963-117">Jūsu izveidotajā lapas fragmentā atlasiet moduli **Noklusējuma iekļautais skripts**.</span><span class="sxs-lookup"><span data-stu-id="95963-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="95963-118">Rekvizītu rūtī labajā pusē zem **iekļautā skripta**ievadiet savu klienta puses skriptu.</span><span class="sxs-lookup"><span data-stu-id="95963-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="95963-119">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="95963-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="95963-120">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="95963-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="95963-121">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="95963-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="95963-122">Atkārtoti izmantojama lapas fragmenta izveide jūsu ārējā skripta kodam</span><span class="sxs-lookup"><span data-stu-id="95963-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="95963-123">Lai izveidotu atkārtoti izmantojamu lapas fragmentu jūsu ārējam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="95963-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="95963-124">Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="95963-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="95963-125">Dialoglodziņā **Jauns lapas fragments** atlasiet **Ārējs skripts**.</span><span class="sxs-lookup"><span data-stu-id="95963-125">In the **New page fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="95963-126">Sadaļā **Lapas fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="95963-126">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="95963-127">Jūsu izveidotajā lapas fragmentā atlasiet moduli **Noklusējuma ārējais skripts**.</span><span class="sxs-lookup"><span data-stu-id="95963-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="95963-128">Rekvizītu rūtī labajā pusē zem **skripta avots**pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam.</span><span class="sxs-lookup"><span data-stu-id="95963-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="95963-129">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="95963-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="95963-130">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="95963-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="95963-131">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="95963-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="95963-132">Pievienot veidnei lapas fragmentu, kas ietver skripta kodu</span><span class="sxs-lookup"><span data-stu-id="95963-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="95963-133">Lai veidnei vietnes veidotājā pievienotu lapas fragmentu, kas ietver skripta kodu, izpildiet tālāk noradītās darbības.</span><span class="sxs-lookup"><span data-stu-id="95963-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="95963-134">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="95963-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="95963-135">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="95963-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="95963-136">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot lapas fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="95963-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="95963-137">Atlasiet fragmentu, ko izveidojāt savam skripta kodam.</span><span class="sxs-lookup"><span data-stu-id="95963-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="95963-138">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="95963-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="95963-139">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="95963-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="95963-140">Pievienot ārēju skriptu vai iekļautu skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="95963-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="95963-141">Ja vēlaties ievietot iekļauto vai ārējo skriptu tieši lapu kopā, kas tiek kontrolēta ar vienu veidni, vispirms nav jāizveido lapas fragments.</span><span class="sxs-lookup"><span data-stu-id="95963-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="95963-142">Pievienot iekļautu skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="95963-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="95963-143">Lai pievienotu iekļauto skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="95963-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="95963-144">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="95963-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="95963-145">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="95963-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="95963-146">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="95963-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="95963-147">Dialoglodziņā **Pievienot moduli** atlasiet **Iekļauts skripts**.</span><span class="sxs-lookup"><span data-stu-id="95963-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="95963-148">Rekvizītu rūtī labajā pusē zem **iekļautā skripta**ievadiet savu klienta puses skriptu.</span><span class="sxs-lookup"><span data-stu-id="95963-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="95963-149">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="95963-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="95963-150">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="95963-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="95963-151">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="95963-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="95963-152">Pievienot ārēju skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="95963-152">Add an external script directly to a template</span></span>

<span data-ttu-id="95963-153">Lai pievienotu ārējo skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="95963-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="95963-154">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="95963-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="95963-155">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="95963-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="95963-156">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="95963-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="95963-157">Dialoglodziņā **Pievienot moduli** atlasiet **Ārējs skripts**.</span><span class="sxs-lookup"><span data-stu-id="95963-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="95963-158">Rekvizītu rūtī labajā pusē zem **skripta avots**pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam.</span><span class="sxs-lookup"><span data-stu-id="95963-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="95963-159">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="95963-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="95963-160">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="95963-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="95963-161">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="95963-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95963-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="95963-162">Additional resources</span></span>

[<span data-ttu-id="95963-163">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="95963-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="95963-164">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="95963-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="95963-165">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="95963-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="95963-166">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="95963-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="95963-167">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="95963-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="95963-168">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="95963-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="95963-169">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="95963-169">Add languages to your site</span></span>](add-languages-to-site.md)
