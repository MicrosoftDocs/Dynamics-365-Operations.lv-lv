---
title: Kārtula Pārvietot uz noliktavu
description: Šajā tēmā ir sniegta informācija par Pārvietošanas uz noliktavu kārtulu, kas nodrošina elastību, veicot izlaišanu noliktavā. Tas pievieno konfigurācijas opciju, kas kontrolē, vai sistēma ļauj izlaist daļēji rezervētās pasūtījumu rindas.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 27030e8dd58b290d80f6b00cbd250e09c1e50819
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432572"
---
# <a name="release-to-warehouse-rule"></a>Kārtula Pārvietot uz noliktavu

[!include [banner](../includes/banner.md)]

Līdzeklis *Pārvietošanas uz noliktavu kārtula* nodrošina elastību, izlaižot to noliktavā. Tā katrai noliktavai pievieno konfigurācijas opciju. Varat izmantot šo opciju, lai norādītu, vai šai noliktavai var nodot daļēji rezervētas pasūtījuma rindas. Funkcija darbojas kopā ar uzlaboto pārkraušanu sadales centrā gadījumos, kad daļa no pasūtījuma rindas daudzuma ir atzīmēta pret piegādes avotu, bet atlikušo daļu var apstrādāt noliktavā. Tāpēc rindu var izlaist, lai varētu turpināt noliktavas apstrādāšanu ar pieejamo krājumu daudzumu.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Ieslēgt un inicializēt līdzekli Pārvietošanas uz noliktavu kārtula

### <a name="turn-on-the-feature"></a>Līdzekļa iespējošana

Lai varētu izmantot līdzekli *Papildu novietojuma zona*, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Iezīmes nosaukums:** *Noliktavas izlaišanas kārtula*

### <a name="initialize-the-feature"></a>Inicializējiet līdzekli

Pēc līdzekļa iespējošanas jūsu sistēmā tas ir jāinicializē, lai iestatītu noteikumu uz pareizo sākotnējo statusu visām noliktavām.

- Noliktavām, kas nav iespējotas noliktavas pārvaldībai, noteikums sākotnēji ir iestatīts kā **Nav piemērojams**.
- Noliktavām, kas nav iespējotas noliktavas pārvaldībai, noteikums sākotnēji ir iestatīts kā **Ļaut daļēju rezervēšanu**

Lai inicializētu līdzekli un iestatītu nodošanu noliktavas kārtulai visām noliktavām, izpildiet tālāk norādītās darbības.

1. Doties uz **Noliktavas vadība \> Iestatīšana \> Noliktavas vadības parametri**.
1. Cilnes **Vispārīgi** sadaļā **Noliktavas pārvaldības parametri**, kas atrodas sadaļā **Uzņēmuma informācija**, atlasiet saiti kārtulai **Inicializēt izlaišanu noliktavā**. (Ja šī saite netiek rādīta, šis līdzeklis nav ieslēgts vai arī tas jau ir inicializēts.)
1. Kad tiek parādīta uzvedne ar aicinājumu apstiprināt darbību, atlasiet **Jā**, lai inicializētu līdzekli.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Iestatīt katras noliktavas nodošanas noliktavas kārtulu

Pēc tam, kad līdzeklis ir ieslēgts un inicializēts, visām noliktavām būs sākotnējais iestatījums, kā aprakstīts iepriekšējā sadaļā. Šo iestatījumu var mainīt atsevišķām noliktavām, veicot šādas darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Noliktavas**.
1. Atlasiet noliktavu, lai konfigurētu to.
1. Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.
1. Kopsavilkuma cilnes **Noliktava** sadaļā **Rezervācijas** lauks **Krājuma rezervācijas prasība** kontrolē, vai ir atļauta daļēja pasūtījumu izpilde. Atlasiet vienu no šīm vērtībām:

    - **Nav piemērojams** – kad šis līdzeklis ir pirmo reizi ieslēgts un inicializēts, šī vērtība tiek automātiski piešķirta visām noliktavām, kas nav iespējotas noliktavas pārvaldībai. To nevar mainīt. Šī vērtība nav pieejama noliktavām, kas ir iespējotas noliktavas pārvaldībai.
    - **Atļaut daļēju rezervāciju** — pasūtījumus var izlaist, ja ir rezervēts kāds daudzums. Sistēma novērtēs, vai nerezervētais daudzums ir jāatzīmē izvērstai pārkraušanai sadales centrā un šis daudzums tiks atzīmēts kā nepieciešams. Ja nav iezīmēšanu, sistēma izveidos darbu tikai rezervētajam daudzumam. Kad šis līdzeklis ir pirmo reizi ieslēgts un inicializēts, šī vērtība tiek automātiski piešķirta visām noliktavām, kas ir iespējotas noliktavas pārvaldībai. Šī vērtība nav pieejama noliktavām, kas nav iespējotas noliktavas pārvaldībai.
    - **Pieprasīt pilnu rezervāciju** — pasūtījumus var izlaist tikai tad, ja viss daudzums ir rezervēts. Tās nevar izlaist, ja kopējais daudzums nav fiziski rezervēts vai plānots pārkraušanai sadales centrā. Šī vērtība nav pieejama noliktavām, kas nav iespējotas noliktavas pārvaldībai.

