---
title: Ar noliktavas konfigurāciju saistīto problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, konfigurējot Microsoft Dynamics 365 Supply Chain Management.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646111"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="8e331-103">Ar noliktavas konfigurāciju saistīto problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="8e331-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e331-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, konfigurējot Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8e331-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="8e331-105">Tiek parādīts šāds kļūdas ziņojums: "Numura zīme vai novietojums nav derīgs."</span><span class="sxs-lookup"><span data-stu-id="8e331-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8e331-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8e331-106">Issue description</span></span>

<span data-ttu-id="8e331-107">Šis kļūdas ziņojums tiek parādīts, skenējot numura zīmes ID vai novietojumu.</span><span class="sxs-lookup"><span data-stu-id="8e331-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8e331-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8e331-108">Issue resolution</span></span>

<span data-ttu-id="8e331-109">Pārliecinieties, ka numura zīmes ID nav rezervējis kas cits.</span><span class="sxs-lookup"><span data-stu-id="8e331-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="8e331-110">Šī problēma parasti radās, kad vērtība, ko lietotājs skenēja noliktavas lietotnē, bija gan derīga atrašanās vieta, gan derīgs numura zīmes ID.</span><span class="sxs-lookup"><span data-stu-id="8e331-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="8e331-111">Tomēr šī problēma tika atrisināta versijā 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="8e331-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="8e331-112">Tiek parādīts šāds kļūdas ziņojums: "Šai numura zīmei ir jābūt norādītai šajā novietojumā."</span><span class="sxs-lookup"><span data-stu-id="8e331-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8e331-113">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8e331-113">Issue description</span></span>

<span data-ttu-id="8e331-114">Šis kļūdas ziņojums tiek parādīts, ja izveidojat pārsūtīšanas pasūtījumu, izmantojot noliktavu, kas ir aktivizēta papildu noliktavas pārvaldībai (WMS), un pēc tam, kad darbs ir pabeigts, jūs mēģināt apstiprināt kravu.</span><span class="sxs-lookup"><span data-stu-id="8e331-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8e331-115">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8e331-115">Issue resolution</span></span>

<span data-ttu-id="8e331-116">**Noklusējuma kvīts novietojuma** lauks ir tukšs noliktavas "no" tranzīta noliktavai.</span><span class="sxs-lookup"><span data-stu-id="8e331-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="8e331-117">Lai labotu šo problēmu, norādiet noklusēto ieejas plūsmas vietu tranzīta noliktavā.</span><span class="sxs-lookup"><span data-stu-id="8e331-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="8e331-118">Pārliecinieties, vai šī atrašanās vieta ir numura zīmes kontrolēta.</span><span class="sxs-lookup"><span data-stu-id="8e331-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="8e331-119">Tiek parādīts šāds kļūdas ziņojums: "Nevar izveidot darba veidnes rindu krājumu statusa maiņai, jo darba veids nav derīgs.</span><span class="sxs-lookup"><span data-stu-id="8e331-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="8e331-120">Atlasiet citu darba veidu."</span><span class="sxs-lookup"><span data-stu-id="8e331-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8e331-121">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8e331-121">Issue description</span></span>

<span data-ttu-id="8e331-122">Darba veidnei nevar atlasīt *Krājumu statusa izmaiņas* kolonnas **Darba veids** sadaļā **Darba veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="8e331-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8e331-123">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8e331-123">Issue resolution</span></span>

<span data-ttu-id="8e331-124">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="8e331-124">This behavior is by design.</span></span> <span data-ttu-id="8e331-125">*Krājumu statusa maiņas* darba veidu izmanto tikai sistēmas procesi.</span><span class="sxs-lookup"><span data-stu-id="8e331-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="8e331-126">To nevar konfigurēt.</span><span class="sxs-lookup"><span data-stu-id="8e331-126">It can't be configured.</span></span> <span data-ttu-id="8e331-127">Tā kā darba veidu saraksts ir fiksēts kā uzskaitījums, papildu ievades nevar filtrēt no **Darba veida** nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="8e331-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="8e331-128">Tiek parādīts šāds kļūdas ziņojums: "Daudzums nav derīgs 1% vienībai."</span><span class="sxs-lookup"><span data-stu-id="8e331-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8e331-129">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8e331-129">Issue description</span></span>

<span data-ttu-id="8e331-130">Daudzums nav derīgs *ea* vienībai, ja ir izdošanas darbs, kuram vienā vietā ir vairākas numura zīmes.</span><span class="sxs-lookup"><span data-stu-id="8e331-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8e331-131">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8e331-131">Issue resolution</span></span>

