---
title: Pārdošanas notikuma Kanban kārtulas izveide
description: Šī procedūra fokusējas uz iestatījumiem, kas ir vajadzīgi, lai izveidotu Kanban nosacījumu, kas tiek izraisīts pārdošanas pasūtījuma izveides laikā.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e33be986886d31c5275df3e36e2ce632f32c6f0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228567"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="ff1eb-103">Pārdošanas notikuma Kanban kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="ff1eb-103">Create a sales event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff1eb-104">Šī procedūra fokusējas uz iestatījumiem, kas ir vajadzīgi, lai izveidotu Kanban nosacījumu, kas tiek izraisīts pārdošanas pasūtījuma izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="ff1eb-105">Notikuma Kanban nosacījums papildina prasības, kas cēlušās no pārdošanas pasūtījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="ff1eb-106">USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ff1eb-107">Tie ir paredzēti procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jaunas vai modificētas preces ražošanai.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="ff1eb-108">Izveidot jaunu Kanban nosacījumu</span><span class="sxs-lookup"><span data-stu-id="ff1eb-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="ff1eb-109">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ff1eb-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-110">Click New.</span></span>
3. <span data-ttu-id="ff1eb-111">Laukā Papildināšanas stratēģija atlasiet "Notikums".</span><span class="sxs-lookup"><span data-stu-id="ff1eb-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="ff1eb-112">Ja atlasīt Notikums, tas nozīmē, ka Kanban nosacījumu izraisa notikums, piemēram, pārdošanas pasūtījuma rindas izveide.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="ff1eb-113">Tas attiecas uz jomām, kur katram Kanban jāaptver specifisku pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="ff1eb-114">Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ff1eb-115">Atlasiet Galīgā montāža.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="ff1eb-116">Izvērsiet sadaļu Detalizēti.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-116">Expand the Details section.</span></span>
6. <span data-ttu-id="ff1eb-117">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="ff1eb-118">Atlasiet L0050.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="ff1eb-119">Notikuma definēšana</span><span class="sxs-lookup"><span data-stu-id="ff1eb-119">Define an event</span></span>
1. <span data-ttu-id="ff1eb-120">Izvērsiet sadali Notikumi.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-120">Expand the Events section.</span></span>
2. <span data-ttu-id="ff1eb-121">Laukā Pārdošanas notikums atlasiet "Automātisks".</span><span class="sxs-lookup"><span data-stu-id="ff1eb-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="ff1eb-122">Ja atlasīt pārdošanas notikumu Automātisks, šis Kanban nosacījums tiks izsaukts automātiski, pārdošanas rindai atbilstot preces un saņemšanas novietojumam.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="ff1eb-123">Šajā procedūrā tā ir prece L0050 noliktavā 13.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="ff1eb-124">Iestatiet Minimālais notikumu daudzums uz "50".</span><span class="sxs-lookup"><span data-stu-id="ff1eb-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="ff1eb-125">Ar minimālo notikumu daudzumu 50, Kanban nosacījumu izraisīs tikai notikumi ar daudzumu 50 vai vairāk.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="ff1eb-126">Izvērsiet sadaļu Ražošanas plūsma.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="ff1eb-127">Ievērojiet, ka Saņemšanas vieta ir noliktava 13.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="ff1eb-128">Tas nozīmē, ka šis Kanban nosacījums tiks izraisīts šim novietojumam.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="ff1eb-129">Šajā piemērā Kanban nosacījumu izraisīs pārdošanas rinda precei L0050 ar daudzumu 50 vai vairāk noliktavā 13.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="ff1eb-130">Pārdošanas rinda izveide notikuma Kanban nosacījuma izraisīšanai</span><span class="sxs-lookup"><span data-stu-id="ff1eb-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="ff1eb-131">Dodieties uz Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="ff1eb-132">Brīdinājums tiek parādīts, kad tiek saglabāts Kanban nosacījums, kas nozīmē, ka vairāki Kanban tiks izveidoti reāllaikā pārdošanas pasūtījuma izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="ff1eb-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-133">Click New.</span></span>
3. <span data-ttu-id="ff1eb-134">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="ff1eb-135">Piemēram, atlasiet US-003.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="ff1eb-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-136">Click OK.</span></span>
5. <span data-ttu-id="ff1eb-137">Laukā Krājuma kods ierakstiet L0050.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="ff1eb-138">Laukā Vieta ierakstiet “1”.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="ff1eb-139">Atlasiet Vieta 1, jo Noliktava 13 atrodas Vietā 1.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="ff1eb-140">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ff1eb-141">Iestatiet Noliktava uz 13.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="ff1eb-142">Daudzuma laukā iestatiet vērtību 75.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="ff1eb-143">Ievadiet daudzumu 50 vai lielāku, lai izraisītu izveidotos Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="ff1eb-144">Pārbaude, vai Kanban ir izveidots</span><span class="sxs-lookup"><span data-stu-id="ff1eb-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="ff1eb-145">Noklikšķiniet uz Preces un piegādes.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-145">Click Product and supply.</span></span>
2. <span data-ttu-id="ff1eb-146">Noklikšķiniet uz Skatīt piesaistes koku.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="ff1eb-147">Ņemiet vērā, ka tiek izveidots Kanban ar tādu pašu daudzumu kā pārdošanas rindā.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="ff1eb-148">Varat arī redzēt, ko problēmām ar materiāliem vajadzēja saražot L0050.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="ff1eb-149">Šā ir pēdējā darbība šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="ff1eb-149">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]