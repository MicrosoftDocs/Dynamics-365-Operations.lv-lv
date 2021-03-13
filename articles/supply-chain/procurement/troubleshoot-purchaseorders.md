---
title: Pirkšanas pasūtījumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pirkšanas pasūtījumiem.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 7b65c23fc7ac04fc30c0001bee9541a475026018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007495"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="92533-103">Pirkšanas pasūtījumu problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="92533-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="92533-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="92533-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="92533-105">Darbību var pabeigt tikai pēc tam, kad rindas numurs ir pilnībā sadalīts.</span><span class="sxs-lookup"><span data-stu-id="92533-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="92533-106">Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.</span><span class="sxs-lookup"><span data-stu-id="92533-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="92533-107">Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="92533-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="92533-108">Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="92533-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="92533-109">Kad pirkšanas pasūtījumi tiek importēti, izmantojot datu pārvaldību, pirkšanas pasūtījuma rindu numuri neseko palielinājumam, kas definēts sistēmas parametros.</span><span class="sxs-lookup"><span data-stu-id="92533-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="92533-110">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="92533-110">Issue description</span></span>

<span data-ttu-id="92533-111">Pēc noklusējuma automātiski ģenerētie rindu numuri pirkšanas pasūtījuma rindām, kas tiek importētas, izmantojot datu elementu *Pirkšanas pasūtījuma rindas V2*, neizmanto sistēmas rindu numuru palielinājumu, kas norādīts sistēmas parametros.</span><span class="sxs-lookup"><span data-stu-id="92533-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="92533-112">Ja manuāli izveidojat pirkšanas pasūtījumu un pievienojat rindas, izmantojot lietotāja interfeisu (UI), rindu numuri tiek palielināti pareizi.</span><span class="sxs-lookup"><span data-stu-id="92533-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="92533-113">Tomēr, ja izmantojat datu pārvaldības struktūras (DMF), tie netiek pareizi palielināti.</span><span class="sxs-lookup"><span data-stu-id="92533-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="92533-114">Šī problēma rodas, ja importējat rindas, izmantojot DMF un importētajā elementā vēl nav piešķirti rindu numuri, tad sistēma izmanto DMF metodi to piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="92533-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="92533-115">Šī metode vienmēr palielina rindu numurus par vienu.</span><span class="sxs-lookup"><span data-stu-id="92533-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="92533-116">Problēmas aprisinājums</span><span class="sxs-lookup"><span data-stu-id="92533-116">Issue workaround</span></span>

<span data-ttu-id="92533-117">Pārliecinieties, lai vēlamie rindu numuri jau ir norādīti datu elementa rindu numuru laukos, kad importējat pirkšanas pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="92533-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="92533-118">Šādā gadījumā DMF nepārrakstīs rindu numurus.</span><span class="sxs-lookup"><span data-stu-id="92533-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="92533-119">Noklusējuma nodokļu grupa un noklusējuma termiņatlaide netiek aizpildīta no rēķina konta.</span><span class="sxs-lookup"><span data-stu-id="92533-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="92533-120">Ja izmantojat rēķina kontu, kas atšķiras no debitora konta, noklusējuma nodokļu grupa un noklusējuma termiņatlaide netiek aizpildīta no rēķina konta, kad tiek izveidots pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="92533-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="92533-121">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="92533-121">This behavior is by design.</span></span> <span data-ttu-id="92533-122">Nodokļu grupas, termiņatlaižu un citas cenu informācijas noklusējuma vērtības ir balstītas uz debitora kontu, nevis uz rēķina kontu.</span><span class="sxs-lookup"><span data-stu-id="92533-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="92533-123">Pirkšanas pasūtījuma apstiprināšanas laikā tiek parādīts kļūdas ziņojums “Objekta atsauce nav iestatīta” vai kreditora rēķina iegrāmatošanas laikā rodas izņēmums “Izsaukšanas mērķis atgriež izņēmumu”.</span><span class="sxs-lookup"><span data-stu-id="92533-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="92533-124">Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.</span><span class="sxs-lookup"><span data-stu-id="92533-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="92533-125">Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="92533-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="92533-126">Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="92533-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="92533-127">Viena vai vairākas uzskaites sadales ir vai nu pārdalītas, vai nepilnīgi sadalītas.</span><span class="sxs-lookup"><span data-stu-id="92533-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="92533-128">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="92533-128">Issue description</span></span>

<span data-ttu-id="92533-129">Tiek parādīts šāds kļūdas ziņojums: “Viena vai vairākas uzskaites sadales ir vai nu pārdalītas, vai nepilnīgi sadalītas.”</span><span class="sxs-lookup"><span data-stu-id="92533-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="92533-130">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="92533-130">Issue resolution</span></span>

