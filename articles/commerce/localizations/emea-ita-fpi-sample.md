---
title: Fiskālā printera integrācijas piemērs Itālijai
description: Šajā tēmā ir sniegts pārskats par fiskālās integrācijas paraugu Itālijai Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 02226fd9f2c92db2518ca48baefb680a3d2f0ac1
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076907"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Fiskālā printera integrācijas piemērs Itālijai

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par fiskālās integrācijas paraugu Itālijai Microsoft Dynamics 365 Commerce.

Itālijai paredzētajā Commerce funkcionalitātē ietilpst tirdzniecības vietas (POS) integrācijas paraugs ar fiskālo printeri. Paraugs paplašina [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) lai tas darbotos ar [Epson FP-90III sērija](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) printeriem no Epson, un tas nodrošina saziņu ar fiskālo printeri tīmekļa servera režīmā, izmantojot EpsonFPMate tīmekļa pakalpojumu, izmantojot Fiscal ePOS-Print API. Paraugs atbalsta tikai Registratore Telematico (RT) režīmu. Paraugs tiek nodrošināts avota koda veidā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Microsoft neizlaiž no Epson nekādu aparatūru, programmatūru vai dokumentāciju. Lai iegūtu informāciju par fiskālā printera iegūšanu un lietošanu, sazinieties ar [Epson Italia SpA](https://www.epson.it)

## <a name="scenarios"></a>Scenāriji

Itālijas fiskālā printera integrācijas paraugā ir ietverti šādi scenāriji.

- Pārdošanas scenāriji:

    - Izdrukājiet fiskālo kvīti par skaidras naudas pārdošanu un atgriešanu.
    - Uztveriet atbildi no fiskālā printera un saglabājiet to kanālu datu bāzē.
    - Nodokļi:

        - Karte ar fiskālā printera nodokļu kodiem (nodaļām).
        - Pārsūtiet kartētos nodokļu datus uz fiskālo printeri.
        - Drukājiet nodokļus fiskālā kvītī.

    - Maksājumi:

        - Karte ar fiskālā printera maksāšanas metodēm.
        - Izdrukājiet maksājumus fiskālā kvītī.
        - Drukāt informāciju par izmaiņām.

    - Drukas līniju atlaides.
    - Dāvanu kartes:

        - Izslēdziet izsniegtu/pārlādētu dāvanu karšu līniju no pārdošanas fiskālā kvīts.
        - Izdrukājiet maksājumu, kurā kā parastais maksāšanas veids tiek izmantota dāvanu karte.

    - Drukājiet fiskālos čekus klientu pasūtījuma operācijām:

        - Par klienta pasūtījuma depozītu netiek drukāta fiskālā kvīts.
        - Drukājiet fiskālo kvīti par klientu hibrīda pasūtījuma izpildes rindām.
        - Izdrukājiet fiskālo kvīti klienta pasūtījuma saņemšanas operācijai.
        - Izdrukājiet atgriešanas pasūtījuma fiskālo kvīti.

    - Izdrukājiet fiskālā kvītī kvīts numura svītrkodu.
    - Izdrukājiet [Klienta informācija](emea-ita-customer-information.md) kas norādīts pārdošanas darījumam fiskālā kvītī. Šīs informācijas piemērs ir klienta loterijas kods. 

- Dienas beigu pārskati (fiskālie X un fiskālie Z pārskati).
- Kļūdu apstrāde, piemēram, šādas opcijas:

    - Atkārtoti mēģiniet veikt fiskālo reģistrāciju, ja ir iespējams atkārtots mēģinājums, piemēram, ja fiskālais printeris nav pievienots, nav gatavs vai nereaģē, printerī ir beidzies papīrs vai ir iestrēdzis papīrs.
    - Atlikt fiskālo reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darījumu kā reģistrētu un iekļaujiet informācijas kodus, lai fiksētu kļūmes iemeslu un papildu informāciju.
    - Pirms jauna pārdošanas darījuma atvēršanas vai pārdošanas darījuma pabeigšanas pārbaudiet fiskālā printera pieejamību.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālā printera integrācijas paraugā ir ieviesti šādi noteikumi, kas saistīti ar dāvanu kartēm:

- Izslēdziet pārdošanas rindas, kas ir saistītas ar *Izsniegt dāvanu karti* un *Pievienot dāvanu kartei* operācijas no fiskālā kvīts.
- Nedrukājiet fiskālo kvīti, ja tajā ir tikai dāvanu kartes rindas.
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
- Ikdienas pārskati (fiskālie X un fiskālie Z) tiek drukāti, izmantojot formātu, kas ir iegults fiskālā printera programmaparatūrā.
- Fiskālais printeris neatbalsta jauktus darījumus. The **Aizliegt vienā kvītī sajaukt pārdošanu un atgriešanu** opcija ir jāiestata uz **Jā** POS funkcionalitātes profilos.
- Paraugs atbalsta integrāciju tikai ar fiskālo printeri, kas darbojas Reģistratore Telematico (RT)) režīmā.

