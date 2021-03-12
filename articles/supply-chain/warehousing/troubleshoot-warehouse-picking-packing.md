---
title: Problēmu novēršana saistībā ar izdošanu un iepakošanu
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, izdodot un iepakojot programmā Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993938"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="8cb34-103">Problēmu novēršana saistībā ar izdošanu un iepakošanu</span><span class="sxs-lookup"><span data-stu-id="8cb34-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cb34-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, izdodot un iepakojot programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8cb34-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="8cb34-105">Tiek parādīts šāds kļūdas ziņojums: "Dimensijas novietojumu nevar atstāt tukšu, ja ir iestatīts dimensijas sērijas numurs."</span><span class="sxs-lookup"><span data-stu-id="8cb34-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cb34-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8cb34-106">Issue description</span></span>

<span data-ttu-id="8cb34-107">Šis kļūdas ziņojums tiek parādīts, ja izveidojat pārsūtīšanas pasūtījumu sērijas krājumam, izmantojot noliktavu, kas ir aktivizēta papildu noliktavas pārvaldībai (WMS), un pēc tam, kad darbs ir pabeigts, jūs mēģināt apstiprināt kravu.</span><span class="sxs-lookup"><span data-stu-id="8cb34-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cb34-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8cb34-108">Issue resolution</span></span>

<span data-ttu-id="8cb34-109">**Noklusējuma kvīts novietojuma** lauks ir tukšs noliktavas "no" tranzīta noliktavai.</span><span class="sxs-lookup"><span data-stu-id="8cb34-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="8cb34-110">Lai labotu šo problēmu, norādiet noklusēto ieejas plūsmas vietu tranzīta noliktavā.</span><span class="sxs-lookup"><span data-stu-id="8cb34-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="8cb34-111">Pārliecinieties, vai šī atrašanās vieta ir numura zīmes kontrolēta.</span><span class="sxs-lookup"><span data-stu-id="8cb34-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="8cb34-112">Tiek parādīts šāds kļūdas ziņojums: "Nederīga numura zīme."</span><span class="sxs-lookup"><span data-stu-id="8cb34-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cb34-113">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8cb34-113">Issue description</span></span>

<span data-ttu-id="8cb34-114">Šis kļūdas ziņojums tiek parādīts noliktavas programmā, skenējot numura zīmes ID.</span><span class="sxs-lookup"><span data-stu-id="8cb34-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cb34-115">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8cb34-115">Issue resolution</span></span>

<span data-ttu-id="8cb34-116">Pārliecinieties, vai numura zīmes ID atrodas numura zīmju tabulā, un ka krājumi un daudzumi numura zīmē ir pieejami (citiem vārdiem sakot, tie nav bloķēti).</span><span class="sxs-lookup"><span data-stu-id="8cb34-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="8cb34-117">Tiek parādīts šāds kļūdas ziņojums: "Lauks 'Kravas svars' (=-%1) var saturēt tikai pozitīvus skaitļus.</span><span class="sxs-lookup"><span data-stu-id="8cb34-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="8cb34-118">Labojumi ir atcelti."</span><span class="sxs-lookup"><span data-stu-id="8cb34-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cb34-119">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8cb34-119">Issue description</span></span>

<span data-ttu-id="8cb34-120">Šis kļūdas ziņojums tiek parādīts, ja, apstrādājot darbu no iepakošanas vietām uz sagatavošanas posmiem vai no sagatavošanas vietām uz doka vietām.</span><span class="sxs-lookup"><span data-stu-id="8cb34-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cb34-121">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8cb34-121">Issue resolution</span></span>

<span data-ttu-id="8cb34-122">Lai labotu šo problēmu, dodieties uz **Sistēmas administrēšana \> Periodiskie uzdevumi \> Datu bāzes \> Konsekvences pārbaude** un palaidiet procesu **Noliktavas kravas svara konsekvences pārbaudei**.</span><span class="sxs-lookup"><span data-stu-id="8cb34-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="8cb34-123">Tiek parādīts šāds kļūdas ziņojums: "Daudzums nav derīgs %1 vienībai."</span><span class="sxs-lookup"><span data-stu-id="8cb34-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cb34-124">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8cb34-124">Issue description</span></span>

<span data-ttu-id="8cb34-125">Šis kļūdas ziņojums tiek parādīts, mēģinot veikt *sadalītu izdošanu* vairākās partijās.</span><span class="sxs-lookup"><span data-stu-id="8cb34-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cb34-126">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8cb34-126">Issue resolution</span></span>

<span data-ttu-id="8cb34-127">Noliktavas darbiniekam jāizmanto *Īsā izdošanas* procedūra noliktavas programmā.</span><span class="sxs-lookup"><span data-stu-id="8cb34-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="8cb34-128">Ja mēģināt izvēlēties vairākas partijas no vienas un tās pašas vietas, varat arī izmantot **Pilno** opciju noliktavas programmā.</span><span class="sxs-lookup"><span data-stu-id="8cb34-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="8cb34-129">Nevar pārvietot krājumu uz atrašanās vietu, ko kontrolē numura zīme.</span><span class="sxs-lookup"><span data-stu-id="8cb34-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cb34-130">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8cb34-130">Issue description</span></span>

