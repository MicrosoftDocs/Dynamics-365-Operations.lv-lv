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
ms.openlocfilehash: fa39a9d459022e391f99e284d41d82215cc10e2b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142574"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="ba242-103">ER Ģenerēt elektroniskos dokumentus maksājumiem, izmantojot formātu konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="ba242-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba242-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izmantot jauno Elektronisko pārskatu (ER) konfigurācijas formātu, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="ba242-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="ba242-105">Šīs darbības var veikt parauga uzņēmumā GBSI.</span><span class="sxs-lookup"><span data-stu-id="ba242-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="ba242-106">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas izveide ar maksājuma dokumenta formātu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="ba242-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="ba242-107">Mainiet elektronisko maksājumu metodes konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="ba242-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="ba242-108">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="ba242-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="ba242-109">Pārslēdziet Faila formāta sadaļu, lai to izvērstu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="ba242-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="ba242-110">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="ba242-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ba242-111">Piemēram, filtrējiet pēc lauka Maksāšanas metodes, izmantojot vērtību 'Electronic'.</span><span class="sxs-lookup"><span data-stu-id="ba242-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="ba242-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="ba242-112">Click Edit.</span></span>
5. <span data-ttu-id="ba242-113">Iestatiet Lauku Vispārīga elektronisko pārskatu veidošana uz Jā.</span><span class="sxs-lookup"><span data-stu-id="ba242-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="ba242-114">Atlasiet Jā, lai izmantotu Vispārējo elektronisko pārskata modeli maksājumu failu izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="ba242-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="ba242-115">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ba242-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ba242-116">Atlasiet BAKS (UK fiktīvs) formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="ba242-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="ba242-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ba242-117">Click Save.</span></span>
9. <span data-ttu-id="ba242-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ba242-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="ba242-119">Pārbaudiet izveidoto maksājumu failu formātu</span><span class="sxs-lookup"><span data-stu-id="ba242-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="ba242-120">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="ba242-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="ba242-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ba242-121">Click New.</span></span>
3. <span data-ttu-id="ba242-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba242-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ba242-123">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ba242-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ba242-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ba242-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ba242-125">Atlasiet VendPay.</span><span class="sxs-lookup"><span data-stu-id="ba242-125">Select VendPay.</span></span>  
6. <span data-ttu-id="ba242-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ba242-126">Click Save.</span></span>
7. <span data-ttu-id="ba242-127">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="ba242-127">Click Lines.</span></span>
8. <span data-ttu-id="ba242-128">Laukā Uzņēmums ierakstiet vērtību “DEMF”.</span><span class="sxs-lookup"><span data-stu-id="ba242-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="ba242-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="ba242-129">DEMF</span></span>  
9. <span data-ttu-id="ba242-130">Laukā Konts norādiet vērtību DE-01001.</span><span class="sxs-lookup"><span data-stu-id="ba242-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="ba242-131">DE — 01001</span><span class="sxs-lookup"><span data-stu-id="ba242-131">DE-01001</span></span>  
10. <span data-ttu-id="ba242-132">Laukā Apraksts, ievadiet 'Maksājums'.</span><span class="sxs-lookup"><span data-stu-id="ba242-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="ba242-133">Maksājums</span><span class="sxs-lookup"><span data-stu-id="ba242-133">Payment</span></span>  
11. <span data-ttu-id="ba242-134">Laukā Debets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="ba242-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="ba242-135">1000</span><span class="sxs-lookup"><span data-stu-id="ba242-135">1000</span></span>  
12. <span data-ttu-id="ba242-136">Noklikšķiniet uz cilnes Maksājums.</span><span class="sxs-lookup"><span data-stu-id="ba242-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="ba242-137">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ba242-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="ba242-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ba242-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ba242-139">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba242-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="ba242-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ba242-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ba242-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ba242-141">Click Save.</span></span>
17. <span data-ttu-id="ba242-142">Noklikšķiniet uz Ģenerēt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="ba242-142">Click Generate payments.</span></span>
18. <span data-ttu-id="ba242-143">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ba242-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="ba242-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ba242-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ba242-145">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba242-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="ba242-146">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ba242-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ba242-147">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba242-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="ba242-148">Ierakstiet vērtību laukā Faila nosaukums.</span><span class="sxs-lookup"><span data-stu-id="ba242-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="ba242-149">Piemēram, ievadiet 'maksājumi'.</span><span class="sxs-lookup"><span data-stu-id="ba242-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="ba242-150">Laukā Bankas konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ba242-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="ba242-151">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ba242-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ba242-152">Atlasiet GBSI OPER vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba242-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="ba242-153">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ba242-153">Click OK.</span></span>
25. <span data-ttu-id="ba242-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ba242-154">Click OK.</span></span>
    * <span data-ttu-id="ba242-155">Analizējiet izveidoto maksājumu failu XML formātā.</span><span class="sxs-lookup"><span data-stu-id="ba242-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="ba242-156">Salīdziniet to ar izstrādāto dokumenta izkārtojumu un definētajiem maksājuma transakcijas atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="ba242-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

