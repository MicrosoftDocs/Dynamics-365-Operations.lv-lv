---
title: Sistēmas noteikta darbu secība
description: Šajā tēmā ir sniegta informācija par sistēmas noteiktu darbu secību. Šī funkcija sniedz iespēju kārtot un filtrēt darba pasūtījumus, kurus sistēma sniedz lietotājiem izpildei. Tas noder scenārijos, kad ir nepieciešami papildu kritēriji, lai virzītu noliktavas izdošanas procesu.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3811486a31d079cac7f7c27ea6323f16de4478d5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970210"
---
# <a name="system-directed-work-sequencing"></a>Sistēmas noteikta darbu secība

[!include [banner](../includes/banner.md)]

Sistēmas noteikta darbu secība ļauj kārtot un filtrēt darba pasūtījumus, kurus sistēma piedāvā lietotājiem izpildei. Tas noder scenārijos, kad ir nepieciešami papildu kritēriji (piemēram, nosūtīšanas laiks, izdošanas zona, vietas profils vai dažādu kritēriju kombinācija), lai virzītu noliktavas izdošanas procesu.

Šī funkcionalitāte paplašina pašreizējo sistēmas virzīto izdošanas funkcionalitāti, pievienojot sistēmas virzītu vaicājumu secību, kur lietotāji var iestatīt secību un vienu vai vairākus vaicājumus, kas novērtēs visus izveidotos darba pasūtījumus. Tiks saglabāti un parādīti tikai tie darba pasūtījumi, kas atbilst mobilās ierīces izvēlnes vienuma iestatīšanā norādītajiem kritērijiem.

Tāpēc šī funkcionalitāte ļauj veikt tālāku noliktavas izdošanas procesu optimizāciju, jo tajā tiek identificēti darba pasūtījumi, kas atbilst norādītajiem kritērijiem, tie tiek piešķirti pareizajam mobilās ierīces izvēlnes vienumam un pēc tam parādīti darbiniekam, pamatojoties uz noteiktu prasmju kopu, izdošanas aprīkojumu vai citām prasībām.

> [!NOTE]
> Ja ir nepieciešami atšķirīgi kritēriji, ir jāizmanto vairāki mobilās ierīces izvēlnes vienumi.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Ieslēdziet līdzekli Organizācijas līmeņa sistēmas noteikta darba secība

Lai varētu izmantot līdzekli Sistēmas noteikta darba secība, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Organizācijas līmeņa sistēmas noteikta darba secība*

## <a name="setup"></a>Iestatīt

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Lai strādātu ar scenāriju, izmantojot šajā tēmā norādītās vērtības, ir jāstrādā ar sistēmu, kurā ir instalēti standarta demonstrācijas dati. Turklāt ir jāatlasa **USMF** juridiskā persona. Scenārijā tiek izmantota noliktava nr. *51* no demonstrācijas datiem.

> [!IMPORTANT]
> Pirms pasūtījumu izdošanas noliktavā pārliecinieties, vai izdošanas vietās ir pietiekami daudz krājumu visām precēm pasūtījumos.
>
> Noklusējuma USMF datiem ir jāatbalsta šis scenārijs. Ja neizmantojat demonstrācijas datus, pārskatiet **Novietojuma direktīvas** iestatījumu, lai uzzinātu, kuras izdošanas vietas tiek izmantotas pārdošanas pasūtījuma izdošanai. Pielāgojot krājumus, varat izveidot manuālo kustību, izmantot papildināšanu vai jebkuru citu plūsmu.

### <a name="set-up-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes vienuma iestatīšana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Mobilās ierīces izvēlnes vienumu sarakstā atlasiet **Pārdošanas izdošana — Sistēma**. Nepieciešamajam izvēlnes vienumam jau vajadzētu pastāvēt. 
1. Apstipriniet tālāk minētos iestatījumus.

    - **Vispārīgās** kopsavilkuma cilnes laukā **Noteica:** ir jāiestata vērtība *Sistēmas noteikts*.
    - Kopsavilkuma cilnē **Darba klases** vajadzētu būt redzamiem tālāk norādītajiem iestatījumiem.

        | Darba klases ID | Darba pasūtījuma veids |
        |---|---|
        | Pārdošana | Pārdošanas pasūtījumi |
        | Pārdošanas pasūtījuma izdošana | Pārdošanas pasūtījumi |

1. Darbības rūtī atlasiet **Sistēmas noteikti darba secības vaicājumi**.
1. Atlasiet **Rediģēt**.
1. Izdzēsiet esošo rindu un pēc tam atlasiet **Jā**, lai apstiprinātu darbību.
1. Lai izveidotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Secības numurs:** *1*
    - **Apraksta lauks:** *Darba daudzums mazāks par 20 un dilstošs*

1. Atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Cilnē **Savienojumi** izvērsiet savienojumu hierarhiju, lai parādītu tabulu **Darba rindas**.
1. Atlasiet tabulu savienojumu **Darba rindas**.
1. Atlasiet **Pievienot tabulu savienojumu**.
1. Tiks parādīts saraksts. Tajā atrodiet un atlasiet rindu, kurai ir tālāk norādītie iestatījumi:

    - **Savienojuma režīms:** *n:1*
    - **Relācija:** *vietas (vieta)*

1. Atlasiet **Atlasīt**.

    Vietas ir pievienotas savienojumu tabulai.

1. Cilnē **Kārtošana** atlasiet **Pievienot**, lai pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Darba daudzums* (paradītajā ziņojumu lodziņā atlasiet **Jā**, lai šim laukam pievienotu kārtošanu.)
    - **Meklēšanas virziens:** *Dilstošā secībā*

1. Atlasiet cilni **Diapazons**.

    Ja secībā ir jāiekļauj tikai noteikt darba kritēriji, tos varat norādīt cilnē **Diapazons**. Šajā piemērā jūs vēlaties iekļaut tikai to darbu, kur daudzums ir mazāks par 20 ea (viszemākā mērvienība).

    Ņemiet vērā, ka dažas rindas jau ir iekļautas. Šīs rindas nedrīkst noņemt.

1. Lai pievienotu rindu, atlasiet **Pievienot**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Krājumu darba daudzums*
    - **Kritēriji:** *\<20* (mazāk par 20)

1. Lai pievienotu vēl vienu rindu, atlasiet **Pievienot**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Darba rindas*
    - **Atveidotā tabula:** *Darba rindas*
    - **Lauks:** *Darba veids*
    - **Kritēriji:** *Izdošana*

1. Lai pievienotu vēl vienu rindu, atlasiet **Pievienot**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Atvasinātā tabula:** *Vietas*
    - **Lauks:** *Atrašanās vietas profila ID*
    - **Kritēriji:** *!STAGE*

        > [!IMPORTANT]
        > Vienuma *STAGE* priekšā noteikti pievienojiet izsaukuma zīmi (*!*).

1. Atlasiet **Labi**, lai saglabātu un aizvērtu vaicājumu.
1. Atlasiet **Saglabāt**.
1. Aizveriet lapu, lai atgrieztos lapā **Mobilās ierīces izvēles vienumi**.

> [!NOTE]
> Šis iestatījums definē, kādi kritēriji tiks izmantoti, lai mobilās ierīces izvēlnes vienumā ievietotu piemēroto darbu. Ja vaicājumam pievienosit vairākas kritēriju rindas, sistēma vispirms izmantos vaicājuma rindu ar viszemāko kārtas numuru. Citiem vārdiem sakot, lietotājam vispirms tiks rādīts viss 1. kārtas numuram piemērotais darbs un pēc tam viss 2. kārtas numuram piemērotais darbs. Tāpēc, ja kopā ir jāizmanto konkrēts diapazons un kārtošana, tie ir jānorāda tajā pašā sistēmas vadītajā darbu secības vaicājumā.
>
> Ar šo iestatījumu tiks nolasīts visa veida darbs, kurā ir vismaz viena rinda ar daudzumu, kas mazāks par 20 ea. Tāpēc, ja darbā ir rinda, kur daudzums ir precīzi 20 ea vai vairāk nekā 20 ea, tā būs derīga, pieņemot, ka darbā ir arī rinda, kuras daudzums ir mazāks par 20 ea.

### <a name="location-directives"></a>Vietas direktīvas

Ja izmantojat noklusējuma Contoso datus, novietojuma direktīvas darbības vaicājumam nebūs nepieciešamas izmaiņas. Tomēr, lai būtu drošs, ka novietojuma direktīvas nolasa pārdošanas pasūtījumos ietvertos vienumus, kad lietojat līdzekli vidē, kas nav Contoso, izveidojiet jaunu vietas direktīvu. Lai demonstrācijas vidē pārbaudītu iestatījumus, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas vadība** \> **Iestatīšana** \> **Novietojuma direktīvas**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.
1. Atlasiet novietojuma direktīvu ar nosaukumu *51. izdošana*.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** darbībai **Izdošana** atlasiet jaunu rindu.
1. Virs režģa atlasiet komandu **Rediģēt vaicājumu**.
1. Pārskatiet vaicājumu **Diapazons**.

    1. Atrodiet rindu, kurā laukam **Lauks** ir iestatīta vērtība *Novietojums*.
    2. Pārbaudiet, vai lauks **Kritēriji** ir tukšs (vai tajā nav ierobežojumu).

