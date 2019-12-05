---
title: Vietas seguma vispārējā plānošana, ja noliktava nav obligāta
description: Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram nodrošinājumam ir iestatīta vietas dimensija.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43989f95764a60dc7f5662ef74c005c5fddaa275
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813735"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="2190c-103">Vietas seguma vispārējā plānošana, ja noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="2190c-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2190c-104">Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram nodrošinājumam ir iestatīta vietas dimensija.</span><span class="sxs-lookup"><span data-stu-id="2190c-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="2190c-105">Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="2190c-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="2190c-106">Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā.</span><span class="sxs-lookup"><span data-stu-id="2190c-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="2190c-107">Noliktavas dimensija nav iestatīta kā obligāta.</span><span class="sxs-lookup"><span data-stu-id="2190c-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="2190c-108">Noliktava var būt zināma, bet tā netiek izmantota vispārējās plānošanas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="2190c-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="2190c-109">Vietas dimensija ir iestatīta seguma plānošanai.</span><span class="sxs-lookup"><span data-stu-id="2190c-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="2190c-110">Noliktavas dimensija seguma plānošanai nav iestatīta.</span><span class="sxs-lookup"><span data-stu-id="2190c-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="2190c-111">Tāpēc piegādi un pieprasījumu apkopo pēc vietas un, iespējams, arī citas seguma plānotas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="2190c-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="2190c-112">Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="2190c-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="2190c-113">Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:</span><span class="sxs-lookup"><span data-stu-id="2190c-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="2190c-114">Krājuma segums tiek definēts krājumam.</span><span class="sxs-lookup"><span data-stu-id="2190c-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="2190c-115">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="2190c-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="2190c-116">Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Krājumu segums**.</span><span class="sxs-lookup"><span data-stu-id="2190c-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="2190c-117">Uzpildīšanas attiecības ir definētas noliktavai.</span><span class="sxs-lookup"><span data-stu-id="2190c-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="2190c-118">Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="2190c-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="2190c-119">Cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.</span><span class="sxs-lookup"><span data-stu-id="2190c-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="2190c-120">Noklusējuma pasūtījuma tips ir iestatīts uz ražošanu, pirkšanas pasūtījumu vai Kanban.</span><span class="sxs-lookup"><span data-stu-id="2190c-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="2190c-121">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="2190c-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="2190c-122">Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="2190c-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="2190c-123">Veidlapā **Pasūtījuma noklusējuma iestatījumi**, skatiet lauku **Noklusējuma pasūtījuma tips**.</span><span class="sxs-lookup"><span data-stu-id="2190c-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Pieprasīt vietas segumu noliktava nav obligāta](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="2190c-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2190c-125">Additional resources</span></span>
--------

[<span data-ttu-id="2190c-126">Vispārēja plānošanas un vairākvietu funkcionalitātes pārskats</span><span class="sxs-lookup"><span data-stu-id="2190c-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="2190c-127">Galvenais plāns vietas un noliktavas segumam, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="2190c-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="2190c-128">Vietas seguma vispārējā plānošana, ja noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="2190c-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="2190c-129">Vietas seguma vispārējā plānošana, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="2190c-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="2190c-130">MK versijas noteikšana</span><span class="sxs-lookup"><span data-stu-id="2190c-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



