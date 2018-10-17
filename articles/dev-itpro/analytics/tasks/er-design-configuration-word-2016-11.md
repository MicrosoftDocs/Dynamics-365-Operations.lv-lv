--- 
title: "ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā"
description: "Nākamajās darbībās ir paskaidrots, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektronisko pārskatu izstrādātājs, var konfigurēt elektronisko pārskatu veidošanas formātus, lai pārskatus ģenerētu kā Microsoft Word failus."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="9b48a-103">ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā</span><span class="sxs-lookup"><span data-stu-id="9b48a-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b48a-104">Nākamajās darbībās ir paskaidrots, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektronisko pārskatu izstrādātājs, var konfigurēt elektronisko pārskatu veidošanas (Electronic reporting — ER) formātus, lai pārskatus ģenerētu kā Microsoft Word failus.</span><span class="sxs-lookup"><span data-stu-id="9b48a-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="9b48a-105">Šīs darbības var veikt uzņēmumā GBSI.</span><span class="sxs-lookup"><span data-stu-id="9b48a-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="9b48a-106">Lai veiktu šīs darbības, jums vispirms ir jāizpilda uzdevuma ceļvedī “Izveidot ER konfigurāciju pārskatu ģenerēšanai formātā OPENXML” norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9b48a-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="9b48a-107">Turklāt jums ir nepieciešams šim pašam pārskatam jau iepriekš lejupielādēt un lokāli saglabāt šādas veidnes:</span><span class="sxs-lookup"><span data-stu-id="9b48a-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="9b48a-108">Maksājumu pārskata veidne</span><span class="sxs-lookup"><span data-stu-id="9b48a-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="9b48a-109">Maksājumu pārskata saistītā veidne</span><span class="sxs-lookup"><span data-stu-id="9b48a-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="9b48a-110">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Microsoft Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="9b48a-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="9b48a-111">Atlasiet esošo ER pārskatu konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="9b48a-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="9b48a-112">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="9b48a-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="9b48a-113">Pārliecinieties, vai konfigurācijas nodrošinātājs “Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="9b48a-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="9b48a-114">ir atlasīts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="9b48a-114">is selected as active.</span></span>  
2. <span data-ttu-id="9b48a-115">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="9b48a-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="9b48a-116">Mēs atkārtoti izmantosim esošo ER konfigurācija, kas sākotnēji tika veidota tā, lai pārskata izvadi ģenerētu formātā OPENXML.</span><span class="sxs-lookup"><span data-stu-id="9b48a-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="9b48a-117">Kokā struktūra izvērsiet sadaļu “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="9b48a-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="9b48a-118">Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="9b48a-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="9b48a-119">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="9b48a-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="9b48a-120">Excel veidni nomainīt pret Word veidni</span><span class="sxs-lookup"><span data-stu-id="9b48a-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="9b48a-121">Pašlaik Excel dokuments tiek izmantots kā veidne, lai ģenerētu izvadi formātā OPENXML.</span><span class="sxs-lookup"><span data-stu-id="9b48a-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="9b48a-122">Mēs šo pārskata veidni importēsim formātā Word.</span><span class="sxs-lookup"><span data-stu-id="9b48a-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="9b48a-123">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="9b48a-123">Click Attachments.</span></span>
    * <span data-ttu-id="9b48a-124">Esošo Excel veidni aizstājiet ar iepriekš lejupielādēto Word veidni SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="9b48a-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="9b48a-125">Ņemiet vērā, ka šī veidne satur tikai dokumenta izkārtojumu, kuru vēlamies ģenerēt kā ER izvadi.</span><span class="sxs-lookup"><span data-stu-id="9b48a-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="9b48a-126">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="9b48a-126">Click Delete.</span></span>
