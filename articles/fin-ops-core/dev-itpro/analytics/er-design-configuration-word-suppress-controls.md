---
title: Word satura vadīklu likvidēšana ģenerētajos pārskatos
description: Šajā tēmā paskaidrots, kā konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu pārskatus kā Microsoft Word failus, kuros satura vadīklas ir likvidētas.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562122"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="0d643-103">Word satura vadīklu likvidēšana ģenerētajos pārskatos</span><span class="sxs-lookup"><span data-stu-id="0d643-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d643-104">Lai ģenerētu pārskatus kā Microsoft Word dokumentus, ir jāizveido veidne pārskatiem kā Word dokuments.</span><span class="sxs-lookup"><span data-stu-id="0d643-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="0d643-105">Šajā veidnē jābūt Word satura vadīklām kā vietturiem datiem, kas tiks aizpildīti izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="0d643-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="0d643-106">Lai izveidoto Word dokumentu izmantotu kā veidni jūsu pārskatiem, varat [konfigurēt](er-design-configuration-word.md) jaunu [elektronisko pārskatu sniegšanas (ER)](general-electronic-reporting.md) [risinājumu](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="0d643-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="0d643-107">Risinājumam jāietver ER [konfigurācija](general-electronic-reporting.md#Configuration), kas satur ER [formāta](general-electronic-reporting.md#FormatComponentOutbound) komponentu.</span><span class="sxs-lookup"><span data-stu-id="0d643-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="0d643-108">Šis ER formāts ir jākonfigurē, lai pārskata ģenerēšanai izmantotu izveidoto veidni.</span><span class="sxs-lookup"><span data-stu-id="0d643-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="0d643-109">Programmas Dynamics 365 Finance versijā 10.0.6 un jaunākās versijās varat konfigurēt formulas savā ER formātā, lai likvidētu dažas Word satura vadīklas ģenerētajos dokumentos.</span><span class="sxs-lookup"><span data-stu-id="0d643-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="0d643-110">Turpmākās darbības paskaidro veidu, kā lietotājs, kuram ir piešķirta sistēmas administratora vai elektronisko pārskatu funkcionālā konsultanta loma, var konfigurēt ER formātu, kas ģenerē pārskatus kā Word failus un likvidē dažas satura vadīklas ģenerētajā pārskatā, kurš ir konfigurēts, izmantojot Word veidni.</span><span class="sxs-lookup"><span data-stu-id="0d643-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="0d643-111">Šīs darbības var veikt uzņēmumā GBSI.</span><span class="sxs-lookup"><span data-stu-id="0d643-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d643-112">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="0d643-112">Prerequisites</span></span>

<span data-ttu-id="0d643-113">Lai veiktu šīs darbības, vispirms veiciet darbības tālāk minētajos uzdevumu ceļvežos.</span><span class="sxs-lookup"><span data-stu-id="0d643-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="0d643-114">Izveidot konfigurāciju atskaišu ģenerēšanai formātā OPENXML</span><span class="sxs-lookup"><span data-stu-id="0d643-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="0d643-115">ER konfigurāciju atkārtota izmantošana ar Excel veidnēm, lai izveidotu pārskatus Word formātā</span><span class="sxs-lookup"><span data-stu-id="0d643-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="0d643-116">Pabeidzot šo uzdevumu ceļvežu darbības, ir sagatavoti tālāk minētie vienumi.</span><span class="sxs-lookup"><span data-stu-id="0d643-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="0d643-117">**Parauga darblapas pārskata** ER formāts, kas ir konfigurēts dokumenta ģenerēšanai Word formātā</span><span class="sxs-lookup"><span data-stu-id="0d643-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="0d643-118">[Melnraksta](general-electronic-reporting.md#component-versioning) versija **Parauga darblapas pārskata** ER formātam, kas ir atzīmēta kā **Palaižama**</span><span class="sxs-lookup"><span data-stu-id="0d643-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="0d643-119">**Elektroniska** maksājumu metode, kas ir konfigurēta, lai izmantotu **Parauga darblapas pārskata** ER formātu kreditoru maksājumu apstrādei</span><span class="sxs-lookup"><span data-stu-id="0d643-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="0d643-120">Turklāt jums ir nepieciešams šim pašam pārskatam lejupielādēt un saglabāt šādu veidni:</span><span class="sxs-lookup"><span data-stu-id="0d643-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="0d643-121">Maksājumu pārskata saistītā 2. veidne (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="0d643-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="0d643-122">Pārskatīt lejupielādēto Word veidni</span><span class="sxs-lookup"><span data-stu-id="0d643-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="0d643-123">Word darbvirsmas programmā atveriet **SampleVendPaymDocReportBounded2.docx veidnes** failu, kuru lejupielādējāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="0d643-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="0d643-124">Pārbaudiet, vai veidnes failā ir kopsavilkuma sadaļa, kurā redzamas kopējās maksājumu summas katram valūtas kodam, kas izpildīts apstrādātajos maksājumos.</span><span class="sxs-lookup"><span data-stu-id="0d643-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="0d643-125">Kopsavilkuma sadaļa atrodas atsevišķā Word dokumenta tabulā.</span><span class="sxs-lookup"><span data-stu-id="0d643-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="0d643-126">Šīs tabulas pirmajā rindā ir tabulu kolonnu virsraksti kā sadaļas virsraksts.</span><span class="sxs-lookup"><span data-stu-id="0d643-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="0d643-127">Šīs tabulas otrajā rindā ir atkārtota satura vadīkla kā sadaļas informācija.</span><span class="sxs-lookup"><span data-stu-id="0d643-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="0d643-128">Šī satura vadīkla ir kartēta uz **Pārskata** pielāgotās XML daļas lauku **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="0d643-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="0d643-129">Pamatojoties uz šo kartēšanu, satura vadīkla ir saistīta ar rediģējamā ER formāta elementu **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="0d643-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d643-130">Atkārtotā satura vadīkla ir atzīmēta ar atslēgu **SummaryLines**, kas atbilst pielāgotās XML daļas laukam, uz kuru tā ir kartēta.</span><span class="sxs-lookup"><span data-stu-id="0d643-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Word veidnes izkārtojums](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="0d643-132">Atlasiet esošo ER pārskatu konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="0d643-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="0d643-133">Tālāk minētajām darbībām jūs atkārtoti izmantosiet esošo ER konfigurāciju, ko konfigurējāt, kad izpildījāt darbības iepriekš minētajos uzdevumu ceļvežos.</span><span class="sxs-lookup"><span data-stu-id="0d643-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="0d643-134">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0d643-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0d643-135">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0d643-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="0d643-136">Lapā **Konfigurācijas**, konfigurācijas koka skatā izvērsiet **Maksājuma modelis** un pēc tam atlasiet **Parauga darbgrāmatas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0d643-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="0d643-137">Atlasiet **Veidotājs**, lai rediģētu atlasītā ER formāta melnraksta versiju.</span><span class="sxs-lookup"><span data-stu-id="0d643-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="0d643-138">Pašreizējo veidni nomainiet ar jaunu veidni</span><span class="sxs-lookup"><span data-stu-id="0d643-138">Replace the current template with the new template</span></span>

<span data-ttu-id="0d643-139">Pašlaik SampleVendPaymDocReportBounded.docx fails tiek izmantots kā veidne, lai ģenerētu izvadi Word formātā.</span><span class="sxs-lookup"><span data-stu-id="0d643-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="0d643-140">Nākamajās darbībās aizstājiet Word veidni ar jauno Word veidni — SampleVendPaymDocReportBounded2.docx —, kuru lejupielādējāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="0d643-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="0d643-141">Lapā **Formāta veidotājs** atlasiet **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="0d643-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="0d643-142">Lai noņemtu esošo veidni, lapā **Pielikumi** atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="0d643-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="0d643-143">Atlasiet **Jā**, lai apstiprinātu dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="0d643-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="0d643-144">Atlasiet **Jauns** \> **Fails**.</span><span class="sxs-lookup"><span data-stu-id="0d643-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="0d643-145">Atlasiet **Pārlūkot** un pārlūkojiet un atlasiet **SampleVendPaymDocReportBounded2.docx** failu, kuru iepriekš lejupielādējāt.</span><span class="sxs-lookup"><span data-stu-id="0d643-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="0d643-146">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0d643-146">Select **OK**.</span></span>
7. <span data-ttu-id="0d643-147">Aizveriet lapu **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="0d643-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="0d643-148">Lapas **Formāta veidotājs** laukā **Veidne** ievadiet vai atlasiet failu **SampleVendPaymDocReportBounded2.docx**.</span><span class="sxs-lookup"><span data-stu-id="0d643-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="0d643-149">Palaist formātu, lai izveidotu Word izvadi</span><span class="sxs-lookup"><span data-stu-id="0d643-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="0d643-150">Pārejiet uz sadaļu **Kreditori** \> **Maksājumi** \> **Maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0d643-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="0d643-151">Lapas **Kreditora maksājumi** cilnē **Saraksts** atlasiet visus maksājumus.</span><span class="sxs-lookup"><span data-stu-id="0d643-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="0d643-152">Atlasiet **Maksājuma statusu**\>**Nav**.</span><span class="sxs-lookup"><span data-stu-id="0d643-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="0d643-153">Atlasiet **Ģenerēt maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="0d643-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="0d643-154">Laukā **Maksājuma metode** atlasiet **Elektronisks**.</span><span class="sxs-lookup"><span data-stu-id="0d643-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="0d643-155">Laukā **Bankas konts** atlasiet **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="0d643-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="0d643-156">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0d643-156">Select **OK**.</span></span>
8. <span data-ttu-id="0d643-157">Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi** un analizējiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="0d643-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Maksājumi apstrāde lapā Kreditora maksājumi](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="0d643-159">Rezultāts ir parādīts Word formātā un satur kopsavilkuma sadaļu.</span><span class="sxs-lookup"><span data-stu-id="0d643-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="0d643-160">Konfigurēt rediģējamu formātu, lai likvidētu kopsavilkuma sadaļu</span><span class="sxs-lookup"><span data-stu-id="0d643-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="0d643-161">Ja vēlaties likvidēt kopsavilkuma sadaļu ģenerētajā dokumentā, pamatojoties uz lietotāja pieprasījumu, kurš lieto šo ER formātu, jums ir jāmodificē rediģējamais ER formāts.</span><span class="sxs-lookup"><span data-stu-id="0d643-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="0d643-162">Pārejiet uz sadaļu **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu sniegšana** un atveriet ER formāta melnraksta versiju rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="0d643-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="0d643-163">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0d643-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="0d643-164">Lapā **Konfigurācijas** konfigurācijas koka skatā izvērsiet  **Maksājuma modelis** \> **Parauga darblapas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0d643-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="0d643-165">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0d643-165">Select **Designer**.</span></span>
5. <span data-ttu-id="0d643-166">Lapā **Formāta veidotājs** izvērsiet **Word** un atlasiet **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="0d643-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="0d643-167">Cilnē **Kartēšana** pievienojiet jaunu datu avotu, lai lietotājam izpildlaikā uzdotu jautājumu, vai kopsavilkuma sadaļa būtu jālikvidē.</span><span class="sxs-lookup"><span data-stu-id="0d643-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="0d643-168">Atlasiet **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="0d643-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="0d643-169">Dialoglodziņā **Pievienot datu avotu** atlasiet **Vispārīgo\lietotāja ievades parametru**, lai atvērtu dialoglodziņu **'Lietotāja ievades parametra datu avota rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="0d643-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="0d643-170">Laukā **Nosaukums** ievadiet **uipSuppress**.</span><span class="sxs-lookup"><span data-stu-id="0d643-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="0d643-171">Laukā **Etiķete** ievadiet **Likvidēt kopsavilkuma sadaļu**.</span><span class="sxs-lookup"><span data-stu-id="0d643-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="0d643-172">Laukā **Operāciju datu veida nosaukums**, atlasiet vai ievadiet **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="0d643-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="0d643-173">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0d643-173">Select **OK**.</span></span>

7. <span data-ttu-id="0d643-174">Pievienojiet jaunu **NoYes** programmas uzskaitījuma veida datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0d643-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="0d643-175">Atlasiet **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="0d643-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="0d643-176">Dialoglodziņā **Pievienot datu avotu** atlasiet **Dynamics 365 for Operations\Uzskaitījums**, lai atvērtu dialoglodziņu **Uzskaitījuma datu avota rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="0d643-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="0d643-177">Laukā **Nosaukums** ievadiet **enumNoYes**.</span><span class="sxs-lookup"><span data-stu-id="0d643-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="0d643-178">Laukā **Etiķete** ievadiet **Likvidēt opcijas**.</span><span class="sxs-lookup"><span data-stu-id="0d643-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="0d643-179">Laukā **Operāciju datu veida nosaukums**, atlasiet vai ievadiet **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="0d643-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="0d643-180">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0d643-180">Select **OK**.</span></span>

8. <span data-ttu-id="0d643-181">Konfigurējiet formulu atlasītajam formāta elementam **SummaryLines**, lai norādītu, kad ar atlasīto formāta elementu saistītā Word satura vadīkla būtu jālikvidē.</span><span class="sxs-lookup"><span data-stu-id="0d643-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="0d643-182">Cilnes **Kartēšana** sadaļā **Noņemts** atlasiet **Rediģēt**, lai atvērtu lapu **[Formulas veidotājs](general-electronic-reporting-formula-designer.md)**.</span><span class="sxs-lookup"><span data-stu-id="0d643-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="0d643-183">Laukā **Formula** ievadiet formulu `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="0d643-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="0d643-184">Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .</span><span class="sxs-lookup"><span data-stu-id="0d643-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0d643-185">Šī formula tiks lietota ģenerētam dokumentam pēc **visu pārējo formāta elementu izpildes**.</span><span class="sxs-lookup"><span data-stu-id="0d643-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="0d643-186">Lai lietotu šo formulu, Word satura vadīkla, kas ir atzīmēta kā formāta elements, kam šī formula ir konfigurēta (šajā gadījumā **SummaryLines**) atrodas ģenerētā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="0d643-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="0d643-187">Pēc tam šī satura vadīkla tiek pilnībā noņemta kopā ar to rindu Word tabulā, kurā tā atrodas.</span><span class="sxs-lookup"><span data-stu-id="0d643-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="0d643-188">Kopsavilkuma sadaļas detalizētās informācijas rinda tiek izņemta no ģenerētā dokumenta.</span><span class="sxs-lookup"><span data-stu-id="0d643-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="0d643-189">Izstrādes laikā varat konfigurēt formulu **Noņemts** formāta elementam, kaut arī Word veidnē, kuru izmantojat, nevienai satura vadīklai, ko izmantojat, nav taga, kas atbilst formāta elementa nosaukumam, kam konfigurēts rekvizīts **Noņemts**.</span><span class="sxs-lookup"><span data-stu-id="0d643-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="0d643-190">Apstiprinot formātu izstrādes laikā, saņemsit [brīdinājumu](er-components-inspections.md#i14) par šo neatbilstību.</span><span class="sxs-lookup"><span data-stu-id="0d643-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="0d643-191">Izpildlaikā tiek izmests izņēmums, ja jūsu lietotajā Word veidnē satura vadīklai nav etiķetes, kas atbilst tā formāta elementa nosaukumam, kuram ir konfigurēts rekvizīts **Noņemts**.</span><span class="sxs-lookup"><span data-stu-id="0d643-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="0d643-192">Cilnes **Kartēšana** sadaļā **Noņemts** iestatiet opciju **Ar vecāku** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0d643-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0d643-193">Šī opcija ir jāiestata uz **Jā**, lai noņemtu visu Word tabulu kā tās rindas vecākobjektu, kura satur kopsavilkuma sadaļas informāciju.</span><span class="sxs-lookup"><span data-stu-id="0d643-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="0d643-194">Ja iestatāt šo opciju uz **Nē**, sadaļas galvenes rinda paliek ģenerētajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="0d643-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="0d643-195">Atlasiet **Saglabāt**, lai saglabātu rediģējamā formāta izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0d643-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Ģenerētā izvade Word formātā](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="0d643-197">Palaist modificēto formātu, lai izveidotu Word izvadi</span><span class="sxs-lookup"><span data-stu-id="0d643-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="0d643-198">Pārejiet uz sadaļu **Kreditori** \> **Maksājumi** \> **Maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0d643-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="0d643-199">Atlasiet izveidoto maksājumu žurnālu un pēc tam atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="0d643-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="0d643-200">Lapā **Kreditora maksājumi** atlasiet visas rindas un pēc tam atlasiet **Maksājuma statuss** \> **Nav**.</span><span class="sxs-lookup"><span data-stu-id="0d643-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="0d643-201">Atlasiet **Ģenerēt maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="0d643-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="0d643-202">Laukā **Maksājuma metode** atlasiet **Elektronisks**.</span><span class="sxs-lookup"><span data-stu-id="0d643-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="0d643-203">Laukā **Bankas konts** atlasiet **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="0d643-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="0d643-204">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0d643-204">Select **OK**.</span></span>
8. <span data-ttu-id="0d643-205">Dialoglodziņa **Elektroniskā pārskata parametri** laukā **Likvidēt kopsavilkuma sadaļu** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0d643-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="0d643-206">Atlasiet **Labi** un analizējiet ģenerēto izvades informāciju.</span><span class="sxs-lookup"><span data-stu-id="0d643-206">Select **OK**, and analyze the generated output.</span></span>

    ![Ģenerētais rezultāts Word formātā](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="0d643-208">Ņemiet vērā, ka izvade neietver kopsavilkuma sadaļu, jo tā ir likvidēta.</span><span class="sxs-lookup"><span data-stu-id="0d643-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d643-209">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0d643-209">Additional resources</span></span>

- [<span data-ttu-id="0d643-210">Izveidot konfigurāciju atskaišu ģenerēšanai formātā OPENXML</span><span class="sxs-lookup"><span data-stu-id="0d643-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="0d643-211">Jaunas ER konfigurācijas noformēšana, lai ģenerētu atskaites Word formātā</span><span class="sxs-lookup"><span data-stu-id="0d643-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="0d643-212">ER konfigurāciju atkārtota izmantošana ar Excel veidnēm, lai izveidotu pārskatus Word formātā</span><span class="sxs-lookup"><span data-stu-id="0d643-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="0d643-213">Konfigurēto ER komponentu pārbaude, lai novērstu izpildlaika problēmas</span><span class="sxs-lookup"><span data-stu-id="0d643-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]