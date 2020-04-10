---
title: Garantijas vēstules darījums
description: Šajā procedūrā ir aprakstīts garantijas vēstules process.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141791"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="18d32-103">Garantijas vēstules darījums</span><span class="sxs-lookup"><span data-stu-id="18d32-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18d32-104">Šajā procedūrā ir aprakstīts garantijas vēstules process.</span><span class="sxs-lookup"><span data-stu-id="18d32-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="18d32-105">Pirms šīs procedūras jābūt pabeigtiem tālāk minētajiem uzdevumiem:</span><span class="sxs-lookup"><span data-stu-id="18d32-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="18d32-106">Iestatiet bankas iestādes un garantijas vēstules grāmatošanas profilus.</span><span class="sxs-lookup"><span data-stu-id="18d32-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="18d32-107">Izveidojiet bankas iestādes līgumu garantijas vēstulei.</span><span class="sxs-lookup"><span data-stu-id="18d32-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="18d32-108">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="18d32-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="18d32-109">Pārdošanas pasūtījuma ar garantijas vēstuli izveide</span><span class="sxs-lookup"><span data-stu-id="18d32-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="18d32-110">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="18d32-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="18d32-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="18d32-111">Click New.</span></span>
3. <span data-ttu-id="18d32-112">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="18d32-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="18d32-113">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="18d32-113">Expand the General section.</span></span>
5. <span data-ttu-id="18d32-114">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="18d32-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="18d32-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d32-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="18d32-116">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="18d32-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="18d32-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d32-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="18d32-118">Laukā Bankas dokumenta veids atlasiet Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="18d32-119">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="18d32-119">Click OK.</span></span>
11. <span data-ttu-id="18d32-120">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="18d32-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="18d32-121">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="18d32-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="18d32-122">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="18d32-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="18d32-123">Noklikšķiniet uz cilnes Piegāde.</span><span class="sxs-lookup"><span data-stu-id="18d32-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="18d32-124">Piezīme. Atlasiet Piegādes datuma kontrole = Nav</span><span class="sxs-lookup"><span data-stu-id="18d32-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="18d32-125">Laukā Pieprasītais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="18d32-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="18d32-126">Laukā Apstiprinātais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="18d32-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="18d32-127">Garantijas vēstules pieprasījuma apstrāde</span><span class="sxs-lookup"><span data-stu-id="18d32-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="18d32-128">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="18d32-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="18d32-129">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="18d32-130">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="18d32-131">Noklikšķiniet uz Pieprasīt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="18d32-132">Laukā Veids ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="18d32-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="18d32-133">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d32-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="18d32-134">Ievadiet skaitli laukā Vērtība.</span><span class="sxs-lookup"><span data-stu-id="18d32-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="18d32-135">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="18d32-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="18d32-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-136">Click OK.</span></span>
10. <span data-ttu-id="18d32-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="18d32-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="18d32-138">Garantijas vēstules iesniegšanas bankā process</span><span class="sxs-lookup"><span data-stu-id="18d32-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="18d32-139">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="18d32-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="18d32-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d32-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="18d32-141">Noklikšķiniet uz Iesniegt bankā, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="18d32-142">Ievadiet vai atlasiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="18d32-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="18d32-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d32-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="18d32-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="18d32-145">Garantijas vēstules saņemšanas no bankas process</span><span class="sxs-lookup"><span data-stu-id="18d32-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="18d32-146">Noklikšķiniet uz Saņemt no bankas, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="18d32-147">Laukā Bankas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="18d32-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="18d32-148">Pārbaudiet laukā Uzcenojums un Izdevumi aprēķinātās vērtības.</span><span class="sxs-lookup"><span data-stu-id="18d32-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="18d32-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-149">Click OK.</span></span>
4. <span data-ttu-id="18d32-150">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="18d32-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="18d32-151">Pārbaudiet ierakstu Saņemt no bankas.</span><span class="sxs-lookup"><span data-stu-id="18d32-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="18d32-152">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="18d32-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="18d32-153">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="18d32-153">Click Lines.</span></span>
    * <span data-ttu-id="18d32-154">Pārbaudiet žurnāla ierakstu grāmatojumu.</span><span class="sxs-lookup"><span data-stu-id="18d32-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="18d32-155">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="18d32-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="18d32-156">Garantijas vēstules izsniegšanas saņēmējam process</span><span class="sxs-lookup"><span data-stu-id="18d32-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="18d32-157">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="18d32-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="18d32-158">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d32-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="18d32-159">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="18d32-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="18d32-160">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="18d32-161">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="18d32-162">Noklikšķiniet uz Nodot saņēmējam, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="18d32-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-163">Click OK.</span></span>
8. <span data-ttu-id="18d32-164">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="18d32-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="18d32-165">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d32-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="18d32-166">Noklikšķiniet uz Nodot saņēmējam, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="18d32-167">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-167">Click OK.</span></span>
12. <span data-ttu-id="18d32-168">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="18d32-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="18d32-169">Pārbaudiet ierakstu Nodot saņēmējam.</span><span class="sxs-lookup"><span data-stu-id="18d32-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="18d32-170">Garantijas vēstules vērtības palielināšanas process</span><span class="sxs-lookup"><span data-stu-id="18d32-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="18d32-171">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="18d32-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="18d32-172">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d32-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="18d32-173">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="18d32-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="18d32-174">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="18d32-175">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="18d32-176">Noklikšķiniet uz Palielināt vērtību, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="18d32-177">Laukā Pievienojamā vērtība ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="18d32-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="18d32-178">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-178">Click OK.</span></span>
9. <span data-ttu-id="18d32-179">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="18d32-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="18d32-180">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d32-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="18d32-181">Noklikšķiniet uz Palielināt vērtību, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="18d32-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-182">Click OK.</span></span>
13. <span data-ttu-id="18d32-183">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="18d32-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="18d32-184">Pārbaudiet ierakstu Palielināt vērtību.</span><span class="sxs-lookup"><span data-stu-id="18d32-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="18d32-185">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d32-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="18d32-186">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="18d32-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="18d32-187">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="18d32-187">Click Lines.</span></span>
    * <span data-ttu-id="18d32-188">Pārbaudiet grāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="18d32-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="18d32-189">Garantijas vēstules iznīcināšanas process</span><span class="sxs-lookup"><span data-stu-id="18d32-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="18d32-190">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="18d32-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="18d32-191">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d32-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="18d32-192">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="18d32-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="18d32-193">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="18d32-194">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="18d32-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="18d32-195">Noklikšķiniet uz Likvidēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="18d32-196">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-196">Click OK.</span></span>
8. <span data-ttu-id="18d32-197">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="18d32-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="18d32-198">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d32-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="18d32-199">Noklikšķiniet uz Likvidēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="18d32-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="18d32-200">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d32-200">Click OK.</span></span>
12. <span data-ttu-id="18d32-201">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="18d32-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="18d32-202">Pārbaudiet ierakstu Likvidēt.</span><span class="sxs-lookup"><span data-stu-id="18d32-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="18d32-203">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d32-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="18d32-204">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="18d32-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="18d32-205">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="18d32-205">Click Lines.</span></span>
    * <span data-ttu-id="18d32-206">Pārbaudiet grāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="18d32-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="18d32-207">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="18d32-207">Close the page.</span></span>

