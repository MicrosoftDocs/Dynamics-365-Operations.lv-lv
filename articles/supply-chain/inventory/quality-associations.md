---
title: Kvalitātes piesaistes
description: Šajā tēmā aprakstīts, kā jūs varat izmantot kvalitātes saistības Microsoft Dynamics 365 Supply Chain Management, lai automātiski izveidotu kvalitātes pasūtījumus, kas ir saistīti ar jūsu pārdošanas, pirkšanas un ražošanas procesiem.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956741"
---
# <a name="quality-associations"></a><span data-ttu-id="9ebd9-103">Kvalitātes piesaistes</span><span class="sxs-lookup"><span data-stu-id="9ebd9-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ebd9-104">Šajā tēmā aprakstīts, kā jūs varat izmantot kvalitātes saistības Microsoft Dynamics 365 Supply Chain Management, lai automātiski izveidotu kvalitātes pasūtījumus, kas ir saistīti ar jūsu pārdošanas, pirkšanas un ražošanas procesiem.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="9ebd9-105">Kvalitātes saistība ģenerētajam kvalitātes pārbaudes pasūtījumam definē visu tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="9ebd9-106">Transakcijas notikums</span><span class="sxs-lookup"><span data-stu-id="9ebd9-106">The transaction event</span></span>
- <span data-ttu-id="9ebd9-107">Testu kopa, kas šiem krājumiem ir jāveic</span><span class="sxs-lookup"><span data-stu-id="9ebd9-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="9ebd9-108">Pieņemamais kvalitātes līmenis (acceptable quality level - AQL)</span><span class="sxs-lookup"><span data-stu-id="9ebd9-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="9ebd9-109">Iztveršanas plāns</span><span class="sxs-lookup"><span data-stu-id="9ebd9-109">The sampling plan</span></span>

<span data-ttu-id="9ebd9-110">Ir jādefinē kvalitātes piesaiste katrai biznesa procesā ietvertajai variācijai, kam ir automātiski jāveido kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="9ebd9-111">Piemēram, kvalitātes pārbaudes pasūtījumu var ģenerēt biznesa procesos, kas paredzēti pirkšanas pasūtījumiem, karantīnas pasūtījumiem, pārdošanas pasūtījumiem un ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="9ebd9-112">Darbs ar kvalitātes saistībām</span><span class="sxs-lookup"><span data-stu-id="9ebd9-112">Working with quality associations</span></span>

