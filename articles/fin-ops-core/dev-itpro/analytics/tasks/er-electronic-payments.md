---
title: ER Ģenerēt elektroniskos dokumentus maksājumiem, izmantojot formātu konfigurāciju
description: Tematā aprakstīts, kā izmantot jaunu elektronisko pārskatu (ER) konfigurāciju, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei.
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 816f98660a5508ada203f49a71e0785548fb9a31
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092204"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="04156-103">ER Ģenerēt elektroniskos dokumentus maksājumiem, izmantojot formātu konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="04156-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04156-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izmantot jauno Elektronisko pārskatu (ER) konfigurācijas formātu, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="04156-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="04156-105">Šīs darbības var veikt parauga uzņēmumā GBSI.</span><span class="sxs-lookup"><span data-stu-id="04156-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="04156-106">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas izveide ar maksājuma dokumenta formātu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="04156-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="04156-107">Mainiet elektronisko maksājumu metodes konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="04156-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="04156-108">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="04156-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="04156-109">Pārslēdziet Faila formāta sadaļu, lai to izvērstu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="04156-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="04156-110">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="04156-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="04156-111">Piemēram, filtrējiet pēc lauka Maksāšanas metodes, izmantojot vērtību 'Electronic'.</span><span class="sxs-lookup"><span data-stu-id="04156-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="04156-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="04156-112">Click Edit.</span></span>
5. <span data-ttu-id="04156-113">Iestatiet Lauku Vispārīga elektronisko pārskatu veidošana uz Jā.</span><span class="sxs-lookup"><span data-stu-id="04156-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="04156-114">Atlasiet Jā, lai izmantotu Vispārējo elektronisko pārskata modeli maksājumu failu izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="04156-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="04156-115">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="04156-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="04156-116">Atlasiet BAKS (UK fiktīvs) formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="04156-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="04156-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="04156-117">Click Save.</span></span>
9. <span data-ttu-id="04156-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="04156-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="04156-119">Pārbaudiet izveidoto maksājumu failu formātu</span><span class="sxs-lookup"><span data-stu-id="04156-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="04156-120">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="04156-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="04156-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="04156-121">Click New.</span></span>
3. <span data-ttu-id="04156-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="04156-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="04156-123">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="04156-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="04156-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="04156-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="04156-125">Atlasiet VendPay.</span><span class="sxs-lookup"><span data-stu-id="04156-125">Select VendPay.</span></span>  
6. <span data-ttu-id="04156-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="04156-126">Click Save.</span></span>
7. <span data-ttu-id="04156-127">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="04156-127">Click Lines.</span></span>
8. <span data-ttu-id="04156-128">Laukā Uzņēmums ierakstiet vērtību “DEMF”.</span><span class="sxs-lookup"><span data-stu-id="04156-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="04156-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="04156-129">DEMF</span></span>  
9. <span data-ttu-id="04156-130">Laukā Konts norādiet vērtību DE-01001.</span><span class="sxs-lookup"><span data-stu-id="04156-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="04156-131">DE — 01001</span><span class="sxs-lookup"><span data-stu-id="04156-131">DE-01001</span></span>  
10. <span data-ttu-id="04156-132">Laukā Apraksts, ievadiet 'Maksājums'.</span><span class="sxs-lookup"><span data-stu-id="04156-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="04156-133">Maksājums</span><span class="sxs-lookup"><span data-stu-id="04156-133">Payment</span></span>  
11. <span data-ttu-id="04156-134">Laukā Debets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="04156-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="04156-135">1000</span><span class="sxs-lookup"><span data-stu-id="04156-135">1000</span></span>  
12. <span data-ttu-id="04156-136">Noklikšķiniet uz cilnes Maksājums.</span><span class="sxs-lookup"><span data-stu-id="04156-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="04156-137">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="04156-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="04156-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="04156-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="04156-139">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="04156-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="04156-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="04156-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="04156-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="04156-141">Click Save.</span></span>
17. <span data-ttu-id="04156-142">Noklikšķiniet uz Ģenerēt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="04156-142">Click Generate payments.</span></span>
18. <span data-ttu-id="04156-143">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="04156-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="04156-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="04156-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="04156-145">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="04156-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="04156-146">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="04156-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="04156-147">Atlasiet Elektronisko vērtību.</span><span class="sxs-lookup"><span data-stu-id="04156-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="04156-148">Ierakstiet vērtību laukā Faila nosaukums.</span><span class="sxs-lookup"><span data-stu-id="04156-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="04156-149">Piemēram, ievadiet 'maksājumi'.</span><span class="sxs-lookup"><span data-stu-id="04156-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="04156-150">Laukā Bankas konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="04156-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="04156-151">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="04156-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="04156-152">Atlasiet GBSI OPER vērtību.</span><span class="sxs-lookup"><span data-stu-id="04156-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="04156-153">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="04156-153">Click OK.</span></span>
25. <span data-ttu-id="04156-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="04156-154">Click OK.</span></span>
    * <span data-ttu-id="04156-155">Analizējiet izveidoto maksājumu failu XML formātā.</span><span class="sxs-lookup"><span data-stu-id="04156-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="04156-156">Salīdziniet to ar izstrādāto dokumenta izkārtojumu un definētajiem maksājuma transakcijas atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="04156-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

