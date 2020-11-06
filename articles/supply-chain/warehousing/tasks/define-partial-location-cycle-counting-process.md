---
title: 'Daļēja novietojuma cikla inventarizācijas procesa definēšana '
description: Ja izmantojat cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat nosūtīt faktiskās inventarizācijas operācijas, pieprasot, lai tiktu uzskaitītas tikai noteiktas preces un preču varianti, nevis visi rīcībā esošie krājumi atrašanās vietā.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39a256a5a88a6d70373d6e23f1f380da6791f418
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016082"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="a5cc0-103">Daļēja novietojuma cikla inventarizācijas procesa definēšana </span><span class="sxs-lookup"><span data-stu-id="a5cc0-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5cc0-104">Ja izmantojat cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat nosūtīt faktiskās inventarizācijas operācijas, pieprasot, lai tiktu uzskaitītas tikai noteiktas preces un preču varianti, nevis visi rīcībā esošie krājumi atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="a5cc0-105">Filtrējot pēc atsevišķām precēm, noliktavas pārvaldnieks var samazināt pārskatīšanas pieskaitāmo daudzumu, palīdzēt izvairīties no konsolidācijas kļūdām un ietaupīt laiku.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="a5cc0-106">Parasti noliktavas pārvaldnieks veic iestatījuma uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="a5cc0-107">Šo procedūru varat izmēģināt, izmantojot USMF demonstrācijas datu uzņēmumu vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="a5cc0-108">Cikla inventarizācijas darba veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="a5cc0-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="a5cc0-109">Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="a5cc0-110">Laukā Darba pasūtījuma veids atlasiet "Cycle counting".</span><span class="sxs-lookup"><span data-stu-id="a5cc0-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="a5cc0-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-111">Click New.</span></span>
4. <span data-ttu-id="a5cc0-112">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="a5cc0-113">Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="a5cc0-114">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="a5cc0-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="a5cc0-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="a5cc0-116">Laukā Darba veidne ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="a5cc0-117">Laukā Darba veidnes apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="a5cc0-118">Laukā Darba kopas ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="a5cc0-119">Laukā Darba prioritāte ievadiet numuru.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="a5cc0-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-120">Click Save.</span></span>
11. <span data-ttu-id="a5cc0-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-121">Click New.</span></span>
12. <span data-ttu-id="a5cc0-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="a5cc0-123">Laukā Darba veids atlasiet "Counting".</span><span class="sxs-lookup"><span data-stu-id="a5cc0-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="a5cc0-124">Laukā Darba klases ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="a5cc0-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-125">Click Save.</span></span>
16. <span data-ttu-id="a5cc0-126">Noklikšķiniet uz Darba rindas pārtraukumi.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="a5cc0-127">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-127">Click New.</span></span>
18. <span data-ttu-id="a5cc0-128">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="a5cc0-129">Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="a5cc0-130">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="a5cc0-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="a5cc0-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-131">Click Save.</span></span>
20. <span data-ttu-id="a5cc0-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-132">Close the page.</span></span>
21. <span data-ttu-id="a5cc0-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="a5cc0-134">Cikla inventarizācijas plāna izveide</span><span class="sxs-lookup"><span data-stu-id="a5cc0-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="a5cc0-135">Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas plāni.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="a5cc0-136">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-136">Click New.</span></span>
3. <span data-ttu-id="a5cc0-137">Ierakstiet vērtību laukā Cikla inventarizācijas plāna ID.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="a5cc0-138">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a5cc0-139">Laukā Maksimālais cikla inventarizāciju skaits ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="a5cc0-140">Laukā Darba veidne, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="a5cc0-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-141">Click New.</span></span>
8. <span data-ttu-id="a5cc0-142">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="a5cc0-143">Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="a5cc0-144">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="a5cc0-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="a5cc0-145">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="a5cc0-146">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-146">Click Save.</span></span>
11. <span data-ttu-id="a5cc0-147">Noklikšķiniet uz Definēt preces vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-147">Click Define product query.</span></span>
12. <span data-ttu-id="a5cc0-148">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="a5cc0-149">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="a5cc0-150">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-150">Click OK.</span></span>
15. <span data-ttu-id="a5cc0-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a5cc0-151">Close the page.</span></span>

