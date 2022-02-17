---
title: Fiskālā printera integrācijas paraugs Polijai
description: Šajā tēmā ir sniegts pārskats par fiskālās integrācijas paraugu Polijai Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 43d9a54334d97a65a1f9a356daf54154f6c069b3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076840"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Fiskālā printera integrācijas paraugs Polijai

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par fiskālās integrācijas paraugu Polijai Microsoft Dynamics 365 Commerce.

The Dynamics 365 Commerce Polijas funkcionalitāte ietver tirdzniecības vietas (POS) integrācijas paraugu ar fiskālo printeri. Paraugs paplašina [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) un atbalsta POSNET THERMAL HD 2.02 protokolu fiskālajiem printeriem no [Posnet Polska SA](https://www.posnet.com.pl) Paraugs nodrošina saziņu ar fiskālo printeri, kas ir pievienots, izmantojot COM portu, izmantojot vietējo programmatūras draiveri. Tas tika ieviests un pārbaudīts, izmantojot programmatūras emulatoru, ko Posnet nodrošināja Posnet Thermal HD FV EJ fiskālajam printerim. Paraugs tiek nodrošināts avota koda veidā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Microsoft neizlaiž no Posnet aparatūru, programmatūru vai dokumentāciju. Lai iegūtu informāciju par fiskālā printera iegūšanu un lietošanu, sazinieties ar [Posnet Polska SA](https://www.posnet.com.pl)

## <a name="scenarios"></a>Scenāriji

Polijas fiskālā printera integrācijas paraugā ir ietverti šādi scenāriji.

- Pārdošanas scenāriji:

    - Izdrukājiet fiskālo kvīti par skaidras naudas pārdošanu un atgriešanu.
    - Uztveriet atbildi no fiskālā printera un saglabājiet to kanālu datu bāzē.
    - Nodokļi:

        - Karte ar fiskālā printera nodokļu kodiem (nodaļām).
        - Pārsūtiet kartētos nodokļu datus uz fiskālo printeri.

    - Maksājumi:

        - Karte ar fiskālā printera maksāšanas metodēm.
        - Izdrukājiet maksājumus fiskālā kvītī.
        - Drukāt informāciju par izmaiņām.

    - Drukas līniju atlaides.
    - Dāvanu kartes:

        - Izslēdziet izsniegtu/atkārtoti iekasētu dāvanu karšu līniju no pārdošanas fiskālā kvīts.
        - Izdrukājiet maksājumu, kurā kā parastais maksāšanas veids tiek izmantota dāvanu karte.

    - Drukājiet fiskālos čekus klientu pasūtījuma operācijām:

        - Par klienta pasūtījuma depozītu netiek drukāta fiskālā kvīts.
        - Drukājiet fiskālo kvīti par klientu hibrīda pasūtījuma izpildes rindām.
        - Izdrukājiet fiskālo kvīti klienta pasūtījuma saņemšanas operācijai.
        - Izdrukājiet atgriešanas pasūtījuma fiskālo kvīti.

    - Izdrukājiet [Klienta informācija](emea-pol-customer-information.md) kas norādīts pārdošanas darījumam fiskālā kvītī. Šīs informācijas piemērs ir klienta PVN maksātāja numurs.

- Dienas beigu pārskati (fiskālie X un fiskālie Z pārskati).
- Kļūdu apstrāde, piemēram, šādas opcijas:

    - Atkārtoti mēģiniet veikt fiskālo reģistrāciju, ja ir iespējams atkārtots mēģinājums, piemēram, ja fiskālais printeris nav pievienots, nav gatavs vai nereaģē, printerī ir beidzies papīrs vai ir iestrēdzis papīrs.
    - Atlikt fiskālo reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darījumu kā reģistrētu un iekļaujiet informācijas kodus, lai fiksētu kļūmes iemeslu un papildu informāciju.
    - Pirms jauna pārdošanas darījuma atvēršanas vai pārdošanas darījuma pabeigšanas pārbaudiet fiskālā printera pieejamību.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālā printera integrācijas paraugā ir ieviesti šādi noteikumi, kas saistīti ar dāvanu kartēm:

- Izslēdziet pārdošanas rindas, kas ir saistītas ar *Izsniegt dāvanu karti* un *Pievienot dāvanu kartei* operācijas no fiskālā kvīts.
- Nedrukājiet fiskālo čeku, ja tajā ir tikai dāvanu kartes rindas.
- Atņemiet kopējo dāvanu karšu summu, kas izsniegtas vai atkārtoti iekasētas darījumā no fiskālā čeka maksājumu rindām.
- Saglabājiet aprēķinātās maksājumu rindu korekcijas kanālu datu bāzē ar atsauci uz atbilstošu fiskālo darījumu.
- Apmaksa ar dāvanu karti tiek uzskatīta par regulāru maksājumu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Klientu noguldījumi un klientu pasūtījumu noguldījumi

Fiskālā printera integrācijas paraugā ir ieviesti šādi noteikumi, kas ir saistīti ar klientu noguldījumiem un klientu pasūtījumu noguldījumiem:

- Nedrukājiet fiskālo kvīti, ja darījums ir klienta depozīts.
- Nedrukājiet fiskālo kvīti, ja darījums ietver tikai klienta pasūtījuma depozītu vai klienta pasūtījuma depozīta atmaksu.
- Drukājiet iepriekš iemaksātās depozīta summu fiskālā kvītī par klienta pasūtījuma saņemšanas operāciju.
- Kad tiek izveidots hibrīda klienta pasūtījums, atņemiet klienta pasūtījuma depozīta summu no maksājumu rindām.
- Saglabājiet aprēķinātās maksājumu rindu korekcijas kanālu datu bāzē ar atsauci uz fiskālo darījumu klienta hibrīda pasūtījumam.

### <a name="limitations-of-the-sample"></a>Izlases ierobežojumi

- Fiskālais printeris atbalsta tikai scenārijus, kuru cenā ir iekļauts tirdzniecības nodoklis. Tāpēc, **Cenā iekļauts pārdošanas nodoklis** opcija ir jāiestata uz **Jā** gan veikaliem, gan klientiem.
- Ikdienas atskaites (fiskālais X un fiskālais Z) tiek drukātas, izmantojot iegulto *Pārskats par maiņu* formātā.
- Svītrkoda drukāšana uz fiskālajām čekiem tiek uzskatīta par iespējamu pielāgošanu, jo šī funkcija netiek atbalstīta iegultajos formātos un to var ieviest, tikai izmantojot pielāgojamo **Superformāts** Ziņot.
- Fiskālais printeris neatbalsta jauktus darījumus. The **Aizliegt vienā kvītī sajaukt pārdošanu un atgriešanu** opcija ir jāiestata uz **Jā** POS funkcionalitātes profilos.

## <a name="set-up-fiscal-integration-for-poland"></a>Izveidot fiskālo integrāciju Polijai

Polijas fiskālā printera integrācijas paraugs ir balstīts uz [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **src\\ Fiskālā integrācija\\ Posnet** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijs (piemēram, [paraugs izlaidumā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir Commerce izpildlaika paplašinājums (CRT), un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Izstrādātāja virtuālajā mašīnā (VM) ir jāizmanto iepriekšējā mazumtirdzniecības SDK versija Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Papildinformāciju skatiet [Polijas fiskālā printera integrācijas izlases izvietošanas vadlīnijas (mantojums)](emea-pol-fpi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

Pabeidziet finanšu integrācijas iestatīšanas soļus, kā aprakstīts sadaļā [Iestatīt finanšu integrāciju commerce kanāliem](setting-up-fiscal-integration-for-retail-channel.md).

1. [Iestatiet finanšu reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ņemiet vērā arī fiskālās reģistrācijas procesa iestatījumus, kas ir [raksturīgi šim finanšu printera integrācijas paraugam](#set-up-the-registration-process).
1. [Iestatiet kļūdu apstrādes iestatījumus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iestatiet finanšu X/Z pārskatus no POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Iespējot atliktās finanšu reģistrācijas](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) manuālu izpildi.
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, veiciet šīs darbības, lai iestatītu Commerce headquarters. Plašāku informāciju skatiet [Set up the fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lejupielādēt finanšu dokumentu nodrošinātāja un finanšu savienotāja konfigurācijas failus:

    1. [Dynamics 365 Commerce Atveriet risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atlasiet pareizu laidiena filiāles versiju atbilstoši SDK/lietojumprogrammas versijai (piemēram, **[laidiens/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atveriet **src \> FiscalIntegration \> Posnet**.
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failu vietnē CommerceRuntime DocumentProvider.PosnetSample Configuration DocumentProviderPosnetSample.xml **(piemēram, \> laidiena fails/9.33 \>).\>**[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu hardwareStation **\> ThermalDeviceSample \> Configuration \> ConnectorPosnetThermalFVEJ.xml** (piemēram, [laidiena fails/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)).

    > [!WARNING]
    > Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas šādās mazumtirdzniecības SDK mapēs izstrādātāja VM LCS:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml
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

- **Pievienotās vērtības nodokļa (PVN) likmju kartēšana** – Tirdzniecības nodokļa kodiem iestatīto nodokļu procentu vērtību kartēšana ar fiskālajam printerim specifiskām PVN likmēm. Šeit ir noklusējuma kartēšana:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Pirmais komponents katrā pārī apzīmē PVN likmes numuru, kas ir konfigurēts fiskālā printerī. Otrā sastāvdaļa atspoguļo atbilstošo PVN likmi. Papildinformāciju par fiskālā printera PVN likmes konfigurāciju skatiet POSNET draivera dokumentācijā.

- **Konkursa veidu kartēšana** – Veikalam konfigurēto maksājumu metožu kartēšana ar maksājumu veidlapām, kuras atbalsta fiskālais printeris. Šeit ir noklusējuma kartēšana:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Pirmais komponents katrā pārī apzīmē veikalam iestatīto maksājuma veidu. Otrais komponents apzīmē atbilstošo maksājuma veidu, ko atbalsta fiskālais printeris. Papildinformāciju par maksājumu veidlapām, ko atbalsta fiskālais printeris, skatiet POSNET draivera dokumentācijā. Jums ir jāmaina kartējuma paraugs atbilstoši jūsu lietojumprogrammā konfigurētajām maksājumu metodēm.

#### <a name="fiscal-connector-settings"></a>Fiskālā savienotāja iestatījumi

Tālāk norādītie iestatījumi ir iekļauti fiskālā savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga.

- **Savienojuma virkne** – Virkne, kas apraksta detalizētu informāciju par savienojumu ar ierīci formātā, ko atbalsta draiveris. Papildinformāciju skatiet POSNET draivera dokumentācijā.
- **Datuma un laika sinhronizācija** – Vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē ar pievienoto aparatūras staciju.
- **Ierīces taimauts** – Laiks milisekundēs, cik ilgi draiveris gaidīs atbildi no ierīces. Papildinformāciju skatiet POSNET draivera dokumentācijā.

### <a name="configure-channel-components"></a>Konfigurējiet kanāla komponentus

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Papildinformāciju skatiet [Polijas fiskālā printera integrācijas izlases izvietošanas vadlīnijas (mantojums)](emea-pol-fpi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

#### <a name="set-up-the-development-environment"></a>Iestatiet izstrādes vidi

Lai iestatītu izstrādes vidi, lai pārbaudītu un paplašinātu paraugu, veiciet šīs darbības.

1. Klonējiet vai lejupielādējiet [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve. Atlasiet pareizo laidiena filiāles versiju atbilstoši savai SDK/lietojumprogrammas versijai. Papildinformāciju skatiet [Lejupielādējiet mazumtirdzniecības SDK paraugus un atsauces pakotnes no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet fiskālā printera integrācijas risinājumu vietnē **Dynamics365Commerce.Solutions\\ Fiskālā integrācija\\ Posnet\\ Posnet.sln**, un izveidojiet to.
1. Uzstādīt CRT paplašinājumi:

    1. Atrodi CRT paplašinājumu instalētājs:

        - **Tirdzniecības mēroga vienība:** Iekš **Posnet\\ Mērvienība\\ ScaleUnit.Posnet.Installer\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **ScaleUnit.Posnet.Installer** uzstādītājs.
        - **Vietējais CRT Mūsdienu POS:** Iekš **Posnet\\ Modern POS\\ ModernPOS.Posnet.Instalētājs\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **ModernPOS.Posnet.Instalētājs** uzstādītājs.

    1. Sāciet CRT paplašinājuma instalētājs no komandrindas:

        - **Tirdzniecības mēroga vienība:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Vietējais CRT Mūsdienu POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Instalējiet aparatūras stacijas paplašinājumus:

    1. Iekš **Posnet\\ HardwareStation\\ HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **HardwareStation.PosnetThermalFVFiscalPrinter.Installer** uzstādītājs.
    1. Sāciet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet norādījumus [Fiskālās integrācijas parauga izveides konveijera iestatīšana](fiscal-integration-sample-build-pipeline.md) lai ģenerētu un atbrīvotu Cloud Scale Unit un pašapkalpošanās izvietojamās pakotnes fiskālās integrācijas paraugam. The **Posnet build-pipeline.yml** veidnes YAML failu var atrast **Cauruļvads\\ YAML_Files** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve.

## <a name="design-of-extensions"></a>Paplašinājumu projektēšana

Polijas fiskālā printera integrācijas paraugs ir balstīts uz [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **src\\ Fiskālā integrācija\\ Posnet** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijs (piemēram, [paraugs izlaidumā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir paplašinājums CRT, un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Papildinformāciju skatiet [Polijas fiskālā printera integrācijas izlases izvietošanas vadlīnijas (mantojums)](emea-pol-fpi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

### <a name="commerce-runtime-extension-design"></a>Tirdzniecības izpildlaika paplašinājuma dizains

Paplašinājuma, kas ir fiskālo dokumentu nodrošinātājs, mērķis ir ģenerēt printerim specifiskus dokumentus un apstrādāt atbildes no fiskālā printera. Šis paplašinājums ģenerē printerim raksturīgu komandu kopu JavaScript Object Notation (JSON) formātā, kas noteiktas POSNET specifikācijā 19-3678.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **DocumentProviderPosnetProtocol** pieprasījumu apstrādātājs ir ieejas punkts pieprasījumam ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Šis pieprasījums atgriež abonējamo notikumu sarakstu. Pašlaik tiek atbalstīti šādi pasākumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Fiskālā dokumenta nodrošinātāja konfigurācijas fails atrodas vietnē **src\\ Fiskālā integrācija\\ Posnet\\ CommerceRuntime\\ DocumentProvider.PosnetSample\\ Konfigurācija\\ DocumentProviderPosnetSample.xml** iekš [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) krātuve. Faila mērķis ir iespējot fiskālo dokumentu nodrošinātāja iestatījumu konfigurēšanu no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar fiskālo printeri. Šis paplašinājums izsauc POSNET draivera funkcijas, lai iesniegtu komandas, kuras CRT paplašinājums tiek ģenerēts fiskālajam printerim. Tas arī apstrādā ierīces kļūdas.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **FiscalPrinterHandler** pieprasījumu apstrādātājs ir ieejas punkts, lai apstrādātu pieprasījumu uz fiskālo perifērijas ierīci.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – Šis pieprasījums nosūta dokumentus uz printeriem un atgriež atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – Šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – Šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Fiskālā savienotāja konfigurācijas fails atrodas vietnē **src\\ Fiskālā integrācija\\ Posnet\\ HardwareStation\\ ThermalDeviceSample\\ Konfigurācija\\ ConnectorPosnetThermalFVEJ.xml** iekš [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) krātuve. Faila mērķis ir iespējot fiskālā savienotāja iestatījumu konfigurēšanu no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
