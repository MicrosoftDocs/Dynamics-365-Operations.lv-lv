---
title: Itālijas fiskālā printera integrācijas parauga izvietošanas vadlīnijas (mantojuma)
description: Šajā tēmā sniegtas vadlīnijas itālijas fiskālā printera integrācijas parauga izvietošanai no Microsoft Dynamics 365 Commerce mazumtirdzniecības programmatūras izstrādes komplekta (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: a7b5f4f042aa5457ff33e9762f0902c5c72f5921
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944844"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Itālijas fiskālā printera integrācijas parauga izvietošanas vadlīnijas (mantojuma)

[!include[banner](../includes/banner.md)]

Šajā tēmā sniegtas vadlīnijas itālijas fiskālā printera integrācijas parauga izvietošanai no mazumtirdzniecības programmatūras izstrādes komplekta (SDK) izstrādātāja virtuālās mašīnas Microsoft Dynamics 365 Commerce (VM) Microsoft Dynamics pakalpojumos Lifecycle Services (LCS). Papildinformāciju par šo fiskālās integrācijas paraugu skatiet [Itālijas fiskālās printera integrācijas paraugs](emea-ita-fpi-sample.md). 

Itālijas finanšu integrācijas paraugs ir daļa no sdk Retail. Informāciju par TO, kā instalēt un izmantot SDK, skatiet [mazumtirdzniecības programmatūras izstrādes komplekta (SDK) arhitektūru](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šis paraugs sastāv no Commerce Runtime () un CRT aparatūras stacijas paplašinājumiem. Lai palaistu šo paraugu, ir jāmodificē un jāveido CRT aparatūras stacijas projekti. Ieteicams izmantot nemodificētu komplektu Retail SDK, lai veiktu šajā tēmā aprakstītās izmaiņas. Iesakām izmantot arī avota kontroles sistēmu, piemēram, Azure DevOps tādu failu, kas vēl nav mainīti.

## <a name="development-environment"></a>Izstrādes vide

Izpildiet šīs darbības, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

### <a name="commerce-runtime-extension-components"></a>Commerce runtime paplašinājuma komponenti

Paplašinājuma CRT komponenti ir ietverti Retail SDK. Lai izpildītu tālāk norādītās procedūras, atveriet **CommerceRuntimeSamples.sln risinājumu zem** **RetailSdk \\ SampleExtensions \\ CommerceRuntime.**

1. Atrast **runtime.Extensions.DocumentProvider.EpsonFP90IISample** projektu un veidot to.
2. Mapē **Extensions.DocumentProvider.EpsonFP90IISample bin Atkļūdošanas mape \\\\ atrodiet** **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IISample.dll montāžas** failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Commerce Scale Unit: kopējiet failu uz mapi bin ext, kas atrodas Interneta informācijas** **\\ pakalpojumu \\** (IIS) Commerce Scale Unit atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo mapi lokālā **\\ klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Commerce Scale Unit: faila nosaukums ir** **commerceruntime.ext.config, un tā atrodas** **IIS Commerce Scale \\ Unit vietas nodalījuma ārējā** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Restartējiet Commerce Scale Unit:

    - **Commerce Scale Unit:** restartējiet Commerce Scale Unit vietni no IIS pārvaldnieka.
    - **Klienta** starpnieks: beigt **dllhost.exe** procesu uzdevumu pārvaldniekā un pēc tam restartēt Modern POS.

### <a name="hardware-station-extension-components"></a>Aparatūras stacijas paplašinājuma komponenti

Aparatūras stacijas paplašinājuma komponenti ir iekļauti Retail SDK. Lai izpildītu tālāk norādītās procedūras, atveriet **HardwareStationSamples.sln risinājumu zem** **RetailSdk \\ SampleExtensions \\** HardwareStation.

1. Atrodiet projektu **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** un izveidojiet to.
2. **Paplašinājumos.EpsonFP90IIIFiscalDeviceSample bin Atkļūdošanas mape \\\\ atrodiet** **Contoso.Commerce.HardwareStation.EpsonFP90IIFiscalDeviceSample.dll montāžas** failu.
3. Kopējiet montāžas failu izvietotā aparatūras stacijas datorā:

    - **Attālās aparatūras** stacija: kopējiet failu uz **nodalījuma mapi** IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Lokālā aparatūras stacija:** kopējiet failu Modern POS klienta starpnieka atrašanās vietā.

4. Atrast aparatūras stacijas paplašinājumu konfigurācijas failu. Faila nosaukums ir **HardwareStation.Extension.config:**

    - **Attālās aparatūras stacija:** fails atrodas IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Lokālā aparatūras stacija:** fails atrodas Modern POS klienta starpnieka atrašanās vietā.

5. Pievienojiet konfigurācijas faila **sastāva** sadaļai šādu sadaļu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Restartējiet aparatūras stacijas pakalpojumu:

    - **Attālā aparatūras stacija:** restartējiet aparatūras stacijas vietni no IIS pārvaldnieka.
    - **Lokālā aparatūras stacija:** beigt **dllhost.exe** procesu uzdevumu pārvaldniekā un pēc tam restartēt Modern POS.

## <a name="production-environment"></a>Ražošanas vide

Lai izveidotu izvietojamus iepakojumus, kas ietver Commerce komponentus, un piemēroiet šīs pakotnes ražošanas vidē, veiciet šos soļus:

1. Veiciet soļus, kas ir aprakstīti izstrādes [vides sadaļā iepriekš šajā](#development-environment) tēmā.
2. Mapē **RetailSdk Assets pakotnes konfigurācijas failos veiciet \\ tālāk norādītās** izmaiņas.

    - **Commerceruntime.ext.config un** **CommerceRuntime.MPOSOffline.Ext.config konfigurācijas failos pievienojiet šim sastāva** **sadaļai šādu** rindu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    - Konfigurācijas failā **HardwareStation.Extension.config** pievienojiet sastāva sadaļai **šādu** rindu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Mapē **BuildTools veiciet šādas** izmaiņas pielāgošanas.iestatījumu pakotnes **pielāgošanas konfigurācijas** failā:

    - Pievienojiet tālāk norādīto rindu, lai CRT ietvertu paplašinājumu izvietojamās pakotnēs.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    - Pievienojiet tālāk norādīto rindu, lai ietvertu aparatūras stacijas paplašinājumu izvietojamās pakotnēs.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Startējiet utilītai MSBuild komandu uzvedni un pēc tam Visual Studio **palaidiet msbuild mapē Retail** SDK, lai izveidotu izvietojamas pakotnes.
5. Piemērot iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet sadaļā [Izvietojamu pakotņu](../dev-itpro/retail-sdk/retail-sdk-packaging.md) izveide.

## <a name="design-of-extensions"></a>Paplašinājumu dizains

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Nolūks paplašinājumam, kas ir fiskālā dokumenta nodrošinātājs, ir izveidot printerim raksturīgus dokumentus un apstrādāt atbildes no fiskālā printera.

Paplašinājums CRT ir **Runtime.Extensions.DocumentProvider.EpsonFP90IISample.**

Papildinformāciju par fiskālās integrācijas risinājuma dizainu skatiet finanšu [reģistrācijas procesā un finanšu integrācijas paraugos finanšu ierīcēm.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Pieprasījumu **apdarinātājs DocumentProviderEpsonFP90III ir ieejas punkts pieprasījumam** ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest — šajā pieprasījumā ir ietverta** informācija par to, kurš dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālajā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest - šis pieprasījums atgriež notikumu sarakstu,** uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas **paplašinājuma** projekta konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- PVN kodu kartējums
- PVN likmju kartējums
- Norēķinu veida kartējums
- Ieejas plūsmas numura svītrkoda veids
- Depozīta maksājuma veids

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, nolūks ir sazināties ar fiskālo printeri.

Aparatūras **stacijas paplašinājums ir HardwareStation.Extension.EpsonFP90IIFiscalDeviceSample.** Šis paplašinājums izmanto HTTP protokolu, lai iesniegtu CRT dokumentus, ko paplašinājums ģenerē fiskālam printerim. Tā apstrādā arī atbildes, kas saņemtas no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EpsonFP90IISample pieprasījuma apdarinātājs ir ieejas punkts finanšu** perifērijas ierīču pieprasījumu apstrādei.

Apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest – šis pieprasījums sūta dokumentus printeriem un atgriež** atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas **paplašinājuma** projekta konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus savienotājam, kas tiks konfigurēts no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- **Galapunkta** adrese – printera URL.
- **Datuma un laika sinhronizācija – vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē** ar pievienoto aparatūras staciju.
