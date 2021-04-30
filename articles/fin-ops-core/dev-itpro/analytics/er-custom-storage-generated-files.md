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
ms.openlocfilehash: bd979bf5369b6878caaee82fc9c6a40d363cc165
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894152"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Pielāgotas glabāšanas vietas norādīšana ģenerētajiem dokumentiem

[!include[banner](../includes/banner.md)]

Elektronisko pārskatu veidošanas (ER) struktūras lietojumprogrammas interfeiss (API) ļauj paplašināt ER formātu ģenerēto dokumentu glabāšanas vietu sarakstu. Šajā tēmā skaidrots, kā pievienot pielāgotu glabāšanas vietu ģenerētajiem dokumentiem, deleģējot uzdevumu izveidot ER galamērķus uz noklusējuma mērķa rūpnīcu un pēc tam ieviešot pielāgotu klasi ar savu mērķa loģiku.

## <a name="prerequisites"></a>Priekšnosacījumi

Izvietojiet topoloģiju, kas atbalsta pastāvīgu būvēšanu. Papildinformāciju skatiet tēmā [Tādu topoloģiju izvietošana, kuras atbalsta pastāvīgu būvēšanu un testu automatizēšanu](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Jums jābūt arī piekļuvei šai topoloģijai ar vienu no tālāk minētajām lomām.

- Elektroniskā pārskata izstrādātājs
- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

Jums jābūt arī piekļuvei šīs topoloģijas izstrādes videi.

Visus šīs tēmas uzdevumus var pabeigt **USMF** uzņēmumā.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Pamatlīdzekļu atjaunošanas ER formāta importēšana

Lai ģenerētu dokumentus, kam plānojat pievienot pielāgotu glabāšanas vietu, [importējiet](er-download-configurations-global-repo.md) **pamatlīdzekļu atjaunošanas** ER formāta konfigurāciju pašreizējā topoloģijā.

![Konfigurācijas repozitorijas lapa.](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Pamatlīdzekļu atjaunošanas pārskata izpilde

1. Doties uz **Pamatlīdzekļi** \> **Pieprasījumi un pārskati** \> **Darījumu pārskati** \> **Pamatlīdzekļu atjaunošana**.
2. Laukā **No datuma** ievadiet **1/1/2017** (2017. gada 1. janvāris).
3. Laukā **Līdz datumam** ievadiet **1/31/2017** (2017. gada 31. janvāris).
4. Laukā **Valūta** atlasiet **Uzskaites valūta**.
5. Laukā **Formāta kartēšana** atlasiet **Pamatlīdzekļu atjaunošana**.
6. Atlasiet **Labi**.

![Izpildlaika dialoglodziņš pamatlīdzekļu atjaunošanas pārskatam](./media/er-custom-storage-generated-files-runtime-dialog.png)

Programmā Microsoft Excel pārskatiet izejošo dokumentu, kas ir izveidots un pieejams lejupielādei. Šī uzvedība ir [noklusējuma uzvedība](electronic-reporting-destinations.md#default-behavior) ER formātam, kam nav konfigurēts neviens [galamērķis](electronic-reporting-destinations.md) un kas darbojas interaktīvajā režīmā.

## <a name="review-the-source-code"></a>Pirmkoda pārskatīšana

Pārskatiet metodes `generateReportByGER()` kodu klasei `AssetRollForwardService`. Ievērojiet, ka `Run()` metode tiek izmantota, lai izsauktu ER struktūru un ģenerētu **pamatlīdzekļu atjaunošanas** pārskatu.

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

## <a name="modify-the-source-code"></a>Pirmkoda modificēšana

1. Savā Visual Studio projektā pievienojiet jaunu klasi (šajā piemērā tā ir`AssetRollForwardDestination` ) un ierakstiet kodu, lai ieviestu savu pielāgoto galamērķi izveidotajiem **pamatlīdzekļu atjaunošanas** pārskatiem.

    - `new()` metode ir izstrādāta, lai iegūtu sākotnējo ER galamērķa objektu un programmas loģisko parametru, kas nosaka pielāgotu atrašanās vietu, kur jāsaglabā ģenerētie pārskati. Šajā piemērā pielāgotā atrašanās vieta ir servera lokālās failu sistēmas nosaukums, kas palaiž Application Object Server (AOS) pakalpojumu.
    - Metode `saveFile()` ir izstrādāta, lai saglabātu ģenerēto dokumentu tā servera lokālās failu sistēmas mapē, kurā darbojas AOS pakalpojums.

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

2. Savā Visual Studio projektā pievienojiet jaunu klasi (šajā piemērā tā ir`AssetRollForwardDestinationFactory` ) un rakstiet kodu, lai iestatītu pielāgotu galamērķa rūpnīcu, kas deleģē galamērķa izveidi noklusējuma mērķa rūpnīcai un aplauž failu galamērķī ar jūsu galamērķi.

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

3. Mainiet esošo `AssetRollForwardService` klasi un rakstiet kodu, lai iestatītu pielāgotu galamērķa rūpnīcu pārskata izpildītajam. Ievērojiet, ka tad, kad tiek veidota pielāgota galamērķa rūpnīca, tiek nodots programmas darbināts parametrs, kas norāda galamērķa mapi. Šādā veidā šī galamērķa mape tiek izmantota, lai glabātu ģenerētos failus.

    > [!NOTE] 
    > Pārliecinieties, ka norādītā mape (šajā piemērā **c:\\0** ) atrodas lokālajā failu sistēmā serverī, kas palaiž AOS pakalpojumu. Pretējā gadījumā izpildlaikā tiks izmests izņēmums [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1).

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

4. Atjaunojiet savu projektu

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Pamatlīdzekļu atjaunošanas pārskata atkārtota izpilde

1. Doties uz **Pamatlīdzekļi** \> **Pieprasījumi un pārskati** \> **Darījumu pārskati** \> **Pamatlīdzekļu atjaunošana**.
2. Laukā **No datuma** ievadiet **1/1/2017**.
3. Laukā **Līdz datumam** ievadiet **1/31/2017**.
4. Laukā **Valūta** atlasiet **Uzskaites valūta**.
5. Laukā **Formāta kartēšana** atlasiet **Pamatlīdzekļu atjaunošana**.
6. Atlasiet **Labi**.
7. Pārlūkojiet vietējo mapi **C:\\0**, lai atrastu ģenerēto failu.

> [!NOTE]
> Tā kā `originDestination` objekts šajā piemērā netiek lietots `AssetRollForwardDestination` objektā, ER formāta [galamērķu](electronic-reporting-destinations.md) konfigurācijas tiks ignorētas izpildlaikā.

## <a name="additional-resources"></a>Papildu resursi

- [Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)
- [Lietojumprogrammas Paplašināmība sākumlapa](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]