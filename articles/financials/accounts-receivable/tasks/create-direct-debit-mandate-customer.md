--- 
title: "Tiešā debeta pilnvarojuma izveide debitoram"
description: "Šajā uzdevumu ceļvedī parādīts, kā izveidot tiešā debeta pilnvarojumu un izmantot to rēķinā."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 66aa30e88cec914a9cd4d02a0992ff7570d1ced2
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="a4cd2-103">Tiešā debeta pilnvarojuma izveide debitoram</span><span class="sxs-lookup"><span data-stu-id="a4cd2-103">Create a direct debit mandate for a customer</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4cd2-104">Šajā uzdevumu ceļvedī parādīts, kā izveidot tiešā debeta pilnvarojumu un izmantot to rēķinā.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="a4cd2-105">Banku konta izveide</span><span class="sxs-lookup"><span data-stu-id="a4cd2-105">Create a bank account</span></span>
1. <span data-ttu-id="a4cd2-106">Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="a4cd2-107">Piemēram, atlasiet US-001</span><span class="sxs-lookup"><span data-stu-id="a4cd2-107">For example, select US-001</span></span>
3. <span data-ttu-id="a4cd2-108">Darbību rūtī noklikšķiniet uz Debitors.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="a4cd2-109">Noklikšķiniet uz Banku konti.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="a4cd2-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-110">Click New.</span></span>
6. <span data-ttu-id="a4cd2-111">Ierakstiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="a4cd2-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="a4cd2-113">Ievadiet vērtību laukā IBAN.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="a4cd2-114">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="a4cd2-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-115">Click Save.</span></span>
11. <span data-ttu-id="a4cd2-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-116">Close the page.</span></span>
12. <span data-ttu-id="a4cd2-117">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="a4cd2-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a4cd2-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="a4cd2-120">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-120">Click Edit.</span></span>
16. <span data-ttu-id="a4cd2-121">Izvērsiet sadaļu Papildu identifikācija.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="a4cd2-122">Laukā Tiešā debeta ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="a4cd2-123">Ievadiet vērtību laukā IBAN.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="a4cd2-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-124">Close the page.</span></span>
20. <span data-ttu-id="a4cd2-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="a4cd2-126">Elektroniskās maksāšanas metodes definēšana</span><span class="sxs-lookup"><span data-stu-id="a4cd2-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="a4cd2-127">Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="a4cd2-128">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-128">Click New.</span></span>
3. <span data-ttu-id="a4cd2-129">Ierakstiet vērtību laukā Maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="a4cd2-130">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a4cd2-131">Maksājuma tipam tiešā debeta pilnvarojuma maksāšanas metodē ir jābūt Elektroniskais maksājums.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="a4cd2-132">Laukā Pieprasīt pilnvarojumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="a4cd2-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="a4cd2-134">Pievienojiet debitoram tiešā debeta pilnvarojumu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="a4cd2-135">Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="a4cd2-136">Piemēram, atlasiet US-001</span><span class="sxs-lookup"><span data-stu-id="a4cd2-136">For example, select US-001</span></span>
3. <span data-ttu-id="a4cd2-137">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-137">Click Edit.</span></span>
4. <span data-ttu-id="a4cd2-138">Izvērsiet Maksāšanas noklusējuma sadaļu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="a4cd2-139">Laukā Maksājuma metode ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="a4cd2-140">Izvērsiet Maksāšanas noklusējuma sadaļu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="a4cd2-141">Izvērsiet sadaļu Tiešā debeta pilnvarojumi.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="a4cd2-142">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-142">Click Add.</span></span>
9. <span data-ttu-id="a4cd2-143">Ievadiet vai atlasiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="a4cd2-144">Laukā Kreditora bankas konts, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="a4cd2-145">Ievadiet maksājumu skaitu, kuru paredzat apstrādāt šim pilnvarojumam.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="a4cd2-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-146">Click OK.</span></span>
13. <span data-ttu-id="a4cd2-147">Klikšķiniet Drukāt.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-147">Click Print.</span></span>
14. <span data-ttu-id="a4cd2-148">Noklikšķiniet uz Pilnvarojuma pārskats.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-148">Click Mandate report.</span></span>
15. <span data-ttu-id="a4cd2-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-149">Close the page.</span></span>
16. <span data-ttu-id="a4cd2-150">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-150">Click Edit.</span></span>
17. <span data-ttu-id="a4cd2-151">Ievadiet datumu laukā Parakstīšanas datums.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="a4cd2-152">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-152">Click Yes.</span></span>
19. <span data-ttu-id="a4cd2-153">Ievadiet pilnvarojuma parakstīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="a4cd2-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-154">Click OK.</span></span>
21. <span data-ttu-id="a4cd2-155">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="a4cd2-156">Brīvā teksta rēķina izveide ar pilnvarojumu</span><span class="sxs-lookup"><span data-stu-id="a4cd2-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="a4cd2-157">Pārejiet uz sadaļu Debitori > Rēķini > Visi brīva teksta rēķini.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="a4cd2-158">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-158">Click New.</span></span>
3. <span data-ttu-id="a4cd2-159">Atlasiet debitoru, kuram pievienojāt šo pilnvarojumu.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="a4cd2-160">Laukā Tiešā debeta pilnvarojuma ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4cd2-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


