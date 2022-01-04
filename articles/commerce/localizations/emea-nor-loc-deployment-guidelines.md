---
title: Izvietošanas vadlīnijas kases reģistriem Norvēģijai (mantojuma)
description: Šī tēma ir izvietošanas rokasgrāmata, kas parāda, kā iespējot Microsoft Dynamics 365 Commerce lokalizāciju Norvēģijai.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: 019bac01abdc0b2e16718c08953b44fbccef83a3
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944792"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Izvietošanas vadlīnijas kases reģistriem Norvēģijai (mantojuma)

[!include [banner](../includes/banner.md)]

Šī tēma ir izvietošanas rokasgrāmata, kas parāda, kā iespējot Microsoft Dynamics 365 Commerce lokalizāciju Norvēģijai. Lokalizācija sastāv no vairākiem Commerce komponentu paplašinājumiem. Piemēram, paplašinājumi ļauj drukāt pielāgotos laukus kvītīs, reģistrēt papildu audita notikumus, pārdošanas darbības un maksājumu darbības Pārdošanas punktā (POS), digitāli parakstītas pārdošanas darbības un drukāt X un Z pārskatus lokālos formātos. Papildinformāciju par Norvēģijas lokalizāciju skatiet [Kases sistēmas funkcionalitāti Norvēģijai](./emea-nor-cash-registers.md).

