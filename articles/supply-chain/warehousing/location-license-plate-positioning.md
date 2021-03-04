---
title: Novietojuma noliktavas vienības pozīcija
description: Noliktavas vienības novietojuma pozīcija ļauj skatīt, kur noliktavas vienība atrodas vairākpalešu novietojumā, piemēram, vietā, kur izmanto dubultdziļus palešu plauktus.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7b0ebfb965e5a8f1bfe1857a9642d998dac2faf3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433100"
---
# <a name="location-license-plate-positioning"></a>Novietojuma noliktavas vienības pozīcija

[!include [banner](../includes/banner.md)]

Noliktavas vienības novietojuma pozīcija ļauj skatīt, kur noliktavas vienība atrodas vairākpalešu novietojumā, piemēram, vietā, kur izmanto dubultdziļus palešu plauktus.

Līdzeklis pievieno secības numuru katrai noliktavas vienībai, kas tiek ievietota glabāšanas vietā. Secības numurs tiek izmantots, lai sakārtotu noliktavas vienības glabāšanas vietā. Tāpēc šis līdzeklis pārdomāti atbalsta scenārijus, kuros klienti izmanto gravitācijas plauktu sistēmu, kā arī izdošanas nolūkos tiem ir jāzina, kura noliktavas vienība ir priekšējā.

Šī tēma iepazīstina ar scenāriju, kas parāda, kā iestatīt un izmantot līdzekli.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>Novietojuma noliktavas vienības pozīcijas līdzekļa ieslēgšana

Lai varētu izmantot noliktavas vienības novietojuma pozīciju, līdzeklim ir jābūt iespējotam sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Novietojuma noliktavas vienības pozīcija*

## <a name="example-scenario"></a>Piemēra situācija

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai strādātu ar šo scenāriju, izmantojot šeit piedāvātās vērtības, ir jāstrādā ar sistēmu, kurā ir instalēti datu paraugi. Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

### <a name="set-up-the-feature-for-this-scenario"></a>Iestatīt līdzekli šim scenārijam

Izpildiet šādas procedūras, lai iestatītu līdzekli *Novietojuma noliktavas vienības pozīcija* scenārijam šajā tēmā.

#### <a name="location-profiles"></a>Atrašanās vietu profili

Līdzeklim ir jābūt iespējotam novietojuma profilā katrai atrašanās vietai, kurā tas tiks izmantots.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.
1. Novietojuma profilu saraksta kreisajā rūtī atlasiet **LIELAPJOMA-06**.
1. Kopsavilkuma cilnē **Vispārīgi** līdzeklis ir pievienojis divas jaunas opcijas. Iestatiet šādas vērtības:

    - **Iespējot noliktavas vienības pozīciju:** *Jā*

        Kad šī opcija ir iestatīta uz *Jā*, noliktavas vienības pozīcija tiek uzturēta noliktavas vienībām šajā novietojumā.

    - **Rādīt mobilās ierīces LP pozīciju:** *Jā*

        Kad šī opcija ir iestatīta uz *Jā*, noliktavas vienības pozīcija tiek rādīta mobilās ierīces lietotājiem korekcijas un inventarizācijas laikā. Opcijas iestatījumu var mainīt tikai tad, kad līdzeklis ir ieslēgts.

1. Atlasiet **Saglabāt**.

#### <a name="location-directives"></a>Vietas direktīvas

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.
1. Kreisajā rūtī pārliecinieties, ka lauks **Darba pasūtījuma veids** ir iestatīts uz *Pārdošanas pasūtījumi*.
1. Novietojuma direktīvu sarakstā atlasiet **61 SO izdošanas pasūtījums**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Rindas** atlasiet rindu ar **Secības numura** vērtību *2*.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet rindu ar **Nosaukums** vērtību *Izdot mazāk par paleti* (tai ir jābūt vienīgajai rindai), un mainiet tās **Secības numura** vērtību uz *2*.
1. Virs režģa atlasiet **Jauns**, lai jaunai novietojuma direktīvas darbībai pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Secības numurs:** *1*
    - **Nosaukums:** *Izdošanas pozīcija 1*

