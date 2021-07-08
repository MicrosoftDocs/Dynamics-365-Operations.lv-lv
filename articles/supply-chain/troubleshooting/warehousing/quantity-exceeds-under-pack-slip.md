---
title: Daudzums nesasniedz pasūtījuma procentus pavadzīmju ģenerēšanas laikā
description: Kad ģenerējat pavadzīmi,, izejošā krava ietver daudzumu, kas nesasniedz pasūtījuma procentus.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249134"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="fa882-103">Daudzums nesasniedz pasūtījuma procentus pavadzīmju ģenerēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="fa882-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="fa882-104">Kļūdas kods: SYS24921</span><span class="sxs-lookup"><span data-stu-id="fa882-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="fa882-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="fa882-105">Symptoms</span></span>

<span data-ttu-id="fa882-106">Kad ģenerējat pavadzīmi,, izejošā krava ietver daudzumu, kas nesasniedz pasūtījuma procentus.</span><span class="sxs-lookup"><span data-stu-id="fa882-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="fa882-107">Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="fa882-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="fa882-108">Nepilns pasūtījums rindā ir %1 %, bet atļauts ir tikai %2 %.</span><span class="sxs-lookup"><span data-stu-id="fa882-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="fa882-109">Tādēļ kravas pavadzīmi nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="fa882-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="fa882-110">Iemesls</span><span class="sxs-lookup"><span data-stu-id="fa882-110">Cause</span></span>

<span data-ttu-id="fa882-111">Kravas vai sūtījuma izdotais daudzums nesasniedz pasūtīto daudzumu, un tas nav pasūtījuma procentuālās vērtības diapazonā.</span><span class="sxs-lookup"><span data-stu-id="fa882-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="fa882-112">Novēršana</span><span class="sxs-lookup"><span data-stu-id="fa882-112">Resolution</span></span>

<span data-ttu-id="fa882-113">Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="fa882-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="fa882-114">Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="fa882-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="fa882-115">Pielāgojiet procentuālās vērtības nesasniegšanu.</span><span class="sxs-lookup"><span data-stu-id="fa882-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="fa882-116">Atsaukt un veikt korekcijas.</span><span class="sxs-lookup"><span data-stu-id="fa882-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="fa882-117">Pielāgojiet procentuālās vērtības nesasniegšanu</span><span class="sxs-lookup"><span data-stu-id="fa882-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="fa882-118">Izmantojiet šo procedūru, lai pielāgotu procentuālās vērtības nesasniegšanu.</span><span class="sxs-lookup"><span data-stu-id="fa882-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="fa882-119">Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="fa882-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="fa882-120">Atlasiet pārdošanas pasūtījumu, kuram nevar grāmatot kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="fa882-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="fa882-121">Cilnē **Pārdošanas pasūtījuma rindas** atlasiet pārdošanas pasūtījuma rindu krājumam, kas nesasniedz pasūtījuma procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="fa882-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="fa882-122">Cilnē  **Rindu detāļas** atlasiet **Piegāde**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="fa882-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="fa882-123">Iestatiet lauku **Pasūtījuma nesasniegšanu** uz lielāku procentuālo vērtību, kas atbilst izdotajam daudzumam attiecībā pret kravas daudzumu, lai varētu turpināt pavadzīmes ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="fa882-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="fa882-124">Atsaukt un veikt korekcijas</span><span class="sxs-lookup"><span data-stu-id="fa882-124">Reverse and make adjustments</span></span>

<span data-ttu-id="fa882-125">Atsauciet visu, kas tika iegrāmatots kravai (piemēram, pavadzīmi, kravas apstiprinājumu un darbu), veiciet pārdošanas pasūtījuma korekcijas, vēlreiz izlaidiet pasūtījumu nosūtīšanai uz noliktavu un veiciet nosūtīšanas procedūru.</span><span class="sxs-lookup"><span data-stu-id="fa882-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="fa882-126">Izmantojiet šo procedūru, lai atceltu pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="fa882-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="fa882-127">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="fa882-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="fa882-128">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atcelt pavadzīmes**.</span><span class="sxs-lookup"><span data-stu-id="fa882-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="fa882-129">Izmantojiet sekojošo procedūru, lai atsauktu sūtījuma apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="fa882-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="fa882-130">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="fa882-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="fa882-131">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="fa882-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="fa882-132">Lai atsauktu darbu, izmantojiet šādu procedūru.</span><span class="sxs-lookup"><span data-stu-id="fa882-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="fa882-133">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="fa882-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="fa882-134">Darbību rūts cilnē **Kravas** grupā **Darbs** atlasiet **Atsaukt darbu**.</span><span class="sxs-lookup"><span data-stu-id="fa882-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
