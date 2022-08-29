---
title: Itālijas fiskālā printera integrācijas parauga izvietošanas vadlīnijas (mantojuma)
description: Šajā rakstā ir sniegtas vadlīnijas itālijas fiskālā printera integrācijas parauga izvietošanai no mazumtirdzniecības Microsoft Dynamics 365 Commerce programmatūras izstrādes komplekta (SDK).
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 46d42a2c2a5f8f40fc8b9693f26a182c8f2e6352
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337240"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Itālijas fiskālā printera integrācijas parauga izvietošanas vadlīnijas (mantojuma)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Vadlīnijas šajā rakstā jālieto tikai tad, ja lietojat versiju Microsoft Dynamics 365 Commerce 10.0.28 vai agrāku versiju. No Commerce versijas 10.0.29 finanšu printera integrācijas paraugs Itālijai ir pieejams Commerce programmatūras izstrādes komplektā (SDK). Papildinformāciju skatiet kanāla [komponentu konfigurēšana](./emea-ita-fpi-sample.md#configure-channel-components).

Šajā rakstā ir sniegtas vadlīnijas par fiskālā printera Dynamics 365 Commerce integrācijas parauga izvietošanu Itālijai no Programmas Retail SDK izstrādātāja virtuālajā datorā (VM) Microsoft Dynamics pakalpojumos Lifecycle Services (LCS). Papildinformāciju par šo fiskālās integrācijas paraugu skatiet Itālijas [fiskālās printera integrācijas paraugs](emea-ita-fpi-sample.md). 