Šis paraugs ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK). Informāciju par SDK skatiet mazumtirdzniecības [programmatūras izstrādes komplekta (SDK) arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Šis paraugs sastāv no Commerce Runtime CRT (), Retail Server un POS paplašinājumiem. Lai palaistu šo paraugu, ir jāmodificē un jāveido CRT, Retail Server un POS projekti. Ieteicams izmantot nemodificētu komplektu Retail SDK, lai veiktu šajā tēmā aprakstītās izmaiņas. Iesakām arī lietot avota kontroles sistēmu, piemēram, Microsoft Visual Studio Online (VSO), kur vēl nav mainīts neviens fails.

> [!NOTE]
> Programmā Commerce 10.0.8 un iepriekš lietojumprogrammā Retail Server ir zināms kā Commerce Scale Unit. Tā kā šī tēma attiecas uz vairākām iepriekšējām programmas versijām, *visā tēmā tiek izmantots Retail* Server.
>
> Daži šīs tēmas procedūru soļi atšķiras atkarībā no izmantotās Commerce versijas. Papildinformāciju skatiet [sadaļā Jaunumi vai Dynamics 365 Retail](../get-started/whats-new.md) izmaiņas.

### <a name="using-certificate-profiles-in-commerce-channels"></a>Sertifikātu profilu izmantošana Commerce kanālos

Commerce versijās 10.0.15 un jaunākās versijās varat izmantot lietotāja definētos mazumtirdzniecības veikalu līdzekļu sertifikātu profilus, kas atbalsta kļūmes bezsaistes režīmā, kad nav pieejama atslēga Outlook vai [Commerce](./certificate-profiles-for-retail-stores.md) Headquarters. Šī funkcija paplašina [mazumtirdzniecības kanālu funkcijas pārvaldīt](../dev-itpro/manage-secrets.md) slepus.

Lai lietotu šo funkcionalitāti CRT paplašinājumā, sekojiet šiem soļiem.

1. Izveidot jaunu CRT paplašinājuma projektu (C# klases bibliotēkas projekta tips). Izmantojiet mazumtirdzniecības programmatūras izstrādes komplekta (SDK) (RetailSDK\SampleExtensions\CommerceRuntime) parauga veidnes.

2. Pievienojiet pielāgotu apdarinātāju CertificateSign izpakojumprogrammasServiceRequest projektā SequentialSignmanagerRegister.

3. Lai lasītu slepeno `GetUserDefinedSecretCertificateServiceRequest` izsaukumu, izmantojot konstruktoru ar profila ID parametru. Tas sāks funkcionalitāti, strādājot ar iestatījumiem no sertifikātu profiliem. Atbilstoši iestatījumiem sertifikāts tiks izgūts no Azure atslēgas Lomas vai lokālās mašīnas krātuves.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Kad sertifikāts tiek izgūts, turpiniet ar datu parakstīšanu.

5. Izveidojiet CRT paplašinājuma projektu.

6. Kopējiet izvades klases bibliotēku un ielīmējiet to ...\RetailServer\webroot\bin\Ext manuālai testēšanai.

7. Failā CommerceRuntime.Ext.config atjauniniet paplašinājuma sastāva sadaļu ar pielāgotu bibliotēkas informāciju.

## <a name="development-environment"></a>Izstrādes vide

Veiciet šīs procedūras, lai iestatītu izstrādes vidi, tādējādi jūs variet pārbaudīt un pagarināt paraugu.

### <a name="the-crt-extension-components"></a>Paplašinājuma CRT komponenti

Paplašinājuma CRT komponenti tiek iekļauti CRT paraugos. Lai izpildītu tālāk norādītās procedūras, atveriet risinājumu CRT **CommerceRuntimeSamples.sln, kas atrodas** **RetailSdk \\ SampleExtensions \\ CommerceRuntime.**

#### <a name="receiptsnorway-component"></a>ReceiptsNorway komponents

1. Atrodiet **Runtime.Extensions.ReceiptsNorway** projektu un izveidojiet to.
2. Mapē **Extensions.ReceiptsNorway \\ bin \\ Debug atrodiet** **Contoso.Commerce.Runtime.ReceiptsNorway.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Retail Server:** kopēt montāžu uz **\\ nodalījuma ārējo mapi Microsoft Internet Information Services \\** (IIS) Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt komponents

1. Atrodiet projektu **Runtime.Extensions.SalesPaymentTransExt** un izveidojiet to.
2. Mapē **Extensions.SalesPaymentTransExt bin Atkļūdošanas atrodiet \\\\** **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="xzreportsnorway-component"></a>XZReportsNorway komponents

1. Atrodiet **Runtime.Extensions.XZReportsNorway** projektu un izveidojiet to.
2. Mapē **Extensions.XZReportsNorway \\ bin \\ Debug atrodiet** **Contoso.Commerce.Runtime.XZReportsNorway.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

# <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent parauga komponents

1. Atrodiet projektu **Runtime.Extensions.RegisterAuditEventSample** un izveidojiet to.
2. Mapē **Extensions.RegisterAuditEventSample \\ bin \\ Debug atrodiet** **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignactionSignaction parauga komponents

1. Atrast projektu **Runtime.Extensions.SalesTransactionSignactionSample.**
2. Modificējiet failu App.config, norādot īssavilkumu, veikala atrašanās vietu un veikala nosaukumu sertifikātam, kas ir jāizmanto pārdošanas **transakciju** parakstam.
3. Veidot projektu.
4. Mapē **Extensions.SalesTransactionSignranSample \\ bin \\ Atkļūdošanas** mape atrodiet šādus failus:

    - **Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll** montāžas fails
    - Konfigurācijas **fails Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll.config**

5. Kopēt failus uz CRT paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

6. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

7. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

# <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent parauga komponents

1. Atrodiet projektu **Runtime.Extensions.RegisterAuditEventSample** un izveidojiet to.
2. Mapē **Extensions.RegisterAuditEventSample \\ bin \\ Debug atrodiet** **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignactionSignaction parauga komponents

1. Atrast projektu **Runtime.Extensions.SalesTransactionSignactionSample.**
2. Modificējiet failu App.config, norādot īssavilkumu, veikala atrašanās vietu un veikala nosaukumu sertifikātam, kas ir jāizmanto pārdošanas **transakciju** parakstam.
3. Veidot projektu.
4. Mapē **Extensions.SalesTransactionSignranSample \\ bin \\ Atkļūdošanas** mape atrodiet šādus failus:

    - **Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll** montāžas fails
    - Konfigurācijas **fails Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll.config**

5. Kopēt failus uz CRT paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

6. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

7. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignmaksājotSample.Ziņojumu komponents

1. Atrodiet **Runtime.Extensions.SalesTransactionSignactionSample.Messages** projektu.
2. Mapē **Extensions.SalesTransactionSignranSample.Messages bin Atkļūdošanas atrodiet \\\\** **Contoso.Commerce.Runtime.SalesTransactionSign pirkšanasSample.Messages.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

# <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent parauga komponents

1. Atrodiet projektu **Runtime.Extensions.RegisterAuditEventSample** un izveidojiet to.
2. Mapē **Extensions.RegisterAuditEventSample \\ bin \\ Debug atrodiet** **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignactionSignaction parauga komponents

1. Atrast projektu **Runtime.Extensions.SalesTransactionSignactionSample.**
2. Modificējiet failu App.config, norādot īssavilkumu, veikala atrašanās vietu un veikala nosaukumu sertifikātam, kas ir jāizmanto pārdošanas **transakciju** parakstam.
3. Veidot projektu.
4. Mapē **Extensions.SalesTransactionSignranSample \\ bin \\ Atkļūdošanas** mape atrodiet šādus failus:

    - **Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll** montāžas fails
    - Konfigurācijas **fails Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll.config**

5. Kopēt failus uz CRT paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

6. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

7. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignmaksājotRegister.Contracts komponents

1. Atrast **Project Runtime.Extensions.SequentialSign runtimeregister.Contracts.**
2. Mapē **Extensions.SequentialSign contosoRegister.Contracts \\ bin \\ Atkļūdošanas** atrast **Contoso.Commerce.Runtime.SequentialSignllaRegister.Contracts.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent parauga komponents

1. Atrodiet projektu **Runtime.Extensions.RegisterAuditEventSample** un izveidojiet to.
2. Mapē **Extensions.RegisterAuditEventSample \\ bin \\ Debug atrodiet** **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="sequentialsignatureregister-component"></a>Para&secīgaisRegister komponents

1. Atrast **projektu Runtime.Extensions.SequentialSign** runtimeregister.
2. Modificējiet failu App.config, norādot īssavilkumu, veikala atrašanās vietu un veikala nosaukumu sertifikātam, kas ir jāizmanto pārdošanas **transakciju** parakstam.
3. Veidot projektu.
4. Mapē **Extensions.SequentialSignmaksājotRegister \\ bin \\ Atkļūdošanas** atrast šādus failus:

    - **Contoso.Commerce.Runtime.SequentialSignmaksājotRegister.dll** montāžas fails
    - Konfigurācijas **fails Contoso.Commerce.Runtime.SequentialSignmaksājotRegister.dll.config**

5. Kopēt failus uz CRT paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

6. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

7. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignranNorway komponents

1. Atrodiet projektu **Runtime.Extensions.SalesTransactionSignactionNorway.**
2. Mapē **Extensions.SalesTransactionSignranNornorway bin Atkļūdošanas atrodiet \\\\** **Contoso.Commerce.Runtime.SalesTransactionSignactionNorway.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignmaksājotRegister.Contracts komponents

1. Atrast **Project Runtime.Extensions.SequentialSign runtimeregister.Contracts.**
2. Mapē **Extensions.SequentialSign contosoRegister.Contracts \\ bin \\ Atkļūdošanas** atrast **Contoso.Commerce.Runtime.SequentialSignllaRegister.Contracts.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponents

1. Atrodiet project **Runtime.Extensions.SalesPaymentTransExtNorway** un izveidojiet to.
2. Mapē **Extensions.SalesPaymentTransExtNorway \\ bin \\ Debug atrodiet** **contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway komponents

1. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

2. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="sequentialsignatureregister-component"></a>Para&secīgaisRegister komponents

1. Atrast **projektu Runtime.Extensions.SequentialSign** runtimeregister.
2. Modificējiet failu App.config, norādot īssavilkumu, veikala atrašanās vietu un veikala nosaukumu sertifikātam, kas ir jāizmanto pārdošanas **transakciju** parakstam.
3. Veidot projektu.
4. Mapē **Extensions.SequentialSignmaksājotRegister \\ bin \\ Atkļūdošanas** atrast šādus failus:

    - **Contoso.Commerce.Runtime.SequentialSignmaksājotRegister.dll** montāžas fails
    - Konfigurācijas **fails Contoso.Commerce.Runtime.SequentialSignmaksājotRegister.dll.config**

5. Kopēt failus uz CRT paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

6. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

7. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignranNorway komponents

1. Atrodiet projektu **Runtime.Extensions.SalesTransactionSignactionNorway.**
2. Mapē **Extensions.SalesTransactionSignranNornorway bin Atkļūdošanas atrodiet \\\\** **Contoso.Commerce.Runtime.SalesTransactionSignactionNorway.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignmaksājotRegister.Contracts komponents

1. Atrast **Project Runtime.Extensions.SequentialSign runtimeregister.Contracts.**
2. Mapē **Extensions.SequentialSign contosoRegister.Contracts \\ bin \\ Atkļūdošanas** atrast **Contoso.Commerce.Runtime.SequentialSignllaRegister.Contracts.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponents

1. Atrodiet project **Runtime.Extensions.SalesPaymentTransExtNorway** un izveidojiet to.
2. Mapē **Extensions.SalesPaymentTransExtNorway \\ bin \\ Debug atrodiet** **contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway komponents

1. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

2. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="sequentialsignatureregister-component"></a>Para&secīgaisRegister komponents

1. Atrast **projektu Runtime.Extensions.SequentialSign** runtimeregister.
2. Modificējiet failu App.config, norādot īssavilkumu, veikala atrašanās vietu un veikala nosaukumu sertifikātam, kas ir jāizmanto pārdošanas **transakciju** parakstam.
3. Veidot projektu.
4. Mapē **Extensions.SequentialSignmaksājotRegister \\ bin \\ Atkļūdošanas** atrast šādus failus:

    - **Contoso.Commerce.Runtime.SequentialSignmaksājotRegister.dll** montāžas fails
    - Konfigurācijas **fails Contoso.Commerce.Runtime.SequentialSignmaksājotRegister.dll.config**

5. Kopēt failus uz CRT paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

6. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

7. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignranNorway komponents

1. Atrodiet projektu **Runtime.Extensions.SalesTransactionSignactionNorway.**
2. Mapē **Extensions.SalesTransactionSignranNornorway bin Atkļūdošanas atrodiet \\\\** **Contoso.Commerce.Runtime.SalesTransactionSignactionNorway.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignmaksājotRegister.Contracts komponents

1. Atrast **Project Runtime.Extensions.SequentialSign runtimeregister.Contracts.**
2. Mapē **Extensions.SequentialSign contosoRegister.Contracts \\ bin \\ Atkļūdošanas** atrast **Contoso.Commerce.Runtime.SequentialSignllaRegister.Contracts.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponents

1. Atrodiet project **Runtime.Extensions.SalesPaymentTransExtNorway** un izveidojiet to.
2. Mapē **Extensions.SalesPaymentTransExtNorway \\ bin \\ Debug atrodiet** **contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** montāžas failu.
3. Kopēt montāžas failu CRT uz paplašinājumu mapi:

    - **Mazumtirdzniecības** serveris: kopēt montāžu **\\ uz nodalījuma ārējo \\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    - **Lokāls CRT modernajā POS:** kopējiet montāžu uz **\\ ārējo mapi lokālā klienta** CRT starpnieka atrašanās vietā.

4. Meklēt paplašinājuma konfigurācijas failu CRT šim:

    - **Retail Server:** faila nosaukums ir **commerceruntime.ext.config, un tā atrodas iiS Retail Server vietnes atrašanās vietas** nodalījuma ārējā **\\** mapē.
    - **Modern POS lokāls: faila nosaukums ir CRT** **CommerceRuntime.MPOSOffline.Ext.config, un tas atrodas vietējā klienta** CRT starpnieka atrašanās vietā.

5. Reģistrēt CRT izmaiņas paplašinājuma konfigurācijas failā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > **Nerediģēt** failus commerceruntime.config un CommerceRuntime.MPOSOffline.config. Šie faili nav paredzēti pielāgošanai.

---

### <a name="the-retail-server-extension-components"></a>Retail Server paplašinājuma komponenti

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSignran Retail Server parauga komponents

1. Mapē **RetailSDK \\ SampleExtensions \\ RetailServer \\ RetailServer.Extensions.SalesTransactionSignactionSample atrodiet projektu** **RetailServer.Extensions.SalesTransactionSignmediaSample** un izveidojiet to.
2. Mapē **RetailServer \\ Extensions.SalesTransactionSignllaSample bin Atkļūdošanas mape \\\\ atrodiet** **Contoso.RetailServer.SalesTransactionSignactionSignactionSample.dll** montāžas failu.
3. Iekopējiet montāžas failu Retail Server paplašinājumu mapē.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    Mape ir nodalījuma **\\ mape,** kas atrodas IIS Retail Server vietnes atrašanās vietā.

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    Mape ir nodalījuma **\\ mape,** kas atrodas IIS Retail Server vietnes atrašanās vietā.

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    Mape ir nodalījuma **\\ ārējā \\** mape, kas atrodas IIS Retail Server vietnes atrašanās vietā.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    Mape ir nodalījuma **\\ ārējā \\** mape, kas atrodas IIS Retail Server vietnes atrašanās vietā.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    Mape ir nodalījuma **\\ ārējā \\** mape, kas atrodas IIS Retail Server vietnes atrašanās vietā.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    Mape ir nodalījuma **\\ ārējā \\** mape, kas atrodas IIS Retail Server vietnes atrašanās vietā.

    ---

4. Atrast Retail Server konfigurācijas failu. Faila nosaukums ir web.config, un tas ir saknes mapē zem **IIS** Retail Server vietnes atrašanās vietas.
5. Reģistrējiet Retail Server paplašinājumus **konfigurācijas faila sadaļā extensionComposition.**

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Reģistrējiet Retail Server paplašinājumu atkarības.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4/)

    1. Mapē **CommerceRuntime \\ Extensions.SalesTransactionSignactionSample \\ bin \\ Atkļūdošana** atrodiet šādus failus:

        - **Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll** montāžas fails
        - Konfigurācijas **fails Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll.config**

    2. Kopējiet failus nodalījuma **\\** mapē, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    3. Reģistrējiet CRT izmaiņas paplašinājuma konfigurācijas CRT failā. Šī faila nosaukums ir **commerceruntime.ext.config, un tas atrodas nodalījuma mapē** zem **IIS** Retail Server vietnes atrašanās vietas.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later/)

    1. Mapē **CommerceRuntime \\ Extensions.SalesTransactionSignmediaSample.Messages bin Atkļūdošanas mape \\ atrodas \\** **Contoso.Commerce.Runtime.SalesTransactionSignactionSample.Messages.dll** montāžas failu.
    2. Kopējiet failu uz nodalījuma **\\** mapi, kas atrodas IIS Retail Server vietnes atrašanās vietā.
    3. Reģistrējiet CRT izmaiņas paplašinājuma konfigurācijas CRT failā. Šī faila nosaukums ir **commerceruntime.ext.config, un tas atrodas nodalījuma mapē** zem **IIS** Retail Server vietnes atrašanās vietas.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Nekādas darbības nav nepieciešamas.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    > [!NOTE]
    > Nekādas darbības nav nepieciešamas.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    > [!NOTE]
    > Nekādas darbības nav nepieciešamas.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    > [!NOTE]
    > Nekādas darbības nav nepieciešamas.

    ---

