---
title: Pārdošanas pasūtījumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas pasūtījumiem.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974789"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="d0ecf-103">Pārdošanas pasūtījumu problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="d0ecf-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="d0ecf-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="d0ecf-105">Mainot pārdošanas pasūtījuma galvenē norādīto atrašanās vietu, nodokļu informācija netiek atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d0ecf-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="d0ecf-106">Issue description</span></span>

<span data-ttu-id="d0ecf-107">Ja vieta, noliktava vai piegādes adrese tiek izmainīta pārdošanas pasūtījuma galvenes vai rindas līmenī, šo rindu nodokļu informācija netiek automātiski atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d0ecf-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="d0ecf-108">Issue resolution</span></span>

<span data-ttu-id="d0ecf-109">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-109">This behavior is by design.</span></span> <span data-ttu-id="d0ecf-110">Problēma rodas, ja piegādes adrese, vieta un noliktava netiek automātiski mainīta rindas līmenī.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="d0ecf-111">Tās ir jāatjaunina manuāli.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="d0ecf-112">Ja vienam periodam vai periodiem, kas pārklājas, ir divi tirdzniecības līgumi, vienmēr tiek atlasīta viena un tā pati līguma rinda.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d0ecf-113">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="d0ecf-113">Issue description</span></span>

<span data-ttu-id="d0ecf-114">Ja divi tirdzniecības līgumi ir definēti vienam periodam vai periodiem, kas pārklājas, viens un tas pats tirdzniecības līgums tiek atlasīts katru reizi, kad izveidojat pārdošanas pasūtījuma rindas, kurās ir ietverti šie vienumi.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d0ecf-115">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="d0ecf-115">Issue resolution</span></span>