1. Turpinot atlasīt jaunāko rindu, atlasiet **Rediģēt vaicājumu** virs režģa.
1. Vaicājumu redaktorā atlasiet cilni **Savienojumi**.
1. Izvērsiet **Novietojumi** tabulas savienojumu, lai parādītu savienojumu ar **Krājumu dimensijas** tabulu.
1. Izvērsiet **Krājumu dimensijas** tabulas savienojumu, lai parādītu savienojumu ar **Rīcībā esošie krājumi** tabulu.
1. Atlasiet **Krājumu dimensijas** un pēc tam atlasiet **Pievienot tabulas savienojumu**.
1. Tabulu sarakstā, kas tiek parādīts kolonnā **Relācija**, atlasiet **Noliktavas vienība (Noliktavas vienība)**. Pēc tam atlasiet **Atlasīt**, lai pievienotu **Noliktavas vienību** tabulas savienojumam **Krājumu dimensijas**.
1. Kamēr **Noliktavas vienība** joprojām ir atlasīta, atlasiet **Pievienot tabulas savienojumu**.
1. Tabulu sarakstā, kas tiek parādīts kolonnā **Relācija**, atlasiet **Novietojuma noliktavas vienības pozīcija (Noliktavas vienība)**. Pēc tam atlasiet **Atlasīt**, lai pievienotu **Novietojuma noliktavas vienības pozīcija** tabulas savienojumam **Krājumu dimensijas**.

    ![Tabulas savienojums](media/LpTableJoin.png "Tabulas savienojums")

1. Atlasiet **Labi**, lai apstiprinātu atjauninātās savienotās tabulas un aizvērtu vaicājumu redaktoru.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** vēlreiz atlasiet **Rediģēt vaicājumu**, lai atkārtoti atvērtu vaicājumu redaktoru.
1. Cilnē **Diapazons** atlasiet **Pievienot**, lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Novietojuma noliktavas vienības pozīcija*
    - **Atveidotā tabula:** *Novietojuma noliktavas vienības pozīcija*
    - **Lauks:** *LP pozīcija*
    - **Kritēriji:** *1*

    ![Jauns diapazons](media/LpPositionCriteria.png "Jauns diapazons")

1. Atlasiet **Labi**, lai apstiprinātu izmaiņas un aizvērtu vaicājumu redaktoru.

### <a name="set-up-sample-data-for-this-scenario"></a>Iestatīt datu paraugus šim scenārijam

Scenārijā lietotājam ir jāpiesakās noliktavas mobilajā programmā, izmantojot darbinieku, kurš ir iestatīts veikt darbu *61* noliktavā. Lietotājam ir jāveic arī darbības.

Tā kā līdzeklis *Novietojuma noliktavas vienības pozīcija* pievieno jaunu identifikatoru noliktavas vienības pozīcijām, tad vispirms ir jāizveido daži dati, lai atbalstītu scenāriju.

#### <a name="spot-count-the-first-location"></a>Pirmās atrašanās vietas inventarizācija

1. Atveriet noliktavas mobilo programmu un piesakieties noliktavā *61*.
1. Doties uz **Krājumi \> Inventarizācija uz vietas**.
1. Lapā **Inventarizācija uz vietas** iestatiet lauku **Atrašanās vieta** uz *01A01R1S1B*.
1. Atlasiet **Labi**.

    Lapā tiek parādītas jūsu ievadītās atrašanās vietas. Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”

1. Atlasiet **Atsvaidzināt**, lai atrašanās vietai pievienotu uzskaiti.
1. Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu**, atlasiet lauku **Krājums** un pēc tam ievadiet vērtību *A0001*.
1. Atlasiet **Labi**.
1. Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu**, atlasiet lauku **LP** un pēc tam ievadiet vērtību *LP1001* (vai citu unikālu noliktavas vienības identifikatoru pēc savas izvēles).

    Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu** parādīta **1. noliktavas vienības pozīcija**.

1. Atlasiet **Labi**.

    Norādiet krājuma daudzumu, kas tika uzskaitīts noliktavas vienībai.

1. Iestatiet lauku **Daudz.** uz *10*.
1. Atlasiet **Labi**.

    Lapā tiek parādītas jūsu ievadītās atrašanās vietas. Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”

