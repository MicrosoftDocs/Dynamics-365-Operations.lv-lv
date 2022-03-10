---
title: Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Vācijai
description: Šajā tēmā sniegts pārskats par Vācijas finanšu integrācijas paraugu Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: 65315a9fd6bc1af26bc225220e096aee4da09be2
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388163"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Fiskālās reģistrācijas pakalpojuma integrācijas paraugs Vācijai

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Šajā tēmā sniegts pārskats par Vācijas finanšu integrācijas paraugu Microsoft Dynamics 365 Commerce.

Lai atbilstu lokāliem finanšu nosacījumiem kases reģistriem Vācijā, Microsoft Dynamics 365 Commerce Vācijas funkcionalitāte ietver pārdošanas punkta (POS) parauga integrāciju ar ārēju finanšu reģistrācijas pakalpojumu. Paraugs paplašina finanšu integrācijas [funkcionalitāti](fiscal-integration-for-retail-channel.md). Tas ir balstīts uz [EFR (Elektronisko finanšu reģistru)](https://www.efsta.eu/de/fiskalloesungen/deutschland)[risinājumu no EFSTA](https://www.efsta.eu/de/) un nodrošina sakarus ar EFR pakalpojumu, izmantojot HTTPS protokolu. EFR pakalpojums ir jā vieso Retail aparatūras stacijā vai atsevišķā datorā, kurā var izveidot savienojumu no aparatūras stacijas. Paraugs ir nodrošināts avota koda formā un ir daļa no mazumtirdzniecības programmatūras izstrādes komplekta (SDK).

Korporācija Microsoft neizlaiž nevienu aparatūru, programmatūru vai dokumentāciju no EFSTA. Lai iegūtu informāciju par to, kā iegūt EFR risinājumu un to izmantot, sazinieties ar [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Scenāriji

Tālāk minētajiem scenārijiem ir ietverti Vācijas finanšu reģistrācijas pakalpojumu integrācijas paraugs.

### <a name="sales-operations"></a>Pārdošanas operācijas

- **Kases un pārnestās pārdošanas un ieņēmumu reģistrācija finanšu reģistrācijas pakalpojumā:**

    Pārdošanas operāciju reģistrācija ietver sekojošos soļus:

    1. Darbības sākuma reģistrācija

        Katras darbības sākums ir reģistrēts tehniskajā drošības elementā (LF), kas savienots ar EFR pakalpojumu. Reģistrācijas rezultātā UZR piešķir darbības ID (TID).

    2. Darbības beigu reģistrācija

        Kad DARBĪBA ir pabeigta POS, tā ir reģistrēta, izmantojot to pašu TID, kas piešķirts darbības sākuma reģistrācijas laikā. Tajā laikā detalizētie darbības dati tiek nosūtīti uz finanšu reģistrācijas pakalpojumu. Šie dati ietver pārdošanas rindas informāciju un informāciju par atlaidēm, maksājumiem un nodokļiem.

    3. Atbildes iegūšana no finanšu reģistrācijas pakalpojuma

        Drošības dati ir saņemti no UZMK kā daļa no atbildes un saglabāti darbības kanāla datu bāzē. Drošības dati sastāv no šādas informācijas:

        - TID (SID)
        - Darījuma sākuma datums un laiks
        - Darījuma beigu datums un laiks
        - Parakstu skaitītājs
        - Pārbaudīt vērtību
        - NUMERĀCIJas sērijas numurs

- **Debitora pasūtījumu reģistrācija finanšu reģistrācijas pakalpojumā:** reģistrācijas process ir tāds pats kā pārdošanas un atgriešanas process, kas tiek veikts skaidrā naudā un ņemot vērā atgriešanu.
- **Operāciju, kurās ir iesaistītas dāvanu kartes un depozītus, reģistrācija:** reģistrācijas process ir vienāds ar pārdošanas un atgriešanu skaidrā naudā procesu.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Tiek paziņots lietotājiem par finanšu reģistrācijas kļūmēm

Ir divi veidi, kā finanšu reģistrācijas pakalpojums var paziņot lietotājiem par finanšu reģistrācijas laikā notikušiem defektiem:

- Izdrukājiet papildu informāciju no atbildes informācijas **ziņojuma laukā** kvītīs.
- Rādīt finanšu pakalpojuma paziņojumus POS kā lietotāja ziņojumus.

    > [!NOTE]
    > Šim paziņojumu mehānismam ir nepieciešams **, lai Connector tehnisko profilu lapā tiktu ieslēgts** **parametrs** Rādīt finanšu reģistrācijas paziņojumus.

#### <a name="printing-receipts"></a>Kvīšu drukāšana

Kvīšu drukāšana ir obligāta Vācijā. Visās kvītīs ir jābūt vismaz šādai informācijai:

- Uzņēmuma nosaukums un adrese
- Informācija par precēm, tostarp to cenām un daudzumiem
- Informācija par saņemtajiem maksājumiem
- Informācija par nodokļiem, iekļaujot kopsummas pēc nodokļu likmes
- Drošības dati:

    - TID (SID)
    - Darījuma sākuma datums un laiks
    - Darījuma beigu datums un laiks
    - Parakstu skaitītājs
    - Pārbaudīt vērtību
    - NUMERĀCIJas sērijas numurs

- Informatīvs ziņojums

> [!NOTE]
> QR kodu var drukāt arī uz kvīts. Lai arī QR kods ir neobligāts, tas ir ļoti ieteicams. Papildinformāciju par to, kā iegūt QR kodu kā daļu no fiskālās reģistrācijas pakalpojuma atbildes, skatiet dokumentā "EFR Guide \[DE\]" [, kas ir publicēts EFSTA dokumentācijas](https://public.efsta.net/efr/) vietnē.
>
> Kvīšu **informācijas** ziņojuma lauks rāda paziņojumu no finanšu reģistrācijas pakalpojuma. Piemēram, ja paraksta ierīce tiek bojāta, uz kvīts var drukāt īpašu tekstu.

#### <a name="voided-suspended-and-recalled-transactions"></a>Anulētās, aizturētās un atsauktās darbības

- Anulētā darbība tiek reģistrēta kā pieprasījums pārtraukt darbību finanšu reģistrācijas pakalpojumā.
- Aizturēta darbība tiek reģistrēta kā pieprasījums pārtraukt darbību finanšu reģistrācijas pakalpojumā.
- Bloķētās darbības atsaukšana ir reģistrēta kā jaunas darbības sākums finanšu reģistrācijas pakalpojumā.

### <a name="non-sales-transactions-and-shift-closing"></a>Darbības, kas nav pārdošanas un maiņas slēgšana

Izmantojot NFS tagu, tālāk norādītās ar pārdošanu nesaistītās darbības tiek reģistrētas kā ar finanšu operāciju saistītas finanšu **reģistrācijas** pakalpojumā:

- Deklarēt sākuma summu
- Mainīgais ieraksts
- Norēķinu noņemšana
- Noguldījums seifā
- Noguldījums bankā
- Ieņēmumu konti
- Izdevumu konti

Darbība **Slēgt maiņu** arī tiek reģistrēta kā finanšu reģistrācijas pakalpojumā operācija, kas nav finanšu operācija, izmantojot **tagu NFS**.

### <a name="data-export-and-audit"></a>Datu eksports un audits

Visām darbībām jābūt parakstītām AR UZZ, lai nodrošinātu to integritāti, precizitāti un pabeigtību un palīdzētu novērst ierakstīto datu manipulāciju.

> [!WARNING]
> Var lietot tikai sertificētu CER INFORMĀCIJU. Informāciju par TO TSE veidiem un modeļiem, kas tiek atbalstīti EFR risinājumā, skatiet dokumentu "EFR rokasgrāmata \[DE\]" [, kas ir publicēta EFSTA dokumentācijas](https://public.efsta.net/efr/) vietnē. Lai iegūtu informāciju par to, kā izvēlēties un iegūt DARBAUB, sazinieties ar [EFSTA](https://www.efsta.eu/at/kontakt).

Noteikumiem Vācijā nepieciešams atbalsts DSFinV-K eksportam. EFR risinājumā var tikt izraisīts DSFinV-K eksports. Papildinformāciju par DSFinV-K eksportēšanu skatiet EFSTA\[ dokumentācijas vietnē publicētajā dokumentā "EFR Guide \] DE [...](https://public.efsta.net/efr/)".

### <a name="limitations-of-the-sample"></a>Parauga ierobežojumi

Finanšu reģistrācijas pakalpojums atbalsta tikai scenārijus, kuros PVN ir iekļauts cenās. Tāpēc gan veikaliem **, gan debitoriem** opcijai Cenās **ir** jāiestata PVN opcija Jā.

Finanšu pakalpojums neatbalsta situācijas, kad vienai darbības rindai tiek lietoti vairāki PVN kodi.

Finanšu integrācijas struktūra neatbalsta pārdošanas piedāvājumus. Tāpēc šīs operācijas nav reģistrētas finanšu pakalpojumā.

## <a name="set-up-commerce-for-germany"></a>Iestatīt Commerce For Vācijai

Šajā sadaļā aprakstīti Commerce iestatījumi, kas ir specifiski un ieteicami Vācijai. Plašāku informāciju par iestatīšanu skatiet Commerce [mājas lapā](../index.md).

Lai lietotu Funkcionalitāti, kas ir raksturīga Vācijai, ir jānorāda šādi iestatījumi.

- Juridiskas personas primārajā adresē iestatiet lauku Valsts **/reģions** uz **DEU** (Vācija).
- Katra Vācijas veikalā izvietotā veikala POS funkcionalitātes profilā iestatiet **ISO** koda lauku uz **DE** (Vācija).

Jānorāda arī sekojošos iestatījumus Vācijai. Pēc iestatīšanas pabeigšanas noteikti palaidiet atbilstošus sadales darbus.

### <a name="set-up-vat-per-german-requirements"></a>Iestatīt PVN vācijas prasībām

Veidojiet PVN kodus, PVN grupas un krājumu PVN grupas. Ir jāiestata arī PVN informācija par produktiem un pakalpojumiem. Papildinformāciju par TO, kā iestatīt un izmantot PVN līdzekļus, skatiet [PVN pārskatā](../../finance/general-ledger/indirect-taxes-overview.md).

Pārdošanas kvītīs var drukāt saīsinātu PVN koda kodu (piemēram, "A" vai "B"). Lai padarītu šo funkcionalitāti pieejamu **, iestatiet kodu drukāšanai** lauku **PVN kodu** lapā.

### <a name="set-up-stores"></a>Veikalu iestatīšana

Lapā Visi **veikali** atjauniniet veikala informāciju. Iestatiet arī šādus parametrus:

- Laukā **PVN grupa** norādiet PVN grupu, kas jāizmanto pārdošanai noklusējuma debitoram.
- Iestatiet opciju **Cenās PVN iekļaut vērtību** Jā **·**.
- Uzņēmuma nosaukumam **laukā** iestatiet nosaukumu. Šīs izmaiņas palīdz pārliecināties, vai uzņēmuma nosaukums ir redzams pārdošanas kvītī. Alternatīvi pārdošanas kvīts izkārtojumam var pievienot uzņēmuma nosaukumu kā brīvas formas tekstu.
- Iestatiet nodokļa **identifikācijas koda (NIK)** lauku uzņēmuma identifikācijas numuram. Šīs izmaiņas palīdz pārliecināties, vai uzņēmuma identifikācijas numurs ir redzams pārdošanas kvītī. Alternatīvi uzņēmuma identifikācijas numuru var pievienot pārdošanas kvīts izkārtojumam kā brīvas formas tekstu.

### <a name="set-up-functionality-profiles"></a>Funkcionalitātes profilu iestatīšana

Iestatiet POS funkcionalitātes profilus. Kopsavilkuma cilnē **Kvīšu numerācija** iestatiet kvīšu numerāciju, **izveidojot** vai atjauninot pārdošanas, **pārdošanas pasūtījuma un** **atgriešanas saņemšanas** darbību tipu ierakstus.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurēt pielāgotos laukus, lai tos varētu izmantot pārdošanas ieejas plūsmu saņemšanas formātiem

Varat konfigurēt valodas tekstu un pielāgotos laukus, kas tiek izmantoti POS ieejas plūsmas formātos. Tā lietotāja noklusējuma uzņēmumam, kurš izveido saņemšanas iestatījumus, jābūt tai pašai juridiskajai personai, kurai tiek veidoti valodas teksta iestatījumi. Alternatīvi vienādi valodas teksti ir jāizveido gan lietotāja noklusējuma uzņēmumā, gan veikala juridiskajā personām, kam ir izveidots iestatījums.

**Lapā Valodas teksts** pievienojiet šādus ierakstus kvīts izkārtojumiem pielāgoto lauku etiķetēm. Ievērojiet, **ka tabulā parādītās** **valodas ID**, **teksta** ID un teksta vērtības ir tikai piemēri. Jūs varat mainīt tos tā, lai tie atbilstu jūsu prasībām. Taču jūsu izmantotajām **teksta ID** vērtībām ir jābūt unikālām un vienādām ar vai lielākam 900001.

Pievienojiet tālāk norādītās POS etiķetes lapas **Valodas teksts** POS **sadaļai**.

| Valodas kods | Teksta ID | Teksts                                  |
|-------------|---------|---------------------------------------|
| en-ASV       | 900001  | QR kods                               |
| en-ASV       | 900002  | Darbības ID                        |
| en-ASV       | 900003  | Nodokļu mazumtirdzniecības drukāšanas kods                 |
| en-ASV       | 900004  | Nodokļu summa (pārdošana)                    |
| en-ASV       | 900005  | Nodokļu bāze (pārdošana)                     |
| en-ASV       | 900006  | Transakcijas sākuma datums un laiks           |
| en-ASV       | 900007  | Transakcijas beigu datums un laiks             |
| en-ASV       | 900008  | Drošības elementa sērijas numurs |
| en-ASV       | 900009  | Parakstu skaitītājs                     |
| en-ASV       | 900010  | Pārbaudīt vērtību                           |
| en-ASV       | 900011  | Informācijas ziņojums                          |

Pielāgoto lauku **lapā pievienojiet** šiem ierakstiem kvīts izkārtojumu pielāgotajiem laukiem. Ievērojiet, **ka uzraksta teksta ID** vērtībām ir **jāatbilst teksta ID** vērtībām, kuras norādījāt **teksta** lapā Valoda.

| Vārds                            | Veids    | Uzraksta teksta ID |
|---------------------------------|---------|-----------------|
| QRCODEDE (datu kods\_)                      | Saņemšana | 900001          |
| TRANSACTIONIDDE\_               | Saņemšana | 900002          |
| RETAILPRINTCODEDE (TIKAI MAZUMTIRDZNIECĪBAS KODS\_)             | Saņemšana | 900003          |
| SALESTAXAMOUNTDE\_              | Saņemšana | 900004          |
| SALESTAXBASISDE\_               | Saņemšana | 900005          |
| TRANSACTIONSTARTDATETIMEDE\_    | Saņemšana | 900006          |
| TRANSACTIONENDDATETIMEDE\_      | Saņemšana | 900007          |
| SECURITYELEMENTSERIALNUMBERDE\_ | Saņemšana | 900008          |
| SIGNCOUNTERDE\_                 | Saņemšana | 900009          |
| PARAKSTĪTIES\_                        | Saņemšana | 900010          |
| INFOMESSAGEDE\_                 | Saņemšana | 900011          |

> [!NOTE]
> Ir svarīgi norādīt pareizos pielāgotos lauku nosaukumus, kā norādīts iepriekšējā tabulā. Nepareizs pielāgotā lauka nosaukums izraisīs ieejas plūsmās trūkstošo datu.

### <a name="configure-receipt-formats"></a>Konfigurēt ieejas plūsmas formātus

Katram pieprasītam kvīts formātam mainiet lauka Drukāšanas režīms **vērtību uz** Vienmēr **drukāt**.

Pievienojiet atbilstošajām saņemšanas sadaļām šādus pielāgotos laukus kvīts formāta veidotājā. Ievērojiet, ka lauku nosaukumi atbilst valodas tekstiem, kas definēti iepriekšējā sadaļā.

- **Virsraksts:** pievienojiet šādus laukus:

    - **Veikala nosaukuma** un nodokļa **identifikācijas koda** lauki, kas tiek izmantoti uzņēmuma nosaukuma un identifikācijas numura drukāšanai kvītīs. Vai arī varat pievienot uzņēmuma nosaukumu un identifikācijas numuru izkārtojumam kā brīvas formas tekstu.
    - **Veikala adrese**, datums **·**, laiks **24 h**, kvīts **numurs** un reģistra **numurs** lauki.

- **Rindas:** pievienojiet šādus laukus:

    - **Preces nosaukuma** lauks
    - **Daudzuma** lauks
    - **Kopējā cena ar nodokļa** lauku
    - **Lauks Nodokļu mazumtirdzniecības** drukāšanas kods, kas tiek izmantots, lai izdrukātu saīsināto kodu, kas atbilst precei piemērotajam PVN kodam

- **Kājene:** pievienojiet šādus laukus:

    - Maksājuma lauki, tādējādi maksājuma summas katrai maksājuma metodei tiek izdrukātas. Piemēram, pievienojiet laukus **Norēķinu nosaukums** **un Norēķinu** summa vienai izkārtojuma rindai.
    - Lauki lauku grupā **Nodokļu nodalīšana**. Visi šīs grupas lauki jādrukā uz vienas atsevišķas rindas.

        - **Nodokļa ID** lauks, kas ir standarta lauks, kas ļauj drukāt PVN kopsavilkumu katram PVN kodam. Lauks jāpievieno jaunai rindai.
        - **Lauks Nodokļa** procenti, kas ir standarta lauks, ko lieto, lai drukātu PVN koda efektīvo nodokļu likmi.
        - **Nodokļu bāzes (pārdošanas)** lauks, kuru izmanto, lai drukātu saņemšanas kopējo skaidras naudas pārdošanas summu PVN kodam. Priekšapmaksas un dāvanu karšu operācijas nav iekļautas.
        - **Pvn summas (pārdošanas)** lauks, kas tiek lietots, lai drukātu kvīts nodokļu summu par pārdošanu skaidrā naudā PVN kodam.
        - **Lauks Nodokļu mazumtirdzniecības** drukāšanas kods, kas tiek izmantots, lai izdrukātu saīsināto kodu, kas atbilst PVN kodam.

    - Lauki, kuros ir iekļauti droši darbību dati, ko atgriezis finanšu reģistrācijas pakalpojums:

        - **Darbības ID** lauks, kas norāda kases darbības numuru finanšu reģistrācijas pakalpojumā
        - **Transakcijas sākuma datuma un laika** lauks
        - **Transakcijas beigu datuma laika** lauks
        - **Drošības elementa lauka sērijas** numurs
        - **Paraksta skaitītāja** lauks
        - **Pārbaudīt vērtības** lauku
        - **QR koda** lauks, ko lieto, lai drukātu atsauci uz reģistrēto kases darbību QR koda formā

        > [!NOTE]
        > QR **koda vērtība** tiek izgūta no finanšu reģistra atbildes. EFR atgriež QR kodu tā atbildē tikai **tad**, ja atribūtu lauka vērtība EFR konfigurācijā ir aprakstīta EFSTA dokumentācijā. QR koda formāts Atribūtu **laukā** EFR konfigurācijā jāiestata uz **BMP**.

    - **Informācijas ziņojuma** lauks, lai paziņojumus no fiskālās reģistrācijas pakalpojuma varētu parādīt kvītīs. Piemēram, ja paraksta ierīce tiek bojāta, uz kvīts var drukāt īpašu tekstu.

Papildinformāciju par to, kā strādāt ar kvīšu formātiem, skatiet [sadaļā Kvīšu formātu iestatīšana un izstrāde](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Iestatīt Fiskālo integrāciju Vācijai

Fiskālo reģistrācijas pakalpojumu integrācijas paraugs Vācijai ir balstīts uz fiskālās [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no Retail SDK. Paraugs atrodas **Solutions repository mapē srcFiscalIntegrationEfr\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Paraugs sastāv [no](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālā dokumenta nodrošinātāja, kas ir Commerce Runtime () paplašinājums (CRT) un fiskālais savienotājs, kas ir Commerce Hardware Station paplašinājums. Papildinformāciju par to, kā izmantot retail SDK, skatiet mazumtirdzniecības [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[arhitektūrā un būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un [paplašinājuma modeļa ierobežojumu dēļ](../dev-itpro/build-pipeline.md) to pašlaik nevar izmantot šim fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātāja virtuālajā datorā (VM) pakalpojumos Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet Vācijas [finanšu integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-deu-fi-sample-sdk.md)
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

Veiciet fiskālās integrācijas iestatīšanas soļus, kā [aprakstīts Commerce kanālu finanšu integrācijas iestatīšanai](setting-up-fiscal-integration-for-retail-channel.md).

1. [Iestatīt fiskālās reģistrācijas procesu](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Atzīmējiet arī fiskālās reģistrācijas procesa iestatījumus, kas ir raksturīgi šim [fiskālās reģistrācijas pakalpojuma integrācijas paraugam](#set-up-the-registration-process).
1. [Iestatīt kļūdu apstrādes iestatījumus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Finanšu integrācijas struktūras kļūdu apstrādes iespējas, iespējams, nav pilnībā saskaņotas ar vietējiem finanšu noteikumiem.
    >
    > - Ieteicams **atstāt** **finanšu** reģistrācijas procesa lapā opciju Turpināt par kļūdu ir izslēgta, jo visām darbībām ir jābūt pareizi reģistrētam pat tad, ja pirmais fiskālās reģistrācijas mēģinājums neizdevās.
    > - Pirms **slēdzat** **·** **fiskālās** reģistrācijas procesa lapā opciju Izlaist vai Iezīmēt kā reģistrētu, šīs fiskālās reģistrācijas procesa izmaiņas ir apspriediet ar savu nodokļu konsultantu vai vietējo nodokļu biroju.

1. [Iespējojiet atliktās finanšu reģistrācijas manuālu izpildi](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurējiet kanāla komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Iestatīt reģistrācijas procesu

Lai iespējotu reģistrācijas procesu, izpildiet šīs darbības, lai iestatītu programmu Commerce Headquarters. Papildinformāciju skatiet [šeit: Komercijas kanālu finanšu integrācijas iestatīšana](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lejupielādēt konfigurācijas failus finanšu dokumentu nodrošinātājam un finanšu savienotājam:

    1. Atveriet risinājumu repozitoriju [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Atlasiet pareizu versijas izlaidi atbilstoši SDK/programmas versijai (piemēram, izlaidums **[/9,33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atvērt **src \> FiscalIntegration \> efr**.
    1. Lejupielādējiet finanšu dokumenta **nodrošinātāja konfigurācijas failu konfigurācijā \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** (piemēram, [fails laidienam/9,33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Lejupielādējiet finanšu savienotāja konfigurācijas failu **Konfigurācijas savienotājos \> ConnectorEFRSample.xml \> (piemēram,** fails laidienam/9,33 [...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Jaunā neatkarīgā iepakojuma un [paplašinājuma modeļa ierobežojumu dēļ](../dev-itpro/build-pipeline.md) to pašlaik nevar izmantot šim fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Šī fiskālās integrācijas parauga konfigurācijas faili atrodas tālākmintās Retail SDK mapēs LCS izstrādātāja VM:
    >
    > - **Finanšu dokumentu nodrošinātāja konfigurācijas fails:** RetailSdkSampleExtensionsCommerceRuntimeExtensions.DocumentProvider.EFRSampleConfigurationDocumentProviderFiscalEFRSampleGermany.xml\\\\\\\\\\
    > - **Finanšu savienotāja konfigurācijas fails:** RetailSdkSampleExtensionsHardwareStationExtension.EFRSampleConfigurationConnectorEFRSample.xml\\\\\\\\\\
    > 
    > Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce koplietotie parametri**. Cilnē Vispārīgi **iestatiet** opciju Aktivizēt **fiskālo integrāciju kā** **Jā**.
1. Dodieties uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas \> finanšu dokumentu nodrošinātājiem** un ielādējiet iepriekš lejupielādēto fiskālā dokumenta nodrošinātāja konfigurācijas failu.
1. Dodieties uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas \> finanšu savienotājiem** un ielādējiet agrāk lejupielādēto fiskālā savienotāja konfigurācijas failu.
1. Pārejiet uz **Sadaļu Mazumtirdzniecības un Commerce \> Channel Setup \> Finanšu integrācijas savienotāja \> funkcionālie profili**. Izveidojiet jaunu savienotāja funkcionalitātes profilu. Atlasiet dokumentu nodrošinātāju un iepriekš ielādēto savienotāju. Pēc vajadzības [atjauniniet datu kartēšanas](#default-data-mapping) iestatījumus.
1. Pārejiet uz **Retail un Commerce Channel \> setup \> Fiscal integration \> Connector tehniskajiem profiliem**. Izveidojiet jaunu savienotāja tehnisko profilu un atlasiet iepriekš ielādēto finanšu savienotāju. Pēc vajadzības [atjauniniet savienotāja](#fiscal-connector-settings) iestatījumus.
1. Pārejiet uz **sadaļu Mazumtirdzniecības un \> Commerce kanālu iestatīšanas \> finanšu integrācijas \> fiskālā savienotāja grupas**. Izveidojiet jaunu finanšu savienotāja grupu iepriekš izveidotajā savienotāja funkcionālajā profilā.
1. Pārejiet uz **Retail un Commerce \> Channel iestatīšanas finanšu \> integrācijas finanšu \> reģistrācijas procesiem**. Izveidojiet jaunu fiskālās reģistrācijas procesu un fiskālās reģistrācijas procesa soli un atlasiet iepriekš izveidoto finanšu savienotāja grupu.
1. Dodieties uz sadaļu **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Funkcionalitātes profili**. Atlasiet funkcionalitātes profilu, kas ir saistīts ar veikalu, kurā ir jāaktivizē reģistrācijas process. Kopsavilkuma cilnē **Finanšu reģistrācijas process** atlasiet iepriekš izveidoto finanšu reģistrācijas procesu.
1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**. Atlasiet aparatūras profilu, kas ir saistīts ar aparatūras staciju, ar kuru tiks pievienots fiskālais printeris. Kopsavilkuma cilnē **Finanšu perifērijas** ierīces atlasiet iepriekš izveidoto savienotāja tehnisko profilu.
1. Atveriet sadales grafiku (**Mazumtirdzniecības un Commerce \> Retail un Commerce IT \> sadales** grafiks) **un atlasiet darbus 1070** **un 1090**, lai pārsūtītu datus uz kanāla datu bāzi.

#### <a name="default-data-mapping"></a>Noklusējuma datu kartēšana

Tālāk redzamais noklusējuma datu kartējums ir ietverts finanšu dokumenta nodrošinātāja konfigurācijā, kas ir nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Norēķinu veida kartēšana** — maksājuma metožu kartēšana **uz PayG** (maksājumu grupas) atribūta vērtībām pieprasījumos, kas tiek nosūtīti finanšu pakalpojumam. Šeit ir noklusējuma kartēšana:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Pirmais komponents katrā pārī attiecas uz veikalam iestatīto maksāšanas metodi. Otrais komponents parāda atbilstošo maksājumu grupu, ko atbalsta EFR finanšu reģistrācijas pakalpojums. Plašāku informāciju par maksājumu grupām, ko EFR atbalsta Vācijai, skatiet [EFR atsauci](https://public.efsta.net/efr/).

    Maksājuma metožu parauga kartējums atbilst standarta demonstrācijas datos konfigurētajām maksāšanas metodēm.

    | Maksājuma metode | Maksāšanas metodes nosaukums |
    |----------------|---------------------|
    | 1              | Skaidra nauda                |
    | 2              | Atzīmēt               |
    | 3              | Karte                |
    | 4              | Debitora konts    |
    | 5              | Cita               |
    | 6              | Valūta            |
    | 7              | Dokuments             |
    | 8              | Dāvanu karte           |
    | 9              | Norēķina noņemšana/mainīšana |
    | 10.             | Lojalitātes programmas kartes       |
    | 11             | Nevietālas pārbaudes    |

    Tāpēc parauga kartējums ir jāpārveidojiet saskaņā ar maksājumu metodēm, kas ir konfigurētas programmā.

- **Iekļaut debitora** datus - ja šis parametrs ir ieslēgts, fiskālā pakalpojuma pieprasījumos būs iekļauta debitora informācija, piemēram, nosaukumi un adreses, gadījumos, kad debitoram tiek pievienots darbība.
- **Pievienotās vērtības nodokļa (PVN) likmju kartēšana -** to nodokļu procentu vērtību kartēšana, kas iestatīti PVN kodiem, uz vērtībām TaxG **(nodokļu grupa)** atribūtu pieprasījumos, kas tiek sūtīti finanšu pakalpojumiem. Šeit ir noklusējuma kartēšana:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Pirmais komponents katrā pārī norāda PVN nodokļu grupu, ko atbalsta EFR finanšu reģistrācijas pakalpojums. Otra sastāvdaļa norāda atbilstošo PVN likmi. Plašāku informāciju par PVN nodokļu grupām, ko EFR atbalsta Vācijai, skatiet [EFR atsauci](https://public.efsta.net/efr/).

- **Dāvanu karšu un depozītu** nodokļu grupa – **TaxG** atribūta vērtība pieprasījumos, kas tiek sūtīti finanšu pakalpojumiem, balstoties uz operācijām, kurās ir iesaistītas dāvanu kartes vai depozītus. Šeit ir noklusējuma kartēšana:

    ```
    G
    ```

- **Nodokļu grupa neapliekamiem** PVN – **TaxG** atribūta vērtība pieprasījumos, kas tiek nosūtīti finanšu pakalpojumiem, pamatojoties uz darbībām, kas ir atbrīvotas no nodokļu saistībām. Šeit ir noklusējuma kartēšana:

    ```
    F
    ```

> [!NOTE]
> Nodokļu iestatījumi noklusējuma datu kartēšanā ir atbildīgi par nodokļu iestatījumu atbilstību sistēmai un nodokļu grupām EFR pakalpojumā. PVN grupas var drukāt kvītīs tikai tad **, ja PVN** kodu lapā ir iestatīts drukāšanas **lauka** kods.

#### <a name="fiscal-connector-settings"></a>Finanšu savienotāja iestatījumi

Šādi iestatījumi ir iekļauti finanšu savienotāja konfigurācijā, kas tiek nodrošināta kā daļa no fiskālās integrācijas parauga:

- **Galapunkta** adrese – finanšu reģistrācijas pakalpojuma URL.
- **Taimauts** – laika daudzums milisekundēs, ko finanšu savienotājs gaidīs uz finanšu reģistrācijas pakalpojuma atbildi.
- **Rādīt finanšu reģistrācijas paziņojumus** – šis karodziņš kontrolē, vai tiek rādīti fiskālās reģistrācijas pakalpojuma atgriešanas paziņojumi operatoram.

### <a name="configure-channel-components"></a>Konfigurēt kanāla komponentus

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un [paplašinājuma modeļa ierobežojumu dēļ](../dev-itpro/build-pipeline.md) to pašlaik nevar izmantot šim fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Vācijas [finanšu integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-deu-fi-sample-sdk.md)
>
> Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

#### <a name="set-up-the-development-environment"></a>Iestatīt izstrādes vidi

Lai iestatītu izstrādes vidi un paplašinātu paraugu ņemšanas, veiciet šādus soļus.

1. Lejupielādējiet Solutions repozitoriju vai [Dynamics 365 Commerce lejupielādējiet](https://github.com/microsoft/Dynamics365Commerce.Solutions) to. Atlasiet pareizu filiāles versiju atbilstoši SDK/programmas versijai. Papildinformāciju skatiet lejupielādes [Retail SDK paraugos un atsauces pakotnēs no GitHub un NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atveriet EFR risinājumu dynamics365Commerce.SolutionsFiscalIntegrationEfrEFR.sln **\\\\\\** un izveidojiet to.
1. Instalēt Commerce Runtime paplašinājumus:

    1. Atrast paplašinājuma CRT instalētāju:

        - **Commerce Scale Unit:** mapē EfrScaleUnitScaleUnit.EFR.InstallerbinDebugnet461 **\\\\\\\\\\** atrodiet mapi ScaleUnit.EFR.Installer **installer.**
        - **CRT Modern POS lokāls:** **mapē EfrModernPOSModernPOS.EFR.InstallerbinDebugnet461\\\\\\\\\\** **atrodiet ModernPOS.EFR.Installer instalētāju.**

    1. Startējiet CRT paplašinājuma instalētāju no komandrindas:

        - **Commerce Scale vienība:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Lokāls CRT modernajā POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Instalēt finanšu savienotāja paplašinājumus:

    Aparatūras staciju vai POS kases [sistēmu var instalēt finanšu](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) savienotāja [paplašinājumus](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Instalēt aparatūras stacijas paplašinājumus:

        1. **Mapē EfrHardwareStationHardwareStation.EFR.InstallerbinDebugnet461\\\\\\\\\\ atrodiet** HardwareStation.EFR.Installer **installer.**
        1. Startējiet paplašinājuma instalētāju no komandrindas, palaižot šādu komandu.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Instalēt POS paplašinājumus:

        1. Atveriet POS **fiskālā savienotāja parauga risinājumu pie Dynamics365Commerce.SolutionsFiscalIntegrationPosFiscalConnectorSampleContoso.PosFiscalConnectorSample.sln\\\\\\** un izveidojiet to.
        1. **Mapē PosFiscalConnectorSampleStoreCommerce.InstallerbinDebugnet461\\\\\\\\** atrodiet mapi Contoso.PosFiscalConnectorSample.StoreCommerce.Installer **installer.**
        1. Startējiet paplašinājuma instalētāju no komandrindas, palaižot šādu komandu.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Ražošanas vide

Izpildiet [darbības](fiscal-integration-sample-build-pipeline.md), kas sadaļā Konveijers ir jāiestata fiskālās integrācijas parauga būvējuma konveijers, lai ģenerētu un izlaistu mākoņa mēroga vienību un pašapkalpošanās izvietojamos iepakojumus fiskālās integrācijas parauga iepakojumam. EFR būvējuma-pipeline.yml **veidnesLFML** **fails var tikt atrasts Risinājumu repozitorija \\** YAML_Files konveijera [Dynamics 365 Commerce mapē.](https://github.com/microsoft/Dynamics365Commerce.Solutions)

## <a name="design-of-extensions"></a>Paplašinājumu dizains

Fiskālo reģistrācijas pakalpojumu integrācijas paraugs Vācijai ir balstīts uz fiskālās [integrācijas funkcionalitāti](fiscal-integration-for-retail-channel.md) un ir daļa no Retail SDK. Paraugs atrodas **Solutions repository mapē srcFiscalIntegrationEfr\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (piemēram, [paraugs release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Paraugs sastāv [no](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskālā dokumenta nodrošinātāja, CRT kas ir Commerce Hardware Station paplašinājums un fiskālais savienotājs. Papildinformāciju par to, kā izmantot retail SDK, skatiet mazumtirdzniecības [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[arhitektūrā un būvējuma konveijera iestatīšana neatkarīgam iepakojuma SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Jaunā neatkarīgā iepakojuma un [paplašinājuma modeļa ierobežojumu dēļ](../dev-itpro/build-pipeline.md) to pašlaik nevar izmantot šim fiskālās integrācijas parauga modelim. Jums ir jāizmanto iepriekšējā Retail SDK versija izstrādātājam VM LCS. Papildinformāciju skatiet Vācijas [finanšu integrācijas parauga izvietošanas vadlīnijās (mantojuma).](emea-deu-fi-sample-sdk.md) Atbalsts jaunajam neatkarīgajam iepakojuma un paplašinājuma modelim finanšu integrācijas paraugos tiek plānots turpmākajām versijām.

### <a name="crt-extension-design"></a>CRT paplašinājuma dizains

Paplašinājuma, kas ir fiskālā dokumenta nodrošinātājs, nolūks ir izveidot pakalpojumiem raksturīgus dokumentus un apstrādāt atbildes no fiskālās reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

Dokumentu nodrošinātājam DocumentProviderEFRFiscalDEU **ir viens pieprasījumu apdarinātājs**. Šis apdarinātājs tiek lietots finanšu dokumentu ģenerēšanai finanšu reģistrācijas pakalpojumam. Tas ir pārmantots no **INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst savienotāja dokumentu nodrošinātāja nosaukumam, kas norādīts programmā Commerce Headquarters.

Savienotājs atbalsta šādus pieprasījumus:

- **GetFiscalDocumentDocumentProviderRequest —** šajā pieprasījumā ir ietverta informācija par to, kurš dokuments ir jāģenerē. Tas atgriež pakalpojumam raksturīgu dokumentu, kas jāreģistrē finanšu reģistrācijas pakalpojumā.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** - šis pieprasījums atgriež atbildi kopā ar paplašinātiem datiem.

#### <a name="configuration"></a>Konfigurācija

Fiskālā dokumenta nodrošinātāja **konfigurācijas fails atrodas solutions repozitorijā ir srcFiscalIntegrationEfrConfigurationsDocumentProvidersDocumentProviderFiscalEFRSampleGermany.xml\\\\\\\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Faila mērķis ir iespējot finanšu dokumentu nodrošinātāja iestatījumus, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

### <a name="hardware-station-extension-design"></a>Aparatūras stacijas paplašinājuma dizains

Paplašinājuma, kas ir fiskālais savienotājs, mērķis ir sazināties ar finanšu reģistrācijas pakalpojumu.

Aparatūras stacijas paplašinājums ir **HardwareStation.Extension.EFRSample**. Tas izmanto HTTP protokolu, lai iesniegtu dokumentus, CRT ko paplašinājums ģenerē finanšu reģistrācijas pakalpojumam. Tas apstrādā arī atbildes, kas saņemtas no fiskālās reģistrācijas pakalpojuma.

#### <a name="request-handler"></a>Pieprasījumu apdarinātājs

**EFRHandler pieprasījumu** apdarinātājs ir ieejas punkts finanšu reģistrācijas pakalpojuma pieprasījumu apstrādei. Šis apdarinātājs ir pārmantots **no INamedRequestHandler** interfeisa. Metode **HandlerName** ir atbildīga par apdarinātāja nosaukuma atgriešanu. Apdarinātāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

Savienotājs atbalsta šādus pieprasījumus:

- **SubmitDocumentFiscalDeviceRequest** – šis pieprasījums nosūta dokumentus finanšu reģistrācijas pakalpojumam un atgriež atbildi no tā.
- **IsReadyFiscalDeviceRequest** – šis pieprasījums tiek izmantots fiskālās reģistrācijas pakalpojuma veselības pārbaudei.
- **InitializeFiscalDeviceRequest** - šis pieprasījums tiek izmantots, lai inicializētu finanšu reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Finanšu savienotāja konfigurācijas **fails atrodas srcFiscalIntegrationEfrConfigurationsConnectorsConnectorEFRSample.xml\\\\\\\\\\**[Dynamics 365 Commerce risinājumu repozitorijā.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot finanšu savienotāja iestatījumus, kas jākonfigurē no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām.

### <a name="pos-fiscal-connector-extension-design"></a>POS finanšu savienotāja paplašinājuma dizains

POS fiskālā savienotāja paplašinājuma mērķis ir sazināties ar POS finanšu reģistrācijas pakalpojumu. Sakaru vajadzībām tas izmanto HTTPS protokolu.

#### <a name="fiscal-connector-factory"></a>Fiskālais savienotāja rūpnīca

Fiskālā savienotāja rūpnīca kartē savienotāja **nosaukumu finanšu savienotāja ieviešanai un atrodas failā Pos.ExtensionConnectorsFiscalConnectorFactory.ts\\\\**. Savienotāja nosaukumam ir jāatbilst programmā Commerce Headquarters norādītajam finanšu savienotāja nosaukumam.

#### <a name="efr-fiscal-connector"></a>EFR finanšu savienotājs

EFR finanšu savienotājs ir novietots **failā Pos.ExtensionConnectorsEfrEfrFiscalConnector.ts\\\\\\**. Tas ievieš **IFiscalConnector interfeisu**, kas atbalsta šādus pieprasījumus:

- **FiscalRegisterSubmitDocumentClientRequest** – šis pieprasījums nosūta dokumentus finanšu reģistrācijas pakalpojumam un atgriež atbildi no tā.
- **FiscalRegisterIsReadyClientRequest** – šis pieprasījums tiek izmantots finanšu reģistrācijas pakalpojuma veselības pārbaudei.
- **FiscalRegisterInitializeClientRequest** — šis pieprasījums tiek izmantots, lai inicializētu finanšu reģistrācijas pakalpojumu.

#### <a name="configuration"></a>Konfigurācija

Konfigurācijas fails atrodas **srcFiscalIntegrationEfrConfigurationsConnectors\\\\\\\\**[Dynamics 365 Commerce mapē Solutions repository.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faila mērķis ir iespējot iestatījumus finanšu savienotājam, lai tos konfigurētu no programmas Commerce Headquarters. Faila formāts ir saskaņots ar finanšu integrācijas konfigurācijas prasībām. Ir pievienoti šādi iestatījumi:

- **Galapunkta** adrese – finanšu reģistrācijas pakalpojuma URL.
- **Taimauts** – laiks milisekundēs, ko savienotājs gaidīs uz finanšu reģistrācijas pakalpojuma atbildi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
