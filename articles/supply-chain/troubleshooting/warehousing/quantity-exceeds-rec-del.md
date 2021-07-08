---
title: Atjaunināšanai izmantotais daudzums pārsniedz saņemto/piegādāto daudzumu.
description: Izveidojot pavadzīmi, izejošā kravā ir daudzums, kas pārsniedz izveidotā darba daudzumu, kas tika izdots un rezervēts pārdošanas pasūtījumam.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249139"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="7ac7c-103">Atjaunināšanai izmantotais daudzums pārsniedz saņemto/piegādāto daudzumu</span><span class="sxs-lookup"><span data-stu-id="7ac7c-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="7ac7c-104">Kļūdas kods: SYS7676</span><span class="sxs-lookup"><span data-stu-id="7ac7c-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="7ac7c-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="7ac7c-105">Symptoms</span></span>

<span data-ttu-id="7ac7c-106">Izveidojot pavadzīmi, izejošā kravā ir daudzums, kas pārsniedz izveidotā darba daudzumu, kas tika izdots un rezervēts pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="7ac7c-107">Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="7ac7c-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="7ac7c-108">Atjaunināšanai atlasītais daudzums pārsniedz saņemto/piegādāto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="7ac7c-109">Tādēļ kravas pavadzīmi nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7ac7c-110">Iemesls</span><span class="sxs-lookup"><span data-stu-id="7ac7c-110">Cause</span></span>

<span data-ttu-id="7ac7c-111">Izdotais darba daudzums nesaskan ar kravas rindā izveidoto darba daudzumu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="7ac7c-112">Piemēram, šī problēma var rasties, ja noslodzes rindas daudzums, darba izveidotais daudzums vai izdotais daudzums nav pareizs.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="7ac7c-113">Novēršana</span><span class="sxs-lookup"><span data-stu-id="7ac7c-113">Resolution</span></span>

<span data-ttu-id="7ac7c-114">Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="7ac7c-115">Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="7ac7c-116">Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="7ac7c-117">Pielāgojiet krāvas rindu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="7ac7c-118">Atsauciet visas izdošanas reģistrācijas un atceliet izdošanu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="7ac7c-119">Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt</span><span class="sxs-lookup"><span data-stu-id="7ac7c-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="7ac7c-120">Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="7ac7c-121">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7ac7c-122">Izvēlieties kravu, kam nevar ģenerēt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="7ac7c-123">Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="7ac7c-124">Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="7ac7c-125">Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="7ac7c-126">Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="7ac7c-127">Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="7ac7c-128">Pielāgojiet kravas rindu daudzumu</span><span class="sxs-lookup"><span data-stu-id="7ac7c-128">Adjust the load line quantity</span></span>

<span data-ttu-id="7ac7c-129">Izmantojiet šo procedūru, lai pielāgotu kravas rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="7ac7c-130">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7ac7c-131">Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="7ac7c-132">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="7ac7c-133">Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas rada problēmu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="7ac7c-134">Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="7ac7c-135">Iestatiet lauku **Samazināt kravas rindu**, lai atspoguļotu korekcijas kravas rindā.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="7ac7c-136">Atsauciet visas izdošanas reģistrācijas un atceliet izdošanu</span><span class="sxs-lookup"><span data-stu-id="7ac7c-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="7ac7c-137">Ja kāds izmanto izdošanas reģistrāciju, lai slēgtu kravas rindu bez darba, var rasties neatbilstība starp kravas rindas daudzumu un izdoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="7ac7c-138">Šajā gadījumā ir jāatgriež manuāla izdošanas reģistrācija un pēc tam, izmantojot mobilo programmu Warehouse Management, izdošanas process ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="7ac7c-139">Lai atsauktu izdošanas reģistrāciju, izmantojiet šādu procedūru.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="7ac7c-140">Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="7ac7c-141">Atlasiet pārdošanas pasūtījumu, kuram nevar grāmatot kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="7ac7c-142">Cilnē **Pārdošanas pasūtījuma rindas** atlasiet pārdošanas pasūtījuma rindu, kam veikta izdošanas reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="7ac7c-143">Atlasiet **Atjaunināt rindu \> Izdot**, lai anulētu krājumu izdošanu.</span><span class="sxs-lookup"><span data-stu-id="7ac7c-143">Select **Update line \> Pick** to unpick the items.</span></span>
