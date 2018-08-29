--- 
title: "ER konfigurāciju noformēšana pārskatu ģenerēšanai OpenXML formātā"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju, kas satur veidni elektronisko dokumentu ģenerēšanai OPENXML formātā."
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="60e8f-103">ER konfigurāciju noformēšana pārskatu ģenerēšanai OpenXML formātā</span><span class="sxs-lookup"><span data-stu-id="60e8f-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60e8f-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju, kas satur veidni elektronisko dokumentu ģenerēšanai OPENXML formātā.</span><span class="sxs-lookup"><span data-stu-id="60e8f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="60e8f-105">Šī konfigurācija tiks izmantota kreditoru maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="60e8f-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="60e8f-106">Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā GBSI uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="60e8f-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="60e8f-107">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="60e8f-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="60e8f-108">Ir nepieciešams arī lejupielādēt un saglabāt Microsoft Excel failu [Maksājumu pārskata veidne](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="60e8f-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="60e8f-109">Augšupielādēt maksājumu datu modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="60e8f-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="60e8f-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="60e8f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="60e8f-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="60e8f-112">Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam "Litware, Inc." Ja jūs neredzat šo konfigurācijas nodrošinātāju, vispirms jāveic darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".</span><span class="sxs-lookup"><span data-stu-id="60e8f-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="60e8f-113">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-113">Click Set active.</span></span>
4. <span data-ttu-id="60e8f-114">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="60e8f-114">Click Repositories.</span></span>
    * <span data-ttu-id="60e8f-115">Atlasiet repozitoriju tipam Operācijas resursi, ja tāds ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="60e8f-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="60e8f-116">Ja tas ir pieejams, izlaidiet nākamās darbības par jauna repozitorija izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="60e8f-117">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="60e8f-118">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="60e8f-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="60e8f-119">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="60e8f-119">Click Create repository.</span></span>
8. <span data-ttu-id="60e8f-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60e8f-120">Click OK.</span></span>
9. <span data-ttu-id="60e8f-121">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-121">Click Open.</span></span>
10. <span data-ttu-id="60e8f-122">Koka struktūrā atlasiet “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="60e8f-123">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-123">Click Import.</span></span>
    * <span data-ttu-id="60e8f-124">Importējiet šo datu modeli.</span><span class="sxs-lookup"><span data-stu-id="60e8f-124">Import this data model.</span></span> <span data-ttu-id="60e8f-125">Tas tiks izmantots kā datu avots jaunā formāta konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="60e8f-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="60e8f-126">Izlaidiet šo darbību, ja šī konfigurācija jau ir importēta.</span><span class="sxs-lookup"><span data-stu-id="60e8f-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="60e8f-127">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="60e8f-127">Click Yes.</span></span>
13. <span data-ttu-id="60e8f-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-128">Close the page.</span></span>
14. <span data-ttu-id="60e8f-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="60e8f-130">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="60e8f-130">Create a new format configuration</span></span>
1. <span data-ttu-id="60e8f-131">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="60e8f-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="60e8f-132">Koka struktūrā atlasiet “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="60e8f-133">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="60e8f-134">Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="60e8f-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="60e8f-135">Izveidojiet formātu, kas ir balstīts uz datu modeli PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="60e8f-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="60e8f-136">Laukā Nosaukums ierakstiet “Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="60e8f-137">Parauga darblapas atskaite</span><span class="sxs-lookup"><span data-stu-id="60e8f-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="60e8f-138">Laukā Apraksts ierakstiet “Parauga darblapas atskaite kreditoru maksājumiem”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="60e8f-139">Parauga darblapas atskaite kreditoru maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="60e8f-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="60e8f-140">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="60e8f-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="60e8f-141">Atlasiet definīciju “CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="60e8f-142">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="60e8f-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="60e8f-143">Noformēt jaunu dokumentu OPENXML darblapas formātā</span><span class="sxs-lookup"><span data-stu-id="60e8f-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="60e8f-144">Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="60e8f-145">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="60e8f-145">Click Designer.</span></span>
3. <span data-ttu-id="60e8f-146">Darbību rūtī noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="60e8f-147">Noklikšķiniet uz Importēt no Excel.</span><span class="sxs-lookup"><span data-stu-id="60e8f-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="60e8f-148">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="60e8f-148">Click Attachments.</span></span>
    * <span data-ttu-id="60e8f-149">Pievienojiet esošo Excel dokumentu kā veidni.</span><span class="sxs-lookup"><span data-stu-id="60e8f-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="60e8f-150">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="60e8f-150">Click New.</span></span>
