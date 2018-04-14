--- 
title: "Noformēt domēnam specifisku datu modeli elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6a9fff90af93e20e7f812022593d25963542fac1
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a><span data-ttu-id="d1f0d-103">Noformēt domēnam specifisku datu modeli elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="d1f0d-103">Design a domain-specific data model for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1f0d-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="d1f0d-105">Šis datu modelis vēlāk tiek izmantots kā datu avots, kad veidojat maksājumu dokumentu formātu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="d1f0d-106">Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="d1f0d-107">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="d1f0d-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d1f0d-109">Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="d1f0d-110">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to ka aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="d1f0d-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="d1f0d-112">Jūs izveidosit konfigurāciju, kas satur datu modeli elektronisko maksājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="d1f0d-113">Šis datu modelis tiks vēlāk izmantots par datu avotu, veidojot maksājumu dokumentu formātu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="d1f0d-114">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="d1f0d-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="d1f0d-115">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="d1f0d-116">Laukā Nosaukums ierakstiet "Maksājumi (vienkāršots modelis)".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="d1f0d-117">Maksājumi (vienkāršots modelis)</span><span class="sxs-lookup"><span data-stu-id="d1f0d-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="d1f0d-118">Laukā Apraksts ierakstiet "Maksājumu modeļa konfigurācija".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="d1f0d-119">Maksājuma modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d1f0d-119">Payment model configuration</span></span>  
    * <span data-ttu-id="d1f0d-120">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="d1f0d-121">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="d1f0d-122">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="d1f0d-123">Noklikšķiniet uz pogas Izveidot konfigurāciju, lai pabeigtu konfigurācijas izveides uzdevumu</span><span class="sxs-lookup"><span data-stu-id="d1f0d-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="d1f0d-124">Datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="d1f0d-124">Create a data model</span></span>
    * <span data-ttu-id="d1f0d-125">Jūs veidojat jaunu datu modeli atlasītajai konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="d1f0d-126">Šīs konfigurācijas versijas statuss būs Melnraksts.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="d1f0d-127">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="d1f0d-128">Definēt struktūru pusei, kas piedalās maksājuma procesā</span><span class="sxs-lookup"><span data-stu-id="d1f0d-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="d1f0d-129">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="d1f0d-130">Laukā Nosaukums ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="d1f0d-131">Puse</span><span class="sxs-lookup"><span data-stu-id="d1f0d-131">Party</span></span>  
