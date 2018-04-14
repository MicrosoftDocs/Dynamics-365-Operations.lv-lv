---
title: "Vietas seguma vispārējā plānošana, ja noliktava ir obligāta"
description: "Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensija ir vieta. Noliktava ir obligāta dimensija."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fcfdbf8cdc6aae7f82ba308d450b754d652ac699
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="bdf3c-104">Vietas seguma vispārējā plānošana, ja noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="bdf3c-104">Master planning for site coverage, mandatory warehouse</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bdf3c-105">Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensija ir vieta.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="bdf3c-106">Noliktava ir obligāta dimensija.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="bdf3c-107">Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="bdf3c-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="bdf3c-108">Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="bdf3c-109">Šo iestatījumu nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="bdf3c-110">Noliktavas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma darbībā.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="bdf3c-111">Vietas dimensija ir iestatīta seguma plānošanai.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="bdf3c-112">Seguma plānošanai var būt iestatītas arī citas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="bdf3c-113">Tomēr tās neietekmē šī vairākvietu funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="bdf3c-114">Noliktavas dimensija seguma plānošanai nav iestatīta.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="bdf3c-115">Tāpēc piegādi un pieprasījumu apkopo pēc vietas un, iespējams, arī citas seguma plānotas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="bdf3c-116">Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="bdf3c-117">Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:</span><span class="sxs-lookup"><span data-stu-id="bdf3c-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="bdf3c-118">Krājuma segums tiek definēts krājumam.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="bdf3c-119">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="bdf3c-120">Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Krājumu segums**.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="bdf3c-121">Uzpildīšanas attiecības ir definētas noliktavai.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="bdf3c-122">Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="bdf3c-123">Cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="bdf3c-124">Noklusējuma pasūtījuma tips ir iestatīts uz Ražošana, Pirkšanas pasūtījums vai Kanban.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="bdf3c-125">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="bdf3c-126">Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="bdf3c-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="bdf3c-127">Formā **Pasūtījuma noklusējuma iestatījumi** skatiet lauku **Noklusējuma pasūtījuma tips** .</span><span class="sxs-lookup"><span data-stu-id="bdf3c-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Pieprasīt vietas segumu noliktava obligāta](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="bdf3c-129">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="bdf3c-129">See also</span></span>
--------

[<span data-ttu-id="bdf3c-130">Vispārējā plānošana un vairākvietu funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="bdf3c-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="bdf3c-131">Vispārējā plānošana — vietas un noliktavas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="bdf3c-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="bdf3c-132">Vispārējā plānošana — vietas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="bdf3c-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="bdf3c-133">Vispārējā plānošana — vietas un noliktavas segums, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="bdf3c-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="bdf3c-134">Vispārējā plānošana — kā tiek noteikta MK versija</span><span class="sxs-lookup"><span data-stu-id="bdf3c-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