1. Atlasiet **Atsvaidzināt**, lai atrašanās vietai pievienotu citu uzskaiti.
1. Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu**, atlasiet lauku **Krājums** un pēc tam ievadiet vērtību *A0002*.
1. Atlasiet **Labi**.
1. Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu** atlasiet lauku **LP** un pēc tam ievadiet vērtību *LP1002* (vai citu unikālu noliktavas vienības identifikatoru pēc savas izvēles, nodrošinot, ka tas atšķiras no iepriekš norādītā).
1. Mainiet noliktavas vienības pozīciju, iestatot lauku **LP pozīcija** uz *2*.
1. Atlasiet **Labi**.
1. Norādiet krājuma daudzumu, kas tika uzskaitīts noliktavas vienībai, iestatot lauku **Daudz.** uz *10*.
1. Atlasiet **Labi**.

    Lapā tiek parādītas jūsu ievadītās atrašanās vietas. Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”

1. Atlasiet **Labi**.

Darbs tagad ir pabeigts.

#### <a name="spot-count-the-second-location"></a>Otrās atrašanās vietas inventarizācija

1. Lapā **Inventarizācija uz vietas** iestatiet lauku **Atrašanās vieta** uz *01A01R1S2B*.
1. Atlasiet **Labi**.

    Lapā tiek parādītas jūsu ievadītās atrašanās vietas. Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”

1. Atlasiet **Atsvaidzināt**, lai atrašanās vietai pievienotu uzskaiti.
1. Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu**, atlasiet lauku **Krājums** un pēc tam ievadiet vērtību *A0002*.
1. Atlasiet **Labi**.
1. Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu** atlasiet lauku **LP** un pēc tam ievadiet vērtību *LP1003* (vai citu unikālu noliktavas vienības identifikatoru pēc savas izvēles, nodrošinot, ka tas atšķiras no abiem iepriekšējā procedūrā norādītajiem).

    Lapā **Cikla inventarizācija: pievienot jaunu LP vai krājumu** parādīta **1. noliktavas vienības pozīcija**.

1. Atlasiet **Labi**.
1. Norādiet krājuma daudzumu, kas tika uzskaitīts noliktavas vienībai, iestatot lauku **Daudz.** uz *10*.
1. Atlasiet **Labi**.

    Lapā tiek parādītas jūsu ievadītās atrašanās vietas. Tiek parādīts arī šāds ziņojums: “Atrašanās vieta ir ievadīta, vai pievienot jaunu LP vai krājumu?”

1. Atlasiet **Labi**.

Darbs tagad ir pabeigts.

#### <a name="work-details"></a>Detalizēta informācija par darbu

> [!NOTE]
> Inventarizācijas uz vietas no mobilās programmas veido cikla inventarizācijas darbu Microsoft Dynamics 365. Darbam nepieciešams, lai inventarizācijas tiktu akceptētas, pirms tās tiek iegrāmatotas krājumos.

1. Pierakstieties programmā Dynamics 365 Supply Chain Management.
1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Cilnē **Pārskats** meklējiet rindas ar šādām vērtībām:

    - **Darba pasūtījuma veids:** *Cikla inventarizācija*
    - **Noliktava:** *61*
    - **Darba statuss:** *Gaida pārskatīšanu*

    Šīm rindām ir jāizveido divi darba ID. Abām darba ID uzskaitēm ir jābūt pieņemtām.

1. Režģī atlasiet pirmo darba ID *Cikla inventarizācija* darba pasūtījuma tipam.
1. Darbību rūts cilnē **Darbs** grupā **Darbs** atlasiet **Cikla inventarizācija**.

    Tiek rādītas divas rindas, pa vienai katrai krājuma un noliktavas vienībai. Vērtībām **Inventarizācijas daudzums** laukos **Atrašanās vieta**, **Noliktavas vienība** un **Krājums** ir jāatbilst mobilajā ierīcē izveidotajiem uzskaites ierakstiem. Ja kāds no šiem laukiem nav redzams, darbību rūtī atlasiet **Parādīt dimensijas**, lai tās pievienotu režģim.

1. Atlasiet abas rindas.
1. Darbību rūtī atlasiet **Pieņemt uzskaiti**.
1. Tiek saņemts ziņojums “Grāmatošana – žurnāls”. Atlasiet **Ziņojuma informācija**, lai apskatītu grāmatotā žurnāla numuru.
1. Aizveriet ziņojuma informāciju.
1. Atsvaidziniet lapu **Darbs**.

    Pirmais darba ID ir aizvērts un vairs netiek rādīts.

    > [!TIP]
    > Lai skatītu slēgto darbu, atzīmējiet izvēles rūtiņu **Rādīt slēgto**, kas atrodas virs režģa.

    Tiek pieņemts darbs noliktavas vienībai *01A01R1S2B* vietā.

