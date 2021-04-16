---
title: ER konfigurāciju ar Excel veidnēm atkārtota izmantošana, lai veidotu pārskatus Word formātā
description: Šajā tēmā ir aprakstīts, kā pārskatu formātus, kas tika veidoti, lai ģenerētu pārskatus kā Excel darbgrāmatas, var konfigurēt, lai ģenerētu pārskatus kā Word dokumentus.
author: NickSelin
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 728984678d78cf626e2b30222f1d1e603e05d117
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755062"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="96492-103">ER konfigurāciju ar Excel veidnēm atkārtota izmantošana, lai veidotu pārskatus Word formātā</span><span class="sxs-lookup"><span data-stu-id="96492-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96492-104">Lai ģenrētu pārskatus kā Microsoft Word dokumentus, varat [konfigurēt](../er-design-configuration-word.md) jaunu [elektronisko pārskatu (ER)](../general-electronic-reporting.md) [formātu](../general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="96492-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="96492-105">Vai arī varat atkārtoti izmantot ER formātu, kas oriģināli tika izveidots, lai ģenerētu pārskatus kā Excel darbgrāmatas.</span><span class="sxs-lookup"><span data-stu-id="96492-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="96492-106">Šajā gadījumā Excel veidne ir jāaizstāj ar Word veidni.</span><span class="sxs-lookup"><span data-stu-id="96492-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="96492-107">Šīs procedūras parāda, kā lietotājs vai nu sistēmas administratora lomā, vai Elektronisko pārskatu izstrādātāja loma var konfigurēt ER formātu, lai ģenerētu pārskatus kā Word failus, atkārtoti izmantojot ER formātu, kas projektēja, lai ģenerētu pārskatus kā Excel failus.</span><span class="sxs-lookup"><span data-stu-id="96492-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="96492-108">Visas šīs procedūras var veikt uzņēmumā GBSI.</span><span class="sxs-lookup"><span data-stu-id="96492-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="96492-109">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="96492-109">Prerequisites</span></span>

