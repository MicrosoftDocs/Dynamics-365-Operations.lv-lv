---
title: Debitoru maksājumu nosacījumu izveide
description: Šī procedūra definē termiņatlaides un apmaksas datuma iestatījumus.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cddccbeb60e3eb9e498affcaa547fddb145a2bb2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846425"
---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="cf211-103">Debitoru maksājumu nosacījumu izveide</span><span class="sxs-lookup"><span data-stu-id="cf211-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf211-104">Šī procedūra definē termiņatlaides un apmaksas datuma iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="cf211-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="cf211-105">Šis uzdevuma ceļvedis izmanto USMF demonstrācijas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="cf211-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="cf211-106">Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Maksāšanas dienas.</span><span class="sxs-lookup"><span data-stu-id="cf211-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="cf211-107">Apmaksas nosacījumu iestatījumi ir kopīgi debitoru parādos un parādos kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="cf211-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="cf211-108">Ja tos definējat modulī, tie būs pieejami arī citā modulī.</span><span class="sxs-lookup"><span data-stu-id="cf211-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="cf211-109">Šajā uzdevumu ceļvedī visi apmaksas nosacījumi izveidoti debitoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="cf211-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="cf211-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cf211-110">Click New.</span></span>
    * <span data-ttu-id="cf211-111">Izveidojiet maksāšanas dienu, ja apmaksas nosacījumos ir prasīta konkrēta nedēļas diena (pirmdiena, otrdiena u.c.) vai konkrēts mēneša datums (5., 10. u.c.).</span><span class="sxs-lookup"><span data-stu-id="cf211-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="cf211-112">Laukā Maksājuma diena ievadiet maksājuma dienas ID.</span><span class="sxs-lookup"><span data-stu-id="cf211-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="cf211-113">Laukā Apraksts ievadiet maksājuma dienas īsu aprakstu.</span><span class="sxs-lookup"><span data-stu-id="cf211-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="cf211-114">Laukā Nedēļa/Mēnesis atlasiet Nedēļa vai Mēnesis.</span><span class="sxs-lookup"><span data-stu-id="cf211-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="cf211-115">Ja vēlaties ievadīt nedēļas dienu, piemēram, pirmdiena, atlasiet Nedēļa.</span><span class="sxs-lookup"><span data-stu-id="cf211-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="cf211-116">Ja vēlaties ievadīt mēneša datumu, piemēram, 10., atlasiet Mēnesis.</span><span class="sxs-lookup"><span data-stu-id="cf211-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="cf211-117">Šim piemēram atlasiet Mēnesis.</span><span class="sxs-lookup"><span data-stu-id="cf211-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="cf211-118">Ievadiet datumu laukā Mēneša diena.</span><span class="sxs-lookup"><span data-stu-id="cf211-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="cf211-119">Datums ir jāievada kā skaitlis, piemēram, "10", nevis "10‑ais".</span><span class="sxs-lookup"><span data-stu-id="cf211-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="cf211-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cf211-120">Click Save.</span></span>
