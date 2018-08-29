--- 
title: "ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā"
description: "Nākamajās darbībās ir paskaidrots, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektronisko pārskatu izstrādātājs, var konfigurēt elektronisko pārskatu veidošanas (Electronic reporting — ER) formātus, lai pārskatus ģenerētu kā Microsoft Word failus."
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 615ab4a4f932478b8b847112d4fed8310187f03b
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="fac38-103">ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā</span><span class="sxs-lookup"><span data-stu-id="fac38-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fac38-104">Nākamajās darbībās ir paskaidrots, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektronisko pārskatu izstrādātājs, var konfigurēt elektronisko pārskatu veidošanas (Electronic reporting — ER) formātus, lai pārskatus ģenerētu kā Microsoft Word failus.</span><span class="sxs-lookup"><span data-stu-id="fac38-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="fac38-105">Šīs darbības var veikt uzņēmumā GBSI.</span><span class="sxs-lookup"><span data-stu-id="fac38-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="fac38-106">Lai veiktu šīs darbības, jums vispirms ir jāizpilda uzdevuma ceļvedī “Izveidot ER konfigurāciju pārskatu ģenerēšanai formātā OPENXML” norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fac38-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="fac38-107">Turklāt jums ir nepieciešams šim pašam pārskatam jau iepriekš lejupielādēt un lokāli saglabāt šādas veidnes:</span><span class="sxs-lookup"><span data-stu-id="fac38-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

