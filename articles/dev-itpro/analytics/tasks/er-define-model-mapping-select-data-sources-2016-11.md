--- 
title: "Definēt modeļa kartēšanu un atlasīt datu avotus elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var atlasīt datu avotus datu modelim Elektroniskie pārskati (ER)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 512e24b5d0e20f00890e2a9abfe45b660a913913
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="ff76b-103">Definēt modeļa kartēšanu un atlasīt datu avotus elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="ff76b-103">Define model mapping and select data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff76b-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var atlasīt datu avotus datu modelim Elektroniskie pārskati (ER).</span><span class="sxs-lookup"><span data-stu-id="ff76b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="ff76b-105">Datu avoti tiks saistīti ar atlasītā datu modeļa atsevišķiem komponentiem noformēšanas laikā un aizpildīs biznesa datus šajā datu modelī izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="ff76b-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="ff76b-106">Šajā piemērā jāatlasa parauga uzņēmumam Litware, Inc. izveidotie esošā datu modeļa datu avoti. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā “Jauna datu modeļa izveidošana” aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ff76b-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="ff76b-107">Atvērt koka struktūru Elektronisko pārskatu veidošanas konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="ff76b-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="ff76b-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="ff76b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ff76b-109">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="ff76b-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="ff76b-110">Jaunas modeļa kartēšanas iespraušana</span><span class="sxs-lookup"><span data-stu-id="ff76b-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="ff76b-111">Kokā atlasiet “Maksājumi (vienkāršotais modelis)”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="ff76b-112">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="ff76b-112">Click Designer.</span></span>
3. <span data-ttu-id="ff76b-113">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="ff76b-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="ff76b-114">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ff76b-114">Click New.</span></span>
    * <span data-ttu-id="ff76b-115">Šādi tiks izveidots jauns ieraksts, kas kartēs datu modeli datu avotos.</span><span class="sxs-lookup"><span data-stu-id="ff76b-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="ff76b-116">Šajā piemērā jūs kartēsiet datu modeli datu avotos vēlamajam maksājuma tipam: kredīta pārsūtīšana.</span><span class="sxs-lookup"><span data-stu-id="ff76b-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="ff76b-117">Ir iespējams izveidot vairāk nekā vienu kartēšanu konkrētam datu modelim.</span><span class="sxs-lookup"><span data-stu-id="ff76b-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="ff76b-118">Piemēram, var izveidot kartēšanu dažāda veida maksājumiem, piemēram, tiešajam debetam vai kredīta pārsūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ff76b-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="ff76b-119">Šajā piemērā jūs izveidosiet kartēšanu kredīta pārsūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ff76b-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="ff76b-120">Laukā Nosaukums ierakstiet “CT kartēšana”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="ff76b-121">CT kartēšana</span><span class="sxs-lookup"><span data-stu-id="ff76b-121">CT mapping</span></span>  
6. <span data-ttu-id="ff76b-122">Laukā Apraksts ierakstiet "Maksājumu modeļa kartēšanas CT".</span><span class="sxs-lookup"><span data-stu-id="ff76b-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="ff76b-123">Maksājumu modeļa kartēšanas CT</span><span class="sxs-lookup"><span data-stu-id="ff76b-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="ff76b-124">Laukā Definīcija ierakstiet “CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="ff76b-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="ff76b-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="ff76b-126">ResolveChanges vienumam Definīcija.</span><span class="sxs-lookup"><span data-stu-id="ff76b-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="ff76b-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff76b-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="ff76b-128">Pašreizējā modeļa kartēšanai nepieciešamo datu avotu definēšana</span><span class="sxs-lookup"><span data-stu-id="ff76b-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="ff76b-129">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="ff76b-129">Click Designer.</span></span>
2. <span data-ttu-id="ff76b-130">Kokā atlasiet "Dynamics 365 for Operations\Table records".</span><span class="sxs-lookup"><span data-stu-id="ff76b-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="ff76b-131">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="ff76b-131">Click Add root.</span></span>
    * <span data-ttu-id="ff76b-132">Ievadiet šo datu avotu, lai piekļūtu maksājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="ff76b-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="ff76b-133">Laukā Nosaukums ierakstiet “Transakcijas”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="ff76b-134">Darbības</span><span class="sxs-lookup"><span data-stu-id="ff76b-134">Transactions</span></span>  
