---
title: Izveidot debitora rēķinu
description: '**Debitora rēķins par pārdošanas pasūtījumu** ir rēķins, kas ir saistīts ar pārdošanu un ko uzņēmums izsniedz debitoram.'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d7c9a61f935503b74ac27b354c875df095d84b4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573145"
---
# <a name="create-a-customer-invoice"></a><span data-ttu-id="e0351-103">Izveidot debitora rēķinu</span><span class="sxs-lookup"><span data-stu-id="e0351-103">Create a customer invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0351-104">**Debitora rēķins par pārdošanas pasūtījumu** ir rēķins, kas ir saistīts ar pārdošanu un ko uzņēmums izsniedz debitoram.</span><span class="sxs-lookup"><span data-stu-id="e0351-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="e0351-105">Šī tipa debitora rēķins tiek izveidots, pamatojoties uz pārdošanas pasūtījumu, kurā ir iekļautas pasūtījuma rindas un krājumu kodi.</span><span class="sxs-lookup"><span data-stu-id="e0351-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="e0351-106">Krājumu numuri tiek noteikti un grāmatoti Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="e0351-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="e0351-107">Debitora rēķinam par pārdošanas pasūtījumu nav pieejami apakšgrāmatas žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="e0351-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="e0351-108">Plašāku informāciju skatiet šeit: [Pārdošanas pasūtījumu rēķinu izveide](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="e0351-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="e0351-109">**Brīva teksta rēķins** nav saistīts ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e0351-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="e0351-110">Tajā ir pasūtījuma rindas, kurās ir iekļauti virsgrāmatas konti, brīva teksta apraksti un jūsu ievadītā pārdošanas summa.</span><span class="sxs-lookup"><span data-stu-id="e0351-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="e0351-111">Šāda veida rēķinā jūs nevarat ievadīt krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="e0351-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="e0351-112">Jums ir jāievada atbilstoša informācija par PVN.</span><span class="sxs-lookup"><span data-stu-id="e0351-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="e0351-113">Galvenais konts pārdošanai ir norādīts katrā rēķina rindā, kuru varat izplatīt vairākiem virsgrāmatas kontiem, lapā **Brīva teksta rēķins** noklikšķinot uz **Sadalīt summas**.</span><span class="sxs-lookup"><span data-stu-id="e0351-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="e0351-114">Turklāt debitora bilance tiek grāmatota kopsavilkuma kontā no grāmatošanas metodes, kas tiek izmantota brīva teksta rēķinam.</span><span class="sxs-lookup"><span data-stu-id="e0351-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="e0351-115">Papildinformāciju skatiet šeit: </span><span class="sxs-lookup"><span data-stu-id="e0351-115">For more information see:</span></span>

[<span data-ttu-id="e0351-116">Brīva teksta rēķina izveide</span><span class="sxs-lookup"><span data-stu-id="e0351-116">Create a free text invoice</span></span>](../accounts-receivable/create-free-text-invoice-new.md)

[<span data-ttu-id="e0351-117">Izveidot brīva teksta rēķina veidni</span><span class="sxs-lookup"><span data-stu-id="e0351-117">Create a free text template</span></span>](../accounts-receivable/create-free-text-invoice-template-new.md)