### <a name="the-modern-pos-extension-components"></a>Modern POS paplašinājuma komponenti

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Ieviest starpniekservera kodu bezsaistes režīmam

Šī daļa ir ekvivalenta Retail Servera kontrollerim, taču tā paplašina lokālu versiju, ko CRT izmanto, kad klients nav izveidojis savienojumu.

1. Pielāgojumu.iestatījumu failā mainiet **sadaļu** **@(RetailServerLibraryPathForProxyGeneration), lai tajā tiek izmantota jaunā Retail Server montāža** starpniekservera ģenerēšanai.
2. Implementē tālāk norādītās interfeisa metodes **klasē StoreOperationsManager.** Pirmajam atkārtojumam pievienojiet šādu kodu:

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    ---

3. Lai atkārtoti ģenerētu starpniekservera kodu, izveidojiet starpniekserveru mapi no komandrindas, izmantojot **komandu** **msbuild/t:Rebuild.**
4. Atrisināt **Proxies.RetailProxy** projekta atkarības:

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    Atveriet **RetailSDK \\ Proxies \\ RetailProxy \\ Proxies.RetailProxy.csproj, pievienojiet risinājumam** **RetailSDK \\ SampleExtensions \\ CommerceRuntime \\ Extensions.SalesTransactionSignmediaSample \\ CommerceRuntime.Extensions.SalesTransactionSignactionSample projektu un pievienojiet projekta atsauci projektam RetailProxy atsaucei uz** **·** **SalesTransactionSignactionSample.**

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    Atveriet **RetailSDK \\ Proxies \\ RetailProxy \\ Proxies.RetailProxy.csproj, pievienojiet** **RetailSDK \\ SampleExtensions \\ CommerceRuntime \\ paplašinājumus.SalesTransactionSignmediaSample.Messages \\ CommerceRuntime.Extensions.SalesTransactionSignactionSample.Messages projektu risinājumam un pievienojiet projekta atsauci uz RetailProxy projektu atsaucei** **·** **SalesTransactionSignactionSignactionSample.Messages.**

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    ---

