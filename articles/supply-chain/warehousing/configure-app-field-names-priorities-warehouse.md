---
title: Warehouse Management mobile programmas lauku konfigurēšana
description: Šajā tēmā ir aprakstīts, kā definēt un konfigurēt Warehouse Management mobile programmā atainotos lauku nosaukumus un prioritātes.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808826"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="30289-103">Warehouse Management mobile programmas lauku konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="30289-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30289-104">Šajā tēmā ir aprakstīts, kā definēt un konfigurēt Warehouse Management mobile programmā atainotos lauku nosaukumus un prioritātes.</span><span class="sxs-lookup"><span data-stu-id="30289-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="30289-105">Šī tēma attiecas uz Warehouse Management līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="30289-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="30289-106">Tā neattiecas uz moduļa Krājumu vadība līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="30289-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="30289-107">Warehouse Management mobile lietojumprogramma ir programma, ko varat izmantot noliktavas uzdevumu veikšanai.</span><span class="sxs-lookup"><span data-stu-id="30289-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="30289-108">Varat definēt un konfigurēt programmā lietoto lauku nosaukumus, kā arī konfigurēt prioritāti, kādai šie lauku nosaukumi ir jāpiešķir.</span><span class="sxs-lookup"><span data-stu-id="30289-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="30289-109">Šajā tēmā ir paskaidrots, kā definēt un konfigurēt šos Warehouse Management mobile programmas lauku nosaukumus un prioritātes un kā tie tiek izmantoti.</span><span class="sxs-lookup"><span data-stu-id="30289-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="30289-110">Konfigurēt noliktavas programmas lauku nosaukumus</span><span class="sxs-lookup"><span data-stu-id="30289-110">Configure warehouse app field names</span></span>

