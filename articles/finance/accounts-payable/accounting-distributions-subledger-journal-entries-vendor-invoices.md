---
title: Uzskaites sadales un žurnālu ieraksti kreditoru rēķiniem
description: Uzskaites sadales tiek izmantotas, lai definētu veidu, kā summa tiek uzskaitīta, piemēram, kā izdevumi, nodokļi vai izmaksas tiek uzskaitīti kreditora rēķinā. Katrai summai, kas ir jānorāda kreditora rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales.
author: abruer
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 513066a597620450f0b482e98e36d31c6f2c980a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189097"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a><span data-ttu-id="36359-104">Uzskaites sadales un žurnālu ieraksti kreditoru rēķiniem</span><span class="sxs-lookup"><span data-stu-id="36359-104">Accounting distributions and journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36359-105">Uzskaites sadales tiek izmantotas, lai definētu veidu, kā summa tiek uzskaitīta, piemēram, kā izdevumi, nodokļi vai izmaksas tiek uzskaitīti kreditora rēķinā.</span><span class="sxs-lookup"><span data-stu-id="36359-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="36359-106">Katrai summai, kas ir jānorāda kreditora rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="36359-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

## <a name="accounting-distributions"></a><span data-ttu-id="36359-107">Uzskaites sadales</span><span class="sxs-lookup"><span data-stu-id="36359-107">Accounting distributions</span></span> 

<span data-ttu-id="36359-108">Lapā Kreditora rēķins varat izmantot tālāk norādītās pogas, lai skatītu un, iespējams, modificētu katras kreditora rēķinā ietvertās summas uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="36359-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="36359-109">**Sadales summas** — skatiet un mainiet uzskaites sadales atsevišķai rindai un jebkurai apakšrindai, piemēram, nodokļiem un izmaksām.</span><span class="sxs-lookup"><span data-stu-id="36359-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="36359-110">Apakšrindas uzskaites sadales varat arī skatīt un modificēt tieši lapā PVN darbības vai Maksu darbības.</span><span class="sxs-lookup"><span data-stu-id="36359-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="36359-111">Mainiet kreditora rēķina galvenes summas, piemēram, izmaksas vai valūtas noapaļošanas summas.</span><span class="sxs-lookup"><span data-stu-id="36359-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="36359-112">Modificējiet kreditora rēķina rindu summas.</span><span class="sxs-lookup"><span data-stu-id="36359-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="36359-113">**Skatīt sadales** — skatiet visu dokumenta rindu uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="36359-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="36359-114">No šī skata uzskaites sadales nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="36359-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="36359-115">Skatiet galveni un rindu summas.</span><span class="sxs-lookup"><span data-stu-id="36359-115">View header and line amounts.</span></span>

