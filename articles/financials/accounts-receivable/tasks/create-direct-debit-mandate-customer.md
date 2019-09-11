---
title: Tiešā debeta pilnvarojuma izveide debitoram
description: Šajā uzdevumu ceļvedī parādīts, kā izveidot tiešā debeta pilnvarojumu un izmantot to rēķinā.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916373"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="c4285-103">Tiešā debeta pilnvarojuma izveide debitoram</span><span class="sxs-lookup"><span data-stu-id="c4285-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4285-104">Šajā uzdevumu ceļvedī parādīts, kā izveidot tiešā debeta pilnvarojumu un izmantot to rēķinā.</span><span class="sxs-lookup"><span data-stu-id="c4285-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="c4285-105">Banku konta izveide</span><span class="sxs-lookup"><span data-stu-id="c4285-105">Create a bank account</span></span>
1. <span data-ttu-id="c4285-106">**Navigācijas rūtī** ejiet uz sadaļu **Moduļi > Debitori > Klienti > Visi klienti**.</span><span class="sxs-lookup"><span data-stu-id="c4285-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="c4285-107">Sarakstā atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c4285-107">In the list, select a record.</span></span> <span data-ttu-id="c4285-108">Piemēram, atlasiet US-001</span><span class="sxs-lookup"><span data-stu-id="c4285-108">For example, select US-001</span></span>
3. <span data-ttu-id="c4285-109">Darbību rūtī noklikšķiniet uz **Klients**.</span><span class="sxs-lookup"><span data-stu-id="c4285-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="c4285-110">Noklikšķiniet uz **Bankas konti**.</span><span class="sxs-lookup"><span data-stu-id="c4285-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="c4285-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c4285-111">Click **New**.</span></span>
6. <span data-ttu-id="c4285-112">Laukā **Bankas konts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4285-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="c4285-113">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4285-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="c4285-114">Laukā **IBAN** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4285-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="c4285-115">Laukā **Valūta** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4285-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="c4285-116">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c4285-116">Click **Save**.</span></span>
11. <span data-ttu-id="c4285-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4285-117">Close the page.</span></span>
12. <span data-ttu-id="c4285-118">**Navigācijas rūtī** pārejiet uz **Moduļi > Naudas un bankas pārvaldība > Bankas konti > Bankas konti**.</span><span class="sxs-lookup"><span data-stu-id="c4285-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="c4285-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c4285-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c4285-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c4285-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="c4285-121">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c4285-121">Click **Edit**.</span></span>
16. <span data-ttu-id="c4285-122">Izvērsiet kopsavilkuma cilni **Papildu identifikācija**.</span><span class="sxs-lookup"><span data-stu-id="c4285-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="c4285-123">Laukā **Tiešā debeta ID** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4285-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="c4285-124">Laukā **IBAN** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4285-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="c4285-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4285-125">Close the page.</span></span>
20. <span data-ttu-id="c4285-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4285-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="c4285-127">Elektroniskās maksāšanas metodes definēšana</span><span class="sxs-lookup"><span data-stu-id="c4285-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="c4285-128">**Navigācijas rūtī** pārejiet uz **Moduļi > Debitori > Maksājumu iestatīšana > Maksāšanas veidi**.</span><span class="sxs-lookup"><span data-stu-id="c4285-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="c4285-129">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c4285-129">Click **New**.</span></span>
3. <span data-ttu-id="c4285-130">Laukā **Maksāšanas veids** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4285-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="c4285-131">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4285-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c4285-132">Laukā **Maksājuma veids** ievadiet „Elektroniskais maksājums”.</span><span class="sxs-lookup"><span data-stu-id="c4285-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="c4285-133">Maksājuma tipam tiešā debeta pilnvarojuma maksāšanas metodē ir jābūt Elektroniskais maksājums.</span><span class="sxs-lookup"><span data-stu-id="c4285-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="c4285-134">Atlasiet „Jā” laukā **Prasīt pilnvarojumu**.</span><span class="sxs-lookup"><span data-stu-id="c4285-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="c4285-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4285-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="c4285-136">Pievienojiet debitoram tiešā debeta pilnvarojumu.</span><span class="sxs-lookup"><span data-stu-id="c4285-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="c4285-137">**Navigācijas rūtī** ejiet uz sadaļu **Moduļi > Debitori > Klienti > Visi klienti**.</span><span class="sxs-lookup"><span data-stu-id="c4285-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="c4285-138">Sarakstā atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c4285-138">In the list, select a record.</span></span> <span data-ttu-id="c4285-139">Piemēram, atlasiet US-001</span><span class="sxs-lookup"><span data-stu-id="c4285-139">For example, select US-001</span></span>
3. <span data-ttu-id="c4285-140">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c4285-140">Click **Edit**.</span></span>
4. <span data-ttu-id="c4285-141">Izvērsiet kopsavilkuma cilni **Maksājumu kavējumi**.</span><span class="sxs-lookup"><span data-stu-id="c4285-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="c4285-142">Ievadiet vai atlasiet vērtību laukā **Maksājuma metode**.</span><span class="sxs-lookup"><span data-stu-id="c4285-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="c4285-143">Izvērsiet kopsavilkuma cilni **Maksājumu kavējumi**.</span><span class="sxs-lookup"><span data-stu-id="c4285-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="c4285-144">Izvērsiet kopsavilkuma cilni **Tiešā debeta pilnvarojumi**.</span><span class="sxs-lookup"><span data-stu-id="c4285-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="c4285-145">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="c4285-145">Click **Add**.</span></span>
9. <span data-ttu-id="c4285-146">Ievadiet vai atlasiet vērtību laukā **Bankas konts**.</span><span class="sxs-lookup"><span data-stu-id="c4285-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="c4285-147">Ievadiet vai atlasiet vērtību laukā **Kreditora bankas konts**.</span><span class="sxs-lookup"><span data-stu-id="c4285-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="c4285-148">Laukā **Maksājumu biežums** ievadiet maksājumu skaitu, ko paredzat apstrādāt šim pilnvarojumam.</span><span class="sxs-lookup"><span data-stu-id="c4285-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="c4285-149">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c4285-149">Click **OK**.</span></span>
13. <span data-ttu-id="c4285-150">Noklikšķiniet uz **Drukāt**.</span><span class="sxs-lookup"><span data-stu-id="c4285-150">Click **Print**.</span></span>
14. <span data-ttu-id="c4285-151">Noklikšķiniet uz **Pilnvarojuma atskaite**.</span><span class="sxs-lookup"><span data-stu-id="c4285-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="c4285-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4285-152">Close the page.</span></span>
16. <span data-ttu-id="c4285-153">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c4285-153">Click **Edit**.</span></span>
17. <span data-ttu-id="c4285-154">Laukā **Paraksta datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="c4285-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="c4285-155">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c4285-155">Click **Yes**.</span></span>
19. <span data-ttu-id="c4285-156">Ievadiet pilnvarojuma parakstīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="c4285-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="c4285-157">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c4285-157">Click **OK**.</span></span>
21. <span data-ttu-id="c4285-158">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4285-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="c4285-159">Brīvā teksta rēķina izveide ar pilnvarojumu</span><span class="sxs-lookup"><span data-stu-id="c4285-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="c4285-160">**Navigācijas rūtī** ejiet uz **Moduļi > Debitori > Rēķini > Visi brīva teksta rēķini**.</span><span class="sxs-lookup"><span data-stu-id="c4285-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="c4285-161">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c4285-161">Click **New**.</span></span>
3. <span data-ttu-id="c4285-162">Atlasiet debitoru, kuram pievienojāt šo pilnvarojumu.</span><span class="sxs-lookup"><span data-stu-id="c4285-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="c4285-163">Ievadiet vai atlasiet vērtību laukā **Tiešā debeta pilnvarojuma ID**.</span><span class="sxs-lookup"><span data-stu-id="c4285-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