7. <span data-ttu-id="60e8f-151">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="60e8f-151">Click File.</span></span>
    * <span data-ttu-id="60e8f-152">Norādiet uz esošo Excel failu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="60e8f-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-153">Close the page.</span></span>
9. <span data-ttu-id="60e8f-154">Ievadiet vai atlasiet kādu vērtību laukā Veidne.</span><span class="sxs-lookup"><span data-stu-id="60e8f-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="60e8f-155">Atlasiet pievienoto Excel failu, ko izmantot kā veidni.</span><span class="sxs-lookup"><span data-stu-id="60e8f-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="60e8f-156">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60e8f-156">Click OK.</span></span>
    * <span data-ttu-id="60e8f-157">Ņemiet vērā, ka ER formātā komponenti tika izveidoti, izstrādājot formātu un pamatojoties uz atsauces MS Excel dokumenta (nosauktie diapazoni) struktūru.</span><span class="sxs-lookup"><span data-stu-id="60e8f-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="60e8f-158">Izveidot jaunu datu avotu, lai aprēķinātu kopsummas pēc valūtu kodiem</span><span class="sxs-lookup"><span data-stu-id="60e8f-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="60e8f-159">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="60e8f-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="60e8f-160">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="60e8f-161">Koka struktūrā atlasiet “Funkcijas\Grupēt pēc”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="60e8f-162">Laukā Nosaukums ierakstiet “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="60e8f-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="60e8f-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="60e8f-164">Noklikšķiniet uz Rediģēt grupu pēc.</span><span class="sxs-lookup"><span data-stu-id="60e8f-164">Click Edit group by.</span></span>
