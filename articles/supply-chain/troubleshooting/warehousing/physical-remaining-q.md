---
title: Vienības fiziskais atlikušais daudzums nedrīkst būt nulle
description: Izveidojot pavadzīmi, tai piegādāto datu krājumu daudzums nav nulle, bet pārdošanas daudzums ir nulle.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248792"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="3e0ff-103">Vienības fiziskais atlikušais daudzums nedrīkst būt nulle</span><span class="sxs-lookup"><span data-stu-id="3e0ff-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="3e0ff-104">Kļūdas kods: SYS19591</span><span class="sxs-lookup"><span data-stu-id="3e0ff-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="3e0ff-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="3e0ff-105">Symptoms</span></span>

<span data-ttu-id="3e0ff-106">Izveidojot pavadzīmi, tai piegādāto datu krājumu daudzums nav nulle, bet pārdošanas daudzums ir nulle.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="3e0ff-107">Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="3e0ff-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="3e0ff-108">Vienības %1 fiziskais atlikums nedrīkst būt nulle.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="3e0ff-109">Tādēļ kravas pavadzīmi nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="3e0ff-110">Iemesls</span><span class="sxs-lookup"><span data-stu-id="3e0ff-110">Cause</span></span>

<span data-ttu-id="3e0ff-111">Sistēma aprēķina fizisko atlikušo daudzumu krājumu uzskaites vienībā un fizisko atlikušo daudzumu nosūtīšanas vienībā.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="3e0ff-112">Ja sistēma konstatē, ka fiziskais atlikušais daudzums nosūtīšanas vienībā ir 0 (nulle), bet fiziskais atlikušais daudzums krājumu uzskaites vienībā nav 0, pavadzīmi nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="3e0ff-113">Piemēram, šī problēma var rasties, ja pārdošanas vienība un krājuma uzskaites vienība atšķiras un vienību pārveidošana nav precīza.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="3e0ff-114">Novēršana</span><span class="sxs-lookup"><span data-stu-id="3e0ff-114">Resolution</span></span>

<span data-ttu-id="3e0ff-115">Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="3e0ff-116">Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="3e0ff-117">Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="3e0ff-118">Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez noapaļošanas problēmām.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="3e0ff-119">Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="3e0ff-120">Pārliecinieties, vai krājumu mērvienība ir mazāka nekā pārdošanas mērvienība.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="3e0ff-121">Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt</span><span class="sxs-lookup"><span data-stu-id="3e0ff-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="3e0ff-122">Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="3e0ff-123">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="3e0ff-124">Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="3e0ff-125">Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="3e0ff-126">Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="3e0ff-127">Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="3e0ff-128">Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="3e0ff-129">Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="3e0ff-130">Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez noapaļošanas problēmām</span><span class="sxs-lookup"><span data-stu-id="3e0ff-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="3e0ff-131">Izmantojiet šo procedūru, lai pārskatītu kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez noapaļošanas problēmām.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="3e0ff-132">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="3e0ff-133">Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="3e0ff-134">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="3e0ff-135">Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz pasūtījuma pārsniegumu.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="3e0ff-136">Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="3e0ff-137">Cilnē  **Rindu detāļas** atlasiet **Pasūtījums**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="3e0ff-138">Iestatiet lauku **Daudzums** uz izdoto daudzumu (t.i., uz lauka **Darba izveidotā daudzuma** vērtību), lai varētu turpināt pavadzīmes ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="3e0ff-139">Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti</span><span class="sxs-lookup"><span data-stu-id="3e0ff-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="3e0ff-140">Izmantojiet šo procedūru, lai pārskatītu kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="3e0ff-141">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="3e0ff-142">Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="3e0ff-143">Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas rada problēmu.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="3e0ff-144">Atzīmējiet lauku **Daudzums** un **Vienība** vērtību.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="3e0ff-145">Pārejiet uz sadaļu **Organizācijas administrēšana \> Vienības \> Vienības**.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="3e0ff-146">Atlasiet vienību, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="3e0ff-147">Pēc vajadzības pielāgojiet lauka **Decimālā precizitāte** vērtību.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="3e0ff-148">Pārliecinieties, vai krājumu mērvienība ir mazāka nekā pārdošanas mērvienība</span><span class="sxs-lookup"><span data-stu-id="3e0ff-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="3e0ff-149">Pārliecinieties, vai krājumu mērvienība ir mazāka nekā pārdošanas mērvienība.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="3e0ff-150">Ja nepieciešams, apsveriet iespēju atkārtoti konfigurēt krājuma mērvienību.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
