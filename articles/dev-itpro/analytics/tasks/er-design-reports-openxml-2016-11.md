--- 
title: "Noformēt konfigurāciju pārskatu ģenerēšanai OpenXML formātā elektronisko pārskatu veidošanai (ER)"
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
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: lv-lv
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="2944a-103">Noformēt konfigurāciju pārskatu ģenerēšanai OpenXML formātā elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="2944a-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2944a-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju, kas satur veidni elektronisko dokumentu ģenerēšanai OPENXML formātā.</span><span class="sxs-lookup"><span data-stu-id="2944a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="2944a-105">Šī konfigurācija tiks izmantota kreditoru maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="2944a-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="2944a-106">Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā GBSI uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="2944a-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="2944a-107">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="2944a-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="2944a-108">Ir nepieciešams arī lejupielādēt un saglabāt Microsoft Excel failu [Maksājumu pārskata veidne](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="2944a-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="2944a-109">Augšupielādēt maksājumu datu modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="2944a-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="2944a-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="2944a-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2944a-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="2944a-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2944a-112">Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam "Litware, Inc." Ja jūs neredzat šo konfigurācijas nodrošinātāju, vispirms jāveic darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".</span><span class="sxs-lookup"><span data-stu-id="2944a-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="2944a-113">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="2944a-113">Click Set active.</span></span>
4. <span data-ttu-id="2944a-114">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="2944a-114">Click Repositories.</span></span>
    * <span data-ttu-id="2944a-115">Atlasiet repozitoriju tipam Operācijas resursi, ja tāds ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="2944a-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="2944a-116">Ja tas ir pieejams, izlaidiet nākamās darbības par jauna repozitorija izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="2944a-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="2944a-117">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2944a-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="2944a-118">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="2944a-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="2944a-119">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="2944a-119">Click Create repository.</span></span>
8. <span data-ttu-id="2944a-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2944a-120">Click OK.</span></span>
9. <span data-ttu-id="2944a-121">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="2944a-121">Click Open.</span></span>
10. <span data-ttu-id="2944a-122">Koka struktūrā atlasiet “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="2944a-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="2944a-123">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="2944a-123">Click Import.</span></span>
    * <span data-ttu-id="2944a-124">Importējiet šo datu modeli.</span><span class="sxs-lookup"><span data-stu-id="2944a-124">Import this data model.</span></span> <span data-ttu-id="2944a-125">Tas tiks izmantots kā datu avots jaunā formāta konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="2944a-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="2944a-126">Izlaidiet šo darbību, ja šī konfigurācija jau ir importēta.</span><span class="sxs-lookup"><span data-stu-id="2944a-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="2944a-127">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="2944a-127">Click Yes.</span></span>
13. <span data-ttu-id="2944a-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2944a-128">Close the page.</span></span>
14. <span data-ttu-id="2944a-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2944a-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="2944a-130">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="2944a-130">Create a new format configuration</span></span>
1. <span data-ttu-id="2944a-131">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="2944a-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="2944a-132">Koka struktūrā atlasiet “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="2944a-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="2944a-133">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2944a-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="2944a-134">Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="2944a-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="2944a-135">Izveidojiet formātu, kas ir balstīts uz datu modeli PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="2944a-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="2944a-136">Laukā Nosaukums ierakstiet “Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="2944a-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="2944a-137">Parauga darblapas atskaite</span><span class="sxs-lookup"><span data-stu-id="2944a-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="2944a-138">Laukā Apraksts ierakstiet “Parauga darblapas atskaite kreditoru maksājumiem”.</span><span class="sxs-lookup"><span data-stu-id="2944a-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="2944a-139">Parauga darblapas atskaite kreditoru maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="2944a-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="2944a-140">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="2944a-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2944a-141">Atlasiet definīciju “CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="2944a-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="2944a-142">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="2944a-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="2944a-143">Noformēt jaunu dokumentu OPENXML darblapas formātā</span><span class="sxs-lookup"><span data-stu-id="2944a-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="2944a-144">Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="2944a-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="2944a-145">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="2944a-145">Click Designer.</span></span>
3. <span data-ttu-id="2944a-146">Darbību rūtī noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="2944a-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="2944a-147">Noklikšķiniet uz Importēt no Excel.</span><span class="sxs-lookup"><span data-stu-id="2944a-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="2944a-148">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="2944a-148">Click Attachments.</span></span>
    * <span data-ttu-id="2944a-149">Pievienojiet esošo Excel dokumentu kā veidni.</span><span class="sxs-lookup"><span data-stu-id="2944a-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="2944a-150">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2944a-150">Click New.</span></span>
