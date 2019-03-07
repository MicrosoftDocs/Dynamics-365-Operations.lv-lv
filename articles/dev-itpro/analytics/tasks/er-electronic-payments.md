---
title: ER Ģenerēt elektroniskos dokumentus maksājumiem, izmantojot formātu konfigurāciju
description: Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izmantot jauno Elektronisko pārskatu (ER) konfigurācijas formātu, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf2ae8fb451eba1054bb94edbce009dcfa8c872c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "348323"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="f20fc-103">ER Ģenerēt elektroniskos dokumentus maksājumiem, izmantojot formātu konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="f20fc-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f20fc-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izmantot jauno Elektronisko pārskatu (ER) konfigurācijas formātu, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="f20fc-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="f20fc-105">Šīs darbības var veikt parauga uzņēmumā GBSI.</span><span class="sxs-lookup"><span data-stu-id="f20fc-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="f20fc-106">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas izveide ar maksājuma dokumenta formātu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="f20fc-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="f20fc-107">Mainiet elektronisko maksājumu metodes konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="f20fc-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="f20fc-108">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="f20fc-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="f20fc-109">Pārslēdziet Faila formāta sadaļu, lai to izvērstu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="f20fc-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="f20fc-110">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="f20fc-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f20fc-111">Piemēram, filtrējiet pēc lauka Maksāšanas metodes, izmantojot vērtību 'Electronic'.</span><span class="sxs-lookup"><span data-stu-id="f20fc-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="f20fc-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f20fc-112">Click Edit.</span></span>
5. <span data-ttu-id="f20fc-113">Iestatiet Lauku Vispārīga elektronisko pārskatu veidošana uz Jā.</span><span class="sxs-lookup"><span data-stu-id="f20fc-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="f20fc-114">Atlasiet Jā, lai izmantotu Vispārējo elektronisko pārskata modeli maksājumu failu izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="f20fc-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="f20fc-115">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f20fc-116">Atlasiet BAKS (UK fiktīvs) formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="f20fc-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="f20fc-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f20fc-117">Click Save.</span></span>
9. <span data-ttu-id="f20fc-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="f20fc-119">Pārbaudiet izveidoto maksājumu failu formātu</span><span class="sxs-lookup"><span data-stu-id="f20fc-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="f20fc-120">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="f20fc-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="f20fc-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f20fc-121">Click New.</span></span>
3. <span data-ttu-id="f20fc-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f20fc-123">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f20fc-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f20fc-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f20fc-125">Atlasiet VendPay.</span><span class="sxs-lookup"><span data-stu-id="f20fc-125">Select VendPay.</span></span>  
6. <span data-ttu-id="f20fc-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f20fc-126">Click Save.</span></span>
7. <span data-ttu-id="f20fc-127">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="f20fc-127">Click Lines.</span></span>
8. <span data-ttu-id="f20fc-128">Laukā Uzņēmums ierakstiet vērtību “DEMF”.</span><span class="sxs-lookup"><span data-stu-id="f20fc-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="f20fc-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="f20fc-129">DEMF</span></span>  
9. <span data-ttu-id="f20fc-130">Laukā Konts norādiet vērtību DE-01001.</span><span class="sxs-lookup"><span data-stu-id="f20fc-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="f20fc-131">DE — 01001</span><span class="sxs-lookup"><span data-stu-id="f20fc-131">DE-01001</span></span>  
10. <span data-ttu-id="f20fc-132">Laukā Apraksts, ievadiet 'Maksājums'.</span><span class="sxs-lookup"><span data-stu-id="f20fc-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="f20fc-133">Maksājums</span><span class="sxs-lookup"><span data-stu-id="f20fc-133">Payment</span></span>  
11. <span data-ttu-id="f20fc-134">Laukā Debets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f20fc-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="f20fc-135">1000</span><span class="sxs-lookup"><span data-stu-id="f20fc-135">1000</span></span>  
12. <span data-ttu-id="f20fc-136">Noklikšķiniet uz cilnes Maksājums.</span><span class="sxs-lookup"><span data-stu-id="f20fc-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="f20fc-137">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f20fc-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f20fc-139">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="f20fc-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="f20fc-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f20fc-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f20fc-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f20fc-141">Click Save.</span></span>
17. <span data-ttu-id="f20fc-142">Noklikšķiniet uz Ģenerēt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="f20fc-142">Click Generate payments.</span></span>
18. <span data-ttu-id="f20fc-143">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="f20fc-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f20fc-145">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="f20fc-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="f20fc-146">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f20fc-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f20fc-147">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="f20fc-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="f20fc-148">Ierakstiet vērtību laukā Faila nosaukums.</span><span class="sxs-lookup"><span data-stu-id="f20fc-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="f20fc-149">Piemēram, ievadiet 'maksājumi'.</span><span class="sxs-lookup"><span data-stu-id="f20fc-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="f20fc-150">Laukā Bankas konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f20fc-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="f20fc-151">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f20fc-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f20fc-152">Atlasiet GBSI OPER vērtību.</span><span class="sxs-lookup"><span data-stu-id="f20fc-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="f20fc-153">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f20fc-153">Click OK.</span></span>
25. <span data-ttu-id="f20fc-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f20fc-154">Click OK.</span></span>
    * <span data-ttu-id="f20fc-155">Analizējiet izveidoto maksājumu failu XML formātā.</span><span class="sxs-lookup"><span data-stu-id="f20fc-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="f20fc-156">Salīdziniet to ar izstrādāto dokumenta izkārtojumu un definētajiem maksājuma transakcijas atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="f20fc-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

