---
title: Vietas seguma vispārējā plānošana, ja noliktava ir obligāta
description: Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensija ir vieta. Noliktava ir obligāta dimensija.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72240e7db8ec914220cb8f8f1185a91a304ff66b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977967"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="c2cca-104">Vietas seguma vispārējā plānošana, ja noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="c2cca-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2cca-105">Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensija ir vieta.</span><span class="sxs-lookup"><span data-stu-id="c2cca-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="c2cca-106">Noliktava ir obligāta dimensija.</span><span class="sxs-lookup"><span data-stu-id="c2cca-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="c2cca-107">Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="c2cca-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="c2cca-108">Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā.</span><span class="sxs-lookup"><span data-stu-id="c2cca-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="c2cca-109">Šo iestatījumu nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="c2cca-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="c2cca-110">Noliktavas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma darbībā.</span><span class="sxs-lookup"><span data-stu-id="c2cca-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="c2cca-111">Vietas dimensija ir iestatīta seguma plānošanai.</span><span class="sxs-lookup"><span data-stu-id="c2cca-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="c2cca-112">Seguma plānošanai var būt iestatītas arī citas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c2cca-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="c2cca-113">Tomēr tās neietekmē šī vairākvietu funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="c2cca-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="c2cca-114">Noliktavas dimensija seguma plānošanai nav iestatīta.</span><span class="sxs-lookup"><span data-stu-id="c2cca-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="c2cca-115">Tāpēc piegādi un pieprasījumu apkopo pēc vietas un, iespējams, arī citas seguma plānotas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c2cca-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="c2cca-116">Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="c2cca-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="c2cca-117">Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:</span><span class="sxs-lookup"><span data-stu-id="c2cca-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="c2cca-118">Krājuma segums tiek definēts krājumam.</span><span class="sxs-lookup"><span data-stu-id="c2cca-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="c2cca-119">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="c2cca-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c2cca-120">Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Krājumu segums**.</span><span class="sxs-lookup"><span data-stu-id="c2cca-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="c2cca-121">Uzpildīšanas attiecības ir definētas noliktavai.</span><span class="sxs-lookup"><span data-stu-id="c2cca-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="c2cca-122">Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="c2cca-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="c2cca-123">Cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.</span><span class="sxs-lookup"><span data-stu-id="c2cca-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="c2cca-124">Noklusējuma pasūtījuma tips ir iestatīts uz Ražošana, Pirkšanas pasūtījums vai Kanban.</span><span class="sxs-lookup"><span data-stu-id="c2cca-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="c2cca-125">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="c2cca-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c2cca-126">Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="c2cca-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="c2cca-127">Formā **Pasūtījuma noklusējuma iestatījumi** skatiet lauku **Noklusējuma pasūtījuma tips** .</span><span class="sxs-lookup"><span data-stu-id="c2cca-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Pieprasīt vietas segumu noliktava obligāta](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="c2cca-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c2cca-129">Additional resources</span></span>
--------

[<span data-ttu-id="c2cca-130">Vispārēja plānošanas un vairākvietu funkcionalitātes pārskats</span><span class="sxs-lookup"><span data-stu-id="c2cca-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="c2cca-131">Galvenais plāns vietas un noliktavas segumam, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="c2cca-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c2cca-132">Vietas seguma vispārējā plānošana, ja noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="c2cca-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c2cca-133">Galvenais plāns vietas un noliktavas segumam, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="c2cca-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c2cca-134">MK versijas noteikšana</span><span class="sxs-lookup"><span data-stu-id="c2cca-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