7. <span data-ttu-id="2944a-151">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="2944a-151">Click File.</span></span>
    * <span data-ttu-id="2944a-152">Norādiet uz esošo Excel failu.</span><span class="sxs-lookup"><span data-stu-id="2944a-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="2944a-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2944a-153">Close the page.</span></span>
9. <span data-ttu-id="2944a-154">Ievadiet vai atlasiet kādu vērtību laukā Veidne.</span><span class="sxs-lookup"><span data-stu-id="2944a-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="2944a-155">Atlasiet pievienoto Excel failu, ko izmantot kā veidni.</span><span class="sxs-lookup"><span data-stu-id="2944a-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="2944a-156">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2944a-156">Click OK.</span></span>
    * <span data-ttu-id="2944a-157">Ņemiet vērā, ka ER formātā komponenti tika izveidoti, izstrādājot formātu un pamatojoties uz atsauces MS Excel dokumenta (nosauktie diapazoni) struktūru.</span><span class="sxs-lookup"><span data-stu-id="2944a-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="2944a-158">Izveidot jaunu datu avotu, lai aprēķinātu kopsummas pēc valūtu kodiem</span><span class="sxs-lookup"><span data-stu-id="2944a-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="2944a-159">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="2944a-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="2944a-160">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="2944a-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="2944a-161">Koka struktūrā atlasiet “Funkcijas\Grupēt pēc”.</span><span class="sxs-lookup"><span data-stu-id="2944a-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="2944a-162">Laukā Nosaukums ierakstiet “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="2944a-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="2944a-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="2944a-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="2944a-164">Noklikšķiniet uz Rediģēt grupu pēc.</span><span class="sxs-lookup"><span data-stu-id="2944a-164">Click Edit group by.</span></span>
