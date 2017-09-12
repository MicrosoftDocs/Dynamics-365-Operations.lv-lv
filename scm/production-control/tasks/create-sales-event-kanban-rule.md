--- 
title: "Pārdošanas notikumu Kanban kārtulas izveide"
description: "Šī procedūra fokusējas uz iestatījumiem, kas ir vajadzīgi, lai izveidotu Kanban nosacījumus, kas tiek izraisīti pārdošanas pasūtījuma izveides laikā."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 33ae479a8479732a1857577743a22068d2059a47
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="837aa-103">Pārdošanas notikumu Kanban kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="837aa-103">Create a sales event kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="837aa-104">Šī procedūra fokusējas uz iestatījumiem, kas ir vajadzīgi, lai izveidotu Kanban nosacījumus, kas tiek izraisīti pārdošanas pasūtījuma izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="837aa-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="837aa-105">Notikumu Kanban nosacījumi papildina prasības, kas cēlušās no pārdošanas pasūtījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="837aa-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="837aa-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="837aa-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="837aa-107">Tie ir paredzēti procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jaunas vai modificētas preces ražošanai.</span><span class="sxs-lookup"><span data-stu-id="837aa-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="837aa-108">Izveidot jaunu Kanban nosacījumu</span><span class="sxs-lookup"><span data-stu-id="837aa-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="837aa-109">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="837aa-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="837aa-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="837aa-110">Click New.</span></span>
3. <span data-ttu-id="837aa-111">Laukā Papildināšanas stratēģija atlasiet "Notikums".</span><span class="sxs-lookup"><span data-stu-id="837aa-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="837aa-112">Ja atlasīt Notikums, tas nozīmē, ka Kanban nosacījumus izraisa notikums, piemēram, pārdošanas pasūtījuma rindas izveide.</span><span class="sxs-lookup"><span data-stu-id="837aa-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="837aa-113">Tas attiecas uz jomām, kur katram Kanban jāaptver specifisku pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="837aa-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="837aa-114">Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="837aa-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="837aa-115">Atlasiet Galīgā montāža.</span><span class="sxs-lookup"><span data-stu-id="837aa-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="837aa-116">Izvērsiet sadaļu Detalizēti.</span><span class="sxs-lookup"><span data-stu-id="837aa-116">Expand the Details section.</span></span>
6. <span data-ttu-id="837aa-117">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="837aa-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="837aa-118">Atlasiet L0050.</span><span class="sxs-lookup"><span data-stu-id="837aa-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="837aa-119">Notikuma definēšana</span><span class="sxs-lookup"><span data-stu-id="837aa-119">Define an event</span></span>
1. <span data-ttu-id="837aa-120">Izvērsiet sadali Notikumi.</span><span class="sxs-lookup"><span data-stu-id="837aa-120">Expand the Events section.</span></span>
2. <span data-ttu-id="837aa-121">Laukā Pārdošanas notikums atlasiet "Automātisks".</span><span class="sxs-lookup"><span data-stu-id="837aa-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="837aa-122">Ja atlasīt pārdošanas notikumu Automātisks, šie Kanban nosacījumi tiks izsaukti automātiski, kad pārdošanas rinda atbilst preču un saņemšanas novietojumam.</span><span class="sxs-lookup"><span data-stu-id="837aa-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="837aa-123">Šajā procedūrā tā ir prece L0050 noliktavā 13.</span><span class="sxs-lookup"><span data-stu-id="837aa-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="837aa-124">Iestatiet Minimālais notikumu daudzums uz "50".</span><span class="sxs-lookup"><span data-stu-id="837aa-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="837aa-125">Ar minimālo notikumu daudzumu 50, Kanban nosacījumus izraisīs tikai notikumi ar daudzumu 50 vai vairāk.</span><span class="sxs-lookup"><span data-stu-id="837aa-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="837aa-126">Izvērsiet sadaļu Ražošanas plūsma.</span><span class="sxs-lookup"><span data-stu-id="837aa-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="837aa-127">Ievērojiet, ka Saņemšanas vieta ir noliktava 13.</span><span class="sxs-lookup"><span data-stu-id="837aa-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="837aa-128">Tas nozīmē, ka šie Kanban nosacījumi tiks izraisīti šim novietojumam.</span><span class="sxs-lookup"><span data-stu-id="837aa-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="837aa-129">Šajā piemērā Kanban nosacījumus izraisīs pārdošanas rinda precei L0050 ar daudzumu 50 vai vairāk noliktavā 13.</span><span class="sxs-lookup"><span data-stu-id="837aa-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="837aa-130">Pārdošanas rinda izveide notikumu Kanban nosacījumu izraisīšanai</span><span class="sxs-lookup"><span data-stu-id="837aa-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="837aa-131">Dodieties uz Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="837aa-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="837aa-132">Brīdinājums tiek parādīts, kad tiek saglabāti Kanban nosacījumi, kas nozīmē, ka vairāki Kanban tiks izveidoti reāllaikā pārdošanas pasūtījuma izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="837aa-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="837aa-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="837aa-133">Click New.</span></span>
3. <span data-ttu-id="837aa-134">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="837aa-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="837aa-135">Piemēram, atlasiet US-003.</span><span class="sxs-lookup"><span data-stu-id="837aa-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="837aa-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="837aa-136">Click OK.</span></span>
5. <span data-ttu-id="837aa-137">Laukā Krājuma kods ierakstiet L0050.</span><span class="sxs-lookup"><span data-stu-id="837aa-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="837aa-138">Laukā Vieta ierakstiet “1”.</span><span class="sxs-lookup"><span data-stu-id="837aa-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="837aa-139">Atlasiet Vieta 1, jo Noliktava 13 atrodas Vietā 1.</span><span class="sxs-lookup"><span data-stu-id="837aa-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="837aa-140">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="837aa-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="837aa-141">Iestatiet Noliktava uz 13.</span><span class="sxs-lookup"><span data-stu-id="837aa-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="837aa-142">Daudzuma laukā iestatiet vērtību 75.</span><span class="sxs-lookup"><span data-stu-id="837aa-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="837aa-143">Ievadiet daudzumu 50 vai lielāku, lai izraisītu izveidotos Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="837aa-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="837aa-144">Pārbaude, vai Kanban ir izveidots</span><span class="sxs-lookup"><span data-stu-id="837aa-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="837aa-145">Noklikšķiniet uz Preces un piegādes.</span><span class="sxs-lookup"><span data-stu-id="837aa-145">Click Product and supply.</span></span>
2. <span data-ttu-id="837aa-146">Noklikšķiniet uz Skatīt piesaistes koku.</span><span class="sxs-lookup"><span data-stu-id="837aa-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="837aa-147">Ņemiet vērā, ka tiek izveidots Kanban ar tādu pašu daudzumu kā pārdošanas rindā.</span><span class="sxs-lookup"><span data-stu-id="837aa-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="837aa-148">Varat arī redzēt, ko problēmām ar materiāliem vajadzēja saražot L0050.</span><span class="sxs-lookup"><span data-stu-id="837aa-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="837aa-149">Šā ir pēdējā darbība šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="837aa-149">This is the last step in this procedure.</span></span>  


