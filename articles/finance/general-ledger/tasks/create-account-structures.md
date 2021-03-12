---
title: Kontu struktūru izveide
description: Šajā uzdevumu ceļvedī aprakstīts, kā radīt konta struktūru.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a8df7d7d9c4555bf46ac1cc3f71695837b1369b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968587"
---
# <a name="create-account-structures"></a><span data-ttu-id="045da-103">Kontu struktūru izveide</span><span class="sxs-lookup"><span data-stu-id="045da-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="045da-104">Šajā uzdevumu ceļvedī aprakstīts, kā radīt konta struktūru.</span><span class="sxs-lookup"><span data-stu-id="045da-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="045da-105">Izmantots demonstrācijas datu uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="045da-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="045da-106">Ejiet uz **Navigācijas rūts > Moduļi > Virsgrāmata > Kontu diagramma > Struktūras > Konta struktūru konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="045da-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="045da-107">**Darbību rūtī** noklikšķiniet uz **Jauna**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="045da-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="045da-108">Laukā **Konta struktūra** ierakstiet vārdu, kas apraksta konta struktūras nolūku.</span><span class="sxs-lookup"><span data-stu-id="045da-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="045da-109">Laukā **Apraksts** ierakstiet aprakstu, kas norāda konta struktūras nolūku.</span><span class="sxs-lookup"><span data-stu-id="045da-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="045da-110">Noklikšķiniet uz **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="045da-110">Click **Create**.</span></span>
6. <span data-ttu-id="045da-111">Lauk­ā **Segmenti un atļautās vērtības** klikšķiniet uz **Pievienot segmentu**.</span><span class="sxs-lookup"><span data-stu-id="045da-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="045da-112">Izmēru sarakstā atlasiet izmēru, ko pievienot konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="045da-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="045da-113">Saraksta beigās klikšķiniet uz **Pievienot segmentu**.</span><span class="sxs-lookup"><span data-stu-id="045da-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="045da-114">Atbilstoši vajadzībām vēlreiz veiciet 6.–9. darbību.</span><span class="sxs-lookup"><span data-stu-id="045da-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="045da-115">Sadaļā **Atļaut vērtības detaļas** atlasiet segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="045da-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="045da-116">Piemēram, klikšķiniet uz lauka **Galvenais konts**.</span><span class="sxs-lookup"><span data-stu-id="045da-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="045da-117">Laukā **Operators** atlasiet opciju, piemēram, „starp” vai „ietver”.</span><span class="sxs-lookup"><span data-stu-id="045da-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="045da-118">Laukā **Vērtība** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="045da-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="045da-119">Piemēram, 600000.</span><span class="sxs-lookup"><span data-stu-id="045da-119">For example, 600000.</span></span>  
13. <span data-ttu-id="045da-120">Laukā **Caur** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="045da-120">In the **through** field, type a value.</span></span> <span data-ttu-id="045da-121">Piemēram, 699999.</span><span class="sxs-lookup"><span data-stu-id="045da-121">For example, 699999.</span></span>  
14. <span data-ttu-id="045da-122">Sadaļā **Atļautās vērtības detaļas** klikšķiniet uz **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="045da-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="045da-123">Atbilstoši vajadzībām vēlreiz veiciet 10.–15. darbību.</span><span class="sxs-lookup"><span data-stu-id="045da-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="045da-124">Sadaļā **Atļautās vērtības detaļas** klikšķiniet uz **Pievienot jaunus kritērijus**.</span><span class="sxs-lookup"><span data-stu-id="045da-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="045da-125">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="045da-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="045da-126">Laukā **Vērtība** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="045da-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="045da-127">Piemēram, 033.</span><span class="sxs-lookup"><span data-stu-id="045da-127">For example, 033.</span></span>  
19. <span data-ttu-id="045da-128">Laukā **Caur** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="045da-128">In the **through** field, type a value.</span></span> <span data-ttu-id="045da-129">Piemēram, 034.</span><span class="sxs-lookup"><span data-stu-id="045da-129">For example, 034.</span></span>  
20. <span data-ttu-id="045da-130">Noklikšķiniet uz **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="045da-130">Click **Apply**.</span></span>
21. <span data-ttu-id="045da-131">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="045da-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="045da-132">Piemēram, Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="045da-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="045da-133">Laukā **IzmaksuCentrs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="045da-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="045da-134">Piemēram, 007..021.</span><span class="sxs-lookup"><span data-stu-id="045da-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="045da-135">Lauk­ā **Segmenti un atļautās vērtības** klikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="045da-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="045da-136">Laukā **GalvenaisKonts** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="045da-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="045da-137">Piemēram, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="045da-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="045da-138">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="045da-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="045da-139">Piemēram, Nodaļa.</span><span class="sxs-lookup"><span data-stu-id="045da-139">For example, Department.</span></span>  
26. <span data-ttu-id="045da-140">Laukā Nodaļa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="045da-140">In the Department field, type a value.</span></span> <span data-ttu-id="045da-141">Piemēram, 032.</span><span class="sxs-lookup"><span data-stu-id="045da-141">For example, 032.</span></span>  
27. <span data-ttu-id="045da-142">Laukā IzmaksuCentrs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="045da-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="045da-143">Piemēram, 086.</span><span class="sxs-lookup"><span data-stu-id="045da-143">For example, 086.</span></span>  
28. <span data-ttu-id="045da-144">**Darbību rūtī** noklikšķiniet uz **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="045da-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="045da-145">**Darbību rūtī** noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="045da-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="045da-146">Noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="045da-146">Click **Activate**.</span></span>