<span data-ttu-id="30289-111">Kad lietojat programmu Noliktava mobilajā ierīcē, lapā **Noliktavas programmu lauku nosaukumi** varat konfigurēt to, kā ierīcē ir jārāda metadati.</span><span class="sxs-lookup"><span data-stu-id="30289-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="30289-112">Jaunā uzņēmumā atlasiet opciju **Izveidot noklusējuma iestatījumus**, lai ģenerētu visus lauku nosaukumus, kas tiks izmantoti noliktavas mobilo ierīču darbplūsmās, un pēc tam piešķiriet tiem vajadzīgo ievades režīmu un ievades veidu.</span><span class="sxs-lookup"><span data-stu-id="30289-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="30289-113">Kad ir ģenerēti visi lauku nosaukumi, varat atlasīt tālāk norādītās ievades opcijas.</span><span class="sxs-lookup"><span data-stu-id="30289-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30289-114">Opcija</span><span class="sxs-lookup"><span data-stu-id="30289-114">Option</span></span></th>
<th><span data-ttu-id="30289-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="30289-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30289-116">Vēlamais ievades režīms</span><span class="sxs-lookup"><span data-stu-id="30289-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="30289-117">Šī opcija nosaka, vai atlasītajam lauka nosaukumam ir jārāda skenēšanas lauks vai manuālas ievades lauks.</span><span class="sxs-lookup"><span data-stu-id="30289-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="30289-118">Šī opcija noder, lai laukus nodalītu atkarībā no tā, vai laukam ir jāizmanto svītrkodi.</span><span class="sxs-lookup"><span data-stu-id="30289-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="30289-119"><strong>Piezīme.</strong> Ja svītrkods ir nenolasāms vai bojāts, tad lauku nosaukumiem, kuru vēlamais ievades režīms ir iestatīts uz <strong>Skenēšana</strong>, informāciju varat ievadīt arī manuāli.</span><span class="sxs-lookup"><span data-stu-id="30289-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30289-120">Ievades tips</span><span class="sxs-lookup"><span data-stu-id="30289-120">Input type</span></span></td>
<td><span data-ttu-id="30289-121">Šī opcija nosaka, kāds ievades tips ir jālieto atlasītajam lauka nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="30289-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="30289-122">Ir pieejamas četras tālāk aprakstītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="30289-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="30289-123"><strong>Atlase</strong> - ietver sarakstu ar opcijām, no kurām varat izvēlēties.</span><span class="sxs-lookup"><span data-stu-id="30289-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="30289-124">Izmantojot šo opciju, lauku nosaukumus nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="30289-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="30289-125"><strong>Datums</strong> - lauku nosaukumi, kas ir norādīti kā datumi, rādīs datuma formātu ar etiķeti.</span><span class="sxs-lookup"><span data-stu-id="30289-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="30289-126">Šī opcija noliktavas darbiniekiem palīdz ieraudzīt, kādā formātā ir jāievada datums.</span><span class="sxs-lookup"><span data-stu-id="30289-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="30289-127">Izmantojot šo opciju, lauku nosaukumus nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="30289-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="30289-128"><strong>Alfa</strong> - ja ir atlasīta šī opcija, tad tiek izmantota ierīces tastatūra, programmā manuāli ievadot informāciju.</span><span class="sxs-lookup"><span data-stu-id="30289-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="30289-129">Tastatūras funkcionalitāti var mainīt atkarībā no tā, kura ierīce tiek lietota.</span><span class="sxs-lookup"><span data-stu-id="30289-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="30289-130"><strong>Skaitlisks</strong> - lauku nosaukumiem, kas izmanto tikai skaitlisko ievadi, varat atlasīt šo opciju, lai ar ievades lauku rādītu pielāgotu cipartastatūru, nevis ierīces tastatūru.</span><span class="sxs-lookup"><span data-stu-id="30289-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="30289-131">Konfigurēt noliktavas programmas lauku prioritāti</span><span class="sxs-lookup"><span data-stu-id="30289-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="30289-132">Lapā **Noliktavas programmas lauku prioritāte** lauku nosaukumus varat salikt dažādās prioritāšu grupās.</span><span class="sxs-lookup"><span data-stu-id="30289-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="30289-133">Šādi varat izlemt, kāda informācija ir jārāda galvenajā uzdevumu lapā, kad noliktavas darbinieki izpilda uzdevumus, izmantojot šo programmu.</span><span class="sxs-lookup"><span data-stu-id="30289-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="30289-134">Ja noklikšķināt uz **Izveidot noklusējuma iestatījumus**, tiek ģenerēta prioritāšu grupu noklusējuma kopa.</span><span class="sxs-lookup"><span data-stu-id="30289-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="30289-135">Varat izveidot tik prioritāšu grupu, cik vien nepieciešams, bet uzdevumu lapā tiks rādītas tikai trīs prioritāšu grupas.</span><span class="sxs-lookup"><span data-stu-id="30289-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="30289-136">Kad no sistēmas uz programmu tiek sūtīti metadati, katram laukam tiek piešķirta relatīva prioritāte atkarībā no lauka prioritāšu grupas un programmas uzdevumu lapā tiek parādītas pirmās trīs metadatos ietvertās prioritāšu grupas.</span><span class="sxs-lookup"><span data-stu-id="30289-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="30289-137">Pārējie metadati tiks rādīti sekundārās informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="30289-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="30289-138">Nākamajā tabulā ir parādīts piemērs ar piecām prioritāšu grupām.</span><span class="sxs-lookup"><span data-stu-id="30289-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30289-139">Prioritātes grupa</span><span class="sxs-lookup"><span data-stu-id="30289-139">Priority group</span></span></th>
<th><span data-ttu-id="30289-140">Piešķirtie lauki</span><span class="sxs-lookup"><span data-stu-id="30289-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="30289-141">10. prioritāte</span><span class="sxs-lookup"><span data-stu-id="30289-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="30289-142">Objekts</span><span class="sxs-lookup"><span data-stu-id="30289-142">Item</span></span></li>
<li><span data-ttu-id="30289-143">Daudzums</span><span class="sxs-lookup"><span data-stu-id="30289-143">Quantity</span></span></li>
<li><span data-ttu-id="30289-144">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="30289-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="30289-145">20. prioritāte</span><span class="sxs-lookup"><span data-stu-id="30289-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="30289-146">Klastera pozīcija</span><span class="sxs-lookup"><span data-stu-id="30289-146">Cluster position</span></span></li>
<li><span data-ttu-id="30289-147">Klasteris</span><span class="sxs-lookup"><span data-stu-id="30289-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="30289-148">30. prioritāte</span><span class="sxs-lookup"><span data-stu-id="30289-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="30289-149">Preces apraksts</span><span class="sxs-lookup"><span data-stu-id="30289-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="30289-150">40. prioritāte</span><span class="sxs-lookup"><span data-stu-id="30289-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="30289-151">Konfigurācija</span><span class="sxs-lookup"><span data-stu-id="30289-151">Configuration</span></span></li>
<li><span data-ttu-id="30289-152">krāsa</span><span class="sxs-lookup"><span data-stu-id="30289-152">Color</span></span></li>
<li><span data-ttu-id="30289-153">izmērs</span><span class="sxs-lookup"><span data-stu-id="30289-153">Size</span></span></li>
<li><span data-ttu-id="30289-154">Stils</span><span class="sxs-lookup"><span data-stu-id="30289-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="30289-155">50. prioritāte</span><span class="sxs-lookup"><span data-stu-id="30289-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="30289-156">Novietojums</span><span class="sxs-lookup"><span data-stu-id="30289-156">Location</span></span></li>
<li><span data-ttu-id="30289-157">Numura zīme</span><span class="sxs-lookup"><span data-stu-id="30289-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="30289-158">Piemēram, kad noliktavas darbinieks izpilda kādu uzdevumu mobilajā ierīcē, ja programmā rādītie metadati sastāv no šādiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="30289-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="30289-159">Objekts</span><span class="sxs-lookup"><span data-stu-id="30289-159">Item</span></span>
-   <span data-ttu-id="30289-160">Daudzums</span><span class="sxs-lookup"><span data-stu-id="30289-160">Quantity</span></span>
-   <span data-ttu-id="30289-161">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="30289-161">Unit of measure</span></span>
-   <span data-ttu-id="30289-162">Preces apraksts</span><span class="sxs-lookup"><span data-stu-id="30289-162">Item description</span></span>
-   <span data-ttu-id="30289-163">Izmērs un novietojums</span><span class="sxs-lookup"><span data-stu-id="30289-163">Size and Location</span></span>

