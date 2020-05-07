---
title: Kvalitātes pārvaldības apskats
description: Šajā tēmā ir aprakstīts, kā varat izmantot kvalitātes pārvaldību programmā Dynamics 365 Supply Chain Management, lai palīdzētu uzlabot preču kvalitāti savā piegādes ķēdē.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1d7828e6bb9a3684c1d76e2cfac96174a8dfbf4
ms.sourcegitcommit: 6d6aa016c4971b0673d461b82fd80b060ae5f7a1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/17/2020
ms.locfileid: "3268820"
---
# <a name="quality-management-overview"></a><span data-ttu-id="ba76f-103">Kvalitātes pārvaldības apskats</span><span class="sxs-lookup"><span data-stu-id="ba76f-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba76f-104">Šajā tēmā ir aprakstīts, kā varat izmantot kvalitātes pārvaldību programmā Dynamics 365 Supply Chain Management, lai palīdzētu uzlabot preču kvalitāti savā piegādes ķēdē.</span><span class="sxs-lookup"><span data-stu-id="ba76f-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="ba76f-105">Kvalitātes pārvaldība jums var palīdzēt pārvaldīt apgrozījumu laikus, kad strādājat ar nekondīcijas precēm, neatkarīgi no to izcelsmes vietas.</span><span class="sxs-lookup"><span data-stu-id="ba76f-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="ba76f-106">Tā kā diagnostikas tipi ir saistīti ar korekciju ziņošanu, Supply Chain Management var plānot uzdevumus, lai izlabotu problēmas un novērstu to atkārtošanos.</span><span class="sxs-lookup"><span data-stu-id="ba76f-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="ba76f-107">Papildus neatbilstības pārvaldības funkcionalitātei kvalitātes pārvaldība ietver arī funkcionalitāti problēmu izsekošanai pēc problēmas tipa (pat iekšējām problēmām) un risinājumu identificēšanai īstermiņā vai ilgtermiņā.</span><span class="sxs-lookup"><span data-stu-id="ba76f-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="ba76f-108">Statistika par galvenajiem darba kvalitātes rādītājiem (KPI) sniedz ieskatu par iepriekšējām neatbilstības problēmām un risinājumiem, kas tika izmantoti to labošanai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="ba76f-109">Vēsturiskos datus varat izmantot, lai pārskatītu iepriekšējo kvalitātes pasākumu efektivitāti un noteiktu, kuri pasākumi ir piemēroti turpmākai izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="ba76f-110">Kad iestatāt kvalitātes saistību, Supply Chain Management var ģenerēt kvalitātes pārbaudes pasūtījumus dažādiem biznesa procesiem, notikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="ba76f-111">Šāda kvalitātes saistība var attiekties uz noteiktu krājumu, noteiktu krājumu grupu vai visiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="ba76f-112">Kvalitātes pārvaldības lietošanas piemēri</span><span class="sxs-lookup"><span data-stu-id="ba76f-112">Examples of the use of quality management</span></span>
<span data-ttu-id="ba76f-113">Kvalitātes pārvaldība ir elastīga, un to var ieviest dažādos veidos, lai atbilstu noteiktu piegādes ķēdes darbību līmeņu prasībām.</span><span class="sxs-lookup"><span data-stu-id="ba76f-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="ba76f-114">Nākamajos piemēros ir parādīti šādu līdzekļu iespējamie lietojumi:</span><span class="sxs-lookup"><span data-stu-id="ba76f-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="ba76f-115">Automātiski uzsākt kvalitātes kontroles procesu, pamatojoties uz iepriekš definētiem kritērijiem (noliktavā reģistrējot kādu pirkšanas pasūtījumu no specifiska kreditora).</span><span class="sxs-lookup"><span data-stu-id="ba76f-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="ba76f-116">Bloķēt krājumus pārbaudes laikā, lai nepieļautu, ka tiek lietoti neapstiprināti krājumi (pirkšanas pasūtījuma daudzumu pilnīga bloķēšana).</span><span class="sxs-lookup"><span data-stu-id="ba76f-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="ba76f-117">Kā daļu no kvalitātes saistības lietot krājuma iztveršanu, lai definētu pašreizējo fizisko krājumu daudzumu, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="ba76f-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="ba76f-118">Paraugu nodošana var būt balstīta uz fiksētiem daudzumiem, procentiem vai pilnu numura zīmi.</span><span class="sxs-lookup"><span data-stu-id="ba76f-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="ba76f-119">_Noliktavas procesu kvalitātes pārvaldības_ līdzeklis paplašina kvalitātes pārvaldības iespējas.</span><span class="sxs-lookup"><span data-stu-id="ba76f-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="ba76f-120">Ja lietojat šo līdzekli, skatiet sadaļu [Noliktavas procesu kvalitātes pārvaldība](quality-management-for-warehouses-processes.md)kā piemēu, kā kvalitātes pārvaldība darbojas, kad tā ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="ba76f-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="ba76f-121">Izveidot kvalitātes pārbaudes pasūtījumus daļējām ieejas plūsmām.</span><span class="sxs-lookup"><span data-stu-id="ba76f-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="ba76f-122">Lai izveidotu kvalitātes pārbaudes pasūtījumu, kura pamatā ir daudzums, kas ir fiziski saņemts ar pasūtījumu, formā **Krājumu iztveršana** ir jāatzīmē izvēles rūtiņa **Pēc atjauninātā daudzuma**.</span><span class="sxs-lookup"><span data-stu-id="ba76f-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="ba76f-123">Izveidot testa tipus, kas ietver minimālās, maksimālās un mērķa testa vērtības, un veikt testēšanu kvalitātei pret kvantitāti, kur ir iepriekš definēti validēšanas rezultāti.</span><span class="sxs-lookup"><span data-stu-id="ba76f-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="ba76f-124">Norādīt pieņemamu kvalitātes līmeni (Acceptable Quality Level — AQL), lai kontrolētu kvalitātes mērījumu tolerances.</span><span class="sxs-lookup"><span data-stu-id="ba76f-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="ba76f-125">Norādīt pārbaudes operācijai nepieciešamos resursus, piemēram, testa apgabalu un testa instrumentus.</span><span class="sxs-lookup"><span data-stu-id="ba76f-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="ba76f-126">Darbs ar kvalitātes saistībām</span><span class="sxs-lookup"><span data-stu-id="ba76f-126">Working with quality associations</span></span>
<span data-ttu-id="ba76f-127">Biznesa process, kas izmanto kvalitātes saistību, var būt saistīts ar dažādiem avota dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem vai ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="ba76f-128">Katrs kvalitātes saistības ieraksts nosaka testu kopu, pieņemamās kvalitātes līmeni (AQL) un iztveršanas plānu, kas tiek lietoti ģenerētajiem kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="ba76f-129">Katrai biznesa procesa variācijai jums ir jādefinē kvalitātes saistības ieraksts.</span><span class="sxs-lookup"><span data-stu-id="ba76f-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="ba76f-130">Piemēram, varat iestatīt kvalitātes saistību, kas ģenerē kvalitātes pārbaudes pasūtījumu, kad tiek atjaunināta pirkšanas pasūtījuma produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="ba76f-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="ba76f-131">Atkarībā no izpildes plāna iestatījumiem pašu aktivizēšanas procesu var bloķēt, kamēr pastāv atvērts kvalitātes pārbaudes pasūtījums, vai iespējams bloķēt nākamos procesus, piemēram, pirkšanas pasūtījumu rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="ba76f-132">**Piezīme.** Kamēr pastāv atvērti kvalitātes pārbaudes pasūtījumi, krājumu daudzumi tiek automātiski bloķēti no izsniegšanas.</span><span class="sxs-lookup"><span data-stu-id="ba76f-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="ba76f-133">Atkarībā no iestatījuma **Pilna bloķēšana** lapā **Krājumu iztveršana**, šis daudzums ir vai nu kvalitātes pasūtījumā norādītais daudzums, vai pirmdokumenta rindā norādītais daudzums.</span><span class="sxs-lookup"><span data-stu-id="ba76f-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="ba76f-134">Noteiktam biznesa procesam kvalitātes saistības ieraksts identificē notikumu un nosacījumus, kādiem tiek ģenerēts kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="ba76f-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="ba76f-135">Nosacījumi var attiekties uz vietu vai juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="ba76f-136">Kvalitātes pārbaudes pasūtījumu, kur ir iesaistīti destruktīvie testi, var ģenerēt tikai tad, ja attiecīgajam notikumam pastāv rīcībā esoši krājumi.</span><span class="sxs-lookup"><span data-stu-id="ba76f-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="ba76f-137">Nākamajos piemēros ir parādīts, kā kvalitātes saistības ieraksts tiek definēts katra darījumu procesa variācijām.</span><span class="sxs-lookup"><span data-stu-id="ba76f-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="ba76f-138">Katram piemēram nākamajā tabulā ir sniegts kopsavilkums par kvalitātes saistības ieraksta definētajiem notikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="ba76f-139">Atsauces veids</span><span class="sxs-lookup"><span data-stu-id="ba76f-139">Reference type</span></span></th>
<th><span data-ttu-id="ba76f-140">Notikuma veids</span><span class="sxs-lookup"><span data-stu-id="ba76f-140">Event type</span></span></th>
<th><span data-ttu-id="ba76f-141">Izpilde</span><span class="sxs-lookup"><span data-stu-id="ba76f-141">Execution</span></span></th>
<th><span data-ttu-id="ba76f-142">Notikumu aizturēšana</span><span class="sxs-lookup"><span data-stu-id="ba76f-142">Event blocking</span></span></th>
<th><span data-ttu-id="ba76f-143">Dokumenta atsauce</span><span class="sxs-lookup"><span data-stu-id="ba76f-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="ba76f-144">Krājumi</span><span class="sxs-lookup"><span data-stu-id="ba76f-144">Inventory</span></span></td>
<td><span data-ttu-id="ba76f-145">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="ba76f-145">Not applicable</span></span></td>
<td><span data-ttu-id="ba76f-146">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="ba76f-146">Not applicable</span></span></td>
<td><span data-ttu-id="ba76f-147">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-147">None</span></span></td>
<td><span data-ttu-id="ba76f-148">Visi</span><span class="sxs-lookup"><span data-stu-id="ba76f-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="ba76f-149">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="ba76f-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="ba76f-150">Izdošanas process ir ieplānots</span><span class="sxs-lookup"><span data-stu-id="ba76f-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="ba76f-151">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-151">Before</span></span></td>
<td><span data-ttu-id="ba76f-152">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="ba76f-153">Konkrēts ID, Grupa vai tikai Visi</span><span class="sxs-lookup"><span data-stu-id="ba76f-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-154">Izdošanas process</span><span class="sxs-lookup"><span data-stu-id="ba76f-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-155">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="ba76f-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-156">Rēķins</span><span class="sxs-lookup"><span data-stu-id="ba76f-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba76f-157">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="ba76f-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-158">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-158">Before</span></span></td>
<td><span data-ttu-id="ba76f-159">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-160">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="ba76f-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-161">Rēķins</span><span class="sxs-lookup"><span data-stu-id="ba76f-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="ba76f-162">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="ba76f-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="ba76f-163">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="ba76f-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="ba76f-164">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-164">Before</span></span></td>
<td><span data-ttu-id="ba76f-165">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-166">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="ba76f-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-167">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="ba76f-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-168">Rēķins</span><span class="sxs-lookup"><span data-stu-id="ba76f-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba76f-169">Pēc</span><span class="sxs-lookup"><span data-stu-id="ba76f-169">After</span></span></td>
<td><span data-ttu-id="ba76f-170">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-171">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="ba76f-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-172">Rēķins</span><span class="sxs-lookup"><span data-stu-id="ba76f-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba76f-173">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="ba76f-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-174">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="ba76f-174">Not applicable</span></span></td>
<td><span data-ttu-id="ba76f-175">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-176">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="ba76f-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-177">Rēķins</span><span class="sxs-lookup"><span data-stu-id="ba76f-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ba76f-178">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="ba76f-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-179">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-179">Before</span></span></td>
<td><span data-ttu-id="ba76f-180">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-181">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="ba76f-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-182">Rēķins</span><span class="sxs-lookup"><span data-stu-id="ba76f-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ba76f-183">Pēc</span><span class="sxs-lookup"><span data-stu-id="ba76f-183">After</span></span></td>
<td><span data-ttu-id="ba76f-184">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-185">Rēķins</span><span class="sxs-lookup"><span data-stu-id="ba76f-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="ba76f-186">Ražošana</span><span class="sxs-lookup"><span data-stu-id="ba76f-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-187">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="ba76f-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-188">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="ba76f-188">Not applicable</span></span></td>
<td><span data-ttu-id="ba76f-189">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="ba76f-190">Visi</span><span class="sxs-lookup"><span data-stu-id="ba76f-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-191">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="ba76f-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-192">Beigt</span><span class="sxs-lookup"><span data-stu-id="ba76f-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ba76f-193">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="ba76f-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-194">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-194">Before</span></span></td>
<td><span data-ttu-id="ba76f-195">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-196">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="ba76f-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-197">Beigt</span><span class="sxs-lookup"><span data-stu-id="ba76f-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ba76f-198">Pēc</span><span class="sxs-lookup"><span data-stu-id="ba76f-198">After</span></span></td>
<td><span data-ttu-id="ba76f-199">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-200">Beigt</span><span class="sxs-lookup"><span data-stu-id="ba76f-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ba76f-201">Karantīna</span><span class="sxs-lookup"><span data-stu-id="ba76f-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-202">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="ba76f-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="ba76f-203">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-203">Before</span></span></td>
<td><span data-ttu-id="ba76f-204">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="ba76f-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-205">Beigt</span><span class="sxs-lookup"><span data-stu-id="ba76f-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-206">Pēc</span><span class="sxs-lookup"><span data-stu-id="ba76f-206">After</span></span></td>
<td><span data-ttu-id="ba76f-207">Beigt</span><span class="sxs-lookup"><span data-stu-id="ba76f-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-208">Beigt</span><span class="sxs-lookup"><span data-stu-id="ba76f-208">End</span></span></td>
<td><span data-ttu-id="ba76f-209">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-209">Before</span></span></td>
<td><span data-ttu-id="ba76f-210">Beigt</span><span class="sxs-lookup"><span data-stu-id="ba76f-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba76f-211">Maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="ba76f-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-212">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="ba76f-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="ba76f-213">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-213">Before</span></span></td>
<td><span data-ttu-id="ba76f-214">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-215">Noteikts ID, Grupa vai Visi, un Resursam raksturīgs, Grupa vai Visi</span><span class="sxs-lookup"><span data-stu-id="ba76f-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-216">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="ba76f-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-217">Pēc</span><span class="sxs-lookup"><span data-stu-id="ba76f-217">After</span></span></td>
<td><span data-ttu-id="ba76f-218">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba76f-219">Līdzprodukta ražošana</span><span class="sxs-lookup"><span data-stu-id="ba76f-219">Co-product production</span></span></td>
<td><span data-ttu-id="ba76f-220">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="ba76f-220">Registration</span></span></td>
<td><span data-ttu-id="ba76f-221">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="ba76f-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-222">Nav</span><span class="sxs-lookup"><span data-stu-id="ba76f-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="ba76f-223">Visi</span><span class="sxs-lookup"><span data-stu-id="ba76f-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ba76f-224">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="ba76f-224">Report as finished</span></span></td>
<td><span data-ttu-id="ba76f-225">Pirms</span><span class="sxs-lookup"><span data-stu-id="ba76f-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-226">Pēc</span><span class="sxs-lookup"><span data-stu-id="ba76f-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba76f-227">Nākamajā tabulā ir plašāka informācija par to, kā kvalitātes pārbaudes pasūtījumus var ģenerēt specifiskiem procesu tipiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="ba76f-228">Procesa tips</span><span class="sxs-lookup"><span data-stu-id="ba76f-228">Type of process</span></span></th>
<th><span data-ttu-id="ba76f-229">Kad kvalitātes pārbaudes pasūtījumus var ģenerēt automātiski</span><span class="sxs-lookup"><span data-stu-id="ba76f-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="ba76f-230">Kad kvalitātes pārbaudes pasūtījums var ģenerēt, ja ir nepieciešama destruktīvā testēšana</span><span class="sxs-lookup"><span data-stu-id="ba76f-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="ba76f-231">Nosacījuma informācija</span><span class="sxs-lookup"><span data-stu-id="ba76f-231">Condition information</span></span></th>
<th><span data-ttu-id="ba76f-232">Manuālas ģenerēšanas informācija</span><span class="sxs-lookup"><span data-stu-id="ba76f-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="ba76f-233">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="ba76f-233">Purchase order</span></span></td>
<td><span data-ttu-id="ba76f-234">Pirms vai pēc tam, kad saņemtajam materiālam tiek grāmatots saņemšanas saraksts vai produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="ba76f-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="ba76f-235">Pēc tam, kad saņemtajam materiālam tiek grāmatota produktu ieejas plūsma, jo šim materiālam ir jābūt pieejamam destruktīvajai testēšanai</span><span class="sxs-lookup"><span data-stu-id="ba76f-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="ba76f-236">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="ba76f-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ba76f-237">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pirkšanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-238">Karantīnas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="ba76f-238">Quarantine order</span></span></td>
<td><span data-ttu-id="ba76f-239">Pirms vai pēc tam, kad karantīnas pasūtījums tiek ziņots kā pabeigts vai beidzies</span><span class="sxs-lookup"><span data-stu-id="ba76f-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="ba76f-240">Nevar ģenerēt kvalitātes pārbaudes pasūtījumus, kam ir nepieciešami destruktīvi testi.</span><span class="sxs-lookup"><span data-stu-id="ba76f-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="ba76f-241">Tiek pieņemts, ka karantīnas pasūtījuma funkcionalitāte nodrošina atbrīvošanos no iznīcinātā materiāla.</span><span class="sxs-lookup"><span data-stu-id="ba76f-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="ba76f-242">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="ba76f-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ba76f-243">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst karantīnas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-244">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="ba76f-244">Sales order</span></span></td>
<td><span data-ttu-id="ba76f-245">Pirms plānotas izdošanas procesa vai pavadzīmes atjaunināšanas krājumiem, kas tiek sūti</span><span class="sxs-lookup"><span data-stu-id="ba76f-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="ba76f-246">Jebkurā posmā</span><span class="sxs-lookup"><span data-stu-id="ba76f-246">At any step</span></span></td>
<td><span data-ttu-id="ba76f-247">Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu, krājumu vai debitoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="ba76f-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ba76f-248">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pārdošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-249">Ražošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="ba76f-249">Production order</span></span></td>
<td><span data-ttu-id="ba76f-250">Pirms vai pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="ba76f-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="ba76f-251">Pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="ba76f-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="ba76f-252">Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu vai krājumu, vai arī šo abu nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="ba76f-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ba76f-253">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst ražošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-254">Ražošanas pasūtījums, kuram ir maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="ba76f-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="ba76f-255">Pirms vai pēc tam, kad kādai operācijai ir pabeigta atskaite</span><span class="sxs-lookup"><span data-stu-id="ba76f-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="ba76f-256">Pēc tam, kad pēdējai operācijai ražošana ir ziņota kā pabeigta</span><span class="sxs-lookup"><span data-stu-id="ba76f-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="ba76f-257">Kvalitātes pārbaudes pasūtījuma pieprasījums ar norādīt noteiktu vietu, krājumu vai operācijas resursu, vai arī šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="ba76f-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ba76f-258">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst maršruta operācijai, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-259">Krājumi</span><span class="sxs-lookup"><span data-stu-id="ba76f-259">Inventory</span></span></td>
<td><span data-ttu-id="ba76f-260">Kvalitātes pārbaudes pasūtījumu nevar automātiski ģenerēt transakcijai krājumu žurnālā vai arī pārsūtīšanas pasūtījuma transakcijām.</span><span class="sxs-lookup"><span data-stu-id="ba76f-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="ba76f-261">Krājuma daudzumam noliktavā ir manuāli jāizveido kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="ba76f-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="ba76f-262">Fiziski rīcībā esošie krājumi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="ba76f-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="ba76f-263">Kvalitātes pārbaudes pasūtījuma automātiskās ģenerēšanas piemēri</span><span class="sxs-lookup"><span data-stu-id="ba76f-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="ba76f-264">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="ba76f-264">Purchasing</span></span>