<span data-ttu-id="9ebd9-113">Biznesa process, kas izmanto kvalitātes saistību, var būt saistīts ar dažādiem avota dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem vai ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="9ebd9-114">Katrs kvalitātes saistības ieraksts nosaka testu kopu, pieņemamās kvalitātes līmeni (AQL) un iztveršanas plānu, kas tiek lietoti ģenerētajiem kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="9ebd9-115">Katrai biznesa procesa variācijai jums ir jādefinē kvalitātes saistības ieraksts.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="9ebd9-116">Piemēram, varat iestatīt kvalitātes saistību, kas ģenerē kvalitātes pārbaudes pasūtījumu, kad tiek atjaunināta pirkšanas pasūtījuma produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="9ebd9-117">Atkarībā no izpildes plāna iestatījumiem pats aktivizēšanas process var tikt bloķēts, kamēr ir atvērts kvalitātes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="9ebd9-118">Alternatīvi sekojošie procesi, piemēram, pirkšanas pasūtījuma rēķina izrakstīšana, var tikt bloķēti.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="9ebd9-119">Kamēr pastāv atvērti kvalitātes pārbaudes pasūtījumi, krājumu daudzumi tiek automātiski bloķēti no izsniegšanas.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="9ebd9-120">Atkarībā no lauka **Pilna bloķēšana** iestatījuma lapā **Krājumu iztveršana**, šis daudzums ir vai nu kvalitātes pasūtījumā norādītais daudzums, vai pirmdokumenta rindā norādītais daudzums.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="9ebd9-121">Papildinformāciju skatiet [Kvalitātes pārvaldības krājumu iztveršana](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="9ebd9-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="9ebd9-122">Noteiktam biznesa procesam kvalitātes saistības ieraksts identificē notikumu un nosacījumus, kādiem tiek ģenerēts kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="9ebd9-123">Nosacījumi var attiekties uz vietu vai juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="9ebd9-124">Kvalitātes pārbaudes pasūtījumu, kur ir iesaistīti destruktīvie testi, var ģenerēt tikai tad, ja attiecīgajam notikumam pastāv rīcībā esoši krājumi.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="9ebd9-125">Lai strādātu ar kvalitātes saistībām, dodieties uz **Krājumu pārvaldība \> Iestatījums \> Kvalitātes kontrole \> Kvalitātes saistības**.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="9ebd9-126">Nākamajos piemēros ir parādīts, kā kvalitātes saistības ieraksts tiek definēts katra darījumu procesa variācijām.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="9ebd9-127">Katram piemēram nākamajā tabulā ir sniegts kopsavilkums par kvalitātes saistības ieraksta definētajiem notikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9ebd9-128">Atsauces veids</span><span class="sxs-lookup"><span data-stu-id="9ebd9-128">Reference type</span></span></th>
<th><span data-ttu-id="9ebd9-129">Notikuma veids</span><span class="sxs-lookup"><span data-stu-id="9ebd9-129">Event type</span></span></th>
<th><span data-ttu-id="9ebd9-130">Izpilde</span><span class="sxs-lookup"><span data-stu-id="9ebd9-130">Execution</span></span></th>
<th><span data-ttu-id="9ebd9-131">Notikumu aizturēšana</span><span class="sxs-lookup"><span data-stu-id="9ebd9-131">Event blocking</span></span></th>
<th><span data-ttu-id="9ebd9-132">Dokumenta atsauce</span><span class="sxs-lookup"><span data-stu-id="9ebd9-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9ebd9-133">Krājumi</span><span class="sxs-lookup"><span data-stu-id="9ebd9-133">Inventory</span></span></td>
<td><span data-ttu-id="9ebd9-134">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-134">Not applicable</span></span></td>
<td><span data-ttu-id="9ebd9-135">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-135">Not applicable</span></span></td>
<td><span data-ttu-id="9ebd9-136">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-136">None</span></span></td>
<td><span data-ttu-id="9ebd9-137">Visi</span><span class="sxs-lookup"><span data-stu-id="9ebd9-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="9ebd9-138">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="9ebd9-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="9ebd9-139">Izdošanas process ir ieplānots</span><span class="sxs-lookup"><span data-stu-id="9ebd9-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="9ebd9-140">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-140">Before</span></span></td>
<td><span data-ttu-id="9ebd9-141">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="9ebd9-142">Konkrēts ID, Grupa vai tikai Visi</span><span class="sxs-lookup"><span data-stu-id="9ebd9-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-143">Izdošanas process</span><span class="sxs-lookup"><span data-stu-id="9ebd9-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-144">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="9ebd9-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-145">Rēķins</span><span class="sxs-lookup"><span data-stu-id="9ebd9-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9ebd9-146">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="9ebd9-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-147">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-147">Before</span></span></td>
<td><span data-ttu-id="9ebd9-148">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-149">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="9ebd9-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-150">Rēķins</span><span class="sxs-lookup"><span data-stu-id="9ebd9-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="9ebd9-151">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="9ebd9-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="9ebd9-152">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="9ebd9-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="9ebd9-153">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-153">Before</span></span></td>
<td><span data-ttu-id="9ebd9-154">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-155">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="9ebd9-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-156">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="9ebd9-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-157">Rēķins</span><span class="sxs-lookup"><span data-stu-id="9ebd9-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9ebd9-158">Pēc</span><span class="sxs-lookup"><span data-stu-id="9ebd9-158">After</span></span></td>
<td><span data-ttu-id="9ebd9-159">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-160">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="9ebd9-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-161">Rēķins</span><span class="sxs-lookup"><span data-stu-id="9ebd9-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9ebd9-162">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="9ebd9-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-163">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-163">Not applicable</span></span></td>
<td><span data-ttu-id="9ebd9-164">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-165">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="9ebd9-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-166">Rēķins</span><span class="sxs-lookup"><span data-stu-id="9ebd9-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9ebd9-167">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="9ebd9-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-168">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-168">Before</span></span></td>
<td><span data-ttu-id="9ebd9-169">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-170">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="9ebd9-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-171">Rēķins</span><span class="sxs-lookup"><span data-stu-id="9ebd9-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9ebd9-172">Pēc</span><span class="sxs-lookup"><span data-stu-id="9ebd9-172">After</span></span></td>
<td><span data-ttu-id="9ebd9-173">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-174">Rēķins</span><span class="sxs-lookup"><span data-stu-id="9ebd9-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="9ebd9-175">Ražošana</span><span class="sxs-lookup"><span data-stu-id="9ebd9-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-176">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="9ebd9-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-177">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-177">Not applicable</span></span></td>
<td><span data-ttu-id="9ebd9-178">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="9ebd9-179">Visi</span><span class="sxs-lookup"><span data-stu-id="9ebd9-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-180">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-181">Beigt</span><span class="sxs-lookup"><span data-stu-id="9ebd9-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9ebd9-182">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-183">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-183">Before</span></span></td>
<td><span data-ttu-id="9ebd9-184">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-185">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-186">Beigt</span><span class="sxs-lookup"><span data-stu-id="9ebd9-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9ebd9-187">Pēc</span><span class="sxs-lookup"><span data-stu-id="9ebd9-187">After</span></span></td>
<td><span data-ttu-id="9ebd9-188">Nav</span><span class="sxs-lookup"><span data-stu-id="9ebd9-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-189">Beigt</span><span class="sxs-lookup"><span data-stu-id="9ebd9-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="9ebd9-190">Karantīna</span><span class="sxs-lookup"><span data-stu-id="9ebd9-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-191">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="9ebd9-192">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-192">Before</span></span></td>
<td><span data-ttu-id="9ebd9-193">Reģistrēt pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-194">Beigt</span><span class="sxs-lookup"><span data-stu-id="9ebd9-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-195">Pēc</span><span class="sxs-lookup"><span data-stu-id="9ebd9-195">After</span></span></td>
<td><span data-ttu-id="9ebd9-196">Beigt</span><span class="sxs-lookup"><span data-stu-id="9ebd9-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-197">Beigt</span><span class="sxs-lookup"><span data-stu-id="9ebd9-197">End</span></span></td>
<td><span data-ttu-id="9ebd9-198">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-198">Before</span></span></td>
<td><span data-ttu-id="9ebd9-199">Beigt</span><span class="sxs-lookup"><span data-stu-id="9ebd9-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9ebd9-200">Maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="9ebd9-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-201">Ziņot kā pabeigtu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="9ebd9-202">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-202">Before</span></span></td>
<td><span data-ttu-id="9ebd9-203">Neviens</span><span class="sxs-lookup"><span data-stu-id="9ebd9-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-204">Noteikts ID, Grupa vai Visi, un raksturīgs Resurss, Grupa vai Visi</span><span class="sxs-lookup"><span data-stu-id="9ebd9-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-205">Ziņot kā pabeigtu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-206">Pēc</span><span class="sxs-lookup"><span data-stu-id="9ebd9-206">After</span></span></td>
<td><span data-ttu-id="9ebd9-207">Neviens</span><span class="sxs-lookup"><span data-stu-id="9ebd9-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9ebd9-208">Līdzprodukta ražošana</span><span class="sxs-lookup"><span data-stu-id="9ebd9-208">Co-product production</span></span></td>
<td><span data-ttu-id="9ebd9-209">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="9ebd9-209">Registration</span></span></td>
<td><span data-ttu-id="9ebd9-210">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-211">Neviens</span><span class="sxs-lookup"><span data-stu-id="9ebd9-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="9ebd9-212">Visu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9ebd9-213">Ziņot kā pabeigtu</span><span class="sxs-lookup"><span data-stu-id="9ebd9-213">Report as finished</span></span></td>
<td><span data-ttu-id="9ebd9-214">Pirms</span><span class="sxs-lookup"><span data-stu-id="9ebd9-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-215">Pēc</span><span class="sxs-lookup"><span data-stu-id="9ebd9-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9ebd9-216">Līdzeklis *Noliktavas procesu kvalitātes pārvaldība* pievieno iespējas kvalitātes pārbaudes pasūtījumu apstrādei ražošanai, kur lauks **Notikuma veids**, kas iestatīts uz *Ziņot, kad pabeigts* un lauks **Izpilde** iestatīts uz *Pēc*, un pirkšanai, kur lauks **Notikuma veids**, kas iestatīts uz *Reģistrāciju*.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="9ebd9-217">Papildinformāciju skatiet [Noliktavas procesu kvalitātes pārvaldība](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="9ebd9-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="9ebd9-218">Nākamajā tabulā ir plašāka informācija par to, kā kvalitātes pārbaudes pasūtījumus var ģenerēt specifiskiem procesu tipiem.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="9ebd9-219">Procesa tips</span><span class="sxs-lookup"><span data-stu-id="9ebd9-219">Type of process</span></span></th>
<th><span data-ttu-id="9ebd9-220">Kad kvalitātes pārbaudes pasūtījumus var ģenerēt automātiski</span><span class="sxs-lookup"><span data-stu-id="9ebd9-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="9ebd9-221">Kad kvalitātes pārbaudes pasūtījums var ģenerēt, ja ir nepieciešama destruktīvā testēšana</span><span class="sxs-lookup"><span data-stu-id="9ebd9-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="9ebd9-222">Nosacījuma informācija</span><span class="sxs-lookup"><span data-stu-id="9ebd9-222">Condition information</span></span></th>
<th><span data-ttu-id="9ebd9-223">Manuālas ģenerēšanas informācija</span><span class="sxs-lookup"><span data-stu-id="9ebd9-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9ebd9-224">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="9ebd9-224">Purchase order</span></span></td>
<td><span data-ttu-id="9ebd9-225">Pirms vai pēc tam, kad saņemtajam materiālam tiek grāmatots saņemšanas saraksts vai produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="9ebd9-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="9ebd9-226">Pēc tam, kad saņemtajam materiālam tiek grāmatota produktu ieejas plūsma, jo šim materiālam ir jābūt pieejamam destruktīvajai testēšanai</span><span class="sxs-lookup"><span data-stu-id="9ebd9-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="9ebd9-227">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9ebd9-228">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pirkšanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-229">Karantīnas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="9ebd9-229">Quarantine order</span></span></td>
<td><span data-ttu-id="9ebd9-230">Pirms vai pēc tam, kad karantīnas pasūtījums tiek ziņots kā pabeigts vai beidzies</span><span class="sxs-lookup"><span data-stu-id="9ebd9-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="9ebd9-231">Nevar ģenerēt kvalitātes pārbaudes pasūtījumus, kam ir nepieciešami destruktīvie testi.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="9ebd9-232">Tiek pieņemts, ka karantīnas pasūtījuma funkcionalitāte veic atbrīvošanos no iznīcinātā materiāla.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="9ebd9-233">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9ebd9-234">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst karantīnas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-235">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="9ebd9-235">Sales order</span></span></td>
<td><span data-ttu-id="9ebd9-236">Pirms plānotas izdošanas procesa vai pavadzīmes atjaunināšanas krājumiem, kas tiek sūti</span><span class="sxs-lookup"><span data-stu-id="9ebd9-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="9ebd9-237">Jebkurā posmā</span><span class="sxs-lookup"><span data-stu-id="9ebd9-237">At any step</span></span></td>
<td><span data-ttu-id="9ebd9-238">Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu, krājumu vai debitoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9ebd9-239">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pārdošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-240">Ražošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="9ebd9-240">Production order</span></span></td>
<td><span data-ttu-id="9ebd9-241">Pirms vai pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="9ebd9-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="9ebd9-242">Pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</span><span class="sxs-lookup"><span data-stu-id="9ebd9-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="9ebd9-243">Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu vai krājumu, vai kreditoru, vai šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9ebd9-244">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst ražošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-245">Ražošanas pasūtījums, kuram ir maršruta operācija</span><span class="sxs-lookup"><span data-stu-id="9ebd9-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="9ebd9-246">Pirms vai pēc tam, kad kādai operācijai ir pabeigta atskaite</span><span class="sxs-lookup"><span data-stu-id="9ebd9-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="9ebd9-247">Pēc tam, kad pēdējai operācijai ražošana ir ziņota kā pabeigta</span><span class="sxs-lookup"><span data-stu-id="9ebd9-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="9ebd9-248">Kvalitātes pārbaudes pasūtījuma pieprasījums ar norādīt noteiktu vietu, krājumu vai operācijas resursu, vai arī šo nosacījumu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9ebd9-249">Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst maršruta operācijai, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-250">Krājums</span><span class="sxs-lookup"><span data-stu-id="9ebd9-250">Inventory</span></span></td>
<td><span data-ttu-id="9ebd9-251">Kvalitātes pārbaudes pasūtījumu nevar automātiski ģenerēt transakcijai krājumu žurnālā vai arī pārsūtīšanas pasūtījuma transakcijām.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="9ebd9-252">Krājumadaudzumam noliktavā ir manuāli jāizveido kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="9ebd9-253">Fiziski rīcībā esošie krājumi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="9ebd9-254">Automātisku kvalitātes pasūtījumu izveidošanas piemēri</span><span class="sxs-lookup"><span data-stu-id="9ebd9-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="9ebd9-255">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="9ebd9-255">Purchasing</span></span>

<span data-ttu-id="9ebd9-256">Pirkšanā, ja iestatāt lauku **Notikuma veids** uz *Produktu ieejas plūsma* un lauku **Izpilde**, kas atrodas lapā *Kvalitātes piesaistes* uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="9ebd9-257">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Jā*, katrai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu un iestatījumiem krājumu iztveršanā.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="9ebd9-258">Katru reizi, kad tiek saņemts daudzums atbilstoši pirkšanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="9ebd9-259">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Nē*, pirmajai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="9ebd9-260">Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no izsekošanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="9ebd9-261">Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākām ieejas plūsmām atbilstoši pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="9ebd9-262">Ražošana</span><span class="sxs-lookup"><span data-stu-id="9ebd9-262">Production</span></span>

<span data-ttu-id="9ebd9-263">Ražošanā, ja iestatāt lauku **Notikuma veids** uz *Norādīts kā pabeigts* un lauku **Izpilde**, kas atrodas lapā *Kvalitātes piesaistes* uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="9ebd9-264">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Jā*, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz katru pabeigto daudzumu un iestatījumiem krājumu iztveršanā.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="9ebd9-265">Katru reizi, kad tiek daudzums tiek norādīts kā pabeigts atbilstoši ražošanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko pabeigto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="9ebd9-266">Šī ģenerēšanas loģika ir saskaņota ar pirkšanu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="9ebd9-267">Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Nē*, pirmajā reizē, kad daudzums tiek norādīts kā pabeigts, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz pabeigto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="9ebd9-268">Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no krājumu iztveršanas izsekošanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="9ebd9-269">Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākajiem pabeigtajiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9ebd9-270">Kvalitātes specifikācija</span><span class="sxs-lookup"><span data-stu-id="9ebd9-270">Quality specification</span></span></th>
<th><span data-ttu-id="9ebd9-271">Pēc atjauninātā daudzuma</span><span class="sxs-lookup"><span data-stu-id="9ebd9-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="9ebd9-272">Pēc izsekošanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="9ebd9-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="9ebd9-273">Rezultāts</span><span class="sxs-lookup"><span data-stu-id="9ebd9-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9ebd9-274">Procentuālā attiecība: 10 %</span><span class="sxs-lookup"><span data-stu-id="9ebd9-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="9ebd9-275">Jā</span><span class="sxs-lookup"><span data-stu-id="9ebd9-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="9ebd9-276">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-276">Batch number: No</span></span></p>
<p><span data-ttu-id="9ebd9-277">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="9ebd9-278">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="9ebd9-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="9ebd9-279">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="9ebd9-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="9ebd9-280">1. kvalitātes pārbaudes pasūtījums 3 vienumiem (10 % no 30)</span><span class="sxs-lookup"><span data-stu-id="9ebd9-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9ebd9-281">Pabeigto krājumu daudzums 70</span><span class="sxs-lookup"><span data-stu-id="9ebd9-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="9ebd9-282">2. kvalitātes pārbaudes pasūtījums 7 vienumiem (10 % no atlikušā pasūtījuma daudzuma, kas šajā gadījumā ir 70)</span><span class="sxs-lookup"><span data-stu-id="9ebd9-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-283">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="9ebd9-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="9ebd9-284">Nr.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-284">No</span></span></td>
<td>
<p><span data-ttu-id="9ebd9-285">Paketes numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-285">Batch number: No</span></span></p>
<p><span data-ttu-id="9ebd9-286">Sērijas numurs: Nr.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="9ebd9-287">Pasūtījuma daudzums: 100</span><span class="sxs-lookup"><span data-stu-id="9ebd9-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="9ebd9-288">Pabeigto krājumu daudzums 30</span><span class="sxs-lookup"><span data-stu-id="9ebd9-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="9ebd9-289">1. kvalitātes pārbaudes pasūtījums vienumam 1 (pirmajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība ir 1)</span><span class="sxs-lookup"><span data-stu-id="9ebd9-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="9ebd9-290">2. kvalitātes pārbaudes pasūtījums vienumam 1 (atlikušajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība joprojām ir 1)</span><span class="sxs-lookup"><span data-stu-id="9ebd9-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9ebd9-291">Pabeigto krājumu daudzums 10</span><span class="sxs-lookup"><span data-stu-id="9ebd9-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="9ebd9-292">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9ebd9-293">Pabeigto krājumu daudzums 60</span><span class="sxs-lookup"><span data-stu-id="9ebd9-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="9ebd9-294">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-295">Fiksēts daudzums: 1</span><span class="sxs-lookup"><span data-stu-id="9ebd9-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="9ebd9-296">Jā</span><span class="sxs-lookup"><span data-stu-id="9ebd9-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="9ebd9-297">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="9ebd9-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="9ebd9-298">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="9ebd9-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="9ebd9-299">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="9ebd9-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="9ebd9-300">Pabeigts 3: 1 partijas numuram b1, sērijas numuram s1; 1 partijas numuram b2, sērijas numuram s2 un 1 partijas numuram b3, sērijas numuram s3</span><span class="sxs-lookup"><span data-stu-id="9ebd9-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="9ebd9-301">1. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b1, sērijas numura s1</span><span class="sxs-lookup"><span data-stu-id="9ebd9-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="9ebd9-302">2. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b2, sērijas numura s2</span><span class="sxs-lookup"><span data-stu-id="9ebd9-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="9ebd9-303">3. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b3, sērijas numura s3</span><span class="sxs-lookup"><span data-stu-id="9ebd9-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9ebd9-304">Pabeigts 2: 1 partijas numuram b4, sērijas numuram s4 un 1 partijas numuram b5, sērijas numuram s5</span><span class="sxs-lookup"><span data-stu-id="9ebd9-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="9ebd9-305">4. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b4, sērijas numura s4</span><span class="sxs-lookup"><span data-stu-id="9ebd9-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="9ebd9-306">5. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b5, sērijas numura s5</span><span class="sxs-lookup"><span data-stu-id="9ebd9-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="9ebd9-307"><strong>Piezīme:</strong> partiju var izmantot atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9ebd9-308">Fiksēts daudzums: 2</span><span class="sxs-lookup"><span data-stu-id="9ebd9-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="9ebd9-309">Nr.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-309">No</span></span></td>
<td>
<p><span data-ttu-id="9ebd9-310">Partijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="9ebd9-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="9ebd9-311">Sērijas numurs: Jā</span><span class="sxs-lookup"><span data-stu-id="9ebd9-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="9ebd9-312">Pasūtījuma daudzums: 10</span><span class="sxs-lookup"><span data-stu-id="9ebd9-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="9ebd9-313">Pabeigts 4: 1 partijas numuram b1, sērijas numuram s1; 1 partijas numuram b2, sērijas numuram s2 un 1 partijas numuram b3, sērijas numuram s3; un 1 partijas numuram b4, sērijas numuram s4</span><span class="sxs-lookup"><span data-stu-id="9ebd9-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="9ebd9-314">1. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b1, sērijas numura s1</span><span class="sxs-lookup"><span data-stu-id="9ebd9-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="9ebd9-315">2. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b2, sērijas numura s2</span><span class="sxs-lookup"><span data-stu-id="9ebd9-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="9ebd9-316">3. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b3, sērijas numura s3</span><span class="sxs-lookup"><span data-stu-id="9ebd9-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="9ebd9-317">4. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b4, sērijas numura s4</span><span class="sxs-lookup"><span data-stu-id="9ebd9-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="9ebd9-318">Kvalitātes pārbaudes pasūtījums 5 vienumam 2 bez atsauces uz partijas numuru un sērijas numuru</span><span class="sxs-lookup"><span data-stu-id="9ebd9-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9ebd9-319">Pabeigts 6: 1 partijas numuram b5, sērijas numuram s5; 1 partijas numuram b6, sērijas numuram s6; 1 partijas numuram b7, sērijas numuram s7; 1 partijas numuram b8, sērijas numuram s8; 1 partijas numuram b9, sērijas numuram s9; un 1 partijas numuram b10, sērijas numuram s10</span><span class="sxs-lookup"><span data-stu-id="9ebd9-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="9ebd9-320">Nav izveidoti kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="9ebd9-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="9ebd9-321">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9ebd9-321">Additional resources</span></span>

- [<span data-ttu-id="9ebd9-322">Kvalitātes pārvaldības procesi</span><span class="sxs-lookup"><span data-stu-id="9ebd9-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="9ebd9-323">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="9ebd9-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="9ebd9-324">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="9ebd9-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
