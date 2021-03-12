---
title: Kravu veidošanas un nosūtīšanas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar kravu veidošanu un nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994035"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="5e902-103">Kravu veidošanas un nosūtīšanas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="5e902-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e902-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar kravu veidošanu un nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5e902-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="5e902-105">Tiek parādīts šāds kļūdas ziņojums: "Nevar izveidot noslodzes rindu šai pasūtījuma rindai, jo tā ietver nederīgas krājumu dimensijas..."</span><span class="sxs-lookup"><span data-stu-id="5e902-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5e902-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5e902-106">Issue description</span></span>

<span data-ttu-id="5e902-107">Tiek parādīts šāds kļūdas ziņojums, mēģinot izlaist atgriešanas pārdošanas pasūtījumu uz noliktavu:</span><span class="sxs-lookup"><span data-stu-id="5e902-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="5e902-108">Nevar izveidot noslodzes rindu šai pasūtījuma rindai, jo tā ietver nederīgas krājumu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="5e902-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="5e902-109">Nevar atsaukties uz krājumu dimensijām, kas atrodas zem novietojuma dimensijas rezervāciju hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="5e902-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="5e902-110">Noņemiet nederīgās dimensijas no pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="5e902-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5e902-111">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5e902-111">Issue resolution</span></span>

<span data-ttu-id="5e902-112">Diemžēl prece pārdošanas atgriešanas procesam neatbalsta noslodzes apstrādi.</span><span class="sxs-lookup"><span data-stu-id="5e902-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="5e902-113">Tāpēc nevar nodot atgriešanas pārdošanas pasūtījumu noliktavai.</span><span class="sxs-lookup"><span data-stu-id="5e902-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="5e902-114">Pārdošanas pasūtījumu transakcijās nevar atsaukties uz krājumu dimensijām, kas atrodas zem **Novietojuma** dimensijas rezervāciju hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="5e902-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="5e902-115">Risinājums ir noņemt nederīgās dimensijas no pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="5e902-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="5e902-116">Tiek parādīts šāds kļūdas ziņojums: "Viena no rindām jau ir kravā.</span><span class="sxs-lookup"><span data-stu-id="5e902-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="5e902-117">Nevar izlaist uz noliktavu. "</span><span class="sxs-lookup"><span data-stu-id="5e902-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5e902-118">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5e902-118">Issue description</span></span>

<span data-ttu-id="5e902-119">Ja manuāli izveidojat kravas vai iestatāt procesu tā, ka krava jau ir izveidota, pirms tiek veikta pārdošanas pasūtījuma rindas ievade, pieņēmums ir tāds, ka nākamā izpilde tiks veikta manuāli, un tiks izmantota maršruta un vērtējums no kravas.</span><span class="sxs-lookup"><span data-stu-id="5e902-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="5e902-120">Citā iespējamajā scenārijā jūs mēģināt veikt automātisku izlaišanu noliktavā, bet kopuma procesam neizdevās izveidot darbu.</span><span class="sxs-lookup"><span data-stu-id="5e902-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="5e902-121">Tāpēc atvērts sūtījums vai krava joprojām tiek izveidota.</span><span class="sxs-lookup"><span data-stu-id="5e902-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="5e902-122">Šis atvērtais sūtījums vai krava pēc tam bloķē sekojošos mēģinājumus automātiski nodot pasūtījumu, līdz jūs vai nu dzēšat atvērto sūtījumu vai kravu, vai manuāli pārstrādājiet kopumu.</span><span class="sxs-lookup"><span data-stu-id="5e902-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5e902-123">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5e902-123">Issue resolution</span></span>