5. <span data-ttu-id="ff76b-135">Laukā Iezīme ievadiet “Transakcijas”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="ff76b-136">Darbības</span><span class="sxs-lookup"><span data-stu-id="ff76b-136">Transactions</span></span>  
6. <span data-ttu-id="ff76b-137">Laukā Palīdzība ievadiet "Virsgrāmatas žurnāla rindas".</span><span class="sxs-lookup"><span data-stu-id="ff76b-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="ff76b-138">Virsgrāmatas žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="ff76b-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="ff76b-139">Laukā Pieprasīt vaicājumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ff76b-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="ff76b-140">Atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ff76b-140">Select Yes.</span></span>  
8. <span data-ttu-id="ff76b-141">Laukā Tabula ierakstiet 'LedgerJournalTrans'.</span><span class="sxs-lookup"><span data-stu-id="ff76b-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="ff76b-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="ff76b-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="ff76b-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ff76b-143">Click OK.</span></span>
    * <span data-ttu-id="ff76b-144">Atlasiet tabulu LedgerJournalTrans kā pašreizējā datu modeļa datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="ff76b-145">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="ff76b-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="ff76b-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ff76b-146">Click Add.</span></span>
    * <span data-ttu-id="ff76b-147">Noklikšķiniet uz Pievienot, lai pievienotu jaunu aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="ff76b-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="ff76b-148">Laukā Nosaukums ierakstiet "$EndToEndID".</span><span class="sxs-lookup"><span data-stu-id="ff76b-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="ff76b-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="ff76b-149">$EndToEndID</span></span>  
13. <span data-ttu-id="ff76b-150">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-150">Click Edit formula.</span></span>
14. <span data-ttu-id="ff76b-151">Kokā atlasiet “Virkne\CONCATENATE”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="ff76b-152">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="ff76b-152">Click Add function.</span></span>
16. <span data-ttu-id="ff76b-153">Kokā izvērsiet sadaļu "Transakcija".</span><span class="sxs-lookup"><span data-stu-id="ff76b-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="ff76b-154">Kokā atlasiet "Transakcijas\Dokuments".</span><span class="sxs-lookup"><span data-stu-id="ff76b-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="ff76b-155">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-155">Click Add data source.</span></span>
19. <span data-ttu-id="ff76b-156">Laukā Formula ievadiet “CONCATENATE(Transactions.Voucher, "-", ”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="ff76b-157">Ierakstiet [ , "-", ] formulas beigās.</span><span class="sxs-lookup"><span data-stu-id="ff76b-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="ff76b-158">Kokā atlasiet "Virkne\TEXT".</span><span class="sxs-lookup"><span data-stu-id="ff76b-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="ff76b-159">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="ff76b-159">Click Add function.</span></span>
22. <span data-ttu-id="ff76b-160">Kokā atlasiet "Transakcijas\Ieraksta ID(RecId)".</span><span class="sxs-lookup"><span data-stu-id="ff76b-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="ff76b-161">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-161">Click Add data source.</span></span>
24. <span data-ttu-id="ff76b-162">Laukā Formula ievadiet “CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="ff76b-163">Ierakstiet [))] formulas beigās.</span><span class="sxs-lookup"><span data-stu-id="ff76b-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="ff76b-164">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff76b-164">Click Save.</span></span>
    * <span data-ttu-id="ff76b-165">Pārliecinieties, ka izveidotajā formulā nav kļūdu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="ff76b-166">Skatiet cilni KĻŪDAS zem formulas redaktora vadīklas.</span><span class="sxs-lookup"><span data-stu-id="ff76b-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="ff76b-167">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-167">Close the page.</span></span>
