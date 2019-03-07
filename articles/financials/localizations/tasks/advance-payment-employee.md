---
title: EEU-00047 avansa maksājums darbiniekam
description: Šajā procedūrā parādīts, kā iestatīt un reģistrēt darbības avansa turētājam.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3c07789bfa0839436caf32e428f3abeecb8f2b7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "371315"
---
# <a name="eeu-00047-advance-payment-to-employee"></a><span data-ttu-id="8d0bc-103">EEU-00047 avansa maksājums darbiniekam</span><span class="sxs-lookup"><span data-stu-id="8d0bc-103">EEU-00047 Advance payment to employee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d0bc-104">Šajā procedūrā parādīts, kā iestatīt un reģistrēt darbības avansa turētājam.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="8d0bc-105">Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Lietuvā.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="8d0bc-106">Šis uzdevums ir paredzēts tikai juridiskām personām, kuru primārā adrese ir Polijā, Lietuvā, Latvijā, Igaunijā, Čehijā vai Ungārijā.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="8d0bc-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="8d0bc-108">Izveidot jaunu kases kontu</span><span class="sxs-lookup"><span data-stu-id="8d0bc-108">Create a new cash account</span></span>
1. <span data-ttu-id="8d0bc-109">Dodieties uz Kases un bankas vadība > Bankas konti > Kases konti.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="8d0bc-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-110">Click New.</span></span>
3. <span data-ttu-id="8d0bc-111">Laukā Kase ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="8d0bc-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8d0bc-113">Laukā Numuru sērijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="8d0bc-114">Izvērsiet sadaļu Apstiprināšana.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="8d0bc-115">Laukā Valūta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="8d0bc-116">Atlasiet Jā laukā Negatīvs atlikums kasē.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="8d0bc-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="8d0bc-118">Izveidot jaunu žurnālu</span><span class="sxs-lookup"><span data-stu-id="8d0bc-118">Create a new journal</span></span>
1. <span data-ttu-id="8d0bc-119">Pārejiet uz sadaļu Virsgrāmata >Žurnāla iestatīšana > Žurnālu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="8d0bc-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-120">Click New.</span></span>
3. <span data-ttu-id="8d0bc-121">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8d0bc-122">Laukā Dokumentu sērijas ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="8d0bc-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-123">Click Save.</span></span>
6. <span data-ttu-id="8d0bc-124">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-124">Click New.</span></span>
7. <span data-ttu-id="8d0bc-125">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="8d0bc-126">Atlasiet opciju laukā Žurnāla veids.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="8d0bc-127">Laukā Dokumentu sērijas ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="8d0bc-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="8d0bc-129">Izveidot avansa turētāju grupu</span><span class="sxs-lookup"><span data-stu-id="8d0bc-129">Create an advance holder group</span></span>
1. <span data-ttu-id="8d0bc-130">Dodieties uz Parādi kreditoriem > Iestatīšana > Avansa turētāji > Avansa turētāju grupas.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="8d0bc-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-131">Click New.</span></span>
3. <span data-ttu-id="8d0bc-132">Laukā Grupa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="8d0bc-133">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8d0bc-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="8d0bc-135">Izveidot darbinieka grāmatošanas metodi</span><span class="sxs-lookup"><span data-stu-id="8d0bc-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="8d0bc-136">Dodieties uz Parādi kreditoriem > Iestatīšana > Avansa turētāji > Darbinieku grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="8d0bc-137">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-137">Click New.</span></span>
3. <span data-ttu-id="8d0bc-138">Ievadiet vērtību laukā Grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="8d0bc-139">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8d0bc-140">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8d0bc-141">Atlasiet opciju laukā Derīguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="8d0bc-142">Laukā Summu konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="8d0bc-143">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="8d0bc-144">Iestatīt avansa turētāja parametrus</span><span class="sxs-lookup"><span data-stu-id="8d0bc-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="8d0bc-145">Pārejiet uz sadaļu Kreditori > Iestatījumi > Kreditoru parametri.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="8d0bc-146">Noklikšķiniet uz cilnes Avansa turētāji.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="8d0bc-147">Laukā Grāmatošanas metode ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="8d0bc-148">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="8d0bc-149">Laukā Kase ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="8d0bc-150">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="8d0bc-151">Laukā Konta tips atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="8d0bc-152">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="8d0bc-153">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="8d0bc-154">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="8d0bc-155">Iestatīt kases grāmatošanas metodi</span><span class="sxs-lookup"><span data-stu-id="8d0bc-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="8d0bc-156">Dodieties uz Kases un bankas vadība > Iestatīšana > Kases grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="8d0bc-157">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-157">Click New.</span></span>
3. <span data-ttu-id="8d0bc-158">Laukā Kases grāmatošana ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="8d0bc-159">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8d0bc-160">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8d0bc-161">Atlasiet opciju laukā Derīguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="8d0bc-162">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="8d0bc-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="8d0bc-164">Iestatīt kases un bankas parametrus</span><span class="sxs-lookup"><span data-stu-id="8d0bc-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="8d0bc-165">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="8d0bc-166">Noklikšķiniet uz cilnes Kase.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="8d0bc-167">Laukā Kase ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="8d0bc-168">Laukā Kases grāmatošana ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="8d0bc-169">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-169">Click Save.</span></span>
6. <span data-ttu-id="8d0bc-170">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="8d0bc-171">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8d0bc-172">Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="8d0bc-173">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="8d0bc-174">Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="8d0bc-175">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="8d0bc-176">Iestatiet maksājumu nosacījumus</span><span class="sxs-lookup"><span data-stu-id="8d0bc-176">Set up terms of payment</span></span>
1. <span data-ttu-id="8d0bc-177">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Apmaksas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="8d0bc-178">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-178">Click Edit.</span></span>
3. <span data-ttu-id="8d0bc-179">Atlasiet Jā laukā No avansa turētāja.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="8d0bc-180">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="8d0bc-181">Izveidot jaunu darbinieku</span><span class="sxs-lookup"><span data-stu-id="8d0bc-181">Create a new worker</span></span>
1. <span data-ttu-id="8d0bc-182">Pārejiet uz sadaļu Personāla vadība > Darbinieki > Darbinieki.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="8d0bc-183">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-183">Click New.</span></span>
3. <span data-ttu-id="8d0bc-184">Laukā Vārds ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="8d0bc-185">Laukā Uzvārds ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="8d0bc-186">Laukā Darbinieka ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="8d0bc-187">Noklikšķiniet uz Pieņemt darbā jaunu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="8d0bc-188">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="8d0bc-189">Iestatīt darbinieku kā avansa turētāju</span><span class="sxs-lookup"><span data-stu-id="8d0bc-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="8d0bc-190">Dodieties uz Parādi kreditoriem > Avansa turētāji > Avansa turētāji.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="8d0bc-191">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-191">Click Edit.</span></span>
3. <span data-ttu-id="8d0bc-192">Laukā Grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="8d0bc-193">Atlasiet Jā laukā Avansa turētājs.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="8d0bc-194">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="8d0bc-195">Izveidot un grāmatot pirkšanas pasūtījuma rēķinu</span><span class="sxs-lookup"><span data-stu-id="8d0bc-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="8d0bc-196">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="8d0bc-197">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-197">Click New.</span></span>
3. <span data-ttu-id="8d0bc-198">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="8d0bc-199">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-199">Click OK.</span></span>
5. <span data-ttu-id="8d0bc-200">Laukā Rindas vai virsraksts atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="8d0bc-201">Izvērsiet sadaļu Cena un atlaide.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="8d0bc-202">Laukā Apmaksas nosacījumi ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="8d0bc-203">Laukā Avansa turētājs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="8d0bc-204">Laukā Rindas vai virsraksts atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="8d0bc-205">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="8d0bc-206">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="8d0bc-207">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="8d0bc-208">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="8d0bc-209">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-209">Click Save.</span></span>
15. <span data-ttu-id="8d0bc-210">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="8d0bc-211">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-211">Click Confirm.</span></span>
17. <span data-ttu-id="8d0bc-212">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="8d0bc-213">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-213">Click Invoice.</span></span>
19. <span data-ttu-id="8d0bc-214">Noklikšķiniet uz Noklusējums no: Produktu ieejas plūsmu daudzums, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="8d0bc-215">Laukā Noklusējuma daudzums rindām atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="8d0bc-216">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-216">Click OK.</span></span>
22. <span data-ttu-id="8d0bc-217">Laukā Numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="8d0bc-218">Laukā Rēķina apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="8d0bc-219">Ievadiet datumu laukā Rēķina datums.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="8d0bc-220">Ievadiet datumu PVN reģistra datums.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="8d0bc-221">Laukā Saņemt dokumenta datumu ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="8d0bc-222">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="8d0bc-223">Bilances un avansa turētāju slēgšanas transakcijas</span><span class="sxs-lookup"><span data-stu-id="8d0bc-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="8d0bc-224">Dodieties uz Parādi kreditoriem > Avansa turētāji > Avansa turētāji.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="8d0bc-225">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-225">Click Transactions.</span></span>
3. <span data-ttu-id="8d0bc-226">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-226">Close the page.</span></span>
4. <span data-ttu-id="8d0bc-227">Noklikšķiniet uz Bilance.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-227">Click Balance.</span></span>
5. <span data-ttu-id="8d0bc-228">Noklikšķiniet uz Slēgt no bankas.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-228">Click Close via bank.</span></span>
6. <span data-ttu-id="8d0bc-229">Atlasiet Jā laukā Automātisks.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="8d0bc-230">Laukā Summa pārsūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-230">In the Amount to be transferred.</span></span> <span data-ttu-id="8d0bc-231">ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-231">field, enter a number.</span></span>
8. <span data-ttu-id="8d0bc-232">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-232">Click OK.</span></span>
9. <span data-ttu-id="8d0bc-233">Noklikšķiniet uz Slēgt no kases.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-233">Click Close via cash.</span></span>
10. <span data-ttu-id="8d0bc-234">Atlasiet Jā laukā Automātisks.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="8d0bc-235">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-235">Click OK.</span></span>
12. <span data-ttu-id="8d0bc-236">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-236">Close the page.</span></span>
13. <span data-ttu-id="8d0bc-237">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-237">Click Transactions.</span></span>

