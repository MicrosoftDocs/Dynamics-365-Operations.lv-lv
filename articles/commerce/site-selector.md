---
title: Vietas atlasītāja modulis
description: Šajā tēmā tiek stāstīts par vietas atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ed00836c435bd391e5edef1f6a99889c80f45211
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985590"
---
# <a name="site-selector-module"></a><span data-ttu-id="48e1a-103">Vietas atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="48e1a-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48e1a-104">Šajā tēmā tiek stāstīts par vietas atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48e1a-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="48e1a-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="48e1a-105">Overview</span></span>

<span data-ttu-id="48e1a-106">Ja uzņēmumam ir dažādas vietas tirgos, reģionos un lokalizācijās, vietas lietotājiem ir nepieciešams viegls veids, kā pārslēgties starp vietām un izvēlēties savu vēlamo iepirkšanās vietu.</span><span class="sxs-lookup"><span data-stu-id="48e1a-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="48e1a-107">Lai pielāgotu šo scenāriju, vietas atlasītāja modulis ļauj lietotājiem pārlūkot vairākās vietās.</span><span class="sxs-lookup"><span data-stu-id="48e1a-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="48e1a-108">Vietas atlasītāja modulis ir jākonfigurē ar vietu sarakstu (tirgiem, reģioniem vai lokalizācijām), ko vietas lietotāji var pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="48e1a-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="48e1a-109">Vietas modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.</span><span class="sxs-lookup"><span data-stu-id="48e1a-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="48e1a-110">Attēlā zemāk ir parādīts vietas atlasītāja moduļa piemērs, kas attēlots vietas lapas galvenē.</span><span class="sxs-lookup"><span data-stu-id="48e1a-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Vietas atlasītāja moduļa piemērs vietas lapas galvenē](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="48e1a-112">Vietas atlasītāja moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="48e1a-112">Site selector module properties</span></span>

| <span data-ttu-id="48e1a-113">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="48e1a-113">Property name</span></span> | <span data-ttu-id="48e1a-114">Vērtība</span><span class="sxs-lookup"><span data-stu-id="48e1a-114">Value</span></span>                 | <span data-ttu-id="48e1a-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="48e1a-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="48e1a-116">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="48e1a-116">Heading</span></span>       | <span data-ttu-id="48e1a-117">Teksts</span><span class="sxs-lookup"><span data-stu-id="48e1a-117">Text</span></span>                  | <span data-ttu-id="48e1a-118">Moduļa virsraksts.</span><span class="sxs-lookup"><span data-stu-id="48e1a-118">The heading for the module.</span></span> |
| <span data-ttu-id="48e1a-119">Vietnes opcijas</span><span class="sxs-lookup"><span data-stu-id="48e1a-119">Site options</span></span>  | <span data-ttu-id="48e1a-120">Nosaukums, attēls, vietrādis URL</span><span class="sxs-lookup"><span data-stu-id="48e1a-120">Name, Image, URL</span></span>      | <span data-ttu-id="48e1a-121">Šis rekvizīts norāda nosaukumu, saiti uz vietas mājas lapu un neobligātu attēlu, ko rādīt katrai vietai, kas ir iekļauta modulī.</span><span class="sxs-lookup"><span data-stu-id="48e1a-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="48e1a-122">Attēls var būt karodziņš vai kāds tirgus, reģiona vai lokalizācijas attēlojums.</span><span class="sxs-lookup"><span data-stu-id="48e1a-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="48e1a-123">Vietas atlasītāja moduļa pievienošana lapai</span><span class="sxs-lookup"><span data-stu-id="48e1a-123">Add a site selector module to a page</span></span>

<span data-ttu-id="48e1a-124">Vietas atlasītāja moduli var pievienot [Galvenes modulim](author-header-module.md) vietas atlasītāja slotā.</span><span class="sxs-lookup"><span data-stu-id="48e1a-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="48e1a-125">Pēc tam, kad tas ir pievienots, varat definēt moduļa virsraksta un vietas opcijas.</span><span class="sxs-lookup"><span data-stu-id="48e1a-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48e1a-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="48e1a-126">Additional resources</span></span>

[<span data-ttu-id="48e1a-127">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="48e1a-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="48e1a-128">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="48e1a-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="48e1a-129">Atpakaļceļa modulis</span><span class="sxs-lookup"><span data-stu-id="48e1a-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="48e1a-130">Navigācijas izvēlnes modulis</span><span class="sxs-lookup"><span data-stu-id="48e1a-130">Navigation menu module</span></span>](nav-menu-module.md)
