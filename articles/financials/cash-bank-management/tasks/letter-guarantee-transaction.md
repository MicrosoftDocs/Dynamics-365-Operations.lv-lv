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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4dc6ee178121fae05d538f5103919442d91e65eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566114"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="a8b5a-103">Garantijas vēstules darījums</span><span class="sxs-lookup"><span data-stu-id="a8b5a-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8b5a-104">Šajā procedūrā ir aprakstīts garantijas vēstules process.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="a8b5a-105">Pirms šīs procedūras jābūt pabeigtiem tālāk minētajiem uzdevumiem:</span><span class="sxs-lookup"><span data-stu-id="a8b5a-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="a8b5a-106">Iestatiet bankas iestādes un garantijas vēstules grāmatošanas profilus.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="a8b5a-107">Izveidojiet bankas iestādes līgumu garantijas vēstulei.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="a8b5a-108">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="a8b5a-109">Pārdošanas pasūtījuma ar garantijas vēstuli izveide</span><span class="sxs-lookup"><span data-stu-id="a8b5a-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="a8b5a-110">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a8b5a-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-111">Click New.</span></span>
3. <span data-ttu-id="a8b5a-112">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="a8b5a-113">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-113">Expand the General section.</span></span>
5. <span data-ttu-id="a8b5a-114">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="a8b5a-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a8b5a-116">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="a8b5a-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a8b5a-118">Laukā Bankas dokumenta veids atlasiet Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="a8b5a-119">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-119">Click OK.</span></span>
11. <span data-ttu-id="a8b5a-120">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="a8b5a-121">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="a8b5a-122">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="a8b5a-123">Noklikšķiniet uz cilnes Piegāde.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="a8b5a-124">Piezīme. Atlasiet Piegādes datuma kontrole = Nav</span><span class="sxs-lookup"><span data-stu-id="a8b5a-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="a8b5a-125">Laukā Pieprasītais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="a8b5a-126">Laukā Apstiprinātais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="a8b5a-127">Garantijas vēstules pieprasījuma apstrāde</span><span class="sxs-lookup"><span data-stu-id="a8b5a-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="a8b5a-128">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="a8b5a-129">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="a8b5a-130">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="a8b5a-131">Noklikšķiniet uz Pieprasīt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="a8b5a-132">Laukā Veids ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="a8b5a-133">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a8b5a-134">Ievadiet skaitli laukā Vērtība.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="a8b5a-135">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="a8b5a-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-136">Click OK.</span></span>
10. <span data-ttu-id="a8b5a-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="a8b5a-138">Garantijas vēstules iesniegšanas bankā process</span><span class="sxs-lookup"><span data-stu-id="a8b5a-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="a8b5a-139">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="a8b5a-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a8b5a-141">Noklikšķiniet uz Iesniegt bankā, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="a8b5a-142">Ievadiet vai atlasiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="a8b5a-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a8b5a-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="a8b5a-145">Garantijas vēstules saņemšanas no bankas process</span><span class="sxs-lookup"><span data-stu-id="a8b5a-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="a8b5a-146">Noklikšķiniet uz Saņemt no bankas, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="a8b5a-147">Laukā Bankas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="a8b5a-148">Pārbaudiet laukā Uzcenojums un Izdevumi aprēķinātās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="a8b5a-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-149">Click OK.</span></span>
4. <span data-ttu-id="a8b5a-150">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="a8b5a-151">Pārbaudiet ierakstu Saņemt no bankas.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="a8b5a-152">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="a8b5a-153">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-153">Click Lines.</span></span>
    * <span data-ttu-id="a8b5a-154">Pārbaudiet žurnāla ierakstu grāmatojumu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="a8b5a-155">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="a8b5a-156">Garantijas vēstules izsniegšanas saņēmējam process</span><span class="sxs-lookup"><span data-stu-id="a8b5a-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="a8b5a-157">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a8b5a-158">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="a8b5a-159">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="a8b5a-160">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="a8b5a-161">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="a8b5a-162">Noklikšķiniet uz Nodot saņēmējam, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="a8b5a-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-163">Click OK.</span></span>
8. <span data-ttu-id="a8b5a-164">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="a8b5a-165">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a8b5a-166">Noklikšķiniet uz Nodot saņēmējam, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="a8b5a-167">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-167">Click OK.</span></span>
12. <span data-ttu-id="a8b5a-168">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="a8b5a-169">Pārbaudiet ierakstu Nodot saņēmējam.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="a8b5a-170">Garantijas vēstules vērtības palielināšanas process</span><span class="sxs-lookup"><span data-stu-id="a8b5a-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="a8b5a-171">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a8b5a-172">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="a8b5a-173">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="a8b5a-174">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="a8b5a-175">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="a8b5a-176">Noklikšķiniet uz Palielināt vērtību, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="a8b5a-177">Laukā Pievienojamā vērtība ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="a8b5a-178">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-178">Click OK.</span></span>
9. <span data-ttu-id="a8b5a-179">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="a8b5a-180">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="a8b5a-181">Noklikšķiniet uz Palielināt vērtību, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="a8b5a-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-182">Click OK.</span></span>
13. <span data-ttu-id="a8b5a-183">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="a8b5a-184">Pārbaudiet ierakstu Palielināt vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="a8b5a-185">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a8b5a-186">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="a8b5a-187">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-187">Click Lines.</span></span>
    * <span data-ttu-id="a8b5a-188">Pārbaudiet grāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="a8b5a-189">Garantijas vēstules iznīcināšanas process</span><span class="sxs-lookup"><span data-stu-id="a8b5a-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="a8b5a-190">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a8b5a-191">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="a8b5a-192">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="a8b5a-193">Noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="a8b5a-194">Darbību rūtī noklikšķiniet uz Garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="a8b5a-195">Noklikšķiniet uz Likvidēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="a8b5a-196">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-196">Click OK.</span></span>
8. <span data-ttu-id="a8b5a-197">Dodieties uz Kases un bankas vadība > Garantijas vēstules > Garantijas vēstules.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="a8b5a-198">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a8b5a-199">Noklikšķiniet uz Likvidēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="a8b5a-200">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-200">Click OK.</span></span>
12. <span data-ttu-id="a8b5a-201">Izvērsiet sadaļu Darbības.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="a8b5a-202">Pārbaudiet ierakstu Likvidēt.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="a8b5a-203">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a8b5a-204">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="a8b5a-205">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-205">Click Lines.</span></span>
    * <span data-ttu-id="a8b5a-206">Pārbaudiet grāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="a8b5a-207">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a8b5a-207">Close the page.</span></span>

