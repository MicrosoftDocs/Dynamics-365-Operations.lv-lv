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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44f36a12195a57e1b4cea524d2e4881f1fa7d0e9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842933"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="d4838-103">Debitora norakstīšanas žurnāla izveide</span><span class="sxs-lookup"><span data-stu-id="d4838-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4838-104">Šajā uzdevuma ceļvedī parādīts, kā iestatīt norakstīšanas parametrus un tad norakstīt transakcijas no iekasēšanas lapas, atvērto debitora rēķinu lapas un debitoru lapas.</span><span class="sxs-lookup"><span data-stu-id="d4838-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="d4838-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="d4838-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="d4838-106">Norakstīšanas parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4838-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="d4838-107">Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru parametri.</span><span class="sxs-lookup"><span data-stu-id="d4838-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="d4838-108">Noklikšķiniet uz cilnes Iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="d4838-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="d4838-109">Izvērsiet vai sakļaujiet sadaļu Norakstīšana.</span><span class="sxs-lookup"><span data-stu-id="d4838-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="d4838-110">Norakstīšanas žurnāls ir Virsgrāmatas žurnāls, kurā ietvertas visas radītās norakstīšanas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="d4838-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="d4838-111">Katrai norakstīšanai varat pievienot iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="d4838-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="d4838-112">Šo noklusēto vērtību norakstīšanas laikā varat ignorēt.</span><span class="sxs-lookup"><span data-stu-id="d4838-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="d4838-113">Iestatiet vērtību Jā, ja norakstīšanas laikā no sākotnējās transakcijas vēlaties atdalīt PVN.</span><span class="sxs-lookup"><span data-stu-id="d4838-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="d4838-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-114">Close the page.</span></span>
5. <span data-ttu-id="d4838-115">Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="d4838-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="d4838-116">Norakstīšanas konts tiks izmantots par izdevumu kontu vai rezervju korekciju Virsgrāmatas žurnālā</span><span class="sxs-lookup"><span data-stu-id="d4838-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="d4838-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="d4838-118">Debitora bilances norakstīšana veco bilanču lapā</span><span class="sxs-lookup"><span data-stu-id="d4838-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="d4838-119">Pārejiet uz sadaļu Kredīts un iekasēšana > Iekasēšana > Vecas bilances.</span><span class="sxs-lookup"><span data-stu-id="d4838-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="d4838-120">Atzīmējiet tā debitora rindu, kuram vēlaties veikt norakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="d4838-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="d4838-121">Piemēram, atzīmējiet rindu ar Birch Company uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="d4838-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="d4838-122">Darbību rūtī noklikšķiniet uz Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="d4838-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="d4838-123">Noklikšķiniet uz Norakstīt.</span><span class="sxs-lookup"><span data-stu-id="d4838-123">Click Write off.</span></span>
5. <span data-ttu-id="d4838-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4838-124">Click OK.</span></span>
6. <span data-ttu-id="d4838-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-125">Close the page.</span></span>
7. <span data-ttu-id="d4838-126">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="d4838-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="d4838-127">Atlasiet žurnālu partijas numuru tam žurnālam, kas satur jūsu norakstāmās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="d4838-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="d4838-128">Lai atgrieztu debitora bilanci, tiek izveidota viena rinda.</span><span class="sxs-lookup"><span data-stu-id="d4838-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="d4838-129">Lai norakstīšanu iegrāmatotu norakstīšanas kontā, tiek izveidota viena vai vairākas rindas.</span><span class="sxs-lookup"><span data-stu-id="d4838-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="d4838-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-130">Close the page.</span></span>
10. <span data-ttu-id="d4838-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="d4838-132">Norakstiet transakcijas no iekasēšanas veidlapas.</span><span class="sxs-lookup"><span data-stu-id="d4838-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="d4838-133">Pārejiet uz sadaļu Kredīts un iekasēšana > Iekasēšana > Vecas bilances.</span><span class="sxs-lookup"><span data-stu-id="d4838-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="d4838-134">Atlasiet tā debitora nosaukumu, kuram atbilst transakcijas, kuras vēlaties norakstīt.</span><span class="sxs-lookup"><span data-stu-id="d4838-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="d4838-135">Piemēram, atlasiet Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="d4838-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="d4838-136">Atzīmējiet pirmās transakcijas rindu.</span><span class="sxs-lookup"><span data-stu-id="d4838-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="d4838-137">Atzīmējiet otrās transakcijas rindu.</span><span class="sxs-lookup"><span data-stu-id="d4838-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="d4838-138">Noklikšķiniet uz Norakstīt.</span><span class="sxs-lookup"><span data-stu-id="d4838-138">Click Write off.</span></span>
6. <span data-ttu-id="d4838-139">Laukā Komentārs par iemeslu ierakstiet "Sliktie parādi".</span><span class="sxs-lookup"><span data-stu-id="d4838-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="d4838-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4838-140">Click OK.</span></span>
8. <span data-ttu-id="d4838-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-141">Close the page.</span></span>
9. <span data-ttu-id="d4838-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-142">Close the page.</span></span>
10. <span data-ttu-id="d4838-143">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="d4838-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="d4838-144">Atlasiet žurnālu partijas numuru tam žurnālam, kas satur jūsu norakstāmās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="d4838-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="d4838-145">Lai atgrieztu debitora bilanci, tiek izveidota viena rinda.</span><span class="sxs-lookup"><span data-stu-id="d4838-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="d4838-146">Lai norakstīšanu iegrāmatotu norakstīšanas kontā, tiek izveidota viena vai vairākas rindas.</span><span class="sxs-lookup"><span data-stu-id="d4838-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="d4838-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-147">Close the page.</span></span>
13. <span data-ttu-id="d4838-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="d4838-149">Rēķina norakstīšana no atvērto debitoru rēķinu lapas</span><span class="sxs-lookup"><span data-stu-id="d4838-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="d4838-150">Pārejiet uz sadaļu Debitori > Rēķini > Atvērtie debitoru rēķini.</span><span class="sxs-lookup"><span data-stu-id="d4838-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="d4838-151">Atzīmējiet rēķina rindu.</span><span class="sxs-lookup"><span data-stu-id="d4838-151">Mark the line for an invoice.</span></span> <span data-ttu-id="d4838-152">Piemēram, atzīmējiet CIV-000667 rindu.</span><span class="sxs-lookup"><span data-stu-id="d4838-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="d4838-153">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="d4838-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="d4838-154">Noklikšķiniet uz Norakstīt.</span><span class="sxs-lookup"><span data-stu-id="d4838-154">Click Write off.</span></span>
5. <span data-ttu-id="d4838-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4838-155">Click OK.</span></span>
6. <span data-ttu-id="d4838-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="d4838-157">Debitora bilances norakstīšana debitora lapā</span><span class="sxs-lookup"><span data-stu-id="d4838-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="d4838-158">Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="d4838-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d4838-159">Izvēlieties debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="d4838-159">Select a customer account.</span></span> <span data-ttu-id="d4838-160">Piemēram, atlasiet US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="d4838-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="d4838-161">Darbību rūtī noklikšķiniet uz Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="d4838-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="d4838-162">Noklikšķiniet uz Norakstīt.</span><span class="sxs-lookup"><span data-stu-id="d4838-162">Click Write off.</span></span>
5. <span data-ttu-id="d4838-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4838-163">Click OK.</span></span>
6. <span data-ttu-id="d4838-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4838-164">Close the page.</span></span>

