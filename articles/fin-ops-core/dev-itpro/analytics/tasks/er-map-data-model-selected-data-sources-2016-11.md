---
title: ER datu modeļa kartēšana ar izvēlētajiem datu avotiem
description: Šajā tēmā ir aprakstīts, kā kartēt elektronisko pārskatu (ER) datu modeli atlasītajiem Microsoft Dynamics 365 Finance datu avotiem.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0eb7f48a50e32637003c1488d80899a704709068
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751490"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="947c3-103">ER datu modeļa kartēšana ar izvēlētajiem datu avotiem</span><span class="sxs-lookup"><span data-stu-id="947c3-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="947c3-104">Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko pārskatu izstrādātājs datu modeli Elektronisko pārskatu veidošana (Electronic reporting — ER) var kartēt uz izvēlētajiem datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="947c3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="947c3-105">Šis modeļa kartējums vēlāk tiks izmantots kā datu avots formāta konfigurācijā, kas tiks izmantota, lai pārvaldītu elektroniskos maksājuma dokumentus.</span><span class="sxs-lookup"><span data-stu-id="947c3-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="947c3-106">Šajā piemērā parauga uzņēmuma Litware, Inc. datu modelis tiek kartēts par datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="947c3-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="947c3-107">Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras "Datu avotu atlasīšana modeļa kartēšanai" darbības.</span><span class="sxs-lookup"><span data-stu-id="947c3-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="947c3-108">ER konfigurācijas koka atvēršana</span><span class="sxs-lookup"><span data-stu-id="947c3-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="947c3-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="947c3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="947c3-110">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="947c3-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="947c3-111">Izveidotās modeļa kartēšanas atlasīšana</span><span class="sxs-lookup"><span data-stu-id="947c3-111">Select created model mapping</span></span>
1. <span data-ttu-id="947c3-112">Kokā atlasiet “Maksājumi (vienkāršotais modelis)”.</span><span class="sxs-lookup"><span data-stu-id="947c3-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="947c3-113">Pārliecinieties, ka modeļa konfigurācija "Maksājumi (vienkāršotas modelis)" tika izveidota iepriekš.</span><span class="sxs-lookup"><span data-stu-id="947c3-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="947c3-114">Pretējā gadījumā beidziet šeit sniegto norādījumu izpildi un atgriezties pēc tam, kad ir izpildīts uzdevuma ceļvedis 'Izveidot jaunu konfigurāciju ar izvēlēta domēna datu modeli'.</span><span class="sxs-lookup"><span data-stu-id="947c3-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="947c3-115">Noklikšķiniet uz Modeļa veidotājs.</span><span class="sxs-lookup"><span data-stu-id="947c3-115">Click Model designer.</span></span>
3. <span data-ttu-id="947c3-116">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="947c3-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="947c3-117">Atlasiet ierakstu "CT kartēšana".</span><span class="sxs-lookup"><span data-stu-id="947c3-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="947c3-118">CT kartēšana</span><span class="sxs-lookup"><span data-stu-id="947c3-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="947c3-119">Izveidoto datu avotu saistīšana ar datu modeļa elementiem</span><span class="sxs-lookup"><span data-stu-id="947c3-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="947c3-120">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="947c3-120">Click Designer.</span></span>
2. <span data-ttu-id="947c3-121">Koka skatā atlasiet Apstrādes datums un laiks(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="947c3-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="947c3-122">Kokā atlasiet "Apstrādes datums(ProcessingDateTime)".</span><span class="sxs-lookup"><span data-stu-id="947c3-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="947c3-123">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-123">Click Bind.</span></span>
5. <span data-ttu-id="947c3-124">Kokā atlasiet "Maksājuma ziņojuma identifikācija(MessageIdentification)".</span><span class="sxs-lookup"><span data-stu-id="947c3-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="947c3-125">Kokā izvērsiet sadaļu "Transakcija".</span><span class="sxs-lookup"><span data-stu-id="947c3-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="947c3-126">Kokā atlasiet "Transakcijas\Žurnāla partijas numurs(JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="947c3-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="947c3-127">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-127">Click Bind.</span></span>
9. <span data-ttu-id="947c3-128">Kokā struktūrā atlasiet "Maksājumi".</span><span class="sxs-lookup"><span data-stu-id="947c3-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="947c3-129">Kokā atlasiet "Transakcijas".</span><span class="sxs-lookup"><span data-stu-id="947c3-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="947c3-130">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-130">Click Bind.</span></span>
12. <span data-ttu-id="947c3-131">Kokā izvērsiet sadaļu “Maksājumi= Transakcijas”.</span><span class="sxs-lookup"><span data-stu-id="947c3-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="947c3-132">Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="947c3-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="947c3-133">Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Kreditors\Konts”.</span><span class="sxs-lookup"><span data-stu-id="947c3-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="947c3-134">Kokā atlasiet "Maksājumi= Transakcijas\Kreditors\Konts\Valūtas kods(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="947c3-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="947c3-135">Kokā izvērsiet "Transakcijas\vendBankAccountInTransactionCompany()".</span><span class="sxs-lookup"><span data-stu-id="947c3-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="947c3-136">Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\Valūta(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="947c3-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="947c3-137">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-137">Click Bind.</span></span>
19. <span data-ttu-id="947c3-138">Kokā atlasiet "Maksājumi= Transakcijas\Kreditors\Konts\IBAN kods(IBAN).</span><span class="sxs-lookup"><span data-stu-id="947c3-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="947c3-139">Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)".</span><span class="sxs-lookup"><span data-stu-id="947c3-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="947c3-140">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-140">Click Bind.</span></span>
22. <span data-ttu-id="947c3-141">Kokā atlasiet “Maksājumi= Transakcijas\Kreditors\Konts\Numurs”.</span><span class="sxs-lookup"><span data-stu-id="947c3-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="947c3-142">Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\Bankas konta numurs(AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="947c3-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="947c3-143">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-143">Click Bind.</span></span>
25. <span data-ttu-id="947c3-144">Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Kreditors\Aģents”.</span><span class="sxs-lookup"><span data-stu-id="947c3-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="947c3-145">Kokā atlasiet “Maksājumi= Transakcijas\Kreditors\Aģents\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="947c3-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="947c3-146">Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="947c3-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="947c3-147">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-147">Click Bind.</span></span>
29. <span data-ttu-id="947c3-148">Kokā atlasiet “Maksājumi= Transakcijas\Kreditors\Aģents\Maršrutēšanas numurs(RoutingNumber)”.</span><span class="sxs-lookup"><span data-stu-id="947c3-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="947c3-149">Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\Maršrutēšanas numurs(RegistrationNum)".</span><span class="sxs-lookup"><span data-stu-id="947c3-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="947c3-150">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-150">Click Bind.</span></span>
32. <span data-ttu-id="947c3-151">Kokā atlasiet "Maksājumi= Transakcijas\Kreditors\Aģents\SWIFT kods(SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="947c3-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="947c3-152">Kokā atlasiet "Transakcijas\vendBankAccountInTransactionCompany()\SWIFT kods(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="947c3-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="947c3-153">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-153">Click Bind.</span></span>
35. <span data-ttu-id="947c3-154">Kokā atlasiet “Maksājumi= Transakcijas\Kreditors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="947c3-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="947c3-155">Kokā izvērsiet sadaļu “Transakcijas\findVendTable()”.</span><span class="sxs-lookup"><span data-stu-id="947c3-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="947c3-156">Koka skatā atlasiet Transakcijas\findVendTable()\name().</span><span class="sxs-lookup"><span data-stu-id="947c3-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="947c3-157">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-157">Click Bind.</span></span>
39. <span data-ttu-id="947c3-158">Kokā atlasiet "Maksājumi= Transakcijas\Valūtas kods(Currency)".</span><span class="sxs-lookup"><span data-stu-id="947c3-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="947c3-159">Kokā izvērsiet 'Transactions\>Relations'.</span><span class="sxs-lookup"><span data-stu-id="947c3-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="947c3-160">Kokā izvērsiet 'Transactions\>Relations\Currency table(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="947c3-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="947c3-161">Kokā atlasiet 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span><span class="sxs-lookup"><span data-stu-id="947c3-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="947c3-162">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-162">Click Bind.</span></span>
44. <span data-ttu-id="947c3-163">Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Debitors”.</span><span class="sxs-lookup"><span data-stu-id="947c3-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="947c3-164">Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Debitors\Konts”.</span><span class="sxs-lookup"><span data-stu-id="947c3-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="947c3-165">Kokā atlasiet "Maksājumi= Transakcijas\Debitors\Konts\Valūtas kods(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="947c3-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="947c3-166">Kokā atlasiet "Bankas konts(BankAccount)".</span><span class="sxs-lookup"><span data-stu-id="947c3-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="947c3-167">Kokā izvērsiet sadaļu "Bankas konts(BankAccount)".</span><span class="sxs-lookup"><span data-stu-id="947c3-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="947c3-168">Kokā atlasiet "Bankas konts(BankAccount)\Valūta(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="947c3-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="947c3-169">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-169">Click Bind.</span></span>
51. <span data-ttu-id="947c3-170">Kokā atlasiet "Bankas konts(BankAccount)\IBAN".</span><span class="sxs-lookup"><span data-stu-id="947c3-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="947c3-171">Kokā atlasiet "Maksājumi= Transakcijas\Debitors\Konts\IBAN kods(IBAN).</span><span class="sxs-lookup"><span data-stu-id="947c3-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="947c3-172">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-172">Click Bind.</span></span>
54. <span data-ttu-id="947c3-173">Kokā atlasiet “Maksājumi= Transakcijas\Debitors\Konts\Numurs”.</span><span class="sxs-lookup"><span data-stu-id="947c3-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="947c3-174">Kokā atlasiet "Bankas konts(BankAccount)\Bankas konta numurs(AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="947c3-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="947c3-175">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-175">Click Bind.</span></span>
57. <span data-ttu-id="947c3-176">Kokā izvērsiet sadaļu “Maksājumi= Transakcijas\Debitors\Aģents”.</span><span class="sxs-lookup"><span data-stu-id="947c3-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="947c3-177">Kokā atlasiet “Maksājumi= Transakcijas\Debitors\Aģents\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="947c3-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="947c3-178">Kokā atlasiet "Bankas konts(BankAccount)\Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="947c3-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="947c3-179">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-179">Click Bind.</span></span>
61. <span data-ttu-id="947c3-180">Kokā atlasiet “Maksājumi= Transakcijas\Debitors\Aģents\Maršrutēšanas numurs(RoutingNumber)”.</span><span class="sxs-lookup"><span data-stu-id="947c3-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="947c3-181">Kokā atlasiet "Bankas konts(BankAccount)\Maršrutēšanas numurs(RegistrationNum)".</span><span class="sxs-lookup"><span data-stu-id="947c3-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="947c3-182">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-182">Click Bind.</span></span>
64. <span data-ttu-id="947c3-183">Kokā atlasiet "Maksājumi= Transakcijas\Debitors\Aģents\SWIFT kods(SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="947c3-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="947c3-184">Kokā atlasiet "Bankas konts(BankAccount)\SWIFT kods(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="947c3-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="947c3-185">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-185">Click Bind.</span></span>
67. <span data-ttu-id="947c3-186">Kokā atlasiet “Maksājumi= Transakcijas\Debitors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="947c3-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="947c3-187">Kokā atlasiet "Informācija par uzņēmumu(Company)".</span><span class="sxs-lookup"><span data-stu-id="947c3-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="947c3-188">Kokā izvērsiet sadaļu "Informācija par uzņēmumu(Company)".</span><span class="sxs-lookup"><span data-stu-id="947c3-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="947c3-189">Kokā atlasiet "Informācija par uzņēmumu(Company)\Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="947c3-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="947c3-190">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-190">Click Bind.</span></span>
72. <span data-ttu-id="947c3-191">Kokā atlasiet “Maksājumi= Transakcijas\Apraksts”.</span><span class="sxs-lookup"><span data-stu-id="947c3-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="947c3-192">Kokā atlasiet “Transakcijas\Apraksts(Txt)”.</span><span class="sxs-lookup"><span data-stu-id="947c3-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="947c3-193">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-193">Click Bind.</span></span>
75. <span data-ttu-id="947c3-194">Kokā atlasiet "Maksājumi= Transakcijas\Pilns identifikācijas kods(End2EndID)".</span><span class="sxs-lookup"><span data-stu-id="947c3-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="947c3-195">Kokā atlasiet 'Transactions\$EndToEndID'.</span><span class="sxs-lookup"><span data-stu-id="947c3-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="947c3-196">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-196">Click Bind.</span></span>
78. <span data-ttu-id="947c3-197">Kokā atlasiet "Maksājumi= Transakcijas\Instruētā summa(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="947c3-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="947c3-198">Kokā atlasiet "Transactions\$Amount".</span><span class="sxs-lookup"><span data-stu-id="947c3-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="947c3-199">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-199">Click Bind.</span></span>
81. <span data-ttu-id="947c3-200">Kokā atlasiet "Maksājumi= Transakcijas\Transakcijas datums(TransactionDate)".</span><span class="sxs-lookup"><span data-stu-id="947c3-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="947c3-201">Kokā atlasiet “Transakcijas\Datums(TransDate)”.</span><span class="sxs-lookup"><span data-stu-id="947c3-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="947c3-202">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="947c3-203">Izveidotās kartēšanas apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="947c3-203">Validate created mapping</span></span>
1. <span data-ttu-id="947c3-204">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="947c3-204">Click Validate.</span></span>
    * <span data-ttu-id="947c3-205">Validējiet jauno kartēšanu, lai pārliecinātos, ka visi saistījumi ir pareizi.</span><span class="sxs-lookup"><span data-stu-id="947c3-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="947c3-206">Noklikšķiniet uz bultiņas, lai izvērstu vai sakļautu sadaļu Kļūdu saraksts.</span><span class="sxs-lookup"><span data-stu-id="947c3-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="947c3-207">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="947c3-207">Click Save.</span></span>
4. <span data-ttu-id="947c3-208">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="947c3-208">Close the page.</span></span>
5. <span data-ttu-id="947c3-209">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="947c3-209">Close the page.</span></span>
6. <span data-ttu-id="947c3-210">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="947c3-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="947c3-211">Mainiet modeļa konfigurācijas pašreizējās versijas statusu.</span><span class="sxs-lookup"><span data-stu-id="947c3-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="947c3-212">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="947c3-212">Click Change status.</span></span>
    * <span data-ttu-id="947c3-213">Mainiet izstrādātās modeļa konfigurācijas statusu — no Melnraksts uz Pabeigts, lai tā kļūtu pieejama maksājumu formāta noformējumam.</span><span class="sxs-lookup"><span data-stu-id="947c3-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="947c3-214">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="947c3-214">Click Complete.</span></span>
    * <span data-ttu-id="947c3-215">Atlasiet Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="947c3-215">Select Complete.</span></span>  
3. <span data-ttu-id="947c3-216">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="947c3-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="947c3-217">Piemēram, “1. versija”.</span><span class="sxs-lookup"><span data-stu-id="947c3-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="947c3-218">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="947c3-218">Click OK.</span></span>
5. <span data-ttu-id="947c3-219">Atlasiet pašreizējās konfigurācijas pabeigto versiju.</span><span class="sxs-lookup"><span data-stu-id="947c3-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="947c3-220">Ņemiet vērā, ka izveidotā konfigurācija tiek saglabāta kā pabeigta versija 1.</span><span class="sxs-lookup"><span data-stu-id="947c3-220">Note that the created configuration is saved as completed version 1.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]