5. Koriģējiet interfeisa metodes **klasē StoreOperationsManager:**

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    > [!NOTE]
    > Šī darbība neattiecas uz šo versiju.

    ---

6. Atjauniniet **failu dllhost.exe.config, lai klienta** starpnieks ielādētu jauno RetailProxy montāžu.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Mazumtirdzniecības starpniekservera paplašinājuma komponents (Retail 7.3.1 un jaunāka versija)

Veiciet tālāk norādītās darbības tikai tad, ja izmantojat programmu Retail 7.3.1 vai jaunāku versiju.

1. **RetailSDK \\ SampleExtensions \\ RetailProxy \\ RetailProxy.Extensions.SalesTransactionSignactionSample mapē atrodiet projektu** **RetailServer.Extensions.SalesTransactionSignmediaSample** un izveidojiet to.
2. Mapē **RetailProxy \\ RetailProxy.Extensions.SalesTransactionSignmediaSample bin Atkļūdošanas mape \\\\ atrodiet** **Contoso.Commerce.RetailProxy.SalesTransactionSignactionSample montāžas** failu.
3. Kopējiet komplektācijas failus ārējā **\\** mapē lokālā klienta CRT starpnieka atrašanās vietā.
4. Reģistrēt mazumtirdzniecības starpniekservera izmaiņas paplašinājuma konfigurācijas failā. Faila nosaukums ir **RetailProxy.MPOSOffline.ext.config, un tas atrodas lokālā** klienta CRT starpnieka atrašanās vietā.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Modernie POS paplašinājuma komponenti

