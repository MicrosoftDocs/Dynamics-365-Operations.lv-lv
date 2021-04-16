---
title: Preču klasifikācijas hierarhijas izveide
description: Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.
author: ShylaThompson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4e2fdc62d7faa73efa78092d7754d3fa1213a94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809378"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="776b5-103">Preču klasifikācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="776b5-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="776b5-104">Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="776b5-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="776b5-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="776b5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="776b5-106">Šī procedūra ir paredzēta kategoriju pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="776b5-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="776b5-107">Jaunas kategoriju hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="776b5-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="776b5-108">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Iestatīšana > Kategorijas un atribūti > Kategoriju hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="776b5-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="776b5-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="776b5-109">Click **New**.</span></span>
3. <span data-ttu-id="776b5-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="776b5-111">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="776b5-112">Noklikšķiniet uz **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="776b5-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="776b5-113">Hierarhijas veidošana</span><span class="sxs-lookup"><span data-stu-id="776b5-113">Build the hierarchy</span></span>
1. <span data-ttu-id="776b5-114">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="776b5-114">Click **New** category node.</span></span>
2. <span data-ttu-id="776b5-115">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="776b5-116">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="776b5-117">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="776b5-118">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="776b5-118">Click **New** category node.</span></span>
6. <span data-ttu-id="776b5-119">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="776b5-120">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="776b5-121">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="776b5-122">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="776b5-122">Click **New** category node.</span></span>
10. <span data-ttu-id="776b5-123">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="776b5-124">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="776b5-125">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="776b5-126">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="776b5-126">Click **New** category node.</span></span>
14. <span data-ttu-id="776b5-127">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="776b5-128">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="776b5-129">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="776b5-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="776b5-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="776b5-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="776b5-131">Hierarhijas klasificēšana</span><span class="sxs-lookup"><span data-stu-id="776b5-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="776b5-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="776b5-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="776b5-133">**Darbību rūtī** noklikšķiniet uz **Kategoriju hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="776b5-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="776b5-134">Noklikšķiniet uz **Saistīt hierarhijas veidu**.</span><span class="sxs-lookup"><span data-stu-id="776b5-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="776b5-135">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="776b5-135">Click **New**.</span></span>
5. <span data-ttu-id="776b5-136">Laukā **Kategoriju hierarhijas veids** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="776b5-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="776b5-137">Atlasiet **Preču koda kategorijas hierarhijas veids preču klasifikācijai**.</span><span class="sxs-lookup"><span data-stu-id="776b5-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="776b5-138">Laukā **Kategoriju hierarhija** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="776b5-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="776b5-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="776b5-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="776b5-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="776b5-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="776b5-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="776b5-141">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]