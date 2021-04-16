---
title: Kontu struktūru izveide
description: Šajā uzdevumu ceļvedī aprakstīts, kā radīt konta struktūru.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aece2b79633802d28ba3b4fd8b51788e26c17a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815168"
---
# <a name="create-account-structures"></a><span data-ttu-id="fc9b3-103">Kontu struktūru izveide</span><span class="sxs-lookup"><span data-stu-id="fc9b3-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc9b3-104">Šajā uzdevumu ceļvedī aprakstīts, kā radīt konta struktūru.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="fc9b3-105">Izmantots demonstrācijas datu uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="fc9b3-106">Ejiet uz **Navigācijas rūts > Moduļi > Virsgrāmata > Kontu diagramma > Struktūras > Konta struktūru konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="fc9b3-107">**Darbību rūtī** noklikšķiniet uz **Jauna**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="fc9b3-108">Laukā **Konta struktūra** ierakstiet vārdu, kas apraksta konta struktūras nolūku.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="fc9b3-109">Laukā **Apraksts** ierakstiet aprakstu, kas norāda konta struktūras nolūku.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="fc9b3-110">Noklikšķiniet uz **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-110">Click **Create**.</span></span>
6. <span data-ttu-id="fc9b3-111">Lauk­ā **Segmenti un atļautās vērtības** klikšķiniet uz **Pievienot segmentu**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="fc9b3-112">Izmēru sarakstā atlasiet izmēru, ko pievienot konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="fc9b3-113">Saraksta beigās klikšķiniet uz **Pievienot segmentu**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="fc9b3-114">Atbilstoši vajadzībām vēlreiz veiciet 6.–9. darbību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="fc9b3-115">Sadaļā **Atļaut vērtības detaļas** atlasiet segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="fc9b3-116">Piemēram, klikšķiniet uz lauka **Galvenais konts**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="fc9b3-117">Laukā **Operators** atlasiet opciju, piemēram, „starp” vai „ietver”.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="fc9b3-118">Laukā **Vērtība** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="fc9b3-119">Piemēram, 600000.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-119">For example, 600000.</span></span>  
13. <span data-ttu-id="fc9b3-120">Laukā **Caur** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-120">In the **through** field, type a value.</span></span> <span data-ttu-id="fc9b3-121">Piemēram, 699999.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-121">For example, 699999.</span></span>  
14. <span data-ttu-id="fc9b3-122">Sadaļā **Atļautās vērtības detaļas** klikšķiniet uz **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="fc9b3-123">Atbilstoši vajadzībām vēlreiz veiciet 10.–15. darbību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="fc9b3-124">Sadaļā **Atļautās vērtības detaļas** klikšķiniet uz **Pievienot jaunus kritērijus**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="fc9b3-125">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="fc9b3-126">Laukā **Vērtība** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="fc9b3-127">Piemēram, 033.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-127">For example, 033.</span></span>  
19. <span data-ttu-id="fc9b3-128">Laukā **Caur** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-128">In the **through** field, type a value.</span></span> <span data-ttu-id="fc9b3-129">Piemēram, 034.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-129">For example, 034.</span></span>  
20. <span data-ttu-id="fc9b3-130">Noklikšķiniet uz **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-130">Click **Apply**.</span></span>
21. <span data-ttu-id="fc9b3-131">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="fc9b3-132">Piemēram, Izmaksu centrs.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="fc9b3-133">Laukā **IzmaksuCentrs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="fc9b3-134">Piemēram, 007..021.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="fc9b3-135">Lauk­ā **Segmenti un atļautās vērtības** klikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="fc9b3-136">Laukā **GalvenaisKonts** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="fc9b3-137">Piemēram, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="fc9b3-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="fc9b3-138">Režģī Izvēlieties segmentu, lai rediģētu atļautās vērtības.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="fc9b3-139">Piemēram, Nodaļa.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-139">For example, Department.</span></span>  
26. <span data-ttu-id="fc9b3-140">Laukā Nodaļa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-140">In the Department field, type a value.</span></span> <span data-ttu-id="fc9b3-141">Piemēram, 032.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-141">For example, 032.</span></span>  
27. <span data-ttu-id="fc9b3-142">Laukā IzmaksuCentrs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="fc9b3-143">Piemēram, 086.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-143">For example, 086.</span></span>  
28. <span data-ttu-id="fc9b3-144">**Darbību rūtī** noklikšķiniet uz **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="fc9b3-145">**Darbību rūtī** noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="fc9b3-146">Noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="fc9b3-146">Click **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]