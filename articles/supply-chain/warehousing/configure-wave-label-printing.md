---
title: Iestatīt un lietot kopuma etiķešu drukāšanu
description: Šajā tēmā ir aprakstīta kopuma etiķešu drukāšana un paskaidrots, kā to iestatīt.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: a08f10c1f5c3ff5b9023f37614c4e113b3a6b30d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211770"
---
# <a name="set-up-and-use-wave-label-printing"></a>Iestatīt un lietot kopuma etiķešu drukāšanu

[!include [banner](../includes/banner.md)]

Kopuma etiķešu drukāšana piedāvā alternatīvu pieeju etiķešu drukāšanai, ieviešot jaunu kopuma darbības metodi, kas ļauj izveidot un drukāt etiķetes tieši no kopuma veidnes, kopuma izpildes laikā. Tāpēc etiķetes jau būs pieejamas, pirms darbinieki palaidīs darba pasūtījumu mobilajā ierīcē. Pēc tam darbinieki var pievienot nepieciešamās etiķetes izdošanas laikā, nevis pēc izdošanas.

Kopuma etiķešu drukāšana izmanto Zebra programmēšanas valodu (ZPL), lai izveidotu etiķešu izkārtojumus. Etiķetes izkārtojums ir sadalīts trīs sadaļās (galvene, pamatteksts un kājene), lai atļautu etiķetes ar atkārtotu struktūru. Kopuma etiķešu veidnes paziņo sistēmai, kuras etiķetes izkārtojums ir jāizmanto. Lietotāji var norādīt, kurš printeris tiek lietots. Pēc nepieciešamības etiķetes ir iespējams drukāt vairākos printeros vienlaicīgi. Lapa **Kopuma etiķešu vēsture** parāda ierakstus par visām etiķetēm, kas ir izveidotas, izmantojot šo iestatījumu.

Etiķetes var drukāt un salīdzināt, pamatojoties uz darba galvenēm, varat drukāt pārtraukuma etiķetes darba galvenei, kā arī varat drukāt konteinera satura etiķetes, gadījumu etiķetes un citas līdzīgas etiķetes.

> [!NOTE]
> Šī funkcionalitāte neaizstāj esošo etiķešu drukāšanas funkcionalitāti, kas ir balstīta uz dokumentu maršrutēšanu.

Kopuma etiķešu drukāšana piedāvā šādus uzlabojumus:

- Etiķešu drukāšana atbilstoši kastu skaitam vienā darba līnijā, neizmantojot konteinerizēšanu. (A “kaste” ir vienība, kas norādīta vienību secību grupas rindās.)
- Vairāku dažādu etiķešu secību drukāšana (piemēram, kastu un palešu etiķetes).
- Iekļaut etiķetes uzskaitījumu (piemēram, 1/124, 2/124,... 124/124) un definēt uzskaitījuma diapazonu (piemēram, darba rinda, kravas rinda vai nosūtīšana).
- Izveidot un drukāt preču transporta pavadzīmes ID etiķetēs, pirms preču transporta pavadzīme tiek ģenerēta.
- Katrai kastei izveidot unikālu seriālo pārvadāšanas konteinera kodu (SSCC) un iekļaut to katrā etiķetē.
- Izveidot GS1 atbilstošas numuru sērijas preču transporta pavadzīmju ID un SSCC.
- Atkārtoti drukājiet etiķetes no mobilajām ierīcēm un bagātinātā klienta.
- Etiķešu anulēšana (piemēram, īsajos izdošanas scenārijos) un atkārtota drukāšana.
- Notīriet kopuma etiķešu vēsturi.
- Dokumenta maršrutēšanas izkārtojumu uzlabojumi tiek koplietoti starp dokumentu maršrutēšanas izkārtojumiem un kopuma etiķešu izkārtojumiem. (Papildinformāciju skatiet sadaļā [Dokumenta maršrutēšanas izkārtojums numura zīmēm](../warehousing/document-routing-layout-for-license-plates.md).)

Šie uzlabojumi padara efektīvāku etiķešu pievienošanu kastēm pirms paletizācijas. Tas jo īpaši atvieglo uzņēmumus, kas nosūta sūtījumus lieliem mazumtirgotājiem, kuri, skenējot katru kasti atsevišķi, automātiski apstiprina pasūtījuma kvītis.

> [!NOTE]
> Varat ieviest šajā tēmā aprakstītos konfigurāciju scenārijus vai nu atsevišķi, vai kombinācijā, atkarībā no jūsu uzņēmuma prasībām. Varat izveidot vairākas kopuma etiķešu veidnes, kas darbojas secībā (kā parādīts 3. scenārijā). Piemēram, varat izmantot 1. scenāriju, lai izdrukātu kastu etiķetes un 2. scenāriju, lai izdrukātu palešu etiķetes (ja paletes krājumā atšķiras pēc lieluma un salikuma).

## <a name="turn-on-the-wave-label-printing-feature"></a>Ieslēgt līdzekli Kopuma etiķešu drukāšana

Lai varētu izmantot līdzekli *Kopuma etiķešu drukāšana*, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Kopuma etiķešu drukāšana*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>1. scenārijs: kopuma etiķešu drukāšana, ģenerējot viena kopuma etiķetes

Šajā scenārijā ir parādīts, kā uzņēmums var drukāt nosūtīšanas etiķetes lieliem mazumtirgotājiem, kuri, skenējot katru kasti atsevišķi, automātiski apstiprina pasūtījuma kvītis.

