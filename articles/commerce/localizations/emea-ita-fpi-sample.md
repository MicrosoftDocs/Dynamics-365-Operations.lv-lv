---
title: Fiskālā printera integrācijas piemērs Itālijai
description: Šajā tēmā sniegts pārskats par Itālijas finanšu integrācijas paraugu Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 592cecff5b6179e7afd1bacb25beda277dfb8fa3
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944638"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Fiskālā printera integrācijas piemērs Itālijai

[!include[banner](../includes/banner.md)]

Šajā tēmā sniegts pārskats par Itālijas finanšu integrācijas paraugu Microsoft Dynamics 365 Commerce.

Itālijas Commerce funkcionalitāte ietver pārdošanas punkta (POS) parauga integrāciju ar fiskālo printeri. Paraugs paplašina fiskālās integrācijas funkcionalitāti tā, lai tas darbojas ar [Epson](fiscal-integration-for-retail-channel.md) FP-90III sērijas printeriem no Epson, un tas ļauj sazināties ar fiskālo printeri tīmekļa servera režīmā, [izmantojot Web pakalpojumu](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) EpsonFPMate, izmantojot finanšu ePOS-Print API. Paraugs atbalsta tikai režīmu Registratore Telematico (RT). Paraugs ir nodrošināts avota koda formā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Korporācija Microsoft neatlaiž nevienu aparatūru, programmatūru vai dokumentāciju no Epson. Lai iegūtu informāciju par to, kā iegūt fiskālo printeri un darbināt to, sazinieties ar [Epson Epson S.p.A](https://www.epson.it).

## <a name="scenarios"></a>Scenāriji

Šos scenārijus iekļauj Itālijas fiskālā printera integrācijas paraugs:

- Pārdošanas scenāriji:

    - Drukājiet finanšu dokumentu par pārdošanu un atgriešanu, kas ir jāveic skaidrā naudā.
    - Notvert atbildi no fiskālā printera un saglabāt to kanāla datu bāzē.
    - Nodokļi:

        - Kartēt uz fiskālā printera nodokļu kodiem (nodaļas).
        - Pārsūtīt kartētos nodokļu datus uz fiskālo printeri.
        - Drukāt nodokļus finanšu kvītī.

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
        - Drukājiet finanšu dokumentu e-debitora pasūtījuma pārnešanas rindām.
        - Drukājiet finanšu dokumentu debitora pasūtījuma saņemšanas darbībai.
        - Drukājiet finanšu dokumentu atgriešanas pasūtījumam.

    - Drukājiet dokumenta numura svītrkodu finanšu dokumenta kvītī.
    - Izdrukājiet [debitora](emea-ita-customer-information.md) informāciju, kas finanšu dokumenta pārdošanas darbībai ir norādīta. Šīs informācijas piemērs ir debitora loteriju kods. 

- Darba dienas beigu pārskati (finanšu X un finanšu Z pārskati).
- Kļūdu apstrāde, piemēram, šādas opcijas:

    - Mēģiniet vēlreiz veikt finanšu reģistrāciju, ja iespējams atkārtot, piemēram, ja fiskālais printeris nav savienots, nav gatavs vai nav atbildes, printeris ir ārpus papīra vai ir iesprūdis papīrs.
    - Atlikt finanšu reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darbību kā reģistrētu un ietveriet infokodus, lai iegūtu kļūmes iemeslu un papildinformāciju.
    - Pirms jaunas pārdošanas darbības atvēršanas vai pārdošanas darbības veikšanas pārbaudiet fiskālā printera pieejamību.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālā printera integrācijas paraugs ievieš tālāk norādītos ar dāvanu kartēm saistītos noteikumus.

- No finanšu dokumenta izslēdziet pārdošanas rindas, kas ir saistītas ar dāvanu kartes izdošanu *un pievienot dāvanu karšu* *operācijām*.
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

- Fiskālais printeris atbalsta tikai scenārijus, kuros PVN ir iekļauts cenā. Tāpēc gan **veikaliem, gan debitoriem opcijai Cena iekļaut PVN** ir jābūt **iestatītai** uz Jā.
- Ikdienas pārskati (finanšu X un finanšu Z) tiek drukāti, izmantojot formātu, kas ir iegults fiskālā printera formā.
- Fiskālais printeris neatbalsta jauktas darbības. POS **funkcionalitātes profilos opcijas Aizliegt jaukšanu un** atgriešanu vienā kvītī **iestatījumam** ir jābūt Jā.
- Paraugs atbalsta integrāciju tikai ar fiskālo printeri, kas darbojas režīmā Registratore Telematico (RT).

## <a name="set-up-fiscal-integration-for-italy"></a>Iestatīt Itālijas fiskālo integrāciju

Itālijas fiskālā printera integrācijas paraugs ir balstīts uz [fiskālās integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no retail SDK. Paraugs atrodas **src \\ FiscalIntegration \\ EpsonFP90IISample mapē Solutions repository (piemēram, paraugs ir**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[izlaišanas/9,33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample) Paraugs sastāv no fiskālā dokumenta nodrošinātāja, kas ir Commerce Runtime () paplašinājums () un finanšu savienotājs, kas ir [Commerce](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) Hardware Station CRT paplašinājums. Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātāja virtuālajā datorā (VM) pakalpojumos Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet Itālijas [fiskālā printera integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-ita-fpi-sample-sdk.md)
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

Izpildiet finanšu integrācijas iestatīšanas soļus, kā [aprakstīts Commerce kanālu finanšu integrācijas iestatīšanai.](setting-up-fiscal-integration-for-retail-channel.md)

1. [Iestatīt finanšu reģistrācijas](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) procesu. Atzīmējiet arī fiskālās reģistrācijas procesa iestatījumus, kas ir [raksturīgi šim fiskālā printera integrācijas paraugam.](#set-up-the-registration-process)
1. [Iestatiet fiskālos tekstus](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts) atlaidēm.
1. [Iestatīt kļūdu apstrādes](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) iestatījumus.
1. [Iestatiet POS finanšu X/Z](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos) pārskatus.
1. [Aktivizējiet atliktās finanšu reģistrācijas manuālu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) izpildi.
1. [Iestatiet debitoru informācijas pārvaldības funkcionalitāti sistēmā](emea-ita-customer-information.md#setup) POS.
1. [Konfigurējiet kanāla](#configure-channel-components) komponentus.

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, izpildiet šīs darbības, lai iestatītu programmu Commerce Headquarters. Papildinformāciju skatiet [sadaļā Komercijas kanālu finanšu integrācijas](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) iestatīšana.

1. Lejupielādēt konfigurācijas failus finanšu dokumentu nodrošinātājam un finanšu savienotājam:

    1. Atveriet risinājumu [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atlasiet pareizu versijas izlaidi atbilstoši SDK/programmas versijai (piemēram, **[izlaidums/9,33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**
    1. Atveriet **src \> FiscalIntegration \> EpsonFP90IISample.**
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failu **commerceRuntime \> DocumentProvider.EpsonFP90IISample \> konfigurācijas \> DocumentProviderEpsonF90IISample.xml** (piemēram, fails laidienam/9,33). [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)
    1. Lejupielādējiet fiskālā savienotāja konfigurācijas failu **HardwareStation \> EpsonFP90IIFiscalDeviceSample \> konfigurācijas \> ConnectorEpsonFP90ISample.xml** (piemēram, fails laidienam/9,33. [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml)

    > [!WARNING]
    > Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas tālākmintās Retail SDK mapēs LCS izstrādātāja VM:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extension.DocumentProvider.EpsonFP90IISample \\ konfigurācijas \\ DocumentProviderEpsonF90IISample.xml
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ Extension.EpsonFP90IIFiscalDeviceSample \\ konfigurācijas \\ ConnectorEpsonFP90IISample.xml
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

- **Norēķinu veidu** kartēšana — to maksāšanas metožu kartēšana, kas ir konfigurētas veikalam, ar fiskāla printera atbalstītajiem maksājumu tipiem. Šajā piemērā parādīts noklusējuma kartējums.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Šajā kartēšanā ir skaidrojums par atribūtiem:

    - **StorePaymentMethod ir maksāšanas metode, kas ir iestatīta veikalam** mazumtirdzniecības **un commerce kanālu \> iestatīšanas maksāšanas \>\>** metodēs.
    - **PrinterPaymentType** un PrinterPaymentIndex ir atbilstošs maksājuma tips un indekss, **kas ir definēts Epson fiskālā** printera dokumentācijā.
    - **DepositPaymentMethod tiek izmantots, lai norādītu printera maksājuma tipu un indeksu debitora pasūtījuma saņemšanas summas daļai, kas ir segta ar debitora pasūtījuma** depozītu.

    Tabulā ir parādīts, kā maksājuma metožu parauga kartēšana atbilst standarta demonstrācijas datos konfigurētajām maksājuma metodēm.

    | Maksāšanas veids | Maksāšanas metodes nosaukums |
    |----------------|---------------------|
    | 1              | Kase                |
    | 3              | Karte                |
    | 4              | Debitora konts    |
    | 6              | Valūta            |
    | 8              | Dāvanu karte           |

    Parauga kartējums ir jāmodificē atbilstoši maksājumu metodēm, kas ir konfigurētas programmā.

- **Svītrkoda tips kvīts** numuram — svītrkoda veids, kas tiek izmantots dokumenta numuram finanšu ieejas plūsmā. Noklusējuma kartējums ir **CODE128**.
- **Drukāt fiskālos datus kvīts virsrakstā — ja šis parametrs ir ieslēgts, veikala** informācija tiks drukāta finanšu dokumentā. Šajā informācijā ir iekļauts veikala nosaukums, adrese, nodokļu identifikācijas numurs un kasiera vārds.
- **Fiskālā printera nodaļas kartēšana – fiskālā printera departamentu kartēšana ar pievienotās vērtības nodokļa (PVN) likmēm, PVN reģistrācijas rakstura likmēm** un preču tipiem. Šajā piemērā parādīts noklusējuma kartējums.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Šajā kartēšanā ir skaidrojums par atribūtiem:

    - **VATRate** ir atbalstīta PVN likme, kas ir konfigurēta kā PVN kods. Kartēšanas vērtībai ir divas decimāldaļas vietas, bet decimāldaļu atdalītājs nav atdalītājs. Piemēram, **2200** attēlo 22 procentus, **un 1000** attēlo 10 procentus.
    - **VATExemptNature ir piemērojams tikai gadījumos, kad PVN likme ir 0 (nulle), ieskaitot gadījumus,** kad nav nodokļa. Pašlaik VATExemptNature tiek atbalstīts tikai dāvanu kartēm, un kartēšanas vērtībai ir **jāatbilst** **VATExemptNatureForGiftCard rekvizīta vērtībai** XML konfigurācijas failā.
    - **ProductType** ir preces veids. Vērtība **0 attēlo** preces, un vērtība **1** attēlo pakalpojumus.
    - **DepartmentNumber** ir nodaļas numurs, kas ir konfigurēts printerī un kas atbilst iepriekšējiem trim atribūtiem.

    Parauga kartējums ir jāmodificē atbilstīgi PVN likmēm, kas ir konfigurētas jūsu programmā, un atbilstošajām nodaļām, kas ir konfigurētas fiskālajā printerī.

- **AR PVN neapliekams dāvanu kartes veids – PVN reģ. reģ. veids, kas ir jāpiemēro, kad dāvanu** karte tiek izsniegta vai atkārtoti piepildīta. Vērtībai ir jāatbilst kādai finanšu printera nodaļas kartēšanas ievadnei. Noklusējuma kartējums ir **NS**.
- **Aktivizējiet brīvās maksas krājumus – ja šis parametrs ir ieslēgts, tiek aktivizēts īpašais apmaksas atlaides korekcijas tips krājumiem, kuriem ir** *100* procentu atlaide.
- **Informācijas kods atgriešanas izcelsmei - informācijas kods, kas tiek izmantots, lai iegūtu atgriešanas darbības** izcelsmi, ja netiek sniegta sākotnējā pārdošanas kvīts. Šis parametrs tiek izmantots kopā ar oriģinālā pārdošanas datuma informācijas kodu un parametru Atgriešanas izcelsmes kartējums, lai finanšu ieejas plūsmā ģenerētu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja nepastāv sākotnējā **pārdošanas** **darbība**. 

    Šis informācijas kods ir jākonfigurē, lai lietotājs varētu atlasīt vai ievadīt vienu no iespējamām atgriešanu izcelsmes jūsu veikalos. Piemēram, to var konfigurēt kā apakškodu sarakstu (piemēram, Atgriešana no vietas **vai** Atgriešana no **vietas**). Pēc **tam** atgriešanas izcelsmes kartēšanas parametrs tiek izmantots, lai translētu informācijas koda vērtību komandā fiskālajam printerim.

    Informācijas kods, kas tiek atlasīts atgriešanas izcelsmes informācijas kodam, jākonfigurē kā obligāts informācijas kods, kas katrā pārdošanas darbībā **tiek** atlaists vienu reizi. POS funkcionalitātes profilā tas jāpiešķir kā atgriešanas preces informācijas kods, lai tas tiktu atlaists, kad tiek palaista operācija **Atgriezt** **preci**.

    Šim kartējumam nav norādīta noklusējuma vērtība. Jāatlasa informācijas kods, kas ir konfigurēts jūsu programmā.

- **Informācijas kods oriģinālajam pārdošanas datumam — informācijas kods, kas tiek izmantots, lai iegūtu atgriezto darbību sākotnējo pārdošanas datumu, ja netiek nodrošināta sākotnējā** pārdošanas kvīts. Šis parametrs tiek izmantots kopā ar informācijas kodu atgriešanas izcelsmes un Atgriešanas izcelsmes kartēšanas parametriem, lai finanšu kvītī izveidotu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja nepastāv sākotnējā **pārdošanas** **darbība**.

    Informācijas kodam jābūt konfigurētam tā, lai **ievades tipa** lauks būtu iestatīts uz **datumu**. Tas ir jākonfigurē kā obligāts informācijas kods, kas pārdošanas darbībai tiek atlaists vienu reizi. Tā ir jāpiešķir arī kā saistītais informācijas kods informācijas kodam, kas ir atlasīts atgriešanas izcelsmes parametra informācijas kodam, lai šie divi informācijas kodi tiktu atlaisti **vienu** pēc **otra**.

    Šim kartējumam nav norādīta noklusējuma vērtība. Jāatlasa informācijas kods, kas ir konfigurēts jūsu programmā.

- **Atgriešanas izcelsmes kartējums – atgriešanas izcelsmes kartējums, kas tiek izmantots, lai izdrukātu atgriešanas darbības** izcelsmi, ja nav sniegta sākotnējā pārdošanas ieejas plūsma. Šis parametrs tiek izmantots kopā ar atgriešanas izcelsmes informācijas kodu un informācijas kodu oriģināla pārdošanas datuma parametriem, lai finanšu ieejas plūsmā ģenerētu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja sākotnējā pārdošanas **darbība** **nepastāv**. Šajā piemērā parādīts noklusējuma kartējums.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Šajā kartēšanā ir skaidrojums par atribūtiem:

    - **ReturnOrigin** ir viena no iespējamām atgriešanas izcelsmei jūsu veikalos. Vērtībai jāatbilst atgriešanas izcelsmes **parametra informācijas koda** vērtībai.
    - **PrinterReturnOrigin ir viena no atgriešanas izcelsmes, ko pieņem** fiskālais **printeris** **·** (POS, POZ, **ND**).
    - **PrinterReturnOriginWithoutFiscalData ir atgriešanas izcelsme, ko fiskālais printeris pieņem un kas atbilst atgriešanas darbībai, kas ir saistīta ar oriģinālo pārdošanas transakciju, kam nav saistītu finanšu datu, jo tā netika reģistrēta, izmantojot** fiskālo printeri. Šajā gadījumā sākotnējais pārdošanas datums tiek identificēts kā sākotnējās pārdošanas darbības datums.

Šie noklusējuma datu kartējumi ir novecojuši un tiek saglabāti tikai atpakaļsaderība:

- Pievienotās vērtības nodokļa (PVN) kodu kartēšana
- Depozīta maksājuma veids

#### <a name="fiscal-connector-settings"></a>Finanšu savienotāja iestatījumi

Šādi iestatījumi ir iekļauti finanšu savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Galapunkta** adrese – printera URL.
- **Datuma un laika sinhronizācija – vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē** ar pievienoto aparatūras staciju.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Itālijas [fiskālā printera integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-ita-fpi-sample-sdk.md)
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

#### <a name="set-up-the-development-environment"></a>Iestatīt izstrādes vidi

Lai iestatītu izstrādes vidi un paplašinātu paraugu ņemšanas, veiciet šādus soļus.

1. Lejupielādējiet Solutions [Dynamics 365 Commerce repozitoriju vai](https://github.com/microsoft/Dynamics365Commerce.Solutions) lejupielādējiet to. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai. Papildinformāciju skatiet lejupielādes [Retail SDK paraugos un atsauces pakotnēs no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet fiskālā printera integrācijas risinājumu **pie Dynamics365Commerce.Solutions \\ FiscalIntegration \\ EpsonFP90IISample \\ EpsonFP90IISample.sln un izveidojiet** to.
1. Instalēt CRT paplašinājumus:

    1. Atrast CRT paplašinājuma instalētāju:

        - **Commerce Scale Unit:** **Mapē EpsonFP90IISample \\ ScaleUnit \\ ScaleUnit.EpsonFP90III.Installer \\ bin \\ Atbug \\ net461 atrodiet** mapi **ScaleUnit.EpsonFP90III.Installer** installer.
        - **CRT Modern POS lokāls: Mapē** **EpsonFP90IISample \\\\ ModernPOS.EpsonFP90III.Installer \\ bin \\ Atkļūdošanas \\ net461** atrodiet **ModernPOS.EpsonFP90III.Installer** installer.

    1. Startējiet CRT paplašinājuma instalētāju no komandrindas:

        - **Commerce Scale vienība:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Lokāls CRT modernajā POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Instalēt aparatūras stacijas paplašinājumus:

    1. Mapē **EpsonFP90IISample \\\\ HardwareStation HardwareStation.EpsonFP90iii.Installer \\ bin \\ Atkļūdošana \\ net461** atrodiet **hardwareStation.EpsonFP90III.Installer** instalētājs.
    1. Startējiet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet darbības, kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos [iepakojumus](fiscal-integration-sample-build-pipeline.md) fiskālās integrācijas parauga iepakojumam. **Fails EpsonFP90II Build-pipeline.yml ir atrodams Solutions repozitorija** **YAML_Files \\**[Dynamics 365 Commerce konveijera](https://github.com/microsoft/Dynamics365Commerce.Solutions) mapē.

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Itālijas fiskālā printera integrācijas paraugs ir balstīts uz [fiskālās integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no retail SDK. Paraugs atrodas **src \\ FiscalIntegration \\ EpsonFP90IISample mapē Solutions repository (piemēram, paraugs ir**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[izlaišanas/9,33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample) Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) no fiskālā dokumenta nodrošinātāja, kas ir CRT Commerce Hardware Station paplašinājums un fiskālais savienotājs. Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Itālijas [fiskālā printera integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-ita-fpi-sample-sdk.md) Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Nolūks paplašinājumam, kas ir fiskālā dokumenta nodrošinātājs, ir izveidot printerim raksturīgus dokumentus un apstrādāt atbildes no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Pieprasījumu **apdarinātājs DocumentProviderEpsonFP90III ir ieejas punkts pieprasījumam** ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest — šajā pieprasījumā ir ietverta** informācija par to, kurš dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālajā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest - šis pieprasījums atgriež notikumu sarakstu,** uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas fails atrodas **src \\ FiscalIntegration \\ EpsonFP90IISample \\ CommerceRuntime \\ DocumentProvider.EpsonFP90IISample \\ Configuration \\ DocumentProviderEpsonF90IISample.xml** risinājumu repozitorijā. [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, nolūks ir sazināties ar fiskālo printeri. Šis paplašinājums izmanto HTTP protokolu, lai iesniegtu CRT dokumentus, ko paplašinājums ģenerē fiskālam printerim. Tā apstrādā arī atbildes, kas saņemtas no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EpsonFP90IISample pieprasījuma apdarinātājs ir ieejas punkts pieprasījumu apstrādei finanšu** perifērijas ierīcē.

Apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest – šis pieprasījums sūta dokumentus printeriem un atgriež** atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja konfigurācijas fails atrodas **\\ src FiscalIntegration \\ EpsonFP90IISample \\ HardwareStation \\ EpsonFP90IIFiscalDeviceSample \\ konfigurācijas \\ ConnectorEpsonFP90IISample.xml** solutions [Dynamics 365 Commerce repozitorijā.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot iestatījumus savienotājam, kas tiks konfigurēts no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
