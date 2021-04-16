---
title: Kredītvēstules eksportēšana
description: Šajā procedūrā ir aprakstīts kredītvēstules eksportēšanas process.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 260ef2d05e1f21708817346af2db2841aa6acdd9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834792"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="93f6e-103">Kredītvēstules eksportēšana</span><span class="sxs-lookup"><span data-stu-id="93f6e-103">Export letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93f6e-104">Šajā procedūrā ir aprakstīts kredītvēstules eksportēšanas process.</span><span class="sxs-lookup"><span data-stu-id="93f6e-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="93f6e-105">Kredītvēstule ir līgums, ko izsniedz banka un kurā banka piekrīt veikt maksājumu pircēja vārdā, ja tiek izpildīti starp pircēju un pārdevēju noslēgtā līguma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="93f6e-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="93f6e-106">Pirms šīs procedūras izpildiet procedūru Bankas iestāžu iestatīšana un metožu grāmatošana un Kredītvēstule_Bankas iestādes līguma izveide.</span><span class="sxs-lookup"><span data-stu-id="93f6e-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="93f6e-107">Lai sekmīgi izpildītu šo procedūru, jāatlasa demonstrācijas uzņēmums “USMF”.</span><span class="sxs-lookup"><span data-stu-id="93f6e-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="93f6e-108">Pārdošanas pasūtījuma izveide kredītvēstules eksportēšanai</span><span class="sxs-lookup"><span data-stu-id="93f6e-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="93f6e-109">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="93f6e-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="93f6e-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="93f6e-110">Click New.</span></span>
3. <span data-ttu-id="93f6e-111">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="93f6e-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="93f6e-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="93f6e-114">Izvērsiet vai sakļaujiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="93f6e-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="93f6e-115">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="93f6e-116">Atlasiet vietu, kur krājums ir jāuzkrāj.</span><span class="sxs-lookup"><span data-stu-id="93f6e-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="93f6e-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="93f6e-118">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="93f6e-119">Atlasiet noliktavu, kur izsniedzamais krājums ir jāuzkrāj.</span><span class="sxs-lookup"><span data-stu-id="93f6e-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="93f6e-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93f6e-121">Ņemiet vērā! Jābūt atlasītam laukam Bankas dokumenta tips un vērtībai Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="93f6e-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="93f6e-122">Laukā Bankas dokumenta veids atlasiet Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="93f6e-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="93f6e-123">Izvērsiet vai sakļaujiet sadaļu Piegāde.</span><span class="sxs-lookup"><span data-stu-id="93f6e-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="93f6e-124">Atlasiet Piegādes datuma kontrole = Nav.</span><span class="sxs-lookup"><span data-stu-id="93f6e-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="93f6e-125">Laukā Pieprasītais saņemšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="93f6e-126">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="93f6e-126">Click OK.</span></span>
15. <span data-ttu-id="93f6e-127">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="93f6e-128">Atlasiet vajadzīgo krājumu, jas ir jāizdod/jāpārdod.</span><span class="sxs-lookup"><span data-stu-id="93f6e-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="93f6e-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="93f6e-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="93f6e-131">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="93f6e-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="93f6e-132">Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="93f6e-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="93f6e-133">Noklikšķiniet uz cilnes Piegāde.</span><span class="sxs-lookup"><span data-stu-id="93f6e-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="93f6e-134">Laukā Pieprasītais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="93f6e-135">Laukā Apstiprinātais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="93f6e-136">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="93f6e-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="93f6e-137">Noklikšķiniet uz Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="93f6e-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="93f6e-138">Laukā Bankas dokumenta numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="93f6e-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="93f6e-139">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="93f6e-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="93f6e-140">Izvērsiet vai sakļaujiet sadaļu Detalizēta informācija par banku.</span><span class="sxs-lookup"><span data-stu-id="93f6e-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="93f6e-141">Laukā Izdevēja banka noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="93f6e-142">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="93f6e-143">Laukā Konsultatīvā banka noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="93f6e-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="93f6e-145">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="93f6e-146">Noklikšķiniet uz Iegūt pārdošanas pasūtījumu kravas.</span><span class="sxs-lookup"><span data-stu-id="93f6e-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="93f6e-147">Noklikšķiniet uz Izsniegt bankas dokumentu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="93f6e-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="93f6e-149">Pavadzīmes grāmatošana</span><span class="sxs-lookup"><span data-stu-id="93f6e-149">Post Packing slip</span></span>
1. <span data-ttu-id="93f6e-150">Darbību rūtī noklikšķiniet uz Izdot un iepakot.</span><span class="sxs-lookup"><span data-stu-id="93f6e-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="93f6e-151">Noklikšķiniet uz Grāmatot pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="93f6e-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="93f6e-152">Izvērsiet vai sakļaujiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="93f6e-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="93f6e-153">Laukā Daudzums atlasiet vērtību “Visi”.</span><span class="sxs-lookup"><span data-stu-id="93f6e-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="93f6e-154">Izvērsiet vai sakļaujiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="93f6e-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="93f6e-155">Laukā Pavadzīmes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="93f6e-156">Atlasiet Sūtīšanas numurs.</span><span class="sxs-lookup"><span data-stu-id="93f6e-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="93f6e-157">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="93f6e-158">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="93f6e-158">Click OK.</span></span>
10. <span data-ttu-id="93f6e-159">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="93f6e-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="93f6e-160">Pārdošanas rēķina grāmatošana</span><span class="sxs-lookup"><span data-stu-id="93f6e-160">Post sales invoice</span></span>
1. <span data-ttu-id="93f6e-161">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="93f6e-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="93f6e-162">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="93f6e-162">Click Invoice.</span></span>
3. <span data-ttu-id="93f6e-163">Izvērsiet vai sakļaujiet sadaļu Pārskats.</span><span class="sxs-lookup"><span data-stu-id="93f6e-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="93f6e-164">Atlasiet Sūtīšanas numurs.</span><span class="sxs-lookup"><span data-stu-id="93f6e-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="93f6e-165">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="93f6e-166">Izvērsiet vai sakļaujiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="93f6e-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="93f6e-167">Laukā Rēķina datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="93f6e-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="93f6e-168">Click OK.</span></span>
9. <span data-ttu-id="93f6e-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="93f6e-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="93f6e-170">Iesniegtā sūtījuma dokumenta statuss</span><span class="sxs-lookup"><span data-stu-id="93f6e-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="93f6e-171">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="93f6e-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="93f6e-172">Noklikšķiniet uz Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="93f6e-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="93f6e-173">Izvērsiet vai sakļaujiet sadaļu Rindas.</span><span class="sxs-lookup"><span data-stu-id="93f6e-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="93f6e-174">Piezīme. Laukam Iesniegtais dokuments jāiestata Jā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="93f6e-175">Kredītvēstules eksportēšanas pārbaude</span><span class="sxs-lookup"><span data-stu-id="93f6e-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="93f6e-176">Dodieties uz Kases un bankas vadība > Akreditīvi > Eksporta akreditatīva un importa iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="93f6e-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="93f6e-177">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="93f6e-178">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93f6e-179">Pārbaudiet, vai lauka Kredītvēstule vienuma Sūtījums statuss ir Iekļauts rēķinā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="93f6e-180">Debitora maksājums</span><span class="sxs-lookup"><span data-stu-id="93f6e-180">Customer payment</span></span>
1. <span data-ttu-id="93f6e-181">Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="93f6e-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="93f6e-182">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="93f6e-182">Click New.</span></span>
3. <span data-ttu-id="93f6e-183">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="93f6e-184">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="93f6e-185">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="93f6e-186">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="93f6e-186">Click Lines.</span></span>
7. <span data-ttu-id="93f6e-187">Laukā Datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="93f6e-188">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="93f6e-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="93f6e-189">Noklikšķiniet uz Nosegšana.</span><span class="sxs-lookup"><span data-stu-id="93f6e-189">Click Settlement.</span></span>
10. <span data-ttu-id="93f6e-190">Atzīmējiet izvēles rūtiņu, kura atrodas lauka Kopsummas galvenē.</span><span class="sxs-lookup"><span data-stu-id="93f6e-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="93f6e-191">Piezīme. Laukam Rādīt iestatiet Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="93f6e-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="93f6e-192">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="93f6e-193">Atzīmējiet vai notīriet izvēles rūtiņu Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="93f6e-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="93f6e-194">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="93f6e-194">Click OK.</span></span>
14. <span data-ttu-id="93f6e-195">Noklikšķiniet uz cilnes Maksājums.</span><span class="sxs-lookup"><span data-stu-id="93f6e-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="93f6e-196">Bankas dokumenta numura un sūtījuma numura detalizētas informācijas pārbaude</span><span class="sxs-lookup"><span data-stu-id="93f6e-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="93f6e-197">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="93f6e-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="93f6e-198">Kredītvēstules eksportēšanas pārbaude pēc maksājuma izpildes</span><span class="sxs-lookup"><span data-stu-id="93f6e-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="93f6e-199">Dodieties uz Kases un bankas vadība > Akreditīvi > Eksporta akreditatīva un importa iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="93f6e-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="93f6e-200">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="93f6e-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="93f6e-201">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="93f6e-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93f6e-202">Pārbaudiet: Sūtījuma statuss = Maksājums saņemts un bilances summa = 0,00.</span><span class="sxs-lookup"><span data-stu-id="93f6e-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]