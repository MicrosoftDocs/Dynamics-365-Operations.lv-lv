---
title: Pavadzīmes ģenerēšanas laikā izdotais daudzums nav pietiekams
description: Izveidojot pavadzīmi, izejošā kravā ir iztotais daudzums, kas neatbilst izveidotajam darba daudzumam uz kravas rindas.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249138"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="f7ea3-103">Pavadzīmes ģenerēšanas laikā izdotais daudzums nav pietiekams</span><span class="sxs-lookup"><span data-stu-id="f7ea3-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="f7ea3-104">Kļūdas kods: SYS54073</span><span class="sxs-lookup"><span data-stu-id="f7ea3-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="f7ea3-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="f7ea3-105">Symptoms</span></span>

<span data-ttu-id="f7ea3-106">Izveidojot pavadzīmi, izejošā kravā ir iztotais daudzums, kas neatbilst izveidotajam darba daudzumam uz kravas rindas.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="f7ea3-107">Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="f7ea3-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="f7ea3-108">Tā kā %1 ir izdoti, %2 nevar grāmatot, ja atlikumam attiecīgi ir jābūt %3.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="f7ea3-109">Tādēļ kravas pavadzīmi nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f7ea3-110">Iemesls</span><span class="sxs-lookup"><span data-stu-id="f7ea3-110">Cause</span></span>

<span data-ttu-id="f7ea3-111">Pavadzīmi nevar ģenerēt tās pašreizējā stāvoklī, jo var pastāvēt viens no tālāk norādītajiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="f7ea3-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="f7ea3-112">Saistītais darbs vēl nav izdots un pārvietots uz beigu nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="f7ea3-113">Izdotais darba daudzums nesaskan ar kravas rindā izveidoto darba daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="f7ea3-114">Kravas rindas daudzums, darba izveidotais daudzums un izdotais daudzums nesakrīt.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="f7ea3-115">Novēršana</span><span class="sxs-lookup"><span data-stu-id="f7ea3-115">Resolution</span></span>

<span data-ttu-id="f7ea3-116">Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="f7ea3-117">Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="f7ea3-118">Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="f7ea3-119">Pielāgojiet krāvas rindu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="f7ea3-120">Atsauciet visas izdošanas reģistrācijas un atceliet izdošanu.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="f7ea3-121">Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt</span><span class="sxs-lookup"><span data-stu-id="f7ea3-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="f7ea3-122">Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="f7ea3-123">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f7ea3-124">Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="f7ea3-125">Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="f7ea3-126">Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="f7ea3-127">Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="f7ea3-128">Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="f7ea3-129">Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="f7ea3-130">Pielāgojiet kravas rindu daudzumu</span><span class="sxs-lookup"><span data-stu-id="f7ea3-130">Adjust the load line quantity</span></span>

<span data-ttu-id="f7ea3-131">Izmantojiet šo procedūru, lai pielāgotu kravas rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="f7ea3-132">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f7ea3-133">Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="f7ea3-134">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="f7ea3-135">Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas rada problēmu.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="f7ea3-136">Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="f7ea3-137">Iestatiet lauku **Samazināt kravas rindu**, lai atspoguļotu korekcijas kravas rindā.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="f7ea3-138">Atsauciet visas izdošanas reģistrācijas un atceliet izdošanu</span><span class="sxs-lookup"><span data-stu-id="f7ea3-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="f7ea3-139">Problēma var rasties, jo kāds izmanto izdošanas reģistrāciju, lai aizvērtu kravas rindu bez darba.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="f7ea3-140">Šajā gadījumā ir jāatgriež manuāla izdošanas reģistrācija un pēc tam, izmantojot mobilo programmu Warehouse Management, izdošanas process ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="f7ea3-141">Lai atsauktu izdošanas reģistrāciju, izmantojiet šādu procedūru.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="f7ea3-142">Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="f7ea3-143">Atlasiet pārdošanas pasūtījumu, kuram nevar grāmatot kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="f7ea3-144">Cilnē **Pārdošanas pasūtījuma rindas** atlasiet pārdošanas pasūtījuma rindu, kam veikta izdošanas reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="f7ea3-145">Atlasiet **Atjaunināt rindu \> Izdot**, lai anulētu krājumu izdošanu.</span><span class="sxs-lookup"><span data-stu-id="f7ea3-145">Select **Update line \> Pick** to unpick the items.</span></span>
