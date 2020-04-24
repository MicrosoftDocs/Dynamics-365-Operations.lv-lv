---
title: Konfigurēt programmas lauku nosaukumus programmā Noliktava
description: Šajā tēmā ir aprakstīts, kā definēt un konfigurēt noliktavu programmas lauku nosaukumus un prioritātes programmatūrā Dynamics 365 Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9b02b93895757580b323a4cd891909d5551ea55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205763"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="b8b82-103">Konfigurēt programmas lauku nosaukumus programmā Noliktava</span><span class="sxs-lookup"><span data-stu-id="b8b82-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8b82-104">Šajā tēmā ir aprakstīts, kā definēt un konfigurēt noliktavu programmas lauku nosaukumus un prioritātes programmatūrā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8b82-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="b8b82-105">Šī tēma attiecas uz moduļa Noliktavas vadība līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="b8b82-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="b8b82-106">Tā neattiecas uz moduļa Krājumu vadība līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="b8b82-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="b8b82-107">Noliktava ir lietojumprogramma, ko varat izmantot noliktavas uzdevumu veikšanai.</span><span class="sxs-lookup"><span data-stu-id="b8b82-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="b8b82-108">Varat definēt un konfigurēt programmā lietoto lauku nosaukumus, kā arī konfigurēt prioritāti, kādai šie lauku nosaukumi ir jāpiešķir.</span><span class="sxs-lookup"><span data-stu-id="b8b82-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="b8b82-109">Šajā tēmā ir paskaidrots, kā definēt un konfigurēt šos noliktavu programmas lauku nosaukumus un prioritātes un kā tie tiek izmantoti programmā Noliktava.</span><span class="sxs-lookup"><span data-stu-id="b8b82-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="b8b82-110">Detalizētu informāciju par to, kā konfigurēt savienojumu ar programmu Noliktava, skatiet apmācībā [Programmas Noliktava instalēšanas un konfigurēšanas pārskats](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="b8b82-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the Warehousing app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="b8b82-111">Konfigurēt noliktavas programmas lauku nosaukumus</span><span class="sxs-lookup"><span data-stu-id="b8b82-111">Configure warehouse app field names</span></span>

<span data-ttu-id="b8b82-112">Kad lietojat programmu Noliktava mobilajā ierīcē, lapā **Noliktavas programmu lauku nosaukumi** varat konfigurēt to, kā ierīcē ir jārāda metadati.</span><span class="sxs-lookup"><span data-stu-id="b8b82-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="b8b82-113">Jaunā uzņēmumā atlasiet opciju **Izveidot noklusējuma iestatījumus**, lai ģenerētu visus lauku nosaukumus, kas tiks izmantoti noliktavas mobilo ierīču darbplūsmās, un pēc tam piešķiriet tiem vajadzīgo ievades režīmu un ievades veidu.</span><span class="sxs-lookup"><span data-stu-id="b8b82-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="b8b82-114">Kad ir ģenerēti visi lauku nosaukumi, varat atlasīt tālāk norādītās ievades opcijas.</span><span class="sxs-lookup"><span data-stu-id="b8b82-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8b82-115">Opcija</span><span class="sxs-lookup"><span data-stu-id="b8b82-115">Option</span></span></th>
<th><span data-ttu-id="b8b82-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b8b82-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8b82-117">Vēlamais ievades režīms</span><span class="sxs-lookup"><span data-stu-id="b8b82-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="b8b82-118">Šī opcija nosaka, vai atlasītajam lauka nosaukumam ir jārāda skenēšanas lauks vai manuālas ievades lauks.</span><span class="sxs-lookup"><span data-stu-id="b8b82-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="b8b82-119">Šī opcija noder, lai laukus nodalītu atkarībā no tā, vai laukam ir jāizmanto svītrkodi.</span><span class="sxs-lookup"><span data-stu-id="b8b82-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="b8b82-120"><strong>Piezīme.</strong> Ja svītrkods ir nenolasāms vai bojāts, tad lauku nosaukumiem, kuru vēlamais ievades režīms ir iestatīts uz <strong>Skenēšana</strong>, informāciju varat ievadīt arī manuāli.</span><span class="sxs-lookup"><span data-stu-id="b8b82-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8b82-121">Ievades tips</span><span class="sxs-lookup"><span data-stu-id="b8b82-121">Input type</span></span></td>
<td><span data-ttu-id="b8b82-122">Šī opcija nosaka, kāds ievades tips ir jālieto atlasītajam lauka nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="b8b82-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="b8b82-123">Ir pieejamas četras tālāk aprakstītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="b8b82-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="b8b82-124"><strong>Atlase</strong> - ietver sarakstu ar opcijām, no kurām varat izvēlēties.</span><span class="sxs-lookup"><span data-stu-id="b8b82-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="b8b82-125">Izmantojot šo opciju, lauku nosaukumus nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b8b82-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="b8b82-126"><strong>Datums</strong> - lauku nosaukumi, kas ir norādīti kā datumi, rādīs datuma formātu ar etiķeti.</span><span class="sxs-lookup"><span data-stu-id="b8b82-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="b8b82-127">Šī opcija noliktavas darbiniekiem palīdz ieraudzīt, kādā formātā ir jāievada datums.</span><span class="sxs-lookup"><span data-stu-id="b8b82-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="b8b82-128">Izmantojot šo opciju, lauku nosaukumus nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b8b82-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="b8b82-129"><strong>Alfa</strong> - ja ir atlasīta šī opcija, tad tiek izmantota ierīces tastatūra, programmā manuāli ievadot informāciju.</span><span class="sxs-lookup"><span data-stu-id="b8b82-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="b8b82-130">Tastatūras funkcionalitāti var mainīt atkarībā no tā, kura ierīce tiek lietota.</span><span class="sxs-lookup"><span data-stu-id="b8b82-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="b8b82-131"><strong>Skaitlisks</strong> - lauku nosaukumiem, kas izmanto tikai skaitlisko ievadi, varat atlasīt šo opciju, lai ar ievades lauku rādītu pielāgotu cipartastatūru, nevis ierīces tastatūru.</span><span class="sxs-lookup"><span data-stu-id="b8b82-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="b8b82-132">Konfigurēt noliktavas programmas lauku prioritāti</span><span class="sxs-lookup"><span data-stu-id="b8b82-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="b8b82-133">Lapā **Noliktavas programmas lauku prioritāte** lauku nosaukumus varat salikt dažādās prioritāšu grupās.</span><span class="sxs-lookup"><span data-stu-id="b8b82-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="b8b82-134">Šādi varat izlemt, kāda informācija ir jārāda galvenajā uzdevumu lapā, kad noliktavas darbinieki izpilda uzdevumus, izmantojot šo programmu.</span><span class="sxs-lookup"><span data-stu-id="b8b82-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="b8b82-135">Ja noklikšķināt uz **Izveidot noklusējuma iestatījumus**, tiek ģenerēta prioritāšu grupu noklusējuma kopa.</span><span class="sxs-lookup"><span data-stu-id="b8b82-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="b8b82-136">Varat izveidot tik prioritāšu grupu, cik vien nepieciešams, bet uzdevumu lapā tiks rādītas tikai trīs prioritāšu grupas.</span><span class="sxs-lookup"><span data-stu-id="b8b82-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="b8b82-137">Kad no sistēmas uz programmu tiek sūtīti metadati, katram laukam tiek piešķirta relatīva prioritāte atkarībā no lauka prioritāšu grupas un programmas uzdevumu lapā tiek parādītas pirmās trīs metadatos ietvertās prioritāšu grupas.</span><span class="sxs-lookup"><span data-stu-id="b8b82-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="b8b82-138">Pārējie metadati tiks rādīti sekundārās informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="b8b82-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="b8b82-139">Nākamajā tabulā ir parādīts piemērs ar piecām prioritāšu grupām.</span><span class="sxs-lookup"><span data-stu-id="b8b82-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8b82-140">Prioritātes grupa</span><span class="sxs-lookup"><span data-stu-id="b8b82-140">Priority group</span></span></th>
<th><span data-ttu-id="b8b82-141">Piešķirtie lauki</span><span class="sxs-lookup"><span data-stu-id="b8b82-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="b8b82-142">10. prioritāte</span><span class="sxs-lookup"><span data-stu-id="b8b82-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="b8b82-143">Objekts</span><span class="sxs-lookup"><span data-stu-id="b8b82-143">Item</span></span></li>
<li><span data-ttu-id="b8b82-144">Daudzums</span><span class="sxs-lookup"><span data-stu-id="b8b82-144">Quantity</span></span></li>
<li><span data-ttu-id="b8b82-145">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="b8b82-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="b8b82-146">20. prioritāte</span><span class="sxs-lookup"><span data-stu-id="b8b82-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="b8b82-147">Klastera pozīcija</span><span class="sxs-lookup"><span data-stu-id="b8b82-147">Cluster position</span></span></li>
<li><span data-ttu-id="b8b82-148">Klasteris</span><span class="sxs-lookup"><span data-stu-id="b8b82-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="b8b82-149">30. prioritāte</span><span class="sxs-lookup"><span data-stu-id="b8b82-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="b8b82-150">Preces apraksts</span><span class="sxs-lookup"><span data-stu-id="b8b82-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="b8b82-151">40. prioritāte</span><span class="sxs-lookup"><span data-stu-id="b8b82-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="b8b82-152">Konfigurācija</span><span class="sxs-lookup"><span data-stu-id="b8b82-152">Configuration</span></span></li>
<li><span data-ttu-id="b8b82-153">krāsa</span><span class="sxs-lookup"><span data-stu-id="b8b82-153">Color</span></span></li>
<li><span data-ttu-id="b8b82-154">izmērs</span><span class="sxs-lookup"><span data-stu-id="b8b82-154">Size</span></span></li>
<li><span data-ttu-id="b8b82-155">Stils</span><span class="sxs-lookup"><span data-stu-id="b8b82-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="b8b82-156">50. prioritāte</span><span class="sxs-lookup"><span data-stu-id="b8b82-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="b8b82-157">Novietojums</span><span class="sxs-lookup"><span data-stu-id="b8b82-157">Location</span></span></li>
<li><span data-ttu-id="b8b82-158">Numura zīme</span><span class="sxs-lookup"><span data-stu-id="b8b82-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b8b82-159">Piemēram, kad noliktavas darbinieks izpilda kādu uzdevumu mobilajā ierīcē, ja programmā rādītie metadati sastāv no šādiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="b8b82-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="b8b82-160">Objekts</span><span class="sxs-lookup"><span data-stu-id="b8b82-160">Item</span></span>
-   <span data-ttu-id="b8b82-161">Daudzums</span><span class="sxs-lookup"><span data-stu-id="b8b82-161">Quantity</span></span>
-   <span data-ttu-id="b8b82-162">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="b8b82-162">Unit of measure</span></span>
-   <span data-ttu-id="b8b82-163">Preces apraksts</span><span class="sxs-lookup"><span data-stu-id="b8b82-163">Item description</span></span>
-   <span data-ttu-id="b8b82-164">Izmērs un novietojums</span><span class="sxs-lookup"><span data-stu-id="b8b82-164">Size and Location</span></span>

<span data-ttu-id="b8b82-165">Pamatojoties uz iepriekšējā tabulā iestatīto noliktavas programmas lauku prioritāti, uzdevumu lapā tiek rādītas šādas 3 informācijas rindas:</span><span class="sxs-lookup"><span data-stu-id="b8b82-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="b8b82-166">1. rinda: Prece, Daudzums, Mērvienība</span><span class="sxs-lookup"><span data-stu-id="b8b82-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="b8b82-167">2. rinda: Preces apraksts</span><span class="sxs-lookup"><span data-stu-id="b8b82-167">Row 2: Item description</span></span>
-   <span data-ttu-id="b8b82-168">3. rinda: Izmērs</span><span class="sxs-lookup"><span data-stu-id="b8b82-168">Row 3: Size</span></span>

<span data-ttu-id="b8b82-169">Atlikušie metadati, piemēram, Novietojums, netiks rādīti uzdevumu lapā, bet tiks rādīti informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="b8b82-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="b8b82-170">Papildinformāciju un lietotāja interfeisa piemērus skatiet emuāra ziņā [Paziņojums par Finance and Operations — Noliktava](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="b8b82-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="b8b82-171">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b8b82-171">Additional resources</span></span>
--------

[<span data-ttu-id="b8b82-172">Instalēt un konfigurēt Noliktavu lietojumprogrammas pārskatu</span><span class="sxs-lookup"><span data-stu-id="b8b82-172">Install and configure the Warehousing app overview</span></span>](install-configure-warehousing-app.md)