<span data-ttu-id="d0ecf-116">Ja noteiktam datumam ir vairāk nekā viens tirdzniecības līgums, vienmēr tiek atlasīts tirdzniecības līgums ar zemāko cenu.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="d0ecf-117">Lai iegūtu papildinformāciju, lejupielādējiet šādu tehnisko dokumentu: [Tirdzniecības līgumi programmā Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="d0ecf-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="d0ecf-118">Vai var saistīt pirkšanas pasūtījumu ar pārdošanas pasūtījumu, lai izpildītu pieprasījumu?</span><span class="sxs-lookup"><span data-stu-id="d0ecf-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="d0ecf-119">Pirkšanas pasūtījumu varat izveidot no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="d0ecf-120">Papildinformāciju skatiet sadaļā [Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="d0ecf-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="d0ecf-121">Nevar atcelt vai dzēst atgriešanas pasūtījumu vai pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="d0ecf-122">Varat atcelt tikai tos pārdošanas pasūtījumus un atgriešanas pasūtījumus, kas ir ar statusu *Izveidots*.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="d0ecf-123">Papildinformāciju skatiet sadaļā [Atgriešanas pasūtījuma atcelšana](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="d0ecf-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="d0ecf-124">Mēģinot atcelt pārdošanas pasūtījumu, tiek atgriezta kļūda “Rezervācijas nevar noņemt, jo ir izveidots darbs, kas balstās uz rezervāciju”.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="d0ecf-125">Kļūdas kods: WAX4661</span><span class="sxs-lookup"><span data-stu-id="d0ecf-125">Error code: WAX4661</span></span>

<span data-ttu-id="d0ecf-126">Ja darbs ir saistīts ar pārdošanas pasūtījumu, jūs nevarat atcelt pārdošanas pasūtījumu, kamēr nav atcelts un atsaukts darbs.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="d0ecf-127">Šī prasība ir spēkā pat tad, ja ar pārdošanas pasūtījumu saistītais darbs ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="d0ecf-128">Lai novērstu šo problēmu, izpildiet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="d0ecf-129">Atceliet darbu un ievietojiet krājumu atpakaļ vēlamajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="d0ecf-130">Dodieties uz atbilstošo pārdošanas pasūtījuma noslodzi un atlasiet **Samazināt izdoto daudzumu** kravas rindā vai **Atsaukt darbu** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="d0ecf-131">Darbs tagad ir ar statusu *Atcelts* un jauns krājumu pārvietošanas darbs tiek automātiski izveidots un apstrādāts, lai ievietotu krājumus atpakaļ novietojumā, kas tika aprakstīts atsaukšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="d0ecf-132">Dzēsiet noslodzi.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-132">Delete the load.</span></span> <span data-ttu-id="d0ecf-133">Tiek dzēsts arī sūtījums.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="d0ecf-134">Tagad varēsit doties uz pārdošanas pasūtījumu un to atcelt.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="d0ecf-135">Nevar atcelt starpuzņēmumu pirkšanas pasūtījumu, kas ir saistīts ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d0ecf-136">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="d0ecf-136">Issue description</span></span>

<span data-ttu-id="d0ecf-137">Mēģinot atcelt starpuzņēmumu pirkšanas pasūtījumu, kas ir saistīts ar pārdošanas pasūtījumu, var tikt parādīts šāds kļūdas ziņojums: “Daudzumu nevar samazināt, jo atlikušais atjaunināšanas daudzums maina zīmi.”</span><span class="sxs-lookup"><span data-stu-id="d0ecf-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d0ecf-138">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="d0ecf-138">Issue resolution</span></span>

<span data-ttu-id="d0ecf-139">Šī problēma tika novērsta Microsoft Dynamics 365 Supply Chain Management versijā 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="d0ecf-140">Šajā un jaunākās versijās tagad varat atcelt starpuzņēmumu pirkšanas pasūtījumu, kas ir saistīts ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="d0ecf-141">Vai var atjaunot rēķinā iekļauto pārdošanas pasūtījumu, kas tika dzēsts?</span><span class="sxs-lookup"><span data-stu-id="d0ecf-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="d0ecf-142">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="d0ecf-142">Issue description</span></span>

<span data-ttu-id="d0ecf-143">Rēķinā iekļautais pārdošanas pasūtījums tika dzēsts kļūdas dēļ, un jūs vēlaties to atjaunot vai skatīt tā detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d0ecf-144">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="d0ecf-144">Issue resolution</span></span>

<span data-ttu-id="d0ecf-145">Ja dzēstais pārdošanas pasūtījums jau ir iekļauts rēķinā, dodieties uz **Debitora konts \> Transakcijas \> Oriģinālais dokuments \> Skatīt detalizētu informāciju**.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="d0ecf-146">Atrodiet meklēto rēķinu un atlasiet to, lai skatītu tā detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="d0ecf-147">Šīs informācija ietver pārdošanas pasūtījuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-147">These details include the sales order reference.</span></span> <span data-ttu-id="d0ecf-148">Pārdošanas pasūtījuma informācijai var piekļūt arī no šīs lapas.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="d0ecf-149">Pārdošanas pasūtījuma izpildes termiņa galveni nevar atrast SalesOrderHeaderV2Entity datu elementā.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="d0ecf-150">Elementā *SalesOrderHeaderV2Entity* nav izpildes termiņa lauka.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="d0ecf-151">Nepieciešams dzēst nošķirtos pārdošanas pasūtījumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="d0ecf-152">Lai notīrītu nošķirtos pārdošanas pasūtījumu ierakstus, palaidiet periodisko uzdevumu *Pārdošanas pasūtījumu dzēšana*, dodoties uz vienu no šīm vietām:</span><span class="sxs-lookup"><span data-stu-id="d0ecf-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="d0ecf-153">Pārdošana un mārketings \> Periodiskie uzdevumi \> Tīrīt \> Dzēst pārdošanas pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="d0ecf-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="d0ecf-154">Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Tīrīt \> Dzēst pārdošanas pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="d0ecf-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="d0ecf-155">Vai ir iespējams aprēķināt komisijas maksu rēķiniem, kas jau ir iegrāmatoti?</span><span class="sxs-lookup"><span data-stu-id="d0ecf-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="d0ecf-156">Supply Chain Management pašlaik neatbalsta komisijas maksu aprēķināšanu iegrāmatotajiem rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="d0ecf-157">Komplekta krājums netiek atbalstīts starpuzņēmumu procesā.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="d0ecf-158">Komplekta krājums nav pieejams pirkšanas pasūtījumam, jo, pārbaudot komplekta krājuma pārdošanas pasūtījuma rindas, jūs ievērosit, ka daudzums ir *0* (nulle) un statuss ir *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="d0ecf-159">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-159">This behavior is by design.</span></span> <span data-ttu-id="d0ecf-160">Pārdošanas pasūtījums iegādājas tikai komplekta krājuma komponentus.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="d0ecf-161">Tas nepērk pašu komplekta krājumu.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="d0ecf-162">Ja ir nepieciešams iegādāties komplektu, apsveriet, vai ir nepieciešams to atzīmēt kā komplekta krājumu, jo šī funkcionalitāte faktiski ir paredzēta ieņēmumu atzīšanas scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="d0ecf-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="d0ecf-163">Papildinformāciju par komplektu krājumiem, skatiet sadaļā [Komplekti](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="d0ecf-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
