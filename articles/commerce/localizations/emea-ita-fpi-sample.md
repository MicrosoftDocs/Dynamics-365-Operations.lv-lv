---
title: Fiskālā printera integrācijas piemērs Itālijai
description: Šajā rakstā sniegts pārskats par Itālijas finanšu integrācijas parauga lietojumprogrammu Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-01
ms.openlocfilehash: 6ad97e87e4114a8f2250d0ba4880b7a466b3689e
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631401"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Fiskālā printera integrācijas piemērs Itālijai

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā rakstā sniegts pārskats par Itālijas finanšu integrācijas parauga lietojumprogrammu Microsoft Dynamics 365 Commerce.

Itālijas Commerce funkcionalitāte ietver pārdošanas punkta (POS) parauga integrāciju ar fiskālo printeri. Paraugs paplašina [fiskālās](fiscal-integration-for-retail-channel.md)[integrācijas funkcionalitāti tā, lai tas darbojas ar Epson FP-90III sērijas](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) printeriem no Epson un ļauj sazināties ar fiskālo printeri tīmekļa servera režīmā, izmantojot Web pakalpojumu EpsonFPMate, izmantojot finanšu ePOS-Print API. Paraugs atbalsta tikai režīmu Registratore Telematico (RT). Paraugs ir nodrošināts avota koda formā un ir daļa no Commerce programmatūras izstrādes komplekta (SDK).

