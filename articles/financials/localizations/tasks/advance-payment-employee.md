--- 
title: "EEU-00047 avansa maksājums darbiniekam"
description: "Šajā procedūrā parādīts, kā iestatīt un reģistrēt darbības avansa turētājam."
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e3c07789bfa0839436caf32e428f3abeecb8f2b7
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="eeu-00047-advance-payment-to-employee"></a><span data-ttu-id="9e797-103">EEU-00047 avansa maksājums darbiniekam</span><span class="sxs-lookup"><span data-stu-id="9e797-103">EEU-00047 Advance payment to employee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e797-104">Šajā procedūrā parādīts, kā iestatīt un reģistrēt darbības avansa turētājam.</span><span class="sxs-lookup"><span data-stu-id="9e797-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="9e797-105">Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Lietuvā.</span><span class="sxs-lookup"><span data-stu-id="9e797-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="9e797-106">Šis uzdevums ir paredzēts tikai juridiskām personām, kuru primārā adrese ir Polijā, Lietuvā, Latvijā, Igaunijā, Čehijā vai Ungārijā.</span><span class="sxs-lookup"><span data-stu-id="9e797-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="9e797-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="9e797-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="9e797-108">Izveidot jaunu kases kontu</span><span class="sxs-lookup"><span data-stu-id="9e797-108">Create a new cash account</span></span>
1. <span data-ttu-id="9e797-109">Dodieties uz Kases un bankas vadība > Bankas konti > Kases konti.</span><span class="sxs-lookup"><span data-stu-id="9e797-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="9e797-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e797-110">Click New.</span></span>
3. <span data-ttu-id="9e797-111">Laukā Kase ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="9e797-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9e797-113">Laukā Numuru sērijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="9e797-114">Izvērsiet sadaļu Apstiprināšana.</span><span class="sxs-lookup"><span data-stu-id="9e797-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="9e797-115">Laukā Valūta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="9e797-116">Atlasiet Jā laukā Negatīvs atlikums kasē.</span><span class="sxs-lookup"><span data-stu-id="9e797-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="9e797-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="9e797-118">Izveidot jaunu žurnālu</span><span class="sxs-lookup"><span data-stu-id="9e797-118">Create a new journal</span></span>
1. <span data-ttu-id="9e797-119">Pārejiet uz sadaļu Virsgrāmata >Žurnāla iestatīšana > Žurnālu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="9e797-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="9e797-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e797-120">Click New.</span></span>
3. <span data-ttu-id="9e797-121">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9e797-122">Laukā Dokumentu sērijas ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="9e797-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-123">Click Save.</span></span>
6. <span data-ttu-id="9e797-124">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e797-124">Click New.</span></span>
7. <span data-ttu-id="9e797-125">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="9e797-126">Atlasiet opciju laukā Žurnāla veids.</span><span class="sxs-lookup"><span data-stu-id="9e797-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="9e797-127">Laukā Dokumentu sērijas ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="9e797-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="9e797-129">Izveidot avansa turētāju grupu</span><span class="sxs-lookup"><span data-stu-id="9e797-129">Create an advance holder group</span></span>
1. <span data-ttu-id="9e797-130">Dodieties uz Parādi kreditoriem > Iestatīšana > Avansa turētāji > Avansa turētāju grupas.</span><span class="sxs-lookup"><span data-stu-id="9e797-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="9e797-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e797-131">Click New.</span></span>
3. <span data-ttu-id="9e797-132">Laukā Grupa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="9e797-133">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9e797-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="9e797-135">Izveidot darbinieka grāmatošanas metodi</span><span class="sxs-lookup"><span data-stu-id="9e797-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="9e797-136">Dodieties uz Parādi kreditoriem > Iestatīšana > Avansa turētāji > Darbinieku grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="9e797-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="9e797-137">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e797-137">Click New.</span></span>
3. <span data-ttu-id="9e797-138">Ievadiet vērtību laukā Grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="9e797-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="9e797-139">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9e797-140">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9e797-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9e797-141">Atlasiet opciju laukā Derīguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="9e797-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="9e797-142">Laukā Summu konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="9e797-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="9e797-143">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="9e797-144">Iestatīt avansa turētāja parametrus</span><span class="sxs-lookup"><span data-stu-id="9e797-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="9e797-145">Pārejiet uz sadaļu Kreditori > Iestatījumi > Kreditoru parametri.</span><span class="sxs-lookup"><span data-stu-id="9e797-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="9e797-146">Noklikšķiniet uz cilnes Avansa turētāji.</span><span class="sxs-lookup"><span data-stu-id="9e797-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="9e797-147">Laukā Grāmatošanas metode ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="9e797-148">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="9e797-149">Laukā Kase ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="9e797-150">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="9e797-151">Laukā Konta tips atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9e797-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="9e797-152">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="9e797-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="9e797-153">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="9e797-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="9e797-154">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="9e797-155">Iestatīt kases grāmatošanas metodi</span><span class="sxs-lookup"><span data-stu-id="9e797-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="9e797-156">Dodieties uz Kases un bankas vadība > Iestatīšana > Kases grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="9e797-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="9e797-157">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e797-157">Click New.</span></span>
3. <span data-ttu-id="9e797-158">Laukā Kases grāmatošana ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="9e797-159">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9e797-160">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9e797-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9e797-161">Atlasiet opciju laukā Derīguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="9e797-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="9e797-162">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="9e797-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="9e797-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="9e797-164">Iestatīt kases un bankas parametrus</span><span class="sxs-lookup"><span data-stu-id="9e797-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="9e797-165">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="9e797-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="9e797-166">Noklikšķiniet uz cilnes Kase.</span><span class="sxs-lookup"><span data-stu-id="9e797-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="9e797-167">Laukā Kase ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="9e797-168">Laukā Kases grāmatošana ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="9e797-169">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-169">Click Save.</span></span>
6. <span data-ttu-id="9e797-170">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="9e797-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="9e797-171">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9e797-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9e797-172">Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="9e797-173">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9e797-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9e797-174">Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="9e797-175">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="9e797-176">Iestatiet maksājumu nosacījumus</span><span class="sxs-lookup"><span data-stu-id="9e797-176">Set up terms of payment</span></span>
1. <span data-ttu-id="9e797-177">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Apmaksas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="9e797-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="9e797-178">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9e797-178">Click Edit.</span></span>
3. <span data-ttu-id="9e797-179">Atlasiet Jā laukā No avansa turētāja.</span><span class="sxs-lookup"><span data-stu-id="9e797-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="9e797-180">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="9e797-181">Izveidot jaunu darbinieku</span><span class="sxs-lookup"><span data-stu-id="9e797-181">Create a new worker</span></span>
1. <span data-ttu-id="9e797-182">Pārejiet uz sadaļu Personāla vadība > Darbinieki > Darbinieki.</span><span class="sxs-lookup"><span data-stu-id="9e797-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="9e797-183">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e797-183">Click New.</span></span>
3. <span data-ttu-id="9e797-184">Laukā Vārds ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="9e797-185">Laukā Uzvārds ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="9e797-186">Laukā Darbinieka ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="9e797-187">Noklikšķiniet uz Pieņemt darbā jaunu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="9e797-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="9e797-188">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="9e797-189">Iestatīt darbinieku kā avansa turētāju</span><span class="sxs-lookup"><span data-stu-id="9e797-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="9e797-190">Dodieties uz Parādi kreditoriem > Avansa turētāji > Avansa turētāji.</span><span class="sxs-lookup"><span data-stu-id="9e797-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="9e797-191">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9e797-191">Click Edit.</span></span>
3. <span data-ttu-id="9e797-192">Laukā Grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="9e797-193">Atlasiet Jā laukā Avansa turētājs.</span><span class="sxs-lookup"><span data-stu-id="9e797-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="9e797-194">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="9e797-195">Izveidot un grāmatot pirkšanas pasūtījuma rēķinu</span><span class="sxs-lookup"><span data-stu-id="9e797-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="9e797-196">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="9e797-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="9e797-197">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e797-197">Click New.</span></span>
3. <span data-ttu-id="9e797-198">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="9e797-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="9e797-199">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="9e797-199">Click OK.</span></span>
5. <span data-ttu-id="9e797-200">Laukā Rindas vai virsraksts atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9e797-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="9e797-201">Izvērsiet sadaļu Cena un atlaide.</span><span class="sxs-lookup"><span data-stu-id="9e797-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="9e797-202">Laukā Apmaksas nosacījumi ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="9e797-203">Laukā Avansa turētājs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="9e797-204">Laukā Rindas vai virsraksts atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9e797-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="9e797-205">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9e797-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="9e797-206">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="9e797-207">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9e797-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="9e797-208">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9e797-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="9e797-209">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9e797-209">Click Save.</span></span>
15. <span data-ttu-id="9e797-210">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="9e797-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="9e797-211">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="9e797-211">Click Confirm.</span></span>
17. <span data-ttu-id="9e797-212">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="9e797-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="9e797-213">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="9e797-213">Click Invoice.</span></span>
19. <span data-ttu-id="9e797-214">Noklikšķiniet uz Noklusējums no: Produktu ieejas plūsmu daudzums, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9e797-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="9e797-215">Laukā Noklusējuma daudzums rindām atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="9e797-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="9e797-216">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="9e797-216">Click OK.</span></span>
22. <span data-ttu-id="9e797-217">Laukā Numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="9e797-218">Laukā Rēķina apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e797-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="9e797-219">Ievadiet datumu laukā Rēķina datums.</span><span class="sxs-lookup"><span data-stu-id="9e797-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="9e797-220">Ievadiet datumu PVN reģistra datums.</span><span class="sxs-lookup"><span data-stu-id="9e797-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="9e797-221">Laukā Saņemt dokumenta datumu ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="9e797-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="9e797-222">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="9e797-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="9e797-223">Bilances un avansa turētāju slēgšanas transakcijas</span><span class="sxs-lookup"><span data-stu-id="9e797-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="9e797-224">Dodieties uz Parādi kreditoriem > Avansa turētāji > Avansa turētāji.</span><span class="sxs-lookup"><span data-stu-id="9e797-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="9e797-225">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="9e797-225">Click Transactions.</span></span>
3. <span data-ttu-id="9e797-226">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9e797-226">Close the page.</span></span>
4. <span data-ttu-id="9e797-227">Noklikšķiniet uz Bilance.</span><span class="sxs-lookup"><span data-stu-id="9e797-227">Click Balance.</span></span>
5. <span data-ttu-id="9e797-228">Noklikšķiniet uz Slēgt no bankas.</span><span class="sxs-lookup"><span data-stu-id="9e797-228">Click Close via bank.</span></span>
6. <span data-ttu-id="9e797-229">Atlasiet Jā laukā Automātisks.</span><span class="sxs-lookup"><span data-stu-id="9e797-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="9e797-230">Laukā Summa pārsūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="9e797-230">In the Amount to be transferred.</span></span> <span data-ttu-id="9e797-231">ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9e797-231">field, enter a number.</span></span>
8. <span data-ttu-id="9e797-232">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9e797-232">Click OK.</span></span>
9. <span data-ttu-id="9e797-233">Noklikšķiniet uz Slēgt no kases.</span><span class="sxs-lookup"><span data-stu-id="9e797-233">Click Close via cash.</span></span>
10. <span data-ttu-id="9e797-234">Atlasiet Jā laukā Automātisks.</span><span class="sxs-lookup"><span data-stu-id="9e797-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="9e797-235">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9e797-235">Click OK.</span></span>
12. <span data-ttu-id="9e797-236">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9e797-236">Close the page.</span></span>
13. <span data-ttu-id="9e797-237">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="9e797-237">Click Transactions.</span></span>


