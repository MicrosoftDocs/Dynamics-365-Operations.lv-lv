---
title: Fiskālā printera integrācijas paraugs Polijai
description: Šajā rakstā sniegts pārskats par finanšu integrācijas paraugu Polijai Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: e71d7b342789e4cf2e7644a46bc847087063fc78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876953"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Fiskālā printera integrācijas paraugs Polijai

[!include[banner](../includes/banner.md)]

Šajā rakstā sniegts pārskats par finanšu integrācijas paraugu Polijai Microsoft Dynamics 365 Commerce.

Polijas Dynamics 365 Commerce funkcionalitāte ietver pārdošanas punkta (POS) parauga integrāciju ar fiskālo printeri. Paraugs paplašina fiskālās [integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un atbalsta POSNET HD 2.02 protokolu fiskālajiem printeriem [no Posnet Polska S.A.](https://www.posnet.com.pl) Paraugs iespējo sakarus ar fiskālo printeri, kas ir savienots, izmantojot COM portu, izmantojot vietējais programmatūras draiveri. Tas tika ieviests un testēts, izmantojot programmatūras konsolidāciju, ko Posnet nodrošina Posnet Hd HD FV EJ finanšu printerim. Paraugs ir nodrošināts avota koda formā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Korporācija Microsoft neatlaiž nevienu aparatūru, programmatūru vai dokumentāciju no Posnet. Lai iegūtu informāciju par to, kā iegūt fiskālo printeri un to izmantot, sazinieties [ar Posnet Polska S.A.](https://www.posnet.com.pl)

## <a name="scenarios"></a>Scenāriji

Šos scenārijus sedz Fiskālā printera integrācijas paraugs Polijai:

- Pārdošanas scenāriji:

    - Drukājiet finanšu dokumentu par pārdošanu un atgriešanu, kas ir jāveic skaidrā naudā.
    - Notvert atbildi no fiskālā printera un saglabāt to kanāla datu bāzē.
    - Nodokļi:

        - Kartēt uz fiskālā printera nodokļu kodiem (nodaļas).
        - Pārsūtīt kartētos nodokļu datus uz fiskālo printeri.

    - Maksājumus:

        - Kartēt uz fiskālā printera maksāšanas metodēm.
        - Drukāt maksājumus finanšu dokumentu
        - Drukājiet izmaiņu informāciju.

    - Drukāt rindu atlaides.
    - Dāvanu kartes:

        - No finanšu dokumenta par pārdošanu izslēdziet izsniegtās/atkārtoti iekasētās dāvanu kartes rindu.
        - Izdrukājiet maksājumu, kas izmanto dāvanu karti kā regulāru maksājuma metodi.

    - Drukāt finanšu ieejas plūsmas debitoru pasūtījumu operācijām:

        - Debitora pasūtījuma depozīta finanšu dokuments nav izdrukāts.
        - Drukājiet finanšu dokumentu šāda debitora pasūtījuma pārnešanas rindām.
        - Drukājiet finanšu dokumentu debitora pasūtījuma saņemšanas darbībai.
        - Drukājiet finanšu dokumentu atgriešanas pasūtījumam.

    - Izdrukājiet [debitora](emea-pol-customer-information.md) informāciju, kas finanšu dokumenta pārdošanas darbībai ir norādīta. Šīs informācijas piemērs ir debitora PVN numurs.

- Darba dienas beigu pārskati (finanšu X un finanšu Z pārskati).
- Kļūdu apstrāde, piemēram, šādas opcijas:

    - Mēģiniet vēlreiz veikt finanšu reģistrāciju, ja iespējams atkārtot, piemēram, ja fiskālais printeris nav savienots, nav gatavs vai nav atbildes, printeris ir ārpus papīra vai ir iesprūdis papīrs.
    - Atlikt finanšu reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darbību kā reģistrētu un ietveriet infokodus, lai iegūtu kļūmes iemeslu un papildinformāciju.
    - Pirms jaunas pārdošanas darbības atvēršanas vai pārdošanas darbības veikšanas pārbaudiet fiskālā printera pieejamību.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālā printera integrācijas paraugs ievieš tālāk norādītos ar dāvanu kartēm saistītos noteikumus.

- No finanšu dokumenta izslēdziet pārdošanas rindas *, kas ir saistītas ar* dāvanu *kartes izdošanu un* pievienot dāvanu karšu operācijām.
- Nedrukāt finanšu dokumentu, ja tas sastāv tikai no dāvanu kartes rindām.
- No finanšu dokumenta maksājumu rindām atņemiet no naudas plūsmas kopsummas, kas ir izsniegtas vai atkārtoti iekasētas.
- Saglabāt aprēķinātos maksājumu rindu pielāgojumus kanāla datu bāzē ar atsauci uz atbilstošu finanšu darbību.
- Maksājums ar dāvanu karti tiek uzskatīts par regulāru maksājumu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Debitora depozīti un debitora pasūtījuma depozīti

Fiskālā printera integrēšanas paraugs ievieš tālāk norādītos noteikumus, kas ir saistīti ar debitora depozītiem un debitora pasūtījuma depozītiem:

- Nedrukāt finanšu dokumentu, ja darbība ir debitora depozīts.
- Nedrukāt finanšu dokumentu, ja darījums ietver tikai debitora pasūtījuma depozītu vai debitora pasūtījuma depozīta atmaksu.
- Drukājiet debitora pasūtījuma saņemšanas operācijas iepriekš apmaksātā deponēījuma summu finanšu kvītī.
- Ieturēt debitora pasūtījuma depozīta summu no maksājuma rindām, kad ir izveidots debitora pasūtījums.
- Saglabāt aprēķinātos maksājumu rindu pielāgojumus kanāla datu bāzē, lai izveidotu atsauci uz debitora pasūtījuma finanšu darbību.

### <a name="limitations-of-the-sample"></a>Parauga ierobežojumi

- Fiskālais printeris atbalsta tikai scenārijus, kuros PVN ir iekļauts cenā. Tāpēc gan veikaliem **, gan debitoriem** opcijai Cena **iekļaut** PVN ir jābūt iestatītai uz Jā.
- Ikdienas pārskati (finanšu X un finanšu Z) tiek drukāti, izmantojot iegulto Maiņas *pārskata* formātu.
- Svītrkoda drukāšana finanšu ieejas plūsmās tiek uzskatīta par potenciālo pielāgošanu, jo šī funkcija netiek atbalstīta iegultos formātos, un to var ieviest tikai, izmantojot pielāgojamu **superformāta** pārskatu.
- Fiskālais printeris neatbalsta jauktas darbības. POS **funkcionalitātes profilos opcijas Aizliegt jaukšanu un** atgriešanu vienā kvītī **iestatījumam** ir jābūt Jā.

## <a name="set-up-fiscal-integration-for-poland"></a>Iestatīt Polijai fiskālo integrāciju

Fiskālā printera integrācijas paraugs Polijai ir balstīts uz finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no Retail SDK. Paraugs atrodas src **FiscalIntegration\\ Posnet \\** mapē Solutions [Dynamics 365 Commerce repository (piemēram,](https://github.com/microsoft/Dynamics365Commerce.Solutions/) paraugs release/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet) Paraugs sastāv [no](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālā dokumenta nodrošinātāja, kas ir Commerce Runtime () paplašinājums (CRT) un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot retail SDK, skatiet mazumtirdzniecības [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[arhitektūrā un būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un [paplašinājuma modeļa ierobežojumu dēļ](../dev-itpro/build-pipeline.md) to pašlaik nevar izmantot šim fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātāja virtuālajā datorā (VM) pakalpojumos Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet Polijas [finanšu printera integrācijas parauga izvietošanas vadlīnijās (mantojuma)](emea-pol-fpi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

Veiciet fiskālās integrācijas iestatīšanas soļus, kā [aprakstīts Commerce kanālu finanšu integrācijas iestatīšanai](setting-up-fiscal-integration-for-retail-channel.md).

1. [Iestatīt fiskālās reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Atzīmējiet arī fiskālās reģistrācijas procesa iestatījumus, kas ir raksturīgi šim [fiskālā printera integrācijas paraugam](#set-up-the-registration-process).
1. [Iestatīt kļūdu apstrādes iestatījumus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iestatiet POS finanšu X/Z pārskatus](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Iespējojiet atliktās finanšu reģistrācijas manuālu izpildi](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, izpildiet šīs darbības, lai iestatītu programmu Commerce Headquarters. Papildinformāciju skatiet [šeit: Komercijas kanālu finanšu integrācijas iestatīšana](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lejupielādēt konfigurācijas failus finanšu dokumentu nodrošinātājam un finanšu savienotājam:

    1. Atveriet risinājumu repozitoriju [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Atlasiet pareizu versijas izlaidi atbilstoši SDK/programmas versijai (piemēram, izlaidums **[/9,33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atveriet **src \> FiscalIntegration \> Posnet**.
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja **konfigurācijas failu commerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml (piemēram**, [fails laidienam/9,33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)).
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu Aparatūras **stacijāKingDeviceSample \> konfigurācijas \> SavienotājaPosnetThermalFVEJ.xml \> (piemēram,** fails laidienam/9,33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)

    > [!WARNING]
    > Jaunā neatkarīgā iepakojuma un [paplašinājuma modeļa ierobežojumu dēļ](../dev-itpro/build-pipeline.md) to pašlaik nevar izmantot šim fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas tālākmintās Retail SDK mapēs LCS izstrādātāja VM:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extension.DocumentProvider.PosnetSample konfigurācijas\\\\ DocumentProviderPosnetSample.xml
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk\\ SampleExtensions\\ HardwareStation\\ Extension.Posnet.PstDeviceSample\\ Configuration\\ ConnectorPosnetThermalFVEJ.xml
    > 
    > Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**. Cilnē Vispārīgi **iestatiet** opciju Aktivizēt **fiskālo integrāciju kā** **Jā**.
1. Dodieties uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas \> finanšu dokumentu nodrošinātājiem** un ielādējiet iepriekš lejupielādēto fiskālā dokumenta nodrošinātāja konfigurācijas failu.
1. Dodieties uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas \> finanšu savienotājiem** un ielādējiet agrāk lejupielādēto fiskālā savienotāja konfigurācijas failu.
1. Pārejiet uz **Sadaļu Mazumtirdzniecības un Commerce \> Channel Setup \> Finanšu integrācijas savienotāja \> funkcionālie profili**. Izveidojiet jaunu savienotāja funkcionalitātes profilu. Atlasiet dokumentu nodrošinātāju un iepriekš ielādēto savienotāju. Pēc vajadzības [atjauniniet datu kartēšanas](#default-data-mapping) iestatījumus.
1. Pārejiet uz **Retail un Commerce Channel \> setup \> Fiscal integration \> Connector tehniskajiem profiliem**. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto finanšu savienotāju. Pēc vajadzības [atjauniniet savienotāja](#fiscal-connector-settings) iestatījumus.
6. Pārejiet uz **sadaļu Mazumtirdzniecības un \> Commerce kanālu iestatīšanas \> finanšu integrācijas \> fiskālā savienotāja grupas**. Izveidojiet jaunu finanšu savienotāja grupu iepriekš izveidotajā savienotāja funkcionālajā profilā.
7. Pārejiet uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas finanšu \> reģistrācijas procesiem**. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālās reģistrācijas procesa soli un atlasiet iepriekš izveidoto finanšu savienotāja grupu.
8. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Atlasiet funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā ir jāaktivizē reģistrācijas process. Kopsavilkuma cilnē **Finanšu reģistrācijas process** atlasiet iepriekš izveidoto finanšu reģistrācijas procesu.
9. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**. Atlasiet aparatūras profilu, kas ir saistīts ar aparatūras staciju, ar kuru tiks pievienots fiskālais printeris. Kopsavilkuma cilnē **Finanšu perifērijas** ierīces atlasiet iepriekš izveidoto savienotāja tehnisko profilu.
10. Atveriet sadales grafiku (**Mazumtirdzniecības un Commerce \> Retail un Commerce IT \> sadales** grafiks) **un atlasiet darbus 1070** **un 1090**, lai pārsūtītu datus uz kanāla datu bāzi.

#### <a name="default-data-mapping"></a>Noklusējuma datu kartēšana

Tālāk redzamais noklusējuma datu kartējums ir ietverts finanšu dokumenta nodrošinātāja konfigurācijā, kas ir nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Pievienotās vērtības nodokļa (PVN)** likmju kartēšana – nodokļu procentu vērtību kartēšana, kas iestatītas PVN kodiem fiskālam printerim - specifiskām PVN likmēm. Šeit ir noklusējuma kartēšana:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Pirmais komponents katrā pārī norāda PVN likmes numuru, kas ir konfigurēts fiskālajā printerī. Otra sastāvdaļa norāda atbilstošo PVN likmi. Papildinformāciju par fiskālā printera PVN likmes konfigurāciju skatiet POSNET draivera dokumentācijā.

- **Norēķinu veidu kartēšana** — to maksāšanas metožu kartēšana, kas ir konfigurētas veikalam, ar maksājumu formām, kuras atbalsta fiskālais printeris. Šeit ir noklusējuma kartēšana:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Pirmais komponents katrā pārī attiecas uz veikalam iestatīto maksāšanas metodi. Otrais komponents norāda atbilstošo maksājuma formu, ko atbalsta fiskālais printeris. Papildinformāciju par maksājumu formām, ko atbalsta fiskālais printeris, skatiet POSNET draivera dokumentācijā. Parauga kartējums ir jāmodificē atbilstoši maksājumu metodēm, kas ir konfigurētas programmā.

#### <a name="fiscal-connector-settings"></a>Finanšu savienotāja iestatījumi

Šādi iestatījumi ir iekļauti finanšu savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Savienojuma virkne** – virkne, kas apraksta detalizētu informāciju par savienojumu ar ierīci draivera atbalstītajā formātā. Papildinformāciju skatiet POSNET draivera dokumentācijā.
- **Datuma un laika sinhronizācija** – vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē ar pievienoto aparatūras staciju.
- **Ierīces taimauts** – laiks milisekundēs, ko autovadītājs gaidīs no ierīces atbildes. Papildinformāciju skatiet POSNET draivera dokumentācijā.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un [paplašinājuma modeļa ierobežojumu dēļ](../dev-itpro/build-pipeline.md) to pašlaik nevar izmantot šim fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Polijas [finanšu printera integrācijas parauga izvietošanas vadlīnijās (mantojuma)](emea-pol-fpi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

#### <a name="set-up-the-development-environment"></a>Iestatīt izstrādes vidi

Lai iestatītu izstrādes vidi un paplašinātu paraugu ņemšanas, veiciet šādus soļus.

1. Lejupielādējiet Solutions repozitoriju vai [Dynamics 365 Commerce lejupielādējiet](https://github.com/microsoft/Dynamics365Commerce.Solutions) to. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai. Papildinformāciju skatiet lejupielādes [Retail SDK paraugos un atsauces pakotnēs no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet fiskālā printera integrācijas risinājumu **dynamics365Commerce.Solutions\\ FiscalIntegration\\ Posnet Posnet.sln\\** un izveidojiet to.
1. Instalēt CRT paplašinājumus:

    1. Atrast paplašinājuma CRT instalētāju:

        - **Commerce Scale Unit:** Posnet **ScaleUnit ScaleUnit.Posnet.Installer\\\\ bin\\ atkļūdošanas\\ net461\\** mapē atrodiet scaleUnit.Posnet.Installer instalētāju **.**
        - **CRT Modern POS lokāls:** **Posnet\\ ModernPOS ModernPOS.Posnet.Installer\\\\ bin\\ atkļūdošanas\\ net461** **mapē atrodiet ModernPOS.Posnet.Installer instalētāju.**

    1. Startējiet CRT paplašinājuma instalētāju no komandrindas:

        - **Commerce Scale vienība:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Lokāls CRT modernajā POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Instalēt aparatūras stacijas paplašinājumus:

    1. Mapē Posnet HardwareStation **HardwareStation.PosnetThermalFVFiscalPrinter.Installer bin\\ Atkļūdot\\ net461\\ atrodiet \\ mapi HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\** instalētājs.**·**
    1. Startējiet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet [darbības](fiscal-integration-sample-build-pipeline.md), kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos iepakojumus fiskālās integrācijas parauga iepakojumam. Posnet būvējuma-pipeline.yml **veidnes TOL** **fails var tikt atrasts Risinājumu repozitorija \\** YAML_Files konveijera [Dynamics 365 Commerce sarakstā.](https://github.com/microsoft/Dynamics365Commerce.Solutions)

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Fiskālā printera integrācijas paraugs Polijai ir balstīts uz finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no Retail SDK. Paraugs atrodas src **FiscalIntegration\\ Posnet \\** mapē Solutions [Dynamics 365 Commerce repository (piemēram,](https://github.com/microsoft/Dynamics365Commerce.Solutions/) paraugs release/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet) Paraugs sastāv [no](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālā dokumenta nodrošinātāja, CRT kas ir Commerce Hardware Station paplašinājums un fiskālais savienotājs. Papildinformāciju par to, kā izmantot retail SDK, skatiet mazumtirdzniecības [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[arhitektūrā un būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un [paplašinājuma modeļa ierobežojumu dēļ](../dev-itpro/build-pipeline.md) to pašlaik nevar izmantot šim fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Polijas [finanšu printera integrācijas parauga izvietošanas vadlīnijās (mantojuma)](emea-pol-fpi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Nolūks paplašinājumam, kas ir fiskālā dokumenta nodrošinātājs, ir izveidot printerim raksturīgus dokumentus un apstrādāt atbildes no fiskālā printera. Šis paplašinājums izveido specifisku printera komandu kopu JavaScript objekta notācijas (JSON) formātā, kas definētas ar POSNET specifikāciju 19-3678.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

DocumentProviderPosnetProtocol **pieprasījuma** apdarinātājs ir ieejas punkts pieprasījumam ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest —** šajā pieprasījumā ir ietverta informācija par to, kurš dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālajā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest** - šis pieprasījums atgriež notikumu sarakstu, uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu **nodrošinātāja konfigurācijas fails atrodas src\\ FiscalIntegration\\ Posnet\\ CommerceRuntime\\ DocumentProvider.PosnetSample konfigurācijas\\\\ DocumentProviderPosnetSample.xml**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) risinājumu repozitorijā. Faila mērķis ir iespējot finanšu dokumentu nodrošinātāja iestatījumus, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, nolūks ir sazināties ar fiskālo printeri. Šis paplašinājums izsauc POSNET draivera funkcijas, lai iesniegtu komandas, kuras paplašinājums CRT ģenerē fiskālam printerim. Tiek apstrādāts arī ierīces kļūdas.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

FiscalPrinterHandler **pieprasījumu apdarinātājs** ir ieejas punkts pieprasījuma apstrādei finanšu perifērijas ierīcē.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – šis pieprasījums sūta dokumentus printeriem un atgriež atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja **konfigurācijas fails atrodas src\\ FiscalIntegration\\ Posnet\\ HardwareStationFiskDeviceSample\\\\ Configuration\\ ConnectorPosnetThermalFVEJ.xml**[Dynamics 365 Commerce risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijā. Faila mērķis ir iespējot finanšu savienotāja iestatījumus, kas jākonfigurē no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