Šajā scenārijā tiek parādīti visi plūsmas posmi.

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Lai sekotu šim scenārijam, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa **USMF** juridiskā persona.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Pārliecinieties, vai kopuma etiķešu metode ir pieejama

Lai padarītu pieejamu kopuma etiķešu drukāšanas metodi, var būt nepieciešams atkārtoti ģenerēt kopuma procesa metodes.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.
1. Apstipriniet, ka **waveLabelPrinting** ir sarakstā. Ja tā nav, darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**, lai to pievienotu.

### <a name="configure-a-wave-template"></a>Konfigurēt kopuma veidni

Kopuma veidnes ļauj saistīt noteiktas kopuma metodes ar atbilstošo kopuma etiķešu veidni.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Atlasiet veidni, kā **62 Sūtījums pēc noklusējuma**.
1. Kopsavilkuma cilnē **Metodes** pārvietojiet metodi **Kopuma etiķešu drukāšana** uz kolonnu **Atlasītās metodes**.
1. Kolonnā **Atlasītās metodes** atlasiet metodi **Kopuma etiķešu drukāšana** un iestatiet tās lauku **Kopuma darbības kods** uz *PrintLabel*. Papildinformāciju par kopuma darbību kodiem skatiet sadaļā [Kopuma darbību kodi](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Izveidot kopuma etiķešu izkārtojumu

Etiķešu izkārtojums kontrolē, kāda informācija tiek drukāta uz etiķetes un kā tā ir izkārtota. Šeit ievadiet ZPL kodu, kas tiek nosūtīts uz printeri.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu izkārtojumi**.
1. Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Carton*
    - **Apraksts:** *kaste (SSCC)*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Kopuma etiķešu rindas iestatījumi**.

    Tiek parādīta lapa **Kopuma etiķešu rindas iestatījumi**. Šeit varat konfigurēt etiķetes dinamisko daļu.

1. Pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Rindas ID:** *WaveLabel*
    - **Rindas tabulas nosaukums:** *WHSWaveLabel*
    - **Rindas sākuma pozīcija:** *0*

        Šis lauks definē vertikālo pozīciju, kur rinda sāksies etiķetē.

    - **Rindas augstums:** *0*

        Šis lauks definē katras rindas augstumu (punktos) atbilstoši ZPL standartam. Rindas augstums ir pozitīvs horizontālajām etiķetēm un negatīvs vertikālajām etiķetēm. Tā kā šajā piemērā ir tikai viena rinda, varat iestatīt vērtību *0* (nulle).

    - **Rindu skaits lapā:** *1*

        Šis lauks definē rindu skaitu, ko var drukāt uz katras etiķetes.

        > [!NOTE]
        > Šis iestatījums radīs atsevišķu ZPL etiķeti, ko drukāt katram ierakstam kopuma etiķešu tabulā.

1. Aizvērt lapu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Darba veids*
    - **Kritēriji:** *Izdošana*

    Šis vaicājums nodrošina, ka etiķetē tiks drukātas tikai izdošanas veida darba rindas, nevis izvietošanas veida darba rindas.

1. Ja vēlaties varēt drukāt preču transporta pavadzīmes ID, cilnē **Savienojumi** atlasiet tabulu **Darba rindas** un pievienojiet tai tabulu **Sūtījumi**.
1. Aizveriet vaicājumu redaktora dialoglodziņu.
1. Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**. Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes kodu. Piemēram, ja lietojat Zebra printerus, varat izmantot šādu kodu.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes pamatteksts**, ievadiet vajadzīgā pamatteksta ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes kājene**, ievadiet vajadzīgās kājenes ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Šajā iestatījumā tiks drukāts viens katras etiķetes eksemplārs. Ja ir nepieciešamas vairākas kopijas (piemēram, viena kopija katrai paletes pusei), iestatiet **n** vērtību sekcijai **\^PQn** kājenē līdz nepieciešamajam kopiju skaitam. Piemēram, lai izdrukātu katras etiķetes četras kopijas, norādiet **\^PQ4**.

Tagad etiķete ir gatava lietošanai.

### <a name="create-a-wave-label-type"></a>Izveidot kopuma etiķešu veidu

Kopuma etiķešu veidi tiek izmantoti, lai saistītu kopuma etiķešu veidnes vienībai ar vienības secību grupas rindām.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidi**.
1. Pievienojiet kopuma etiķešu veidu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes veids:** *Carton*
    - **Apraksts:** *kaste*

### <a name="set-up-unit-sequence-groups"></a>Iestatīt vienību secību grupas

Pēc tam iestatiet vienības secību grupu kopuma etiķetes veidam.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Vienību secību grupas**.
1. Atlasiet grupu **Ea Box PL**.
1. Rindā **Kaste** iestatiet lauku **Kopuma līmeņa veids** uz *Kartons*.

### <a name="create-a-wave-label-template"></a>Izveidot kopuma etiķešu veidni

Pēc tam izveidojiet kopuma etiķešu veidni kopuma etiķetes veidam.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidnes**.
1. Pievienojiet kopuma līmeņa veidni un galvenē iestatiet šādas vērtības:

    - **Etiķetes veidnes nosaukums:** *Carton labels*
    - **Apraksts:** *Kastes etiķetes*
    - **Kopuma darbības kods:** *PrintLabel*
    - **Noliktava:** *62*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Kopuma etiķešu veids** uz *Kaste*.
1. Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** pievienojiet jaunu rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Carton*
    - **Printera nosaukums:** atlasiet atbilstošu ZPL printeri.
    - **Izpildīt vaicājumu:** *Jā* (Šis iestatījums nav obligāts, bet tas ir ieteicams optimālai veiktspējai.)

1. Darbību rūtī atlasiet **Saglabāt**.
1. Neobligāti: ja iestatāt debitoram raksturīgu etiķešu noformējumu, ir jāizveido vaicājums, lai atrastu debitora kontu. Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** atlasiet **Rediģēt vaicājumu**. Pēc tam, vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Sūtījumi*
    - **Atvasinātā tabula:** *Sūtījumi*
    - **Lauks:** *Konta numurs*
    - **Kritēriji:** ievadiet atbilstošo debitora konta numuru.

    Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.

1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktora dialoglodziņu visai etiķešu veidnei.
1. Vaicājumu redaktora dialoglodziņā, cilnē **Kārtošana** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Atsauces kravas rindas ID (Ieraksta ID)*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.
1. Ziņojuma lodziņš aicina apstiprināt grupēšanas atiestatīšanas darbību. Lai turpinātu, atlasiet **Jā**.
1. Darbību rūtī atlasiet **Kopuma etiķešu veidņu grupēšana**.
1. Dialoglodziņā **Kopuma etiķešu veidņu grupēšana** atlasiet rindu, kurā lauks **Atsauces lauka nosaukums** ir iestatīts uz *Atsauces kravas rindas ID*, un pēc tam atzīmējiet izvēles rūtiņu **Etiķešu kompilācijas ID** šai rindai.

    > [!NOTE]
    > Šis iestatījums izveidos vienu etiķetes secību (“carton 1 X”) kravas rindai visā kopumā, neņemot vērā darba grupēšanas iestatījumus. Šo etiķešu secību var drukāt uz etiķešu izkārtojuma.

### <a name="configure-number-sequence-extensions"></a>Konfigurēt numuru sērijas paplašinājumus

Numuru sērijas paplašinājumi kontrolē GS1 atbilstību noteiktām numuru sērijām. Šī konfigurācija nav obligāta pašreizējam scenārijam. Papildinformāciju un konfigurācijas norādījumus skatiet sadaļā [Konfigurēt numuru sērijas paplašinājumus](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Izveidot pārdošanas pasūtījumu un nodot to noliktavai

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.
1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *62*

1. Pievienojiet divus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - 1. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *A0001*
        - **Daudzums:** *9024*
        - **Vienība:** *katra* (9024 ea = 376 Box = 47 PL)

    - 2. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *A0002*
        - **Daudzums:** *9016*
        - **Vienība:** *katra* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > Šeit sniegtie krājumi un daudzumi ir tikai piemēri. Tie izmantos vienības secību grupu, ko definējāt iepriekš, tāpēc tiem ir jādefinē piemērota vienību pārveidošana no *ea* uz *Box* uz *PL* un krājumiem ir jābūt *62* noliktavā. Papildinformāciju skatiet sadaļā [Mērvienību un krājumu politikas](unit-measure-stocking-policies.md).

1. Atlasiet 1. pārdošanas pasūtījuma rindu. Pēc tam sadaļas **Pārdošanas pasūtījuma rinda** izvēlnē **Krājumi** atlasiet **Rezervācijas**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.
1. Atkārtojiet 4. un 5. soli pārdošanas pasūtījuma 2. rindai.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Notiek tālāk aprakstītie notikumi:

    - Sistēma apstrādā izveidoto sūtījumu, izmantojot veidni, kas ietver etiķetes drukāšanas darbību. Etiķetes izkārtojums tiks izmantots etiķetes formāta definēšanai un rezultāts būs etiķete, kas tiek drukāta uz printera, kas ir atlasīts etiķetes veidnē.
    - Kopuma etiķetes tiek ģenerētas un izdrukātas. Etiķešu skaits būs vienāds ar kastu skaitu (šajā piemērā 376 kastu etiķetes 1. rindai un 322 kastu etiķetes 2. rindai).
    - Sūtījumiem tiek ģenerēts jauns preču transporta pavadzīmes ID. Ja konfigurējāt numuru sērijas paplašinājumus, kopuma etiķešu ID sekos **SSCC-18** numura formātam. 

Varat skatīt un atkārtoti drukāt kopuma etiķetes no šādām lapām. Katras lapas darbību rūts cilnē **Sūtījumi** grupā **Saistītā informācija**, atlasiet **Kopuma etiķetes**.

- Visi sūtījumi \> Sūtījuma informācija
- Visas kravas \> Kravas informācija
- Visi kopumi
- Kopuma etiķetes
- Kopuma etiķešu vēsture

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>2. scenārijs: kopuma etiķešu drukāšana konteinerizēšanai (bez kopuma etiķešu ierakstiem)

Šis scenārijs ļauj drukāt kopuma etiķetes, lietojot konteinerizēšanu, automātiskai krājumu sadalīšanai kastēs un tādēļ nav nepieciešams kopuma etiķešu ieraksts. Šādā gadījumā konteinera ID darbojas kā SSCC vietturis.

Tālāk ir norādītas galvenās atšķirības starp šo scenāriju un 1. scenāriju:

- **Kopuma etiķešu veidnes:** jūs nevarēsit atlasīt kopuma etiķešu veidu kopuma etiķešu veidnei, un nevajadzēs etiķešu kompilācijas grupēšanu. Pretējā gadījumā tiks konfigurēta kopuma etiķešu veidne, kas tiks saistīta ar kopuma veidni tādā pašā veidā, kā aprakstīts 1. scenārijā. Lai nepieļautu kopuma etiķešu ģenerēšanu, kopuma etiķešu veids ir jāatstāj tukšs.
- **Kopuma etiķešu izkārtojumi:** konfigurējiet kopuma etiķešu izkārtojuma rindas iestatījumus darba rindām, nevis kopuma etiķešu ierakstiem. Etiķetes izkārtojumam ir jākonfigurē rindas iestatījums, izmantojot **WHSWorkLine** tabulu, nevis **WHSWaveLabel** tabulu. Iestatījums **Rindu skaits lapā** kontrolē rindu skaitu, kas būs pamatteksta sadaļā. 

Šī konfigurācija ir piemērota arī uzņēmējdarbības scenārijiem, kur vairāki dažādi krājumi ir iepakoti vienā atzīmētā kastē vai uz paletes, un šo iepakošanas procesu var definēt pēc darba izveides (piemēram, darbs, kas grupēts pēc sūtījuma).

Šajā scenārijā tiek parādīti visi plūsmas posmi.

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Lai sekotu šim scenārijam, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa **USMF** juridiskā persona.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Pārliecinieties, vai kopuma etiķešu metode ir pieejama

Lai padarītu pieejamu kopuma etiķešu drukāšanas metodi, var būt nepieciešams atkārtoti ģenerēt kopuma procesa metodes.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.
1. Apstipriniet, ka **waveLabelPrinting** ir sarakstā. Ja tā nav, darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**, lai to pievienotu.

### <a name="set-up-a-wave-template"></a>Iestatiet kopuma veidni

Kopuma veidnes ļauj saistīt noteiktas kopuma metodes ar atbilstošo kopuma etiķešu veidni.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Atlasiet veidni, kā **63 Konteinerizēšana**.
1. Kopsavilkuma cilnē **Metodes** pārvietojiet metodi **Kopuma etiķešu drukāšana** uz kolonnu **Atlasītās metodes**.
1. Kolonnā **Atlasītās metodes** atlasiet metodi **Kopuma etiķešu drukāšana** un iestatiet tās lauku **Kopuma darbības kods** uz *PrintLabel*. Papildinformāciju par kopuma darbību kodiem skatiet sadaļā [Kopuma darbību kodi](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Izveidot kopuma etiķešu izkārtojumu

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu izkārtojumi**.
1. Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Carton*
    - **Apraksts:** *kaste (SSCC)*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Kopuma etiķešu rindas iestatījumi**.

    Tiek parādīta lapa **Kopuma etiķešu rindas iestatījumi**. Šeit varat konfigurēt etiķetes dinamisko daļu.

1. Pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Rindas ID:** *WorkLine*
    - **Rindas tabulas nosaukums:** *WHSWorkLine*
    - **Rindas sākuma pozīcija:** *500*

        Šis lauks definē vertikālo pozīciju, kur rinda sāksies etiķetē.

    - **Rindas augstums:** *-50*

        Šis lauks definē katras rindas augstumu. Rindas augstums ir pozitīvs horizontālajām etiķetēm un negatīvs vertikālajām etiķetēm.

    - **Rindu skaits lapā:** *5*

        Šis lauks definē rindu skaitu, ko var drukāt uz katras etiķetes.

        > [!NOTE]
        > Šajā iestatījumā tiks drukātas vairākas ZPL etiķetes katram darbam, kur katra lapa var ietvert līdz piecām darba rindām. Piemēram, ja etiķete tiek drukāta konteineram ar 12 rindām, tiks izdrukātas trīs etiķetes. Ja vēlaties drukāt atsevišķu etiķeti katrai izdošanas rindai, iestatiet šo vērtību uz *1*.

1. Aizvērt lapu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Darba veids*
    - **Kritēriji:** *Izdošana*

1. Ja vēlaties varēt drukāt preču transporta pavadzīmes ID, cilnē **Savienojumi** atlasiet tabulu **Darba rindas** un pievienojiet tai tabulu **Sūtījumi**.
1. Aizveriet vaicājumu redaktora dialoglodziņu.
1. Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**. Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes kodu. Piemēram, ja lietojat Zebra printerus, varat izmantot šādu kodu.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes pamatteksts**, ievadiet vajadzīgā pamatteksta ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes kājene**, ievadiet vajadzīgās kājenes ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Šajā iestatījumā tiks drukāts viens katras etiķetes eksemplārs. Ja ir nepieciešamas vairākas kopijas (piemēram, viena kopija katrai paletes pusei), iestatiet **n** vērtību sekcijai **\^PQn** kājenē līdz nepieciešamajam kopiju skaitam. Piemēram, lai izdrukātu katras etiķetes četras kopijas, norādiet **\^PQ4**.

Tagad etiķete ir gatava lietošanai.

### <a name="create-a-wave-label-template"></a>Izveidot kopuma etiķešu veidni

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidnes**.
1. Pievienojiet kopuma līmeņa veidni un galvenē iestatiet šādas vērtības:

    - **Etiķetes veidnes nosaukums:** *Container labels*
    - **Apraksts:** *Konteineru etiķetes*
    - **Kopuma darbības kods:** *PrintLabel*
    - **Noliktava:** *63*

1. Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Container*
    - **Printera nosaukums:** atlasiet atbilstošu ZPL printeri.
    - **Izpildīt vaicājumu:** *Jā* (Šis iestatījums nav obligāts, bet tas ir ieteicams optimālai veiktspējai.)

1. Darbību rūtī atlasiet **Saglabāt**.
1. Neobligāti: ja iestatāt debitoram raksturīgu etiķešu noformējumu, ir jāizveido vaicājums, lai atrastu debitora kontu. Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** atlasiet **Rediģēt vaicājumu**. Pēc tam, vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Sūtījumi*
    - **Atvasinātā tabula:** *Sūtījumi*
    - **Lauks:** *Konta numurs*
    - **Kritēriji:** ievadiet atbilstošo debitora konta numuru.

    Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.

### <a name="configure-number-sequence-extensions"></a>Konfigurēt numuru sērijas paplašinājumus

Numuru sērijas paplašinājumi kontrolē GS1 atbilstību noteiktām numuru sērijām. Šī konfigurācija nav obligāta pašreizējam scenārijam. Papildinformāciju un konfigurācijas norādījumus skatiet sadaļā [Konfigurēt numuru sērijas paplašinājumus](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Izveidot pārdošanas pasūtījumu un nodot to noliktavai

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.
1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *63*

1. Pievienojiet piecas pārdošanas pasūtījuma rindas:

    - 1. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *A0001*
        - **Daudzums:** *10*

    - 2. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *A0002*
        - **Daudzums:** *20*

    - 3. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *L0006*
        - **Daudzums:** *20*

    - 4. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *L0100*
        - **Daudzums:** *40*

    - 5. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *L0101*
        - **Daudzums:** *50*

    > [!NOTE]
    > Šeit sniegtie krājumi un daudzumi ir tikai piemēri. Krājumiem ir jābūt norādītajā noliktavā.

1. Atlasiet 1. pārdošanas pasūtījuma rindu. Pēc tam sadaļas **Pārdošanas pasūtījuma rinda** izvēlnē **Krājumi** atlasiet **Rezervācijas**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.
1. Atkārtojiet 4. un 5. soli katrai papildu pārdošanas pasūtījuma rindai.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Notiek tālāk aprakstītie notikumi:

    - Sistēma apstrādā izveidoto sūtījumu, izmantojot veidni, kas ietver etiķetes drukāšanas darbību. Etiķetes izkārtojums tiks izmantots etiķetes formāta definēšanai un gala rezultāts būs etiķete ar piecām rindām un, kas tiek drukāta uz printera, kas ir atlasīts etiķetes veidnē.
    - Sūtījumiem tiek ģenerēts jauns preču transporta pavadzīmes ID. Ja konfigurējāt numuru sērijas paplašinājumus, kopuma etiķešu ID sekos **SSCC-18** numura formātam. 

Varat atkārtoti drukāt šīs kopuma etiķetes, dodoties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Kopuma etiķešu vēsture**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>3. scenārijs: kopuma etiķešu drukāšana vairākrindu etiķetēm

Šajā scenārijā ir parādīts, kā izmantot kopuma etiķešu drukāšanas funkcionalitāti, kad noliktavas procesos ir nepieciešamas vairākas nosūtīšanas etiķešu rindas. Piemēram, atsevišķas etiķetes ir jādrukā kastēm un paletēm, un var būt nepieciešams drukāt pārtraukuma etiķetes visam sūtījumam. Pārtraukuma etiķetes ir atsevišķs etiķešu veids, ko var izmantot kā dalītāju starp ruļļiem un konteineriem, piemēram, sūtījuma ID un svītrkoda etiķetes, lai etiķetes varētu viegli kārtot pēc to drukāšanas.

Galvenā atšķirība starp šī scenārija konfigurāciju un 1. scenārija konfigurāciju, papildus faktam, ka ir iespējotas pārtraukuma etiķetes, ir tā, ka vairāki kopuma etiķešu veidi ir jāsaista ar kopuma etiķešu veidnēm un vienību secību grupas rindām. Lai izpildītu šo konfigurāciju, šim scenārijam jāiestata šādi elementi:

- **Kopuma apstrādes metodes:** atzīmējiet kopuma etiķešu metodi kā “atkārtojamu”, pievienojiet to diviem (vai vairākiem) laikiem kopuma veidnē un iestatiet dažādus kopuma darbību kodus.
- **Kopuma etiķešu veidnes:** konfigurējiet kopuma etiķešu veidnes un saistiet tās ar kopuma veidnēm. Katrai kopuma etiķešu veidnei ir savs kopuma etiķetes veids.
- **Kopuma etiķešu izkārtojumi:** tiks izveidoti vairāki kopuma etiķešu izkārtojumi. Katrai etiķešu “rindai” būs atsevišķs etiķešu izkārtojums, kā arī pārtraukuma etiķešu izkārtojums.

Šajā scenārijā tiek parādīti visi plūsmas posmi.

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Lai sekotu šim scenārijam, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa **USMF** juridiskā persona.

### <a name="set-up-a-wave-process-method"></a>Kopuma apstrādes metodes iestatīšana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.
1. Apstipriniet, ka **waveLabelPrinting** ir sarakstā. Ja tā nav, darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**, lai to pievienotu.
1. Metodei **waveLabelPrinting** atzīmējiet izvēles rūtiņu **Metode atkārtojama**.

### <a name="set-up-a-wave-template"></a>Iestatiet kopuma veidni

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
2. Atlasiet veidni, kā **62 Sūtījums pēc noklusējuma**.
3. Kopsavilkuma cilnē **Metodes** pārvietojiet metodi **Kopuma etiķešu drukāšana** uz kolonnu **Atlasītās metodes**.
4. Kolonnā **Atlasītās metodes** piešķiriet **Kopuma darbības kods** vērtību, piemēram, *Kaste* metodei **Kopuma etiķešu drukāšana**. Papildinformāciju par kopuma darbību kodiem skatiet sadaļā [Kopuma darbību kodi](wave-step-codes.md).
5. Pārvietojiet metodi **Kopuma etiķešu drukāšana** uz kolonnu **Atlasītās metodes** otro reizi.
6. Kolonnā **Atlasītās metodes** piešķiriet citu **Kopuma darbības kods** vērtību, piemēram, *Palete* otrai **Kopuma etiķešu drukāšana** metodei. Papildinformāciju par kopuma darbību kodiem skatiet sadaļā [Kopuma darbību kodi](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Izveidot trīs kopuma etiķešu izkārtojumus

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu izkārtojumi**.
1. Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Carton*
    - **Apraksts:** *kaste (SSCC)*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Kopuma etiķešu rindas iestatījumi**.

    Tiek parādīta lapa **Kopuma etiķešu rindas iestatījumi**. Šeit varat konfigurēt etiķetes dinamisko daļu.

1. Pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Rindas ID:** *WaveLabel*
    - **Rindas tabulas nosaukums:** *WHSWaveLabel*
    - **Rindas sākuma pozīcija:** *0*

        Šis lauks definē vertikālo pozīciju, kur rinda sāksies etiķetē.

    - **Rindas augstums:** *0*

        Šis lauks definē katras rindas augstumu (punktos) atbilstoši ZPL standartam. Rindas augstums ir pozitīvs horizontālajām etiķetēm un negatīvs vertikālajām etiķetēm. Tā kā šajā piemērā ir tikai viena rinda, varat iestatīt vērtību *0* (nulle).

    - **Rindu skaits lapā:** *1*

        Šis lauks definē rindu skaitu, ko var drukāt uz katras etiķetes.

        > [!NOTE]
        > Šis iestatījums radīs atsevišķu ZPL etiķeti, ko drukāt katram ierakstam kopuma etiķešu tabulā.

1. Aizvērt lapu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Darba veids*
    - **Kritēriji:** *Izdošana*

    Šis vaicājums nodrošina, ka etiķetē tiks drukātas tikai izdošanas veida darba rindas, nevis izvietošanas veida darba rindas.

1. Ja vēlaties varēt drukāt preču transporta pavadzīmes ID, cilnē **Savienojumi** atlasiet tabulu **Darba rindas** un pievienojiet tai tabulu **Sūtījumi**. 
1. Aizveriet vaicājumu redaktora dialoglodziņu.
1. Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**. Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes kodu. Piemēram, ja lietojat Zebra printerus, varat izmantot šādu kodu.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes pamatteksts**, ievadiet vajadzīgā pamatteksta ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes kājene**, ievadiet vajadzīgās kājenes ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Šajā iestatījumā tiks drukāts viens katras etiķetes eksemplārs. Ja ir nepieciešamas vairākas kopijas (piemēram, viena kopija katrai paletes pusei), iestatiet **n** vērtību sekcijai **\^PQn** kājenē līdz nepieciešamajam kopiju skaitam. Piemēram, lai izdrukātu katras etiķetes četras kopijas, norādiet **\^PQ4**.

1. Pirmā etiķete tagad ir gatava lietošanai.
1. Izveidojiet otru izkārtojuma ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Pallet*
    - **Apraksts:** *Palete*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Kopuma etiķešu rindas iestatījumi**.

    Tiek parādīta lapa **Kopuma etiķešu rindas iestatījumi**. Šeit varat konfigurēt etiķetes dinamisko daļu.

1. Pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Rindas ID:** *WaveLabel*
    - **Rindas tabulas nosaukums:** *WHSWaveLabel*
    - **Rindas sākuma pozīcija:** *0*

        Šis lauks definē vertikālo pozīciju, kur rinda sāksies etiķetē.

    - **Rindas augstums:** *0*

        Šis lauks definē katras rindas augstumu (punktos) atbilstoši ZPL standartam. Rindas augstums ir pozitīvs horizontālajām etiķetēm un negatīvs vertikālajām etiķetēm. Tā kā šajā piemērā ir tikai viena rinda, varat iestatīt vērtību *0* (nulle).

    - **Rindu skaits lapā:** *1*

        Šis lauks definē rindu skaitu, ko var drukāt uz katras etiķetes.

        > [!NOTE]
        > Šis iestatījums rada atsevišķu ZPL etiķeti, ko drukāt katram ierakstam kopuma etiķešu tabulā.

1. Aizvērt lapu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Darba veids*
    - **Kritēriji:** *Izdošana*

    Šis vaicājums nodrošina, ka etiķetē tiks drukātas tikai izdošanas veida darba rindas, nevis izvietošanas veida darba rindas.

1. Ja vēlaties varēt drukāt preču transporta pavadzīmes ID, cilnē **Savienojumi** atlasiet tabulu **Darba rindas** un pievienojiet tai tabulu **Sūtījumi**.
1. Aizveriet vaicājumu redaktora dialoglodziņu.
1. Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**. Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes kodu. Piemēram, ja lietojat Zebra printerus, varat izmantot šādu kodu.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes pamatteksts**, ievadiet vajadzīgā pamatteksta ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes kājene**, ievadiet vajadzīgās kājenes ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Šajā iestatījumā tiks drukāts viens katras etiķetes eksemplārs. Ja ir nepieciešamas vairākas kopijas (piemēram, viena kopija katrai paletes pusei), iestatiet **n** vērtību sekcijai **\^PQn** kājenē līdz nepieciešamajam kopiju skaitam. Piemēram, lai izdrukātu katras etiķetes četras kopijas, norādiet **\^PQ4**.

1. Otrā etiķete tagad ir gatava lietošanai.
1. Izveidojiet trešo izkārtojuma ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Break*
    - **Apraksts:** *Pārtraukuma etiķete*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**. Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes ZPL kodu. Tālāk ir minēts piemērs.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Šoreiz pamatteksts nav nepieciešams. Tādēļ vienkārši ievadiet nepieciešamo tekstu sadaļā **Kājenes sadaļa**. Tālāk ir minēts piemērs.

    ```plaintext
    ^XZ
    ```

    Trešā etiķete tagad ir gatava lietošanai.

    > [!NOTE]
    > Trešā etiķete ir pārtraukuma etiķete, kas tiks izmantota kā dalītājs starp etiķešu ruļļiem.

### <a name="create-two-wave-label-types"></a>Izveidot divus kopuma etiķešu veidus

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidi**.
1. Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes veids:** *Carton*
    - **Apraksts:** *Kaste*

1. Izveidojiet otru ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes veids:** *Pallet*
    - **Apraksts:** *Palete*

### <a name="set-up-unit-sequence-groups"></a>Iestatīt vienību secību grupas

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Vienību secību grupas**.
1. Atlasiet vai izveidojiet **Ea Box PL** grupu.
1. Rindā **Kaste** iestatiet lauku **Kopuma līmeņa veids** uz *Kartons*.
1. Rindā **PL** iestatiet lauku **Kopuma līmeņa veids** uz *Palete*.

### <a name="create-wave-label-templates"></a>Izveidot kopuma etiķešu veidnes

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidnes**.
1. Izveidojiet etiķešu veidni, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes veidnes nosaukums:** *Carton labels*
    - **Apraksts:** *Kastu etiķetes*
    - **Kopuma darbības kods:** *Carton*
    - **Noliktava:** *62*

1. Kopsavilkuma cilnes **Vispārīgi** laukā **Kopuma etiķešu veids** atlasiet vērtību, piemēram, *Kaste*.
1. Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Carton*
    - **Printera nosaukums:** atlasiet atbilstošu ZPL printeri.
    - **Izpildīt vaicājumu:** *Jā* (Šis iestatījums nav obligāts, bet tas ir ieteicams optimālai veiktspējai.)

1. Darbību rūtī atlasiet **Saglabāt**.
1. Neobligāti: ja iestatāt debitoram raksturīgu etiķešu noformējumu, ir jāizveido vaicājums, lai atrastu debitora kontu. Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** atlasiet **Rediģēt vaicājumu**. Pēc tam, vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Sūtījumi*
    - **Atvasinātā tabula:** *Sūtījumi*
    - **Lauks:** *Konta numurs*
    - **Kritēriji:** ievadiet atbilstošo debitora konta numuru.

    Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.

1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktora dialoglodziņu visai etiķešu veidnei.
1. Vaicājumu redaktora dialoglodziņā, cilnē **Kārtošana** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Atsauces kravas rindas ID (Ieraksta ID)*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Pievienojiet otru rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Sūtījuma ID*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.
1. Ziņojuma lodziņš aicina apstiprināt grupēšanas atiestatīšanas darbību. Lai turpinātu, atlasiet **Jā**.
1. Darbību rūtī atlasiet **Kopuma etiķešu veidņu grupēšana**.
1. Dialoglodziņā **Kopuma etiķešu veidņu grupēšana** rindai, kur lauks **Atsauces lauka nosaukums** ir iestatīts uz *Sūtījuma ID*, iestatiet šādas vērtības:

    - **Drukāt pārtraukuma etiķetes:** atzīmējiet šo izvēles rūtiņu.
    - **Etiķetes izkārtojuma ID:** atlasiet pārtraukuma etiķeti. (Piemēram, atlasiet etiķešu izkārtojumu *Break*, ko izveidojāt iepriekš šajā scenārijā.)
    - **Printera nosaukums:** atlasiet printeri pārtraukuma etiķetēm. (Parasti, lai sadalītu etiķešu ruļļus, ir jāatlasa tas pats printeris, kas atlasīts kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija**. Tomēr ir iespējami arī citi scenāriji.)

1. Rindai, kuras lauks **Atsauces lauka nosaukums** ir iestatīts uz *Atsauces kravas rindas ID*, atzīmējiet izvēles rūtiņu **Etiķešu kompilācijas ID**.

    > [!NOTE]
    > Šis iestatījums izveidos vienu etiķetes secību (“carton 1 X”) kravas rindai visā kopumā, neņemot vērā darba grupēšanas iestatījumus. Šo etiķešu secību var drukāt uz etiķešu izkārtojuma. Turklāt atlasītās pārtraukuma etiķetes atdala dažādu sūtījumu etiķetes.

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Kopuma etiķešu veidņu grupēšana**.
1. Izveidojiet otru etiķešu veidni, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes veidnes nosaukums:** *Pallet labels*
    - **Apraksts:** *Palešu etiķetes*
    - **Kopuma darbības kods:** *Pallet*
    - **Noliktava:** *62*

1. Kopsavilkuma cilnes **Vispārīgi** laukā **Kopuma etiķešu veids** atlasiet vērtību, piemēram, *Palete*.
1. Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Etiķetes izkārtojuma ID:** *Pallet*
    - **Printera nosaukums:** atlasiet atbilstošu ZPL printeri.
    - **Izpildīt vaicājumu:** *Jā* (Šis iestatījums nav obligāts, bet tas ir ieteicams optimālai veiktspējai.)

1. Darbību rūtī atlasiet **Saglabāt**.
1. Neobligāti: ja iestatāt debitoram raksturīgu etiķešu noformējumu, ir jāizveido vaicājums, lai atrastu debitora kontu. Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** atlasiet **Rediģēt vaicājumu**. Pēc tam, vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Sūtījumi*
    - **Atvasinātā tabula:** *Sūtījumi*
    - **Lauks:** *Konta numurs*
    - **Kritēriji:** ievadiet atbilstošo debitora konta numuru.

    Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu. 

1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktora dialoglodziņu visai etiķešu veidnei.
1. Vaicājumu redaktora dialoglodziņā, cilnē **Kārtošana** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Atsauces kravas rindas ID (Ieraksta ID)*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Pievienojiet otru rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Sūtījuma ID*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.
1. Ziņojuma lodziņš aicina apstiprināt grupēšanas atiestatīšanas darbību. Lai turpinātu, atlasiet **Jā**.
1. Darbību rūtī atlasiet **Kopuma etiķešu veidņu grupēšana**.
1. Dialoglodziņā **Kopuma etiķešu veidņu grupēšana** rindai, kur lauks **Atsauces lauka nosaukums** ir iestatīts uz *Sūtījuma ID*, iestatiet šādas vērtības:

    - **Drukāt pārtraukuma etiķetes:** atzīmējiet šo izvēles rūtiņu.
    - **Etiķetes izkārtojuma ID:** atlasiet pārtraukuma etiķeti. (Piemēram, atlasiet etiķešu izkārtojumu *Break*, ko izveidojāt iepriekš šajā scenārijā.)
    - **Printera nosaukums:** atlasiet printeri pārtraukuma etiķetēm. (Parasti, lai sadalītu etiķešu ruļļus, ir jāatlasa tas pats printeris, kas atlasīts kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija**. Tomēr ir iespējami arī citi scenāriji.)

1. Rindai, kuras lauks **Atsauces lauka nosaukums** ir iestatīts uz *Atsauces kravas rindas ID*, atzīmējiet izvēles rūtiņu **Etiķešu kompilācijas ID**.

    > [!NOTE]
    > Šis iestatījums izveidos vienu etiķetes secību (“carton 1 X”) kravas rindai visā kopumā, neņemot vērā darba grupēšanas iestatījumus. Šo etiķešu secību var drukāt uz etiķešu izkārtojuma. Turklāt atlasītās pārtraukuma etiķetes atdala dažādu sūtījumu etiķetes.

### <a name="configure-number-sequence-extensions"></a>Konfigurēt numuru sērijas paplašinājumus

Numuru sērijas paplašinājumi kontrolē GS1 atbilstību noteiktām numuru sērijām. Šī konfigurācija nav obligāta pašreizējam scenārijam. Papildinformāciju un konfigurācijas norādījumus skatiet sadaļā [Konfigurēt numuru sērijas paplašinājumus](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Izveidot pārdošanas pasūtījumu un nodot to noliktavai

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.
1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *62*

1. Pievienojiet divas pārdošanas pasūtījuma rindas:

    - 1. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *A0001*
        - **Daudzums:** *9024*
        - **Vienība:** *katra* (9024 ea = 376 Box = 47 PL)

    - 2. pārdošanas pasūtījuma rinda:

        - **Krājuma numurs:** *A0002*
        - **Daudzums:** *9016*
        - **Vienība:** *katra* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > Šeit sniegtie krājumi un daudzumi ir tikai piemēri. Tie izmantos vienības secību grupu, ko definējāt iepriekš, tāpēc tiem ir jādefinē piemērota vienību pārveidošana no *ea* uz *Box* uz *PL* un krājumiem ir jābūt *62* noliktavā. Papildinformāciju skatiet sadaļā [Mērvienību un krājumu politikas](unit-measure-stocking-policies.md).

1. Atlasiet 1. pārdošanas pasūtījuma rindu. Pēc tam sadaļas **Pārdošanas pasūtījuma rinda** izvēlnē **Krājumi** atlasiet **Rezervācijas**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.
1. Atkārtojiet 4. un 5. soli pārdošanas pasūtījuma 2. rindai.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Notiek tālāk aprakstītie notikumi: 

    - Sistēma apstrādā izveidoto sūtījumu, izmantojot veidni, kas ietver etiķetes drukāšanas darbību. Etiķetes izkārtojums tiks izmantots etiķetes formāta definēšanai un rezultāts būs etiķete, kas tiek drukāta uz printera, kas ir atlasīts etiķetes veidnē.
    - Kopuma etiķetes tiek ģenerētas un izdrukātas. Etiķešu skaits būs vienāds ar kastu skaitu (šajā piemērā 376 kastu etiķetes 1. rindai un 322 kastu etiķetes 2. rindai, 47 PL etiķetes 1. rindai, 47 PL etiķetes 2. rindai un divas pārtraukuma etiķetes ar sūtījuma ID).
    - Sūtījumiem tiek ģenerēts jauns preču transporta pavadzīmes ID. Ja konfigurējāt numuru sērijas paplašinājumus, kopuma etiķešu ID sekos **SSCC-18** numura formātam. 

Varat skatīt un atkārtoti drukāt kopuma etiķetes no šādām lapām:

- Visi sūtījumi \> Sūtījuma informācija
- Visas kravas \> Kravas informācija
- Visi kopumi
- Kopuma etiķetes
- Kopuma etiķešu vēsture

Vairumam šo lapu varat atrast atbilstošo funkciju darbību rūts cilnē **Sūtījumi** grupā **Saistītā informācija**, atlasot **Kopuma etiķetes**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]