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
ms.openlocfilehash: d7882a7a17f5736d9d5a11cd91ac963fa89ff12f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042900"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="9bc30-103">ER domēnam specifiska datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="9bc30-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9bc30-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="9bc30-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="9bc30-105">Šis datu modelis vēlāk tiek izmantots kā datu avots, kad veidojat maksājumu dokumentu formātu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="9bc30-106">Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="9bc30-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="9bc30-107">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="9bc30-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="9bc30-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="9bc30-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="9bc30-109">Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9bc30-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="9bc30-110">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to ka aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
    
2. <span data-ttu-id="9bc30-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="9bc30-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="9bc30-112">Jūs izveidosit konfigurāciju, kas satur datu modeli elektronisko maksājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="9bc30-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="9bc30-113">Šis datu modelis tiks vēlāk izmantots par datu avotu, veidojot maksājumu dokumentu formātu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="9bc30-114">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="9bc30-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="9bc30-115">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="9bc30-116">Laukā Nosaukums ierakstiet "Maksājumi (vienkāršots modelis)".</span><span class="sxs-lookup"><span data-stu-id="9bc30-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="9bc30-117">Laukā Apraksts ierakstiet "Maksājumu modeļa konfigurācija".</span><span class="sxs-lookup"><span data-stu-id="9bc30-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="9bc30-118">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="9bc30-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="9bc30-119">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="9bc30-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="9bc30-120">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="9bc30-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="9bc30-121">Noklikšķiniet uz pogas Izveidot konfigurāciju, lai pabeigtu konfigurācijas izveides uzdevumu</span><span class="sxs-lookup"><span data-stu-id="9bc30-121">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="9bc30-122">Datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="9bc30-122">Create a data model</span></span>
<span data-ttu-id="9bc30-123">Jūs veidojat jaunu datu modeli atlasītajai konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="9bc30-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="9bc30-124">Šīs konfigurācijas versijas statuss būs Melnraksts.</span><span class="sxs-lookup"><span data-stu-id="9bc30-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="9bc30-125">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="9bc30-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="9bc30-126">Definēt struktūru pusei, kas piedalās maksājuma procesā</span><span class="sxs-lookup"><span data-stu-id="9bc30-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="9bc30-127">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="9bc30-128">Laukā Nosaukums ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="9bc30-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-129">Click Add.</span></span>
4. <span data-ttu-id="9bc30-130">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="9bc30-131">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="9bc30-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="9bc30-132">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="9bc30-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="9bc30-133">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-133">Click Add.</span></span>
8. <span data-ttu-id="9bc30-134">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="9bc30-135">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="9bc30-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="9bc30-136">Šī modeļa bankas struktūras definēšana</span><span class="sxs-lookup"><span data-stu-id="9bc30-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="9bc30-137">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="9bc30-138">Laukā Nosaukums ierakstiet "Aģents".</span><span class="sxs-lookup"><span data-stu-id="9bc30-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="9bc30-139">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="9bc30-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="9bc30-140">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-140">Click Add.</span></span>
5. <span data-ttu-id="9bc30-141">Laukā Apraksts ierakstiet “Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="9bc30-142">Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="9bc30-143">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="9bc30-144">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="9bc30-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="9bc30-145">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="9bc30-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="9bc30-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-146">Click Add.</span></span>
10. <span data-ttu-id="9bc30-147">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="9bc30-148">Laukā Nosaukums ierakstiet "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="9bc30-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="9bc30-149">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-149">Click Add.</span></span>
13. <span data-ttu-id="9bc30-150">Laukā Apraksts ievadiet “Bankas identifikācijas kods”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="9bc30-151">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="9bc30-152">Laukā Nosaukums ierakstiet "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="9bc30-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="9bc30-153">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-153">Click Add.</span></span>
17. <span data-ttu-id="9bc30-154">Laukā Apraksts ievadiet “Reģistrācijas numurs”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="9bc30-155">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="9bc30-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="9bc30-156">Šī modeļa bankas konta struktūras definēšana</span><span class="sxs-lookup"><span data-stu-id="9bc30-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="9bc30-157">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="9bc30-158">Laukā Nosaukums ierakstiet "Konts".</span><span class="sxs-lookup"><span data-stu-id="9bc30-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="9bc30-159">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="9bc30-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="9bc30-160">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-160">Click Add.</span></span>
5. <span data-ttu-id="9bc30-161">Laukā Apraksts ierakstiet “Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="9bc30-162">Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).</span><span class="sxs-lookup"><span data-stu-id="9bc30-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="9bc30-163">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="9bc30-164">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="9bc30-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="9bc30-165">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="9bc30-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="9bc30-166">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-166">Click Add.</span></span>
10. <span data-ttu-id="9bc30-167">Laukā Apraksts ievadiet “Valūtas kods”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="9bc30-168">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="9bc30-169">Laukā Nosaukums ierakstiet "Number".</span><span class="sxs-lookup"><span data-stu-id="9bc30-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="9bc30-170">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-170">Click Add.</span></span>
14. <span data-ttu-id="9bc30-171">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="9bc30-172">Laukā Nosaukums ierakstiet "IBAN".</span><span class="sxs-lookup"><span data-stu-id="9bc30-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="9bc30-173">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-173">Click Add.</span></span>
17. <span data-ttu-id="9bc30-174">Laukā Apraksts ievadiet “Starptautiskais bankas konta numurs ”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="9bc30-175">Definēt maksājuma ziņojuma struktūru kredīta pārsūtīšanas maksājuma veidam</span><span class="sxs-lookup"><span data-stu-id="9bc30-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="9bc30-176">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="9bc30-177">Laukā Jauns zars ievadiet “Modeļa sakne”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="9bc30-178">Laukā Nosaukums ierakstiet "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="9bc30-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="9bc30-179">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-179">Click Add.</span></span>
5. <span data-ttu-id="9bc30-180">Laukā Atrast ierakstiet “CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="9bc30-181">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="9bc30-181">Click Find previous.</span></span>
7. <span data-ttu-id="9bc30-182">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="9bc30-183">Laukā Nosaukums ievadiet "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="9bc30-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="9bc30-184">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-184">Click Add.</span></span>
10. <span data-ttu-id="9bc30-185">Laukā Apraksts ievadiet “Atsauce no punkta uz punktu, kuru norādījusi instruējošā puse ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="9bc30-186">Atsauce no punkta uz punktu, kuru piešķīrusi instruējošā puse, ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).</span><span class="sxs-lookup"><span data-stu-id="9bc30-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="9bc30-187">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="9bc30-188">Laukā Nosaukums ievadiet "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="9bc30-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="9bc30-189">Laukā Vienuma tips atlasiet "DateTime".</span><span class="sxs-lookup"><span data-stu-id="9bc30-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="9bc30-190">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-190">Click Add.</span></span>
15. <span data-ttu-id="9bc30-191">Laukā Apraksts ievadiet “Maksājuma ziņojuma izveides datums un laiks.”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="9bc30-192">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="9bc30-193">Definējiet maksāšanas transakcijas struktūras šim modelim.</span><span class="sxs-lookup"><span data-stu-id="9bc30-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="9bc30-194">Laukā Nosaukums ierakstiet "Maksājumi".</span><span class="sxs-lookup"><span data-stu-id="9bc30-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="9bc30-195">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="9bc30-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="9bc30-196">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-196">Click Add.</span></span>
20. <span data-ttu-id="9bc30-197">Laukā Apraksts ievadiet "Aktīvā ziņojuma maksājuma rindas".</span><span class="sxs-lookup"><span data-stu-id="9bc30-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="9bc30-198">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="9bc30-199">Laukā Nosaukums ierakstiet "Kreditors".</span><span class="sxs-lookup"><span data-stu-id="9bc30-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="9bc30-200">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="9bc30-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="9bc30-201">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-201">Click Add.</span></span>
25. <span data-ttu-id="9bc30-202">Laukā Apraksts ierakstiet “Puse, kurai ir jāsaņem kāda naudas summa.”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="9bc30-203">Noklikšķiniet uz Pārslēgt vienuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="9bc30-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="9bc30-204">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="9bc30-205">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="9bc30-205">Click Find next.</span></span>
29. <span data-ttu-id="9bc30-206">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="9bc30-206">Click OK.</span></span>
30. <span data-ttu-id="9bc30-207">Laukā Atrast ierakstiet “Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="9bc30-208">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="9bc30-208">Click Find next.</span></span>
32. <span data-ttu-id="9bc30-209">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="9bc30-210">Laukā Nosaukums ierakstiet "Debitors".</span><span class="sxs-lookup"><span data-stu-id="9bc30-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="9bc30-211">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-211">Click Add.</span></span>
35. <span data-ttu-id="9bc30-212">Laukā Apraksts ierakstiet “Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="9bc30-213">Noklikšķiniet uz Pārslēgt vienuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="9bc30-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="9bc30-214">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="9bc30-215">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="9bc30-215">Click Find next.</span></span>
39. <span data-ttu-id="9bc30-216">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="9bc30-216">Click OK.</span></span>
40. <span data-ttu-id="9bc30-217">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="9bc30-217">Click Find next.</span></span>
41. <span data-ttu-id="9bc30-218">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="9bc30-219">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="9bc30-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="9bc30-220">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="9bc30-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="9bc30-221">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-221">Click Add.</span></span>
45. <span data-ttu-id="9bc30-222">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="9bc30-223">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="9bc30-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="9bc30-224">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-224">Click Add.</span></span>
48. <span data-ttu-id="9bc30-225">Laukā Apraksts ievadiet “Valūtas kods”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="9bc30-226">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="9bc30-227">Laukā Nosaukums ierakstiet "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="9bc30-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="9bc30-228">Laukā Vienuma tips atlasiet "Date".</span><span class="sxs-lookup"><span data-stu-id="9bc30-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="9bc30-229">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-229">Click Add.</span></span>
53. <span data-ttu-id="9bc30-230">Laukā Apraksts ievadiet “Darījuma datums”.</span><span class="sxs-lookup"><span data-stu-id="9bc30-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="9bc30-231">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="9bc30-232">Laukā Nosaukums ierakstiet "'InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="9bc30-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="9bc30-233">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="9bc30-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="9bc30-234">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-234">Click Add.</span></span>
58. <span data-ttu-id="9bc30-235">Laukā Apraksts ievadiet “Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru, pirms ir ieturētas maksas.</span><span class="sxs-lookup"><span data-stu-id="9bc30-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="9bc30-236">Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.".</span><span class="sxs-lookup"><span data-stu-id="9bc30-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="9bc30-237">Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru pirms maksu ieturēšanas.</span><span class="sxs-lookup"><span data-stu-id="9bc30-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="9bc30-238">Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="9bc30-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="9bc30-239">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="9bc30-240">Laukā Nosaukums ierakstiet "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="9bc30-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="9bc30-241">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="9bc30-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="9bc30-242">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9bc30-242">Click Add.</span></span>
63. <span data-ttu-id="9bc30-243">Laukā Apraksts ievadiet “Unikālais identifikators, kuru piešķīrusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="9bc30-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="9bc30-244">Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā."</span><span class="sxs-lookup"><span data-stu-id="9bc30-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="9bc30-245">Laukā Nosaukums ierakstiet "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="9bc30-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="9bc30-246">PaymentModel nosaukums sakrīt ar iepriekš definētiem maksājumu veidlapu interfeisiem.</span><span class="sxs-lookup"><span data-stu-id="9bc30-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="9bc30-247">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9bc30-247">Click Save.</span></span>
66. <span data-ttu-id="9bc30-248">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9bc30-248">Close the page.</span></span>

