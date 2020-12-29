---
title: Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju
description: Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413993"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="56f73-103">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="56f73-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="56f73-104">Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.</span><span class="sxs-lookup"><span data-stu-id="56f73-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="56f73-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="56f73-105">Overview</span></span>

<span data-ttu-id="56f73-106">Tīmekļa analīze ir svarīgs rīks, lai izprastu, kā jūsu klienti mijiedarbojas ar jūsu vietni, un pieņemtu lēmumus, kas palīdzēs optimizēt maksimālo pārveidošanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="56f73-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="56f73-107">Daudzas tīmekļa analīzes pakotnes ir pieejamas šo mērķu sasniegšanai, piemēram, Google Analytics, Clicker, Moz Analytics un KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="56f73-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="56f73-108">Lielākajai daļai tīmekļa analīzes pakotņu ir nepieciešams pievienot klienta puses skripta kodu HTML **\<head\>** elementā visām jūsu vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="56f73-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="56f73-109">Šajā tēmā instrukcijas attiecas arī uz citu pielāgotu klienta puses funkcionalitāti, ko programma Microsoft Dynamics 365 Commerce vispārēji nepiedāvā.</span><span class="sxs-lookup"><span data-stu-id="56f73-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="56f73-110">Atkārtoti izmantojama fragmenta izveide jūsu skripta kodam</span><span class="sxs-lookup"><span data-stu-id="56f73-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="56f73-111">Fragments ļauj atkārtoti izmantot iekļautos vai ārējos skripta kodus visās jūsu vietnes lapās neatkarīgi no veidnes, ko tās izmanto.</span><span class="sxs-lookup"><span data-stu-id="56f73-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="56f73-112">Atkārtoti izmantojama fragmenta izveide jūsu iekļautā skripta kodam</span><span class="sxs-lookup"><span data-stu-id="56f73-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="56f73-113">Lai izveidotu atkārtoti izmantojamu fragmentu jūsu iekļautajam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="56f73-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="56f73-114">Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="56f73-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="56f73-115">Dialoglodziņā **Jauns fragments** atlasiet **Iekļauts skripts**.</span><span class="sxs-lookup"><span data-stu-id="56f73-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="56f73-116">Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="56f73-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="56f73-117">Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma iekļautais skripts**.</span><span class="sxs-lookup"><span data-stu-id="56f73-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="56f73-118">Rekvizītu rūtī labajā pusē zem **iekļautā skripta** ievadiet savu klienta puses skriptu.</span><span class="sxs-lookup"><span data-stu-id="56f73-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="56f73-119">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="56f73-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="56f73-120">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="56f73-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="56f73-121">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="56f73-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="56f73-122">Atkārtoti izmantojama fragmenta izveide jūsu ārējā skripta kodam</span><span class="sxs-lookup"><span data-stu-id="56f73-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="56f73-123">Lai izveidotu atkārtoti izmantojamu fragmentu jūsu ārējam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="56f73-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="56f73-124">Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="56f73-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="56f73-125">Dialoglodziņā **Jauns fragments** atlasiet **Ārējs skripts**.</span><span class="sxs-lookup"><span data-stu-id="56f73-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="56f73-126">Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="56f73-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="56f73-127">Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma ārējais skripts**.</span><span class="sxs-lookup"><span data-stu-id="56f73-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="56f73-128">Rekvizītu rūtī labajā pusē zem **skripta avots** pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam.</span><span class="sxs-lookup"><span data-stu-id="56f73-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="56f73-129">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="56f73-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="56f73-130">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="56f73-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="56f73-131">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="56f73-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="56f73-132">Ja jūsu vietnei ir iespējota satura drošības politika (CSP), pārliecinieties, vai visi ārējie vietrāži URL ir pievienoti **script-src** CSP direktīvai Commerce vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="56f73-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="56f73-133">Papildinformāciju skatiet [Pārvaldīt satura drošības politiku (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="56f73-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="56f73-134">Pievienot veidnei fragmentu, kas ietver skripta kodu</span><span class="sxs-lookup"><span data-stu-id="56f73-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="56f73-135">Lai veidnei vietnes veidotājā pievienotu fragmentu, kas ietver skripta kodu, izpildiet tālāk noradītās darbības.</span><span class="sxs-lookup"><span data-stu-id="56f73-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="56f73-136">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="56f73-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="56f73-137">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="56f73-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="56f73-138">Slotā **HTML galvene** atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="56f73-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="56f73-139">Atlasiet fragmentu, ko izveidojāt savam skripta kodam.</span><span class="sxs-lookup"><span data-stu-id="56f73-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="56f73-140">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="56f73-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="56f73-141">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="56f73-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="56f73-142">Pievienot ārēju skriptu vai iekļautu skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="56f73-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="56f73-143">Ja vēlaties ievietot iekļauto vai ārējo skriptu tieši lapu kopā, kas tiek kontrolēta ar vienu veidni, vispirms nav jāizveido fragments.</span><span class="sxs-lookup"><span data-stu-id="56f73-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="56f73-144">Pievienot iekļautu skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="56f73-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="56f73-145">Lai pievienotu iekļauto skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="56f73-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="56f73-146">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="56f73-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="56f73-147">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="56f73-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="56f73-148">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="56f73-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="56f73-149">Dialoglodziņā **Pievienot moduli** atlasiet **Iekļauts skripts**.</span><span class="sxs-lookup"><span data-stu-id="56f73-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="56f73-150">Rekvizītu rūtī labajā pusē zem **iekļautā skripta** ievadiet savu klienta puses skriptu.</span><span class="sxs-lookup"><span data-stu-id="56f73-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="56f73-151">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="56f73-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="56f73-152">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="56f73-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="56f73-153">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="56f73-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="56f73-154">Pievienot ārēju skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="56f73-154">Add an external script directly to a template</span></span>

<span data-ttu-id="56f73-155">Lai pievienotu ārējo skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="56f73-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="56f73-156">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="56f73-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="56f73-157">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="56f73-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="56f73-158">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="56f73-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="56f73-159">Dialoglodziņā **Pievienot moduli** atlasiet **Ārējs skripts**.</span><span class="sxs-lookup"><span data-stu-id="56f73-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="56f73-160">Rekvizītu rūtī labajā pusē zem **skripta avots** pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam.</span><span class="sxs-lookup"><span data-stu-id="56f73-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="56f73-161">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="56f73-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="56f73-162">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="56f73-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="56f73-163">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="56f73-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56f73-164">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="56f73-164">Additional resources</span></span>

[<span data-ttu-id="56f73-165">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="56f73-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="56f73-166">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="56f73-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="56f73-167">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="56f73-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="56f73-168">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="56f73-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="56f73-169">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="56f73-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="56f73-170">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="56f73-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="56f73-171">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="56f73-171">Add languages to your site</span></span>](add-languages-to-site.md)
