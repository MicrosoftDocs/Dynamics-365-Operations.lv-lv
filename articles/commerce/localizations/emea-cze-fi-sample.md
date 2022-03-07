---
title: Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Čehijai
description: Šajā tēmā ir sniegts pārskats par fiskālās integrācijas paraugu Čehijas Republikā Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 990de96f57f4a22b4d58da5f970b1b96f5fc21f5
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077094"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Čehijai

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par fiskālās integrācijas paraugu Čehijas Republikā Microsoft Dynamics 365 Commerce.

Lai izpildītu vietējās fiskālās prasības attiecībā uz kases aparātiem Čehijas Republikā,Dynamics 365 Commerce Čehijas Republikai paredzēta funkcionalitāte ietver tirdzniecības vietas (POS) integrācijas paraugu ar ārēju nodokļu reģistrācijas pakalpojumu. Paraugs paplašina [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md). Tas ir balstīts uz [EFR (elektroniskais fiskālais reģistrs)](https://efsta.org/sicherheitsloesungen/) risinājums no [EFSTA](https://efsta.org/) un nodrošina saziņu ar EFR pakalpojumu, izmantojot HTTPS protokolu. EFR pakalpojums nodrošina pārdošanas elektronisko reģistrāciju (EET - Elektronická bizonyíték tržeb), tas ir, pārdošanas datu tiešsaistes pārsūtīšanu uz nodokļu iestāžu fiskālo tīmekļa pakalpojumu.

EFR pakalpojumam jābūt mitinātam Commerce Hardware stacijā vai atsevišķā iekārtā, ar kuru var izveidot savienojumu no aparatūras stacijas. Paraugs tiek nodrošināts avota koda veidā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Microsoft neizlaiž nekādu aparatūru, programmatūru vai dokumentāciju no EFSTA. Lai iegūtu informāciju par to, kā iegūt EFR risinājumu un to izmantot, sazinieties ar [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Scenāriji

Čehijas Republikas fiskālās reģistrācijas pakalpojuma integrācijas paraugā ir ietverti šādi scenāriji.

- Skaidras naudas darījumu reģistrācija fiskālās reģistrācijas dienestā.

    - Nosūtiet detalizētus darījumu datus fiskālās reģistrācijas dienestam. Šie dati ietver informāciju par pārdošanas līniju, kā arī informāciju par atlaidēm, maksājumiem un nodokļiem. Tālāk fiskālās reģistrācijas dienests nosūta datus uz nodokļu administrācijas tīmekļa pakalpojumu un saņem no tā apstiprinājumu, kurā norādīts darījuma fiskālā identifikācijas kods.
    - Uzņemiet atbildi no fiskālās reģistrācijas pakalpojuma. Šajā atbildē ir iekļauti fiskālie dati, piemēram, fiskālās identifikācijas kods un darījuma drošības kods utt.
    - Izdrukājiet čekā reģistrēta darījuma fiskālos datus.

- Dāvanu karšu operāciju un klientu noguldījumu reģistrācija fiskālās reģistrācijas dienestā.

    - Izsniedziet dāvanu karti vai pievienojiet tai naudu.
    - Reģistrējiet depozītu klienta kontā.
    - Izveidojiet klienta pasūtījumu un reģistrējiet pasūtījuma depozītu.
    - Rediģēt klienta pasūtījumu un ignorēt pasūtījuma depozītu.
    - Atcelt klienta pasūtījumu un atmaksāt pasūtījuma depozītu.

- Kļūdu apstrāde, piemēram, tālāk norādītās opcijas.

    - Atkārtoti mēģiniet veikt fiskālo reģistrāciju, ja ir iespējams atkārtots mēģinājums, piemēram, ja fiskālās reģistrācijas pakalpojums nav pieejams, nav gatavs vai nereaģē.
    - Atlikt fiskālo reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darījumu kā reģistrētu un iekļaujiet informācijas kodus, lai fiksētu kļūmes iemeslu un papildu informāciju.
    - Pirms jauna pārdošanas darījuma atvēršanas vai pārdošanas darījuma pabeigšanas pārbaudiet fiskālās reģistrācijas pakalpojuma pieejamību.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālās reģistrācijas pakalpojuma integrācijas paraugā ir ieviesti šādi noteikumi, kas saistīti ar dāvanu kartēm.

- Pārdošanas līnijas, kas ir saistītas ar *Izsniegt dāvanu karti* vai *Pievienot dāvanu kartei* operācijas pārdošanas darījumā tiek atzīmētas ar īpašu atribūtu, kad darījums tiek reģistrēts fiskālās reģistrācijas dienestā.
- Dāvanu kartes maksājums tiek uzskatīts par parastu maksājumu un tiek atzīmēts ar īpašu atribūtu, kad darījums tiek reģistrēts fiskālās reģistrācijas dienestā.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Klientu kontu noguldījumi un klientu pasūtījumu noguldījumi

Fiskālās reģistrācijas pakalpojuma integrācijas paraugs ievieš šādus noteikumus, kas ir saistīti ar klienta konta depozītiem un klientu pasūtījumu depozītiem.

- Darījums, kas saistīts ar klienta konta depozītu vai klienta pasūtījuma depozītu, tiek reģistrēts fiskālās reģistrācijas dienestā kā vienas rindas darījums un tiek atzīmēts ar īpašu atribūtu. Šajā rindā ir norādīta depozīta PVN grupa.
- Kad tiek izveidots klienta hibrīdpasūtījums, tas ir, klienta pasūtījums, kurā ir preces, kuras klients var veikt no veikala, kā arī preces, kuras tiks izņemtas vai nosūtītas vēlāk, darījums tiek reģistrēts fiskālās reģistrācijas pakalpojumā. satur rindas produktiem, kas tiek veikti, kā arī rinda pasūtījuma depozītam.
- Maksājums no klienta konta tiek uzskatīts par parastu maksājumu un tiek atzīmēts ar īpašu atribūtu, kad darījums tiek reģistrēts fiskālās reģistrācijas dienestā.
- Klienta pasūtījuma depozīta summa, kas tiek piemērota klienta pasūtījumam *Pacelt* darbība tiek uzskatīta par regulāru maksājumu un tiek atzīmēta ar īpašu atribūtu, kad darījums tiek reģistrēts fiskālās reģistrācijas dienestā.

### <a name="offline-registration"></a>Reģistrācija bezsaistē

Ja fiskālās reģistrācijas pakalpojumam neizdodas pārsūtīt darījuma datus nodokļu iestāžu fiskālajam tīmekļa dienestam (piemēram, atbildes noildzes dēļ) un saņemt apstiprinājumu no tīmekļa pakalpojuma (tas ir, darījuma fiskālo identifikācijas kodu), tas ģenerē darījuma vietējo parakstu un iekļauj to un īpašu kļūdas kodu atbildē. Fiskālā reģistrācijas pakalpojums no jauna nosūta darījumus sākotnējā secībā fonā, tiklīdz tiek atjaunots tīkla savienojums.

### <a name="limitations-of-the-sample"></a>Izlases ierobežojumi

Fiskālās reģistrācijas pakalpojums atbalsta tikai scenārijus, kuros cenā ir iekļauts tirdzniecības nodoklis. Tāpēc, **Cenā iekļauts pārdošanas nodoklis** opcija ir jāiestata uz **Jā** gan veikaliem, gan klientiem.

## <a name="set-up-commerce-for-the-czech-republic"></a>Iestatiet Commerce Čehijas Republikai

Šajā sadaļā ir aprakstīti tirdzniecības iestatījumi, kas ir īpaši un ieteicami Čehijai. Papildinformāciju skatiet [Tirdzniecības mājas lapa](../index.md).

Lai izmantotu Čehijai raksturīgo funkcionalitāti, ir jānorāda šādi iestatījumi.

- Juridiskās personas primārajā adresē iestatiet **Valsts/reģions** lauks uz **CZE** (Čehu Republika).
- Katra veikala POS funkcionalitātes profilā, kas atrodas Čehijas Republikā, iestatiet **ISO kods** lauks uz **CZ** (Čehu Republika).

Čehijai ir jānorāda arī šādi iestatījumi. Ņemiet vērā, ka pēc iestatīšanas ir jāpalaiž atbilstoši izplatīšanas darbi.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Iestatiet PVN prasības atbilstoši Čehijas Republikas prasībām


Ir jāizveido PVN kodi, PVN grupas un krājumu PVN grupas. Ir arī jāiestata PVN informācija precēm un pakalpojumiem. Plašāku informāciju par PVN līdzekļu iestata un lietošanu skatiet [PVN pārskatā](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Iestatīt veikalus

**Lapā Visi veikali** atjauniniet veikala informāciju. Konkrēti, iestatiet tālāk norādītos parametrus.

- Laukā **PVN grupa** norādiet PVN grupu, kas jāizmanto pārdošanai noklusētajam debitoram.
- Iestatiet opciju **Cenas iekļaut PVN** uz **Jā**.
- Iestatiet **lauku Nosaukums** uz uzņēmuma nosaukumu. Šīs izmaiņas palīdz garantēt, ka uzņēmuma nosaukums ir redzams pārdošanas kvītī. Varat arī pievienot uzņēmuma nosaukumu pārdošanas kvīts izkārtojumam kā brīvas formas tekstu.
- Iestatiet **lauku Nodokļu identifikācijas numurs (NMIN)** uz uzņēmuma identifikācijas numuru. Šīs izmaiņas palīdz garantēt, ka uzņēmuma identifikācijas numurs tiek parādīts pārdošanas kvītī. Varat arī pievienot uzņēmuma identifikācijas numuru pārdošanas ieejas plūsmas izkārtojumam kā brīvas formas tekstu.

### <a name="set-up-functionality-profiles"></a>Iestatīt funkcionalitātes profilus

Iestatiet POS funkcionalitātes profilus.

- **Kopsavilkuma cilnē Saņemšanas pavadzīmes numerācija** iestatiet saņemšanas pavadzīmes numerēšanu, izveidojot vai atjauninot ierakstus **pārdošanas**, **pārdošanas pasūtījuma** un **atgriezto preču** saņemšanas darbību tipiem.

### <a name="set-up-registration-numbers"></a>Iestatiet reģistrācijas numurus

1. Iet uz **Organizācijas administrēšana \> Globālā adrešu grāmata \> Reģistrācijas veidi \> Reģistrācijas veidi**. Izveidojiet jaunu reģistrācijas veidu. Norādiet **Valsts/reģions** lauks uz **CZE** (Čehija) un noteikt to tikai organizācijai.
2. Iet uz **Organizācijas administrēšana \> Globālā adrešu grāmata \> Reģistrācijas veidi \> Reģistrācijas kategorijas**. Izveidojiet jaunu reģistrācijas kategoriju. Iepriekšējā darbībā atlasiet reģistrācijas veidu un iestatiet **Reģistrācijas kategorija** uz **Uzņēmuma telpas ID**.
3. Pārejiet uz sadaļu **Organizācijas administrēšana \> Organizācijas \> Pārvaldības struktūrvienības**. Katram veikalam, kas atrodas Čehijas Republikā, atlasiet ar veikalu saistīto vienību. Uz **Adrese** FastTab izvērsiet **Vairāk iespēju** nolaižamajā sarakstā un atlasiet **Papildu**. 
4. Atvērtajā **Pārvaldīt adreses** lapā jānorāda šāds iestatījums.

    - Uz **Adrese** FastTab iestatiet **Valsts/reģions** lauks uz **CZE**.
    - Uz **Reģistrācijas ID** FastTab izveido jaunu ierakstu. Izvēlieties iepriekš izveidoto reģistrācijas veidu un iestatiet reģistrācijas numuru.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotus laukus, lai tos varētu izmantot ieejas plūsmas formātos pārdošanas ieejas plūsmām

Var konfigurēt valodas tekstu un pielāgotos laukus, kas tiek izmantoti POS saņemšanas formātos. Tā lietotāja noklusējuma uzņēmumam, kurš izveido ieejas plūsmas iestatījumus, jābūt tai pašai juridiskajai personai, kurā tiek izveidots valodas teksta iestatījums. Alternatīvi, gan lietotāja noklusējuma uzņēmumā, gan veikala juridiskajā personā, kurai ir izveidots iestatījums, ir jāizveido vieni un tie paši valodas teksti.

**Lapā Teksts** valodā pievienojiet šādus ierakstus ieejas plūsmu izkārtojumu pielāgoto lauku etiķetēm. Ņemiet vērā, **ka** tabulā norādītās vērtības Valodas ID **, Teksta ID** un **Teksts** ir tikai piemēri. Jūs varat tos mainīt, lai tie atbilstu jūsu prasībām. Tomēr izmantotajām **teksta ID** vērtībām jābūt unikālām, un tām jābūt vienādām ar vai lielākām par 900001.

Pievienojiet tālāk norādītās POS etiķetes **POS** sadaļa **Valodas teksts** no tabulas:

| Valodas kods | Teksta ID | Teksts                   |
|-------------|---------|------------------------|
| en-US       | 900001  | ID provozovny/pokladny |
| en-US       | 900002  | BKP                    |
| en-US       | 900003  | PKP                    |
| en-US       | 900004  | FIK                    |
| en-US       | 900005  | Informācija                   |
| en-US       | 900006  | Sērijas numurs        |

**Lapā Pielāgotie lauki** pievienojiet šādus ierakstus pielāgotajiem laukiem saņemšanas shēmu izkārtojumiem. Pieraksti to **Parakstu teksta ID** vērtībām jāatbilst **Teksta ID** vērtības, kuras norādījāt **Valodas teksts** lappuse:

| Nosaukums                 | Veids    | Uzraksta teksta ID |
|----------------------|---------|-----------------|
| TLT                  | Saņemšana | 900001          |
| SEC                  | Saņemšana | 900002          |
| PARAKSTI                 | Saņemšana | 900003          |
| FISKĀLAIS               | Saņemšana | 900004          |
| INFORMĀCIJA                 | Saņemšana | 900005          |
| NEPĀRTRAUKTSNUMURS     | Saņemšana | 900006          |

> [!NOTE]
> Ir svarīgi norādīt pareizus pielāgoto lauku nosaukumus, kā norādīts iepriekšējā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs trūkstošus datus kvītīs.

### <a name="configure-receipt-formats"></a>Konfigurēt kvīšu formātus

Katram nepieciešamajam kvīts formātam mainiet vērtību **Drukas darbība** lauks uz **Vienmēr drukājiet**.

Saņemšanas formāta noformētājā atbilstošajām saņemšanas sadaļām pievienojiet šādus pielāgotus laukus. Ievērojiet, ka lauku nosaukumi atbilst iepriekšējā sadaļā definētajiem valodu tekstiem.

- **Galvene:** pievienojiet šādus laukus.

    - **Veikala nosaukums** un **nodokļu identifikācijas numurs**: šie lauki tiek izmantoti, lai drukātu uzņēmuma nosaukumu un identifikācijas numuru kvītīs. Alternatīvi, izkārtojumam varat pievienot uzņēmuma nosaukumu un identifikācijas numuru kā brīvas formas tekstu.
    - **Veikala adrese**, **datums**, **laiks 24H**, **Kvīts numurs** un **Reģistra numurs**.
    - **Kārtas numurs**: šis lauks identificē kases darbības numuru finanšu reģistrācijas pakalpojumā.

- **Rindas:** pievienojiet šādus laukus.

    - **Krājuma nosaukums**
    - **Daudz.**
    - **Kopējā cena ar nodokļiem**

- **Kājene:** pievienojiet šādus laukus.

    - Maksājumu lauki, lai tiktu izdrukātas katra maksājuma veida maksājuma summas. Piemēram, pievienojiet **laukus Norēķinu nosaukums** un **Norēķinu summa** vienai izkārtojuma rindai.
    - **ID provozovny/pokladny**: šajā laukā tiek drukāti uzņēmuma telpu un kases aparāta identifikatori.
    - **BKP**: šajā laukā tiek drukāts nodokļu maksātāja drošības kods, ko piešķir finanšu reģistrācijas pakalpojums.
    - **FIK**: šis lauks drukā tās darbības finanšu identifikācijas kodu, ko veiksmīgas tiešsaistes reģistrācijas gadījumā piešķir nodokļu iestāžu tīmekļa pakalpojums.
    - **PKP**: šis lauks izdrukā nodokļu maksātāja paraksta kodu, ko ģenerē finanšu reģistrācijas pakalpojums bezsaistes reģistrācijas gadījumā.
    - **Info**: šajā laukā tiek izdrukāta papildinformācija no finanšu reģistrācijas pakalpojuma.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, skatiet [set up and design receipt formats](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Iestatīt finanšu integrāciju Čehijai

Čehijas Republikas finanšu reģistrācijas pakalpojuma integrācijas izlase ir balstīta uz fiskālās [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **risinājumu\\ repozitorija mapē \\ srcFiscalIntegrationEfr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs laidienā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir Commerce izpildlaika paplašinājums (CRT), un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Izstrādātāja virtuālajā mašīnā (VM) ir jāizmanto iepriekšējā mazumtirdzniecības SDK versija Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Plašāku informāciju skatiet [Guidelines for the Fiscal Integration sample for the Czech Republic (legacy)](emea-cze-fi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

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
    1. Lejupielādējiet finanšu dokumentu nodrošinātāja konfigurācijas failu vietnē Configurations **DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml \> (piemēram,** laidiena fails/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)
    1. Lejupielādējiet fiskālā savienotāja konfigurācijas failu vietnē **Konfigurācijas \> Savienotāji \> SavienotājsEFRSample.xml** (piemēram, [izlaišanas fails/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas šādās mazumtirdzniecības SDK mapēs izstrādātāja VM LCS:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml
    > - **Fiskālā savienotāja konfigurācijas fails:** RetailSdk\\ Extensions paraugi\\ HardwareStation\\ Paplašinājums.EFRSample\\ Konfigurācija\\ SavienotājsEFRSample.xml
    > 
    > Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**. Cilnē **Vispārīgi** iestatiet opciju **Iespējot finanšu integrāciju** uz **Jā**.
1. Dodieties uz **Mazumtirdzniecības un tirdzniecības \> kanāla iestatījumu \> Finanšu integrācija \> Finanšu dokumentu nodrošinātāji** un ielādējiet iepriekš lejupielādēto finanšu dokumentu nodrošinātāja konfigurācijas failu.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connectors un ielādējiet iepriekš lejupielādēto finanšu savienotāja konfigurācijas** failu.
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector funkcionālie profili**. Izveidojiet jaunu savienotāja funkcionālo profilu. Atlasiet dokumentu nodrošinātāju un savienotāju, ko ielādējāt iepriekš. Pēc vajadzības atjauniniet [datu kartēšanas iestatījumus](#default-data-mapping).
1. Dodieties uz **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto finanšu savienotāju. Atjauniniet [savienotāja iestatījumi](#fiscal-connector-settings) kā prasīts.
1. Iet uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālo savienotāju grupas**. Izveidojiet jaunu fiskālo savienotāju grupu savienotāja funkcionālajam profilam, ko izveidojāt iepriekš.
1. Iet uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Fiskālā integrācija \> Fiskālās reģistrācijas procesi**. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālā reģistrācijas procesa darbību un atlasiet iepriekš izveidoto fiskālo savienotāju grupu.
1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Izvēlieties funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā jāaktivizē reģistrācijas process. Uz **Fiskālās reģistrācijas process** FastTab atlasiet fiskālās reģistrācijas procesu, ko izveidojāt iepriekš.
1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**. Atlasiet aparatūras profilu, kas ir saistīts ar aparatūras staciju, kurai tiks pievienots fiskālais printeris. Uz **Fiskālās perifērijas ierīces** FastTab atlasiet savienotāja tehnisko profilu, ko izveidojāt iepriekš.
1. Atveriet izplatīšanas grafiku (**Mazumtirdzniecība un tirdzniecība \> Mazumtirdzniecības un tirdzniecības IT \> Izplatīšanas grafiks**) un atlasiet darbus **1070** un **1090** lai pārsūtītu datus uz kanālu datu bāzi.

#### <a name="default-data-mapping"></a>Noklusējuma datu kartēšana

Fiskālā dokumenta nodrošinātāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga, ir iekļauta šāda noklusējuma datu kartēšana:

- **Pievienotās vērtības nodokļa (PVN) likmju kartēšana** – Tirdzniecības nodokļa kodiem iestatīto nodokļu procentu vērtību kartēšana ar vērtībām **NodoklisG** (nodokļu grupa) atribūts pieprasījumos, kas tiek nosūtīti fiskālajam dienestam. Šeit ir noklusējuma kartēšana:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Katra pāra pirmā sastāvdaļa ir PVN nodokļu grupa, kuru atbalsta EFR fiskālās reģistrācijas pakalpojums. Otrā sastāvdaļa atspoguļo atbilstošo PVN likmi. Plašāku informāciju par PVN nodokļu grupām, ko EFR atbalsta Čehijai, skatiet [EFR atsaucē](https://public.efsta.net/efr/).

- **Noklusējuma PVN grupas kartēšana** — visas PVN summas, kuras nevar kartēt uz kādu no iepriekš noteiktām PVN grupām, tiks attiecinātas uz noklusējuma (pamata) PVN grupu. Šeit ir noklusējuma kartēšana:

    ```
    A
    ```

- **Depozīta PVN grupu kartēšana** – klienta depozīta summas un klienta pasūtījuma depozīta summas tiks attiecinātas uz depozīta PVN grupu. Šeit ir noklusējuma kartēšana:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Fiskālā savienotāja iestatījumi

Tālāk norādītie iestatījumi ir iekļauti fiskālā savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga.

- **Galapunkta adrese** – Fiskālās reģistrācijas pakalpojuma URL.
- **Pārtraukums** — Laiks milisekundēs, cik ilgi fiskālais savienotājs gaidīs atbildi no fiskālās reģistrācijas pakalpojuma.

### <a name="configure-channel-components"></a>Konfigurējiet kanāla komponentus

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Plašāku informāciju skatiet [Guidelines for the Fiscal Integration sample for the Czech Republic (legacy)](emea-cze-fi-sample-sdk.md).
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
    1. Sāciet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet norādījumus [Fiskālās integrācijas parauga izveides konveijera iestatīšana](fiscal-integration-sample-build-pipeline.md) lai ģenerētu un atbrīvotu Cloud Scale Unit un pašapkalpošanās izvietojamās pakotnes fiskālās integrācijas paraugam. The **EFR build-pipeline.yml** veidnes YAML failu var atrast **Cauruļvads\\ YAML_Files** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve.

## <a name="design-of-extensions"></a>Paplašinājumu projektēšana

Čehijas Republikas finanšu reģistrācijas pakalpojuma integrācijas izlase ir balstīta uz fiskālās [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **risinājumu\\ repozitorija mapē \\ srcFiscalIntegrationEfr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs laidienā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir paplašinājums CRT, un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Plašāku informāciju skatiet [Guidelines for the Fiscal Integration sample for the Czech Republic (legacy)](emea-cze-fi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

### <a name="commerce-runtime-extension-design"></a>Tirdzniecības izpildlaika paplašinājuma dizains

Paplašinājuma, kas ir fiskālo dokumentu nodrošinātājs, mērķis ir ģenerēt pakalpojumam specifiskus dokumentus un apstrādāt atbildes no fiskālā reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

Dokumentu nodrošinātājam ir vienots **DocumentProviderEFRFiscalCZE** pieprasījumu apdarinātājs, kas tiek izmantots, lai ģenerētu finanšu dokumentus finanšu reģistrācijas pakalpojumam.

Šis apstrādātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus.

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē fiskālās reģistrācijas pakalpojumā.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Šis pieprasījums atgriež abonējamo notikumu sarakstu. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, klientu kontu noguldījumi un klientu pasūtījumu noguldījumi.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Šis pieprasījums atgriež atbildi no fiskālās reģistrācijas dienesta. Šī atbilde tiek serializēta, lai izveidotu virkni, lai tā būtu gatava saglabāšanai.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas fails atrodas risinājumu repozitorijā **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot fiskālo dokumentu nodrošinātāja iestatījumu konfigurēšanu no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar fiskālās reģistrācijas pakalpojumu. Aparatūras stacijas paplašinājums izmanto HTTP protokolu, lai iesniegtu dokumentus, ko CRT paplašinājums ģenerē finanšu reģistrācijas pakalpojumam. Tas arī apstrādā atbildes, kas tiek saņemtas no fiskālās reģistrācijas dienesta.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **EFRHandler** pieprasījumu apstrādātājs ir piekļuves punkts, lai apstrādātu pieprasījumus nodokļu reģistrācijas dienestam.

Apdarinātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus.

- **SubmitDocumentFiscalDeviceRequest** – Šis pieprasījums nosūta dokumentus fiskālās reģistrācijas dienestam un atgriež no tā atbildi.
- **IsReadyFiscalDeviceRequest** – Šis pieprasījums tiek izmantots fiskālās reģistrācijas dienesta veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – Šis pieprasījums tiek izmantots, lai inicializētu fiskālās reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Fiskālā savienotāja konfigurācijas fails atrodas vietnē **src\\ Fiskālā integrācija\\ Efr\\ Konfigurācijas\\ Savienotāji\\ SavienotājsEFRSample.xml** iekš [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) krātuve. Faila mērķis ir iespējot fiskālā savienotāja iestatījumu konfigurēšanu no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
