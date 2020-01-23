---
title: Logotipa pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot logotipu savai vietnei programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914627"
---
# <a name="add-a-logo"></a><span data-ttu-id="bb118-103">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="bb118-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bb118-104">Šajā tēmā ir aprakstīts, kā pievienot logotipu savai vietnei programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb118-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bb118-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="bb118-105">Overview</span></span>

<span data-ttu-id="bb118-106">Veidojot vietni, viena no pirmajām lietām, ko jūs, iespējams, darīsiet, ir vietnes galvenē pievienosiet sava uzņēmuma vai zīmola logotipu.</span><span class="sxs-lookup"><span data-stu-id="bb118-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="bb118-107">Dynamics 365 Commerce tiešsaistes sākuma komplekts nodrošina moduli, kas padara šo uzdevumu vieglu.</span><span class="sxs-lookup"><span data-stu-id="bb118-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="bb118-108">Logotipu var pievienot tieši veidnei, izkārtojumam vai lapai.</span><span class="sxs-lookup"><span data-stu-id="bb118-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="bb118-109">Tādā veidā jūs varat viegli nomainīt logotipu, kas parādās konkrētās lapās vai lapu grupās.</span><span class="sxs-lookup"><span data-stu-id="bb118-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="bb118-110">Tomēr šī tēma attiecas uz visbiežāk sastopamo scenāriju, kur jūs pievienojat savu logotipu galvenes fragmentam, ko var atkārtoti izmantot visās vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="bb118-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bb118-111">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="bb118-111">Prerequisites</span></span>

<span data-ttu-id="bb118-112">Lai varētu pievienot logotipu visām vietnes lapām, jums ir jāizpilda tālāk aprakstītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="bb118-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="bb118-113">Augšupielādējiet savu logotipu digitālo līdzekļu pārvaldniekā, kuram varat piekļūt no lapas **Līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="bb118-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="bb118-114">izveidojiet galvenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="bb118-114">Create a header fragment.</span></span> <span data-ttu-id="bb118-115">Vairāk informācijas par fragmentu izveidi un izmantošanu skatiet sadaļā [Darbs ar fragmentiem](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="bb118-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="bb118-116">Iekļaujiet veidnē galvenes fragmentu, kuru jūsu vietnes lapas izmanto izkārtojumu un moduļu opcijām.</span><span class="sxs-lookup"><span data-stu-id="bb118-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="bb118-117">Vairāk informācijas par veidnēm skatiet sadaļā [Darbs ar veidnēm](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="bb118-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="bb118-118">Logotipa pievienošana galvenes fragmentam</span><span class="sxs-lookup"><span data-stu-id="bb118-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="bb118-119">Lai pievienotu logotipu vietnes galvenes fragmentam, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="bb118-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="bb118-120">Kreisajā navigācijas rūtī atlasiet **Fragmenti** un pēc tam atlasiet izveidoto galvenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="bb118-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="bb118-121">Atlasiet **Paņemt**.</span><span class="sxs-lookup"><span data-stu-id="bb118-121">Select **Check out**.</span></span>
3. <span data-ttu-id="bb118-122">Izvērsiet slotu **Galvene** un slotu **Logotips**.</span><span class="sxs-lookup"><span data-stu-id="bb118-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="bb118-123">Atlasiet daudzpunktes pogu (**...**) slotam **Logotips** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="bb118-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="bb118-124">Atlasiet logotipa moduli.</span><span class="sxs-lookup"><span data-stu-id="bb118-124">Select the logo module.</span></span>
6. <span data-ttu-id="bb118-125">Rekvizītu rūtī labajā pusē konfigurējiet logotipa moduli tā, lai tajā būtu redzams jūsu logotips.</span><span class="sxs-lookup"><span data-stu-id="bb118-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="bb118-126">Saglabājiet galvenes fragmentu, pārbaudiet un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="bb118-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="bb118-127">Pēc atjauninātā galvenes fragmenta publicēšanas visās vietņu lapās, kurās tiek izmantota veidne, kurā ir galvenes fragments, tiks parādīts jūsu logotips.</span><span class="sxs-lookup"><span data-stu-id="bb118-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb118-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bb118-128">Additional resources</span></span>

[<span data-ttu-id="bb118-129">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="bb118-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="bb118-130">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="bb118-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="bb118-131">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="bb118-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="bb118-132">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="bb118-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="bb118-133">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="bb118-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="bb118-134">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="bb118-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="bb118-135">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="bb118-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