<span data-ttu-id="92533-131">Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.</span><span class="sxs-lookup"><span data-stu-id="92533-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="92533-132">Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="92533-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="92533-133">Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="92533-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="92533-134">Vai var parādīt tikai manis izveidotos pirkšanas pasūtījumus?</span><span class="sxs-lookup"><span data-stu-id="92533-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="92533-135">Šī funkcionalitāte pašlaik nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="92533-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="92533-136">Vai var rezervēt krājumus un izveidot darījumus saistībā ar pirkšanas pasūtījumā reģistrētajiem krājumiem?</span><span class="sxs-lookup"><span data-stu-id="92533-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="92533-137">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="92533-137">Issue description</span></span>

<span data-ttu-id="92533-138">Pat ja vienības pirkšanas pasūtījumā ir ar stāvokli *Reģistrēts*, krājumus joprojām var rezervēt.</span><span class="sxs-lookup"><span data-stu-id="92533-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="92533-139">Citiem vārdiem, varat izveidot darbības saistībā ar reģistrētajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="92533-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="92533-140">Problēmas atveide</span><span class="sxs-lookup"><span data-stu-id="92533-140">Reproduce the issue</span></span>

<span data-ttu-id="92533-141">Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.</span><span class="sxs-lookup"><span data-stu-id="92533-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="92533-142">Izveidojiet pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="92533-142">Create a purchase order.</span></span>
2. <span data-ttu-id="92533-143">Reģistrējiet pirkšanas pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="92533-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="92533-144">Ievērojiet, ka varat veikt rezervācijas vai darbības saistībā ar reģistrētajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="92533-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="92533-145">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="92533-145">Issue resolution</span></span>

<span data-ttu-id="92533-146">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="92533-146">This behavior is by design.</span></span> <span data-ttu-id="92533-147">Sagaidāmais rezultāts ir reģistrēto krājumu fiziska saņemšana noliktavā vai krājumos, lai tādējādi tie būtu pieejami rezervēšanai.</span><span class="sxs-lookup"><span data-stu-id="92533-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="92533-148">Pirkšanas pasūtījumi neatspoguļo juridiskās personas valodas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="92533-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="92533-149">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="92533-149">Issue description</span></span>

<span data-ttu-id="92533-150">Preces nosaukums pirkšanas pasūtījumā tiek norādīts sistēmas valodā, nevis valodā, kas iestatīta juridiskajai personai, kurai tika izveidots pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="92533-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="92533-151">Problēmas atveide</span><span class="sxs-lookup"><span data-stu-id="92533-151">Reproduce the issue</span></span>

<span data-ttu-id="92533-152">Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.</span><span class="sxs-lookup"><span data-stu-id="92533-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="92533-153">Iestatiet sistēmas valodu uz *EN-US* (ASV angļu valoda).</span><span class="sxs-lookup"><span data-stu-id="92533-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="92533-154">Pārliecinieties, vai pastāv prece, kam preces nosaukuma tulkošanai tiek saglabātas *EN-US* un *DE* (vācu valoda) valoda.</span><span class="sxs-lookup"><span data-stu-id="92533-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="92533-155">Mainiet juridiskās personas valodu uz *DE*.</span><span class="sxs-lookup"><span data-stu-id="92533-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="92533-156">Juridiskajai personai, kurai ir iestatīta *DE* valoda, izveidojiet pirkšanas pasūtījumu, kas ietver preci.</span><span class="sxs-lookup"><span data-stu-id="92533-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="92533-157">Ņemiet vērā, ka preces nosaukums joprojām ir redzams ASV angļu valodā (sistēmas valoda).</span><span class="sxs-lookup"><span data-stu-id="92533-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="92533-158">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="92533-158">Issue resolution</span></span>

<span data-ttu-id="92533-159">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="92533-159">This behavior is by design.</span></span> <span data-ttu-id="92533-160">Pirkšanas pasūtījumos prece vienmēr tiek rādīta sistēmas valodā.</span><span class="sxs-lookup"><span data-stu-id="92533-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="92533-161">Pirkšanas pasūtījuma valoda tiek izmantota, kad tiek izveidots apstiprinājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="92533-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="92533-162">Pēc preces elementa apstiprinātais piegādātāju saraksts neļauj mainīt spēkā stāšanās datumu.</span><span class="sxs-lookup"><span data-stu-id="92533-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="92533-163">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="92533-163">Issue description</span></span>

