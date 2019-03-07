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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "346828"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="d563f-103">Preču klasifikācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="d563f-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d563f-104">Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="d563f-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="d563f-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="d563f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d563f-106">Šī procedūra ir paredzēta kategoriju pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="d563f-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="d563f-107">Jaunas kategoriju hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="d563f-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="d563f-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatījumi > Kategorijas un atribūti > Kategoriju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="d563f-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="d563f-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d563f-109">Click New.</span></span>
3. <span data-ttu-id="d563f-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d563f-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d563f-112">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="d563f-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="d563f-113">Hierarhijas veidošana</span><span class="sxs-lookup"><span data-stu-id="d563f-113">Build the hierarchy</span></span>
1. <span data-ttu-id="d563f-114">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="d563f-114">Click New category node.</span></span>
2. <span data-ttu-id="d563f-115">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="d563f-116">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="d563f-117">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="d563f-118">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="d563f-118">Click New category node.</span></span>
6. <span data-ttu-id="d563f-119">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="d563f-120">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="d563f-121">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="d563f-122">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="d563f-122">Click New category node.</span></span>
10. <span data-ttu-id="d563f-123">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="d563f-124">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="d563f-125">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="d563f-126">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="d563f-126">Click New category node.</span></span>
14. <span data-ttu-id="d563f-127">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="d563f-128">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="d563f-129">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d563f-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="d563f-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d563f-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="d563f-131">Hierarhijas klasificēšana</span><span class="sxs-lookup"><span data-stu-id="d563f-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="d563f-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d563f-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="d563f-133">Darbību rūtī noklikšķiniet uz Kategoriju hierarhija.</span><span class="sxs-lookup"><span data-stu-id="d563f-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="d563f-134">Noklikšķiniet uz Saistīt hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="d563f-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="d563f-135">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d563f-135">Click New.</span></span>
5. <span data-ttu-id="d563f-136">Laukā Kategoriju hierarhijas tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="d563f-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="d563f-137">Preču klasifikācijai atlasiet Preču koda kategorijas hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="d563f-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="d563f-138">Laukā Kategoriju hierarhija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d563f-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d563f-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d563f-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d563f-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d563f-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d563f-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d563f-141">Close the page.</span></span>

