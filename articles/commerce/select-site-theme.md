---
title: Vietnes dizaina atlase
description: Šajā tēmā ir aprakstīts, kā iestatīt vai mainīt vietnes dizainu programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c54a3e9471fdeb56f27fe7c567c7cd7f0b7fd218
ms.sourcegitcommit: 2ef23dcd4e42362186b9951e675010d97d55c6bd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4556433"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="8c5b7-103">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="8c5b7-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8c5b7-104">Šajā tēmā ir aprakstīts, kā iestatīt vai mainīt vietnes dizainu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8c5b7-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="8c5b7-105">Overview</span></span>

<span data-ttu-id="8c5b7-106">Vietnes izkārtojums un stils (piemēram, fonti, lielumi un krāsas) tiek definēti ar dizainu, ko atlasāt un piemērojat vietnei.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="8c5b7-107">Dizainu veido un izvieto izstrādātājs jūsu uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="8c5b7-108">Lai skatītu dizainu pārskatu, skatiet sadaļu [Dizainu pārskats](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="8c5b7-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="8c5b7-109">Papildinformāciju par to, kā izveidot un izvietot dizainus, skatiet sadaļā [Jaunu dizainu izveide](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="8c5b7-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="8c5b7-110">Pēc noklusējuma, pirmoreiz izveidojot vietni, tā lieto tēmu ar nosaukumu **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="8c5b7-111">Šis noklusējuma dizains tiek nodrošināts kā Commerce moduļu bibliotēkas daļa.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="8c5b7-112">Pēc tam, kad esat izvietojis papildu dizainus vietnei, varat konfigurēt vietni, lai tā vietā izmantotu vienu no tiem.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="8c5b7-113">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="8c5b7-113">Select the site theme</span></span>

<span data-ttu-id="8c5b7-114">Lai atlasītu dizainu, kas ir piemērots vietnei, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="8c5b7-115">Vietnes autorēšanas vidē dodieties uz savu vietni.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="8c5b7-116">Dodieties uz **Vietnes pārvaldība** \> **Paplašināmība**.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="8c5b7-117">Sadaļas **Dizains** nolaižamajā izvēlnē atlasiet dizainu.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="8c5b7-118">Lai lietotu atlasīto dizainu savai vietnei, atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="8c5b7-119">Jūsu atlasītais dizains tiek publicēts jūsu vietnē, tiklīdz atlasāt **Saglabāt un publicēt** lapā **Paplašināmība**.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="8c5b7-120">Lai priekšskatītu dizainu vietnē, pirms to lietojat, varat izmantot izstrādes vai smilškastes vidi.</span><span class="sxs-lookup"><span data-stu-id="8c5b7-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c5b7-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8c5b7-121">Additional resources</span></span>

[<span data-ttu-id="8c5b7-122">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="8c5b7-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="8c5b7-123">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="8c5b7-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="8c5b7-124">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="8c5b7-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="8c5b7-125">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="8c5b7-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="8c5b7-126">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="8c5b7-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="8c5b7-127">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="8c5b7-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="8c5b7-128">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="8c5b7-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="8c5b7-129">Dizainu izstrādes pārskats</span><span class="sxs-lookup"><span data-stu-id="8c5b7-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="8c5b7-130">Jauna projekta tēma</span><span class="sxs-lookup"><span data-stu-id="8c5b7-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