<span data-ttu-id="30289-164">Pamatojoties uz iepriekšējā tabulā iestatīto noliktavas programmas lauku prioritāti, uzdevumu lapā tiek rādītas šādas 3 informācijas rindas:</span><span class="sxs-lookup"><span data-stu-id="30289-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="30289-165">1. rinda: Prece, Daudzums, Mērvienība</span><span class="sxs-lookup"><span data-stu-id="30289-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="30289-166">2. rinda: Preces apraksts</span><span class="sxs-lookup"><span data-stu-id="30289-166">Row 2: Item description</span></span>
-   <span data-ttu-id="30289-167">3. rinda: Izmērs</span><span class="sxs-lookup"><span data-stu-id="30289-167">Row 3: Size</span></span>

<span data-ttu-id="30289-168">Atlikušie metadati, piemēram, Novietojums, netiks rādīti uzdevumu lapā, bet tiks rādīti informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="30289-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="30289-169">Papildinformāciju un lietotāja interfeisa piemērus skatiet emuāra ziņā [Paziņojums par Finance and Operations — Noliktava](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="30289-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="30289-170">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="30289-170">Additional resources</span></span>
--------

[<span data-ttu-id="30289-171">Noliktavas pārvaldības mobilās programmas instalēšana un savienošana</span><span class="sxs-lookup"><span data-stu-id="30289-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]