3. <span data-ttu-id="9b48a-127">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="9b48a-127">Click Yes.</span></span>
4. <span data-ttu-id="9b48a-128">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9b48a-128">Click New.</span></span>
5. <span data-ttu-id="9b48a-129">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="9b48a-129">Click File.</span></span>
6. <span data-ttu-id="9b48a-130">Noklikšķiniet uz Pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="9b48a-130">Click Browse.</span></span> <span data-ttu-id="9b48a-131">Pārejiet uz iepriekš lejupielādēto veidni SampleVendPaymDocReport.docx un atlasiet to.</span><span class="sxs-lookup"><span data-stu-id="9b48a-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="9b48a-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9b48a-132">Click OK.</span></span>
    * <span data-ttu-id="9b48a-133">Atlasiet veidni, kuru lejupielādējāt iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="9b48a-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="9b48a-134">Ievadiet vai atlasiet kādu vērtību laukā Veidne.</span><span class="sxs-lookup"><span data-stu-id="9b48a-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="9b48a-135">Paplašināt Word veidni, pievienojot pielāgotu XML daļu</span><span class="sxs-lookup"><span data-stu-id="9b48a-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="9b48a-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9b48a-136">Click Save.</span></span>
    * <span data-ttu-id="9b48a-137">Papildus konfigurācijas izmaiņu uzglabāšanai darbība Saglabāt arī atjaunina pievienoto Word veidni.</span><span class="sxs-lookup"><span data-stu-id="9b48a-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="9b48a-138">Izstrādātā formāta struktūra tiek pārnesta uz pievienoto Word dokumentu kā jauna pielāgota XML daļa ar nosaukumu “Pārskats”.</span><span class="sxs-lookup"><span data-stu-id="9b48a-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="9b48a-139">Ņemiet vērā, ka pievienotajā Word veidnē ir ne tikai dokumenta izkārtojums, kādā vēlamies ģenerēt ER izvadi, bet tajā ir arī datu struktūra, ar ko ER izpildlaikā aizpildīs šo veidni.</span><span class="sxs-lookup"><span data-stu-id="9b48a-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="9b48a-140">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="9b48a-140">Click Attachments.</span></span>
    * <span data-ttu-id="9b48a-141">Tagad pielāgotās XML daļas “Pārskats” elementi ir jāsaista ar Word dokumenta daļām.</span><span class="sxs-lookup"><span data-stu-id="9b48a-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="9b48a-142">Ja pārzināt Word dokumentus, ko var noformēt kā veidlapas, kurās atrodas ar pielāgotām XML daļām saistītas satura vadīklas — atskaņojiet visas nākamā apakšuzdevuma darbības, lai izveidotu šādu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="9b48a-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="9b48a-143">Papildinformāciju skatiet šajā saitē: https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="9b48a-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="9b48a-144">Pretējā gadījumā izlaidiet visas nākamā apakšuzdevuma darbības.</span><span class="sxs-lookup"><span data-stu-id="9b48a-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="9b48a-145">Panākt, ka Word un pielāgotai XML daļai tiek veikti datu saistījumi</span><span class="sxs-lookup"><span data-stu-id="9b48a-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="9b48a-146">Atveriet šo dokumentu programmā Word un izpildiet tālāk aprakstītos norādījumus. - Atveriet cilni Word izstrādātājs (pielāgojiet lenti, ja tā vēl nav iespējota).</span><span class="sxs-lookup"><span data-stu-id="9b48a-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="9b48a-147">- Atlasiet XML kartēšanas rūti.</span><span class="sxs-lookup"><span data-stu-id="9b48a-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="9b48a-148">- Uzmeklēšanā atlasiet pielāgoto XML daļu “Pārskats”.</span><span class="sxs-lookup"><span data-stu-id="9b48a-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="9b48a-149">- Veiciet atlasītās pielāgotās XML daļas elementu un Word dokumenta satura vadīklu kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="9b48a-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="9b48a-150">- Atjaunināto Word dokumentu saglabājiet lokālajā diskā.</span><span class="sxs-lookup"><span data-stu-id="9b48a-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="9b48a-151">Augšupielādēt Word veidni, kur ar satura vadīklām ir saistīta pielāgota XML daļa</span><span class="sxs-lookup"><span data-stu-id="9b48a-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="9b48a-152">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="9b48a-152">Click Delete.</span></span>
