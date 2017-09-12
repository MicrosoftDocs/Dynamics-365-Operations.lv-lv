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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 51208cbc5118e95fd402cca3cbc228ef1b87a47f
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="655bd-103">Noformēt konfigurāciju pārskatu ģenerēšanai OpenXML formātā elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="655bd-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="655bd-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju, kas satur veidni elektronisko dokumentu ģenerēšanai OPENXML formātā.</span><span class="sxs-lookup"><span data-stu-id="655bd-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="655bd-105">Šī konfigurācija tiks izmantota kreditoru maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="655bd-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="655bd-106">Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā GBSI uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="655bd-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="655bd-107">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="655bd-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="655bd-108">Jums ir nepieciešams arī Excel fails, kas tiks importēts, veidojot veidni.</span><span class="sxs-lookup"><span data-stu-id="655bd-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="655bd-109">Šim failam var piekļūt no vietnes: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="655bd-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="655bd-110">Augšupielādēt maksājumu datu modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="655bd-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="655bd-111">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="655bd-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="655bd-112">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="655bd-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="655bd-113">Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam "Litware, Inc." Ja jūs neredzat šo konfigurācijas nodrošinātāju, vispirms jāveic darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".</span><span class="sxs-lookup"><span data-stu-id="655bd-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="655bd-114">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="655bd-114">Click Set active.</span></span>
4. <span data-ttu-id="655bd-115">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="655bd-115">Click Repositories.</span></span>
    * <span data-ttu-id="655bd-116">Atlasiet repozitoriju tipam Operācijas resursi, ja tāds ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="655bd-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="655bd-117">Ja tas ir pieejams, izlaidiet nākamās darbības par jauna repozitorija izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="655bd-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="655bd-118">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="655bd-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="655bd-119">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="655bd-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="655bd-120">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="655bd-120">Click Create repository.</span></span>
8. <span data-ttu-id="655bd-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="655bd-121">Click OK.</span></span>
9. <span data-ttu-id="655bd-122">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="655bd-122">Click Open.</span></span>
10. <span data-ttu-id="655bd-123">Koka struktūrā atlasiet “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="655bd-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="655bd-124">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="655bd-124">Click Import.</span></span>
    * <span data-ttu-id="655bd-125">Importējiet šo datu modeli.</span><span class="sxs-lookup"><span data-stu-id="655bd-125">Import this data model.</span></span> <span data-ttu-id="655bd-126">Tas tiks izmantots kā datu avots jaunā formāta konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="655bd-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="655bd-127">Izlaidiet šo darbību, ja šī konfigurācija jau ir importēta.</span><span class="sxs-lookup"><span data-stu-id="655bd-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="655bd-128">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="655bd-128">Click Yes.</span></span>
13. <span data-ttu-id="655bd-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="655bd-129">Close the page.</span></span>
14. <span data-ttu-id="655bd-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="655bd-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="655bd-131">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="655bd-131">Create a new format configuration</span></span>
1. <span data-ttu-id="655bd-132">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="655bd-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="655bd-133">Koka struktūrā atlasiet “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="655bd-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="655bd-134">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="655bd-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="655bd-135">Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="655bd-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="655bd-136">Izveidojiet formātu, kas ir balstīts uz datu modeli PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="655bd-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="655bd-137">Laukā Nosaukums ierakstiet “Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="655bd-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="655bd-138">Parauga darblapas atskaite</span><span class="sxs-lookup"><span data-stu-id="655bd-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="655bd-139">Laukā Apraksts ierakstiet “Parauga darblapas atskaite kreditoru maksājumiem”.</span><span class="sxs-lookup"><span data-stu-id="655bd-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="655bd-140">Parauga darblapas atskaite kreditoru maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="655bd-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="655bd-141">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="655bd-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="655bd-142">Atlasiet definīciju “CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="655bd-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="655bd-143">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="655bd-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="655bd-144">Noformēt jaunu dokumentu OPENXML darblapas formātā</span><span class="sxs-lookup"><span data-stu-id="655bd-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="655bd-145">Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="655bd-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="655bd-146">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="655bd-146">Click Designer.</span></span>
3. <span data-ttu-id="655bd-147">Darbību rūtī noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="655bd-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="655bd-148">Noklikšķiniet uz Importēt no Excel.</span><span class="sxs-lookup"><span data-stu-id="655bd-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="655bd-149">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="655bd-149">Click Attachments.</span></span>
    * <span data-ttu-id="655bd-150">Pievienojiet esošo Excel dokumentu kā veidni.</span><span class="sxs-lookup"><span data-stu-id="655bd-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="655bd-151">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="655bd-151">Click New.</span></span>