## <a name="set-up-fiscal-integration-for-italy"></a>Izveidot fiskālo integrāciju Itālijai

Fiskālā printera integrācijas paraugs Itālijai ir balstīts uz [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **src\\ Fiskālā integrācija\\ EpsonFP90IIISample** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijs (piemēram, [paraugs izlaidumā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir Commerce izpildlaika paplašinājums (CRT), un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Izstrādātāja virtuālajā mašīnā (VM) ir jāizmanto iepriekšējā mazumtirdzniecības SDK versija Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Papildinformāciju skatiet [Izvēršanas vadlīnijas fiskālā printera integrācijas paraugam Itālijai (mantots)](emea-ita-fpi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

Pabeidziet finanšu integrācijas iestatīšanas soļus, kā aprakstīts sadaļā [Iestatīt finanšu integrāciju commerce kanāliem](setting-up-fiscal-integration-for-retail-channel.md).

1. [Iestatiet finanšu reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ņemiet vērā arī fiskālās reģistrācijas procesa iestatījumus, kas ir [raksturīgi šim finanšu printera integrācijas paraugam](#set-up-the-registration-process).
1. [Iestatiet fiskālos tekstus atlaidēm](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Iestatiet kļūdu apstrādes iestatījumus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iestatiet finanšu X/Z pārskatus no POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Iespējot atliktās finanšu reģistrācijas](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) manuālu izpildi.
1. [Iestatiet funkcionalitāti klientu informācijas pārvaldībai POS](emea-ita-customer-information.md#setup).
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, veiciet šīs darbības, lai iestatītu Commerce headquarters. Plašāku informāciju skatiet [Set up the fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lejupielādēt finanšu dokumentu nodrošinātāja un finanšu savienotāja konfigurācijas failus:

    1. [Dynamics 365 Commerce Atveriet risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atlasiet pareizu laidiena filiāles versiju atbilstoši SDK/lietojumprogrammas versijai (piemēram, **[laidiens/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atvērt **src \> Fiskālā integrācija \> EpsonFP90IIISample**.
    1. Lejupielādējiet fiskālo dokumentu nodrošinātāja konfigurācijas failu vietnē **CommerceRuntime \> DocumentProvider.EpsonFP90IIIParaugs \> Konfigurācija \> DocumentProviderEpsonFP90IIISample.xml** (piemēram, [izlaišanas fails/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Lejupielādējiet fiskālā savienotāja konfigurācijas failu vietnē **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Konfigurācija \> ConnectorEpsonFP90IIISample.xml** (piemēram, [izlaišanas fails/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml).

    > [!WARNING]
    > Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas šādās mazumtirdzniecības SDK mapēs izstrādātāja VM LCS:
    >
    > - **Fiskālo dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk\\ Extensions paraugi\\ CommerceRuntime\\ Extension.DocumentProvider.EpsonFP90IIISample\\ Konfigurācija\\ DocumentProviderEpsonFP90IIISample.xml
    > - **Fiskālā savienotāja konfigurācijas fails:** RetailSdk\\ Extensions paraugi\\ HardwareStation\\ Paplašinājums.EpsonFP90IIIFiscalDeviceSample\\ Konfigurācija\\ ConnectorEpsonFP90IIISample.xml
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

- **Konkursa veidu kartēšana** – Veikalam konfigurēto maksājumu metožu kartēšana ar maksājumu veidiem, ko atbalsta fiskālais printeris. Nākamajā piemērā ir parādīta noklusējuma kartēšana.

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

    Šeit ir šīs kartēšanas atribūtu skaidrojums:

    - **Veikala Maksājuma metode** ir maksājuma veids, kas ir iestatīts veikalam plkst **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Maksājuma metodes \> Maksājuma metodes**.
    - **Printera maksājuma veids** un **PrinterPaymentIndex** ir atbilstošais maksājuma veids un indekss, kas definēts Epson fiskālā printera dokumentācijā.
    - **Depozīta apmaksas metode** tiek izmantots, lai norādītu printera maksājuma veidu un indeksu tai daļai no klienta pasūtījuma saņemšanas summas, kas tiek norēķināta ar klienta pasūtījuma depozītu.

    Šajā tabulā parādīts, kā maksājumu metožu izlases kartēšana atbilst krātuves maksāšanas metodēm, kas ir konfigurētas standarta demonstrācijas datos.

    | Maksāšanas veids | Maksāšanas metodes nosaukums |
    |----------------|---------------------|
    | 1              | Kase                |
    | 3              | Karte                |
    | 4              | Debitora konts    |
    | 6              | Valūta            |
    | 8              | Dāvanu karte           |

    Jums ir jāmaina kartējuma paraugs atbilstoši jūsu lietojumprogrammā konfigurētajām maksājumu metodēm.

- **Ieejas plūsmas numura** svītrkoda tips – svītrkoda tips, kas tiek izmantots, lai finanšu kvītī parādītu ieejas plūsmas numuru. Noklusējuma kartējums ir **CODE128**.
- **Drukāt fiskālos datus saņemšanas virsrakstam** – ja šis parametrs ir ieslēgts, uz finanšu ieejas plūsmas tiks drukāta veikala informācija. Šī informācija ietver veikala nosaukumu, adresi un nodokļu maksātāja identifikācijas numuru, kā arī kasiera vārdu.
- **Fiskālo printeru nodaļas kartēšana** – fiskālā printera nodaļu kartēšana uz pievienotās vērtības nodokļa (PVN) likmēm, no PVN atbrīvotajiem raksturs un produktu veidiem. Nākamajā piemērā ir parādīta noklusējuma kartēšana.

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

    Šeit ir šīs kartēšanas atribūtu skaidrojums:

    - **PVN likme** ir atbalstīta PVN likme, kas ir konfigurēta kā PVN kods. Kartējuma vērtībai ir divas decimāldaļas, bet nav decimāldaļu atdalītāja. Piemēram, **2200** ir 22 procenti, bet **1000** — 10 procenti.
    - **PVNExemptNature** ir piemērojams tikai gadījumos, kad PVN likme ir 0 (nulle), ieskaitot gadījumus, kad nav nodokļa. **Pašlaik VATExemptNature** tiek atbalstīts tikai dāvanu kartēm, un kartēšanas vērtībai jāatbilst XML konfigurācijas faila rekvizīta VATExemptNatureForGiftCard **vērtībai**.
    - **ProductType** ir produkta tips. Vērtība **0** apzīmē preces, un vērtība **1** atspoguļo pakalpojumus.
    - **DepartmentNumber** ir nodaļā konfigurētās nodaļas numurs, kas atbilst iepriekšējiem trim atribūtiem.

    Parauga kartējums ir jāmodificē atbilstoši lietojumprogrammā konfigurētajām PVN likmēm un atbilstošajām nodaļām, kas ir konfigurētas jūsu finanšu printerī.

- **No PVN atbrīvotā daba dāvanu kartei** – No PVN atbrīvots raksturs, kas jāpiemēro, izsniedzot vai uzpildot dāvanu karti. Vērtībai jāatbilst kādam ierakstam fiskālā printeru nodaļas kartējumā. Noklusējuma kartējums ir **NS**.
- **Iespējot bez maksas preces** – ja šis parametrs ir ieslēgts, ir iespējots īpašais *omaggio* atlaides korekcijas tips precēm ar 100 procentu atlaidi.
- **Atgriešanas izcelsmes** informācijas kods — informācijas kods, kas tiek izmantots, lai fiksētu atgriešanas transakcijas izcelsmi, ja nav norādīta sākotnējā pārdošanas kvīts. Šis parametrs tiek izmantots kopā ar **informācijas kodu sākotnējam pārdošanas datumam** un **Atgriešanas izcelsmes kartēšanas** parametriem, lai finanšu kvītī ģenerētu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja nav oriģinālas pārdošanas darbības. 

    Šis informācijas kods ir jākonfigurē tā, lai lietotājs varētu atlasīt vai ievadīt kādu no iespējamajām preču atgriešanas pirmsākumiem jūsu veikalos. Piemēram, to var konfigurēt kā apakškodu sarakstu (piemēram **, Atgriezties no vietnes** vai **Atgriezt no kioska**). Pēc tam atgriešanas **izcelsmes kartēšanas** parametrs tiek izmantots, lai informācijas koda vērtību pārvērstu par fiskālā printera komandu.

    Informācijas kods, kas atlasīts atgriešanas **izcelsmes** informācijas kodam, jākonfigurē kā obligāts informācijas kods, kas tiek atlaists vienu reizi pārdošanas darījumā. Tas ir jāpiešķir kā atgriešanas **produkta** informācijas kods POS funkcionalitātes profilā, lai tas tiktu atlaists, kad **tiek palaista atgriešanas produkta** operācija.

    Šim kartējumam nav norādīta noklusējuma vērtība. Jāatlasa lietojumprogrammā konfigurēts informācijas kods.

- **Sākotnējā pārdošanas datuma** informācijas kods — informācijas kods, kas tiek izmantots, lai fiksētu atgriešanas transakcijas sākotnējo pārdošanas datumu, ja nav norādīta sākotnējā pārdošanas kvīts. Šis parametrs tiek izmantots kopā ar **informācijas kodu atgriešanas izcelsmei** un **Atgriešanas izcelsmes kartēšanas** parametriem, lai finanšu kvītī ģenerētu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja nav oriģinālas pārdošanas darbības.

    Informācijas kods jākonfigurē tā, lai lauks Ievades **tips** būtu iestatīts uz **Datums**. Tas jākonfigurē kā obligāts informācijas kods, kas tiek atlaists vienu reizi katrā pārdošanas darījumā. Tas jāpiešķir arī kā **saistītās informācijas kods** informācijas kodam, kas atlasīts parametram **Return Origin** Info kods, lai abi informācijas kodi tiktu atlaisti cits pēc otra.

    Šim kartējumam nav norādīta noklusējuma vērtība. Jāatlasa lietojumprogrammā konfigurēts informācijas kods.

- **Atgriešanas izcelsmes kartējums** — atgriešanas izcelsmes kartējums, kas tiek izmantots atgriešanas darbības izcelsmes drukāšanai, ja nav norādīta sākotnējā pārdošanas ieejas plūsma. Šis parametrs tiek izmantots kopā ar **atgriezto preču izcelsmes** informācijas kodu un **informācijas kodu sākotnējiem pārdošanas datuma** parametriem, lai finanšu kvītī ģenerētu pareizu ziņojumu par atgriešanas darbības izcelsmi, ja nav oriģinālas pārdošanas darbības. Nākamajā piemērā ir parādīta noklusējuma kartēšana.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Šeit ir šīs kartēšanas atribūtu skaidrojums:

    - **ReturnOrigin** ir viena no iespējamām atgriešanās pirmsākumiem jūsu veikalos. Vērtībai jāatbilst parametra Return Origin **informācijas koda vērtībai**.
    - **PrinterReturnOrigin** ir viena no atgriešanas pirmsākumiem, ko akceptē finanšu printeris (**POS**, **VR** vai **ND**).
    - **PrinterReturnOriginWithoutFiscalData** ir atgriešanas izcelsme, ko pieņem finanšu printeris un kas atbilst atgriešanas darbībai, kura ir saistīta ar sākotnējo pārdošanas transakciju, kurai nav saistītu finanšu datu, jo tā nav reģistrēta, izmantojot fiskālo printeri. Šajā gadījumā sākotnējais pārdošanas datums tiek identificēts kā sākotnējās pārdošanas darbības datums.

Šādi noklusējuma datu kartējumi ir novecojuši un tiek glabāti tikai atpakaļsaderībai:

- Pievienotās vērtības nodokļa (PVN) kodu kartēšana
- Depozīta maksājuma veids

#### <a name="fiscal-connector-settings"></a>Fiskālā savienotāja iestatījumi

Tālāk norādītie iestatījumi ir iekļauti fiskālā savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga.

- **Galapunkta adrese** – Printera URL.
- **Datuma un laika sinhronizācija** – Vērtība, kas norāda, vai printera datums un laiks ir jāsinhronizē ar pievienoto aparatūras staciju.

### <a name="configure-channel-components"></a>Konfigurējiet kanāla komponentus

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Papildinformāciju skatiet [Izvēršanas vadlīnijas fiskālā printera integrācijas paraugam Itālijai (mantots)](emea-ita-fpi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

#### <a name="set-up-the-development-environment"></a>Iestatiet izstrādes vidi

Lai iestatītu izstrādes vidi, lai pārbaudītu un paplašinātu paraugu, veiciet šīs darbības.

1. Klonējiet vai lejupielādējiet [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve. Atlasiet pareizo laidiena filiāles versiju atbilstoši savai SDK/lietojumprogrammas versijai. Papildinformāciju skatiet [Lejupielādējiet mazumtirdzniecības SDK paraugus un atsauces pakotnes no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet finanšu printera integrācijas risinājumu **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln** un izveidojiet to.
1. Uzstādīt CRT paplašinājumi:

    1. Atrodi CRT paplašinājumu instalētājs:

        - **Commerce Scale Unit:** mapē **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** atrodiet mapiUnit.EpsonFP90III.Installer **instalētāju.**
        - **Lokālais CRT vietnē Modern POS:** **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** atrodiet **modernPOS.EpsonFP90III.Installer** instalētāju.

    1. Sāciet CRT paplašinājuma instalētājs no komandrindas:

        - **Tirdzniecības mēroga vienība:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Vietējais CRT Mūsdienu POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Instalējiet aparatūras stacijas paplašinājumus:

    1. **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** atrodiet **HardwareStation.EpsonFP90III.Installer** instalētāju.
    1. Sāciet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet norādījumus [Fiskālās integrācijas parauga izveides konveijera iestatīšana](fiscal-integration-sample-build-pipeline.md) lai ģenerētu un atbrīvotu Cloud Scale Unit un pašapkalpošanās izvietojamās pakotnes fiskālās integrācijas paraugam. **EpsonFP90III build-pipeline.yml** veidnes YAML failu var atrast **risinājumu\\ repozitorija mapē** Pipeline [Dynamics 365 Commerce YAML_Files](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Paplašinājumu projektēšana

Fiskālā printera integrācijas paraugs Itālijai ir balstīts uz [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **src\\ Fiskālā integrācija\\ EpsonFP90IIISample** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijs (piemēram, [paraugs izlaidumā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir paplašinājums CRT, un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Papildinformāciju skatiet [Izvēršanas vadlīnijas fiskālā printera integrācijas paraugam Itālijai (mantots)](emea-ita-fpi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

### <a name="commerce-runtime-extension-design"></a>Tirdzniecības izpildlaika paplašinājuma dizains

Paplašinājuma, kas ir fiskālo dokumentu nodrošinātājs, mērķis ir ģenerēt printerim specifiskus dokumentus un apstrādāt atbildes no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **DocumentProviderEpsonFP90III** pieprasījumu apstrādātājs ir ieejas punkts pieprasījumam ģenerēt dokumentus no fiskālā printera.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež printerim raksturīgu dokumentu, kas jāreģistrē fiskālā printerī.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Šis pieprasījums atgriež abonējamo notikumu sarakstu. Pašlaik tiek atbalstīti šādi pasākumi: pārdošana, X pārskata drukāšana un Z pārskata drukāšana.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas fails atrodas **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** [Dynamics 365 Commerce risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijā. Faila mērķis ir iespējot iestatījumus dokumentu nodrošinātājam, ko konfigurē Commerce galvenajā mītnē. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar fiskālo printeri. Šis paplašinājums izmanto HTTP protokolu, lai iesniegtu dokumentus, kas CRT paplašinājums tiek ģenerēts fiskālajam printerim. Tas arī apstrādā atbildes, kas tiek saņemtas no fiskālā printera.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

**EpsonFP90IIISample** pieprasījumu apdarinātājs ir ieejas punkts pieprasījuma apstrādei finanšu perifērijas ierīcē.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – Šis pieprasījums nosūta dokumentus uz printeriem un atgriež atbildi no fiskālā printera.
- **IsReadyFiscalDeviceRequest** – Šis pieprasījums tiek izmantots ierīces veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – Šis pieprasījums tiek izmantots printera inicializēšanai.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja konfigurācijas fails atrodas **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** [Dynamics 365 Commerce risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijā. Faila mērķis ir iespējot savienotāja iestatījumus, kas jākonfigurē no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
