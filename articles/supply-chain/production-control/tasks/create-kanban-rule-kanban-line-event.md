---
title: Kanban kārtulas izveide, izmantojot Kanban rindas notikumu
description: Ar šo procedūru tiek izveidots Kanban nosacījums, izmantojot Kanban rindas notikuma iestatījumu izvilkuma aktivizēšanai no procesa aktivitātes.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe2fa817229af541baa61406487bd60b20ddc8b7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838683"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="259be-103">Kanban kārtulas izveide, izmantojot Kanban rindas notikumu</span><span class="sxs-lookup"><span data-stu-id="259be-103">Create a kanban rule using a kanban line event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="259be-104">Ar šo procedūru tiek izveidots Kanban nosacījums, izmantojot Kanban rindas notikuma iestatījumu izvilkuma aktivizēšanai no procesa aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="259be-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="259be-105">Kanban nosacījums tiek aktivizēts ar Kanban procesa aktivitāti un ar daudzumu, kas katrs ir vienāds ar vai lielāks par 25.</span><span class="sxs-lookup"><span data-stu-id="259be-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="259be-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="259be-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="259be-107">Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad viņi sagatavo jaunas vai modificētas preces ražošanu racionālā vidē.</span><span class="sxs-lookup"><span data-stu-id="259be-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="259be-108">Kanban nosacījumu izveide</span><span class="sxs-lookup"><span data-stu-id="259be-108">Create a kanban rule</span></span>
1. <span data-ttu-id="259be-109">Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="259be-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="259be-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="259be-110">Click New.</span></span>
3. <span data-ttu-id="259be-111">Laukā Papildināšanas stratēģija atlasiet "Notikums".</span><span class="sxs-lookup"><span data-stu-id="259be-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="259be-112">Šādi Kanban tiek ģenerēti tieši no pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="259be-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="259be-113">Šī procedūra tiek izmantota, lai iestatītu kārtulas, kas definē pasūtījuma veikšanas scenāriju.</span><span class="sxs-lookup"><span data-stu-id="259be-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="259be-114">Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="259be-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="259be-115">Ievadiet vai atlasiet vērtību SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="259be-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="259be-116">Pirmā ražošanas Kanban nosacījuma aktivitāte ir procesa aktivitāte ražošanas plūsmā.</span><span class="sxs-lookup"><span data-stu-id="259be-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="259be-117">Kad atlasāt šo aktivitāti, aktivitātes derīguma datumi tiek kopēti uz Kanban nosacījumu derīguma datumiem.</span><span class="sxs-lookup"><span data-stu-id="259be-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="259be-118">Izvērsiet sadaļu Detalizēti.</span><span class="sxs-lookup"><span data-stu-id="259be-118">Expand the Details section.</span></span>
6. <span data-ttu-id="259be-119">Laukā Prece ierakstiet “L0001”.</span><span class="sxs-lookup"><span data-stu-id="259be-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="259be-120">Izvērsiet sadali Notikumi.</span><span class="sxs-lookup"><span data-stu-id="259be-120">Expand the Events section.</span></span>
8. <span data-ttu-id="259be-121">Laukā Kanban rindas notikums atlasiet “Automātisks”.</span><span class="sxs-lookup"><span data-stu-id="259be-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="259be-122">Šādi notikumu Kanban tiek ģenerēti pēc pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="259be-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="259be-123">Šis lauks tiek izmantots, lai konfigurētu Kanban nosacījumus, kuri papildina materiālu, kas ir nepieciešams lejupstraumes procesa aktivitātei.</span><span class="sxs-lookup"><span data-stu-id="259be-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="259be-124">Kad atlasāt Automātisks, notikumu Kanban tiek izveidoti ar pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="259be-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="259be-125">Šis iestatījums ir ieteicams, ja ražošanu plānojat izpildīt tajā pašā dienā.</span><span class="sxs-lookup"><span data-stu-id="259be-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="259be-126">Iestatiet Minimālais notikumu daudzums uz "25".</span><span class="sxs-lookup"><span data-stu-id="259be-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="259be-127">Notikumu Kanban tiek ģenerēti, kad pieprasījuma daudzums ir vienāds ar vai lielāks par vērtību šajā laukā.</span><span class="sxs-lookup"><span data-stu-id="259be-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="259be-128">Tas ir noderīgi, ja pasūtījuma daudzumu, kas ir mazāks par šī lauka vērtību, vēlaties ražot vienā mašīnā, bet daudzumu, kas ir lielāks par šī lauka vērtību, vēlaties ražot citā mašīnā.</span><span class="sxs-lookup"><span data-stu-id="259be-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="259be-129">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="259be-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="259be-130">Izveidot pārdošanas pasūtījumu un aktivizēt Kanban ķēdi</span><span class="sxs-lookup"><span data-stu-id="259be-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="259be-131">Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="259be-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="259be-132">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="259be-132">Click New.</span></span>
3. <span data-ttu-id="259be-133">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="259be-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="259be-134">Atlasiet Debitora konts US-003, Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="259be-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="259be-135">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="259be-135">Click OK.</span></span>
5. <span data-ttu-id="259be-136">Laukā Krājuma kods ierakstiet L0001.</span><span class="sxs-lookup"><span data-stu-id="259be-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="259be-137">L0001 ir krājums, kuram jūs izveidojāt šo Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="259be-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="259be-138">Daudzuma laukā iestatiet vērtību 27.</span><span class="sxs-lookup"><span data-stu-id="259be-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="259be-139">Tā kā vērtība 27 ir lielāka par Kanban nosacījuma minimālo daudzumu 25, tad ar šo tiks aktivizēts notikuma Kanban.</span><span class="sxs-lookup"><span data-stu-id="259be-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="259be-140">Laukā Vieta ierakstiet “1”.</span><span class="sxs-lookup"><span data-stu-id="259be-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="259be-141">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="259be-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="259be-142">Atlasiet noliktavu 13.</span><span class="sxs-lookup"><span data-stu-id="259be-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="259be-143">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="259be-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="259be-144">Skatīt Kanban nosacījuma ģenerētu Kanban</span><span class="sxs-lookup"><span data-stu-id="259be-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="259be-145">Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="259be-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="259be-146">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="259be-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="259be-147">Izvērsiet sadaļu Vairāki Kanban.</span><span class="sxs-lookup"><span data-stu-id="259be-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="259be-148">Ņemiet vērā, ka Kanban vērtībai 27 tika izveidots, lai apstrādātu aktivitāti, pamatojoties uz izveidoto Kanban nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="259be-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="259be-149">Šis ir pēdējais solis.</span><span class="sxs-lookup"><span data-stu-id="259be-149">This is the last step.</span></span>  

