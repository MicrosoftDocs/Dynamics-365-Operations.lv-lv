---
title: "Kvalitātes pārvaldības apskats"
description: "Šajā tēmā ir aprakstīts, kā programmā Microsoft Dynamics 365 for Finance and Operations varat izmantot kvalitātes pārvaldību, lai uzlabotu produktu kvalitāti savā piegādes ķēdē."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 79b3127f726a08cc24c20145b5ad9969157a899c
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="quality-management-overview"></a><span data-ttu-id="233a7-103">Kvalitātes pārvaldības apskats</span><span class="sxs-lookup"><span data-stu-id="233a7-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="233a7-104">Šajā tēmā ir aprakstīts, kā programmā Microsoft Dynamics 365 for Finance and Operations varat izmantot kvalitātes pārvaldību, lai uzlabotu produktu kvalitāti savā piegādes ķēdē.</span><span class="sxs-lookup"><span data-stu-id="233a7-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="233a7-105">Kvalitātes pārvaldība jums var palīdzēt pārvaldīt apgrozījumu laikus, kad strādājat ar nekondīcijas precēm, neatkarīgi no to izcelsmes vietas.</span><span class="sxs-lookup"><span data-stu-id="233a7-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="233a7-106">Tā kā diagnostikas tipi ir saistīti ar korekciju ziņošanu, Microsoft Dynamics 365 for Finance and Operations var plānot uzdevumus, lai izlabotu problēmas un novērstu to atkārtošanos.</span><span class="sxs-lookup"><span data-stu-id="233a7-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="233a7-107">Papildus neatbilstības pārvaldības funkcionalitātei kvalitātes pārvaldība ietver arī funkcionalitāti problēmu izsekošanai pēc problēmas tipa (pat iekšējām problēmām) un risinājumu identificēšanai īstermiņā vai ilgtermiņā.</span><span class="sxs-lookup"><span data-stu-id="233a7-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="233a7-108">Statistika par galvenajiem darba kvalitātes rādītājiem (KPI) sniedz ieskatu par iepriekšējām neatbilstības problēmām un risinājumiem, kas tika izmantoti to labošanai.</span><span class="sxs-lookup"><span data-stu-id="233a7-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="233a7-109">Vēsturiskos datus varat izmantot, lai pārskatītu iepriekšējo kvalitātes pasākumu efektivitāti un noteiktu, kuri pasākumi ir piemēroti turpmākai izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="233a7-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="233a7-110">Kad iestatāt kvalitātes saistību, Finance and Operations var ģenerēt kvalitātes pārbaudes pasūtījumus dažādiem biznesa procesiem, notikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="233a7-111">Šāda kvalitātes saistība var attiekties uz noteiktu krājumu, noteiktu krājumu grupu vai visiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="233a7-112">Kvalitātes pārvaldības lietošanas piemēri</span><span class="sxs-lookup"><span data-stu-id="233a7-112">Examples of the use of quality management</span></span>
<span data-ttu-id="233a7-113">Kvalitātes pārvaldība ir elastīga, un to var ieviest dažādos veidos, lai atbilstu noteiktu piegādes ķēdes darbību līmeņu prasībām.</span><span class="sxs-lookup"><span data-stu-id="233a7-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="233a7-114">Nākamajos piemēros ir parādīti šādu līdzekļu iespējamie lietojumi:</span><span class="sxs-lookup"><span data-stu-id="233a7-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="233a7-115">Automātiski uzsākt kvalitātes kontroles procesu, pamatojoties uz iepriekš definētiem kritērijiem (noliktavā reģistrējot kādu pirkšanas pasūtījumu no specifiska kreditora).</span><span class="sxs-lookup"><span data-stu-id="233a7-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="233a7-116">Bloķēt krājumus pārbaudes laikā, lai nepieļautu, ka tiek lietoti neapstiprināti krājumi (pirkšanas pasūtījuma daudzumu pilnīga bloķēšana).</span><span class="sxs-lookup"><span data-stu-id="233a7-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="233a7-117">Kā daļu no kvalitātes saistības lietot krājuma iztveršanu, lai definētu pašreizējo fizisko krājumu daudzumu, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="233a7-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="233a7-118">Iztveršana var būt balstīta uz fiksētiem daudzumiem vai procentiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="233a7-119">Izveidot kvalitātes pārbaudes pasūtījumus daļējām ieejas plūsmām.</span><span class="sxs-lookup"><span data-stu-id="233a7-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="233a7-120">Lai izveidotu kvalitātes pārbaudes pasūtījumu, kura pamatā ir daudzums, kas ir fiziski saņemts ar pasūtījumu, formā **Krājumu iztveršana** ir jāatzīmē izvēles rūtiņa **Pēc atjauninātā daudzuma**.</span><span class="sxs-lookup"><span data-stu-id="233a7-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="233a7-121">Izveidot testa tipus, kas ietver minimālās, maksimālās un mērķa testa vērtības, un veikt testēšanu kvalitātei pret kvantitāti, kur ir iepriekš definēti validēšanas rezultāti.</span><span class="sxs-lookup"><span data-stu-id="233a7-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="233a7-122">Norādīt pieņemamu kvalitātes līmeni (Acceptable Quality Level — AQL), lai kontrolētu kvalitātes mērījumu tolerances.</span><span class="sxs-lookup"><span data-stu-id="233a7-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="233a7-123">Norādīt pārbaudes operācijai nepieciešamos resursus, piemēram, testa apgabalu un testa instrumentus.</span><span class="sxs-lookup"><span data-stu-id="233a7-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="233a7-124">Darbs ar kvalitātes saistībām</span><span class="sxs-lookup"><span data-stu-id="233a7-124">Working with quality associations</span></span>
<span data-ttu-id="233a7-125">Biznesa process, kas izmanto kvalitātes saistību, var būt saistīts ar dažādiem avota dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem vai ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="233a7-126">Katrs kvalitātes saistības ieraksts nosaka testu kopu, pieņemamās kvalitātes līmeni (AQL) un iztveršanas plānu, kas tiek lietoti ģenerētajiem kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="233a7-127">Katrai biznesa procesa variācijai jums ir jādefinē kvalitātes saistības ieraksts.</span><span class="sxs-lookup"><span data-stu-id="233a7-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="233a7-128">Piemēram, varat iestatīt kvalitātes saistību, kas ģenerē kvalitātes pārbaudes pasūtījumu, kad tiek atjaunināta pirkšanas pasūtījuma produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="233a7-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="233a7-129">Atkarībā no izpildes plāna iestatījumiem pašu aktivizēšanas procesu var bloķēt, kamēr pastāv atvērts kvalitātes pārbaudes pasūtījums, vai iespējams bloķēt nākamos procesus, piemēram, pirkšanas pasūtījumu rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="233a7-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="233a7-130">**Piezīme.** Kamēr pastāv atvērti kvalitātes pārbaudes pasūtījumi, krājumu daudzumi tiek automātiski bloķēti no izsniegšanas.</span><span class="sxs-lookup"><span data-stu-id="233a7-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="233a7-131">Atkarībā no iestatījuma **Pilna bloķēšana** lapā **Krājumu iztveršana**, šis daudzums ir vai nu kvalitātes pasūtījumā norādītais daudzums, vai pirmdokumenta rindā norādītais daudzums.</span><span class="sxs-lookup"><span data-stu-id="233a7-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="233a7-132">Noteiktam biznesa procesam kvalitātes saistības ieraksts identificē notikumu un nosacījumus, kādiem tiek ģenerēts kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="233a7-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="233a7-133">Nosacījumi var attiekties uz vietu vai juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="233a7-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="233a7-134">Kvalitātes pārbaudes pasūtījumu, kur ir iesaistīti destruktīvie testi, var ģenerēt tikai tad, ja attiecīgajam notikumam pastāv rīcībā esoši krājumi.</span><span class="sxs-lookup"><span data-stu-id="233a7-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="233a7-135">Nākamajos piemēros ir parādīts, kā kvalitātes saistības ieraksts tiek definēts katra darījumu procesa variācijām.</span><span class="sxs-lookup"><span data-stu-id="233a7-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="233a7-136">Katram piemēram nākamajā tabulā ir sniegts kopsavilkums par kvalitātes saistības ieraksta definētajiem notikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="233a7-137">Atsauces veids</span><span class="sxs-lookup"><span data-stu-id="233a7-137">Reference type</span></span></th>
<th><span data-ttu-id="233a7-138">Notikuma veids</span><span class="sxs-lookup"><span data-stu-id="233a7-138">Event type</span></span></th>
<th><span data-ttu-id="233a7-139">Izpilde</span><span class="sxs-lookup"><span data-stu-id="233a7-139">Execution</span></span></th>
<th><span data-ttu-id="233a7-140">Notikumu aizturēšana</span><span class="sxs-lookup"><span data-stu-id="233a7-140">Event blocking</span></span></th>
<th><span data-ttu-id="233a7-141">Dokumenta atsauce</span><span class="sxs-lookup"><span data-stu-id="233a7-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="233a7-142">Krājumi</span><span class="sxs-lookup"><span data-stu-id="233a7-142">Inventory</span></span></td>
<td><span data-ttu-id="233a7-143">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="233a7-143">Not applicable</span></span></td>
<td><span data-ttu-id="233a7-144">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="233a7-144">Not applicable</span></span></td>
<td><span data-ttu-id="233a7-145">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-145">None</span></span></td>
<td><span data-ttu-id="233a7-146">Visi</span><span class="sxs-lookup"><span data-stu-id="233a7-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="233a7-147">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="233a7-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="233a7-148">Izdošanas process ir ieplānots</span><span class="sxs-lookup"><span data-stu-id="233a7-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="233a7-149">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-149">Before</span></span></td>
<td><span data-ttu-id="233a7-150">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="233a7-151">Konkrēts ID, Grupa vai tikai Visi</span><span class="sxs-lookup"><span data-stu-id="233a7-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-152">Izdošanas process</span><span class="sxs-lookup"><span data-stu-id="233a7-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-153">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="233a7-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-154">Rēķins</span><span class="sxs-lookup"><span data-stu-id="233a7-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="233a7-155">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="233a7-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-156">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-156">Before</span></span></td>
<td><span data-ttu-id="233a7-157">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-158">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="233a7-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-159">Rēķins</span><span class="sxs-lookup"><span data-stu-id="233a7-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="233a7-160">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="233a7-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="233a7-161">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="233a7-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="233a7-162">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-162">Before</span></span></td>
<td><span data-ttu-id="233a7-163">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-164">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="233a7-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-165">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="233a7-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-166">Rēķins</span><span class="sxs-lookup"><span data-stu-id="233a7-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="233a7-167">Pēc</span><span class="sxs-lookup"><span data-stu-id="233a7-167">After</span></span></td>
<td><span data-ttu-id="233a7-168">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-169">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="233a7-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-170">Rēķins</span><span class="sxs-lookup"><span data-stu-id="233a7-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="233a7-171">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="233a7-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-172">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="233a7-172">Not applicable</span></span></td>
<td><span data-ttu-id="233a7-173">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-174">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="233a7-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-175">Rēķins</span><span class="sxs-lookup"><span data-stu-id="233a7-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="233a7-176">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="233a7-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-177">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-177">Before</span></span></td>
<td><span data-ttu-id="233a7-178">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-179">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="233a7-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-180">Rēķins</span><span class="sxs-lookup"><span data-stu-id="233a7-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="233a7-181">Pēc</span><span class="sxs-lookup"><span data-stu-id="233a7-181">After</span></span></td>
<td><span data-ttu-id="233a7-182">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-183">Rēķins</span><span class="sxs-lookup"><span data-stu-id="233a7-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="233a7-184">Ražošana</span><span class="sxs-lookup"><span data-stu-id="233a7-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-185">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="233a7-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-186">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="233a7-186">Not applicable</span></span></td>
<td><span data-ttu-id="233a7-187">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="233a7-188">Visi</span><span class="sxs-lookup"><span data-stu-id="233a7-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-189">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="233a7-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-190">Beigt</span><span class="sxs-lookup"><span data-stu-id="233a7-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="233a7-191">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="233a7-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-192">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-192">Before</span></span></td>
<td><span data-ttu-id="233a7-193">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-194">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="233a7-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-195">Beigt</span><span class="sxs-lookup"><span data-stu-id="233a7-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="233a7-196">Pēc</span><span class="sxs-lookup"><span data-stu-id="233a7-196">After</span></span></td>
<td><span data-ttu-id="233a7-197">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-198">Beigt</span><span class="sxs-lookup"><span data-stu-id="233a7-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="233a7-199">Karantīna</span><span class="sxs-lookup"><span data-stu-id="233a7-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-200">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="233a7-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="233a7-201">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-201">Before</span></span></td>
<td><span data-ttu-id="233a7-202">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="233a7-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-203">Beigt</span><span class="sxs-lookup"><span data-stu-id="233a7-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-204">Pēc</span><span class="sxs-lookup"><span data-stu-id="233a7-204">After</span></span></td>
<td><span data-ttu-id="233a7-205">Beigt</span><span class="sxs-lookup"><span data-stu-id="233a7-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-206">Beigt</span><span class="sxs-lookup"><span data-stu-id="233a7-206">End</span></span></td>
<td><span data-ttu-id="233a7-207">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-207">Before</span></span></td>
<td><span data-ttu-id="233a7-208">Beigt</span><span class="sxs-lookup"><span data-stu-id="233a7-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="233a7-209">Maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="233a7-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-210">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="233a7-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="233a7-211">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-211">Before</span></span></td>
<td><span data-ttu-id="233a7-212">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-213">Noteikts ID, Grupa vai Visi, un Resursam raksturīgs, Grupa vai Visi</span><span class="sxs-lookup"><span data-stu-id="233a7-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-214">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="233a7-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-215">Pēc</span><span class="sxs-lookup"><span data-stu-id="233a7-215">After</span></span></td>
<td><span data-ttu-id="233a7-216">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="233a7-217">Līdzprodukta ražošana</span><span class="sxs-lookup"><span data-stu-id="233a7-217">Co-product production</span></span></td>
<td><span data-ttu-id="233a7-218">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="233a7-218">Registration</span></span></td>
<td><span data-ttu-id="233a7-219">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="233a7-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-220">Nav</span><span class="sxs-lookup"><span data-stu-id="233a7-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="233a7-221">Visi</span><span class="sxs-lookup"><span data-stu-id="233a7-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="233a7-222">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="233a7-222">Report as finished</span></span></td>
<td><span data-ttu-id="233a7-223">Pirms</span><span class="sxs-lookup"><span data-stu-id="233a7-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-224">Pēc</span><span class="sxs-lookup"><span data-stu-id="233a7-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="233a7-225">Nākamajā tabulā ir plašāka informācija par to, kā kvalitātes pārbaudes pasūtījumus var ģenerēt specifiskiem procesu tipiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="233a7-226">Procesa tips</span><span class="sxs-lookup"><span data-stu-id="233a7-226">Type of process</span></span></th>
<th><span data-ttu-id="233a7-227">Kad kvalitātes pārbaudes pasūtījumus var ģenerēt automātiski</span><span class="sxs-lookup"><span data-stu-id="233a7-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="233a7-228">Kad kvalitātes pārbaudes pasūtījums var ģenerēt, ja ir nepieciešama destruktīvā testēšana</span><span class="sxs-lookup"><span data-stu-id="233a7-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="233a7-229">Nosacījuma informācija</span><span class="sxs-lookup"><span data-stu-id="233a7-229">Condition information</span></span></th>
<th><span data-ttu-id="233a7-230">Manuālas ģenerēšanas informācija</span><span class="sxs-lookup"><span data-stu-id="233a7-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="233a7-231">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="233a7-231">Purchase order</span></span></td>
<td><span data-ttu-id="233a7-232">Pirms vai pēc tam, kad saņemtajam materiālam tiek grāmatots saņemšanas saraksts vai produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="233a7-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="233a7-233">Pēc tam, kad saņemtajam materiālam tiek grāmatota produktu ieejas plūsma, jo šim materiālam ir jābūt pieejamam destruktīvajai testēšanai</span><span class="sxs-lookup"><span data-stu-id="233a7-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="233a7-234">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="233a7-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="233a7-235">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pirkšanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="233a7-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-236">Karantīnas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="233a7-236">Quarantine order</span></span></td>
<td><span data-ttu-id="233a7-237">Pirms vai pēc tam, kad karantīnas pasūtījums tiek ziņots kā pabeigts vai beidzies</span><span class="sxs-lookup"><span data-stu-id="233a7-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="233a7-238">Nevar ģenerēt kvalitātes pārbaudes pasūtījumus, kam ir nepieciešami destruktīvie testi.</span><span class="sxs-lookup"><span data-stu-id="233a7-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="233a7-239">Tiek pieņemts, ka karantīnas pasūtījuma funkcionalitāte veic atbrīvošanos no iznīcinātā materiāla.</span><span class="sxs-lookup"><span data-stu-id="233a7-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="233a7-240">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="233a7-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="233a7-241">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst karantīnas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="233a7-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-242">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="233a7-242">Sales order</span></span></td>
<td><span data-ttu-id="233a7-243">Pirms plānotas izdošanas procesa vai pavadzīmes atjaunināšanas krājumiem, kas tiek sūti</span><span class="sxs-lookup"><span data-stu-id="233a7-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="233a7-244">Jebkurā posmā</span><span class="sxs-lookup"><span data-stu-id="233a7-244">At any step</span></span></td>
<td><span data-ttu-id="233a7-245">Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu, krājumu vai debitoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="233a7-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="233a7-246">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pārdošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="233a7-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-247">Ražošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="233a7-247">Production order</span></span></td>
<td><span data-ttu-id="233a7-248">Pirms vai pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="233a7-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="233a7-249">Pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="233a7-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="233a7-250">Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu vai krājumu, vai arī šo abu nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="233a7-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="233a7-251">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst ražošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="233a7-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-252">Ražošanas pasūtījums, kuram ir maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="233a7-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="233a7-253">Pirms vai pēc tam, kad kādai operācijai ir pabeigta atskaite</span><span class="sxs-lookup"><span data-stu-id="233a7-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="233a7-254">Pēc tam, kad pēdējai operācijai ražošana ir ziņota kā pabeigta</span><span class="sxs-lookup"><span data-stu-id="233a7-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="233a7-255">Kvalitātes pārbaudes pasūtījuma pieprasījums ar norādīt noteiktu vietu, krājumu vai operācijas resursu, vai arī šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="233a7-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="233a7-256">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst maršruta operācijai, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="233a7-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="233a7-257">Krājumi</span><span class="sxs-lookup"><span data-stu-id="233a7-257">Inventory</span></span></td>
<td><span data-ttu-id="233a7-258">Kvalitātes pārbaudes pasūtījumu nevar automātiski ģenerēt transakcijai krājumu žurnālā vai arī pārsūtīšanas pasūtījuma transakcijām.</span><span class="sxs-lookup"><span data-stu-id="233a7-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="233a7-259">Krājumu daudzumam kvalitātes pārbaudes pasūtījums ir jāveido manuāli.</span><span class="sxs-lookup"><span data-stu-id="233a7-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="233a7-260">Fiziski rīcībā esošie krājumi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="233a7-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="233a7-261">Kvalitātes pārvaldības lapas</span><span class="sxs-lookup"><span data-stu-id="233a7-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="233a7-262">Lapa</span><span class="sxs-lookup"><span data-stu-id="233a7-262">Page</span></span></th>
<th><span data-ttu-id="233a7-263">Apraksts</span><span class="sxs-lookup"><span data-stu-id="233a7-263">Description</span></span></th>
<th><span data-ttu-id="233a7-264">Piemērs</span><span class="sxs-lookup"><span data-stu-id="233a7-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="233a7-265">Kvalitātes piesaistes</span><span class="sxs-lookup"><span data-stu-id="233a7-265">Quality associations</span></span></td>
<td><span data-ttu-id="233a7-266">Skatiet šī raksta iepriekšējās sadaļas.</span><span class="sxs-lookup"><span data-stu-id="233a7-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="233a7-267">Kvalitātes saistība ģenerētajam kvalitātes pārbaudes pasūtījumam definē visu tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="233a7-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="233a7-268">Transakcijas notikums</span><span class="sxs-lookup"><span data-stu-id="233a7-268">The transaction event</span></span></li>
<li><span data-ttu-id="233a7-269">Testu kopa, kas šiem krājumiem ir jāveic</span><span class="sxs-lookup"><span data-stu-id="233a7-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="233a7-270">Pieņemamais kvalitātes līmenis (AQL)</span><span class="sxs-lookup"><span data-stu-id="233a7-270">The AQL</span></span></li>
<li><span data-ttu-id="233a7-271">Iztveršanas plāns</span><span class="sxs-lookup"><span data-stu-id="233a7-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="233a7-272">Ir jādefinē kvalitātes piesaiste katrai biznesa procesā ietvertajai variācijai, kam ir automātiski jāveido kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="233a7-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="233a7-273">Piemēram, kvalitātes pārbaudes pasūtījumu var ģenerēt biznesa procesos, kas paredzēti pirkšanas pasūtījumiem, karantīnas pasūtījumiem, pārdošanas pasūtījumiem un ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="233a7-274">Testi</span><span class="sxs-lookup"><span data-stu-id="233a7-274">Tests</span></span></td>
<td><span data-ttu-id="233a7-275">Izmantojiet šo lapu, lai definētu un skatītu atsevišķos testus, kas nosaka, vai preces atbilst kvalitātes specifikācijām.</span><span class="sxs-lookup"><span data-stu-id="233a7-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="233a7-276">Vienu vai vairākus atsevišķus testus varat piešķirt testu grupai.</span><span class="sxs-lookup"><span data-stu-id="233a7-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="233a7-277">Šajā gadījumā jums ir jānorāda arī testa specifiskā informācija, piemēram, pieņemamās mērījumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="233a7-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="233a7-278">Mērījumu vērtības tiek izmantotas kvantitatīvajiem testiem, un testa mainīgie tiek lietoti kvalitatīvajiem testiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="233a7-279">Kvantitatīvajam testam testa tips ir <strong>Vesels skaitlis</strong> vai <strong>Daļskaitlis</strong>, un tam ir arī norādīta mērvienība.</span><span class="sxs-lookup"><span data-stu-id="233a7-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="233a7-280">Kvalitātes specifikācijas un testa rezultāti tiek izteikti kā skaitļi.</span><span class="sxs-lookup"><span data-stu-id="233a7-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="233a7-281">Kvalitatīvajam testam testa tips ir <strong>Opcija</strong>.</span><span class="sxs-lookup"><span data-stu-id="233a7-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="233a7-282">Kvalitatīvajiem testiem ir nepieciešama papildinformācija par testa mainīgo, kas tiek mērīts, un tā uzskaitīšanas iespējam.</span><span class="sxs-lookup"><span data-stu-id="233a7-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="233a7-283">Kvalitātes specifikācijas un testa rezultāti tiek izteikti atbilstoši rezultātam.</span><span class="sxs-lookup"><span data-stu-id="233a7-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="233a7-284">Ražošanas uzņēmums iepirktajam materiālam veic divus testus: kvantitatīvo testu par materiāla kvalitāti un kvalitatīvo testu par iepakojuma bojājumu.</span><span class="sxs-lookup"><span data-stu-id="233a7-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="233a7-285">Uzņēmums definē papildu informāciju par kvalitātes testu, lai identificētu testa mainīgo (bojāto iepakojumu) un tā rezultātus.</span><span class="sxs-lookup"><span data-stu-id="233a7-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="233a7-286">Uzņēmums izmanto lapu <strong>Testu grupas</strong>, lai abus testus piešķirtu testu grupai un norādītu testa specifisko informāciju.</span><span class="sxs-lookup"><span data-stu-id="233a7-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="233a7-287">Kvalitātes pasūtījumam tiek piešķirta testa grupā, tādējādi uzņēmums var ziņot testa rezultātus par diviem testiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="233a7-288">Testa grupas</span><span class="sxs-lookup"><span data-stu-id="233a7-288">Test groups</span></span></td>
<td><span data-ttu-id="233a7-289">Izmantojiet šo lapu, lai iestatītu, rediģētu un apskatītu testu grupas un atsevišķus testus, kas ir piešķirti kādai testu grupai.</span><span class="sxs-lookup"><span data-stu-id="233a7-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="233a7-290">Augšējā rūtī ir atainotas testu grupas, bet apakšējā rūtī ir atainoti testi, kas piešķirti atlasītajai testu grupai.</span><span class="sxs-lookup"><span data-stu-id="233a7-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="233a7-291">Jūs testu grupai piešķirat vairākus ierobežojumus, piemēram, iztveršanas plānu, pieņemamo kvalitātes līmeni (AQL) un destruktīvās testēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="233a7-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="233a7-292">Kad atsevišķu testu piešķirat testu grupai, jūs definējat papildu informāciju, piemēram, secību, dokumentus un derīguma datumus.</span><span class="sxs-lookup"><span data-stu-id="233a7-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="233a7-293">Kvantitatīvam testam jūsu definēta informācija ietver arī pieņemamās mērījumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="233a7-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="233a7-294">Kvalitatīvam testam šī informācija ietver testa mainīgo un noklusējuma iznākumu.</span><span class="sxs-lookup"><span data-stu-id="233a7-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="233a7-295">Testa grupa, kas ir piešķirta kādam kvalitātes pārbaudes pasūtījumam, nosaka noklusējuma kopu ar testiem, kas ir jāizpilda norādītajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="233a7-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="233a7-296">Taču kvalitātes pārbaudes pasūtījumā testus varat pievienot, dzēst vai mainīt.</span><span class="sxs-lookup"><span data-stu-id="233a7-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="233a7-297">Katra testa rezultāti tiek uzrādīti kvalitātes pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="233a7-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="233a7-298">Ražošanas uzņēmums definē testu grupu katrai tās kvalitātes vadlīniju variācijai.</span><span class="sxs-lookup"><span data-stu-id="233a7-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="233a7-299">Dažādās testu grupas parāda atšķirības iztveršanas plānos, kopā izpildāmo testu kopās, pieņemamajos kvalitātes līmeņos AQL un citos faktoros.</span><span class="sxs-lookup"><span data-stu-id="233a7-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="233a7-300">Kvantitatīvajiem testiem pastāv arī pieņemamo mērījumu vērtību atšķirības.</span><span class="sxs-lookup"><span data-stu-id="233a7-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="233a7-301">Lai īstenotu savas kvalitātes vadlīnijas, automātiski ģenerētiem kvalitātes pārbaudes pasūtījumiem lapā <strong>Kvalitātes saistības</strong> uzņēmums piešķir testu grupu katrai kārtulai, kā arī piešķir testu grupu manuāli izveidotajiem kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="233a7-302">Krājumu kvalitātes grupas</span><span class="sxs-lookup"><span data-stu-id="233a7-302">Item quality groups</span></span></td>
<td><span data-ttu-id="233a7-303">Izmantojiet šo lapu, lai iestatītu, rediģētu un skatītu krājumus, kas ir piešķirti kvalitātes grupai vai kvalitātes grupām, kuras ir piešķirtas kādam krājumam.</span><span class="sxs-lookup"><span data-stu-id="233a7-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="233a7-304">Kvalitātes grupa norāda kopējās testēšanas vajadzības krājumam.</span><span class="sxs-lookup"><span data-stu-id="233a7-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="233a7-305">Kad lapā <strong>Testu grupas</strong> ir definētas testa prasības, varat definēt kārtulas automātiskai kvalitātes pārbaudes pasūtījumu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="233a7-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="233a7-306">Lai vienkāršotu šo procesu, jūs nedefinējat kārtulas atsevišķiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-306">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="233a7-307">Tā vietā jūs definējat kārtulas kvalitātes grupai, izmantojot lapu <strong>Kvalitātes saistības</strong>.</span><span class="sxs-lookup"><span data-stu-id="233a7-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="233a7-308">Varat arī izmantot lapu <strong>Krājuma kvalitātes grupas</strong> atlasītai kvalitātes grupai, lai šai grupai piešķirtu atbilstošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="233a7-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="233a7-309">Varat arī izmantot lapu <strong>Krājuma kvalitātes grupas</strong> atlasītam krājumam, lai šim krājumam piešķirtu atbilstošās kvalitātes grupas.</span><span class="sxs-lookup"><span data-stu-id="233a7-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="233a7-310">Ražošanas uzņēmums iegādājas vairākus izejmateriālus, kuriem ir tādas pašas testēšanas vajadzības ienākošajai pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="233a7-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="233a7-311">Uzņēmums definē kvalitātes grupu un pēc tam piešķir krājumu numurus, kas ir saistīti ar izejmateriāliem šai grupai.</span><span class="sxs-lookup"><span data-stu-id="233a7-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="233a7-312">Vēlāk uzņēmums iegādājas jauna tipa izejmateriālu, kuram ir tādas pašas testēšanas vajadzības.</span><span class="sxs-lookup"><span data-stu-id="233a7-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="233a7-313">Tā vietā, lai jaunajam materiālam iestatītu jaunas testēšanas vajadzības, jaunā materiāla krājumu kodu uzņēmums pievieno jau esošajai kvalitātes grupai.</span><span class="sxs-lookup"><span data-stu-id="233a7-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="233a7-314">Tas pats ražošanas uzņēmums ražo arī krājumus, kuriem ir tādas pašas ražošanas testēšanas vajadzības, un krājumus, kuriem ir tādas pašas vajadzības, sūta uz testēšanu pirms sūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="233a7-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="233a7-315">Uzņēmums definē divas papildu kvalitātes grupas un pēc tam piešķir atbilstošos krājumu numurus katrai grupai.</span><span class="sxs-lookup"><span data-stu-id="233a7-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="233a7-316">Testa mainīgie lielumi</span><span class="sxs-lookup"><span data-stu-id="233a7-316">Test variables</span></span></td>
<td><span data-ttu-id="233a7-317">Izmantojiet šo lapu, lai definētu un skatītu mainīgos, kas ir saistīti ar kādu kvalitātes testu.</span><span class="sxs-lookup"><span data-stu-id="233a7-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="233a7-318">Katram mainīgajam varat definēt uzskaitītos iznākumus, kas apzīmē iespējamās opcijas.</span><span class="sxs-lookup"><span data-stu-id="233a7-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="233a7-319">Testus jūs definējat lapā <strong>Testi</strong>.</span><span class="sxs-lookup"><span data-stu-id="233a7-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="233a7-320">Kvalitatīvajiem testiem testa tipu jūs iestatāt uz <strong>Opcija</strong>.</span><span class="sxs-lookup"><span data-stu-id="233a7-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="233a7-321">Izmantojiet lapu <strong>Testu grupas</strong>, lai testa mainīgo piešķirtu atsevišķam testam.</span><span class="sxs-lookup"><span data-stu-id="233a7-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="233a7-322">Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu.</span><span class="sxs-lookup"><span data-stu-id="233a7-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="233a7-323">Šajā pārbaudes testā ir vairāki mainīgie.</span><span class="sxs-lookup"><span data-stu-id="233a7-323">This inspection test has several variables.</span></span> <span data-ttu-id="233a7-324">Viens mainīgais ir garša, un šī mainīgā iespējamie iznākumi ir laba vai slikta.</span><span class="sxs-lookup"><span data-stu-id="233a7-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="233a7-325">Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.</span><span class="sxs-lookup"><span data-stu-id="233a7-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="233a7-326">Testa mainīgo lielumu iznākumi</span><span class="sxs-lookup"><span data-stu-id="233a7-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="233a7-327">Izmantojiet šo lapu, lai iestatītu, rediģētu un skatītu iespējamos testa rezultātus ar kvalitatīvo testu saistītam testa mainīgajam.</span><span class="sxs-lookup"><span data-stu-id="233a7-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="233a7-328">Katram iznākumam jums ir jāpiešķir statuss <strong>sekmīgs</strong> vai <strong>nesekmīgs</strong>.</span><span class="sxs-lookup"><span data-stu-id="233a7-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="233a7-329">Jums ir jādefinē mainīgais un tā iznākumi katram kvalitatīvajam testam, kas ir definēts lapā <strong>Testi</strong>.</span><span class="sxs-lookup"><span data-stu-id="233a7-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="233a7-330">(Kvalitatīvajiem testiem testa tips lapā <strong>Testi</strong> ir iestatīts uz <strong>Opcija</strong>.) Lai testa mainīgo un noklusējuma iznākumu piešķirtu atsevišķam kvalitatīvajam testam, izmantojiet lapu <strong>Testu grupas</strong>.</span><span class="sxs-lookup"><span data-stu-id="233a7-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="233a7-331">Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu.</span><span class="sxs-lookup"><span data-stu-id="233a7-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="233a7-332">Šajā pārbaudes testā ir vairāki mainīgie.</span><span class="sxs-lookup"><span data-stu-id="233a7-332">This inspection test has of several variables.</span></span> <span data-ttu-id="233a7-333">Viens mainīgais ir garša, un šī mainīgā iespējamie iznākumi ir laba vai slikta.</span><span class="sxs-lookup"><span data-stu-id="233a7-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="233a7-334">Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.</span><span class="sxs-lookup"><span data-stu-id="233a7-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="233a7-335">Katram iznākumam tiek piešķirts ir statuss <strong>sekmīgs</strong> vai <strong>nesekmīgs</strong>.</span><span class="sxs-lookup"><span data-stu-id="233a7-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="233a7-336">Katra mainīgā pārbaudes testa laikā pārbaudītājs ziņo testa rezultātu, izvēloties vienu no rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="233a7-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="233a7-337">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="233a7-337">Additional resources</span></span>
--------

[<span data-ttu-id="233a7-338">Kvalitātes pārvaldības procesi</span><span class="sxs-lookup"><span data-stu-id="233a7-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="233a7-339">Neatbilstības pārvaldības iespējošana</span><span class="sxs-lookup"><span data-stu-id="233a7-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

