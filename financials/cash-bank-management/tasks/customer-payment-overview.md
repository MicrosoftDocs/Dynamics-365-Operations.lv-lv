--- 
title: "Debitoru maksājumu pārskats"
description: "Šis uzdevumu ceļvedis palīdzēs izprast dažādas metodes, kuras izmanto, lai ievadītu debitora maksājumus."
author: kweekley
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e6e10d0d0a05b0594ba5cf6a77f474b461bd9dca
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="customer-payment-overview"></a><span data-ttu-id="32738-103">Debitoru maksājumu pārskats</span><span class="sxs-lookup"><span data-stu-id="32738-103">Customer payment overview</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32738-104">Šis uzdevumu ceļvedis palīdzēs izprast dažādas metodes, kuras izmanto, lai ievadītu debitora maksājumus.</span><span class="sxs-lookup"><span data-stu-id="32738-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="32738-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="32738-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="32738-106">Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="32738-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="32738-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="32738-107">Click New.</span></span>
3. <span data-ttu-id="32738-108">Atlasiet maksājumu žurnālu, kurā tiks saglabāti debitoru maksājumi.</span><span class="sxs-lookup"><span data-stu-id="32738-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="32738-109">Atlasiet žurnālu vai ievadiet to manuāli.</span><span class="sxs-lookup"><span data-stu-id="32738-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="32738-110">Noklikšķiniet uz Ievadīt debitora maksājumus.</span><span class="sxs-lookup"><span data-stu-id="32738-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="32738-111">Lauks Ievadīt debitora maksājumus tiek izmantots, lai vienā reizē ierakstītu vienu debitoru maksājumu.</span><span class="sxs-lookup"><span data-stu-id="32738-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="32738-112">Informāciju par maksājumu ievadiet augšpusē un pēc tam atzīmējiet rēķinus, kas visi vienā lapā ar maksājumu tiek nomaksāti.</span><span class="sxs-lookup"><span data-stu-id="32738-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="32738-113">Ievadiet debitoru, no kura saņēmāt maksājumu.</span><span class="sxs-lookup"><span data-stu-id="32738-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="32738-114">Ja nezināt debitoru, bet zināt apmaksāto transakciju, lai ievadītu maksājumu, var izmantot lauku Transakcija.</span><span class="sxs-lookup"><span data-stu-id="32738-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="32738-115">Ievadiet vai atlasiet rēķinu laukā Transakcija.</span><span class="sxs-lookup"><span data-stu-id="32738-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="32738-116">Kad atlasīsiet transakciju, debitors automātiski parādīsies pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="32738-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="32738-117">Laukā Maksājuma atsauce ievadiet maksājuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="32738-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="32738-118">Maksājuma atsauce var būt debitora čeka numurs vai atsauce no klienta elektroniskā maksājuma.</span><span class="sxs-lookup"><span data-stu-id="32738-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="32738-119">Maksājuma atsauce ir nepieciešama tikai tad, ja atzīmējat maksājumu iekļaušanai depozīta kvītī.</span><span class="sxs-lookup"><span data-stu-id="32738-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="32738-120">Atlasiet, vai maksājums tiks iekļauts depozīta kvītī.</span><span class="sxs-lookup"><span data-stu-id="32738-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="32738-121">Ievadiet debitora maksājuma summu.</span><span class="sxs-lookup"><span data-stu-id="32738-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="32738-122">Maksājuma summa pēc noklusējuma neparādīsies.</span><span class="sxs-lookup"><span data-stu-id="32738-122">The payment amount will not default.</span></span> <span data-ttu-id="32738-123">Tā jāievada manuāli.</span><span class="sxs-lookup"><span data-stu-id="32738-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="32738-124">Atzīmējiet rēķinus, kurus apmaksāja debitors.</span><span class="sxs-lookup"><span data-stu-id="32738-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="32738-125">Ja maksājums ir priekšapmaksa, jums nav nepieciešams atzīmēt rēķinus nosegšanai.</span><span class="sxs-lookup"><span data-stu-id="32738-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="32738-126">Maksājumu joprojām var saglabāt un iegrāmatot.</span><span class="sxs-lookup"><span data-stu-id="32738-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="32738-127">Rēķina segšana var notikt vēlāk.</span><span class="sxs-lookup"><span data-stu-id="32738-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="32738-128">Ievadiet maksājuma summu, kura jāsedz atzīmētajam rēķinam.</span><span class="sxs-lookup"><span data-stu-id="32738-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="32738-129">Šo lauku var izmantot, kad maksājums ir daļējs maksājums.</span><span class="sxs-lookup"><span data-stu-id="32738-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="32738-130">Ja neievadāt summu, nosedzamā summa tiks noteikta automātiski.</span><span class="sxs-lookup"><span data-stu-id="32738-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="32738-131">Noklikšķiniet uz Saglabāt žurnālā.</span><span class="sxs-lookup"><span data-stu-id="32738-131">Click Save in journal.</span></span>
    * <span data-ttu-id="32738-132">Pirms saglabājat maksājumu žurnālā, pārliecinieties, vai ir definēts korespondējošais konts.</span><span class="sxs-lookup"><span data-stu-id="32738-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="32738-133">Izmantojot funkciju Saglabāt žurnālā, maksājums tiks saglabāts un pārvietots uz žurnālu.</span><span class="sxs-lookup"><span data-stu-id="32738-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="32738-134">Pēc tam var turpināt ievadīt nākamo maksājumu.</span><span class="sxs-lookup"><span data-stu-id="32738-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="32738-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="32738-135">Close the page.</span></span>
