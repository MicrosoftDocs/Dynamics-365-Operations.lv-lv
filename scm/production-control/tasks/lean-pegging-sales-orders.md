--- 
title: "Racionālā piesaiste no pārdošanas pasūtījumiem"
description: "Šajā procedūrā aprakstīts piesaistes koka validācijas process no pārdošanas rindas, kur krājums tiek ražots ar Kanban."
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
ms.openlocfilehash: 3aa8cd2c0be56875904158f041cf120c466d9e9a
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="07b7d-103">Racionālā piesaiste no pārdošanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="07b7d-103">Lean pegging from sales orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07b7d-104">Šajā procedūrā aprakstīts piesaistes koka validācijas process no pārdošanas rindas, kur krājums tiek ražots ar Kanban.</span><span class="sxs-lookup"><span data-stu-id="07b7d-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="07b7d-105">Pēc piesaistes koka validācijas, visu Kanban darbu statuss ir Plānots.</span><span class="sxs-lookup"><span data-stu-id="07b7d-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="07b7d-106">Tas ir noderīgi saistībā ar tādiem pasūtījumiem, kur pasūtījuma ņēmējam ir jānodrošina, ka ražošanu var sākt nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="07b7d-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="07b7d-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="07b7d-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="07b7d-108">Šī procedūra ir paredzēta papildu pasūtījuma ņēmējam, kas strādā aizdevumu pakalpojumu uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="07b7d-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="07b7d-109">Pārdošanas pasūtījuma izveide Kanban kontrolētam krājumam</span><span class="sxs-lookup"><span data-stu-id="07b7d-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="07b7d-110">Dodieties uz Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="07b7d-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="07b7d-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="07b7d-111">Click New.</span></span>
3. <span data-ttu-id="07b7d-112">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="07b7d-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="07b7d-113">Lietojiet formu ASV-001.</span><span class="sxs-lookup"><span data-stu-id="07b7d-113">Use US-001.</span></span>  
4. <span data-ttu-id="07b7d-114">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="07b7d-114">Click OK.</span></span>
5. <span data-ttu-id="07b7d-115">Laukā Krājuma kods ierakstiet L0001.</span><span class="sxs-lookup"><span data-stu-id="07b7d-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="07b7d-116">Daudzuma laukā iestatiet vērtību 30.</span><span class="sxs-lookup"><span data-stu-id="07b7d-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="07b7d-117">Ir svarīgi, ka daudzuma vērtība ir lielāka par 24, lai aktivizētu notikuma Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="07b7d-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="07b7d-118">Piesaistes koka atvēršana</span><span class="sxs-lookup"><span data-stu-id="07b7d-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="07b7d-119">Noklikšķiniet uz Preces un piegādes.</span><span class="sxs-lookup"><span data-stu-id="07b7d-119">Click Product and supply.</span></span>
2. <span data-ttu-id="07b7d-120">Noklikšķiniet uz Skatīt piesaistes koku.</span><span class="sxs-lookup"><span data-stu-id="07b7d-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="07b7d-121">Ņemiet vērā! Piesaistes kokā tiek rādīti visi pārdošanas pasūtījuma rindai nepieciešamie piesaistes līmeņi.</span><span class="sxs-lookup"><span data-stu-id="07b7d-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="07b7d-122">Šajā gadījumā ir divu līmeņu Kanban un visi nepieciešamie komponenti.</span><span class="sxs-lookup"><span data-stu-id="07b7d-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="07b7d-123">Piesaistes koka plānošana</span><span class="sxs-lookup"><span data-stu-id="07b7d-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="07b7d-124">Kokā atlasiet Pārdošanas rinda 000832\Kanban 000558.</span><span class="sxs-lookup"><span data-stu-id="07b7d-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="07b7d-125">Izvērsiet sadaļu Kanban darbi.</span><span class="sxs-lookup"><span data-stu-id="07b7d-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="07b7d-126">Ņemiet vērā! Kanban darba statuss ir Nav plānots.</span><span class="sxs-lookup"><span data-stu-id="07b7d-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="07b7d-127">Noklikšķiniet uz Plānot visu piesaistes koku.</span><span class="sxs-lookup"><span data-stu-id="07b7d-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="07b7d-128">Tādējādi tiks plānoti visi piesaistes kokā esošie Kanban darbi, mainot lauka Darba statuss vērtību no Nav plānots uz Plānots.</span><span class="sxs-lookup"><span data-stu-id="07b7d-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="07b7d-129">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="07b7d-129">Refresh the page.</span></span>
    * <span data-ttu-id="07b7d-130">Ņemiet vērā! Kanban darba statuss tika mainīts no Nav plānots uz Plānots.</span><span class="sxs-lookup"><span data-stu-id="07b7d-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="07b7d-131">Koka struktūrā atlasiet Pārdošanas rinda 000832\Kanban 000558\L0001 izdošana\Kanban 000559.</span><span class="sxs-lookup"><span data-stu-id="07b7d-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="07b7d-132">Otrā Kanban darba status arī ir Plānots, jo visa piesaistes koka statuss ir Plānots.</span><span class="sxs-lookup"><span data-stu-id="07b7d-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="07b7d-133">Ņemiet vērā! Kanban darba statuss tika mainīts no Nav plānots uz Plānots.</span><span class="sxs-lookup"><span data-stu-id="07b7d-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  