## <a name="scenario"></a>Scenārijs

### <a name="create-sales-order-picking-work"></a>Izveidojiet pārdošanas pasūtījuma izdošanas darbu

Pirms sistēmas vadītas izdošanas izpildes ir jāizveido izejošais darbs. Šim scenārijam izveidojiet četrus pārdošanas pasūtījumus, kuru pamatā ir norādītie sistēmas vadītās darbu secības vaicājumi.

Katram pārdošanas pasūtījumam rezervējiet krājumu daudzumus. Līdz ar to rezervēto krājumu nevar izņemt no noliktavas citiem pasūtījumiem, ja vien netiek atcelta šī krājuma rezervācija vai daļa no krājuma rezervācijas.

Pēc tam izlaidiet noliktavā katru pārdošanas pasūtījumu, lai izveidotu izejošo darbu.

#### <a name="sales-order-1"></a>1. pārdošanas pasūtījums

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Lai izveidotu 1. pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - Sadaļā **Klients** laukam **Klienta konts** iestatiet vērtību *US-004*.
    - Sadaļā **Vispārīgi** laukam **Noliktava** iestatiet vērtību *51*.

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu. Pierakstiet pārdošanas pasūtījuma numuru.
1. Pievienojiet rindu jaunajam pārdošanas pasūtījumam un iestatiet tālāk norādītās vērtības.

    - **Krājuma numurs:** *M9200*
    - **Daudzums:** *20*

1. Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
1. Aizveriet lapu **Rezervācija**.
1. Darbību rūts cilnē **Noliktava** atlasiet **Pārvietot uz noliktavu**, lai noliktavai izveidotu darbu.

    Tiks saņemti informatīvi ziņojumi, kuros būs norādīts pārdošanas pasūtījumam izveidotais kopuma ID un sūtījuma ID.

#### <a name="sales-order-2"></a>2. pārdošanas pasūtījums

1. Lai izveidotu 2. pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-007*
    - **Noliktava:** *51*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu. Pierakstiet pārdošanas pasūtījuma numuru.
1. Pievienojiet rindu jaunajam pārdošanas pasūtījumam un iestatiet tālāk norādītās vērtības.

    - **Krājuma numurs:** *M9200*
    - **Daudzums:** *5*

1. Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:

    - **Krājuma numurs:** *M9201*
    - **Daudzums:** *1*

1. Rezervējiet krājumus abām rindām.
1. Izlaidiet pasūtījumu noliktavā.

#### <a name="sales-order-3"></a>3. pārdošanas pasūtījums

1. Lai izveidotu 3. pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-009*
    - **Noliktava:** *51*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu. Pierakstiet pārdošanas pasūtījuma numuru.
1. Pievienojiet rindu jaunajam pārdošanas pasūtījumam un iestatiet tālāk norādītās vērtības.

    - **Krājuma numurs:** *M9200*
    - **Daudzums:** *7*

1. Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:

    - **Krājuma numurs:** *M9202*
    - **Daudzums:** *8*

1. Rezervējiet krājumus abām rindām.
1. Izlaidiet pasūtījumu noliktavā.

#### <a name="sales-order-4"></a>4. pārdošanas pasūtījums

1. Lai izveidotu 4. pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-010*
    - **Noliktava:** *51*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu. Pierakstiet pārdošanas pasūtījuma numuru.
1. Pievienojiet rindu jaunajam pārdošanas pasūtījumam un iestatiet tālāk norādītās vērtības.

    - **Krājuma numurs:** *M9200*
    - **Daudzums:** *25*

1. Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:

    - **Krājuma numurs:** *M9202*
    - **Daudzums:** *10*

1. Rezervējiet krājumus abām rindām.
1. Izlaidiet pasūtījumu noliktavā.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Darba ID iegūšana izveidotajam darbam

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Laukā **Noliktava** veiciet filtrēšanu tā, lai darbs tiktu rādīts tikai noliktavai nr. *51*.
1. Ir jābūt izveidotiem četriem darba ID: Pierakstiet katra pārdošanas pasūtījuma darba ID.

    | Pārdošanas pasūtījuma ID | Darba ID | Darba daudzums |
    |---|---|---|
    | 1. pārdošanas pasūtījums | 1. darba ID | 20 ea |
    | 2. pārdošanas pasūtījums | 2. darba ID | 6 ea (abu rindu summa) |
    | 3. pārdošanas pasūtījums | 3. darba ID | 15 ea (abu rindu summa) |
    | 4. pārdošanas pasūtījums | 4. darba ID | 35 ea (abu rindu summa) |

