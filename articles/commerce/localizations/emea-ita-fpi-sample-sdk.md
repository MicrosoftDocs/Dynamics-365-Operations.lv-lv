---
title: Izvēršanas vadlīnijas fiskālā printera integrācijas paraugam Itālijai (mantots)
description: Šajā tēmā ir sniegtas vadlīnijas fiskālā printera integrācijas parauga izvietošanai Itālijā no Microsoft Dynamics 365 Commerce Mazumtirdzniecības programmatūras izstrādes komplekts (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 93aca34239affb41998f4309d7c03f29f7b5f003
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076890"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Izvēršanas vadlīnijas fiskālā printera integrācijas paraugam Itālijai (mantots)

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegtas vadlīnijas fiskālā printera integrācijas parauga izvietošanai Itālijā no Microsoft Dynamics 365 Commerce Mazumtirdzniecības programmatūras izstrādes komplekts (SDK) izstrādātāja virtuālajā mašīnā (VM).Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Papildinformāciju par šo fiskālās integrācijas paraugu skatiet [Fiskālā printera integrācijas paraugs Itālijai](emea-ita-fpi-sample.md). 

Itālijas fiskālās integrācijas paraugs ir daļa no mazumtirdzniecības SDK. Informāciju par SDK instalēšanu un lietošanu skatiet sadaļā [Mazumtirdzniecības programmatūras izstrādes komplekta (SDK) arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šis paraugs sastāv no Commerce izpildlaika paplašinājumiem (CRT) un aparatūras stacija. Lai palaistu šo paraugu, jums ir jāmaina un jāveido CRT un Aparatūras staciju projekti. Lai veiktu šajā tēmā aprakstītās izmaiņas, ieteicams izmantot nepārveidotu mazumtirdzniecības SDK. Mēs arī iesakām izmantot avota kontroles sistēmu, piemēram,Azure DevOps kur neviens fails vēl nav mainīts.

## <a name="development-environment"></a>Izstrādes vide

Veiciet šīs darbības, lai iestatītu izstrādes vidi, lai varētu pārbaudīt un paplašināt paraugu.

### <a name="commerce-runtime-extension-components"></a>Tirdzniecības izpildlaika paplašinājuma komponenti

The CRT paplašinājuma komponenti ir iekļauti mazumtirdzniecības SDK. Lai pabeigtu tālāk norādītās procedūras, atveriet **CommerceRuntimeSamples.sln** risinājums zem **RetailSdk\\ Extensions paraugi\\ CommerceRuntime**.

1. Atrodi **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** projektu un uzbūvēt to.
2. Iekš **Paplašinājumi.DocumentProvider.EpsonFP90IIISample\\ atkritumu tvertne\\ Atkļūdošana** mapi, atrodiet **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** montāžas fails.
3. Kopējiet montāžas failu uz CRT paplašinājumu mape:

    - **Tirdzniecības mēroga vienība:** Kopējiet failu uz **\\ atkritumu tvertne\\ ext** mapē Interneta informācijas pakalpojumu (IIS) Commerce Scale Unit vietnes atrašanās vietā.
    - **Vietējais CRT Mūsdienu POS:** Kopējiet failu uz **\\ ext** mape zem vietējā CRT klienta brokera atrašanās vieta.

4. Atrodiet paplašinājuma konfigurācijas failu CRT:

    - **Tirdzniecības mēroga vienība:** Fails ir nosaukts **commerceruntime.ext.config**, un tas atrodas **atkritumu tvertne\\ ext** mapi zem IIS Commerce Scale Unit vietnes atrašanās vietas.
    - **Vietējais CRT Mūsdienu POS:** Fails ir nosaukts **CommerceRuntime.MPOSOffline.Ext.config**, un tas ir zem vietējā CRT klienta brokera atrašanās vieta.

5. Reģistrējieties CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Restartējiet Commerce Scale Unit:

    - **Tirdzniecības mēroga vienība:** Restartējiet vietni Commerce Scale Unit no IIS pārvaldnieka.
    - **Klientu brokeris:** Beidziet **dllhost.exe** procesu uzdevumu pārvaldniekā un pēc tam restartējiet Modern POS.

### <a name="hardware-station-extension-components"></a>Aparatūras stacijas paplašinājuma sastāvdaļas

Aparatūras stacijas paplašinājuma komponenti ir iekļauti mazumtirdzniecības SDK. Lai pabeigtu tālāk norādītās procedūras, atveriet **HardwareStationSamples.sln** risinājums zem **RetailSdk\\ Extensions paraugi\\ HardwareStation**.

1. Atrodi **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** projektu un uzbūvēt to.
2. Iekš **Extensions.EpsonFP90IIIFiscalDeviceSample\\ atkritumu tvertne\\ Atkļūdošana** mapi, atrodiet **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll** montāžas fails.
3. Kopējiet montāžas failu izvietotajā aparatūras stacijas mašīnā:

    - **Attālā aparatūras stacija:** Kopējiet failu uz **atkritumu tvertne** mapi zem IIS aparatūras stacijas vietnes atrašanās vietas.
    - **Vietējā aparatūras stacija:** Kopējiet failu uz Modern POS klienta brokera atrašanās vietu.

4. Atrodiet aparatūras stacijas paplašinājumu konfigurācijas failu. Fails ir nosaukts **HardwareStation.Extension.config**:

    - **Attālā aparatūras stacija:** Fails atrodas zem IIS aparatūras stacijas vietnes atrašanās vietas.
    - **Vietējā aparatūras stacija:** Fails atrodas Modern POS klienta brokera atrašanās vietā.

5. Pievienojiet šādu sadaļu **sastāvu** konfigurācijas faila sadaļā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Restartējiet aparatūras stacijas pakalpojumu:

    - **Attālā aparatūras stacija:** Restartējiet aparatūras stacijas vietni no IIS pārvaldnieka.
    - **Vietējā aparatūras stacija:** Beidziet **dllhost.exe** procesu uzdevumu pārvaldniekā un pēc tam restartējiet Modern POS.

## <a name="production-environment"></a>Ražošanas vide

Lai izveidotu izvietojamas pakotnes, kas satur Commerce komponentus, un lietotu šīs pakotnes ražošanas vidē, veiciet šīs darbības.

1. Pabeidziet darbības, kas aprakstītas sadaļā [Attīstības vide](#development-environment) sadaļā iepriekš šajā tēmā.
2. Veiciet tālāk norādītās izmaiņas pakotnes konfigurācijas failos **RetailSdk\\Assets**:

    - Iekš **commerceruntime.ext.config** un **CommerceRuntime.MPOSOffline.Ext.config** konfigurācijas failus, pievienojiet šādu rindiņu **sastāvu** sadaļā.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    - Konfigurācijas failā **HardwareStation.Extension.config** kompozīcijas **sadaļai** pievienojiet šādu rindu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Mapē BuildTools veiciet šādas izmaiņas **pielāgošanas.settings** pakotnes pielāgošanas konfigurācijas **failā**:

    - Pievienojiet šo rindiņu, lai iekļautu CRT paplašinājums izvietojamās pakotnēs.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    - Pievienojiet šo rindiņu, lai izvietojamās pakotnēs iekļautu aparatūras stacijas paplašinājumu.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Sāciet MSBuild komandu uzvedni Visual Studio utilītu un pēc tam palaist **msbuild** mapē Retail SDK, lai izveidotu izvietojamas pakotnes.
5. Uzklājiet iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet rakstā [Izvietojamo pakotņu](../dev-itpro/retail-sdk/retail-sdk-packaging.md) izveide.

## <a name="design-of-extensions"></a>Paplašinājumu projektēšana

### <a name="commerce-runtime-extension-design"></a>Tirdzniecības izpildlaika paplašinājuma dizains

Paplašinājuma, kas ir fiskālo dokumentu nodrošinātājs, mērķis ir ģenerēt printerim specifiskus dokumentus un apstrādāt atbildes no fiskālā printera.

The CRT pagarinājums ir **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Papildinformāciju par fiskālās integrācijas risinājuma izstrādi skatiet [fiscal registration process and fiscal integration samples for fiscal devices and services](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **DocumentProviderEpsonFP90III** pieprasījumu apstrādātājs ir ieejas punkts pieprasījumam ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Šis pieprasījums atgriež abonējamo notikumu sarakstu. Pašlaik tiek atbalstīti šādi pasākumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas mapē **Konfigurācija** paplašinājuma projekta mapi. Faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, ko konfigurē Commerce galvenajā mītnē. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām. Tiek pievienoti šādi iestatījumi:

- PVN kodu kartējums
- PVN likmju kartējums
- Norēķinu veida kartējums
- Ieejas plūsmas numura svītrkoda veids
- Depozīta maksājuma veids

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar fiskālo printeri.

Aparatūras stacijas paplašinājums ir **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Šis paplašinājums izmanto HTTP protokolu, lai iesniegtu dokumentus, kas CRT paplašinājums tiek ģenerēts fiskālajam printerim. Tas arī apstrādā atbildes, kas tiek saņemtas no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **EpsonFP90IIISample** pieprasījumu apstrādātājs ir ieejas punkts, lai apstrādātu pieprasījumus fiskālajai perifērijas ierīcei.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – Šis pieprasījums nosūta dokumentus uz printeriem un atgriež atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – Šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – Šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas mapē **Konfigurācija** paplašinājuma projekta mapi. Faila mērķis ir iespējot savienotāja iestatījumus, kas jākonfigurē no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām. Tiek pievienoti šādi iestatījumi:

- **Galapunkta adrese** – Printera URL.
- **Datuma un laika sinhronizācija** – Vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē ar pievienoto aparatūras staciju.