1. Atveriet risinājumu **retailSdk \\ POS ModernPOS.sln un pārliecinieties, vai to var \\** kompilēt bez kļūdām. Turklāt pārliecinieties, ka modern POS var darbināt no Visual Studio Microsoft, izmantojot **komandu** Palaist.

    > [!NOTE]
    > Modern POS nevar pielāgot. Ir jāiespējo lietotāja konta kontrole (UAC), un jums pēc vajadzības jāatinstalē iepriekš instalētās Modern POS instances.

2. Ietveriet šādas esošās avota koda mapes **POS.Extensions** projektā.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    ---

3. Iespējojiet paplašinājumus, kas ir kompilēti **tsconfig.json,** noņemot šādas mapes no izslēgšanas saraksta.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    ---

4. Iespējojiet paplašinājumu iekraut **paplašinājumos.json,** atbilstošā vietā pievienojot tālāk norādītās rindas.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Papildinformāciju par paraugi, kas parāda, kā iekļaut pirmkoda mapes un iespējot ielādēšanai paplašinājumus, skatiet instrukcijas readme.md **pos.Extensions** projektā.

5. Atjaunot risinājumu.
6. Atkļūdotāja izpildiet Modern POS un pārbaudiet funkcionalitāti.

### <a name="cloud-pos-extension-components"></a>Mākoņa POS paplašinājuma komponenti

