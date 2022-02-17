---
title: Izvēršanas vadlīnijas vadības bloku integrācijas paraugam Zviedrijai (mantots)
description: Šajā tēmā ir sniegtas vadlīnijas vadības bloka integrācijas parauga izvietošanai Zviedrijai no mazumtirdzniecības SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: b8d60f32d986dec6bb26d78ebdfe8cee3a6b688a
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077042"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Izvēršanas vadlīnijas vadības bloku integrācijas paraugam Zviedrijai (mantots)

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegtas vadlīnijas vadības bloka integrācijas parauga izvietošanai Zviedrijai no mazumtirdzniecības programmatūras izstrādes komplekta (SDK) izstrādātāja virtuālajā mašīnā (VM)Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Papildinformāciju par šo fiskālās integrācijas paraugu skatiet [Vadības bloka integrācijas paraugs Zviedrijai](emea-swe-fi-sample.md). 

Zviedrijas fiskālās integrācijas paraugs ir daļa no mazumtirdzniecības SDK. Informāciju par SDK instalēšanu un lietošanu skatiet sadaļā [Mazumtirdzniecības programmatūras izstrādes komplekta (SDK) arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šis paraugs sastāv no Commerce izpildlaika paplašinājumiem (CRT), Aparatūras stacija un tirdzniecības vieta (POS). Lai palaistu šo paraugu, jums ir jāmaina un jāveido CRT, Aparatūras stacija un POS projekti. Lai veiktu šajā tēmā aprakstītās izmaiņas, ieteicams izmantot nepārveidotu mazumtirdzniecības SDK. Mēs arī iesakām izmantot avota kontroles sistēmu, piemēram,Azure DevOps kur neviens fails vēl nav mainīts.

## <a name="development-environment"></a>Izstrādes vide

Veiciet šīs darbības, lai iestatītu izstrādes vidi, lai varētu pārbaudīt un paplašināt paraugu.

### <a name="enable-crt-extensions"></a>Iespējot CRT paplašinājumi

The CRT paplašinājuma komponenti ir iekļauti CRT paraugi. Lai pabeigtu tālāk norādītās procedūras, atveriet **CommerceRuntimeSamples.sln** risinājums zem **RetailSdk\\ Extensions paraugi\\ CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample komponents

1. Atrodi **Runtime.Extensions.DocumentProvider.CleanCashSample** projektu un uzbūvēt to.
2. Iekš **Runtime.Extensions.DocumentProvider.CleanCashSample\\ atkritumu tvertne\\ Atkļūdošana** mapi, atrodiet **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** montāžas fails.
3. Kopējiet montāžas failu uz CRT paplašinājumu mape:

    - **Tirdzniecības mēroga vienība:** Kopējiet failu uz **\\ atkritumu tvertne\\ ext** mapē Interneta informācijas pakalpojumu (IIS) Commerce Scale Unit vietnes atrašanās vietā.
    - **Vietējais CRT Mūsdienu POS:** Kopējiet failu uz **\\ ext** mape zem vietējā CRT klienta brokera atrašanās vieta.

4. Atrodiet paplašinājuma konfigurācijas failu CRT:

    - **Tirdzniecības mēroga vienība:** Fails ir nosaukts **commerceruntime.ext.config**, un tas atrodas **atkritumu tvertne\\ ext** mapi zem IIS Commerce Scale Unit vietnes atrašanās vietas.
    - **Vietējais CRT Mūsdienu POS:** Fails ir nosaukts **CommerceRuntime.MPOSOffline.Ext.config**, un tas ir zem vietējā CRT klienta brokera atrašanās vieta.

5. Reģistrējieties CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Paplašinājuma konfigurācijas fails

1. Atrodiet paplašinājuma konfigurācijas failu CRT:

    - **Tirdzniecības mēroga vienība:** Fails ir nosaukts **commerceruntime.ext.config**, un tas atrodas **atkritumu tvertne\\ ext** mapi zem IIS Commerce Scale Unit vietnes atrašanās vietas.
    - **Vietējais CRT Mūsdienu POS:** Fails ir nosaukts **CommerceRuntime.MPOSOffline.Ext.config**, un tas ir zem vietējā CRT klienta brokera atrašanās vieta.

2. Reģistrējieties CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Iespējot aparatūras staciju paplašinājumus

Aparatūras stacijas paplašinājuma komponenti ir iekļauti aparatūras stacijas paraugos. Lai pabeigtu tālāk norādītās procedūras, atveriet **HardwareStationSamples.sln** risinājums zem **RetailSdk\\ Extensions paraugi\\ HardwareStation**.

#### <a name="cleancash-component"></a>CleanCash komponents

1. Atrodi **HardwareStation.Extension.CleanCashSample** projektu un uzbūvēt to.
2. Iekš **Extension.CleanCashSample\\ atkritumu tvertne\\ Atkļūdošana** mapi, atrodiet **Contoso.Commerce.HardwareStation.CleanCashSample.dll** un **Interop.CleanCash\_ 1\_ 1.dll** montāžas faili.
3. Kopējiet montāžas failus mapē Aparatūras stacijas paplašinājumi:

    - **Koplietojama aparatūras stacija:** Kopējiet failus uz **atkritumu tvertne** mapi zem IIS aparatūras stacijas vietnes atrašanās vietas.
    - **Īpaša aparatūras stacija modernajā POS:** Kopējiet failus uz Modern POS klienta brokera atrašanās vietu.

4. Atrodiet aparatūras stacijas paplašinājumu konfigurācijas failu. Faila nosaukums **ir HardwareStation.Extension.config**.

    - **Koplietojama aparatūras stacija:** fails atrodas IIS aparatūras stacijas atrašanās vietā.
    - **Īpaša aparatūras stacija modern pos:** fails atrodas Modern POS klienta brokera atrašanās vietā.

5. Pievienojiet konfigurācijas faila kompozīcijas **sadaļai** šādu rindu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Iespējot modernos POS paplašinājuma komponentus

1. **Atveriet ModernPOS.sln** risinājumu sadaļā **RetailSdk\\POS** un pārliecinieties, ka to var apkopot bez kļūdām. Turklāt pārliecinieties, vai modern pos Visual Studio var palaist, **izmantojot komandu Palaist**.

    > [!NOTE]
    > Modern POS nedrīkst pielāgot. Ir jāiespējo lietotāja konta kontrole (User Account Control — UAC), un pēc vajadzības ir jāatinstalē iepriekš instalētie modern POS gadījumi.

2. Iespējojiet ielādējamos paplašinājumus, failā **extensions.json** pievienojot šādas rindas.

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
    > Papildinformāciju un paraugus, kas parāda, kā iekļaut pirmkoda mapes un iespējot paplašinājumu ielādi, skatiet projekta Pos.Extensions **faila** readme.md norādījumus.

3. Pārbūvējiet risinājumu.
4. Atkļūdošanā palaidiet Modern POS un pārbaudiet funkcionalitāti.

### <a name="enable-cloud-pos-extension-components"></a>Mākoņa POS paplašinājuma komponentu iespējošana

1. **Atveriet CloudPOS.sln** risinājumu sadaļā **RetailSdk\\POS** un pārliecinieties, vai to var kompilēt bez kļūdām.
2. Iespējojiet ielādējamos paplašinājumus, failā **extensions.json** pievienojot šādas rindas.

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
    > Papildinformāciju un paraugus, kas parāda, kā iekļaut pirmkoda mapes un iespējot paplašinājumu ielādi, skatiet projekta Pos.Extensions **faila** readme.md norādījumus.

3. Pārbūvējiet risinājumu.
4. Palaidiet risinājumu, **izmantojot komandu Palaist** un sperot mazumtirdzniecības SDK rokasgrāmatā norādītās darbības.

## <a name="production-environment"></a>Ražošanas vide

Iepriekšējā procedūra ļauj paplašinājumus, kas ir vadības bloka integrācijas parauga komponenti. Turklāt ir jāveic šīs darbības, lai izveidotu izvietojamas pakotnes, kurās ir Commerce komponenti, un lietotu šīs pakotnes ražošanas vidē.

1. Veiciet tālāk norādītās izmaiņas pakotnes konfigurācijas failos **RetailSdk\\Assets**:

    - Konfigurācijas failos commerceruntime.ext.config **un** CommerceRuntime.MPOSOffline.Ext.config **kompozīcijas** sadaļai pievienojiet šādas rindas **.**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Konfigurācijas failā **HardwareStation.Extension.config** kompozīcijas **sadaļai** pievienojiet šādu rindu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Mapē BuildTools veiciet šādas izmaiņas **pielāgošanas.settings** pakotnes pielāgošanas konfigurācijas **failā**:

    - Pievienojiet šo rindu, lai paplašinājumus iekļautu CRT izvietojamās pakotnēm.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Pievienojiet šādas rindas, lai izvietojamās pakās iekļautu aparatūras stacijas paplašinājumu.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Iespējojiet POS paplašinājumu, pievienojot šādas rindas failā extensions.json **mapē** **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Startējiet MSBuild komandu uzvedni utilītai Visual Studio un palaidiet **msbuild** zem mapes Retail SDK, lai izveidotu izvietojamas pakotnes.
5. Uzklājiet iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet rakstā [Izvietojamo pakotņu](../dev-itpro/retail-sdk/retail-sdk-packaging.md) izveide.
6. Pabeidziet visus nepieciešamos iestatīšanas uzdevumus, kas aprakstīti sadaļā [Integrācijas iestatīšana ar vadības blokiem](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Paplašinājumu dizains

### <a name="crt-extension-design"></a>CRT pagarinājuma dizains

Paplašinājuma, kas ir finanšu dokumentu nodrošinātājs, mērķis ir ģenerēt pakalpojumam specifiskus dokumentus un apstrādāt vadības bloka atbildes.

Paplašinājums CRT ir **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Papildinformāciju par fiskālās integrācijas risinājuma izstrādi skatiet [fiscal registration process and fiscal integration samples for fiscal devices and services](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

Dokumentu nodrošinātājam ir vienots **DocumentProviderCleanCash** pieprasījumu apdarinātājs. Šo apdarinātāju izmanto, lai ģenerētu vadības bloka finanšu dokumentus.

Šis apstrādātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež servisam raksturīgu dokumentu, kas jāreģistrē vadības blokā.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Šis pieprasījums atgriež abonējamo notikumu sarakstu. Pašlaik tiek atbalstīti pārdošanas notikumi un audita notikumi.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas **fails DocumentProviderFiscalCleanCashSample** atrodas **paplašinājuma projekta konfigurācijas** mapē. Šī faila mērķis ir iespējot iestatījumus dokumentu nodrošinātāja konfigurēšanai no Commerce headquarters. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām. Tiek pievienoti šādi iestatījumi:

- PVN kodu kartējums

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir finanšu savienotājs, mērķis ir sazināties ar vadības bloku.

Aparatūras stacijas paplašinājums ir **HardwareStation.Extension.CleanCashSample**. Tas izmanto HTTP protokolu, lai vadības blokam iesniegtu dokumentus, ko CRT paplašinājums ģenerē. Tā arī apstrādā atbildes, kas saņemtas no vadības bloka.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

**CleanCashHandler** pieprasījumu apdarinātājs ir ieejas punkts pieprasījumu apstrādei vadības blokā.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** — šis pieprasījums nosūta dokumentus vadības blokam un atgriež no tā atbildi.
- **IsReadyFiscalDeviceRequest** — šis pieprasījums tiek izmantots vadības bloka veselības pārbaudei.
- **InicializētfiscalDeviceRequest** — šis pieprasījums tiek izmantots, lai inicializētu vadības bloku.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas paplašinājuma **projekta konfigurācijas** mapē. Faila mērķis ir iespējot finanšu savienotāja iestatījumus, kas jākonfigurē no Commerce headquarters. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām. Tiek pievienoti šādi iestatījumi:

- **Savienojumu virkne** — vadības bloka savienojuma iestatījumi.
- **Taimauts** - laiks milisekundēs, ka vadītājs gaidīs atbildi no vadības bloka.

## <a name="migrating-from-the-earlier-integration-sample"></a>Migrēšana no iepriekšējās integrācijas izlases

Ja izmantojat iepriekšējo [paraugu POS integrācijai ar Zviedrijas](retail-sdk-control-unit-sample.md) vadības blokiem, iespējams, no tā būs jāpāriet uz pašreizējo integrācijas paraugu. Lai ieviestu izmaiņas un saņemtu savlaicīgus atjauninājumus zviedrijas funkcijām nākotnē, iespējams, būs jāveic nelieli koda un konfigurācijas pielāgojumi jūsu veidotajos paplašinājumos un jāatjauno risinājumi. Izveidotajā paplašinājuma loģikā būtiskas izmaiņas nav nepieciešamas. Iepriekšējais integrācijas paraugs un pielāgojumi turpinās darboties, ja no jūsu puses netiks veiktas izmaiņas. Tāpēc jūs varat plānot, sagatavoties un veikt vides uzņemšanu.

### <a name="migration-process"></a>Migrācijas process

Pārejai no iepriekšējās integrācijas izlases uz pašreizējo kontroles bloka integrācijas izlasi būtu jābalstās uz pakāpeniskas atjaunināšanas koncepciju. Citiem vārdiem sakot, visi Commerce headquarters un Commerce Scale Unit komponenti jau ir jāatjaunina, pirms sākat atjaunināt POS un aparatūras stacijas komponentus.

Lai novērstu situāciju, kad notikums vai darījums ir parakstīts divreiz (t.i., to paraksta gan iepriekšējais paplašinājums, gan pašreizējais paplašinājums) vai ja notikumu vai darījumu nevar parakstīt trūkstošās konfigurācijas dēļ, ieteicams izslēgt visas POS un aparatūras stacijas ierīces, kas izmanto iepriekšējo paraugu, un pēc tam tos vienlaikus atjaunināt. Šo vienlaicīgo atjaunināšanu var veikt, piemēram, pa veikaliem, atjauninot veikala funkcionalitātes profilu un aparatūras stacijas aparatūras profilu.

Migrācijas procesam būtu jāietver šādas darbības.

1. Atjauniniet Commerce headquarters komponentus.
1. Atjauniniet Commerce Scale Unit komponentus un iespējojiet pašreizējā parauga paplašinājumus.
1. Pārliecinieties, vai visas bezsaistes transakcijas ir sinhronizētas no mpos ierīcēm, kurās iespējota bezsaiste.
1. Izslēdziet visas ierīces, kas izmanto vecākā parauga komponentus.
1. Pabeidziet visus nepieciešamos iestatīšanas uzdevumus, kas aprakstīti sadaļā [Integrācijas iestatīšana ar vadības blokiem](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Atjauniniet POS un aparatūras stacijas komponentus, atspējojiet paplašinājumus, kas ir vecākā parauga daļas, un iespējojiet pašreizējā parauga paplašinājumus.

    > [!NOTE]
    > Atkarībā no vides veida plašāku informāciju par migrācijas procesu [varat atrast sadaļā Migrācija izstrādes vidē](#migration-in-a-development-environment) vai [šīs tēmas sadaļā Migrācija ražošanas vidē](#migration-in-a-production-environment).

### <a name="migration-in-a-development-environment"></a>Migrācija attīstības vidē

#### <a name="update-crt"></a>Labot CRT

1. Atrodi **Runtime.Extensions.DocumentProvider.CleanCashSample** projektu un uzbūvēt to.
2. Iekš **Runtime.Extensions.DocumentProvider.CleanCashSample\\ atkritumu tvertne\\ Atkļūdošana** mapi, atrodiet **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** montāžas fails.
3. Kopējiet montāžas failu uz CRT paplašinājumu mape:

    - **Commerce Scale Unit (Commerce Scale Unit):** kopējiet failu **\\bin\\ext** mapē, kas atrodas IIS Commerce mēroga vienības vietnes atrašanās vietā.
    - **Vietējais CRT Mūsdienu POS:** Kopējiet failu uz **\\ ext** mape zem vietējā CRT klienta brokera atrašanās vieta.

4. Atrodiet paplašinājuma konfigurācijas failu CRT:

    - **Commerce Scale Unit:** faila nosaukums **ir CommerceRuntime.ext.config**, un tas atrodas **bin\\ext**, kas atrodas IIS Commerce Scale Unit vietnes atrašanās vietā.
    - **Lokālais CRT vietnē Modern POS:** faila nosaukums **ir CommerceRuntime.MPOSOffline.Ext.config**, un tas atrodas **bin\\ext** mapē zem lokālā CRT klienta brokera atrašanās vietas.

    > [!WARNING]
    > Nerediģējiet **failus** CommerceRuntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti nekādiem pielāgojumiem.

5. Atrodiet un noņemiet iepriekšējo CRT paplašinājumu no paplašinājuma konfigurācijas faila.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Nepabeidziet šo darbību, kamēr neatjaunināsit visas POS ierīces, kas darbojas ar šo CRT gadījumu.

6. Reģistrēt pašreizējos parauga CRT paplašinājumus paplašinājuma konfigurācijas failā, pievienojot šādas rindas.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Atjaunināt aparatūras staciju

1. Atrodi **HardwareStation.Extension.CleanCashSample** projektu un uzbūvēt to.
2. Iekš **Extension.CleanCashSample\\ atkritumu tvertne\\ Atkļūdošana** mapi, atrodiet **Contoso.Commerce.HardwareStation.CleanCashSample.dll** un **Interop.CleanCash\_ 1\_ 1.dll** montāžas faili.
3. Kopējiet montāžas failus mapē Aparatūras stacijas paplašinājumi:

    - **Koplietojama aparatūras stacija:** Kopējiet failus uz **atkritumu tvertne** mapi zem IIS aparatūras stacijas vietnes atrašanās vietas.
    - **Īpaša aparatūras stacija modernajā POS:** Kopējiet failus uz Modern POS klienta brokera atrašanās vietu.

4. **Atrodiet HardwareStation.Extension.config** paplašinājuma konfigurācijas failu:

    - **Attālās aparatūras stacija:** fails atrodas IIS aparatūras stacijas atrašanās vietā.
    - **Lokālā aparatūras stacija modern pos:** fails atrodas modern pos klienta brokera atrašanās vietā.

    > [!WARNING]
    > Nerediģējiet **failus** CommerceRuntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti nekādiem pielāgojumiem.

5. Atrodiet un noņemiet iepriekšējo aparatūras stacijas paplašinājumu no paplašinājuma konfigurācijas faila.

    # <a name="retail-73-and-earlier"></a>[Mazumtirdzniecība 7.3 un vecākas versijas](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Mazumtirdzniecība 7.3.1 un jaunākas versijas](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Mazumtirdzniecība 10.0 un jaunākas versijas](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Pievienojiet šādu rindu paplašinājuma **konfigurācijas faila kompozīcijas** sadaļai.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Atjaunināt moderno POS

1. **Atveriet CloudPOS.sln** risinājumu sadaļā **RetailSdk\\POS**.
2. Atspējojiet iepriekšējo POS paplašinājumu, noņemot **no faila extensions.json** šādas rindas.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Iespējojiet pašreizējo POS paplašinājuma paraugu, pievienojot šādas rindas failā **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Atjaunināt mākoņa POS

1. Atveriet **ModernPOS.sln** risinājums zem **RetailSdk\\ POS**.
2. Atspējojiet iepriekšējo POS paplašinājumu, noņemot **no faila extensions.json** šādas rindas.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Iespējojiet pašreizējo POS paplašinājuma paraugu, pievienojot šādas rindas failā **extensions.json**.

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

1. Noņemiet iepriekšējo CRT paplašinājums no **CommerceRuntime.ext.config** un **CommerceRuntime.MPOSOffline.Ext.config** konfigurācijas faili zem **RetailSdk\\ Aktīvi** mapi.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Nepabeidziet šo darbību, kamēr neatjaunināsit visas POS ierīces, kas darbojas ar šo CRT gadījumu.

2. Iespējot pašreizējo paraugu CRT paplašinājumiem, veicot tālāk norādītās izmaiņas **CommerceRuntime.ext.config** un **CommerceRuntime.MPOSOffline.Ext.config** konfigurācijas faili zem **RetailSdk\\ Aktīvi** mapi.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Iekš **Customization.settings** pakotnes pielāgošanas konfigurācijas fails zem **BuildTools** mapē, pievienojiet šo rindiņu, lai iekļautu pašreizējo paraugu CRT paplašinājums izvietojamās pakotnēs.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Atjaunināt aparatūras staciju

1. Noņemiet iepriekšējo aparatūras stacijas paplašinājumu, modificējot **HardwareStation.Extension.config** konfigurācijas fails.

    # <a name="retail-73-and-earlier"></a>[Mazumtirdzniecība 7.3 un vecākas versijas](#tab/retail-7-3)

    Noņemiet nākamo sadaļu no **HardwareStation.Shared.config** un **HardwareStation.Dedicated.config** konfigurācijas faili.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Mazumtirdzniecība 7.3.1 un jaunākas versijas](#tab/retail-7-3-1)

    Noņemiet nākamo sadaļu no **HardwareStation.Extension.config** konfigurācijas fails.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Mazumtirdzniecība 10.0 un jaunākas versijas](#tab/retail-10-0)

    Noņemiet nākamo sadaļu no **HardwareStation.Extension.config** konfigurācijas fails.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Iespējojiet pašreizējo parauga aparatūras stacijas paplašinājumu, pievienojot šādu rindiņu **sastāvu** sadaļā **HardwareStation.Extension.config** konfigurācijas fails.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Mapē BuildTools veiciet šādas izmaiņas **pielāgošanas.settings** pakotnes pielāgošanas konfigurācijas **failā**:

    - Noņemiet šo rindiņu, lai izslēgtu iepriekšējo aparatūras stacijas paplašinājumu no izvietojamām pakotnēm.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Pievienojiet šīs rindas, lai izvietojamās pakotnēs iekļautu pašreizējo aparatūras stacijas paplašinājuma paraugu.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Atjaunināt moderno POS

1. Atveriet **CloudPOS.sln** risinājums plkst **RetailSdk\\ POS**.
2. Atspējojiet iepriekšējo POS paplašinājumu:

    - Iekš **tsconfig.json** failu, pievienojiet **FiscalRegisterSample** mapi izslēgšanas sarakstā.
    - Noņemiet šādas rindas no **extensions.json** failu zem **RetailSDK\\ POS\\ Paplašinājumi** mapi.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Iespējojiet pašreizējo POS paplašinājuma paraugu, pievienojot tālāk norādītās rindiņas **extensions.json** failu zem **RetailSDK\\ POS\\ Paplašinājumi** mapi.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Atjaunināt mākoņa POS

1. Atveriet **ModernPOS.sln** risinājums zem **RetailSdk\\ POS**.
2. Atspējojiet iepriekšējo POS paplašinājumu:

    - Iekš **tsconfig.json** failu, pievienojiet **FiscalRegisterSample** mapi izslēgšanas sarakstā.
    - Noņemiet šādas rindas no **extensions.json** failu zem **RetailSDK\\ POS\\ Paplašinājumi** mapi.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Iespējojiet pašreizējo POS paplašinājuma paraugu, pievienojot tālāk norādītās rindiņas **extensions.json** failu zem **RetailSDK\\ POS\\ Paplašinājumi** mapi.

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

Skrien **msbuild** visam mazumtirdzniecības SDK, lai izveidotu izvietojamas pakotnes. Uzklājiet iepakojumus, izmantojot LCS vai manuāli. Plašāku informāciju skatiet [Mazumtirdzniecības SDK iepakojums](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
