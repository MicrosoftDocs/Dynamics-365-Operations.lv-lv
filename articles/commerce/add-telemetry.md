---
title: Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju
description: Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761253"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="e77e5-103">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="e77e5-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e77e5-104">Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="e77e5-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="e77e5-105">Overview</span></span>

<span data-ttu-id="e77e5-106">Tīmekļa analīze ir svarīgs rīks, lai izprastu, kā jūsu klienti mijiedarbojas ar jūsu vietni, un pieņemtu lēmumus, kas palīdzēs optimizēt maksimālo pārveidošanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="e77e5-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="e77e5-107">Daudzas tīmekļa analīzes pakotnes ir pieejamas šo mērķu sasniegšanai, piemēram, Google Analytics, Clicker, Moz Analytics un KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="e77e5-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="e77e5-108">Lielākajai daļai tīmekļa analīzes pakotņu ir nepieciešams pievienot klienta puses skripta kodu HTML **\<head\>** elementā visām jūsu vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="e77e5-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="e77e5-109">Šajā tēmā instrukcijas attiecas arī uz citu pielāgotu klienta puses funkcionalitāti, ko programma Microsoft Dynamics 365 Commerce vispārēji nepiedāvā.</span><span class="sxs-lookup"><span data-stu-id="e77e5-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="e77e5-110">Atkārtoti izmantojama fragmenta izveide jūsu skripta kodam</span><span class="sxs-lookup"><span data-stu-id="e77e5-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="e77e5-111">Fragments ļauj atkārtoti izmantot iekļautos vai ārējos skripta kodus visās jūsu vietnes lapās neatkarīgi no veidnes, ko tās izmanto.</span><span class="sxs-lookup"><span data-stu-id="e77e5-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="e77e5-112">Atkārtoti izmantojama fragmenta izveide jūsu iekļautā skripta kodam</span><span class="sxs-lookup"><span data-stu-id="e77e5-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="e77e5-113">Lai izveidotu atkārtoti izmantojamu fragmentu jūsu iekļautajam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e77e5-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e77e5-114">Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="e77e5-115">Dialoglodziņā **Jauns fragments** atlasiet **Iekļauts skripts**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="e77e5-116">Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e77e5-117">Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma iekļautais skripts**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="e77e5-118">Rekvizītu rūtī labajā pusē zem **iekļautā skripta**ievadiet savu klienta puses skriptu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="e77e5-119">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="e77e5-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e77e5-120">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e77e5-121">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="e77e5-122">Atkārtoti izmantojama fragmenta izveide jūsu ārējā skripta kodam</span><span class="sxs-lookup"><span data-stu-id="e77e5-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="e77e5-123">Lai izveidotu atkārtoti izmantojamu fragmentu jūsu ārējam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e77e5-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e77e5-124">Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="e77e5-125">Dialoglodziņā **Jauns fragments** atlasiet **Ārējs skripts**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="e77e5-126">Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e77e5-127">Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma ārējais skripts**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="e77e5-128">Rekvizītu rūtī labajā pusē zem **skripta avots**pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam.</span><span class="sxs-lookup"><span data-stu-id="e77e5-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="e77e5-129">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="e77e5-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e77e5-130">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e77e5-131">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-131">Select **Publish**.</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="e77e5-132">Pievienot veidnei fragmentu, kas ietver skripta kodu</span><span class="sxs-lookup"><span data-stu-id="e77e5-132">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="e77e5-133">Lai veidnei vietnes veidotājā pievienotu fragmentu, kas ietver skripta kodu, izpildiet tālāk noradītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e77e5-133">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e77e5-134">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e77e5-135">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e77e5-136">Slotā **HTML galvene** atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="e77e5-137">Atlasiet fragmentu, ko izveidojāt savam skripta kodam.</span><span class="sxs-lookup"><span data-stu-id="e77e5-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="e77e5-138">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e77e5-139">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="e77e5-140">Pievienot ārēju skriptu vai iekļautu skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="e77e5-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="e77e5-141">Ja vēlaties ievietot iekļauto vai ārējo skriptu tieši lapu kopā, kas tiek kontrolēta ar vienu veidni, vispirms nav jāizveido fragments.</span><span class="sxs-lookup"><span data-stu-id="e77e5-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="e77e5-142">Pievienot iekļautu skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="e77e5-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="e77e5-143">Lai pievienotu iekļauto skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e77e5-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e77e5-144">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e77e5-145">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e77e5-146">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e77e5-147">Dialoglodziņā **Pievienot moduli** atlasiet **Iekļauts skripts**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="e77e5-148">Rekvizītu rūtī labajā pusē zem **iekļautā skripta**ievadiet savu klienta puses skriptu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="e77e5-149">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="e77e5-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e77e5-150">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e77e5-151">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="e77e5-152">Pievienot ārēju skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="e77e5-152">Add an external script directly to a template</span></span>

<span data-ttu-id="e77e5-153">Lai pievienotu ārējo skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e77e5-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e77e5-154">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e77e5-155">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="e77e5-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e77e5-156">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e77e5-157">Dialoglodziņā **Pievienot moduli** atlasiet **Ārējs skripts**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="e77e5-158">Rekvizītu rūtī labajā pusē zem **skripta avots**pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam.</span><span class="sxs-lookup"><span data-stu-id="e77e5-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="e77e5-159">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="e77e5-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e77e5-160">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e77e5-161">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="e77e5-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e77e5-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e77e5-162">Additional resources</span></span>

[<span data-ttu-id="e77e5-163">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="e77e5-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e77e5-164">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="e77e5-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="e77e5-165">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="e77e5-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="e77e5-166">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="e77e5-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e77e5-167">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="e77e5-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e77e5-168">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="e77e5-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e77e5-169">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="e77e5-169">Add languages to your site</span></span>](add-languages-to-site.md)