[<span data-ttu-id="fac38-108">Maksājumu pārskata veidne</span><span class="sxs-lookup"><span data-stu-id="fac38-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

[<span data-ttu-id="fac38-109">Maksājumu pārskata saistītā veidne</span><span class="sxs-lookup"><span data-stu-id="fac38-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="fac38-110">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Microsoft Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="fac38-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="fac38-111">Atlasiet esošo ER pārskatu konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="fac38-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="fac38-112">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="fac38-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fac38-113">Pārliecinieties, vai konfigurācijas nodrošinātājs “Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="fac38-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="fac38-114">ir atlasīts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="fac38-114">is selected as active.</span></span>  
2. <span data-ttu-id="fac38-115">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="fac38-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="fac38-116">Mēs atkārtoti izmantosim esošo ER konfigurācija, kas sākotnēji tika veidota tā, lai pārskata izvadi ģenerētu formātā OPENXML.</span><span class="sxs-lookup"><span data-stu-id="fac38-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="fac38-117">Kokā struktūra izvērsiet sadaļu “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="fac38-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="fac38-118">Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="fac38-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="fac38-119">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="fac38-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="fac38-120">Excel veidni nomainīt pret Word veidni</span><span class="sxs-lookup"><span data-stu-id="fac38-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="fac38-121">Pašlaik Excel dokuments tiek izmantots kā veidne, lai ģenerētu izvadi formātā OPENXML.</span><span class="sxs-lookup"><span data-stu-id="fac38-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="fac38-122">Mēs šo pārskata veidni importēsim formātā Word.</span><span class="sxs-lookup"><span data-stu-id="fac38-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="fac38-123">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="fac38-123">Click Attachments.</span></span>
    * <span data-ttu-id="fac38-124">Aizstājiet esošo Excel veidni ar iepriekš lejupielādēto Word veidni Maksājumu pārskata veidne.</span><span class="sxs-lookup"><span data-stu-id="fac38-124">Replace the existing Excel template with the Word template that you downloaded earlier, Template of Payment Report.</span></span> <span data-ttu-id="fac38-125">Ņemiet vērā, ka šī veidne satur tikai dokumenta izkārtojumu, kuru vēlamies ģenerēt kā ER izvadi.</span><span class="sxs-lookup"><span data-stu-id="fac38-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="fac38-126">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="fac38-126">Click Delete.</span></span>
3. <span data-ttu-id="fac38-127">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="fac38-127">Click Yes.</span></span>
4. <span data-ttu-id="fac38-128">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="fac38-128">Click New.</span></span>
5. <span data-ttu-id="fac38-129">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="fac38-129">Click File.</span></span>
6. <span data-ttu-id="fac38-130">Noklikšķiniet uz Pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="fac38-130">Click Browse.</span></span> <span data-ttu-id="fac38-131">Pārejiet uz iepriekš lejupielādēto veidni SampleVendPaymDocReport.docx un atlasiet to.</span><span class="sxs-lookup"><span data-stu-id="fac38-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="fac38-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fac38-132">Click OK.</span></span>
    * <span data-ttu-id="fac38-133">Atlasiet veidni, kuru lejupielādējāt iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="fac38-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="fac38-134">Ievadiet vai atlasiet kādu vērtību laukā Veidne.</span><span class="sxs-lookup"><span data-stu-id="fac38-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="fac38-135">Paplašināt Word veidni, pievienojot pielāgotu XML daļu</span><span class="sxs-lookup"><span data-stu-id="fac38-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="fac38-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="fac38-136">Click Save.</span></span>
    * <span data-ttu-id="fac38-137">Papildus konfigurācijas izmaiņu uzglabāšanai darbība Saglabāt arī atjaunina pievienoto Word veidni.</span><span class="sxs-lookup"><span data-stu-id="fac38-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="fac38-138">Izstrādātā formāta struktūra tiek pārnesta uz pievienoto Word dokumentu kā jauna pielāgota XML daļa ar nosaukumu “Pārskats”.</span><span class="sxs-lookup"><span data-stu-id="fac38-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="fac38-139">Ņemiet vērā, ka pievienotajā Word veidnē ir ne tikai dokumenta izkārtojums, kādā vēlamies ģenerēt ER izvadi, bet tajā ir arī datu struktūra, ar ko ER izpildlaikā aizpildīs šo veidni.</span><span class="sxs-lookup"><span data-stu-id="fac38-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="fac38-140">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="fac38-140">Click Attachments.</span></span>
    * <span data-ttu-id="fac38-141">Tagad pielāgotās XML daļas “Pārskats” elementi ir jāsaista ar Word dokumenta daļām.</span><span class="sxs-lookup"><span data-stu-id="fac38-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="fac38-142">Ja pārzināt Word dokumentus, ko var noformēt kā veidlapas, kurās atrodas ar pielāgotām XML daļām saistītas satura vadīklas — atskaņojiet visas nākamā apakšuzdevuma darbības, lai izveidotu šādu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="fac38-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="fac38-143">Papildinformāciju skatiet šajā saitē: https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="fac38-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="fac38-144">Pretējā gadījumā izlaidiet visas nākamā apakšuzdevuma darbības.</span><span class="sxs-lookup"><span data-stu-id="fac38-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="fac38-145">Panākt, ka Word un pielāgotai XML daļai tiek veikti datu saistījumi</span><span class="sxs-lookup"><span data-stu-id="fac38-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="fac38-146">Atveriet šo dokumentu programmā Word un izpildiet tālāk aprakstītos norādījumus. - Atveriet cilni Word izstrādātājs (pielāgojiet lenti, ja tā vēl nav iespējota).</span><span class="sxs-lookup"><span data-stu-id="fac38-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="fac38-147">- Atlasiet XML kartēšanas rūti.</span><span class="sxs-lookup"><span data-stu-id="fac38-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="fac38-148">- Uzmeklēšanā atlasiet pielāgoto XML daļu “Pārskats”.</span><span class="sxs-lookup"><span data-stu-id="fac38-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="fac38-149">- Veiciet atlasītās pielāgotās XML daļas elementu un Word dokumenta satura vadīklu kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="fac38-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="fac38-150">- Atjaunināto Word dokumentu saglabājiet lokālajā diskā.</span><span class="sxs-lookup"><span data-stu-id="fac38-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="fac38-151">Augšupielādēt Word veidni, kur ar satura vadīklām ir saistīta pielāgota XML daļa</span><span class="sxs-lookup"><span data-stu-id="fac38-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="fac38-152">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="fac38-152">Click Delete.</span></span>
2. <span data-ttu-id="fac38-153">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="fac38-153">Click Yes.</span></span>
    * <span data-ttu-id="fac38-154">Pievienojiet jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="fac38-154">Add a new template.</span></span> <span data-ttu-id="fac38-155">Ja esat izpildījis iepriekšējā apakšuzdevumā aprakstītās darbības, atlasiet Word dokumentu, kuru sagatavojāt un lokāli saglabājāt.</span><span class="sxs-lookup"><span data-stu-id="fac38-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="fac38-156">Pretējā gadījumā atlasiet iepriekš lejupielādēto SampleVendPaymDocReportBounded.docx MS Word veidni.</span><span class="sxs-lookup"><span data-stu-id="fac38-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="fac38-157">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="fac38-157">Click New.</span></span>
4. <span data-ttu-id="fac38-158">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="fac38-158">Click File.</span></span>
5. <span data-ttu-id="fac38-159">Noklikšķiniet uz Pārlūkot.</span><span class="sxs-lookup"><span data-stu-id="fac38-159">Click Browse.</span></span> <span data-ttu-id="fac38-160">Pārejiet uz iepriekš lejupielādēto veidni SampleVendPaymDocReportBounded.docx un atlasiet to.</span><span class="sxs-lookup"><span data-stu-id="fac38-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="fac38-161">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="fac38-161">Click OK.</span></span>
6. <span data-ttu-id="fac38-162">Laukā Veidne atlasiet dokumentu, kuru lejupielādējāt iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="fac38-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="fac38-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="fac38-163">Click Save.</span></span>
8. <span data-ttu-id="fac38-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fac38-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="fac38-165">Izpildīt formātu, lai izveidotu Word izvadi</span><span class="sxs-lookup"><span data-stu-id="fac38-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="fac38-166">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="fac38-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="fac38-167">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="fac38-167">Click User parameters.</span></span>
3. <span data-ttu-id="fac38-168">Laukā Palaist iestatījumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="fac38-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="fac38-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fac38-169">Click OK.</span></span>
5. <span data-ttu-id="fac38-170">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="fac38-170">Click Edit.</span></span>
6. <span data-ttu-id="fac38-171">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="fac38-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="fac38-172">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="fac38-172">Click Save.</span></span>
8. <span data-ttu-id="fac38-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fac38-173">Close the page.</span></span>
9. <span data-ttu-id="fac38-174">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fac38-174">Close the page.</span></span>
10. <span data-ttu-id="fac38-175">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="fac38-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="fac38-176">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="fac38-176">Click Lines.</span></span>
12. <span data-ttu-id="fac38-177">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="fac38-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="fac38-178">Noklikšķiniet uz Maksājuma statuss.</span><span class="sxs-lookup"><span data-stu-id="fac38-178">Click Payment status.</span></span>
14. <span data-ttu-id="fac38-179">Noklikšķiniet uz Nav.</span><span class="sxs-lookup"><span data-stu-id="fac38-179">Click None.</span></span>
15. <span data-ttu-id="fac38-180">Noklikšķiniet uz Ģenerēt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="fac38-180">Click Generate payments.</span></span>
16. <span data-ttu-id="fac38-181">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fac38-181">Click OK.</span></span>
17. <span data-ttu-id="fac38-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fac38-182">Click OK.</span></span>
    * <span data-ttu-id="fac38-183">Analizējiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="fac38-183">Analyze the generated output.</span></span> <span data-ttu-id="fac38-184">Ņemiet vērā, ka izveidotā izvade tiek rādīta formātā Word, un tā ietver detalizētu informāciju par apstrādātajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="fac38-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


