---
title: Izvietošanas vadlīnijas fiskālā printera integrācijas paraugs Polijai (mantotais)
description: Šajā rakstā ir sniegtas vadlīnijas par finanšu printera integrēšanas parauga izvietošanu Polijai no Microsoft Dynamics 365 Commerce mazumtirdzniecības programmatūras izstrādes komplekta (SDK).
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 178301e6d8e5f87376ed893e4bf5f966260cad62
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337245"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Izvietošanas vadlīnijas fiskālā printera integrācijas paraugs Polijai (mantotais)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Vadlīnijas šajā rakstā jālieto tikai tad, ja lietojat versiju Microsoft Dynamics 365 Commerce 10.0.28 vai agrāku versiju. No Commerce versijas 10.0.29 fiskālā printera integrācijas paraugs Polijai ir pieejams Commerce programmatūras izstrādes komplektā (SDK). Papildinformāciju skatiet kanāla [komponentu konfigurēšana](./emea-pol-fpi-sample.md#configure-channel-components).

Šajā rakstā ir sniegtas vadlīnijas par fiskālā printera Dynamics 365 Commerce integrēšanas parauga izvietošanu Polijai no Retail SDK izstrādātāja virtuālajā datorā (VM) Microsoft Dynamics pakalpojumos Lifecycle Services (LCS). Papildinformāciju par šo finanšu integrācijas paraugu skatiet Polijas [fiskālās printera integrācijas paraugs](emea-pol-fpi-sample.md). 

