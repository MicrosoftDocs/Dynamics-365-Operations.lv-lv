--- 
title: "Preču klasifikācijas hierarhijas izveide"
description: "Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 46a5d21550cfe1728ee6ca468c4ad523beb719da
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="46fef-103">Preču klasifikācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="46fef-103">Create a hierarchy of product classification</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46fef-104">Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="46fef-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="46fef-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="46fef-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="46fef-106">Šī procedūra ir paredzēta kategoriju pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="46fef-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="46fef-107">Jaunas kategoriju hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="46fef-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="46fef-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatījumi > Kategorijas un atribūti > Kategoriju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="46fef-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="46fef-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="46fef-109">Click New.</span></span>
3. <span data-ttu-id="46fef-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="46fef-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="46fef-112">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="46fef-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="46fef-113">Hierarhijas veidošana</span><span class="sxs-lookup"><span data-stu-id="46fef-113">Build the hierarchy</span></span>
1. <span data-ttu-id="46fef-114">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="46fef-114">Click New category node.</span></span>
2. <span data-ttu-id="46fef-115">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="46fef-116">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="46fef-117">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="46fef-118">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="46fef-118">Click New category node.</span></span>
6. <span data-ttu-id="46fef-119">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="46fef-120">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="46fef-121">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="46fef-122">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="46fef-122">Click New category node.</span></span>
10. <span data-ttu-id="46fef-123">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="46fef-124">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="46fef-125">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="46fef-126">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="46fef-126">Click New category node.</span></span>
14. <span data-ttu-id="46fef-127">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="46fef-128">Laukā Kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="46fef-129">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46fef-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="46fef-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="46fef-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="46fef-131">Hierarhijas klasificēšana</span><span class="sxs-lookup"><span data-stu-id="46fef-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="46fef-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="46fef-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="46fef-133">Darbību rūtī noklikšķiniet uz Kategoriju hierarhija.</span><span class="sxs-lookup"><span data-stu-id="46fef-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="46fef-134">Noklikšķiniet uz Saistīt hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="46fef-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="46fef-135">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="46fef-135">Click New.</span></span>
5. <span data-ttu-id="46fef-136">Laukā Kategoriju hierarhijas tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="46fef-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="46fef-137">Preču klasifikācijai atlasiet Preču koda kategorijas hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="46fef-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="46fef-138">Laukā Kategoriju hierarhija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="46fef-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="46fef-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="46fef-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="46fef-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="46fef-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="46fef-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="46fef-141">Close the page.</span></span>


