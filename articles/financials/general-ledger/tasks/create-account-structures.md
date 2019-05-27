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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571286"
---
# <a name="create-account-structures"></a><span data-ttu-id="cda55-103">Kontu struktūru izveide</span><span class="sxs-lookup"><span data-stu-id="cda55-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cda55-104">Šajā uzdevumu ceļvedī aprakstīts, kā radīt konta struktūru.</span><span class="sxs-lookup"><span data-stu-id="cda55-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="cda55-105">Izmantots demonstrācijas datu uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="cda55-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="cda55-106">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Struktūras > Konfigurēt kontu struktūras.</span><span class="sxs-lookup"><span data-stu-id="cda55-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="cda55-107">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="cda55-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="cda55-108">Laukā Konta struktūra ierakstiet nosaukumu, lai aprakstītu konta struktūras nolūku.</span><span class="sxs-lookup"><span data-stu-id="cda55-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="cda55-109">Laukā Apraksts ierakstiet aprakstu, lai norādītu konta struktūras nolūku.</span><span class="sxs-lookup"><span data-stu-id="cda55-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="cda55-110">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="cda55-110">Click Create.</span></span>
6. <span data-ttu-id="cda55-111">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="cda55-111">Click Add segment.</span></span>
7. <span data-ttu-id="cda55-112">Sarakstā Dimensijas atlasiet dimensiju, kas jāpievieno konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="cda55-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="cda55-113">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="cda55-113">Click Add segment.</span></span>
9. <span data-ttu-id="cda55-114">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="cda55-114">Click Add segment.</span></span>
10. <span data-ttu-id="cda55-115">Sarakstā Dimensijas atlasiet dimensiju, kas jāpievieno konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="cda55-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="cda55-116">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="cda55-116">Click Add segment.</span></span>
12. <span data-ttu-id="cda55-117">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="cda55-117">Click Add segment.</span></span>
13. <span data-ttu-id="cda55-118">Sarakstā Dimensijas atlasiet dimensiju, kas jāpievieno konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="cda55-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="cda55-119">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="cda55-119">Click Add segment.</span></span>
15. <span data-ttu-id="cda55-120">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="cda55-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="cda55-121">Piemēram, noklikšķiniet uz Galvenais konts.</span><span class="sxs-lookup"><span data-stu-id="cda55-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="cda55-122">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="cda55-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="cda55-123">Laukā Vērtība ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="cda55-124">Piemēram, 600000.</span><span class="sxs-lookup"><span data-stu-id="cda55-124">For example, 600000.</span></span>  
18. <span data-ttu-id="cda55-125">Laukā Caur ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="cda55-126">Piemēram, 699999.</span><span class="sxs-lookup"><span data-stu-id="cda55-126">For example, 699999.</span></span>  
19. <span data-ttu-id="cda55-127">Noklikšķiniet uz Lietot.</span><span class="sxs-lookup"><span data-stu-id="cda55-127">Click Apply.</span></span>
20. <span data-ttu-id="cda55-128">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="cda55-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="cda55-129">Piemēram, Nodaļa.</span><span class="sxs-lookup"><span data-stu-id="cda55-129">For example, Department.</span></span>  
21. <span data-ttu-id="cda55-130">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="cda55-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="cda55-131">Laukā Vērtība ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="cda55-132">Piemēram, 022.</span><span class="sxs-lookup"><span data-stu-id="cda55-132">For example, 022.</span></span>  
23. <span data-ttu-id="cda55-133">Laukā Caur ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="cda55-134">Piemēram, 031.</span><span class="sxs-lookup"><span data-stu-id="cda55-134">For example, 031.</span></span>  
24. <span data-ttu-id="cda55-135">Noklikšķiniet uz Pievienot jaunus kritērijus.</span><span class="sxs-lookup"><span data-stu-id="cda55-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="cda55-136">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="cda55-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="cda55-137">Laukā Vērtība ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="cda55-138">Piemēram, 033.</span><span class="sxs-lookup"><span data-stu-id="cda55-138">For example, 033.</span></span>  
27. <span data-ttu-id="cda55-139">Laukā Caur ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="cda55-140">Piemēram, 034.</span><span class="sxs-lookup"><span data-stu-id="cda55-140">For example, 034.</span></span>  
28. <span data-ttu-id="cda55-141">Noklikšķiniet uz Lietot.</span><span class="sxs-lookup"><span data-stu-id="cda55-141">Click Apply.</span></span>
29. <span data-ttu-id="cda55-142">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="cda55-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="cda55-143">Piemēram, Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="cda55-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="cda55-144">Laukā CostCenter ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="cda55-145">Piemēram, 007..021.</span><span class="sxs-lookup"><span data-stu-id="cda55-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="cda55-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="cda55-146">Click Add.</span></span>
32. <span data-ttu-id="cda55-147">Laukā MainAccount ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="cda55-148">Piemēram, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="cda55-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="cda55-149">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="cda55-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="cda55-150">Piemēram, Nodaļa.</span><span class="sxs-lookup"><span data-stu-id="cda55-150">For example, Department.</span></span>  
34. <span data-ttu-id="cda55-151">Laukā Nodaļa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="cda55-152">Piemēram, 032.</span><span class="sxs-lookup"><span data-stu-id="cda55-152">For example, 032.</span></span>  
35. <span data-ttu-id="cda55-153">Laukā CostCenter ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda55-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="cda55-154">Piemēram, 086.</span><span class="sxs-lookup"><span data-stu-id="cda55-154">For example, 086.</span></span>  
36. <span data-ttu-id="cda55-155">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="cda55-155">Click Validate.</span></span>
37. <span data-ttu-id="cda55-156">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="cda55-156">Click Activate.</span></span>
38. <span data-ttu-id="cda55-157">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="cda55-157">Click Activate.</span></span>