6. <span data-ttu-id="2944a-165">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="2944a-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="2944a-166">Kokā atlasiet “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="2944a-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="2944a-167">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="2944a-167">Click Add field to.</span></span>
9. <span data-ttu-id="2944a-168">Noklikšķiniet uz Ko grupēt.</span><span class="sxs-lookup"><span data-stu-id="2944a-168">Click What to group.</span></span>
10. <span data-ttu-id="2944a-169">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="2944a-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="2944a-170">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="2944a-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="2944a-171">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="2944a-171">Click Add field to.</span></span>
13. <span data-ttu-id="2944a-172">Noklikšķiniet uz Grupētie lauki.</span><span class="sxs-lookup"><span data-stu-id="2944a-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="2944a-173">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Instruētā summa(InstructedAmount)”.</span><span class="sxs-lookup"><span data-stu-id="2944a-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="2944a-174">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="2944a-174">Click Add field to.</span></span>
16. <span data-ttu-id="2944a-175">Noklikšķiniet uz Apkopojuma lauki.</span><span class="sxs-lookup"><span data-stu-id="2944a-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="2944a-176">Atlasiet opciju laukā Metode.</span><span class="sxs-lookup"><span data-stu-id="2944a-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="2944a-177">Atlasiet SUM apkopošanas funkciju.</span><span class="sxs-lookup"><span data-stu-id="2944a-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="2944a-178">Laukā Nosaukums ierakstiet “TotalInstructuredAmount”.</span><span class="sxs-lookup"><span data-stu-id="2944a-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="2944a-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="2944a-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="2944a-180">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2944a-180">Click Save.</span></span>
20. <span data-ttu-id="2944a-181">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2944a-181">Close the page.</span></span>
21. <span data-ttu-id="2944a-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2944a-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="2944a-183">Kartēt formāta komponentus uz datu avotiem</span><span class="sxs-lookup"><span data-stu-id="2944a-183">Map format components to data sources</span></span>
1. <span data-ttu-id="2944a-184">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="2944a-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="2944a-185">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="2944a-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="2944a-186">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Iniciējošā puse(InitiatingParty)”.</span><span class="sxs-lookup"><span data-stu-id="2944a-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="2944a-187">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Iniciējošā puse(InitiatingParty)\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="2944a-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="2944a-188">Koka struktūrā izvērsiet zaru “Excel\ReportHeader”.</span><span class="sxs-lookup"><span data-stu-id="2944a-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="2944a-189">Koka struktūrā atlasiet zaru “Excel\ReportHeader\CompanyName”.</span><span class="sxs-lookup"><span data-stu-id="2944a-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="2944a-190">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-190">Click Bind.</span></span>
8. <span data-ttu-id="2944a-191">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="2944a-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="2944a-192">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditors\Identifikācija“.</span><span class="sxs-lookup"><span data-stu-id="2944a-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="2944a-193">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditors\Identifikācija\Avota ID(SourceID)“.</span><span class="sxs-lookup"><span data-stu-id="2944a-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="2944a-194">Koka struktūrā izvērsiet zaru “Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="2944a-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="2944a-195">Koka struktūrā atlasiet zaru “Excel\PaymLines\VendAccountName”.</span><span class="sxs-lookup"><span data-stu-id="2944a-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="2944a-196">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-196">Click Bind.</span></span>
14. <span data-ttu-id="2944a-197">Kokā atlasiet “modelis\Maksājumi\Kreditors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="2944a-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="2944a-198">Koka struktūrā atlasiet zaru “Excel\PaymLines\VendName”.</span><span class="sxs-lookup"><span data-stu-id="2944a-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="2944a-199">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-199">Click Bind.</span></span>
17. <span data-ttu-id="2944a-200">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="2944a-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="2944a-201">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Nosaukums“.</span><span class="sxs-lookup"><span data-stu-id="2944a-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="2944a-202">Koka struktūrā atlasiet zaru “Excel\PaymLines\Banka”.</span><span class="sxs-lookup"><span data-stu-id="2944a-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="2944a-203">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-203">Click Bind.</span></span>
21. <span data-ttu-id="2944a-204">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Maršrutēšanas numurs(RoutingNumber)”.</span><span class="sxs-lookup"><span data-stu-id="2944a-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="2944a-205">Koka struktūrā atlasiet zaru “Excel\PaymLines\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="2944a-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="2944a-206">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-206">Click Bind.</span></span>
24. <span data-ttu-id="2944a-207">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)“.</span><span class="sxs-lookup"><span data-stu-id="2944a-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="2944a-208">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija“.</span><span class="sxs-lookup"><span data-stu-id="2944a-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="2944a-209">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija\Numurs“.</span><span class="sxs-lookup"><span data-stu-id="2944a-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="2944a-210">Koka struktūrā atlasiet zaru “Excel\PaymLines\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="2944a-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="2944a-211">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-211">Click Bind.</span></span>
29. <span data-ttu-id="2944a-212">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Instruētā summa(InstructedAmount)”.</span><span class="sxs-lookup"><span data-stu-id="2944a-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="2944a-213">Koka struktūrā atlasiet zaru “Excel\PaymLines\Debit”.</span><span class="sxs-lookup"><span data-stu-id="2944a-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="2944a-214">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-214">Click Bind.</span></span>
32. <span data-ttu-id="2944a-215">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="2944a-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="2944a-216">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)“.</span><span class="sxs-lookup"><span data-stu-id="2944a-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="2944a-217">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="2944a-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="2944a-218">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="2944a-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="2944a-219">Koka struktūrā atlasiet zaru “Excel\PaymLines\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="2944a-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="2944a-220">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-220">Click Bind.</span></span>
38. <span data-ttu-id="2944a-221">Koka struktūrā izvērsiet elementu “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="2944a-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="2944a-222">Koka struktūrā izvērsiet elementu “PaymentByCurrency\grupēts”.</span><span class="sxs-lookup"><span data-stu-id="2944a-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="2944a-223">Koka struktūrā atlasiet elementu “PaymentByCurrency\grupēts\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="2944a-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="2944a-224">Koka struktūrā izvērsiet zaru “Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="2944a-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="2944a-225">Koka struktūrā atlasiet zaru “Excel\SummaryLines\SummaryCurrency”.</span><span class="sxs-lookup"><span data-stu-id="2944a-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="2944a-226">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-226">Click Bind.</span></span>
44. <span data-ttu-id="2944a-227">Koka struktūrā izvērsiet elementu “PaymentByCurrency\apkopots”.</span><span class="sxs-lookup"><span data-stu-id="2944a-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="2944a-228">Koka struktūrā atlasiet elementu “PaymentByCurrency\apkopots\TotalInstructuredAmount”.</span><span class="sxs-lookup"><span data-stu-id="2944a-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="2944a-229">Koka struktūrā atlasiet zaru “Excel\SummaryLines\SummaryAmount”.</span><span class="sxs-lookup"><span data-stu-id="2944a-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="2944a-230">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-230">Click Bind.</span></span>
48. <span data-ttu-id="2944a-231">Koka struktūrā atlasiet elementu “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="2944a-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="2944a-232">Koka struktūrā atlasiet zaru “Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="2944a-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="2944a-233">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-233">Click Bind.</span></span>
51. <span data-ttu-id="2944a-234">Kokā atlasiet “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="2944a-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="2944a-235">Koka struktūrā atlasiet zaru “Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="2944a-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="2944a-236">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2944a-236">Click Bind.</span></span>
54. <span data-ttu-id="2944a-237">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2944a-237">Click Save.</span></span>
55. <span data-ttu-id="2944a-238">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2944a-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="2944a-239">Izmantojiet izveidoto konfigurāciju maksājumu apstrādei</span><span class="sxs-lookup"><span data-stu-id="2944a-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="2944a-240">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="2944a-240">Click Change status.</span></span>
2. <span data-ttu-id="2944a-241">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="2944a-241">Click Complete.</span></span>
3. <span data-ttu-id="2944a-242">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2944a-242">Click OK.</span></span>
4. <span data-ttu-id="2944a-243">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2944a-243">Close the page.</span></span>
5. <span data-ttu-id="2944a-244">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2944a-244">Close the page.</span></span>
6. <span data-ttu-id="2944a-245">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="2944a-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="2944a-246">Izmantojiet līdzekli Ātrais filtrs, lai filtrētu pēc lauka Maksāšanas metode ar vērtību “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="2944a-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="2944a-247">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="2944a-247">Electronic</span></span>  
8. <span data-ttu-id="2944a-248">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="2944a-248">Click Edit.</span></span>
9. <span data-ttu-id="2944a-249">Izvērsiet sadaļu Failu formāti.</span><span class="sxs-lookup"><span data-stu-id="2944a-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="2944a-250">Laukā Vispārīga elektronisko pārskatu veidošana atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="2944a-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="2944a-251">Ievadiet vai atlasiet vērtību laukā Eksporta formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="2944a-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="2944a-252">Atlasiet konfigurāciju “Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="2944a-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="2944a-253">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2944a-253">Click Save.</span></span>
13. <span data-ttu-id="2944a-254">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2944a-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="2944a-255">Izmantot izveidoto konfigurāciju maksājumu žurnālu apstrādes testēšanai</span><span class="sxs-lookup"><span data-stu-id="2944a-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="2944a-256">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="2944a-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2944a-257">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2944a-257">Click New.</span></span>
    * <span data-ttu-id="2944a-258">Izveidojiet jaunu maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="2944a-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="2944a-259">Laukā Nosaukums ierakstiet VendPay.</span><span class="sxs-lookup"><span data-stu-id="2944a-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="2944a-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="2944a-260">VendPay</span></span>  
