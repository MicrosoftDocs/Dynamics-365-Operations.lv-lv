---
title: Fiziskā daudzuma decimāldaļas noapaļošana nav pareiza
description: Izveidojot pavadzīmi, izejošā kravā ir daudzums, kas neatbilst decimāldaļas precizitātei, kas ir definēta vienībā.
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248793"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="14106-103">Fiziskā daudzuma decimāldaļas noapaļošana nav pareiza</span><span class="sxs-lookup"><span data-stu-id="14106-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="14106-104">Kļūdas kods: SYS19589</span><span class="sxs-lookup"><span data-stu-id="14106-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="14106-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="14106-105">Symptoms</span></span>

<span data-ttu-id="14106-106">Izveidojot pavadzīmi, izejošā kravā ir daudzums, kas neatbilst decimāldaļas precizitātei, kas ir definēta vienībā.</span><span class="sxs-lookup"><span data-stu-id="14106-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="14106-107">Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="14106-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="14106-108">Nepareizi noapaļotas vienības %1 fiziskā daudzuma decimāldaļas.</span><span class="sxs-lookup"><span data-stu-id="14106-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="14106-109">Tādēļ kravas pavadzīmi nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="14106-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="14106-110">Iemesls</span><span class="sxs-lookup"><span data-stu-id="14106-110">Cause</span></span>

<span data-ttu-id="14106-111">Sistēma novērtē, vai nosūtīšanas daudzuma decimālā noapaļošana atbilst nosūtīšanas vienībai definētajai decimāldaļas precizitātei.</span><span class="sxs-lookup"><span data-stu-id="14106-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="14106-112">Kad sistēma noapaļo nosūtāmo daudzumu līdz norādītajam decimāldaļu skaitam, ja tiek atrasts, ka noapaļotais nosūtīšanas daudzums neatbilst faktiskajam nosūtīšanas daudzumam, jūs nevarat ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="14106-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="14106-113">Piemēram, šī problēma var rasties, ja pārdošanas daudzums ir 1,75 kilogrami (kg), bet decimālā precizitāte ir iestatīta uz *1*.</span><span class="sxs-lookup"><span data-stu-id="14106-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="14106-114">Novēršana</span><span class="sxs-lookup"><span data-stu-id="14106-114">Resolution</span></span>

<span data-ttu-id="14106-115">Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="14106-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="14106-116">Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="14106-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="14106-117">Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez decimālskaitļiem un jebkurām citām noapaļošanas problēmām.</span><span class="sxs-lookup"><span data-stu-id="14106-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="14106-118">Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti.</span><span class="sxs-lookup"><span data-stu-id="14106-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="14106-119">Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez decimālskaitļiem un jebkurām citām noapaļošanas problēmām</span><span class="sxs-lookup"><span data-stu-id="14106-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="14106-120">Izmantojiet šo procedūru, lai pārskatītu kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez decimālskaitļiem un jebkurām citām noapaļošanas problēmām.</span><span class="sxs-lookup"><span data-stu-id="14106-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="14106-121">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="14106-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="14106-122">Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="14106-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="14106-123">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="14106-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="14106-124">Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas rada problēmu.</span><span class="sxs-lookup"><span data-stu-id="14106-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="14106-125">Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="14106-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="14106-126">Cilnē  **Rindu detāļas** atlasiet **Pasūtījums**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="14106-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="14106-127">Iestatiet lauku **Daudzums** uz izdoto daudzumu (t.i., uz lauka **Darba izveidotā daudzuma** vērtību), lai varētu turpināt pavadzīmes ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="14106-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="14106-128">Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti</span><span class="sxs-lookup"><span data-stu-id="14106-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="14106-129">Izmantojiet šo procedūru, lai pārskatītu kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti.</span><span class="sxs-lookup"><span data-stu-id="14106-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="14106-130">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="14106-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="14106-131">Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="14106-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="14106-132">Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas rada problēmu.</span><span class="sxs-lookup"><span data-stu-id="14106-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="14106-133">Atzīmējiet lauku **Daudzums** un **Vienība** vērtību.</span><span class="sxs-lookup"><span data-stu-id="14106-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="14106-134">Pārejiet uz sadaļu **Organizācijas administrēšana \> Vienības \> Vienības**.</span><span class="sxs-lookup"><span data-stu-id="14106-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="14106-135">Atlasiet vienību, kurai nevar ģenerēt pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="14106-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="14106-136">Pēc vajadzības pielāgojiet lauka **Decimālā precizitāte** vērtību.</span><span class="sxs-lookup"><span data-stu-id="14106-136">Adjust the value of the **Decimal precision** field as required.</span></span>
