---
title: 'Daļēja novietojuma cikla inventarizācijas procesa definēšana '
description: Ja izmantojat cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat nosūtīt faktiskās inventarizācijas operācijas, pieprasot, lai tiktu uzskaitītas tikai noteiktas preces un preču varianti, nevis visi rīcībā esošie krājumi atrašanās vietā.
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: bacad87e2b9146e08e6fe16af01356954eb90574
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2019
ms.locfileid: "373410"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="9f4d1-103">Daļēja novietojuma cikla inventarizācijas procesa definēšana </span><span class="sxs-lookup"><span data-stu-id="9f4d1-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f4d1-104">Ja izmantojat cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat nosūtīt faktiskās inventarizācijas operācijas, pieprasot, lai tiktu uzskaitītas tikai noteiktas preces un preču varianti, nevis visi rīcībā esošie krājumi atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="9f4d1-105">Filtrējot pēc atsevišķām precēm, noliktavas pārvaldnieks var samazināt pārskatīšanas pieskaitāmo daudzumu, palīdzēt izvairīties no konsolidācijas kļūdām un ietaupīt laiku.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="9f4d1-106">Parasti noliktavas pārvaldnieks veic iestatījuma uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="9f4d1-107">Šo procedūru varat izmēģināt, izmantojot USMF demonstrācijas datu uzņēmumu vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="9f4d1-108">Cikla inventarizācijas darba veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="9f4d1-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="9f4d1-109">Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="9f4d1-110">Laukā Darba pasūtījuma veids atlasiet "Cycle counting".</span><span class="sxs-lookup"><span data-stu-id="9f4d1-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="9f4d1-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-111">Click New.</span></span>
4. <span data-ttu-id="9f4d1-112">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="9f4d1-113">Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="9f4d1-114">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="9f4d1-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="9f4d1-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9f4d1-116">Laukā Darba veidne ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="9f4d1-117">Laukā Darba veidnes apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="9f4d1-118">Laukā Darba kopas ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="9f4d1-119">Laukā Darba prioritāte ievadiet numuru.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="9f4d1-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-120">Click Save.</span></span>
11. <span data-ttu-id="9f4d1-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-121">Click New.</span></span>
12. <span data-ttu-id="9f4d1-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="9f4d1-123">Laukā Darba veids atlasiet "Counting".</span><span class="sxs-lookup"><span data-stu-id="9f4d1-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="9f4d1-124">Laukā Darba klases ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="9f4d1-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-125">Click Save.</span></span>
16. <span data-ttu-id="9f4d1-126">Noklikšķiniet uz Darba rindas pārtraukumi.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="9f4d1-127">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-127">Click New.</span></span>
18. <span data-ttu-id="9f4d1-128">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="9f4d1-129">Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="9f4d1-130">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="9f4d1-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="9f4d1-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-131">Click Save.</span></span>
20. <span data-ttu-id="9f4d1-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-132">Close the page.</span></span>
21. <span data-ttu-id="9f4d1-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="9f4d1-134">Cikla inventarizācijas plāna izveide</span><span class="sxs-lookup"><span data-stu-id="9f4d1-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="9f4d1-135">Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas plāni.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="9f4d1-136">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-136">Click New.</span></span>
3. <span data-ttu-id="9f4d1-137">Ierakstiet vērtību laukā Cikla inventarizācijas plāna ID.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="9f4d1-138">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9f4d1-139">Laukā Maksimālais cikla inventarizāciju skaits ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="9f4d1-140">Laukā Darba veidne, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="9f4d1-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-141">Click New.</span></span>
8. <span data-ttu-id="9f4d1-142">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="9f4d1-143">Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="9f4d1-144">Vērtībai jābūt lielākai par 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="9f4d1-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="9f4d1-145">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="9f4d1-146">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-146">Click Save.</span></span>
11. <span data-ttu-id="9f4d1-147">Noklikšķiniet uz Definēt preces vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-147">Click Define product query.</span></span>
12. <span data-ttu-id="9f4d1-148">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="9f4d1-149">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="9f4d1-150">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-150">Click OK.</span></span>
15. <span data-ttu-id="9f4d1-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9f4d1-151">Close the page.</span></span>

