---
title: "Kredītkartes iestatīšana, autorizācija un nolasīšana"
description: "Šajā rakstā ir sniegts pārskats par kredītkartes autorizāciju programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise. Šeit ir iekļauta arī informācija par to, kā iestatīt maksājumu pakalpojumu, pievienot kredītkarti pārdošanas pasūtījumam un anulēt autorizāciju."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dad3964003d0be0c22b0346aba2b3319278ffaa9
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="a321f-104">Kredītkartes iestatīšana, autorizācija un nolasīšana</span><span class="sxs-lookup"><span data-stu-id="a321f-104">Credit card setup, authorization, and capture</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="a321f-105">Šajā rakstā ir sniegts pārskats par kredītkartes autorizāciju programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise.</span><span class="sxs-lookup"><span data-stu-id="a321f-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="a321f-106">Šeit ir iekļauta arī informācija par to, kā iestatīt maksājumu pakalpojumu, pievienot kredītkarti pārdošanas pasūtījumam un anulēt autorizāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="a321f-107">Kredītkartes maksājumu pakalpojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a321f-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="a321f-108">Lai izmantotu kredītkartes, ir jāiestata un jāaktivizē maksājumu pakalpojums lapā Maksājumu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="a321f-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="a321f-109">Maksājumu pakalpojums nodrošina starpniecību starp jūsu juridisko personu un banku, kas apstrādā debitora maksājumus ar kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="a321f-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="a321f-110">Jums ir jāsadarbojas ar kredītkartes nodrošinātāju, kas ir norādīts laukā Maksājumu savienotājs, un jāiestata šī nodrošinātāja konts.</span><span class="sxs-lookup"><span data-stu-id="a321f-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="a321f-111">Pēc tam jums ir jāiesta citas opcijas lapā Maksājumu pakalpojumi, jāiestata kredītkaršu veidi American Express, Discover, MasterCard un Discover lapā Kredītkaršu veidi un jāaktivizē maksājuma nodrošinātājs kā noklusējuma nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="a321f-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="a321f-112">Lai pabeigtu iestatīšanu, ir jāveic arī tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a321f-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="a321f-113">Lapā Debitoru parādu parametri norādiet kredītkaršu autorizācijas izmantošanas parametrus.</span><span class="sxs-lookup"><span data-stu-id="a321f-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="a321f-114">Lapā Apmaksas nosacījumi iestatiet kredītkaršu maksājumu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="a321f-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="a321f-115">Laukā Maksājuma veids atlasiet opciju Kredītkarte.</span><span class="sxs-lookup"><span data-stu-id="a321f-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="a321f-116">Lapā Debitora kredītkartes ievadiet debitoru kredītkaršu informāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="a321f-117">Jaunas kredītkartes pievienošana</span><span class="sxs-lookup"><span data-stu-id="a321f-117">Adding a new credit card</span></span>
<span data-ttu-id="a321f-118">Varat izveidot jaunus kredītkaršu ierakstus lapā Debitori izmantojot opcijas Debitors, Iestatīt, Kredītkarte.</span><span class="sxs-lookup"><span data-stu-id="a321f-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="a321f-119">Varat arī izveidot kredītkaršu ierakstus, kad ievadāt pārdošanas pasūtījumus lapā Pārdošanas pasūtījums, izmantojot opcijas Pārvaldīt, Debitors, Kredītkarte, Reģistrēt.</span><span class="sxs-lookup"><span data-stu-id="a321f-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>
<span data-ttu-id="a321f-120">Kredītkartes pievienošana pārdošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="a321f-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="a321f-121">Varat pievienot kredītkarti pārdošanas pasūtījumam, atlasot kredītkarti kredītkartes uzmeklēšanas laukā lapas Pārdošanas pasūtījums kopsavilkuma cilnē Debitora kredītkartes.</span><span class="sxs-lookup"><span data-stu-id="a321f-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="a321f-122">Lai sāktu autorizācijas procesu, cilnes Pārvaldīt darbību rūtī atlasiet opcijas Kredītkarte un Autorizēt.</span><span class="sxs-lookup"><span data-stu-id="a321f-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>
<span data-ttu-id="a321f-123">Kredītkartes autorizācija</span><span class="sxs-lookup"><span data-stu-id="a321f-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="a321f-124">Autorizējot kredītkarti, tiek pārbaudīts kartes numurs un kartes īpašnieka vārds un tiek apstiprināta pieejamā kredīta bilance.</span><span class="sxs-lookup"><span data-stu-id="a321f-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="a321f-125">Pēc izvēles tiek pārbaudīta kartes verificēšanas vērtība un kartes īpašnieka adrese.</span><span class="sxs-lookup"><span data-stu-id="a321f-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="a321f-126">Pēc tam debitora pieejamā kredīta bilance tiek samazināta par rēķina summu.</span><span class="sxs-lookup"><span data-stu-id="a321f-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="a321f-127">Maksājumu pakalpojums nosūta informāciju par to, ka kredītkarte ir apstiprināta vai noraidīta.</span><span class="sxs-lookup"><span data-stu-id="a321f-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="a321f-128">Kad pārdošanas pasūtījums tiek iekļauts rēķinā, no kredītkartes konta tiek iekasēta (nolasīta) rēķina summa.</span><span class="sxs-lookup"><span data-stu-id="a321f-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="a321f-129">Kartes verificēšanas vērtība</span><span class="sxs-lookup"><span data-stu-id="a321f-129">Card verification value</span></span>