<span data-ttu-id="92533-164">Precei ir apstiprināts piegādātājs, kura spēkā stāšanās datums ir, piemēram, 2018. gada 11. janvāris (*01/11/2018*) un beigu datums ir *Nekad*.</span><span class="sxs-lookup"><span data-stu-id="92533-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="92533-165">Ja mēģināsit mainīt spēkā stāšanās datumu uz 2018. gada 10. janvāri (*01/10/2018*) vai 2018. gada 12. janvāri (*01/12/2018*), tiks parādīta šāda kļūda:</span><span class="sxs-lookup"><span data-stu-id="92533-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="92533-166">Nevar izveidot ierakstu apstiprinātā piegādātāja sarakstā (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="92533-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="92533-167">Vērtībai “Termiņa beigas” ir jābūt lielākai vai vienādai ar vērtību “Spēkā esošs”.</span><span class="sxs-lookup"><span data-stu-id="92533-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="92533-168">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="92533-168">Issue resolution</span></span>

<span data-ttu-id="92533-169">Varat pagarināt tikai periodu, kurā piegādātājs ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="92533-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="92533-170">Ir spēkā šādi nosacījumi:</span><span class="sxs-lookup"><span data-stu-id="92533-170">The following rules apply:</span></span>

- <span data-ttu-id="92533-171">Lai mainītu spēkā stāšanās datumu tā, ka tas ir agrāks par krājuma kreditora esošajiem ierakstiem (periodiem), jaunā perioda beigu datumam ir jābūt pirms visu esošo ierakstu beigu datumiem.</span><span class="sxs-lookup"><span data-stu-id="92533-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="92533-172">Lai mainītu beigu datumu tā, lai tas būtu vēlāks par jebkuru no esošajiem periodiem, spēkā stāšanās datumam jābūt pēc vēlākā beigu datuma jebkurā esošajā ierakstā.</span><span class="sxs-lookup"><span data-stu-id="92533-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="92533-173">Lai samazinātu kopējo periodu, kurā kreditors ir apstiprināts, ir jādzēš vai jāmodificē esošie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="92533-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="92533-174">Vai arī importēšanas laikā varat izmantot slēdzi **Saīsināt**.</span><span class="sxs-lookup"><span data-stu-id="92533-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="92533-175">Šis slēdzis dzēš visus esošos ierakstus tabulā apstiprinātajiem piegādātājiem pēc krājuma.</span><span class="sxs-lookup"><span data-stu-id="92533-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="92533-176">Piemēra scenārijam, kas ir aprakstīts problēmas aprakstā, kur ierakstam ir spēkā stāšanās datums *01/11/2018* un beigu datums *Nekad*, jūs varat importēt jaunu ierakstu, kam ir spēkā stāšanās datums *01/10/2018* un beigu datums *Nekad*.</span><span class="sxs-lookup"><span data-stu-id="92533-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="92533-177">Tomēr jūs nevarat samazināt periodu tā, lai spēkā stāšanās datums tiktu atjaunināts uz *01/12/2018*, izmantojot datu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="92533-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="92533-178">Šīs izmaiņas jāveic, izmantojot lietotāja interfeisu.</span><span class="sxs-lookup"><span data-stu-id="92533-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a><span data-ttu-id="92533-179">Pēc piegādes adreses maiņas pirkšanas pasūtījuma galvenē piegādes nosaukums netiek sinhronizēts.</span><span class="sxs-lookup"><span data-stu-id="92533-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="92533-180">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="92533-180">Issue description</span></span>

<span data-ttu-id="92533-181">Pirkšanas pasūtījuma galvenē norādītā adrese tiek atjaunināta uz adresi, kas nav piegādes adrese.</span><span class="sxs-lookup"><span data-stu-id="92533-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="92533-182">Lai gan adrese tiek atjaunināta pirkšanas pasūtījumā, piegādes nosaukums netiek atjaunināts, pamatojoties uz atjaunināto adresi.</span><span class="sxs-lookup"><span data-stu-id="92533-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="92533-183">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="92533-183">Issue resolution</span></span>

<span data-ttu-id="92533-184">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="92533-184">This behavior is by design.</span></span> <span data-ttu-id="92533-185">Atlasītā adrese ir jāklasificē kā piegādes adrese.</span><span class="sxs-lookup"><span data-stu-id="92533-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="92533-186">Pretējā gadījumā piegādes nosaukums netiek atjaunināts, pamatojoties uz atlasīto adresi.</span><span class="sxs-lookup"><span data-stu-id="92533-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="92533-187">Vai ir iespējams atrast lietotāju, kurš atcēla pirkšanas pasūtījumu?</span><span class="sxs-lookup"><span data-stu-id="92533-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="92533-188">Šī informācija tiek izsekota tikai tad, ja pirkšanas pasūtījums ir pakļauts izmaiņu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="92533-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="92533-189">Ja izmantojat izmaiņu pārvaldību, jūs varat redzēt, kurš iesniedzis izmaiņas (atcelšanu) un kurš tās apstiprinājis.</span><span class="sxs-lookup"><span data-stu-id="92533-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