Pirms plūsmas izpildes mobilajā ierīcē pārliecinieties, vai tikko izveidotā darba noliktavas nr. *51* un darba pasūtījuma tipa *Pārdošanas pasūtījums* statuss ir *Atvērts*. Pretējā gadījumā testa rezultāti var atšķirties, jo sistēmas tiešajā izdošanā tiks iekļauts viss piemērotais darbs.

1. Atveriet **Noliktavas pārvaldība \> Darbs \> Izejošs \> Atvērts pārdošanas darbs**.
1. Režģī **Atvērts pārdošanas darbs** laukā **Noliktava** veiciet filtrēšanu tā, lai darbs tiktu rādīts tikai noliktavai nr. *51*.
1. Pārliecinieties, vai tiek rādīti tikai iepriekš izveidotie četri darba ID.
1. Aizveriet lapu **Darbs**.

### <a name="mobile-device-flow-execution"></a>Mobilās ierīces plūsmas izpilde

Ņemot vērā iestatījumu, sistēma rādīs lietotāja darbu, kas tiek kārtots no augstākās darba rindas daudzuma uz zemāko. Daudzums katrā rindā būs mazāks par 20 ea.

Ņemiet vērā, ka ar šo iestatījumu tiks nolasīts visa veida darbs, kurā ir vismaz viena rinda ar daudzumu, kas mazāks par 20 ea. Līdz ar to, ja darbam ir cita rinda, kuras daudzums ir tieši 20 ea vai vairāk par 20 ea, arī tā būs derīga.

#### <a name="mobile-app"></a>Mobilā programma

1. Pierakstieties noliktavas programmā kā lietotājs noliktavā *51*.
1. Atveriet **Izejošs \> Pārdošanas izdošana – Sistēma**.

    Tiek rādīts *4.*  darba ID izdošanas solis. Šis darba ID tiek rādīts vispirms sistēmas noteikta vaicājuma pasūtījuma iestatīšanas dēļ, kur jūs norādījāt, ka darba secība ir jāveido, ņemot vērā darba rindu daudzumu dilstošā secībā.

1. Pabeidziet nepieciešamo izdošanu un novietojiet, lai aizvērtu darba ID.

    Pēc tam tiek rādīts *3.*  darba ID. Viena no tā darba rindām ir nākamā secībā, ņemot vērā darba rindas daudzumu.

1. Pabeidziet izdošanu un novietojiet, lai aizvērtu darba ID.

    Pēc tam tiek rādīts *2.*  darba ID. Šī darba izdošanas rinda ir nākamā secībā.

1. Pabeidziet izdošanu un novietojiet, lai aizvērtu darba ID.

    Cits darbs jums vairs netiks rādīts. *1.*  darba ID šim mobilās ierīces izvēlnes vienumam nav piemērots, jo vaicājumā ir norādīts, ka darba galvenes tiek ņemtas vērā tikai tad, ja darba rindu daudzums ir mazāks par 20 ea.

## <a name="tips"></a>Padomi

Sistēmas norādītie darbu secības vaicājumi ir *iekļauti*. Šo faktu ir svarīgi atcerēties dažiem iestatījumiem. Piemēram, jūs vēlaties, lai konkrēts izvēlnes vienums apstrādā tikai to darbu, kur darba vienība ir *ea*, un jūs šo ierobežojumu norādāt vaicājuma cilnē **Diapazons**. Šajā gadījumā darbiniekam tiks parādīts viss darbs, kur vismaz vienā darba rindā kādai darba vienībai būs iestatīts *ea*. Tāpēc šajā darbā var būt ietverts arī darbs, kurā darba rindām būs cits darba vienības iestatījums, nevis *ea* (piemēram, *kaste* vai *palete*). Vaicājums izslēgs tikai to darbu, kur nevienai darba rindai nebūs darba vienības ar iestatījumu *ea*.

Tāpēc šī scenārija piemērā vaicājumā bija iekļauts arī *4.*  darba ID. Pēc tā izveidošanas tika pievienotas divas rindas: viena iestatījumam 25 ea un otra — 10 ea. Darbs vienalga tika rādīts darbiniekam, jo vismaz vienā darba rindā iekļautais daudzums bija mazāks par 20 ea.

Atkarībā no scenārija varat novērst šādu norisi, izmantojot darba pārtraukumus.
