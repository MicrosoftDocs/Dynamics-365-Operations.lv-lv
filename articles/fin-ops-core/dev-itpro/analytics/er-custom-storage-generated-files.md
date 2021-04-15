---
title: Pielāgotas glabāšanas vietas norādīšana ģenerētajiem dokumentiem
description: Šajā tēmā izskaidrots, kā paplašināt elektronisko pārskatu veidošanas (Electronic Reporting — ER) formātu ģenerēto dokumentu glabāšanas vietu sarakstu.
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 25719de3d86785442e00f7375de525b95bdb094d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753700"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="85e7b-103">Pielāgotas glabāšanas vietas norādīšana ģenerētajiem dokumentiem</span><span class="sxs-lookup"><span data-stu-id="85e7b-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="85e7b-104">Elektronisko pārskatu veidošanas (ER) struktūras lietojumprogrammas interfeiss (API) ļauj paplašināt ER formātu ģenerēto dokumentu glabāšanas vietu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="85e7b-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="85e7b-105">Šajā tēmā skaidrots, kā pievienot pielāgotu glabāšanas vietu ģenerētajiem dokumentiem, deleģējot uzdevumu izveidot ER galamērķus uz noklusējuma mērķa rūpnīcu un pēc tam ieviešot pielāgotu klasi ar savu mērķa loģiku.</span><span class="sxs-lookup"><span data-stu-id="85e7b-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="85e7b-106">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="85e7b-106">Prerequisites</span></span>

<span data-ttu-id="85e7b-107">Izvietojiet topoloģiju, kas atbalsta pastāvīgu būvēšanu.</span><span class="sxs-lookup"><span data-stu-id="85e7b-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="85e7b-108">Papildinformāciju skatiet tēmā [Tādu topoloģiju izvietošana, kuras atbalsta pastāvīgu būvēšanu un testu automatizēšanu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="85e7b-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="85e7b-109">Jums jābūt arī piekļuvei šai topoloģijai ar vienu no tālāk minētajām lomām.</span><span class="sxs-lookup"><span data-stu-id="85e7b-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="85e7b-110">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="85e7b-110">Electronic reporting developer</span></span>
- <span data-ttu-id="85e7b-111">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="85e7b-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="85e7b-112">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="85e7b-112">System administrator</span></span>

