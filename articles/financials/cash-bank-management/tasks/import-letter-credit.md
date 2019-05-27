---
title: Importa akreditatīvs
description: Šajā procedūrā ir aprakstīts kredītvēstules importēšanas process.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d5539fbd17c880d8bbadd47444c9cc53fce039c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566298"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="1ab76-103">Importa akreditatīvs</span><span class="sxs-lookup"><span data-stu-id="1ab76-103">Import letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ab76-104">Šajā procedūrā ir aprakstīts kredītvēstules importēšanas process.</span><span class="sxs-lookup"><span data-stu-id="1ab76-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="1ab76-105">Pirms šīs procedūras veikšanas ir jāiestata: bankas iestādes, grāmatošanas profili, bankas iestādes līgums un kreditora bankas dati.</span><span class="sxs-lookup"><span data-stu-id="1ab76-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="1ab76-106">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="1ab76-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="1ab76-107">Pirkšanas pasūtījuma ar kredītvēstuli izveide</span><span class="sxs-lookup"><span data-stu-id="1ab76-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="1ab76-108">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="1ab76-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="1ab76-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1ab76-109">Click New.</span></span>
3. <span data-ttu-id="1ab76-110">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="1ab76-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="1ab76-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="1ab76-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1ab76-113">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="1ab76-113">Expand the General section.</span></span>
7. <span data-ttu-id="1ab76-114">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="1ab76-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1ab76-116">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="1ab76-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="1ab76-118">Laukā Uzskaites datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="1ab76-119">Laukā Piegādes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="1ab76-120">Ņemiet vērā! Jābūt atlasītam laukam Bankas dokumenta tips un vērtībai Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="1ab76-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="1ab76-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ab76-121">Click OK.</span></span>
14. <span data-ttu-id="1ab76-122">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="1ab76-123">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="1ab76-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="1ab76-125">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="1ab76-126">Noklikšķiniet uz cilnes Piegāde.</span><span class="sxs-lookup"><span data-stu-id="1ab76-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="1ab76-127">Laukā Piegādes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="1ab76-128">Laukā Apstiprinātais piegādes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="1ab76-129">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="1ab76-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="1ab76-130">Ievadiet detalizētu informāciju vienumam Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="1ab76-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="1ab76-131">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="1ab76-132">Noklikšķiniet uz Kredītvēstule/importa inkaso.</span><span class="sxs-lookup"><span data-stu-id="1ab76-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="1ab76-133">Laukā Izmantošanas datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="1ab76-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="1ab76-134">Pārbaudiet, vai lauka Bankas konts ir aktīvs noklusējuma Bankas konts, kas tiek izmantots, ņemot vērā pieteikuma datumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="1ab76-135">Laukā Bankas dokumenta numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="1ab76-136">Laukā Ieejas plūsmas datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="1ab76-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="1ab76-137">Izvērsiet sadaļu Bankas dokuments.</span><span class="sxs-lookup"><span data-stu-id="1ab76-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="1ab76-138">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="1ab76-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="1ab76-139">Izvērsiet sadaļu Detalizēta informācija par banku.</span><span class="sxs-lookup"><span data-stu-id="1ab76-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="1ab76-140">Laukā Konsultatīvā banka ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="1ab76-141">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="1ab76-142">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-142">Click Save.</span></span>
33. <span data-ttu-id="1ab76-143">Noklikšķiniet uz Iegūt pirkšanas pasūtījumu kravas.</span><span class="sxs-lookup"><span data-stu-id="1ab76-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="1ab76-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-144">Close the page.</span></span>
35. <span data-ttu-id="1ab76-145">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="1ab76-146">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-146">Click Confirm.</span></span>
37. <span data-ttu-id="1ab76-147">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="1ab76-148">Noklikšķiniet uz Kredītvēstule/importa inkaso.</span><span class="sxs-lookup"><span data-stu-id="1ab76-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="1ab76-149">Noklikšķiniet uz Apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-149">Click Process.</span></span>
40. <span data-ttu-id="1ab76-150">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-150">Click Confirm.</span></span>
    * <span data-ttu-id="1ab76-151">Pārbaudiet, vai lauka Kredītlīnijas bilance vērtība samazina pirkšanas pasūtījuma summu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="1ab76-152">Šajā piemērā pirkuma summa ir 500,00; iestādes ierobežojums ir 10 000,00 un atbilstoši iestādes bilance ir 9500,00.</span><span class="sxs-lookup"><span data-stu-id="1ab76-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="1ab76-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-153">Close the page.</span></span>
