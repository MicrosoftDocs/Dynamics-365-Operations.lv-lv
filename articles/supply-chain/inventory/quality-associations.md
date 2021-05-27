---
title: Kvalitātes piesaistes
description: Šajā tēmā aprakstīts, kā jūs varat izmantot kvalitātes saistības Microsoft Dynamics 365 Supply Chain Management, lai automātiski izveidotu kvalitātes pasūtījumus, kas ir saistīti ar jūsu pārdošanas, pirkšanas un ražošanas procesiem.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6fab1b89b7e58d9e443c27da03a6b13afcc9c6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022328"
---
# <a name="quality-associations"></a><span data-ttu-id="d8d7a-103">Kvalitātes piesaistes</span><span class="sxs-lookup"><span data-stu-id="d8d7a-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8d7a-104">Šajā tēmā aprakstīts, kā jūs varat izmantot kvalitātes saistības Microsoft Dynamics 365 Supply Chain Management, lai automātiski izveidotu kvalitātes pasūtījumus, kas ir saistīti ar jūsu pārdošanas, pirkšanas un ražošanas procesiem.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="d8d7a-105">Kvalitātes saistība ģenerētajam kvalitātes pārbaudes pasūtījumam definē visu tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="d8d7a-106">Transakcijas notikums</span><span class="sxs-lookup"><span data-stu-id="d8d7a-106">The transaction event</span></span>
- <span data-ttu-id="d8d7a-107">Testu kopa, kas šiem krājumiem ir jāveic</span><span class="sxs-lookup"><span data-stu-id="d8d7a-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="d8d7a-108">Pieņemamais kvalitātes līmenis (acceptable quality level - AQL)</span><span class="sxs-lookup"><span data-stu-id="d8d7a-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="d8d7a-109">Iztveršanas plāns</span><span class="sxs-lookup"><span data-stu-id="d8d7a-109">The sampling plan</span></span>

<span data-ttu-id="d8d7a-110">Ir jādefinē kvalitātes piesaiste katrai biznesa procesā ietvertajai variācijai, kam ir automātiski jāveido kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="d8d7a-111">Piemēram, kvalitātes pārbaudes pasūtījumu var ģenerēt biznesa procesos, kas paredzēti pirkšanas pasūtījumiem, karantīnas pasūtījumiem, pārdošanas pasūtījumiem un ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="d8d7a-112">Darbs ar kvalitātes saistībām</span><span class="sxs-lookup"><span data-stu-id="d8d7a-112">Working with quality associations</span></span>