27. <span data-ttu-id="ff76b-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ff76b-168">Click OK.</span></span>
    * <span data-ttu-id="ff76b-169">Pievienojiet aprēķināto lauku šim datu avotam.</span><span class="sxs-lookup"><span data-stu-id="ff76b-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="ff76b-170">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ff76b-170">Click Add.</span></span>
    * <span data-ttu-id="ff76b-171">Noklikšķiniet uz Pievienot, lai pievienotu jaunu aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="ff76b-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="ff76b-172">Laukā Nosaukums ierakstiet "$Amount".</span><span class="sxs-lookup"><span data-stu-id="ff76b-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="ff76b-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="ff76b-173">$Amount</span></span>  
30. <span data-ttu-id="ff76b-174">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-174">Click Edit formula.</span></span>
31. <span data-ttu-id="ff76b-175">Kokā izvērsiet sadaļu "Transakcija".</span><span class="sxs-lookup"><span data-stu-id="ff76b-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="ff76b-176">Kokā atlasiet "Transakcijas\Debets(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="ff76b-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="ff76b-177">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-177">Click Add data source.</span></span>
34. <span data-ttu-id="ff76b-178">Laukā Formula ievadiet “Transactions.AmountCurDebit - ”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="ff76b-179">Ierakstiet [ - ] formulas beigās.</span><span class="sxs-lookup"><span data-stu-id="ff76b-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="ff76b-180">Kokā atlasiet "Transakcijas\Kredīts(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="ff76b-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="ff76b-181">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-181">Click Add data source.</span></span>
37. <span data-ttu-id="ff76b-182">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff76b-182">Click Save.</span></span>
38. <span data-ttu-id="ff76b-183">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-183">Close the page.</span></span>
39. <span data-ttu-id="ff76b-184">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ff76b-184">Click OK.</span></span>
    * <span data-ttu-id="ff76b-185">Šādi pašreizējam datu modelim atlasītajam datu avotam tiks pievienots aprēķinātais lauks $Amount.</span><span class="sxs-lookup"><span data-stu-id="ff76b-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="ff76b-186">Kokā atlasiet "Transactions\$Amount".</span><span class="sxs-lookup"><span data-stu-id="ff76b-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="ff76b-187">Kokā izvērsiet sadaļu "Transakcija".</span><span class="sxs-lookup"><span data-stu-id="ff76b-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="ff76b-188">Koka struktūrā izvērsiet vai sakļaujiet zaru “Transactions\$Amount".</span><span class="sxs-lookup"><span data-stu-id="ff76b-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="ff76b-189">Koka struktūrā izvērsiet vai sakļaujiet zaru “Transakcijas”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="ff76b-190">Kokā atlasiet "Dynamics 365 for Operations\Table records".</span><span class="sxs-lookup"><span data-stu-id="ff76b-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="ff76b-191">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="ff76b-191">Click Add root.</span></span>
    * <span data-ttu-id="ff76b-192">Ievadiet šo datu avotu, lai piekļūtu uzņēmuma bankas konta detaļām.</span><span class="sxs-lookup"><span data-stu-id="ff76b-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="ff76b-193">Laukā Nosaukums ierakstiet "BankAccount".</span><span class="sxs-lookup"><span data-stu-id="ff76b-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="ff76b-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="ff76b-194">BankAccount</span></span>  
47. <span data-ttu-id="ff76b-195">Laukā Iezīme ievadiet “Bankas konts”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="ff76b-196">Bankas konts</span><span class="sxs-lookup"><span data-stu-id="ff76b-196">Bank Account</span></span>  
48. <span data-ttu-id="ff76b-197">Laukā Palīdzība ievadiet “Bankas konts”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="ff76b-198">Bankas konts</span><span class="sxs-lookup"><span data-stu-id="ff76b-198">Bank Account</span></span>  
49. <span data-ttu-id="ff76b-199">Laukā Pieprasīt vaicājumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ff76b-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="ff76b-200">Atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ff76b-200">Select Yes.</span></span>  
50. <span data-ttu-id="ff76b-201">Laukā Tabula ierakstiet "BankAccountTable".</span><span class="sxs-lookup"><span data-stu-id="ff76b-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="ff76b-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="ff76b-202">BankAccountTable</span></span>  
51. <span data-ttu-id="ff76b-203">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ff76b-203">Click OK.</span></span>
    * <span data-ttu-id="ff76b-204">Atlasiet tabulu BankAccountTable kā pašreizējā datu modeļa datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="ff76b-205">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="ff76b-205">Click Add root.</span></span>
    * <span data-ttu-id="ff76b-206">Ievadiet šo datu avotu, lai piekļūtu uzņēmuma bankas konta rekvizītiem.</span><span class="sxs-lookup"><span data-stu-id="ff76b-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="ff76b-207">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="ff76b-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="ff76b-208">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="ff76b-208">Company</span></span>  
54. <span data-ttu-id="ff76b-209">Laukā Iezīme ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ff76b-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="ff76b-210">Uzņēmuma informācija</span><span class="sxs-lookup"><span data-stu-id="ff76b-210">Company information</span></span>  
55. <span data-ttu-id="ff76b-211">Laukā Palīdzība ievadiet "Uzņēmuma informācija".</span><span class="sxs-lookup"><span data-stu-id="ff76b-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="ff76b-212">Uzņēmuma informācija</span><span class="sxs-lookup"><span data-stu-id="ff76b-212">Company information</span></span>  
56. <span data-ttu-id="ff76b-213">Laukā Pieprasīt vaicājumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ff76b-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="ff76b-214">Atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ff76b-214">Select Yes.</span></span>  
57. <span data-ttu-id="ff76b-215">Laukā Tabula ierakstiet "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="ff76b-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="ff76b-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="ff76b-216">CompanyInfo</span></span>  
58. <span data-ttu-id="ff76b-217">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ff76b-217">Click OK.</span></span>
    * <span data-ttu-id="ff76b-218">Atlasiet tabulu CompanyInfo kā pašreizējā datu modeļa datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="ff76b-219">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="ff76b-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="ff76b-220">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="ff76b-220">Click Add root.</span></span>
    * <span data-ttu-id="ff76b-221">Iespraudiet aprēķināto lauku kā jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="ff76b-222">Laukā Nosaukums ievadiet "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="ff76b-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="ff76b-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="ff76b-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="ff76b-224">Laukā Atzīme ievadiet tekstu Apstrādes datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="ff76b-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="ff76b-225">Apstrādes datums un laiks</span><span class="sxs-lookup"><span data-stu-id="ff76b-225">Processing date & time</span></span>  
63. <span data-ttu-id="ff76b-226">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-226">Click Edit formula.</span></span>
64. <span data-ttu-id="ff76b-227">Koka struktūrā atlasiet zaru “Datums/laiks\SESSIONNOW”.</span><span class="sxs-lookup"><span data-stu-id="ff76b-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="ff76b-228">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="ff76b-228">Click Add function.</span></span>
66. <span data-ttu-id="ff76b-229">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff76b-229">Click Save.</span></span>
67. <span data-ttu-id="ff76b-230">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-230">Close the page.</span></span>
68. <span data-ttu-id="ff76b-231">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ff76b-231">Click OK.</span></span>
    * <span data-ttu-id="ff76b-232">Pievienojiet aprēķināto lauku ProcessingDateTime kā pašreizējā datu modeļa datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="ff76b-233">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff76b-233">Click Save.</span></span>
70. <span data-ttu-id="ff76b-234">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-234">Close the page.</span></span>
71. <span data-ttu-id="ff76b-235">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-235">Close the page.</span></span>
72. <span data-ttu-id="ff76b-236">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff76b-236">Close the page.</span></span>


