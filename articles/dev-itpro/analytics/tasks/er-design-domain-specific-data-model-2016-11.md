--- 
title: "ER domēnam specifiska datu modeļa izveide"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="b278e-103">ER domēnam specifiska datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="b278e-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b278e-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="b278e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="b278e-105">Šis datu modelis vēlāk tiek izmantots kā datu avots, kad veidojat maksājumu dokumentu formātu.</span><span class="sxs-lookup"><span data-stu-id="b278e-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="b278e-106">Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="b278e-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="b278e-107">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="b278e-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="b278e-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="b278e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b278e-109">Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b278e-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="b278e-110">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to ka aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="b278e-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="b278e-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="b278e-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="b278e-112">Jūs izveidosit konfigurāciju, kas satur datu modeli elektronisko maksājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="b278e-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="b278e-113">Šis datu modelis tiks vēlāk izmantots par datu avotu, veidojot maksājumu dokumentu formātu.</span><span class="sxs-lookup"><span data-stu-id="b278e-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="b278e-114">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="b278e-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="b278e-115">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="b278e-116">Laukā Nosaukums ierakstiet "Maksājumi (vienkāršots modelis)".</span><span class="sxs-lookup"><span data-stu-id="b278e-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="b278e-117">Maksājumi (vienkāršots modelis)</span><span class="sxs-lookup"><span data-stu-id="b278e-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="b278e-118">Laukā Apraksts ierakstiet "Maksājumu modeļa konfigurācija".</span><span class="sxs-lookup"><span data-stu-id="b278e-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="b278e-119">Maksājuma modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="b278e-119">Payment model configuration</span></span>  
    * <span data-ttu-id="b278e-120">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="b278e-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="b278e-121">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b278e-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="b278e-122">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="b278e-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="b278e-123">Noklikšķiniet uz pogas Izveidot konfigurāciju, lai pabeigtu konfigurācijas izveides uzdevumu</span><span class="sxs-lookup"><span data-stu-id="b278e-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="b278e-124">Datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="b278e-124">Create a data model</span></span>
    * <span data-ttu-id="b278e-125">Jūs veidojat jaunu datu modeli atlasītajai konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="b278e-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="b278e-126">Šīs konfigurācijas versijas statuss būs Melnraksts.</span><span class="sxs-lookup"><span data-stu-id="b278e-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="b278e-127">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="b278e-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="b278e-128">Definēt struktūru pusei, kas piedalās maksājuma procesā</span><span class="sxs-lookup"><span data-stu-id="b278e-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="b278e-129">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b278e-130">Laukā Nosaukums ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="b278e-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="b278e-131">Puse</span><span class="sxs-lookup"><span data-stu-id="b278e-131">Party</span></span>  
