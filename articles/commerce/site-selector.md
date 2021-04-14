---
title: Vietas atlasītāja modulis
description: Šajā tēmā aplūkots vietņu atlasītāja modulis un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6e8eefe7afe385ca77eca6027638ff938e1356e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791779"
---
# <a name="site-selector-module"></a><span data-ttu-id="715a4-103">Vietņu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="715a4-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="715a4-104">Šajā tēmā aplūkots vietņu atlasītāja modulis un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="715a4-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="715a4-105">Ja uzņēmumam ir dažādas vietas tirgos, reģionos un lokalizācijās, vietas lietotājiem ir nepieciešams viegls veids, kā pārslēgties starp vietām un izvēlēties savu vēlamo iepirkšanās vietu.</span><span class="sxs-lookup"><span data-stu-id="715a4-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="715a4-106">Lai pielāgotu šo scenāriju, vietas atlasītāja modulis ļauj lietotājiem pārlūkot vairākās vietās.</span><span class="sxs-lookup"><span data-stu-id="715a4-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="715a4-107">Vietas atlasītāja modulis ir jākonfigurē ar vietu sarakstu (tirgiem, reģioniem vai lokalizācijām), ko vietas lietotāji var pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="715a4-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="715a4-108">Vietas modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.</span><span class="sxs-lookup"><span data-stu-id="715a4-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="715a4-109">Attēlā zemāk ir parādīts vietas atlasītāja moduļa piemērs, kas attēlots vietas lapas galvenē.</span><span class="sxs-lookup"><span data-stu-id="715a4-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Vietas atlasītāja moduļa piemērs vietas lapas galvenē](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="715a4-111">Vietas atlasītāja moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="715a4-111">Site selector module properties</span></span>

| <span data-ttu-id="715a4-112">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="715a4-112">Property name</span></span> | <span data-ttu-id="715a4-113">Vērtība</span><span class="sxs-lookup"><span data-stu-id="715a4-113">Value</span></span>                 | <span data-ttu-id="715a4-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="715a4-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="715a4-115">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="715a4-115">Heading</span></span>       | <span data-ttu-id="715a4-116">Teksts</span><span class="sxs-lookup"><span data-stu-id="715a4-116">Text</span></span>                  | <span data-ttu-id="715a4-117">Moduļa virsraksts.</span><span class="sxs-lookup"><span data-stu-id="715a4-117">The heading for the module.</span></span> |
| <span data-ttu-id="715a4-118">Vietnes opcijas</span><span class="sxs-lookup"><span data-stu-id="715a4-118">Site options</span></span>  | <span data-ttu-id="715a4-119">Nosaukums, attēls, vietrādis URL</span><span class="sxs-lookup"><span data-stu-id="715a4-119">Name, Image, URL</span></span>      | <span data-ttu-id="715a4-120">Šis rekvizīts norāda nosaukumu, saiti uz vietas mājas lapu un neobligātu attēlu, ko rādīt katrai vietai, kas ir iekļauta modulī.</span><span class="sxs-lookup"><span data-stu-id="715a4-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="715a4-121">Attēls var būt karodziņš vai kāds tirgus, reģiona vai lokalizācijas attēlojums.</span><span class="sxs-lookup"><span data-stu-id="715a4-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="715a4-122">Vietas atlasītāja moduļa pievienošana lapai</span><span class="sxs-lookup"><span data-stu-id="715a4-122">Add a site selector module to a page</span></span>

<span data-ttu-id="715a4-123">Vietas atlasītāja moduli var pievienot [Galvenes modulim](author-header-module.md) vietas atlasītāja slotā.</span><span class="sxs-lookup"><span data-stu-id="715a4-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="715a4-124">Pēc tam, kad tas ir pievienots, varat definēt moduļa virsraksta un vietas opcijas.</span><span class="sxs-lookup"><span data-stu-id="715a4-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="715a4-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="715a4-125">Additional resources</span></span>

[<span data-ttu-id="715a4-126">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="715a4-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="715a4-127">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="715a4-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="715a4-128">Atpakaļceļa modulis</span><span class="sxs-lookup"><span data-stu-id="715a4-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="715a4-129">Navigācijas izvēlnes modulis</span><span class="sxs-lookup"><span data-stu-id="715a4-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]