1. Atveriet risinājumu **retailSdk \\ POS CloudPOS.sln un pārliecinieties, vai to var \\** kompilēt bez kļūdām.
2. Ietveriet šādas esošās avota koda mapes **pos.Extensions** projektā.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    ---

3. Iespējojiet paplašinājumus, kas ir kompilēti **tsconfig.json,** noņemot šādas mapes no izslēgšanas saraksta.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    - SalesTransactionSignactionSample
    - SalesTransactionSignactionNorway
    - Secīgsparāds

    ---

4. Iespējojiet paplašinājumu iekraut **paplašinājumos.json,** atbilstošā vietā pievienojot tālāk norādītās rindas.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Papildinformāciju par paraugi, kas parāda, kā iekļaut pirmkoda mapes un iespējot ielādēšanai paplašinājumus, skatiet instrukcijas readme.md **pos.Extensions** projektā.

5. Atjaunot risinājumu.
6. Palaidiet risinājumu, izmantojot komandu **Palaist** un izpildiet Retail SDK rokasgrāmatā norādītās darbības.
7. Pārbaudiet funkcionalitāti.

### <a name="set-up-required-parameters-in-headquarters"></a>Iestatīt programmā Headquarters nepieciešamos parametrus

Plašāku informāciju skatiet kases [sistēmas funkcionalitātē Norvēģijai.](./emea-nor-cash-registers.md)