3. <span data-ttu-id="b278e-132">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-132">Click Add.</span></span>
4. <span data-ttu-id="b278e-133">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="b278e-134">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="b278e-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="b278e-135">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="b278e-135">Name</span></span>  
6. <span data-ttu-id="b278e-136">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b278e-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="b278e-137">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-137">Click Add.</span></span>
8. <span data-ttu-id="b278e-138">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="b278e-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="b278e-139">Puse</span><span class="sxs-lookup"><span data-stu-id="b278e-139">Party</span></span>  
9. <span data-ttu-id="b278e-140">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="b278e-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="b278e-141">Šī modeļa bankas struktūras definēšana</span><span class="sxs-lookup"><span data-stu-id="b278e-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="b278e-142">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b278e-143">Laukā Nosaukums ierakstiet "Aģents".</span><span class="sxs-lookup"><span data-stu-id="b278e-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="b278e-144">Aģents</span><span class="sxs-lookup"><span data-stu-id="b278e-144">Agent</span></span>  
3. <span data-ttu-id="b278e-145">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="b278e-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="b278e-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-146">Click Add.</span></span>
5. <span data-ttu-id="b278e-147">Laukā Apraksts ierakstiet “Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.”.</span><span class="sxs-lookup"><span data-stu-id="b278e-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="b278e-148">Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.</span><span class="sxs-lookup"><span data-stu-id="b278e-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="b278e-149">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="b278e-150">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="b278e-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="b278e-151">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="b278e-151">Name</span></span>  
8. <span data-ttu-id="b278e-152">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b278e-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="b278e-153">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-153">Click Add.</span></span>
10. <span data-ttu-id="b278e-154">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="b278e-155">Laukā Nosaukums ierakstiet "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="b278e-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="b278e-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="b278e-156">SWIFT</span></span>  
12. <span data-ttu-id="b278e-157">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-157">Click Add.</span></span>
13. <span data-ttu-id="b278e-158">Laukā Apraksts ievadiet “Bankas identifikācijas kods”.</span><span class="sxs-lookup"><span data-stu-id="b278e-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="b278e-159">Bankas identifikācijas kods</span><span class="sxs-lookup"><span data-stu-id="b278e-159">Bank identification code</span></span>  
14. <span data-ttu-id="b278e-160">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="b278e-161">Laukā Nosaukums ierakstiet "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="b278e-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="b278e-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="b278e-162">RoutingNumber</span></span>  
16. <span data-ttu-id="b278e-163">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-163">Click Add.</span></span>
17. <span data-ttu-id="b278e-164">Laukā Apraksts ievadiet “Reģistrācijas numurs”.</span><span class="sxs-lookup"><span data-stu-id="b278e-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="b278e-165">Reģistrācijas numurs</span><span class="sxs-lookup"><span data-stu-id="b278e-165">Routing number</span></span>  
18. <span data-ttu-id="b278e-166">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="b278e-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="b278e-167">Šī modeļa bankas konta struktūras definēšana</span><span class="sxs-lookup"><span data-stu-id="b278e-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="b278e-168">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b278e-169">Laukā Nosaukums ierakstiet "Konts".</span><span class="sxs-lookup"><span data-stu-id="b278e-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="b278e-170">Konts</span><span class="sxs-lookup"><span data-stu-id="b278e-170">Account</span></span>  
3. <span data-ttu-id="b278e-171">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="b278e-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="b278e-172">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-172">Click Add.</span></span>
5. <span data-ttu-id="b278e-173">Laukā Apraksts ierakstiet “Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).”.</span><span class="sxs-lookup"><span data-stu-id="b278e-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="b278e-174">Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).</span><span class="sxs-lookup"><span data-stu-id="b278e-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="b278e-175">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="b278e-176">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="b278e-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="b278e-177">Valūta</span><span class="sxs-lookup"><span data-stu-id="b278e-177">Currency</span></span>  
8. <span data-ttu-id="b278e-178">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b278e-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="b278e-179">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-179">Click Add.</span></span>
10. <span data-ttu-id="b278e-180">Laukā Apraksts ievadiet “Valūtas kods”.</span><span class="sxs-lookup"><span data-stu-id="b278e-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="b278e-181">Valūtas kods</span><span class="sxs-lookup"><span data-stu-id="b278e-181">Currency code</span></span>  
11. <span data-ttu-id="b278e-182">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b278e-183">Laukā Nosaukums ierakstiet "Number".</span><span class="sxs-lookup"><span data-stu-id="b278e-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="b278e-184">Skaits</span><span class="sxs-lookup"><span data-stu-id="b278e-184">Number</span></span>  
13. <span data-ttu-id="b278e-185">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-185">Click Add.</span></span>
14. <span data-ttu-id="b278e-186">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="b278e-187">Laukā Nosaukums ierakstiet "IBAN".</span><span class="sxs-lookup"><span data-stu-id="b278e-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="b278e-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="b278e-188">IBAN</span></span>  
16. <span data-ttu-id="b278e-189">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-189">Click Add.</span></span>
17. <span data-ttu-id="b278e-190">Laukā Apraksts ievadiet “Starptautiskais bankas konta numurs ”.</span><span class="sxs-lookup"><span data-stu-id="b278e-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="b278e-191">Starptautiskais bankas konta numurs</span><span class="sxs-lookup"><span data-stu-id="b278e-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="b278e-192">Definēt maksājuma ziņojuma struktūru kredīta pārsūtīšanas maksājuma veidam</span><span class="sxs-lookup"><span data-stu-id="b278e-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="b278e-193">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b278e-194">Laukā Jauns zars ievadiet “Modeļa sakne”.</span><span class="sxs-lookup"><span data-stu-id="b278e-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="b278e-195">Laukā Nosaukums ierakstiet "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="b278e-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="b278e-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="b278e-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="b278e-197">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-197">Click Add.</span></span>
5. <span data-ttu-id="b278e-198">Laukā Atrast ierakstiet “CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="b278e-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="b278e-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="b278e-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="b278e-200">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="b278e-200">Click Find previous.</span></span>
7. <span data-ttu-id="b278e-201">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b278e-202">Laukā Nosaukums ievadiet "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="b278e-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="b278e-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="b278e-203">MessageIdentification</span></span>  
9. <span data-ttu-id="b278e-204">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-204">Click Add.</span></span>
10. <span data-ttu-id="b278e-205">Laukā Apraksts ievadiet “Atsauce no punkta uz punktu, kuru norādījusi instruējošā puse ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).”.</span><span class="sxs-lookup"><span data-stu-id="b278e-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="b278e-206">Atsauce no punkta uz punktu, kuru piešķīrusi instruējošā puse, ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).</span><span class="sxs-lookup"><span data-stu-id="b278e-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="b278e-207">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b278e-208">Laukā Nosaukums ievadiet "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="b278e-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="b278e-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="b278e-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="b278e-210">Laukā Vienuma tips atlasiet "DateTime".</span><span class="sxs-lookup"><span data-stu-id="b278e-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="b278e-211">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-211">Click Add.</span></span>
15. <span data-ttu-id="b278e-212">Laukā Apraksts ievadiet “Maksājuma ziņojuma izveides datums un laiks.”.</span><span class="sxs-lookup"><span data-stu-id="b278e-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="b278e-213">Datums un laiks, kad maksājuma ziņojums tika izveidots.</span><span class="sxs-lookup"><span data-stu-id="b278e-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="b278e-214">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="b278e-215">Definējiet maksāšanas transakcijas struktūras šim modelim.</span><span class="sxs-lookup"><span data-stu-id="b278e-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="b278e-216">Laukā Nosaukums ierakstiet "Maksājumi".</span><span class="sxs-lookup"><span data-stu-id="b278e-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="b278e-217">Maksājumi</span><span class="sxs-lookup"><span data-stu-id="b278e-217">Payments</span></span>  
18. <span data-ttu-id="b278e-218">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="b278e-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="b278e-219">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-219">Click Add.</span></span>
20. <span data-ttu-id="b278e-220">Laukā Apraksts ievadiet "Aktīvā ziņojuma maksājuma rindas".</span><span class="sxs-lookup"><span data-stu-id="b278e-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="b278e-221">Pašreizējā ziņojuma maksājuma rindas</span><span class="sxs-lookup"><span data-stu-id="b278e-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="b278e-222">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b278e-223">Laukā Nosaukums ierakstiet "Kreditors".</span><span class="sxs-lookup"><span data-stu-id="b278e-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="b278e-224">Kreditors</span><span class="sxs-lookup"><span data-stu-id="b278e-224">Creditor</span></span>  
23. <span data-ttu-id="b278e-225">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="b278e-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="b278e-226">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-226">Click Add.</span></span>
25. <span data-ttu-id="b278e-227">Laukā Apraksts ierakstiet “Puse, kurai ir jāsaņem kāda naudas summa.”.</span><span class="sxs-lookup"><span data-stu-id="b278e-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="b278e-228">Puse, kurai ir jāsaņem kāda naudas summa.</span><span class="sxs-lookup"><span data-stu-id="b278e-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="b278e-229">Noklikšķiniet uz Pārslēgt vienuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="b278e-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="b278e-230">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="b278e-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="b278e-231">Puse</span><span class="sxs-lookup"><span data-stu-id="b278e-231">Party</span></span>  
28. <span data-ttu-id="b278e-232">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="b278e-232">Click Find next.</span></span>
29. <span data-ttu-id="b278e-233">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b278e-233">Click OK.</span></span>
30. <span data-ttu-id="b278e-234">Laukā Atrast ierakstiet “Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="b278e-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="b278e-235">Maksājumi</span><span class="sxs-lookup"><span data-stu-id="b278e-235">Payments</span></span>  
31. <span data-ttu-id="b278e-236">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="b278e-236">Click Find next.</span></span>
32. <span data-ttu-id="b278e-237">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="b278e-238">Laukā Nosaukums ierakstiet "Debitors".</span><span class="sxs-lookup"><span data-stu-id="b278e-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="b278e-239">Debitors</span><span class="sxs-lookup"><span data-stu-id="b278e-239">Debtor</span></span>  
34. <span data-ttu-id="b278e-240">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-240">Click Add.</span></span>
35. <span data-ttu-id="b278e-241">Laukā Apraksts ierakstiet “Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.”.</span><span class="sxs-lookup"><span data-stu-id="b278e-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="b278e-242">Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.</span><span class="sxs-lookup"><span data-stu-id="b278e-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="b278e-243">Noklikšķiniet uz Pārslēgt vienuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="b278e-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="b278e-244">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="b278e-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="b278e-245">Puse</span><span class="sxs-lookup"><span data-stu-id="b278e-245">Party</span></span>  
38. <span data-ttu-id="b278e-246">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="b278e-246">Click Find next.</span></span>
39. <span data-ttu-id="b278e-247">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="b278e-247">Click OK.</span></span>
40. <span data-ttu-id="b278e-248">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="b278e-248">Click Find next.</span></span>
41. <span data-ttu-id="b278e-249">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="b278e-250">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="b278e-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="b278e-251">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b278e-251">Description</span></span>  
43. <span data-ttu-id="b278e-252">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b278e-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="b278e-253">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-253">Click Add.</span></span>
45. <span data-ttu-id="b278e-254">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="b278e-255">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="b278e-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="b278e-256">Valūta</span><span class="sxs-lookup"><span data-stu-id="b278e-256">Currency</span></span>  
47. <span data-ttu-id="b278e-257">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-257">Click Add.</span></span>
48. <span data-ttu-id="b278e-258">Laukā Apraksts ievadiet “Valūtas kods”.</span><span class="sxs-lookup"><span data-stu-id="b278e-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="b278e-259">Valūtas kods</span><span class="sxs-lookup"><span data-stu-id="b278e-259">Currency code</span></span>  
49. <span data-ttu-id="b278e-260">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="b278e-261">Laukā Nosaukums ierakstiet "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="b278e-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="b278e-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="b278e-262">TransactionDate</span></span>  
51. <span data-ttu-id="b278e-263">Laukā Vienuma tips atlasiet "Date".</span><span class="sxs-lookup"><span data-stu-id="b278e-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="b278e-264">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-264">Click Add.</span></span>
53. <span data-ttu-id="b278e-265">Laukā Apraksts ievadiet “Darījuma datums”.</span><span class="sxs-lookup"><span data-stu-id="b278e-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="b278e-266">Darījuma datums</span><span class="sxs-lookup"><span data-stu-id="b278e-266">Transaction date</span></span>  
54. <span data-ttu-id="b278e-267">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="b278e-268">Laukā Nosaukums ierakstiet "'InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="b278e-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="b278e-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="b278e-269">InstructedAmount</span></span>  
56. <span data-ttu-id="b278e-270">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="b278e-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="b278e-271">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-271">Click Add.</span></span>
58. <span data-ttu-id="b278e-272">Laukā Apraksts ievadiet “Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru, pirms ir ieturētas maksas.</span><span class="sxs-lookup"><span data-stu-id="b278e-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="b278e-273">Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.".</span><span class="sxs-lookup"><span data-stu-id="b278e-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="b278e-274">Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru pirms maksu ieturēšanas.</span><span class="sxs-lookup"><span data-stu-id="b278e-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="b278e-275">Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="b278e-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="b278e-276">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b278e-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="b278e-277">Laukā Nosaukums ierakstiet "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="b278e-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="b278e-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="b278e-278">End2EndID</span></span>  
61. <span data-ttu-id="b278e-279">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b278e-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="b278e-280">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b278e-280">Click Add.</span></span>
63. <span data-ttu-id="b278e-281">Laukā Apraksts ievadiet “Unikālais identifikators, kuru piešķīrusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="b278e-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="b278e-282">Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā."</span><span class="sxs-lookup"><span data-stu-id="b278e-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="b278e-283">Unikāls identifikators, kuru piešķīrusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="b278e-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="b278e-284">Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā.</span><span class="sxs-lookup"><span data-stu-id="b278e-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="b278e-285">Laukā Nosaukums ierakstiet "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="b278e-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="b278e-286">PaymentModel nosaukums sakrīt ar iepriekš definētiem maksājumu veidlapu interfeisiem.</span><span class="sxs-lookup"><span data-stu-id="b278e-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="b278e-287">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b278e-287">Click Save.</span></span>
66. <span data-ttu-id="b278e-288">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b278e-288">Close the page.</span></span>