8. <span data-ttu-id="cf211-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cf211-121">Close the page.</span></span>
9. <span data-ttu-id="cf211-122">Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Apmaksas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="cf211-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="cf211-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cf211-123">Click New.</span></span>
    * <span data-ttu-id="cf211-124">Apmaksas noteikumi tiek izmantoti, lai definētu, kā tiks aprēķināti apmaksas termiņi.</span><span class="sxs-lookup"><span data-stu-id="cf211-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="cf211-125">Termiņatlaides datuma iestatīšana ir definēta atsevišķā lapā.</span><span class="sxs-lookup"><span data-stu-id="cf211-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="cf211-126">Laukā Apmaksas nosacījumi ievadiet ID.</span><span class="sxs-lookup"><span data-stu-id="cf211-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="cf211-127">Ievadiet aprakstu laukā Apraksts.</span><span class="sxs-lookup"><span data-stu-id="cf211-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="cf211-128">Atlasiet maksāšanas metodi, piemēram, COD, neto, pašreizējā mēnesī u.c.</span><span class="sxs-lookup"><span data-stu-id="cf211-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="cf211-129">Maksāšanas metode tiek izmantota, lai definētu, kā tiks aprēķināts apmaksas termiņa sākums.</span><span class="sxs-lookup"><span data-stu-id="cf211-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="cf211-130">Piemēram, neto tiek izmantots, ja apmaksas datums vienmēr ir noteikts mēnešu vai dienu skaits pēc rēķina datuma.</span><span class="sxs-lookup"><span data-stu-id="cf211-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="cf211-131">SPB var izmantot, ja maksājums ir nepieciešams, saņemot rēķinu, tāpēc apmaksas datums netiek rēķināts.</span><span class="sxs-lookup"><span data-stu-id="cf211-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="cf211-132">Šim piemēram atlasiet Pašreizējais mēnesis.</span><span class="sxs-lookup"><span data-stu-id="cf211-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="cf211-133">Ja aprēķinā iekļauta noteikta nedēļas diena vai datums, atlasiet maksāšanas dienu.</span><span class="sxs-lookup"><span data-stu-id="cf211-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="cf211-134">Atkarībā no maksāšanas termiņa var ievadīt daudzumu, norādot mēnešu vai dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="cf211-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="cf211-135">Vai var izmantot maksāšanas grafiku vai maksāšanas dienu, kas jāpievieno maksāšanas metodes beigās.</span><span class="sxs-lookup"><span data-stu-id="cf211-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="cf211-136">Ja apmaksas datums vienmēr ir nākamā mēneša 10. datums, atlasiet maksāšanas dienu 10. datumu.</span><span class="sxs-lookup"><span data-stu-id="cf211-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="cf211-137">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cf211-137">Click Save.</span></span>
16. <span data-ttu-id="cf211-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cf211-138">Close the page.</span></span>
17. <span data-ttu-id="cf211-139">Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Termiņatlaides.</span><span class="sxs-lookup"><span data-stu-id="cf211-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="cf211-140">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cf211-140">Click New.</span></span>
    * <span data-ttu-id="cf211-141">Šajā lapā tiek definēts, kā tiks aprēķināts termiņatlaides datums.</span><span class="sxs-lookup"><span data-stu-id="cf211-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="cf211-142">Laukā Termiņatlaide ievadiet ID.</span><span class="sxs-lookup"><span data-stu-id="cf211-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="cf211-143">Ievadiet aprakstu laukā Apraksts.</span><span class="sxs-lookup"><span data-stu-id="cf211-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="cf211-144">Ja ir pieejama pa pakāpēm sadalīta termiņatlaide, atlasiet nākamo atlaižu kodu, kas ir attiecināms pēc šīs jaunās termiņatlaides.</span><span class="sxs-lookup"><span data-stu-id="cf211-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="cf211-145">Ievadiet dienu skaitu, kas tiek aprēķināts termiņatlaides datumu.</span><span class="sxs-lookup"><span data-stu-id="cf211-145">Enter the number of days used to calculate the cash dicount date.</span></span>
    * <span data-ttu-id="cf211-146">Ja ir atlasīts neto princips, termiņatlaides datuma aprēķināšanai rēķina datumam tiks pieskaitīts noteikts dienu skaits.</span><span class="sxs-lookup"><span data-stu-id="cf211-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="cf211-147">Ievadiet termiņatlaides procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="cf211-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="cf211-148">Ievadiet galveno kontu, kurā jāgrāmato debitoru rēķinu termiņatlaide.</span><span class="sxs-lookup"><span data-stu-id="cf211-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="cf211-149">Atlasiet opciju laukā Atlaides korespondējošie konti.</span><span class="sxs-lookup"><span data-stu-id="cf211-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="cf211-150">Atlasot Konti rēķina rindās, termiņatlaide tiks iegrāmatota tajā pašā līdzekļu/izdevumu galvenajā kontā, kurā kreditora rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="cf211-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="cf211-151">Atlasot Kreditoru rēķiniem izmantot galveno kontu, termiņatlaide tiks iegrāmatota galvenajā kontā, kurš definēts laukā Kreditoru rēķinu galvenais konts.</span><span class="sxs-lookup"><span data-stu-id="cf211-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="cf211-152">Šim piemēram izvēlieties Kreditoru rēķiniem izmantot galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="cf211-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="cf211-153">Ievadiet galveno kontu, kurā jāgrāmato kreditoru rēķinu termiņatlaide.</span><span class="sxs-lookup"><span data-stu-id="cf211-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="cf211-154">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cf211-154">Click Save.</span></span>

