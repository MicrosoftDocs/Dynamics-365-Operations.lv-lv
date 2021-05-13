---
title: Noliktavas krājumu korekcija
description: Šajā tēmā sniegta informācija par noliktavas krājumu korekciju žurnālu un apstrādi, ja izmantojat mēroga vienības.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938230"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="e009d-103">Noliktavas krājumu korekcija</span><span class="sxs-lookup"><span data-stu-id="e009d-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e009d-104">Noliktavas krājumu korekcijas līdzeklis tiek izmantots, palaižot mākoņa un malas skalas vienības [ražošanas darba noslodzei](cloud-edge-workload-manufacturing.md) un [noliktavas pārvaldības darba noslodzei](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="e009d-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="e009d-105">Ja darbinieks veic krājumu korekciju, izmantojot noliktavas programmu pret mēroga vienības noliktavas pārvaldības darba slodzi, fiziskais rīcībā esošo krājumu atjauninājums ir jāapstrādā ar pakešuzdevumu **Noliktavas krājumu korekcijas žurnāls**, ko palaižat un plānojat, atverot **Noliktavas pārvaldība > Periodiskie uzdevumi > Noliktavas krājumu korekciju žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="e009d-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="e009d-106">Tālāk minētajiem noliktavas programmas darba procesiem pašlaik tiek izmantots **Noliktavas krājumu korekcijas žurnāls** mēroga vienības darba noslodzei:</span><span class="sxs-lookup"><span data-stu-id="e009d-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="e009d-107">Korekcija ienākošā/izejošā</span><span class="sxs-lookup"><span data-stu-id="e009d-107">Adjustment in/out</span></span>
- <span data-ttu-id="e009d-108">Cikla inventarizācija</span><span class="sxs-lookup"><span data-stu-id="e009d-108">Cycle counting</span></span>
- <span data-ttu-id="e009d-109">Numura zīmes ielāde</span><span class="sxs-lookup"><span data-stu-id="e009d-109">License plate loading</span></span>

<span data-ttu-id="e009d-110">Vairākas krājumu darbības ir izveidotas kā daļa no mākoņa un malas krājumu korekcijas procesa, jo centrmezgla un mēroga vienību izvietojumi koplieto šos krājumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e009d-110">Several inventory transactions are created as part of cloud and edge an inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="e009d-111">Krājumu korekciju piemērs</span><span class="sxs-lookup"><span data-stu-id="e009d-111">Inventory adjustment example</span></span>

<span data-ttu-id="e009d-112">Šajā piemērā noliktavas darbinieks ir izmantojis noliktavas programmu, lai reģistrētu rīcībā esošo krājumu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="e009d-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="e009d-113">Vispirms mēroga vienības darba noslodze izveido noliktavas krājumu korekcijas darbību pozitīvam fiziskajam pielāgojumam, kas pēc tam tiek sinhronizēts ar centrmezglu, un rezultātā palielinās rīcībā esošie krājumi centrmezgla ietvaros.</span><span class="sxs-lookup"><span data-stu-id="e009d-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="e009d-114">tips</span><span class="sxs-lookup"><span data-stu-id="e009d-114">Type</span></span>                                    | <span data-ttu-id="e009d-115">Mēroga vienība</span><span class="sxs-lookup"><span data-stu-id="e009d-115">Scale unit</span></span> | <span data-ttu-id="e009d-116">Virziens</span><span class="sxs-lookup"><span data-stu-id="e009d-116">Direction</span></span> | <span data-ttu-id="e009d-117">Centrmezgls</span><span class="sxs-lookup"><span data-stu-id="e009d-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="e009d-118">Noliktavas krājumu korekcija</span><span class="sxs-lookup"><span data-stu-id="e009d-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="e009d-119">+1</span><span class="sxs-lookup"><span data-stu-id="e009d-119">+1</span></span>         | ->        | <span data-ttu-id="e009d-120">+1</span><span class="sxs-lookup"><span data-stu-id="e009d-120">+1</span></span>  |