Polijas finanšu integrācijas paraugs ir daļa no sdk Retail. Informāciju par TO, kā instalēt un izmantot SDK, skatiet mazumtirdzniecības [programmatūras izstrādes komplekta (SDK) arhitektūru](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šis paraugs sastāv no Commerce Runtime () un aparatūras CRT stacijas paplašinājumiem. Lai palaistu šo paraugu, ir jāmodificē un jāveido aparatūras CRT stacijas projekti. Ieteicams izmantot nemodificētu komplektu Retail SDK, lai veiktu šajā rakstā aprakstītās izmaiņas. Iesakām izmantot arī avota kontroles sistēmu, piemēram, tādu Azure DevOps failu, kas vēl nav mainīti.

## <a name="development-environment"></a>Izstrādes vide

Izpildiet šīs darbības, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

### <a name="commerce-runtime-extension-components"></a>Commerce runtime paplašinājuma komponenti

Paplašinājuma CRT komponenti ir ietverti Retail SDK. Lai izpildītu tālāk norādītās procedūras, atveriet **commerceRuntimeSamples.sln** **risinājumu zem RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

1. Atrast Runtime.Extensions.DocumentProvider.PosnetSample **projektu** un veidot to.
2. **Mapē Extensions.DocumentProvider.PosnetSample bin\\ Debug \\** atrodiet Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll **montāžas** failu.
3. Kopēt montāžas failu uz CRT paplašinājuma mapi:

    - **Commerce Scale Unit:** kopējiet failu uz **\\ mapi bin\\ ext**, kas atrodas Interneta informācijas pakalpojumu (IIS) Commerce Scale Unit atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo **\\** mapi lokālā klienta starpnieka CRT atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**,**\\** un tā atrodas IIS Commerce Scale Unit vietas nodalījuma ārējā mapē.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

5. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Restartējiet Commerce Service:

    - **Commerce Scale Vienība: restartējiet** Commerce Service vietni no IIS pārvaldnieka.
    - **Klienta starpnieks:** beigt **dllhost.exe** procesu uzdevumu pārvaldniekā un pēc tam restartēt Modern POS.

### <a name="hardware-station-extension-components"></a>Aparatūras stacijas paplašinājuma komponenti

Aparatūras stacijas paplašinājuma komponenti ir iekļauti Retail SDK. Lai izpildītu tālāk norādītās procedūras, atveriet **hardwareStationSamples.sln** **risinājumu zem RetailSdk\\ SampleExtensions\\ HardwareStation**.

1. Atrast hardwareStation.Extension.PosnetThermalFVFiscalPrinterSample **projektu** un veidot to.
2. Mapē Extension.Posnet.ContosoFVFiscalPrinterSample **bin\\ Atkļūdošana\\** atrodiet contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll **montāžas** failu.
3. Kopējiet montāžas failu izvietotā aparatūras stacijas datorā:

    - **Attālās aparatūras stacija:** kopējiet failu uz **nodalījuma mapi** IIS aparatūras stacijas vietnes atrašanās vietā. Kopējiet printera draivera bibliotēkas (libposcmbth.dll **,** libcmbth **serial.dll\_ un** cmbth **pl.lng\_**).

4. Atrast aparatūras stacijas paplašinājumu konfigurācijas failu. Faila nosaukums ir **HardwareStation.Extension.config**:

    - **Attālās aparatūras stacija:** fails atrodas IIS aparatūras stacijas vietnes atrašanās vietā.

5. Pievienojiet konfigurācijas faila sastāva **sadaļai** šādu rindu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Restartējiet aparatūras stacijas pakalpojumu:

    - **Attālā aparatūras stacija: restartējiet** aparatūras stacijas vietni no IIS pārvaldnieka.

## <a name="production-environment"></a>Ražošanas vide

Iepriekšējā procedūrā ir iespējoti paplašinājumi, kas ir fiskālās reģistrācijas pakalpojuma integrācijas parauga komponenti. Turklāt šīs darbības ir jāveic, lai izveidotu izvietojamas pakotnes, kurās ir Commerce komponenti, un lai piemērotu šīs pakotnes ražošanas vidē.

1. Mapē RetailSdk Assets pakotnes **konfigurācijas failos\\ veiciet tālāk norādītās** izmaiņas.

    - Commerceruntime.ext.config **un** CommerceRuntime.MPOSOffline.Ext.config **konfigurācijas** failos pievienojiet šim sastāva sadaļai šādu **rindu.**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Konfigurācijas failā **HardwareStation.Extension.config** pievienojiet sastāva sadaļai šādu **rindu**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. **Mapē BuildTools veiciet šādas izmaiņas pielāgošanas.iestatījumu** pakotnes pielāgošanas **konfigurācijas** failā:

    - Pievienojiet tālāk norādīto rindu, lai ietvertu CRT paplašinājumu izvietojamās pakotnēs.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Pievienojiet tālāk norādīto rindu, lai ietvertu aparatūras stacijas paplašinājumu izvietojamās pakotnēs.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Startējiet utilītai MSBuild komandu Visual Studio uzvedni un palaidiet msbuild **mapē Retail SDK,** lai izveidotu izvietojamas pakotnes.
1. Piemērot iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet sadaļā [Izvietojamu pakotņu izveide](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Fiskālā printera integrācijas paraugs Polijai ir balstīts uz finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md). Papildinformāciju par fiskālās integrācijas risinājuma dizainu skatiet [finanšu integrācijas parauga dizaina apskatā](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Nolūks paplašinājumam, kas ir fiskālā dokumenta nodrošinātājs, ir izveidot printerim raksturīgus dokumentus un apstrādāt atbildes no fiskālā printera.

Paplašinājums CRT ir **Runtime.Extensions.DocumentProvider.PosnetSample**. Šis paplašinājums izveido specifisku printera komandu kopu JavaScript objekta notācijas (JSON) formātā, kas definētas ar POSNET specifikāciju 19-3678.

Papildinformāciju par fiskālās integrācijas risinājuma dizainu skatiet finanšu [reģistrācijas procesā un finanšu integrācijas paraugos fiskālajām ierīcēm un pakalpojumiem](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

DocumentProviderPosnetProtocol **pieprasījuma** apdarinātājs ir ieejas punkts pieprasījumam ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest —** šajā pieprasījumā ir ietverta informācija par to, kurš dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālajā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest** - šis pieprasījums atgriež notikumu sarakstu, uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails ir atrodams paplašinājuma **projekta** konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- PVN likmju kartējums
- Norēķinu veida kartējums
- Depozīta maksājuma veids

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, nolūks ir sazināties ar fiskālo printeri.

Aparatūras stacijas paplašinājums **ir HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Šis paplašinājums izsauc POSNET draivera funkcijas, lai iesniegtu komandas, kuras paplašinājums CRT ģenerē fiskālam printerim. Tiek apstrādāts arī ierīces kļūdas.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

FiscalPrinterHandler **pieprasījumu apdarinātājs** ir ieejas punkts pieprasījuma apstrādei finanšu perifērijas ierīcē.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – šis pieprasījums sūta dokumentus printeriem un atgriež atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas paplašinājuma **projekta** konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus savienotājam, kas tiks konfigurēts no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- **Savienojuma virkne** – virkne, kas apraksta detalizētu informāciju par savienojumu ar ierīci draivera atbalstītajā formātā. Papildinformāciju skatiet POSNET draivera dokumentācijā.
- **Datuma un laika sinhronizācija** – vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē ar pievienoto aparatūras staciju.
- **Ierīces taimauts** – laiks milisekundēs, ko autovadītājs gaidīs no ierīces atbildes. Papildinformāciju skatiet POSNET draivera dokumentācijā.
