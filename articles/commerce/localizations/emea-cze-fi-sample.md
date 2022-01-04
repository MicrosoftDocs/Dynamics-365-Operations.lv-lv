---
title: Čehijas Republikas finanšu reģistrācijas pakalpojuma integrācijas paraugs
description: Šajā tēmā sniegts pārskats par čehijas Republikas finanšu integrācijas parauga apskatu Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 0a04ebb7685ff0b72207d9268b4aea980679572e
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944993"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Čehijas Republikas finanšu reģistrācijas pakalpojuma integrācijas paraugs

[!include[banner](../includes/banner.md)]

Šajā tēmā sniegts pārskats par čehijas Republikas finanšu integrācijas parauga apskatu Microsoft Dynamics 365 Commerce.

Lai atbilstu čehijas Republikas kases reģistru lokālajām finanšu prasībām, Čehijas Republikai paredzēts funkcionalitāte ietver pārdošanas punkta (POS) ar ārēju finanšu reģistrācijas pakalpojumu parauga Dynamics 365 Commerce integrāciju. Paraugs paplašina finanšu [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md). Tas ir balstīts uz [EFR (Elektronisko finanšu reģistru)](https://efsta.org/sicherheitsloesungen/) risinājumu no [EFSTA](https://efsta.org/) un nodrošina sakarus ar EFR pakalpojumu, izmantojot HTTPS protokolu. EFR pakalpojums nodrošina pārdošanas elektronisko reģistrāciju (RAIDĪŠANAS - Elektronicklf evidence tržeb), tas ir, pārdošanas datu tiešsaistes pārsūtīšanu uz nodokļu iestāžu finanšu tīmekļa pakalpojumu.

EFR pakalpojums ir jā vieso Commerce Aparatūras stacijā vai atsevišķā datorā, kam var izveidot savienojumu no aparatūras stacijas. Paraugs ir nodrošināts avota koda formā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Korporācija Microsoft neizlaiž nevienu aparatūru, programmatūru vai dokumentāciju no EFSTA. Lai iegūtu informāciju par to, kā iegūt EFR risinājumu un to izmantot, sazinieties ar [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Scenāriji

Šos scenārijus sedz Čehijas Republikas finanšu reģistrācijas pakalpojumu integrācijas paraugs.

- Kases darbību reģistrācija finanšu reģistrācijas pakalpojumā.

    - Sūtiet detalizētus darbību datus finanšu reģistrācijas pakalpojumam. Šie dati ietver pārdošanas rindas informāciju un informāciju par atlaidēm, maksājumiem un nodokļiem. Finanšu reģistrācijas pakalpojums tālāk nosūta datus nodokļu iestāžu tīmekļa pakalpojumam un saņem no tā apstiprinājumu, kas ietver darbības finanšu identifikācijas kodu.
    - Notvert finanšu reģistrācijas pakalpojuma atbildi. Šī atbilde ietver finanšu datus, piemēram, finanšu identifikācijas kodu un darbības drošības kodu, utt.
    - Drukājiet ieejas plūsmā reģistrētās darbības finanšu datus.

- Dāvanu karšu operāciju un debitoru depozītu reģistrēšana finanšu reģistrācijas pakalpojumā.

    - Dāvanu kartei izsniegt vai pievienot naudu
    - Reģistrējiet debitora konta depozītu.
    - Izveidojiet debitora pasūtījumu un reģistrējiet pasūtījuma depozītu.
    - Rediģējiet debitora pasūtījumu un ignorējot pasūtījuma depozītu.
    - Atceliet debitora pasūtījumu un atmaksājam depozītu par pasūtījumu.

- Kļūdu apstrāde, piemēram, šādas opcijas.

    - Atkārtoti mēģināt veikt finanšu reģistrāciju, ja ir iespējams atkārtot mēģinājums, piemēram, ja finanšu reģistrācijas pakalpojums nav pieejams, nav gatavs vai nav atbildes.
    - Atlikt finanšu reģistrāciju.
    - Izlaidiet fiskālo reģistrāciju vai atzīmējiet darbību kā reģistrētu un ietveriet infokodus, lai iegūtu kļūmes iemeslu un papildinformāciju.
    - Pārbaudiet fiskālo reģistrācijas pakalpojumu pieejamību pirms jaunas pārdošanas darbības atvēršanas vai pārdošanas darbības veikšanas.

### <a name="gift-cards"></a>Dāvanu kartes

Fiskālās reģistrācijas pakalpojuma integrācijas paraugs ievieš tālāk norādītos ar dāvanu kartēm saistītos noteikumus.

- Pārdošanas rindas, kas saistītas ar pārdošanas darbības dāvanu kartes izsniegšanas vai pievienošanas dāvanu kartes operācijām, tiek atzīmētas ar īpašu atribūtu, kad darbība ir reģistrēta *finanšu* reģistrācijas *pakalpojumā*.
- Maksājums ar dāvanu karti tiek uzskatīts par regulāru maksājumu un atzīmēts ar īpašu atribūtu, kad darbība ir reģistrēta finanšu reģistrācijas pakalpojumā.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Debitora kontu depozīti un debitora pasūtījuma depozīti

Fiskālās reģistrācijas pakalpojuma integrācijas paraugs ievieš tālāk norādītos noteikumus, kas ir saistīti ar debitora konta depozītiem un debitora pasūtījuma depozītiem.

- Darbība, kas ir saistīta ar debitora konta depozītu vai debitora pasūtījuma depozītu, ir reģistrēta finanšu reģistrācijas pakalpojumā kā viena rindas darbība un atzīmēta ar īpašu atribūtu. Šajā rindā ir norādīta depozīta PVN grupa.
- Kad izveidots pārpildīšanas debitora pasūtījums, tas ir, debitora pasūtījums, kurā ir preces, ko debitors var veikt veikalā, kā arī produkti, kas tiks izdoti vai nosūtīti vēlāk, finanšu reģistrācijas pakalpojumā reģistrētajās darbībās ir iekļautas preces, kas tiek veiktas, kā arī rinda pasūtījuma depozītam.
- Maksājums no debitora konta tiek uzskatīts par regulāru maksājumu un atzīmēts ar īpašu atribūtu, kad darbība ir reģistrēta finanšu reģistrācijas pakalpojumā.
- Debitora pasūtījuma depozīta summa, kas tiek piemērota debitora pasūtījuma saņemšanas operācijai, tiek uzskatīta par regulāru maksājumu un atzīmēta ar īpašu atribūtu, kad darbība ir reģistrēta *finanšu* reģistrācijas pakalpojumā.

### <a name="offline-registration"></a>Bezsaistes reģistrācija

Ja finanšu reģistrācijas pakalpojums nepārsūta darbības datus nodokļu iestāžu finanšu tīmekļa pakalpojumam (piemēram, atbildes taimauta dēļ) un saņem apstiprinājumu no tīmekļa pakalpojuma (t.i., darbības finanšu identifikācijas kods), tas ģenerē darbības lokālo parakstu un atbildē iekļauj to, kā arī īpašu kļūdas kodu. Finanšu reģistrācijas pakalpojums atkārtoti sajā kārtībā oriģināli sajā kārtībā ies pēc tīkla savienojuma atjaunošanas.

### <a name="limitations-of-the-sample"></a>Parauga ierobežojumi

Finanšu reģistrācijas pakalpojums atbalsta tikai scenārijus, kuros PVN ir iekļauts cenā. Tāpēc gan **veikaliem, gan debitoriem opcijai Cena iekļaut PVN** ir jābūt **iestatītai** uz Jā.

## <a name="set-up-commerce-for-the-czech-republic"></a>Iestatīt Commerce Čehijas Republikai

Šajā sadaļā aprakstīti Commerce iestatījumi, kas ir specifiski un ieteicami Čehijas Republikai. Papildinformāciju skatiet Commerce [mājas](../index.md) lapā.

Lai lietotu Čeka raksturīgo funkcionalitāti, ir jānorāda šādi iestatījumi.

- Juridiskas personas primārajā adresē iestatiet lauku **Valsts/reģions** uz **CZ** (Čehijas Republika).
- Katra čehijas Republikas veikala POS funkcionalitātes profilā iestatiet ISO koda lauku **uz** **CZ** (Čehijas Republika).

Čehijas Republikai ir jānorāda arī šādi iestatījumi. Ievērojiet, ka pēc iestatīšanas pabeigšanas ir jāveic atbilstoši sadales darbi.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Iestatīt PVN prasības Čehijas Republikai


Veidojiet PVN kodus, PVN grupas un krājumu PVN grupas. Ir jāiestata arī PVN informācija par produktiem un pakalpojumiem. Papildinformāciju par TO, kā iestatīt un izmantot PVN līdzekļus, skatiet [PVN](../../finance/general-ledger/indirect-taxes-overview.md) pārskatā.

### <a name="set-up-stores"></a>Veikalu iestatīšana

Lapā **Visi veikali** atjauniniet veikala informāciju. Iestatiet arī šādus parametrus.

- Laukā **PVN grupa norādiet PVN** grupu, kas jāizmanto pārdošanai noklusējuma debitoram.
- Iestatiet opciju **Cenās PVN iekļaut** vērtību **Jā**.
- Uzņēmuma **nosaukumam** laukā iestatiet nosaukumu. Šīs izmaiņas palīdz nodrošināt to, ka uzņēmuma nosaukums tiek parādīts pārdošanas kvītī. Alternatīvi pārdošanas kvīts izkārtojumam var pievienot uzņēmuma nosaukumu kā brīvas formas tekstu.
- Iestatiet **nodokļa identifikācijas koda** (NIK) lauku uzņēmuma identifikācijas numuram. Šīs izmaiņas palīdz nodrošināt, ka uzņēmuma identifikācijas numurs tiek parādīts pārdošanas kvītī. Alternatīvi uzņēmuma identifikācijas numuru var pievienot pārdošanas kvīts izkārtojumam kā brīvas formas tekstu.

### <a name="set-up-functionality-profiles"></a>Funkcionalitātes profilu iestatīšana

Iestatiet POS funkcionalitātes profilus.

- Kopsavilkuma cilnē Kvīšu numerācija iestatiet kvīšu numerāciju, izveidojot vai atjauninot pārdošanas, pārdošanas pasūtījuma un atgriešanas **saņemšanas** darbību **tipu** **·** **ierakstus**.

### <a name="set-up-registration-numbers"></a>Iestatīt reģistrācijas numurus

1. Dodieties uz **organizācijas \> administrēšanas globālās adrešu \> grāmatas reģistrācijas tipu reģistrācijas \>** tipiem. Izveidojiet jaunu reģistrācijas tipu. Norādiet lauku **Valsts/reģions** uz **BAG** (Čehijas Republika) un ierobežojiet to ar organizāciju.
2. Doties uz **organizācijas \> administrēšanas globālās adrešu \> grāmatas reģistrācijas tipu reģistrācijas \>** kategorijām. Izveidot jaunu reģistrācijas kategoriju. Atlasiet reģistrācijas tipu no iepriekšējā soļa un iestatiet reģistrācijas **kategoriju uz Biznesa telpu** **ID**.
3. Pārejiet uz sadaļu **Organizācijas administrēšana \> Organizācijas \> Pārvaldības struktūrvienības**. Katram veikalam, kas atrodas Čehijas Republikā, atlasiet ar veikalu saistīto vienību. Kopsavilkuma **cilnē** Adrese paplašiniet **nolaižamajā sarakstā Papildu opcijas un atlasiet** **Papildu**. 
4. Atvērtajā lapu **Pārvaldīt adreses jums ir jānorāda** sekojošos iestatījumus.

    - Kopsavilkuma **cilnē** Adrese iestatiet lauka **Valsts/reģions** vērtību **LATVIJĀ**.
    - Kopsavilkuma cilnē **Reģistrācijas ID** izveidojiet jaunu ierakstu. Atlasiet agrāk izveidoto reģistrācijas tipu un iestatiet reģistrācijas numuru.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotos laukus, lai tos varētu izmantot pārdošanas ieejas plūsmu saņemšanas formātiem

Varat konfigurēt valodas tekstu un pielāgotos laukus, kas tiek izmantoti POS ieejas plūsmas formātos. Tā lietotāja noklusējuma uzņēmumam, kurš izveido saņemšanas iestatījumus, jābūt tai pašai juridiskajai personai, kurai tiek veidoti valodas teksta iestatījumi. Alternatīvi vienādi valodas teksti ir jāizveido gan lietotāja noklusējuma uzņēmumā, gan veikala juridiskajā personām, kam ir izveidots iestatījums.

Lapā **Valodas teksts** pievienojiet šādus ierakstus kvīts izkārtojumiem pielāgoto lauku etiķetēm. **Ievērojiet, ka tabulā** **parādītās valodas ID, teksta ID un teksta vērtības ir tikai** **piemēri**. Jūs varat mainīt tos tā, lai tie atbilstu jūsu prasībām. Taču jūsu izmantotajām teksta ID vērtībām ir jābūt unikālām un vienādām ar vai **lielākam** 900001.

Pievienojiet šādas POS iezīmes **tabulas POS** valodas teksta **sadaļai**:

| Valodas kods | Teksta ID | Teksts                   |
|-------------|---------|------------------------|
| en-ASV       | 900001  | IDprovkcijas/pirkšanas dokuments |
| en-ASV       | 900002  | BKP (Datu bKP)                    |
| en-ASV       | 900003  | PkP (Pkp)                    |
| en-ASV       | 900004  | FIK (FIK)                    |
| en-ASV       | 900005  | Informācija                   |
| en-ASV       | 900006  | Sērijas numurs        |

Pielāgoto **lauku lapā pievienojiet šiem ierakstiem kvīts izkārtojumu** pielāgotajiem laukiem. **Ievērojiet, ka uzraksta teksta ID vērtībām ir jāatbilst teksta ID** **vērtībām**, kas norādītas **teksta lapā** Valoda:

| Nosaukums                 | Veids    | Uzraksta teksta ID |
|----------------------|---------|-----------------|
| TLT                  | Saņemšana | 900001          |
| SEC                  | Saņemšana | 900002          |
| PARAKSTĪT                 | Saņemšana | 900003          |
| FINANŠU               | Saņemšana | 900004          |
| INFO                 | Saņemšana | 900005          |
| NEPĀRTRAUKTS NUMURS     | Saņemšana | 900006          |

> [!NOTE]
> Ir svarīgi norādīt pareizos pielāgotos lauku nosaukumus, kā norādīts iepriekšējā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs ieejas plūsmās trūkstošo datu.

### <a name="configure-receipt-formats"></a>Konfigurēt ieejas plūsmas formātus

Katram nepieciešamajam kvīts formātam mainiet lauka **Drukāšanas režīms** vērtību uz **Vienmēr** drukāt.

Pievienojiet atbilstošajām saņemšanas sadaļām šādus pielāgotos laukus kvīts formāta veidotājā. Ievērojiet, ka lauku nosaukumi atbilst valodas tekstiem, kas definēti iepriekšējā sadaļā.

- **Virsraksts:** pievienojiet šādus laukus.

    - **Veikala nosaukums** un **nodokļa identifikācijas kods: šie lauki tiek izmantoti, lai kvītīs drukātu uzņēmuma** nosaukumu un identitātes numuru. Pēc izvēles var arī pievienot uzņēmuma nosaukumu un identitātes numuru izkārtojumam kā brīvas formas tekstu.
    - **Veikala** adrese, **datums**, **laiks 24** h, **kvīts** numurs un reģistra **numurs**.
    - **Sērijas** numurs: šis lauks norāda kases darbības numuru finanšu reģistrācijas pakalpojumā.

- **Rindas:** pievienojiet šādus laukus.

    - **Krājuma nosaukums**
    - **Daudz.**
    - **Kopējā cena ar nodokļiem**

- **Kājene:** pievienojiet šādus laukus.

    - Maksājuma lauki, tādējādi maksājuma summas katrai maksājuma metodei tiek izdrukātas. Piemēram, pievienojiet **laukus Norēķinu** nosaukums un Norēķinu summa vienai izkārtojuma **rindai**.
    - **IDprov pirkšanas/pirkšanas datu lauks tiek drukāts biznesa telpu un kases sistēmas** identifikatoros.
    - **BKP:** šis lauks drukā nodokļu maksātāja drošības kodu, ko piešķir finanšu reģistrācijas pakalpojums.
    - **FIK: šis lauks drukā finanšu identifikācijas kodu darbībai, kuru piešķir nodokļu iestādes tīmekļa pakalpojums** veiksmīgas tiešsaistes reģistrācijas gadījumā.
    - **PKP: šis lauks drukā nodokļu maksātāja paraksta kodu, ko izveido finanšu reģistrācijas** pakalpojums bezsaistes reģistrācijas gadījumā.
    - **Informācija:** šis lauks drukā papildinformāciju no finanšu reģistrācijas pakalpojuma.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, [skatiet sadaļā Kvīšu formātu iestatīšana un](../receipt-templates-printing.md) noformēšana.

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Iestatīt Čehijas Republikai fiskālo integrāciju

Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Čehijas Republikai ir balstīts uz [fiskālās integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no Retail SDK. Paraugs atrodas Solutions repository mapē **src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Paraugs sastāv no fiskālā dokumenta nodrošinātāja, kas ir Commerce Runtime () paplašinājums () un finanšu savienotājs, kas ir [Commerce](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) Hardware Station CRT paplašinājums. Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātāja virtuālajā datorā (VM) pakalpojumos Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet [Čehijas Republikas finanšu integrācijas parauga izvietošanas vadlīnijās (mantojuma)](emea-cze-fi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

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
    1. Lejupielādējiet finanšu dokumenta nodrošinātāja konfigurācijas failu **konfigurācijā \> DocumentProviders \> DocumentProviderFiscalEFRSampleKodēch.xml** (piemēram, fails laidienam/9,33). [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu **Konfigurācijas \> savienotājos \> ConnectorEFRSample.xml** (piemēram, fails [laidienam/9,33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)

    > [!WARNING]
    > Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas tālākmintās Retail SDK mapēs LCS izstrādātāja VM:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extensions.DocumentProvider.EFRSample \\ konfigurācijas \\ DocumentProviderFiscalEFRSampleRsch.xml
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ Extension.EFRSample \\ Konfigurācijas \\ ConnectorEFRSample.xml
    > 
    > Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**. Cilnē **Vispārīgi** iestatiet opciju Aktivizēt fiskālo integrāciju **kā** **Jā**.
1. Dodieties uz **Retail un Commerce Channel \> iestatīšanas finanšu integrācijas finanšu dokumentu nodrošinātājiem un \>\>** ielādējiet iepriekš lejupielādēto fiskālā dokumenta nodrošinātāja konfigurācijas failu.
1. Dodieties uz **mazumtirdzniecības un commerce kanālu iestatīšanas finanšu integrācijas finanšu savienotājiem un \>\>\>** ielādējiet agrāk lejupielādēto fiskālā savienotāja konfigurācijas failu.
1. Pārejiet uz **Sadaļu Mazumtirdzniecības \> un Commerce Channel Setup Finanšu integrācijas \>\> savienotāja funkcionālie** profili. Izveidojiet jaunu savienotāja funkcionalitātes profilu. Atlasiet dokumentu nodrošinātāju un iepriekš ielādēto savienotāju. Pēc vajadzības [atjauniniet datu](#default-data-mapping) kartēšanas iestatījumus.
1. Pārejiet uz **Retail un Commerce Channel setup Fiscal integration Connector \>\>\> tehniskajiem** profiliem. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto finanšu savienotāju. Pēc vajadzības [atjauniniet](#fiscal-connector-settings) savienotāja iestatījumus.
1. Pārejiet uz **sadaļu \> Mazumtirdzniecības un Commerce kanālu \> iestatīšanas finanšu integrācijas finanšu \> savienotāja** grupas. Izveidojiet jaunu finanšu savienotāja grupu iepriekš izveidotajā savienotāja funkcionālajā profilā.
1. Pārejiet uz **mazumtirdzniecības un Commerce \> channel \> iestatīšanas finanšu integrācijas \> finanšu reģistrācijas** procesiem. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālās reģistrācijas procesa soli un atlasiet iepriekš izveidoto finanšu savienotāja grupu.
1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Atlasiet funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā ir jāaktivizē reģistrācijas process. Kopsavilkuma **cilnē Finanšu reģistrācijas process** atlasiet iepriekš izveidoto finanšu reģistrācijas procesu.
1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**. Atlasiet aparatūras profilu, kas ir saistīts ar aparatūras staciju, ar kuru tiks pievienots fiskālais printeris. Kopsavilkuma cilnē **Finanšu** perifērijas ierīces atlasiet iepriekš izveidoto savienotāja tehnisko profilu.
1. Atveriet sadales grafiku (Mazumtirdzniecības un Commerce Retail un Commerce IT sadales grafiks) un atlasiet darbus **\>\>** **1070 un** **1090,** lai pārsūtītu datus uz kanāla datu bāzi.

#### <a name="default-data-mapping"></a>Noklusējuma datu kartēšana

Tālāk redzamais noklusējuma datu kartējums ir ietverts finanšu dokumenta nodrošinātāja konfigurācijā, kas ir nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Pievienotās vērtības nodokļa (PVN) likmju kartēšana - to nodokļu procentu vērtību kartēšana, kas iestatīti PVN kodiem, uz** **vērtībām TaxG (nodokļu grupa) atribūtu pieprasījumos, kas tiek sūtīti finanšu** pakalpojumiem. Šeit ir noklusējuma kartēšana:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Pirmais komponents katrā pārī norāda PVN nodokļu grupu, ko atbalsta EFR finanšu reģistrācijas pakalpojums. Otra sastāvdaļa norāda atbilstošo PVN likmi. Plašāku informāciju par PVN nodokļu grupām, ko EFR atbalsta Čehijas Republikai, skatiet [EFR](https://public.efsta.net/efr/) atsauci.

- **Noklusējuma PVN grupas kartēšana — jebkādas PVN summas, ko nevar kartēt uz vienu no iepriekš noteiktu PVN grupām, tiks attiecinātas uz noklusējuma** (pamata) PVN grupu. Šeit ir noklusējuma kartēšana:

    ```
    A
    ```

- **Depozīta** PVN grupas kartēšana – debitoru depozītu summas un debitora pasūtījuma depozīta summas tiks attiecinātas uz depozīta PVN grupu. Šeit ir noklusējuma kartēšana:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Finanšu savienotāja iestatījumi

Šādi iestatījumi ir iekļauti finanšu savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Galapunkta** adrese – finanšu reģistrācijas pakalpojuma URL.
- **Taimauts** – laika daudzums milisekundēs, ko finanšu savienotājs gaidīs uz finanšu reģistrācijas pakalpojuma atbildi.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet [Čehijas Republikas finanšu integrācijas parauga izvietošanas vadlīnijās (mantojuma)](emea-cze-fi-sample-sdk.md).
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
    1. Startējiet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet darbības, kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos [iepakojumus](fiscal-integration-sample-build-pipeline.md) fiskālās integrācijas parauga iepakojumam. **EFR būvējuma pipeline.yml veidnesPOZITOML fails var tikt atrasts Risinājumu** **\\ repozitorija YAML_Files**[Dynamics 365 Commerce konveijera](https://github.com/microsoft/Dynamics365Commerce.Solutions) sarakstā.

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Čehijas Republikai ir balstīts uz [fiskālās integrācijas](fiscal-integration-for-retail-channel.md) funkcionalitāti un ir daļa no Retail SDK. Paraugs atrodas Solutions repository mapē **src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) no fiskālā dokumenta nodrošinātāja, kas ir CRT Commerce Hardware Station paplašinājums un fiskālais savienotājs. Papildinformāciju par to, kā izmantot retail SDK, skatiet [mazumtirdzniecības SDK arhitektūrā](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un paplašinājuma modeļa ierobežojumu dēļ to [pašlaik nevar izmantot šim](../dev-itpro/build-pipeline.md) fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet [Čehijas Republikas finanšu integrācijas parauga izvietošanas vadlīnijās (mantojuma)](emea-cze-fi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

### <a name="commerce-runtime-extension-design"></a>Commerce runtime paplašinājuma dizains

Paplašinājuma, kas ir fiskālā dokumenta nodrošinātājs, nolūks ir izveidot pakalpojumiem raksturīgus dokumentus un apstrādāt atbildes no fiskālās reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Pastāv viens **DocumentProviderEFRFiscalLF pieprasījuma apstrādātājs dokumenta nodrošinātājam, kas tiek izmantots, lai ģenerētu finanšu dokumentus** finanšu reģistrācijas pakalpojumam.

Šis apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus.

- **GetFiscalDocumentDocumentProviderRequest — šajā pieprasījumā ir ietverta** informācija par to, kurš dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē finanšu reģistrācijas pakalpojumā.
- **GetSupportedRegistrableEventsDocumentProviderRequest - šis pieprasījums atgriež notikumu sarakstu,** uz kuriem ir jāabonē. Pašlaik tiek atbalstīti šādi notikumi: pārdošana, debitora konta depozīti un debitora pasūtījuma depozīti.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest - šis pieprasījums atgriež atbildi** no finanšu reģistrācijas pakalpojuma. Šī atbilde ir serializēta, lai veidotu virkni tā, lai tā būtu gatava saglabāt.

#### <a name="configuration"></a>Konfigurācija

Finanšu dokumentu nodrošinātāja konfigurācijas fails atrodas **src \\ FiscalIntegration \\ Efr \\ Configurations \\ DocumentProviders \\ DocumentProviderFiscalEFRSamplePlench.xml,**[Dynamics 365 Commerce kas atrodas Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitorijā. Faila mērķis ir iespējot finanšu dokumentu nodrošinātāja iestatījumus, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar finanšu reģistrācijas pakalpojumu. Aparatūras stacijas paplašinājums izmanto HTTP protokolu, lai iesniegtu CRT dokumentus, ko paplašinājums ģenerē finanšu reģistrācijas pakalpojumam. Tas apstrādā arī atbildes, kas saņemtas no fiskālās reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EFRHandler** pieprasījumu apdarinātājs ir ieejas punkts finanšu reģistrācijas pakalpojuma pieprasījumu apstrādei.

Apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus.

- **SubmitDocumentFiscalDeviceRequest – šis pieprasījums nosūta dokumentus finanšu reģistrācijas pakalpojumam un** atgriež atbildi no tā.
- **IsReadyFiscalDeviceRequest – šis pieprasījums tiek izmantots fiskālās reģistrācijas** pakalpojuma veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots, lai inicializētu finanšu reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja konfigurācijas fails atrodas **src \\ FiscalIntegration \\ Efr \\\\ Configurations Connectors \\ ConnectorEFRSample.xml** risinājumu [Dynamics 365 Commerce repozitorijā.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot finanšu savienotāja iestatījumus, kas jākonfigurē no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