<span data-ttu-id="36359-116">Ja kreditora rēķinā ir atsauces uz pirkšanas pasūtījumu, uzskaites sadales varat sadalīt un modificēt tām rindām, kas ietver uzkrāto krājumu.</span><span class="sxs-lookup"><span data-stu-id="36359-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="36359-117">Ja kreditora rēķina rindā nav atsauces uz pirkšanas pasūtījuma rindu, uzskaites sadali varat arī dzēst.</span><span class="sxs-lookup"><span data-stu-id="36359-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="36359-118">Nevar sadalīt vai dzēst maksu, nodokļu un rindas atlaižu rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="36359-119">Jūs varat modificēt virsgrāmatas kontu, bet nav iespējams mainīt summas vai procentus.</span><span class="sxs-lookup"><span data-stu-id="36359-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="36359-120">Ja pamatrinda satur krājumu, kas netiek uzkrāts, un uzskaites sadales ir sadalītas, apakšrinda tiek sadalīta automātiski, lai atbilstu pamatrindas finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="36359-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="36359-121">Apakšrindas uzskaites sadales nevar papildus sadalīt vai dzēst, bet atkarībā no apakšrindas iestatījumiem, iespējams, varat mainīt virsgrāmatas kontu apakšrindas uzskaites sadalē.</span><span class="sxs-lookup"><span data-stu-id="36359-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="36359-122">Summu sadalīšana</span><span class="sxs-lookup"><span data-stu-id="36359-122">Distributing amounts</span></span>
<span data-ttu-id="36359-123">Ievadot kreditora rēķinu, katra summa tiek sadalīta tālāk aprakstītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="36359-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36359-124">Kreditora rēķina rindas tips</span><span class="sxs-lookup"><span data-stu-id="36359-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="36359-125">Prioritāšu secība, kas nosaka, no kāda avota tiek parādīts galvenais konts</span><span class="sxs-lookup"><span data-stu-id="36359-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="36359-126">Prioritāšu secība, kas nosaka, kuras noklusējuma finanšu dimensijas tiek parādītas</span><span class="sxs-lookup"><span data-stu-id="36359-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36359-127">Uzkrātā prece</span><span class="sxs-lookup"><span data-stu-id="36359-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-128">Uzskaites sadale pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-129">Lauks Galvenais konts, kad lapā Grāmatošana ir atlasīta opcija Produkta pirkšanas izdevumi.</span><span class="sxs-lookup"><span data-stu-id="36359-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-130">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-131">Kreditora rēķinā izmantot noklusējuma finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="36359-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36359-132">Sagādes kategorija vai prece, kas netiek uzkrāta</span><span class="sxs-lookup"><span data-stu-id="36359-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-133">Uzskaites sadale pirkšanas pasūtījuma rindai, ja kreditora rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="36359-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="36359-134">Lauks Galvenais konts, kad lapā Grāmatošana ir atlasīta opcija Pirkšanas tēriņi izdevumu sadaļai.</span><span class="sxs-lookup"><span data-stu-id="36359-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-135">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-136">Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</span><span class="sxs-lookup"><span data-stu-id="36359-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="36359-137">Kreditora rēķinā izmantot noklusējuma finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="36359-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="36359-138">Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-139">Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="36359-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36359-140">Pamatlīdzeklis</span><span class="sxs-lookup"><span data-stu-id="36359-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-141">Uzskaites sadale pirkšanas pasūtījuma rindai, ja kreditora rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="36359-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="36359-142">Ja veidlapā Kreditora rēķins ir atlasīta lauka Darījuma veids vērtība Iegāde, tad lauks Galvenais konts, kad lapā Pamatlīdzekļu grāmatošanas metodes ir atlasīta opcija Iegāde.</span><span class="sxs-lookup"><span data-stu-id="36359-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="36359-143">Ja veidlapā Kreditora rēķins ir atlasīta lauka Darījuma veids vērtība Kapitālās izmaksas, tad lauks Galvenais konts, kad lapā Pamatlīdzekļu grāmatošanas metodes ir atlasīta opcija Kapitālās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="36359-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-144">Izmantot konta sadali pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="36359-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="36359-145">Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-146">Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="36359-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36359-147">Kreditora rēķina rindā noteikts projekts</span><span class="sxs-lookup"><span data-stu-id="36359-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-148">Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="36359-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="36359-149">Ja lapā Projektu grupas ir atlasīta lauka Izmaksu grāmatošana — krājumi vērtība Bilance, tad lauks Galvenais konts, kad lapā Grāmatošanas iestatījumi virsgrāmatā ir atlasīta opcija Izmaksas.</span><span class="sxs-lookup"><span data-stu-id="36359-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="36359-150">Ja lapā Projektu grupas ir atlasīta lauka Izmaksu grāmatošana — krājumi vērtība Peļņa un zaudējumi, tad lauks Galvenais konts, kad lapā Grāmatošanas iestatījumi virsgrāmatā ir atlasīta opcija Izmaksas — krājumi.</span><span class="sxs-lookup"><span data-stu-id="36359-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-151">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36359-152">Rindas atlaide</span><span class="sxs-lookup"><span data-stu-id="36359-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-153">Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="36359-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="36359-154">Lauks Galvenais konts, kad lapā Grāmatošana ir atlasīta opcija Atlaide.</span><span class="sxs-lookup"><span data-stu-id="36359-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="36359-155">Ja grāmatošanas metodē nav definēts atlaides galvenais konts, tad pilnās cenas uzskaites sadale pirkšanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="36359-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-156">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot uzskaites sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-157">Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="36359-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-158">Izmantot finanšu dimensiju vērtības kreditora rēķina rindām.</span><span class="sxs-lookup"><span data-stu-id="36359-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-159">Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="36359-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36359-160">Pirkšanas izmaksas, kas ir ievadītas pirkšanas pasūtījuma rindas cilnē Cena un atlaide.</span><span class="sxs-lookup"><span data-stu-id="36359-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-161">Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="36359-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="36359-162">Uzskaites sadale pilnai cenai pirkšanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="36359-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-163">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-164">Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="36359-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36359-165">Rindu maksas</span><span class="sxs-lookup"><span data-stu-id="36359-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-166">Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="36359-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="36359-167">Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Virsgrāmatas konts, tad lauks Debeta konts lapā Maksas kods.</span><span class="sxs-lookup"><span data-stu-id="36359-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="36359-168">Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Krājums, tad pirkšanas pasūtījuma rindā norādītās pilnās cenas uzskaites sadale.</span><span class="sxs-lookup"><span data-stu-id="36359-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-169">Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Debitors/kreditors, tad lauks Kredīta konts lapā Maksas kods.</span><span class="sxs-lookup"><span data-stu-id="36359-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-170">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-171">Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="36359-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-172">Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-173">Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="36359-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36359-174">Nodokļi ar šādu nosacījumu:</span><span class="sxs-lookup"><span data-stu-id="36359-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="36359-175">Lapā Virsgrāmatas parametri ir atlasīta opcija Lietot ASV nodokļu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="36359-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="36359-176">Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="36359-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="36359-177">Pilnās cenas vai maksas uzskaites sadale.</span><span class="sxs-lookup"><span data-stu-id="36359-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-178">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-179">Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="36359-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-180">Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36359-181">Nodokļi ar šādiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="36359-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="36359-182">Lapā Virsgrāmatas parametri ir noņemta atzīme no opcijas Lietot ASV nodokļu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="36359-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="36359-183">PVN grupai lapā PVN grupas ir noņemta atzīme no opcijas Importa nodoklis.</span><span class="sxs-lookup"><span data-stu-id="36359-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="36359-184">Ja nodokļu summa ir atgūstama, tad lauks Saņemtais PVN lapā Virsgrāmatas grāmatošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="36359-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="36359-185">Ja nodokļu summa nav atgūstama, tad pilna cena vai maksas uzskaites sadale.</span><span class="sxs-lookup"><span data-stu-id="36359-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-186">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-187">Izmantot finanšu dimensijas no pilnās cenas vai uzskaites sadales kreditora rēķina rindā norādītajai maksai.</span><span class="sxs-lookup"><span data-stu-id="36359-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-188">Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-189">Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="36359-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36359-190">Nodokļi ar šādiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="36359-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="36359-191">Lapā Virsgrāmatas parametri ir noņemta atzīme no opcijas Lietot ASV nodokļu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="36359-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="36359-192">PVN grupai lapā PVN grupas ir atlasīta opcija Importa nodoklis.</span><span class="sxs-lookup"><span data-stu-id="36359-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="36359-193">Ja nodokļu summa ir atgūstama, tad lauks Saņemtais PVN lapā Virsgrāmatas grāmatošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="36359-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="36359-194">Ja nodokļu summa nav atgūstama, tad lauks Importa nodokļa izdevumi lapā Virsgrāmatas grāmatošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="36359-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-195">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-196">Izmantot finanšu dimensijas no pilnās cenas vai uzskaites sadales kreditora rēķina rindā norādītajai maksai.</span><span class="sxs-lookup"><span data-stu-id="36359-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-197">Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-198">Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="36359-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36359-199">Galvenā maksa</span><span class="sxs-lookup"><span data-stu-id="36359-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-200">Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Virsgrāmatas konts, tad lauks Debeta konts lapā Maksas kods.</span><span class="sxs-lookup"><span data-stu-id="36359-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="36359-201">Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Debitors/kreditors, tad lauks Kredīta konts lapā Maksas kods.</span><span class="sxs-lookup"><span data-stu-id="36359-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-202">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-203">Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</span><span class="sxs-lookup"><span data-stu-id="36359-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="36359-204">Izmantot finanšu dimensiju noklusēto veidņu vērtības no kreditora rēķina galvenes.</span><span class="sxs-lookup"><span data-stu-id="36359-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="36359-205">Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-206">Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="36359-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36359-207">Virsraksta atlaide</span><span class="sxs-lookup"><span data-stu-id="36359-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="36359-208">Kreditora rēķina atlaides grāmatošanas veida lauks Galvenais konts lapā Automātisko darījumu konti.</span><span class="sxs-lookup"><span data-stu-id="36359-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="36359-209">Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="36359-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="36359-210">Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="36359-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-211">Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="36359-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="36359-212">Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="36359-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a><span data-ttu-id="36359-213">Nodokļu sadalīšana</span><span class="sxs-lookup"><span data-stu-id="36359-213">Distributing taxes</span></span>