<span data-ttu-id="85e7b-113">Jums jābūt arī piekļuvei šīs topoloģijas izstrādes videi.</span><span class="sxs-lookup"><span data-stu-id="85e7b-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="85e7b-114">Visus šīs tēmas uzdevumus var pabeigt **USMF** uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="85e7b-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="85e7b-115">Pamatlīdzekļu atjaunošanas ER formāta importēšana</span><span class="sxs-lookup"><span data-stu-id="85e7b-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="85e7b-116">Lai ģenerētu dokumentus, kam plānojat pievienot pielāgotu glabāšanas vietu, [importējiet](er-download-configurations-global-repo.md) **pamatlīdzekļu atjaunošanas** ER formāta konfigurāciju pašreizējā topoloģijā.</span><span class="sxs-lookup"><span data-stu-id="85e7b-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Konfigurācijas repozitorijas lapa.](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="85e7b-118">Pamatlīdzekļu atjaunošanas pārskata izpilde</span><span class="sxs-lookup"><span data-stu-id="85e7b-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="85e7b-119">Doties uz **Pamatlīdzekļi** \> **Pieprasījumi un pārskati** \> **Darījumu pārskati** \> **Pamatlīdzekļu atjaunošana**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="85e7b-120">Laukā **No datuma** ievadiet **1/1/2017** (2017. gada 1. janvāris).</span><span class="sxs-lookup"><span data-stu-id="85e7b-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="85e7b-121">Laukā **Līdz datumam** ievadiet **1/31/2017** (2017. gada 31. janvāris).</span><span class="sxs-lookup"><span data-stu-id="85e7b-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="85e7b-122">Laukā **Valūta** atlasiet **Uzskaites valūta**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="85e7b-123">Laukā **Formāta kartēšana** atlasiet **Pamatlīdzekļu atjaunošana**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="85e7b-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-124">Select **OK**.</span></span>

![Izpildlaika dialoglodziņš pamatlīdzekļu atjaunošanas pārskatam](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="85e7b-126">Programmā Microsoft Excel pārskatiet izejošo dokumentu, kas ir izveidots un pieejams lejupielādei.</span><span class="sxs-lookup"><span data-stu-id="85e7b-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="85e7b-127">Šī uzvedība ir [noklusējuma uzvedība](electronic-reporting-destinations.md#default-behavior) ER formātam, kam nav konfigurēts neviens [galamērķis](electronic-reporting-destinations.md) un kas darbojas interaktīvajā režīmā.</span><span class="sxs-lookup"><span data-stu-id="85e7b-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="85e7b-128">Pirmkoda pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="85e7b-128">Review the source code</span></span>

<span data-ttu-id="85e7b-129">Pārskatiet metodes `generateReportByGER()` kodu klasei `AssetRollForwardService`.</span><span class="sxs-lookup"><span data-stu-id="85e7b-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="85e7b-130">Ievērojiet, ka `Run()` metode tiek izmantota, lai izsauktu ER struktūru un ģenerētu **pamatlīdzekļu atjaunošanas** pārskatu.</span><span class="sxs-lookup"><span data-stu-id="85e7b-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
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

## <a name="modify-the-source-code"></a><span data-ttu-id="85e7b-131">Pirmkoda modificēšana</span><span class="sxs-lookup"><span data-stu-id="85e7b-131">Modify the source code</span></span>

1. <span data-ttu-id="85e7b-132">Savā Visual Studio projektā pievienojiet jaunu klasi (šajā piemērā tā ir`AssetRollForwardDestination` ) un ierakstiet kodu, lai ieviestu savu pielāgoto galamērķi izveidotajiem **pamatlīdzekļu atjaunošanas** pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="85e7b-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="85e7b-133">`new()` metode ir izstrādāta, lai iegūtu sākotnējo ER galamērķa objektu un programmas loģisko parametru, kas nosaka pielāgotu atrašanās vietu, kur jāsaglabā ģenerētie pārskati.</span><span class="sxs-lookup"><span data-stu-id="85e7b-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="85e7b-134">Šajā piemērā pielāgotā atrašanās vieta ir servera lokālās failu sistēmas nosaukums, kas palaiž Application Object Server (AOS) pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="85e7b-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="85e7b-135">Metode `saveFile()` ir izstrādāta, lai saglabātu ģenerēto dokumentu tā servera lokālās failu sistēmas mapē, kurā darbojas AOS pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="85e7b-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="85e7b-136">Savā Visual Studio projektā pievienojiet jaunu klasi (šajā piemērā tā ir`AssetRollForwardDestinationFactory` ) un rakstiet kodu, lai iestatītu pielāgotu galamērķa rūpnīcu, kas deleģē galamērķa izveidi noklusējuma mērķa rūpnīcai un aplauž failu galamērķī ar jūsu galamērķi.</span><span class="sxs-lookup"><span data-stu-id="85e7b-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="85e7b-137">Mainiet esošo `AssetRollForwardService` klasi un rakstiet kodu, lai iestatītu pielāgotu galamērķa rūpnīcu pārskata izpildītajam.</span><span class="sxs-lookup"><span data-stu-id="85e7b-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="85e7b-138">Ievērojiet, ka tad, kad tiek veidota pielāgota galamērķa rūpnīca, tiek nodots programmas darbināts parametrs, kas norāda galamērķa mapi.</span><span class="sxs-lookup"><span data-stu-id="85e7b-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="85e7b-139">Šādā veidā šī galamērķa mape tiek izmantota, lai glabātu ģenerētos failus.</span><span class="sxs-lookup"><span data-stu-id="85e7b-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="85e7b-140">Pārliecinieties, ka norādītā mape (šajā piemērā **c:\\0** ) atrodas lokālajā failu sistēmā serverī, kas palaiž AOS pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="85e7b-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="85e7b-141">Pretējā gadījumā izpildlaikā tiks izmests izņēmums [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="85e7b-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
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

4. <span data-ttu-id="85e7b-142">Atjaunojiet savu projektu</span><span class="sxs-lookup"><span data-stu-id="85e7b-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="85e7b-143">Pamatlīdzekļu atjaunošanas pārskata atkārtota izpilde</span><span class="sxs-lookup"><span data-stu-id="85e7b-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="85e7b-144">Doties uz **Pamatlīdzekļi** \> **Pieprasījumi un pārskati** \> **Darījumu pārskati** \> **Pamatlīdzekļu atjaunošana**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="85e7b-145">Laukā **No datuma** ievadiet **1/1/2017**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="85e7b-146">Laukā **Līdz datumam** ievadiet **1/31/2017**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="85e7b-147">Laukā **Valūta** atlasiet **Uzskaites valūta**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="85e7b-148">Laukā **Formāta kartēšana** atlasiet **Pamatlīdzekļu atjaunošana**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="85e7b-149">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-149">Select **OK**.</span></span>
7. <span data-ttu-id="85e7b-150">Pārlūkojiet vietējo mapi **C:\\0**, lai atrastu ģenerēto failu.</span><span class="sxs-lookup"><span data-stu-id="85e7b-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="85e7b-151">Tā kā `originDestination` objekts šajā piemērā netiek lietots `AssetRollForwardDestination` objektā, ER formāta [galamērķu](electronic-reporting-destinations.md) konfigurācijas tiks ignorētas izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="85e7b-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85e7b-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="85e7b-152">Additional resources</span></span>

- [<span data-ttu-id="85e7b-153">Elektroniskās pārskatu veidošanas (ER) adresāti</span><span class="sxs-lookup"><span data-stu-id="85e7b-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="85e7b-154">Lietojumprogrammas Paplašināmība sākumlapa</span><span class="sxs-lookup"><span data-stu-id="85e7b-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]