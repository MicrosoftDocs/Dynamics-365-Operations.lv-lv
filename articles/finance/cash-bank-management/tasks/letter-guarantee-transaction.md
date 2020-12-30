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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445684"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="2ef5e-103">Garantijas vēstules darījums</span><span class="sxs-lookup"><span data-stu-id="2ef5e-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ef5e-104">Šajā procedūrā ir aprakstīts garantijas vēstules process.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="2ef5e-105">Pirms šīs procedūras jābūt pabeigtiem tālāk minētajiem uzdevumiem:</span><span class="sxs-lookup"><span data-stu-id="2ef5e-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="2ef5e-106">Iestatiet bankas iestādes un garantijas vēstules grāmatošanas profilus.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="2ef5e-107">Izveidojiet bankas iestādes līgumu garantijas vēstulei.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="2ef5e-108">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="2ef5e-109">Pārdošanas pasūtījuma ar garantijas vēstuli izveide</span><span class="sxs-lookup"><span data-stu-id="2ef5e-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="2ef5e-110">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="2ef5e-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-111">Click New.</span></span>
3. <span data-ttu-id="2ef5e-112">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="2ef5e-113">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-113">Expand the General section.</span></span>
5. <span data-ttu-id="2ef5e-114">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="2ef5e-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2ef5e-116">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="2ef5e-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2ef5e-118">Laukā Bankas dokumenta veids atlasiet Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="2ef5e-119">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-119">Click OK.</span></span>
11. <span data-ttu-id="2ef5e-120">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="2ef5e-121">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="2ef5e-122">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="2ef5e-123">Noklikšķiniet uz cilnes Piegāde.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="2ef5e-124">Piezīme. Atlasiet Piegādes datuma kontrole = Nav</span><span class="sxs-lookup"><span data-stu-id="2ef5e-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="2ef5e-125">Laukā Pieprasītais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="2ef5e-126">Laukā Apstiprinātais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="2ef5e-127">Garantijas vēstules pieprasījuma apstrāde</span><span class="sxs-lookup"><span data-stu-id="2ef5e-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="2ef5e-128">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="2ef5e-129">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="2ef5e-130">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="2ef5e-131">Noklikšķiniet uz Pieprasīt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="2ef5e-132">Laukā Veids ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="2ef5e-133">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2ef5e-134">Ievadiet skaitli laukā Vērtība.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="2ef5e-135">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="2ef5e-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-136">Click OK.</span></span>
10. <span data-ttu-id="2ef5e-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="2ef5e-138">Garantijas vēstules iesniegšanas bankā process</span><span class="sxs-lookup"><span data-stu-id="2ef5e-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="2ef5e-139">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="2ef5e-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2ef5e-141">Noklikšķiniet uz Iesniegt bankā, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="2ef5e-142">Ievadiet vai atlasiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="2ef5e-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2ef5e-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="2ef5e-145">Garantijas vēstules saņemšanas no bankas process</span><span class="sxs-lookup"><span data-stu-id="2ef5e-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="2ef5e-146">Noklikšķiniet uz Saņemt no bankas, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="2ef5e-147">Laukā Bankas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="2ef5e-148">Pārbaudiet laukā Uzcenojums un Izdevumi aprēķinātās vērtības.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="2ef5e-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-149">Click OK.</span></span>
4. <span data-ttu-id="2ef5e-150">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="2ef5e-151">Pārbaudiet ierakstu Saņemt no bankas.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="2ef5e-152">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="2ef5e-153">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-153">Click Lines.</span></span>
    * <span data-ttu-id="2ef5e-154">Pārbaudiet žurnāla ierakstu grāmatojumu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="2ef5e-155">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="2ef5e-156">Garantijas vēstules izsniegšanas saņēmējam process</span><span class="sxs-lookup"><span data-stu-id="2ef5e-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="2ef5e-157">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="2ef5e-158">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="2ef5e-159">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="2ef5e-160">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="2ef5e-161">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="2ef5e-162">Noklikšķiniet uz Nodot saņēmējam, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="2ef5e-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-163">Click OK.</span></span>
8. <span data-ttu-id="2ef5e-164">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="2ef5e-165">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="2ef5e-166">Noklikšķiniet uz Nodot saņēmējam, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="2ef5e-167">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-167">Click OK.</span></span>
12. <span data-ttu-id="2ef5e-168">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="2ef5e-169">Pārbaudiet ierakstu Nodot saņēmējam.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="2ef5e-170">Garantijas vēstules vērtības palielināšanas process</span><span class="sxs-lookup"><span data-stu-id="2ef5e-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="2ef5e-171">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="2ef5e-172">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="2ef5e-173">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="2ef5e-174">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="2ef5e-175">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="2ef5e-176">Noklikšķiniet uz Palielināt vērtību, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="2ef5e-177">Laukā Pievienojamā vērtība ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="2ef5e-178">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-178">Click OK.</span></span>
9. <span data-ttu-id="2ef5e-179">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="2ef5e-180">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="2ef5e-181">Noklikšķiniet uz Palielināt vērtību, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="2ef5e-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-182">Click OK.</span></span>
13. <span data-ttu-id="2ef5e-183">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="2ef5e-184">Pārbaudiet ierakstu Palielināt vērtību.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="2ef5e-185">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="2ef5e-186">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="2ef5e-187">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-187">Click Lines.</span></span>
    * <span data-ttu-id="2ef5e-188">Pārbaudiet grāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="2ef5e-189">Garantijas vēstules iznīcināšanas process</span><span class="sxs-lookup"><span data-stu-id="2ef5e-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="2ef5e-190">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="2ef5e-191">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="2ef5e-192">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="2ef5e-193">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="2ef5e-194">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="2ef5e-195">Noklikšķiniet uz Likvidēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="2ef5e-196">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-196">Click OK.</span></span>
8. <span data-ttu-id="2ef5e-197">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="2ef5e-198">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="2ef5e-199">Noklikšķiniet uz Likvidēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="2ef5e-200">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-200">Click OK.</span></span>
12. <span data-ttu-id="2ef5e-201">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="2ef5e-202">Pārbaudiet ierakstu Likvidēt.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="2ef5e-203">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="2ef5e-204">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="2ef5e-205">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-205">Click Lines.</span></span>
    * <span data-ttu-id="2ef5e-206">Pārbaudiet grāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="2ef5e-207">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2ef5e-207">Close the page.</span></span>