## <a name="production-environment"></a>Ražošanas vide

Veiciet šīs darbības, lai izveidotu izvietojamas pakotnes, kurās ir Commerce komponenti, un lai piemērotu šīs pakotnes ražošanas vidē.

1. Veiciet tālāk šīs tēmas sadaļā aprakstītās darbības Mākoņa POS paplašinājuma komponentos vai [Modern](#cloud-pos-extension-components) POS [paplašinājuma](#modern-pos-extension-components) komponentu sadaļā.
2. Mapē **RetailSdk Assets pakotnes konfigurācijas failos veiciet \\ tālāk norādītās** izmaiņas.

    1. **Commerceruntime.ext.config un** **CommerceRuntime.MPOSOffline.Ext.config konfigurācijas failos pievienojiet šim sastāva** **sadaļai** šādas rindas:

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Iespējot Commerce starpniekservera pielāgošanu:

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        Konfigurācijas failā **dllhost.exe.config pievienojiet tālāk norādītās rindas** **konfigurācijas sadaļas appSettings** **apakšsadaļai.**

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

        Konfigurācijas failā **dllhost.exe.config pievienojiet tālāk norādītās rindas** **konfigurācijas sadaļas appSettings** **apakšsadaļai.**

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

        Konfigurācijas failā **RetailProxy.MPOSOffline.ext.config pievienojiet** sastāva sadaļai **šādas** rindas:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

        Konfigurācijas failā **RetailProxy.MPOSOffline.ext.config pievienojiet** sastāva sadaļai **šādas** rindas:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

        Konfigurācijas failā **RetailProxy.MPOSOffline.ext.config pievienojiet** sastāva sadaļai **šādas** rindas:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

        Konfigurācijas failā **RetailProxy.MPOSOffline.ext.config pievienojiet** sastāva sadaļai **šādas** rindas:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Pielāgošanas.iestatījumu pakotnes **pielāgošanas** konfigurācijas failā veiciet šādas izmaiņas:

    1. Iespējojiet Retail starpniekservera pielāgošanu.

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        Pievienojiet tālāk norādītās rindas sadaļai **&lt; ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == &gt;** '' .

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

        Pievienojiet tālāk norādītās rindas sadaļai **&lt; ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == &gt;** '' .

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

        Pievienojiet tālāk norādītās rindas sadaļai **ItemGroup**, lai ietvertu Retail starpniekservera paplašinājumu izvietojamās pakotnēs:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

        Pievienojiet tālāk norādītās rindas sadaļai **ItemGroup**, lai ietvertu Retail starpniekservera paplašinājumu izvietojamās pakotnēs:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

        Pievienojiet tālāk norādītās rindas sadaļai **ItemGroup**, lai ietvertu Retail starpniekservera paplašinājumu izvietojamās pakotnēs:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

        Pievienojiet tālāk norādītās rindas sadaļai **ItemGroup**, lai ietvertu Retail starpniekservera paplašinājumu izvietojamās pakotnēs:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Pievienojiet sadaļai ItemGroup tālāk **norādītās** rindas, lai CRT ietvertu paplašinājumus izvietojamās pakotnēs:

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Pievienojiet sadaļai **ItemGroup tālāk norādītās** rindas, lai ietvertu Retail Server paplašinājumu izvietojamās pakotnēs:

        # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Modificējiet tālāk norādītos failus, lai ietvertu Norvēģijas resursu failus izvietojamās pakotnēs:
    - Iepakojumi \_ SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Iepakojumi\RetailServer\Sdk.RetailServerSetup.proj
  
  - **Sdk.ModernPos.Shared.csproj** failam 
    - Pievienot rindu sadaļai **ItemGroup**
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Tā <File_name> resursu faila nosaukumu. Tas pats attiecas uz citiem tālāk minētiem piemēriem.
 
    - Pievienot rindu mērķa **nosaukumam="CopyPackageFiles"** sadaļai
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - Failam **Sdk.RetailServerSetup.proj** 
    - Pievienot rindu sadaļai **ItemGroup**
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Pievienot rindu mērķa **nosaukumam="CopyPackageFiles"** sadaļai
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Modificējiet sertifikāta konfigurācijas failu, norādot īssavilkumu, veikala atrašanās vietu un veikala nosaukumu sertifikātam, kas ir jāizmanto pārdošanas transakciju parakstam. Pēc tam kopējiet konfigurācijas failu **uz mapi** Atsauces.

    # <a name="application-update-4"></a>[Application Update 4](#tab/app-update-4)

    Faila nosaukums ir **Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll.dll.config, un tā paplašinājums ir** **CommerceRuntime \\ Extensions.SalesTransactionSignactionSample \\ bin \\ Atkļūdotājs**.

    # <a name="application-update-5-and-later"></a>[5. un jaunāka programmas atjaunināšana](#tab/app-update-5-and-later)

    Faila nosaukums ir **Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll.dll.config, un tā paplašinājums ir** **CommerceRuntime \\ Extensions.SalesTransactionSignactionSample \\ bin \\ Atkļūdotājs**.

    # <a name="retail-731"></a>[Mazumtirdzniecības 7.3.1](#tab/retail-7-3-1)

    Faila nosaukums ir **Contoso.Commerce.Runtime.SalesTransactionSignactionSample.dll.dll.config, un tā paplašinājums ir** **CommerceRuntime \\ Extensions.SalesTransactionSignactionSample \\ bin \\ Atkļūdotājs**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 vai jaunāka versija](#tab/retail-7-3-2)

    Faila nosaukums ir **Contoso.Commerce.Runtime.SequentialSignllaRegister.dll.config, un tā atrodas** paplašinājumos.SequentialSign **runtimeregister \\ bin \\ atkļūdotājs.**

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 vai jaunāka versija](#tab/retail-7-3-5)

    Faila nosaukums ir **Contoso.Commerce.Runtime.SequentialSignllaRegister.dll.config, un tā atrodas** paplašinājumos.SequentialSign **runtimeregister \\ bin \\ atkļūdotājs.**

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 vai jaunāka versija](#tab/retail-8-1-1)

    Faila nosaukums ir **Contoso.Commerce.Runtime.SequentialSignllaRegister.dll.config, un tā atrodas** paplašinājumos.SequentialSign **runtimeregister \\ bin \\ atkļūdotājs.**

    ---

6. Atjauniniet Retail Server konfigurācijas failu. Failā **RetailSDK \\ Packages \\ RetailServer Code web.config pievienojiet sadaļā \\\\** **extensionComposition norādītās** rindas.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Palaidiet **msbuild** visam Retail SDK, lai izveidotu izvietojamas pakotnes.
8. Izmantojiet pakotnes, izmantojot Microsoft Dynamics Lifecycle Services (LCS) vai manuāli. Papildinformāciju skatiet sadaļā [Izvietojamu pakotņu](../dev-itpro/retail-sdk/retail-sdk-packaging.md) izveide.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Iespējojiet ciparparakstu Modern POS bezsaistes režīmā

Lai iespējotu ciparparakstu Modern POS bezsaistes režīmā, pēc Modern POS aktivizēšanas jaunā ierīcē veiciet šīs darbības.

1. Pierakstieties POS.
2. Lapā Datu **bāzes savienojuma statuss** pārliecinieties, vai bezsaistes datu bāze ir pilnībā sinhronizēta. Ja lauka Gaidošie **lejupielādes vērtība** ir **0** (nulle), datu bāze ir pilnībā sinhronizēta.
3. Izrakstīties no POS.
4. Uzgaidiet, kamēr bezsaistes datu bāze ir pilnībā sinhronizēta.
5. Pierakstieties POS.
6. Lapā Datu **bāzes savienojuma statuss** pārliecinieties, vai bezsaistes datu bāze ir pilnībā sinhronizēta. Ja gaidošo darbību **vērtība bezsaistes datu bāzes** laukā ir **0** (nulle), datu bāze ir pilnībā sinhronizēta.
7. Restartējiet Modern POS.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
