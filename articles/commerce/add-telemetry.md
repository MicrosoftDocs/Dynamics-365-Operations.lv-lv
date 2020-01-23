---
title: Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju
description: Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914543"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="2f0a4-103">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="2f0a4-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2f0a4-104">Šajā tēmā ir aprakstīts, kā pievienot klienta puses skripta kodu jūsu vietnes lapām, lai atbalstītu klienta puses telemetrijas vākšanu.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="2f0a4-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="2f0a4-105">Overview</span></span>

<span data-ttu-id="2f0a4-106">Tīmekļa analīze ir svarīgs rīks, lai izprastu, kā jūsu klienti mijiedarbojas ar jūsu vietni, un pieņemtu lēmumus, kas palīdzēs optimizēt maksimālo pārveidošanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="2f0a4-107">Daudzas tīmekļa analīzes pakotnes ir pieejamas šo mērķu sasniegšanai, piemēram, Google Analytics, Clicker, Moz Analytics un KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="2f0a4-108">Lielākajai daļai tīmekļa analīzes pakotņu ir nepieciešams pievienot klienta puses skripta kodu HTML **\<galvenajā\>** elementā visām jūsu vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="2f0a4-109">Šajā tēmā instrukcijas attiecas arī uz citu pielāgotu klienta puses funkcionalitāti, ko programma Microsoft Dynamics 365 Commerce vispārēji nepiedāvā.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="2f0a4-110">Atkārtoti izmantojama fragmenta izveide jūsu skripta kodam</span><span class="sxs-lookup"><span data-stu-id="2f0a4-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="2f0a4-111">Pēc tam, kad esat izveidojis fragmentu savam skripta kodam, to var atkārtoti izmantot visās vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="2f0a4-112">Dodieties uz **Fragmenti \>Jaunas lapas fragments**.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="2f0a4-113">Atlasiet **Ārējais skripts**, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="2f0a4-114">Fragmentu hierarhijā atlasiet **skripta ievadītājs**, kas ir jūsu tikko izveidotā fragmenta moduļa apakšelements.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="2f0a4-115">Labajā pusē rekvizītu rūtī pievienojiet jūsu klienta puses skriptu un iestatiet citas konfigurācijas opcijas pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="2f0a4-116">Fragmenta pievienošana veidnēm</span><span class="sxs-lookup"><span data-stu-id="2f0a4-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="2f0a4-117">Dodieties uz **Veidnes** un atveriet veidni lapām, kurām vēlaties pievienot skripta kodu.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="2f0a4-118">Kreisajā rūtī izvērsiet veidnes hierarhiju, lai parādītu **HTML galveno** slotu.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="2f0a4-119">Atlasiet daudzpunktes pogu (**...**) **HTML galvenajam** slotam un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="2f0a4-120">Atlasiet fragmentu, ko izveidojāt savam skripta kodam.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="2f0a4-121">Saglabājiet veidni un pārbaudiet to.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="2f0a4-122">Pēc pabeigšanas jums ir jāpublicē fragments un pamata veidne.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="2f0a4-123">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2f0a4-123">Additional resources</span></span>

[<span data-ttu-id="2f0a4-124">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="2f0a4-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2f0a4-125">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="2f0a4-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2f0a4-126">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="2f0a4-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2f0a4-127">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="2f0a4-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2f0a4-128">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="2f0a4-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="2f0a4-129">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="2f0a4-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2f0a4-130">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="2f0a4-130">Add languages to your site</span></span>](add-languages-to-site.md)

