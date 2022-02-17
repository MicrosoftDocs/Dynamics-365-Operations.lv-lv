---
title: Izvēršanas vadlīnijas fiskālā reģistrācijas pakalpojuma integrācijas paraugam Čehijas Republikai (mantots)
description: Šajā tēmā ir sniegtas vadlīnijas fiskālās integrācijas parauga izvietošanai Čehijas Republikā no Microsoft Dynamics 365 Commerce Mazumtirdzniecības programmatūras izstrādes komplekts (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: adafde2123afdc793a6ef4edf8fa16b857c55bf8
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076940"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>Izvēršanas vadlīnijas fiskālā reģistrācijas pakalpojuma integrācijas paraugam Čehijas Republikai (mantots)

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegtas vadlīnijas fiskālā reģistrācijas pakalpojuma integrācijas parauga izvietošanai Čehijas Republikā no Microsoft Dynamics 365 Commerce Mazumtirdzniecības programmatūras izstrādes komplekts (SDK) izstrādātāja virtuālajā mašīnā (VM).Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Papildinformāciju par šo fiskālās integrācijas paraugu skatiet [Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Čehijai](emea-cze-fi-sample.md). 

Čehijas Republikas fiskālās integrācijas paraugs ir daļa no mazumtirdzniecības SDK. Informāciju par SDK instalēšanu un lietošanu skatiet sadaļā [Mazumtirdzniecības programmatūras izstrādes komplekta (SDK) arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šis paraugs sastāv no Commerce izpildlaika paplašinājumiem (CRT) un aparatūras stacija. Lai palaistu šo paraugu, jums ir jāmaina un jāveido CRT un Aparatūras staciju projekti. Lai veiktu šajā tēmā aprakstītās izmaiņas, ieteicams izmantot nepārveidotu mazumtirdzniecības SDK. Mēs arī iesakām izmantot avota kontroles sistēmu, piemēram,Azure DevOps kur neviens fails vēl nav mainīts.

## <a name="development-environment"></a>Izstrādes vide

Veiciet šīs darbības, lai iestatītu izstrādes vidi, lai varētu pārbaudīt un paplašināt paraugu.

### <a name="enable-commerce-runtime-extensions"></a>Iespējot Commerce izpildlaika paplašinājumus

The CRT paplašinājuma komponenti ir iekļauti CRT paraugi. Lai pabeigtu tālāk norādītās procedūras, atveriet **CommerceRuntimeSamples.sln** risinājums zem **RetailSdk\\ Extensions paraugi\\ CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample komponents

1. Atrodi **Runtime.Extensions.DocumentProvider.EFRSample** projektu un uzbūvēt to.
2. Iekš **Runtime.Extensions.DocumentProvider.EFRSample\\ atkritumu tvertne\\ Atkļūdošana** mapi, atrodiet **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** montāžas fails.
3. Kopējiet montāžas failu uz CRT paplašinājumu mape:

    - **Tirdzniecības mēroga vienība:** Kopējiet failu uz **\\ atkritumu tvertne\\ ext** mapē Interneta informācijas pakalpojumu (IIS) Commerce Scale Unit vietnes atrašanās vietā.
    - **Vietējais CRT Mūsdienu POS:** Kopējiet failu uz **\\ ext** mape zem vietējā CRT klienta brokera atrašanās vieta.

4. Atrodiet paplašinājuma konfigurācijas failu CRT:

    - **Tirdzniecības mēroga vienība:** Fails ir nosaukts **commerceruntime.ext.config**, un tas atrodas **atkritumu tvertne\\ ext** mapi zem IIS Commerce Scale Unit vietnes atrašanās vietas.
    - **Vietējais CRT Mūsdienu POS:** Fails ir nosaukts **CommerceRuntime.MPOSOffline.Ext.config**, un tas ir zem vietējā CRT klienta brokera atrašanās vieta.

5. Reģistrējieties CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponents

1. Atrodi **Runtime.Extensions.DocumentProvider.DataModelEFR** projektu un uzbūvēt to.
2. Iekš **Runtime.Extensions.DocumentProvider.DataModelEFR\\ atkritumu tvertne\\ Atkļūdošana** mapi, atrodiet **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** montāžas fails.
3. Kopējiet montāžas failu uz CRT paplašinājumu mape:

    - **Commerce Scale Unit (Commerce Scale Unit):** kopējiet failu **\\bin\\ext** mapē, kas atrodas IIS Commerce mēroga vienības vietnes atrašanās vietā.
    - **Vietējais CRT Mūsdienu POS:** Kopējiet failu uz **\\ ext** mape zem vietējā CRT klienta brokera atrašanās vieta.

4. Atrodiet paplašinājuma konfigurācijas failu CRT:

    - **Tirdzniecības mēroga vienība:** Fails ir nosaukts **commerceruntime.ext.config**, un tas atrodas **atkritumu tvertne\\ ext** mapi zem IIS Commerce Scale Unit vietnes atrašanās vietas.
    - **Vietējais CRT Mūsdienu POS:** Fails ir nosaukts **CommerceRuntime.MPOSOffline.Ext.config**, un tas ir zem vietējā CRT klienta brokera atrašanās vieta.

5. Reģistrējieties CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Paplašinājuma konfigurācijas fails

1. Atrodiet paplašinājuma konfigurācijas failu CRT:

    - **Tirdzniecības mēroga vienība:** Fails ir nosaukts **commerceruntime.ext.config**, un tas atrodas **atkritumu tvertne\\ ext** mapi zem IIS Commerce Scale Unit vietnes atrašanās vietas.
    - **Vietējais CRT Mūsdienu POS:** Fails ir nosaukts **CommerceRuntime.MPOSOffline.Ext.config**, un tas ir zem vietējā CRT klienta brokera atrašanās vieta.

2. Reģistrējieties CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-hardware-station-extensions"></a>Iespējot aparatūras staciju paplašinājumus

Aparatūras stacijas paplašinājuma komponenti ir iekļauti aparatūras stacijas paraugos. Lai pabeigtu tālāk norādītās procedūras, atveriet **HardwareStationSamples.sln** risinājums zem **RetailSdk\\ Extensions paraugi\\ HardwareStation**.

#### <a name="efrsample-component"></a>EFRSparauga komponents

1. Atrodi **HardwareStation.Extension.EFRSample** projektu un uzbūvēt to.
2. Iekš **Paplašinājums.EFRSample\\ atkritumu tvertne\\ Atkļūdošana** mapē atrodiet šādus montāžas failus:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopējiet montāžas failus mapē Aparatūras stacijas paplašinājumi:

    - **Koplietojama aparatūras stacija:** Kopējiet failus uz **atkritumu tvertne** mapi zem IIS aparatūras stacijas vietnes atrašanās vietas.
    - **Īpaša aparatūras stacija modernajā POS:** Kopējiet failus uz Modern POS klienta brokera atrašanās vietu.

4. Atrodiet aparatūras stacijas paplašinājumu konfigurācijas failu. Faila nosaukums **ir HardwareStation.Extension.config**.

    - **Koplietojama aparatūras stacija:** Fails atrodas zem IIS aparatūras stacijas vietnes atrašanās vietas.
    - **Īpaša aparatūras stacija modernajā POS:** Fails atrodas Modern POS klienta brokera atrašanās vietā.

5. Pievienojiet konfigurācijas faila kompozīcijas **sadaļai** šādu rindu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="production-environment"></a>Ražošanas vide

Iepriekšējā procedūra iespējo paplašinājumus, kas ir fiskālās reģistrācijas pakalpojuma integrācijas parauga sastāvdaļas. Turklāt ir jāveic šīs darbības, lai izveidotu izvietojamas pakotnes, kurās ir Commerce komponenti, un lietotu šīs pakotnes ražošanas vidē.

1. Veiciet šādas izmaiņas pakotnes konfigurācijas failos zem **RetailSdk\\ Aktīvi** mapi.

    - Konfigurācijas failos commerceruntime.ext.config **un** CommerceRuntime.MPOSOffline.Ext.config **kompozīcijas** sadaļai pievienojiet šādas rindas **.**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - Konfigurācijas failā **HardwareStation.Extension.config** kompozīcijas **sadaļai** pievienojiet šādu rindu.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. Veiciet tālāk norādītās izmaiņas **Customization.settings** pakotnes pielāgošanas konfigurācijas fails zem **BuildTools** mapi.

    - Pievienojiet šādas rindas, lai iekļautu CRT paplašinājumus izvietojamās pakotnēs.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Pievienojiet šo rindiņu, lai izvietojamās pakotnēs iekļautu aparatūras stacijas paplašinājumu.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Startējiet MSBuild komandu uzvedni utilītai Visual Studio un palaidiet **msbuild** zem mapes Retail SDK, lai izveidotu izvietojamas pakotnes.
4. Uzklājiet iepakojumus, izmantojot LCS vai manuāli. Papildinformāciju skatiet rakstā [Izvietojamo pakotņu](../dev-itpro/retail-sdk/retail-sdk-packaging.md) izveide.
5. Pabeidziet visus nepieciešamos iestatīšanas uzdevumus, kas aprakstīti [Iestatiet Commerce Čehijas Republikai](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic).

## <a name="design-of-extensions"></a>Paplašinājumu projektēšana

Čehijas Republikas nodokļu reģistrācijas pakalpojuma integrācijas paraugs ir balstīts uz [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md). Papildinformāciju par fiskālās integrācijas risinājuma izstrādi skatiet rakstā [pārskats par fiskālās integrācijas parauga dizainu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Tirdzniecības izpildlaika paplašinājuma dizains

Paplašinājuma, kas ir fiskālo dokumentu nodrošinātājs, mērķis ir ģenerēt pakalpojumam specifiskus dokumentus un apstrādāt atbildes no fiskālā reģistrācijas pakalpojuma.

The CRT pagarinājums ir **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

Ir viens **DocumentProviderEFRFiscalCZE** dokumentu nodrošinātāja pieprasījumu apstrādātājs. To izmanto, lai ģenerētu fiskālos dokumentus fiskālās reģistrācijas pakalpojumam.

Šis apstrādātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē fiskālās reģistrācijas pakalpojumā.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Šis pieprasījums atgriež abonējamo notikumu sarakstu. Šobrīd tiek atbalstīti šādi notikumi: pārdošana, iemaksas klientu kontā un klientu pasūtījumu iemaksas.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Šis pieprasījums atgriež atbildi no fiskālās reģistrācijas dienesta. Šī atbilde tiek serializēta, lai izveidotu virkni, lai tā būtu gatava saglabāšanai.

#### <a name="configuration"></a>Konfigurācija

The **DocumentProviderFiscalEFRSampleChech** konfigurācijas fails atrodas mapē **Konfigurācija** paplašinājuma projekta mapi. Šī faila mērķis ir iespējot iestatījumus dokumentu nodrošinātāja konfigurēšanai no Commerce headquarters. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām. Tiek pievienoti šādi iestatījumi:

- PVN likmju kartējums
- Noklusējuma PVN grupa
- Depozīta PVN grupa

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar fiskālās reģistrācijas pakalpojumu.

Aparatūras stacijas paplašinājums ir **HardwareStation.Extension.EFRSample**. Aparatūras stacijas paplašinājums izmanto HTTP protokolu, lai iesniegtu dokumentus, ko CRT paplašinājums ģenerē finanšu reģistrācijas pakalpojumam. Tas arī apstrādā atbildes, kas tiek saņemtas no fiskālās reģistrācijas dienesta.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **EFRHandler** pieprasījumu apstrādātājs ir piekļuves punkts, lai apstrādātu pieprasījumus nodokļu reģistrācijas dienestam.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – Šis pieprasījums nosūta dokumentus fiskālās reģistrācijas dienestam un atgriež no tā atbildi.
- **IsReadyFiscalDeviceRequest** – Šis pieprasījums tiek izmantots fiskālās reģistrācijas dienesta veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – Šis pieprasījums tiek izmantots, lai inicializētu fiskālās reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas mapē **Konfigurācija** paplašinājuma projekta mapi. Faila mērķis ir iespējot finanšu savienotāja iestatījumus, kas jākonfigurē no Commerce headquarters. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām. Tiek pievienoti šādi iestatījumi:

- **Galapunkta adrese** – Fiskālās reģistrācijas pakalpojuma URL.
- **Pārtraukums** – Laiks milisekundēs, cik ilgi vadītājs gaidīs atbildi no fiskālās reģistrācijas dienesta.
