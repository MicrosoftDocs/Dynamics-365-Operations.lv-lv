--- 
title: "Kanban kārtulas izveide, izmantojot minimālo krājumu notikumu"
description: "Šī procedūra koncentrējas uz iestatīšanu, kas ir nepieciešama, lai izveidotu Kanban nosacījumu, izmantojot minimālo krājumu notikumu, tādējādi nodrošinot, ka konkrētā novietojumā vienmēr ir pieejama konkrēta prece."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: b325f659ea026797205cde8408c2fb3de27bb48d
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="094d4-103">Kanban kārtulas izveide, izmantojot minimālo krājumu notikumu</span><span class="sxs-lookup"><span data-stu-id="094d4-103">Create a kanban rule using a minimum stock event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="094d4-104">Šī procedūra koncentrējas uz iestatīšanu, kas ir nepieciešama, lai izveidotu Kanban nosacījumu, izmantojot minimālo krājumu notikumu, tādējādi nodrošinot, ka konkrētā novietojumā vienmēr ir pieejama konkrēta prece.</span><span class="sxs-lookup"><span data-stu-id="094d4-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="094d4-105">Kanban nosacījums tiek izveidots, lai materiālu pārsūtītu uz novietojumu, kad krājumu līmenis kļūst mazāks nekā 200 gab.</span><span class="sxs-lookup"><span data-stu-id="094d4-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="094d4-106">Palaižot pieprasījuma notikuma apstrādi, tiek izveidoti nepieciešamie Kanban.</span><span class="sxs-lookup"><span data-stu-id="094d4-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="094d4-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="094d4-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="094d4-108">Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad viņi sagatavo jaunas vai modificētas preces ražošanu racionālā vidē.</span><span class="sxs-lookup"><span data-stu-id="094d4-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="094d4-109">Izveidot jaunu Kanban nosacījumu</span><span class="sxs-lookup"><span data-stu-id="094d4-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="094d4-110">Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="094d4-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="094d4-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="094d4-111">Click New.</span></span>
3. <span data-ttu-id="094d4-112">Laukā Veids, atlasiet 'Atvilkums'.</span><span class="sxs-lookup"><span data-stu-id="094d4-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="094d4-113">Šis tips tiek izmantots, lai izveidotu pārsūtīšanas Kanban.</span><span class="sxs-lookup"><span data-stu-id="094d4-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="094d4-114">Laukā Papildināšanas stratēģija atlasiet "Notikums".</span><span class="sxs-lookup"><span data-stu-id="094d4-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="094d4-115">Notikumu stratēģija tiek izmantota, lai izveidotu pārsūtīšanas Kanban, pamatojoties uz notikumu.</span><span class="sxs-lookup"><span data-stu-id="094d4-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="094d4-116">Vēlāk šajā procedūrā jūs aktivizēsiet pārsūtīšanas Kanban, izmantojot krājumu papildināšanu.</span><span class="sxs-lookup"><span data-stu-id="094d4-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="094d4-117">Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="094d4-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="094d4-118">Ievadiet vai Atlasiet ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="094d4-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="094d4-119">Šai pārsūtīšanas aktivitātei ir ieejas plūsmas (izvades) noliktava un novietojums 12, kas nozīmē, ka materiāli tiks pārvietoti uz novietojumu 12 noliktavā 12.</span><span class="sxs-lookup"><span data-stu-id="094d4-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="094d4-120">Izvērsiet sadaļu Detalizēti.</span><span class="sxs-lookup"><span data-stu-id="094d4-120">Expand the Details section.</span></span>
7. <span data-ttu-id="094d4-121">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="094d4-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="094d4-122">Atlasiet M0007.</span><span class="sxs-lookup"><span data-stu-id="094d4-122">Select M0007.</span></span>  
8. <span data-ttu-id="094d4-123">Izvērsiet sadali Notikumi.</span><span class="sxs-lookup"><span data-stu-id="094d4-123">Expand the Events section.</span></span>
9. <span data-ttu-id="094d4-124">Laukā Krājumu papildināšanas notikums “Partija”.</span><span class="sxs-lookup"><span data-stu-id="094d4-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="094d4-125">Ar šo tiek izveidoti Kanban materiālu vajadzību izpildīšanai saistītajā novietojumā, kamēr notiek Pieprasījuma notikuma apstrāde.</span><span class="sxs-lookup"><span data-stu-id="094d4-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="094d4-126">Iestatīt krājumam minimālo daudzumu</span><span class="sxs-lookup"><span data-stu-id="094d4-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="094d4-127">Noklikšķiniet, lai sekotu saitei laukā Prece.</span><span class="sxs-lookup"><span data-stu-id="094d4-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="094d4-128">Noklikšķiniet, lai sekotu saitei laukā Krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="094d4-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="094d4-129">Izvērsiet preces attēla papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="094d4-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="094d4-130">Darbību rūtī noklikšķiniet uz Plānot.</span><span class="sxs-lookup"><span data-stu-id="094d4-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="094d4-131">Noklikšķiniet uz Krājumu vajadzība.</span><span class="sxs-lookup"><span data-stu-id="094d4-131">Click Item coverage.</span></span>
6. <span data-ttu-id="094d4-132">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="094d4-132">Click New.</span></span>
7. <span data-ttu-id="094d4-133">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="094d4-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="094d4-134">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="094d4-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="094d4-135">Iestatiet Noliktava uz 12.</span><span class="sxs-lookup"><span data-stu-id="094d4-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="094d4-136">Vērtību Minimums iestatiet uz “200”.</span><span class="sxs-lookup"><span data-stu-id="094d4-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="094d4-137">Palaist pakešveida notikuma izveidošanas darbu</span><span class="sxs-lookup"><span data-stu-id="094d4-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="094d4-138">Doties uz Ražošanas kontrole > Periodiskie uzdevumi > Kanban darbu pakešveida apstrāde > Pieprasījuma notikuma apstrāde.</span><span class="sxs-lookup"><span data-stu-id="094d4-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="094d4-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="094d4-139">Click OK.</span></span>
3. <span data-ttu-id="094d4-140">Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="094d4-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="094d4-141">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="094d4-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="094d4-142">Atlasiet Kanban nosacījumu, kuru izveidojāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="094d4-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="094d4-143">Izvērsiet sadaļu Vairāki Kanban.</span><span class="sxs-lookup"><span data-stu-id="094d4-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="094d4-144">Ņemiet vērā, ka Kanban tika izveidots, lai nepieciešamos materiālus pārsūtītu uz noliktavu 12.</span><span class="sxs-lookup"><span data-stu-id="094d4-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  