[<span data-ttu-id="e0351-118">Brīva teksta rēķina veidnes piešķiršana klientam</span><span class="sxs-lookup"><span data-stu-id="e0351-118">Assign a free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="e0351-119">Periodisku brīva teksta rēķinu ģenerēšana un grāmatošana</span><span class="sxs-lookup"><span data-stu-id="e0351-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="e0351-120">**Pro forma rēķins** ir rēķins, kas tiek sagatavots kā faktisko rēķina summu novērtējums pirms rēķina grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="e0351-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="e0351-121">Pro forma rēķinu varat drukāt debitora rēķinam par pārdošanas pasūtījumu vai brīva teksta rēķinam.</span><span class="sxs-lookup"><span data-stu-id="e0351-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="e0351-122">Atsevišķu, uz pārdošanas pasūtījumiem balstītu debitoru rēķinu grāmatošana un drukāšana</span><span class="sxs-lookup"><span data-stu-id="e0351-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="e0351-123">Izmantojiet šo procesu, lai izveidotu rēķinu, kas ir balstīts uz pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e0351-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="e0351-124">To varat darīt, ja izlemjat debitoram rēķinu izrakstīt pirms preču vai pakalpojumu piegādes.</span><span class="sxs-lookup"><span data-stu-id="e0351-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="e0351-125">Kad grāmatojat kādu rēķinu, katra krājuma daudzums **Rēķina atlikums** tiek atjaunināts ar kopējiem rēķinā iekļautajiem daudzumiem no atlasītā pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e0351-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="e0351-126">Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pārdošanas pasūtījumā ir 0 (nulle), pārdošanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**.</span><span class="sxs-lookup"><span data-stu-id="e0351-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="e0351-127">Ja daudzums **Rēķina atlikums** nav 0 (nulle), pārdošanas pasūtījuma statuss paliek nemainīgs, un tam var ievadīt papildu rēķinus.</span><span class="sxs-lookup"><span data-stu-id="e0351-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="e0351-128">Pārdošanas pasūtījumu statusu varat skatīt saraksta lapā **Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e0351-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="e0351-129">Lai skatītu rēķinus, kurus grāmatojāt, izmantojiet saraksta lapu **Atvērtie debitoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="e0351-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="e0351-130">Atsevišķu, uz pavadzīmēm un datumu balstītu debitoru rēķinu grāmatošana un drukāšana</span><span class="sxs-lookup"><span data-stu-id="e0351-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="e0351-131">Izmantojiet šo procesu, ja pārdošanas pasūtījumam ir grāmatota viena vai vairākas pavadzīmes.</span><span class="sxs-lookup"><span data-stu-id="e0351-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="e0351-132">Debitora rēķins tiek pamatots ar šīm pavadzīmēm un atspoguļo tajās norādītos daudzumus.</span><span class="sxs-lookup"><span data-stu-id="e0351-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="e0351-133">Rēķina finanšu informācija ir balstīta uz informāciju, kas tiek ievadīta, kad grāmatojat rēķinu.</span><span class="sxs-lookup"><span data-stu-id="e0351-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="e0351-134">Varat izveidot debitora rēķinu, kas ir balstīts uz pavadzīme rindas krājumiem, kuri ir piegādāti līdz šim datumam — arī tad, ja krājumi konkrētam pārdošanas pasūtījumam vēl nav nosūtīti.</span><span class="sxs-lookup"><span data-stu-id="e0351-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="e0351-135">To varat izdarīt, piemēram, ja jūsu juridiskā persona izsniedz vienu rēķinu katram debitoram mēnesī, kas sedz visas piegādes, kuras attiecīgā mēneša laikā piegādājat.</span><span class="sxs-lookup"><span data-stu-id="e0351-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="e0351-136">Katra pavadzīme ataino daļēju vai pilnīgu krājumu piegādi pēc pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e0351-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="e0351-137">Kad grāmatojat rēķinu, daudzums **Rēķina atlikums** katram krājumam tiek atjaunināts ar kopīgo piegādāto daudzumu no atlasītajām pavadzīmēm.</span><span class="sxs-lookup"><span data-stu-id="e0351-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="e0351-138">Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pārdošanas pasūtījumā ir 0 (nulle), tad pārdošanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**.</span><span class="sxs-lookup"><span data-stu-id="e0351-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="e0351-139">Ja daudzums **Rēķina atlikums** nav 0 (nulle), pārdošanas pasūtījuma statuss paliek nemainīgs, un tam var ievadīt papildu rēķinus.</span><span class="sxs-lookup"><span data-stu-id="e0351-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="e0351-140">Inventāra transakcijas tiek atjauninātas ar rēķina numuru, un statuss pārdošanas pasūtījuma laukā **Rindas statuss** mainās uz **Iekļauts rēķinā**.</span><span class="sxs-lookup"><span data-stu-id="e0351-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="e0351-141">Pārdošanas pasūtījumu statusu skatiet saraksta lapā **Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e0351-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="e0351-142">Pārdošanas pasūtījumu vai pavadzīmju konsolidēšana grāmatošanai</span><span class="sxs-lookup"><span data-stu-id="e0351-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="e0351-143">Izmantojiet šo procesu, kad viens vai vairāki pārdošanas pasūtījumi ir gatavi rēķina izrakstīšanai un vēlaties tos konsolidēt vienā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="e0351-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="e0351-144">Saraksta lapā **Pārdošanas pasūtījums** varat atlasīt vairākus rēķinus un pēc tam izmantot vienumu **Ģenerēt rēķinus**, lai tos konsolidētu.</span><span class="sxs-lookup"><span data-stu-id="e0351-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="e0351-145">Lapā **Rēķina grāmatošana** varat mainīt iestatījumu **Koppasūtījums**, lai apkopotu pēc pasūtījuma numura (ja vienam pārdošanas pasūtījumam ir vairākas pavadzīmes) vai pēc rēķina konta (ja vienam rēķina kontam ir vairāki pārdošanas pasūtījumi).</span><span class="sxs-lookup"><span data-stu-id="e0351-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="e0351-146">Izmantojiet pogu **Sakārtot**, lai pārdošanas pasūtījumus sakārtotu vienā rēķinā, pamatojoties uz iestatījumiem **Koppasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="e0351-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="e0351-147">Papildu iestatījumi, kas maina grāmatošanas darbību</span><span class="sxs-lookup"><span data-stu-id="e0351-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="e0351-148">Grāmatošanas procesa darbību maina tālāk uzskaitītie lauki.</span><span class="sxs-lookup"><span data-stu-id="e0351-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0351-149">Lauks</span><span class="sxs-lookup"><span data-stu-id="e0351-149">Field</span></span></th>
<th><span data-ttu-id="e0351-150">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e0351-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0351-151">Daudzums</span><span class="sxs-lookup"><span data-stu-id="e0351-151">Quantity</span></span></td>
<td><span data-ttu-id="e0351-152">Atlasiet daudzumus, uz ko balstīt dokumentu grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="e0351-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="e0351-153">Pieejamās opcijas ir atkarīgas no grāmatojamā dokumenta tipa, piemēram, vai dokuments ir pavadzīme vai rēķins.</span><span class="sxs-lookup"><span data-stu-id="e0351-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="e0351-154"><strong>Piegādāt tūlīt</strong> — atlasiet visus daudzumus, kas ir ievadīti laukā <strong>Piegādāt tūlīt</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0351-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="e0351-155">Izmantojiet šo opciju, lai apstiprinātu vai piegādātu daļēju pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e0351-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="e0351-156"><strong>Izdots</strong> — atlasiet visus daudzumus, kas ir izdoti.</span><span class="sxs-lookup"><span data-stu-id="e0351-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="e0351-157"><strong>Visi</strong> — atlasiet visus pārdošanas pasūtījumā ietvertos daudzumus, kas vēl nav atjaunināti, izmantojot pašreizējo dokumenta tipu.</span><span class="sxs-lookup"><span data-stu-id="e0351-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="e0351-158"><strong>Pavadzīme</strong> — atlasiet visus daudzumus, kas ir atjaunināti ar pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="e0351-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="e0351-159"><strong>Izdotais daudzums un neuzkrātās preces</strong> — atlasiet visus daudzumus, kas ir izdoti, un visus preču daudzumus, kas nav uzkrāti.</span><span class="sxs-lookup"><span data-stu-id="e0351-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0351-160">Grāmatošana</span><span class="sxs-lookup"><span data-stu-id="e0351-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="e0351-161">Atlasiet šo opciju, lai reģistrētu žurnālā pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e0351-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="e0351-162">Notīriet šo opciju, lai drukātu pro forma pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e0351-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="e0351-163"><strong>Piezīme.</strong> Ja esat izveidojis maksājumu grafika līgumu, pro forma pārdošanas pasūtījumā netiek rādīts maksājumu grafiks.</span><span class="sxs-lookup"><span data-stu-id="e0351-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="e0351-164">Maksājumu grafiki tiek rādīti tikai faktiskos pārdošanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="e0351-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0351-165">Vēlā atlase</span><span class="sxs-lookup"><span data-stu-id="e0351-165">Late selection</span></span></td>
<td><span data-ttu-id="e0351-166">Atlasiet šo opciju, lai lietotu atlasīto vaicājumu vēlāk.</span><span class="sxs-lookup"><span data-stu-id="e0351-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="e0351-167">Šī opcija tiek izmantota pakešuzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="e0351-167">This option is used for batch jobs.</span></span> <span data-ttu-id="e0351-168">Vaicājums tiek izpildīts, kad tiek veikts pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="e0351-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0351-169">Samazināt daudzumu</span><span class="sxs-lookup"><span data-stu-id="e0351-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="e0351-170">Atlasiet šo opciju, lai automātiski samazinātu piegādāto daudzumu, kad dokuments ir grāmatots, tādējādi piegādātais daudzums ir vienāds ar pieejamiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="e0351-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0351-171">Drukāt</span><span class="sxs-lookup"><span data-stu-id="e0351-171">Print</span></span></td>
<td><span data-ttu-id="e0351-172">Atlasiet, kad drukāt dokumentus:</span><span class="sxs-lookup"><span data-stu-id="e0351-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="e0351-173"><strong>Pašreizējais</strong> — drukāt dokumentus pēc katra rēķina atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="e0351-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="e0351-174"><strong>Pēc</strong> — drukāt dokumentus pēc visu rēķinu atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="e0351-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="e0351-175">
<strong>Piezīme.</strong> Lauks <strong>Drukāt</strong> ir pieejams tikai tad, ja atlasāt opciju <strong>Drukāt rēķinu</strong>, <strong>Drukāt apstiprinājumu</strong>, <strong>Drukāt izdošanas sarakstu</strong> vai <strong>Drukāt pavadzīmi</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0351-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="e0351-176">Piemēram, lapā <strong>Formu kārtošana</strong> esat iestatījis sistēmu, lai informāciju kārtotu pēc rēķina konta.</span><span class="sxs-lookup"><span data-stu-id="e0351-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="e0351-177">Pēc tam varat atlasīt <strong>Pēc</strong>, lai drukātu dokumentus partijā, kas tiek kārtota pēc rēķina konta.</span><span class="sxs-lookup"><span data-stu-id="e0351-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="e0351-178">Pretējā gadījumā dokumenti tiek drukāti pirms apstrādes pabeigšanas un dokumenti netiek kārtoti secībā, kas ir norādīta lapā <strong>Formu kārtošana</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0351-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0351-179">Drukāt rēķinu</span><span class="sxs-lookup"><span data-stu-id="e0351-179">Print invoice</span></span></td>
<td><span data-ttu-id="e0351-180">Atzīmējiet šo opciju, lai izdrukātu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="e0351-180">Select this option to print the invoice.</span></span> <span data-ttu-id="e0351-181">Ja šī opcija ir izslēgta, rēķinu varat grāmatot, to nedrukājot.</span><span class="sxs-lookup"><span data-stu-id="e0351-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0351-182">Nosūtīt e-pastu</span><span class="sxs-lookup"><span data-stu-id="e0351-182">Send e-mail</span></span></td>
<td><span data-ttu-id="e0351-183">Atlasiet šo opciju, lai pēc rēķina grāmatošanas šo rēķinu par pārdošanas pasūtījumu sūtītu debitoram kā e-pasta pielikumu.</span><span class="sxs-lookup"><span data-stu-id="e0351-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="e0351-184">Pielikumi tiek sūtīti kā PDF un XML faili.</span><span class="sxs-lookup"><span data-stu-id="e0351-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="e0351-185">Šī opcija ir pieejama tikai tad, ja lapā <strong>Elektroniskā rēķina parametri</strong> atlasāt opciju <strong>Iespējot CFD (elektroniskie rēķini)</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0351-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="e0351-186"><strong>Piezīme.</strong> (MEX) Šī vadīkla ir pieejama tikai juridiskām personām, kuru primārā adrese ir Meksikā.</span><span class="sxs-lookup"><span data-stu-id="e0351-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0351-187">Lietot drukas pārvaldības adresātu</span><span class="sxs-lookup"><span data-stu-id="e0351-187">Use print management destination</span></span></td>
<td><span data-ttu-id="e0351-188">Atlasiet šo opciju, lai lietotu drukas iestatījumus, kas transakcijai, dokumentam vai modulim ir norādīti lapā <strong>Drukāšanas parametru iestatīšana</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0351-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0351-189">Kredīta limita pārbaude</span><span class="sxs-lookup"><span data-stu-id="e0351-189">Check credit limit</span></span></td>
<td><span data-ttu-id="e0351-190">Atlasiet informāciju, kas ir jāanalizē, veicot kredīta limita pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="e0351-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="e0351-191"><strong>Nav</strong> — nav vajadzības pēc kredīta limita pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="e0351-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="e0351-192"><strong>Bilance</strong> — kredīta limits tiek pārbaudīts pret debitora bilanci.</span><span class="sxs-lookup"><span data-stu-id="e0351-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="e0351-193"><strong>Bilance + pavadzīme vai produktu ieejas plūsma</strong> — kredīta limits tiek pārbaudīts pret debitora bilanci un piegādēm.</span><span class="sxs-lookup"><span data-stu-id="e0351-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="e0351-194"><strong>Bilance+viss</strong> — kredīta limits tiek pārbaudīts pret debitora bilanci, piegādēm un atvērtajiem pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="e0351-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0351-195">Kredīta korekcija</span><span class="sxs-lookup"><span data-stu-id="e0351-195">Credit correction</span></span></td>
<td><span data-ttu-id="e0351-196">Atzīmējiet šo opciju, lai dokumentu transakcijās kredīta notu rādītu kā debetu.</span><span class="sxs-lookup"><span data-stu-id="e0351-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0351-197">Kreditēt atlikušo summu</span><span class="sxs-lookup"><span data-stu-id="e0351-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="e0351-198">Ja grāmatojat kredīta notu, atzīmējiet šo opciju, lai saglabātu atlikušo daudzumu pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="e0351-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="e0351-199">Ja šī opcija ir notīrīta, atlikušais daudzums ir iestatīts uz 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="e0351-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0351-200">Kopgrāmatojums, kas paredzēts:</span><span class="sxs-lookup"><span data-stu-id="e0351-200">Summary update for</span></span></td>
<td><span data-ttu-id="e0351-201">Atlasiet, kā jāveic vairāku pārdošanas pasūtījumu apkopošana:</span><span class="sxs-lookup"><span data-stu-id="e0351-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="e0351-202"><strong>Nav</strong> — neveikt pārdošanas pasūtījumu apkopošanu.</span><span class="sxs-lookup"><span data-stu-id="e0351-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="e0351-203">Piemēram, katram pārdošanas pasūtījumam tiks veidots atsevišķs rēķins.</span><span class="sxs-lookup"><span data-stu-id="e0351-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="e0351-204"><strong>Rēķina konts</strong> — apkopot visus atlasītos pasūtījumus, balstoties uz lapā <strong>Kopgrāmatošanas parametri</strong> iestatītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="e0351-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="e0351-205"><strong>Pasūtījums</strong> — atlasītu pasūtījumu diapazonu atkopot vienā, jūsu norādītā pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="e0351-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="e0351-206">Pasūtījumu apkopošana ir atkarīga no kritērijiem, ko iestatāt lapā<strong>Kopgrāmatošanas parametri</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0351-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="e0351-207">Ja atlasāt šo opciju, ir jāatlasa kāda vērtība laukā <strong>Pārdošanas pasūtījums</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0351-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="e0351-208"><strong>Automātisks kopsavilkums</strong> — ja lapā <strong>Kopgrāmatošana</strong> ir norādīti kopgrāmatojumi, apkopojiet visus atlasītos pasūtījumus, pamatojoties uz lapā <strong>Kopgrāmatošanas parametri</strong> iestatītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="e0351-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="e0351-209">Ja nav norādīti kopgrāmatojumi, pasūtījums tiek grāmatots atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="e0351-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="e0351-210"><strong>Pavadzīme</strong> — atlasīto pasūtījumu diapazonu apkopo vienā rēķinā par katru pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="e0351-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="e0351-211">Šī opcija ir pieejama tikai tad, ja laukā <strong>Daudzums</strong> ir atlasīta vērtība <strong>Pavadzīme</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0351-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





