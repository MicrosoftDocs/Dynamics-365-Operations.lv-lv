---
title: Vācijas (mantojuma) finanšu reģistrācijas pakalpojuma integrācijas parauga izvietošanas vadlīnijas
description: Šajā rakstā ir sniegtas vadlīnijas par finanšu integrācijas parauga izvietošanu Vācijai no Microsoft Dynamics 365 Commerce Retail programmatūras izstrādes komplekta (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 9f6ecc715e10538806998459b7fd837648494ad7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845841"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Vācijas (mantojuma) finanšu reģistrācijas pakalpojuma integrācijas parauga izvietošanas vadlīnijas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegtas Microsoft Dynamics 365 Commerce vadlīnijas par finanšu reģistrācijas pakalpojumu integrācijas parauga izvietošanu Vācijā no mazumtirdzniecības programmatūras izstrādes komplekta (SDK) izstrādātāja virtuālās mašīnas (VM) Microsoft Dynamics pakalpojumā Lifecycle Services (LCS). Papildinformāciju par šo finanšu integrācijas paraugu skatiet Vācijas [finanšu reģistrācijas pakalpojuma integrācijas paraugs](emea-deu-fi-sample.md). 

Vācijas finanšu integrācijas paraugs ir daļa no sdk Retail. Informāciju par TO, kā instalēt un izmantot SDK, skatiet mazumtirdzniecības [programmatūras izstrādes komplekta (SDK) arhitektūru](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šis paraugs sastāv no Commerce Runtime () un aparatūras CRT stacijas paplašinājumiem. Lai palaistu šo paraugu, ir jāmodificē un jāveido aparatūras CRT stacijas projekti. Ieteicams izmantot nemodificētu komplektu Retail SDK, lai veiktu šajā rakstā aprakstītās izmaiņas. Iesakām izmantot arī avota kontroles sistēmu, piemēram, tādu Azure DevOps failu, kas vēl nav mainīti.

## <a name="development-environment"></a>Izstrādes vide

Izpildiet šīs darbības, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

### <a name="enable-commerce-runtime-extensions"></a>Iespējot Commerce izpildlaika paplašinājumus

Paplašinājuma CRT komponenti tiek iekļauti paraugos CRT. Lai izpildītu tālāk norādītās procedūras, atveriet **commerceRuntimeSamples.sln** **risinājumu zem RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample komponents

1. Atrast Runtime.Extensions.DocumentProvider.EFRSample **projektu** un veidot to.
2. Mapē Runtime.Extensions.DocumentProvider.EFRSample bin Debug **\\ atrodiet contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll montāžas\\ failu.** **·**
3. Kopēt montāžas failu uz CRT paplašinājumu mapi:

    - **Commerce Scale Unit:** kopējiet failu uz **\\ mapi bin\\ ext**, kas atrodas Interneta informācijas pakalpojumu (IIS) Commerce Scale Unit atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo **\\** mapi lokālā klienta starpnieka CRT atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**,**\\** un tā atrodas IIS Commerce Scale Unit vietas nodalījuma ārējā mapē.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

5. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponents

1. Atrast Runtime.Extensions.DocumentProvider.DataModelEFR **projektu** un izveidojiet to.
2. **Mapē Runtime.Extensions.DocumentProvider.DataModelEFR bin\\ Atkļūdošanas\\** atrast Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll **montāžas** failu.
3. Kopēt montāžas failu uz CRT paplašinājumu mapi:

    - **Commerce Scale Unit:** kopējiet failu uz **\\ mapi bin\\ ext**, kas atrodas IIS Commerce Scale Unit vietas atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo **\\** mapi lokālā klienta starpnieka CRT atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**,**\\** un tā atrodas IIS Commerce Scale Unit vietas nodalījuma ārējā mapē.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

5. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Paplašinājuma konfigurācijas fails

1. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**,**\\** un tā atrodas IIS Commerce Scale Unit vietas nodalījuma ārējā mapē.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

2. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Iespējot finanšu savienotāja paplašinājumus

Aparatūras staciju vai POS kases sistēmā [varat iespējot finanšu](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) savienotāja [paplašinājumus](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Iespējot aparatūras stacijas paplašinājumus

Aparatūras stacijas paplašinājuma komponenti ir ietverti aparatūras stacijas paraugos. Lai izpildītu tālāk norādītās procedūras, atveriet **hardwareStationSamples.sln** **risinājumu zem RetailSdk\\ SampleExtensions\\ HardwareStation**.

##### <a name="efrsample-component"></a>EFRSample komponents

1. Atrast HardwareStation.Extension.EFRSample **projektu** un veidot to.
2. Paplašinājuma.EFRSample **nodalījuma\\ atkļūdošanas\\** mapē atrodiet šādus montāžas failus:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopēt komplektācijas failus aparatūras stacijas paplašinājumu mapē:

    - **Koplietojamā aparatūras stacija:** kopējiet failus nodalījuma **mapē** IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Dedicated aparatūras stacija Modern POS: kopējiet** failus Modern POS klienta starpnieka atrašanās vietā.

4. Atrodiet aparatūras stacijas paplašinājumu konfigurācijas failu. Faila nosaukums ir **HardwareStation.Extension.config**.

    - **Koplietojamā aparatūras stacija:** fails atrodas IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Dedicated aparatūras stacija Modern POS:** fails atrodas Modern POS klienta starpnieka atrašanās vietā.

5. Pievienojiet konfigurācijas faila sastāva **sadaļai** šādu rindu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>Iespējot POS paplašinājumus

POS paplašinājuma paraugs atrodas src **FiscalIntegration\\ PosFiscalConnectorSample\\** mapē Solutions repository [Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

Lai mantojuma SDK izmantotu POS paplašinājuma paraugu, izpildiet šīs darbības.

1. Kopējiet **mapi Pos.Extension** uz mantojuma SDK POS **paplašinājumu** mapi (piemēram, `C:\RetailSDK\src\POS\Extensions`).
1. Pārdēvējiet **Pos.Extension mapes** **PosFiscalConnector kopiju**.
1. Noņemiet tālāk norādītās mapes un failus no **mapes PosFiscalConnector**:

    - nodalījums
    - DataService (datu pakalpojums)
    - devDependencies
    - Bibliotēkas
    - Obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. **Atveriet CloudPos.sln** vai **ModernPos.sln** risinājumu.
1. Projektā **Pos.Extensions** ietveriet mapi **PosFiscalConnector**.
1. Atveriet failu **extensions.json** un pievienojiet **paplašinājumu PosFiscalConnector**.
1. Veidot SDK.

### <a name="production-environment"></a>Ražošanas vide

Iepriekšējā procedūrā ir iespējoti paplašinājumi, kas ir fiskālās reģistrācijas pakalpojuma integrācijas parauga komponenti. Turklāt šīs darbības ir jāveic, lai izveidotu izvietojamas pakotnes, kurās ir Commerce komponenti, un lai piemērotu šīs pakotnes ražošanas vidē.

1. Mapē RetailSdk Assets pakotnes **konfigurācijas failos\\ veiciet tālāk norādītās** izmaiņas.

    - Commerceruntime.ext.config **un** CommerceRuntime.MPOSOffline.Ext.config **konfigurācijas** failos pievienojiet šim sastāva sadaļai šādas **rindas.**

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - Konfigurācijas failā **HardwareStation.Extension.config** saliācijas sadaļai pievienojiet šādas **rindas**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. **Mapē BuildTools veiciet šādas izmaiņas pielāgošanas.iestatījumu** pakotnes pielāgošanas **konfigurācijas** failā:

    - Pievienojiet tālāk norādītās rindas, lai ietvertu CRT paplašinājumus izvietojamās pakotnēs.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Pievienojiet tālāk norādītās rindas, lai ietvertu aparatūras stacijas paplašinājumus izvietojamās pakotnēs.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Startējiet utilītai MSBuild komandu Visual Studio uzvedni un palaidiet msbuild **mapē Retail SDK,** lai izveidotu izvietojamas pakotnes.
4. Piemērot iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet sadaļā [Izvietojamu pakotņu izveide](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Pabeidziet visus nepieciešamos iestatīšanas uzdevumus, kas aprakstīti sadaļā [Iestatīt Commerce for Vācijai](emea-deu-fi-sample.md#set-up-commerce-for-germany).

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Finanšu reģistrācijas pakalpojuma integrācijas paraugs Vācijai ir balstīts uz finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md). Papildinformāciju par fiskālās integrācijas risinājuma dizainu skatiet [finanšu integrācijas parauga dizaina apskatā](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Paplašinājuma, kas ir fiskālā dokumenta nodrošinātājs, nolūks ir izveidot pakalpojumiem raksturīgus dokumentus un apstrādāt atbildes no fiskālās reģistrācijas pakalpojuma.

Paplašinājums CRT ir **Runtime.Extensions.DocumentProvider.EFRSample**. Papildinformāciju par fiskālās integrācijas risinājuma dizainu skatiet tirdzniecības [kanālu finanšu integrācijas pārskatā](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Dokumentu nodrošinātājam DocumentProviderEFRFiscalDEU **ir viens pieprasījumu apdarinātājs**. Šis apdarinātājs tiek lietots finanšu dokumentu ģenerēšanai finanšu reģistrācijas pakalpojumam. Tas ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest —** šajā pieprasījumā ir ietverta informācija par to, kurš dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē finanšu reģistrācijas pakalpojumā.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** - šis pieprasījums atgriež atbildi kopā ar paplašinātiem datiem.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas **fails DocumentProviderFiscalEFRSampleGermany** **atrodas** paplašinājuma projekta konfigurācijas mapē. Šī faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

Ir pievienoti šādi iestatījumi:

- **PVN likmju kartēšana** - **nodokļu procentu vērtību kartēšana, kas ir iestatītas PVN kodiem uz taxG** (nodokļu grupas) atribūta vērtībām pieprasījumiem, kas tiek nosūtīti finanšu pakalpojumiem.
- **Dāvanu karšu un depozītu** nodokļu grupa – **TaxG** atribūta vērtība pieprasījumos, kas tiek sūtīti finanšu pakalpojumiem, balstoties uz operācijām, kurās ir iesaistītas dāvanu kartes vai depozītus.
- **Norēķinu veida kartēšana** — maksājuma metožu kartēšana **uz PayG** (maksājumu grupas) atribūta vērtībām pieprasījumos, kas tiek nosūtīti finanšu pakalpojumam.
- **Nodokļu grupa neapliekamiem** PVN – **TaxG** atribūta vērtība pieprasījumos, kas tiek nosūtīti finanšu pakalpojumiem, pamatojoties uz darbībām, kas ir atbrīvotas no nodokļu saistībām.
- **Iekļaut debitora** datus - ja šis parametrs ir ieslēgts, fiskālā pakalpojuma pieprasījumos būs iekļauta debitora informācija, piemēram, nosaukumi un adreses, gadījumos, kad debitoram tiek pievienots darbība.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar finanšu reģistrācijas pakalpojumu.

Aparatūras stacijas paplašinājums ir **HardwareStation.Extension.EFRSample**. Tas izmanto HTTP protokolu, lai iesniegtu dokumentus, CRT ko paplašinājums ģenerē finanšu reģistrācijas pakalpojumam. Tas apstrādā arī atbildes, kas saņemtas no fiskālās reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EFRHandler pieprasījumu** apdarinātājs ir ieejas punkts finanšu reģistrācijas pakalpojuma pieprasījumu apstrādei. Šis apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – šis pieprasījums nosūta dokumentus finanšu reģistrācijas pakalpojumam un atgriež atbildi no tā.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots fiskālās reģistrācijas pakalpojuma veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots, lai inicializētu finanšu reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas paplašinājuma **projekta** konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus finanšu savienotājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

Ir pievienoti šādi iestatījumi:

- **Galapunkta** adrese – finanšu reģistrācijas pakalpojuma URL.
- **Noildze** – laiks milisekundēs (ms), ko transporta vadītājs gaidīs uz finanšu reģistrācijas pakalpojuma atbildi.
- **Rādīt finanšu reģistrācijas paziņojumus — ja šis parametrs ir ieslēgts**, paziņojumi no finanšu pakalpojuma tiks rādīti POS kā lietotāja ziņojumi.

### <a name="pos-fiscal-connector-extension-design"></a>POS finanšu savienotāja paplašinājuma dizains

POS fiskālā savienotāja paplašinājuma mērķis ir sazināties ar POS finanšu reģistrācijas pakalpojumu. Sakaru vajadzībām tas izmanto HTTPS protokolu.

#### <a name="fiscal-connector-factory"></a>Fiskālais savienotāja rūpnīca

Fiskālā savienotāja rūpnīca kartē savienotāja **nosaukumu finanšu savienotāja ieviešanai un atrodas failā Pos.Extension\\ Connectors\\ FiscalConnectorFactory.ts**. Savienotāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

#### <a name="efr-fiscal-connector"></a>EFR finanšu savienotājs

EFR finanšu savienotājs atrodas **failā Pos.Extension\\ Connectors\\ Efr\\ EfrFiscalConnector.ts**. Tas ievieš **IFiscalConnector interfeisu**, kas atbalsta šādus pieprasījumus:

- **FiscalRegisterSubmitDocumentClientRequest** – šis pieprasījums nosūta dokumentus finanšu reģistrācijas pakalpojumam un atgriež atbildi no tā.
- **FiscalRegisterIsReadyClientRequest** – šis pieprasījums tiek izmantots finanšu reģistrācijas pakalpojuma veselības pārbaudei.
- **FiscalRegisterInitializeClientRequest** — šis pieprasījums tiek izmantots, lai inicializētu finanšu reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas **src\\ FiscalIntegration\\ Efr\\ Configurations Connectors\\ mapē** Solutions [Dynamics 365 Commerce repozitorijā](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Faila mērķis ir iespējot iestatījumus finanšu savienotājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- **Galapunkta** adrese – finanšu reģistrācijas pakalpojuma URL.
- **Taimauts** – laiks milisekundēs, ko savienotājs gaidīs uz finanšu reģistrācijas pakalpojuma atbildi.