<span data-ttu-id="e009d-121">Pēc tam centrmezgls apstrādā uzskaites žurnāla grāmatošanu, kas tiek saņemta, izmantojot [ziņojumu procesora ziņojumus](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="e009d-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="e009d-122">Tas atjaunina rīcībā esošos papildu krājumus.</span><span class="sxs-lookup"><span data-stu-id="e009d-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="e009d-123">Lai novērstu dubultos rīcībā esošos krājumus, centrmezgls kā daļu no šī procesa izveido korespondējošo darbību un noņem iepriekš reģistrētos rīcībā esošos krājumus, kas ir saistīti ar noliktavas krājumu korekciju.</span><span class="sxs-lookup"><span data-stu-id="e009d-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="e009d-124">tips</span><span class="sxs-lookup"><span data-stu-id="e009d-124">Type</span></span>                                    | <span data-ttu-id="e009d-125">Mēroga vienība</span><span class="sxs-lookup"><span data-stu-id="e009d-125">Scale unit</span></span> | <span data-ttu-id="e009d-126">Virziens</span><span class="sxs-lookup"><span data-stu-id="e009d-126">Direction</span></span> | <span data-ttu-id="e009d-127">Centrmezgls</span><span class="sxs-lookup"><span data-stu-id="e009d-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="e009d-128">Inventarizācija</span><span class="sxs-lookup"><span data-stu-id="e009d-128">Counting</span></span>                                | <span data-ttu-id="e009d-129">+1</span><span class="sxs-lookup"><span data-stu-id="e009d-129">+1</span></span>         | <-        | <span data-ttu-id="e009d-130">+1</span><span class="sxs-lookup"><span data-stu-id="e009d-130">+1</span></span>  |
| <span data-ttu-id="e009d-131">Noliktavas krājuma korekcija (korespondējošā)</span><span class="sxs-lookup"><span data-stu-id="e009d-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="e009d-132">-1</span><span class="sxs-lookup"><span data-stu-id="e009d-132">-1</span></span>         | <-        | <span data-ttu-id="e009d-133">-1</span><span class="sxs-lookup"><span data-stu-id="e009d-133">-1</span></span>  |

<span data-ttu-id="e009d-134">Kad mēroga vienība centrmezglā ir izveidojusi **Noliktavas krājumu korekciju žurnālu**, varat pārskatīt gan **Inventarizācijas žurnālu**, gan **Korespondējošo žurnālu**, kas ir izveidots centrmezglā kā daļa korekcijas procesa.</span><span class="sxs-lookup"><span data-stu-id="e009d-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="e009d-135">Jūs variet pārskatīt katru no šiem žurnāla ierakstiem un transakcijam Supply Chain Management, rīkojoties šādi:</span><span class="sxs-lookup"><span data-stu-id="e009d-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="e009d-136">Pieteikties mēroga vienībā.</span><span class="sxs-lookup"><span data-stu-id="e009d-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="e009d-137">Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Noliktavas krājumu korekciju žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="e009d-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="e009d-138">Lapā **Noliktavas krājumu korekciju žurnāls** atrodiet un atveriet žurnālu, kurā ierakstītas rīcībā esošo krājumu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="e009d-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="e009d-139">Sadaļā **Žurnāla rindas** ir parādīti visi šajā žurnālā ierakstītie pielāgojumi.</span><span class="sxs-lookup"><span data-stu-id="e009d-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="e009d-140">Pieteikties centrmezglā.</span><span class="sxs-lookup"><span data-stu-id="e009d-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="e009d-141">Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Noliktavas krājumu korekciju žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="e009d-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="e009d-142">Ja pārkraušanas mezgls un mēroga vienība ir sinhronizēta, lapā **Noliktavas krājumu korekciju žurnāls** jums vajadzētu redzēt to pašu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="e009d-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="e009d-143">Atvērt žurnālu.</span><span class="sxs-lookup"><span data-stu-id="e009d-143">Open the journal.</span></span> <span data-ttu-id="e009d-144">Ja [ziņojumu procesora ziņojumi](cloud-edge-message-processor-messages.md) ir apstrādāti, virsrakstā redzēsit saites uz **Inventarizācijas žurnālu** un **Korespondējošo žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="e009d-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="e009d-145">Žurnālam **Inventarizācijas žurnāls** jārāda tādas pašas dimensiju vērtības kā žurnāla rindām.</span><span class="sxs-lookup"><span data-stu-id="e009d-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="e009d-146">Žurnālam **Korespondējošais žurnāls** ir jārāda nobīdi, kas noņem dubulto krājuma korekciju.</span><span class="sxs-lookup"><span data-stu-id="e009d-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="e009d-147">Kad sinhronizācija un apstrāde ir pabeigta, **Inventarizācijas žurnāls** un **Korespondējošais žurnāls** tiek sinhronizēti atpakaļ uz mēroga vienību.</span><span class="sxs-lookup"><span data-stu-id="e009d-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="e009d-148">Tos var arī skatīt no atbilstošās lapas **Noliktavas krājumu korekciju žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="e009d-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
