---
title: Vadības ierīces integrācijas paraugs izmantošanai Zviedrijā
description: Šajā tēmā ir sniegts pārskats par fiskālās integrācijas paraugu Zviedrijai Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: ace1bd5b1a06317b6753a34779ecfa96e519a63e
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077017"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Vadības ierīces integrācijas paraugs izmantošanai Zviedrijā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par fiskālās integrācijas paraugu Zviedrijai Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Šī fiskālās integrācijas funkcionalitātes paraugs aizstāj iepriekšējo [paraugs POS integrācijai ar vadības blokiem Zviedrijai](retail-sdk-control-unit-sample.md). Iepriekšējais paraugs neizmanto priekšrocības [fiskālās integrācijas sistēma](./fiscal-integration-for-retail-channel.md) un vēlākos atjauninājumos novecos. Lai iegūtu informāciju par to, kā migrēt no iepriekšējā parauga uz paraugu, kas atbilst Dynamics 365 Commerce versija **10.0.22 un agrāk**, skat [Migrēšana no iepriekšējās integrācijas parauga](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Tirdzniecības funkcionalitāte Zviedrijai ietver pārdošanas punkta (POS) parauga integrāciju ar Zviedrijai specifiskām fiskālajām ierīcēm, kas pazīstamas kā *vadības bloki*. Šis paraugs paplašina [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md). Tiek pieņemts, ka vadības bloks ir fiziski savienots ar aparatūras staciju, ar kuru POS ir savienots pārī. Piemēram, šajā paraugā tiek izmantota lietojumprogrammu saskarne (API).[CleanCash A tips](https://www.retailinnovation.se/produkter) Retail Innovation HTT AB vadības bloks. Tiek izmantota CleanCash API versija 1.1.4.