42. <span data-ttu-id="1ab76-154">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="1ab76-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="1ab76-155">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-155">Click Save.</span></span>
44. <span data-ttu-id="1ab76-156">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="1ab76-157">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-157">Click Confirm.</span></span>
    * <span data-ttu-id="1ab76-158">Vienības cenu izmaiņu dēļ jalabo lauks Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="1ab76-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="1ab76-159">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="1ab76-160">Noklikšķiniet uz Kredītvēstule/importa inkaso.</span><span class="sxs-lookup"><span data-stu-id="1ab76-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="1ab76-161">Pirkšanas vienības cenas izmaiņu dēļ jalabo lauks Kredītvēstule.</span><span class="sxs-lookup"><span data-stu-id="1ab76-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="1ab76-162">Noklikšķiniet uz Apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-162">Click Process.</span></span>
49. <span data-ttu-id="1ab76-163">Noklikšķiniet uz Labot.</span><span class="sxs-lookup"><span data-stu-id="1ab76-163">Click Amend.</span></span>
50. <span data-ttu-id="1ab76-164">Noklikšķiniet uz Noņemt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-164">Click Remove.</span></span>
51. <span data-ttu-id="1ab76-165">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-165">Click Yes.</span></span>
52. <span data-ttu-id="1ab76-166">Noklikšķiniet uz Iegūt pirkšanas pasūtījumu kravas.</span><span class="sxs-lookup"><span data-stu-id="1ab76-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="1ab76-167">Noklikšķiniet uz Apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-167">Click Process.</span></span>
54. <span data-ttu-id="1ab76-168">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-168">Click Confirm.</span></span>
    * <span data-ttu-id="1ab76-169">Pārbaudiet, vai lauka Kredītlīnijas bilance vērtība samazina pirkšanas pasūtījuma summu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="1ab76-170">Šajā piemērā rediģētā pirkuma summa ir 600,00; iestādes ierobežojums ir 10 000,00; tāpēc iestādes bilance ir 9400,00.</span><span class="sxs-lookup"><span data-stu-id="1ab76-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="1ab76-171">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="1ab76-172">Pavadzīmes grāmatošana</span><span class="sxs-lookup"><span data-stu-id="1ab76-172">Post Packing slip</span></span>
1. <span data-ttu-id="1ab76-173">Darbību rūtī noklikšķiniet uz Saņemt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="1ab76-174">Noklikšķiniet uz Produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="1ab76-174">Click Product receipt.</span></span>
3. <span data-ttu-id="1ab76-175">Laukā PurchParmTable_Num ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="1ab76-176">Atlasiet kopā ar kredītvēstules atsauci izveidoto lauku Sūtīšanas numurs.</span><span class="sxs-lookup"><span data-stu-id="1ab76-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="1ab76-177">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1ab76-178">Laukā Produktu ieejas plūsmas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="1ab76-179">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ab76-179">Click OK.</span></span>
7. <span data-ttu-id="1ab76-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-180">Close the page.</span></span>
8. <span data-ttu-id="1ab76-181">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="1ab76-182">Darbības Kredītvēstules importēšana statusa pārbaude</span><span class="sxs-lookup"><span data-stu-id="1ab76-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="1ab76-183">Dodieties uz Kases un bankas vadība > Akreditatīvi > Importa akreditatīvs un importa iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="1ab76-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="1ab76-184">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1ab76-185">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1ab76-186">Pārbaudiet darbības Kredītvēstules importēšana statusu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="1ab76-187">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-187">Close the page.</span></span>
5. <span data-ttu-id="1ab76-188">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="1ab76-189">Pirkšanas rēķina grāmatošana</span><span class="sxs-lookup"><span data-stu-id="1ab76-189">Post purchase invoice</span></span>
1. <span data-ttu-id="1ab76-190">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="1ab76-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="1ab76-191">Atlasiet pirkšanas pasūtījumu, kas tika izveidots kopā ar kredītvēstuli.</span><span class="sxs-lookup"><span data-stu-id="1ab76-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="1ab76-192">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1ab76-193">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1ab76-194">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="1ab76-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="1ab76-195">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="1ab76-195">Click Invoice.</span></span>
6. <span data-ttu-id="1ab76-196">Laukā Numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="1ab76-197">Laukā Sūtīšanas numurs ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="1ab76-198">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1ab76-199">Laukā Rēķina datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="1ab76-200">Noklikšķiniet uz Atjaunināt atbilstības statusu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-200">Click Update match status.</span></span>
11. <span data-ttu-id="1ab76-201">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="1ab76-201">Click Post.</span></span>
12. <span data-ttu-id="1ab76-202">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-202">Close the page.</span></span>
13. <span data-ttu-id="1ab76-203">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="1ab76-204">Darbības Kredītvēstules importēšana statusa pārbaude</span><span class="sxs-lookup"><span data-stu-id="1ab76-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="1ab76-205">Dodieties uz Kases un bankas vadība > Akreditatīvi > Importa akreditatīvs un importa iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="1ab76-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="1ab76-206">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1ab76-207">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1ab76-208">Pārbaudiet darbību Importēt kredītvēstuli 2.</span><span class="sxs-lookup"><span data-stu-id="1ab76-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="1ab76-209">Pārbaudiet: Sūtījuma statuss = rēķinos iekļautie bankas dati</span><span class="sxs-lookup"><span data-stu-id="1ab76-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="1ab76-210">Noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-210">Click View.</span></span>
5. <span data-ttu-id="1ab76-211">Noklikšķiniet uz Drukāt pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-211">Click Print application.</span></span>
6. <span data-ttu-id="1ab76-212">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ab76-212">Click OK.</span></span>
    * <span data-ttu-id="1ab76-213">Pārbaudiet, vai kredītvēstules pieteikums tiek izdrukāts.</span><span class="sxs-lookup"><span data-stu-id="1ab76-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="1ab76-214">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-214">Close the page.</span></span>
