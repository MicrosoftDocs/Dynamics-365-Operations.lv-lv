---
title: Kvalitātes pārvaldības apskats
description: Šajā tēmā ir aprakstīts, kā varat izmantot kvalitātes pārvaldību programmā Dynamics 365 Supply Chain Management, lai palīdzētu uzlabot preču kvalitāti savā piegādes ķēdē.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2d51c659d9d06f075458359d81de978e7a6d14b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814402"
---
# <a name="quality-management-overview"></a><span data-ttu-id="617d8-103">Kvalitātes pārvaldības apskats</span><span class="sxs-lookup"><span data-stu-id="617d8-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="617d8-104">Šajā tēmā ir aprakstīts, kā varat izmantot kvalitātes pārvaldību programmā Dynamics 365 Supply Chain Management, lai palīdzētu uzlabot preču kvalitāti savā piegādes ķēdē.</span><span class="sxs-lookup"><span data-stu-id="617d8-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="617d8-105">Kvalitātes pārvaldība jums var palīdzēt pārvaldīt apgrozījumu laikus, kad strādājat ar nekondīcijas precēm, neatkarīgi no to izcelsmes vietas.</span><span class="sxs-lookup"><span data-stu-id="617d8-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="617d8-106">Tā kā diagnostikas tipi ir saistīti ar korekciju ziņošanu, Supply Chain Management var plānot uzdevumus, lai izlabotu problēmas un novērstu to atkārtošanos.</span><span class="sxs-lookup"><span data-stu-id="617d8-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="617d8-107">Papildus neatbilstības pārvaldības funkcionalitātei kvalitātes pārvaldība ietver arī funkcionalitāti problēmu izsekošanai pēc problēmas tipa (pat iekšējām problēmām) un risinājumu identificēšanai īstermiņā vai ilgtermiņā.</span><span class="sxs-lookup"><span data-stu-id="617d8-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="617d8-108">Statistika par galvenajiem darba kvalitātes rādītājiem (KPI) sniedz ieskatu par iepriekšējām neatbilstības problēmām un risinājumiem, kas tika izmantoti to labošanai.</span><span class="sxs-lookup"><span data-stu-id="617d8-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="617d8-109">Vēsturiskos datus varat izmantot, lai pārskatītu iepriekšējo kvalitātes pasākumu efektivitāti un noteiktu, kuri pasākumi ir piemēroti turpmākai izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="617d8-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="617d8-110">Kad iestatāt kvalitātes saistību, Supply Chain Management var ģenerēt kvalitātes pārbaudes pasūtījumus dažādiem biznesa procesiem, notikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="617d8-111">Šāda kvalitātes saistība var attiekties uz noteiktu krājumu, noteiktu krājumu grupu vai visiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="617d8-112">Kvalitātes pārvaldības lietošanas piemēri</span><span class="sxs-lookup"><span data-stu-id="617d8-112">Examples of the use of quality management</span></span>
<span data-ttu-id="617d8-113">Kvalitātes pārvaldība ir elastīga, un to var ieviest dažādos veidos, lai atbilstu noteiktu piegādes ķēdes darbību līmeņu prasībām.</span><span class="sxs-lookup"><span data-stu-id="617d8-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="617d8-114">Nākamajos piemēros ir parādīti šādu līdzekļu iespējamie lietojumi:</span><span class="sxs-lookup"><span data-stu-id="617d8-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="617d8-115">Automātiski uzsākt kvalitātes kontroles procesu, pamatojoties uz iepriekš definētiem kritērijiem (noliktavā reģistrējot kādu pirkšanas pasūtījumu no specifiska kreditora).</span><span class="sxs-lookup"><span data-stu-id="617d8-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="617d8-116">Bloķēt krājumus pārbaudes laikā, lai nepieļautu, ka tiek lietoti neapstiprināti krājumi (pirkšanas pasūtījuma daudzumu pilnīga bloķēšana).</span><span class="sxs-lookup"><span data-stu-id="617d8-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="617d8-117">Kā daļu no kvalitātes saistības lietot krājuma iztveršanu, lai definētu pašreizējo fizisko krājumu daudzumu, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="617d8-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="617d8-118">Iztveršana var būt balstīta uz fiksētiem daudzumiem vai procentiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="617d8-119">Izveidot kvalitātes pārbaudes pasūtījumus daļējām ieejas plūsmām.</span><span class="sxs-lookup"><span data-stu-id="617d8-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="617d8-120">Lai izveidotu kvalitātes pārbaudes pasūtījumu, kura pamatā ir daudzums, kas ir fiziski saņemts ar pasūtījumu, formā **Krājumu iztveršana** ir jāatzīmē izvēles rūtiņa **Pēc atjauninātā daudzuma**.</span><span class="sxs-lookup"><span data-stu-id="617d8-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="617d8-121">Izveidot testa tipus, kas ietver minimālās, maksimālās un mērķa testa vērtības, un veikt testēšanu kvalitātei pret kvantitāti, kur ir iepriekš definēti validēšanas rezultāti.</span><span class="sxs-lookup"><span data-stu-id="617d8-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="617d8-122">Norādīt pieņemamu kvalitātes līmeni (Acceptable Quality Level — AQL), lai kontrolētu kvalitātes mērījumu tolerances.</span><span class="sxs-lookup"><span data-stu-id="617d8-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="617d8-123">Norādīt pārbaudes operācijai nepieciešamos resursus, piemēram, testa apgabalu un testa instrumentus.</span><span class="sxs-lookup"><span data-stu-id="617d8-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="617d8-124">Darbs ar kvalitātes saistībām</span><span class="sxs-lookup"><span data-stu-id="617d8-124">Working with quality associations</span></span>
<span data-ttu-id="617d8-125">Biznesa process, kas izmanto kvalitātes saistību, var būt saistīts ar dažādiem avota dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem vai ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="617d8-126">Katrs kvalitātes saistības ieraksts nosaka testu kopu, pieņemamās kvalitātes līmeni (AQL) un iztveršanas plānu, kas tiek lietoti ģenerētajiem kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="617d8-127">Katrai biznesa procesa variācijai jums ir jādefinē kvalitātes saistības ieraksts.</span><span class="sxs-lookup"><span data-stu-id="617d8-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="617d8-128">Piemēram, varat iestatīt kvalitātes saistību, kas ģenerē kvalitātes pārbaudes pasūtījumu, kad tiek atjaunināta pirkšanas pasūtījuma produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="617d8-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="617d8-129">Atkarībā no izpildes plāna iestatījumiem pašu aktivizēšanas procesu var bloķēt, kamēr pastāv atvērts kvalitātes pārbaudes pasūtījums, vai iespējams bloķēt nākamos procesus, piemēram, pirkšanas pasūtījumu rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="617d8-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="617d8-130">**Piezīme.** Kamēr pastāv atvērti kvalitātes pārbaudes pasūtījumi, krājumu daudzumi tiek automātiski bloķēti no izsniegšanas.</span><span class="sxs-lookup"><span data-stu-id="617d8-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="617d8-131">Atkarībā no iestatījuma **Pilna bloķēšana** lapā **Krājumu iztveršana**, šis daudzums ir vai nu kvalitātes pasūtījumā norādītais daudzums, vai pirmdokumenta rindā norādītais daudzums.</span><span class="sxs-lookup"><span data-stu-id="617d8-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="617d8-132">Noteiktam biznesa procesam kvalitātes saistības ieraksts identificē notikumu un nosacījumus, kādiem tiek ģenerēts kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="617d8-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="617d8-133">Nosacījumi var attiekties uz vietu vai juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="617d8-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="617d8-134">Kvalitātes pārbaudes pasūtījumu, kur ir iesaistīti destruktīvie testi, var ģenerēt tikai tad, ja attiecīgajam notikumam pastāv rīcībā esoši krājumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="617d8-135">Nākamajos piemēros ir parādīts, kā kvalitātes saistības ieraksts tiek definēts katra darījumu procesa variācijām.</span><span class="sxs-lookup"><span data-stu-id="617d8-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="617d8-136">Katram piemēram nākamajā tabulā ir sniegts kopsavilkums par kvalitātes saistības ieraksta definētajiem notikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="617d8-137">Atsauces veids</span><span class="sxs-lookup"><span data-stu-id="617d8-137">Reference type</span></span></th>
<th><span data-ttu-id="617d8-138">Notikuma veids</span><span class="sxs-lookup"><span data-stu-id="617d8-138">Event type</span></span></th>
<th><span data-ttu-id="617d8-139">Izpilde</span><span class="sxs-lookup"><span data-stu-id="617d8-139">Execution</span></span></th>
<th><span data-ttu-id="617d8-140">Notikumu aizturēšana</span><span class="sxs-lookup"><span data-stu-id="617d8-140">Event blocking</span></span></th>
<th><span data-ttu-id="617d8-141">Dokumenta atsauce</span><span class="sxs-lookup"><span data-stu-id="617d8-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="617d8-142">Krājumi</span><span class="sxs-lookup"><span data-stu-id="617d8-142">Inventory</span></span></td>
<td><span data-ttu-id="617d8-143">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="617d8-143">Not applicable</span></span></td>
<td><span data-ttu-id="617d8-144">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="617d8-144">Not applicable</span></span></td>
<td><span data-ttu-id="617d8-145">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-145">None</span></span></td>
<td><span data-ttu-id="617d8-146">Visi</span><span class="sxs-lookup"><span data-stu-id="617d8-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="617d8-147">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="617d8-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="617d8-148">Izdošanas process ir ieplānots</span><span class="sxs-lookup"><span data-stu-id="617d8-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="617d8-149">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-149">Before</span></span></td>
<td><span data-ttu-id="617d8-150">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="617d8-151">Konkrēts ID, Grupa vai tikai Visi</span><span class="sxs-lookup"><span data-stu-id="617d8-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-152">Izdošanas process</span><span class="sxs-lookup"><span data-stu-id="617d8-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-153">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="617d8-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-154">Rēķins</span><span class="sxs-lookup"><span data-stu-id="617d8-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="617d8-155">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="617d8-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-156">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-156">Before</span></span></td>
<td><span data-ttu-id="617d8-157">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-158">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="617d8-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-159">Rēķins</span><span class="sxs-lookup"><span data-stu-id="617d8-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="617d8-160">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="617d8-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="617d8-161">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="617d8-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="617d8-162">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-162">Before</span></span></td>
<td><span data-ttu-id="617d8-163">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-164">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="617d8-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-165">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="617d8-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-166">Rēķins</span><span class="sxs-lookup"><span data-stu-id="617d8-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="617d8-167">Pēc</span><span class="sxs-lookup"><span data-stu-id="617d8-167">After</span></span></td>
<td><span data-ttu-id="617d8-168">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-169">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="617d8-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-170">Rēķins</span><span class="sxs-lookup"><span data-stu-id="617d8-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="617d8-171">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="617d8-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-172">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="617d8-172">Not applicable</span></span></td>
<td><span data-ttu-id="617d8-173">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-174">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="617d8-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-175">Rēķins</span><span class="sxs-lookup"><span data-stu-id="617d8-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="617d8-176">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="617d8-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-177">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-177">Before</span></span></td>
<td><span data-ttu-id="617d8-178">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-179">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="617d8-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-180">Rēķins</span><span class="sxs-lookup"><span data-stu-id="617d8-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="617d8-181">Pēc</span><span class="sxs-lookup"><span data-stu-id="617d8-181">After</span></span></td>
<td><span data-ttu-id="617d8-182">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-183">Rēķins</span><span class="sxs-lookup"><span data-stu-id="617d8-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="617d8-184">Ražošana</span><span class="sxs-lookup"><span data-stu-id="617d8-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-185">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="617d8-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-186">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="617d8-186">Not applicable</span></span></td>
<td><span data-ttu-id="617d8-187">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="617d8-188">Visi</span><span class="sxs-lookup"><span data-stu-id="617d8-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-189">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="617d8-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-190">Beigt</span><span class="sxs-lookup"><span data-stu-id="617d8-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="617d8-191">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="617d8-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-192">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-192">Before</span></span></td>
<td><span data-ttu-id="617d8-193">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-194">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="617d8-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-195">Beigt</span><span class="sxs-lookup"><span data-stu-id="617d8-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="617d8-196">Pēc</span><span class="sxs-lookup"><span data-stu-id="617d8-196">After</span></span></td>
<td><span data-ttu-id="617d8-197">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-198">Beigt</span><span class="sxs-lookup"><span data-stu-id="617d8-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="617d8-199">Karantīna</span><span class="sxs-lookup"><span data-stu-id="617d8-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-200">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="617d8-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="617d8-201">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-201">Before</span></span></td>
<td><span data-ttu-id="617d8-202">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="617d8-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-203">Beigt</span><span class="sxs-lookup"><span data-stu-id="617d8-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-204">Pēc</span><span class="sxs-lookup"><span data-stu-id="617d8-204">After</span></span></td>
<td><span data-ttu-id="617d8-205">Beigt</span><span class="sxs-lookup"><span data-stu-id="617d8-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-206">Beigt</span><span class="sxs-lookup"><span data-stu-id="617d8-206">End</span></span></td>
<td><span data-ttu-id="617d8-207">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-207">Before</span></span></td>
<td><span data-ttu-id="617d8-208">Beigt</span><span class="sxs-lookup"><span data-stu-id="617d8-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="617d8-209">Maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="617d8-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-210">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="617d8-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="617d8-211">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-211">Before</span></span></td>
<td><span data-ttu-id="617d8-212">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-213">Noteikts ID, Grupa vai Visi, un Resursam raksturīgs, Grupa vai Visi</span><span class="sxs-lookup"><span data-stu-id="617d8-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-214">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="617d8-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-215">Pēc</span><span class="sxs-lookup"><span data-stu-id="617d8-215">After</span></span></td>
<td><span data-ttu-id="617d8-216">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="617d8-217">Līdzprodukta ražošana</span><span class="sxs-lookup"><span data-stu-id="617d8-217">Co-product production</span></span></td>
<td><span data-ttu-id="617d8-218">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="617d8-218">Registration</span></span></td>
<td><span data-ttu-id="617d8-219">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="617d8-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-220">Nav</span><span class="sxs-lookup"><span data-stu-id="617d8-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="617d8-221">Visi</span><span class="sxs-lookup"><span data-stu-id="617d8-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="617d8-222">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="617d8-222">Report as finished</span></span></td>
<td><span data-ttu-id="617d8-223">Pirms</span><span class="sxs-lookup"><span data-stu-id="617d8-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-224">Pēc</span><span class="sxs-lookup"><span data-stu-id="617d8-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="617d8-225">Nākamajā tabulā ir plašāka informācija par to, kā kvalitātes pārbaudes pasūtījumus var ģenerēt specifiskiem procesu tipiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="617d8-226">Procesa tips</span><span class="sxs-lookup"><span data-stu-id="617d8-226">Type of process</span></span></th>
<th><span data-ttu-id="617d8-227">Kad kvalitātes pārbaudes pasūtījumus var ģenerēt automātiski</span><span class="sxs-lookup"><span data-stu-id="617d8-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="617d8-228">Kad kvalitātes pārbaudes pasūtījums var ģenerēt, ja ir nepieciešama destruktīvā testēšana</span><span class="sxs-lookup"><span data-stu-id="617d8-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="617d8-229">Nosacījuma informācija</span><span class="sxs-lookup"><span data-stu-id="617d8-229">Condition information</span></span></th>
<th><span data-ttu-id="617d8-230">Manuālas ģenerēšanas informācija</span><span class="sxs-lookup"><span data-stu-id="617d8-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="617d8-231">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="617d8-231">Purchase order</span></span></td>
<td><span data-ttu-id="617d8-232">Pirms vai pēc tam, kad saņemtajam materiālam tiek grāmatots saņemšanas saraksts vai produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="617d8-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="617d8-233">Pēc tam, kad saņemtajam materiālam tiek grāmatota produktu ieejas plūsma, jo šim materiālam ir jābūt pieejamam destruktīvajai testēšanai</span><span class="sxs-lookup"><span data-stu-id="617d8-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="617d8-234">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="617d8-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="617d8-235">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pirkšanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="617d8-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-236">Karantīnas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="617d8-236">Quarantine order</span></span></td>
<td><span data-ttu-id="617d8-237">Pirms vai pēc tam, kad karantīnas pasūtījums tiek ziņots kā pabeigts vai beidzies</span><span class="sxs-lookup"><span data-stu-id="617d8-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="617d8-238">Nevar ģenerēt kvalitātes pārbaudes pasūtījumus, kam ir nepieciešami destruktīvi testi.</span><span class="sxs-lookup"><span data-stu-id="617d8-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="617d8-239">Tiek pieņemts, ka karantīnas pasūtījuma funkcionalitāte nodrošina atbrīvošanos no iznīcinātā materiāla.</span><span class="sxs-lookup"><span data-stu-id="617d8-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="617d8-240">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="617d8-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="617d8-241">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst karantīnas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="617d8-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-242">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="617d8-242">Sales order</span></span></td>
<td><span data-ttu-id="617d8-243">Pirms plānotas izdošanas procesa vai pavadzīmes atjaunināšanas krājumiem, kas tiek sūti</span><span class="sxs-lookup"><span data-stu-id="617d8-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="617d8-244">Jebkurā posmā</span><span class="sxs-lookup"><span data-stu-id="617d8-244">At any step</span></span></td>
<td><span data-ttu-id="617d8-245">Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu, krājumu vai debitoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="617d8-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="617d8-246">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pārdošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="617d8-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-247">Ražošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="617d8-247">Production order</span></span></td>
<td><span data-ttu-id="617d8-248">Pirms vai pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="617d8-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="617d8-249">Pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="617d8-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="617d8-250">Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu vai krājumu, vai arī šo abu nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="617d8-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="617d8-251">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst ražošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="617d8-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-252">Ražošanas pasūtījums, kuram ir maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="617d8-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="617d8-253">Pirms vai pēc tam, kad kādai operācijai ir pabeigta atskaite</span><span class="sxs-lookup"><span data-stu-id="617d8-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="617d8-254">Pēc tam, kad pēdējai operācijai ražošana ir ziņota kā pabeigta</span><span class="sxs-lookup"><span data-stu-id="617d8-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="617d8-255">Kvalitātes pārbaudes pasūtījuma pieprasījums ar norādīt noteiktu vietu, krājumu vai operācijas resursu, vai arī šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="617d8-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="617d8-256">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst maršruta operācijai, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="617d8-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="617d8-257">Krājumi</span><span class="sxs-lookup"><span data-stu-id="617d8-257">Inventory</span></span></td>
<td><span data-ttu-id="617d8-258">Kvalitātes pārbaudes pasūtījumu nevar automātiski ģenerēt transakcijai krājumu žurnālā vai arī pārsūtīšanas pasūtījuma transakcijām.</span><span class="sxs-lookup"><span data-stu-id="617d8-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="617d8-259">Krājuma daudzumam noliktavā ir manuāli jāizveido kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="617d8-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="617d8-260">Fiziski rīcībā esošie krājumi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="617d8-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="617d8-261">Kvalitātes pārbaudes pasūtījuma automātiskās ģenerēšanas piemēri</span><span class="sxs-lookup"><span data-stu-id="617d8-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="617d8-262">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="617d8-262">Purchasing</span></span>

