---
title: Lean manufacturing pārsūtīšanas aktivitāšu izveide
description: Izveidojiet lean manufacturing pārsūtīšanas aktivitāti.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 04cb0afa74cb95acf4007e9292f9fb88d4c86f87
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837738"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="482e1-103">Lean manufacturing pārsūtīšanas aktivitāšu izveide</span><span class="sxs-lookup"><span data-stu-id="482e1-103">Create transfer activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="482e1-104">Izveidojiet lean manufacturing pārsūtīšanas aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="482e1-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="482e1-105">Priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="482e1-105">Prerequisites:</span></span> 

1. <span data-ttu-id="482e1-106">Ir jāizveido ražošanas plūsma un versija, kas nav aktīva.</span><span class="sxs-lookup"><span data-stu-id="482e1-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="482e1-107">Ir jāizveido avota un mērķa noliktava un novietojumi.</span><span class="sxs-lookup"><span data-stu-id="482e1-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="482e1-108">Ja nepieciešams, jāizveido uzpildīšana vai papildināta darba šūna.</span><span class="sxs-lookup"><span data-stu-id="482e1-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="482e1-109">Ražošanas plūsmas versijas atrašana</span><span class="sxs-lookup"><span data-stu-id="482e1-109">Find the production flow version</span></span>
1. <span data-ttu-id="482e1-110">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="482e1-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="482e1-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="482e1-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="482e1-112">Ņemiet vērā, ka ražošanas plūsmai jābūt versijai melnraksta statusā.</span><span class="sxs-lookup"><span data-stu-id="482e1-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="482e1-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="482e1-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="482e1-114">Jaunas aktivitātes izveide</span><span class="sxs-lookup"><span data-stu-id="482e1-114">Create a new activity</span></span>
1. <span data-ttu-id="482e1-115">Noklikšķiniet uz Aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="482e1-115">Click Activities.</span></span>
    * <span data-ttu-id="482e1-116">Nodrošiniet, lai atlasītajai ražošanas plūsmai būtu versija melnrakstā un atlasiet šo versiju.</span><span class="sxs-lookup"><span data-stu-id="482e1-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="482e1-117">Noklikšķiniet uz Izveidojiet jaunu plāna aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="482e1-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="482e1-118">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="482e1-118">Click Next.</span></span>
4. <span data-ttu-id="482e1-119">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="482e1-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="482e1-120">Laukā Aktivitātes tips atlasiet "Pārsūtīšana".</span><span class="sxs-lookup"><span data-stu-id="482e1-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="482e1-121">Laukā Apstrādes daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="482e1-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="482e1-122">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="482e1-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="482e1-123">Darba šūnu atlase</span><span class="sxs-lookup"><span data-stu-id="482e1-123">Select the Work cells</span></span>
1. <span data-ttu-id="482e1-124">Laukā Papildināšana noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="482e1-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="482e1-125">Lai izmantotu darba šūnu izvades vietu kā avota novietojumu pārsūtīšanas aktivitātē, atlasiet darba šūnu.</span><span class="sxs-lookup"><span data-stu-id="482e1-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="482e1-126">To pašu var izdarīt ar papildinātu darba šūnu, kas nosaka pārsūtīšanas aktivitātes mērķa novietojumu.</span><span class="sxs-lookup"><span data-stu-id="482e1-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="482e1-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="482e1-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="482e1-128">Krājumu atjauninājumu definēšana</span><span class="sxs-lookup"><span data-stu-id="482e1-128">Define the inventory updates</span></span>
1. <span data-ttu-id="482e1-129">Laukā Preces tips atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="482e1-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="482e1-130">Ņemiet vērā, ka pārsūtīšana nemaina preces tipu.</span><span class="sxs-lookup"><span data-stu-id="482e1-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="482e1-131">Varat pārsūtīt pabeigtās preces vai daļēji pabeigtas preces (pārsūtīšana starp divām ražošanas plūsmas aktivitātēm un, iespējams, Kanban plūsmu).</span><span class="sxs-lookup"><span data-stu-id="482e1-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="482e1-132">Pārsūtot pabeigtās preces, varat atlasīt, vai izdošanas vai saņemšanas rezultātā tiek radīta krājuma transakcija.</span><span class="sxs-lookup"><span data-stu-id="482e1-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="482e1-133">Pārsūtīšanas novietojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="482e1-133">Define the transfer locations</span></span>
1. <span data-ttu-id="482e1-134">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="482e1-134">Click Next.</span></span>
2. <span data-ttu-id="482e1-135">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="482e1-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="482e1-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="482e1-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="482e1-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="482e1-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="482e1-138">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="482e1-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="482e1-139">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="482e1-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="482e1-140">Lauka Kravas pārvadātājs atlasiet "Nosūtītājs".</span><span class="sxs-lookup"><span data-stu-id="482e1-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="482e1-141">Opcijas ietver: Kravas nosūtītājs — organizācija, kas darbina nosūtīšanas noliktavu, Saņēmējs — organizācija, kas darbina saņemšanas noliktavu, Pārvadātājs — trešās puses kreditors.</span><span class="sxs-lookup"><span data-stu-id="482e1-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="482e1-142">Ja darbinoša organizācija ir kreditors, pārsūtīšanas aktivitātei nepieciešams apakšuzņēmuma līgums.</span><span class="sxs-lookup"><span data-stu-id="482e1-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="482e1-143">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="482e1-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="482e1-144">Aktivitātes laiku definēšana</span><span class="sxs-lookup"><span data-stu-id="482e1-144">Define the activity times</span></span>
1. <span data-ttu-id="482e1-145">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="482e1-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="482e1-146">Ir nepieciešams noteikt Izpildlaiku.</span><span class="sxs-lookup"><span data-stu-id="482e1-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="482e1-147">Izpildlaiks tiek izmantots, lai aprēķinātu izmaksas un Kanban darbu caurlaides laiku.</span><span class="sxs-lookup"><span data-stu-id="482e1-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="482e1-148">Izpildlaiki netiek lietoti, lai aprēķinātu noslodzes grafiku un patēriņu, kuri tiek aprēķināti pēc cikla laika, atvasināti no ražošanas plūsmas versijas uzdevuma.</span><span class="sxs-lookup"><span data-stu-id="482e1-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="482e1-149">Laukā Laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="482e1-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="482e1-150">Laukā Mērvienība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="482e1-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="482e1-151">Atlasiet Laika vienība.</span><span class="sxs-lookup"><span data-stu-id="482e1-151">Select the Time unit.</span></span>
5. <span data-ttu-id="482e1-152">Laukā Uz daudzumu ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="482e1-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="482e1-153">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="482e1-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="482e1-154">Gaidīšanas laiki nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="482e1-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="482e1-155">Laukā Laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="482e1-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="482e1-156">Laukā Mērvienība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="482e1-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="482e1-157">Atlasiet Laika vienība.</span><span class="sxs-lookup"><span data-stu-id="482e1-157">Select the Time unit.</span></span>
10. <span data-ttu-id="482e1-158">Laukā Uz daudzumu ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="482e1-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="482e1-159">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="482e1-159">Click Next.</span></span>
12. <span data-ttu-id="482e1-160">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="482e1-160">Click Finish.</span></span>
13. <span data-ttu-id="482e1-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="482e1-161">Close the page.</span></span>

