---
title: Lean manufacturing procesa aktivitāšu izveide
description: Izveidojiet lean manufacturing procesa aktivitāti.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fa4d7fe2345d54faf405086a1e1bef599265470b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "345218"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="9b6e1-103">Lean manufacturing procesa aktivitāšu izveide</span><span class="sxs-lookup"><span data-stu-id="9b6e1-103">Create process activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b6e1-104">Izveidojiet lean manufacturing procesa aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="9b6e1-105">Priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="9b6e1-105">Prerequisites:</span></span> 

1. <span data-ttu-id="9b6e1-106">Ir jāizveido ražošanas plūsma un versija, kas nav aktīva.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="9b6e1-107">Ir jāizveido darba šūna.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="9b6e1-108">Ražošanas plūsmas versijas atrašana</span><span class="sxs-lookup"><span data-stu-id="9b6e1-108">Find the production flow version</span></span>
1. <span data-ttu-id="9b6e1-109">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="9b6e1-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9b6e1-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="9b6e1-112">Jaunas aktivitātes izveide</span><span class="sxs-lookup"><span data-stu-id="9b6e1-112">Create a new activity</span></span>
1. <span data-ttu-id="9b6e1-113">Noklikšķiniet uz Aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-113">Click Activities.</span></span>
    * <span data-ttu-id="9b6e1-114">Nodrošiniet, lai atlasītajai ražošanas plūsmai būtu versija melnrakstā un atlasiet šo versiju.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="9b6e1-115">Noklikšķiniet uz Izveidojiet jaunu plāna aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="9b6e1-116">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-116">Click Next.</span></span>
4. <span data-ttu-id="9b6e1-117">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9b6e1-118">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9b6e1-119">Ņemiet vērā, ka dotās ražošanas plūsmas nosaukumam jābūt unikālam visās versijās.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="9b6e1-120">Laukā Apstrādes daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="9b6e1-121">Ņemiet vērā, ka neatkarīgi no tā, kāds darba apjoms tiks apstrādāts, tas ir minimālais daudzums uz darbu, lai aprēķinātu darbaspēka izmaksas.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="9b6e1-122">Ja darbu daudzumi atšķiras no šī daudzuma, tiks izveidota darbaspēka izmaksu novirze.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="9b6e1-123">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="9b6e1-124">Darba šūnas atlase</span><span class="sxs-lookup"><span data-stu-id="9b6e1-124">Select the work cell</span></span>
1. <span data-ttu-id="9b6e1-125">Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="9b6e1-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="9b6e1-127">Krājumu atjauninājumu definēšana</span><span class="sxs-lookup"><span data-stu-id="9b6e1-127">Define the inventory updates</span></span>
1. <span data-ttu-id="9b6e1-128">Atzīmējiet vai notīriet izvēles rūtiņu Atjauniniet rīcībā esošo krājumu saņemšanu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="9b6e1-129">Ja Atjauniniet rīcībā esošos krājumus = Nē, varat definēt aktivitāti, lai saņemtu daļēji pabeigtu preci (aktivitāte nesasniedz nākamo MK līmeni).</span><span class="sxs-lookup"><span data-stu-id="9b6e1-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="9b6e1-130">Varat arī atlasīt patērēt daļēji pabeigtās preces.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="9b6e1-131">Izdošanas aktivitāšu definēšana</span><span class="sxs-lookup"><span data-stu-id="9b6e1-131">Define the picking activities</span></span>
1. <span data-ttu-id="9b6e1-132">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-132">Click Next.</span></span>
2. <span data-ttu-id="9b6e1-133">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9b6e1-134">Atlasītās darba šūnas ievades vietai tiek izveidota noklusējuma izdošanas aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="9b6e1-135">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-135">Click Add.</span></span>
    * <span data-ttu-id="9b6e1-136">Varat izveidot papildu izdošanas aktivitātes īpašām precēm, kas nav izveidotas darba šūnu ievades aktivitātē.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="9b6e1-137">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9b6e1-138">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="9b6e1-139">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9b6e1-140">Ar šo definīciju, visi aktivitātes patērētie materiāli tiek izdoti no noklusējuma ievades noliktavas un novietojuma, izņemot krājumu, kas ir definēts otrajā izdošanas aktivitātē.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="9b6e1-141">Šis krājums tiks izdots no citas noliktavas un novietojuma.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="9b6e1-142">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9b6e1-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9b6e1-144">Atzīmējiet vai notīriet izvēles rūtiņu Reģistrēt brāķi.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="9b6e1-145">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="9b6e1-146">Aktivitātes laiku definēšana</span><span class="sxs-lookup"><span data-stu-id="9b6e1-146">Define the activity times</span></span>
1. <span data-ttu-id="9b6e1-147">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9b6e1-148">Ir nepieciešams noteikt Izpildlaiku.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="9b6e1-149">Izpildlaiks tiek izmantots, lai aprēķinātu izmaksas un Kanban darbu caurlaides laiku.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="9b6e1-150">Izpildlaiki netiek lietoti, lai aprēķinātu noslodzes grafiku un patēriņu, tie tiek aprēķināti pēc cikla laika, atvasināti no ražošanas plūsmas versijas uzdevuma.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="9b6e1-151">Laukā Laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="9b6e1-152">Laukā Mērvienība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="9b6e1-153">Atlasiet Laika vienība.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-153">Select the Time unit.</span></span>
5. <span data-ttu-id="9b6e1-154">Laukā Uz daudzumu ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="9b6e1-155">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9b6e1-156">Gaidīšanas laiki nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="9b6e1-157">Laukā Laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="9b6e1-158">Laukā Mērvienība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="9b6e1-159">Atlasiet Laika vienība.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-159">Select the Time unit.</span></span>
10. <span data-ttu-id="9b6e1-160">Laukā Uz daudzumu ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="9b6e1-161">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-161">Click Next.</span></span>
12. <span data-ttu-id="9b6e1-162">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-162">Click Finish.</span></span>
13. <span data-ttu-id="9b6e1-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9b6e1-163">Close the page.</span></span>