<span data-ttu-id="617d8-263">Pirkšanā, ja iestatāt lauku **Notikuma veids** uz **Produktu ieejas plūsma** un lauku **Izpilde**, kas atrodas lapā **Kvalitātes piesaistes** uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="617d8-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="617d8-264">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Jā**, katrai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu un iestatījumiem krājumu iztveršanā.</span><span class="sxs-lookup"><span data-stu-id="617d8-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="617d8-265">Katru reizi, kad tiek saņemts daudzums atbilstoši pirkšanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="617d8-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="617d8-266">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Nē**, pirmajai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="617d8-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="617d8-267">Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no izsekošanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="617d8-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="617d8-268">Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākām ieejas plūsmām atbilstoši pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="617d8-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="617d8-269">Kvalitātes specifikācija</span><span class="sxs-lookup"><span data-stu-id="617d8-269">Quality specification</span></span></th>
<th><span data-ttu-id="617d8-270">Pēc atjauninātā daudzuma</span><span class="sxs-lookup"><span data-stu-id="617d8-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="617d8-271">Pēc izsekošanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="617d8-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="617d8-272">Rezultāts</span><span class="sxs-lookup"><span data-stu-id="617d8-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="617d8-273">Procentuālā attiecība: 10 %</span><span class="sxs-lookup"><span data-stu-id="617d8-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="617d8-274">Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="617d8-275">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="617d8-275">Batch number: No</span></span></p>
<p><span data-ttu-id="617d8-276">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="617d8-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="617d8-277">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="617d8-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="617d8-278">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="617d8-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="617d8-279">Kvalitātes pārbaudes pasūtījums #1 3 vienumiem (10 % no 30)</span><span class="sxs-lookup"><span data-stu-id="617d8-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-280">Pabeigto krājumu daudzums 70</span><span class="sxs-lookup"><span data-stu-id="617d8-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="617d8-281">Kvalitātes pārbaudes pasūtījums #2 7 vienumiem (10 % no atlikušā pasūtījuma daudzuma, kas šajā gadījumā ir vienāds ar 70)</span><span class="sxs-lookup"><span data-stu-id="617d8-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="617d8-282">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="617d8-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="617d8-283">Nē</span><span class="sxs-lookup"><span data-stu-id="617d8-283">No</span></span></td>
<td>
<p><span data-ttu-id="617d8-284">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="617d8-284">Batch number: No</span></span></p>
<p><span data-ttu-id="617d8-285">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="617d8-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="617d8-286">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="617d8-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="617d8-287">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="617d8-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="617d8-288">Kvalitātes pārbaudes pasūtījums #1 tiek izveidots vienumam 1 (pirmajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība ir 1).</span><span class="sxs-lookup"><span data-stu-id="617d8-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="617d8-289">Saskaņā ar atlikušo daudzumu nav izveidoti citi kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-290">Pabeigto krājumu daudzums 10</span><span class="sxs-lookup"><span data-stu-id="617d8-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="617d8-291">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-292">Pabeigto krājumu daudzums 60</span><span class="sxs-lookup"><span data-stu-id="617d8-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="617d8-293">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="617d8-294">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="617d8-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="617d8-295">Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="617d8-296">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="617d8-297">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="617d8-298">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="617d8-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="617d8-299">Pabeigto krājumu daudzums 3</span><span class="sxs-lookup"><span data-stu-id="617d8-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="617d8-300">Kvalitātes pārbaudes pasūtījums #1 1 vienumam no partijas #b1, sērijas #s1</span><span class="sxs-lookup"><span data-stu-id="617d8-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="617d8-301">Kvalitātes pārbaudes pasūtījums #2 1 vienumam no partijas #b2, sērijas #s2</span><span class="sxs-lookup"><span data-stu-id="617d8-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="617d8-302">Kvalitātes pārbaudes pasūtījums #3 1 vienumam no partijas #b3, sērijas #s3</span><span class="sxs-lookup"><span data-stu-id="617d8-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-303">Pabeigto krājumu daudzums 2</span><span class="sxs-lookup"><span data-stu-id="617d8-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="617d8-304">Kvalitātes pārbaudes pasūtījums #4 1 vienumam no partijas #b4, sērijas #s4</span><span class="sxs-lookup"><span data-stu-id="617d8-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="617d8-305">Kvalitātes pārbaudes pasūtījums #5 1 vienumam no partijas #b5, sērijas #s5</span><span class="sxs-lookup"><span data-stu-id="617d8-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="617d8-306"><strong>Piezīme:</strong> partiju var izmantot atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="617d8-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="617d8-307">Fiksēts daudzums: 2</span><span class="sxs-lookup"><span data-stu-id="617d8-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="617d8-308">Nē</span><span class="sxs-lookup"><span data-stu-id="617d8-308">No</span></span></td>
<td>
<p><span data-ttu-id="617d8-309">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="617d8-310">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="617d8-311">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="617d8-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="617d8-312">Pabeigto krājumu daudzums 4</span><span class="sxs-lookup"><span data-stu-id="617d8-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="617d8-313">Kvalitātes pārbaudes pasūtījums #1 1 vienumam no partijas #b1, sērijas #s1.</span><span class="sxs-lookup"><span data-stu-id="617d8-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="617d8-314">Kvalitātes pārbaudes pasūtījums #2 1 vienumam no partijas #b2, sērijas #s2.</span><span class="sxs-lookup"><span data-stu-id="617d8-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="617d8-315">Kvalitātes pārbaudes pasūtījums #3 1 vienumam no partijas #b3, sērijas #s3.</span><span class="sxs-lookup"><span data-stu-id="617d8-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="617d8-316">Kvalitātes pārbaudes pasūtījums #4 1 vienumam no partijas #b4, sērijas #s4.</span><span class="sxs-lookup"><span data-stu-id="617d8-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="617d8-317">Saskaņā ar atlikušo daudzumu nav izveidoti citi kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-318">Pabeigto krājumu daudzums 6</span><span class="sxs-lookup"><span data-stu-id="617d8-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="617d8-319">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="617d8-320">Ražošana</span><span class="sxs-lookup"><span data-stu-id="617d8-320">Production</span></span>