2. <span data-ttu-id="9b48a-153">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="9b48a-153">Click Yes.</span></span>
    * <span data-ttu-id="9b48a-154">Pievienojiet jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="9b48a-154">Add a new template.</span></span> <span data-ttu-id="9b48a-155">Ja esat izpildījis iepriekšējā apakšuzdevumā aprakstītās darbības, atlasiet Word dokumentu, kuru sagatavojāt un lokāli saglabājāt.</span><span class="sxs-lookup"><span data-stu-id="9b48a-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="9b48a-156">Pretējā gadījumā atlasiet iepriekš lejupielādēto SampleVendPaymDocReportBounded.docx MS Word veidni.</span><span class="sxs-lookup"><span data-stu-id="9b48a-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="9b48a-157">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9b48a-157">Click New.</span></span>
4. <span data-ttu-id="9b48a-158">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="9b48a-158">Click File.</span></span>
5. <span data-ttu-id="9b48a-159">Noklikšķiniet uz Pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="9b48a-159">Click Browse.</span></span> <span data-ttu-id="9b48a-160">Pārejiet uz iepriekš lejupielādēto veidni SampleVendPaymDocReportBounded.docx un atlasiet to.</span><span class="sxs-lookup"><span data-stu-id="9b48a-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="9b48a-161">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="9b48a-161">Click OK.</span></span>
6. <span data-ttu-id="9b48a-162">Laukā Veidne atlasiet dokumentu, kuru lejupielādējāt iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="9b48a-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="9b48a-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9b48a-163">Click Save.</span></span>
8. <span data-ttu-id="9b48a-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9b48a-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="9b48a-165">Izpildīt formātu, lai izveidotu Word izvadi</span><span class="sxs-lookup"><span data-stu-id="9b48a-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="9b48a-166">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="9b48a-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="9b48a-167">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="9b48a-167">Click User parameters.</span></span>
3. <span data-ttu-id="9b48a-168">Laukā Palaist iestatījumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9b48a-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="9b48a-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9b48a-169">Click OK.</span></span>
5. <span data-ttu-id="9b48a-170">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9b48a-170">Click Edit.</span></span>
6. <span data-ttu-id="9b48a-171">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9b48a-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="9b48a-172">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9b48a-172">Click Save.</span></span>
8. <span data-ttu-id="9b48a-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9b48a-173">Close the page.</span></span>
9. <span data-ttu-id="9b48a-174">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9b48a-174">Close the page.</span></span>
10. <span data-ttu-id="9b48a-175">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="9b48a-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="9b48a-176">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="9b48a-176">Click Lines.</span></span>
12. <span data-ttu-id="9b48a-177">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="9b48a-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="9b48a-178">Noklikšķiniet uz Maksājuma statuss.</span><span class="sxs-lookup"><span data-stu-id="9b48a-178">Click Payment status.</span></span>
14. <span data-ttu-id="9b48a-179">Noklikšķiniet uz Nav.</span><span class="sxs-lookup"><span data-stu-id="9b48a-179">Click None.</span></span>
15. <span data-ttu-id="9b48a-180">Noklikšķiniet uz Ģenerēt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="9b48a-180">Click Generate payments.</span></span>
16. <span data-ttu-id="9b48a-181">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9b48a-181">Click OK.</span></span>
17. <span data-ttu-id="9b48a-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9b48a-182">Click OK.</span></span>
    * <span data-ttu-id="9b48a-183">Analizējiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="9b48a-183">Analyze the generated output.</span></span> <span data-ttu-id="9b48a-184">Ņemiet vērā, ka izveidotā izvade tiek rādīta formātā Word, un tā ietver detalizētu informāciju par apstrādātajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="9b48a-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


