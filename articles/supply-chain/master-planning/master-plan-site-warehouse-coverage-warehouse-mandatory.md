---
title: "Vietas un noliktavas segums vispārējā plānošana, ja noliktava ir obligāta"
description: "Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensijas ir vieta un noliktava. Noliktavas dimensija ir obligāta."
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 61c007711c593df063a497b980f501589d88470c
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="1c9d9-104">Vietas un noliktavas segums vispārējā plānošana, ja noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="1c9d9-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c9d9-105">Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensijas ir vieta un noliktava.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="1c9d9-106">Noliktavas dimensija ir obligāta.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="1c9d9-107">Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="1c9d9-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="1c9d9-108">Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="1c9d9-109">Noliktavas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma darbībā.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="1c9d9-110">Vieta un noliktavas dimensija ir iestatīta seguma plānošanai.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="1c9d9-111">Seguma plānošanai var iestatīt arī citas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="1c9d9-112">Tomēr tās neietekmēs daudzvietu funkcija.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="1c9d9-113">Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="1c9d9-114">Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:</span><span class="sxs-lookup"><span data-stu-id="1c9d9-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="1c9d9-115">Noliktavas iestatījums ir **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="1c9d9-116">Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="1c9d9-117">Kopsavilkuma cilnē **Vispārējā plānošana** skatiet lauku **Manuāls**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="1c9d9-118">Krājuma segums tiek definēts krājumam.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="1c9d9-119">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="1c9d9-120">Atlasiet krājumu un pēc tam darbību rūts cilnē **Plāns** noklikšķiniet uz **Krājumu segums**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="1c9d9-121">Uzpildīšanas attiecības ir definētas noliktavai.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="1c9d9-122">Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="1c9d9-123">Kopsavilkuma cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="1c9d9-124">Noklusējuma pasūtījuma tips ir iestatīts uz Ražošana, Pirkšanas pasūtījums vai Kanban.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="1c9d9-125">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="1c9d9-126">Atlasiet krājumu un pēc tam darbību rūts cilnē **Plāns** noklikšķiniet uz **Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="1c9d9-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="1c9d9-127">Formā **Pasūtījuma noklusējuma iestatījumi** skatiet lauku **Noklusējuma pasūtījuma tips** .</span><span class="sxs-lookup"><span data-stu-id="1c9d9-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Pieprasīt vietas un noliktavas segumu, ja obligāts](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="1c9d9-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1c9d9-129">Additional resources</span></span>
--------

[<span data-ttu-id="1c9d9-130">Vispārēja plānošana un vairākvietu funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="1c9d9-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="1c9d9-131">Vispārējā plānošana — vietas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="1c9d9-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="1c9d9-132">Vispārējā plānošana — vietas segums, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="1c9d9-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="1c9d9-133">Vispārējā plānošana — vietas un noliktavas segums, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="1c9d9-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="1c9d9-134">Vispārējā plānošana — kā tiek noteikta MK versija</span><span class="sxs-lookup"><span data-stu-id="1c9d9-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




