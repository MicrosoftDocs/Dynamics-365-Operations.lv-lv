---
title: Uzskaites sadales un žurnālu ieraksti brīva teksta rēķiniem
description: Uzskaites sadales tiek izmantotas, lai definētu, kā summa tiek uzskaitīta, piemēram, kā ieņēmumi, nodokļi vai izmaksas tiek uzskaitīti brīva teksta rēķinā. Katrai summai, kas ir jānorāda brīva teksta rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f3ee26825ec48a8e8e32401ceaa8c80ecd679d2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993203"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a><span data-ttu-id="19da0-104">Uzskaites sadales un apakšgrāmatas ieraksti brīva teksta rēķiniem</span><span class="sxs-lookup"><span data-stu-id="19da0-104">Accounting distributions and subledger entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19da0-105">Uzskaites sadales tiek izmantotas, lai definētu, kā summa tiek uzskaitīta, piemēram, kā ieņēmumi, nodokļi vai izmaksas tiek uzskaitīti brīva teksta rēķinā.</span><span class="sxs-lookup"><span data-stu-id="19da0-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="19da0-106">Katrai summai, kas ir jānorāda brīva teksta rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="19da0-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="19da0-107">Uzskaites sadales</span><span class="sxs-lookup"><span data-stu-id="19da0-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="19da0-108">Brīva teksta rēķina lapā varat izmantot tālāk aprakstītās pogas, lai brīva teksta rēķinā skatītu un, iespējams, mainītu katras summas uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="19da0-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="19da0-109">**Sadalīt summas**— skatiet un mainiet uzskaites sadales atsevišķai rindai un jebkurai apakšrindai, piemēram, nodokļiem vai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="19da0-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="19da0-110">Apakšrindu uzskaites sadales varat arī skatīt un mainīt tieši no lapas Pārdošanas nodokļa transakcijas vai Maksu darbības.</span><span class="sxs-lookup"><span data-stu-id="19da0-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="19da0-111">Mainiet brīva teksta rēķina galvenes summas, piemēram, izmaksas vai valūtas noapaļošanas summas.</span><span class="sxs-lookup"><span data-stu-id="19da0-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="19da0-112">Mainiet brīva teksta rēķina rindas summas.</span><span class="sxs-lookup"><span data-stu-id="19da0-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="19da0-113">**Skatīt sadales**— skatiet visu dokumenta rindu uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="19da0-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="19da0-114">No šī skata uzskaites sadales nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="19da0-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="19da0-115">Skatiet galveni un rindu summas.</span><span class="sxs-lookup"><span data-stu-id="19da0-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="19da0-116">Summu sadalīšana</span><span class="sxs-lookup"><span data-stu-id="19da0-116">Distributing amounts</span></span>
<span data-ttu-id="19da0-117">Kad ievadāt brīva teksta rēķinu, katra summa tiek sadalīta tālāk aprakstītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="19da0-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19da0-118">Naudas summas tips</span><span class="sxs-lookup"><span data-stu-id="19da0-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="19da0-119">Kur tiek ņemts rādītais galvenais konts</span><span class="sxs-lookup"><span data-stu-id="19da0-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="19da0-120">Prioritāšu secība, kas nosaka, kuras noklusējuma finanšu dimensijas tiek parādītas</span><span class="sxs-lookup"><span data-stu-id="19da0-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19da0-121">Brīvā teksta rēķina rinda</span><span class="sxs-lookup"><span data-stu-id="19da0-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="19da0-122">Virsgrāmatas konts brīva teksta rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="19da0-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="19da0-123">Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</span><span class="sxs-lookup"><span data-stu-id="19da0-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="19da0-124">Ja galvenais konts nav sadalījuma konts, brīva teksta rēķina rindā izmantot finanšu dimensijas noklusējuma veidni.</span><span class="sxs-lookup"><span data-stu-id="19da0-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="19da0-125">Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="19da0-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="19da0-126">Izmantot noklusējuma finanšu dimensiju vērtības no virsgrāmatas konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="19da0-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19da0-127">Brīva teksta rēķina rinda pamatlīdzekļa numura un vērtības modeļa kombinācijai</span><span class="sxs-lookup"><span data-stu-id="19da0-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="19da0-128"><strong>Piezīme</strong></span><span class="sxs-lookup"><span data-stu-id="19da0-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19da0-129">Galvenais konts brīvā teksta rēķina rindā būs pamatlīdzekļu izslēgšanas konts.</span><span class="sxs-lookup"><span data-stu-id="19da0-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="19da0-130">Virsgrāmatas konts brīva teksta rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="19da0-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="19da0-131">Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="19da0-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="19da0-132">Izmantot noklusējuma finanšu dimensiju vērtības no virsgrāmatas konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="19da0-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19da0-133">Brīva teksta rēķina atlaides summa</span><span class="sxs-lookup"><span data-stu-id="19da0-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="19da0-134">Lauks Galvenais konts debitoru atlaidēm lapā Termiņatlaides.</span><span class="sxs-lookup"><span data-stu-id="19da0-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="19da0-135">Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</span><span class="sxs-lookup"><span data-stu-id="19da0-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="19da0-136">Ja galvenais konts nav sadalījuma konts, brīva teksta rēķina rindā izmantot finanšu dimensijas noklusējuma veidni.</span><span class="sxs-lookup"><span data-stu-id="19da0-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="19da0-137">Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="19da0-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="19da0-138">Izmantot noklusējuma finanšu dimensiju vērtības no virsgrāmatas konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="19da0-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19da0-139">Brīva teksta rēķina pārdošanas nodokļa summa</span><span class="sxs-lookup"><span data-stu-id="19da0-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="19da0-140">Lauks Maksājamais pārdošanas nodoklis lapā Virsgrāmatas grāmatošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="19da0-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="19da0-141">Izmantot finanšu dimensijas, kas ir definētas brīva teksta rēķina rindas summai, vai sadales maksa rindas summai.</span><span class="sxs-lookup"><span data-stu-id="19da0-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="19da0-142">Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="19da0-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="19da0-143">Izmantot noklusējuma finanšu dimensiju vērtības no virsgrāmatas konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="19da0-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19da0-144">Brīva teksta rēķina maksas rindas summa</span><span class="sxs-lookup"><span data-stu-id="19da0-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="19da0-145">Lauks Kredīta konts lapā Maksas kods.</span><span class="sxs-lookup"><span data-stu-id="19da0-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="19da0-146">Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</span><span class="sxs-lookup"><span data-stu-id="19da0-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="19da0-147">Ja galvenais konts nav sadalījuma konts, brīva teksta rēķina rindā izmantot finanšu dimensijas noklusējuma veidni.</span><span class="sxs-lookup"><span data-stu-id="19da0-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="19da0-148">Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="19da0-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="19da0-149">Izmantot noklusējuma finanšu dimensiju vērtības no virsgrāmatas konta lapā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="19da0-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="19da0-150">Nodokļu sadalīšana</span><span class="sxs-lookup"><span data-stu-id="19da0-150">Distributing taxes</span></span>
<span data-ttu-id="19da0-151">Nodokļu uzskaites sadales var izveidot tikai pēc nodokļu aprēķināšanas.</span><span class="sxs-lookup"><span data-stu-id="19da0-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="19da0-152">Lai aprēķinātu pārdošanas nodokļus, ir jāizpilda viens no tālāk aprakstītajiem uzdevumiem formā Brīva teksta rēķins.</span><span class="sxs-lookup"><span data-stu-id="19da0-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="19da0-153">Apskatiet PVN.</span><span class="sxs-lookup"><span data-stu-id="19da0-153">View the sales tax.</span></span>
-   <span data-ttu-id="19da0-154">Apskatiet rēķina kopsummu.</span><span class="sxs-lookup"><span data-stu-id="19da0-154">View the invoice total.</span></span>
-   <span data-ttu-id="19da0-155">Apskatiet skaidras naudas plūsmu.</span><span class="sxs-lookup"><span data-stu-id="19da0-155">View the cash flow.</span></span>
-   <span data-ttu-id="19da0-156">Apskatiet uzskaites sadales visam brīva teksta rēķinam.</span><span class="sxs-lookup"><span data-stu-id="19da0-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="19da0-157">Apskatiet apakšgrāmatas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="19da0-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="19da0-158">Apakšgrāmatas žurnāli brīva teksta rēķiniem</span><span class="sxs-lookup"><span data-stu-id="19da0-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="19da0-159">Pirms grāmatojat brīva teksta rēķinu, varat apskatīt pilnu uzskaites ierakstu šim rēķinam, kas ietver debetu un kredītu, lai pārliecinātos, ka rēķins tiek grāmatots pareizajos kontos.</span><span class="sxs-lookup"><span data-stu-id="19da0-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="19da0-160">Šis pilnās uzskaites ieraksta skats tiek saukts par apakšgrāmatas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="19da0-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="19da0-161">Ja pirms brīva teksta rēķina reģistrēšanas žurnālā priekšskatāt apakšgrāmatas žurnāla ierakstu un tas ir nepareizs, šo apakšgrāmatas žurnāla ierakstu nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="19da0-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="19da0-162">Tā vietā ir jāmaina uzskaites sadales vai grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="19da0-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="19da0-163">Uzskaites sadales tiek izmantotas, lai noteiktu uzskaites ieraksta vienu pusi, debetu vai kredītu.</span><span class="sxs-lookup"><span data-stu-id="19da0-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="19da0-164">Korespondējošais apakšgrāmatas žurnāla konta ieraksts tiek izveidots no grāmatošanas metodēm, piemēram, no debitora konta vai nodokļiem.</span><span class="sxs-lookup"><span data-stu-id="19da0-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>



