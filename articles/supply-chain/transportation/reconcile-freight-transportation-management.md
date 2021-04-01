---
title: Saskaņot kravu transportēšanas pārvaldībā
description: Šajā tēmā ir izklāstīts kravas saskaņošanas process.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7af7bbb500de25e0a796147fae42cd7d943be9df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205230"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="29fe6-103">Saskaņot kravu transportēšanas pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="29fe6-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29fe6-104">Šajā tēmā ir izklāstīts kravas saskaņošanas process.</span><span class="sxs-lookup"><span data-stu-id="29fe6-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="29fe6-105">Kravas saskaņošanu var izpildīt manuāli vai to var iestatīt automātiskai izpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="29fe6-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="29fe6-106">Lai izmantotu automātisko kravas saskaņošanu, ir jāiestata audita šablons, kur varat definēt kritērijus, kuri nosaka, kādi kravas rēķini tiek saskaņoti automātiski.</span><span class="sxs-lookup"><span data-stu-id="29fe6-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="29fe6-107">Kravas saskaņošanas process</span><span class="sxs-lookup"><span data-stu-id="29fe6-107">The freight reconciliation process</span></span>

<span data-ttu-id="29fe6-108">Kravas pārvadāšanas likmes aprēķina likmes noteikšanas programma, kas ir saistīta ar attiecīgo sūtījumu pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="29fe6-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="29fe6-109">Ja krava ir apstiprināta, tiek ģenerēta kravas pavadzīme un uz to tiek pārsūtītas kravas pārvadāšanas likmes.</span><span class="sxs-lookup"><span data-stu-id="29fe6-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="29fe6-110">Kravas pārvadāšanas likmes tiek iedalītas kā papildmaksas attiecīgajam pirmdokumentam (pirkšanas pasūtījumam, pārdošanas pasūtījumam un/vai pārsūtīšanas pasūtījumam) atkarībā no regulārajam norēķinu procesam izmantotajiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="29fe6-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="29fe6-111">Kravas saskaņošanas process (kas tiek saukts arī par salīdzināšanas procesu) var sākties, tiklīdz tiek saņemts kravas rēķins no sūtījumu pārvadātāja.</span><span class="sxs-lookup"><span data-stu-id="29fe6-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="29fe6-112">Rēķinu var saņemt elektroniski vai papīra formātā.</span><span class="sxs-lookup"><span data-stu-id="29fe6-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="29fe6-113">Ja rēķins tiek saņemts papīra formātā, varat ģenerēt elektronisku rēķinu, izmantojot kravas pavadzīmi kā veidni.</span><span class="sxs-lookup"><span data-stu-id="29fe6-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="29fe6-114">[![Kravas saskaņošanas process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="29fe6-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="29fe6-115">Manuāla saskaņošana</span><span class="sxs-lookup"><span data-stu-id="29fe6-115">Manual reconciliation</span></span>

<span data-ttu-id="29fe6-116">Ja kravu saskaņojat manuāli, tad rēķinā iekļautajai kravai katra rēķina rinda ir jāsalīdzina ar kravas pavadzīmes rindu vai rindām.</span><span class="sxs-lookup"><span data-stu-id="29fe6-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="29fe6-117">Šo salīdzināšanu jūs veicat lapā **Kravas pavadzīmes un rēķina salīdzināšana**.</span><span class="sxs-lookup"><span data-stu-id="29fe6-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="29fe6-118">Ja rēķina rindas summa neatbilst kravas pavadzīmes summai, jums ir jāatlasa saskaņošanas iemesls šai atšķirībai.</span><span class="sxs-lookup"><span data-stu-id="29fe6-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="29fe6-119">Ja saskaņošanai pastāv vairāki iemesli, neatbilstošo summu varat sadalīt starp tiem.</span><span class="sxs-lookup"><span data-stu-id="29fe6-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="29fe6-120">Saskaņošanas iemesls nosaka, kā šīs starpību summas tiek grāmatotas virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="29fe6-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="29fe6-121">Kad ir izpildīta visa rēķina summas saskaņošana, tā tiek iesniegta apstiprināšanai, un pēc tam žurnāls tiek grāmatots.</span><span class="sxs-lookup"><span data-stu-id="29fe6-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="29fe6-122">Nākamajā attēlā ir parādīts, kā ģenerēt kravas rēķinu un veikt kravas saskaņošanu.</span><span class="sxs-lookup"><span data-stu-id="29fe6-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="29fe6-123">[![Kravas saskaņošanas uzdevumi](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="29fe6-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="29fe6-124">Automātiska saskaņošana</span><span class="sxs-lookup"><span data-stu-id="29fe6-124">Automatic reconciliation</span></span>

<span data-ttu-id="29fe6-125">Lai izmantotu automātisko saskaņošanu, jums ir jānorāda saskaņošanas grafiks, kā arī izmantojamie rēķini un sūtījumu pārvadātāji.</span><span class="sxs-lookup"><span data-stu-id="29fe6-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="29fe6-126">Rēķinu rindu un kravu pavadzīmju salīdzināšana tiek veikta atbilstoši audita šablona iestatījumiem un kravas pavadzīmes tipam.</span><span class="sxs-lookup"><span data-stu-id="29fe6-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="29fe6-127">Kad esat izpildījis automātisko saskaņošanu, jums ir jāapstrādā visi rēķini, kurus sistēma nespēj saskaņot.</span><span class="sxs-lookup"><span data-stu-id="29fe6-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="29fe6-128">Pēc tam jums šie rēķini ir jāpārstrādā manuāli, pirms visus rēķinus varat grāmatot maksājumam.</span><span class="sxs-lookup"><span data-stu-id="29fe6-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="29fe6-129">Saskaņot kravas pavadzīmes ar kravas rēķiniem, izmantojot automātisku vai manuālu saskaņošanu</span><span class="sxs-lookup"><span data-stu-id="29fe6-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="29fe6-130">*Saskaņošana* ir process, kurā tiek meklētas kravu pavadzīmes, kas atbilst katram kravas pavadzīmei.</span><span class="sxs-lookup"><span data-stu-id="29fe6-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="29fe6-131">To var izdarīt, saskaņojot rēķinu rindas pa vienai (manuāla saskaņošana) vai saskaņojot visus pieejamos rēķinus uzreiz (automātiskā saskaņošana).</span><span class="sxs-lookup"><span data-stu-id="29fe6-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="29fe6-132">Automātiskā saskaņošana</span><span class="sxs-lookup"><span data-stu-id="29fe6-132">Auto matching</span></span>

<span data-ttu-id="29fe6-133">Saskaņojot vairākus kravas rēķinus ar vienu kravas pavadzīmi, automātiskās atbilstības process darbojas šādi:</span><span class="sxs-lookup"><span data-stu-id="29fe6-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="29fe6-134">Visi saskaņotie kravas rēķini tiek kārtoti pēc summas, un pirmā ir vislielākā summa.</span><span class="sxs-lookup"><span data-stu-id="29fe6-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="29fe6-135">Kravas pavadzīmes tiek saskaņotas vienu pa vienam, līdz kravas pavadzīmei nav atlicis pozitīvs daudzums.</span><span class="sxs-lookup"><span data-stu-id="29fe6-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="29fe6-136">Atkarībā no audita šablona iestatījumiem un kravas pavadzīmju atlikušās summas, tiek iestatīta atlikusī summa.</span><span class="sxs-lookup"><span data-stu-id="29fe6-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="29fe6-137">Manuāla saskaņošana</span><span class="sxs-lookup"><span data-stu-id="29fe6-137">Manual matching</span></span>

<span data-ttu-id="29fe6-138">Visas kravas pavadzīmes ar pozitīvām summām būs pieejamas saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="29fe6-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="29fe6-139">Līdzīgi automātiskajai saskaņošanai lietotājs varēs saskaņot tikai kravas pavadzīmes ar negatīvām summām kravas pavadzīmēm, kas nav pilnībā saskaņotas.</span><span class="sxs-lookup"><span data-stu-id="29fe6-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="29fe6-140">Paraugs</span><span class="sxs-lookup"><span data-stu-id="29fe6-140">Example</span></span>

<span data-ttu-id="29fe6-141">Pieņemsim, ka jums ir kravas pavadzīme (FB) par summu 1500 un esat izveidojis trīs kravas pavadzīmes kravas pavadzīmes rēķinus ar vienu rēķina rindu katram rēķinam ar šādiem iestatījumiem:</span><span class="sxs-lookup"><span data-stu-id="29fe6-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="29fe6-142">Sākotnējā kravas pavadzīme (FB): summa 1500</span><span class="sxs-lookup"><span data-stu-id="29fe6-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="29fe6-143">1. rēķins (Inv1): summa 1000</span><span class="sxs-lookup"><span data-stu-id="29fe6-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="29fe6-144">2. rēķins (Inv2): summa 600</span><span class="sxs-lookup"><span data-stu-id="29fe6-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="29fe6-145">3. rēķins (Inv3): summa -100</span><span class="sxs-lookup"><span data-stu-id="29fe6-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="29fe6-146">Automātiska atbilstības rezultāts</span><span class="sxs-lookup"><span data-stu-id="29fe6-146">Automatic matching result</span></span>

<span data-ttu-id="29fe6-147">Automātiskā saskaņošana tiks izpildīta šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="29fe6-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="29fe6-148">Kārtot visus kravas rēķinus dilstošā secībā pēc summas: Inv1 -> Inv2 -> Inv3.</span><span class="sxs-lookup"><span data-stu-id="29fe6-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="29fe6-149">Saskaņot Inv1 ar FB.</span><span class="sxs-lookup"><span data-stu-id="29fe6-149">Match Inv1 with FB.</span></span> <span data-ttu-id="29fe6-150">Inv1 ir 1000 saskaņots, un FB atlikusī summa ir 500, tāpēc statuss ir iestatīts uz *Daļēji saskaņots*.</span><span class="sxs-lookup"><span data-stu-id="29fe6-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="29fe6-151">Saskaņot Inv2 ar FB.</span><span class="sxs-lookup"><span data-stu-id="29fe6-151">Match Inv2 with FB.</span></span> <span data-ttu-id="29fe6-152">Inv2 ir 500 saskaņoti, un FB atlikusī summa ir 0, tāpēc statuss ir iestatīts uz *Pilnībā saskaņots*.</span><span class="sxs-lookup"><span data-stu-id="29fe6-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="29fe6-153">Tā kā FB tagad ir pilnībā saskaņots, Inv3 netiks apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="29fe6-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="29fe6-154">Manuālas atbilstības rezultāts</span><span class="sxs-lookup"><span data-stu-id="29fe6-154">Manual matching result</span></span>

<span data-ttu-id="29fe6-155">Manuālai saskaņošanai rezultāti mainās atkarībā no atbilstības secības, kā ilustrēts šajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="29fe6-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="29fe6-156">Manuālas saskaņošanas gadījums 1</span><span class="sxs-lookup"><span data-stu-id="29fe6-156">Manual matching case 1</span></span>

<span data-ttu-id="29fe6-157">Viens veids, kā veikt manuālu atbilstības šajā piemērā ir turpināt šādi:</span><span class="sxs-lookup"><span data-stu-id="29fe6-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="29fe6-158">Saskaņot Inv1 ar FB.</span><span class="sxs-lookup"><span data-stu-id="29fe6-158">Match FB with Inv1.</span></span> <span data-ttu-id="29fe6-159">FB ir 500 saskaņoti, tāpēc statuss ir iestatīts uz *Daļēji saskaņots*.</span><span class="sxs-lookup"><span data-stu-id="29fe6-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="29fe6-160">Saskaņot Inv2 ar FB.</span><span class="sxs-lookup"><span data-stu-id="29fe6-160">Match Inv2 with FB.</span></span> <span data-ttu-id="29fe6-161">Inv2 ir 500 saskaņoti, un FB atlikusī summa ir 0, tāpēc statuss ir iestatīts uz *Pilnībā saskaņots*.</span><span class="sxs-lookup"><span data-stu-id="29fe6-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="29fe6-162">Manuāli saskaņojot Inv3, jūs neatradīsiet nevienu nesaskaņotu kravu pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="29fe6-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="29fe6-163">Šis gadījums pamatā ir tāds pats kā automātiskā saskaņošana</span><span class="sxs-lookup"><span data-stu-id="29fe6-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="29fe6-164">Manuālas saskaņošanas gadījums 2</span><span class="sxs-lookup"><span data-stu-id="29fe6-164">Manual matching case 2</span></span>

<span data-ttu-id="29fe6-165">Viens veids, kā veikt manuālu atbilstības šajā piemērā ir turpināt šādi:</span><span class="sxs-lookup"><span data-stu-id="29fe6-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="29fe6-166">Saskaņot Inv3 ar FB.</span><span class="sxs-lookup"><span data-stu-id="29fe6-166">Match Inv3 with FB.</span></span> <span data-ttu-id="29fe6-167">Tagad FB atlikusī summa ir 1600, kas ir tā pati, kas atņemot negatīvos 100 pa virsu 1500.</span><span class="sxs-lookup"><span data-stu-id="29fe6-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="29fe6-168">Gan FB, gan Inv3 atbilstošais daudzums ir -100.</span><span class="sxs-lookup"><span data-stu-id="29fe6-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="29fe6-169">Saskaņot Inv1 un Inv 2 ar FB vienu pēc otra.</span><span class="sxs-lookup"><span data-stu-id="29fe6-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="29fe6-170">FB ir pilnībā saskaņots.</span><span class="sxs-lookup"><span data-stu-id="29fe6-170">FB is fully matched.</span></span>

<span data-ttu-id="29fe6-171">Kā redzams šajā piemērā, atbilstošie kravas rēķini ar negatīvām summām ir jāveic tikai manuāli.</span><span class="sxs-lookup"><span data-stu-id="29fe6-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="29fe6-172">Tas nodrošina, ka vienmēr ir iespējams saskaņot kravas pavadzīmes ar negatīvām summām un kravas pavadzīmi, kas nav pilnībā saskaņotas, jo tādējādi var kontrolēt atbilstošo secību.</span><span class="sxs-lookup"><span data-stu-id="29fe6-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]