7. <span data-ttu-id="655bd-152">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="655bd-152">Click File.</span></span>
    * <span data-ttu-id="655bd-153">Norādiet uz esošo Excel failu.</span><span class="sxs-lookup"><span data-stu-id="655bd-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="655bd-154">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="655bd-154">Close the page.</span></span>
9. <span data-ttu-id="655bd-155">Ievadiet vai atlasiet kādu vērtību laukā Veidne.</span><span class="sxs-lookup"><span data-stu-id="655bd-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="655bd-156">Atlasiet pievienoto Excel failu, ko izmantot kā veidni.</span><span class="sxs-lookup"><span data-stu-id="655bd-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="655bd-157">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="655bd-157">Click OK.</span></span>
    * <span data-ttu-id="655bd-158">Ņemiet vērā, ka ER formātā komponenti tika izveidoti, izstrādājot formātu un pamatojoties uz atsauces MS Excel dokumenta (nosauktie diapazoni) struktūru.</span><span class="sxs-lookup"><span data-stu-id="655bd-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="655bd-159">Izveidot jaunu datu avotu, lai aprēķinātu kopsummas pēc valūtu kodiem</span><span class="sxs-lookup"><span data-stu-id="655bd-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="655bd-160">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="655bd-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="655bd-161">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="655bd-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="655bd-162">Koka struktūrā atlasiet “Funkcijas\Grupēt pēc”.</span><span class="sxs-lookup"><span data-stu-id="655bd-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="655bd-163">Laukā Nosaukums ierakstiet “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="655bd-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="655bd-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="655bd-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="655bd-165">Noklikšķiniet uz Rediģēt grupu pēc.</span><span class="sxs-lookup"><span data-stu-id="655bd-165">Click Edit group by.</span></span>