<span data-ttu-id="617d8-321">Ražošanā, ja iestatāt lauku **Notikuma veids** uz **Norādīts kā pabeigts** un lauku **Izpilde**, kas atrodas lapā **Kvalitātes piesaistes** uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="617d8-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="617d8-322">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Jā**, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz katru pabeigto daudzumu un iestatījumiem krājumu iztveršanā.</span><span class="sxs-lookup"><span data-stu-id="617d8-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="617d8-323">Katru reizi, kad tiek daudzums tiek norādīts kā pabeigts atbilstoši ražošanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko pabeigto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="617d8-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="617d8-324">Šī ģenerēšanas loģika ir saskaņota ar pirkšanu.</span><span class="sxs-lookup"><span data-stu-id="617d8-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="617d8-325">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Nē**, pirmajā reizē, kad daudzums tiek norādīts kā pabeigts, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz pabeigto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="617d8-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="617d8-326">Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no krājumu iztveršanas izsekošanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="617d8-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="617d8-327">Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākajiem pabeigtajiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="617d8-328">Kvalitātes specifikācija</span><span class="sxs-lookup"><span data-stu-id="617d8-328">Quality specification</span></span></th>
<th><span data-ttu-id="617d8-329">Pēc atjauninātā daudzuma</span><span class="sxs-lookup"><span data-stu-id="617d8-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="617d8-330">Pēc izsekošanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="617d8-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="617d8-331">Rezultāts</span><span class="sxs-lookup"><span data-stu-id="617d8-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="617d8-332">Procentuālā attiecība: 10 %</span><span class="sxs-lookup"><span data-stu-id="617d8-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="617d8-333">Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="617d8-334">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="617d8-334">Batch number: No</span></span></p>
<p><span data-ttu-id="617d8-335">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="617d8-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="617d8-336">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="617d8-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="617d8-337">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="617d8-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="617d8-338">Kvalitātes pārbaudes pasūtījums #1 3 vienumiem (10 % no 30)</span><span class="sxs-lookup"><span data-stu-id="617d8-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-339">Pabeigto krājumu daudzums 70</span><span class="sxs-lookup"><span data-stu-id="617d8-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="617d8-340">Kvalitātes pārbaudes pasūtījums #2 7 vienumiem (10 % no atlikušā pasūtījuma daudzuma, kas šajā gadījumā ir vienāds ar 70)</span><span class="sxs-lookup"><span data-stu-id="617d8-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="617d8-341">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="617d8-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="617d8-342">Nē</span><span class="sxs-lookup"><span data-stu-id="617d8-342">No</span></span></td>
<td>
<p><span data-ttu-id="617d8-343">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="617d8-343">Batch number: No</span></span></p>
<p><span data-ttu-id="617d8-344">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="617d8-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="617d8-345">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="617d8-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="617d8-346">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="617d8-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="617d8-347">Kvalitātes pārbaudes pasūtījums #1 vienumam 1 (pirmajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība ir 1)</span><span class="sxs-lookup"><span data-stu-id="617d8-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="617d8-348">Kvalitātes pārbaudes pasūtījums #2 vienumam 1 (atlikušajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība joprojām ir 1)</span><span class="sxs-lookup"><span data-stu-id="617d8-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-349">Pabeigto krājumu daudzums 10</span><span class="sxs-lookup"><span data-stu-id="617d8-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="617d8-350">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-351">Pabeigto krājumu daudzums 60</span><span class="sxs-lookup"><span data-stu-id="617d8-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="617d8-352">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="617d8-353">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="617d8-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="617d8-354">Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="617d8-355">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="617d8-356">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="617d8-357">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="617d8-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="617d8-358">Norādīt kā pabeigtu vienumam 3: 1 #b1 #s1; 1 #b2, #s2; un 1 #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="617d8-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="617d8-359">Kvalitātes pārbaudes pasūtījums #1 1 vienumam no partijas #b1, sērijas #s1</span><span class="sxs-lookup"><span data-stu-id="617d8-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="617d8-360">Kvalitātes pārbaudes pasūtījums #2 1 vienumam no partijas #b2, sērijas #s2</span><span class="sxs-lookup"><span data-stu-id="617d8-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="617d8-361">Kvalitātes pārbaudes pasūtījums #3 1 vienumam no partijas #b3, sērijas #s3</span><span class="sxs-lookup"><span data-stu-id="617d8-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-362">Norādīt kā pabeigtu vienumam 2: 1 #b4, #s4 un 1 #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="617d8-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="617d8-363">Kvalitātes pārbaudes pasūtījums #4 1 vienumam no partijas #b4, sērijas #s4</span><span class="sxs-lookup"><span data-stu-id="617d8-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="617d8-364">Kvalitātes pārbaudes pasūtījums #5 1 vienumam no partijas #b5, sērijas #s5</span><span class="sxs-lookup"><span data-stu-id="617d8-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="617d8-365"><strong>Piezīme:</strong> partiju var izmantot atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="617d8-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="617d8-366">Fiksēts daudzums: 2</span><span class="sxs-lookup"><span data-stu-id="617d8-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="617d8-367">Nē</span><span class="sxs-lookup"><span data-stu-id="617d8-367">No</span></span></td>
<td>
<p><span data-ttu-id="617d8-368">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="617d8-369">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="617d8-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="617d8-370">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="617d8-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="617d8-371">Norādīt kā pabeigtu vienumam 4: 1 #b1 #s1; 1 #b2, #s2; un 1 #b3, #s3 un 1 #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="617d8-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="617d8-372">Kvalitātes pārbaudes pasūtījums #1 1 vienumam no partijas #b1, sērijas #s1</span><span class="sxs-lookup"><span data-stu-id="617d8-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="617d8-373">Kvalitātes pārbaudes pasūtījums #2 1 vienumam no partijas #b2, sērijas #s2</span><span class="sxs-lookup"><span data-stu-id="617d8-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="617d8-374">Kvalitātes pārbaudes pasūtījums #3 1 vienumam no partijas #b3, sērijas #s3</span><span class="sxs-lookup"><span data-stu-id="617d8-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="617d8-375">Kvalitātes pārbaudes pasūtījums #4 1 vienumam no partijas #b4, sērijas #s4</span><span class="sxs-lookup"><span data-stu-id="617d8-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="617d8-376">Kvalitātes pārbaudes pasūtījums #5 vienumam 2 bez atsauces uz partijas un sērijas numuru</span><span class="sxs-lookup"><span data-stu-id="617d8-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="617d8-377">Norādīt kā pabeigtu vienumam 6: 1 #b5 #s5; 1 #b6, #s6; 1 #b7, #s7; 1 #b8, #s8; 1 #b9, #s9 un 1 #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="617d8-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="617d8-378">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="617d8-379">Kvalitātes pārvaldības lapas</span><span class="sxs-lookup"><span data-stu-id="617d8-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="617d8-380">Lapa</span><span class="sxs-lookup"><span data-stu-id="617d8-380">Page</span></span></th>
<th><span data-ttu-id="617d8-381">Apraksts</span><span class="sxs-lookup"><span data-stu-id="617d8-381">Description</span></span></th>
<th><span data-ttu-id="617d8-382">Paraugs</span><span class="sxs-lookup"><span data-stu-id="617d8-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="617d8-383">Kvalitātes piesaistes</span><span class="sxs-lookup"><span data-stu-id="617d8-383">Quality associations</span></span></td>
<td><span data-ttu-id="617d8-384">Skatiet šī raksta iepriekšējās sadaļas.</span><span class="sxs-lookup"><span data-stu-id="617d8-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="617d8-385">Kvalitātes saistība ģenerētajam kvalitātes pārbaudes pasūtījumam definē visu tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="617d8-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="617d8-386">Transakcijas notikums</span><span class="sxs-lookup"><span data-stu-id="617d8-386">The transaction event</span></span></li>
<li><span data-ttu-id="617d8-387">Testu kopa, kas šiem krājumiem ir jāveic</span><span class="sxs-lookup"><span data-stu-id="617d8-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="617d8-388">Pieņemamais kvalitātes līmenis (AQL)</span><span class="sxs-lookup"><span data-stu-id="617d8-388">The AQL</span></span></li>
<li><span data-ttu-id="617d8-389">Iztveršanas plāns</span><span class="sxs-lookup"><span data-stu-id="617d8-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="617d8-390">Ir jādefinē kvalitātes piesaiste katrai biznesa procesā ietvertajai variācijai, kam ir automātiski jāveido kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="617d8-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="617d8-391">Piemēram, kvalitātes pārbaudes pasūtījumu var ģenerēt biznesa procesos, kas paredzēti pirkšanas pasūtījumiem, karantīnas pasūtījumiem, pārdošanas pasūtījumiem un ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="617d8-392">Testi</span><span class="sxs-lookup"><span data-stu-id="617d8-392">Tests</span></span></td>
<td><span data-ttu-id="617d8-393">Izmantojiet šo lapu, lai definētu un skatītu atsevišķos testus, kas nosaka, vai preces atbilst kvalitātes specifikācijām.</span><span class="sxs-lookup"><span data-stu-id="617d8-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="617d8-394">Vienu vai vairākus atsevišķus testus varat piešķirt testu grupai.</span><span class="sxs-lookup"><span data-stu-id="617d8-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="617d8-395">Šajā gadījumā jums ir jānorāda arī testa specifiskā informācija, piemēram, pieņemamās mērījumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="617d8-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="617d8-396">Mērījumu vērtības tiek izmantotas kvantitatīvajiem testiem, un testa mainīgie tiek lietoti kvalitatīvajiem testiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="617d8-397">Kvantitatīvajam testam testa tips ir <strong>Vesels skaitlis</strong> vai <strong>Daļskaitlis</strong>, un tam ir arī norādīta mērvienība.</span><span class="sxs-lookup"><span data-stu-id="617d8-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="617d8-398">Kvalitātes specifikācijas un testa rezultāti tiek izteikti kā skaitļi.</span><span class="sxs-lookup"><span data-stu-id="617d8-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="617d8-399">Kvalitatīvajam testam testa tips ir <strong>Opcija</strong>.</span><span class="sxs-lookup"><span data-stu-id="617d8-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="617d8-400">Kvalitatīvajiem testiem ir nepieciešama papildinformācija par testa mainīgo, kas tiek mērīts, un tā uzskaitīšanas iespējam.</span><span class="sxs-lookup"><span data-stu-id="617d8-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="617d8-401">Kvalitātes specifikācijas un testa rezultāti tiek izteikti atbilstoši rezultātam.</span><span class="sxs-lookup"><span data-stu-id="617d8-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="617d8-402">Ražošanas uzņēmums iepirktajam materiālam veic divus testus: kvantitatīvo testu par materiāla kvalitāti un kvalitatīvo testu par iepakojuma bojājumu.</span><span class="sxs-lookup"><span data-stu-id="617d8-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="617d8-403">Uzņēmums definē papildu informāciju par kvalitātes testu, lai identificētu testa mainīgo (bojāto iepakojumu) un tā rezultātus.</span><span class="sxs-lookup"><span data-stu-id="617d8-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="617d8-404">Uzņēmums izmanto lapu <strong>Testu grupas</strong>, lai abus testus piešķirtu testu grupai un norādītu testa specifisko informāciju.</span><span class="sxs-lookup"><span data-stu-id="617d8-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="617d8-405">Kvalitātes pasūtījumam tiek piešķirta testa grupā, tādējādi uzņēmums var ziņot testa rezultātus par diviem testiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="617d8-406">Testa grupas</span><span class="sxs-lookup"><span data-stu-id="617d8-406">Test groups</span></span></td>
<td><span data-ttu-id="617d8-407">Izmantojiet šo lapu, lai iestatītu, rediģētu un apskatītu testu grupas un atsevišķus testus, kas ir piešķirti kādai testu grupai.</span><span class="sxs-lookup"><span data-stu-id="617d8-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="617d8-408">Augšējā rūtī ir atainotas testu grupas, bet apakšējā rūtī ir atainoti testi, kas piešķirti atlasītajai testu grupai.</span><span class="sxs-lookup"><span data-stu-id="617d8-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="617d8-409">Jūs testu grupai piešķirat vairākus ierobežojumus, piemēram, iztveršanas plānu, pieņemamo kvalitātes līmeni (AQL) un destruktīvās testēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="617d8-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="617d8-410">Kad atsevišķu testu piešķirat testu grupai, jūs definējat papildu informāciju, piemēram, secību, dokumentus un derīguma datumus.</span><span class="sxs-lookup"><span data-stu-id="617d8-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="617d8-411">Kvantitatīvam testam jūsu definēta informācija ietver arī pieņemamās mērījumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="617d8-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="617d8-412">Kvalitatīvam testam šī informācija ietver testa mainīgo un noklusējuma iznākumu.</span><span class="sxs-lookup"><span data-stu-id="617d8-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="617d8-413">Testa grupa, kas ir piešķirta kādam kvalitātes pārbaudes pasūtījumam, nosaka noklusējuma kopu ar testiem, kas ir jāizpilda norādītajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="617d8-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="617d8-414">Taču kvalitātes pārbaudes pasūtījumā testus varat pievienot, dzēst vai mainīt.</span><span class="sxs-lookup"><span data-stu-id="617d8-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="617d8-415">Katra testa rezultāti tiek uzrādīti kvalitātes pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="617d8-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="617d8-416">Ražošanas uzņēmums definē testu grupu katrai tās kvalitātes vadlīniju variācijai.</span><span class="sxs-lookup"><span data-stu-id="617d8-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="617d8-417">Dažādās testu grupas parāda atšķirības iztveršanas plānos, kopā izpildāmo testu kopās, pieņemamajos kvalitātes līmeņos AQL un citos faktoros.</span><span class="sxs-lookup"><span data-stu-id="617d8-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="617d8-418">Kvantitatīvajiem testiem pastāv arī pieņemamo mērījumu vērtību atšķirības.</span><span class="sxs-lookup"><span data-stu-id="617d8-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="617d8-419">Lai īstenotu savas kvalitātes vadlīnijas, automātiski ģenerētiem kvalitātes pārbaudes pasūtījumiem lapā <strong>Kvalitātes saistības</strong> uzņēmums piešķir testu grupu katrai kārtulai, kā arī piešķir testu grupu manuāli izveidotajiem kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="617d8-420">Krājumu kvalitātes grupas</span><span class="sxs-lookup"><span data-stu-id="617d8-420">Item quality groups</span></span></td>
<td><span data-ttu-id="617d8-421">Izmantojiet šo lapu, lai iestatītu, rediģētu un skatītu krājumus, kas ir piešķirti kvalitātes grupai vai kvalitātes grupām, kuras ir piešķirtas kādam krājumam.</span><span class="sxs-lookup"><span data-stu-id="617d8-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="617d8-422">Kvalitātes grupa norāda kopējās testēšanas vajadzības krājumam.</span><span class="sxs-lookup"><span data-stu-id="617d8-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="617d8-423">Kad lapā <strong>Testu grupas</strong> ir definētas testa prasības, varat definēt kārtulas automātiskai kvalitātes pārbaudes pasūtījumu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="617d8-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="617d8-424">Lai vienkāršotu šo procesu, netiek definētas kārtulas atsevišķiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="617d8-425">Tā vietā jūs definējat kārtulas kvalitātes grupai, izmantojot lapu <strong>Kvalitātes saistības</strong>.</span><span class="sxs-lookup"><span data-stu-id="617d8-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="617d8-426">Varat arī izmantot lapu <strong>Krājuma kvalitātes grupas</strong> atlasītai kvalitātes grupai, lai šai grupai piešķirtu atbilstošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="617d8-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="617d8-427">Varat arī izmantot lapu <strong>Krājuma kvalitātes grupas</strong> atlasītam krājumam, lai šim krājumam piešķirtu atbilstošās kvalitātes grupas.</span><span class="sxs-lookup"><span data-stu-id="617d8-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="617d8-428">Ražošanas uzņēmums iegādājas vairākus izejmateriālus, kuriem ir tādas pašas testēšanas vajadzības ienākošajai pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="617d8-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="617d8-429">Uzņēmums definē kvalitātes grupu un pēc tam piešķir krājumu numurus, kas ir saistīti ar izejmateriāliem šai grupai.</span><span class="sxs-lookup"><span data-stu-id="617d8-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="617d8-430">Vēlāk uzņēmums iegādājas jauna tipa izejmateriālu, kuram ir tādas pašas testēšanas vajadzības.</span><span class="sxs-lookup"><span data-stu-id="617d8-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="617d8-431">Tā vietā, lai jaunajam materiālam iestatītu jaunas testēšanas vajadzības, jaunā materiāla krājumu kodu uzņēmums pievieno jau esošajai kvalitātes grupai.</span><span class="sxs-lookup"><span data-stu-id="617d8-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="617d8-432">Tas pats ražošanas uzņēmums ražo arī krājumus, kuriem ir tādas pašas ražošanas testēšanas vajadzības, un krājumus, kuriem ir tādas pašas vajadzības, sūta uz testēšanu pirms sūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="617d8-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="617d8-433">Uzņēmums definē divas papildu kvalitātes grupas un pēc tam piešķir atbilstošos krājumu numurus katrai grupai.</span><span class="sxs-lookup"><span data-stu-id="617d8-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="617d8-434">Testa mainīgie lielumi</span><span class="sxs-lookup"><span data-stu-id="617d8-434">Test variables</span></span></td>
<td><span data-ttu-id="617d8-435">Izmantojiet šo lapu, lai definētu un skatītu mainīgos, kas ir saistīti ar kādu kvalitātes testu.</span><span class="sxs-lookup"><span data-stu-id="617d8-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="617d8-436">Katram mainīgajam varat definēt uzskaitītos iznākumus, kas apzīmē iespējamās opcijas.</span><span class="sxs-lookup"><span data-stu-id="617d8-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="617d8-437">Testus jūs definējat lapā <strong>Testi</strong>.</span><span class="sxs-lookup"><span data-stu-id="617d8-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="617d8-438">Kvalitatīvajiem testiem testa tipu jūs iestatāt uz <strong>Opcija</strong>.</span><span class="sxs-lookup"><span data-stu-id="617d8-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="617d8-439">Izmantojiet lapu <strong>Testu grupas</strong>, lai testa mainīgo piešķirtu atsevišķam testam.</span><span class="sxs-lookup"><span data-stu-id="617d8-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="617d8-440">Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu.</span><span class="sxs-lookup"><span data-stu-id="617d8-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="617d8-441">Šajā pārbaudes testā ir vairāki mainīgie.</span><span class="sxs-lookup"><span data-stu-id="617d8-441">This inspection test has several variables.</span></span> <span data-ttu-id="617d8-442">Viens mainīgais ir garša, un šī mainīgā iespējamie iznākumi ir laba vai slikta.</span><span class="sxs-lookup"><span data-stu-id="617d8-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="617d8-443">Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.</span><span class="sxs-lookup"><span data-stu-id="617d8-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="617d8-444">Testa mainīgo lielumu iznākumi</span><span class="sxs-lookup"><span data-stu-id="617d8-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="617d8-445">Izmantojiet šo lapu, lai iestatītu, rediģētu un skatītu iespējamos testa rezultātus ar kvalitatīvo testu saistītam testa mainīgajam.</span><span class="sxs-lookup"><span data-stu-id="617d8-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="617d8-446">Katram iznākumam jums ir jāpiešķir statuss <strong>sekmīgs</strong> vai <strong>nesekmīgs</strong>.</span><span class="sxs-lookup"><span data-stu-id="617d8-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="617d8-447">Jums ir jādefinē mainīgais un tā iznākumi katram kvalitatīvajam testam, kas ir definēts lapā <strong>Testi</strong>.</span><span class="sxs-lookup"><span data-stu-id="617d8-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="617d8-448">(Kvalitatīvajiem testiem testa tips lapā <strong>Testi</strong> ir iestatīts uz <strong>Opcija</strong>.) Lai testa mainīgo un noklusējuma iznākumu piešķirtu atsevišķam kvalitatīvajam testam, izmantojiet lapu <strong>Testu grupas</strong>.</span><span class="sxs-lookup"><span data-stu-id="617d8-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="617d8-449">Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu.</span><span class="sxs-lookup"><span data-stu-id="617d8-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="617d8-450">Šajā pārbaudes testā ir vairāki mainīgie.</span><span class="sxs-lookup"><span data-stu-id="617d8-450">This inspection test has of several variables.</span></span> <span data-ttu-id="617d8-451">Viens mainīgais ir garša, un šī mainīgā iespējamie iznākumi ir laba vai slikta.</span><span class="sxs-lookup"><span data-stu-id="617d8-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="617d8-452">Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.</span><span class="sxs-lookup"><span data-stu-id="617d8-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="617d8-453">Katram iznākumam tiek piešķirts ir statuss <strong>sekmīgs</strong> vai <strong>nesekmīgs</strong>.</span><span class="sxs-lookup"><span data-stu-id="617d8-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="617d8-454">Katra mainīgā pārbaudes testa laikā pārbaudītājs ziņo testa rezultātu, izvēloties vienu no rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="617d8-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="617d8-455">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="617d8-455">Additional resources</span></span>
--------

[<span data-ttu-id="617d8-456">Kvalitātes pārvaldības procesi</span><span class="sxs-lookup"><span data-stu-id="617d8-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="617d8-457">Neatbilstības pārvaldība</span><span class="sxs-lookup"><span data-stu-id="617d8-457">Nonconformance management</span></span>](enable-nonconformance-management.md)
