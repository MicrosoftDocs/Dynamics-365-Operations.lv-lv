---
title: MK rindas notikumu Kanban kārtulas izveide
description: Šis uzdevums fokusējas nepieciešamajam iestatījumam, lai izveidotu notikuma kanban nosacījumu, lai nodrošinātu piegādes ražošanas MK rindām, jauktā racionālā un klasiskā ražošanas vidē.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a4252548fd030f2a044436ff607da5125d2854
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "337099"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="a203b-103">MK rindas notikumu Kanban kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="a203b-103">Create a BOM line event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a203b-104">Šis uzdevums fokusējas nepieciešamajam iestatījumam, lai izveidotu notikuma kanban nosacījumu, lai nodrošinātu piegādes ražošanas MK rindām, jauktā racionālā un klasiskā ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="a203b-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="a203b-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="a203b-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="a203b-106">Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jaunas vai modificētas preces ražošanai.</span><span class="sxs-lookup"><span data-stu-id="a203b-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="a203b-107">Izveidot jaunu Kanban nosacījumu</span><span class="sxs-lookup"><span data-stu-id="a203b-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="a203b-108">Dodieties uz Ražošanas kontrole > Periodiskie uzdevumi > Kanban daudzuma aprēķins > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="a203b-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="a203b-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a203b-109">Click New.</span></span>
3. <span data-ttu-id="a203b-110">Laukā Veids, atlasiet 'Atvilkums'.</span><span class="sxs-lookup"><span data-stu-id="a203b-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="a203b-111">Atvilkuma tips tiek izmantots, lai izveidotu pārsūtīšanas Kanban.</span><span class="sxs-lookup"><span data-stu-id="a203b-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="a203b-112">Laukā Papildināšanas stratēģija atlasiet "Notikums".</span><span class="sxs-lookup"><span data-stu-id="a203b-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="a203b-113">Notikumu stratēģija tiek atlasīta, lai izveidotu Kanban pārsūtīšanu, pamatojoties uz notikumu.</span><span class="sxs-lookup"><span data-stu-id="a203b-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="a203b-114">Vēlāk, uzdevuma rokasgrāmatā, mēs to aktivizēsim, novērtējot ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a203b-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="a203b-115">Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a203b-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="a203b-116">Ievadiet vai Atlasiet ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="a203b-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="a203b-117">Šai pārsūtīšanas aktivitātei ir saņemšanas (izdošana) noliktava un atrašanās vieta 12, kas nozīmē, ka materiāls tiks pārvietots uz atrašanās vietu noliktavā 12.</span><span class="sxs-lookup"><span data-stu-id="a203b-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="a203b-118">Izvērsiet sadaļu Detalizēti.</span><span class="sxs-lookup"><span data-stu-id="a203b-118">Expand the Details section.</span></span>
7. <span data-ttu-id="a203b-119">Laukā Prece, ievadiet vai atlasiet M0001.</span><span class="sxs-lookup"><span data-stu-id="a203b-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="a203b-120">Izvērsiet sadali Notikumi.</span><span class="sxs-lookup"><span data-stu-id="a203b-120">Expand the Events section.</span></span>
9. <span data-ttu-id="a203b-121">Laukā MK rinda, atlasiet "Automātisks".</span><span class="sxs-lookup"><span data-stu-id="a203b-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="a203b-122">Ar MK rindas notikuma lauku iestatītu uz Automātisks, tiks izveidots kanban, lai apmierinātu materiālu vajadzības ražošanas pasūtījuma MK rindām.</span><span class="sxs-lookup"><span data-stu-id="a203b-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="a203b-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a203b-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="a203b-124">Izveidojiet un modificējiet jaunu ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a203b-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="a203b-125">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a203b-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="a203b-126">Noklikšķiniet uz Jauns ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a203b-126">Click New production order.</span></span>
3. <span data-ttu-id="a203b-127">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a203b-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a203b-128">Ievadiet vai atlasiet 'L0001'.</span><span class="sxs-lookup"><span data-stu-id="a203b-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="a203b-129">Mēs izmantojam krājumu L0001, jo krājums M0001 ir iekļauts MK krājumam L0001.</span><span class="sxs-lookup"><span data-stu-id="a203b-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="a203b-130">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="a203b-130">Click Create.</span></span>
5. <span data-ttu-id="a203b-131">Sarakstā noklikšķiniet uz saites rindā priekš L0001</span><span class="sxs-lookup"><span data-stu-id="a203b-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="a203b-132">Noklikšķiniet uz MK.</span><span class="sxs-lookup"><span data-stu-id="a203b-132">Click BOM.</span></span>
7. <span data-ttu-id="a203b-133">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a203b-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a203b-134">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="a203b-134">Click Edit.</span></span>
9. <span data-ttu-id="a203b-135">Laukā Rindas tips atlasiet “Pieprasīta piegāde”.</span><span class="sxs-lookup"><span data-stu-id="a203b-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="a203b-136">Pieprasīta piegāde tiek atlasīta, lai aktivizētu kanban piegādes izveidi.</span><span class="sxs-lookup"><span data-stu-id="a203b-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="a203b-137">Laukā Resursu patēriņš, atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="a203b-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="a203b-138">Notīrot izvēles rūtiņu Resursu patēriņš, ļauj mums mainīt noliktavu.</span><span class="sxs-lookup"><span data-stu-id="a203b-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="a203b-139">Izvērsiet sadaļu Krājuma dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a203b-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="a203b-140">Laukā Noliktava ierakstiet "12".</span><span class="sxs-lookup"><span data-stu-id="a203b-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="a203b-141">Noliktava ir iestatīta uz 12, jo šī ir ražojumu noliktava atvilkuma aktivitātei.</span><span class="sxs-lookup"><span data-stu-id="a203b-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="a203b-142">Laukā Atrašanās vieta, ierakstiet "12".</span><span class="sxs-lookup"><span data-stu-id="a203b-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="a203b-143">Atrašanās vieta ir iestatīta uz 12, jo šī ir atvilkuma aktivitātes atrašanās vieta.</span><span class="sxs-lookup"><span data-stu-id="a203b-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="a203b-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a203b-144">Close the page.</span></span>
15. <span data-ttu-id="a203b-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a203b-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="a203b-146">Novērtējiet ražošanas pasūtījumu, un skatiet izveidoto kanban</span><span class="sxs-lookup"><span data-stu-id="a203b-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="a203b-147">Noklikšķiniet uz Novērtējums.</span><span class="sxs-lookup"><span data-stu-id="a203b-147">Click Estimate.</span></span>
    * <span data-ttu-id="a203b-148">Ražošanas pasūtījuma novērtēšana aktivizēs saistītā kanban izveidi, lai nodrošinātu krājumu M0001.</span><span class="sxs-lookup"><span data-stu-id="a203b-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="a203b-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a203b-149">Click OK.</span></span>
3. <span data-ttu-id="a203b-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a203b-150">Close the page.</span></span>
4. <span data-ttu-id="a203b-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a203b-151">Close the page.</span></span>
5. <span data-ttu-id="a203b-152">Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="a203b-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="a203b-153">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a203b-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a203b-154">Atlasiet notikumu, ko kanban nosacījums izveidoja krājumam M0001.</span><span class="sxs-lookup"><span data-stu-id="a203b-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="a203b-155">Izvērsiet sadaļu Vairāki Kanban.</span><span class="sxs-lookup"><span data-stu-id="a203b-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="a203b-156">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a203b-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a203b-157">Ņemiet vērā, kanban, kas tika izveidots M0001 nodrošināšanai, prognozējamajam ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a203b-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="a203b-158">Šis ir pēdējais solis!</span><span class="sxs-lookup"><span data-stu-id="a203b-158">This is the last step!</span></span>  

