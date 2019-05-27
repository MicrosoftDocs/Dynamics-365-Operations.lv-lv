---
title: Preču klasifikācijas hierarhijas izveide
description: Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb49f5f3f8a5a788cb4c6d1be69534ba808e3675
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568424"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="37e69-103">Preču klasifikācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="37e69-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37e69-104">Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="37e69-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="37e69-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="37e69-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="37e69-106">Šī procedūra ir paredzēta kategoriju pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="37e69-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="37e69-107">Jaunas kategoriju hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="37e69-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="37e69-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatījumi > Kategorijas un atribūti > Kategoriju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="37e69-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="37e69-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="37e69-109">Click New.</span></span>
3. <span data-ttu-id="37e69-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="37e69-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="37e69-112">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="37e69-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="37e69-113">Hierarhijas veidošana</span><span class="sxs-lookup"><span data-stu-id="37e69-113">Build the hierarchy</span></span>
1. <span data-ttu-id="37e69-114">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="37e69-114">Click New category node.</span></span>
2. <span data-ttu-id="37e69-115">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="37e69-116">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="37e69-117">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="37e69-118">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="37e69-118">Click New category node.</span></span>
6. <span data-ttu-id="37e69-119">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="37e69-120">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="37e69-121">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="37e69-122">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="37e69-122">Click New category node.</span></span>
10. <span data-ttu-id="37e69-123">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="37e69-124">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="37e69-125">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="37e69-126">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="37e69-126">Click New category node.</span></span>
14. <span data-ttu-id="37e69-127">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="37e69-128">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="37e69-129">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37e69-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="37e69-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="37e69-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="37e69-131">Hierarhijas klasificēšana</span><span class="sxs-lookup"><span data-stu-id="37e69-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="37e69-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="37e69-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="37e69-133">Darbību rūtī noklikšķiniet uz Kategoriju hierarhija.</span><span class="sxs-lookup"><span data-stu-id="37e69-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="37e69-134">Noklikšķiniet uz Saistīt hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="37e69-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="37e69-135">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="37e69-135">Click New.</span></span>
5. <span data-ttu-id="37e69-136">Laukā Kategoriju hierarhijas tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="37e69-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="37e69-137">Preču klasifikācijai atlasiet Preču koda kategorijas hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="37e69-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="37e69-138">Laukā Kategoriju hierarhija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="37e69-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="37e69-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="37e69-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="37e69-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="37e69-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="37e69-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="37e69-141">Close the page.</span></span>

