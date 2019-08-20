---
title: Kontu struktūru izveide
description: Šajā uzdevumu ceļvedī aprakstīts, kā radīt konta struktūru.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2183f88356fc8094781af147bf079c4e53ffb2b4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846707"
---
# <a name="create-account-structures"></a><span data-ttu-id="be720-103">Kontu struktūru izveide</span><span class="sxs-lookup"><span data-stu-id="be720-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be720-104">Šajā uzdevumu ceļvedī aprakstīts, kā radīt konta struktūru.</span><span class="sxs-lookup"><span data-stu-id="be720-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="be720-105">Izmantots demonstrācijas datu uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="be720-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="be720-106">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Struktūras > Konfigurēt kontu struktūras.</span><span class="sxs-lookup"><span data-stu-id="be720-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="be720-107">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="be720-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="be720-108">Laukā Konta struktūra ierakstiet nosaukumu, lai aprakstītu konta struktūras nolūku.</span><span class="sxs-lookup"><span data-stu-id="be720-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="be720-109">Laukā Apraksts ierakstiet aprakstu, lai norādītu konta struktūras nolūku.</span><span class="sxs-lookup"><span data-stu-id="be720-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="be720-110">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="be720-110">Click Create.</span></span>
6. <span data-ttu-id="be720-111">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="be720-111">Click Add segment.</span></span>
7. <span data-ttu-id="be720-112">Sarakstā Dimensijas atlasiet dimensiju, kas jāpievieno konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="be720-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="be720-113">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="be720-113">Click Add segment.</span></span>
9. <span data-ttu-id="be720-114">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="be720-114">Click Add segment.</span></span>
10. <span data-ttu-id="be720-115">Sarakstā Dimensijas atlasiet dimensiju, kas jāpievieno konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="be720-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="be720-116">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="be720-116">Click Add segment.</span></span>
12. <span data-ttu-id="be720-117">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="be720-117">Click Add segment.</span></span>
13. <span data-ttu-id="be720-118">Sarakstā Dimensijas atlasiet dimensiju, kas jāpievieno konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="be720-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="be720-119">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="be720-119">Click Add segment.</span></span>
15. <span data-ttu-id="be720-120">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="be720-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="be720-121">Piemēram, noklikšķiniet uz Galvenais konts.</span><span class="sxs-lookup"><span data-stu-id="be720-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="be720-122">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="be720-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="be720-123">Laukā Vērtība ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="be720-124">Piemēram, 600000.</span><span class="sxs-lookup"><span data-stu-id="be720-124">For example, 600000.</span></span>  
18. <span data-ttu-id="be720-125">Laukā Caur ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="be720-126">Piemēram, 699999.</span><span class="sxs-lookup"><span data-stu-id="be720-126">For example, 699999.</span></span>  
19. <span data-ttu-id="be720-127">Noklikšķiniet uz Lietot.</span><span class="sxs-lookup"><span data-stu-id="be720-127">Click Apply.</span></span>
20. <span data-ttu-id="be720-128">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="be720-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="be720-129">Piemēram, Nodaļa.</span><span class="sxs-lookup"><span data-stu-id="be720-129">For example, Department.</span></span>  
21. <span data-ttu-id="be720-130">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="be720-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="be720-131">Laukā Vērtība ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="be720-132">Piemēram, 022.</span><span class="sxs-lookup"><span data-stu-id="be720-132">For example, 022.</span></span>  
23. <span data-ttu-id="be720-133">Laukā Caur ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="be720-134">Piemēram, 031.</span><span class="sxs-lookup"><span data-stu-id="be720-134">For example, 031.</span></span>  
24. <span data-ttu-id="be720-135">Noklikšķiniet uz Pievienot jaunus kritērijus.</span><span class="sxs-lookup"><span data-stu-id="be720-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="be720-136">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="be720-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="be720-137">Laukā Vērtība ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="be720-138">Piemēram, 033.</span><span class="sxs-lookup"><span data-stu-id="be720-138">For example, 033.</span></span>  
27. <span data-ttu-id="be720-139">Laukā Caur ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="be720-140">Piemēram, 034.</span><span class="sxs-lookup"><span data-stu-id="be720-140">For example, 034.</span></span>  
28. <span data-ttu-id="be720-141">Noklikšķiniet uz Lietot.</span><span class="sxs-lookup"><span data-stu-id="be720-141">Click Apply.</span></span>
29. <span data-ttu-id="be720-142">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="be720-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="be720-143">Piemēram, Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="be720-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="be720-144">Laukā CostCenter ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="be720-145">Piemēram, 007..021.</span><span class="sxs-lookup"><span data-stu-id="be720-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="be720-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="be720-146">Click Add.</span></span>
32. <span data-ttu-id="be720-147">Laukā MainAccount ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="be720-148">Piemēram, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="be720-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="be720-149">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="be720-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="be720-150">Piemēram, Nodaļa.</span><span class="sxs-lookup"><span data-stu-id="be720-150">For example, Department.</span></span>  
34. <span data-ttu-id="be720-151">Laukā Nodaļa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="be720-152">Piemēram, 032.</span><span class="sxs-lookup"><span data-stu-id="be720-152">For example, 032.</span></span>  
35. <span data-ttu-id="be720-153">Laukā CostCenter ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="be720-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="be720-154">Piemēram, 086.</span><span class="sxs-lookup"><span data-stu-id="be720-154">For example, 086.</span></span>  
36. <span data-ttu-id="be720-155">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="be720-155">Click Validate.</span></span>
37. <span data-ttu-id="be720-156">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="be720-156">Click Activate.</span></span>
38. <span data-ttu-id="be720-157">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="be720-157">Click Activate.</span></span>