4. <span data-ttu-id="2944a-261">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="2944a-261">Click Lines.</span></span>
5. <span data-ttu-id="2944a-262">Laukā Konts norādiet vērtības “GB_SI_000001”.</span><span class="sxs-lookup"><span data-stu-id="2944a-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="2944a-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="2944a-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="2944a-264">Vienumam Debets norādiet vērtību “1000”.</span><span class="sxs-lookup"><span data-stu-id="2944a-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="2944a-265">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2944a-265">Click New.</span></span>
8. <span data-ttu-id="2944a-266">Laukā Konts norādiet vērtības “GB_SI_000005”.</span><span class="sxs-lookup"><span data-stu-id="2944a-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="2944a-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="2944a-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="2944a-268">Vienumam Debets norādiet vērtību “2000”.</span><span class="sxs-lookup"><span data-stu-id="2944a-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="2944a-269">Laukā Valūta ierakstiet vērtību “EUR”.</span><span class="sxs-lookup"><span data-stu-id="2944a-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="2944a-270">EUR</span><span class="sxs-lookup"><span data-stu-id="2944a-270">EUR</span></span>  
11. <span data-ttu-id="2944a-271">Laukā Korespondējošais konts norādiet vērtības “GBSI OPER”.</span><span class="sxs-lookup"><span data-stu-id="2944a-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="2944a-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="2944a-272">GBSI OPER</span></span>  
12. <span data-ttu-id="2944a-273">Laukā Maksāšanas metode ierakstiet “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="2944a-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="2944a-274">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="2944a-274">Electronic</span></span>  
13. <span data-ttu-id="2944a-275">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2944a-275">Click Save.</span></span>
14. <span data-ttu-id="2944a-276">Noklikšķiniet uz Ģenerēt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="2944a-276">Click Generate payments.</span></span>
15. <span data-ttu-id="2944a-277">Laukā Maksāšanas metode ierakstiet “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="2944a-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="2944a-278">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="2944a-278">Electronic</span></span>  
16. <span data-ttu-id="2944a-279">Laukā Faila nosaukums ierakstiet “Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="2944a-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="2944a-280">Piemēram, tips Maksājumi.</span><span class="sxs-lookup"><span data-stu-id="2944a-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="2944a-281">Laukā Bankas konts atlasiet “GBSI OPER”.</span><span class="sxs-lookup"><span data-stu-id="2944a-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="2944a-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="2944a-282">GBSI OPER</span></span>  
18. <span data-ttu-id="2944a-283">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2944a-283">Click OK.</span></span>
19. <span data-ttu-id="2944a-284">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2944a-284">Click OK.</span></span>
    * <span data-ttu-id="2944a-285">Pārskatiet izveidoto darblapu, tostarp informāciju par maksājuma rindām, kā arī kopsummas katram valūtas kodam, kas ir izmantots šajā maksājuma ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="2944a-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


