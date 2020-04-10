---
title: ER domēnam specifiska datu modeļa izveide
description: Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2b93f74a121de4c23eb5dddfb94c6596b78544d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142666"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="b8018-103">ER domēnam specifiska datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="b8018-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8018-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="b8018-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="b8018-105">Šis datu modelis vēlāk tiek izmantots kā datu avots, kad veidojat maksājumu dokumentu formātu.</span><span class="sxs-lookup"><span data-stu-id="b8018-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="b8018-106">Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="b8018-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="b8018-107">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas aprakstītas procedūrā "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".</span><span class="sxs-lookup"><span data-stu-id="b8018-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="b8018-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="b8018-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="b8018-109">Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="b8018-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="b8018-110">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".</span><span class="sxs-lookup"><span data-stu-id="b8018-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="b8018-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="b8018-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="b8018-112">Jūs izveidosit konfigurāciju, kas satur datu modeli elektronisko maksājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="b8018-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="b8018-113">Šis datu modelis tiks vēlāk izmantots par datu avotu, veidojot maksājumu dokumentu formātu.</span><span class="sxs-lookup"><span data-stu-id="b8018-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="b8018-114">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="b8018-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="b8018-115">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="b8018-116">Laukā Nosaukums ierakstiet "Maksājumi (vienkāršots modelis)".</span><span class="sxs-lookup"><span data-stu-id="b8018-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="b8018-117">Laukā Apraksts ierakstiet "Maksājumu modeļa konfigurācija".</span><span class="sxs-lookup"><span data-stu-id="b8018-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="b8018-118">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="b8018-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="b8018-119">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b8018-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="b8018-120">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="b8018-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="b8018-121">Noklikšķiniet uz pogas 'Izveidot konfigurāciju', lai pabeigtu konfigurācijas izveides uzdevumu</span><span class="sxs-lookup"><span data-stu-id="b8018-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="b8018-122">Datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="b8018-122">Create a data model</span></span>
<span data-ttu-id="b8018-123">Jūs veidojat jaunu datu modeli atlasītajai konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="b8018-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="b8018-124">Šīs konfigurācijas versijas statuss būs Melnraksts.</span><span class="sxs-lookup"><span data-stu-id="b8018-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="b8018-125">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="b8018-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="b8018-126">Definēt struktūru pusei, kas piedalās maksājuma procesā</span><span class="sxs-lookup"><span data-stu-id="b8018-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="b8018-127">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b8018-128">Laukā Nosaukums ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="b8018-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="b8018-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-129">Click Add.</span></span>
4. <span data-ttu-id="b8018-130">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="b8018-131">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="b8018-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="b8018-132">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b8018-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="b8018-133">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-133">Click Add.</span></span>
8. <span data-ttu-id="b8018-134">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="b8018-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="b8018-135">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="b8018-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="b8018-136">Šī modeļa bankas struktūras definēšana</span><span class="sxs-lookup"><span data-stu-id="b8018-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="b8018-137">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b8018-138">Laukā Nosaukums ierakstiet "Aģents".</span><span class="sxs-lookup"><span data-stu-id="b8018-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="b8018-139">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="b8018-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="b8018-140">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-140">Click Add.</span></span>
5. <span data-ttu-id="b8018-141">Laukā Apraksts ierakstiet “Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.”.</span><span class="sxs-lookup"><span data-stu-id="b8018-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="b8018-142">Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.</span><span class="sxs-lookup"><span data-stu-id="b8018-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="b8018-143">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="b8018-144">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="b8018-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="b8018-145">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b8018-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="b8018-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-146">Click Add.</span></span>
10. <span data-ttu-id="b8018-147">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="b8018-148">Laukā Nosaukums ierakstiet "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="b8018-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="b8018-149">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-149">Click Add.</span></span>
13. <span data-ttu-id="b8018-150">Laukā Apraksts ievadiet “Bankas identifikācijas kods”.</span><span class="sxs-lookup"><span data-stu-id="b8018-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="b8018-151">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="b8018-152">Laukā Nosaukums ierakstiet "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="b8018-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="b8018-153">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-153">Click Add.</span></span>
17. <span data-ttu-id="b8018-154">Laukā Apraksts ievadiet “Reģistrācijas numurs”.</span><span class="sxs-lookup"><span data-stu-id="b8018-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="b8018-155">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="b8018-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="b8018-156">Šī modeļa bankas konta struktūras definēšana</span><span class="sxs-lookup"><span data-stu-id="b8018-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="b8018-157">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b8018-158">Laukā Nosaukums ierakstiet "Konts".</span><span class="sxs-lookup"><span data-stu-id="b8018-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="b8018-159">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="b8018-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="b8018-160">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-160">Click Add.</span></span>
5. <span data-ttu-id="b8018-161">Laukā Apraksts ierakstiet “Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).”.</span><span class="sxs-lookup"><span data-stu-id="b8018-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="b8018-162">Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).</span><span class="sxs-lookup"><span data-stu-id="b8018-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="b8018-163">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="b8018-164">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="b8018-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="b8018-165">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b8018-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="b8018-166">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-166">Click Add.</span></span>
10. <span data-ttu-id="b8018-167">Laukā Apraksts ievadiet “Valūtas kods”.</span><span class="sxs-lookup"><span data-stu-id="b8018-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="b8018-168">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b8018-169">Laukā Nosaukums ierakstiet "Number".</span><span class="sxs-lookup"><span data-stu-id="b8018-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="b8018-170">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-170">Click Add.</span></span>
14. <span data-ttu-id="b8018-171">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="b8018-172">Laukā Nosaukums ierakstiet "IBAN".</span><span class="sxs-lookup"><span data-stu-id="b8018-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="b8018-173">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-173">Click Add.</span></span>
17. <span data-ttu-id="b8018-174">Laukā Apraksts ievadiet “Starptautiskais bankas konta numurs ”.</span><span class="sxs-lookup"><span data-stu-id="b8018-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="b8018-175">Definēt maksājuma ziņojuma struktūru kredīta pārsūtīšanas maksājuma veidam</span><span class="sxs-lookup"><span data-stu-id="b8018-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="b8018-176">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b8018-177">Laukā Jauns zars ievadiet “Modeļa sakne”.</span><span class="sxs-lookup"><span data-stu-id="b8018-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="b8018-178">Laukā Nosaukums ierakstiet "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="b8018-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="b8018-179">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-179">Click Add.</span></span>
5. <span data-ttu-id="b8018-180">Laukā Atrast ierakstiet “CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="b8018-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="b8018-181">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="b8018-181">Click Find previous.</span></span>
7. <span data-ttu-id="b8018-182">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b8018-183">Laukā Nosaukums ievadiet "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="b8018-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="b8018-184">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-184">Click Add.</span></span>
10. <span data-ttu-id="b8018-185">Laukā Apraksts ievadiet “Atsauce no punkta uz punktu, kuru norādījusi instruējošā puse ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).”.</span><span class="sxs-lookup"><span data-stu-id="b8018-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="b8018-186">Atsauce no punkta uz punktu, kuru piešķīrusi instruējošā puse, ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).</span><span class="sxs-lookup"><span data-stu-id="b8018-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="b8018-187">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b8018-188">Laukā Nosaukums ievadiet "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="b8018-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="b8018-189">Laukā Vienuma tips atlasiet "DateTime".</span><span class="sxs-lookup"><span data-stu-id="b8018-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="b8018-190">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-190">Click Add.</span></span>
15. <span data-ttu-id="b8018-191">Laukā Apraksts ievadiet “Maksājuma ziņojuma izveides datums un laiks.”.</span><span class="sxs-lookup"><span data-stu-id="b8018-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="b8018-192">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="b8018-193">Definējiet maksāšanas transakcijas struktūras šim modelim.</span><span class="sxs-lookup"><span data-stu-id="b8018-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="b8018-194">Laukā Nosaukums ierakstiet "Maksājumi".</span><span class="sxs-lookup"><span data-stu-id="b8018-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="b8018-195">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="b8018-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="b8018-196">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-196">Click Add.</span></span>
20. <span data-ttu-id="b8018-197">Laukā Apraksts ievadiet "Aktīvā ziņojuma maksājuma rindas".</span><span class="sxs-lookup"><span data-stu-id="b8018-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="b8018-198">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b8018-199">Laukā Nosaukums ierakstiet "Kreditors".</span><span class="sxs-lookup"><span data-stu-id="b8018-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="b8018-200">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="b8018-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="b8018-201">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-201">Click Add.</span></span>
25. <span data-ttu-id="b8018-202">Laukā Apraksts ierakstiet “Puse, kurai ir jāsaņem kāda naudas summa.”.</span><span class="sxs-lookup"><span data-stu-id="b8018-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="b8018-203">Noklikšķiniet uz Pārslēgt vienuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="b8018-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="b8018-204">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="b8018-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="b8018-205">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="b8018-205">Click Find next.</span></span>
29. <span data-ttu-id="b8018-206">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="b8018-206">Click OK.</span></span>
30. <span data-ttu-id="b8018-207">Laukā Atrast ierakstiet “Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="b8018-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="b8018-208">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="b8018-208">Click Find next.</span></span>
32. <span data-ttu-id="b8018-209">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="b8018-210">Laukā Nosaukums ierakstiet "Debitors".</span><span class="sxs-lookup"><span data-stu-id="b8018-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="b8018-211">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-211">Click Add.</span></span>
35. <span data-ttu-id="b8018-212">Laukā Apraksts ierakstiet “Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.”.</span><span class="sxs-lookup"><span data-stu-id="b8018-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="b8018-213">Noklikšķiniet uz Pārslēgt vienuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="b8018-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="b8018-214">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="b8018-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="b8018-215">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="b8018-215">Click Find next.</span></span>
39. <span data-ttu-id="b8018-216">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="b8018-216">Click OK.</span></span>
40. <span data-ttu-id="b8018-217">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="b8018-217">Click Find next.</span></span>
41. <span data-ttu-id="b8018-218">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="b8018-219">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="b8018-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="b8018-220">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b8018-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="b8018-221">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-221">Click Add.</span></span>
45. <span data-ttu-id="b8018-222">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="b8018-223">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="b8018-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="b8018-224">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-224">Click Add.</span></span>
48. <span data-ttu-id="b8018-225">Laukā Apraksts ievadiet “Valūtas kods”.</span><span class="sxs-lookup"><span data-stu-id="b8018-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="b8018-226">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="b8018-227">Laukā Nosaukums ierakstiet "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="b8018-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="b8018-228">Laukā Vienuma tips atlasiet "Date".</span><span class="sxs-lookup"><span data-stu-id="b8018-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="b8018-229">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-229">Click Add.</span></span>
53. <span data-ttu-id="b8018-230">Laukā Apraksts ievadiet “Darījuma datums”.</span><span class="sxs-lookup"><span data-stu-id="b8018-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="b8018-231">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="b8018-232">Laukā Nosaukums ierakstiet "'InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="b8018-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="b8018-233">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="b8018-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="b8018-234">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-234">Click Add.</span></span>
58. <span data-ttu-id="b8018-235">Laukā Apraksts ievadiet “Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru, pirms ir ieturētas maksas.</span><span class="sxs-lookup"><span data-stu-id="b8018-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="b8018-236">Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.".</span><span class="sxs-lookup"><span data-stu-id="b8018-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="b8018-237">Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru pirms maksu ieturēšanas.</span><span class="sxs-lookup"><span data-stu-id="b8018-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="b8018-238">Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="b8018-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="b8018-239">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b8018-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="b8018-240">Laukā Nosaukums ierakstiet "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="b8018-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="b8018-241">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="b8018-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="b8018-242">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b8018-242">Click Add.</span></span>
63. <span data-ttu-id="b8018-243">Laukā Apraksts ievadiet “Unikālais identifikators, kuru piešķīrusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="b8018-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="b8018-244">Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā."</span><span class="sxs-lookup"><span data-stu-id="b8018-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="b8018-245">Laukā Nosaukums ierakstiet "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="b8018-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="b8018-246">PaymentModel nosaukums sakrīt ar iepriekš definētiem maksājumu veidlapu interfeisiem.</span><span class="sxs-lookup"><span data-stu-id="b8018-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="b8018-247">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b8018-247">Click Save.</span></span>
66. <span data-ttu-id="b8018-248">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b8018-248">Close the page.</span></span>

