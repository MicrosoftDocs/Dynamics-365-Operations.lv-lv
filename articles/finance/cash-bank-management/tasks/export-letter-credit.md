---
title: Kredītvēstules eksportēšana
description: Šajā procedūrā ir aprakstīts kredītvēstules eksportēšanas process.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b46ba174d658d27f5349762f3314ea8110490d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976395"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="279f9-103">Kredītvēstules eksportēšana</span><span class="sxs-lookup"><span data-stu-id="279f9-103">Export letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="279f9-104">Šajā procedūrā ir aprakstīts kredītvēstules eksportēšanas process.</span><span class="sxs-lookup"><span data-stu-id="279f9-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="279f9-105">Kredītvēstule ir līgums, ko izsniedz banka un kurā banka piekrīt veikt maksājumu pircēja vārdā, ja tiek izpildīti starp pircēju un pārdevēju noslēgtā līguma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="279f9-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="279f9-106">Pirms šīs procedūras izpildiet procedūru Bankas iestāžu iestatīšana un metožu grāmatošana un Kredītvēstule_Bankas iestādes līguma izveide.</span><span class="sxs-lookup"><span data-stu-id="279f9-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="279f9-107">Lai sekmīgi izpildītu šo procedūru, jāatlasa demonstrācijas uzņēmums “USMF”.</span><span class="sxs-lookup"><span data-stu-id="279f9-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="279f9-108">Pārdošanas pasūtījuma izveide kredītvēstules eksportēšanai</span><span class="sxs-lookup"><span data-stu-id="279f9-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="279f9-109">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="279f9-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="279f9-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="279f9-110">Click New.</span></span>
3. <span data-ttu-id="279f9-111">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="279f9-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="279f9-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="279f9-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="279f9-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="279f9-114">Izvērsiet vai sakļaujiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="279f9-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="279f9-115">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="279f9-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="279f9-116">Atlasiet vietu, kur krājums ir jāuzkrāj.</span><span class="sxs-lookup"><span data-stu-id="279f9-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="279f9-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="279f9-118">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="279f9-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="279f9-119">Atlasiet noliktavu, kur izsniedzamais krājums ir jāuzkrāj.</span><span class="sxs-lookup"><span data-stu-id="279f9-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="279f9-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="279f9-121">Ņemiet vērā! Jābūt atlasītam laukam Bankas dokumenta tips un vērtībai Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="279f9-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="279f9-122">Laukā Bankas dokumenta veids atlasiet Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="279f9-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="279f9-123">Izvērsiet vai sakļaujiet sadaļu Piegāde.</span><span class="sxs-lookup"><span data-stu-id="279f9-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="279f9-124">Atlasiet Piegādes datuma kontrole = Nav.</span><span class="sxs-lookup"><span data-stu-id="279f9-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="279f9-125">Laukā Pieprasītais saņemšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="279f9-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="279f9-126">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="279f9-126">Click OK.</span></span>
15. <span data-ttu-id="279f9-127">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="279f9-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="279f9-128">Atlasiet vajadzīgo krājumu, jas ir jāizdod/jāpārdod.</span><span class="sxs-lookup"><span data-stu-id="279f9-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="279f9-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="279f9-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="279f9-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="279f9-131">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="279f9-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="279f9-132">Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="279f9-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="279f9-133">Noklikšķiniet uz cilnes Piegāde.</span><span class="sxs-lookup"><span data-stu-id="279f9-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="279f9-134">Laukā Pieprasītais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="279f9-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="279f9-135">Laukā Apstiprinātais nosūtīšanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="279f9-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="279f9-136">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="279f9-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="279f9-137">Noklikšķiniet uz Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="279f9-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="279f9-138">Laukā Bankas dokumenta numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="279f9-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="279f9-139">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="279f9-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="279f9-140">Izvērsiet vai sakļaujiet sadaļu Detalizēta informācija par banku.</span><span class="sxs-lookup"><span data-stu-id="279f9-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="279f9-141">Laukā Izdevēja banka noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="279f9-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="279f9-142">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="279f9-143">Laukā Konsultatīvā banka noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="279f9-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="279f9-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="279f9-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="279f9-145">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="279f9-146">Noklikšķiniet uz Iegūt pārdošanas pasūtījumu kravas.</span><span class="sxs-lookup"><span data-stu-id="279f9-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="279f9-147">Noklikšķiniet uz Izsniegt bankas dokumentu.</span><span class="sxs-lookup"><span data-stu-id="279f9-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="279f9-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="279f9-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="279f9-149">Pavadzīmes grāmatošana</span><span class="sxs-lookup"><span data-stu-id="279f9-149">Post Packing slip</span></span>
1. <span data-ttu-id="279f9-150">Darbību rūtī noklikšķiniet uz Izdot un iepakot.</span><span class="sxs-lookup"><span data-stu-id="279f9-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="279f9-151">Noklikšķiniet uz Grāmatot pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="279f9-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="279f9-152">Izvērsiet vai sakļaujiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="279f9-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="279f9-153">Laukā Daudzums atlasiet vērtību “Visi”.</span><span class="sxs-lookup"><span data-stu-id="279f9-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="279f9-154">Izvērsiet vai sakļaujiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="279f9-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="279f9-155">Laukā Pavadzīmes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="279f9-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="279f9-156">Atlasiet Sūtīšanas numurs.</span><span class="sxs-lookup"><span data-stu-id="279f9-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="279f9-157">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="279f9-158">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="279f9-158">Click OK.</span></span>
10. <span data-ttu-id="279f9-159">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="279f9-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="279f9-160">Pārdošanas rēķina grāmatošana</span><span class="sxs-lookup"><span data-stu-id="279f9-160">Post sales invoice</span></span>
1. <span data-ttu-id="279f9-161">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="279f9-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="279f9-162">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="279f9-162">Click Invoice.</span></span>
3. <span data-ttu-id="279f9-163">Izvērsiet vai sakļaujiet sadaļu Pārskats.</span><span class="sxs-lookup"><span data-stu-id="279f9-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="279f9-164">Atlasiet Sūtīšanas numurs.</span><span class="sxs-lookup"><span data-stu-id="279f9-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="279f9-165">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="279f9-166">Izvērsiet vai sakļaujiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="279f9-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="279f9-167">Laukā Rēķina datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="279f9-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="279f9-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="279f9-168">Click OK.</span></span>
9. <span data-ttu-id="279f9-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="279f9-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="279f9-170">Iesniegtā sūtījuma dokumenta statuss</span><span class="sxs-lookup"><span data-stu-id="279f9-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="279f9-171">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="279f9-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="279f9-172">Noklikšķiniet uz Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="279f9-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="279f9-173">Izvērsiet vai sakļaujiet sadaļu Rindas.</span><span class="sxs-lookup"><span data-stu-id="279f9-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="279f9-174">Piezīme. Laukam Iesniegtais dokuments jāiestata Jā.</span><span class="sxs-lookup"><span data-stu-id="279f9-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="279f9-175">Kredītvēstules eksportēšanas pārbaude</span><span class="sxs-lookup"><span data-stu-id="279f9-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="279f9-176">Dodieties uz Kases un bankas vadība > Akreditīvi > Eksporta akreditatīva un importa iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="279f9-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="279f9-177">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="279f9-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="279f9-178">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="279f9-179">Pārbaudiet, vai lauka Kredītvēstule vienuma Sūtījums statuss ir Iekļauts rēķinā.</span><span class="sxs-lookup"><span data-stu-id="279f9-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="279f9-180">Debitora maksājums</span><span class="sxs-lookup"><span data-stu-id="279f9-180">Customer payment</span></span>
1. <span data-ttu-id="279f9-181">Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="279f9-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="279f9-182">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="279f9-182">Click New.</span></span>
3. <span data-ttu-id="279f9-183">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="279f9-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="279f9-184">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="279f9-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="279f9-185">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="279f9-186">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="279f9-186">Click Lines.</span></span>
7. <span data-ttu-id="279f9-187">Laukā Datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="279f9-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="279f9-188">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="279f9-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="279f9-189">Noklikšķiniet uz Nosegšana.</span><span class="sxs-lookup"><span data-stu-id="279f9-189">Click Settlement.</span></span>
10. <span data-ttu-id="279f9-190">Atzīmējiet izvēles rūtiņu, kura atrodas lauka Kopsummas galvenē.</span><span class="sxs-lookup"><span data-stu-id="279f9-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="279f9-191">Piezīme. Laukam Rādīt iestatiet Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="279f9-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="279f9-192">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="279f9-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="279f9-193">Atzīmējiet vai notīriet izvēles rūtiņu Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="279f9-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="279f9-194">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="279f9-194">Click OK.</span></span>
14. <span data-ttu-id="279f9-195">Noklikšķiniet uz cilnes Maksājums.</span><span class="sxs-lookup"><span data-stu-id="279f9-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="279f9-196">Bankas dokumenta numura un sūtījuma numura detalizētas informācijas pārbaude</span><span class="sxs-lookup"><span data-stu-id="279f9-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="279f9-197">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="279f9-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="279f9-198">Kredītvēstules eksportēšanas pārbaude pēc maksājuma izpildes</span><span class="sxs-lookup"><span data-stu-id="279f9-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="279f9-199">Dodieties uz Kases un bankas vadība > Akreditīvi > Eksporta akreditatīva un importa iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="279f9-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="279f9-200">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="279f9-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="279f9-201">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="279f9-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="279f9-202">Pārbaudiet: Sūtījuma statuss = Maksājums saņemts un bilances summa = 0,00.</span><span class="sxs-lookup"><span data-stu-id="279f9-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

