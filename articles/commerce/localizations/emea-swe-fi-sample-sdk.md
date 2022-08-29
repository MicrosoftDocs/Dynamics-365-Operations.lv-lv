---
title: Izvietošanas vadlīnijas kontroles vienības integrācijas paraugs Zviedrijai (mantotais)
description: Šajā rakstā ir sniegtas vadlīnijas par kontroles vienību integrācijas parauga izvietošanu Zviedrijā no Retail SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: fcc35a2203641b24fe4edd2ab34f2e4d5db9bb53
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324302"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Izvietošanas vadlīnijas kontroles vienības integrācijas paraugs Zviedrijai (mantotais)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegtas vadlīnijas par kontroles vienības integrācijas parauga izvietošanu Zviedrijā no mazumtirdzniecības programmatūras izstrādes komplekta (SDK) izstrādātāja virtuālās mašīnas (VM) Microsoft Dynamics pakalpojumos Lifecycle Services (LCS). Papildinformāciju par šo finanšu integrācijas paraugu skatiet Zviedrijas [kontroles vienību integrācijas paraugs](emea-swe-fi-sample.md). 

Zviedrijas finanšu integrācijas paraugs ir daļa no sdk Retail. Informāciju par TO, kā instalēt un izmantot SDK, skatiet mazumtirdzniecības [programmatūras izstrādes komplekta (SDK) arhitektūru](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šis paraugs sastāv no Commerce Runtime (CRT), Aparatūras stacijas un pārdošanas punkta (POS) paplašinājumiem. Lai palaistu šo paraugu, ir jāmodificē un jāizveido CRT aparatūras stacijas un POS projekti. Ieteicams izmantot nemodificētu komplektu Retail SDK, lai veiktu šajā rakstā aprakstītās izmaiņas. Iesakām izmantot arī avota kontroles sistēmu, piemēram, tādu Azure DevOps failu, kas vēl nav mainīti.

## <a name="development-environment"></a>Izstrādes vide

Izpildiet šīs darbības, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

### <a name="enable-crt-extensions"></a>Iespējot CRT paplašinājumus

Paplašinājuma CRT komponenti tiek iekļauti paraugos CRT. Lai izpildītu tālāk norādītās procedūras, atveriet **commerceRuntimeSamples.sln** **risinājumu zem RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample komponents

1. Atrast Runtime.Extensions.DocumentProvider.CleanCashSample **projektu** un veidot to.
2. Mapē Runtime.Extensions.DocumentProvider.CleanCashSample bin Debug **\\ atrodiet montāžas failu Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll\\.** **·**
3. Kopēt montāžas failu uz CRT paplašinājumu mapi:

    - **Commerce Scale Unit:** kopējiet failu uz **\\ mapi bin\\ ext**, kas atrodas Interneta informācijas pakalpojumu (IIS) Commerce Scale Unit atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo **\\** mapi lokālā klienta starpnieka CRT atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**,**\\** un tā atrodas IIS Commerce Scale Unit vietas nodalījuma ārējā mapē.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

5. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Paplašinājuma konfigurācijas fails

1. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir commerceruntime.ext.config**,**\\** un tā atrodas IIS Commerce Scale Unit vietas nodalījuma ārējā mapē.
    - **Modern CRT POS lokāls:** faila **nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas vietējā klienta starpnieka atrašanās CRT vietā.

2. Reģistrēt izmaiņas CRT paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Iespējot aparatūras stacijas paplašinājumus

Aparatūras stacijas paplašinājuma komponenti ir ietverti aparatūras stacijas paraugos. Lai izpildītu tālāk norādītās procedūras, atveriet **hardwareStationSamples.sln** **risinājumu zem RetailSdk\\ SampleExtensions\\ HardwareStation**.

#### <a name="cleancash-component"></a>CleanCash komponents

1. Atrast project **HardwareStation.Extension.CleanCashSample** un veidot to.
2. **Mapē Extension.CleanCashSample\\ bin\\ Debug** **atrodiet Contoso.Commerce.HardwareStation.CleanCashSample.dll** un **Interop.CleanCash\_ 1 1.dll\_** montāžas failus.
3. Kopēt komplektācijas failus aparatūras stacijas paplašinājumu mapē:

    - **Koplietojamā aparatūras stacija:** kopējiet failus nodalījuma **mapē** IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Dedicated aparatūras stacija Modern POS: kopējiet** failus Modern POS klienta starpnieka atrašanās vietā.

4. Atrodiet aparatūras stacijas paplašinājumu konfigurācijas failu. Faila nosaukums ir **HardwareStation.Extension.config**.

    - **Koplietojamā aparatūras stacija:** fails atrodas IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Dedicated aparatūras stacija Modern POS:** fails ir Modern POS klienta starpnieka atrašanās vietā.

5. Pievienojiet konfigurācijas faila sastāva **sadaļai** šādu rindu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Iespējot Modern POS paplašinājuma komponentus

1. **Atveriet ModernPOS.sln** risinājumu zem **RetailSdk\\ POS** un pārliecinieties, ka to var kompilēt bez kļūdām. Turklāt pārliecinieties, vai moderno POS var palaist, Visual Studio izmantojot komandu **Palaist**.

    > [!NOTE]
    > Modern POS nevar pielāgot. Ir jāiespējo lietotāja konta kontrole (UAC), un jums pēc vajadzības jāatinstalē iepriekš instalētās Modern POS instances.

2. Iespējojiet paplašinājumus, kas ir jāielādē, pievienojot paplašinājumiem.json **failam tālāk norādītās** rindas.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Papildinformāciju par paraugu, kuri parāda, kā iekļaut pirmkoda mapes un iespējot ielādēšanas paplašinājumus, skatiet readme.md **sadaļā Pos.Extensions** projekta instrukcijas.

3. Atjaunot risinājumu.
4. Atkļūdotāja izpildiet Modern POS un pārbaudiet funkcionalitāti.

### <a name="enable-cloud-pos-extension-components"></a>Iespējot Cloud POS paplašinājuma komponentus

1. **Atveriet CloudPOS.sln** risinājumu sistēmā **RetailSdk\\ POS** un pārliecinieties, ka to var kompilēt bez kļūdām.
2. Iespējojiet paplašinājumus, kas ir jāielādē, pievienojot paplašinājumiem.json **failam tālāk norādītās** rindas.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Papildinformāciju par paraugu, kuri parāda, kā iekļaut pirmkoda mapes un iespējot ielādēšanas paplašinājumus, skatiet readme.md **sadaļā Pos.Extensions** projekta instrukcijas.

3. Atjaunot risinājumu.
4. Palaidiet risinājumu, izmantojot komandu **Palaist un** izpildiet Retail SDK rokasgrāmatā norādītās darbības.

## <a name="production-environment"></a>Ražošanas vide

Iepriekšējā procedūra iespējo paplašinājumus, kas ir kontroles vienības integrācijas parauga komponenti. Turklāt šīs darbības ir jāveic, lai izveidotu izvietojamas pakotnes, kurās ir Commerce komponenti, un lai piemērotu šīs pakotnes ražošanas vidē.

1. Mapē RetailSdk Assets pakotnes **konfigurācijas failos\\ veiciet tālāk norādītās** izmaiņas.

    - Commerceruntime.ext.config **un** CommerceRuntime.MPOSOffline.Ext.config **konfigurācijas** failos pievienojiet šim sastāva sadaļai šādas **rindas.**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Konfigurācijas failā **HardwareStation.Extension.config** pievienojiet sastāva sadaļai šādu **rindu**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. **Mapē BuildTools veiciet šādas izmaiņas pielāgošanas.iestatījumu** pakotnes pielāgošanas **konfigurācijas** failā:

    - Pievienojiet tālāk norādīto rindu, lai ietvertu CRT paplašinājumus izvietojamās pakotnēs.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Pievienojiet tālāk norādītās rindas, lai ietvertu aparatūras stacijas paplašinājumu izvietojamās pakotnēs.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Iespējojiet POS paplašinājumu, pievienojot tālāk norādītās rindas **failā extensions.json** zem mapes **RetailSDK\\ POS\\ paplašinājumi**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Startējiet utilītai MSBuild komandu Visual Studio uzvedni un palaidiet msbuild **mapē Retail SDK,** lai izveidotu izvietojamas pakotnes.
5. Piemērot iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet sadaļā [Izvietojamu pakotņu izveide](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Veiciet visus nepieciešamos iestatīšanas uzdevumus, kas aprakstīti [sadaļā Integrācijas iestatīšana ar kontroles vienībām](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Paplašinājumu dizains

### <a name="crt-extension-design"></a>CRT paplašinājuma dizains

Paplašinājuma, kas ir fiskālā dokumenta nodrošinātājs, nolūks ir izveidot pakalpojumiem raksturīgus dokumentus un apstrādāt atbildes no kontroles vienības.

Paplašinājums CRT ir **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Papildinformāciju par fiskālās integrācijas risinājuma dizainu skatiet finanšu [reģistrācijas procesā un finanšu integrācijas paraugos fiskālajām ierīcēm un pakalpojumiem](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Dokumentu nodrošinātājam ir **atsevišķs DocumentProviderCleanCash** pieprasījumu apdarinātājs. Šis apdarinātājs tiek izmantots, lai ģenerētu kontroles vienībai finanšu dokumentus.

Šis apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest —** šajā pieprasījumā ir ietverta informācija par to, kurš dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē kontroles vienībā.
- **GetSupportedRegistrableEventsDocumentProviderRequest** - šis pieprasījums atgriež notikumu sarakstu, uz kuriem ir jāabonē. Pašlaik tiek atbalstīti pārdošanas notikumi un audita notikumi.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas **fails DocumentProviderFiscalCleanCashSample** **atrodas** paplašinājuma projekta konfigurācijas mapē. Šī faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- PVN kodu kartējums

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, nolūks ir sazināties ar kontroles vienību.

Aparatūras stacijas paplašinājums **ir HardwareStation.Extension.CleanCashSample**. Tas izmanto HTTP protokolu, lai iesniegtu dokumentus CRT, ko paplašinājums ģenerē kontroles vienībai. Tā apstrādā arī atbildes, kas saņemtas no kontroles vienības.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

CleanCashHandler **pieprasījumu apdarinātājs** ir ieejas punkts vadības vienības pieprasījumu apstrādei.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – šis pieprasījums sūta dokumentus kontroles vienībai un atgriež atbildi no tās.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots kontroles vienības veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – šis pieprasījums tiek izmantots, lai inicializētu kontroles vienību.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas paplašinājuma **projekta** konfigurācijas mapē. Faila mērķis ir iespējot iestatījumus finanšu savienotājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- **Savienojumu virkne** – vadības vienības savienojuma iestatījumi.
- **Noildze** – laiks milisekundēs, ko autovadītājs gaidīs uz kontroles vienības atbildi.

## <a name="migrating-from-the-earlier-integration-sample"></a>Migrē no agrākā integrācijas parauga

Ja agrāko paraugu izmantojat [POS integrācijai ar Zviedrijas kontroles](retail-sdk-control-unit-sample.md) vienībām, iespējams, ir jāmigrē no tā uz pašreizējo integrācijas paraugu. Lai uzstāt izmaiņas un saņemtu laicīgus atjauninājumus zviedrijas līdzekļiem nākotnē, iespējams, būs jāveic papildkods un jāveic konfigurācijas pielāgojumi paplašinājumos, kas tiek veidoti, un no jauna jāveido risinājumi. Izveidotā paplašinājuma loģikā nav nepieciešamas galvenās izmaiņas. Agrākais integrācijas paraugs un pielāgojumi turpinās darboties, ja no savas puses nav veiktas izmaiņas. Tāpēc varat plānot, sagatavoties un uzņemšanu jūsu vidē.

### <a name="migration-process"></a>Migrācijas process

Migrācijai no agrākā integrācijas parauga uz pašreizējo kontroles vienības integrācijas paraugu ir jābūt balstītai uz atjaunināšanas koncepcijas. Citiem vārdiem sakot, pirms POS un aparatūras stacijas komponentu atjaunināšanas ir jau jābūt atjauninātiem visiem Commerce Headquarters un Commerce Scale Unit komponentiem.

Lai palīdzētu novērst situāciju, kad notikums vai darbība ir parakstīta divreiz (t. i., to parakstīja gan agrākais paplašinājums, gan pašreizējais paplašinājums) vai gadījumos, kad notikumu vai transakciju nevar parakstīt trūkstošās konfigurācijas dēļ, ieteicams izslēgt visas POS un aparatūras stacijas ierīces, kas izmanto agrāko paraugu. un pēc tam atjauniniet tos vienlaicīgi. Šo vienlaicīgu atjaunināšanu var veikt, piemēram, veikalā pa veikalam atjauninot veikala funkcionalitātes profilu un Aparatūras stacijas aparatūras profilu.

Migrācijas procesā ir jāietver šādi soļi.

1. Atjaunināt Commerce Headquarters komponentus.
1. Atjauniniet Commerce Scale Unit komponentus un iespējojiet pašreizējā parauga paplašinājumus.
1. Pārliecinieties, vai visas bezsaistes darbības ir sinhronizētas no bezsaistes iespējotām MPOS ierīcēm.
1. Izslēdziet visas ierīces, kas izmanto iepriekšējā parauga komponentus.
1. Veiciet visus nepieciešamos iestatīšanas uzdevumus, kas aprakstīti [sadaļā Integrācijas iestatīšana ar kontroles vienībām](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Atjauniniet POS un aparatūras stacijas komponentus, atspējojiet paplašinājumus, kas ir agrāka parauga daļa, un iespējojiet pašreizējā parauga paplašinājumus.

    > [!NOTE]
    > Atkarībā no vides tipa, jūs varat atrast tehnisko informāciju par migrācijas procesu vai nu sadaļā Migrācija attīstības vides sadaļā, [...](#migration-in-a-development-environment)[vai](#migration-in-a-production-environment) migrāciju šī raksta ražošanas vides sadaļā.

### <a name="migration-in-a-development-environment"></a>Migrācija izstrādes vidē

#### <a name="update-crt"></a>Labot CRT

1. Atrast Runtime.Extensions.DocumentProvider.CleanCashSample **projektu** un veidot to.
2. Mapē Runtime.Extensions.DocumentProvider.CleanCashSample bin Debug **\\ atrodiet montāžas failu Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll\\.** **·**
3. Kopēt montāžas failu uz CRT paplašinājumu mapi:

    - **Commerce Scale Unit:** kopējiet failu uz **\\ mapi bin\\ ext**, kas atrodas IIS Commerce Scale Unit vietas atrašanās vietā.
    - **Lokāls CRT vai Modern POS:** kopējiet failu uz ārējo **\\** mapi lokālā klienta starpnieka CRT atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu šim CRT:

    - **Commerce Scale Unit:** faila **nosaukums ir CommerceRuntime.ext.config**,**\\** un tā vieta atrodas IIS Commerce Scale Unit vietas nodalījuma ārējā mapē.
    - **Modern CRT POS lokāls:** **faila nosaukums ir CommerceRuntime.MPOSOffline.Ext.config**, un tā ir nodalījuma ārējā mapē zem lokālā klienta starpnieka atrašanās **\\** CRT vietas.

    > [!WARNING]
    > Nerediģēt **failus** CommerceRuntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

5. Atrodiet un noņemiet agrāko CRT paplašinājumu no paplašinājuma konfigurācijas faila.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Šī darbība nav jāveic līdz brīdim, kad atjaunināsiet visas POS ierīces, kas darbojas ar šo instanci CRT.

6. Reģistrējiet pašreizējos CRT parauga paplašinājumus paplašinājuma konfigurācijas failā, pievienojot šādas rindas.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Atjaunināt aparatūras staciju

1. Atrast project **HardwareStation.Extension.CleanCashSample** un veidot to.
2. **Mapē Extension.CleanCashSample\\ bin\\ Debug** **atrodiet Contoso.Commerce.HardwareStation.CleanCashSample.dll** un **Interop.CleanCash\_ 1 1.dll\_** montāžas failus.
3. Kopēt komplektācijas failus aparatūras stacijas paplašinājumu mapē:

    - **Koplietojamā aparatūras stacija:** kopējiet failus nodalījuma **mapē** IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Dedicated aparatūras stacija Modern POS: kopējiet** failus Modern POS klienta starpnieka atrašanās vietā.

4. **Atrast HardwareStation.Extension.config paplašinājuma** konfigurācijas failu:

    - **Attālās aparatūras stacija:** fails atrodas IIS aparatūras stacijas vietnes atrašanās vietā.
    - **Lokālā aparatūras stacija Modern POS:** fails ir Modern POS klienta starpnieka atrašanās vietā.

    > [!WARNING]
    > Nerediģēt **failus** CommerceRuntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

5. Atrodiet un noņemiet agrāko aparatūras stacijas paplašinājumu no paplašinājuma konfigurācijas faila.

    # <a name="retail-73-and-earlier"></a>[Mazumtirdzniecība 7.3 un agrāka](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 vai jaunāka versija](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Mazumtirdzniecība 10.0 un jaunāka versija](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Pievienojiet šādu rindu paplašinājuma **konfigurācijas** faila sastāva sadaļai.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Atjaunināt Modern POS

1. **Atveriet CloudPOS.sln risinājumu** sistēmā **RetailSdk\\ POS**.
2. Atspējojiet agrāko POS paplašinājumu, noņemot tālāk norādītās rindas no **faila extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Iespējojiet pašreizējo POS paplašinājuma paraugu, paplašinājumu.json **failā pievienojot tālāk norādītās** rindas.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Atjaunināt Cloud POS

1. **Atveriet ModernPOS.sln risinājumu** zem **RetailSdk\\ POS**.
2. Atspējojiet agrāko POS paplašinājumu, noņemot tālāk norādītās rindas no **faila extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Iespējojiet pašreizējo POS paplašinājuma paraugu, paplašinājumu.json **failā pievienojot tālāk norādītās** rindas.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Migrācija ražošanas vidē

#### <a name="update-crt"></a>Labot CRT

1. Noņemiet agrāko CRT **paplašinājumu no commerceRuntime.ext.config** un **CommerceRuntime.MPOSOffline.Ext.config** **konfigurācijas failiem zem mapes RetailSdk\\ Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Šī darbība nav jāveic līdz brīdim, kad atjaunināsiet visas POS ierīces, kas darbojas ar šo instanci CRT.

2. Iespējojiet pašreizējos CRT parauga paplašinājumus **, veicot tālāk norādītās izmaiņas commerceRuntime.ext.config** **un CommerceRuntime.MPOSOffline.Ext.config konfigurācijas** **failos, kas atrodas mapē RetailSdk\\ Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Pielāgojumu.iestatījumu **pakotnes pielāgošanas** konfigurācijas **failā zem mapes BuildTools** pievienojiet tālāk norādīto rindu, lai ietvertu pašreizējo parauga CRT paplašinājumu izvietojamās pakotnēs.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Atjaunināt aparatūras staciju

1. Noņemiet agrāko aparatūras stacijas paplašinājumu, modificējot **konfigurācijas failu HardwareStation.Extension.config**.

    # <a name="retail-73-and-earlier"></a>[Mazumtirdzniecība 7.3 un agrāka](#tab/retail-7-3)

    Noņemiet šo sadaļu no **HardwareStation.Shared.config** un **HardwareStation.Dedicated.config** konfigurācijas failiem.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 vai jaunāka versija](#tab/retail-7-3-1)

    Noņemiet šo sadaļu no **HardwareStation.Extension.config** konfigurācijas faila.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Mazumtirdzniecība 10.0 un jaunāka versija](#tab/retail-10-0)

    Noņemiet šo sadaļu no **HardwareStation.Extension.config** konfigurācijas faila.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Iespējojiet pašreizējo aparatūras stacijas **paplašinājuma** **paraugu, pievienojot konfigurācijas failam HardwareStation.Extension.config sastāvam šādu** rindu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. **Mapē BuildTools veiciet šādas izmaiņas pielāgošanas.iestatījumu** pakotnes pielāgošanas **konfigurācijas** failā:

    - Noņemiet tālāk norādīto rindu, lai izslēgtu agrāko aparatūras stacijas paplašinājumu no izvietojamām pakotnēm.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Pievienojiet tālāk norādītās rindas, lai ietvertu pašreizējo aparatūras stacijas paplašinājuma paraugu izvietojamās pakotnēs.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Atjaunināt Modern POS

1. **Atveriet CloudPOS.sln risinājumu** retailSdk **\\ POS**.
2. Atspējot agrāko POS paplašinājumu:

    - Failā tsconfig.json **izslēgšanas** sarakstam pievienojiet mapi FiscalRegisterSample **.**
    - Noņemiet tālāk norādītās rindas no **paplašinājumiem.json** faila mapē **RetailSDK\\ POS\\ paplašinājumi**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Iespējojiet pašreizējo PARAUGA POS paplašinājumu, **pievienojot tālāk norādītās rindas paplašinājumiem.json** failā **zem mapes RetailSDK\\ POS\\ paplašinājumi**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Atjaunināt Cloud POS

1. **Atveriet ModernPOS.sln risinājumu** zem **RetailSdk\\ POS**.
2. Atspējot agrāko POS paplašinājumu:

    - Failā tsconfig.json **izslēgšanas** sarakstam pievienojiet mapi FiscalRegisterSample **.**
    - Noņemiet tālāk norādītās rindas no **paplašinājumiem.json** faila mapē **RetailSDK\\ POS\\ paplašinājumi**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Iespējojiet pašreizējo PARAUGA POS paplašinājumu, **pievienojot tālāk norādītās rindas paplašinājumiem.json** failā **zem mapes RetailSDK\\ POS\\ paplašinājumi**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>Izvietojamu pakotņu izveide

Palaidiet **msbuild visam** Retail SDK, lai izveidotu izvietojamas pakotnes. Piemērot iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet mazumtirdzniecības [SDK iepakojumos](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
