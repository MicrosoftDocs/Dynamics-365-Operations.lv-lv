---
title: Daudzums pārsniedz pasūtījuma pārsnieguma procentus pavadzīmju ģenerēšanas laikā
description: Kad ģenerējat pavadzīmi,, izejošā krava ietver daudzumu, kas pārsniedz pasūtījuma pārsniegšanas procentus.
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249136"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="a7ef2-103">Daudzums pārsniedz pasūtījuma pārsnieguma procentus pavadzīmju ģenerēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="a7ef2-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="a7ef2-104">Kļūdas kods: SYS24920</span><span class="sxs-lookup"><span data-stu-id="a7ef2-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="a7ef2-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="a7ef2-105">Symptoms</span></span>

<span data-ttu-id="a7ef2-106">Kad ģenerējat pavadzīmi,, izejošā krava ietver daudzumu, kas pārsniedz pasūtījuma pārsniegšanas procentus.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="a7ef2-107">Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="a7ef2-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="a7ef2-108">Pasūtījuma pārsniegšana rindā ir %1 %, bet atļauts ir tikai %2 %.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="a7ef2-109">Tādēļ kravas pavadzīmi nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="a7ef2-110">Iemesls</span><span class="sxs-lookup"><span data-stu-id="a7ef2-110">Cause</span></span>

<span data-ttu-id="a7ef2-111">Kravas vai sūtījuma izdotais daudzums pārsniedz pasūtīto daudzumu, un tas nav pasūtījuma pārslogotās procentuālās vērtības diapazonā.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="a7ef2-112">Novēršana</span><span class="sxs-lookup"><span data-stu-id="a7ef2-112">Resolution</span></span>

<span data-ttu-id="a7ef2-113">Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="a7ef2-114">Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="a7ef2-115">Pielāgojiet krāvas rindu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="a7ef2-116">Pielāgojiet pārsnieguma procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="a7ef2-117">Atsaukt un veikt korekcijas.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="a7ef2-118">Pielāgojiet kravas rindu daudzumu</span><span class="sxs-lookup"><span data-stu-id="a7ef2-118">Adjust the load line quantity</span></span>

<span data-ttu-id="a7ef2-119">Izmantojiet šo procedūru, lai pielāgotu kravas rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="a7ef2-120">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a7ef2-121">Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="a7ef2-122">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="a7ef2-123">Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz pasūtījuma pārsnieguma procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="a7ef2-124">Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="a7ef2-125">Cilnē  **Rindu detāļas** atlasiet **Pasūtījums**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="a7ef2-126">Iestatiet lauku **Daudzums** uz izdoto daudzumu (t.i., uz lauka **Darba izveidotā daudzuma** vērtību), lai varētu turpināt pavadzīmes ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="a7ef2-127">Pielāgojiet pārsnieguma procentuālo vērtību</span><span class="sxs-lookup"><span data-stu-id="a7ef2-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="a7ef2-128">Izmantojiet šo procedūru, lai pielāgotu pārsnieguma procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="a7ef2-129">Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="a7ef2-130">Atlasiet pārdošanas pasūtījumu, kuram nevar grāmatot kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="a7ef2-131">Cilnē **Pārdošanas pasūtījuma rindas** atlasiet pārdošanas pasūtījuma rindu krājumam, kas pārsniedz pasūtījuma pārsnieguma procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="a7ef2-132">Cilnē  **Rindu detāļas** atlasiet **Piegāde**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="a7ef2-133">Iestatiet lauku **Pasūtījuma pārsniegšana** uz lielāku procentuālo vērtību, kas atbilst izdotajam daudzumam attiecībā pret kravas daudzumu, lai varētu turpināt pavadzīmes ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="a7ef2-134">Atsaukt un veikt korekcijas</span><span class="sxs-lookup"><span data-stu-id="a7ef2-134">Reverse and make adjustments</span></span>

<span data-ttu-id="a7ef2-135">Atsauciet visu, kas tika iegrāmatots kravai (piemēram, pavadzīmi, kravas apstiprinājumu un darbu), veiciet pārdošanas pasūtījuma korekcijas, vēlreiz izlaidiet pasūtījumu nosūtīšanai uz noliktavu un veiciet nosūtīšanas procedūru.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="a7ef2-136">Izmantojiet šo procedūru, lai atceltu pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="a7ef2-137">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a7ef2-138">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atcelt pavadzīmes**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="a7ef2-139">Izmantojiet sekojošo procedūru, lai atsauktu sūtījuma apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="a7ef2-140">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a7ef2-141">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="a7ef2-142">Lai atsauktu darbu, izmantojiet šādu procedūru.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="a7ef2-143">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a7ef2-144">Darbību rūts cilnē **Kravas** grupā **Darbs** atlasiet **Atsaukt darbu**.</span><span class="sxs-lookup"><span data-stu-id="a7ef2-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