1. Atlasiet **Saglabāt**.

## <a name="scenarios"></a>Scenāriji

Šajā sadaļā ir sniegti divi scenāriji, ar kuriem var strādāt, lai uzzinātu, ko līdzeklis dara un kā to lietot.

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šos scenārijus, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

Varat izmantot šo demonstrāciju arī kā vadlīnijas šī līdzekļa izmantošanai, strādājot ar ražošanas sistēmu. Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>1. scenārijs: pieprasīt pilnu laidienu (nav plānotas pārkraušanas sadales centrā)

Šis scenārijs parāda, kā līdzeklis darbojas noliktavām, kas iestatītas, lai **Pieprasītu pilnīgu rezervāciju**.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Noliktavas**.
1. Noliktavas _62_ iestatiet lauku **Prasība krājuma rezervēšanai** uz **Pieprasīt pilnīgu rezervāciju**, kā aprakstīts šīs tēmas iepriekš minētajā sadaļā [Iestatīt pārvietošanas uz noliktavu kārtulu katrai noliktavai](#set-option-warehouse).
1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - Kopsavilkuma cilnē **Klients** iestatiet laukam **Klienta konts** vērtību _US-004_.
    - Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību _62_.

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu un izveidotu jaunu pirkšanas pasūtījumu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tam ir jāietver jauna, tukša rinda režģī kopsavilkuma sadaļā **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *2*

1. Atlasiet **Pievienot rindu**, lai pievienotu jaunu rindu, un iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0002*
    - **Daudzums:** *2*

1. Atlasiet pirmo pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Nerezervēt otro pasūtījuma rindu.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.
1. Ievērojiet, ka tiek parādīts šāds kļūdas ziņojums: "Pilns daudzums ir fiziski jārezervē." Tāpēc sistēma neveido nekādu darbu, sūtījumu vai noslodzi pasūtījumam.

    > [!NOTE]
    > Jūs saņemsiet to pašu kļūdas ziņojumu, ja jūs daļēji rezervējat otro rindu.

### <a name="scenario-2-allow-partial-release"></a>2. scenārijs: Atļaut daļēju pārvietošanu

Šis scenārijs parāda, kā līdzeklis darbojas noliktavām, kas iestatītas, lai **Pieprasītu daļēju pārvietošanu**.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Noliktavas**.
1. Noliktavai _62_ iestatiet lauku **Prasība krājuma rezervēšanai** uz **Pieprasīt daļēju rezervāciju**, kā aprakstīts šīs tēmas iepriekš minētajā sadaļā [Iestatīt pārvietošanas uz noliktavu kārtulu katrai noliktavai](#set-option-warehouse).
1. Kā darījāt [iepriekšējā scenārijā](#scenario1), dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu klienta kontam _ASV-004_ no noliktavas _62_. Pievienojiet šādas divas pasūtījuma rindas:

    - **1. rinda:** Iestatiet lauku **Krājuma numurs** uz _A0001_, lauku **Daudzums** uz _2_ un lauku **Vienība** uz _Gab_.
    - **2. rinda:** Iestatiet lauku **Krājuma numurs** uz _A0002_, lauku **Daudzums** uz _2_ un lauku **Vienība** uz _Gab_.

1. Kā darījāt [iepriekšējā scenārijā](#scenario1), rezervējiet pilnu daudzumu pasūtījuma rindai 1, bet nerezervējiet 2. pasūtījuma rindu.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.
1. Ievērojiet, ka pašlaik netiek saņemts kļūdas ziņojums. Tā vietā sistēma izveido darbu, sūtījumus un noslodzes, kā prasīts, un parāda rezultātus.
1. Lai skatītu sūtījuma, noslodzes un darba informāciju, izmantojiet opcijas **Noliktavas** izvēlnē virs režģa:

    - **1. rinda:** Ir pieejamas trīs opcijas: **Detalizēta informācija par piegādi**, **Detalizēta informācija par kravu** un **Detalizēta informācija par darbu**. Atlasiet katru opciju, lai skatītu detalizētu informāciju par sūtīšanu, noslodzi un darbu, kas tika izveidots, kad pasūtījums tika nodots noliktavai.
    - **2. rinda:** Ir pieejama tikai opcija **Detalizēta informācija par darbu**. Atlasiet to un ievērojiet, ka darbs nav izveidots, jo nav rezervēts neviens krājums. Tāpēc netika izveidota sūtīšana vai noslodze.

> [!NOTE]
> Tas pats rezultāts tiek prognozēts, kad otrā rinda ir daļēji rezervēta. Šādā gadījumā tiks izveidots darbs rezervētās rindas daudzumam, bet ne nerezervētajam daudzumam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]