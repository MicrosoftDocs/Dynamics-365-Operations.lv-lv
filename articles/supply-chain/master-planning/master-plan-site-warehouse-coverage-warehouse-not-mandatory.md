---
title: "Vietas un noliktavas segums vispārējā plānošana, ja noliktava nav obligāta"
description: "Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensijas ir vieta un noliktava. Noliktavas dimensija nav obligāta."
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
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9c7b13a7a018ce584c877fed6212abc3c2913903
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="3eb8c-104">Vietas un noliktavas segums vispārējā plānošana, ja noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="3eb8c-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3eb8c-105">Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensijas ir vieta un noliktava.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="3eb8c-106">Noliktavas dimensija nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="3eb8c-107">Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="3eb8c-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="3eb8c-108">Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="3eb8c-109">Šo iestatījumu nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="3eb8c-110">Noliktavas dimensija nav iestatīta kā obligāta.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="3eb8c-111">Noliktava var būt zināma, bet tā netiek izmantota vispārējās plānošanas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="3eb8c-112">Vieta un noliktavas dimensija ir iestatīti seguma plānošanai.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="3eb8c-113">Seguma plānošanai var iestatīt arī citas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="3eb8c-114">Tomēr tās neietekmēs daudzvietu funkcija.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="3eb8c-115">Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="3eb8c-116">Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:</span><span class="sxs-lookup"><span data-stu-id="3eb8c-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="3eb8c-117">Noliktava iestatīta kā Manuāli.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="3eb8c-118">Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="3eb8c-119">Kopsavilkuma cilnē **Vispārējā plānošana** skatiet lauku **Manuāls**.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="3eb8c-120">Krājuma segums tiek definēts krājumam.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="3eb8c-121">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="3eb8c-122">Atlasiet krājumu un pēc tam darbību rūts cilnē **Plāns** noklikšķiniet uz **Krājumu segums**.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="3eb8c-123">Uzpildīšanas attiecības ir definētas noliktavai.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="3eb8c-124">Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="3eb8c-125">Kopsavilkuma cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="3eb8c-126">Noklusējuma pasūtījuma tips ir iestatīts uz Ražošana, Pirkšanas pasūtījums vai Kanban.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="3eb8c-127">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="3eb8c-128">Atlasiet krājumu un pēc tam darbību rūts cilnē **Plāns** noklikšķiniet uz **Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="3eb8c-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="3eb8c-129">Formā **Pasūtījuma noklusējuma iestatījumi** skatiet lauku **Noklusējuma pasūtījuma tips** .</span><span class="sxs-lookup"><span data-stu-id="3eb8c-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Pieprasīt vietu un noliktavu, noliktavu nē](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a><span data-ttu-id="3eb8c-131">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="3eb8c-131">See also</span></span>
--------

[<span data-ttu-id="3eb8c-132">Vispārējā plānošana un vairākvietu funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="3eb8c-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="3eb8c-133">Vispārējā plānošana — vietas un noliktavas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="3eb8c-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3eb8c-134">Vispārējā plānošana — vietas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="3eb8c-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3eb8c-135">Vispārējā plānošana — vietas segums, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="3eb8c-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="3eb8c-136">Vispārējā plānošana — kā tiek noteikta MK versija</span><span class="sxs-lookup"><span data-stu-id="3eb8c-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