6. <span data-ttu-id="60e8f-165">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="60e8f-166">Kokā atlasiet “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="60e8f-167">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="60e8f-167">Click Add field to.</span></span>
9. <span data-ttu-id="60e8f-168">Noklikšķiniet uz Ko grupēt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-168">Click What to group.</span></span>
10. <span data-ttu-id="60e8f-169">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="60e8f-170">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="60e8f-171">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="60e8f-171">Click Add field to.</span></span>
13. <span data-ttu-id="60e8f-172">Noklikšķiniet uz Grupētie lauki.</span><span class="sxs-lookup"><span data-stu-id="60e8f-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="60e8f-173">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Instruētā summa(InstructedAmount)”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="60e8f-174">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="60e8f-174">Click Add field to.</span></span>
16. <span data-ttu-id="60e8f-175">Noklikšķiniet uz Apkopojuma lauki.</span><span class="sxs-lookup"><span data-stu-id="60e8f-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="60e8f-176">Atlasiet opciju laukā Metode.</span><span class="sxs-lookup"><span data-stu-id="60e8f-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="60e8f-177">Atlasiet SUM apkopošanas funkciju.</span><span class="sxs-lookup"><span data-stu-id="60e8f-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="60e8f-178">Laukā Nosaukums ierakstiet “TotalInstructuredAmount”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="60e8f-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="60e8f-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="60e8f-180">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-180">Click Save.</span></span>
20. <span data-ttu-id="60e8f-181">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-181">Close the page.</span></span>
21. <span data-ttu-id="60e8f-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60e8f-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="60e8f-183">Kartēt formāta komponentus uz datu avotiem</span><span class="sxs-lookup"><span data-stu-id="60e8f-183">Map format components to data sources</span></span>
1. <span data-ttu-id="60e8f-184">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="60e8f-185">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="60e8f-186">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Iniciējošā puse(InitiatingParty)”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="60e8f-187">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Iniciējošā puse(InitiatingParty)\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="60e8f-188">Koka struktūrā izvērsiet zaru “Excel\ReportHeader”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="60e8f-189">Koka struktūrā atlasiet zaru “Excel\ReportHeader\CompanyName”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="60e8f-190">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-190">Click Bind.</span></span>
8. <span data-ttu-id="60e8f-191">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="60e8f-192">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditors\Identifikācija“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="60e8f-193">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditors\Identifikācija\Avota ID(SourceID)“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="60e8f-194">Koka struktūrā izvērsiet zaru “Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="60e8f-195">Koka struktūrā atlasiet zaru “Excel\PaymLines\VendAccountName”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="60e8f-196">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-196">Click Bind.</span></span>
14. <span data-ttu-id="60e8f-197">Kokā atlasiet “modelis\Maksājumi\Kreditors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="60e8f-198">Koka struktūrā atlasiet zaru “Excel\PaymLines\VendName”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="60e8f-199">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-199">Click Bind.</span></span>
17. <span data-ttu-id="60e8f-200">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="60e8f-201">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Nosaukums“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="60e8f-202">Koka struktūrā atlasiet zaru “Excel\PaymLines\Banka”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="60e8f-203">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-203">Click Bind.</span></span>
21. <span data-ttu-id="60e8f-204">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Maršrutēšanas numurs(RoutingNumber)”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="60e8f-205">Koka struktūrā atlasiet zaru “Excel\PaymLines\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="60e8f-206">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-206">Click Bind.</span></span>
24. <span data-ttu-id="60e8f-207">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="60e8f-208">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="60e8f-209">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija\Numurs“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="60e8f-210">Koka struktūrā atlasiet zaru “Excel\PaymLines\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="60e8f-211">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-211">Click Bind.</span></span>
29. <span data-ttu-id="60e8f-212">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Instruētā summa(InstructedAmount)”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="60e8f-213">Koka struktūrā atlasiet zaru “Excel\PaymLines\Debit”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="60e8f-214">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-214">Click Bind.</span></span>
32. <span data-ttu-id="60e8f-215">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="60e8f-216">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="60e8f-217">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="60e8f-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="60e8f-218">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="60e8f-219">Koka struktūrā atlasiet zaru “Excel\PaymLines\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="60e8f-220">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-220">Click Bind.</span></span>
38. <span data-ttu-id="60e8f-221">Koka struktūrā izvērsiet elementu “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="60e8f-222">Koka struktūrā izvērsiet elementu “PaymentByCurrency\grupēts”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="60e8f-223">Koka struktūrā atlasiet elementu “PaymentByCurrency\grupēts\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="60e8f-224">Koka struktūrā izvērsiet zaru “Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="60e8f-225">Koka struktūrā atlasiet zaru “Excel\SummaryLines\SummaryCurrency”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="60e8f-226">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-226">Click Bind.</span></span>
44. <span data-ttu-id="60e8f-227">Koka struktūrā izvērsiet elementu “PaymentByCurrency\apkopots”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="60e8f-228">Koka struktūrā atlasiet elementu “PaymentByCurrency\apkopots\TotalInstructuredAmount”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="60e8f-229">Koka struktūrā atlasiet zaru “Excel\SummaryLines\SummaryAmount”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="60e8f-230">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-230">Click Bind.</span></span>
48. <span data-ttu-id="60e8f-231">Koka struktūrā atlasiet elementu “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="60e8f-232">Koka struktūrā atlasiet zaru “Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="60e8f-233">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-233">Click Bind.</span></span>
51. <span data-ttu-id="60e8f-234">Kokā atlasiet “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="60e8f-235">Koka struktūrā atlasiet zaru “Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="60e8f-236">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-236">Click Bind.</span></span>
54. <span data-ttu-id="60e8f-237">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-237">Click Save.</span></span>
55. <span data-ttu-id="60e8f-238">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="60e8f-239">Izmantojiet izveidoto konfigurāciju maksājumu apstrādei</span><span class="sxs-lookup"><span data-stu-id="60e8f-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="60e8f-240">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-240">Click Change status.</span></span>
2. <span data-ttu-id="60e8f-241">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-241">Click Complete.</span></span>
3. <span data-ttu-id="60e8f-242">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60e8f-242">Click OK.</span></span>
4. <span data-ttu-id="60e8f-243">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-243">Close the page.</span></span>
5. <span data-ttu-id="60e8f-244">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-244">Close the page.</span></span>
6. <span data-ttu-id="60e8f-245">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="60e8f-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="60e8f-246">Izmantojiet līdzekli Ātrais filtrs, lai filtrētu pēc lauka Maksāšanas metode ar vērtību “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="60e8f-247">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="60e8f-247">Electronic</span></span>  
8. <span data-ttu-id="60e8f-248">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-248">Click Edit.</span></span>
9. <span data-ttu-id="60e8f-249">Izvērsiet sadaļu Failu formāti.</span><span class="sxs-lookup"><span data-stu-id="60e8f-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="60e8f-250">Laukā Vispārīga elektronisko pārskatu veidošana atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="60e8f-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="60e8f-251">Ievadiet vai atlasiet vērtību laukā Eksporta formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="60e8f-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="60e8f-252">Atlasiet konfigurāciju “Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="60e8f-253">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-253">Click Save.</span></span>
13. <span data-ttu-id="60e8f-254">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="60e8f-255">Izmantot izveidoto konfigurāciju maksājumu žurnālu apstrādes testēšanai</span><span class="sxs-lookup"><span data-stu-id="60e8f-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="60e8f-256">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="60e8f-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="60e8f-257">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="60e8f-257">Click New.</span></span>
    * <span data-ttu-id="60e8f-258">Izveidojiet jaunu maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="60e8f-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="60e8f-259">Laukā Nosaukums ierakstiet VendPay.</span><span class="sxs-lookup"><span data-stu-id="60e8f-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="60e8f-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="60e8f-260">VendPay</span></span>  