<span data-ttu-id="8e331-132">Pārbaudiet, vai lauki **Vienības secības grupas ID** un **Vienības konvertēšana** izlaistajā precē vai preces variantā tiek iestatīti pareizi.</span><span class="sxs-lookup"><span data-stu-id="8e331-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="8e331-133">Ņemiet vērā, ka kļūdas ziņojums ir uzlabots versijā 10.0.15 (skatiet [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="8e331-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="8e331-134">Jaunais kļūdas ziņojums ir "Daudzums nav derīgs.</span><span class="sxs-lookup"><span data-stu-id="8e331-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="8e331-135">Paredzamais %1 %2."</span><span class="sxs-lookup"><span data-stu-id="8e331-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="8e331-136">Novietojuma direktīvās, kas attiecas uz pārdošanas pasūtījuma izvietošanas darbu, vairāku SKU opcija nenovērtē vairākas atrašanās vietas direktīvas darbības.</span><span class="sxs-lookup"><span data-stu-id="8e331-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8e331-137">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8e331-137">Issue description</span></span>

<span data-ttu-id="8e331-138">*Pārdošanas pasūtījuma* darba pasūtījuma veida un *Izvietošanas* darba veida novietojuma direktīvas nenovērtē vairākas novietojuma direktīvas, kad ir atlasīta opcija. **Vairāki SKU**.</span><span class="sxs-lookup"><span data-stu-id="8e331-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="8e331-139">Tiek novērtēta tikai pirmā novietojuma direktīvas darbība.</span><span class="sxs-lookup"><span data-stu-id="8e331-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8e331-140">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8e331-140">Issue resolution</span></span>

<span data-ttu-id="8e331-141">Versijā 10.0.15 ir pievienots jauns līdzeklis *Novērtēt visas darbības vairāku SKU novietojuma direktīvām* (skatiet [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="8e331-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="8e331-142">Šis līdzeklis novērtē visas darbības vairāku SKU novietojuma direktīvām.</span><span class="sxs-lookup"><span data-stu-id="8e331-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="8e331-143">Ja jums ir nepieciešams šis līdzeklis, izmantojiet [funkciju pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="8e331-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="8e331-144">Nevar izmantot noliktavas programmu, lai veiktu daļēju izdošanu.</span><span class="sxs-lookup"><span data-stu-id="8e331-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8e331-145">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8e331-145">Issue description</span></span>

<span data-ttu-id="8e331-146">Pārdošanas un pārsūtīšanas pasūtījumiem nevar izlaist krājumus un veiktu daļēju izdošanu.</span><span class="sxs-lookup"><span data-stu-id="8e331-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8e331-147">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8e331-147">Issue resolution</span></span>

<span data-ttu-id="8e331-148">Lapā **Mobilās ierīces izvēlnes vienumi** katram izvēlnes elementam, kas iestatīts, lai apstrādātu pārdošanas pasūtījumus vai pārsūtīšanas pasūtījumus, iestatiet opciju **Atļaut sadalīt darbu** kopsavilkuma cilnē **Vispārīgi** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="8e331-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="8e331-149">Kā var veikt krājumu statusa izmaiņas daļējiem daudzuma darbiem?</span><span class="sxs-lookup"><span data-stu-id="8e331-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="8e331-150">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="8e331-150">Issue description</span></span>

<span data-ttu-id="8e331-151">Vēlaties veikt krājumu statusa izmaiņas daļējam paketes daudzumam.</span><span class="sxs-lookup"><span data-stu-id="8e331-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8e331-152">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="8e331-152">Issue resolution</span></span>

<span data-ttu-id="8e331-153">Lai ļautu darbiniekiem veikt šīs izmaiņas, varat izveidot izvēlnes elementu noliktavas programmai.</span><span class="sxs-lookup"><span data-stu-id="8e331-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="8e331-154">Izveidojiet (vai rediģējiet) izvēlnes vienumu lapā **Mobilās ierīces izvēlnes vienumi**, kam ir sekojošie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="8e331-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="8e331-155">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="8e331-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="8e331-156">**Izmantot esošo darbu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="8e331-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="8e331-157">**Darba izveides process:** *Kustība*</span><span class="sxs-lookup"><span data-stu-id="8e331-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="8e331-158">**Rādīt krājumu statusu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="8e331-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="8e331-159">Varat iestatīt citus laukus lapā pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="8e331-159">You can set other fields on the page as you require.</span></span>