<span data-ttu-id="8cb34-131">Kravai nevar samazināt izdotos daudzumus.</span><span class="sxs-lookup"><span data-stu-id="8cb34-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cb34-132">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8cb34-132">Issue resolution</span></span>

<span data-ttu-id="8cb34-133">Agrākās versijās kravai nevar samazināt izdotos daudzumus.</span><span class="sxs-lookup"><span data-stu-id="8cb34-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="8cb34-134">Tomēr tagad varat neizdot uz novietojumu, ko kontrolē numura zīme.</span><span class="sxs-lookup"><span data-stu-id="8cb34-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="8cb34-135">Lapā **Samazināt izdoto daudzumu** ir jānorāda gan **Novietojuma** vērtība, gan **Numura zīmes** vērtība.</span><span class="sxs-lookup"><span data-stu-id="8cb34-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="8cb34-136">Vai var drukāt piegādes pavadzīmi vai iepakojuma saturu pēc noliktavas?</span><span class="sxs-lookup"><span data-stu-id="8cb34-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cb34-137">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8cb34-137">Issue description</span></span>

<span data-ttu-id="8cb34-138">Jūs vēlaties drukāt piegādes pavadzīmi vai iepakojuma saturu pēc noliktavas vai vietnes lapā **Darba audita veidnes rindas atjaunināšana**.</span><span class="sxs-lookup"><span data-stu-id="8cb34-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cb34-139">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8cb34-139">Issue resolution</span></span>

<span data-ttu-id="8cb34-140">Kad drukājat dokumentu, izmantojot drukas pārvaldības iestatījumus, ierobežojiet tvērumu (vietne/noliktava), izmantojot Drukas pārvaldību, nevis atlasot **Rediģēt drukas iestatījumus** lapā **Darba audita veidnes rindas atjaunināšana**.</span><span class="sxs-lookup"><span data-stu-id="8cb34-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="8cb34-141">Nevar atcelt pavadzīmi pēc tās grāmatošanas no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="8cb34-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cb34-142">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8cb34-142">Issue description</span></span>

<span data-ttu-id="8cb34-143">Kad izdošanas un nosūtīšanas procesi ir iespējoti WMS, pavadzīmi nevar atcelt pēc tās grāmatošanas no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="8cb34-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cb34-144">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8cb34-144">Issue resolution</span></span>

<span data-ttu-id="8cb34-145">Lai labotu grāmatotās pavadzīmes krājumiem, kas ir iespējoti WMS, grāmatošana ir jāveic no kravas, nevis tieši no pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="8cb34-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="8cb34-146">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="8cb34-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="8cb34-147">Parasti pārdošanas pasūtījums, kas ir izdots un nosūtīts ar noliktavas pārvaldības procesu starpniecību, var būt pavadzīmē atjaunināts no kravas vai sūtījuma un paša pārdošanas pasūtījuma dokumenta.</span><span class="sxs-lookup"><span data-stu-id="8cb34-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="8cb34-148">Tomēr, ja pavadzīmē atjauniniet pārdošanas pasūtījumu no pārdošanas pasūtījuma dokumenta, pavadzīmes atgriešana joprojām nevar tikt veikta no kravas vai pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="8cb34-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="8cb34-149">Tāpēc ieteicams izmantot pavadzīmes grāmatošanu no kravas.</span><span class="sxs-lookup"><span data-stu-id="8cb34-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="8cb34-150">Šādā gadījumā tiks aktivizēta atgriešana, kas ir jāveic no kravas.</span><span class="sxs-lookup"><span data-stu-id="8cb34-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="8cb34-151">Es saņemu sekojošu kļūdas ziņojumu: "Klasterim nav atrasts pietiekami darba."</span><span class="sxs-lookup"><span data-stu-id="8cb34-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cb34-152">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8cb34-152">Issue description</span></span>

<span data-ttu-id="8cb34-153">Ja izmantojat *Sistēmas virzītu klastera izdošanas* procesu, konfigurējot klastera profilu, kur, piemēram, var izdot 10 pozīcijas, process darbojas kā plānots, kad ir pietiekami daudz darba, lai izdotu 10 pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="8cb34-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="8cb34-154">Tomēr, ja izdošanai ir tikai astoņas pozīcijas, tiek parādīts šis kļūdas ziņojums, jo vienā klasterī nav pietiekami daudz darba.</span><span class="sxs-lookup"><span data-stu-id="8cb34-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cb34-155">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8cb34-155">Issue resolution</span></span>

<span data-ttu-id="8cb34-156">Lai labotu šo problēmu, rediģējiet klastera profilu un iestatiet opciju **Aktivizēt pozīcijas** uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="8cb34-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
