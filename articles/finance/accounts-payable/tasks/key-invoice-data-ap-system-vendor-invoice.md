---
title: Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu
description: Šis uzdevuma ceļvedis palīdzēs izveidot kreditora rēķinu no pirkšanas pasūtījuma un apskatīt pirkšanas pasūtījuma, kvīts un rēķina saskaņošanas rezultātus (3 virzienu atbilstība).
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20a058eb17bcab11056c91ab3570d6cd5b84b631
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227212"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="7a63a-103">Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu</span><span class="sxs-lookup"><span data-stu-id="7a63a-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a63a-104">Šis uzdevuma ceļvedis palīdzēs izveidot kreditora rēķinu no pirkšanas pasūtījuma un apskatīt pirkšanas pasūtījuma, kvīts un rēķina saskaņošanas rezultātus (3 virzienu atbilstība).</span><span class="sxs-lookup"><span data-stu-id="7a63a-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="7a63a-105">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="7a63a-105">Create a purchase order</span></span>
1. <span data-ttu-id="7a63a-106">Navigācijas rūtī dodieties uz **Moduļi > Kreditori > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="7a63a-107">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-107">Click **New**.</span></span>
3. <span data-ttu-id="7a63a-108">Laukā **Kreditora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7a63a-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7a63a-109">Atrodiet kreditoru, kuru atlasīt.</span><span class="sxs-lookup"><span data-stu-id="7a63a-109">Find a vendor to select.</span></span> <span data-ttu-id="7a63a-110">Piemēram, ritiniet uz leju līdz US-104.</span><span class="sxs-lookup"><span data-stu-id="7a63a-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="7a63a-111">Atlasiet kreditoru US-104.</span><span class="sxs-lookup"><span data-stu-id="7a63a-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="7a63a-112">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-112">Click **OK**.</span></span>
7. <span data-ttu-id="7a63a-113">Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7a63a-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7a63a-114">Atlasiet krājuma vienību.</span><span class="sxs-lookup"><span data-stu-id="7a63a-114">Select an inventory item.</span></span> <span data-ttu-id="7a63a-115">Piemēram, atlasiet krājuma kodu 1000.</span><span class="sxs-lookup"><span data-stu-id="7a63a-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="7a63a-116">Izvērsiet kopsavilkuma cilni **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="7a63a-117">Noklikšķiniet uz cilnes **Iestatīšana**. Varat ignorēt atbilstības ierobežojumus, lai izmantotu ierobežojumu bez atbilstības, 2 virzienu atbilstību vai 3 virzienu atbilstību.</span><span class="sxs-lookup"><span data-stu-id="7a63a-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="7a63a-118">Darbību rūtī noklikšķ. uz **Pirkšana**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="7a63a-119">Noklikšķiniet uz **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="7a63a-120">Preču saņemšana</span><span class="sxs-lookup"><span data-stu-id="7a63a-120">Receive the products</span></span>
1. <span data-ttu-id="7a63a-121">Darbību rūtī noklikšķ. uz **Saņemt**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="7a63a-122">Nokl. **Pr. ieejas pl**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="7a63a-123">Laukā **Produktu ieejas plūsma** ievadiet produktu ieejas plūsmas numuru.</span><span class="sxs-lookup"><span data-stu-id="7a63a-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="7a63a-124">Piemēram, ievadiet PR123.</span><span class="sxs-lookup"><span data-stu-id="7a63a-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="7a63a-125">Lai iegrāmatotu produktu ieejas plūsmu, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="7a63a-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a63a-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="7a63a-127">Kreditora rēķina izveidošana</span><span class="sxs-lookup"><span data-stu-id="7a63a-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="7a63a-128">Navigācijas rūtī dodieties uz **Moduļi > Kreditori > Pirkšanas pasūtījumi > Pirkšanas pasūtījumi, kas ir saņemti, bet kam nav izveidots rēķins**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="7a63a-129">Atlasiet pirkšanas pasūtījumu, kuru izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="7a63a-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="7a63a-130">Darbību rūtī noklikšķiniet uz **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="7a63a-131">Noklikšķiniet uz **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="7a63a-132">Ievadiet rēķina numuru laukā **Numurs**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="7a63a-133">Laukā **Rēķina apraksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7a63a-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="7a63a-134">Ievadiet datumu laukā **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="7a63a-135">Laukā **Vienības cena** ievadiet 1200.</span><span class="sxs-lookup"><span data-stu-id="7a63a-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="7a63a-136">Nokl. **Piev. r.**</span><span class="sxs-lookup"><span data-stu-id="7a63a-136">Click **Add line**.</span></span>
10. <span data-ttu-id="7a63a-137">Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7a63a-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7a63a-138">Sarakstā atrodiet instalācijas maksas krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="7a63a-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="7a63a-139">Piemēram, S0001</span><span class="sxs-lookup"><span data-stu-id="7a63a-139">For example, S0001</span></span>
12. <span data-ttu-id="7a63a-140">Atlasiet instalācijas maksas krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="7a63a-140">Select the installation charge item number.</span></span> <span data-ttu-id="7a63a-141">Ņemiet vērā, ka kopš izmaiņu veikšanas salīdzināšana nav veikta.</span><span class="sxs-lookup"><span data-stu-id="7a63a-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="7a63a-142">Noklikšķiniet uz **Atjaunināt atbilstības statusu**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="7a63a-143">Darbību rūtī nokl. uz **Pārskatīt**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="7a63a-144">Nokl. **Atb. det. inf**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-144">Click **Matching details**.</span></span> <span data-ttu-id="7a63a-145">Nav nepieciešams noteikt atbilstību jaunai pakalpojumu rindai, tāpēc tās statuss paliek "Nav veikta".</span><span class="sxs-lookup"><span data-stu-id="7a63a-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="7a63a-146">Atlasiet produktu ieejas plūsmu krājuma vienībai, kuru esat saņēmis.</span><span class="sxs-lookup"><span data-stu-id="7a63a-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="7a63a-147">Rindai ar produktu ieejas plūsmu atbilstība tika noteikta, bet ir daudzuma vai cenas neatbilstība, tāpēc tā nav izdevusies.</span><span class="sxs-lookup"><span data-stu-id="7a63a-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="7a63a-148">Laukā **Vienības cena** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="7a63a-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="7a63a-149">Tagad vienības cena atbilst, statuss tiek atjaunināts uz Nokārtots.</span><span class="sxs-lookup"><span data-stu-id="7a63a-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="7a63a-150">Ja jūsu politika atļauj neatbilstības vai salīdzināšana ir tikai brīdinājums, rēķinu joprojām varat iegrāmatot.</span><span class="sxs-lookup"><span data-stu-id="7a63a-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="7a63a-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a63a-151">Close the page.</span></span>
19. <span data-ttu-id="7a63a-152">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="7a63a-152">Click **Post**.</span></span>
20. <span data-ttu-id="7a63a-153">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="7a63a-153">Close the form.</span></span> <span data-ttu-id="7a63a-154">Ņemiet vērā, ka pirkšanas pasūtījuma norāde vairs neatbilst statusam, ka tas ir saņemts, bet rēķins nav izrakstīts.</span><span class="sxs-lookup"><span data-stu-id="7a63a-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]