3. <span data-ttu-id="d1f0d-132">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-132">Click Add.</span></span>
4. <span data-ttu-id="d1f0d-133">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="d1f0d-134">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="d1f0d-135">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="d1f0d-135">Name</span></span>  
6. <span data-ttu-id="d1f0d-136">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="d1f0d-137">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-137">Click Add.</span></span>
8. <span data-ttu-id="d1f0d-138">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="d1f0d-139">Puse</span><span class="sxs-lookup"><span data-stu-id="d1f0d-139">Party</span></span>  
9. <span data-ttu-id="d1f0d-140">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="d1f0d-141">Šī modeļa bankas struktūras definēšana</span><span class="sxs-lookup"><span data-stu-id="d1f0d-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="d1f0d-142">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="d1f0d-143">Laukā Nosaukums ierakstiet "Aģents".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="d1f0d-144">Aģents</span><span class="sxs-lookup"><span data-stu-id="d1f0d-144">Agent</span></span>  
3. <span data-ttu-id="d1f0d-145">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="d1f0d-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-146">Click Add.</span></span>
5. <span data-ttu-id="d1f0d-147">Laukā Apraksts ierakstiet “Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="d1f0d-148">Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="d1f0d-149">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="d1f0d-150">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="d1f0d-151">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="d1f0d-151">Name</span></span>  
8. <span data-ttu-id="d1f0d-152">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="d1f0d-153">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-153">Click Add.</span></span>
10. <span data-ttu-id="d1f0d-154">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="d1f0d-155">Laukā Nosaukums ierakstiet "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="d1f0d-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="d1f0d-156">SWIFT</span></span>  
12. <span data-ttu-id="d1f0d-157">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-157">Click Add.</span></span>
13. <span data-ttu-id="d1f0d-158">Laukā Apraksts ievadiet “Bankas identifikācijas kods”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="d1f0d-159">Bankas identifikācijas kods</span><span class="sxs-lookup"><span data-stu-id="d1f0d-159">Bank identification code</span></span>  
14. <span data-ttu-id="d1f0d-160">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="d1f0d-161">Laukā Nosaukums ierakstiet "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="d1f0d-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="d1f0d-162">RoutingNumber</span></span>  
16. <span data-ttu-id="d1f0d-163">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-163">Click Add.</span></span>
17. <span data-ttu-id="d1f0d-164">Laukā Apraksts ievadiet “Reģistrācijas numurs”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="d1f0d-165">Reģistrācijas numurs</span><span class="sxs-lookup"><span data-stu-id="d1f0d-165">Routing number</span></span>  
18. <span data-ttu-id="d1f0d-166">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="d1f0d-167">Šī modeļa bankas konta struktūras definēšana</span><span class="sxs-lookup"><span data-stu-id="d1f0d-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="d1f0d-168">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="d1f0d-169">Laukā Nosaukums ierakstiet "Konts".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="d1f0d-170">Konts</span><span class="sxs-lookup"><span data-stu-id="d1f0d-170">Account</span></span>  
3. <span data-ttu-id="d1f0d-171">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="d1f0d-172">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-172">Click Add.</span></span>
5. <span data-ttu-id="d1f0d-173">Laukā Apraksts ierakstiet “Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="d1f0d-174">Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).</span><span class="sxs-lookup"><span data-stu-id="d1f0d-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="d1f0d-175">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="d1f0d-176">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="d1f0d-177">Valūta</span><span class="sxs-lookup"><span data-stu-id="d1f0d-177">Currency</span></span>  
8. <span data-ttu-id="d1f0d-178">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="d1f0d-179">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-179">Click Add.</span></span>
10. <span data-ttu-id="d1f0d-180">Laukā Apraksts ievadiet “Valūtas kods”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="d1f0d-181">Valūtas kods</span><span class="sxs-lookup"><span data-stu-id="d1f0d-181">Currency code</span></span>  
11. <span data-ttu-id="d1f0d-182">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="d1f0d-183">Laukā Nosaukums ierakstiet "Number".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="d1f0d-184">Skaits</span><span class="sxs-lookup"><span data-stu-id="d1f0d-184">Number</span></span>  
13. <span data-ttu-id="d1f0d-185">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-185">Click Add.</span></span>
14. <span data-ttu-id="d1f0d-186">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="d1f0d-187">Laukā Nosaukums ierakstiet "IBAN".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="d1f0d-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="d1f0d-188">IBAN</span></span>  
16. <span data-ttu-id="d1f0d-189">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-189">Click Add.</span></span>
17. <span data-ttu-id="d1f0d-190">Laukā Apraksts ievadiet “Starptautiskais bankas konta numurs ”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="d1f0d-191">Starptautiskais bankas konta numurs</span><span class="sxs-lookup"><span data-stu-id="d1f0d-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="d1f0d-192">Definēt maksājuma ziņojuma struktūru kredīta pārsūtīšanas maksājuma veidam</span><span class="sxs-lookup"><span data-stu-id="d1f0d-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="d1f0d-193">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="d1f0d-194">Laukā Jauns zars ievadiet “Modeļa sakne”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="d1f0d-195">Laukā Nosaukums ierakstiet "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="d1f0d-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="d1f0d-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="d1f0d-197">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-197">Click Add.</span></span>
5. <span data-ttu-id="d1f0d-198">Laukā Atrast ierakstiet “CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="d1f0d-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="d1f0d-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="d1f0d-200">Noklikšķiniet uz Atrast iepriekšējo.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-200">Click Find previous.</span></span>
7. <span data-ttu-id="d1f0d-201">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="d1f0d-202">Laukā Nosaukums ievadiet "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="d1f0d-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="d1f0d-203">MessageIdentification</span></span>  
9. <span data-ttu-id="d1f0d-204">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-204">Click Add.</span></span>
10. <span data-ttu-id="d1f0d-205">Laukā Apraksts ievadiet “Atsauce no punkta uz punktu, kuru norādījusi instruējošā puse ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="d1f0d-206">Atsauce no punkta uz punktu, kuru piešķīrusi instruējošā puse, ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).</span><span class="sxs-lookup"><span data-stu-id="d1f0d-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="d1f0d-207">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="d1f0d-208">Laukā Nosaukums ievadiet "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="d1f0d-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="d1f0d-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="d1f0d-210">Laukā Vienuma tips atlasiet "DateTime".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="d1f0d-211">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-211">Click Add.</span></span>
15. <span data-ttu-id="d1f0d-212">Laukā Apraksts ievadiet “Maksājuma ziņojuma izveides datums un laiks.”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="d1f0d-213">Datums un laiks, kad maksājuma ziņojums tika izveidots.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="d1f0d-214">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="d1f0d-215">Definējiet maksāšanas transakcijas struktūras šim modelim.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="d1f0d-216">Laukā Nosaukums ierakstiet "Maksājumi".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="d1f0d-217">Maksājumi</span><span class="sxs-lookup"><span data-stu-id="d1f0d-217">Payments</span></span>  
18. <span data-ttu-id="d1f0d-218">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="d1f0d-219">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-219">Click Add.</span></span>
20. <span data-ttu-id="d1f0d-220">Laukā Apraksts ievadiet "Aktīvā ziņojuma maksājuma rindas".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="d1f0d-221">Pašreizējā ziņojuma maksājuma rindas</span><span class="sxs-lookup"><span data-stu-id="d1f0d-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="d1f0d-222">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="d1f0d-223">Laukā Nosaukums ierakstiet "Kreditors".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="d1f0d-224">Kreditors</span><span class="sxs-lookup"><span data-stu-id="d1f0d-224">Creditor</span></span>  
23. <span data-ttu-id="d1f0d-225">Laukā Vienuma tips atlasiet "Record".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="d1f0d-226">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-226">Click Add.</span></span>
25. <span data-ttu-id="d1f0d-227">Laukā Apraksts ierakstiet “Puse, kurai ir jāsaņem kāda naudas summa.”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="d1f0d-228">Puse, kurai ir jāsaņem kāda naudas summa.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="d1f0d-229">Noklikšķiniet uz Pārslēgt vienuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="d1f0d-230">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="d1f0d-231">Puse</span><span class="sxs-lookup"><span data-stu-id="d1f0d-231">Party</span></span>  
28. <span data-ttu-id="d1f0d-232">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-232">Click Find next.</span></span>
29. <span data-ttu-id="d1f0d-233">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-233">Click OK.</span></span>
30. <span data-ttu-id="d1f0d-234">Laukā Atrast ierakstiet “Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="d1f0d-235">Maksājumi</span><span class="sxs-lookup"><span data-stu-id="d1f0d-235">Payments</span></span>  
31. <span data-ttu-id="d1f0d-236">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-236">Click Find next.</span></span>
32. <span data-ttu-id="d1f0d-237">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="d1f0d-238">Laukā Nosaukums ierakstiet "Debitors".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="d1f0d-239">Debitors</span><span class="sxs-lookup"><span data-stu-id="d1f0d-239">Debtor</span></span>  
34. <span data-ttu-id="d1f0d-240">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-240">Click Add.</span></span>
35. <span data-ttu-id="d1f0d-241">Laukā Apraksts ierakstiet “Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="d1f0d-242">Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="d1f0d-243">Noklikšķiniet uz Pārslēgt vienuma atsauci.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="d1f0d-244">Laukā Atrast ierakstiet “Puse”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="d1f0d-245">Puse</span><span class="sxs-lookup"><span data-stu-id="d1f0d-245">Party</span></span>  
38. <span data-ttu-id="d1f0d-246">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-246">Click Find next.</span></span>
39. <span data-ttu-id="d1f0d-247">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-247">Click OK.</span></span>
40. <span data-ttu-id="d1f0d-248">Noklikšķiniet uz Atrast nākamo.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-248">Click Find next.</span></span>
41. <span data-ttu-id="d1f0d-249">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="d1f0d-250">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="d1f0d-251">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d1f0d-251">Description</span></span>  
43. <span data-ttu-id="d1f0d-252">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="d1f0d-253">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-253">Click Add.</span></span>
45. <span data-ttu-id="d1f0d-254">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="d1f0d-255">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="d1f0d-256">Valūta</span><span class="sxs-lookup"><span data-stu-id="d1f0d-256">Currency</span></span>  
47. <span data-ttu-id="d1f0d-257">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-257">Click Add.</span></span>
48. <span data-ttu-id="d1f0d-258">Laukā Apraksts ievadiet “Valūtas kods”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="d1f0d-259">Valūtas kods</span><span class="sxs-lookup"><span data-stu-id="d1f0d-259">Currency code</span></span>  
49. <span data-ttu-id="d1f0d-260">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="d1f0d-261">Laukā Nosaukums ierakstiet "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="d1f0d-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="d1f0d-262">TransactionDate</span></span>  
51. <span data-ttu-id="d1f0d-263">Laukā Vienuma tips atlasiet "Date".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="d1f0d-264">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-264">Click Add.</span></span>
53. <span data-ttu-id="d1f0d-265">Laukā Apraksts ievadiet “Darījuma datums”.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="d1f0d-266">Darījuma datums</span><span class="sxs-lookup"><span data-stu-id="d1f0d-266">Transaction date</span></span>  
54. <span data-ttu-id="d1f0d-267">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="d1f0d-268">Laukā Nosaukums ierakstiet "'InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="d1f0d-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="d1f0d-269">InstructedAmount</span></span>  
56. <span data-ttu-id="d1f0d-270">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="d1f0d-271">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-271">Click Add.</span></span>
58. <span data-ttu-id="d1f0d-272">Laukā Apraksts ievadiet “Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru, pirms ir ieturētas maksas.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="d1f0d-273">Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="d1f0d-274">Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru pirms maksu ieturēšanas.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="d1f0d-275">Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="d1f0d-276">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="d1f0d-277">Laukā Nosaukums ierakstiet "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="d1f0d-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="d1f0d-278">End2EndID</span></span>  
61. <span data-ttu-id="d1f0d-279">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="d1f0d-280">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-280">Click Add.</span></span>
63. <span data-ttu-id="d1f0d-281">Laukā Apraksts ievadiet “Unikālais identifikators, kuru piešķīrusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="d1f0d-282">Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā."</span><span class="sxs-lookup"><span data-stu-id="d1f0d-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="d1f0d-283">Unikāls identifikators, kuru piešķīrusi iniciējošā puse.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="d1f0d-284">Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="d1f0d-285">Laukā Nosaukums ierakstiet "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="d1f0d-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="d1f0d-286">PaymentModel nosaukums sakrīt ar iepriekš definētiem maksājumu veidlapu interfeisiem.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="d1f0d-287">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-287">Click Save.</span></span>
66. <span data-ttu-id="d1f0d-288">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-288">Close the page.</span></span>