6. <span data-ttu-id="655bd-166">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="655bd-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="655bd-167">Kokā atlasiet “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="655bd-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="655bd-168">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="655bd-168">Click Add field to.</span></span>
9. <span data-ttu-id="655bd-169">Noklikšķiniet uz Ko grupēt.</span><span class="sxs-lookup"><span data-stu-id="655bd-169">Click What to group.</span></span>
10. <span data-ttu-id="655bd-170">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="655bd-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="655bd-171">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="655bd-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="655bd-172">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="655bd-172">Click Add field to.</span></span>
13. <span data-ttu-id="655bd-173">Noklikšķiniet uz Grupētie lauki.</span><span class="sxs-lookup"><span data-stu-id="655bd-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="655bd-174">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Instruētā summa(InstructedAmount)”.</span><span class="sxs-lookup"><span data-stu-id="655bd-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="655bd-175">Noklikšķiniet uz Pievienot lauku pie.</span><span class="sxs-lookup"><span data-stu-id="655bd-175">Click Add field to.</span></span>
16. <span data-ttu-id="655bd-176">Noklikšķiniet uz Apkopojuma lauki.</span><span class="sxs-lookup"><span data-stu-id="655bd-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="655bd-177">Atlasiet opciju laukā Metode.</span><span class="sxs-lookup"><span data-stu-id="655bd-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="655bd-178">Atlasiet SUM apkopošanas funkciju.</span><span class="sxs-lookup"><span data-stu-id="655bd-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="655bd-179">Laukā Nosaukums ierakstiet “TotalInstructuredAmount”.</span><span class="sxs-lookup"><span data-stu-id="655bd-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="655bd-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="655bd-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="655bd-181">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="655bd-181">Click Save.</span></span>
20. <span data-ttu-id="655bd-182">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="655bd-182">Close the page.</span></span>
21. <span data-ttu-id="655bd-183">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="655bd-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="655bd-184">Kartēt formāta komponentus uz datu avotiem</span><span class="sxs-lookup"><span data-stu-id="655bd-184">Map format components to data sources</span></span>
1. <span data-ttu-id="655bd-185">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="655bd-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="655bd-186">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="655bd-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="655bd-187">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Iniciējošā puse(InitiatingParty)”.</span><span class="sxs-lookup"><span data-stu-id="655bd-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="655bd-188">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Iniciējošā puse(InitiatingParty)\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="655bd-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="655bd-189">Koka struktūrā izvērsiet zaru “Excel\ReportHeader”.</span><span class="sxs-lookup"><span data-stu-id="655bd-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="655bd-190">Koka struktūrā atlasiet zaru “Excel\ReportHeader\CompanyName”.</span><span class="sxs-lookup"><span data-stu-id="655bd-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="655bd-191">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-191">Click Bind.</span></span>
8. <span data-ttu-id="655bd-192">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="655bd-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="655bd-193">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditors\Identifikācija“.</span><span class="sxs-lookup"><span data-stu-id="655bd-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="655bd-194">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditors\Identifikācija\Avota ID(SourceID)“.</span><span class="sxs-lookup"><span data-stu-id="655bd-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="655bd-195">Koka struktūrā izvērsiet zaru “Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="655bd-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="655bd-196">Koka struktūrā atlasiet zaru “Excel\PaymLines\VendAccountName”.</span><span class="sxs-lookup"><span data-stu-id="655bd-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="655bd-197">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-197">Click Bind.</span></span>
14. <span data-ttu-id="655bd-198">Kokā atlasiet “modelis\Maksājumi\Kreditors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="655bd-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="655bd-199">Koka struktūrā atlasiet zaru “Excel\PaymLines\VendName”.</span><span class="sxs-lookup"><span data-stu-id="655bd-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="655bd-200">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-200">Click Bind.</span></span>
17. <span data-ttu-id="655bd-201">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="655bd-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="655bd-202">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Nosaukums“.</span><span class="sxs-lookup"><span data-stu-id="655bd-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="655bd-203">Koka struktūrā atlasiet zaru “Excel\PaymLines\Banka”.</span><span class="sxs-lookup"><span data-stu-id="655bd-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="655bd-204">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-204">Click Bind.</span></span>
21. <span data-ttu-id="655bd-205">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Maršrutēšanas numurs(RoutingNumber)”.</span><span class="sxs-lookup"><span data-stu-id="655bd-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="655bd-206">Koka struktūrā atlasiet zaru “Excel\PaymLines\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="655bd-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="655bd-207">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-207">Click Bind.</span></span>
24. <span data-ttu-id="655bd-208">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)“.</span><span class="sxs-lookup"><span data-stu-id="655bd-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="655bd-209">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija“.</span><span class="sxs-lookup"><span data-stu-id="655bd-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="655bd-210">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija\Numurs“.</span><span class="sxs-lookup"><span data-stu-id="655bd-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="655bd-211">Koka struktūrā atlasiet zaru “Excel\PaymLines\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="655bd-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="655bd-212">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-212">Click Bind.</span></span>
29. <span data-ttu-id="655bd-213">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Instruētā summa(InstructedAmount)”.</span><span class="sxs-lookup"><span data-stu-id="655bd-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="655bd-214">Koka struktūrā atlasiet zaru “Excel\PaymLines\Debit”.</span><span class="sxs-lookup"><span data-stu-id="655bd-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="655bd-215">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-215">Click Bind.</span></span>
32. <span data-ttu-id="655bd-216">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="655bd-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="655bd-217">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)“.</span><span class="sxs-lookup"><span data-stu-id="655bd-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="655bd-218">Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)“.</span><span class="sxs-lookup"><span data-stu-id="655bd-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="655bd-219">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="655bd-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="655bd-220">Koka struktūrā atlasiet zaru “Excel\PaymLines\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="655bd-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="655bd-221">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-221">Click Bind.</span></span>
38. <span data-ttu-id="655bd-222">Koka struktūrā izvērsiet elementu “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="655bd-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="655bd-223">Koka struktūrā izvērsiet elementu “PaymentByCurrency\grupēts”.</span><span class="sxs-lookup"><span data-stu-id="655bd-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="655bd-224">Koka struktūrā atlasiet elementu “PaymentByCurrency\grupēts\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="655bd-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="655bd-225">Koka struktūrā izvērsiet zaru “Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="655bd-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="655bd-226">Koka struktūrā atlasiet zaru “Excel\SummaryLines\SummaryCurrency”.</span><span class="sxs-lookup"><span data-stu-id="655bd-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="655bd-227">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-227">Click Bind.</span></span>
44. <span data-ttu-id="655bd-228">Koka struktūrā izvērsiet elementu “PaymentByCurrency\apkopots”.</span><span class="sxs-lookup"><span data-stu-id="655bd-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="655bd-229">Koka struktūrā atlasiet elementu “PaymentByCurrency\apkopots\TotalInstructuredAmount”.</span><span class="sxs-lookup"><span data-stu-id="655bd-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="655bd-230">Koka struktūrā atlasiet zaru “Excel\SummaryLines\SummaryAmount”.</span><span class="sxs-lookup"><span data-stu-id="655bd-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="655bd-231">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-231">Click Bind.</span></span>
48. <span data-ttu-id="655bd-232">Koka struktūrā atlasiet elementu “PaymentByCurrency”.</span><span class="sxs-lookup"><span data-stu-id="655bd-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="655bd-233">Koka struktūrā atlasiet zaru “Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="655bd-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="655bd-234">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-234">Click Bind.</span></span>
51. <span data-ttu-id="655bd-235">Kokā atlasiet “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="655bd-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="655bd-236">Koka struktūrā atlasiet zaru “Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="655bd-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="655bd-237">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="655bd-237">Click Bind.</span></span>
54. <span data-ttu-id="655bd-238">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="655bd-238">Click Save.</span></span>
55. <span data-ttu-id="655bd-239">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="655bd-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="655bd-240">Izmantojiet izveidoto konfigurāciju maksājumu apstrādei</span><span class="sxs-lookup"><span data-stu-id="655bd-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="655bd-241">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="655bd-241">Click Change status.</span></span>
2. <span data-ttu-id="655bd-242">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="655bd-242">Click Complete.</span></span>
3. <span data-ttu-id="655bd-243">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="655bd-243">Click OK.</span></span>
4. <span data-ttu-id="655bd-244">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="655bd-244">Close the page.</span></span>
5. <span data-ttu-id="655bd-245">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="655bd-245">Close the page.</span></span>
6. <span data-ttu-id="655bd-246">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="655bd-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="655bd-247">Izmantojiet līdzekli Ātrais filtrs, lai filtrētu pēc lauka Maksāšanas metode ar vērtību “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="655bd-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="655bd-248">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="655bd-248">Electronic</span></span>  
8. <span data-ttu-id="655bd-249">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="655bd-249">Click Edit.</span></span>
9. <span data-ttu-id="655bd-250">Izvērsiet sadaļu Failu formāti.</span><span class="sxs-lookup"><span data-stu-id="655bd-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="655bd-251">Laukā Vispārīga elektronisko pārskatu veidošana atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="655bd-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="655bd-252">Ievadiet vai atlasiet vērtību laukā Eksporta formāta konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="655bd-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="655bd-253">Atlasiet konfigurāciju “Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="655bd-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="655bd-254">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="655bd-254">Click Save.</span></span>
13. <span data-ttu-id="655bd-255">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="655bd-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="655bd-256">Izmantot izveidoto konfigurāciju maksājumu žurnālu apstrādes testēšanai</span><span class="sxs-lookup"><span data-stu-id="655bd-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="655bd-257">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="655bd-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="655bd-258">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="655bd-258">Click New.</span></span>
    * <span data-ttu-id="655bd-259">Izveidojiet jaunu maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="655bd-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="655bd-260">Laukā Nosaukums ierakstiet VendPay.</span><span class="sxs-lookup"><span data-stu-id="655bd-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="655bd-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="655bd-261">VendPay</span></span>  