Korporācija Microsoft neatlaiž nevienu aparatūru, programmatūru vai dokumentāciju no Epson. Lai iegūtu informāciju par to, kā iegūt fiskālo printeri un darbināt to, sazinieties ar [Epson Epson S.p.A.](https://www.epson.it)

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

        - No finanšu dokumenta par pārdošanu izslēgt izsniegtu/nodāvintu dāvanu kartes rindu.
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
    - Atlikto maksājumu finanšu reģistrācija
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darbību kā reģistrētu un ietveriet infokodus, lai iegūtu kļūmes iemeslu un papildinformāciju.
    - Pirms jaunas pārdošanas darbības atvēršanas vai pārdošanas darbības veikšanas pārbaudiet fiskālā printera pieejamību.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālā printera integrācijas paraugs ievieš tālāk norādītos ar dāvanu kartēm saistītos noteikumus.

- No finanšu dokumenta izslēdziet pārdošanas rindas *, kas ir saistītas ar* dāvanu *kartes izdošanu un* pievienot dāvanu karšu operācijām.
- Nedrukāt finanšu dokumentu, ja tas sastāv tikai no dāvanu kartes rindām.
- Atņemiet no finanšu dokumenta maksājumu rindām izsniegto vai piesaistīto dāvanu karšu kopsummu.
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
- Ikdienas pārskati (finanšu X un finanšu Z) tiek drukāti, izmantojot formātu, kas ir iegults fiskālā printera formā.
- Fiskālais printeris neatbalsta jauktas darbības. POS **funkcionalitātes profilos opcijas Aizliegt jaukšanu un** atgriešanu vienā kvītī **iestatījumam** ir jābūt Jā.
- Paraugs atbalsta integrāciju tikai ar fiskālo printeri, kas darbojas režīmā Registratore Telematico (RT).

## <a name="set-up-fiscal-integration-for-italy"></a>Iestatīt Itālijas fiskālo integrāciju

Itālijas fiskālā printera integrācijas paraugs ir balstīts uz finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no Commerce SDK. Paraugs atrodas src **FiscalIntegration\\ EpsonFP90IISample\\** mapē Solutions repository [Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) no fiskālā dokumenta nodrošinātāja, kas ir Commerce Runtime () paplašinājums (CRT) un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot Commerce SDK, [skatiet download Commerce SDK par paraugos un atsauces pakotnēs no GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md)[un un iestatiet būvējuma konveijeru neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Itālijas fiskālā printera integrācijas paraugs ir pieejams Commerce SDK versijā 10.0.29. Commerce versijā 10.0.28 vai agrākā versijā jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātāja virtuālajā datorā (VM) Microsoft Dynamics pakalpojumos Lifecycle Services (LCS). Papildinformāciju skatiet Itālijas [fiskālā printera integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-ita-fpi-sample-sdk.md)

Veiciet fiskālās integrācijas iestatīšanas soļus, kā [aprakstīts Commerce kanālu finanšu integrācijas iestatīšanai](setting-up-fiscal-integration-for-retail-channel.md).

1. [Iestatīt fiskālās reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Atzīmējiet arī fiskālās reģistrācijas procesa iestatījumus, kas ir raksturīgi šim [fiskālā printera integrācijas paraugam](#set-up-the-registration-process).
1. [Iestatiet fiskālos tekstus atlaidēm](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Iestatīt kļūdu apstrādes iestatījumus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iestatiet POS finanšu X/Z pārskatus](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Iespējojiet atliktās finanšu reģistrācijas manuālu izpildi](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Iestatiet debitoru informācijas pārvaldības funkcionalitāti sistēmā POS](emea-ita-customer-information.md#setup).
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, izpildiet šīs darbības, lai iestatītu programmu Commerce Headquarters. Papildinformāciju skatiet [šeit: Komercijas kanālu finanšu integrācijas iestatīšana](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lejupielādēt konfigurācijas failus finanšu dokumentu nodrošinātājam un finanšu savienotājam:

    1. Atveriet risinājumu repozitoriju [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai.
    1. Atveriet **src \> FiscalIntegration \> EpsonFP90IISample**.
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failu **commerceRuntime \> DocumentProvider.EpsonFP90IISample \> konfigurācijas \> DocumentProviderEpsonF90IISample.xml**.
    1. Lejupielādējiet fiskālā savienotāja **konfigurācijas failu Aparatūras stacijā \> EpsonFP90IIFiscalDeviceSample \> konfigurācijas \> ConnectorEpsonFP90IISample.xml**.

    > [!NOTE]
    > Commerce versijā 10.0.28 vai agrākai versijai ir jāizmanto retail SDK iepriekšējā versija izstrādātājam VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas tālākmintās Retail SDK mapēs LCS izstrādātāja VM:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extension.DocumentProvider.EpsonFP90IISample\\ konfigurācijas\\ DocumentProviderEpsonF90IISample.xml
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk\\ SampleExtensions\\ HardwareStation\\ Extension.EpsonFP90IIFiscalDeviceSample konfigurācijas\\\\ ConnectorEpsonFP90IISample.xml

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

- **Norēķinu veidu kartēšana** — to maksāšanas metožu kartēšana, kas ir konfigurētas veikalam, ar fiskāla printera atbalstītajiem maksājumu tipiem. Šajā piemērā parādīts noklusējuma kartējums.

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

    - **StorePaymentMethod** ir maksāšanas metode, kas ir iestatīta veikalam mazumtirdzniecības **un commerce \> kanālu iestatīšanas maksāšanas \> metodēs \>**.
    - **PrinterPaymentType** un **PrinterPaymentIndex** ir atbilstošs maksājuma tips un indekss, kas ir definēts Epson fiskālā printera dokumentācijā.
    - **DepositPaymentMethod** tiek izmantots, lai norādītu printera maksājuma tipu un indeksu debitora pasūtījuma saņemšanas summas daļai, kas ir segta ar debitora pasūtījuma depozītu.

    Tabulā ir parādīts, kā maksājuma metožu parauga kartēšana atbilst standarta demonstrācijas datos konfigurētajām maksājuma metodēm.

    | Maksājuma metode | Maksāšanas metodes nosaukums |
    |----------------|---------------------|
    | 1              | Skaidra nauda                |
    | 3              | Karte                |
    | 4              | Debitora konts    |
    | 6              | Valūta            |
    | 8              | Dāvanu karte           |

    Parauga kartējums ir jāmodificē atbilstoši maksājumu metodēm, kas ir konfigurētas programmā.

- **Svītrkoda tips kvīts numuram** — svītrkoda veids, kas tiek izmantots dokumenta numuram finanšu ieejas plūsmā. Noklusējuma kartējums ir **CODE128**.
- **Drukāt fiskālos datus kvīts** virsrakstā — ja šis parametrs ir ieslēgts, veikala informācija tiks drukāta finanšu dokumentā. Šajā informācijā ir iekļauts veikala nosaukums, adrese, nodokļu identifikācijas numurs un kasiera vārds.
- **Fiskālā printera nodaļas** kartēšana – fiskālā printera departamentu kartēšana ar pievienotās vērtības nodokļa (PVN) likmēm, PVN reģistrācijas rakstura likmēm un preču tipiem. Šajā piemērā parādīts noklusējuma kartējums.

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

    - **VATRate** ir atbalstīta PVN likme, kas ir konfigurēta kā PVN kods. Kartēšanas vērtībai ir divas decimāldaļas vietas, bet decimāldaļu atdalītājs nav atdalītājs. Piemēram, **2200 attēlo** 22 procentus, **un 1000** attēlo 10 procentus.
    - **VATExemptNature ir** piemērojams tikai gadījumos, kad PVN likme ir 0 (nulle), ieskaitot gadījumus, kad nav nodokļa. Pašlaik VATExemptNature **tiek atbalstīts tikai dāvanu kartēm,** **un kartēšanas vērtībai ir jāatbilst VATExemptNatureForGiftCard** rekvizīta vērtībai XML konfigurācijas failā.
    - **ProductType** ir preces veids. **Vērtība 0 attēlo** preces, un vērtība **1 attēlo** pakalpojumus.
    - **DepartmentNumber** ir nodaļas numurs, kas ir konfigurēts printerī un kas atbilst iepriekšējiem trim atribūtiem.

    Parauga kartējums ir jāmodificē atbilstīgi PVN likmēm, kas ir konfigurētas jūsu programmā, un atbilstošajām nodaļām, kas ir konfigurētas fiskālajā printerī.

- **AR PVN neapliekams** dāvanu kartes veids – PVN reģ. reģ. veids, kas ir jāpiemēro, kad dāvanu karte tiek izsniegta vai atkārtoti piepildīta. Vērtībai ir jāatbilst kādai finanšu printera nodaļas kartēšanas ievadnei. Noklusējuma kartējums ir **NS**.
- **Aktivizējiet brīvās** maksas krājumus – ja šis parametrs ir ieslēgts, *tiek aktivizēts īpašais apmaksas* atlaides korekcijas tips krājumiem, kuriem ir 100 procentu atlaide.
- **Informācijas kods atgriešanas izcelsmei** - informācijas kods, kas tiek izmantots, lai iegūtu atgriešanas darbības izcelsmi, ja netiek sniegta sākotnējā pārdošanas kvīts. Šis parametrs **tiek izmantots kopā ar oriģinālā pārdošanas datuma informācijas** **kodu** un parametru Atgriešanas izcelsmes kartējums, lai finanšu ieejas plūsmā ģenerētu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja nepastāv sākotnējā pārdošanas darbība. 

    Šis informācijas kods ir jākonfigurē, lai lietotājs varētu atlasīt vai ievadīt vienu no iespējamām atgriešanu izcelsmes jūsu veikalos. Piemēram, to var konfigurēt kā apakškodu sarakstu (**piemēram, Atgriešana no vietas vai** **Atgriešana no ieejas**). Pēc **tam atgriešanas** izcelsmes kartēšanas parametrs tiek izmantots, lai translētu informācijas koda vērtību komandā fiskālajam printerim.

    Informācijas kods, kas tiek atlasīts **atgriešanas** izcelsmes informācijas kodam, jākonfigurē kā obligāts informācijas kods, kas katrā pārdošanas darbībā tiek atlaists vienu reizi. POS funkcionalitātes profilā **tas** jāpiešķir kā atgriešanas preces informācijas kods, lai tas tiktu **atlaists**, kad tiek palaista operācija Atgriezt preci.

    Šim kartējumam nav norādīta noklusējuma vērtība. Jāatlasa informācijas kods, kas ir konfigurēts jūsu programmā.

- **Informācijas kods oriģinālajam pārdošanas datumam** — informācijas kods, kas tiek izmantots, lai iegūtu atgriezto darbību sākotnējo pārdošanas datumu, ja netiek nodrošināta sākotnējā pārdošanas kvīts. Šis **parametrs** **tiek** izmantots kopā ar informācijas kodu atgriešanas izcelsmes un Atgriešanas izcelsmes kartēšanas parametriem, lai finanšu kvītī izveidotu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja nepastāv sākotnējā pārdošanas darbība.

    Informācijas kodam jābūt konfigurētam tā, lai ievades **tipa lauks** būtu iestatīts uz **datumu**. Tas ir jākonfigurē kā obligāts informācijas kods, kas pārdošanas darbībai tiek atlaists vienu reizi. Tā ir **jāpiešķir** **arī** kā saistītais informācijas kods informācijas kodam, kas ir atlasīts atgriešanas izcelsmes parametra informācijas kodam, lai šie divi informācijas kodi tiktu atlaisti vienu pēc otra.

    Šim kartējumam nav norādīta noklusējuma vērtība. Jāatlasa informācijas kods, kas ir konfigurēts jūsu programmā.

- **Atgriešanas izcelsmes kartējums** – atgriešanas izcelsmes kartējums, kas tiek izmantots, lai izdrukātu atgriešanas darbības izcelsmi, ja nav sniegta sākotnējā pārdošanas ieejas plūsma. Šis **parametrs** **tiek** izmantots kopā ar atgriešanas izcelsmes informācijas kodu un informācijas kodu oriģināla pārdošanas datuma parametriem, lai finanšu ieejas plūsmā ģenerētu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja sākotnējā pārdošanas darbība nepastāv. Šajā piemērā parādīts noklusējuma kartējums.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Šajā kartēšanā ir skaidrojums par atribūtiem:

    - **ReturnOrigin** ir viena no iespējamām atgriešanas izcelsmei jūsu veikalos. Vērtībai jāatbilst atgriešanas izcelsmes parametra **informācijas koda vērtībai**.
    - **PrinterReturnOrigin ir** viena no atgriešanas izcelsmes, ko pieņem fiskālais printeris (**POS,POZITO** **vai** **ND).**
    - **PrinterReturnOriginWithoutFiscalData** ir atgriešanas izcelsme, ko fiskālais printeris pieņem un kas atbilst atgriešanas darbībai, kas ir saistīta ar oriģinālo pārdošanas transakciju, kam nav saistītu finanšu datu, jo tā netika reģistrēta, izmantojot fiskālo printeri. Šajā gadījumā sākotnējais pārdošanas datums tiek identificēts kā sākotnējās pārdošanas darbības datums.

Šie noklusējuma datu kartējumi ir novecojuši un tiek saglabāti tikai atpakaļsaderība:

- Pievienotās vērtības nodokļa (PVN) kodu kartēšana
- Depozīta maksājuma veids

#### <a name="fiscal-connector-settings"></a>Finanšu savienotāja iestatījumi

Šādi iestatījumi ir iekļauti finanšu savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Galapunkta** adrese – printera URL.
- **Datuma un laika sinhronizācija** – vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē ar pievienoto aparatūras staciju.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

> [!NOTE]
> - Itālijas fiskālā printera integrācijas paraugs ir pieejams Commerce SDK versijā 10.0.29. Commerce versijā 10.0.28 vai agrākā versijā ir jāizmanto retail SDK iepriekšējā versija izstrādātājam VM LCS. Papildinformāciju skatiet Itālijas [fiskālā printera integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-ita-fpi-sample-sdk.md)
> - Commerce paraugi, kas ir izvietoti jūsu vidē, netiek automātiski atjaunināti, kad commerce komponentiem izmantojat pakalpojumu vai kvalitātes atjauninājumus. Jums manuāli jāatjaunina nepieciešamie paraugi.

#### <a name="set-up-the-development-environment"></a>Iestatīt izstrādes vidi

Lai iestatītu izstrādes vidi un paplašinātu paraugu ņemšanas, veiciet šādus soļus.

1. Lejupielādējiet Solutions repozitoriju vai [Dynamics 365 Commerce lejupielādējiet](https://github.com/microsoft/Dynamics365Commerce.Solutions) to. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai. Papildinformāciju skatiet Lejupielādes [Commerce SDK paraugos un atsauces pakotnēs no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet fiskālā printera **integrācijas risinājumu pie Dynamics365Commerce.Solutions\\ FiscalIntegration\\ EpsonFP90IISample\\ EpsonFP90IISample.sln** un izveidojiet to.
1. Instalēt CRT paplašinājumus:

    1. Atrast paplašinājuma CRT instalētāju:

        - **Commerce Scale Unit:** Mapē EpsonFP90IISample **ScaleUnit ScaleUnit.EpsonFP90III.Installer\\\\ bin\\ Atbug\\ net461 atrodiet\\** mapi ScaleUnit.EpsonFP90III.Installer installer **.**
        - **CRT Modern POS lokāls:** **Mapē EpsonFP90IISample\\ ModernPOS.EpsonFP90III.Installer\\\\ bin\\ Atkļūdošanas\\ net461** atrodiet **ModernPOS.EpsonFP90III.Installer installer**.

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

    1. **Mapē EpsonFP90IISample\\ HardwareStation\\ HardwareStation.EpsonFP90iii.Installer\\ bin\\ Atkļūdošana\\ net461** atrodiet **hardwareStation.EpsonFP90III.Installer instalētājs**.
    1. Startējiet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet [darbības](fiscal-integration-sample-build-pipeline.md), kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos iepakojumus fiskālās integrācijas parauga iepakojumam. Fails EpsonFP90II Build-pipeline.yml **ir atrodams Solutions** **repozitorija YAML_Files\\** konveijera [Dynamics 365 Commerce mapē.](https://github.com/microsoft/Dynamics365Commerce.Solutions)

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Itālijas fiskālā printera integrācijas paraugs ir balstīts uz finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no Commerce SDK. Paraugs atrodas src **FiscalIntegration\\ EpsonFP90IISample\\** mapē Solutions repository [Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) no fiskālā dokumenta nodrošinātāja, CRT kas ir Commerce Hardware Station paplašinājums un fiskālais savienotājs. Papildinformāciju par to, kā izmantot Commerce SDK, [skatiet download Commerce SDK par paraugos un atsauces pakotnēs no GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md)[un un iestatiet būvējuma konveijeru neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Itālijas fiskālā printera integrācijas paraugs ir pieejams Commerce SDK versijā 10.0.29. Commerce versijā 10.0.28 vai agrākā versijā ir jāizmanto retail SDK iepriekšējā versija izstrādātājam VM LCS. Papildinformāciju skatiet Itālijas [fiskālā printera integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-ita-fpi-sample-sdk.md)

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Nolūks paplašinājumam, kas ir fiskālā dokumenta nodrošinātājs, ir izveidot printerim raksturīgus dokumentus un apstrādāt atbildes no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Pieprasījumu **apdarinātājs DocumentProviderEpsonFP90III ir** ieejas punkts pieprasījumam ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest —** šajā pieprasījumā ir ietverta informācija par to, kurš dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālajā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest** - šis pieprasījums atgriež notikumu sarakstu, uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas fails atrodas src **FiscalIntegration\\ EpsonFP90IISample CommerceRuntime\\ DocumentProvider.EpsonFP90IISample\\ Configuration\\ DocumentProviderEpsonF90IISample.xml\\\\ risinājumu** repozitorijā [Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, nolūks ir sazināties ar fiskālo printeri. Šis paplašinājums izmanto HTTP protokolu, lai iesniegtu dokumentus, ko CRT paplašinājums ģenerē fiskālam printerim. Tā apstrādā arī atbildes, kas saņemtas no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EpsonFP90IISample** pieprasījuma apdarinātājs ir ieejas punkts pieprasījumu apstrādei finanšu perifērijas ierīcē.

Apdarinātājs ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – šis pieprasījums sūta dokumentus printeriem un atgriež atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja konfigurācijas fails atrodas src **FiscalIntegration\\ EpsonFP90IISample\\ HardwareStation\\ EpsonFP90IIFiscalDeviceSample\\ konfigurācijas\\ ConnectorEpsonFP90IISample.xml\\** solutions repozitorijā [Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot iestatījumus savienotājam, kas tiks konfigurēts no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