Paraugs tiek nodrošināts avota koda veidā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Microsoft neizlaiž nekādu aparatūru, programmatūru vai dokumentāciju no Retail Innovation HTT AB. Lai iegūtu informāciju par to, kā iegūt vadības ierīci un to darbināt, sazinieties ar [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Scenāriji

Zviedrijas vadības bloka integrācijas paraugs ietver šādas iespējas:

- Pārdošanas, atgriešanas un kvīšu kopijas tiek automātiski reģistrētas vadības blokā, kas ir savienots ar aparatūras staciju, kas ir savienota pārī ar POS.
- Kontroles kods un vadības bloka ražošanas numurs reģistrētam darījumam tiek uztverts no vadības bloka un saglabāts darījumā. Šie dati tiek saukti arī par a *fiskālā reakcija*. Fiskālo atbildi var apskatīt **Veikala darījumi** lappuse.
- Kvīts izkārtojumam var pievienot pielāgotus laukus kontroles kodam un vadības bloka ražošanas numuram. Tādā veidā jūs varat izdrukāt darījuma fiskālo atbildi kvītī.
- Darījuma fiskālā atbilde ir parādīta uz **Elektroniskais žurnāls (Zviedrija)** kanāla pārskats.
- Ir pieejamas vairākas kļūdu apstrādes iespējas. Daži piemēri:

    - Ja iespējams, mēģiniet vēlreiz reģistrēt fiskālu. Varat vēlreiz mēģināt veikt fiskālo reģistrāciju, ja, piemēram, vadības bloks nav pievienots, nav gatavs vai nereaģē.
    - Atlikt fiskālo reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darījumu kā reģistrētu un iekļaujiet informācijas kodus, lai fiksētu kļūmes iemeslu un papildu informāciju.
    - Pirms jauna pārdošanas darījuma atvēršanas vai pārdošanas darījuma pabeigšanas pārbaudiet vadības bloka pieejamību.

### <a name="limitations-of-the-sample"></a>Izlases ierobežojumi

Vadības bloka integrācijas paraugs Zviedrijai pašlaik neatbalsta klientu pasūtījumu scenārijus.

## <a name="setting-up-the-integration-with-control-units"></a>Integrācijas iestatīšana ar vadības blokiem

Papildinformāciju par iestatīšanu, kas nepieciešama Zviedrijai, skatiet [Tirdzniecības iestatīšana Zviedrijai](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Zviedrijai raksturīgo kvīšu konfigurēšana

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotus laukus, lai tos varētu izmantot ieejas plūsmas formātos pārdošanas ieejas plūsmām

Varat konfigurēt valodas tekstu un pielāgotos laukus, kas tiek izmantoti POS kvīšu formātos. Tā lietotāja noklusējuma uzņēmumam, kurš izveido ieejas plūsmas iestatījumus, jābūt tai pašai juridiskajai personai, kurā tiek izveidots valodas teksta iestatījums. Alternatīvi, gan lietotāja noklusējuma uzņēmumā, gan veikala juridiskajā personā, kurai ir izveidots iestatījums, ir jāizveido vieni un tie paši valodas teksti.

**Lapā Teksts** valodā pievienojiet šādus ierakstus ieejas plūsmu izkārtojumu pielāgoto lauku etiķetēm. Ņemiet vērā, **ka** tabulā norādītās vērtības Valodas ID **, Teksta ID** un **Teksts** ir tikai piemēri. Jūs varat tos mainīt, lai tie atbilstu jūsu prasībām. Tomēr, **Teksta ID** izmantotajām vērtībām ir jābūt unikālām, un tām ir jābūt vienādām ar vai lielākām par 900001.

Pievienojiet tālāk norādītās POS etiķetes **POS** sadaļā **Valodas teksts** lappuse.

| Valodas kods | Teksta ID | Teksts                  |
|-------------|---------|-----------------------|
| en-US       | 900001  | Reģistrēt kontroles kodu |
| en-US       | 900002  | Reģistrēt ierīci       |

**Lapā Pielāgotie lauki** pievienojiet šādus ierakstus pielāgotajiem laukiem saņemšanas shēmu izkārtojumiem. Pieraksti to **Parakstu teksta ID** vērtībām jāatbilst **Teksta ID** vērtības, kuras norādījāt **Valodas teksts** lappuse.

| Nosaukums                         | Veids    | Uzraksta teksta ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Saņemšana | 900001          |
| SE_FISCALREGISTERID          | Saņemšana | 900002          |

> [!NOTE]
> Ir svarīgi norādīt pareizos pielāgoto lauku nosaukumus, kā norādīts iepriekšējā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs trūkstošus datus kvītīs.

#### <a name="configure-receipt-formats"></a>Konfigurēt kvīšu formātus

Katram nepieciešamajam ieejas plūsmas formātam mainiet lauka Drukas izturēšanās **vērtību** uz **Vienmēr drukāt**.

Kvīts formāta noformētājā pievienojiet tālāk norādītos pielāgotos laukus **Kājene** sadaļā. Ņemiet vērā, ka lauku nosaukumi atbilst valodas tekstiem, ko definējāt šīs tēmas iepriekšējā sadaļā.

- **Reģistrēt kontroles kodu** – Šajā laukā tiek izdrukāts kontroles kods.
- **Reģistrēt ierīci** – Šajā laukā tiek izdrukāts vadības bloka ražošanas numurs.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, skatiet [Kvītu veidnes un druka](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Izveidot fiskālo integrāciju Zviedrijai

Vadības bloka integrācijas paraugs Zviedrijai ir balstīts uz [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **src\\ Fiskālā integrācija\\ CleanCash** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijs (piemēram, [paraugs izlaidumā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir Commerce izpildlaika paplašinājums (CRT), un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Izstrādātāja virtuālajā mašīnā (VM) ir jāizmanto iepriekšējā mazumtirdzniecības SDK versija Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Papildinformāciju skatiet [Izvēršanas vadlīnijas vadības bloku integrācijas paraugam Zviedrijai (mantots)](emea-swe-fi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

Pabeidziet finanšu integrācijas iestatīšanas soļus, kā aprakstīts sadaļā [Iestatīt finanšu integrāciju commerce kanāliem](setting-up-fiscal-integration-for-retail-channel.md).

1. [Iestatiet finanšu reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Pierakstiet arī fiskālās reģistrācijas procesa iestatījumus [raksturīgs šim vadības bloka integrācijas paraugam](#set-up-the-registration-process).
1. [Iestatiet kļūdu apstrādes iestatījumus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iespējot atliktās finanšu reģistrācijas](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) manuālu izpildi.
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, veiciet šīs darbības, lai iestatītu Commerce headquarters. Plašāku informāciju skatiet [Set up the fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lejupielādēt finanšu dokumentu nodrošinātāja un finanšu savienotāja konfigurācijas failus:

    1. [Dynamics 365 Commerce Atveriet risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atlasiet pareizu laidiena filiāles versiju atbilstoši SDK/lietojumprogrammas versijai (piemēram, **[laidiens/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atvērt **src \> Fiskālā integrācija \> CleanCash**.
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failu vietnē CommerceRuntime DocumentProvider.CleanCashSample **Konfigurācijas \> dokumentsProviderFiscalCleanCashSample.xml \> (piemēram, \> laidiena fails/9.33**).[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu hardwareStation Connector.CleanCashSample **konfigurācijas \> savienotājsCleanCashSample.xml \> (piemēram, \> laidiena fails/9.33**).[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)

    > [!WARNING]
    > Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas šādās mazumtirdzniecības SDK mapēs izstrādātāja VM LCS:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**. Cilnē **Vispārīgi** iestatiet opciju **Iespējot finanšu integrāciju** uz **Jā**.
1. Dodieties uz **Mazumtirdzniecības un tirdzniecības \> kanāla iestatījumu \> Finanšu integrācija \> Finanšu dokumentu nodrošinātāji** un ielādējiet iepriekš lejupielādēto finanšu dokumentu nodrošinātāja konfigurācijas failu.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connectors un ielādējiet iepriekš lejupielādēto finanšu savienotāja konfigurācijas** failu.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector funkcionālie profili**. Izveidojiet jaunu savienotāja funkcionālo profilu. Atlasiet dokumentu nodrošinātāju un savienotāju, ko ielādējāt iepriekš. Pēc vajadzības atjauniniet [datu kartēšanas iestatījumus](#default-data-mapping).
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto finanšu savienotāju. Atjauniniet [savienotāja iestatījumi](#fiscal-connector-settings) kā prasīts.
6. Iet uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālo savienotāju grupas**. Izveidojiet jaunu fiskālo savienotāju grupu savienotāja funkcionālajam profilam, ko izveidojāt iepriekš.
7. Iet uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālās reģistrācijas procesi**. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālā reģistrācijas procesa darbību un atlasiet iepriekš izveidoto fiskālo savienotāju grupu.
8. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Izvēlieties funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā jāaktivizē reģistrācijas process. Uz **Fiskālās reģistrācijas process** FastTab atlasiet fiskālās reģistrācijas procesu, ko izveidojāt iepriekš.
9. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**. Atlasiet aparatūras profilu, kas ir saistīts ar aparatūras staciju, kurai tiks pievienots fiskālais printeris. Uz **Fiskālās perifērijas ierīces** FastTab atlasiet savienotāja tehnisko profilu, ko izveidojāt iepriekš.
10. Atveriet izplatīšanas grafiku (**Mazumtirdzniecība un tirdzniecība \> Mazumtirdzniecības un tirdzniecības IT \> Izplatīšanas grafiks**) un atlasiet darbus **1070** un **1090** lai pārsūtītu datus uz kanālu datu bāzi.

#### <a name="default-data-mapping"></a>Noklusējuma datu kartēšana

Fiskālā dokumenta nodrošinātāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga, ir iekļauta šāda noklusējuma datu kartēšana:

- **Pievienotās vērtības nodokļa (PVN) kodu kartēšana** — šis kartējums iestata ierīcei specifiskus pievienotās vērtības nodokļa (PVN) kodus atbilstošajiem PVN kodiem. PVN kodu kartēšanai jābūt šādā formātā:

    ```
    1 : code1 ; 2 : code2
    ```

    Tālāk minēts šī formāta paskaidrojums:

    - *1* un *2* ir ierīcei specifiski PVN kodi.
    - Semikols (;) tiek izmantots kā atdalītājs.
    - *kods1* un *kods2* ir PVN kodi, kas konfigurēti programmā Commerce Headquarters. Parauga kartējums ir jāmodificē atbilstoši nodokļu kodiem, kas ir konfigurēti jūsu lietojumprogrammā.

    Vadības bloki atbalsta ne vairāk kā četrus dažādus PVN kodus. Tāpēc PVN kodu kartējumu var iestatīt šādi:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Vairākus PVN kodus var kartēt uz vienu ierīcei raksturīgu PVN kodu.

#### <a name="fiscal-connector-settings"></a>Fiskālā savienotāja iestatījumi

Tālāk norādītie iestatījumi ir iekļauti fiskālā savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga.

- **Savienojumu virkne** — vadības bloka savienojuma iestatījumi.
- **Taimauts** - laiks milisekundēs, ka vadītājs gaidīs atbildi no vadības bloka.

### <a name="configure-channel-components"></a>Konfigurējiet kanāla komponentus

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Papildinformāciju skatiet [Izvēršanas vadlīnijas vadības bloku integrācijas paraugam Zviedrijai (mantots)](emea-swe-fi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

#### <a name="set-up-the-development-environment"></a>Iestatiet izstrādes vidi

Lai iestatītu izstrādes vidi, lai pārbaudītu un paplašinātu paraugu, veiciet šīs darbības.

1. Klonējiet vai lejupielādējiet [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve. Atlasiet pareizo laidiena filiāles versiju atbilstoši savai SDK/lietojumprogrammas versijai. Papildinformāciju skatiet [Lejupielādējiet mazumtirdzniecības SDK paraugus un atsauces pakotnes no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet vadības bloka integrācijas risinājumu **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln** un izveidojiet to.
1. Uzstādīt CRT paplašinājumi:

    1. Atrodi CRT paplašinājumu instalētājs:

        - **Commerce Scale Unit:** mapē **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** atrodiet installer **ScaleUnit.CleanCash.Installer**.
        - **Lokālais CRT vietnē Modern POS:** mapē **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** atrodiet **modernPOS.CleanCash.Installer** instalētāju.

    2. Sāciet CRT paplašinājuma instalētājs no komandrindas:

        - **Tirdzniecības mēroga vienība:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Vietējais CRT Mūsdienu POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Instalējiet aparatūras stacijas paplašinājumus:

    1. Mapē **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461**  atrodiet **HardwareStation.CleanCash.Installer** instalētāju.
    1. Sāciet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet norādījumus [Fiskālās integrācijas parauga izveides konveijera iestatīšana](fiscal-integration-sample-build-pipeline.md) lai ģenerētu un atbrīvotu Cloud Scale Unit un pašapkalpošanās izvietojamās pakotnes fiskālās integrācijas paraugam. **CleanCash build-pipeline.yml** veidnes YAML failu var atrast **risinājumu\\ repozitorija mapē** Pipeline [Dynamics 365 Commerce YAML_Files](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-the-extensions"></a>Paplašinājumu dizains

Vadības bloka integrācijas paraugs Zviedrijai ir balstīts uz [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **src\\ Fiskālā integrācija\\ CleanCash** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijs (piemēram, [paraugs izlaidumā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir paplašinājums CRT, un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Papildinformāciju skatiet [Izvēršanas vadlīnijas vadības bloku integrācijas paraugam Zviedrijai (mantots)](emea-swe-fi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

### <a name="crt-extension-design"></a>CRT pagarinājuma dizains

Paplašinājuma, kas ir finanšu dokumentu nodrošinātājs, mērķis ir ģenerēt pakalpojumam specifiskus dokumentus un apstrādāt vadības bloka atbildes.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

Dokumentu nodrošinātājam ir vienots **DocumentProviderCleanCash** pieprasījumu apdarinātājs. Šo apdarinātāju izmanto, lai ģenerētu vadības bloka finanšu dokumentus.

Šis apstrādātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež servisam raksturīgu dokumentu, kas jāreģistrē vadības blokā.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Šis pieprasījums atgriež abonējamo notikumu sarakstu. Pašlaik tiek atbalstīti pārdošanas notikumi un audita notikumi.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas fails atrodas **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml**[Dynamics 365 Commerce risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijā. Šī faila mērķis ir iespējot iestatījumus dokumentu nodrošinātāja konfigurēšanai no Commerce headquarters. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir finanšu savienotājs, mērķis ir sazināties ar vadības bloku. Tas izmanto HTTP protokolu, lai vadības blokam iesniegtu dokumentus, ko CRT paplašinājums ģenerē. Tā arī apstrādā atbildes, kas saņemtas no vadības bloka.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

**CleanCashHandler** pieprasījumu apdarinātājs ir ieejas punkts pieprasījumu apstrādei vadības blokā.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** — šis pieprasījums nosūta dokumentus vadības blokam un atgriež no tā atbildi.
- **IsReadyFiscalDeviceRequest** — šis pieprasījums tiek izmantots vadības bloka veselības pārbaudei.
- **InicializētfiscalDeviceRequest** — šis pieprasījums tiek izmantots, lai inicializētu vadības bloku.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja konfigurācijas fails atrodas **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** [Dynamics 365 Commerce risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijā. Faila mērķis ir iespējot finanšu savienotāja iestatījumus, kas jākonfigurē no Commerce headquarters. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