8. <span data-ttu-id="1ab76-215">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-215">Close the page.</span></span>
9. <span data-ttu-id="1ab76-216">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="1ab76-217">Kreditoru maksājumu žurnāla grāmatošana izveidotajam pirkšanas rēķinam ar kredītvēstuli</span><span class="sxs-lookup"><span data-stu-id="1ab76-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="1ab76-218">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="1ab76-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="1ab76-219">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1ab76-219">Click New.</span></span>
3. <span data-ttu-id="1ab76-220">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="1ab76-221">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1ab76-222">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="1ab76-222">Click Lines.</span></span>
6. <span data-ttu-id="1ab76-223">Laukā Datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="1ab76-224">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1ab76-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="1ab76-225">Noklikšķiniet uz Transakciju nosegšana.</span><span class="sxs-lookup"><span data-stu-id="1ab76-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="1ab76-226">Izvērsiet sadaļu Kopsummas.</span><span class="sxs-lookup"><span data-stu-id="1ab76-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="1ab76-227">Laukā Rādīt atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="1ab76-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="1ab76-228">Pārbaudiet, vai lauks Bankas dokumenta numurs un Sūtījuma numurs tika atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="1ab76-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="1ab76-229">Atzīmējiet izvēles rūtiņu Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="1ab76-230">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ab76-230">Click OK.</span></span>
13. <span data-ttu-id="1ab76-231">Noklikšķiniet uz cilnes Maksājums.</span><span class="sxs-lookup"><span data-stu-id="1ab76-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="1ab76-232">Pārbaudiet, vai lauks Bankas dokumenta numurs un Sūtījuma numurs tika atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="1ab76-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="1ab76-233">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="1ab76-233">Click Post.</span></span>
15. <span data-ttu-id="1ab76-234">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-234">Close the page.</span></span>
16. <span data-ttu-id="1ab76-235">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="1ab76-236">Darbības Kredītvēstules importēšana statusa pārbaude pēc rēķina apmaksas</span><span class="sxs-lookup"><span data-stu-id="1ab76-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="1ab76-237">Dodieties uz Kases un bankas vadība > Akreditatīvi > Importa akreditatīvs un importa iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="1ab76-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="1ab76-238">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1ab76-239">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1ab76-240">Pārbaudiet darbības Kredītvēstules importēšana statusu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="1ab76-241">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="1ab76-242">Bankas iestādes ierobežojuma un lietojuma pārskata pārbaude</span><span class="sxs-lookup"><span data-stu-id="1ab76-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="1ab76-243">Dodieties uz Kases un bankas vadība > Uzziņas un atskaites > Akreditatīvi vai garantijas vēstules > Bankas pakalpojumu un lietojuma atskaite.</span><span class="sxs-lookup"><span data-stu-id="1ab76-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="1ab76-244">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="1ab76-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="1ab76-245">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="1ab76-245">Click Filter.</span></span>
    * <span data-ttu-id="1ab76-246">Definējiet lauka Kritēriji vērtību, izmantojot nepieciešamo bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="1ab76-247">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ab76-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="1ab76-248">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ab76-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1ab76-249">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ab76-249">Click OK.</span></span>
7. <span data-ttu-id="1ab76-250">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ab76-250">Click OK.</span></span>
    * <span data-ttu-id="1ab76-251">Pārbaudiet pārskatu, kurā ir norādītas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="1ab76-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="1ab76-252">Pārbaudiet, vai pārskatā ir ietvertas transakcijas ar šādiem elementiem Bankas dokumenta numurs, Iestādes ierobežojums, Izmantotā summa un Iestādes bilances summa.</span><span class="sxs-lookup"><span data-stu-id="1ab76-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="1ab76-253">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ab76-253">Close the page.</span></span>

