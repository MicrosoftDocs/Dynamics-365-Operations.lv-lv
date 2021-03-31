---
title: Logotipa pievienošana
description: Šajā tēmā aprakstīts, kā pievienot logotipu vietnei risinājumā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 143c1ab33547119ceab0a4fba165669bc8b22bf4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207583"
---
# <a name="add-a-logo"></a><span data-ttu-id="adc62-103">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="adc62-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="adc62-104">Šajā tēmā aprakstīts, kā pievienot logotipu vietnei risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="adc62-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="adc62-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="adc62-105">Overview</span></span>

<span data-ttu-id="adc62-106">Veidojot vietni, viena no pirmajām lietām, ko jūs, iespējams, darīsiet, ir vietnes galvenē pievienosiet sava uzņēmuma vai zīmola logotipu.</span><span class="sxs-lookup"><span data-stu-id="adc62-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="adc62-107">Tiešsaistes moduļu bibliotēka Dynamics 365 Commerce nodrošina moduli, kas atvieglo šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="adc62-107">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="adc62-108">Logotipu var pievienot tieši veidnei, izkārtojumam vai lapai.</span><span class="sxs-lookup"><span data-stu-id="adc62-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="adc62-109">Tādā veidā jūs varat viegli nomainīt logotipu, kas parādās konkrētās lapās vai lapu grupās.</span><span class="sxs-lookup"><span data-stu-id="adc62-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="adc62-110">Tomēr šī tēma attiecas uz visbiežāk sastopamo scenāriju, kur jūs pievienojat savu logotipu galvenes fragmentam, ko var atkārtoti izmantot visās vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="adc62-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="adc62-111">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="adc62-111">Prerequisites</span></span>

<span data-ttu-id="adc62-112">Lai varētu pievienot logotipu visām vietnes lapām, jums ir jāizpilda tālāk aprakstītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="adc62-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="adc62-113">Savs logotipa augšupielāde multivides bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="adc62-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="adc62-114">izveidojiet galvenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="adc62-114">Create a header fragment.</span></span> <span data-ttu-id="adc62-115">Vairāk informācijas par fragmentu izveidi un izmantošanu skatiet sadaļā [Darbs ar fragmentiem](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="adc62-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="adc62-116">Iekļaujiet veidnē galvenes fragmentu, kuru jūsu vietnes lapas izmanto izkārtojumu un moduļu opcijām.</span><span class="sxs-lookup"><span data-stu-id="adc62-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="adc62-117">Vairāk informācijas par veidnēm skatiet sadaļā [Darbs ar veidnēm](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="adc62-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="adc62-118">Logotipa pievienošana galvenes fragmentam</span><span class="sxs-lookup"><span data-stu-id="adc62-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="adc62-119">Lai pievienotu logotipu vietnes galvenes fragmentam, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="adc62-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="adc62-120">Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="adc62-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="adc62-121">Atlasiet iepriekš izveidoto galvenes fragmentu un pēc tam izvēlieties **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="adc62-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="adc62-122">Paplašiniet galvenes moduli.</span><span class="sxs-lookup"><span data-stu-id="adc62-122">Expand the header module.</span></span>
1. <span data-ttu-id="adc62-123">Galvenes moduļa rekvizītu rūtī ir jānorāda logotipa attēls un saite.</span><span class="sxs-lookup"><span data-stu-id="adc62-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="adc62-124">Saglabājiet galvenes fragmentu, pabeidziet to rediģēt un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="adc62-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="adc62-125">Pēc atjauninātā galvenes fragmenta publicēšanas visās vietņu lapās, kurās tiek izmantota veidne, kurā ir galvenes fragments, tiks parādīts jūsu logotips.</span><span class="sxs-lookup"><span data-stu-id="adc62-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adc62-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="adc62-126">Additional resources</span></span>

[<span data-ttu-id="adc62-127">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="adc62-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="adc62-128">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="adc62-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="adc62-129">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="adc62-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="adc62-130">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="adc62-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="adc62-131">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="adc62-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="adc62-132">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="adc62-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="adc62-133">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="adc62-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]