4. <span data-ttu-id="60e8f-261">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="60e8f-261">Click Lines.</span></span>
5. <span data-ttu-id="60e8f-262">Laukā Konts norādiet vērtības “GB_SI_000001”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="60e8f-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="60e8f-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="60e8f-264">Vienumam Debets norādiet vērtību “1000”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="60e8f-265">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="60e8f-265">Click New.</span></span>
8. <span data-ttu-id="60e8f-266">Laukā Konts norādiet vērtības “GB_SI_000005”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="60e8f-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="60e8f-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="60e8f-268">Vienumam Debets norādiet vērtību “2000”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="60e8f-269">Laukā Valūta ierakstiet vērtību “EUR”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="60e8f-270">EUR</span><span class="sxs-lookup"><span data-stu-id="60e8f-270">EUR</span></span>  
11. <span data-ttu-id="60e8f-271">Laukā Korespondējošais konts norādiet vērtības “GBSI OPER”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="60e8f-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="60e8f-272">GBSI OPER</span></span>  
12. <span data-ttu-id="60e8f-273">Laukā Maksāšanas metode ierakstiet “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="60e8f-274">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="60e8f-274">Electronic</span></span>  
13. <span data-ttu-id="60e8f-275">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="60e8f-275">Click Save.</span></span>
14. <span data-ttu-id="60e8f-276">Noklikšķiniet uz Ģenerēt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="60e8f-276">Click Generate payments.</span></span>
15. <span data-ttu-id="60e8f-277">Laukā Maksāšanas metode ierakstiet “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="60e8f-278">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="60e8f-278">Electronic</span></span>  
16. <span data-ttu-id="60e8f-279">Laukā Faila nosaukums ierakstiet “Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="60e8f-280">Piemēram, tips Maksājumi.</span><span class="sxs-lookup"><span data-stu-id="60e8f-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="60e8f-281">Laukā Bankas konts atlasiet “GBSI OPER”.</span><span class="sxs-lookup"><span data-stu-id="60e8f-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="60e8f-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="60e8f-282">GBSI OPER</span></span>  
18. <span data-ttu-id="60e8f-283">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60e8f-283">Click OK.</span></span>
19. <span data-ttu-id="60e8f-284">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60e8f-284">Click OK.</span></span>
    * <span data-ttu-id="60e8f-285">Pārskatiet izveidoto darblapu, tostarp informāciju par maksājuma rindām, kā arī kopsummas katram valūtas kodam, kas ir izmantots šajā maksājuma ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="60e8f-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


