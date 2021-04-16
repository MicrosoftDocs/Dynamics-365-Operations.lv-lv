---
title: Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju
description: Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797435"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="85901-103">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="85901-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="85901-104">Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.</span><span class="sxs-lookup"><span data-stu-id="85901-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="85901-105">Tīmekļa analīze ir svarīgs rīks, lai izprastu, kā jūsu klienti mijiedarbojas ar jūsu vietni, un pieņemtu lēmumus, kas palīdzēs optimizēt maksimālo pārveidošanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="85901-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="85901-106">Daudzas tīmekļa analīzes pakotnes ir pieejamas šo mērķu sasniegšanai, piemēram, Google Analytics, Clicker, Moz Analytics un KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="85901-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="85901-107">Lielākajai daļai tīmekļa analīzes pakotņu ir nepieciešams pievienot klienta puses skripta kodu HTML **\<head\>** elementā visām jūsu vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="85901-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="85901-108">Šīs tēmas norādījumi attiecas arī uz citām pielāgotām klienta funkcionalitātēm, kuras Microsoft Dynamics 365 Commerce sākotnēji nepiedāvā.</span><span class="sxs-lookup"><span data-stu-id="85901-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="85901-109">Atkārtoti izmantojama fragmenta izveide jūsu skripta kodam</span><span class="sxs-lookup"><span data-stu-id="85901-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="85901-110">Fragments ļauj atkārtoti izmantot iekļautos vai ārējos skripta kodus visās jūsu vietnes lapās neatkarīgi no veidnes, ko tās izmanto.</span><span class="sxs-lookup"><span data-stu-id="85901-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="85901-111">Atkārtoti izmantojama fragmenta izveide jūsu iekļautā skripta kodam</span><span class="sxs-lookup"><span data-stu-id="85901-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="85901-112">Lai izveidotu atkārtoti izmantojamu fragmentu jūsu iekļautajam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="85901-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85901-113">Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="85901-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="85901-114">Dialoglodziņā **Jauns fragments** atlasiet **Iekļauts skripts**.</span><span class="sxs-lookup"><span data-stu-id="85901-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="85901-115">Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="85901-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="85901-116">Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma iekļautais skripts**.</span><span class="sxs-lookup"><span data-stu-id="85901-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="85901-117">Rekvizītu rūtī labajā pusē zem **iekļautā skripta** ievadiet savu klienta puses skriptu.</span><span class="sxs-lookup"><span data-stu-id="85901-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="85901-118">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="85901-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="85901-119">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="85901-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85901-120">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="85901-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="85901-121">Atkārtoti izmantojama fragmenta izveide jūsu ārējā skripta kodam</span><span class="sxs-lookup"><span data-stu-id="85901-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="85901-122">Lai izveidotu atkārtoti izmantojamu fragmentu jūsu ārējam skripta kodam vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="85901-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85901-123">Dodieties uz **Fragmenti** un tad atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="85901-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="85901-124">Dialoglodziņā **Jauns fragments** atlasiet **Ārējs skripts**.</span><span class="sxs-lookup"><span data-stu-id="85901-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="85901-125">Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="85901-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="85901-126">Jūsu izveidotajā fragmentā atlasiet moduli **Noklusējuma ārējais skripts**.</span><span class="sxs-lookup"><span data-stu-id="85901-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="85901-127">Rekvizītu rūtī labajā pusē zem **skripta avots** pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam.</span><span class="sxs-lookup"><span data-stu-id="85901-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="85901-128">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="85901-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="85901-129">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="85901-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85901-130">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="85901-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="85901-131">Ja jūsu vietnei ir iespējota satura drošības politika (CSP), pārliecinieties, vai visi ārējie vietrāži URL ir pievienoti **script-src** CSP direktīvai Commerce vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="85901-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="85901-132">Papildinformāciju skatiet [Pārvaldīt satura drošības politiku (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="85901-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="85901-133">Pievienot veidnei fragmentu, kas ietver skripta kodu</span><span class="sxs-lookup"><span data-stu-id="85901-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="85901-134">Lai veidnei vietnes veidotājā pievienotu fragmentu, kas ietver skripta kodu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="85901-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85901-135">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="85901-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="85901-136">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="85901-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="85901-137">Slotā **HTML galvene** atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="85901-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="85901-138">Atlasiet fragmentu, ko izveidojāt savam skripta kodam.</span><span class="sxs-lookup"><span data-stu-id="85901-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="85901-139">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="85901-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85901-140">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="85901-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="85901-141">Pievienot ārēju skriptu vai iekļautu skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="85901-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="85901-142">Ja vēlaties ievietot iekļauto vai ārējo skriptu tieši lapu kopā, kas tiek kontrolēta ar vienu veidni, vispirms nav jāizveido fragments.</span><span class="sxs-lookup"><span data-stu-id="85901-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="85901-143">Pievienot iekļautu skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="85901-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="85901-144">Lai pievienotu iekļauto skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="85901-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85901-145">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="85901-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="85901-146">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="85901-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="85901-147">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="85901-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="85901-148">Dialoglodziņā **Pievienot moduli** atlasiet **Iekļauts skripts**.</span><span class="sxs-lookup"><span data-stu-id="85901-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="85901-149">Rekvizītu rūtī labajā pusē zem **iekļautā skripta** ievadiet savu klienta puses skriptu.</span><span class="sxs-lookup"><span data-stu-id="85901-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="85901-150">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="85901-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="85901-151">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="85901-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85901-152">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="85901-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="85901-153">Pievienot ārēju skriptu tieši veidnei</span><span class="sxs-lookup"><span data-stu-id="85901-153">Add an external script directly to a template</span></span>

<span data-ttu-id="85901-154">Lai pievienotu ārējo skriptu tieši veidnes vietnes veidotājā, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="85901-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85901-155">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="85901-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="85901-156">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="85901-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="85901-157">**HTML galvenajā** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="85901-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="85901-158">Dialoglodziņā **Pievienot moduli** atlasiet **Ārējs skripts**.</span><span class="sxs-lookup"><span data-stu-id="85901-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="85901-159">Rekvizītu rūtī labajā pusē zem **skripta avots** pievienojiet ārēju vai relatīvu vietrādi URL ārējam skripta avotam.</span><span class="sxs-lookup"><span data-stu-id="85901-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="85901-160">Pēc tam un pēc nepieciešamības konfigurējiet citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="85901-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="85901-161">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="85901-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85901-162">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="85901-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85901-163">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="85901-163">Additional resources</span></span>

[<span data-ttu-id="85901-164">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="85901-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="85901-165">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="85901-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="85901-166">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="85901-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="85901-167">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="85901-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="85901-168">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="85901-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="85901-169">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="85901-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="85901-170">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="85901-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
