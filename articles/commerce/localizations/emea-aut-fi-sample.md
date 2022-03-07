---
title: Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Austrijai
description: Šajā tēmā ir sniegts pārskats par Austrijas fiskālās integrācijas paraugu Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: d720bffb98965bdc0276660d2a2e50d2bf155e74
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077169"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Austrijai

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par Austrijas fiskālās integrācijas paraugu Microsoft Dynamics 365 Commerce.

Lai izpildītu vietējās fiskālās prasības attiecībā uz kases aparātiem Austrijā,Dynamics 365 Retail Austrijas funkcionalitāte ietver tirdzniecības vietas (POS) integrācijas paraugu ar ārēju nodokļu reģistrācijas pakalpojumu. Paraugs paplašina [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md). Tas ir balstīts uz [EFR (elektroniskais fiskālais reģistrs)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) risinājums no [EFSTA](https://www.efsta.eu/at/) un nodrošina saziņu ar EFR pakalpojumu, izmantojot HTTPS protokolu. EFR pakalpojumam jābūt mitinātam mazumtirdzniecības aparatūras stacijā vai atsevišķā iekārtā, ar kuru var izveidot savienojumu no aparatūras stacijas. Paraugs tiek nodrošināts avota koda veidā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Microsoft neizlaiž nekādu aparatūru, programmatūru vai dokumentāciju no EFSTA. Lai iegūtu informāciju par to, kā iegūt EFR risinājumu un to izmantot, sazinieties ar [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Scenāriji

Austrijas fiskālās reģistrācijas pakalpojuma integrācijas paraugā ir ietverti šādi scenāriji.

- Skaidras naudas darījumu reģistrācija fiskālās reģistrācijas dienestā:

    - Nosūtiet detalizētus darījumu datus fiskālās reģistrācijas dienestam. Šie dati ietver informāciju par pārdošanas līniju, kā arī informāciju par atlaidēm, maksājumiem un nodokļiem.
    - Uzņemiet atbildi no fiskālās reģistrācijas pakalpojuma. Šajā atbildē ir iekļauts ciparparaksts un saite uz reģistrēto darījumu.
    - Reģistrējiet nodokļus un savienojiet tos ar nodokļu reģistrācijas dienesta nodokļu kodiem.
    - Uz kvīts izdrukājiet reģistrēta darījuma QR kodu.

- Dāvanu karšu operāciju un klientu noguldījumu kā bezskaidras naudas darījumu reģistrēšana fiskālās reģistrācijas pakalpojumā:

    - Izsniedziet dāvanu karti vai pievienojiet tai naudu.
    - Reģistrējiet depozītu klienta kontā.
    - Reģistrējiet klienta pasūtījuma depozītu.

- Ārpuspārdošanas darījumu un notikumu reģistrēšana kā bezskaidras naudas darījumi fiskālās reģistrācijas dienestā:

    - Atvērt maiņu un aizvērt maiņu
    - Sākuma summa, Float ierakstīšana un piedāvājuma noņemšana
    - Cenas ignorēšana
    - Nodokļa ignorēšana
    - Čeka kopijas drukāšana
    - Atvērt naudas kasti
    - X pārskata drukāšana
    - Drukāt Z pārskatu

- Dienas beigu izrakstu (X/Z pārskatu) drukāšana ar Austrijai raksturīgiem laukiem:

    - Kopējais klientiem piegādāto produktu vai pakalpojumu skaits
    - Pārdošanas sadalījums pēc nodokļu likmes
    - Maksājumu sadalījums pēc kasiera/kases aparāta operatora
    - Cenu atlaides un atgriešana, kas samazina ikdienas pārdošanas apjomu
    - Nulles izpārdošana (dāvanas)

- Kļūdu apstrāde, piemēram, šādas opcijas:

    - Atkārtoti mēģiniet veikt fiskālo reģistrāciju, ja ir iespējams atkārtots mēģinājums, piemēram, ja fiskālās reģistrācijas pakalpojums nav pieejams, nav gatavs vai nereaģē.
    - Atlikt fiskālo reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darījumu kā reģistrētu un iekļaujiet informācijas kodus, lai fiksētu kļūmes iemeslu un papildu informāciju.
    - Pirms jauna pārdošanas darījuma atvēršanas vai pārdošanas darījuma pabeigšanas pārbaudiet fiskālās reģistrācijas pakalpojuma pieejamību.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālās reģistrācijas pakalpojuma integrācijas paraugā ir ieviesti šādi noteikumi, kas saistīti ar dāvanu kartēm:

- Izslēdziet pārdošanas rindas, kas ir saistītas ar *Izsniegt dāvanu karti* un *Pievienot dāvanu kartei* operācijas no skaidras naudas darījuma. Tā vietā, lai reģistrētu šīs rindas kā skaidras naudas darījuma daļu, fiskālās reģistrācijas pakalpojumā reģistrējiet tās kā atsevišķu bezskaidras naudas darījumu.
- Nedrukājiet čekā nodokļu grupu sadalījumu un QR kodu, ja kvīts sastāv tikai no dāvanu kartes rindām.
- Izdrukājiet dāvanu karšu kopējo summu, kas tiek izsniegta vai atkārtoti iekasēta darījumā atsevišķi no skaidras naudas darījuma summas uz čeka.
- Saglabājiet aprēķinātās maksājumu rindu korekcijas kanālu datu bāzē ar atsauci uz atbilstošu fiskālo darījumu.
- Apmaksa ar dāvanu karti tiek uzskatīta par regulāru maksājumu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Klientu noguldījumi un klientu pasūtījumu noguldījumi

Fiskālās reģistrācijas pakalpojuma integrācijas paraugs ievieš šādus noteikumus, kas ir saistīti ar klientu noguldījumiem un klientu pasūtījumu noguldījumiem:

- Reģistrējiet bezskaidras naudas darījumu, ja darījums ir klienta depozīts.
- Reģistrēt bezskaidras naudas darījumu, ja darījums ietver tikai klienta pasūtījuma depozītu vai klienta pasūtījuma depozīta atmaksu.
- Kad tiek izveidots hibrīda klienta pasūtījums, atņemiet klienta pasūtījuma depozīta summu no maksājumu rindām.
- Saglabājiet aprēķinātās maksājumu rindu korekcijas kanālu datu bāzē ar atsauci uz fiskālo darījumu klienta hibrīda pasūtījumam.

### <a name="limitations-of-the-sample"></a>Izlases ierobežojumi

Fiskālās reģistrācijas pakalpojums atbalsta tikai scenārijus, kuros cenā ir iekļauts tirdzniecības nodoklis. Tāpēc, **Cenā iekļauts pārdošanas nodoklis** opcija ir jāiestata uz **Jā** gan veikaliem, gan klientiem.

## <a name="set-up-commerce-for-austria"></a>Iestatiet Commerce Austrijai

Šajā sadaļā ir aprakstīti tirdzniecības iestatījumi, kas ir īpaši un ieteicami Austrijai. Papildinformāciju par iestatīšanu skatiet sadaļā [Tirdzniecības mājas lapa](../index.md).

Lai izmantotu Austrijai raksturīgo funkcionalitāti, ir jānorāda šādi iestatījumi:

- Juridiskās personas primārajā adresē iestatiet **Valsts/reģions** lauks uz **AUT** (Austrija).
- Katra veikala POS funkcionalitātes profilā, kas atrodas Austrijā, iestatiet **ISO kods** lauks uz **AT** (Austrija).

Austrijai ir jānorāda arī šādi iestatījumi. Ņemiet vērā, ka pēc iestatīšanas ir jāpalaiž atbilstoši izplatīšanas darbi.

### <a name="set-up-vat-per-austrian-requirements"></a>Iestatiet PVN atbilstoši Austrijas prasībām

Ir jāizveido PVN kodi, PVN grupas un krājumu PVN grupas. Ir arī jāiestata PVN informācija precēm un pakalpojumiem. Plašāku informāciju par PVN līdzekļu iestata un lietošanu skatiet [PVN pārskatā](../../finance/general-ledger/indirect-taxes-overview.md).

Pārdošanas kvītīs var izdrukāt saīsinātu kodu PVN kodam (piemēram, "A" vai "B"). Lai šī funkcionalitāte būtu pieejama, iestatiet **Drukāt kodu** lauks uz **Pārdošanas nodokļa kodi** lappuse.

### <a name="set-up-stores"></a>Iestatīt veikalus

**Lapā Visi veikali** atjauniniet veikala informāciju. Konkrēti, iestatiet šādus parametrus:

- Laukā **PVN grupa** norādiet PVN grupu, kas jāizmanto pārdošanai noklusētajam debitoram.
- Iestatiet opciju **Cenas iekļaut PVN** uz **Jā**.
- Iestatiet **lauku Nosaukums** uz uzņēmuma nosaukumu. Šīs izmaiņas palīdz garantēt, ka uzņēmuma nosaukums ir redzams pārdošanas kvītī. Varat arī pievienot uzņēmuma nosaukumu pārdošanas kvīts izkārtojumam kā brīvas formas tekstu.
- Iestatiet **lauku Nodokļu identifikācijas numurs (NMIN)** uz uzņēmuma identifikācijas numuru. Šīs izmaiņas palīdz garantēt, ka uzņēmuma identifikācijas numurs tiek parādīts pārdošanas kvītī. Varat arī pievienot uzņēmuma identifikācijas numuru pārdošanas ieejas plūsmas izkārtojumam kā brīvas formas tekstu.

### <a name="set-up-functionality-profiles"></a>Iestatīt funkcionalitātes profilus

Iestatiet POS funkcionalitātes profilus:

- **Kopsavilkuma cilnē Saņemšanas pavadzīmes numerācija** iestatiet saņemšanas pavadzīmes numerēšanu, izveidojot vai atjauninot ierakstus **pārdošanas**, **pārdošanas pasūtījuma** un **atgriezto preču** saņemšanas darbību tipiem.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotus laukus, lai tos varētu izmantot ieejas plūsmas formātos pārdošanas ieejas plūsmām

Var konfigurēt valodas tekstu un pielāgotos laukus, kas tiek izmantoti POS saņemšanas formātos. Tā lietotāja noklusējuma uzņēmumam, kurš izveido ieejas plūsmas iestatījumus, jābūt tai pašai juridiskajai personai, kurā tiek izveidots valodas teksta iestatījums. Alternatīvi, gan lietotāja noklusējuma uzņēmumā, gan veikala juridiskajā personā, kurai ir izveidots iestatījums, ir jāizveido vieni un tie paši valodas teksti.

**Lapā Teksts** valodā pievienojiet šādus ierakstus ieejas plūsmu izkārtojumu pielāgoto lauku etiķetēm. Ņemiet vērā, **ka** tabulā norādītās vērtības Valodas ID **, Teksta ID** un **Teksts** ir tikai piemēri. Varat tos mainīt, lai tie atbilstu jūsu prasībām. Tomēr izmantotajām **teksta ID** vērtībām jābūt unikālām, un tām jābūt vienādām ar vai lielākām par 900001.

Pievienojiet tālāk norādītās POS etiķetes **POS** sadaļa **Valodas teksts** no tabulas:

| Valodas kods | Teksta ID | Teksts                      |
|-------------|---------|---------------------------|
| en-US       | 900001  | QR kods                   |
| en-US       | 900002  | Nepārtraukts numurs         |
| en-US       | 900003  | Nodokļu mazumtirdzniecības drukas kods     |
| en-US       | 900004  | Kopā (pārdošana)             |
| en-US       | 900005  | Kopējais nodoklis (pārdošana)         |
| en-US       | 900006  | Kopā iekļauts nodoklis (pārdošana) |
| en-US       | 900007  | Nodokļa summa (pārdošana)        |
| en-US       | 900008  | Nodokļa bāze (pārdošana)         |

**Lapā Pielāgotie lauki** pievienojiet šādus ierakstus pielāgotajiem laukiem saņemšanas shēmu izkārtojumiem. Pieraksti to **Parakstu teksta ID** vērtībām jāatbilst **Teksta ID** vērtības, kuras norādījāt **Valodas teksts** lappuse:

| Nosaukums                 | Veids    | Uzraksta teksta ID |
|----------------------|---------|-----------------|
| QRKODS               | Saņemšana | 900001          |
| NEPĀRTRAUKTSNUMURS     | Saņemšana | 900002          |
| MAZUMTIRDZNIECĪBAS PRINTKODS      | Saņemšana | 900003          |
| SALESTOTAL           | Saņemšana | 900004          |
| PĀRDOŠANAS NODOKLIS        | Saņemšana | 900005          |
| SALESTOTALINCLUDETAX | Saņemšana | 900006          |
| PĀRDOŠANAS SUMMA       | Saņemšana | 900007          |
| TIRDZNIECĪBAS BĀZE        | Saņemšana | 900008          |

> [!NOTE]
> Ir svarīgi norādīt pareizus pielāgoto lauku nosaukumus, kā norādīts iepriekšējā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs trūkstošus datus kvītīs.

### <a name="configure-receipt-formats"></a>Konfigurēt kvīšu formātus

Katram nepieciešamajam kvīts formātam mainiet vērtību **Drukas darbība** lauks uz **Vienmēr drukājiet**.

Saņemšanas formāta noformētājā atbilstošajām saņemšanas sadaļām pievienojiet šādus pielāgotus laukus. Ievērojiet, ka lauku nosaukumi atbilst iepriekšējā sadaļā definētajiem valodu tekstiem.

- **Galvene:** Pievienojiet šādus laukus:

    - **Veikala nosaukums** un **Nodokļu identifikācijas numurs** lauki, kurus izmanto, lai uz čekiem izdrukātu uzņēmuma nosaukumu un personas kodu. Alternatīvi, izkārtojumam varat pievienot uzņēmuma nosaukumu un identifikācijas numuru kā brīvas formas tekstu.
    - **Veikala adrese**, **Datums**, **Laiks 24H**, **Kvīts numurs** un **Reģistrēt numuru** laukus.
    - **Nepārtraukts numurs** laukus, lai identificētu skaidras naudas darījuma numuru fiskālās reģistrācijas pakalpojumā.

- **Rindas:** Pievienojiet šādus laukus:

    - **Priekšmeta nosaukums**.
    - **Daudzums**.
    - **Kopējā cena ar nodokli**.
    - **Nodokļu mazumtirdzniecības drukas kods**, ko izmanto, lai izdrukātu saīsināto kodu, kas atbilst tirdzniecības nodokļa kodam, kas attiecas uz preci.

- **Kājene:** pievienojiet šādus laukus:

    - Maksājumu lauki, lai tiktu izdrukātas katra maksājuma veida maksājuma summas. Piemēram, pievienojiet **laukus Norēķinu nosaukums** un **Norēķinu summa** vienai izkārtojuma rindai.
    - **Kopējais pārdošanas apjoms** lauku grupa:

        - **Kopā (pārdošana)** lauks, kas tiek izmantots, lai izdrukātu čeka kopējo skaidras naudas pārdošanas summu. Summā nav iekļauti nodokļi. Priekšapmaksa un dāvanu karšu operācijas nav iekļautas.
        - **Kopā iekļauts nodoklis (pārdošana)** lauks, kas tiek izmantots, lai izdrukātu čeka kopējo skaidras naudas pārdošanas summu. Summā iekļauts nodoklis. Priekšapmaksa un dāvanu karšu operācijas nav iekļautas.
        - **kopējais nodoklis (PVN),** kas tiek izmantots, lai drukātu kases pārdošanas ieejas plūsmas kopējo nodokļa summu. Priekšapmaksa un dāvanu karšu operācijas nav iekļautas.

    - **Nodokļu sadalīšanas** lauku grupa. Visi šīs lauku grupas lauki jādrukā vienā atsevišķā rindā.

        - **Lauks PVN ID**, kas ir standarta lauks, kas ļauj drukāt PVN kopsavilkumu katram PVN kodam. Lauks jāpievieno jaunai rindai.
        - **Lauks Nodokļa procenti**, kas ir standarta lauks, kuru izmanto, lai drukātu PVN koda efektīvo nodokļa likmi.
        - **lauks PVN bāze (pārdošana),** kas tiek izmantots, lai drukātu PVN koda kopējo kases pārdošanas summu. Priekšapmaksa un dāvanu karšu operācijas nav iekļautas.
        - **PVN summa (PVN)** summa, kas tiek izmantota, lai drukātu PVN koda kases pārdošanas ieejas nodokļa summu.
        - **Lauks Nodokļu mazumtirdzniecības drukas kods**, kas tiek izmantots, lai drukātu saīsināto kodu, kas atbilst PVN kodam.

    - **QR koda** lauks, ko izmanto, lai drukātu atsauci uz reģistrēto kases darbību QR koda veidā.

        > [!NOTE]
        > **QR koda** vērtība tiek izgūta no finanšu reģistra atbildes. EFR atgriež QR kodu savā atbildē tikai tad, ja efsta dokumentācijā ir aprakstīta EFR konfigurācijas lauka Atribūti **vērtība**. QR koda formātam **EFR konfigurācijas laukā Atribūti** jābūt iestatītam uz **BMP**.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, skatiet [set up and design receipt formats](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Iestatīt finanšu integrāciju Austrijai

Austrijas fiskālās reģistrācijas pakalpojuma integrācijas izlase ir balstīta uz fiskālās [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **risinājumu\\ repozitorija mapē \\ srcFiscalIntegrationEfr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs laidienā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir Commerce izpildlaika paplašinājums (CRT), un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Izstrādātāja virtuālajā mašīnā (VM) ir jāizmanto iepriekšējā mazumtirdzniecības SDK versija Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Plašāku informāciju skatiet [Guidelines for the Fiscal integration sample for Austria (legacy)](emea-aut-fi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

Izpildiet finanšu integrācijas iestatīšanas soļus, kā aprakstīts sadaļā [Iestatīt finanšu integrāciju Commerce kanāliem](setting-up-fiscal-integration-for-retail-channel.md):

1. [Iestatiet finanšu reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ņemiet vērā arī šīs finanšu reģistrācijas pakalpojuma integrācijas izlasei [raksturīgos](#set-up-the-registration-process) fiskālās reģistrācijas procesa iestatījumus.
1. [Iestatiet kļūdu apstrādes iestatījumus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iespējot atliktās finanšu reģistrācijas](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) manuālu izpildi.
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, veiciet šīs darbības, lai iestatītu Commerce headquarters. Plašāku informāciju skatiet [Set up the fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lejupielādēt finanšu dokumentu nodrošinātāja un finanšu savienotāja konfigurācijas failus:

    1. [Dynamics 365 Commerce Atveriet risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atlasiet pareizu laidiena filiāles versiju atbilstoši SDK/lietojumprogrammas versijai (piemēram, **[laidiens/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atveriet **src \> FiscalIntegration \> Efr**.
    1. Atveriet **konfigurāciju dokumentu datu failus \> un lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failus**: **DocumentProviderFiscalEFRSampleAustria.xml** un **DocumentProviderNonFiscalEFRSampleAustria.xml** (piemēram, [release failu atrašanās vieta/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)).
    1. Lejupielādējiet fiskālā savienotāja konfigurācijas failu vietnē **Konfigurācijas \> Savienotāji \> SavienotājsEFRSample.xml** (piemēram, [izlaišanas fails/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas šādās mazumtirdzniecības SDK mapēs izstrādātāja VM LCS:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas faili:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration
    > 
    > Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**. Cilnē **Vispārīgi** iestatiet opciju **Iespējot finanšu integrāciju** uz **Jā**.
1. Dodieties uz **Mazumtirdzniecības un tirdzniecības \> kanāla iestatījumu \> Finanšu integrācija \> Finanšu dokumentu nodrošinātāji** un ielādējiet iepriekš lejupielādētos finanšu dokumentu nodrošinātāja konfigurācijas failus.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connectors un ielādējiet iepriekš lejupielādēto finanšu savienotāja konfigurācijas** failu.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector funkcionālie profili**. Izveidojiet divus jaunus savienotāja funkcionālos profilus, pa vienam katram iepriekš ielādētajam finanšu dokumentu nodrošinātājam, un atlasiet iepriekš ielādēto finanšu savienotāju. Pēc vajadzības atjauniniet [datu kartēšanas iestatījumus](#default-data-mapping).
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto finanšu savienotāju. Atjauniniet [savienotāja iestatījumi](#fiscal-connector-settings) kā prasīts.
1. Iet uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālo savienotāju grupas**. Izveidojiet divas jaunas finanšu savienotāju grupas, pa vienai katram iepriekš izveidotajam savienotāja funkcionālajam profilam.
1. Iet uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālās reģistrācijas procesi**. Izveidojiet jaunu finanšu reģistrācijas procesu un divas finanšu reģistrācijas procesa darbības un atlasiet iepriekš izveidotās finanšu savienotāju grupas.
1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Izvēlieties funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā jāaktivizē reģistrācijas process. Uz **Fiskālās reģistrācijas process** FastTab atlasiet fiskālās reģistrācijas procesu, ko izveidojāt iepriekš. Lai iespējotu nefiskālu notikumu reģistrāciju POS, **kopsavilkuma cilnes Funkcijas** sadaļā **POS** iestatiet **opciju Audit (Audita** jā **·**).
1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**. Atlasiet aparatūras profilu, kas ir saistīts ar aparatūras staciju, kurai tiks pievienots fiskālais printeris. Uz **Fiskālās perifērijas ierīces** FastTab atlasiet savienotāja tehnisko profilu, ko izveidojāt iepriekš.
1. Atveriet izplatīšanas grafiku (**Mazumtirdzniecība un tirdzniecība \> Mazumtirdzniecības un tirdzniecības IT \> Izplatīšanas grafiks**) un atlasiet darbus **1070** un **1090** lai pārsūtītu datus uz kanālu datu bāzi.

#### <a name="default-data-mapping"></a>Noklusējuma datu kartēšana

Fiskālā dokumenta nodrošinātāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga, ir iekļauta šāda noklusējuma datu kartēšana:

- **Pievienotās vērtības nodokļa (PVN) likmju kartēšana** – Tirdzniecības nodokļa kodiem iestatīto nodokļu procentu vērtību kartēšana ar vērtībām **NodoklisG** (nodokļu grupa) atribūts pieprasījumos, kas tiek nosūtīti fiskālajam dienestam. Šeit ir noklusējuma kartēšana:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Katra pāra pirmā sastāvdaļa ir PVN nodokļu grupa, kuru atbalsta EFR fiskālās reģistrācijas pakalpojums. Otrā sastāvdaļa atspoguļo atbilstošo PVN likmi. Plašāku informāciju par PVN nodokļu grupām, ko EFR atbalsta Austrijai, skatiet [EFR atsaucē](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Fiskālā savienotāja iestatījumi

Tālāk norādītie iestatījumi ir iekļauti fiskālā savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga.

- **Galapunkta adrese** – Fiskālās reģistrācijas pakalpojuma URL.
- **Ierīces taimauts** — laiks milisekundēs, ko finanšu savienotājs gaidīs atbildi no finanšu reģistrācijas pakalpojuma.
- **Rādīt nodokļu reģistrācijas paziņojumus** – Šis karodziņš nosaka, vai operatoram ir jāparāda paziņojumi, ko nosūta nodokļu reģistrācijas pakalpojums.

### <a name="configure-channel-components"></a>Konfigurējiet kanāla komponentus

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Plašāku informāciju skatiet [Guidelines for the Fiscal integration sample for Austria (legacy)](emea-aut-fi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

#### <a name="set-up-the-development-environment"></a>Iestatiet izstrādes vidi

Lai iestatītu izstrādes vidi, lai pārbaudītu un paplašinātu paraugu, veiciet šīs darbības.

1. Klonējiet vai lejupielādējiet [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve. Atlasiet pareizo laidiena filiāles versiju atbilstoši savai SDK/lietojumprogrammas versijai. Papildinformāciju skatiet [Lejupielādējiet mazumtirdzniecības SDK paraugus un atsauces pakotnes no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet EFR risinājumu plkst **Dynamics365Commerce.Solutions\\ Fiskālā integrācija\\ Efr\\ EFR.sln**, un izveidojiet to.
1. Uzstādīt CRT paplašinājumi:

    1. Atrodi CRT paplašinājumu instalētājs:

        - **Tirdzniecības mēroga vienība:** Iekš **Efr\\ Mērvienība\\ ScaleUnit.EFR.Installer\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **ScaleUnit.EFR.Installer** uzstādītājs.
        - **Vietējais CRT Mūsdienu POS:** Iekš **Efr\\ Modern POS\\ ModernPOS.EFR.Instalētājs\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **ModernPOS.EFR.Instalētājs** uzstādītājs.

    1. Sāciet CRT paplašinājuma instalētājs no komandrindas:

        - **Tirdzniecības mēroga vienība:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Vietējais CRT Mūsdienu POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Instalējiet aparatūras stacijas paplašinājumus:

    1. Iekš **Efr\\ HardwareStation\\ HardwareStation.EFR.Installer\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **HardwareStation.EFR.Installer** uzstādītājs.
    1. Startējiet paplašinājuma instalētāju no komandrindas.

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet norādījumus [Fiskālās integrācijas parauga izveides konveijera iestatīšana](fiscal-integration-sample-build-pipeline.md) lai ģenerētu un atbrīvotu Cloud Scale Unit un pašapkalpošanās izvietojamās pakotnes fiskālās integrācijas paraugam. The **EFR build-pipeline.yml** veidnes YAML failu var atrast **Cauruļvads\\ YAML_Files** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve.

## <a name="design-of-extensions"></a>Paplašinājumu projektēšana

Austrijas fiskālās reģistrācijas pakalpojuma integrācijas izlase ir balstīta uz fiskālās [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **risinājumu\\ repozitorija mapē \\ srcFiscalIntegrationEfr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs laidienā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir paplašinājums CRT, un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Plašāku informāciju skatiet [Guidelines for the Fiscal integration sample for Austria (legacy)](emea-aut-fi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

### <a name="commerce-runtime-extension-design"></a>Tirdzniecības izpildlaika paplašinājuma dizains

Paplašinājuma, kas ir fiskālo dokumentu nodrošinātājs, mērķis ir ģenerēt pakalpojumam specifiskus dokumentus un apstrādāt atbildes no fiskālā reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

Dokumentu nodrošinātājiem ir divi pieprasījumu apstrādātāji:

- **DocumentProviderEFRFiscalAUT** – Šis apdarinātājs tiek izmantots, lai ģenerētu fiskālos dokumentus fiskālās reģistrācijas pakalpojumam.
- **DocumentProviderEFRNonFiscalAUT** – Šis apstrādātājs tiek izmantots, lai ģenerētu nefiskālos dokumentus nodokļu reģistrācijas pakalpojumam.

Šie apstrādātāji ir mantoti no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē fiskālās reģistrācijas pakalpojumā.
- **GetNonFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds nefiskālais dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē fiskālās reģistrācijas pakalpojumā.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Šis pieprasījums atgriež abonējamo notikumu sarakstu. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, X pārskata drukāšana, Z pārskata drukāšana, klientu konta depozīti, klientu pasūtījumu noguldījumi, audita pasākumi un ar pārdošanu nesaistīti darījumi.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Šis pieprasījums atgriež atbildi no fiskālās reģistrācijas dienesta. Šī atbilde tiek serializēta, lai izveidotu virkni, lai tā būtu gatava saglabāšanai.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas faili atrodas risinājumu repozitorija mapē **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** [Dynamics 365 Commerce:](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

- **DocumentProviderFiscalEFRSampleAustria** – finanšu dokumentu nodrošinātāja konfigurācijas fails finanšu dokumentiem.
- **DocumentProviderNonFiscalEFRSampleAustria** – finanšu dokumentu nodrošinātāja konfigurācijas fails nefiskāliem dokumentiem.

Šo failu mērķis ir iespējot finanšu dokumentu nodrošinātāja iestatījumu konfigurēšanu no Commerce headquarters. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar fiskālās reģistrācijas pakalpojumu. Aparatūras stacijas paplašinājums izmanto HTTP protokolu, lai iesniegtu dokumentus, ko CRT paplašinājums ģenerē finanšu reģistrācijas pakalpojumam. Tas arī apstrādā atbildes, kas tiek saņemtas no fiskālās reģistrācijas dienesta.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **EFRHandler** pieprasījumu apstrādātājs ir piekļuves punkts, lai apstrādātu pieprasījumus nodokļu reģistrācijas dienestam.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Finanšu savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – Šis pieprasījums nosūta dokumentus fiskālās reģistrācijas dienestam un atgriež no tā atbildi.
- **IsReadyFiscalDeviceRequest** – Šis pieprasījums tiek izmantots fiskālās reģistrācijas dienesta veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – Šis pieprasījums tiek izmantots, lai inicializētu fiskālās reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Fiskālā savienotāja konfigurācijas fails atrodas vietnē **src\\ Fiskālā integrācija\\ Efr\\ Konfigurācijas\\ Savienotāji\\ SavienotājsEFRSample.xml** iekš [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) krātuve. Faila mērķis ir iespējot fiskālā savienotāja iestatījumu konfigurēšanu no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
