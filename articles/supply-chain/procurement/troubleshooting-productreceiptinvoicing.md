---
title: Produktu ieejas plūsmu un rēķinu izrakstīšanas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar produktu ieejas plūsmām un rēķinu izrakstīšanu.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d86fa3df1de13cc0e0fb94449207a326069da25b
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834394"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="5c504-103">Produktu ieejas plūsmu un rēķinu izrakstīšanas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="5c504-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="5c504-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar produktu ieejas plūsmām un rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="5c504-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="5c504-105">Nevar grāmatot vairāk par vienu rēķinu pirkšanas pasūtījuma rindai ar kategorijām atbilstošajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="5c504-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="5c504-106">Grāmatojot rēķinus, daudzums ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="5c504-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="5c504-107">Tāpēc, ja pilnam rindas daudzumam ir izrakstīts rēķins par tikai daļēju summu, jūs nevarēsit izrakstīt rēķinu atlikušajai summai citā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="5c504-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="5c504-108">Pirkšanas pasūtījuma apstiprināšanas laikā tiek parādīts kļūdas ziņojums “Objekta atsauce nav iestatīta” vai kreditora rēķina iegrāmatošanas laikā rodas izņēmums “Izsaukšanas mērķis atgriež izņēmumu”.</span><span class="sxs-lookup"><span data-stu-id="5c504-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="5c504-109">Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.</span><span class="sxs-lookup"><span data-stu-id="5c504-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="5c504-110">Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="5c504-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="5c504-111">Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="5c504-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="5c504-112">Nevar konsolidēt vairāku produktu ieejas plūsmas vienā pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="5c504-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="5c504-113">Nevar konsolidēt vairāku produktu ieejas plūsmas vienā pirkšanas pasūtījumā, ja dažādām produktu ieejas plūsmu rindām ir dažādi uzskaites datumi.</span><span class="sxs-lookup"><span data-stu-id="5c504-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="5c504-114">Iepriekšējās Microsoft Dynamics 365 Supply Chain Management versijās šajā situācijā konsolidācija tika atļauta.</span><span class="sxs-lookup"><span data-stu-id="5c504-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="5c504-115">Tomēr praksē pastāv nosliece uz kļūdu.</span><span class="sxs-lookup"><span data-stu-id="5c504-115">However, the practice is prone to error.</span></span> <span data-ttu-id="5c504-116">Izveidotais pirkšanas pasūtījuma rindu uzskaites datums nedrīkst atšķirties no uzskaites datuma produktu ieejas plūsmas rindās, no kurām tika izveidotas šīs pirkšanas pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="5c504-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="5c504-117">(Pirkšanas pasūtījuma rindu uzskaites datums atbilst uzskaites datumam pirkšanas pasūtījuma galvenē.) Tāpēc vairāku produktu ieejas plūsmu konsolidēšana vienā pirkšanas pasūtījumā vairs netiek atļauta.</span><span class="sxs-lookup"><span data-stu-id="5c504-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="5c504-118">Uzskaites datums tiek izmantots, piemēram, budžeta rezervācijām un apgrūtinājumam.</span><span class="sxs-lookup"><span data-stu-id="5c504-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="5c504-119">Tāpēc tas jāsaglabā pārejas periodā no produktu ieejas plūsmas uz pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5c504-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="5c504-120">Kad produktu ieejas plūsmas ir atceltas, darījumus var grāmatot aizturētajā Virsgrāmatas kontā.</span><span class="sxs-lookup"><span data-stu-id="5c504-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5c504-121">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5c504-121">Issue description</span></span>

<span data-ttu-id="5c504-122">Ja produktu ieejas plūsma ir atcelta, sistēma ļauj grāmatot darījumus aizturētajos Virsgrāmatas kontos, pat ja galvenie konti ir aizturēti.</span><span class="sxs-lookup"><span data-stu-id="5c504-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="5c504-123">Problēmas atveide</span><span class="sxs-lookup"><span data-stu-id="5c504-123">Reproduce the issue</span></span>

<span data-ttu-id="5c504-124">Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.</span><span class="sxs-lookup"><span data-stu-id="5c504-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="5c504-125">Lapā **Kreditoru parametri** cilnē **Vispārīgi** pārliecinieties, vai opcija **Grāmatot produktu ieejas plūsmu Virsgrāmatā** ir iestatīta uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="5c504-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="5c504-126">Izveidojiet pirkšanas pasūtījumu un pievienojiet pasūtījuma rindu, kurā preces daudzums ir *1 000*.</span><span class="sxs-lookup"><span data-stu-id="5c504-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="5c504-127">Apstipriniet pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5c504-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="5c504-128">Grāmatojiet produktu ieejas plūsmu un pārbaudiet dokumentus.</span><span class="sxs-lookup"><span data-stu-id="5c504-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="5c504-129">Aizturiet attiecīgos galvenos kontus, *200140* un *140200*.</span><span class="sxs-lookup"><span data-stu-id="5c504-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="5c504-130">Atceliet grāmatoto produktu ieejas plūsmu.</span><span class="sxs-lookup"><span data-stu-id="5c504-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="5c504-131">Ievērojiet, ka darījumus var grāmatot aizturētajos Virsgrāmatas kontos.</span><span class="sxs-lookup"><span data-stu-id="5c504-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5c504-132">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5c504-132">Issue resolution</span></span>