<span data-ttu-id="36359-214">Nodokļu uzskaites sadales var izveidot tikai pēc nodokļu aprēķināšanas.</span><span class="sxs-lookup"><span data-stu-id="36359-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="36359-215">Lai aprēķinātu PVN, lapā Kreditora rēķins ir jāizpilda viens no tālāk aprakstītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="36359-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="36359-216">Apskatiet rēķina kopsummu.</span><span class="sxs-lookup"><span data-stu-id="36359-216">View the invoice total.</span></span>
-   <span data-ttu-id="36359-217">Apskatiet PVN.</span><span class="sxs-lookup"><span data-stu-id="36359-217">View the sales tax.</span></span>
-   <span data-ttu-id="36359-218">Apskatiet apakšgrāmatas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="36359-218">View the subledger journal.</span></span>
-   <span data-ttu-id="36359-219">Apskatiet uzskaites sadales visam kreditora rēķinam.</span><span class="sxs-lookup"><span data-stu-id="36359-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="36359-220">Aizturiet kreditora rēķinu.</span><span class="sxs-lookup"><span data-stu-id="36359-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="36359-221">Grāmatojiet kreditora rēķinu.</span><span class="sxs-lookup"><span data-stu-id="36359-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="36359-222">Apakšgrāmatas žurnāli kreditoru rēķiniem</span><span class="sxs-lookup"><span data-stu-id="36359-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="36359-223">Pirms grāmatojat kreditora rēķinu, varat apskatīt pilnu uzskaites ierakstu šim rēķinam, kas ietver debetu un kredītu, lai pārliecinātos, ka rēķins tiek grāmatots pareizajos kontos.</span><span class="sxs-lookup"><span data-stu-id="36359-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="36359-224">Šis pilnās uzskaites ieraksta skats tiek saukts par apakšgrāmatas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="36359-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="36359-225">Ja pirms kreditora rēķina reģistrēšanas žurnālā priekšskatāt apakšgrāmatas žurnāla ierakstu un tas ir nepareizs, šo apakšgrāmatas žurnāla ierakstu nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="36359-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="36359-226">Tā vietā ir jāmodificē uzskaites sadales vai grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="36359-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="36359-227">Uzskaites sadales tiek izmantotas, lai noteiktu uzskaites ieraksta vienu pusi, debetu vai kredītu.</span><span class="sxs-lookup"><span data-stu-id="36359-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="36359-228">Korespondējošais apakšgrāmatas žurnāla konta ieraksts tiek izveidots, izmantojot grāmatošanas metodes, piemēram, no kreditora konta vai nodokļiem.</span><span class="sxs-lookup"><span data-stu-id="36359-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]