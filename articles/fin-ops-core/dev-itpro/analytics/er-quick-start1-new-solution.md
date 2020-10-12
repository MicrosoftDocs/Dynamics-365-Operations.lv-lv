---
title: Izveidot jaunu ER risinājumu, lai izdrukātu pielāgotu pārskatu
description: Šajā tēmā skaidrots, kā noformēt elektronisko pārskatu (ER) risinājumu, lai izdrukātu pielāgotu pārskatu.
author: NickSelin
manager: AnnBe
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ede88bc1767304a86a86ec27365db9403c5a951d
ms.sourcegitcommit: 4909e55529f03310d24b7e40d52751e24d35259b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/10/2020
ms.locfileid: "3678252"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="0e459-103">Izveidot jaunu ER risinājumu, lai izdrukātu pielāgotu pārskatu</span><span class="sxs-lookup"><span data-stu-id="0e459-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0e459-104">Tālāk aprakstītajās darbībās izskaidrots, kā lietotājs sistēmas administratora, elektroniskā pārskatu izstrādātāja vai elektroniskās ziņošanas funkcionālās konsultanta lomā var konfigurēt ER struktūras parametrus, veidot jaunā ER risinājuma nepieciešamās ER konfigurācijas, lai piekļūtu konkrētā biznesa domēna datiem un izstrādātu pielāgotu pārskatu Microsoft Office formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="0e459-105">Šīs darbības var veikt uzņēmumā **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0e459-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="0e459-106">ER struktūras konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="0e459-107">Konfigurējiet ER parametrus</span><span class="sxs-lookup"><span data-stu-id="0e459-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="0e459-108">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="0e459-109">ER konfigurācijas nodrošinātāju saraksta pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0e459-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="0e459-110">Jauna ER konfigurācijas nodrošinātāja pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="0e459-111">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="0e459-112">Domēnam specifiska datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="0e459-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="0e459-113">Importēt jaunu datu modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="0e459-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="0e459-114">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="0e459-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="0e459-115">Datu modeļa nosaukšana</span><span class="sxs-lookup"><span data-stu-id="0e459-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="0e459-116">Datu modeļa lauku pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="0e459-117">Datu modeļa noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="0e459-118">Konfigurētā datu modeļa kartēšanas izveidošana</span><span class="sxs-lookup"><span data-stu-id="0e459-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="0e459-119">Jaunas modeļa kartēšanas konfigurācijas importēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="0e459-120">Jauna modeļa kartēšanas konfigurācijas izveidošana</span><span class="sxs-lookup"><span data-stu-id="0e459-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="0e459-121">Jaunu modeļa kartēšanas komponentu izveidošana</span><span class="sxs-lookup"><span data-stu-id="0e459-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="0e459-122">Datu avotu pievienošana piekļuves pieteikumu tabulām</span><span class="sxs-lookup"><span data-stu-id="0e459-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="0e459-123">Datu avotu pievienošana piekļuves pieteikumu uzskaitījumiem</span><span class="sxs-lookup"><span data-stu-id="0e459-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="0e459-124">ER etiķešu pievienošana, lai ģenerētu pārskatu noteiktā valodā</span><span class="sxs-lookup"><span data-stu-id="0e459-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="0e459-125">Datu avotu pievienošana, lai pārveidotu uzskaitījuma vērtību salīdzināšanas rezultātus teksta vērtībā</span><span class="sxs-lookup"><span data-stu-id="0e459-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="0e459-126">Datu avotu saistīšana uz datu modeļa laukiem</span><span class="sxs-lookup"><span data-stu-id="0e459-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="0e459-127">Modeļa kartēšanas noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="0e459-128">Veidnes izveide pielāgotam pārskatam</span><span class="sxs-lookup"><span data-stu-id="0e459-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="0e459-129">Formāta veidošana</span><span class="sxs-lookup"><span data-stu-id="0e459-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="0e459-130">Izstrādātā formāta konfigurācijas importēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="0e459-131">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="0e459-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="0e459-132">Pārskata veidnes importēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="0e459-133">Formāta konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="0e459-134">Pārskata nosaukuma datu saistījumu definēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="0e459-135">Modeļa datu avota pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0e459-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="0e459-136">Formāta elementu saistīšana ar datu avotu laukiem</span><span class="sxs-lookup"><span data-stu-id="0e459-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="0e459-137">Izveidoto formātu palaišana no ER</span><span class="sxs-lookup"><span data-stu-id="0e459-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="0e459-138">Izveidotā formāta noskaņošana</span><span class="sxs-lookup"><span data-stu-id="0e459-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="0e459-139">Formātu modificēšana, lai mainītu ģenerētā dokumenta nosaukumu</span><span class="sxs-lookup"><span data-stu-id="0e459-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="0e459-140">Formātu modificēšana, lai mainītu jautājumu secību</span><span class="sxs-lookup"><span data-stu-id="0e459-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="0e459-141">Modificēto formātu palaišana no ER</span><span class="sxs-lookup"><span data-stu-id="0e459-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="0e459-142">Formāta noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="0e459-143">Pieteikumu artefaktu izstrādāšana, lai izsauktu paredzēto pārskatu</span><span class="sxs-lookup"><span data-stu-id="0e459-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="0e459-144">Pirmkoda modificēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="0e459-145">Datu līguma klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="0e459-146">UI veidotāja klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="0e459-147">Datu nodrošinātāja klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="0e459-148">Etiķešu faila pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="0e459-149">Pārskata pakalpojumu klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="0e459-150">Pārskata kontrolētāja klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="0e459-151">Izvēlnes elementa pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="0e459-152">Izvēlnes krājuma pievienošana izvēlnei</span><span class="sxs-lookup"><span data-stu-id="0e459-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="0e459-153">Visual Studio projekta izveide</span><span class="sxs-lookup"><span data-stu-id="0e459-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="0e459-154">Formāta palaišana no programmas</span><span class="sxs-lookup"><span data-stu-id="0e459-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="0e459-155">Izstrādāta ER risinājuma noregulēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="0e459-156">Modeļa kartējuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="0e459-157">Datu avotu pievienošana piekļuves datu līguma objektam</span><span class="sxs-lookup"><span data-stu-id="0e459-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="0e459-158">Datu avota pievienošana, lai piekļūtu ER formāta kartēšanas ierakstiem</span><span class="sxs-lookup"><span data-stu-id="0e459-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="0e459-159">Datu avota pievienošana, lai piekļūtu tekošā ER formāta kartēšanas ierakstam</span><span class="sxs-lookup"><span data-stu-id="0e459-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="0e459-160">Tekošā ER formāta nosaukuma ievadīšana datu modelī</span><span class="sxs-lookup"><span data-stu-id="0e459-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="0e459-161">Modeļa kartēšanas noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="0e459-162">Formāta modificēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="0e459-163">Jauna formāta elementa pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="0e459-164">Pievienotā formāta elementa saistīšana</span><span class="sxs-lookup"><span data-stu-id="0e459-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="0e459-165">Formāta noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="0e459-166">Formāta palaišana no programmas</span><span class="sxs-lookup"><span data-stu-id="0e459-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="0e459-167">Formāta palaišana no ER</span><span class="sxs-lookup"><span data-stu-id="0e459-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="0e459-168">Formāta mērķa konfigurēšana ekrānā redzamajā priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="0e459-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="0e459-169">Formāta palaišana no programmas, lai to priekšskatītu kā PDF dokumentu</span><span class="sxs-lookup"><span data-stu-id="0e459-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="0e459-170">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0e459-170">Additional resources</span></span>](#References)

<span data-ttu-id="0e459-171">Šajā piemērā tiks izveidots jauns ER risinājums [Anketas](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) modulim.</span><span class="sxs-lookup"><span data-stu-id="0e459-171">In this example, you will create a new ER solution for the [Questionnaire](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) module.</span></span> <span data-ttu-id="0e459-172">Šis jaunais ER risinājums sniedz iespēju izveidot pārskatu, izmantojot Microsoft Excel darblapu kā veidni.</span><span class="sxs-lookup"><span data-stu-id="0e459-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="0e459-173">Pēc tam varat izveidot **Anketu** pārskatu Excel vai PDF formātā papildus esošo SQL Server pārskatu izveides pakalpojumu (SSRS) pārskata ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="0e459-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="0e459-174">Jauno pārskatu var arī modificēt vēlāk pēc pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="0e459-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="0e459-175">Kodēšana nav nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="0e459-175">No coding is required.</span></span>

1. <span data-ttu-id="0e459-176">Lai palaistu esošo pārskatu, dodieties uz **Anketa** \> **Dizains** \> **Anketas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Atlasot Anketu pārskata izvēlnes krājumu Anketas modulī, lai palaistu esošo SSRS pārskatu](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="0e459-178">Dialoglodziņā **Anketu pārskats** norādiet atlases kritērijus.</span><span class="sxs-lookup"><span data-stu-id="0e459-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="0e459-179">Lietojiet filtru, lai pārskats iekļautu tikai **SBCCrsExam** anketu.</span><span class="sxs-lookup"><span data-stu-id="0e459-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Dialoglodziņā Anketu pārskats norādiet atlases kritērijus](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="0e459-181">Sekojošajā attēlā parādīta SSRS pārskata ģenerētā versija **SBCCrsExam** anketai.</span><span class="sxs-lookup"><span data-stu-id="0e459-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Ģenerētais SSRS pārskats](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="0e459-183">ER struktūras konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-183">Configure the ER framework</span></span>

<span data-ttu-id="0e459-184">Kā lietotājam Elektronisko pārskatu attīstības lomā, jums ir jākonfigurē minimāls ER parametru kopums, pirms varat sākt izmantot ER struktūru, lai veidotu jaunu ER risinājumu.</span><span class="sxs-lookup"><span data-stu-id="0e459-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="0e459-185">Konfigurējiet ER parametrus</span><span class="sxs-lookup"><span data-stu-id="0e459-185">Configure ER parameters</span></span>

1. <span data-ttu-id="0e459-186">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0e459-187">IDarbvietā **Elektronisko pārskatu veidošana** atlasiet **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="0e459-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="0e459-188">Lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi** iestatiet opciju **Iespējot noformēšanas režīmu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0e459-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="0e459-189">Cilnē **Pielikumi** iestatiet šādus parametrus:</span><span class="sxs-lookup"><span data-stu-id="0e459-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="0e459-190">Iestatiet lauku **Konfigurācijas** uz **Fails** uzņēmumam **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0e459-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="0e459-191">Iestatiet **Darbu arhīvs**, **Pagaidu**, **Bāzlīnija** un **Citi** laukus uz **Fails**.</span><span class="sxs-lookup"><span data-stu-id="0e459-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="0e459-192">Papildinformāciju par ER parametriem skatiet sadaļā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e459-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="0e459-193">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="0e459-194">Katra ER konfigurācija tiek atzīmēta kā piederoša ER konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="0e459-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="0e459-195">Tāpēc, pirms sākat pievienot vai rediģēt ER konfigurācijas, jums ir jāaktivizē ER konfigurācijas nodrošinātājs **Elektroniskie pārskati** jebkurā darbvietā.</span><span class="sxs-lookup"><span data-stu-id="0e459-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="0e459-196">Tikai ER konfigurācijas īpašnieks var to rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0e459-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="0e459-197">Tāpēc, pirms ER konfigurācija var tikt rediģēta, darbvietā **Elektroniskie pārskati** ir jāaktivizē atbilstošais ER konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="0e459-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="0e459-198">ER konfigurācijas nodrošinātāju saraksta pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0e459-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="0e459-199">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0e459-200">Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.</span><span class="sxs-lookup"><span data-stu-id="0e459-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="0e459-201">Lapā **Konfigurācijas nodrošinātāji** katrai konfigurācijai ir unikāls nosaukums un URL.</span><span class="sxs-lookup"><span data-stu-id="0e459-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="0e459-202">Pārskatiet šīs lapas saturu.</span><span class="sxs-lookup"><span data-stu-id="0e459-202">Review the contents of this page.</span></span> <span data-ttu-id="0e459-203">Ja ieraksts **Litware, Inc.** (`https://www.litware.com`) jau pastāv, izlaidiet nākamo procedūru, [Jauna ER konfigurācijas nodrošinātāja pievienošana](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="0e459-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="0e459-204">Jauna ER konfigurācijas nodrošinātāja pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="0e459-205">Lapā **Konfigurācijas nodrošinātāji** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e459-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="0e459-206">Laukā **Nosaukums** ievadiet **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="0e459-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="0e459-207">Laukā **Interneta adrese** ievadiet  `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="0e459-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="0e459-208">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="0e459-209">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="0e459-210">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0e459-211">**Elektroniskā pārskata** darbvietā atlasiet **Litware, Inc.** jūsu konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="0e459-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="0e459-212">Atlasiet **Iestatīt kā aktīvu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-212">Select **Set active**.</span></span>

<span data-ttu-id="0e459-213">Papildinformāciju par ER konfigurācijas nodrošinātājiem skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0e459-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="0e459-214">Domēnam specifiska datu modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="0e459-214">Design a domain-specific data model</span></span>

<span data-ttu-id="0e459-215">Ir jāizveido jauna ER konfigurācija, kas satur [datu modeļa](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentu **Anketas** biznesa domēnam.</span><span class="sxs-lookup"><span data-stu-id="0e459-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="0e459-216">Šis datu modelis vēlāk tiks izmantots kā datu avots, noformējot ER formātu, lai ģenerētu **Anketas** pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="0e459-217">Veicot darbības, kas norādītas sadaļā [Importēt jaunu datu modeļa konfigurāciju](#ImportDataModel), jūs varat importēt nepieciešamo datu modeli no norādītā XML faila.</span><span class="sxs-lookup"><span data-stu-id="0e459-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="0e459-218">Vai arī varat veikt darbības, kas aprakstītas sadaļā [Izveidot jaunu datu modeļa konfigurāciju](#DesignDataModel), lai izveidotu šo datu modeli no jauna.</span><span class="sxs-lookup"><span data-stu-id="0e459-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="0e459-219">Importēt jaunu datu modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="0e459-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="0e459-220">Lejupielādējiet [Anketu model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) failu un saglabājiet to lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="0e459-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="0e459-221">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0e459-222">Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="0e459-223">Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="0e459-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="0e459-224">Atlasiet **Pārlūkot** un pēc tam atrodiet un atlasiet **Anketu model.version.1.xml** failu.</span><span class="sxs-lookup"><span data-stu-id="0e459-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="0e459-225">Atlasiet **Labi**, lai importētu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="0e459-226">Lai turpinātu, izlaidiet nākamo procedūru [Izveidot jaunu datu modeļa konfigurāciju](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="0e459-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="0e459-227">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="0e459-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="0e459-228">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0e459-229">Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="0e459-230">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="0e459-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="0e459-231">Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Anketas modelis**.</span><span class="sxs-lookup"><span data-stu-id="0e459-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="0e459-232">Atlasiet **Izveidot konfigurāciju**, lai izveidotu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="0e459-233">Datu modeļa nosaukšana</span><span class="sxs-lookup"><span data-stu-id="0e459-233">Name the data model</span></span>

1. <span data-ttu-id="0e459-234">Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas modelis**.</span><span class="sxs-lookup"><span data-stu-id="0e459-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="0e459-235">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0e459-235">Select **Designer**.</span></span>
3. <span data-ttu-id="0e459-236">Lapas **Datu modeļa veidotājs**, kopsavilkuma cilnē **Vispārēji**, laukā **Nosaukums** ievadiet <a name="DataModeName"></a>**Anketas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="0e459-237">Jaunu datu modeļa lauku pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-237">Add new data model fields</span></span>

1. <span data-ttu-id="0e459-238">Lapā **Datu modeļa noformētājs** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e459-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="0e459-239">Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="0e459-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="0e459-240">Atlasiet **Modeļa sakni** kā jaunā zara tipu.</span><span class="sxs-lookup"><span data-stu-id="0e459-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="0e459-241">Laikā **Nosaukums** ievadiet <a name="RootDefinitionName"></a>**Sakne**.</span><span class="sxs-lookup"><span data-stu-id="0e459-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="0e459-242">Atlasiet **Pievienot**, lai pievienotu jaunu zaru.</span><span class="sxs-lookup"><span data-stu-id="0e459-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="0e459-243">Šis saknes deskriptors tiks izmantots, lai sniegtu datus **Anketas** pārskatam.</span><span class="sxs-lookup"><span data-stu-id="0e459-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="0e459-244">Vienam datu modelim var būt vairāki deskriptori.</span><span class="sxs-lookup"><span data-stu-id="0e459-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="0e459-245">Katru deskriptoru var norādīt vienam ER formātam, lai identificētu datus, kas ir nepieciešami pārskata ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="0e459-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="0e459-246">Vēlreiz atlasiet **Jauns** nolaižamajā dialoglodziņā datu modeļa mezgla pievienošanai veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="0e459-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="0e459-247">Atlasiet **Aktīvā mezgla atvasi** kā jaunā zara tipu.</span><span class="sxs-lookup"><span data-stu-id="0e459-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="0e459-248">Laukā **Nosaukums** ievadiet **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="0e459-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="0e459-249">Laukā **Vienuma veids** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="0e459-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="0e459-250">Atlasiet **Pievienot**, lai pievienotu jaunu lauku.</span><span class="sxs-lookup"><span data-stu-id="0e459-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="0e459-251">Šis lauks ir nepieciešams, lai nodotu dotā uzņēmuma nosaukumu ER pārskatam, kas patērē šo datu modeli kā datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="0e459-252">Vēlreiz atlasiet **Jauns** nolaižamajā dialoglodziņā datu modeļa mezgla pievienošanai veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="0e459-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="0e459-253">Atlasiet **Aktīvā mezgla atvasi** kā jaunā zara tipu.</span><span class="sxs-lookup"><span data-stu-id="0e459-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="0e459-254">Laukā **Nosaukums** ievadiet **Anketa**.</span><span class="sxs-lookup"><span data-stu-id="0e459-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="0e459-255">Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="0e459-256">Atlasiet **Pievienot**, lai pievienotu jaunu lauku.</span><span class="sxs-lookup"><span data-stu-id="0e459-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="0e459-257">Šis lauks tiks izmantots, lai nodotu anketu sarakstu ER pārskatam, kas patērē šo datu modeli kā datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="0e459-258">Atlasiet **Anketas** mezglu.</span><span class="sxs-lookup"><span data-stu-id="0e459-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="0e459-259">Turpiniet pievienot vajadzīgos rediģējamo datu modeļa laukus tādā pašā veidā, līdz tiek pabeigta šāda datu modeļa struktūra.</span><span class="sxs-lookup"><span data-stu-id="0e459-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="0e459-260">Lauka ceļš</span><span class="sxs-lookup"><span data-stu-id="0e459-260">Field path</span></span>                                                    | <span data-ttu-id="0e459-261">Datu tips</span><span class="sxs-lookup"><span data-stu-id="0e459-261">Data type</span></span>   | <span data-ttu-id="0e459-262">Lauka apzīmējums/atgrieztā vērtība</span><span class="sxs-lookup"><span data-stu-id="0e459-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="0e459-263">Sakne</span><span class="sxs-lookup"><span data-stu-id="0e459-263">Root</span></span>                                                          |             | <span data-ttu-id="0e459-264">Atsauces punkts, lai pieprasītu anketas datus.</span><span class="sxs-lookup"><span data-stu-id="0e459-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="0e459-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="0e459-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="0e459-266">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-266">String</span></span>      | <span data-ttu-id="0e459-267">Pašreizējā uzņēmuma nosaukums.</span><span class="sxs-lookup"><span data-stu-id="0e459-267">The name of the current company.</span></span> |
    | <span data-ttu-id="0e459-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="0e459-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="0e459-269">Reģistrēt</span><span class="sxs-lookup"><span data-stu-id="0e459-269">Record</span></span>      | <span data-ttu-id="0e459-270">Formāta izpildes detalizēta informācija.</span><span class="sxs-lookup"><span data-stu-id="0e459-270">Format execution details.</span></span> |
    | <span data-ttu-id="0e459-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="0e459-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="0e459-272">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-272">String</span></span>      | <span data-ttu-id="0e459-273">Palaistā ER formāta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="0e459-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="0e459-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="0e459-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="0e459-275">Ierakstu saraksts</span><span class="sxs-lookup"><span data-stu-id="0e459-275">Record list</span></span> | <span data-ttu-id="0e459-276">Anketu saraksts</span><span class="sxs-lookup"><span data-stu-id="0e459-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="0e459-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="0e459-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="0e459-278">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-278">String</span></span>      | <span data-ttu-id="0e459-279">Pašreizējais anketas statuss.</span><span class="sxs-lookup"><span data-stu-id="0e459-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="0e459-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="0e459-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="0e459-281">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-281">String</span></span>      | <span data-ttu-id="0e459-282">Pašreizējais anketas kods.</span><span class="sxs-lookup"><span data-stu-id="0e459-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="0e459-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="0e459-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="0e459-284">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-284">String</span></span>      | <span data-ttu-id="0e459-285">Pašreizējais anketas apraksts.</span><span class="sxs-lookup"><span data-stu-id="0e459-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="0e459-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="0e459-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="0e459-287">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-287">String</span></span>      | <span data-ttu-id="0e459-288">Pašreizējais anketas tips.</span><span class="sxs-lookup"><span data-stu-id="0e459-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="0e459-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="0e459-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="0e459-290">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-290">String</span></span>      | <span data-ttu-id="0e459-291">Pašreizējais anketas skaitliskā kārtība.</span><span class="sxs-lookup"><span data-stu-id="0e459-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="0e459-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="0e459-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="0e459-293">Reģistrēt</span><span class="sxs-lookup"><span data-stu-id="0e459-293">Record</span></span>      | <span data-ttu-id="0e459-294">Pašreizējie anketas rezultātu parametri.</span><span class="sxs-lookup"><span data-stu-id="0e459-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="0e459-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="0e459-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="0e459-296">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-296">String</span></span>      | <span data-ttu-id="0e459-297">Pašreizējās rezultātu grupas identifikācijas kods.</span><span class="sxs-lookup"><span data-stu-id="0e459-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="0e459-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="0e459-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="0e459-299">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-299">String</span></span>      | <span data-ttu-id="0e459-300">Pašreizējais rezultātu grupas apraksts.</span><span class="sxs-lookup"><span data-stu-id="0e459-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="0e459-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="0e459-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="0e459-302">Reāls</span><span class="sxs-lookup"><span data-stu-id="0e459-302">Real</span></span>        | <span data-ttu-id="0e459-303">Maksimālais punktu skaits, ko varētu nopelnīt.</span><span class="sxs-lookup"><span data-stu-id="0e459-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="0e459-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="0e459-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="0e459-305">Ierakstu saraksts</span><span class="sxs-lookup"><span data-stu-id="0e459-305">Record list</span></span> | <span data-ttu-id="0e459-306">Pašreizējās anketas jautājumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="0e459-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="0e459-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="0e459-308">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="0e459-308">Integer</span></span>     | <span data-ttu-id="0e459-309">Pašreizējās atbilžu kolekcijas sērijas numurs.</span><span class="sxs-lookup"><span data-stu-id="0e459-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="0e459-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="0e459-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="0e459-311">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-311">String</span></span>      | <span data-ttu-id="0e459-312">Pašreizējā jautājuma identifikācijas kods.</span><span class="sxs-lookup"><span data-stu-id="0e459-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="0e459-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="0e459-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="0e459-314">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-314">String</span></span>      | <span data-ttu-id="0e459-315">Karodziņš, kas norāda, vai ir jāatbild uz pašreizējo jautājumu.</span><span class="sxs-lookup"><span data-stu-id="0e459-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="0e459-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="0e459-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="0e459-317">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-317">String</span></span>      | <span data-ttu-id="0e459-318">Karodziņš, kas norāda, vai ir jāatbild uz pašreizējo jautājumu, ir primārs.</span><span class="sxs-lookup"><span data-stu-id="0e459-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="0e459-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="0e459-320">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="0e459-320">Integer</span></span>     | <span data-ttu-id="0e459-321">Pašreizējā jautājuma sērijas numurs.</span><span class="sxs-lookup"><span data-stu-id="0e459-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="0e459-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="0e459-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="0e459-323">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-323">String</span></span>      | <span data-ttu-id="0e459-324">Pašreizējā jautājuma teksts.</span><span class="sxs-lookup"><span data-stu-id="0e459-324">The text of the current question.</span></span> |
    | <span data-ttu-id="0e459-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="0e459-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="0e459-326">Ierakstu saraksts</span><span class="sxs-lookup"><span data-stu-id="0e459-326">Record list</span></span> | <span data-ttu-id="0e459-327">Pašreizējā jautājuma atbilžu saraksts.</span><span class="sxs-lookup"><span data-stu-id="0e459-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="0e459-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="0e459-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="0e459-329">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-329">String</span></span>      | <span data-ttu-id="0e459-330">Karodziņš, kas norāda, vai pašreizējā atbilde ir pareiza.</span><span class="sxs-lookup"><span data-stu-id="0e459-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="0e459-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="0e459-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="0e459-332">Reāls</span><span class="sxs-lookup"><span data-stu-id="0e459-332">Real</span></span>        | <span data-ttu-id="0e459-333">Punkti, kas ir iegūti, kad ir atlasīta pašreizējā atbilde.</span><span class="sxs-lookup"><span data-stu-id="0e459-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="0e459-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="0e459-335">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="0e459-335">Integer</span></span>     | <span data-ttu-id="0e459-336">Pašreizējās atbildes sērijas numurs.</span><span class="sxs-lookup"><span data-stu-id="0e459-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="0e459-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="0e459-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="0e459-338">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-338">String</span></span>      | <span data-ttu-id="0e459-339">Pašreizējās atbildes teksts.</span><span class="sxs-lookup"><span data-stu-id="0e459-339">The text of the current answer.</span></span> |

    <span data-ttu-id="0e459-340">Sekojošajā attēlā ir parādīts pabeigts rediģējamais datu modelis lapā **Datu modeļu noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0e459-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Konfigurētais datu modelis ER datu modeļu noformētājā](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="0e459-342">Saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0e459-342">Save your changes.</span></span>
8. <span data-ttu-id="0e459-343">Aizveriet lapu **Datu modeļa noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0e459-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="0e459-344">Datu modeļa noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="0e459-345">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-346">Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas modelis**.</span><span class="sxs-lookup"><span data-stu-id="0e459-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="0e459-347">Kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="0e459-348">Atlasiet **Mainīt statusu** \> **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0e459-349">Šīs konfigurācijas 1. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0e459-350">1. versiju vairs nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="0e459-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="0e459-351">Šī versija satur konfigurēto datu modeli, un to var izmantot kā pamatu citām ER konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="0e459-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="0e459-352">Šīs konfigurācijas 2. versija ir izveidota un tās statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0e459-353">Varat rediģēt šo versiju, lai koriģētu **Anketas** datu modeli.</span><span class="sxs-lookup"><span data-stu-id="0e459-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Rediģējamās ER konfigurācijas versijas Konfigurāciju lapā](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="0e459-355">Lai iegūtu vairāk informācijas par versiju izveidi ER konfigurācijām, skatiet [Elektronisko pārskatu (ER) apskatu](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="0e459-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="0e459-356">Konfigurētais datu modelis ir jūsu abstrakta **Anketas** biznesa domēna pārstāvība, un tas neuztur attiecības ar artefaktiem, kas ir raksturīgi Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="0e459-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="0e459-357">Konfigurētā datu modeļa kartēšanas izveidošana</span><span class="sxs-lookup"><span data-stu-id="0e459-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="0e459-358">Kā lietotājam Elektroniskajā pārskata izstrādātāja lomā, ir jāizveido jauna ER konfigurācija, kas ietver [modeļa kartēšanas](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentu **Anketas** datu modelim.</span><span class="sxs-lookup"><span data-stu-id="0e459-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="0e459-359">Tā kā šis komponents implementē konfigurēto datu modeli Finance, tas ir saistīts ar Finance.</span><span class="sxs-lookup"><span data-stu-id="0e459-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="0e459-360">Ir jākonfigurē modeļa kartēšanas komponents, lai norādītu programmas objektus, kas jāizmanto, lai aizpildītu konfigurēto datu modeli ar programmas datiem izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="0e459-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="0e459-361">Lai izpildītu šo uzdevumu, jums jāzina par biznesa domēna **Anketa** datu struktūras ieviešanas detaļām programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="0e459-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="0e459-362">Veicot darbības, kas norādītas sekojošajā sadaļā [Importēt jaunu modeļa kartēšanas konfigurāciju](#ImportModelMapping), jūs varat importēt nepieciešamā modeļa kartēšanas konfigurāciju no norādītā XML faila.</span><span class="sxs-lookup"><span data-stu-id="0e459-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="0e459-363">Vai arī varat veikt darbības, kas aprakstītas sadaļā [Izveidot jaunu modeļa kartēšanas konfigurāciju](#CreateModelMapping), lai izveidotu šo modeļa kartēšanu no jauna.</span><span class="sxs-lookup"><span data-stu-id="0e459-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="0e459-364">Jaunas modeļa kartēšanas konfigurācijas importēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="0e459-365">Lejupielādējiet [Anketu mapping.version.1.1.xm](https://go.microsoft.com/fwlink/?linkid=851448) failu un saglabājiet to lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="0e459-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="0e459-366">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0e459-367">Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="0e459-368">Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="0e459-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="0e459-369">Atlasiet **Pārlūkot** un pēc tam atrodiet un atlasiet **Anketu mapping.version.1.1.xm** failu.</span><span class="sxs-lookup"><span data-stu-id="0e459-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="0e459-370">Atlasiet **Labi**, lai importētu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="0e459-371">Lai turpinātu, izlaidiet nākamo procedūru [Izveidot jaunu modeļa kartēšanas konfigurāciju](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="0e459-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="0e459-372">Jauna modeļa kartēšanas konfigurācijas izveidošana</span><span class="sxs-lookup"><span data-stu-id="0e459-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="0e459-373">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-374">Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas modelis**.</span><span class="sxs-lookup"><span data-stu-id="0e459-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="0e459-375">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="0e459-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="0e459-376">Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0e459-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0e459-377">Laukā **Jauns** atlasiet **Uz datu modeļa anketām balstīts modeļa kartējums**.</span><span class="sxs-lookup"><span data-stu-id="0e459-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="0e459-378">Laukā **Nosaukums** ievadiet **Anketu kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="0e459-379">Laukā **Datu modeļa definīcija** atlasiet **Saknes** definīciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="0e459-380">Atlasiet **Izveidot konfigurāciju**, lai izveidotu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="0e459-381">Jaunu modeļa kartēšanas komponentu izveidošana</span><span class="sxs-lookup"><span data-stu-id="0e459-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="0e459-382">Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="0e459-383">Atlasiet **Noformētājs**, lai atvērtu kartējumu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0e459-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="0e459-384">Atlasiet **Anketu kartēšanas** kartēšanu, kas tika automātiski pievienota **Saknes** definīcijai</span><span class="sxs-lookup"><span data-stu-id="0e459-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="0e459-385">Atlasiet **Noformētājs**, lai sāktu konfigurēt atlasīto kartējumu.</span><span class="sxs-lookup"><span data-stu-id="0e459-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="0e459-386">**Saknes** definīcijai automātiski tiek pievienota jauna kartēšana.</span><span class="sxs-lookup"><span data-stu-id="0e459-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="0e459-387">Šim kartējumam ir **Uz modeli** virziens.</span><span class="sxs-lookup"><span data-stu-id="0e459-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="0e459-388">Tāpēc šo kartējumu var izmantot, lai aizpildītu datu modeli ar nepieciešamajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="0e459-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="0e459-389">Datu avotu pievienošana piekļuves pieteikumu tabulām</span><span class="sxs-lookup"><span data-stu-id="0e459-389">Add data sources to access application tables</span></span>

<span data-ttu-id="0e459-390">Datu avoti ir jākonfigurē, lai piekļūtu programmas tabulām, kas ietver informāciju par anketu.</span><span class="sxs-lookup"><span data-stu-id="0e459-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="0e459-391">Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="0e459-392">Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu tabulai KMCollection, kur katrs ieraksts pārstāv vienu anketu:</span><span class="sxs-lookup"><span data-stu-id="0e459-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="0e459-393">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0e459-394">Dialoglodziņa laukā **Nosaukums** ievadiet **Anketa**.</span><span class="sxs-lookup"><span data-stu-id="0e459-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="0e459-395">Laukā **Tabula** ievadiet **KMCollection**.</span><span class="sxs-lookup"><span data-stu-id="0e459-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="0e459-396">Iestatiet opciju **Jautāt anketu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0e459-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="0e459-397">Tad varēsiet norādīt [filtrēšanas](../../fin-ops/get-started/advanced-filtering-query-options.md) opcijas šai tabulai sistēmas vaicājuma dialoglodziņā izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="0e459-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="0e459-398">Atlasiet **Labi**, lai pievienotu jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="0e459-399">Rūtī **Datu avota tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="0e459-400">Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu tabulai KMQuestion, kur katrs ieraksts pārstāv vienu jautājumu anketā:</span><span class="sxs-lookup"><span data-stu-id="0e459-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="0e459-401">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0e459-402">Dialoglodziņa laukā **Nosaukums** ievadiet **Jautājumu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="0e459-403">Laukā **Tabula** ievadiet **KMQuestion**.</span><span class="sxs-lookup"><span data-stu-id="0e459-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="0e459-404">Atlasiet **Labi**, lai pievienotu jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="0e459-405">Rūtī **Datu avota tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="0e459-406">Pievienojiet jaunu datu avota mēģinājumu, kas tiks izmantots, lai piekļūtu tabulai KMAnswer, kur katrs ieraksts pārstāv vienu atbildi uz jautājumu anketā:</span><span class="sxs-lookup"><span data-stu-id="0e459-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="0e459-407">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0e459-408">Laikā **Nosaukums** ievadiet **Atbilde**.</span><span class="sxs-lookup"><span data-stu-id="0e459-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="0e459-409">Laukā **Tabula** ievadiet **KMAnswer**.</span><span class="sxs-lookup"><span data-stu-id="0e459-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="0e459-410">Atlasiet **Labi**, lai pievienotu jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="0e459-411">Rūtī **Datu avota tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="0e459-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="0e459-412">Pievienojiet jaunu aprēķināto lauku, kas tiks izmantots, lai piekļūtu KMQuestionResultGroup tabulas ierakstam no katra pamata KMCollection tabulas ieraksta:</span><span class="sxs-lookup"><span data-stu-id="0e459-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="0e459-413">Atlasiet **Pievienot sakni** rūtī **Anketa**.</span><span class="sxs-lookup"><span data-stu-id="0e459-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="0e459-414">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-414">Select **Add**.</span></span>
    3. <span data-ttu-id="0e459-415">Dialoglodziņa laukā **Nosaukums** ievadiet **\$ResultGroup**.</span><span class="sxs-lookup"><span data-stu-id="0e459-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="0e459-416">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="0e459-417">[ER formulas redaktorā](general-electronic-reporting-formula-designer.md), laukā **Formula** ievadiet **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)**, lai tiktu izmantots [ceļš](er-formula-language.md#paths) no vienas uz daudzām attiecībām starp KMCollection un KMQuestionResultGroup tabulām.</span><span class="sxs-lookup"><span data-stu-id="0e459-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="0e459-418">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="0e459-419">Atlasiet **Labi**, lai pievienotu jaunu aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="0e459-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="0e459-420">Rūtī **Datu avota tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="0e459-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="0e459-421">Pievienojiet jaunu aprēķināto lauku, kas tiks izmantots, lai piekļūtu KMQuestion jautājuma ierakstiem no katra pamata KMCollectionQuestion tabulas ieraksta:</span><span class="sxs-lookup"><span data-stu-id="0e459-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="0e459-422">Atlasiet **Pievienot sakni** rūtī **Anketa**.</span><span class="sxs-lookup"><span data-stu-id="0e459-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="0e459-423">Izvērsiet **\<Relāciju** mezglu, kas satur KMCollection tabulas relāciju viens pret daudziem.</span><span class="sxs-lookup"><span data-stu-id="0e459-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="0e459-424">Atlasiet saistīto **KMCollectionQuestion** tabulu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="0e459-425">Dialoglodziņa laukā **Nosaukums** ievadiet **\$Jautājumu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="0e459-426">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="0e459-427">Formulas redaktorā laukā **Formula** ievadiet **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))**, lai atgrieztu attiecīgos jautājumu ierakstus no KMQuestion tabulas.</span><span class="sxs-lookup"><span data-stu-id="0e459-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="0e459-428">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="0e459-429">Atlasiet **Labi**, lai pievienotu jaunu aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="0e459-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="0e459-430">Rūtī **Datu avota tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="0e459-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="0e459-431">Pievienojiet jaunu aprēķināto lauku, kas tiks izmantots, lai piekļūtu KMAnswer tabulas atbilžu ierakstiem no katra pamata KMQuestion tabulas ieraksta:</span><span class="sxs-lookup"><span data-stu-id="0e459-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="0e459-432">Rūtī **Datu avoti** atlasiet **Questionnaire.\<Relations.KMCollectionQuestion.\$Question** un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="0e459-433">Dialoglodziņa laukā **Nosaukums** ievadiet **\$Answer**.</span><span class="sxs-lookup"><span data-stu-id="0e459-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="0e459-434">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="0e459-435">Formulas redaktorā laukā **Formula** ievadiet **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)**, lai atgrieztu attiecīgos jautājumu ierakstus no KMAnswer tabulas.</span><span class="sxs-lookup"><span data-stu-id="0e459-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="0e459-436">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="0e459-437">Atlasiet **Labi**, lai pievienotu jaunu aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="0e459-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="0e459-438">Rūtī **Datu avota tipi** atlasiet **Dynamics 365 for Operations\\Tabula**.</span><span class="sxs-lookup"><span data-stu-id="0e459-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="0e459-439">Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu CompanyInfo tabulas metodēm.</span><span class="sxs-lookup"><span data-stu-id="0e459-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="0e459-440">Ievērojiet, ka šīs tabulas **meklēšanas()** metode atgriež ierakstu, kas pārstāv pašreizējās Finance instances uzņēmumu, ar kuru šī kartēšana tiek izsaukta kontekstā.</span><span class="sxs-lookup"><span data-stu-id="0e459-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="0e459-441">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0e459-442">Dialoglodziņa laukā **Nosaukums** ievadiet **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="0e459-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="0e459-443">Laukā **Tabula** ievadiet **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="0e459-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="0e459-444">Atlasiet **Labi**, lai pievienotu jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="0e459-445">Datu avotu pievienošana piekļuves pieteikumu uzskaitījumiem</span><span class="sxs-lookup"><span data-stu-id="0e459-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="0e459-446">Datu avoti ir jākonfigurē, lai piekļūtu pieteikumu uzskaitījumiem un salīdzinātu to vērtības ar **Numerācijas** tipa lauku vērtībām.</span><span class="sxs-lookup"><span data-stu-id="0e459-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="0e459-447">Lai aizpildītu attiecīgos datu modeļa laukus, ir jāizmanto salīdzinājuma rezultāts.</span><span class="sxs-lookup"><span data-stu-id="0e459-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="0e459-448">Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Uzskaitījums**.</span><span class="sxs-lookup"><span data-stu-id="0e459-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="0e459-449">Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu **EnumAppNoYes** uzskaitījuma vērtībām:</span><span class="sxs-lookup"><span data-stu-id="0e459-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="0e459-450">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0e459-451">Dialoglodziņa laukā **Nosaukums** ievadiet **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="0e459-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="0e459-452">**Uzskaitījuma** laukā ievadiet **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="0e459-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="0e459-453">Atlasiet **Labi**, lai pievienotu jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="0e459-454">Rūtī **Datu avota tipi** atlasiet **Dynamics 365 for Operations\\Uzskaitījums**.</span><span class="sxs-lookup"><span data-stu-id="0e459-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="0e459-455">Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu **KMCollectionQuestionMode** uzskaitījuma vērtībām:</span><span class="sxs-lookup"><span data-stu-id="0e459-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="0e459-456">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0e459-457">Dialoglodziņa laukā **Nosaukums** ievadiet **EnumAppQuestionOrder**.</span><span class="sxs-lookup"><span data-stu-id="0e459-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="0e459-458">**Uzskaitījuma** laukā ievadiet **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="0e459-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="0e459-459">Atlasiet **Labi**, lai pievienotu jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="0e459-460">ER etiķešu pievienošana, lai ģenerētu pārskatu noteiktā valodā</span><span class="sxs-lookup"><span data-stu-id="0e459-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="0e459-461">Varat pievienot ER etiķetes, lai konfigurētu dažus datu avotus, lai atgrieztu vērtības, kas ir atkarīgas no valodas, kas definēta modeļa kartēšanas izsaukuma kontekstā.</span><span class="sxs-lookup"><span data-stu-id="0e459-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="0e459-462">Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avoti** atlasiet **Atbilde** un tad atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="0e459-463">Aktivizējiet lauku **Etiķete**.</span><span class="sxs-lookup"><span data-stu-id="0e459-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="0e459-464">Atlasiet **Tulkot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-464">Select **Translate**.</span></span>
4. <span data-ttu-id="0e459-465">Dialoglodziņā **Teksta tulkojums** veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="0e459-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0e459-466">Laukā **Etiķetes ID** ievadiet **PositiveAnswer**.</span><span class="sxs-lookup"><span data-stu-id="0e459-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="0e459-467">Laukā **Teksts noklusējuma valodā** ievadiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0e459-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="0e459-468">Atlasiet **Tulkot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="0e459-469">Laukā **Etiķetes ID** ievadiet **NegativeAnswer**.</span><span class="sxs-lookup"><span data-stu-id="0e459-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="0e459-470">Laukā **Teksts noklusējuma valodā** ievadiet **Nē**.</span><span class="sxs-lookup"><span data-stu-id="0e459-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="0e459-471">Atlasiet **Tulkot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-471">Select **Translate**.</span></span>

5. <span data-ttu-id="0e459-472">Aizveriet dialoglodziņu **Teksta tulkojums**.</span><span class="sxs-lookup"><span data-stu-id="0e459-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="0e459-473">Atlasiet **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-473">Select **Cancel**.</span></span>

![Pievienot ER etiķetes rediģējamā modeļa kartēšanai](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="0e459-475">Jūs esat ievadījis tikai noklusējuma valodas ER etiķetes.</span><span class="sxs-lookup"><span data-stu-id="0e459-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="0e459-476">Lai iegūtu informāciju par to, kā ER etiķetes var tulkot citās valodās, skatiet rakstu [Vairākvalodu pārskati](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="0e459-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="0e459-477">Datu avotu pievienošana, lai pārveidotu uzskaitījuma vērtību salīdzināšanas rezultātus teksta vērtībā</span><span class="sxs-lookup"><span data-stu-id="0e459-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="0e459-478">Tā kā ir jātransformē salīdzinājuma vērtību un teksta vērtību vairāku reižu pārveidošanas rezultāti ar dažādiem avotiem, ir ieteicams konfigurēt šo loģiku kā vienu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="0e459-479">Tomēr, lai padarītu šo datu avotu atkārtoti izmantojamu, tas ir jākonfigurē kā parametrizēts datu avots.</span><span class="sxs-lookup"><span data-stu-id="0e459-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="0e459-480">Papildu informāciju skatiet [Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="0e459-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="0e459-481">Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Vispārīgi\\Tukšs konteiners**.</span><span class="sxs-lookup"><span data-stu-id="0e459-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="0e459-482">Pievienot jaunu konteinera datu avotu:</span><span class="sxs-lookup"><span data-stu-id="0e459-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="0e459-483">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0e459-484">Dialoglodziņa laukā **Nosaukums** ievadiet **Palīgs**.</span><span class="sxs-lookup"><span data-stu-id="0e459-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="0e459-485">Atlasiet **Labi**, lai pievienotu jaunu konteinera datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="0e459-486">Rūtī **Datu avota tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="0e459-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="0e459-487">Pievienot jaunu datu avotu:</span><span class="sxs-lookup"><span data-stu-id="0e459-487">Add a new data source:</span></span>

    1. <span data-ttu-id="0e459-488">Rūtī **Datu avoti** atlasiet **Palīgs**.</span><span class="sxs-lookup"><span data-stu-id="0e459-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="0e459-489">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-489">Select **Add**.</span></span>
    3. <span data-ttu-id="0e459-490">Dialoglodziņa laukā **Nosaukums** ievadiet **NoYesEnumToString**.</span><span class="sxs-lookup"><span data-stu-id="0e459-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="0e459-491">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="0e459-492">Formulas redaktorā atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="0e459-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="0e459-493">Lai precizētu parametrus konfigurētajai izteiksmei, sekojiet šiem soļiem:</span><span class="sxs-lookup"><span data-stu-id="0e459-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="0e459-494">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e459-494">Select **New**.</span></span>
        2. <span data-ttu-id="0e459-495">Dialoglodziņa laukā **Nosaukums** ievadiet **Arguments**.</span><span class="sxs-lookup"><span data-stu-id="0e459-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="0e459-496">Laukā **Tips** atlasiet **Būla** datu tipu.</span><span class="sxs-lookup"><span data-stu-id="0e459-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="0e459-497">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-497">Select **OK**.</span></span>

    7. <span data-ttu-id="0e459-498">Laukā **Formula** ievadiet **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** lai atgrieztu attiecīgās ER etiķetes tekstu atkarībā no izpildes konteksta valodas un norādītā parametra vērtības.</span><span class="sxs-lookup"><span data-stu-id="0e459-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="0e459-499">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="0e459-500">Atlasiet **Labi**, lai pievienotu jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0e459-500">Select **OK** to add the new data source.</span></span>

![Konfigurētā modeļa kartēšana ER modeļa kartēšanas noformētājā](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="0e459-502">Datu avotu saistīšana uz datu modeļa laukiem</span><span class="sxs-lookup"><span data-stu-id="0e459-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="0e459-503">Konfigurētie datu avoti ir jāpiesaista datu modeļa laukiem, lai norādītu, kā datu modelis tiks aizpildīts ar programmas datiem izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="0e459-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="0e459-504">Lapā **Modeļa kartējuma noformētājs** rūtī **Datu modelis** atlasiet **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="0e459-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="0e459-505">Rūtī **Datu avoti** paplašiniet **CompanyInfo** un pēc tam rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="0e459-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="0e459-506">Paplašiniet **CompanyInfo.find()** mezglu, kas apzīmē CompanyInfo tabulas **find()** metodi.</span><span class="sxs-lookup"><span data-stu-id="0e459-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="0e459-507">Atlasiet **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="0e459-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="0e459-508">Atlasiet **Saistīt**, lai aizpildītu uzņēmuma nosaukumu, ko konfigurētā modeļa kartēšana izsauc izpildlaika ietvaros.</span><span class="sxs-lookup"><span data-stu-id="0e459-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="0e459-509">Atlasiet **Anketa** rūtī **Datu modelis**.</span><span class="sxs-lookup"><span data-stu-id="0e459-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="0e459-510">Rūtī **Datu avoti** atlasiet **Anketa** un tad atlasiet **Saistīt**, lai aizpildītu anketas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="0e459-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="0e459-511">Rūtī **Datu modelis** paplašiniet **Anketa** un pēc tam rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="0e459-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="0e459-512">Atlasiet **Aktīvs** rūtī **Datu modelis**.</span><span class="sxs-lookup"><span data-stu-id="0e459-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="0e459-513">Atlasiet **Rediģēt** rūtī **Datu modelis**.</span><span class="sxs-lookup"><span data-stu-id="0e459-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="0e459-514">Laukā **Formula** ievadiet **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** lai aizpildītu no teksta atkarīgu un no valodas atkarīgu rezultātu salīdzinājumā starp uzskaitījuma vērtībām.</span><span class="sxs-lookup"><span data-stu-id="0e459-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="0e459-515">Turpiniet saistīt datu avotus ar datu modeļa laukiem tādā pašā veidā, līdz tiek sasniegts šāds rezultāts.</span><span class="sxs-lookup"><span data-stu-id="0e459-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="0e459-516">Lauka ceļš</span><span class="sxs-lookup"><span data-stu-id="0e459-516">Field path</span></span>                                              | <span data-ttu-id="0e459-517">Datu tips</span><span class="sxs-lookup"><span data-stu-id="0e459-517">Data type</span></span>   | <span data-ttu-id="0e459-518">Darbība</span><span class="sxs-lookup"><span data-stu-id="0e459-518">Action</span></span> | <span data-ttu-id="0e459-519">Saistīšanas izteiksme</span><span class="sxs-lookup"><span data-stu-id="0e459-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="0e459-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="0e459-520">CompanyName</span></span>                                             | <span data-ttu-id="0e459-521">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-521">String</span></span>      | <span data-ttu-id="0e459-522">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-522">Bind</span></span>   | <span data-ttu-id="0e459-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="0e459-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="0e459-524">Anketa</span><span class="sxs-lookup"><span data-stu-id="0e459-524">Questionnaire</span></span>                                           | <span data-ttu-id="0e459-525">Ierakstu saraksts</span><span class="sxs-lookup"><span data-stu-id="0e459-525">Record list</span></span> | <span data-ttu-id="0e459-526">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-526">Bind</span></span>   | <span data-ttu-id="0e459-527">Anketa</span><span class="sxs-lookup"><span data-stu-id="0e459-527">Questionnaire</span></span> |
    | <span data-ttu-id="0e459-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="0e459-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="0e459-529">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-529">String</span></span>      | <span data-ttu-id="0e459-530">Labot</span><span class="sxs-lookup"><span data-stu-id="0e459-530">Edit</span></span>   | <span data-ttu-id="0e459-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="0e459-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="0e459-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="0e459-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="0e459-533">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-533">String</span></span>      | <span data-ttu-id="0e459-534">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-534">Bind</span></span>   | <span data-ttu-id="0e459-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="0e459-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="0e459-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="0e459-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="0e459-537">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-537">String</span></span>      | <span data-ttu-id="0e459-538">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-538">Bind</span></span>   | <span data-ttu-id="0e459-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="0e459-539">\@.Description</span></span> |
    | <span data-ttu-id="0e459-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="0e459-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="0e459-541">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-541">String</span></span>      | <span data-ttu-id="0e459-542">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-542">Bind</span></span>   | <span data-ttu-id="0e459-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="0e459-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="0e459-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="0e459-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="0e459-545">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-545">String</span></span>      | <span data-ttu-id="0e459-546">Labot</span><span class="sxs-lookup"><span data-stu-id="0e459-546">Edit</span></span>   | <span data-ttu-id="0e459-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="0e459-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="0e459-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="0e459-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="0e459-549">EnumAppQuestionOrder.Random, "Random (procentuāli anketā)",</span><span class="sxs-lookup"><span data-stu-id="0e459-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="0e459-550">EnumAppQuestionOrder.RandomGroup, "Random (procentuāli rezultāti grupās)",</span><span class="sxs-lookup"><span data-stu-id="0e459-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="0e459-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="0e459-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="0e459-552">"")</span><span class="sxs-lookup"><span data-stu-id="0e459-552">"")</span></span> |
    | <span data-ttu-id="0e459-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="0e459-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="0e459-554">Reģistrēt</span><span class="sxs-lookup"><span data-stu-id="0e459-554">Record</span></span>      |        | |
    | <span data-ttu-id="0e459-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="0e459-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="0e459-556">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-556">String</span></span>      | <span data-ttu-id="0e459-557">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-557">Bind</span></span>   | <span data-ttu-id="0e459-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="0e459-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="0e459-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="0e459-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="0e459-560">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-560">String</span></span>      | <span data-ttu-id="0e459-561">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-561">Bind</span></span>   | <span data-ttu-id="0e459-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="0e459-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="0e459-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="0e459-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="0e459-564">Reāls</span><span class="sxs-lookup"><span data-stu-id="0e459-564">Real</span></span>        | <span data-ttu-id="0e459-565">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-565">Bind</span></span>   | <span data-ttu-id="0e459-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="0e459-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="0e459-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="0e459-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="0e459-568">Ierakstu saraksts</span><span class="sxs-lookup"><span data-stu-id="0e459-568">Record list</span></span> | <span data-ttu-id="0e459-569">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-569">Bind</span></span>   | <span data-ttu-id="0e459-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="0e459-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="0e459-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="0e459-572">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="0e459-572">Integer</span></span>     | <span data-ttu-id="0e459-573">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-573">Bind</span></span>   | <span data-ttu-id="0e459-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="0e459-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="0e459-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="0e459-576">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-576">String</span></span>      | <span data-ttu-id="0e459-577">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-577">Bind</span></span>   | <span data-ttu-id="0e459-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="0e459-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="0e459-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="0e459-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="0e459-580">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-580">String</span></span>      | <span data-ttu-id="0e459-581">Labot</span><span class="sxs-lookup"><span data-stu-id="0e459-581">Edit</span></span>   | <span data-ttu-id="0e459-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="0e459-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="0e459-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="0e459-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="0e459-584">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-584">String</span></span>      | <span data-ttu-id="0e459-585">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-585">Bind</span></span>   | <span data-ttu-id="0e459-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="0e459-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="0e459-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="0e459-588">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="0e459-588">Integer</span></span>     | <span data-ttu-id="0e459-589">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-589">Bind</span></span>   | <span data-ttu-id="0e459-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="0e459-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="0e459-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="0e459-592">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-592">String</span></span>      | <span data-ttu-id="0e459-593">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-593">Bind</span></span>   | <span data-ttu-id="0e459-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="0e459-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="0e459-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="0e459-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="0e459-596">Ierakstu saraksts</span><span class="sxs-lookup"><span data-stu-id="0e459-596">Record list</span></span> | <span data-ttu-id="0e459-597">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-597">Bind</span></span>   | <span data-ttu-id="0e459-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="0e459-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="0e459-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="0e459-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="0e459-600">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-600">String</span></span>      | <span data-ttu-id="0e459-601">Labot</span><span class="sxs-lookup"><span data-stu-id="0e459-601">Edit</span></span>   | <span data-ttu-id="0e459-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="0e459-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="0e459-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="0e459-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="0e459-604">Reāls</span><span class="sxs-lookup"><span data-stu-id="0e459-604">Real</span></span>        | <span data-ttu-id="0e459-605">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-605">Bind</span></span>   | <span data-ttu-id="0e459-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="0e459-606">\@.point</span></span> |
    | <span data-ttu-id="0e459-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="0e459-608">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="0e459-608">Integer</span></span>     | <span data-ttu-id="0e459-609">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-609">Bind</span></span>   | <span data-ttu-id="0e459-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="0e459-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="0e459-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="0e459-612">Virkne</span><span class="sxs-lookup"><span data-stu-id="0e459-612">String</span></span>      | <span data-ttu-id="0e459-613">Saistīt</span><span class="sxs-lookup"><span data-stu-id="0e459-613">Bind</span></span>   | <span data-ttu-id="0e459-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="0e459-614">\@.text</span></span> |

    <span data-ttu-id="0e459-615">Sekojošajā attēlā redzama konfigurētā modeļa kartēšanas pēdējais stāvoklis **Modeļa kartēšanas veidotāja** lapā.</span><span class="sxs-lookup"><span data-stu-id="0e459-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Pilnībā konfigurētā modeļa kartēšana ER modeļa kartēšanas noformētājā](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="0e459-617">Saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0e459-617">Save your changes.</span></span>
8. <span data-ttu-id="0e459-618">Aizveriet lapu **Modeļa kartējuma noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0e459-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="0e459-619">Modeļa kartēšanas noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="0e459-620">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-621">Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="0e459-622">Kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="0e459-623">Atlasiet **Mainīt statusu** \> **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0e459-624">Šīs konfigurācijas 1.1. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0e459-625">1.1. versiju vairs nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="0e459-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="0e459-626">Šī versija satur konfigurēto modeļa kartēšanu, un to var izmantot kā pamatu citām ER konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="0e459-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="0e459-627">Šīs konfigurācijas 1.2. versija ir izveidota un tās statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0e459-628">Varat rediģēt šo versiju, lai koriģētu **Anketas kartēšanas** konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Rediģējamās ER konfigurācijas versijas Konfigurāciju lapā](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="0e459-630">Konfigurētā modeļa kartēšana ir jūsu Finance specifiska abstraktā datu modeļa implementēšana, kas pārstāv **Anketas** biznesa domēnu.</span><span class="sxs-lookup"><span data-stu-id="0e459-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="0e459-631">Veidnes izveide pielāgotam pārskatam</span><span class="sxs-lookup"><span data-stu-id="0e459-631">Design a template for a custom report</span></span>

<span data-ttu-id="0e459-632">EP struktūra izmanto iepriekš definētas veidnes, lai ģenerētu pārskatus Microsoft Office formātos (Excel darbgrāmatas vai Word dokumentus).</span><span class="sxs-lookup"><span data-stu-id="0e459-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="0e459-633">Kamēr tiek ģenerēts pieprasītais pārskats, veidne tiek aizpildīta ar nepieciešamajiem datiem atbilstoši konfigurētajām darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="0e459-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="0e459-634">Tāpēc vispirms ir jāizveido jūsu pielāgotā pārskata veidne.</span><span class="sxs-lookup"><span data-stu-id="0e459-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="0e459-635">Šī veidne ir jāveido kā Excel darbgrāmata, kuras struktūra ir pielāgota pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="0e459-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="0e459-636">Jums jāpiešķir nosaukums katram Excel vienumam, ko plānojat aizpildīt ar nepieciešamajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="0e459-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="0e459-637">Lejupielādējiet [Anketu report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) failu un saglabājiet to lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="0e459-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="0e459-638">Atveriet failu programmā Excel un pārskatiet darbgrāmatas struktūru.</span><span class="sxs-lookup"><span data-stu-id="0e459-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="0e459-639">Kā redzams sekojošajā attēlā, lejupielādētā veidne ir izstrādāta, lai izdrukātu norādītās anketas, kas sniedz anketas jautājumus kopā ar atbilstošajām atbildēm.</span><span class="sxs-lookup"><span data-stu-id="0e459-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Excel veidne, lai izdrukātu norādītās anketas](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="0e459-641">Lai aizpildītu anketu detaļas, šai veidnei ir pievienoti Excel nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="0e459-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="0e459-642">Varat izmantot Nosaukumu pārvaldnieku, lai pārskatītu Excel nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="0e459-642">You can use Name Manager to review the Excel names.</span></span>

![Izmantot Nosaukumu pārvaldnieku, lai pārskatītu Excel nosaukumus norādītajā Excel veidnē](./media/er-quick-start1-template-names.png)

<span data-ttu-id="0e459-644">Angļu valodas pārskata etiķetes ir pievienotas kā fiksēts teksts.</span><span class="sxs-lookup"><span data-stu-id="0e459-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="0e459-645">Varat aizstāt pārskata etiķetes ar jaunajiem Excel nosaukumiem, kas aizpilda etiķetes ar no valodas atkarīgu tekstu, izmantojot ER formāta [etiķetes](#AddMmLabels), kā tas tika paveikts valodu pārdomātām izteiksmēm konfigurētajā modeļa kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="0e459-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="0e459-646">Šajā gadījumā ER etiķetes ir jāpievieno rediģējamā ER formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="0e459-647">Kā redzams sekojošajā attēlā, pielāgotas atskaites galvene ir norādīta, lai iespējotu Excel veikt lapošanu.</span><span class="sxs-lookup"><span data-stu-id="0e459-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Pielāgots pārskata virsraksts norādītajā Excel veidnē](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="0e459-649">Formāta veidošana</span><span class="sxs-lookup"><span data-stu-id="0e459-649">Design a format</span></span>

<span data-ttu-id="0e459-650">Kā lietotājs Elektroniskās ziņošanas funkcionālā konsultanta lomā jums ir jāizveido jauna ER konfigurācija, kas ietver [formāta](general-electronic-reporting.md#FormatComponentOutbound) komponentu.</span><span class="sxs-lookup"><span data-stu-id="0e459-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="0e459-651">Ir jākonfigurē formāta komponents, lai norādītu, kā pārskata veidne tiks aizpildīta ar nepieciešamajiem datiem izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="0e459-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="0e459-652">Veicot darbības, kas norādītas sadaļā [Importēt izveidotā formāta konfigurāciju](#FormatImport), jūs varat importēt nepieciešamo formātu no norādītā XML faila.</span><span class="sxs-lookup"><span data-stu-id="0e459-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="0e459-653">Vai arī varat veikt darbības, kas aprakstītas sadaļā [Izveidot jaunu formāta konfigurāciju](#FormatCreate), lai izveidotu šo formātu no jauna.</span><span class="sxs-lookup"><span data-stu-id="0e459-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="0e459-654">Izstrādātā formāta konfigurācijas importēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="0e459-655">Lejupielādējiet [Anketu format.version.1.1.xm](https://go.microsoft.com/fwlink/?linkid=851448) failu un saglabājiet to lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="0e459-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="0e459-656">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0e459-657">Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="0e459-658">Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="0e459-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="0e459-659">Atlasiet **Pārlūkot** un pēc tam atrodiet un atlasiet **Anketu format.version.1.1.xm** failu.</span><span class="sxs-lookup"><span data-stu-id="0e459-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="0e459-660">Atlasiet **Labi**, lai importētu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="0e459-661">Lai turpinātu, izlaidiet nākamo procedūru [Izveidot jaunu formāta konfigurāciju](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="0e459-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="0e459-662">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="0e459-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="0e459-663">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-664">Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas modelis**.</span><span class="sxs-lookup"><span data-stu-id="0e459-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="0e459-665">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="0e459-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="0e459-666">Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0e459-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0e459-667">Laukā **Jauns** atlasiet **Uz datu modeļa anketām balstīts formāts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="0e459-668">Laukā **Nosaukums** ievadiet **Anketu pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="0e459-669">Laukā **Datu modeļa versija** atlasiet **1**.</span><span class="sxs-lookup"><span data-stu-id="0e459-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="0e459-670">Ja jūs atlasāt noteiktu pamatdatu modeļa versiju, atbilstošā datu modeļa sistēmas struktūra tiks parādīta kā **Modeļa** datu avota struktūra izveidotajā formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="0e459-671">Jūs varat atstāt šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="0e459-671">You can leave this field blank.</span></span> <span data-ttu-id="0e459-672">Šādā gadījumā datu modeļa **Melnraksta** versijas struktūra tiks attēlota kā **Modeļa** datu avota struktūra izveidotajā formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="0e459-673">Pēc tam varat koriģēt modeli un uzreiz redzēt šos pielāgojumus jūsu formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="0e459-674">Šī pieeja varētu uzlabot ER risinājuma dizaina efektivitāti, konfigurējot datu modeli, modeļa kartēšanu un formātu vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="0e459-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="0e459-675">Ja atlasāt noteiktu pamatdatu modeļa versiju, varat vēlāk pārslēgt to uz **Melnraksta** versiju.</span><span class="sxs-lookup"><span data-stu-id="0e459-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="0e459-676">Laukā **Datu modeļa definīcija** atlasiet **Saknes** definīciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="0e459-677">Atlasiet **Izveidot konfigurāciju**, lai izveidotu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="0e459-678">Pārskata veidnes importēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-678">Import a report template</span></span>

1. <span data-ttu-id="0e459-679">Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="0e459-680">Atlasiet **Noformētājs**, lai sāktu pielāgotā formāta konfigurēšanu.</span><span class="sxs-lookup"><span data-stu-id="0e459-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="0e459-681">Lapā **Formāta noformētājs**, darbību rūtī atlasiet **Importēt** \> **Importēt no Excel**.</span><span class="sxs-lookup"><span data-stu-id="0e459-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="0e459-682">NDialoglodziņā veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="0e459-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0e459-683">Atlasiet **Pievienot veidni**.</span><span class="sxs-lookup"><span data-stu-id="0e459-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="0e459-684">Meklējiet un atlasiet lokāli saglabāto **Anketu pārskata template.xslx** failu un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="0e459-685">Atlasiet **Labi**, lai importētu veidni.</span><span class="sxs-lookup"><span data-stu-id="0e459-685">Select **OK** to import the template.</span></span>

    ![Pārskata veidnes importēšana](./media/er-quick-start1-template-import.png)

<span data-ttu-id="0e459-687">**Excel\\File** formāta elements tiek automātiski pievienots rediģējamam formātam kā saknes elements.</span><span class="sxs-lookup"><span data-stu-id="0e459-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="0e459-688">Turklāt **Excel\\Range** formāta elements vai **Excel\\Cell** formāta elements tiek automātiski pievienots katram importētās veidnes atpazītajam Excel nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="0e459-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="0e459-689">**Excel\\Header** formāts, kas ietver ligzdotu **Virknes** elementu, tiek automātiski pievienots, lai atspoguļotu importētās veidnes virsraksta iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="0e459-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Formatēt struktūru, kas ietver automātiski pievienotos elementus ER operāciju rīkā](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="0e459-691">Formāta konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-691">Configure a format</span></span>

1. <span data-ttu-id="0e459-692">Lapā **Formāta veidotājs** formatēšanas kokā atlasiet **Excel** saknes elementu.</span><span class="sxs-lookup"><span data-stu-id="0e459-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="0e459-693">Cilnē **Formāts**, kas atrodas lapas labajā pusē, laukā **Nosaukums** ievadiet <a name="AddFormatRootElement"></a>**Pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="0e459-694">Laukā **Valodas izvēle** atlasiet **Lietotāja preference**, lai palaistu pārskatu lietotāja vēlamajā valodā.</span><span class="sxs-lookup"><span data-stu-id="0e459-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="0e459-695">Laukā **Kultūras izvēle** atlasiet **Lietotāja preference**, lai palaistu pārskatu lietotāja vēlamajā kultūrā.</span><span class="sxs-lookup"><span data-stu-id="0e459-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="0e459-696">Informāciju par to, kā noteikt valodas un kultūras kontekstu ER procesam, skatiet šeit: [Vairākvalodu pārskatu noformēšana](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="0e459-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Valodas un kultūras iestatījumu konfigurēšana plānotajam pārskatam ER operāciju veidotājā](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="0e459-698">Formatēšanas kokā izvērsiet saknes mezglu un pēc tam atlasiet **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="0e459-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="0e459-699">Cilnē **Formāts** laukā **Replicēšanas virziens** atlasiet **Nav replikācijas**, jo nav paredzēts, ka vienai anketai ir vairākas rezultātu grupas.</span><span class="sxs-lookup"><span data-stu-id="0e459-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Definēt replicēšanas virzienu diapazona formāta elementiem, kas atrodas ER operāciju veidotājā](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="0e459-701">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="0e459-702">Pārskata nosaukuma datu saistījumu definēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-702">Define the data binding for a report title</span></span>

<span data-ttu-id="0e459-703">Ir jānorāda datu saistījums formāta elementam, kas tiek izmantots, lai aizpildītu ģenerētā pārskata nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0e459-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="0e459-704">Lapas **Formāta noformētājs** labās puses cilnē **Kartēšana** atlasiet **Report\\ReportTitle** elementu.</span><span class="sxs-lookup"><span data-stu-id="0e459-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="0e459-705">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="0e459-706">Formulas redaktorā atlasiet **Tulkot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="0e459-707">Dialoglodziņā **Teksta tulkojums** veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="0e459-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0e459-708">Laukā **Etiķetes ID** ievadiet **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="0e459-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="0e459-709">Laukā **Teksts noklusējuma valodā** ievadiet **Aptaujas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="0e459-710">Atlasiet **Tulkot** un pēc tam **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="0e459-711">Atlasiet **Tulkot**, lai aizvērtu **Teksta tulkojuma** dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0e459-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="0e459-712">Aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-712">Close the formula editor.</span></span>

    ![Saistījuma konfigurēšana, lai aizpildītu ģenerētā pārskata nosaukumu](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="0e459-714">Varat izmantot šo metodi, lai visas pārējās pašreizējās veidnes etiķetes būtu atkarīgas no valodas.</span><span class="sxs-lookup"><span data-stu-id="0e459-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="0e459-715">Lai iegūtu informāciju par to, kā vienas ER konfigurācijas pievienotās etiķetes var tulkot visās atbalstītajās valodās, skatiet rakstu [Daudzvalodu pārskatu izveide](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="0e459-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="0e459-716">Modeļa datu avota pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0e459-716">Review model data source</span></span>

1. <span data-ttu-id="0e459-717">Lapā **Formāta veidotājs** cilnē **Kartēšana** atlasiet <a name="ModelDSName"></a>**modeļa** datu avotu, kas apzīmē šī ER formāta pamata datu modeli.</span><span class="sxs-lookup"><span data-stu-id="0e459-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="0e459-718">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-718">Select **Edit**.</span></span>
3. <span data-ttu-id="0e459-719">Pārskatiet informāciju dialoglodziņā **Datu avota rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="0e459-720">Šis datu avots pārstāv **Anketu** datu modeļa komponenta 1. versiju, kas atrodas **Anketu modeļa** ER konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="0e459-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Rekvizīti par modeļa datu avotu ER operāciju noformētājā](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="0e459-722">Formāta elementu saistīšana ar datu avotu laukiem</span><span class="sxs-lookup"><span data-stu-id="0e459-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="0e459-723">Lai norādītu, kā tiek aizpildīta veidne izpildlaikā, ir jāpiesaista katrs formāta elements, kas ir saistīts ar atbilstošu Excel nosaukumu atsevišķam šī formāta datu avota laukam.</span><span class="sxs-lookup"><span data-stu-id="0e459-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="0e459-724">Lapā **Formāta veidotājs** formatēšanas kokā atlasiet **Report\\CompanyName** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="0e459-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="0e459-725">Cilnē **Kartēšana** atlasiet **model.CompanyName** **Virknes** tipa datu avota lauku.</span><span class="sxs-lookup"><span data-stu-id="0e459-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="0e459-726">Atlasiet **Saistīt**, lai ievadītu uzņēmuma nosaukumu veidnē.</span><span class="sxs-lookup"><span data-stu-id="0e459-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="0e459-727">Formāta kokā atlasiet **Report\\Questionnaire** elementu.</span><span class="sxs-lookup"><span data-stu-id="0e459-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="0e459-728">Cilnē **Kartēšana** atlasiet **model.Questionnaire** **Ieraksta saraksta** tipa datu avota lauku.</span><span class="sxs-lookup"><span data-stu-id="0e459-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="0e459-729">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-729">Select **Bind**.</span></span>
7. <span data-ttu-id="0e459-730">Atlasiet **Rādīt detaļas**, lai skatītu plašāku informāciju par formāta elementiem.</span><span class="sxs-lookup"><span data-stu-id="0e459-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="0e459-731">**Anketas** diapazona formāta elements ir konfigurēts kā vertikāli replicēts.</span><span class="sxs-lookup"><span data-stu-id="0e459-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="0e459-732">Kad tas ir piesaistīts datu avotam ar **Ierakstu saraksta** tipu, atbilstošais Excel veidnes **Anketu** diapazons tiek atkārtots katram saistītā datu avota ierakstam.</span><span class="sxs-lookup"><span data-stu-id="0e459-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Anketu diapazona formāta elementu saistīšana ar atbilstošajiem Ierakstu saraksta datu avotiem ER operāciju veidotājā](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="0e459-734">Tā kā Excel veidnes **Anketu** diapazons ir definēts no 5. līdz 14. rindai, šīs rindas tiek atkārtotas katrai pārskatā iekļautajai anketai.</span><span class="sxs-lookup"><span data-stu-id="0e459-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Rindas Excel veidnē, kas tiks atkārtotas ģenerētajā pārskatā katram Ierakstu saraksta datu avotu ierakstam](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="0e459-736">Konfigurējiet līdzīgus saistījumus atlikušajiem formāta elementiem, kā aprakstīts šajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="0e459-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0e459-737">Šajā tabulā informācija kolonnā "Datu avota ceļš" tiek pieņemts, ka [relatīvā ceļa](relative-path-data-bindings-er-models-format.md) ER funkcija ir ieslēgta.</span><span class="sxs-lookup"><span data-stu-id="0e459-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="0e459-738">Formatēt elementa ceļu</span><span class="sxs-lookup"><span data-stu-id="0e459-738">Format element path</span></span>                                      | <span data-ttu-id="0e459-739">Datu avota ceļš</span><span class="sxs-lookup"><span data-stu-id="0e459-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="0e459-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="0e459-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="0e459-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="0e459-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="0e459-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="0e459-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="0e459-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="0e459-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="0e459-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="0e459-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="0e459-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="0e459-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="0e459-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="0e459-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="0e459-747">**\@.Active**, kur **\@** ir **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="0e459-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="0e459-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="0e459-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="0e459-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="0e459-749">**\@.Code**</span></span> |
    | <span data-ttu-id="0e459-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="0e459-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="0e459-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="0e459-751">**\@.Description**</span></span> |
    | <span data-ttu-id="0e459-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="0e459-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="0e459-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="0e459-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="0e459-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="0e459-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="0e459-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="0e459-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="0e459-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="0e459-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="0e459-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="0e459-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="0e459-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="0e459-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="0e459-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="0e459-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="0e459-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="0e459-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="0e459-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="0e459-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="0e459-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="0e459-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="0e459-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="0e459-763">**\@.Question**</span></span> |
    | <span data-ttu-id="0e459-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="0e459-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="0e459-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="0e459-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="0e459-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="0e459-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="0e459-767">**\@.Id**</span></span> |
    | <span data-ttu-id="0e459-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="0e459-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="0e459-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="0e459-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="0e459-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="0e459-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="0e459-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="0e459-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="0e459-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0e459-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="0e459-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0e459-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="0e459-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="0e459-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="0e459-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="0e459-775">**\@.Text**</span></span> |
    | <span data-ttu-id="0e459-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="0e459-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="0e459-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="0e459-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="0e459-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="0e459-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="0e459-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="0e459-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="0e459-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="0e459-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="0e459-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="0e459-781">**\@.Points**</span></span> |
    | <span data-ttu-id="0e459-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="0e459-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="0e459-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="0e459-783">**\@.Text**</span></span> |

9. <span data-ttu-id="0e459-784">Pēc pabeigšanas atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="0e459-785">Sekojošajā attēlā redzama konfigurētās datu saistīšanas pēdējais stāvoklis **Formāta veidotāja** lapā.</span><span class="sxs-lookup"><span data-stu-id="0e459-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Konfigurētie datu saistījumi ER operāciju noformētājā](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="0e459-787">Visu norādīto datu avotu un saistījumu kolekcija attēlo konfigurētā formāta kartējuma komponentu.</span><span class="sxs-lookup"><span data-stu-id="0e459-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="0e459-788">Šī formāta kartēšana tiek izsaukta, palaižot konfigurēto formātu pārskata ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="0e459-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="0e459-789">Izveidoto formātu palaišana no ER</span><span class="sxs-lookup"><span data-stu-id="0e459-789">Run a designed format from ER</span></span>

<span data-ttu-id="0e459-790">Tagad ir iespējams palaist noformētu formātu testēšanas nolūkiem no **Konfigurāciju** lapas.</span><span class="sxs-lookup"><span data-stu-id="0e459-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="0e459-791">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-792">Lapā **Konfigurācija**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="0e459-793">Izvēlieties **Noformētāju** formāta versijai ar statusu **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="0e459-794">Lapā **Formāta veidotājs** atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="0e459-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="0e459-795">Dialoglodziņā **ER parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.</span><span class="sxs-lookup"><span data-stu-id="0e459-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="0e459-796">Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="0e459-797">Atlasiet **Labi**, lai palaistu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="0e459-798">Pārskatiet ģenerēto pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-798">Review the generated report.</span></span>

<span data-ttu-id="0e459-799">Pēc [noklusējuma](electronic-reporting-destinations.md#default-behavior) ģenerētais pārskats tiek piegādāts kā Excel fails, ko var lejupielādēt.</span><span class="sxs-lookup"><span data-stu-id="0e459-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="0e459-800">Šajā ilustrācijā ir parādītas divas ģenerētā pārskata lapas Excel formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Ģenerētā pārskata piemērs Excel formātā, 1. lpp.](./media/er-quick-start1-report1a.png)

![Ģenerētā pārskata piemērs Excel formātā, 2. lpp.](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="0e459-803">Izveidotā formāta noskaņošana</span><span class="sxs-lookup"><span data-stu-id="0e459-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="0e459-804">Formātu modificēšana, lai mainītu ģenerētā dokumenta nosaukumu</span><span class="sxs-lookup"><span data-stu-id="0e459-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="0e459-805">Pēc noklusējuma ģenerētais dokuments tiek nosaukts, izmantojot pašreizējā lietotāja aizstājvārdu.</span><span class="sxs-lookup"><span data-stu-id="0e459-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="0e459-806">Modificējot formātu, varat mainīt šo darbību tā, lai ģenerētais dokuments tiktu nosaukts, pamatojoties uz jūsu pielāgoto loģiku.</span><span class="sxs-lookup"><span data-stu-id="0e459-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="0e459-807">Piemēram, ģenerētā dokumenta nosaukums var pamatoties uz pašreizējo sesijas datumu un laiku, kā arī uz pārskata nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0e459-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="0e459-808">Lapā **Formāta veidotājs** atlasiet saknes krājumu **Pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="0e459-809">Cilnē **Kartēšana** atlasiet **Rediģēt faila nosaukumu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="0e459-810">Laukā **Formula** ievadiet **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="0e459-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="0e459-811">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="0e459-812">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="0e459-813">Formātu modificēšana, lai mainītu jautājumu secību</span><span class="sxs-lookup"><span data-stu-id="0e459-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="0e459-814">Jautājumi nav pareizi sakārtoti ģenerētajā pārskatā.</span><span class="sxs-lookup"><span data-stu-id="0e459-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="0e459-815">Varat mainīt secību, modificējot formātu.</span><span class="sxs-lookup"><span data-stu-id="0e459-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="0e459-816">Lapā **Formāta veidotājs** atlasiet saknes krājumu **Pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="0e459-817">Cilnē **Kartēšana** formatēšanas kokā izvērsiet **Pārskats\\Aptauja\\Jautājums**.</span><span class="sxs-lookup"><span data-stu-id="0e459-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Diapazona tipa jautājuma formāta elements ER operāciju veidotājā](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="0e459-819">Cilnē **Kartēšana** atlasiet **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="0e459-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="0e459-820">Atlasiet **Pievienot** \> **Funkcijas\\Aprēķinātais lauks** un pēc tam laukā **Nosaukums** ievadiet **OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="0e459-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="0e459-821">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="0e459-822">Formulas redaktorā laukā **Formula** ievadiet **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)**, lai numurētu pašreizējās anketas jautājumu sarakstu pēc secības pasūtījuma numura.</span><span class="sxs-lookup"><span data-stu-id="0e459-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="0e459-823">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="0e459-824">Atlasiet **Labi**, lai pabeigtu jauna aprēķinātā lauka ievadi.</span><span class="sxs-lookup"><span data-stu-id="0e459-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="0e459-825">Cilnē **Kartēšana** atlasiet **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="0e459-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="0e459-826">Formatēšanas kokā atlasiet **Excel\\Aptauja\\Jautājums**.</span><span class="sxs-lookup"><span data-stu-id="0e459-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="0e459-827">Atlasiet **Saistīt** un tad apstipriniet, ka pašreizējais **model.Questionnaire.Questions** ceļš ir aizstāts ar jauno **model.Questionnaire.OrderedQuestions** ceļu visos ligzdoto elementu saistījumos.</span><span class="sxs-lookup"><span data-stu-id="0e459-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="0e459-828">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-828">Select **Save**.</span></span>

![Jautājuma formāta elementu saistīšana ar konfigurēto OrderedQuestions datu avotu, kas atrodas ER operāciju veidotājā](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="0e459-830">Modificēto formātu palaišana no ER</span><span class="sxs-lookup"><span data-stu-id="0e459-830">Run a modified format from ER</span></span>

<span data-ttu-id="0e459-831">Tagad varat izmantot modificēto formātu testēšanas nolūkiem no ER struktūras.</span><span class="sxs-lookup"><span data-stu-id="0e459-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="0e459-832">Lapā **Formāta veidotājs** atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="0e459-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="0e459-833">Dialoglodziņā **ER parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.</span><span class="sxs-lookup"><span data-stu-id="0e459-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="0e459-834">Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="0e459-835">Atlasiet **Labi**, lai palaistu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="0e459-836">Pārskatiet ģenerēto pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-836">Review the generated report.</span></span>

<span data-ttu-id="0e459-837">Sekojošajā attēlā redzams ģenerētais pārskats Excel formātā, kur jautājumi ir pareizi sakārtoti.</span><span class="sxs-lookup"><span data-stu-id="0e459-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Ģenerētais pārskats Excel formātā, kur ir pareizi sakārtoti jautājumi](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="0e459-839">Formāta noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-839">Complete the format design</span></span>

1. <span data-ttu-id="0e459-840">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-841">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="0e459-842">Kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="0e459-843">Atlasiet **Mainīt statusu** \> **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0e459-844">Šīs konfigurācijas 1.1. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0e459-845">1.1. versiju vairs nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="0e459-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="0e459-846">Šajā versijā ir konfigurēts formāts, un to var izmantot, lai izdrukātu jūsu pielāgoto pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="0e459-847">Šīs konfigurācijas 1.2. versija ir izveidota un tās statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0e459-848">Varat rediģēt šo versiju, lai koriģētu jūsu **Anketas** pārskata formātu.</span><span class="sxs-lookup"><span data-stu-id="0e459-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Rediģējamās ER konfigurācijas versijas Konfigurāciju lapā](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="0e459-850">Konfigurētais formāts ir jūsu **Anketas** pārskata noformējums, un tas nesatur attiecības ar Finance saistītiem artefaktiem.</span><span class="sxs-lookup"><span data-stu-id="0e459-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="0e459-851">Pieteikumu artefaktu izstrādāšana, lai izsauktu paredzēto pārskatu</span><span class="sxs-lookup"><span data-stu-id="0e459-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="0e459-852">Kā lietotājam lomā Sistēmas administrators, jums ir jāizstrādā jauna loģika, lai konfigurēto ER formātu varētu izsaukt no lietojumprogrammas lietotāja interfeisa (UI), lai ģenerētu pielāgoto pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="0e459-853">Pašlaik ER nepiedāvā nekādu iespēju konfigurēt šāda veida loģiku.</span><span class="sxs-lookup"><span data-stu-id="0e459-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="0e459-854">Tāpēc ir nepieciešams atsevišķs tehniskais darbs.</span><span class="sxs-lookup"><span data-stu-id="0e459-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="0e459-855">Lai attīstītu jaunu loģiku, jums jāizvieto topoloģija, kas atbalsta pastāvīgu būvēšanu.</span><span class="sxs-lookup"><span data-stu-id="0e459-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="0e459-856">Papildinformāciju skatiet tēmā [Tādu topoloģiju izvietošana, kuras atbalsta pastāvīgu būvēšanu un testu automatizēšanu](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="0e459-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="0e459-857">Jums jābūt arī piekļuvei šīs topoloģijas izstrādes videi.</span><span class="sxs-lookup"><span data-stu-id="0e459-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="0e459-858">Papildinformāciju par pieejamo ER API skatiet sadaļā [ER struktūras API](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="0e459-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="0e459-859">Pirmkoda modificēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="0e459-860">Datu līguma klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-860">Add a data contract class</span></span>

<span data-ttu-id="0e459-861">Pievienojiet jaunu **QuestionnairesErReportContract** klasi savam Microsoft Visual Studio projektam un ierakstiet kodu, kas norāda datu līgumu, kas jāizmanto, lai darbinātu konfigurēto ER formātu.</span><span class="sxs-lookup"><span data-stu-id="0e459-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="0e459-862">UI veidotāja klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-862">Add a UI builder class</span></span>

<span data-ttu-id="0e459-863">Pievienojiet jaunu **QuestionnairesErReportUIBuilder** klasi jūsu Visual Studio projektam un ierakstiet kodu, lai ģenerētu izpildlaika dialoglodziņu, kas tiks izmantots, lai uzmeklētu ER formāta kartējuma ID, kas ir jāpalaiž.</span><span class="sxs-lookup"><span data-stu-id="0e459-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="0e459-864">Norādītais kods meklē tikai ER formātus, kas satur **Datu modeļa** tipa datu avotu, kas attiecas uz **[Anketu](#DataModeName)** datu modeli, izmantojot **[Saknes](#RootDefinitionName)** definīciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="0e459-865">Varat arī izmantot ER integrācijas punktus, lai filtrētu ER formātus.</span><span class="sxs-lookup"><span data-stu-id="0e459-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="0e459-866">Plašāku informāciju skatiet [API, lai parādītu formāta kartēšanas uzmeklēšanu](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="0e459-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="0e459-867">Datu nodrošinātāja klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-867">Add a data provider class</span></span>

<span data-ttu-id="0e459-868">Pievienojiet jaunu **QuestionnairesErReportDP** klasi savam Microsoft Visual Studio projektam un ierakstiet kodu, kas iepazīstina datu nodrošinātāju, kas jāizmanto, lai darbinātu konfigurēto ER formātu.</span><span class="sxs-lookup"><span data-stu-id="0e459-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="0e459-869">Norādītais kods ietver tikai datu līgumu šim datu nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="0e459-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="0e459-870">Etiķešu faila pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-870">Add a labels file</span></span>

<span data-ttu-id="0e459-871">Pievienojiet jaunajam **QuestionnairesErReportLabels\_en-US** etiķešu failu jūsu Visual Studio projektam un precizējiet sekojošās etiķetes jaunajiem UI resursiem:</span><span class="sxs-lookup"><span data-stu-id="0e459-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="0e459-872">**\@QuestionnairesReport** etiķete jaunajam izvēlnes krājumam, kas satur sekojošo tekstu angļu valodā (en-US): **Aptauju pārskats (darbina ER)**</span><span class="sxs-lookup"><span data-stu-id="0e459-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="0e459-873">**\@QuestionnairesReportBatchJobDescription** etiķete pakešuzdevuma nosaukumam, ja atlasītais ER formāts ir plānots izpildei kā pakešuzdevums</span><span class="sxs-lookup"><span data-stu-id="0e459-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="0e459-874">Pārskata pakalpojumu klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-874">Add a report service class</span></span>

<span data-ttu-id="0e459-875">Pievienojiet jaunu **QuestionnairesErReportService** klasi jūsu Visual Studio projektam un rakstāt kodu, kas izsauc ER formātu identificē to ar formāta kartēšanas ID un nodrošina datu līgumu kā parametru.</span><span class="sxs-lookup"><span data-stu-id="0e459-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="0e459-876">Kad jāizmanto ER formāts, kas palaiž programmas datus, ir jākonfigurē **Datu modeļa** tipa datu avots formāta kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="0e459-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="0e459-877">Šis datu avots attiecas uz specifisku noteikta datu modeļa daļu, izmantojot vienu saknes definīciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="0e459-878">Kad ER formāts ir palaists, to sauc par šo datu avotu, lai piekļūtu atbilstošajai ER modeļa kartēšanai, kas ir konfigurēta dotajam modelim un saknes definīcijai.</span><span class="sxs-lookup"><span data-stu-id="0e459-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="0e459-879">Visu informāciju, ko jūs varētu sagatavot pirmkodā un saglabāt kā daļu no datu līguma, var nodot uz palaisto ER formātu, izmantojot šāda veida ER modeļa kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="0e459-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="0e459-880">ER modeļa kartēšanai ir jākonfigurē **Objekta** tipa datu avots, kas attiecas uz **[QuestionnairesErReportContract](#DataContractClass)** klasi.</span><span class="sxs-lookup"><span data-stu-id="0e459-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="0e459-881">Lai identificētu modeļa kartēšanu, jānorāda datu avots, kas izsauc šo modeļa kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="0e459-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="0e459-882">Nodrošinātāja kodā šis datu avots, ko norādījis **ERModelDataSourceName** konstants, kuram ir **[modeļa](#ModelDSName)** vērtība.</span><span class="sxs-lookup"><span data-stu-id="0e459-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="0e459-883">Lai noteiktu, kurš datu avots tiek izmantots datu līguma atklāšanai modeļa kartēšanā, jānorāda datu avota nosaukums.</span><span class="sxs-lookup"><span data-stu-id="0e459-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="0e459-884">Nodrošinātāja kodā šis nosaukums, ko norādījis **ParametersDataSourceName** konstants, kuram ir <a name="DataContractDSName"></a>**RunTimeParameters** vērtība.</span><span class="sxs-lookup"><span data-stu-id="0e459-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="0e459-885">Jaunā vidē var būt nepieciešams atsvaidzināt ER metadatus, lai šis klases veids būtu pieejams ER modeļu kartēšanas veidotājā.</span><span class="sxs-lookup"><span data-stu-id="0e459-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="0e459-886">Papildinformāciju skatiet tēmā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="0e459-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="0e459-887">Pārskata kontrolētāja klases pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-887">Add a report controller class</span></span>

<span data-ttu-id="0e459-888">Pievienojiet projektam jaunu **QuestionnairesErReportController** klasi jūsu Visual Studio projektam un ierakstiet kodu, kas palaiž ER formātu sinhronajā režīmā vai partijas režīmā, kā vēlaties, dialoglodziņā, kas tiek veidots, pamatojoties uz nodrošinātās **QuestionnairesErReportUIBuilder** klasi.</span><span class="sxs-lookup"><span data-stu-id="0e459-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="0e459-889">Izvēlnes elementa pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-889">Add a menu item</span></span>

<span data-ttu-id="0e459-890">Pievienojiet jūsu Visual Studio projektam jaunu **QuestionnairesErReport** izvēlnes elementu.</span><span class="sxs-lookup"><span data-stu-id="0e459-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="0e459-891">**Objekta** rekvizītā šis izvēlnes elements attiecas uz **QuestionnairesErReportController** klasi, un to izmanto, lai norādītu lietotāja atļauju atlasīt un palaist ER formātu.</span><span class="sxs-lookup"><span data-stu-id="0e459-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="0e459-892">**Etiķetes** rekvizītā šis izvēlnes elements attiecas uz **\@QuestionnairesReport** etiķeti, ko jūs iepriekš izveidojāt, lai pareizais teksts tiktu parādīts programmā UI.</span><span class="sxs-lookup"><span data-stu-id="0e459-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="0e459-893">Izvēlnes krājuma pievienošana izvēlnei</span><span class="sxs-lookup"><span data-stu-id="0e459-893">Add a menu item to a menu</span></span>

<span data-ttu-id="0e459-894">Pievienojiet projektam esošu **KM** izvēlni jūsu Visual Studio projektam.</span><span class="sxs-lookup"><span data-stu-id="0e459-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="0e459-895">Šai izvēlnei ir jāpievieno jauns **Izejošā** tipa **QuestionnairesErReport** krājums izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="0e459-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="0e459-896">Šim krājumam ir jāattiecas uz **QuestionnairesErReport** izvēlnes elementu, kas aprakstīts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="0e459-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="0e459-897">Visual Studio projekta izveide</span><span class="sxs-lookup"><span data-stu-id="0e459-897">Build a Visual Studio project</span></span>

<span data-ttu-id="0e459-898">Izveidojiet savu projektu, lai jaunais izvēlnes elements būtu pieejams lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="0e459-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="0e459-899">Formāta palaišana no programmas</span><span class="sxs-lookup"><span data-stu-id="0e459-899">Run a format from the application</span></span>

1. <span data-ttu-id="0e459-900">Dodieties uz **Aptauja** \> **Noformējums** \> **Aptauju pārskats (darbina ER)**.</span><span class="sxs-lookup"><span data-stu-id="0e459-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Atlasot Anketu pārskata (darbina ER) izvēlnes krājumu Anketas modulī, lai palaistu konfigurēto ER formātu](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="0e459-902">Dialoglodziņā **Formāta kartēšana** atlasiet **Anketu pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="0e459-903">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-903">Select **OK**.</span></span>
4. <span data-ttu-id="0e459-904">Dialoglodziņā **Elektronisko pārskatu parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.</span><span class="sxs-lookup"><span data-stu-id="0e459-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="0e459-905">Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="0e459-906">Atlasiet **Labi**, lai palaistu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-906">Select **OK** to run the report.</span></span>

    ![Dialoglodziņā Elektroniskais pārskats norādiet atlases kritērijus](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="0e459-908">Pārskatiet ģenerēto pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="0e459-909">Izstrādāta ER risinājuma noregulēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-909">Tune a designed ER solution</span></span>

<span data-ttu-id="0e459-910">Varat modificēt konfigurēto ER risinājumu tā, lai tas izmantotu datu nodrošinātāju klasi, ko izstrādājāt, lai piekļūtu informācijai par darbojošos ER formātu, un tā, lai tā ievadītu šī ER formāta nosaukumu ģenerētajā pārskatā.</span><span class="sxs-lookup"><span data-stu-id="0e459-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="0e459-911">Modeļa kartējuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="0e459-912">Datu avotu pievienošana piekļuves datu līguma objektam</span><span class="sxs-lookup"><span data-stu-id="0e459-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="0e459-913">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-914">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="0e459-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="0e459-915">Atlasiet **Noformētājs**, lai atvērtu **Modelis datu avota kartēšanas** lapu.</span><span class="sxs-lookup"><span data-stu-id="0e459-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="0e459-916">Atlasiet **Noformētājs**, lai atvērtu atlasīto kartējumu modeļa kartēšanas veidotājā.</span><span class="sxs-lookup"><span data-stu-id="0e459-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="0e459-917">Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Objekts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="0e459-918">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="0e459-919">Dialoglodziņā **Nosaukums** ievadiet **[RunTimeParameters](#DataContractDSName)**, kā definēts **QuestionnairesErReportService** klases pirmkodā.</span><span class="sxs-lookup"><span data-stu-id="0e459-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="0e459-920">Laukā **Klase** ievadiet **[QuestionnairesErReportContract](#DataContractClass)**, kas tika iepriekš kodēts.</span><span class="sxs-lookup"><span data-stu-id="0e459-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="0e459-921">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-921">Select **OK**.</span></span>
10. <span data-ttu-id="0e459-922">Izvērst **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="0e459-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="0e459-923">Pievienotais datu avots sniedz informāciju par palaisto ER formāta kartēšanas ieraksta ID.</span><span class="sxs-lookup"><span data-stu-id="0e459-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Pievienots datu avots ER modeļu kartēšanas veidotājā](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="0e459-925">Datu avota pievienošana, lai piekļūtu ER formāta kartēšanas ierakstiem</span><span class="sxs-lookup"><span data-stu-id="0e459-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="0e459-926">Turpiniet rediģēt atlasīto modeļa kartēšanu, pievienojot datu avotu, lai piekļūtu ER formāta kartēšanas ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="0e459-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="0e459-927">Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="0e459-928">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="0e459-929">Dialoglodziņa laukā **Nosaukums** ievadiet **ER1**.</span><span class="sxs-lookup"><span data-stu-id="0e459-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="0e459-930">Laukā **Tabula** ievadiet **ERFormatMappingTable**.</span><span class="sxs-lookup"><span data-stu-id="0e459-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="0e459-931">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="0e459-932">Datu avota pievienošana, lai piekļūtu tekošā ER formāta kartēšanas ierakstam</span><span class="sxs-lookup"><span data-stu-id="0e459-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="0e459-933">Turpiniet rediģēt atlasīto modeļa kartēšanu, pievienojot datu avotu, lai piekļūtu palaistā ER formāta formāta kartēšanas ierakstam.</span><span class="sxs-lookup"><span data-stu-id="0e459-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="0e459-934">Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="0e459-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="0e459-935">Atlasiet **Pievienot sakni** rūtī **Datu avoti**.</span><span class="sxs-lookup"><span data-stu-id="0e459-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="0e459-936">Dialoglodziņa laukā **Nosaukums** ievadiet **ER2**.</span><span class="sxs-lookup"><span data-stu-id="0e459-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="0e459-937">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="0e459-938">Formulu redaktorā laukā **Formula** ievadiet **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="0e459-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="0e459-939">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="0e459-940">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="0e459-941">Tekošā ER formāta nosaukuma ievadīšana datu modelī</span><span class="sxs-lookup"><span data-stu-id="0e459-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="0e459-942">Turpiniet rediģēt atlasīto modeļa kartēšanu, lai datu modelī tiktu ievadīts palaists ER formāta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="0e459-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="0e459-943">Lapā **Modeļa kartējuma noformētājs** rūtī **Datu modelis** izvērsiet **ExecutionContext** un tad atlasiet **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="0e459-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="0e459-944">Rūtī **Datu modelis** atlasiet **Rediģēt**, lai konfigurētu datu saistījumu atlasītajam datu modeļa laukam.</span><span class="sxs-lookup"><span data-stu-id="0e459-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="0e459-945">Formulas redaktorā laukā **Formula** ievadiet **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="0e459-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="0e459-946">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="0e459-947">Tā kā jūs izmantojāt lauku **FormatName**, konfigurētā modeļa kartēšana tagad pakļauj ER formāta nosaukumu, kas izsauc šo modeļa kartēšanu izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="0e459-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Datu modeļa lauku saistīšana ar pievienoto datu avota metodi ER modeļa kartēšanas veidotājā](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="0e459-949">Modeļa kartēšanas noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="0e459-950">Lapā **Modeļa kartēšanas noformētājs** atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="0e459-951">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e459-951">Close the page.</span></span>
3. <span data-ttu-id="0e459-952">Aizveriet modeļa kartējumu lapu.</span><span class="sxs-lookup"><span data-stu-id="0e459-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="0e459-953">**Konfigurāciju** lapā, konfigurācijas kokā pārliecinieties, vai **Aptaujas kartēšanas** konfigurācija joprojām ir atlasīta.</span><span class="sxs-lookup"><span data-stu-id="0e459-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="0e459-954">Tad kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="0e459-955">Atlasiet **Mainīt statusu** \> **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0e459-956">Šīs konfigurācijas 1.2. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0e459-957">1.2. versiju vairs nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="0e459-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="0e459-958">Šī versija satur konfigurēto modeļa kartēšanu, un to var izmantot kā pamatu citām ER konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="0e459-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="0e459-959">Šīs konfigurācijas 1.3. versija ir izveidota un tās statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0e459-960">Varat rediģēt šo versiju, lai koriģētu **Anketas** modeļa kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="0e459-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="0e459-961">Formāta modificēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-961">Modify a format</span></span>

<span data-ttu-id="0e459-962">Varat modificēt konfigurēto ER formātu tā, lai tā nosaukums būtu redzams pārskata kājenē, kas tiek ģenerēts, kad tiek palaists ER formāts.</span><span class="sxs-lookup"><span data-stu-id="0e459-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="0e459-963">Jauna formāta elementa pievienošana</span><span class="sxs-lookup"><span data-stu-id="0e459-963">Add a new format element</span></span>

1. <span data-ttu-id="0e459-964">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-965">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="0e459-966">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0e459-966">Select **Designer**.</span></span>
4. <span data-ttu-id="0e459-967">Lapā **Formāta veidotājs** atlasiet saknes krājumu **Pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="0e459-968">Atlasiet **Pievienot**, lai atlasītajam **Pārskata** saknes krājumam pievienotu jaunu ligzdotu formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="0e459-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="0e459-969">Atlasiet **Excel\\Footer**.</span><span class="sxs-lookup"><span data-stu-id="0e459-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="0e459-970">Laikā **Nosaukums** ievadiet **Kājene**.</span><span class="sxs-lookup"><span data-stu-id="0e459-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="0e459-971">Atlasiet **Pārskats/Kājene** un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="0e459-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="0e459-972">Atlasiet **Teksts\\Virkne**.</span><span class="sxs-lookup"><span data-stu-id="0e459-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="0e459-973">Pievienotā formāta elementa saistīšana</span><span class="sxs-lookup"><span data-stu-id="0e459-973">Bind the added format element</span></span>

1. <span data-ttu-id="0e459-974">Lapā **Formāta noformētājs**, cilnē **Kartēšana**, formatēšanas kokā elementā **Kājene\\Virkne** atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="0e459-975">Formulas redaktorā laukā **Formula** ievadiet **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="0e459-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="0e459-976">Atlasiet **Saglabāt** un aizveriet formulas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="0e459-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="0e459-977">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-977">Select **Save**.</span></span>

<span data-ttu-id="0e459-978">Konfigurētais formāts tagad ir pārveidots tā, lai tā nosaukums tiktu ievadīts ģenerētā pārskata kājenē, izmantojot **Kājenes\\Virknes** elementu.</span><span class="sxs-lookup"><span data-stu-id="0e459-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Kājenes formāta elementa pievienošana konfigurētajam formātam ER operāciju veidotājā](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="0e459-980">Formāta noformējuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0e459-980">Complete the format design</span></span>

1. <span data-ttu-id="0e459-981">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="0e459-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="0e459-982">**Konfigurāciju** lapā, konfigurācijas kokā pārliecinieties, vai **Aptaujas pārskats** konfigurācija joprojām ir atlasīta.</span><span class="sxs-lookup"><span data-stu-id="0e459-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="0e459-983">Tad kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="0e459-984">Atlasiet **Mainīt statusu** \> **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0e459-985">Šīs konfigurācijas 1.2. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**.</span><span class="sxs-lookup"><span data-stu-id="0e459-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0e459-986">1.2. versiju vairs nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="0e459-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="0e459-987">Šī versija satur konfigurēto formātu, un to var izmantot kā pamatu citām ER konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="0e459-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="0e459-988">Šīs konfigurācijas 1.3. versija ir izveidota un tās statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0e459-989">Varat rediģēt šo versiju, lai koriģētu **Anketas** pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="0e459-990">Formāta palaišana no programmas</span><span class="sxs-lookup"><span data-stu-id="0e459-990">Run a format from the application</span></span>

1. <span data-ttu-id="0e459-991">Dodieties uz **Aptauja** \> **Noformējums** \> **Aptauju pārskats (darbina ER)**.</span><span class="sxs-lookup"><span data-stu-id="0e459-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="0e459-992">Dialoglodziņā **Formāta kartēšana** atlasiet **Anketu pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="0e459-993">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-993">Select **OK**.</span></span>
4. <span data-ttu-id="0e459-994">Dialoglodziņā **ER parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.</span><span class="sxs-lookup"><span data-stu-id="0e459-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="0e459-995">Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="0e459-996">Atlasiet **Labi**, lai palaistu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="0e459-997">Pārskatiet ģenerēto failu Excel formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="0e459-998">Ievērojiet, ka ģenerētā pārskata kājenē ir norādīts tā ER formāta nosaukums, kas tika izmantots, lai to ģenerētu.</span><span class="sxs-lookup"><span data-stu-id="0e459-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Ģenerētais fails Excel formātā](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="0e459-1000">Formāta palaišana no ER</span><span class="sxs-lookup"><span data-stu-id="0e459-1000">Run a format from ER</span></span>

1. <span data-ttu-id="0e459-1001">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0e459-1002">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="0e459-1003">Darbību rūtī atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="0e459-1004">Dialoglodziņā **Elektronisko pārskatu parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.</span><span class="sxs-lookup"><span data-stu-id="0e459-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="0e459-1005">Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="0e459-1006">Atlasiet **Labi**, lai palaistu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="0e459-1007">Pārskatiet ģenerēto failu Excel formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="0e459-1008">Ievērojiet, ka ģenerētā pārskata kājenē nav ER formāta nosaukuma, kas tika izmantots, lai to ģenerētu, jo datu līguma objekts netika nodots darbības modeļa kartēšanai, kad to izsauca ER formāts, kas tika palaists no ER.</span><span class="sxs-lookup"><span data-stu-id="0e459-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="0e459-1009">Formāta mērķa konfigurēšana ekrānā redzamajā priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="0e459-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="0e459-1010">Dodieties uz **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Elektroniskās pārskatu veidošanas adresāts**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="0e459-1011">**Elektroniskās ziņošanas mērķa** lapā konfigurētajam **Anketas pārskata** ER formātam pievienojiet mērķa ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0e459-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="0e459-1012">Kopsavilkuma cilnē **Faila mērķis** iestatiet **Ekrāna** [mērķi](er-destination-type-screen.md) **Pārskata** formāta komponentam, kas ir [pievienots](#AddFormatRootElement) kā konfigurētā **Anketas pārskata** ER formāta saknes elements.</span><span class="sxs-lookup"><span data-stu-id="0e459-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="0e459-1013">Kopsavilkuma cilnē **PDF pārvēršanas iestatījumi** konfigurējiet mērķi, lai pārveidotu pārskatu [PDF formātā](electronic-reporting-destinations.md#OutputConversionToPDF), kas izmanto **Ainavas** lapas orientāciju.</span><span class="sxs-lookup"><span data-stu-id="0e459-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Pielāgota ekrāna mērķa konfigurēšana ER formātam elektroniskās ziņošanas mērķa lapā](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="0e459-1015">Formāta palaišana no programmas, lai to priekšskatītu kā PDF dokumentu</span><span class="sxs-lookup"><span data-stu-id="0e459-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="0e459-1016">Dodieties uz **Aptauja** \> **Noformējums** \> **Aptauju pārskats (darbina ER)**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="0e459-1017">Dialoglodziņā **Formāta kartēšana** atlasiet **Anketu pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="0e459-1018">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1018">Select **OK**.</span></span>
4. <span data-ttu-id="0e459-1019">Dialoglodziņā **Elektronisko pārskatu parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.</span><span class="sxs-lookup"><span data-stu-id="0e459-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="0e459-1020">Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="0e459-1021">Kopsavilkuma cilnē **Galamērķi** ievērojiet, ka **Izvades** lauks ir iestatīts uz **Ekrāns**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="0e459-1022">Ja vēlaties mainīt konfigurēto mērķi, atlasiet **Mainīt**.</span><span class="sxs-lookup"><span data-stu-id="0e459-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![ER pārskata izpildlaika dialoglodziņš, kur varat mainīt konfigurēto mērķi](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="0e459-1024">Atlasiet **Labi**, lai palaistu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0e459-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="0e459-1025">Pārskatiet ģenerēto failu PDF formātā.</span><span class="sxs-lookup"><span data-stu-id="0e459-1025">Review the generated report in PDF format.</span></span>

    ![Ģenerētā faila ekrāna priekšskatījums PDF formātā](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="0e459-1027">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0e459-1027">Additional resources</span></span>

- [<span data-ttu-id="0e459-1028">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="0e459-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0e459-1029">Elektronisko atskaišu veidošanas formulas valoda</span><span class="sxs-lookup"><span data-stu-id="0e459-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="0e459-1030">Daudzvalodu pārskatu noformēšana</span><span class="sxs-lookup"><span data-stu-id="0e459-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="0e459-1031">Elektronisko pārskatu struktūras API</span><span class="sxs-lookup"><span data-stu-id="0e459-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="0e459-1032">CASE funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="0e459-1033">CONCATENATE funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="0e459-1034">DATETIMEFORMAT funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="0e459-1035">FILTER funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="0e459-1036">FIRSTORNULL funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="0e459-1037">FORMAT funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="0e459-1038">IF funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="0e459-1039">ORDERBY funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="0e459-1040">SESSIONNOW funkcija</span><span class="sxs-lookup"><span data-stu-id="0e459-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)