<span data-ttu-id="ba76f-265">Pirkšanā, ja iestatāt lauku **Notikuma veids** uz **Produktu ieejas plūsma** un lauku **Izpilde**, kas atrodas lapā **Kvalitātes piesaistes** uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="ba76f-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="ba76f-266">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Jā**, katrai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu un iestatījumiem krājumu iztveršanā.</span><span class="sxs-lookup"><span data-stu-id="ba76f-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="ba76f-267">Katru reizi, kad tiek saņemts daudzums atbilstoši pirkšanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="ba76f-268">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Nē**, pirmajai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="ba76f-269">Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no izsekošanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="ba76f-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="ba76f-270">Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākām ieejas plūsmām atbilstoši pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="ba76f-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="ba76f-271">Ražošana</span><span class="sxs-lookup"><span data-stu-id="ba76f-271">Production</span></span>

<span data-ttu-id="ba76f-272">Ražošanā, ja iestatāt lauku **Notikuma veids** uz **Norādīts kā pabeigts** un lauku **Izpilde**, kas atrodas lapā **Kvalitātes piesaistes** uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="ba76f-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="ba76f-273">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Jā**, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz katru pabeigto daudzumu un iestatījumiem krājumu iztveršanā.</span><span class="sxs-lookup"><span data-stu-id="ba76f-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="ba76f-274">Katru reizi, kad tiek daudzums tiek norādīts kā pabeigts atbilstoši ražošanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko pabeigto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="ba76f-275">Šī ģenerēšanas loģika ir saskaņota ar pirkšanu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="ba76f-276">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Nē**, pirmajā reizē, kad daudzums tiek norādīts kā pabeigts, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz pabeigto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="ba76f-277">Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no krājumu iztveršanas izsekošanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="ba76f-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="ba76f-278">Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākajiem pabeigtajiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="ba76f-279">Kvalitātes specifikācija</span><span class="sxs-lookup"><span data-stu-id="ba76f-279">Quality specification</span></span></th>
<th><span data-ttu-id="ba76f-280">Pēc atjauninātā daudzuma</span><span class="sxs-lookup"><span data-stu-id="ba76f-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="ba76f-281">Pēc izsekošanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="ba76f-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="ba76f-282">Rezultāts</span><span class="sxs-lookup"><span data-stu-id="ba76f-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="ba76f-283">Procentuālā attiecība: 10 %</span><span class="sxs-lookup"><span data-stu-id="ba76f-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="ba76f-284">Jā</span><span class="sxs-lookup"><span data-stu-id="ba76f-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="ba76f-285">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="ba76f-285">Batch number: No</span></span></p>
<p><span data-ttu-id="ba76f-286">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="ba76f-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="ba76f-287">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="ba76f-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="ba76f-288">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="ba76f-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="ba76f-289">Kvalitātes pārbaudes pasūtījums #1 3 vienumiem (10 % no 30)</span><span class="sxs-lookup"><span data-stu-id="ba76f-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ba76f-290">Pabeigto krājumu daudzums 70</span><span class="sxs-lookup"><span data-stu-id="ba76f-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="ba76f-291">Kvalitātes pārbaudes pasūtījums #2 7 vienumiem (10 % no atlikušā pasūtījuma daudzuma, kas šajā gadījumā ir vienāds ar 70)</span><span class="sxs-lookup"><span data-stu-id="ba76f-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-292">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="ba76f-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="ba76f-293">Nē</span><span class="sxs-lookup"><span data-stu-id="ba76f-293">No</span></span></td>
<td>
<p><span data-ttu-id="ba76f-294">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="ba76f-294">Batch number: No</span></span></p>
<p><span data-ttu-id="ba76f-295">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="ba76f-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="ba76f-296">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="ba76f-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="ba76f-297">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="ba76f-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="ba76f-298">Kvalitātes pārbaudes pasūtījums #1 vienumam 1 (pirmajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība ir 1)</span><span class="sxs-lookup"><span data-stu-id="ba76f-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="ba76f-299">Kvalitātes pārbaudes pasūtījums #2 vienumam 1 (atlikušajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība joprojām ir 1)</span><span class="sxs-lookup"><span data-stu-id="ba76f-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ba76f-300">Pabeigto krājumu daudzums 10</span><span class="sxs-lookup"><span data-stu-id="ba76f-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="ba76f-301">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ba76f-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ba76f-302">Pabeigto krājumu daudzums 60</span><span class="sxs-lookup"><span data-stu-id="ba76f-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="ba76f-303">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ba76f-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-304">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="ba76f-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="ba76f-305">Jā</span><span class="sxs-lookup"><span data-stu-id="ba76f-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="ba76f-306">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="ba76f-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="ba76f-307">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="ba76f-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="ba76f-308">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="ba76f-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="ba76f-309">Norādīt kā pabeigtu vienumam 3: 1 #b1 #s1; 1 #b2, #s2; un 1 #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="ba76f-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="ba76f-310">Kvalitātes pārbaudes pasūtījums #1 1 vienumam no partijas #b1, sērijas #s1</span><span class="sxs-lookup"><span data-stu-id="ba76f-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="ba76f-311">Kvalitātes pārbaudes pasūtījums #2 1 vienumam no partijas #b2, sērijas #s2</span><span class="sxs-lookup"><span data-stu-id="ba76f-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="ba76f-312">Kvalitātes pārbaudes pasūtījums #3 1 vienumam no partijas #b3, sērijas #s3</span><span class="sxs-lookup"><span data-stu-id="ba76f-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ba76f-313">Norādīt kā pabeigtu vienumam 2: 1 #b4, #s4 un 1 #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="ba76f-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="ba76f-314">Kvalitātes pārbaudes pasūtījums #4 1 vienumam no partijas #b4, sērijas #s4</span><span class="sxs-lookup"><span data-stu-id="ba76f-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="ba76f-315">Kvalitātes pārbaudes pasūtījums #5 1 vienumam no partijas #b5, sērijas #s5</span><span class="sxs-lookup"><span data-stu-id="ba76f-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="ba76f-316"><strong>Piezīme:</strong> partiju var izmantot atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="ba76f-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="ba76f-317">Fiksēts daudzums: 2</span><span class="sxs-lookup"><span data-stu-id="ba76f-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="ba76f-318">Nē</span><span class="sxs-lookup"><span data-stu-id="ba76f-318">No</span></span></td>
<td>
<p><span data-ttu-id="ba76f-319">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="ba76f-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="ba76f-320">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="ba76f-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="ba76f-321">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="ba76f-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="ba76f-322">Norādīt kā pabeigtu vienumam 4: 1 #b1 #s1; 1 #b2, #s2; un 1 #b3, #s3 un 1 #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="ba76f-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="ba76f-323">Kvalitātes pārbaudes pasūtījums #1 1 vienumam no partijas #b1, sērijas #s1</span><span class="sxs-lookup"><span data-stu-id="ba76f-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="ba76f-324">Kvalitātes pārbaudes pasūtījums #2 1 vienumam no partijas #b2, sērijas #s2</span><span class="sxs-lookup"><span data-stu-id="ba76f-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="ba76f-325">Kvalitātes pārbaudes pasūtījums #3 1 vienumam no partijas #b3, sērijas #s3</span><span class="sxs-lookup"><span data-stu-id="ba76f-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="ba76f-326">Kvalitātes pārbaudes pasūtījums #4 1 vienumam no partijas #b4, sērijas #s4</span><span class="sxs-lookup"><span data-stu-id="ba76f-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="ba76f-327">Kvalitātes pārbaudes pasūtījums #5 vienumam 2 bez atsauces uz partijas un sērijas numuru</span><span class="sxs-lookup"><span data-stu-id="ba76f-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ba76f-328">Norādīt kā pabeigtu vienumam 6: 1 #b5 #s5; 1 #b6, #s6; 1 #b7, #s7; 1 #b8, #s8; 1 #b9, #s9 un 1 #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="ba76f-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="ba76f-329">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ba76f-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ba76f-330">*Noliktavas procesu kvalitātes pārvaldības* līdzeklis pievieno iespējas kvalitātes pārbaudes pasūtījumu apstrādei ražošanai ar **Notikuma veidu**, kas iestatīts uz *Ziņot, kad pabeigts* un **Izpilde** iestatīts uz *Pēc*, un pirkšanai ar **Notikuma veidu**, kas iestatīts uz *Reģistrāciju*.</span><span class="sxs-lookup"><span data-stu-id="ba76f-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="ba76f-331">Detalizētu informāciju skatiet [Noliktavas procesu kvalitātes pārvaldība](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="ba76f-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="ba76f-332">Kvalitātes pārvaldības lapas</span><span class="sxs-lookup"><span data-stu-id="ba76f-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba76f-333">Lapa</span><span class="sxs-lookup"><span data-stu-id="ba76f-333">Page</span></span></th>
<th><span data-ttu-id="ba76f-334">apraksts</span><span class="sxs-lookup"><span data-stu-id="ba76f-334">Description</span></span></th>
<th><span data-ttu-id="ba76f-335">Paraugs</span><span class="sxs-lookup"><span data-stu-id="ba76f-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ba76f-336">Kvalitātes piesaistes</span><span class="sxs-lookup"><span data-stu-id="ba76f-336">Quality associations</span></span></td>
<td><span data-ttu-id="ba76f-337">Skatiet šī raksta iepriekšējās sadaļas.</span><span class="sxs-lookup"><span data-stu-id="ba76f-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="ba76f-338">Kvalitātes saistība ģenerētajam kvalitātes pārbaudes pasūtījumam definē visu tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="ba76f-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="ba76f-339">Transakcijas notikums</span><span class="sxs-lookup"><span data-stu-id="ba76f-339">The transaction event</span></span></li>
<li><span data-ttu-id="ba76f-340">Testu kopa, kas šiem krājumiem ir jāveic</span><span class="sxs-lookup"><span data-stu-id="ba76f-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="ba76f-341">Pieņemamais kvalitātes līmenis (AQL)</span><span class="sxs-lookup"><span data-stu-id="ba76f-341">The AQL</span></span></li>
<li><span data-ttu-id="ba76f-342">Iztveršanas plāns</span><span class="sxs-lookup"><span data-stu-id="ba76f-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="ba76f-343">Ir jādefinē kvalitātes piesaiste katrai biznesa procesā ietvertajai variācijai, kam ir automātiski jāveido kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ba76f-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="ba76f-344">Piemēram, kvalitātes pārbaudes pasūtījumu var ģenerēt biznesa procesos, kas paredzēti pirkšanas pasūtījumiem, karantīnas pasūtījumiem, pārdošanas pasūtījumiem un ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba76f-345">Testi</span><span class="sxs-lookup"><span data-stu-id="ba76f-345">Tests</span></span></td>
<td><span data-ttu-id="ba76f-346">Izmantojiet šo lapu, lai definētu un skatītu atsevišķos testus, kas nosaka, vai preces atbilst kvalitātes specifikācijām.</span><span class="sxs-lookup"><span data-stu-id="ba76f-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="ba76f-347">Vienu vai vairākus atsevišķus testus varat piešķirt testu grupai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="ba76f-348">Šajā gadījumā jums ir jānorāda arī testa specifiskā informācija, piemēram, pieņemamās mērījumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="ba76f-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="ba76f-349">Mērījumu vērtības tiek izmantotas kvantitatīvajiem testiem, un testa mainīgie tiek lietoti kvalitatīvajiem testiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="ba76f-350">Kvantitatīvajam testam testa tips ir <strong>Vesels skaitlis</strong> vai <strong>Daļskaitlis</strong>, un tam ir arī norādīta mērvienība.</span><span class="sxs-lookup"><span data-stu-id="ba76f-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="ba76f-351">Kvalitātes specifikācijas un testa rezultāti tiek izteikti kā skaitļi.</span><span class="sxs-lookup"><span data-stu-id="ba76f-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="ba76f-352">Kvalitatīvajam testam testa tips ir <strong>Opcija</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba76f-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="ba76f-353">Kvalitatīvajiem testiem ir nepieciešama papildinformācija par testa mainīgo, kas tiek mērīts, un tā uzskaitīšanas iespējam.</span><span class="sxs-lookup"><span data-stu-id="ba76f-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="ba76f-354">Kvalitātes specifikācijas un testa rezultāti tiek izteikti atbilstoši rezultātam.</span><span class="sxs-lookup"><span data-stu-id="ba76f-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="ba76f-355">Ražošanas uzņēmums iepirktajam materiālam veic divus testus: kvantitatīvo testu par materiāla kvalitāti un kvalitatīvo testu par iepakojuma bojājumu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="ba76f-356">Uzņēmums definē papildu informāciju par kvalitātes testu, lai identificētu testa mainīgo (bojāto iepakojumu) un tā rezultātus.</span><span class="sxs-lookup"><span data-stu-id="ba76f-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="ba76f-357">Uzņēmums izmanto lapu <strong>Testu grupas</strong>, lai abus testus piešķirtu testu grupai un norādītu testa specifisko informāciju.</span><span class="sxs-lookup"><span data-stu-id="ba76f-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="ba76f-358">Kvalitātes pasūtījumam tiek piešķirta testa grupā, tādējādi uzņēmums var ziņot testa rezultātus par diviem testiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba76f-359">Testa grupas</span><span class="sxs-lookup"><span data-stu-id="ba76f-359">Test groups</span></span></td>
<td><span data-ttu-id="ba76f-360">Izmantojiet šo lapu, lai iestatītu, rediģētu un apskatītu testu grupas un atsevišķus testus, kas ir piešķirti kādai testu grupai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="ba76f-361">Augšējā rūtī ir atainotas testu grupas, bet apakšējā rūtī ir atainoti testi, kas piešķirti atlasītajai testu grupai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="ba76f-362">Jūs testu grupai piešķirat vairākus ierobežojumus, piemēram, iztveršanas plānu, pieņemamo kvalitātes līmeni (AQL) un destruktīvās testēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="ba76f-363">Kad atsevišķu testu piešķirat testu grupai, jūs definējat papildu informāciju, piemēram, secību, dokumentus un derīguma datumus.</span><span class="sxs-lookup"><span data-stu-id="ba76f-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="ba76f-364">Kvantitatīvam testam jūsu definēta informācija ietver arī pieņemamās mērījumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="ba76f-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="ba76f-365">Kvalitatīvam testam šī informācija ietver testa mainīgo un noklusējuma iznākumu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="ba76f-366">Testa grupa, kas ir piešķirta kādam kvalitātes pārbaudes pasūtījumam, nosaka noklusējuma kopu ar testiem, kas ir jāizpilda norādītajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="ba76f-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="ba76f-367">Taču kvalitātes pārbaudes pasūtījumā testus varat pievienot, dzēst vai mainīt.</span><span class="sxs-lookup"><span data-stu-id="ba76f-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="ba76f-368">Katra testa rezultāti tiek uzrādīti kvalitātes pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="ba76f-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="ba76f-369">Ražošanas uzņēmums definē testu grupu katrai tās kvalitātes vadlīniju variācijai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="ba76f-370">Dažādās testu grupas parāda atšķirības iztveršanas plānos, kopā izpildāmo testu kopās, pieņemamajos kvalitātes līmeņos AQL un citos faktoros.</span><span class="sxs-lookup"><span data-stu-id="ba76f-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="ba76f-371">Kvantitatīvajiem testiem pastāv arī pieņemamo mērījumu vērtību atšķirības.</span><span class="sxs-lookup"><span data-stu-id="ba76f-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="ba76f-372">Lai īstenotu savas kvalitātes vadlīnijas, automātiski ģenerētiem kvalitātes pārbaudes pasūtījumiem lapā <strong>Kvalitātes saistības</strong> uzņēmums piešķir testu grupu katrai kārtulai, kā arī piešķir testu grupu manuāli izveidotajiem kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba76f-373">Krājumu kvalitātes grupas</span><span class="sxs-lookup"><span data-stu-id="ba76f-373">Item quality groups</span></span></td>
<td><span data-ttu-id="ba76f-374">Izmantojiet šo lapu, lai iestatītu, rediģētu un skatītu krājumus, kas ir piešķirti kvalitātes grupai vai kvalitātes grupām, kuras ir piešķirtas kādam krājumam.</span><span class="sxs-lookup"><span data-stu-id="ba76f-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="ba76f-375">Kvalitātes grupa norāda kopējās testēšanas vajadzības krājumam.</span><span class="sxs-lookup"><span data-stu-id="ba76f-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="ba76f-376">Kad lapā <strong>Testu grupas</strong> ir definētas testa prasības, varat definēt kārtulas automātiskai kvalitātes pārbaudes pasūtījumu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="ba76f-377">Lai vienkāršotu šo procesu, netiek definētas kārtulas atsevišķiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="ba76f-378">Tā vietā jūs definējat kārtulas kvalitātes grupai, izmantojot lapu <strong>Kvalitātes saistības</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba76f-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="ba76f-379">Varat arī izmantot lapu <strong>Krājuma kvalitātes grupas</strong> atlasītai kvalitātes grupai, lai šai grupai piešķirtu atbilstošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="ba76f-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="ba76f-380">Varat arī izmantot lapu <strong>Krājuma kvalitātes grupas</strong> atlasītam krājumam, lai šim krājumam piešķirtu atbilstošās kvalitātes grupas.</span><span class="sxs-lookup"><span data-stu-id="ba76f-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="ba76f-381">Ražošanas uzņēmums iegādājas vairākus izejmateriālus, kuriem ir tādas pašas testēšanas vajadzības ienākošajai pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="ba76f-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="ba76f-382">Uzņēmums definē kvalitātes grupu un pēc tam piešķir krājumu numurus, kas ir saistīti ar izejmateriāliem šai grupai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="ba76f-383">Vēlāk uzņēmums iegādājas jauna tipa izejmateriālu, kuram ir tādas pašas testēšanas vajadzības.</span><span class="sxs-lookup"><span data-stu-id="ba76f-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="ba76f-384">Tā vietā, lai jaunajam materiālam iestatītu jaunas testēšanas vajadzības, jaunā materiāla krājumu kodu uzņēmums pievieno jau esošajai kvalitātes grupai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="ba76f-385">Tas pats ražošanas uzņēmums ražo arī krājumus, kuriem ir tādas pašas ražošanas testēšanas vajadzības, un krājumus, kuriem ir tādas pašas vajadzības, sūta uz testēšanu pirms sūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="ba76f-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="ba76f-386">Uzņēmums definē divas papildu kvalitātes grupas un pēc tam piešķir atbilstošos krājumu numurus katrai grupai.</span><span class="sxs-lookup"><span data-stu-id="ba76f-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba76f-387">Testa mainīgie lielumi</span><span class="sxs-lookup"><span data-stu-id="ba76f-387">Test variables</span></span></td>
<td><span data-ttu-id="ba76f-388">Izmantojiet šo lapu, lai definētu un skatītu mainīgos, kas ir saistīti ar kādu kvalitātes testu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="ba76f-389">Katram mainīgajam varat definēt uzskaitītos iznākumus, kas apzīmē iespējamās opcijas.</span><span class="sxs-lookup"><span data-stu-id="ba76f-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="ba76f-390">Testus jūs definējat lapā <strong>Testi</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba76f-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="ba76f-391">Kvalitatīvajiem testiem testa tipu jūs iestatāt uz <strong>Opcija</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba76f-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="ba76f-392">Izmantojiet lapu <strong>Testu grupas</strong>, lai testa mainīgo piešķirtu atsevišķam testam.</span><span class="sxs-lookup"><span data-stu-id="ba76f-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="ba76f-393">Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="ba76f-394">Šajā pārbaudes testā ir vairāki mainīgie.</span><span class="sxs-lookup"><span data-stu-id="ba76f-394">This inspection test has several variables.</span></span> <span data-ttu-id="ba76f-395">Viens mainīgais ir garša, un šī mainīgā iespējamie iznākumi ir laba vai slikta.</span><span class="sxs-lookup"><span data-stu-id="ba76f-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="ba76f-396">Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.</span><span class="sxs-lookup"><span data-stu-id="ba76f-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba76f-397">Testa mainīgo lielumu iznākumi</span><span class="sxs-lookup"><span data-stu-id="ba76f-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="ba76f-398">Izmantojiet šo lapu, lai iestatītu, rediģētu un skatītu iespējamos testa rezultātus ar kvalitatīvo testu saistītam testa mainīgajam.</span><span class="sxs-lookup"><span data-stu-id="ba76f-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="ba76f-399">Katram iznākumam jums ir jāpiešķir statuss <strong>sekmīgs</strong> vai <strong>nesekmīgs</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba76f-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="ba76f-400">Jums ir jādefinē mainīgais un tā iznākumi katram kvalitatīvajam testam, kas ir definēts lapā <strong>Testi</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba76f-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="ba76f-401">(Kvalitatīvajiem testiem testa tips lapā <strong>Testi</strong> ir iestatīts uz <strong>Opcija</strong>.) Lai testa mainīgo un noklusējuma iznākumu piešķirtu atsevišķam kvalitatīvajam testam, izmantojiet lapu <strong>Testu grupas</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba76f-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="ba76f-402">Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu.</span><span class="sxs-lookup"><span data-stu-id="ba76f-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="ba76f-403">Šajā pārbaudes testā ir vairāki mainīgie.</span><span class="sxs-lookup"><span data-stu-id="ba76f-403">This inspection test has of several variables.</span></span> <span data-ttu-id="ba76f-404">Viens mainīgais ir garša, un šī mainīgā iespējamie iznākumi ir laba vai slikta.</span><span class="sxs-lookup"><span data-stu-id="ba76f-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="ba76f-405">Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.</span><span class="sxs-lookup"><span data-stu-id="ba76f-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="ba76f-406">Katram iznākumam tiek piešķirts ir statuss <strong>sekmīgs</strong> vai <strong>nesekmīgs</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba76f-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="ba76f-407">Katra mainīgā pārbaudes testa laikā pārbaudītājs ziņo testa rezultātu, izvēloties vienu no rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="ba76f-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="ba76f-408">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ba76f-408">Additional resources</span></span>
--------

[<span data-ttu-id="ba76f-409">Kvalitātes pārvaldības procesi</span><span class="sxs-lookup"><span data-stu-id="ba76f-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="ba76f-410">Neatbilstības pārvaldība</span><span class="sxs-lookup"><span data-stu-id="ba76f-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="ba76f-411">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="ba76f-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