<span data-ttu-id="a321f-130">Varat pieprasīt kartes verificēšanas vērtību, kas dažreiz tiek saukta par kartes drošības kodu.</span><span class="sxs-lookup"><span data-stu-id="a321f-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="a321f-131">American Express kartei tā ir četrciparu vērtība.</span><span class="sxs-lookup"><span data-stu-id="a321f-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="a321f-132">Discover, MasterCard un Visa kartēm tā ir trīsciparu vērtība.</span><span class="sxs-lookup"><span data-stu-id="a321f-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="a321f-133">Adreses pārbaude</span><span class="sxs-lookup"><span data-stu-id="a321f-133">Address verification</span></span>

<span data-ttu-id="a321f-134">Maksājuma nodrošinātājam vienmēr tiek nosūtīta adreses pārbaudes informācija.</span><span class="sxs-lookup"><span data-stu-id="a321f-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="a321f-135">Varat izlemt, cik daudz informācijas ir nepieciešams, lai transakciju pieņemtu.</span><span class="sxs-lookup"><span data-stu-id="a321f-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="a321f-136">Noteikti sazinieties ar savu nodrošinātāju, lai noteiktu, vai tas pieņem šo informāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="a321f-137">Tālāk ir norādītas adreses pārbaudes opcijas.</span><span class="sxs-lookup"><span data-stu-id="a321f-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="a321f-138">**Vienmēr pieņemt transakciju** — pieņemt transakciju neatkarīgi no adreses pārbaudes rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="a321f-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="a321f-139">**Konta īpašnieks** — salīdzināt transakcijā norādīto kartes īpašnieka vārdu ar kredītkartes nodrošinātājam pieejamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="a321f-140">**Rēķina adrese** — salīdzināt transakcijā norādīto kartes īpašnieka vārdu un rēķina adresi ar kredītkartes nodrošinātājam pieejamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="a321f-141">**Rēķina pasta kods** — salīdzināt transakcijā norādīto kartes īpašnieka vārdu, rēķina adresi un pasta indeksu ar kredītkartes nodrošinātājam pieejamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="a321f-142">Datu atbalsts</span><span class="sxs-lookup"><span data-stu-id="a321f-142">Data support</span></span>
<span data-ttu-id="a321f-143">Katram atbalstītajam kredītkartes veidam varat norādīt datu atbalsta līmeni.</span><span class="sxs-lookup"><span data-stu-id="a321f-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="a321f-144">Izmantojot šo līmeni, tiek kontrolēts, cik daudz informācijas par transakciju tiek pārsūtīts uz maksājumu pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="a321f-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="a321f-145">Noteikti sazinieties ar savu maksājumu nodrošinātāju, lai noteiktu, vai nodrošinātājs var sniegt šo informāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="a321f-146">Tālāk ir norādītas datu atbalsta līmeņa opcijas.</span><span class="sxs-lookup"><span data-stu-id="a321f-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="a321f-147">**1. līmenis** — pārsūtīt transakcijas datumu, transakcijas summu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="a321f-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="a321f-148">**2. līmenis** — pārsūtīt visu 1. līmeņa informāciju, kā arī piegādes un tirgotāja adreses un nodokļu informāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="a321f-149">**3. līmenis** — pārsūtīt visu 2. līmeņa informāciju, kā arī pasūtījuma rindas informāciju.</span><span class="sxs-lookup"><span data-stu-id="a321f-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="a321f-150">Daļēji maksājumi</span><span class="sxs-lookup"><span data-stu-id="a321f-150">Partial payments</span></span>
<span data-ttu-id="a321f-151">Ja nosūtāt daļu pasūtījuma, tiek nolasīta daļējā pasūtījuma summa un tiek slēgta autorizācija, kas attiecas uz visa pasūtījuma summu.</span><span class="sxs-lookup"><span data-stu-id="a321f-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="a321f-152">Pēc tam tiek iesniegta jauna autorizācija, kas attiecas uz atlikušo nenosūtītas pasūtījuma daļas summu.</span><span class="sxs-lookup"><span data-stu-id="a321f-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="a321f-153">Autorizācijas anulēšana</span><span class="sxs-lookup"><span data-stu-id="a321f-153">Voiding an authorization</span></span>
<span data-ttu-id="a321f-154">Lai anulētu kredītkartes autorizāciju, varat mainīt maksājuma metodi, izvēloties citu metodi, kuras vieds nav Kredītkarte.</span><span class="sxs-lookup"><span data-stu-id="a321f-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>






