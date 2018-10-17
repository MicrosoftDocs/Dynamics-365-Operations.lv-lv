--- 
title: "Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu"
description: "Šis uzdevuma ceļvedis palīdzēs izveidot kreditora rēķinu no pirkšanas pasūtījuma un apskatīt pirkšanas pasūtījuma, kvīts un rēķina saskaņošanas rezultātus (3 virzienu atbilstība)."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="79239-103">Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu</span><span class="sxs-lookup"><span data-stu-id="79239-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79239-104">Šis uzdevuma ceļvedis palīdzēs izveidot kreditora rēķinu no pirkšanas pasūtījuma un apskatīt pirkšanas pasūtījuma, kvīts un rēķina saskaņošanas rezultātus (3 virzienu atbilstība).</span><span class="sxs-lookup"><span data-stu-id="79239-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="79239-105">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="79239-105">Create a purchase order</span></span>
1. <span data-ttu-id="79239-106">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="79239-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="79239-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="79239-107">Click New.</span></span>
3. <span data-ttu-id="79239-108">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="79239-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="79239-109">Atrodiet kreditoru, kuru atlasīt.</span><span class="sxs-lookup"><span data-stu-id="79239-109">Find a vendor to select.</span></span> <span data-ttu-id="79239-110">Piemēram, ritiniet uz leju līdz US-104.</span><span class="sxs-lookup"><span data-stu-id="79239-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="79239-111">Atlasiet kreditoru US-104.</span><span class="sxs-lookup"><span data-stu-id="79239-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="79239-112">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="79239-112">Click OK.</span></span>
7. <span data-ttu-id="79239-113">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="79239-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="79239-114">Atlasiet krājuma vienību.</span><span class="sxs-lookup"><span data-stu-id="79239-114">Select an inventory item.</span></span> <span data-ttu-id="79239-115">Piemēram, atlasiet krājuma kodu 1000.</span><span class="sxs-lookup"><span data-stu-id="79239-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="79239-116">Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="79239-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="79239-117">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="79239-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="79239-118">Varat ignorēt atbilstības ierobežojumus, lai izmantotu ierobežojumu bez atbilstības, 2 virzienu atbilstību vai 3 virzienu atbilstību.</span><span class="sxs-lookup"><span data-stu-id="79239-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="79239-119">Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="79239-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="79239-120">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="79239-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="79239-121">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="79239-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="79239-122">Preču saņemšana</span><span class="sxs-lookup"><span data-stu-id="79239-122">Receive the products</span></span>
1. <span data-ttu-id="79239-123">Darbību rūtī noklikšķiniet uz Saņemt.</span><span class="sxs-lookup"><span data-stu-id="79239-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="79239-124">Noklikšķiniet uz Produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="79239-124">Click Product receipt.</span></span>
3. <span data-ttu-id="79239-125">Laukā Produktu ieejas plūsma ievadiet produktu ieejas plūsmas numuru.</span><span class="sxs-lookup"><span data-stu-id="79239-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="79239-126">Piemēram, ievadiet PR123.</span><span class="sxs-lookup"><span data-stu-id="79239-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="79239-127">Lai iegrāmatotu produktu ieejas plūsmu, noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="79239-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="79239-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="79239-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="79239-129">Kreditora rēķina izveidošana</span><span class="sxs-lookup"><span data-stu-id="79239-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="79239-130">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Pirkšanas pasūtījumi, kas saņemti, bet nav ierakstīti rēķinā.</span><span class="sxs-lookup"><span data-stu-id="79239-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="79239-131">Atlasiet pirkšanas pasūtījumu, kuru izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="79239-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="79239-132">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="79239-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="79239-133">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="79239-133">Click Invoice.</span></span>
5. <span data-ttu-id="79239-134">Ievadiet rēķina numuru laukā Numurs.</span><span class="sxs-lookup"><span data-stu-id="79239-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="79239-135">Laukā Rēķina apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="79239-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="79239-136">Laukā Rēķina datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="79239-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="79239-137">Laukā Vienības cena ievadiet 1200.</span><span class="sxs-lookup"><span data-stu-id="79239-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="79239-138">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="79239-138">Click Add line.</span></span>
10. <span data-ttu-id="79239-139">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="79239-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="79239-140">Sarakstā atrodiet instalācijas maksas krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="79239-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="79239-141">Piemēram, S0001</span><span class="sxs-lookup"><span data-stu-id="79239-141">For example, S0001</span></span>
12. <span data-ttu-id="79239-142">Atlasiet instalācijas maksas krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="79239-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="79239-143">Ņemiet vērā, ka kopš izmaiņu veikšanas salīdzināšana nav veikta.</span><span class="sxs-lookup"><span data-stu-id="79239-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="79239-144">Noklikšķiniet uz Atjaunināt atbilstības statusu.</span><span class="sxs-lookup"><span data-stu-id="79239-144">Click Update match status.</span></span>
14. <span data-ttu-id="79239-145">Darbību rūtī noklikšķiniet uz Pārskatīt.</span><span class="sxs-lookup"><span data-stu-id="79239-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="79239-146">Noklikšķiniet uz Detalizēta informācija par atbilstību.</span><span class="sxs-lookup"><span data-stu-id="79239-146">Click Matching details.</span></span>
    * <span data-ttu-id="79239-147">Nav nepieciešams noteikt atbilstību jaunai pakalpojumu rindai, tāpēc tās statuss paliek "Nav veikta".</span><span class="sxs-lookup"><span data-stu-id="79239-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="79239-148">Atlasiet produktu ieejas plūsmu krājuma vienībai, kuru esat saņēmis.</span><span class="sxs-lookup"><span data-stu-id="79239-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="79239-149">Rindai ar produktu ieejas plūsmu atbilstība tika noteikta, bet ir daudzuma vai cenas neatbilstība, tāpēc tā nav izdevusies.</span><span class="sxs-lookup"><span data-stu-id="79239-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="79239-150">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="79239-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="79239-151">Tagad vienības cena atbilst, statuss tiek atjaunināts uz Nokārtots.</span><span class="sxs-lookup"><span data-stu-id="79239-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="79239-152">Ja jūsu politika atļauj neatbilstības vai salīdzināšana ir tikai brīdinājums, rēķinu joprojām varat iegrāmatot.</span><span class="sxs-lookup"><span data-stu-id="79239-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="79239-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="79239-153">Close the page.</span></span>
19. <span data-ttu-id="79239-154">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="79239-154">Click Post.</span></span>
20. <span data-ttu-id="79239-155">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="79239-155">Close the form.</span></span>
    * <span data-ttu-id="79239-156">Ņemiet vērā, ka pirkšanas pasūtījuma norāde vairs neatbilst statusam, ka tas ir saņemts, bet rēķins nav izrakstīts.</span><span class="sxs-lookup"><span data-stu-id="79239-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


