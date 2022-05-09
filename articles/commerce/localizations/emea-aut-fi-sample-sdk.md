---
title: Finanšu reģistrācijas pakalpojuma integrācijas parauga izvietošanas vadlīnijas Austrijai (mantojuma)
description: Šajā tēmā ir sniegtas vadlīnijas austrijas finanšu integrācijas parauga izvietošanai no mazumtirdzniecības Microsoft Dynamics 365 Commerce programmatūras izstrādes komplekta (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 7cb0e7b665add397b12e1a841b6a2e9565528d6d
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/19/2022
ms.locfileid: "8613940"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Finanšu reģistrācijas pakalpojuma integrācijas parauga izvietošanas vadlīnijas Austrijai (mantojuma)

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegtas vadlīnijas Microsoft Dynamics 365 Commerce finanšu reģistrācijas pakalpojumu integrācijas parauga izvietošanai Austrijā no Mazumtirdzniecības programmatūras izstrādes komplekta (SDK) izstrādātāja virtuālās mašīnas (VM) Microsoft Dynamics pakalpojumā Lifecycle Services (LCS). Papildinformāciju par šo finanšu integrācijas paraugu skatiet Austrijas [finanšu reģistrācijas pakalpojuma integrācijas paraugs](emea-aut-fi-sample.md). 

Austrijas finanšu integrācijas paraugs ir daļa no sdk Retail. Informāciju par TO, kā instalēt un izmantot SDK, skatiet mazumtirdzniecības [programmatūras izstrādes komplekta (SDK) arhitektūru](../dev-itpro/retail-sdk/retail-sdk-overview.md). Finanšu integrācijas paraugs sastāv no Commerce Runtime (CRT), Aparatūras stacijas un pārdošanas punkta (POS) paplašinājumiem. Lai palaistu šo paraugu, ir jāmodificē un jāizveido CRT aparatūras stacijas un POS projekti. Ieteicams izmantot nemodificētu komplektu Retail SDK, lai veiktu šajā tēmā aprakstītās izmaiņas. Iesakām izmantot arī avota kontroles sistēmu, piemēram, tādu Azure DevOps failu, kas vēl nav mainīti.

## <a name="development-environment"></a>Izstrādes vide

Izpildiet šīs darbības, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

### <a name="enable-commerce-runtime-extensions"></a>Iespējot Commerce izpildlaika paplašinājumus

Paplašinājuma CRT komponenti tiek iekļauti paraugos CRT. Lai izpildītu tālāk norādītās procedūras, **atveriet CommerceRuntimeSamples.sln** **risinājumu zem RetailSdkSampleExtensionsCommerceRuntime \\\\**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample komponents

1. Atrast Runtime.Extensions.DocumentProvider.EFRSample **projektu** un veidot to.
2. **Mapē Runtime.Extensions.DocumentProvider.EFRSamplebinDebug\\\\** **atrodiet contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll montāžas** failu.
3. Kopēt montāžas failu uz CRT paplašinājumu mapi:

    - **Commerce Scale Unit:** kopējiet failu uz **\\ binext\\** mapi, kas atrodas Interneta informācijas pakalpojumu (IIS) Commerce Scale Unit atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo **\\** mapi lokālā klienta starpnieka CRT atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**, un tā atrodas binext **\\ mapē, kas atrodas IIS Commerce Scale Unit vietas atrašanās** vietā.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

5. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponents

1. Atrast Runtime.Extensions.DocumentProvider.DataModelEFR **projektu** un izveidojiet to.
2. **Mapē Runtime.Extensions.DocumentProvider.DataModelEFRbinDebug\\\\** **atrodiet contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll montāžas** failu.
3. Kopēt montāžas failu uz CRT paplašinājumu mapi:

    - **Commerce Scale Unit:** kopējiet failu uz **\\ binext\\ mapi, kas** atrodas IIS Commerce Scale Unit vietas atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo **\\** mapi lokālā klienta starpnieka CRT atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**, un tā atrodas binext **\\ mapē, kas atrodas IIS Commerce Scale Unit vietas atrašanās** vietā.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

5. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Paplašinājuma konfigurācijas fails

1. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**, un tā atrodas binext **\\ mapē, kas atrodas IIS Commerce Scale Unit vietas atrašanās** vietā.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

2. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Iespējot finanšu savienotāja paplašinājumus

Aparatūras staciju vai POS kases sistēmā [varat iespējot finanšu](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) savienotāja [paplašinājumus](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Iespējot aparatūras stacijas paplašinājumus

Aparatūras stacijas paplašinājuma komponenti ir ietverti aparatūras stacijas paraugos. Lai izpildītu tālāk norādītās procedūras, atveriet **risinājumu HardwareStationSamples.sln** **zem RetailSdkSampleExtensionsHardwareStation\\\\**.

##### <a name="efrsample-component"></a>EFRSample komponents

1. Atrast HardwareStation.Extension.EFRSample **projektu** un veidot to.
2. **Mapē Extension.EFRSamplebinDebug\\\\** atrodiet šādus montāžas failus:

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

POS paplašinājuma paraugs atrodas **Solutions repository mapē srcFiscalIntegrationPosFiscalConnectorSample\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).

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

### <a name="enable-modern-pos-extension-components"></a>Iespējot Modern POS paplašinājuma komponentus

1. **Atveriet ModernPOS.sln** risinājumu zem **RetailSdkPOS\\** un pārliecinieties, ka to var kompilēt bez kļūdām. Turklāt pārliecinieties, vai moderno POS var palaist, Visual Studio izmantojot komandu **Palaist**.

    > [!NOTE]
    > Modern POS nevar pielāgot. Ir jāiespējo lietotāja konta kontrole (UAC), un jums pēc vajadzības jāatinstalē iepriekš instalētās Modern POS instances.

2. Iespējojiet paplašinājumu ielādēšanu, pievienojot paplašinājumiem.json **failā tālāk norādītās** rindas.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Papildinformāciju par paraugu, kuri parāda, kā iekļaut pirmkoda mapes un iespējot ielādēšanas paplašinājumus, skatiet readme.md **sadaļā Pos.Extensions** projekta instrukcijas.

3. Atjaunot risinājumu.
4. Atkļūdotāja izpildiet Modern POS un pārbaudiet funkcionalitāti.

### <a name="enable-cloud-pos-extension-components"></a>Iespējot Cloud POS paplašinājuma komponentus

1. **Atveriet CloudPOS.sln** risinājumu zem **RetailSdkPOS\\** un pārliecinieties, ka to var kompilēt bez kļūdām.
2. Iespējojiet paplašinājumu ielādēšanu, pievienojot paplašinājumiem.json **failā tālāk norādītās** rindas.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Papildinformāciju par paraugu, kuri parāda, kā iekļaut pirmkoda mapes un iespējot ielādēšanas paplašinājumus, skatiet readme.md **sadaļā Pos.Extensions** projekta instrukcijas.

3. Atjaunot risinājumu.
4. Palaidiet risinājumu, izmantojot komandu **Palaist un** izpildiet Retail SDK rokasgrāmatā norādītās darbības.

## <a name="production-environment"></a>Ražošanas vide

Iepriekšējā procedūra iespējo paplašinājumus, kas ir fiskālās reģistrācijas pakalpojuma integrācijas parauga komponenti. Turklāt šīs darbības ir jāveic, lai izveidotu izvietojamas pakotnes, kurās ir Commerce komponenti, un lai piemērotu šīs pakotnes ražošanas vidē.

1. Mapē RetailSdkAssets **veiciet \\ tālāk norādītās izmaiņas pakotnes konfigurācijas failos**:

    - Commerceruntime.ext.config **un** CommerceRuntime.MPOSOffline.Ext.config **konfigurācijas** failos pievienojiet šim sastāva sadaļai šādas **rindas.**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - Konfigurācijas failā **HardwareStation.Extension.config** pievienojiet sastāva sadaļai šādu **rindu**.

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

    - Pievienojiet tālāk norādīto rindu, lai ietvertu aparatūras stacijas paplašinājumu izvietojamās pakotnēs.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Startējiet utilītai MSBuild komandu Visual Studio uzvedni un palaidiet msbuild **mapē Retail SDK,** lai izveidotu izvietojamas pakotnes.
4. Piemērot iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet sadaļā [Izvietojamu pakotņu izveide](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Pabeidziet visus nepieciešamos iestatīšanas uzdevumus, kas aprakstīti [sadaļā Iestatīt Commerce for Austria](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Finanšu reģistrācijas pakalpojuma integrācijas paraugs Austrijai ir balstīts uz finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md). Papildinformāciju par fiskālās integrācijas risinājuma dizainu skatiet [finanšu integrācijas parauga dizaina apskatā](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Paplašinājuma, kas ir fiskālā dokumenta nodrošinātājs, nolūks ir izveidot pakalpojumiem raksturīgus dokumentus un apstrādāt atbildes no fiskālās reģistrācijas pakalpojuma.

Paplašinājums CRT ir **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Dokumentu nodrošinātājiem ir divi pieprasījumu apdarinātāji:

- **DocumentProviderEFRFiscalAUT** — šis apdarinātājs tiek izmantots, lai ģenerētu finanšu dokumentus finanšu reģistrācijas pakalpojumam.
- **DocumentProviderEFRNonFiscalAUT — šis apdarinātājs** tiek izmantots, lai finanšu reģistrācijas pakalpojumam ģenerētu dokumentus, kas nav finanšu dokumenti.

Šie apdarinātāji ir pārmantoti no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest —** šajā pieprasījumā ir ietverta informācija par to, kurš dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē finanšu reģistrācijas pakalpojumā.
- **GetNonFiscalDocumentDocumentProviderRequest** – šajā pieprasījumā ir ietverta informācija par to, kas ir jāģenerē ar fiskālo dokumentu. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē finanšu reģistrācijas pakalpojumā.
- **GetSupportedRegistrableEventsDocumentProviderRequest** - šis pieprasījums atgriež notikumu sarakstu, uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana, Z pārskata drukāšana, debitoru kontu depozīti, debitoru pasūtījumu depozīti, audita notikumi un darbības, kas nav pārdošanas darbības.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** - šis pieprasījums atgriež atbildi no finanšu reģistrācijas pakalpojuma. Šī atbilde ir serializēta, lai veidotu virkni tā, lai tā būtu gatava saglabāt.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas faili atrodas paplašinājuma **projekta** konfigurācijas mapē:

- **DocumentProviderFiscalEFRSampleAustria** — finanšu dokumentiem.
- **DocumentProviderNonFiscalEFRSampleAustria** – ar finanšu dokumentiem nesaistītiem dokumentiem.

Šo failu mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Tiek pievienots šāds iestatījums:

- PVN likmju kartējums

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Fiskālā savienotāja paplašinājuma mērķis ir sazināties ar finanšu reģistrācijas pakalpojumu. Aparatūras stacijas paplašinājums ir nosaukts **HardwareStation.Extension.EFRSample**. Tas izmanto HTTP vai HTTPS protokolu, lai iesniegtu dokumentus, ko CRT paplašinājums ģenerē finanšu reģistrācijas pakalpojumam. Tas apstrādā arī atbildes, kas saņemtas no fiskālās reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EFRHandler pieprasījumu** apdarinātājs ir ieejas punkts finanšu reģistrācijas pakalpojuma pieprasījumu apstrādei.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – šis pieprasījums nosūta dokumentus finanšu reģistrācijas pakalpojumam un atgriež atbildi no tā.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots fiskālās reģistrācijas pakalpojuma veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots, lai inicializētu finanšu reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas paplašinājuma **projekta** konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus finanšu savienotājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- **Galapunkta** adrese – finanšu reģistrācijas pakalpojuma URL.
- **Noildze** – laiks milisekundēs, ko autovadītājs gaidīs uz finanšu reģistrācijas pakalpojuma atbildi.

### <a name="pos-fiscal-connector-extension-design"></a>POS finanšu savienotāja paplašinājuma dizains

POS fiskālā savienotāja paplašinājuma mērķis ir sazināties ar POS finanšu reģistrācijas pakalpojumu. Sakaru vajadzībām tas izmanto HTTPS protokolu.

#### <a name="fiscal-connector-factory"></a>Fiskālais savienotāja rūpnīca

Fiskālā savienotāja rūpnīca kartē savienotāja **nosaukumu finanšu savienotāja ieviešanai un atrodas failā Pos.ExtensionConnectorsFiscalConnectorFactory.ts\\\\**. Savienotāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

#### <a name="efr-fiscal-connector"></a>EFR finanšu savienotājs

EFR finanšu savienotājs ir novietots **failā Pos.ExtensionConnectorsEfrEfrFiscalConnector.ts\\\\\\**. Tas ievieš **IFiscalConnector interfeisu**, kas atbalsta šādus pieprasījumus:

- **FiscalRegisterSubmitDocumentClientRequest** – šis pieprasījums nosūta dokumentus finanšu reģistrācijas pakalpojumam un atgriež atbildi no tā.
- **FiscalRegisterIsReadyClientRequest** – šis pieprasījums tiek izmantots finanšu reģistrācijas pakalpojuma veselības pārbaudei.
- **FiscalRegisterInitializeClientRequest** — šis pieprasījums tiek izmantots, lai inicializētu finanšu reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas **srcFiscalIntegrationEfrConfigurationsConnectors\\\\\\\\**[Dynamics 365 Commerce mapē Solutions repository.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot iestatījumus finanšu savienotājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- **Galapunkta** adrese – finanšu reģistrācijas pakalpojuma URL.
- **Taimauts** – laiks milisekundēs, ko savienotājs gaidīs uz finanšu reģistrācijas pakalpojuma atbildi.