14. <span data-ttu-id="32738-136">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="32738-136">Click Lines.</span></span>
    * <span data-ttu-id="32738-137">Atverot Rindas, ieraudzīsiet visus maksājumus, kas ierakstīti lapā Ievadīt debitora maksājumus un saglabāti žurnālā.</span><span class="sxs-lookup"><span data-stu-id="32738-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="32738-138">Šo lapu var arī izmantot, lai ievadītu jaunos debitoru maksājumus vai rediģēt esošos debitora maksājumus pirms to grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="32738-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="32738-139">Noklikšķiniet uz Jauns, lai izveidotu citu maksājumu.</span><span class="sxs-lookup"><span data-stu-id="32738-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="32738-140">Atlasiet debitoru, no kura saņēmāt maksājumu.</span><span class="sxs-lookup"><span data-stu-id="32738-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="32738-141">Ja nezināt debitoru, bet zināt ar maksājumu apmaksāto rēķinu, izmantojiet lauku Rēķins, lai manuāli ievadītu vai atlasītu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="32738-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="32738-142">Debitors parādīsies pēc noklusējuma, kad tiks atlasīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="32738-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="32738-143">Noklikšķiniet uz Transakciju nosegšana, lai atzīmētu apmaksātos rēķinus.</span><span class="sxs-lookup"><span data-stu-id="32738-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="32738-144">Jums nav nepieciešams segt rēķinu maksājumus.</span><span class="sxs-lookup"><span data-stu-id="32738-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="32738-145">Ja tā ir priekšapmaksa vai ja nezināt, kāds rēķins tiek apmaksāts, varat ievadīt un iegrāmatot maksājumu.</span><span class="sxs-lookup"><span data-stu-id="32738-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="32738-146">Ar maksājumu var nosegt rēķinu vēlāk.</span><span class="sxs-lookup"><span data-stu-id="32738-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="32738-147">Atzīmējiet rēķinus, kas apmaksāti ar šo maksājumu.</span><span class="sxs-lookup"><span data-stu-id="32738-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="32738-148">Ievadiet maksājuma summu, kura tiks segta šim rēķinam.</span><span class="sxs-lookup"><span data-stu-id="32738-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="32738-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="32738-149">Click OK.</span></span>
21. <span data-ttu-id="32738-150">Laukā Maksājuma atsauce ievadiet maksājuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="32738-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="32738-151">.</span><span class="sxs-lookup"><span data-stu-id="32738-151">.</span></span>
    * <span data-ttu-id="32738-152">Maksājuma atsauce ir nepieciešama tikai tad, ja atzīmējat maksājumu iekļaušanai depozīta kvītī.</span><span class="sxs-lookup"><span data-stu-id="32738-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="32738-153">Iegrāmatojiet debitora maksājumus.</span><span class="sxs-lookup"><span data-stu-id="32738-153">Post the customer payments.</span></span> 


