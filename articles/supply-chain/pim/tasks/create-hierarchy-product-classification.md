---
title: Preču klasifikācijas hierarhijas izveide
description: Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ac87356f46edc118a592acd393823603815917a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150120"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="eb9f1-103">Preču klasifikācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="eb9f1-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb9f1-104">Šajā procedūrā tiek parādīts, kā izveidot jaunu kategoriju hierarhiju un piešķirt preču kodu hierarhijas tipu.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="eb9f1-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="eb9f1-106">Šī procedūra ir paredzēta kategoriju pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="eb9f1-107">Jaunas kategoriju hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="eb9f1-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="eb9f1-108">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Iestatīšana > Kategorijas un atribūti > Kategoriju hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="eb9f1-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-109">Click **New**.</span></span>
3. <span data-ttu-id="eb9f1-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="eb9f1-111">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="eb9f1-112">Noklikšķiniet uz **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="eb9f1-113">Hierarhijas veidošana</span><span class="sxs-lookup"><span data-stu-id="eb9f1-113">Build the hierarchy</span></span>
1. <span data-ttu-id="eb9f1-114">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-114">Click **New** category node.</span></span>
2. <span data-ttu-id="eb9f1-115">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="eb9f1-116">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="eb9f1-117">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="eb9f1-118">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-118">Click **New** category node.</span></span>
6. <span data-ttu-id="eb9f1-119">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="eb9f1-120">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="eb9f1-121">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="eb9f1-122">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-122">Click **New** category node.</span></span>
10. <span data-ttu-id="eb9f1-123">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="eb9f1-124">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="eb9f1-125">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="eb9f1-126">Noklikšķiniet uz kategorijas zara **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-126">Click **New** category node.</span></span>
14. <span data-ttu-id="eb9f1-127">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="eb9f1-128">Laukā **Kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="eb9f1-129">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="eb9f1-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="eb9f1-131">Hierarhijas klasificēšana</span><span class="sxs-lookup"><span data-stu-id="eb9f1-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="eb9f1-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="eb9f1-133">**Darbību rūtī** noklikšķiniet uz **Kategoriju hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="eb9f1-134">Noklikšķiniet uz **Saistīt hierarhijas veidu**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="eb9f1-135">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-135">Click **New**.</span></span>
5. <span data-ttu-id="eb9f1-136">Laukā **Kategoriju hierarhijas veids** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="eb9f1-137">Atlasiet **Preču koda kategorijas hierarhijas veids preču klasifikācijai**.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="eb9f1-138">Laukā **Kategoriju hierarhija** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="eb9f1-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="eb9f1-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="eb9f1-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="eb9f1-141">Close the page.</span></span>