<span data-ttu-id="96492-110">Lai veiktu šīs procedūras darbības, jums vispirms ir jāizpilda procedūra [Noformēt konfigurāciju pārskatu ģenerēšanai formātā OPENXML”](er-design-reports-openxml-2016-11.md) uzdevuma ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="96492-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="96492-111">Turklāt jums ir nepieciešams šim pašam pārskatam lejupielādēt un lokāli saglabāt šādas veidnes:</span><span class="sxs-lookup"><span data-stu-id="96492-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="96492-112">Maksājumu pārskata veidne (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="96492-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="96492-113">Maksājumu pārskata saistītā veidne (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="96492-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="96492-114">Šīs procedūras ir līdzeklim, kas ir pievienots versijā Dynamics 365 for Operations 1611 (2016. gada novembrī).</span><span class="sxs-lookup"><span data-stu-id="96492-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="96492-115">Atlasiet esošo ER pārskatu konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="96492-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="96492-116">Pakalpojumā Dynamics 365 Finance dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="96492-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="96492-117">Pārliecinieties, ka konfigurācijas nodrošinātājs **Litware, Inc.** ir atlasīts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="96492-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="96492-118">Ja tā nav, izpildiet konfigurācijas nodrošinātāju darbības sadaļā [Konfigurācijas nodrošinātāju izveidē un atzīmējiet tos kā](er-configuration-provider-mark-it-active-2016-11.md) aktīvus uzdevumu ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="96492-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="96492-119">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="96492-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="96492-120">Jūs atkārtoti izmantosim esošo ER konfigurāciju, kas sākotnēji tika veidota tā, lai pārskata izvadi ģenerētu formātā OPENXML.</span><span class="sxs-lookup"><span data-stu-id="96492-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="96492-121">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **Parauga darbgrāmatas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="96492-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="96492-122">Atlasītā ER formāta melnrakstu var rediģēt kopsavilkuma cilnē **Versijas**.</span><span class="sxs-lookup"><span data-stu-id="96492-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="96492-123">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="96492-123">Select **Designer**.</span></span>
6. <span data-ttu-id="96492-124">**Formāta veidotāja** lapā ievērojiet, ka saknes formāta elementa nosaukums norāda, ka pašlaik tiek izmantota Excel veidne.</span><span class="sxs-lookup"><span data-stu-id="96492-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Atlasiet esošo konfigurāciju](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="96492-126">Pārskatīt lejupielādēto Word veidni</span><span class="sxs-lookup"><span data-stu-id="96492-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="96492-127">Word darbvirsmas programmā atveriet **SampleVendPaymDocReport.docx veidnes** failu, kuru lejupielādējāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="96492-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="96492-128">Ņemiet vērā, ka šī veidne satur tikai dokumenta izkārtojumu, kuru vēlaties ģenerēt kā ER izvadi.</span><span class="sxs-lookup"><span data-stu-id="96492-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Pārskata parauga veidnes priekšskatīšana Word darbvirsmas programmā](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="96492-130">Aizstāt Excel veidni ar Word veidni un pievienot pielāgotu XML daļu</span><span class="sxs-lookup"><span data-stu-id="96492-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="96492-131">Pašlaik Excel dokuments tiek izmantots kā veidne, lai ģenerētu izvadi formātā OPENXML.</span><span class="sxs-lookup"><span data-stu-id="96492-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="96492-132">Esošo Excel veidni aizstājiet ar iepriekš lejupielādēto Word veidni SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="96492-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="96492-133">Paplašiniet Word veidni, pievienojot pielāgotu XML daļu.</span><span class="sxs-lookup"><span data-stu-id="96492-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="96492-134">Pakalpojuma Finance lapas **Formāta veidotājs** cilnē **Formāts** atlasiet **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="96492-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="96492-135">Lai noņemtu esošo Excel veidni, lapā **Pielikumi** atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="96492-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="96492-136">Atlasiet **Jā**, lai apstiprinātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="96492-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="96492-137">Atlasiet **Jauns** \> **Fails**.</span><span class="sxs-lookup"><span data-stu-id="96492-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="96492-138">Izmantojiet dokumenta veidu, kas [konfigurēts](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER parametros, lai glabātu ER formāta veidnes.</span><span class="sxs-lookup"><span data-stu-id="96492-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="96492-139">Atlasiet **Pārlūkot** un pēc tam pārlūkojiet un atlasiet **SampleVendPaymDocReport.docx** failu, kuru iepriekš lejupielādējāt.</span><span class="sxs-lookup"><span data-stu-id="96492-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="96492-140">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96492-140">Select **OK**.</span></span>
6. <span data-ttu-id="96492-141">Aizveriet lapu **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="96492-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="96492-142">**Formāta veidotāja** lapas laukā **Veidne** ievadiet vai atlasiet **SampleVendPaymDocReport.docx** failu, lai izmantotu šo Word veidni iepriekš izmantotās Excel veidnes vietā.</span><span class="sxs-lookup"><span data-stu-id="96492-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="96492-143">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="96492-143">Select **Save**.</span></span>

    <span data-ttu-id="96492-144">Papildus konfigurācijas izmaiņu uzglabāšanai darbība **Saglabāt** arī atjaunina pievienoto Word veidni.</span><span class="sxs-lookup"><span data-stu-id="96492-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="96492-145">Izstrādātā formāta struktūra tiek pārnesta uz pievienoto Word dokumentu kā jauna pielāgota XML daļa ar nosaukumu **Pārskats**.</span><span class="sxs-lookup"><span data-stu-id="96492-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="96492-146">Ņemiet vērā, ka pievienotajā Word veidnē ir ne tikai dokumenta izkārtojums, kādā vēlamies ģenerēt ER izvadi, bet tajā ir arī datu struktūra, ar ko ER izpildlaikā aizpildīs šo veidni.</span><span class="sxs-lookup"><span data-stu-id="96492-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="96492-147">Formāta veidotāja lapā ievērojiet, ka saknes formāta elementa nosaukums norāda, ka pašlaik tiek izmantota Excel veidne.</span><span class="sxs-lookup"><span data-stu-id="96492-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Aizstāt Excel veidni ar Word veidni un pievienot pielāgotu XML daļu](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="96492-149">Cilnē **Formāts** atlasiet **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="96492-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="96492-150">Veiciet elementu kartēšanu no **Pārskata** pielāgotās XML daļas un Word dokumenta satura vadīklām.</span><span class="sxs-lookup"><span data-stu-id="96492-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="96492-151">Ja pārzināt Word dokumentus, ko var noformēt kā veidlapas, kurās ir [satura vadīklas](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word), kas ir kartētas ar [pielāgotu XML daļu elementiem](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), pabeidziet visas darbības nākamajā procedūŗā, lai izveidotu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="96492-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="96492-152">Papildinformāciju skatiet rakstā [Veidlapu izveide, kuras lietotāji var aizpildīt un izdrukāt Word formātā](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="96492-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="96492-153">Pretējā gadījumā izlaidiet nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="96492-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="96492-154">Iegūt Word dokumentu, kam ir pielāgota XML daļa, un veikt datu kartēšanu</span><span class="sxs-lookup"><span data-stu-id="96492-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="96492-155">Finanšu lapā **Pielikumi** atlasiet **Atvērt**, lai lejupielādētu atlasīto veidni no Finanšu un uzglabātu to lokāli kā Word dokumentu.</span><span class="sxs-lookup"><span data-stu-id="96492-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="96492-156">Word datora programmā atveriet tikko lejupielādēto dokumentu.</span><span class="sxs-lookup"><span data-stu-id="96492-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="96492-157">Cilnē **Izstrādātājs** atlasiet **XML kartēšanas rūts**.</span><span class="sxs-lookup"><span data-stu-id="96492-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="96492-158">Ja cilne **Izstrādātājs** nav redzama lentē, pielāgojiet lenti tās pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="96492-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="96492-159">**XML kartējuma** rūts laukā **Pielāgotā XML daļa** atlasiet **Pārskata** pielāgoto XML daļu.</span><span class="sxs-lookup"><span data-stu-id="96492-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="96492-160">Veiciet elementu kartēšanu no **Pārskata** pielāgotās XML daļas un Word dokumenta satura vadīklām.</span><span class="sxs-lookup"><span data-stu-id="96492-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="96492-161">Saglabājiet atjaunināto Word dokumentu lokāli kā **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="96492-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="96492-162">Pārskatīt Word veidni, kur pielāgotā XML daļa ir kartēta uz satura vadīklām</span><span class="sxs-lookup"><span data-stu-id="96492-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="96492-163">Word darbvirsmas programmā atveriet **SampleVendPaymDocReport.docx veidnes** veidnes failu.</span><span class="sxs-lookup"><span data-stu-id="96492-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="96492-164">Ņemiet vērā, ka šī veidne satur tikai dokumenta izkārtojumu, kuru vēlaties ģenerēt kā ER izvadi.</span><span class="sxs-lookup"><span data-stu-id="96492-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="96492-165">Satura vadīklas, kas tiek izmantotas kā vietturi datiem, ko ER ievadīs šajā veidnē izpildlaikā, ir balstītas uz kartējumiem, kas ir konfigurēti starp **Pārskata** pielāgotās XML daļas elementiem un Word dokumenta satura vadīklām.</span><span class="sxs-lookup"><span data-stu-id="96492-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Pārskata parauga veidnes priekšskatīšana Word darbvirsmas programmā](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="96492-167">Pārskatīt Word veidni, kur pielāgotā XML daļa ir kartēta uz satura vadīklām</span><span class="sxs-lookup"><span data-stu-id="96492-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="96492-168">Finanšu dokumentu lapā **Pielikumi** atlasiet **Dzēst**, lai noņemtu Word veidni, kam nav kartējumu starp **Pārskata** pielāgotās XML daļas un satura kontroles elementiem.</span><span class="sxs-lookup"><span data-stu-id="96492-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="96492-169">Atlasiet **Jā**, lai apstiprinātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="96492-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="96492-170">Atlasiet **Jauns** \> **Fails**, lai pievienotu jaunu veidnes failu, kas satur kartējumus starp **Pārskata** pielāgotās XML daļas elementiem un satura vadīklām.</span><span class="sxs-lookup"><span data-stu-id="96492-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="96492-171">Izmantojiet dokumenta veidu, kas [konfigurēts](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER parametros, lai glabātu ER formāta veidnes.</span><span class="sxs-lookup"><span data-stu-id="96492-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="96492-172">Atlasiet **Pārlūkot** un pēc tam pārlūkojiet un atlasiet **SampleVendPaymDocReportBounded.docx** failu, kuru lejupielādējat vai sagatavojat, izpildot procedūru sadaļā [Iegūt Word, kam ir pielāgota XML daļa, lai paveiktu datu kartēšanu](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="96492-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="96492-173">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96492-173">Select **OK**.</span></span>
5. <span data-ttu-id="96492-174">Aizveriet lapu **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="96492-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="96492-175">**Formāta veidotāja** lapas laukā **Veidnes** izvēlieties dokumentu, ko tikko lejupielādējāt.</span><span class="sxs-lookup"><span data-stu-id="96492-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="96492-176">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="96492-176">Select **Save**.</span></span>
8. <span data-ttu-id="96492-177">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="96492-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="96492-178">Atzīmēt konfigurēto formātu kā palaižamu</span><span class="sxs-lookup"><span data-stu-id="96492-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="96492-179">Lai palaistu rediģējamā formāta melnraksta versiju, tā ir jāpadara [palaižama](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="96492-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="96492-180">Pakalpojuma Finance lapas **Konfigurācijas** darbību rūts cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="96492-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="96492-181">Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Palaist iestatījumus** uz **Jā** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96492-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="96492-182">Atlasiet **Rediģēt**, lai pašreizējo lapu varētu rediģēt pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="96492-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="96492-183">Pašlaik atlasītajai **Parauga darblapas pārskata** konfigurācijai iestatiet opciju **Palaist melnrakstu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="96492-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="96492-184">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="96492-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="96492-185">Palaist formātu, lai izveidotu izvadi Word formātā</span><span class="sxs-lookup"><span data-stu-id="96492-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="96492-186">Dodieties uz **Kreditori** \> **Maksājumi** \> **Maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="96492-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="96492-187">Iepriekš ievadītajā maksājumu žurnālā atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="96492-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="96492-188">Lapā **Kreditoru maksājumi** atlasiet visas režģa rindas.</span><span class="sxs-lookup"><span data-stu-id="96492-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="96492-189">Atlasiet **Maksājuma statusu** \> **Nav**.</span><span class="sxs-lookup"><span data-stu-id="96492-189">Select **Payment status** \> **None**.</span></span>

    ![Maksājumi apstrāde lapā Kreditora maksājumi](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="96492-191">Darbību rūtī atlasiet **Ģenerēt maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="96492-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="96492-192">Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="96492-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="96492-193">Laukā **Maksājuma metode** atlasiet **Elektronisks**.</span><span class="sxs-lookup"><span data-stu-id="96492-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="96492-194">Laukā **Bankas konts** atlasiet **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="96492-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="96492-195">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96492-195">Select **OK**.</span></span>

7. <span data-ttu-id="96492-196">Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96492-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="96492-197">Izveidotā izvade tiek rādīta formātā Word, un tā ietver detalizētu informāciju par apstrādātajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="96492-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="96492-198">Analizējiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="96492-198">Analyze the generated output.</span></span>

    ![Ģenerētais rezultāts Word formātā](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="96492-200">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="96492-200">Additional resources</span></span>

- [<span data-ttu-id="96492-201">ER konfigurāciju noformēšana, lai ģenerētu atskaites Word formātā</span><span class="sxs-lookup"><span data-stu-id="96492-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="96492-202">Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER</span><span class="sxs-lookup"><span data-stu-id="96492-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]