Itālijas finanšu integrācijas paraugs ir daļa no sdk Retail. Informāciju par TO, kā instalēt un izmantot SDK, skatiet mazumtirdzniecības [programmatūras izstrādes komplekta (SDK) arhitektūru](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šis paraugs sastāv no Commerce Runtime () un aparatūras CRT stacijas paplašinājumiem. Lai palaistu šo paraugu, ir jāmodificē un jāveido aparatūras CRT stacijas projekti. Ieteicams izmantot nemodificētu komplektu Retail SDK, lai veiktu šajā rakstā aprakstītās izmaiņas. Iesakām izmantot arī avota kontroles sistēmu, piemēram, tādu Azure DevOps failu, kas vēl nav mainīti.

## <a name="development-environment"></a>Izstrādes vide

Izpildiet šīs darbības, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

### <a name="commerce-runtime-extension-components"></a>Commerce runtime paplašinājuma komponenti

Paplašinājuma CRT komponenti ir ietverti Retail SDK. Lai izpildītu tālāk norādītās procedūras, atveriet **commerceRuntimeSamples.sln** **risinājumu zem RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

1. Atrast runtime.Extensions.DocumentProvider.EpsonFP90IISample **projektu** un veidot to.
2. Mapē Extensions.DocumentProvider.EpsonFP90IISample **bin\\ Atkļūdošanas\\ mape atrodiet** Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IISample.dll **montāžas failu.**
3. Kopēt montāžas failu uz CRT paplašinājumu mapi:

    - **Commerce Scale Unit:** kopējiet failu uz **\\ mapi bin\\ ext**, kas atrodas Interneta informācijas pakalpojumu (IIS) Commerce Scale Unit atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo **\\** mapi lokālā klienta starpnieka CRT atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**,**\\** un tā atrodas IIS Commerce Scale Unit vietas nodalījuma ārējā mapē.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

5. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Restartējiet Commerce Scale Unit:

    - **Commerce Scale Unit: restartējiet** Commerce Scale Unit vietni no IIS pārvaldnieka.
    - **Klienta starpnieks:** beigt **dllhost.exe** procesu uzdevumu pārvaldniekā un pēc tam restartēt Modern POS.

### <a name="hardware-station-extension-components"></a>Aparatūras stacijas paplašinājuma komponenti

Aparatūras stacijas paplašinājuma komponenti ir iekļauti Retail SDK. Lai izpildītu tālāk norādītās procedūras, atveriet **hardwareStationSamples.sln** **risinājumu zem RetailSdk\\ SampleExtensions\\ HardwareStation**.

1. Atrodiet projektu **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** un izveidojiet to.
2. **Paplašinājumos.EpsonFP90IIIFiscalDeviceSample\\ bin\\** Atkļūdošanas mape atrodiet **Contoso.Commerce.HardwareStation.EpsonFP90IIFiscalDeviceSample.dll** montāžas failu.
3. Kopējiet montāžas failu izvietotā aparatūras stacijas datorā:

    - **Attālās aparatūras stacija:** kopējiet failu uz **nodalījuma mapi** IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Lokālā aparatūras stacija:** kopējiet failu Modern POS klienta starpnieka atrašanās vietā.

4. Atrast aparatūras stacijas paplašinājumu konfigurācijas failu. Faila nosaukums ir **HardwareStation.Extension.config**:

    - **Attālās aparatūras stacija:** fails atrodas IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Lokālā aparatūras stacija:** fails atrodas Modern POS klienta starpnieka atrašanās vietā.

5. Pievienojiet konfigurācijas faila sastāva **sadaļai** šādu sadaļu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Restartējiet aparatūras stacijas pakalpojumu:

    - **Attālā aparatūras stacija: restartējiet** aparatūras stacijas vietni no IIS pārvaldnieka.
    - **Lokālā aparatūras stacija:** beigt **dllhost.exe** procesu uzdevumu pārvaldniekā un pēc tam restartēt Modern POS.

## <a name="production-environment"></a>Ražošanas vide

Lai izveidotu izvietojamus iepakojumus, kas ietver Commerce komponentus, un piemēroiet šīs pakotnes ražošanas vidē, veiciet šos soļus:

1. Veiciet soļus, kas ir aprakstīti izstrādes [vides sadaļā](#development-environment) iepriekš šajā rakstā.
2. Mapē RetailSdk Assets pakotnes **konfigurācijas failos\\ veiciet tālāk norādītās** izmaiņas.

    1. Commerceruntime.ext.config **un** CommerceRuntime.MPOSOffline.Ext.config **konfigurācijas** failos pievienojiet šim sastāva sadaļai šādu **rindu.**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. Konfigurācijas failā **HardwareStation.Extension.config** pievienojiet sastāva sadaļai šādu **rindu**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. **Mapē BuildTools veiciet šādas izmaiņas pielāgošanas.iestatījumu** pakotnes pielāgošanas **konfigurācijas** failā:

    1. Pievienojiet tālāk norādīto rindu, lai ietvertu CRT paplašinājumu izvietojamās pakotnēs.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Pievienojiet tālāk norādīto rindu, lai ietvertu aparatūras stacijas paplašinājumu izvietojamās pakotnēs.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Veiciet tālāk norādītās **izmaiņas failā Sdk.ModernPos.Shared.csproj** **mapē Iepakojumi\_ SharedPackagingProjectComponents, lai ietvertu Itālijas resursu failus izvietojamās pakotnēs**:

    1. Pievienojiet ItemGroup **sadaļu**, kas satur mezglus, kas norāda uz resursu failiem nepieciešamajiem tulkojumiem. Pārliecinieties, ka ir jānorāda pareizās nosaukumvietas un parauga nosaukumi. Šis piemērs tam pievieno resursu mezglus **un** **tas-CH lokāļi**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Sadaļā Mērķa **Nosaukums="CopyPackageFiles"** pievienojiet vienu rindu katrai lokālajai sadaļai, kā parādīts šajā piemērā.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Veiciet tālāk norādītās izmaiņas **failā Sdk.RetailServerSetup.proj** **, kas atrodas mapē Packages\_ SharedPackagingProjectComponents**, lai ietvertu Itālijas resursu failus izvietojamās pakotnēs:

    1. Pievienojiet ItemGroup **sadaļu**, kas satur mezglus, kas norāda uz resursu failiem nepieciešamajiem tulkojumiem. Pārliecinieties, ka ir jānorāda pareizās nosaukumvietas un parauga nosaukumi. Šis piemērs tam pievieno resursu mezglus **un** **tas-CH lokāļi**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Sadaļā Mērķa **Nosaukums="CopyPackageFiles"** pievienojiet vienu rindu katrai lokālajai sadaļai, kā parādīts šajā piemērā.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Startējiet utilītai MSBuild komandu Visual Studio uzvedni un pēc tam palaidiet msbuild **mapē Retail SDK,** lai izveidotu izvietojamas pakotnes.
7. Piemērot iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet sadaļā [Izvietojamu pakotņu izveide](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Paplašinājumu dizains

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Nolūks paplašinājumam, kas ir fiskālā dokumenta nodrošinātājs, ir izveidot printerim raksturīgus dokumentus un apstrādāt atbildes no fiskālā printera.

Paplašinājums CRT ir **Runtime.Extensions.DocumentProvider.EpsonFP90IISample**.

Papildinformāciju par fiskālās integrācijas risinājuma dizainu skatiet finanšu [reģistrācijas procesā un finanšu integrācijas paraugos fiskālajām ierīcēm un pakalpojumiem](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Pieprasījumu **apdarinātājs DocumentProviderEpsonFP90III ir** ieejas punkts pieprasījumam ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest —** šajā pieprasījumā ir ietverta informācija par to, kurš dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālajā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest** - šis pieprasījums atgriež notikumu sarakstu, uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas paplašinājuma **projekta** konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- PVN kodu kartējums
- PVN likmju kartējums
- Norēķinu veida kartējums
- Ieejas plūsmas numura svītrkoda veids
- Depozīta maksājuma veids

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, nolūks ir sazināties ar fiskālo printeri.

Aparatūras stacijas paplašinājums **ir HardwareStation.Extension.EpsonFP90IIFiscalDeviceSample**. Šis paplašinājums izmanto HTTP protokolu, lai iesniegtu dokumentus, ko CRT paplašinājums ģenerē fiskālam printerim. Tā apstrādā arī atbildes, kas saņemtas no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EpsonFP90IISample** pieprasījuma apdarinātājs ir ieejas punkts finanšu perifērijas ierīču pieprasījumu apstrādei.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – šis pieprasījums sūta dokumentus printeriem un atgriež atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas paplašinājuma **projekta** konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus savienotājam, kas tiks konfigurēts no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- **Galapunkta** adrese – printera URL.
- **Datuma un laika sinhronizācija** – vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē ar pievienoto aparatūras staciju.
