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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055834"
---
# <a name="site-selector-module"></a><span data-ttu-id="ae909-103">Vietas atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="ae909-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ae909-104">Šajā tēmā tiek stāstīts par vietas atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ae909-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ae909-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ae909-105">Overview</span></span>

<span data-ttu-id="ae909-106">Ja uzņēmumam ir dažādas vietas tirgos, reģionos un lokalizācijās, vietas lietotājiem ir nepieciešams viegls veids, kā pārslēgties starp vietām un izvēlēties savu vēlamo iepirkšanās vietu.</span><span class="sxs-lookup"><span data-stu-id="ae909-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="ae909-107">Lai pielāgotu šo scenāriju, vietas atlasītāja modulis ļauj lietotājiem pārlūkot vairākās vietās.</span><span class="sxs-lookup"><span data-stu-id="ae909-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="ae909-108">Vietas atlasītāja modulis ir jākonfigurē ar vietu sarakstu (tirgiem, reģioniem vai lokalizācijām), ko vietas lietotāji var pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="ae909-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="ae909-109">Vietas modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.</span><span class="sxs-lookup"><span data-stu-id="ae909-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="ae909-110">Attēlā zemāk ir parādīts vietas atlasītāja moduļa piemērs, kas attēlots vietas lapas galvenē.</span><span class="sxs-lookup"><span data-stu-id="ae909-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Vietas atlasītāja moduļa piemērs vietas lapas galvenē](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="ae909-112">Vietas atlasītāja moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="ae909-112">Site selector module properties</span></span>

| <span data-ttu-id="ae909-113">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="ae909-113">Property name</span></span> | <span data-ttu-id="ae909-114">Vērtība</span><span class="sxs-lookup"><span data-stu-id="ae909-114">Value</span></span>                 | <span data-ttu-id="ae909-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ae909-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="ae909-116">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="ae909-116">Heading</span></span>       | <span data-ttu-id="ae909-117">Teksts</span><span class="sxs-lookup"><span data-stu-id="ae909-117">Text</span></span>                  | <span data-ttu-id="ae909-118">Moduļa virsraksts.</span><span class="sxs-lookup"><span data-stu-id="ae909-118">The heading for the module.</span></span> |
| <span data-ttu-id="ae909-119">Vietnes opcijas</span><span class="sxs-lookup"><span data-stu-id="ae909-119">Site options</span></span>  | <span data-ttu-id="ae909-120">Nosaukums, attēls, vietrādis URL</span><span class="sxs-lookup"><span data-stu-id="ae909-120">Name, Image, URL</span></span>      | <span data-ttu-id="ae909-121">Šis rekvizīts norāda nosaukumu, saiti uz vietas mājas lapu un neobligātu attēlu, ko rādīt katrai vietai, kas ir iekļauta modulī.</span><span class="sxs-lookup"><span data-stu-id="ae909-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="ae909-122">Attēls var būt karodziņš vai kāds tirgus, reģiona vai lokalizācijas attēlojums.</span><span class="sxs-lookup"><span data-stu-id="ae909-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="ae909-123">Vietas atlasītāja moduļa pievienošana lapai</span><span class="sxs-lookup"><span data-stu-id="ae909-123">Add a site selector module to a page</span></span>

<span data-ttu-id="ae909-124">Vietas atlasītāja moduli var pievienot [Galvenes modulim](author-header-module.md) vietas atlasītāja slotā.</span><span class="sxs-lookup"><span data-stu-id="ae909-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="ae909-125">Pēc tam, kad tas ir pievienots, varat definēt moduļa virsraksta un vietas opcijas.</span><span class="sxs-lookup"><span data-stu-id="ae909-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae909-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ae909-126">Additional resources</span></span>

[<span data-ttu-id="ae909-127">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="ae909-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ae909-128">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="ae909-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ae909-129">Atpakaļceļa modulis</span><span class="sxs-lookup"><span data-stu-id="ae909-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="ae909-130">Navigācijas izvēlnes modulis</span><span class="sxs-lookup"><span data-stu-id="ae909-130">Navigation menu module</span></span>](nav-menu-module.md)
