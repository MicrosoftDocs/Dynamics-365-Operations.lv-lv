---
title: Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Austrijai
description: Šajā tēmā sniegts pārskats par Austrijas finanšu integrācijas paraugu Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: f03eab49f0abfc8a279ea43f69fa2ac0100bd34a
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7945043"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Austrijai

[!include[banner](../includes/banner.md)]

Šajā tēmā sniegts pārskats par Austrijas finanšu integrācijas paraugu Microsoft Dynamics 365 Commerce.

Lai nodrošinātu atbilstību austrijas kases reģistru lokālajām finanšu prasībām, Austrijas funkcionalitāte ietver pārdošanas punkta (POS) parauga integrāciju ar Dynamics 365 Retail ārēju finanšu reģistrācijas pakalpojumu. Paraugs paplašina finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md). Tas ir balstīts uz [EFR (Elektronisko finanšu reģistru)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) risinājumu no [EFSTA](https://www.efsta.eu/at/) un nodrošina sakarus ar EFR pakalpojumu, izmantojot HTTPS protokolu. EFR pakalpojums ir jā vieso Retail aparatūras stacijā vai atsevišķā datorā, kam var izveidot savienojumu no aparatūras stacijas. Paraugs ir nodrošināts avota koda formā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Korporācija Microsoft neizlaiž nevienu aparatūru, programmatūru vai dokumentāciju no EFSTA. Lai iegūtu informāciju par to, kā iegūt EFR risinājumu un to izmantot, sazinieties ar [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Scenāriji

Šos scenārijus iekļauj Austrijas finanšu reģistrācijas pakalpojumu integrācijas paraugs:

- Kases darbību reģistrācija finanšu reģistrācijas pakalpojumā:

    - Sūtiet detalizētus darbību datus finanšu reģistrācijas pakalpojumam. Šie dati ietver pārdošanas rindas informāciju un informāciju par atlaidēm, maksājumiem un nodokļiem.
    - Notvert finanšu reģistrācijas pakalpojuma atbildi. Šajā atbildē ir iekļauts ciparparaksts un saite uz reģistrēto darbību.
    - Reģistrējiet nodokļus un kartējiet tos uz finanšu reģistrācijas pakalpojuma nodokļu kodiem.
    - Drukājiet QR kodu reģistrētai darbībai kvītī.

- Dāvanu karšu operāciju un debitoru depozītu reģistrēšana finanšu reģistrācijas pakalpojumā kā bezskaidras naudas darbības:

    - Dāvanu kartei izsniegt vai pievienot naudu
    - Reģistrējiet debitora konta depozītu.
    - Reģistrējiet debitora pasūtījuma depozītu.

- Bezskaidras naudas darbību un notikumu reģistrēšana finanšu reģistrācijas pakalpojumā:

    - Atvērt maiņu un slēgt maiņu
    - Sākuma summa, mainīgā ievade un norēķinu noņemšana
    - Cenas ignorēšana
    - Nodokļa ignorēšana
    - Čeka kopijas drukāšana
    - Atvērt naudas kasti
    - X pārskata drukāšana
    - Drukāt Z pārskatu

- Drukājiet darba dienas beigu izrakstus (X/Z pārskatus), kuriem ir Austrijai raksturīgi lauki:

    - Kopējais preču vai pakalpojumu skaits, kas piegādāti debitoriem
    - PVN sadalījums pēc nodokļa likmes
    - Maksājumu sadalījums pēc kasiera/kases sistēmas operatora
    - Cenu atlaides un ieņēmumi, kas samazina ikdienas pārdošanu
    - Nulles pārdošanas (pasūtījuma)

- Kļūdu apstrāde, piemēram, šādas opcijas:

    - Atkārtoti mēģināt veikt finanšu reģistrāciju, ja ir iespējams atkārtot mēģinājums, piemēram, ja finanšu reģistrācijas pakalpojums nav pieejams, nav gatavs vai nav atbildes.
    - Atlikt finanšu reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darbību kā reģistrētu un ietveriet infokodus, lai iegūtu kļūmes iemeslu un papildinformāciju.
    - Pārbaudiet fiskālo reģistrācijas pakalpojumu pieejamību pirms jaunas pārdošanas darbības atvēršanas vai pārdošanas darbības veikšanas.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālās reģistrācijas pakalpojuma integrācijas paraugs ievieš tālāk norādītos ar dāvanu kartēm saistītos nosacījumus:

- No kases darbības izslēdziet pārdošanas rindas, kuras ir saistītas ar dāvanu kartes izdošanu *un pievienot dāvanu karšu* *operācijām*. Tā vietā, lai reģistrētu šīs rindas kā daļu no skaidras naudas darbības, reģistrējiet tās kā atsevišķu bezskaidras naudas darbību finanšu reģistrācijas pakalpojumā.
- Nedrukāt nodokļu grupas sadalījumu un QR kodu kvītī, ja kvītī ir ietvertas tikai dāvanu kartes rindas.
- Izdrukājiet darbību izsniegto vai atkārtoti iekasēto dāvanu karšu kopsummu atsevišķi no kases darbības summas kvītī.
- Saglabāt aprēķinātos maksājumu rindu pielāgojumus kanāla datu bāzē ar atsauci uz atbilstošu finanšu darbību.
- Maksājums ar dāvanu karti tiek uzskatīts par regulāru maksājumu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Debitora depozīti un debitora pasūtījuma depozīti

Fiskālās reģistrācijas pakalpojuma integrācijas paraugs ievieš tālāk norādītos noteikumus, kas ir saistīti ar debitoru depozītiem un debitora pasūtījuma depozītiem:

- Reģistrējiet bezskaidras naudas darbību, ja darbība ir debitora depozīts.
- Reģistrējiet bezskaidras naudas darbību, ja darbība ietver tikai debitora pasūtījuma depozītu vai debitora pasūtījuma deponējumu atmaksu.
- Ieturēt debitora pasūtījuma depozīta summu no maksājuma rindām, kad ir izveidots debitora pasūtījums.
- Saglabāt aprēķinātos maksājumu rindu pielāgojumus kanāla datu bāzē, lai izveidotu atsauci uz debitora pasūtījuma finanšu darbību.

### <a name="limitations-of-the-sample"></a>Parauga ierobežojumi

Finanšu reģistrācijas pakalpojums atbalsta tikai scenārijus, kuros PVN ir iekļauts cenā. Tāpēc gan **veikaliem, gan debitoriem opcijai Cena iekļaut PVN** ir jābūt **iestatītai** uz Jā.

## <a name="set-up-commerce-for-austria"></a>Iestatiet Commerce Austrijai

Šajā sadaļā aprakstīti Commerce iestatījumi, kas ir specifiski Un ieteicami Austrijai. Papildinformāciju par iestatīto informāciju skatiet [Commerce mājas](../index.md) lapā.

Lai izmantotu Austrijas specifisko funkcionalitāti, ir jānorāda šādi iestatījumi:

- Juridiskas personas primārajā adresē iestatiet lauku **Valsts/reģions** uz **AUT** (Austrija).
- Katra Austrijā izvietotā veikala POS funkcionalitātes profilā iestatiet ISO koda lauku **uz** AT **·** (Austrija).

Austrijai ir jānorāda arī šādi iestatījumi. Ievērojiet, ka pēc iestatīšanas pabeigšanas ir jāveic atbilstoši sadales darbi.

### <a name="set-up-vat-per-austrian-requirements"></a>Pvn iestatīšana austriešu prasībām

Veidojiet PVN kodus, PVN grupas un krājumu PVN grupas. Ir jāiestata arī PVN informācija par produktiem un pakalpojumiem. Papildinformāciju par TO, kā iestatīt un izmantot PVN līdzekļus, skatiet [PVN](../../finance/general-ledger/indirect-taxes-overview.md) pārskatā.

Pārdošanas kvītīs var drukāt saīsinātu PVN koda kodu (piemēram, "A" vai "B"). Lai padarītu šo funkcionalitāti pieejamu, **iestatiet** drukas koda lauku **PVN kodu** lapā.

### <a name="set-up-stores"></a>Veikalu iestatīšana

Lapā **Visi veikali** atjauniniet veikala informāciju. Iestatiet arī šādus parametrus:

- Laukā **PVN grupa norādiet PVN** grupu, kas jāizmanto pārdošanai noklusējuma debitoram.
- Iestatiet opciju **Cenās PVN iekļaut** vērtību **Jā**.
- Uzņēmuma **nosaukumam** laukā iestatiet nosaukumu. Šīs izmaiņas palīdz nodrošināt to, ka uzņēmuma nosaukums tiek parādīts pārdošanas kvītī. Alternatīvi pārdošanas kvīts izkārtojumam var pievienot uzņēmuma nosaukumu kā brīvas formas tekstu.
- Iestatiet **nodokļa identifikācijas koda** (NIK) lauku uzņēmuma identifikācijas numuram. Šīs izmaiņas palīdz nodrošināt, ka uzņēmuma identifikācijas numurs tiek parādīts pārdošanas kvītī. Alternatīvi uzņēmuma identifikācijas numuru var pievienot pārdošanas kvīts izkārtojumam kā brīvas formas tekstu.

### <a name="set-up-functionality-profiles"></a>Funkcionalitātes profilu iestatīšana

Iestatiet POS funkcionalitātes profilus:

- Kopsavilkuma cilnē Kvīšu numerācija iestatiet kvīšu numerāciju, izveidojot vai atjauninot pārdošanas, pārdošanas pasūtījuma un atgriešanas **saņemšanas** darbību **tipu** **·** **ierakstus**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotos laukus, lai tos varētu izmantot pārdošanas ieejas plūsmu saņemšanas formātiem

Varat konfigurēt valodas tekstu un pielāgotos laukus, kas tiek izmantoti POS ieejas plūsmas formātos. Tā lietotāja noklusējuma uzņēmumam, kurš izveido saņemšanas iestatījumus, jābūt tai pašai juridiskajai personai, kurai tiek veidoti valodas teksta iestatījumi. Alternatīvi vienādi valodas teksti ir jāizveido gan lietotāja noklusējuma uzņēmumā, gan veikala juridiskajā personām, kam ir izveidots iestatījums.

Lapā **Valodas teksts** pievienojiet šādus ierakstus kvīts izkārtojumiem pielāgoto lauku etiķetēm. **Ievērojiet, ka tabulā** **parādītās valodas ID, teksta ID un teksta vērtības ir tikai** **piemēri**. Jūs varat mainīt tos tā, lai tie atbilstu jūsu prasībām. Taču jūsu izmantotajām teksta ID vērtībām ir jābūt unikālām un vienādām ar vai **lielākam** 900001.

Pievienojiet šādas POS iezīmes **tabulas POS** valodas teksta **sadaļai**:

| Valodas kods | Teksta ID | Teksts                      |
|-------------|---------|---------------------------|
| en-ASV       | 900001  | QR kods                   |
| en-ASV       | 900002  | Nepārtraukts numurs         |
| en-ASV       | 900003  | Nodokļu mazumtirdzniecības drukāšanas kods     |
| en-ASV       | 900004  | Kopā (pārdošana)             |
| en-ASV       | 900005  | Nodokļu kopsumma (pārdošana)         |
| en-ASV       | 900006  | Kopsumma, iekļaut nodokli (pārdošana) |
| en-ASV       | 900007  | Nodokļu summa (pārdošana)        |
| en-ASV       | 900008  | Nodokļu bāze (pārdošana)         |

Pielāgoto **lauku lapā pievienojiet šiem ierakstiem kvīts izkārtojumu** pielāgotajiem laukiem. **Ievērojiet, ka uzraksta teksta ID vērtībām ir jāatbilst teksta ID** **vērtībām**, kas norādītas **teksta lapā** Valoda:

| Nosaukums                 | Veids    | Uzraksta teksta ID |
|----------------------|---------|-----------------|
| QR KODS               | Saņemšana | 900001          |
| NEPĀRTRAUKTS NUMURS     | Saņemšana | 900002          |
| MAZUMTIRDZNIECĪBAS DRUKĀTS KODS      | Saņemšana | 900003          |
| SALESTOTAL (PĀRDOŠANAS PASŪTĪJUMS)           | Saņemšana | 900004          |
| SALERNOX        | Saņemšana | 900005          |
| SALESTOTALINCLUDETAX | Saņemšana | 900006          |
| SALESTAXAMOUNT<A2       | Saņemšana | 900007          |
| SALESTAXBASIS (PVN)        | Saņemšana | 900008          |

> [!NOTE]
> Ir svarīgi norādīt pareizos pielāgotos lauku nosaukumus, kā norādīts iepriekšējā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs ieejas plūsmās trūkstošo datu.

### <a name="configure-receipt-formats"></a>Konfigurēt ieejas plūsmas formātus

Katram nepieciešamajam kvīts formātam mainiet lauka **Drukāšanas režīms** vērtību uz **Vienmēr** drukāt.

Pievienojiet atbilstošajām saņemšanas sadaļām šādus pielāgotos laukus kvīts formāta veidotājā. Ievērojiet, ka lauku nosaukumi atbilst valodas tekstiem, kas definēti iepriekšējā sadaļā.

- **Virsraksts:** pievienojiet šādus laukus:

    - **Veikala nosaukuma** un **nodokļa identifikācijas koda lauki, kas tiek izmantoti, lai kvītīs drukātu** uzņēmuma nosaukumu un identitātes numuru. Pēc izvēles var arī pievienot uzņēmuma nosaukumu un identitātes numuru izkārtojumam kā brīvas formas tekstu.
    - **Veikala** adreses, **datuma**, **laika 24** h, **kvīts** numura un reģistra **numura** lauki.
    - **Nepārtrauktie** numura lauki, lai identificētu kases darbības numuru finanšu reģistrācijas pakalpojumā.

- **Rindas:** pievienojiet šādus laukus:

    - **Krājuma** nosaukums.
    - **Daudz.**
    - **Kopējā cena ar** nodokļiem.
    - **Nodokļu mazumtirdzniecības drukāšanas kods, kas tiek izmantots, lai izdrukātu saīsināto kodu, kas atbilst precei** piemērotajam PVN kodam.

- **Kājene:** pievienojiet šādus laukus:

    - Maksājuma lauki, tādējādi maksājuma summas katrai maksājuma metodei tiek izdrukātas. Piemēram, pievienojiet **laukus Norēķinu** nosaukums un Norēķinu summa vienai izkārtojuma **rindai**.
    - **Pārdošanas** kopsummas lauku grupa:

        - **Kopējais (pārdošanas)** lauks, kas tiek izmantots, lai drukātu kvīts kopējo skaidras naudas pārdošanas summu. Summa neietver nodokli. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.
        - **Kopējais lauks Iekļaut nodokli** (pārdošanas), kas tiek izmantots, lai drukātu kvīts kopējo kases pārdošanas summu. Summa ietver nodokļus. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.
        - **Kopējais pvn** (pārdošanas) lauks, kas tiek izmantots, lai drukātu ieņēmumu kopējo nodokļu summu par pārdošanu skaidrā naudā. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.

    - **Nodokļu pārtraukumu** lauku grupa. Visi šīs grupas lauki jādrukā uz vienas atsevišķas rindas.

        - **Nodokļa ID lauks, kas ir standarta lauks, kas ļauj drukāt PVN kopsavilkumu** katram PVN kodam. Lauks jāpievieno jaunai rindai.
        - **Lauks** Nodokļa procenti, kas ir standarta lauks, ko lieto, lai drukātu PVN koda efektīvo nodokļu likmi.
        - **Nodokļu bāzes (pārdošanas) lauks, kuru izmanto, lai drukātu saņemšanas kopējo skaidras naudas pārdošanas summu** PVN kodam. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.
        - **Pvn summas (pārdošanas) lauks, kas tiek lietots, lai drukātu kvīts nodokļu summu par pārdošanu skaidrā naudā** PVN kodam.
        - **Lauks Nodokļu mazumtirdzniecības drukāšanas kods, kas tiek izmantots, lai** izdrukātu saīsināto kodu, kas atbilst PVN kodam.

    - **QR koda** lauks, ko lieto, lai drukātu atsauci uz reģistrēto kases darbību QR koda formā.

        > [!NOTE]
        > **QR koda** vērtība tiek izgūta no finanšu reģistra atbildes. EFR atgriež QR kodu tā atbildē tikai tad, ja atribūtu lauka vērtība EFR konfigurācijā **ir** aprakstīta EFSTA dokumentācijā. QR koda formāts Atribūtu **laukā EFR konfigurācijā** jāiestata uz **BMP**.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, [skatiet sadaļā Kvīšu formātu iestatīšana un](../receipt-templates-printing.md) noformēšana.

## <a name="set-up-fiscal-integration-for-austria"></a>Iestatīt Fiskālo integrāciju Austrijai

Fiskālo reģistrācijas pakalpojumu integrācijas paraugs Austrijai ir balstīts uz [fiskālās integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no Retail SDK. Paraugs atrodas Solutions repository mapē **src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Paraugs sastāv no fiskālā dokumenta nodrošinātāja, kas ir Commerce Runtime () paplašinājums () un finanšu savienotājs, kas ir [Commerce](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) Hardware Station CRT paplašinājums. Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātāja virtuālajā datorā (VM) pakalpojumos Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet Austrijas finanšu integrācijas parauga [izvietošanas vadlīnijās (mantojuma).](emea-aut-fi-sample-sdk.md) Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

Izpildiet finanšu integrācijas iestatīšanas soļus, kā [aprakstīts Commerce kanālu finanšu integrācijas iestatīšanai:](setting-up-fiscal-integration-for-retail-channel.md)

1. [Iestatīt finanšu reģistrācijas](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) procesu. Atzīmējiet arī fiskālās reģistrācijas procesa iestatījumus, kas ir [raksturīgi šim fiskālās reģistrācijas pakalpojuma integrācijas](#set-up-the-registration-process) paraugam.
1. [Iestatīt kļūdu apstrādes](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) iestatījumus.
1. [Aktivizējiet atliktās finanšu reģistrācijas manuālu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) izpildi.
1. [Konfigurējiet kanāla](#configure-channel-components) komponentus.

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, izpildiet šīs darbības, lai iestatītu programmu Commerce Headquarters. Papildinformāciju skatiet [sadaļā Komercijas kanālu finanšu integrācijas](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) iestatīšana.

1. Lejupielādēt konfigurācijas failus finanšu dokumentu nodrošinātājam un finanšu savienotājam:

    1. Atveriet risinājumu [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atlasiet pareizu versijas izlaidi atbilstoši SDK/programmas versijai (piemēram, **[izlaidums/9,33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**
    1. Atvērt **src \> FiscalIntegration \>** efr.
    1. Atveriet konfigurācijas DocumentProviders un lejupielādējiet finanšu dokumenta nodrošinātāja konfigurācijas **\>** failus: **DocumentProviderFiscalEFRSampleAustria.xml un** **DocumentProviderNonFiscalEFRSampleAustria.xml (piemēram, failu atrašanās vieta** laidienam/9,33). [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu **Konfigurācijas \> savienotājos \> ConnectorEFRSample.xml** (piemēram, fails [laidienam/9,33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)

    > [!WARNING]
    > Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas tālākmintās Retail SDK mapēs LCS izstrādātāja VM:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas faili:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extensions.DocumentProvider.EFRSample \\ konfigurācija
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ Extension.EFRSample \\ konfigurācija
    > 
    > Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**. Cilnē **Vispārīgi** iestatiet opciju Aktivizēt fiskālo integrāciju **kā** **Jā**.
1. Dodieties uz **Retail un Commerce Channel \> iestatīšanas finanšu integrācijas finanšu dokumentu nodrošinātājiem un \>\>** ielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failus, kas tika lejupielādēti iepriekš.
1. Dodieties uz **mazumtirdzniecības un commerce kanālu iestatīšanas finanšu integrācijas finanšu savienotājiem un \>\>\>** ielādējiet agrāk lejupielādēto fiskālā savienotāja konfigurācijas failu.
1. Pārejiet uz **Sadaļu Mazumtirdzniecības \> un Commerce Channel Setup Finanšu integrācijas \>\> savienotāja funkcionālie** profili. Izveidojiet divus jaunus savienotāja funkcionālos profilus – vienu katram agrāk ielādētam finanšu dokumentu nodrošinātājam un atlasiet iepriekš ielādēto finanšu savienotāju. Pēc vajadzības [atjauniniet datu](#default-data-mapping) kartēšanas iestatījumus.
1. Pārejiet uz **Retail un Commerce Channel setup Fiscal integration Connector \>\>\> tehniskajiem** profiliem. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto finanšu savienotāju. Pēc vajadzības [atjauniniet](#fiscal-connector-settings) savienotāja iestatījumus.
1. Pārejiet uz **sadaļu \> Mazumtirdzniecības un Commerce kanālu \> iestatīšanas finanšu integrācijas finanšu \> savienotāja** grupas. Izveidojiet divas jaunas finanšu savienotāja grupas – vienu katram iepriekš izveidotajā savienotāja funkcionālā profilam.
1. Pārejiet uz **mazumtirdzniecības un Commerce \> channel \> iestatīšanas finanšu integrācijas \> finanšu reģistrācijas** procesiem. Izveidojiet jaunu finanšu reģistrācijas procesu un divus fiskālās reģistrācijas procesa soļus un atlasiet iepriekš izveidotās finanšu savienotāja grupas.
1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Atlasiet funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā ir jāaktivizē reģistrācijas process. Kopsavilkuma **cilnē Finanšu reģistrācijas process** atlasiet iepriekš izveidoto finanšu reģistrācijas procesu. Lai iespējotu ar finanšu iestatījumiem nesaistīto notikumu reģistrēšanu POS, kopsavilkuma cilnes Funkcijas sadaļā POS **iestatiet** **·** **audita** opciju uz **Jā**.
1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**. Atlasiet aparatūras profilu, kas ir saistīts ar aparatūras staciju, ar kuru tiks pievienots fiskālais printeris. Kopsavilkuma cilnē **Finanšu** perifērijas ierīces atlasiet iepriekš izveidoto savienotāja tehnisko profilu.
1. Atveriet sadales grafiku (Mazumtirdzniecības un Commerce Retail un Commerce IT sadales grafiks) un atlasiet darbus **\>\>** **1070 un** **1090,** lai pārsūtītu datus uz kanāla datu bāzi.

#### <a name="default-data-mapping"></a>Noklusējuma datu kartēšana

Tālāk redzamais noklusējuma datu kartējums ir ietverts finanšu dokumenta nodrošinātāja konfigurācijā, kas ir nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Pievienotās vērtības nodokļa (PVN) likmju kartēšana - to nodokļu procentu vērtību kartēšana, kas iestatīti PVN kodiem, uz** **vērtībām TaxG (nodokļu grupa) atribūtu pieprasījumos, kas tiek sūtīti finanšu** pakalpojumiem. Šeit ir noklusējuma kartēšana:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Pirmais komponents katrā pārī norāda PVN nodokļu grupu, ko atbalsta EFR finanšu reģistrācijas pakalpojums. Otra sastāvdaļa norāda atbilstošo PVN likmi. Plašāku informāciju par PVN nodokļu grupām, ko EFR atbalsta Austrijai, skatiet [EFR](https://public.efsta.net/efr/) atsauci.

#### <a name="fiscal-connector-settings"></a>Finanšu savienotāja iestatījumi

Šādi iestatījumi ir iekļauti finanšu savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Galapunkta** adrese – finanšu reģistrācijas pakalpojuma URL.
- **Ierīces taimauts** – laiks milisekundēs, ko finanšu savienotājs gaidīs uz finanšu reģistrācijas pakalpojuma atbildi.
- **Rādīt finanšu reģistrācijas paziņojumus – šis karodziņš kontrolē, vai tiek rādīti fiskālās reģistrācijas** pakalpojuma atgriešanas paziņojumi operatoram.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Austrijas finanšu integrācijas parauga [izvietošanas vadlīnijās (mantojuma).](emea-aut-fi-sample-sdk.md)
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

#### <a name="set-up-the-development-environment"></a>Iestatīt izstrādes vidi

Lai iestatītu izstrādes vidi un paplašinātu paraugu ņemšanas, veiciet šādus soļus.

1. Lejupielādējiet Solutions [Dynamics 365 Commerce repozitoriju vai](https://github.com/microsoft/Dynamics365Commerce.Solutions) lejupielādējiet to. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai. Papildinformāciju skatiet lejupielādes [Retail SDK paraugos un atsauces pakotnēs no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet EFR risinājumu **dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ Efr EFR.sln** un izveidojiet to.
1. Instalēt CRT paplašinājumus:

    1. Atrast CRT paplašinājuma instalētāju:

        - **Commerce Scale Unit:** **mapē Efr \\ ScaleUnit \\ ScaleUnit.EFR.Installer \\ bin \\ Atkļūdošanas \\ net461 atrodiet mapi** **ScaleUnit.EFR.Installer** installer.
        - **Modern CRT POS lokāls:** **Efr \\ ModernPOS \\ ModernPOS.EFR.Installer bin atkļūdošanas net461 mapē atrodiet \\\\\\** **ModernPOS.EFR.Installer** instalētāju.

    1. Startējiet CRT paplašinājuma instalētāju no komandrindas:

        - **Commerce Scale vienība:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Lokāls CRT modernajā POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Instalēt aparatūras stacijas paplašinājumus:

    1. Mapē **Efr \\ HardwareStation \\ HardwareStation.EFR.Installer \\ bin \\\\ Atkļūdošana net461** atrodiet **HardwareStation.EFR.Installer** instalētāju.
    1. Startējiet paplašinājuma instalētāju no komandrindas.

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet darbības, kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos [iepakojumus](fiscal-integration-sample-build-pipeline.md) fiskālās integrācijas parauga iepakojumam. **EFR būvējuma pipeline.yml veidnesPOZITOML fails var tikt atrasts Risinājumu** **\\ repozitorija YAML_Files**[Dynamics 365 Commerce konveijera](https://github.com/microsoft/Dynamics365Commerce.Solutions) sarakstā.

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Fiskālo reģistrācijas pakalpojumu integrācijas paraugs Austrijai ir balstīts uz [fiskālās integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no Retail SDK. Paraugs atrodas Solutions repository mapē **src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) no fiskālā dokumenta nodrošinātāja, kas ir CRT Commerce Hardware Station paplašinājums un fiskālais savienotājs. Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Austrijas finanšu integrācijas parauga [izvietošanas vadlīnijās (mantojuma).](emea-aut-fi-sample-sdk.md) Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Paplašinājuma, kas ir fiskālā dokumenta nodrošinātājs, nolūks ir izveidot pakalpojumiem raksturīgus dokumentus un apstrādāt atbildes no fiskālās reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Dokumentu nodrošinātājiem ir divi pieprasījumu apdarinātāji:

- **DocumentProviderEFRFiscalAUT — šis apdarinātājs tiek izmantots, lai** ģenerētu finanšu dokumentus finanšu reģistrācijas pakalpojumam.
- **DocumentProviderEFRNonFiscalAUT — šis apdarinātājs tiek izmantots, lai finanšu reģistrācijas pakalpojumam ģenerētu dokumentus, kas** nav finanšu dokumenti.

Šie apdarinātāji ir pārmantoti no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest — šajā pieprasījumā ir ietverta** informācija par to, kurš dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē finanšu reģistrācijas pakalpojumā.
- **GetNonFiscalDocumentDocumentProviderRequest – šajā pieprasījumā ir ietverta informācija par to, kas ir jāģenerē ar fiskālo** dokumentu. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē finanšu reģistrācijas pakalpojumā.
- **GetSupportedRegistrableEventsDocumentProviderRequest - šis pieprasījums atgriež notikumu sarakstu,** uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana, Z pārskata drukāšana, debitoru kontu depozīti, debitoru pasūtījumu depozīti, audita notikumi un darbības, kas nav pārdošanas darbības.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest - šis pieprasījums atgriež atbildi** no finanšu reģistrācijas pakalpojuma. Šī atbilde ir serializēta, lai veidotu virkni tā, lai tā būtu gatava saglabāt.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas faili atrodas Risinājumu repozitorija mapē **src \\ FiscalIntegration \\ Efr \\ Configurations \\ DocumentProviders:**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

- **DocumentProviderFiscalEFRSampleAustria — finanšu dokumentu nodrošinātāja** konfigurācijas fails.
- **DocumentProviderNonFiscalEFRSampleAustria – finanšu dokumentu nodrošinātāja konfigurācijas fails,** kas nav finanšu dokumenti.

Šo failu mērķis ir iespējot finanšu dokumentu nodrošinātāja iestatījumus, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar finanšu reģistrācijas pakalpojumu. Aparatūras stacijas paplašinājums izmanto HTTP protokolu, lai iesniegtu CRT dokumentus, ko paplašinājums ģenerē finanšu reģistrācijas pakalpojumam. Tas apstrādā arī atbildes, kas saņemtas no fiskālās reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EFRHandler** pieprasījumu apdarinātājs ir ieejas punkts finanšu reģistrācijas pakalpojuma pieprasījumu apstrādei.

Apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Finanšu savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest – šis pieprasījums nosūta dokumentus finanšu reģistrācijas pakalpojumam un** atgriež atbildi no tā.
- **IsReadyFiscalDeviceRequest – šis pieprasījums tiek izmantots fiskālās reģistrācijas** pakalpojuma veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots, lai inicializētu finanšu reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja konfigurācijas fails atrodas **src \\ FiscalIntegration \\ Efr \\\\ Configurations Connectors \\ ConnectorEFRSample.xml** risinājumu [Dynamics 365 Commerce repozitorijā.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot finanšu savienotāja iestatījumus, kas jākonfigurē no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
