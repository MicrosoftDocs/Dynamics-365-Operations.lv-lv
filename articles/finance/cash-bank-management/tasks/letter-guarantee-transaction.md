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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 566849cfcedd29f4bb92d08a17b67e16b1cbc372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225373"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="aa4ca-103">Garantijas vēstules darījums</span><span class="sxs-lookup"><span data-stu-id="aa4ca-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa4ca-104">Šajā procedūrā ir aprakstīts garantijas vēstules process.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="aa4ca-105">Pirms šīs procedūras jābūt pabeigtiem tālāk minētajiem uzdevumiem:</span><span class="sxs-lookup"><span data-stu-id="aa4ca-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="aa4ca-106">Iestatiet bankas iestādes un garantijas vēstules grāmatošanas profilus.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="aa4ca-107">Izveidojiet bankas iestādes līgumu garantijas vēstulei.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="aa4ca-108">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="aa4ca-109">Pārdošanas pasūtījuma ar garantijas vēstuli izveide</span><span class="sxs-lookup"><span data-stu-id="aa4ca-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="aa4ca-110">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="aa4ca-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-111">Click New.</span></span>
3. <span data-ttu-id="aa4ca-112">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="aa4ca-113">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-113">Expand the General section.</span></span>
5. <span data-ttu-id="aa4ca-114">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="aa4ca-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="aa4ca-116">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="aa4ca-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="aa4ca-118">Laukā Bankas dokumenta veids atlasiet Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="aa4ca-119">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-119">Click OK.</span></span>
11. <span data-ttu-id="aa4ca-120">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="aa4ca-121">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="aa4ca-122">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="aa4ca-123">Noklikšķiniet uz cilnes Piegāde.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="aa4ca-124">Piezīme. Atlasiet Piegādes datuma kontrole = Nav</span><span class="sxs-lookup"><span data-stu-id="aa4ca-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="aa4ca-125">Laukā Pieprasītais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="aa4ca-126">Laukā Apstiprinātais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="aa4ca-127">Garantijas vēstules pieprasījuma apstrāde</span><span class="sxs-lookup"><span data-stu-id="aa4ca-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="aa4ca-128">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="aa4ca-129">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="aa4ca-130">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="aa4ca-131">Noklikšķiniet uz Pieprasīt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="aa4ca-132">Laukā Veids ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="aa4ca-133">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="aa4ca-134">Ievadiet skaitli laukā Vērtība.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="aa4ca-135">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="aa4ca-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-136">Click OK.</span></span>
10. <span data-ttu-id="aa4ca-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="aa4ca-138">Garantijas vēstules iesniegšanas bankā process</span><span class="sxs-lookup"><span data-stu-id="aa4ca-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="aa4ca-139">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="aa4ca-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="aa4ca-141">Noklikšķiniet uz Iesniegt bankā, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="aa4ca-142">Ievadiet vai atlasiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="aa4ca-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="aa4ca-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="aa4ca-145">Garantijas vēstules saņemšanas no bankas process</span><span class="sxs-lookup"><span data-stu-id="aa4ca-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="aa4ca-146">Noklikšķiniet uz Saņemt no bankas, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="aa4ca-147">Laukā Bankas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="aa4ca-148">Pārbaudiet laukā Uzcenojums un Izdevumi aprēķinātās vērtības.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="aa4ca-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-149">Click OK.</span></span>
4. <span data-ttu-id="aa4ca-150">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="aa4ca-151">Pārbaudiet ierakstu Saņemt no bankas.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="aa4ca-152">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="aa4ca-153">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-153">Click Lines.</span></span>
    * <span data-ttu-id="aa4ca-154">Pārbaudiet žurnāla ierakstu grāmatojumu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="aa4ca-155">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="aa4ca-156">Garantijas vēstules izsniegšanas saņēmējam process</span><span class="sxs-lookup"><span data-stu-id="aa4ca-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="aa4ca-157">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="aa4ca-158">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="aa4ca-159">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="aa4ca-160">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="aa4ca-161">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="aa4ca-162">Noklikšķiniet uz Nodot saņēmējam, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="aa4ca-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-163">Click OK.</span></span>
8. <span data-ttu-id="aa4ca-164">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="aa4ca-165">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="aa4ca-166">Noklikšķiniet uz Nodot saņēmējam, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="aa4ca-167">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-167">Click OK.</span></span>
12. <span data-ttu-id="aa4ca-168">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="aa4ca-169">Pārbaudiet ierakstu Nodot saņēmējam.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="aa4ca-170">Garantijas vēstules vērtības palielināšanas process</span><span class="sxs-lookup"><span data-stu-id="aa4ca-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="aa4ca-171">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="aa4ca-172">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="aa4ca-173">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="aa4ca-174">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="aa4ca-175">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="aa4ca-176">Noklikšķiniet uz Palielināt vērtību, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="aa4ca-177">Laukā Pievienojamā vērtība ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="aa4ca-178">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-178">Click OK.</span></span>
9. <span data-ttu-id="aa4ca-179">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="aa4ca-180">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="aa4ca-181">Noklikšķiniet uz Palielināt vērtību, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="aa4ca-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-182">Click OK.</span></span>
13. <span data-ttu-id="aa4ca-183">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="aa4ca-184">Pārbaudiet ierakstu Palielināt vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="aa4ca-185">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="aa4ca-186">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="aa4ca-187">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-187">Click Lines.</span></span>
    * <span data-ttu-id="aa4ca-188">Pārbaudiet grāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="aa4ca-189">Garantijas vēstules iznīcināšanas process</span><span class="sxs-lookup"><span data-stu-id="aa4ca-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="aa4ca-190">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="aa4ca-191">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="aa4ca-192">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="aa4ca-193">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="aa4ca-194">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="aa4ca-195">Noklikšķiniet uz Likvidēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="aa4ca-196">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-196">Click OK.</span></span>
8. <span data-ttu-id="aa4ca-197">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="aa4ca-198">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="aa4ca-199">Noklikšķiniet uz Likvidēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="aa4ca-200">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-200">Click OK.</span></span>
12. <span data-ttu-id="aa4ca-201">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="aa4ca-202">Pārbaudiet ierakstu Likvidēt.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="aa4ca-203">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="aa4ca-204">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="aa4ca-205">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-205">Click Lines.</span></span>
    * <span data-ttu-id="aa4ca-206">Pārbaudiet grāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="aa4ca-207">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="aa4ca-207">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]