<span data-ttu-id="d8d7a-113">Biznesa process, kas izmanto kvalitātes saistību, var būt saistīts ar dažādiem avota dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem vai ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="d8d7a-114">Katrs kvalitātes saistības ieraksts nosaka testu kopu, pieņemamās kvalitātes līmeni (AQL) un iztveršanas plānu, kas tiek lietoti ģenerētajiem kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="d8d7a-115">Katrai biznesa procesa variācijai jums ir jādefinē kvalitātes saistības ieraksts.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="d8d7a-116">Piemēram, varat iestatīt kvalitātes saistību, kas ģenerē kvalitātes pārbaudes pasūtījumu, kad tiek atjaunināta pirkšanas pasūtījuma produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="d8d7a-117">Atkarībā no izpildes plāna iestatījumiem pats aktivizēšanas process var tikt bloķēts, kamēr ir atvērts kvalitātes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="d8d7a-118">Alternatīvi sekojošie procesi, piemēram, pirkšanas pasūtījuma rēķina izrakstīšana, var tikt bloķēti.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="d8d7a-119">Kamēr pastāv atvērti kvalitātes pārbaudes pasūtījumi, krājumu daudzumi tiek automātiski bloķēti no izsniegšanas.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="d8d7a-120">Atkarībā no lauka **Pilna bloķēšana** iestatījuma lapā **Krājumu iztveršana**, šis daudzums ir vai nu kvalitātes pasūtījumā norādītais daudzums, vai pirmdokumenta rindā norādītais daudzums.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="d8d7a-121">Papildinformāciju skatiet [Kvalitātes pārvaldības krājumu iztveršana](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="d8d7a-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="d8d7a-122">Noteiktam biznesa procesam kvalitātes saistības ieraksts identificē notikumu un nosacījumus, kādiem tiek ģenerēts kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="d8d7a-123">Nosacījumi var attiekties uz vietu vai juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="d8d7a-124">Kvalitātes pārbaudes pasūtījumu, kur ir iesaistīti destruktīvie testi, var ģenerēt tikai tad, ja attiecīgajam notikumam pastāv rīcībā esoši krājumi.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="d8d7a-125">Lai strādātu ar kvalitātes saistībām, dodieties uz **Krājumu pārvaldība \> Iestatījums \> Kvalitātes kontrole \> Kvalitātes saistības**.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="d8d7a-126">Nākamajos piemēros ir parādīts, kā kvalitātes saistības ieraksts tiek definēts katra darījumu procesa variācijām.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="d8d7a-127">Katram piemēram nākamajā tabulā ir sniegts kopsavilkums par kvalitātes saistības ieraksta definētajiem notikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d8d7a-128">Atsauces veids</span><span class="sxs-lookup"><span data-stu-id="d8d7a-128">Reference type</span></span></th>
<th><span data-ttu-id="d8d7a-129">Notikuma veids</span><span class="sxs-lookup"><span data-stu-id="d8d7a-129">Event type</span></span></th>
<th><span data-ttu-id="d8d7a-130">Izpilde</span><span class="sxs-lookup"><span data-stu-id="d8d7a-130">Execution</span></span></th>
<th><span data-ttu-id="d8d7a-131">Notikumu aizturēšana</span><span class="sxs-lookup"><span data-stu-id="d8d7a-131">Event blocking</span></span></th>
<th><span data-ttu-id="d8d7a-132">Dokumenta atsauce</span><span class="sxs-lookup"><span data-stu-id="d8d7a-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d8d7a-133">Krājumi</span><span class="sxs-lookup"><span data-stu-id="d8d7a-133">Inventory</span></span></td>
<td><span data-ttu-id="d8d7a-134">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-134">Not applicable</span></span></td>
<td><span data-ttu-id="d8d7a-135">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-135">Not applicable</span></span></td>
<td><span data-ttu-id="d8d7a-136">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-136">None</span></span></td>
<td><span data-ttu-id="d8d7a-137">Visi</span><span class="sxs-lookup"><span data-stu-id="d8d7a-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="d8d7a-138">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="d8d7a-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="d8d7a-139">Izdošanas process ir ieplānots</span><span class="sxs-lookup"><span data-stu-id="d8d7a-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="d8d7a-140">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-140">Before</span></span></td>
<td><span data-ttu-id="d8d7a-141">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="d8d7a-142">Konkrēts ID, Grupa vai tikai Visi</span><span class="sxs-lookup"><span data-stu-id="d8d7a-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-143">Izdošanas process</span><span class="sxs-lookup"><span data-stu-id="d8d7a-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-144">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="d8d7a-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-145">Rēķins</span><span class="sxs-lookup"><span data-stu-id="d8d7a-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d8d7a-146">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="d8d7a-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-147">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-147">Before</span></span></td>
<td><span data-ttu-id="d8d7a-148">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-149">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="d8d7a-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-150">Rēķins</span><span class="sxs-lookup"><span data-stu-id="d8d7a-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="d8d7a-151">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="d8d7a-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="d8d7a-152">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="d8d7a-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="d8d7a-153">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-153">Before</span></span></td>
<td><span data-ttu-id="d8d7a-154">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-155">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="d8d7a-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-156">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="d8d7a-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-157">Rēķins</span><span class="sxs-lookup"><span data-stu-id="d8d7a-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d8d7a-158">Pēc</span><span class="sxs-lookup"><span data-stu-id="d8d7a-158">After</span></span></td>
<td><span data-ttu-id="d8d7a-159">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-160">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="d8d7a-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-161">Rēķins</span><span class="sxs-lookup"><span data-stu-id="d8d7a-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d8d7a-162">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="d8d7a-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-163">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-163">Not applicable</span></span></td>
<td><span data-ttu-id="d8d7a-164">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-165">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="d8d7a-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-166">Rēķins</span><span class="sxs-lookup"><span data-stu-id="d8d7a-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d8d7a-167">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="d8d7a-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-168">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-168">Before</span></span></td>
<td><span data-ttu-id="d8d7a-169">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-170">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="d8d7a-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-171">Rēķins</span><span class="sxs-lookup"><span data-stu-id="d8d7a-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d8d7a-172">Pēc</span><span class="sxs-lookup"><span data-stu-id="d8d7a-172">After</span></span></td>
<td><span data-ttu-id="d8d7a-173">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-174">Rēķins</span><span class="sxs-lookup"><span data-stu-id="d8d7a-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="d8d7a-175">Ražošana</span><span class="sxs-lookup"><span data-stu-id="d8d7a-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-176">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="d8d7a-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-177">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-177">Not applicable</span></span></td>
<td><span data-ttu-id="d8d7a-178">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="d8d7a-179">Visi</span><span class="sxs-lookup"><span data-stu-id="d8d7a-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-180">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-181">Beigt</span><span class="sxs-lookup"><span data-stu-id="d8d7a-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d8d7a-182">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-183">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-183">Before</span></span></td>
<td><span data-ttu-id="d8d7a-184">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-185">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-186">Beigt</span><span class="sxs-lookup"><span data-stu-id="d8d7a-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d8d7a-187">Pēc</span><span class="sxs-lookup"><span data-stu-id="d8d7a-187">After</span></span></td>
<td><span data-ttu-id="d8d7a-188">Nav</span><span class="sxs-lookup"><span data-stu-id="d8d7a-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-189">Beigt</span><span class="sxs-lookup"><span data-stu-id="d8d7a-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d8d7a-190">Karantīna</span><span class="sxs-lookup"><span data-stu-id="d8d7a-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-191">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="d8d7a-192">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-192">Before</span></span></td>
<td><span data-ttu-id="d8d7a-193">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-194">Beigt</span><span class="sxs-lookup"><span data-stu-id="d8d7a-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-195">Pēc</span><span class="sxs-lookup"><span data-stu-id="d8d7a-195">After</span></span></td>
<td><span data-ttu-id="d8d7a-196">Beigt</span><span class="sxs-lookup"><span data-stu-id="d8d7a-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-197">Beigt</span><span class="sxs-lookup"><span data-stu-id="d8d7a-197">End</span></span></td>
<td><span data-ttu-id="d8d7a-198">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-198">Before</span></span></td>
<td><span data-ttu-id="d8d7a-199">Beigt</span><span class="sxs-lookup"><span data-stu-id="d8d7a-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d8d7a-200">Maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="d8d7a-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-201">Ziņot kā pabeigtu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="d8d7a-202">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-202">Before</span></span></td>
<td><span data-ttu-id="d8d7a-203">Neviens</span><span class="sxs-lookup"><span data-stu-id="d8d7a-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-204">Noteikts ID, Grupa vai Visi, un raksturīgs Resurss, Grupa vai Visi</span><span class="sxs-lookup"><span data-stu-id="d8d7a-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-205">Ziņot kā pabeigtu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-206">Pēc</span><span class="sxs-lookup"><span data-stu-id="d8d7a-206">After</span></span></td>
<td><span data-ttu-id="d8d7a-207">Neviens</span><span class="sxs-lookup"><span data-stu-id="d8d7a-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d8d7a-208">Līdzprodukta ražošana</span><span class="sxs-lookup"><span data-stu-id="d8d7a-208">Co-product production</span></span></td>
<td><span data-ttu-id="d8d7a-209">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="d8d7a-209">Registration</span></span></td>
<td><span data-ttu-id="d8d7a-210">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-211">Neviens</span><span class="sxs-lookup"><span data-stu-id="d8d7a-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="d8d7a-212">Visu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d8d7a-213">Ziņot kā pabeigtu</span><span class="sxs-lookup"><span data-stu-id="d8d7a-213">Report as finished</span></span></td>
<td><span data-ttu-id="d8d7a-214">Pirms</span><span class="sxs-lookup"><span data-stu-id="d8d7a-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-215">Pēc</span><span class="sxs-lookup"><span data-stu-id="d8d7a-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d8d7a-216">Līdzeklis *Noliktavas procesu kvalitātes pārvaldība* pievieno iespējas kvalitātes pārbaudes pasūtījumu apstrādei ražošanai, kur lauks **Notikuma veids**, kas iestatīts uz *Ziņot, kad pabeigts* un lauks **Izpilde** iestatīts uz *Pēc*, un pirkšanai, kur lauks **Notikuma veids**, kas iestatīts uz *Reģistrāciju*.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="d8d7a-217">Papildinformāciju skatiet [Noliktavas procesu kvalitātes pārvaldība](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="d8d7a-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="d8d7a-218">Nākamajā tabulā ir plašāka informācija par to, kā kvalitātes pārbaudes pasūtījumus var ģenerēt specifiskiem procesu tipiem.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="d8d7a-219">Procesa tips</span><span class="sxs-lookup"><span data-stu-id="d8d7a-219">Type of process</span></span></th>
<th><span data-ttu-id="d8d7a-220">Kad kvalitātes pārbaudes pasūtījumus var ģenerēt automātiski</span><span class="sxs-lookup"><span data-stu-id="d8d7a-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="d8d7a-221">Kad kvalitātes pārbaudes pasūtījums var ģenerēt, ja ir nepieciešama destruktīvā testēšana</span><span class="sxs-lookup"><span data-stu-id="d8d7a-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="d8d7a-222">Nosacījuma informācija</span><span class="sxs-lookup"><span data-stu-id="d8d7a-222">Condition information</span></span></th>
<th><span data-ttu-id="d8d7a-223">Manuālas ģenerēšanas informācija</span><span class="sxs-lookup"><span data-stu-id="d8d7a-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d8d7a-224">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="d8d7a-224">Purchase order</span></span></td>
<td><span data-ttu-id="d8d7a-225">Pirms vai pēc tam, kad saņemtajam materiālam tiek grāmatots saņemšanas saraksts vai produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="d8d7a-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="d8d7a-226">Pēc tam, kad saņemtajam materiālam tiek grāmatota produktu ieejas plūsma, jo šim materiālam ir jābūt pieejamam destruktīvajai testēšanai</span><span class="sxs-lookup"><span data-stu-id="d8d7a-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="d8d7a-227">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d8d7a-228">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pirkšanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-229">Karantīnas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="d8d7a-229">Quarantine order</span></span></td>
<td><span data-ttu-id="d8d7a-230">Pirms vai pēc tam, kad karantīnas pasūtījums tiek ziņots kā pabeigts vai beidzies</span><span class="sxs-lookup"><span data-stu-id="d8d7a-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="d8d7a-231">Nevar ģenerēt kvalitātes pārbaudes pasūtījumus, kam ir nepieciešami destruktīvie testi.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="d8d7a-232">Tiek pieņemts, ka karantīnas pasūtījuma funkcionalitāte veic atbrīvošanos no iznīcinātā materiāla.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="d8d7a-233">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d8d7a-234">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst karantīnas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-235">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="d8d7a-235">Sales order</span></span></td>
<td><span data-ttu-id="d8d7a-236">Pirms plānotas izdošanas procesa vai pavadzīmes atjaunināšanas krājumiem, kas tiek sūti</span><span class="sxs-lookup"><span data-stu-id="d8d7a-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="d8d7a-237">Jebkurā posmā</span><span class="sxs-lookup"><span data-stu-id="d8d7a-237">At any step</span></span></td>
<td><span data-ttu-id="d8d7a-238">Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu, krājumu vai debitoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d8d7a-239">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pārdošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-240">Ražošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="d8d7a-240">Production order</span></span></td>
<td><span data-ttu-id="d8d7a-241">Pirms vai pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="d8d7a-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="d8d7a-242">Pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="d8d7a-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="d8d7a-243">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu vai krājumu, vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d8d7a-244">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst ražošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-245">Ražošanas pasūtījums, kuram ir maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="d8d7a-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="d8d7a-246">Pirms vai pēc tam, kad kādai operācijai ir pabeigta atskaite</span><span class="sxs-lookup"><span data-stu-id="d8d7a-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="d8d7a-247">Pēc tam, kad pēdējai operācijai ražošana ir ziņota kā pabeigta</span><span class="sxs-lookup"><span data-stu-id="d8d7a-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="d8d7a-248">Kvalitātes pārbaudes pasūtījuma pieprasījums ar norādīt noteiktu vietu, krājumu vai operācijas resursu, vai arī šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d8d7a-249">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst maršruta operācijai, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-250">Krājums</span><span class="sxs-lookup"><span data-stu-id="d8d7a-250">Inventory</span></span></td>
<td><span data-ttu-id="d8d7a-251">Kvalitātes pārbaudes pasūtījumu nevar automātiski ģenerēt transakcijai krājumu žurnālā vai arī pārsūtīšanas pasūtījuma transakcijām.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d8d7a-252">Krājumadaudzumam noliktavā ir manuāli jāizveido kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="d8d7a-253">Fiziski rīcībā esošie krājumi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="d8d7a-254">Automātisku kvalitātes pasūtījumu izveidošanas piemēri</span><span class="sxs-lookup"><span data-stu-id="d8d7a-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="d8d7a-255">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="d8d7a-255">Purchasing</span></span>

<span data-ttu-id="d8d7a-256">Pirkšanā, ja iestatāt lauku **Notikuma veids** uz *Produktu ieejas plūsma* un lauku **Izpilde**, kas atrodas lapā *Kvalitātes piesaistes* uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="d8d7a-257">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Jā*, katrai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu un iestatījumiem krājumu iztveršanā.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="d8d7a-258">Katru reizi, kad tiek saņemts daudzums atbilstoši pirkšanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="d8d7a-259">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Nē*, pirmajai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="d8d7a-260">Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no izsekošanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="d8d7a-261">Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākām ieejas plūsmām atbilstoši pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="d8d7a-262">Ražošana</span><span class="sxs-lookup"><span data-stu-id="d8d7a-262">Production</span></span>

<span data-ttu-id="d8d7a-263">Ražošanā, ja iestatāt lauku **Notikuma veids** uz *Norādīts kā pabeigts* un lauku **Izpilde**, kas atrodas lapā *Kvalitātes piesaistes* uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="d8d7a-264">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Jā*, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz katru pabeigto daudzumu un iestatījumiem krājumu iztveršanā.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="d8d7a-265">Katru reizi, kad tiek daudzums tiek norādīts kā pabeigts atbilstoši ražošanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko pabeigto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="d8d7a-266">Šī ģenerēšanas loģika ir saskaņota ar pirkšanu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="d8d7a-267">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Nē*, pirmajā reizē, kad daudzums tiek norādīts kā pabeigts, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz pabeigto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="d8d7a-268">Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no krājumu iztveršanas izsekošanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="d8d7a-269">Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākajiem pabeigtajiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d8d7a-270">Kvalitātes specifikācija</span><span class="sxs-lookup"><span data-stu-id="d8d7a-270">Quality specification</span></span></th>
<th><span data-ttu-id="d8d7a-271">Pēc atjauninātā daudzuma</span><span class="sxs-lookup"><span data-stu-id="d8d7a-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="d8d7a-272">Pēc izsekošanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="d8d7a-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="d8d7a-273">Rezultāts</span><span class="sxs-lookup"><span data-stu-id="d8d7a-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d8d7a-274">Procentuālā attiecība: 10 %</span><span class="sxs-lookup"><span data-stu-id="d8d7a-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="d8d7a-275">Jā</span><span class="sxs-lookup"><span data-stu-id="d8d7a-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="d8d7a-276">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-276">Batch number: No</span></span></p>
<p><span data-ttu-id="d8d7a-277">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="d8d7a-278">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="d8d7a-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="d8d7a-279">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="d8d7a-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="d8d7a-280">1. kvalitātes pārbaudes pasūtījums 3 vienumiem (10 % no 30)</span><span class="sxs-lookup"><span data-stu-id="d8d7a-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d8d7a-281">Pabeigto krājumu daudzums 70</span><span class="sxs-lookup"><span data-stu-id="d8d7a-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="d8d7a-282">2. kvalitātes pārbaudes pasūtījums 7 vienumiem (10 % no atlikušā pasūtījuma daudzuma, kas šajā gadījumā ir 70)</span><span class="sxs-lookup"><span data-stu-id="d8d7a-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-283">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="d8d7a-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="d8d7a-284">Nr.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-284">No</span></span></td>
<td>
<p><span data-ttu-id="d8d7a-285">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-285">Batch number: No</span></span></p>
<p><span data-ttu-id="d8d7a-286">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="d8d7a-287">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="d8d7a-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="d8d7a-288">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="d8d7a-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="d8d7a-289">1. kvalitātes pārbaudes pasūtījums vienumam 1 (pirmajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība ir 1)</span><span class="sxs-lookup"><span data-stu-id="d8d7a-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="d8d7a-290">2. kvalitātes pārbaudes pasūtījums vienumam 1 (atlikušajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība joprojām ir 1)</span><span class="sxs-lookup"><span data-stu-id="d8d7a-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d8d7a-291">Pabeigto krājumu daudzums 10</span><span class="sxs-lookup"><span data-stu-id="d8d7a-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="d8d7a-292">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d8d7a-293">Pabeigto krājumu daudzums 60</span><span class="sxs-lookup"><span data-stu-id="d8d7a-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="d8d7a-294">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-295">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="d8d7a-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="d8d7a-296">Jā</span><span class="sxs-lookup"><span data-stu-id="d8d7a-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="d8d7a-297">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="d8d7a-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="d8d7a-298">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="d8d7a-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="d8d7a-299">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="d8d7a-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="d8d7a-300">Pabeigts 3: 1 partijas numuram b1, sērijas numuram s1; 1 partijas numuram b2, sērijas numuram s2 un 1 partijas numuram b3, sērijas numuram s3</span><span class="sxs-lookup"><span data-stu-id="d8d7a-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="d8d7a-301">1. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b1, sērijas numura s1</span><span class="sxs-lookup"><span data-stu-id="d8d7a-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="d8d7a-302">2. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b2, sērijas numura s2</span><span class="sxs-lookup"><span data-stu-id="d8d7a-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="d8d7a-303">3. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b3, sērijas numura s3</span><span class="sxs-lookup"><span data-stu-id="d8d7a-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d8d7a-304">Pabeigts 2: 1 partijas numuram b4, sērijas numuram s4 un 1 partijas numuram b5, sērijas numuram s5</span><span class="sxs-lookup"><span data-stu-id="d8d7a-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="d8d7a-305">4. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b4, sērijas numura s4</span><span class="sxs-lookup"><span data-stu-id="d8d7a-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="d8d7a-306">5. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b5, sērijas numura s5</span><span class="sxs-lookup"><span data-stu-id="d8d7a-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="d8d7a-307"><strong>Piezīme:</strong> partiju var izmantot atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8d7a-308">Fiksēts daudzums: 2</span><span class="sxs-lookup"><span data-stu-id="d8d7a-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="d8d7a-309">Nr.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-309">No</span></span></td>
<td>
<p><span data-ttu-id="d8d7a-310">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="d8d7a-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="d8d7a-311">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="d8d7a-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="d8d7a-312">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="d8d7a-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="d8d7a-313">Pabeigts 4: 1 partijas numuram b1, sērijas numuram s1; 1 partijas numuram b2, sērijas numuram s2 un 1 partijas numuram b3, sērijas numuram s3; un 1 partijas numuram b4, sērijas numuram s4</span><span class="sxs-lookup"><span data-stu-id="d8d7a-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="d8d7a-314">1. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b1, sērijas numura s1</span><span class="sxs-lookup"><span data-stu-id="d8d7a-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="d8d7a-315">2. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b2, sērijas numura s2</span><span class="sxs-lookup"><span data-stu-id="d8d7a-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="d8d7a-316">3. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b3, sērijas numura s3</span><span class="sxs-lookup"><span data-stu-id="d8d7a-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="d8d7a-317">4. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b4, sērijas numura s4</span><span class="sxs-lookup"><span data-stu-id="d8d7a-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="d8d7a-318">Kvalitātes pārbaudes pasūtījums 5 vienumam 2 bez atsauces uz partijas numuru un sērijas numuru</span><span class="sxs-lookup"><span data-stu-id="d8d7a-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d8d7a-319">Pabeigts 6: 1 partijas numuram b5, sērijas numuram s5; 1 partijas numuram b6, sērijas numuram s6; 1 partijas numuram b7, sērijas numuram s7; 1 partijas numuram b8, sērijas numuram s8; 1 partijas numuram b9, sērijas numuram s9; un 1 partijas numuram b10, sērijas numuram s10</span><span class="sxs-lookup"><span data-stu-id="d8d7a-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="d8d7a-320">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="d8d7a-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="d8d7a-321">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d8d7a-321">Additional resources</span></span>

- [<span data-ttu-id="d8d7a-322">Kvalitātes pārvaldības procesi</span><span class="sxs-lookup"><span data-stu-id="d8d7a-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="d8d7a-323">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="d8d7a-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="d8d7a-324">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="d8d7a-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
