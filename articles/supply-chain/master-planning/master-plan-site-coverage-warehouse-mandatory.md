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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14df626025a22237afe30cc5b08d42b475fc3a4f
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="37bae-104">Vietas seguma vispārējā plānošana, ja noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="37bae-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="37bae-105">Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensija ir vieta.</span><span class="sxs-lookup"><span data-stu-id="37bae-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="37bae-106">Noliktava ir obligāta dimensija.</span><span class="sxs-lookup"><span data-stu-id="37bae-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="37bae-107">Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="37bae-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="37bae-108">Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā.</span><span class="sxs-lookup"><span data-stu-id="37bae-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="37bae-109">Šo iestatījumu nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="37bae-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="37bae-110">Noliktavas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma darbībā.</span><span class="sxs-lookup"><span data-stu-id="37bae-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="37bae-111">Vietas dimensija ir iestatīta seguma plānošanai.</span><span class="sxs-lookup"><span data-stu-id="37bae-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="37bae-112">Seguma plānošanai var būt iestatītas arī citas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="37bae-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="37bae-113">Tomēr tās neietekmē šī vairākvietu funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="37bae-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="37bae-114">Noliktavas dimensija seguma plānošanai nav iestatīta.</span><span class="sxs-lookup"><span data-stu-id="37bae-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="37bae-115">Tāpēc piegādi un pieprasījumu apkopo pēc vietas un, iespējams, arī citas seguma plānotas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="37bae-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="37bae-116">Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="37bae-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="37bae-117">Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:</span><span class="sxs-lookup"><span data-stu-id="37bae-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="37bae-118">Krājuma segums tiek definēts krājumam.</span><span class="sxs-lookup"><span data-stu-id="37bae-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="37bae-119">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="37bae-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="37bae-120">Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Krājumu segums**.</span><span class="sxs-lookup"><span data-stu-id="37bae-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="37bae-121">Uzpildīšanas attiecības ir definētas noliktavai.</span><span class="sxs-lookup"><span data-stu-id="37bae-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="37bae-122">Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="37bae-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="37bae-123">Cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.</span><span class="sxs-lookup"><span data-stu-id="37bae-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="37bae-124">Noklusējuma pasūtījuma tips ir iestatīts uz Ražošana, Pirkšanas pasūtījums vai Kanban.</span><span class="sxs-lookup"><span data-stu-id="37bae-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="37bae-125">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="37bae-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="37bae-126">Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="37bae-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="37bae-127">Formā **Pasūtījuma noklusējuma iestatījumi** skatiet lauku **Noklusējuma pasūtījuma tips** .</span><span class="sxs-lookup"><span data-stu-id="37bae-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Pieprasīt vietas segumu noliktava obligāta](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="37bae-129">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="37bae-129">See also</span></span>
--------

[<span data-ttu-id="37bae-130">Vispārējā plānošana un vairākvietu funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="37bae-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="37bae-131">Vispārējā plānošana — vietas un noliktavas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="37bae-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="37bae-132">Vispārējā plānošana — vietas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="37bae-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="37bae-133">Vispārējā plānošana — vietas un noliktavas segums, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="37bae-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="37bae-134">Vispārējā plānošana — kā tiek noteikta MK versija</span><span class="sxs-lookup"><span data-stu-id="37bae-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




