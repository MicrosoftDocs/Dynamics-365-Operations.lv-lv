---
title: Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Vācijai
description: Šajā tēmā ir sniegts pārskats par Vācijas fiskālās integrācijas paraugu Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: 128c94407a283bf45e5626de060cee82430f087b
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076866"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Vācijai

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par Vācijas fiskālās integrācijas paraugu Microsoft Dynamics 365 Commerce.

Lai izpildītu vietējās fiskālās prasības kases aparātiem Vācijā,Microsoft Dynamics 365 Commerce Vācijas funkcionalitāte ietver tirdzniecības vietas (POS) integrācijas paraugu ar ārēju nodokļu reģistrācijas pakalpojumu. Paraugs paplašina [fiskālās integrācijas funkcionalitāte](fiscal-integration-for-retail-channel.md). Tas ir balstīts uz [EFR (elektroniskais fiskālais reģistrs)](https://www.efsta.eu/de/fiskalloesungen/deutschland) risinājums no [EFSTA](https://www.efsta.eu/de/) un nodrošina saziņu ar EFR pakalpojumu, izmantojot HTTPS protokolu. EFR pakalpojumam jābūt mitinātam mazumtirdzniecības aparatūras stacijā vai atsevišķā datorā, ar kuru var izveidot savienojumu no aparatūras stacijas. Paraugs tiek nodrošināts avota koda veidā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Microsoft neizlaiž nekādu aparatūru, programmatūru vai dokumentāciju no EFSTA. Lai iegūtu informāciju par to, kā iegūt EFR risinājumu un to izmantot, sazinieties ar [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Scenāriji

Vācijai paredzētā fiskālā reģistrācijas pakalpojuma integrācijas paraugā ir ietverti šādi scenāriji.

### <a name="sales-operations"></a>Pārdošanas operācijas

- **Skaidras naudas pārdošanas un atgriešanas reģistrācija fiskālā reģistrācijas pakalpojumā:**

    Pārdošanas operāciju reģistrācija ietver šādas darbības:

    1. Darījuma sākuma reģistrācija

        Katra darījuma sākums tiek reģistrēts tehniskās drošības elementā (TSE), kas ir savienots ar EFR pakalpojumu. Reģistrācijas rezultātā TSE piešķir darījuma ID (TID).

    2. Darījuma beigu reģistrācija

        Noslēdzot darījumu POS, tas tiek reģistrēts, izmantojot to pašu TID, kas tika piešķirts darījuma sākuma reģistrācijas laikā. Tajā brīdī detalizēti darījumu dati tiek nosūtīti fiskālās reģistrācijas dienestam. Šie dati ietver informāciju par pārdošanas līniju, kā arī informāciju par atlaidēm, maksājumiem un nodokļiem.

    3. Atbildes tveršana no fiskālās reģistrācijas dienesta

        Drošības dati tiek saņemti no TSE kā atbildes daļa un tiek saglabāti darījumā kanāla datubāzē. Drošības dati sastāv no šādas informācijas:

        - TID
        - Darījuma sākuma datums un laiks
        - Darījuma beigu datums un laiks
        - Parakstu skaitītājs
        - Pārbaudiet vērtību
        - TSE sērijas numurs

- **Klientu pasūtījumu reģistrācija fiskālās reģistrācijas pakalpojumā:** Reģistrācijas process ir tāds pats kā skaidras naudas pārdošanas un atgriešanas process.
- **Dāvanu karšu un depozītu operāciju reģistrācija:** Reģistrācijas process ir tāds pats kā skaidras naudas pārdošanas un atgriešanas process.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Lietotāju informēšana par fiskālās reģistrācijas kļūmēm

Ir divi veidi, kā fiskālās reģistrācijas pakalpojums var informēt lietotājus par kļūmēm, kas radušās fiskālās reģistrācijas laikā:

- Izdrukājiet papildu informāciju no atbildes **Informācijas ziņa** lauks uz čekiem.
- Rādīt paziņojumus no fiskālā pakalpojuma kā lietotāja ziņojumus POS.

    > [!NOTE]
    > Šis paziņošanas mehānisms pieprasa, lai **Rādīt nodokļu reģistrācijas paziņojumus** parametrs uz **Savienotāju tehniskie profili** lapa ir ieslēgta.

#### <a name="printing-receipts"></a>Kvīšu drukāšana

Kvīts druka Vācijā ir obligāta. Visās kvītīs jāietver vismaz šāda informācija:

- Uzņēmuma nosaukums un adrese
- Informācija par precēm, ieskaitot to cenas un daudzumus
- Informācija par saņemtajiem maksājumiem
- Informācija par nodokļiem, ieskaitot kopējās summas par nodokļu likmi
- Drošības dati:

    - TID
    - Darījuma sākuma datums un laiks
    - Darījuma beigu datums un laiks
    - Parakstu skaitītājs
    - Pārbaudiet vērtību
    - TSE sērijas numurs

- Informatīvs ziņojums

> [!NOTE]
> QR kodu var izdrukāt arī uz čekiem. Lai gan QR kods nav obligāts, tas ir ļoti ieteicams. Lai iegūtu papildinformāciju par to, kā saņemt QR kodu kā daļu no atbildes no fiskālās reģistrācijas dienesta, skatiet "EFR rokasgrāmatu\[ DE\] " dokuments, kas publicēts [EFSTA dokumentācija](https://public.efsta.net/efr/) vietne.
>
> The **Informācijas ziņa** kvīšu laukā ir redzams paziņojums no fiskālās reģistrācijas dienesta. Piemēram, ja ir bojāta paraksta ierīce, kvītī var izdrukāt īpašu tekstu.

#### <a name="voided-suspended-and-recalled-transactions"></a>Anulēti, apturēti un atsaukti darījumi

- Anulēts darījums tiek reģistrēts kā lūgums izbeigt darījumu fiskālās reģistrācijas dienestā.
- Apturēts darījums tiek reģistrēts kā lūgums izbeigt darījumu fiskālās reģistrācijas dienestā.
- Apturēta darījuma atsaukšana fiskālās reģistrācijas dienestā tiek reģistrēta kā jauna darījuma sākums.

### <a name="non-sales-transactions-and-shift-closing"></a>Ar pārdošanu nesaistīti darījumi un maiņas slēgšana

Kā nefiskālas operācijas fiskālās reģistrācijas pakalpojumā tiek reģistrēti šādi ar pārdošanu nesaistīti darījumi, izmantojot **NFS** tags:

- Deklarēt sākuma summu
- Mainīgais ieraksts
- Norēķinu noņemšana
- Noguldījums seifā
- Noguldījums bankā
- Ieņēmumu konti
- Izdevumu konti

The **Aizvērt maiņu** darbība tiek reģistrēta arī kā nefiskāla operācija fiskālās reģistrācijas pakalpojumā, izmantojot **NFS** tagu.

### <a name="data-export-and-audit"></a>Datu eksports un audits

Visi darījumi ir jāparaksta TSE, lai nodrošinātu to integritāti, autentiskumu un pilnīgumu un palīdzētu novērst manipulācijas ar reģistrētajiem datiem.

> [!WARNING]
> Var izmantot tikai sertificētu TSE. Informāciju par TSE veidiem un modeļiem, kas tiek atbalstīti EFR risinājumā, skatiet "EFR rokasgrāmatā\[ DE\] " dokuments, kas publicēts [EFSTA dokumentācija](https://public.efsta.net/efr/) vietne. Lai iegūtu informāciju par to, kā izvēlēties un iegūt TSE, sazinieties ar [EFSTA](https://www.efsta.eu/at/kontakt).

Saskaņā ar noteikumiem Vācijā ir nepieciešams atbalsts DSFinV-K eksportam. DSFinV-K eksportu var aktivizēt EFR risinājumā. Papildinformāciju par DSFinV-K eksportēšanu skatiet "EFR rokasgrāmatā\[ DE\] " dokuments, kas publicēts [EFSTA dokumentācija](https://public.efsta.net/efr/) vietne.

### <a name="limitations-of-the-sample"></a>Izlases ierobežojumi

Fiskālās reģistrācijas pakalpojums atbalsta tikai scenārijus, kuros cenās ir iekļauts tirdzniecības nodoklis. Tāpēc, **Cenās iekļauts pārdošanas nodoklis** opcija ir jāiestata uz **Jā** gan veikaliem, gan klientiem.

Fiskālais pakalpojums neatbalsta situācijas, kad vienai transakcijas rindai tiek lietots vairāk nekā viens tirdzniecības nodokļa kods.

Fiskālās integrācijas sistēma neatbalsta pārdošanas kotācijas. Tāpēc šīs darbības nav reģistrētas fiskālā dienestā.

## <a name="set-up-commerce-for-germany"></a>Iestatiet Commerce for Germany

Šajā sadaļā ir aprakstīti tirdzniecības iestatījumi, kas ir īpaši un ieteicami Vācijai. Papildinformāciju par iestatīšanu skatiet [Tirdzniecības mājas lapa](../index.md).

Lai izmantotu Vācijai raksturīgo funkcionalitāti, ir jānorāda šādi iestatījumi.

- Juridiskās personas primārajā adresē lauku Valsts/reģions **iestatiet** uz **DEU** (Vācija).
- Katra Vācijā izvietotā veikala POS funkcionalitātes profilā iestatiet **ISO koda** lauku uz **DE** (Vācija).

Jānorāda arī šādi Vācijas iestatījumi. Pēc uzstādīšanas pabeigšanas noteikti palaidiet atbilstošus sadales darbus.

### <a name="set-up-vat-per-german-requirements"></a>Iestatīt PVN pēc Vācijas prasībām

Ir jāizveido PVN kodi, PVN grupas un krājumu PVN grupas. Ir arī jāiestata PVN informācija precēm un pakalpojumiem. Plašāku informāciju par PVN līdzekļu iestata un lietošanu skatiet [PVN pārskatā](../../finance/general-ledger/indirect-taxes-overview.md).

Pārdošanas kvītīs var izdrukāt saīsinātu kodu PVN kodam (piemēram, "A" vai "B"). Lai padarītu šo funkcionalitāti pieejamu, lapā PVN kodi iestatiet **lauku** Kods **drukāšanai**.

### <a name="set-up-stores"></a>Iestatīt veikalus

**Lapā Visi veikali** atjauniniet veikala informāciju. Konkrēti, iestatiet šādus parametrus:

- Laukā **PVN grupa** norādiet PVN grupu, kas jāizmanto pārdošanai noklusētajam debitoram.
- Iestatiet opciju **Cenas iekļaut PVN** uz **Jā**.
- Iestatiet **lauku Nosaukums** uz uzņēmuma nosaukumu. Šīs izmaiņas palīdz nodrošināt, ka uzņēmuma nosaukums tiek parādīts pārdošanas kvītī. Varat arī pievienot uzņēmuma nosaukumu pārdošanas kvīts izkārtojumam kā brīvas formas tekstu.
- Iestatiet **lauku Nodokļu identifikācijas numurs (NMIN)** uz uzņēmuma identifikācijas numuru. Šīs izmaiņas palīdz nodrošināt, ka uzņēmuma identifikācijas numurs tiek parādīts pārdošanas kvītī. Varat arī pievienot uzņēmuma identifikācijas numuru pārdošanas ieejas plūsmas izkārtojumam kā brīvas formas tekstu.

### <a name="set-up-functionality-profiles"></a>Iestatīt funkcionalitātes profilus

Iestatiet POS funkcionalitātes profilus. **Kopsavilkuma cilnē Saņemšanas pavadzīmes numerācija** iestatiet saņemšanas pavadzīmes numerēšanu, izveidojot vai atjauninot ierakstus **pārdošanas**, **pārdošanas pasūtījuma** un **atgriezto preču** saņemšanas darbību tipiem.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotus laukus, lai tos varētu izmantot ieejas plūsmas formātos pārdošanas ieejas plūsmām

Var konfigurēt valodas tekstu un pielāgotos laukus, kas tiek izmantoti POS saņemšanas formātos. Tā lietotāja noklusējuma uzņēmumam, kurš izveido ieejas plūsmas iestatījumus, jābūt tai pašai juridiskajai personai, kurā tiek izveidots valodas teksta iestatījums. Alternatīvi, gan lietotāja noklusējuma uzņēmumā, gan veikala juridiskajā personā, kurai ir izveidots iestatījums, ir jāizveido vieni un tie paši valodas teksti.

**Lapā Teksts** valodā pievienojiet šādus ierakstus ieejas plūsmu izkārtojumu pielāgoto lauku etiķetēm. Ņemiet vērā, **ka** tabulā norādītās vērtības Valodas ID **, Teksta ID** un **Teksts** ir tikai piemēri. Varat tos mainīt, lai tie atbilstu jūsu prasībām. Tomēr izmantotajām **teksta ID** vērtībām jābūt unikālām, un tām jābūt vienādām ar vai lielākām par 900001.

Pievienojiet šādas POS etiķetes **valodas teksta** lapas POS **sadaļai**.

| Valodas kods | Teksta ID | Teksts                                  |
|-------------|---------|---------------------------------------|
| en-US       | 900001  | QR kods                               |
| en-US       | 900002  | Darbības ID                        |
| en-US       | 900003  | Nodokļu mazumtirdzniecības drukas kods                 |
| en-US       | 900004  | Nodokļa summa (pārdošana)                    |
| en-US       | 900005  | Nodokļa bāze (pārdošana)                     |
| en-US       | 900006  | Transakcijas sākuma datums un laiks           |
| en-US       | 900007  | Transakcijas beigu datums un laiks             |
| en-US       | 900008  | Drošības elementa sērijas numurs |
| en-US       | 900009  | Parakstu skaitītājs                     |
| en-US       | 900010  | Pārbaudiet vērtību                           |
| en-US       | 900011  | Informācijas ziņojums                          |

**Lapā Pielāgotie lauki** pievienojiet šādus ierakstus pielāgotajiem laukiem saņemšanas shēmu izkārtojumiem. Ņemiet vērā, **ka paraksta teksta ID** vērtībām jāatbilst **teksta ID** vērtībām, kas norādītas **lapā Valodas teksts**.

| Nosaukums                            | Veids    | Uzraksta teksta ID |
|---------------------------------|---------|-----------------|
| QRCODEDE\_                      | Saņemšana | 900001          |
| TRANSACTIONIDDE\_               | Saņemšana | 900002          |
| RETAILPRINTCODEDE\_             | Saņemšana | 900003          |
| SALESTAXAMOUNTDE\_              | Saņemšana | 900004          |
| SALESTAXBASISDE\_               | Saņemšana | 900005          |
| TRANSACTIONSTARTDATETIMEDE\_    | Saņemšana | 900006          |
| TRANSACTIONENDDATETIMEDE\_      | Saņemšana | 900007          |
| SECURITYELEMENTSERIALNUMBERDE\_ | Saņemšana | 900008          |
| SIGNCOUNTERDE\_                 | Saņemšana | 900009          |
| SIGNDE\_                        | Saņemšana | 900010          |
| INFOMESSAGEDE\_                 | Saņemšana | 900011          |

> [!NOTE]
> Ir svarīgi norādīt pareizus pielāgoto lauku nosaukumus, kā norādīts iepriekšējā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs trūkstošus datus kvītīs.

### <a name="configure-receipt-formats"></a>Konfigurēt kvīšu formātus

Katram nepieciešamajam ieejas plūsmas formātam mainiet lauka Drukas izturēšanās **vērtību** uz **Vienmēr drukāt**.

Saņemšanas formāta noformētājā atbilstošajām saņemšanas sadaļām pievienojiet šādus pielāgotus laukus. Ievērojiet, ka lauku nosaukumi atbilst iepriekšējā sadaļā definētajiem valodu tekstiem.

- **Galvene:** Pievienojiet šādus laukus:

    - **Laukos Veikala nosaukums** un **Nodokļu identifikācijas numurs**, kas tiek izmantoti, lai drukātu uzņēmuma nosaukumu un identifikācijas numuru kvītīs. Varat arī pievienot uzņēmuma nosaukumu un identifikācijas numuru izkārtojumam kā brīvas formas tekstu.
    - **Veikala adrese**, **Datums**, **Laiks 24H**, **Kvīts numurs** un **Reģistrēt numuru** laukus.

- **Rindas:** Pievienojiet šādus laukus:

    - **Krājuma nosaukuma** lauks
    - **Lauks Daudzums**
    - **Kopējā cena ar nodokļu** lauku
    - **Lauks Nodokļu mazumtirdzniecības drukas kods**, ko izmanto, lai drukātu saīsināto kodu, kas atbilst krājumam kodam

- **Kājene:** pievienojiet šādus laukus:

    - Maksājumu lauki, lai tiktu izdrukātas katra maksājuma veida maksājuma summas. Piemēram, pievienojiet **laukus Norēķinu nosaukums** un **Norēķinu summa** vienai izkārtojuma rindai.
    - **Lauki lauku grupā Nodokļu sadalīšana**. Visi šīs lauku grupas lauki jādrukā vienā atsevišķā rindā.

        - **Lauks PVN ID**, kas ir standarta lauks, kas ļauj drukāt PVN kopsavilkumu katram PVN kodam. Lauks jāpievieno jaunai rindai.
        - **Lauks Nodokļa procenti**, kas ir standarta lauks, kuru izmanto, lai drukātu PVN koda efektīvo nodokļa likmi.
        - **lauks PVN bāze (pārdošana),** kas tiek izmantots, lai drukātu PVN koda kopējo kases pārdošanas summu. Priekšapmaksa un dāvanu karšu operācijas nav iekļautas.
        - **PVN summa (PVN)** summa, kas tiek izmantota, lai drukātu PVN koda kases pārdošanas ieejas nodokļa summu.
        - **Lauks Nodokļu mazumtirdzniecības drukas kods**, kas tiek izmantots, lai drukātu saīsināto kodu, kas atbilst PVN kodam.

    - Lauki, kuros ir droši darbības dati, kurus atgriež finanšu reģistrācijas pakalpojums:

        - **Darbības ID**, kas identificē kases darbības numuru finanšu reģistrācijas pakalpojumā
        - **Darbības sākuma datuma laika** lauks
        - **Darbības beigu datuma laika** lauks
        - **Drošības elementa** lauka sērijas numurs
        - **Paraksta skaitītāja** lauks
        - **Pārbaudīt vērtības** lauku
        - **QR koda** lauks, ko izmanto, lai drukātu atsauci uz reģistrēto kases darījumu QR koda veidā

        > [!NOTE]
        > **QR koda** vērtība tiek izgūta no finanšu reģistra atbildes. EFR atgriež QR kodu savā atbildē tikai tad, ja efsta dokumentācijā ir aprakstīta EFR konfigurācijas lauka Atribūti **vērtība**. QR koda formātam **EFR konfigurācijas laukā Atribūti** jābūt iestatītam uz **BMP**.

    - **Informācijas ziņojuma** lauks, lai saņemšanas pavadzīmēs varētu parādīt paziņojumu ziņojumus no finanšu reģistrācijas pakalpojuma. Piemēram, ja ir bojāta paraksta ierīce, kvītī var izdrukāt īpašu tekstu.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, skatiet [set up and design receipt formats](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Iestatīt vācijas finanšu integrāciju

Vācijas finanšu reģistrācijas pakalpojumu integrācijas izlase ir balstīta uz fiskālās [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **risinājumu\\ repozitorija mapē \\ srcFiscalIntegrationEfr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs laidienā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir Commerce izpildlaika paplašinājums (CRT), un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Izstrādātāja virtuālajā mašīnā (VM) ir jāizmanto iepriekšējā mazumtirdzniecības SDK versija Microsoft Dynamics Dzīves cikla pakalpojumi (LCS). Plašāku informāciju skatiet [Guidelines for the Fiscal Integration sample for Germany (legacy)](emea-deu-fi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

Izpildiet finanšu integrācijas iestatīšanas soļus, kā aprakstīts sadaļā [Iestatīt finanšu integrāciju Commerce kanāliem](setting-up-fiscal-integration-for-retail-channel.md):

1. [Iestatiet finanšu reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ņemiet vērā arī šīs finanšu reģistrācijas pakalpojuma integrācijas izlasei [raksturīgos](#set-up-the-registration-process) fiskālās reģistrācijas procesa iestatījumus.
1. [Iestatiet kļūdu apstrādes iestatījumus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Iespējams, ka fiskālās integrācijas sistēmas kļūdu apstrādes iespējas nav pilnībā saskaņotas ar vietējiem finanšu noteikumiem.
    >
    > - Ieteicams lapā Fiskālās reģistrācijas process **atstāt opciju** **Turpināt kļūdu** izslēgt, jo visām darbībām jābūt pareizi reģistrētām, pat ja pirmais fiskālās reģistrācijas mēģinājums nav izdevies.
    > - **Pirms izvēles Izvēles Izlaist** vai **Atzīmēt kā reģistrētu** **lapā Fiskālās reģistrācijas process**, šīs izmaiņas finanšu reģistrācijas procesā ir jāapspriež ar savu nodokļu konsultantu vai vietējo nodokļu iestādi.

1. [Iespējot atliktās finanšu reģistrācijas](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) manuālu izpildi.
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, veiciet šīs darbības, lai iestatītu Commerce headquarters. Plašāku informāciju skatiet [Set up the fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lejupielādēt finanšu dokumentu nodrošinātāja un finanšu savienotāja konfigurācijas failus:

    1. [Dynamics 365 Commerce Atveriet risinājumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repozitoriju.
    1. Atlasiet pareizu laidiena filiāles versiju atbilstoši SDK/lietojumprogrammas versijai (piemēram, **[laidiens/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atveriet **src \> FiscalIntegration \> Efr**.
    1. Lejupielādējiet fiskālā dokumenta nodrošinātāja konfigurācijas failu vietnē **Konfigurācijas \> Dokumentu nodrošinātāji \> DocumentProviderFiscalEFRSampleGermany.xml** (piemēram, [izlaišanas fails/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Lejupielādējiet fiskālā savienotāja konfigurācijas failu vietnē **Konfigurācijas \> Savienotāji \> SavienotājsEFRSample.xml** (piemēram, [izlaišanas fails/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas šādās mazumtirdzniecības SDK mapēs izstrādātāja VM LCS:
    >
    > - **Fiskālo dokumentu nodrošinātāja konfigurācijas fails:** RetailSdk\\ Extensions paraugi\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Konfigurācija\\ DocumentProviderFiscalEFRSampleGermany.xml
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

- **Konkursa veidu kartēšana** – Maksājumu metožu kartēšana ar vērtībām **PayG** (maksājumu grupa) atribūts pieprasījumos, kas tiek nosūtīti fiskālajam dienestam. Šeit ir noklusējuma kartēšana:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Pirmais komponents katrā pārī apzīmē veikalam iestatīto maksājuma veidu. Otrais komponents apzīmē atbilstošo maksājumu grupu, kuru atbalsta EFR fiskālās reģistrācijas pakalpojums. Papildinformāciju par maksājumu grupām, kuras EFR atbalsta Vācijā, skatiet vietnē [EFR atsauce](https://public.efsta.net/efr/).

    Maksājumu metožu kartējuma paraugs atbilst veikala maksājumu metodēm, kas ir konfigurētas standarta demonstrācijas datos.

    | Maksāšanas veids | Maksāšanas metodes nosaukums |
    |----------------|---------------------|
    | 1              | Kase                |
    | 2              | Atzīmēt               |
    | 3              | Karte                |
    | 4              | Debitora konts    |
    | 5              | Cits               |
    | 6              | Valūta            |
    | 7              | Dokuments             |
    | 8              | Dāvanu karte           |
    | 9              | Norēķina noņemšana/mainīšana |
    | 10.             | Lojalitātes programmas kartes       |
    | 11             | Nevietējās pārbaudes    |

    Tāpēc jums ir jāmaina kartējuma paraugs atbilstoši jūsu lietojumprogrammā konfigurētajām maksājumu metodēm.

- **Iekļaujiet klienta datus** – Ja šis parametrs ir ieslēgts, fiskālā dienesta pieprasījumos būs ietverta klienta informācija, piemēram, vārdi un adreses, gadījumos, kad darījumam tiek pievienots klients.
- **Pievienotās vērtības nodokļa (PVN) likmju kartēšana** – Tirdzniecības nodokļa kodiem iestatīto nodokļu procentu vērtību kartēšana ar vērtībām **NodoklisG** (nodokļu grupa) atribūts pieprasījumos, kas tiek nosūtīti fiskālajam dienestam. Šeit ir noklusējuma kartēšana:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Katra pāra pirmā sastāvdaļa ir PVN nodokļu grupa, kuru atbalsta EFR fiskālās reģistrācijas pakalpojums. Otrā sastāvdaļa atspoguļo atbilstošo PVN likmi. Papildinformāciju par PVN nodokļu grupām, kuras EFR atbalsta Vācijā, skatiet vietnē [EFR atsauce](https://public.efsta.net/efr/).

- **Nodokļu grupa dāvanu kartēm un noguldījumiem** – vērtība **NodoklisG** atribūts pieprasījumos, kas tiek nosūtīti fiskālajam dienestam, pamatojoties uz darbībām, kas saistītas ar dāvanu kartēm vai noguldījumiem. Šeit ir noklusējuma kartēšana:

    ```
    G
    ```

- **Nodokļu grupa bez PVN** – vērtība **NodoklisG** atribūts pieprasījumos, kas tiek nosūtīti fiskālajam dienestam, pamatojoties uz darbībām, kas ir atbrīvotas no nodokļu saistībām. Šeit ir noklusējuma kartēšana:

    ```
    F
    ```

> [!NOTE]
> Noklusējuma datu kartēšanas nodokļu iestatījumi ir atbildīgi par nodokļu iestatījumu saskaņošanu sistēmā un nodokļu grupām EFR pakalpojumā. Nodokļu grupas var drukāt uz čekiem tikai tad, ja **Kods drukāšanai** lauks ir iestatīts uz **Pārdošanas nodokļa kodi** lappuse.

#### <a name="fiscal-connector-settings"></a>Fiskālā savienotāja iestatījumi

Tālāk norādītie iestatījumi ir iekļauti fiskālā savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga.

- **Galapunkta adrese** – Fiskālās reģistrācijas pakalpojuma URL.
- **Pārtraukums** — Laiks milisekundēs, cik ilgi fiskālais savienotājs gaidīs atbildi no fiskālās reģistrācijas pakalpojuma.
- **Rādīt nodokļu reģistrācijas paziņojumus** – Šis karodziņš nosaka, vai operatoram ir jāparāda paziņojumi, ko nosūta nodokļu reģistrācijas pakalpojums.

### <a name="configure-channel-components"></a>Konfigurējiet kanāla komponentus

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Plašāku informāciju skatiet [Guidelines for the Fiscal Integration sample for Germany (legacy)](emea-deu-fi-sample-sdk.md).
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

#### <a name="set-up-the-development-environment"></a>Iestatiet izstrādes vidi

Lai iestatītu izstrādes vidi, lai pārbaudītu un paplašinātu paraugu, veiciet šīs darbības.

1. Klonējiet vai lejupielādējiet [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve. Atlasiet pareizo laidiena filiāles versiju atbilstoši savai SDK/lietojumprogrammas versijai. Papildinformāciju skatiet [Lejupielādējiet mazumtirdzniecības SDK paraugus un atsauces pakotnes no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet EFR risinājumu plkst **Dynamics365Commerce.Solutions\\ Fiskālā integrācija\\ Efr\\ EFR.sln**, un izveidojiet to.
1. Instalējiet Commerce izpildlaika paplašinājumus:

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

    - Iekš **Efr\\ HardwareStation\\ HardwareStation.EFR.Installer\\ atkritumu tvertne\\ Atkļūdošana\\ net461** mapi, atrodiet **HardwareStation.EFR.Installer** uzstādītājs.
    - Sāciet paplašinājuma instalētāju no komandrindas:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet norādījumus [Fiskālās integrācijas parauga izveides konveijera iestatīšana](fiscal-integration-sample-build-pipeline.md) lai ģenerētu un atbrīvotu Cloud Scale Unit un pašapkalpošanās izvietojamās pakotnes fiskālās integrācijas paraugam. The **EFR build-pipeline.yml** veidnes YAML failu var atrast **Cauruļvads\\ YAML_Files** mape [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions) krātuve.

## <a name="design-of-extensions"></a>Paplašinājumu projektēšana

Vācijas finanšu reģistrācijas pakalpojumu integrācijas izlase ir balstīta uz fiskālās [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no mazumtirdzniecības SDK. Paraugs atrodas **risinājumu\\ repozitorija mapē \\ srcFiscalIntegrationEfr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs laidienā/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Paraugs [sastāv](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālo dokumentu nodrošinātāja, kas ir paplašinājums CRT, un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot mazumtirdzniecības SDK, skatiet [Mazumtirdzniecības SDK arhitektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) un [Iestatiet neatkarīgā iepakojuma SDK izveides konveijeru](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Ierobežojumu dēļ [jauns neatkarīgs iepakojuma un pagarinājuma modelis](../dev-itpro/build-pipeline.md), to pašlaik nevar izmantot šim fiskālās integrācijas paraugam. Iepriekšējā mazumtirdzniecības SDK versija ir jāizmanto izstrādātāja VM LCS. Plašāku informāciju skatiet [Guidelines for the Fiscal Integration sample for Germany (legacy)](emea-deu-fi-sample-sdk.md). Atbalsts jaunajam neatkarīgajam iepakojuma un paplašināšanas modelim fiskālās integrācijas paraugiem ir plānots vēlākās versijās.

### <a name="crt-extension-design"></a>CRT pagarinājuma dizains

Paplašinājuma, kas ir fiskālo dokumentu nodrošinātājs, mērķis ir ģenerēt pakalpojumam specifiskus dokumentus un apstrādāt atbildes no fiskālā reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

Dokumentu nodrošinātājam ir viens pieprasījumu apstrādātājs, **DocumentProviderEFRFiscalDEU**. Šis apstrādātājs tiek izmantots, lai ģenerētu fiskālos dokumentus fiskālās reģistrācijas pakalpojumam. Tas ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumenta nodrošinātāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest** – Šis pieprasījums satur informāciju par to, kāds dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē fiskālās reģistrācijas pakalpojumā.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Šis pieprasījums atgriež atbildi kopā ar paplašinātajiem datiem.

#### <a name="configuration"></a>Konfigurācija

Fiskālā dokumenta nodrošinātāja konfigurācijas fails atrodas vietnē **src\\ Fiskālā integrācija\\ Efr\\ Konfigurācijas\\ Dokumentu nodrošinātāji\\ DocumentProviderFiscalEFRSampleGermany.xml** iekš [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) krātuve. Faila mērķis ir iespējot fiskālo dokumentu nodrošinātāja iestatījumu konfigurēšanu no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar fiskālās reģistrācijas pakalpojumu.

Aparatūras stacijas paplašinājums ir **HardwareStation.Extension.EFRSample**. Tas izmanto HTTP protokolu, lai iesniegtu dokumentus, kas CRT paplašinājums ģenerē fiskālās reģistrācijas pakalpojumam. Tas arī apstrādā atbildes, kas tiek saņemtas no fiskālās reģistrācijas dienesta.

#### <a name="request-handler"></a>Pieprasījumu apstrādātājs

The **EFRHandler** pieprasījumu apstrādātājs ir piekļuves punkts, lai apstrādātu pieprasījumus nodokļu reģistrācijas dienestam. Šis apstrādātājs ir mantots no **INamedRequestHandler** saskarne. The **Apdarinātāja vārds** metode ir atbildīga par apstrādātāja vārda atgriešanu. Apdarinātāja nosaukumam ir jāatbilst fiskālā savienotāja nosaukumam, kas norādīts Commerce galvenajā mītnē.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – Šis pieprasījums nosūta dokumentus fiskālās reģistrācijas dienestam un atgriež no tā atbildi.
- **IsReadyFiscalDeviceRequest** – Šis pieprasījums tiek izmantots fiskālās reģistrācijas dienesta veselības pārbaudei.
- **InitializeFiscalDeviceRequest** – Šis pieprasījums tiek izmantots, lai inicializētu fiskālās reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Fiskālā savienotāja konfigurācijas fails atrodas vietnē **src\\ Fiskālā integrācija\\ Efr\\ Konfigurācijas\\ Savienotāji\\ SavienotājsEFRSample.xml** iekš [Dynamics 365 Commerce Risinājumi](https://github.com/microsoft/Dynamics365Commerce.Solutions/) krātuve. Faila mērķis ir iespējot fiskālā savienotāja iestatījumu konfigurēšanu no Commerce galvenās mītnes. Faila formāts ir saskaņots ar fiskālās integrācijas konfigurācijas prasībām.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