<span data-ttu-id="5c504-133">Darījumus var grāmatot aizturētajos Virsgrāmatas kontos, kad produktu ieejas plūsmas ir atceltas, jo šī darbība ļauj labot grāmatojumus.</span><span class="sxs-lookup"><span data-stu-id="5c504-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="5c504-134">Produktu ieejas plūsmas dokumenta numurs tiek patērēts pat tad, ja nav izveidots finanšu dokuments produktu ieejas plūsmas laikā.</span><span class="sxs-lookup"><span data-stu-id="5c504-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="5c504-135">Ja krājumu modeļu grupu opcija **Uzkrāt saistības produktu ieejas plūsmā** ir iestatīta uz *Nē*, grāmatošana Virsgrāmatā netiks veikta.</span><span class="sxs-lookup"><span data-stu-id="5c504-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="5c504-136">Tomēr fizisks notikums tiks ierakstīts, lai veiktu uzskaiti apakšgrāmatā, un šim notikumam nepieciešams dokumenta numurs.</span><span class="sxs-lookup"><span data-stu-id="5c504-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="5c504-137">Šis dokumenta numurs ir dokumenta numurs, uz kuru ir atsauce krājumu darījumā.</span><span class="sxs-lookup"><span data-stu-id="5c504-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="5c504-138">Ieteicams iestatīt opciju **Uzkrāt saistības produktu ieejas plūsmā** uz *Jā*, kā aprakstīts šajā emuāra ierakstā: [Papildmaksu grāmatošana produktu ieejas plūsmas laikā](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="5c504-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="5c504-139">Virsgrāmatas iestatījumā nav ieslēgta Grāmatošana izmaksu kontā.</span><span class="sxs-lookup"><span data-stu-id="5c504-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5c504-140">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5c504-140">Issue description</span></span>

<span data-ttu-id="5c504-141">Šī problēma rodas, izrakstot rēķinu pirkšanas pasūtījumam, ja opcija **Grāmatot Virsgrāmatas izmaksu kontā** ir iestatīta uz *Jā* cilnē **Rēķins**, kas atrodas lapā **Kreditoru parametri**.</span><span class="sxs-lookup"><span data-stu-id="5c504-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="5c504-142">Problēmas atveide</span><span class="sxs-lookup"><span data-stu-id="5c504-142">Reproduce the issue</span></span>

<span data-ttu-id="5c504-143">Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.</span><span class="sxs-lookup"><span data-stu-id="5c504-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="5c504-144">Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa parametri**.</span><span class="sxs-lookup"><span data-stu-id="5c504-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="5c504-145">Cilnē **Rēķins** iestatiet opciju **Grāmatot Virsgrāmatas izmaksu kontā** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="5c504-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="5c504-146">Doties uz **Krājumu vadība \> Iestatīšana \> Grāmatojums \> Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="5c504-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="5c504-147">Cilnē **Pirkšanas pasūtījums** pārliecinieties, vai visas preces pirkšanas izdevumu rindas ir izdzēstas.</span><span class="sxs-lookup"><span data-stu-id="5c504-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="5c504-148">Dodieties uz **Kreditori \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5c504-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="5c504-149">Izveidojiet pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5c504-149">Create a purchase order.</span></span> <span data-ttu-id="5c504-150">Laukā **Kreditora konts** atlasiet *1001 Acme Office Supplies*.</span><span class="sxs-lookup"><span data-stu-id="5c504-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="5c504-151">Pievienojiet pirkšanas pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="5c504-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="5c504-152">**Krājuma kods:** *D0011 Laser Projector*</span><span class="sxs-lookup"><span data-stu-id="5c504-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="5c504-153">**Vieta:** *1*</span><span class="sxs-lookup"><span data-stu-id="5c504-153">**Site:** *1*</span></span>
    - <span data-ttu-id="5c504-154">**Noliktava:** *11*</span><span class="sxs-lookup"><span data-stu-id="5c504-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="5c504-155">**Daudzums:** *4*</span><span class="sxs-lookup"><span data-stu-id="5c504-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="5c504-156">Darbību rūts cilnē **Pirkšana**, grupā **Darbība** atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="5c504-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="5c504-157">Darbību rūtī cilnes **Saņemt** grupā **Ģenerēt**, atlasiet **Produktu ieejas plūsma**.</span><span class="sxs-lookup"><span data-stu-id="5c504-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="5c504-158">Dialoglodziņā **Produktu ieejas plūsmas grāmatošana** laukā **Produktu ieejas plūsma**, ievadiet patvaļīgu numuru un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5c504-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="5c504-159">Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="5c504-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="5c504-160">Laukā **Numurs** ievadiet patvaļīgu numuru kā rēķina numuru.</span><span class="sxs-lookup"><span data-stu-id="5c504-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="5c504-161">Atjauniniet atbilstības statusu un grāmatojiet.</span><span class="sxs-lookup"><span data-stu-id="5c504-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="5c504-162">Ievērojiet, ka tagad, ģenerējot rēķinu no pirkšanas pasūtījuma, tiek parādīta šāda kļūda: “Konta numurs darbības veidam Preces pirkšanas izdevumi nepastāv.”</span><span class="sxs-lookup"><span data-stu-id="5c504-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5c504-163">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="5c504-163">Issue resolution</span></span>

<span data-ttu-id="5c504-164">Tas ir atkarīgs no rēķinu un rēķinu grupu parametru iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="5c504-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="5c504-165">Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas izmaksu un krājumu izmaiņu uzskaite](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="5c504-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
