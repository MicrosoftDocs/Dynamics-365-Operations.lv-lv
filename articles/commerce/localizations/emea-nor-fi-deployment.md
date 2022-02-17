---
title: Norvēģijas kases aparātu izvietošanas vadlīnijas
description: Šajā tēmā ir sniegti norādījumi par to, kā iespējot kases aparāta funkcionalitāti Microsoft Dynamics 365 Commerce lokalizācija Norvēģijai.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: f0744b18ed59c692ae336c92e488d339ae158368
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077144"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Norvēģijas kases aparātu izvietošanas vadlīnijas

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegti norādījumi par to, kā iespējot kases aparāta funkcionalitāti Microsoft Dynamics 365 Commerce lokalizācija Norvēģijai. Lokalizācija sastāv no vairākiem komponentu paplašinājumiem. Šie paplašinājumi ļauj veikt tādas darbības kā pielāgotu lauku drukāšana kvītīs, papildu audita notikumu, pārdošanas darījumu un maksājumu darījumu reģistrēšana tirdzniecības vietā (POS), pārdošanas darījumu digitālā parakstīšana un pārskatu drukāšana vietējos formātos. Papildinformāciju par Norvēģijas lokalizāciju skatiet [Kases aparāta funkcionalitāte Norvēģijai](./emea-nor-cash-registers.md). Papildinformāciju par to, kā konfigurēt Commerce Norvēģijai, skatiet [Iestatiet komerciju Norvēģijai](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šai lokalizācijas funkcionalitātei. Jums ir jāizmanto Norvēģijai paredzētā digitālā paraksta parauga versija mazumtirdzniecības programmatūras izstrādes komplekta (SDK) iepriekšējā versijā izstrādātāja virtuālajā mašīnā (VM)Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Papildinformāciju skatiet [Norvēģijas kases aparātu izvietošanas vadlīnijas (mantots)](./emea-nor-loc-deployment-guidelines.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

## <a name="set-up-fiscal-registration-for-norway"></a>Iestatiet Norvēģijas fiskālo reģistrāciju

Norvēģijas fiskālās reģistrācijas paraugs ir balstīts uz [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **src\\ Fiskālā integrācija\\ SequentialSignatureNorvēģija** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijs (piemēram, [paraugs izlaidumā/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāju un fiskālo savienotāju, kas ir Commerce izpildlaika paplašinājumi (CRT). Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

Pabeidziet fiskālās reģistrācijas iestatīšanas darbības, kas aprakstītas rakstā [Iestatiet fiskālo integrāciju tirdzniecības kanāliem](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Iestatiet fiskālās reģistrācijas procesu](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Noteikti pierakstiet fiskālās reģistrācijas procesa iestatījumus [specifiski Norvēģijai](#configure-the-fiscal-registration-process).
1. [Iestatiet kļūdu apstrādes iestatījumus](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iespējot atliktās fiskālās reģistrācijas manuālu izpildi](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Konfigurējiet fiskālās reģistrācijas procesu

Veiciet šīs darbības, lai iespējotu Norvēģijas fiskālās reģistrācijas procesu Commerce galvenajā mītnē.

1. Lejupielādējiet fiskālo dokumentu nodrošinātāja un fiskālā savienotāja konfigurācijas failus no Commerce SDK:

    1. [Dynamics 365 Commerce Atveriet risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atveriet pēdējo pieejamo laidiena filiāli (piemēram, **[izlaidums/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Atvērt **src \> Fiskālā integrācija \> SequentialSignatureNorvēģija \> CommerceRuntime**.
    1. Lejupielādējiet fiskālo dokumentu nodrošinātāja konfigurācijas failu vietnē **DocumentProvider.SequentialSignNorway \> Konfigurācija \> DocumentProviderSequentialSignatureNorwaySample.xml** (piemēram, [izlaišanas fails/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)).
    1. Lejupielādējiet fiskālā savienotāja konfigurācijas failu vietnē **Connector.SequentialSignNorway \> Konfigurācija \> ConnectorSequentialSignatureNorwaySample.xml** (piemēram, [izlaišanas fails/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)).

1. Iet uz **Mazumtirdzniecība un tirdzniecība \> Galvenās mītnes iestatīšana \> Parametri \> Kopīgie parametri**. Cilnē **Vispārīgi** iestatiet opciju **Iespējot finanšu integrāciju** uz **Jā**.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connectors un ielādējiet iepriekš lejupielādēto finanšu savienotāja konfigurācijas** failu.
1. Dodieties uz **Mazumtirdzniecības un tirdzniecības \> kanāla iestatījumu \> Finanšu integrācija \> Finanšu dokumentu nodrošinātāji** un ielādējiet iepriekš lejupielādēto finanšu dokumentu nodrošinātāja konfigurācijas failu.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector funkcionālie profili**. Izveidojiet jaunu savienotāja funkcionālo profilu un atlasiet dokumentu nodrošinātāju un savienotāju, ko ielādējāt iepriekš.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet savienotāju, kuru ielādējāt iepriekš. Iestatiet savienotāja veidu uz **Iekšējais**.
1. Iet uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālo savienotāju grupas** un izveidojiet jaunu fiskālo savienotāju grupu savienotāja funkcionālajam profilam, ko izveidojāt iepriekš.
1. Iet uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālās reģistrācijas procesi**. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālā reģistrācijas procesa darbību un atlasiet iepriekš izveidoto fiskālo savienotāju grupu.
1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Izvēlieties funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā jāaktivizē reģistrācijas process. Uz **Fiskālās reģistrācijas process** FastTab atlasiet fiskālās reģistrācijas procesu, ko izveidojāt iepriekš. Uz **Fiskālie pakalpojumi** FastTab atlasiet savienotāja tehnisko profilu, ko izveidojāt iepriekš. 
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**. Atveriet izplatīšanas grafiku un atlasiet darbus **1070** un **1090** lai pārsūtītu datus uz kanālu datu bāzi.

### <a name="configure-the-digital-signature-parameters"></a>Konfigurējiet digitālā paraksta parametrus

Jums ir jākonfigurē sertifikāti, kas tiks izmantoti pārdošanas darījumu ciparparakstīšanai veikalā. Parakstīšanai tiek izmantots digitālais sertifikāts, kas tiek glabāts Azure Key Vault. Modernās POS bezsaistes režīmā parakstīšanu var veikt arī, izmantojot digitālo sertifikātu, kas tiek saglabāts tās iekārtas lokālajā krātuvē, kurā ir instalēta Modern POS.

Lai varētu izmantot ciparu sertifikātu, kas tiek glabāts Key Vault krātuvē, ir jāveic šādas darbības.

1. Jāizveido Key Vault krātuve. Mēs iesakām izvietot krātuvi tajā pašā ģeogrāfiskajā reģionā, kur atrodas Commerce Scale Unit.
1. Sertifikāts ir jāaugšupielādē Key Vault krātuvē kā base64 virknes noslēpums.
1. Lietojumprogrammu objektu servera (AOS) lietojumprogrammai jābūt pilnvarotai nolasīt noslēpumus no Key Vault krātuves.

Papildinformāciju par to, kā strādāt ar Key Vault, skatiet sadaļā [Sāciet darbu ar Azure Key Vault](/azure/key-vault/key-vault-get-started).

Tālāk, uz **Key Vault parametri** lapā, jums jānorāda parametri, lai piekļūtu Key Vault krātuvei:

- **Vārds** un **Apraksts** – Key Vault krātuves nosaukums un apraksts.
- **Key Vault URL** — Key Vault krātuves URL.
- **Key Vault klients** – interaktīvs klienta ID Azure Active Directory (Azure AD) lietojumprogramma, kas autentifikācijas nolūkos ir saistīta ar Key Vault krātuvi. Šim klientam ir jābūt piekļuvei krātuves noslēpumu lasīšanai.
- **Key Vault slepenā atslēga** - Slepenā atslēga, kas ir saistīta ar Azure AD lietojumprogramma, kas tiek izmantota autentifikācijai Key Vault krātuvē.
- **Vārds**, **·**, un **Slepenā atsauce** – Sertifikāta nosaukums, apraksts un slepenā atsauce.

Pēc tam jums ir jākonfigurē savienotājs saviem sertifikātiem, kas tiek glabāti Key Vault vai vietējā sertifikātu krātuvē. Šis savienotājs tiek izmantots parakstīšanai kanāla pusē.

1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**.
1. Uz **Iestatījumi** FastTab, norādiet šādus ciparparakstu parametrus:

    - **Slepenais vārds** – Atlasiet slepeno nosaukumu, ko iepriekš konfigurējāt **Key Vault parametri** lappuse.
    - **Vietējā sertifikāta īkšķa nospiedums** – Nodrošiniet īkšķa nospiedumu sertifikātam, kas tiek glabāts lokāli.
    - **Hash algoritms** – Norādiet vienu no atbalstītajiem kriptogrāfijas jaukšanas algoritmiem Microsoft .NET, piemēram, **SHA1**.
    - **Sertifikātu veikala nosaukums** – Šis lauks nav obligāts. Izmantojiet to, lai norādītu noklusējuma veikala nosaukumu, kas jāizmanto lokālo sertifikātu meklēšanai.
    - **Sertifikātu veikala atrašanās vieta** – Šis lauks nav obligāts. Izmantojiet to, lai norādītu noklusējuma veikala atrašanās vietu, kas jāizmanto lokālo sertifikātu meklēšanai.
    - **Vispirms izmēģiniet vietējo sertifikātu** – Atlasiet šo opciju, lai pēc noklusējuma datu parakstīšanai izmantotu sertifikātu no vietējā veikala, nevis sertifikātu no Key Vault.
    - **Aktivizējiet veselības pārbaudi** – Papildinformāciju par veselības pārbaudes funkciju sk [Fiskālās reģistrācijas veselības pārbaude](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Tikai **SHA1** kriptogrāfiskais jaukšanas algoritms pašlaik ir pieņemams Norvēģijā.
> - Noklusējuma veikala nosaukums un veikala atrašanās vieta ir pievienoti, lai vienkāršotu vietējo sertifikātu meklēšanas procesu CRT. X509StoreProvider satur sarakstu ar mapēm, kur tiek glabāti sertifikāti. Ja noklusējuma veikala nosaukums un noklusējuma veikala atrašanās vieta nav norādīts, X509StoreProvider mēģina atrast sertifikātu visās tā sarakstā esošajās mapēs.

### <a name="configure-channel-components"></a>Konfigurējiet kanāla komponentus

### <a name="development-environment"></a>Izstrādes vide

Veiciet šīs darbības, lai iestatītu izstrādes vidi, lai varētu pārbaudīt un paplašināt paraugu.

1. Klonējiet vai lejupielādējiet [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve. Atlasiet pareizo laidiena filiāles versiju atbilstoši savai SDK/lietojumprogrammas versijai. Papildinformāciju skatiet [Lejupielādējiet mazumtirdzniecības SDK paraugus un atsauces pakotnes no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet **SequentialSignatureNorway.sln** risinājums zem **Dynamics365Commerce.Solutions\\ Fiskālā integrācija\\ SequentialSignatureNorvēģija**, un izveidojiet to.
1. Uzstādīt CRT paplašinājumi:

    1. Atrodi CRT paplašinājumu instalētājs:

        - **Tirdzniecības mēroga vienība:** Iekš **SequentialSignatureNorvēģija\\ Mērvienība\\ ScaleUnit.SequentialSignNorway.Installer\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **ScaleUnit.SequentialSignNorway.Installer** uzstādītājs.
        - **Vietējais CRT Mūsdienu POS:** Iekš **SequentialSignatureNorvēģija\\ Modern POS\\ ModernPos.SequentialSignNorvēģija.Instalētājs\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **ModernPos.SequentialSignNorvēģija.Instalētājs** uzstādītājs.

    1. Sāciet CRT paplašinājuma instalētājs no komandrindas:

        - **Tirdzniecības mēroga vienība:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Vietējais CRT Mūsdienu POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Ražošanas vide

Izpildiet norādījumus [Fiskālās integrācijas parauga izveides konveijera iestatīšana](fiscal-integration-sample-build-pipeline.md) lai ģenerētu un atbrīvotu Cloud Scale Unit un pašapkalpošanās izvietojamās pakotnes fiskālās integrācijas paraugam. **SequentialSignatureNorway build-pipeline.yaml** veidnes YAML failu var atrast **risinājumu\\ repozitorija mapē** Pipeline [Dynamics 365 Commerce YAML_Files](https://github.com/microsoft/Dynamics365Commerce.Solutions).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Digitālā paraksta iespējošana bezsaistes režīmā modern pos

Lai iespējotu ciparparakstu modern pos bezsaistes režīmā, pēc modern POS aktivizēšanas jaunā ierīcē ir jāveic šīs darbības.

1. Pierakstieties POS.
1. **Lapā Datu bāzes savienojuma statuss** pārliecinieties, vai bezsaistes datu bāze ir pilnībā sinhronizēta. Ja lauka Gaida lejupielādes **vērtība** ir **0** (nulle), datu bāze ir pilnībā sinhronizēta.
1. Izrakstieties no POS.
1. Pagaidiet, līdz bezsaistes datu bāze tiek pilnībā sinhronizēta.
1. Pierakstieties POS.
1. **Lapā Datu bāzes savienojuma statuss** pārliecinieties, vai bezsaistes datu bāze ir pilnībā sinhronizēta. Ja nepabeigto **transakciju vērtība bezsaistes datu bāzes** laukā ir **0** (nulle), datu bāze ir pilnībā sinhronizēta.
1. Atkārtoti atveriet moderno POS.
