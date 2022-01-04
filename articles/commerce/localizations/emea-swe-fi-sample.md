---
title: Vadības ierīces integrācijas paraugs izmantošanai Zviedrijā
description: Šajā tēmā sniegts zviedrijas finanšu integrācijas parauga apskats Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 32c2cf31d82d17d3391536e7a9f1722e1462c336
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944770"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Vadības ierīces integrācijas paraugs izmantošanai Zviedrijā

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegts zviedrijas finanšu integrācijas parauga apskats Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Šis finanšu integrācijas funkcionalitātes paraugs aizstāj [agrāko POS integrēšanas paraugu ar Zviedrijas kontroles vienībām](retail-sdk-control-unit-sample.md). Agrākais paraugs neizmanto finanšu integrācijas struktūras priekšrocības [un](./fiscal-integration-for-retail-channel.md) vēlākos atjauninājumos kļūs novecojis. Papildinformāciju par to, kā migrēt no agrākā parauga uz paraugu, kas atbilst Dynamics 365 Commerce **versijai 10.0.22 vai jaunākai versijai, skatiet Migrēšana no agrākā**[integrācijas](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample) parauga.

Zviedrijas Commerce funkcionalitāte ietver pārdošanas punkta (POS) parauga integrēšanu ar Zviedrijas raksturīgajām finanšu ierīcēm, kas pazīstamas kā *kontroles* vienības. Šis paraugs paplašina finanšu [integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti. Ir pieņemts, ka vadības vienība ir fiziski savienota ar aparatūras staciju, ar kuru POS ir savienots pārī. Piemēram, šim parauga vienībai tiek izmantots [CleanCash tipa A](https://www.retailinnovation.se/produkter) kontroles vienības programmas programmēšanas interfeiss (API). Tiek izmantota CleanCash API versija 1.1.4.

Paraugs ir nodrošināts avota koda formā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Korporācija Microsoft neatlaiž nevienu aparatūru, programmatūru vai dokumentāciju no Retail Gmt HTT AB. Lai iegūtu informāciju par to, kā vadības mērvienība ir pieejama un to var izmantot, sazinieties ar [mazumtirdzniecībastāŠturs HTT](https://www.retailinnovation.se/) AB.

## <a name="scenarios"></a>Scenāriji

Zviedrijas kontroles vienības integrācijas paraugs ietver šādas iespējas:

- Pārdošanas, atgriešanas un kvīšu kopijas tiek automātiski reģistrētas vadības vienībā, kas ir pievienota aparatūras stacijai, kas ir savienota pārī ar POS.
- Reģistrētas darbības kontroles vienības kontroles kods un ražošanas numurs tiek iegūts no kontroles vienības un saglabāts darbībā. Šie dati tiek saukti arī par *finanšu* atbildi. Finanšu atbildi var skatīt veikala **darbību** lapā.
- Ieejas plūsmas izkārtojumam var pievienot pielāgotus kontroles kodus un kontroles vienības ražošanas numuru. Šādā veidā var drukāt finanšu atbildi darbībai uz saņemšanas.
- Darbības finanšu atbilde ir parādīta elektroniskā žurnāla **(Zviedrija)** kanāla pārskatā.
- Ir pieejamas vairākas kļūdu apstrādes opcijas. Daži piemēri:

    - Atkārtot finanšu reģistrāciju, ja iespējams atkārtot. Fiskālo reģistrāciju varat atkārtot, ja, piemēram, kontroles vienība nav pievienota, nav gatava vai nav atbildēta.
    - Atlikt finanšu reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darbību kā reģistrētu un ietveriet infokodus, lai iegūtu kļūmes iemeslu un papildinformāciju.
    - Pirms jaunas pārdošanas darbības atvēršanas vai pārdošanas darbības veikšanas pārbaudiet kontroles vienības pieejamību.

### <a name="limitations-of-the-sample"></a>Parauga ierobežojumi

Kontroles vienības integrācijas paraugs Zviedrijā pašlaik neatbalsta debitoru pasūtījumu scenārijus.

## <a name="setting-up-the-integration-with-control-units"></a>Integrācijas ar vadības vienībām iestatīšana

Papildinformāciju par Zviedrijas iestatījumiem skatiet Zviedrijas [Commerce](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden) iestatīšana.

### <a name="configuring-swedenspecific-receipts"></a>Zviedrijai specifisku ieejas plūsmu konfigurēšana

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotos laukus, lai tos varētu izmantot pārdošanas ieejas plūsmu saņemšanas formātiem

Varat konfigurēt valodas tekstu un pielāgotos laukus, kas tiek izmantoti POS ieejas plūsmas formātos. Tā lietotāja noklusējuma uzņēmumam, kurš izveido saņemšanas iestatījumus, jābūt tai pašai juridiskajai personai, kurai tiek veidoti valodas teksta iestatījumi. Alternatīvi vienādi valodas teksti ir jāizveido gan lietotāja noklusējuma uzņēmumā, gan veikala juridiskajā personām, kam ir izveidots iestatījums.

Lapā **Valodas teksts** pievienojiet šādus ierakstus kvīts izkārtojumiem pielāgoto lauku etiķetēm. **Ievērojiet, ka tabulā** **parādītās valodas ID, teksta ID un teksta vērtības ir tikai** **piemēri**. Jūs varat mainīt tos tā, lai tie atbilstu jūsu prasībām. Taču jūsu **izmantotajām teksta ID** vērtībām ir jābūt unikālām un vienādām ar vai lielākam par 900001.

Valodas teksta lapas POS sadaļā POS pievienojiet šādas **POS** **etiķetes**.

| Valodas kods | Teksta ID | Teksts                  |
|-------------|---------|-----------------------|
| en-ASV       | 900001  | Reģistra kontroles kods |
| en-ASV       | 900002  | Reģistrēt ierīci       |

Pielāgoto **lauku lapā pievienojiet šiem ierakstiem kvīts izkārtojumu** pielāgotajiem laukiem. **Ievērojiet, ka** uzraksta teksta ID vērtībām ir jāatbilst teksta **ID** vērtībām, kas norādītas **teksta lapā** Valoda.

| Nosaukums                         | Veids    | Uzraksta teksta ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Saņemšana | 900001          |
| SE_FISCALREGISTERID          | Saņemšana | 900002          |

> [!NOTE]
> Ir svarīgi norādīt pareizus pielāgotos lauku nosaukumus, kā norādīts augstāk esošajā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs ieejas plūsmās trūkstošo datu.

#### <a name="configure-receipt-formats"></a>Konfigurēt ieejas plūsmas formātus

Katram pieprasītam kvīts formātam mainiet lauka Drukāšanas režīms **vērtību uz** Vienmēr **drukāt**.

Sadaļai Kājene pievienojiet šādus pielāgotos laukus kvīts formāta **veidotājā**. Ievērojiet, ka lauku nosaukumi atbilst valodas tekstiem, kas definēti šīs tēmas iepriekšējā sadaļā.

- **Reģistra kontroles kods** – šis lauks drukā kontroles kodu.
- **Reģistra ierīce** - šis lauks drukā kontroles vienības ražošanas numuru.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, skatiet [sadaļā Kvīšu veidnes un](../receipt-templates-printing.md) drukāšana.

### <a name="set-up-fiscal-integration-for-sweden"></a>Iestatīt Zviedrijas finanšu integrāciju

Kontroles vienības integrācijas paraugs Zviedrijai ir balstīts uz [finanšu integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no Retail SDK. Paraugs atrodas Solutions repository mapē **src \\ FiscalIntegration \\ CleanCash**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash) Paraugs sastāv no fiskālā dokumenta nodrošinātāja, kas ir Commerce Runtime () paplašinājums () un finanšu savienotājs, kas ir [Commerce](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) Hardware Station CRT paplašinājums. Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātāja virtuālajā datorā (VM) pakalpojumos Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet Zviedrijas [kontroles vienības integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-swe-fi-sample-sdk.md)
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

Izpildiet finanšu integrācijas iestatīšanas soļus, kā [aprakstīts Commerce kanālu finanšu integrācijas iestatīšanai.](setting-up-fiscal-integration-for-retail-channel.md)

1. [Iestatīt finanšu reģistrācijas](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) procesu. Atzīmējiet arī fiskālās reģistrācijas procesa iestatījumus, kas ir specifiski [šim kontroles vienības integrācijas paraugam.](#set-up-the-registration-process)
1. [Iestatīt kļūdu apstrādes](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) iestatījumus.
1. [Aktivizējiet atliktās finanšu reģistrācijas manuālu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) izpildi.
1. [Konfigurējiet kanāla](#configure-channel-components) komponentus.

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, izpildiet šīs darbības, lai iestatītu programmu Commerce Headquarters. Papildinformāciju skatiet [sadaļā Komercijas kanālu finanšu integrācijas](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) iestatīšana.

1. Lejupielādēt konfigurācijas failus finanšu dokumentu nodrošinātājam un finanšu savienotājam:

    1. Atveriet risinājumu [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atlasiet pareizu versijas izlaidi atbilstoši SDK/programmas versijai (piemēram, **[izlaidums/9,33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**
    1. Atveriet **src \> FiscalIntegration \> CleanCash.**
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failu **commerceRuntime \> DocumentProvider.CleanCashSample \> konfigurācijas \> DocumentProviderFiscalCleanCashSample.xml** (piemēram, fails laidienam/9,33). [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu **pie HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (piemēram, fails laidienam/9,33). [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)

    > [!WARNING]
    > Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas tālākmintās Retail SDK mapēs LCS izstrādātāja VM:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extensions.DocumentProvider.CleanCashSample \\ konfigurācijas \\ DocumentProviderFiscalCleanCashSample.xml
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ Extension.CleanCashSample \\ konfigurācijas \\ ConnectorCleanCashSample.xml
    > 
    > Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**. Cilnē **Vispārīgi** iestatiet opciju Aktivizēt fiskālo integrāciju **kā** **Jā**.
1. Dodieties uz **Retail un Commerce Channel \> iestatīšanas finanšu integrācijas finanšu dokumentu nodrošinātājiem un \>\>** ielādējiet iepriekš lejupielādēto fiskālā dokumenta nodrošinātāja konfigurācijas failu.
1. Dodieties uz **mazumtirdzniecības un commerce kanālu iestatīšanas finanšu integrācijas finanšu savienotājiem un \>\>\>** ielādējiet agrāk lejupielādēto fiskālā savienotāja konfigurācijas failu.
1. Pārejiet uz **Sadaļu Mazumtirdzniecības \> un Commerce Channel Setup Finanšu integrācijas \>\> savienotāja funkcionālie** profili. Izveidojiet jaunu savienotāja funkcionalitātes profilu. Atlasiet dokumentu nodrošinātāju un iepriekš ielādēto savienotāju. Pēc vajadzības [atjauniniet datu](#default-data-mapping) kartēšanas iestatījumus.
1. Pārejiet uz **Retail un Commerce Channel setup Fiscal integration Connector \>\>\> tehniskajiem** profiliem. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto finanšu savienotāju. Pēc vajadzības [atjauniniet](#fiscal-connector-settings) savienotāja iestatījumus.
6. Pārejiet uz **sadaļu \> Mazumtirdzniecības un Commerce kanālu \> iestatīšanas finanšu integrācijas finanšu \> savienotāja** grupas. Izveidojiet jaunu finanšu savienotāja grupu iepriekš izveidotajā savienotāja funkcionālajā profilā.
7. Pārejiet uz **mazumtirdzniecības un Commerce \> channel \> iestatīšanas finanšu integrācijas \> finanšu reģistrācijas** procesiem. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālās reģistrācijas procesa soli un atlasiet iepriekš izveidoto finanšu savienotāja grupu.
8. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Atlasiet funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā ir jāaktivizē reģistrācijas process. Kopsavilkuma **cilnē Finanšu reģistrācijas process** atlasiet iepriekš izveidoto finanšu reģistrācijas procesu.
9. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**. Atlasiet aparatūras profilu, kas ir saistīts ar aparatūras staciju, ar kuru tiks pievienots fiskālais printeris. Kopsavilkuma cilnē **Finanšu** perifērijas ierīces atlasiet iepriekš izveidoto savienotāja tehnisko profilu.
10. Atveriet sadales grafiku (Mazumtirdzniecības un Commerce Retail un Commerce IT sadales grafiks) un atlasiet darbus **\>\>** **1070 un** **1090,** lai pārsūtītu datus uz kanāla datu bāzi.

#### <a name="default-data-mapping"></a>Noklusējuma datu kartēšana

Tālāk redzamais noklusējuma datu kartējums ir ietverts finanšu dokumenta nodrošinātāja konfigurācijā, kas ir nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Pievienotās vērtības nodokļa (PVN) koda kartēšana – izmantojot šo kartēšanu ierīces noteiktām pievienotās vērtības nodokļa (PVN) kodiem** tiek iestatīti atbilstošie PVN kodi. PVN koda kartēšanas formātam jābūt šādam:

    ```
    1 : code1 ; 2 : code2
    ```

    Tālāk minēts šī formāta paskaidrojums:

    - *1* un *2 ir ierīces specifiski PVN* kodi.
    - Semikols (;) tiek izmantots kā atdalītājs.
    - *code1* un *code2 ir PVN* kodi, kas ir konfigurēti programmā Commerce Headquarters. Parauga kartējums ir jāmodificē atbilstīgi nodokļu kodiem, kas ir konfigurēti programmā.

    Kontroles vienības atbalsta līdz pat četriem PVN kodiem. Tāpēc PVN koda kartēšanu var iestatīt šādā veidā:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Vairākus PVN kodus var kartēt uz vienu un to pašu ierīces specifisko PVN kodu.

#### <a name="fiscal-connector-settings"></a>Finanšu savienotāja iestatījumi

Šādi iestatījumi ir iekļauti finanšu savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Savienojumu virkne** – vadības vienības savienojuma iestatījumi.
- **Noildze** – laiks milisekundēs, ko autovadītājs gaidīs uz kontroles vienības atbildi.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Zviedrijas [kontroles vienības integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-swe-fi-sample-sdk.md)
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

#### <a name="set-up-the-development-environment"></a>Iestatīt izstrādes vidi

Lai iestatītu izstrādes vidi un paplašinātu paraugu ņemšanas, veiciet šādus soļus.

1. Lejupielādējiet Solutions [Dynamics 365 Commerce repozitoriju vai](https://github.com/microsoft/Dynamics365Commerce.Solutions) lejupielādējiet to. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai. Papildinformāciju skatiet lejupielādes [Retail SDK paraugos un atsauces pakotnēs no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet kontroles vienības integrācijas risinājumu **dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ CleanCash CleanCash.sln** un izveidojiet to.
1. Instalēt CRT paplašinājumus:

    1. Atrast CRT paplašinājuma instalētāju:

        - **Commerce Scale Unit: mapē** **CleanCash \\\\ ScaleUnit ScaleUnit.CleanCash.Installer \\ bin \\ Atkļūdošanas net461 atrodiet mapi \\** **ScaleUnit.CleanCash.Installer** installer.
        - **Modern CRT POS lokāls:** **\\ CleanCash \\ ModernPOS ModernPOS.CleanCash.Installer bin atkļūdošanas \\\\\\ net461 mapē atrodiet** **ModernPOS.CleanCash.Installer** instalētāju.

    2. Startējiet CRT paplašinājuma instalētāju no komandrindas:

        - **Commerce Scale vienība:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Lokāls CRT modernajā POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Instalēt aparatūras stacijas paplašinājumus:

    1. Mapē **CleanCash \\ HardwareStation \\ HardwareStation.CleanCash.Installer \\ bin \\\\ Atkļūdošana net461** atrodiet **HardwareStation.CleanCash.Installer** instalētāju.
    1. Startējiet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet darbības, kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos [iepakojumus](fiscal-integration-sample-build-pipeline.md) fiskālās integrācijas parauga iepakojumam. **CleanCash būvējuma pipeline.yml veidnesPOZITOML fails var tikt atrasts Risinājumu repozitorija** YAML_Files **\\**[Dynamics 365 Commerce konveijera](https://github.com/microsoft/Dynamics365Commerce.Solutions) sarakstā.

## <a name="design-of-the-extensions"></a>Paplašinājumu dizains

Kontroles vienības integrācijas paraugs Zviedrijai ir balstīts uz [finanšu integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no Retail SDK. Paraugs atrodas Solutions repository mapē **src \\ FiscalIntegration \\ CleanCash**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash) Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) no fiskālā dokumenta nodrošinātāja, kas ir CRT Commerce Hardware Station paplašinājums un fiskālais savienotājs. Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Zviedrijas [kontroles vienības integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-swe-fi-sample-sdk.md) Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

### <a name="crt-extension-design"></a>CRT paplašinājuma dizains

Paplašinājuma, kas ir fiskālā dokumenta nodrošinātājs, nolūks ir izveidot pakalpojumiem raksturīgus dokumentus un apstrādāt atbildes no kontroles vienības.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Dokumentu nodrošinātājam ir **atsevišķs DocumentProviderCleanCash** pieprasījumu apdarinātājs. Šis apdarinātājs tiek izmantots, lai ģenerētu kontroles vienībai finanšu dokumentus.

Šis apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest — šajā pieprasījumā ir ietverta** informācija par to, kurš dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē kontroles vienībā.
- **GetSupportedRegistrableEventsDocumentProviderRequest - šis pieprasījums atgriež notikumu sarakstu,** uz kuriem ir jāabonē. Pašlaik tiek atbalstīti pārdošanas notikumi un audita notikumi.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas fails atrodas **src \\ FiscalIntegration \\ CleanCash \\ CommerceRuntime \\ DocumentProvider.CleanCashSample \\ konfigurācijas \\ DocumentProviderFiscalCleanCashSample.xml**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) risinājumu repozitorijā. Šī faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, nolūks ir sazināties ar kontroles vienību. Tas izmanto HTTP protokolu, lai iesniegtu CRT dokumentus, ko paplašinājums ģenerē kontroles vienībai. Tā apstrādā arī atbildes, kas saņemtas no kontroles vienības.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**CleanCashHandler** pieprasījumu apdarinātājs ir ieejas punkts vadības vienības pieprasījumu apstrādei.

Apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest – šis pieprasījums sūta dokumentus kontroles vienībai un** atgriež atbildi no tās.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots kontroles vienības veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – šis pieprasījums tiek izmantots, lai inicializētu kontroles vienību.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja konfigurācijas fails atrodas **src \\ FiscalIntegration \\ CleanCash \\ HardwareStation \\ Connector.CleanCashSample \\ Configuration \\ ConnectorCleanCashSample.xml,**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) kas atrodas Solutions repozitorijā. Faila mērķis ir iespējot iestatījumus finanšu savienotājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