1. Cilnē **Pārskats**, atlasiet otru darba ID darba pasūtījuma veidam *Cikla inventarizācija*.
1. Darbību rūts cilnē **Darbs** grupā **Darbs** atlasiet **Cikla inventarizācija**.

    Tiek rādīta viena rinda krājumam un noliktavas vienībai. Vērtībām **Inventarizācijas daudzums** laukos **Atrašanās vieta**, **Noliktavas vienība** un **Krājums** ir jāatbilst mobilajā ierīcē izveidotajiem uzskaites ierakstiem.

1. Atlasiet rindu.
1. Darbību rūtī atlasiet **Pieņemt uzskaiti**.
1. Tiek saņemts ziņojums “Grāmatošana – žurnāls”. Atlasiet **Ziņojuma informācija**, lai apskatītu grāmatotā žurnāla numuru.
1. Aizveriet ziņojuma informāciju.
1. Atsvaidziniet lapu **Darbs**.

    Otrais darba ID ir aizvērts un vairs netiek rādīts.

    > [!TIP]
    > Lai skatītu slēgto darbu, atzīmējiet izvēles rūtiņu **Rādīt slēgto**, kas atrodas virs režģa.

#### <a name="on-hand-by-location"></a>Rīcībā esošie krājumi pēc atrašanās vietas

1. Dodieties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Rīcībā esošie krājumi pēc atrašanās vietas**.
1. Iestatiet šādas vērtības:

    - **Vieta:** *6*
    - **Noliktava:** *61*
    - **Atsvaidzināt vairākās atrašanās vietās:** *Jā*

1. Ievērojiet, ka novietojumam *01A01R1S1B* ir divas noliktavas vienības:

    - **A0001**, kur lauks **LP pozīcija** ir iestatīts uz *1*
    - **A0002**, kur lauks **LP pozīcija** ir iestatīts uz *2*

1. Ievērojiet, ka novietojumam *01A01R1S2B* ir viena noliktavas vienība:

    - **A0002**, kur lauks **LP pozīcija** ir iestatīts uz *1*

### <a name="sales-order-scenario"></a>Pārdošanas pasūtījuma scenārijs

Tagad, kad ir iestatīts līdzeklis *Novietojuma noliktavas vienības pozīcija* un krājumi ir nodrošināti, ir jāizveido pārdošanas pasūtījums, lai ģenerētu izdošanas darbu, kas novirzīs noliktavas darbinieku izdot krājumu *A0002* no krājumu novietojuma, kur paletes ID ir pozīcijā *1*.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-004*
    - **Noliktava:** *61*

1. Atlasiet **Labi**.
1. Kopsavilkuma cilnes režģim **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda. Šajā rindā iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0002*
    - **Daudzums:** *1*

1. Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus pasūtījuma rindai.
1. Aizveriet lapu **Rezervācija**.
1. Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.

    Tiek saņemts informatīvs ziņojums, norādot pasūtījumam izveidoto kopuma ID un sūtījuma ID.

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Noliktava** virs režģa, atlasiet **Darba informācija**.
1. Tiek parādīta lapa **Darbs**, un tā parāda darbu, kas tika izveidots pārdošanas rindai. Pierakstiet parādīto darba ID.

### <a name="sales-picking-scenario"></a>Pārdošanas izdošanas scenārijs

1. Atveriet mobilo programmu un piesakieties noliktavā *61*.
1. Doties uz **Izejošs \> Pārdošanas izdošana**.
1. Lapā **Skenēt darba ID / noliktavas vienības ID** atlasiet lauku **ID** un pēc tam ievadiet darba ID no pārdošanas rindas.
1. Ņemiet vērā, ka izdošanas darbs jūs novirza izdot krājumu *A0002* no atrašanās vietas *01A01R1S2B*. Šī instrukcija tiek saņemta, jo krājums *A0002* atrodas noliktavas vienībā, kas ir novietojuma pozīcijā *1*.

    ![1. pozīcijas novietojums](media/LocationLicensePlatePositioning.png "1. pozīcijas novietojums")

1. Ievadiet novietojuma izveidoto noliktavas vienības ID un pēc tam sekojiet uzvednēm, lai izdotu pārdošanas pasūtījumu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]