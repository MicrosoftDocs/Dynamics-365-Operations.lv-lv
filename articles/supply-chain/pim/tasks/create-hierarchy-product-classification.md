---
title: Preču klasifikācijas hierarhijas izveide
description: Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74be72ac5787273e13692abdb9db18be4c5ccc08
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966959"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="bcf41-103">Preču klasifikācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="bcf41-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcf41-104">Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="bcf41-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="bcf41-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="bcf41-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bcf41-106">Šī procedūra ir paredzēta kategoriju pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="bcf41-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="bcf41-107">Jaunas kategoriju hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="bcf41-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="bcf41-108">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Iestatīšana > Kategorijas un atribūti > Kategoriju hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="bcf41-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-109">Click **New**.</span></span>
3. <span data-ttu-id="bcf41-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="bcf41-111">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="bcf41-112">Noklikšķiniet uz **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="bcf41-113">Hierarhijas veidošana</span><span class="sxs-lookup"><span data-stu-id="bcf41-113">Build the hierarchy</span></span>
1. <span data-ttu-id="bcf41-114">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-114">Click **New** category node.</span></span>
2. <span data-ttu-id="bcf41-115">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="bcf41-116">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="bcf41-117">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="bcf41-118">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-118">Click **New** category node.</span></span>
6. <span data-ttu-id="bcf41-119">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="bcf41-120">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="bcf41-121">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="bcf41-122">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-122">Click **New** category node.</span></span>
10. <span data-ttu-id="bcf41-123">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="bcf41-124">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="bcf41-125">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="bcf41-126">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-126">Click **New** category node.</span></span>
14. <span data-ttu-id="bcf41-127">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="bcf41-128">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="bcf41-129">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bcf41-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="bcf41-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bcf41-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="bcf41-131">Hierarhijas klasificēšana</span><span class="sxs-lookup"><span data-stu-id="bcf41-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="bcf41-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="bcf41-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="bcf41-133">**Darbību rūtī** noklikšķiniet uz **Kategoriju hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="bcf41-134">Noklikšķiniet uz **Saistīt hierarhijas veidu**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="bcf41-135">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-135">Click **New**.</span></span>
5. <span data-ttu-id="bcf41-136">Laukā **Kategoriju hierarhijas veids** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="bcf41-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="bcf41-137">Atlasiet **Preču koda kategorijas hierarhijas veids preču klasifikācijai**.</span><span class="sxs-lookup"><span data-stu-id="bcf41-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="bcf41-138">Laukā **Kategoriju hierarhija** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="bcf41-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bcf41-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="bcf41-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="bcf41-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="bcf41-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bcf41-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bcf41-141">Close the page.</span></span>

