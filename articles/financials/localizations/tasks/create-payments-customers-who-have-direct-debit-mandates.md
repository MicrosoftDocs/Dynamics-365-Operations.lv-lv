--- 
title: "Maksājumu izveide debitoram ar tiešā debeta mandātiem"
description: "Šajā procedūrā parādīts, kā izveidot ISO20022 tiešā debeta maksājuma failu debitoram, kuram ir konfigurēts tiešais debets un ir apmaksājams rēķins."
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: acd6a8076288d8d1d1aa05af33e306c6a29780f7
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="41f6a-103">Maksājumu izveide debitoram ar tiešā debeta mandātiem</span><span class="sxs-lookup"><span data-stu-id="41f6a-103">Create payments for a customer who have direct debit mandates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41f6a-104">Šajā procedūrā parādīts, kā izveidot ISO20022 tiešā debeta maksājuma failu debitoram, kuram ir konfigurēts tiešais debets un ir apmaksājams rēķins.</span><span class="sxs-lookup"><span data-stu-id="41f6a-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="41f6a-105">Rēķina izveide un grāmatošana nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="41f6a-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="41f6a-106">Apmaksājama rēķina vietā, jūs, pirms maksājuma faila ģenerēšanas, varat atlasīt pilnvarojumu žurnālā, lai atbalstītu debitoru priekšapmaksas gadījumā.</span><span class="sxs-lookup"><span data-stu-id="41f6a-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="41f6a-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.</span><span class="sxs-lookup"><span data-stu-id="41f6a-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="41f6a-108">Šis ir piektā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="41f6a-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="41f6a-109">Lai varētu pabeigt šo uzdevumu, jums ir jāpabeidz iepriekšējie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="41f6a-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="41f6a-110">Vispirms jāimportē debitora maksājumu elektronisko pārskatu veidošanas konfigurācijas, jākonfigurē maksājumu metode un jāiestata uzņēmuma un debitora informācija.</span><span class="sxs-lookup"><span data-stu-id="41f6a-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="41f6a-111">Brīva teksta rēķina ar tiešā debeta informāciju grāmatošana</span><span class="sxs-lookup"><span data-stu-id="41f6a-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="41f6a-112">Pārejiet uz sadaļu Debitori > Rēķini > Visi brīva teksta rēķini.</span><span class="sxs-lookup"><span data-stu-id="41f6a-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="41f6a-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="41f6a-113">Click New.</span></span>
3. <span data-ttu-id="41f6a-114">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="41f6a-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="41f6a-115">Piemēram, atlasiet DE-010.</span><span class="sxs-lookup"><span data-stu-id="41f6a-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="41f6a-116">Laukā Maksājuma metode ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="41f6a-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="41f6a-117">Piemēram,</span><span class="sxs-lookup"><span data-stu-id="41f6a-117">For example.</span></span> <span data-ttu-id="41f6a-118">atlasiet elektronisks.</span><span class="sxs-lookup"><span data-stu-id="41f6a-118">select Electronic.</span></span>  
5. <span data-ttu-id="41f6a-119">Laukā Tiešā debeta pilnvarojuma ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="41f6a-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="41f6a-120">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="41f6a-120">Click Add line.</span></span>
7. <span data-ttu-id="41f6a-121">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="41f6a-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="41f6a-122">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="41f6a-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="41f6a-123">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="41f6a-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="41f6a-124">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="41f6a-124">Click Post.</span></span>
11. <span data-ttu-id="41f6a-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="41f6a-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="41f6a-126">Maksājuma izveidošana</span><span class="sxs-lookup"><span data-stu-id="41f6a-126">Create a payment</span></span>
1. <span data-ttu-id="41f6a-127">Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="41f6a-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="41f6a-128">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="41f6a-128">Click New.</span></span>
3. <span data-ttu-id="41f6a-129">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="41f6a-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="41f6a-130">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="41f6a-130">Click Lines.</span></span>
5. <span data-ttu-id="41f6a-131">Noklikšķiniet uz Maksājuma priekšlikums.</span><span class="sxs-lookup"><span data-stu-id="41f6a-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="41f6a-132">Noklikšķiniet uz Izveidot maksājuma priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="41f6a-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="41f6a-133">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="41f6a-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="41f6a-134">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="41f6a-134">Click Filter.</span></span>
9. <span data-ttu-id="41f6a-135">Sarakstā atlasiet rindu, kas attiecas uz klienta darījumu tabulu, un lauku Maksājuma metode.</span><span class="sxs-lookup"><span data-stu-id="41f6a-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="41f6a-136">Jūs varat lietot visus kritērijus, atlasot debitoru transakcijas, kas jāapmaksā.</span><span class="sxs-lookup"><span data-stu-id="41f6a-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="41f6a-137">Šajā piemērā izmantojiet Elektronisks kā maksājuma metodi, lai filtrētu darījumus.</span><span class="sxs-lookup"><span data-stu-id="41f6a-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="41f6a-138">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="41f6a-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="41f6a-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="41f6a-139">Click OK.</span></span>
12. <span data-ttu-id="41f6a-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="41f6a-140">Click OK.</span></span>
13. <span data-ttu-id="41f6a-141">Noklikšķiniet uz Izveidot maksājumus.</span><span class="sxs-lookup"><span data-stu-id="41f6a-141">Click Create payments.</span></span>

## <a name="generate-a-payment-file"></a><span data-ttu-id="41f6a-142">Maksājuma faila ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="41f6a-142">Generate a payment file</span></span>


