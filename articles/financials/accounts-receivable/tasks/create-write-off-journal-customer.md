---
title: Debitora norakstīšanas žurnāla izveide
description: Šajā uzdevuma ceļvedī parādīts, kā iestatīt norakstīšanas parametrus un tad norakstīt transakcijas no iekasēšanas lapas, atvērto debitora rēķinu lapas un debitoru lapas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cd576458bab1e4654d21773b581a5b0f726c928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545559"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="7c543-103">Debitora norakstīšanas žurnāla izveide</span><span class="sxs-lookup"><span data-stu-id="7c543-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c543-104">Šajā uzdevuma ceļvedī parādīts, kā iestatīt norakstīšanas parametrus un tad norakstīt transakcijas no iekasēšanas lapas, atvērto debitora rēķinu lapas un debitoru lapas.</span><span class="sxs-lookup"><span data-stu-id="7c543-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="7c543-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="7c543-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="7c543-106">Norakstīšanas parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7c543-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="7c543-107">Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru parametri.</span><span class="sxs-lookup"><span data-stu-id="7c543-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="7c543-108">Noklikšķiniet uz cilnes Iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="7c543-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="7c543-109">Izvērsiet vai sakļaujiet sadaļu Norakstīšana.</span><span class="sxs-lookup"><span data-stu-id="7c543-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="7c543-110">Norakstīšanas žurnāls ir Virsgrāmatas žurnāls, kurā ietvertas visas radītās norakstīšanas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="7c543-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="7c543-111">Katrai norakstīšanai varat pievienot iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="7c543-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="7c543-112">Šo noklusēto vērtību norakstīšanas laikā varat ignorēt.</span><span class="sxs-lookup"><span data-stu-id="7c543-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="7c543-113">Iestatiet vērtību Jā, ja norakstīšanas laikā no sākotnējās transakcijas vēlaties atdalīt PVN.</span><span class="sxs-lookup"><span data-stu-id="7c543-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="7c543-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-114">Close the page.</span></span>
5. <span data-ttu-id="7c543-115">Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="7c543-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="7c543-116">Norakstīšanas konts tiks izmantots par izdevumu kontu vai rezervju korekciju Virsgrāmatas žurnālā</span><span class="sxs-lookup"><span data-stu-id="7c543-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="7c543-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="7c543-118">Debitora bilances norakstīšana veco bilanču lapā</span><span class="sxs-lookup"><span data-stu-id="7c543-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="7c543-119">Pārejiet uz sadaļu Kredīts un iekasēšana > Iekasēšana > Vecas bilances.</span><span class="sxs-lookup"><span data-stu-id="7c543-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="7c543-120">Atzīmējiet tā debitora rindu, kuram vēlaties veikt norakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="7c543-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="7c543-121">Piemēram, atzīmējiet rindu ar Birch Company uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="7c543-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="7c543-122">Darbību rūtī noklikšķiniet uz Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="7c543-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="7c543-123">Noklikšķiniet uz Norakstīt.</span><span class="sxs-lookup"><span data-stu-id="7c543-123">Click Write off.</span></span>
5. <span data-ttu-id="7c543-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7c543-124">Click OK.</span></span>
6. <span data-ttu-id="7c543-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-125">Close the page.</span></span>
7. <span data-ttu-id="7c543-126">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="7c543-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="7c543-127">Atlasiet žurnālu partijas numuru tam žurnālam, kas satur jūsu norakstāmās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="7c543-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="7c543-128">Lai atgrieztu debitora bilanci, tiek izveidota viena rinda.</span><span class="sxs-lookup"><span data-stu-id="7c543-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="7c543-129">Lai norakstīšanu iegrāmatotu norakstīšanas kontā, tiek izveidota viena vai vairākas rindas.</span><span class="sxs-lookup"><span data-stu-id="7c543-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="7c543-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-130">Close the page.</span></span>
10. <span data-ttu-id="7c543-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="7c543-132">Norakstiet transakcijas no iekasēšanas veidlapas.</span><span class="sxs-lookup"><span data-stu-id="7c543-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="7c543-133">Pārejiet uz sadaļu Kredīts un iekasēšana > Iekasēšana > Vecas bilances.</span><span class="sxs-lookup"><span data-stu-id="7c543-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="7c543-134">Atlasiet tā debitora nosaukumu, kuram atbilst transakcijas, kuras vēlaties norakstīt.</span><span class="sxs-lookup"><span data-stu-id="7c543-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="7c543-135">Piemēram, atlasiet Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="7c543-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="7c543-136">Atzīmējiet pirmās transakcijas rindu.</span><span class="sxs-lookup"><span data-stu-id="7c543-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="7c543-137">Atzīmējiet otrās transakcijas rindu.</span><span class="sxs-lookup"><span data-stu-id="7c543-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="7c543-138">Noklikšķiniet uz Norakstīt.</span><span class="sxs-lookup"><span data-stu-id="7c543-138">Click Write off.</span></span>
6. <span data-ttu-id="7c543-139">Laukā Komentārs par iemeslu ierakstiet "Sliktie parādi".</span><span class="sxs-lookup"><span data-stu-id="7c543-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="7c543-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7c543-140">Click OK.</span></span>
8. <span data-ttu-id="7c543-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-141">Close the page.</span></span>
9. <span data-ttu-id="7c543-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-142">Close the page.</span></span>
10. <span data-ttu-id="7c543-143">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="7c543-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="7c543-144">Atlasiet žurnālu partijas numuru tam žurnālam, kas satur jūsu norakstāmās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="7c543-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="7c543-145">Lai atgrieztu debitora bilanci, tiek izveidota viena rinda.</span><span class="sxs-lookup"><span data-stu-id="7c543-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="7c543-146">Lai norakstīšanu iegrāmatotu norakstīšanas kontā, tiek izveidota viena vai vairākas rindas.</span><span class="sxs-lookup"><span data-stu-id="7c543-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="7c543-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-147">Close the page.</span></span>
13. <span data-ttu-id="7c543-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="7c543-149">Rēķina norakstīšana no atvērto debitoru rēķinu lapas</span><span class="sxs-lookup"><span data-stu-id="7c543-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="7c543-150">Pārejiet uz sadaļu Debitori > Rēķini > Atvērtie debitoru rēķini.</span><span class="sxs-lookup"><span data-stu-id="7c543-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="7c543-151">Atzīmējiet rēķina rindu.</span><span class="sxs-lookup"><span data-stu-id="7c543-151">Mark the line for an invoice.</span></span> <span data-ttu-id="7c543-152">Piemēram, atzīmējiet CIV-000667 rindu.</span><span class="sxs-lookup"><span data-stu-id="7c543-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="7c543-153">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="7c543-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="7c543-154">Noklikšķiniet uz Norakstīt.</span><span class="sxs-lookup"><span data-stu-id="7c543-154">Click Write off.</span></span>
5. <span data-ttu-id="7c543-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7c543-155">Click OK.</span></span>
6. <span data-ttu-id="7c543-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="7c543-157">Debitora bilances norakstīšana debitora lapā</span><span class="sxs-lookup"><span data-stu-id="7c543-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="7c543-158">Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="7c543-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="7c543-159">Izvēlieties debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="7c543-159">Select a customer account.</span></span> <span data-ttu-id="7c543-160">Piemēram, atlasiet US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="7c543-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="7c543-161">Darbību rūtī noklikšķiniet uz Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="7c543-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="7c543-162">Noklikšķiniet uz Norakstīt.</span><span class="sxs-lookup"><span data-stu-id="7c543-162">Click Write off.</span></span>
5. <span data-ttu-id="7c543-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7c543-163">Click OK.</span></span>
6. <span data-ttu-id="7c543-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7c543-164">Close the page.</span></span>