<span data-ttu-id="5e902-124">Var veikt izlaišanu no pārdošanas pasūtījuma lapas vai automātiski izlaist no izlaišanas pārdošanas pasūtījuma lapas, tikai tad, ja pirms nodošanas noliktavai neeksistē neviena krava.</span><span class="sxs-lookup"><span data-stu-id="5e902-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="5e902-125">Krava tiks automātiski izveidota pēc kopuma apstrādes.</span><span class="sxs-lookup"><span data-stu-id="5e902-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="5e902-126">Tiek parādīts šāds kļūdas ziņojums: "Nevar apstrādāt piegādes pavadzīmes labojumu.</span><span class="sxs-lookup"><span data-stu-id="5e902-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="5e902-127">Piegādes pavadzīmē ir ietverti tikai tie krājumi, kas ir pakļauti noliktavas pārvaldības procesiem, jo tie netiek atbalstīti ar Piegādes pavadzīmes labojumu."</span><span class="sxs-lookup"><span data-stu-id="5e902-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5e902-128">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5e902-128">Issue description</span></span>

<span data-ttu-id="5e902-129">Pēc tam, kad ir iegrāmatota piegādes pavadzīme, to nevar atcelt, jo poga **Atcelt** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="5e902-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="5e902-130">Jūs arī nevarat labot piegādes pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="5e902-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="5e902-131">Ja mēģināt, tiek parādīts šis kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="5e902-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5e902-132">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5e902-132">Issue resolution</span></span>

<span data-ttu-id="5e902-133">Lai labotu grāmatotās pavadzīmes krājumiem, kas ir iespējoti papildu noliktavas pārvaldībai (WMS), jāveic grāmatošana no kravas, nevis tieši no pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="5e902-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="5e902-134">Kā var izveidot darbu no izejošajām kravām, nevis no kopumiem?</span><span class="sxs-lookup"><span data-stu-id="5e902-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="5e902-135">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5e902-135">Issue description</span></span>

<span data-ttu-id="5e902-136">Lūk, viens no veidiem, kā reproducēt šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="5e902-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="5e902-137">izveidojiet izejošo kravu, izmantojot pārdošanas pasūtījumu vai pārsūtīšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5e902-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="5e902-138">Izlaiž noslodzi nosūtīšanai uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5e902-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="5e902-139">Ievērojiet, ka izdošanas darbs vēl nav izveidots.</span><span class="sxs-lookup"><span data-stu-id="5e902-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5e902-140">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5e902-140">Issue resolution</span></span>

<span data-ttu-id="5e902-141">Ja, izlaižot noslodzi, darbs ir jāveido nekavējoties, ir attiecīgi jākonfigurē laidiena veidne.</span><span class="sxs-lookup"><span data-stu-id="5e902-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="5e902-142">Laidiena veidnē iestatiet šādas opcijas uz *Jā*:</span><span class="sxs-lookup"><span data-stu-id="5e902-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="5e902-143">Automatizēt kopuma izveidi</span><span class="sxs-lookup"><span data-stu-id="5e902-143">Automate wave creation</span></span>
- <span data-ttu-id="5e902-144">Apstrādāt kopumu, to pārvietojot uz noliktavu</span><span class="sxs-lookup"><span data-stu-id="5e902-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="5e902-145">Automatizēt kopuma izlaidi</span><span class="sxs-lookup"><span data-stu-id="5e902-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="5e902-146">Nav iespējams atkārtoti izlaist daļēji nosūtītu noslodzi.</span><span class="sxs-lookup"><span data-stu-id="5e902-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5e902-147">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5e902-147">Issue description</span></span>

<span data-ttu-id="5e902-148">Nevar izlaist daļēji nosūtītu kravu uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5e902-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="5e902-149">Kad veicat izlaišanu uz noliktavu, parādās ziņojums "Operācija pabeigta", bet nekas nenotiek, un atlikušajam daudzumam netiek izveidots neviens darbs.</span><span class="sxs-lookup"><span data-stu-id="5e902-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="5e902-150">Šī problēma rodas, kad izmantojat transportēšanas noslodzes funkcionalitāti un ir nepilnīga rezervācija.</span><span class="sxs-lookup"><span data-stu-id="5e902-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5e902-151">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5e902-151">Issue resolution</span></span>

<span data-ttu-id="5e902-152">[KB problēma 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Daļēji nosūtītas kravas var atkārtoti ielikt kopumā un atkārtoti apstrādāt") ir fiksēta [laidienā 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="5e902-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