4. <span data-ttu-id="655bd-262">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="655bd-262">Click Lines.</span></span>
5. <span data-ttu-id="655bd-263">Laukā Konts norādiet vērtības “GB_SI_000001”.</span><span class="sxs-lookup"><span data-stu-id="655bd-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="655bd-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="655bd-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="655bd-265">Vienumam Debets norādiet vērtību “1000”.</span><span class="sxs-lookup"><span data-stu-id="655bd-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="655bd-266">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="655bd-266">Click New.</span></span>
8. <span data-ttu-id="655bd-267">Laukā Konts norādiet vērtības “GB_SI_000005”.</span><span class="sxs-lookup"><span data-stu-id="655bd-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="655bd-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="655bd-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="655bd-269">Vienumam Debets norādiet vērtību “2000”.</span><span class="sxs-lookup"><span data-stu-id="655bd-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="655bd-270">Laukā Valūta ierakstiet vērtību “EUR”.</span><span class="sxs-lookup"><span data-stu-id="655bd-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="655bd-271">EUR</span><span class="sxs-lookup"><span data-stu-id="655bd-271">EUR</span></span>  
11. <span data-ttu-id="655bd-272">Laukā Korespondējošais konts norādiet vērtības “GBSI OPER”.</span><span class="sxs-lookup"><span data-stu-id="655bd-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="655bd-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="655bd-273">GBSI OPER</span></span>  
12. <span data-ttu-id="655bd-274">Laukā Maksāšanas metode ierakstiet “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="655bd-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="655bd-275">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="655bd-275">Electronic</span></span>  
13. <span data-ttu-id="655bd-276">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="655bd-276">Click Save.</span></span>
14. <span data-ttu-id="655bd-277">Noklikšķiniet uz Ģenerēt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="655bd-277">Click Generate payments.</span></span>
15. <span data-ttu-id="655bd-278">Laukā Maksāšanas metode ierakstiet “Elektroniski”.</span><span class="sxs-lookup"><span data-stu-id="655bd-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="655bd-279">Elektroniski</span><span class="sxs-lookup"><span data-stu-id="655bd-279">Electronic</span></span>  
16. <span data-ttu-id="655bd-280">Laukā Faila nosaukums ierakstiet “Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="655bd-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="655bd-281">Piemēram, tips Maksājumi.</span><span class="sxs-lookup"><span data-stu-id="655bd-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="655bd-282">Laukā Bankas konts atlasiet “GBSI OPER”.</span><span class="sxs-lookup"><span data-stu-id="655bd-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="655bd-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="655bd-283">GBSI OPER</span></span>  
18. <span data-ttu-id="655bd-284">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="655bd-284">Click OK.</span></span>
19. <span data-ttu-id="655bd-285">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="655bd-285">Click OK.</span></span>
    * <span data-ttu-id="655bd-286">Pārskatiet izveidoto darblapu, tostarp informāciju par maksājuma rindām, kā arī kopsummas katram valūtas kodam, kas ir izmantots šajā maksājuma ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="655bd-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


