---
title: Cikla inventarizācijas piemēru scenāriji
description: Šajā tēmā ir sniegts scenāriju apkopojums, kas izpēta Microsoft Dynamics 365 Supply Chain Management cikla inventarizācijas līdzekļus.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 09ca57d6a3654e56e12240af73d6793002eb1794e4b41d25e182b9b1d3b66df5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746799"
---
# <a name="cycle-counting-example-scenarios"></a>Cikla inventarizācijas piemēru scenāriji

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts scenāriju apkopojums, kas izpēta Microsoft Dynamics 365 Supply Chain Management cikla inventarizācijas līdzekļus. Tas vispirms apraksta jūsu esošās Supply Chain Management vides prasības. Pēc tam tajā skaidrots, kā konfigurēt cikla inventarizāciju un aprakstītas visas cikla inventarizācijas stadijas. Kad esat beidzis, jums ir jābūt labi izpratnei par cikla inventarizāciju, tostarp vadīto cikla inventarizāciju, aklo cikla inventarizāciju, vietu cikla inventarizāciju, cikla inventarizācijas robežvērtībām un cikla inventarizācijas plāniem.

## <a name="prerequisites"></a>Priekšnosacījumi

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Katrs scenārijs šajā tēmā atsaucas uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, strādājot ar scenārijiem, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu (uzņēmumu) **USMF**, pirms sākat darbu.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Warehouse Management mobilās programmas atbalsta ieslēgšana

Lai varētu lietot jauno Warehouse Management mobilo programmu, sistēmā tai ir jāpievieno atbalsts. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Lietotāja iestatījumi, ikonas un darbību nosaukumi jaunajai noliktavas programmai*

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Sagatavot demonstrācijas datus scenārijiem

Izpildiet šīs darbības, lai apstiprinātu, ka visi scenārijiem nepieciešamie demonstrācijas dati ir pieejami USMF uzņēmumā jūsu sistēmā. Izveidojiet visus ierakstus vai trūkstošās vērtības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.
1. Saraksta rūtī atlasiet **Jūlija Funderburka**.
1. Kopsavilkuma cilnē **Lietotāji** atlasiet rindu, kurā ir šādas vērtības. Ja nevienai esošai rindai nav šo vērtību, izveidojiet to.

    - **Lietotāja ID:** *61*
    - **Lietotājvārds:** *WH61*
    - **Noklusējuma noliktava:** *61*
    - **Izvēlnes nosaukums:** *Galvenā*

1. Kopsavilkuma cilnē **Darbs** iestatiet tālāk norādītās vērtības lietotājam *61*, ja tās vēl nav iestatītas.

    - **Ir cikla inventarizācijas supervizors:** *Nē*
    - **Maksimālais procentuālais ierobežojums:** *0*
    - **Maksimālais daudzuma ierobežojums:** *0*
    - **Maksimālā robežvērtība:** *0*

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba pūli**.
1. Darba kopas tiek izmantotas, lai nošķirtu noliktavas darbu, pamatojoties uz darba veidu (šajā gadījumā cikla inventarizācijas darbs). Pārliecinieties, vai pastāv ieraksts ar šādiem iestatījumiem:

    - **Darba pūla ID:** *CycleCount*
    - **Apraksts:** *Cikla inventarizācija*

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Saraksta rūtī atlasiet ierakstu ar nosaukumu *Cikla inventarizācija*. Ja nevienam esošam ierakstam nav šī nosaukuma, izveidojiet to. Apstipriniet vai iestatiet ierakstam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Cikla inventarizācija*
    - **Nosaukums:** *Vadītā cikla inventarizācija*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Jā*
    - **Virzīts:** *Sistēmas virzīts* (šī vērtība norāda, ka Supply Chain Management darbiniekam piešķirs cikla inventarizācijas darba ID.)
    - **Rādīt krājumu statusu:** *Jā*

1. Darbību rūtī atlasiet **Cikla inventarizācija**.
1. Dialoglodziņā **Mobilās ierīces cikla inventarizācija** apstipriniet vai iestatiet šādas vērtības:

    - **Rādīt krājuma kodu:** *Jā*
    - **Rādīt numura zīmi:** *Jā*
    - **Mēģinājumu skaits:** *1*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Saraksta rūtī atlasiet ierakstu ar nosaukumu *Akla cikla inventarizācija*. Ja nevienam esošam ierakstam nav šī nosaukuma, izveidojiet to. Apstipriniet vai iestatiet ierakstam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Akla cikla inventarizācija*
    - **Nosaukums:** *Akla cikla inventarizācija*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Jā*
    - **Vādīts:** *Cikla inventarizācijas grupēšana* (šī vērtība norāda, ka darbinieks var grupēt cikla inventarizācijas darba ID, kas noteikti novietojumam, zonai vai darbu kopai.)

1. Darbību rūtī atlasiet **Cikla inventarizācija**.
1. Dialoglodziņā **Mobilās ierīces cikla inventarizācija** apstipriniet vai iestatiet šādas vērtības:

    - **Rādīt krājuma kodu:** *Nē*
    - **Rādīt numura zīmi:** *Nē*
    - **Mēģinājumu skaits:** *0*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Saraksta rūtī atlasiet ierakstu ar nosaukumu *Vietu inventarizācija*. Ja nevienam esošam ierakstam nav šī nosaukuma, izveidojiet to. Apstipriniet vai iestatiet ierakstam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Vietu inventarizācija*
    - **Nosaukums:** *Vietas inventarizācija*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Nē*
    - **Darba izveides process:** *Vietas cikla inventarizācija* (šī vērtība norāda, ka darbinieks jebkurā laikā var saskaitīt noliktavas novietojumā esošos krājumus, neveidojot cikla inventarizācijas darbu. Lai veiktu vietas cikla inventarizāciju kādā novietojumā, darbinieks ievada novietojuma ID.)

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Saraksta rūtī atlasiet ierakstu ar nosaukumu *Krājumi*. Ja nevienam esošam ierakstam nav šī nosaukuma, izveidojiet to. Apstipriniet, ka kolonnā **Izvēlnes struktūra** ir redzami šādi cikla inventarizācijas izvēlnes vienumi:

    - Cikla inventarizācija
    - Akla cikla inventarizācija
    - Vietas inventarizācija

1. Doties uz **Noliktavas vadība \> Iestatīšana \> Noliktavas vadības parametri**.
1. Cilnē **Cikla inventarizācija** iestatiet šādas vērtības:

    - **Noklusējuma cikla inventarizācijas korekcijas tips:** *Cikla inventarizācija* (šis lauks norāda žurnāla tipu, kas tiek grāmatots, kad ir pabeigta cikla inventarizācija.)
    - **Noklusējuma cikla inventarizācijas darba klases ID:** *CCount* (šis lauks norāda darba klasi, kas tiek izmantota cikla inventarizācijai.)
    - **Noklusējuma cikla inventarizācijas darba prioritāte:** *50* (šajā laukā tiek iestatīta prioritāte, kas cikla inventarizācijas darbam ir attiecībā pret citiem darba tipiem noliktavā. Ievadot skaitli, kas ir mazāks par skaitli, kas ievadīts citu darba veidiem, jūs palielināsiet cikla inventarizācijas darba prioritāti.)

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Krājumi \> Korekcijas veidi**.
1. Lapa **Korekcijas veidi** ļauj izveidot kodus dažādiem pielāgojumiem, kas var rasties. Apstipriniet, vai pastāv ieraksts ar šādiem iestatījumiem:

    - **Krājumu korekcijas veids:** *Cikla inventarizācija*
    - **Apraksts:** *Cikla inventarizācija*
    - **Nosaukums:** *ICnt*

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktavas iestatījumi \> Noliktavas**.
1. Saraksta rūtī atlasiet noliktavu *61*. Ja nevienam esošam ierakstam nav šī nosaukuma, izveidojiet to.
1. Kopsavilkuma cilnē **Noliktava** iestatiet šādas vērtības:

    - **Izmantot noliktavas pārvaldības procesu:** *Jā* (šī vērtība iespējo noliktavu noliktavas pārvaldības procesiem.)
    - **Atļaut numura zīmes pārvietošanu cikla inventarizācijas laikā:** *Jā* (šī vērtība ļauj darbiniekiem pārvietot numura zīmes cikla inventarizācijas laikā.)

## <a name="scenario-1-guided-cycle-counting"></a>1. scenārijs: vadītā cikla inventarizācija

Pirms var notikt vadīta cikla inventarizācija, ir jāizveido kāds darbs. Šis darbs palīdzēs piešķirtajai personai, izmantojot noliktavu, no vietas līdz vietai, pabeigt darbā iestatīto skaitu.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Izveidot cikla inventarizācijas darbu 1. scenārijam

Izpildiet šīs darbības, lai izveidotu cikla inventarizācijas darbu krājumu novietojumam *01A02R2S2B* (BULK-06) noliktavā *61*.

1. Dodieties uz **Noliktavas pārvaldība \> Cikla inventarizācija \> Cikla inventarizācijas arbs pēc atrašanās vietas**.
1. Dialoglodziņā **Izveidot cikla inventarizācijas darbu pēc atrašanās vietas** iestatiet lauku **Darba pūla ID** uz *CycleCount*.
1. Kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrs**.
1. Vaicājumu redaktora dialoglodziņā cilnē **Diapazons** veiciet šādas darbības:

    - Rindai, kur lauks **Lauks** ir iestatīts uz *Noliktava*, iestatiet lauku **Kritēriji** uz *61*.
    - Rindai, kur lauks **Lauks** ir iestatīts uz *Atrašanās vieta*, iestatiet lauku **Kritēriji** uz *01A02R2S2B*.

1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Izveidot cikla inventarizācijas darbu pēc atrašanās vietas**.

    Kad darba izveides process ir pabeigts, Darbību centrā parādās ziņojums.

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Atrodiet jaunizveidoto darbu, iestatot filtru kolonnā **Darbu pūla ID**, lai atrastu ierakstus, kuru vērtība ir *CycleCount*.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Veiciet cikla inventarizācijas darbu 1. scenārijam

Kad ir izveidots cikla inventarizācijas darbs, darbu veic, saskaitot noliktavas vietā esošos krājumus un pēc tam izmantojot mobilo ierīci, lai ievadītu rezultātus programmā Supply Chain Management. Izpildiet šīs darbības, lai varētu veikt cikla inventarizācijas darbu mobilajā programmā Warehouse Management.

1. Piesakieties mobilajā programmā Warehouse Management kā darba lietotājs, ko iepriekš šajā tēmā iestatījāt sadaļā [Sagatavot demonstrācijas datus scenārijiem](#prepare-demo-data). Piemēram šajā tēmā lietotājs ir nosaukts *Jūlija Funderburka* un ir iestatīts noliktavai *61*. (USMF demonstrācijas datiem jāsniedz jums iespēju pieteikties kā šim darba lietotājam, ievadot *61* kā lietotāja ID un *1* kā paroli.)
1. Galvenajā izvēlnē atlasiet **Krājumi**.
1. Izvēlnē **Krājumi** atlasiet **Vadīto cikla inventarizāciju**.
1. Atlasiet lauku **Daudzums**, ievadiet *9*, izmantojot ciparu tastatūru, un pēc tam atlasiet **Labi** (izvēles rūtiņas pogu).
1. Sistēma paredzēja, ka šim krājumam, novietojumam un numura zīmei ievadīsiet 10 gabalu skaitu. Tāpēc jūs lūdz pārskaitīt. Atlasiet lauku **Daudzums**, atkal ievadiet *9*, izmantojot ciparu tastatūru, un pēc tam atlasiet **Labi** (izvēles rūtiņas pogu). Otrajā mēģinājumā jūsu skaits tiks pieņemts.

    > [!NOTE]
    > Kad sistēma konstatēja atšķirību starp paredzamo rīcībā esošo daudzumu un ievadīto daudzumu, tā lūdz jums skaitīt otru reizi, jo lauks **Mēģinājumu skaits** ir iestatīts uz *1* mobilās ierīces izvēlnes vienumam **Vadīta cikla inventarizācija**. Jūs tikāt novirzīts uz noteiktu krājuma numuru un numura zīmes numuru, jo gan opcija **Rādīt krājuma numuru**, gan opcija **Rādīt numura zīmi** ir iestatīta uz *Jā* mobilās ierīces izvēlnes vienumam.

1. Atlasiet pogu **Labi** (atzīmes poga).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Pārskatīt 1. scenārija cikla inventarizācijas atšķirības

Veiciet šīs darbības, lai pārskatītu cikla inventarizācijas atšķirības.

1. Atgriezieties Supply Chain Management.
1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Atrodiet un atlasiet cikla inventarizācijas darbu, ko skatījāt agrāk. (Piemēram, iestatiet filtru kolonnā **Darbu pūla ID**, lai atrastu ierakstus, kuru vērtība ir *CycleCount*.) Ņemiet vērā, ka lauks **Darba statuss** šim darbam tagad ir iestatīts uz *Gaida pārskatīšanu*.

    > [!NOTE]
    > Darba lietotāja kontam, ko izmantojāt inventarizācijas darbam, opcija **Cikla inventarizācijas pārraugs** ir iestatīta uz *Nē*, un lauki **Maksimālais procentuālais ierobežojums**, **Maksimālais daudzums** un **Maksimālās vērtības ierobežojums** tiek iestatīti uz *0* (nulle). Tādēļ visas inventarizācijas atšķirības, kas šim lietotāja pārskatiem ir manuāli jāapstiprina, un saistītā darba lauks **Darba statuss** tiek iestatīts uz *Gaida pārskatīšanu*. Ja aprēķinātā vērtība bija novirzes robežās (kā norādīts laukos **Maksimālais procentuālais ierobežojums** vai **Maksimālais daudzuma limits** lapā **Darba lietotāji** ) vai ja lietotājam opcija **Cikla inventarizācijas parraugs** bija iestatīta uz *Jā*, darbs automātiski tiktu slēgts.

1. Darbību rūts cilnē **Darbs** atlasiet **Cikla inventarizācija**.
1. Darbību rūtī atlasiet **Pieņemt uzskaiti**.

    Starpība tiek grāmatota, izmantojot standarta uzskaites žurnālu, un tiek izveidots jauns darba pasūtījums.

1. Lapā **Cikla inventarizācijas transakcijas** darbību rūtī atlasiet **Atvasinātais darbs**, lai atrastu darbu, kas tika izveidots apstiprinātajai starpībai.

## <a name="scenario-2-blind-cycle-counting"></a>2. scenārijs: aklā cikla inventarizācija

Šim scenārijam ir nepieciešams, lai jūsu sistēmā jau tiktu pabeigts 1. scenārijs.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Izveidot cikla inventarizācijas darbu 2. scenārijam

Pirms var notikt aklā cikla inventarizācija, ir jāizveido kāds darbs. Izpildiet šīs darbības, lai izveidotu cikla inventarizācijas darbu krājumu novietojumam *01A02R2S2B* (BULK-06) noliktavā *61*.

1. Dodieties uz **Noliktavas pārvaldība \> Cikla inventarizācija \> Cikla inventarizācijas darbs pēc krājuma**.
1. Dialoglodziņā **Izveidot cikla inventarizācijas darbu pēc krājuma** iestatiet lauku **Darba pūla ID** uz *CycleCount*.
1. Kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrs**.
1. Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet trīs rindas, kam ir turpmāk aprakstītie iestatījumi:

    - Rinda 1:

        - **Tabula:** *Krājums*
        - **Lauks:** *Krājuma numurs*
        - **Kritēriji:** *L0101*

    - Rinda 2:

        - **Tabula:** *Cilne Krājumu dimensijas*
        - **Lauks:** *Noliktava*
        - **Kritēriji:** *61*

    - Rinda 3:

        - **Tabula:** *Cilne Krājumu dimensijas*
        - **Lauks:** *Novietojums*
        - **Kritēriji:** *01A02R2S2B*

1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Izveidot cikla inventarizācijas darbu pēc krājuma**.

    Kad darba izveides process ir pabeigts, saņemsit informatīvu ziņojumu.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Veiciet cikla inventarizācijas darbu 2. scenārijam

Pēc cikla inventarizācijas darba izveides, izpildot šīs darbības, lai veiktu darbu mobilajā programmā Warehouse Management.

1. Piesakieties mobilajā programmā Warehouse Management kā darba lietotājs, ko iepriekš šajā tēmā iestatījāt sadaļā [Sagatavot demonstrācijas datus scenārijiem](#prepare-demo-data). Piemēram šajā tēmā lietotājs ir nosaukts *Jūlija Funderburka* un ir iestatīts noliktavai *61*. (USMF demonstrācijas datiem jāsniedz jums iespēju pieteikties kā šim darba lietotājam, ievadot *61* kā lietotāja ID un *1* kā paroli.)
1. Galvenajā izvēlnē atlasiet **Krājumi**.
1. Izvēlnē **Krājumi** atlasiet **Aklo cikla inventarizāciju**.
1. Atlasiet lauku **Zonas ID**, ievadiet *BULK06* un tad atlasiet **Labi** (atzīmes poga).
1. Atlasiet lauku **Krājums**, ievadiet *L0101* un tad atlasiet **Labi** (atzīmes poga).
1. Atlasiet lauku **Numura zīme**, ievadiet *LP\_BULK\_06\_01* un tad atlasiet **Labi** (atzīmes poga).
1. Atlasiet lauku **Daudzums**, ievadiet *10* un tad atlasiet **Labi** (atzīmes poga).

    > [!NOTE]
    > Pat ja sistēma konstatēja atšķirību starp paredzamo rīcībā esošo daudzumu un skenēto daudzumu, tā neprasīja, lai jūs skaitītu otru reizi, jo lauks **Mēģinājumu skaits** ir iestatīts uz *0* (nulle) mobilās ierīces izvēlnes vienumam **Aklā cikla inventarizācija**. Jums tika lūgts skenēt krājuma numuru un numura zīmi, jo gan opcija **Rādīt krājuma numuru**, gan opcija **Rādīt numura zīmi** ir iestatīta uz *Nē* mobilās ierīces izvēlnes vienumam.

1. Atlasiet pogu **Labi** (atzīmes poga).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Pārskatīt 2. scenārija cikla inventarizācijas atšķirības

Veiciet šīs darbības, lai pārskatītu cikla inventarizācijas atšķirības.

1. Atgriezieties Supply Chain Management.
1. Atvēriet **Noliktavas pārvaldība \> Kopējais \> Darbs \> Izskatīšanu gaidošais cikla inventarizācijas darbs**.
1. Darbību rūts cilnē **Darbs** atlasiet **Cikla inventarizācija**.
1. Darbību rūtī atlasiet **Noraidīt uzskaiti**.

    Ņemot vērā, ka uzskaites starpība tika noraidīta, darbs ir slēgts.

## <a name="scenario-3-spot-cycle-counting"></a>3. scenārijs: vietas cikla inventarizācija

Rīcībā esošie ieraksti norāda, ka novietojumā *01A02R2S2B* ir rīcībā esošās preces *L0101* daudzums. Noliktavas darbinieks atrodas vietā *01A02R2S1B*. Lai gan šai vietai ir jābūt tukšai, tā ir pilna. Tāpēc noliktavas darbinieks nekavējoties veic ša novietojuma vietas inventarizāciju.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Veiciet cikla inventarizācijas darbu 3. scenārijam

Izpildiet šīs darbības, lai varētu veikt cikla inventarizācijas darbu mobilajā programmā Warehouse Management.

1. Piesakieties mobilajā programmā Warehouse Management kā darba lietotājs, ko iepriekš šajā tēmā iestatījāt sadaļā [Sagatavot demonstrācijas datus scenārijiem](#prepare-demo-data). Piemēram šajā tēmā lietotājs ir nosaukts *Jūlija Funderburka* un ir iestatīts noliktavai *61*. (USMF demonstrācijas datiem jāsniedz jums iespēju pieteikties kā šim darba lietotājam, ievadot *61* kā lietotāja ID un *1* kā paroli.)
1. Galvenajā izvēlnē atlasiet **Krājumi**.
1. Izvēlnē **Krājumi** atlasiet **Vietas inventarizāciju**.
1. Atlasiet lauku **Atrašanās vieta**, ievadiet *01A02R2S1B* un tad atlasiet **Labi** (atzīmes poga).

    Sistēma konstatē, ka Supply Chain Management vieta ir tukša.

1. Atlasiet **Pievienot LP vai krājumu**.
1. Atlasiet lauku **Krājums**, ievadiet *L0101* un tad atlasiet **Labi** (atzīmes poga).
1. Atlasiet lauku **Numura zīme**, ievadiet *LP\_BULK\_06\_01* un tad atlasiet **Labi** (atzīmes poga).
1. Atlasiet lauku **Daudzums**, ievadiet *9* un tad atlasiet **Labi** (atzīmes poga).

    Tā kā sistēma konstatē, ka norādītā numura zīme ir jau pieejama citā Supply Chain Management vietā, šī numura zīme tiks pārvietota uz pašreizējo vietu. Tādēļ sistēma prasa apstiprināt kustību.

1. Atlasiet pogu **Labi** (atzīmes poga).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Pārskatīt 3. scenārija cikla inventarizācijas atšķirības

Veiciet šīs darbības, lai pārskatītu inventarizācijas rezultātus.

1. Atgriezieties Supply Chain Management.
1. Dodieties uz **Noliktavas pārvaldība \> Kopējais \> Darba informācija**.
1. Atlasiet izvēles rūtiņu **Rādīt slēgto** režģa augšpusē.
1. Iestatiet filtru kolonnai **Darba pasūtījuma tips** uz *Krājumu kustība*.

    Sistēma šo inventarizāciju automātiski noteica kā krājumu kustību. Šī kustība ir atļauta, jo opcija **Atļaut numura zīmes pārvietošanos cikla inventarizācijas laikā** ir iestatīta uz *Jā*, noliktavai *61* lapā **Noliktavas**.

## <a name="scenario-4-define-cycle-count-thresholds"></a>4. scenārijs: Definēt cikla inventarizācijas robežvērtības

Viens cikla inventarizācijas darba izveides veids ir izmantot sliekšņus. Cikla inventarizācijas slieksnis norāda krājumu vienību daudzumu vai procentuālo ierobežojumu. Cikla inventarizācijas darbs tiek izveidots automātiski, kad tiek sasniegts sliekšnis.

Piemēram, novietojumā, kura cikla inventarizācijas sliekšņa vērtība ir 40, ir 60 krājumi. Pārdošanas pasūtījuma transakcijas laikā 25 krājumi tiek izdoti no novietojuma un izvietoti sagatavošanas posma novietojumā. Jaunais krājumu skaits ir 35, un tas ir mazāks par sliekšņa vērtību, tādēļ cikla inventarizācijas darbs novietojumam tiek izveidots automātiski.

Veiciet šīs darbības, lai iestatītu cikla inventarizācijas sliekšņus.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Cikla inventarizācija \> Cikla inventarizācijas robežvērtības**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu sliekšni, un iestatiet šādas vērtības:

    - **Cikla inventarizācijas sliekšņa ID:** *L0101*
    - **Apraksts:** *Slieksnis L0101*
    - **Sliekšņa daudzums:** *2*
    - **Vienība:** *ea*
    - **Ietilpības slieksnis procentos:** *0,00*
    - **Cikla inventarizācijas sliekšņa veids:** *Daudzums*
    - **Nekavējoties apstrādāt cikla inventarizāciju:** *Jā*
    - **Dienu skaits starp cikla inventarizācijām:** *1*
    - **Darba pūla ID:** *CycleCount*

1. Darbību rūtī atlasiet **Atlasīt krājumus**.
1. Vaicājuma redaktora dialoglodziņā cilnē **Diapazons** sameklējiet rindu, kurā lauks **Lauks** ir iestatīts uz *Krājuma numurs*. Iestatiet lauku **Kritēriji** tai rindai uz *L0101*.
1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.

    Tagad esat definējis cikla inventarizācijas slieksni krājumam *L0101*.

Cikla inventarizācija tiks izveidota krājumam *L0101* jebkurā vietā, ja rīcībā esošo krājumu daudzums ir mazāks par 2 un ja pēdējās novietojuma cikla inventarizācijas datums nav šodien.

## <a name="scenario-5-define-cycle-count-plans"></a>5. scenārijs: Definēt cikla inventarizācijas plānus

Cikla inventarizācijas plāni ļauj automatizēt cikla inventarizācijas darba izveidi. Varat iestatīt katru cikla inventarizācijas plānu ar specifiskiem krājumu un novietojumu vaicājumiem. Kad pakešuzdevums tiek palaists, tas izveidos cikla inventarizācijas darbu visām atrašanās vietām, kas atbilst krājuma un novietojuma kritērijiem (līdz plānam norādītajam maksimālajam skaitam). Kad tiek izveidots cikla inventarizācijas darbs, inventarizācijas darba rinda satur informāciju par atrašanās vietu, kas ir jāsaskaita. Ar šo atrašanās vietu saistītie rīcībā esošie krājumi nav bloķēti. Tāpēc tā ir pieejama rezervēšanai un izejošai apstrādei pat tad, ja pastāv atvērts inventarizācijas darbs.

Veiciet šīs darbības, lai iestatītu cikla inventarizācijas plānu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Cikla inventarizācija \> Cikla inventarizācijas plāni**.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu rindu režģim, un iestatiet tai šādas vērtības:

    - **Cikla inventarizācijas plāna ID:** *BULK06*
    - **Apraksts:** *BULK06 novietojuma inventarizācija*
    - **Darba pūla ID:** *CycleCount*
    - **Maksimālais ciklu skaitu daudzums:** *10*
    - **Dienu skaits starp cikla inventarizācijām:** *10*
    - **Tukšas atrašanās vietas:** *Izslēgt tukšos*
    - **Darba veidne:** Atstājiet šo lauku tukšu.

1. Darbību rūtī atlasiet **Atlasīt atrašanās vietas**.
1. Parādās standarta vaicājumu redaktora dialoglodziņš. Cilnē **Diapazons** pievienojiet rindu un iestātiet tai sekojošas vērtības:

    - **Tabula:** *Novietojumi*
    - **Lauks:** *Zonas ID*
    - **Kritēriji:** *BULK06*

1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.
1. Darbību rūtī atlasiet **Procesa cikla inventarizācijas plāns**.
1. Dialoglodziņā **Cikla inventarizācijas plāni**, kopsavilkuma cilnē **Palaist fonā** iestatiet opciju **Pakešapstrāde** uz *Jā*.
1. Atlasiet **Periodiskums**.
1. Dialoglodziņā **Definēt periodiskumu** iestatiet pakešuzdevumu tā, lai tas nekavējoties sāktos un palaistos vienu reizi minūtē, un tā, lai būtu beigu datums.
1. Lai dialoglodziņu **Definēt periodiskumu** aizvērtu, atlasiet **Labi**.
1. Lai dialoglodziņu **Cikla inventarizācijas plāni** aizvērtu, atlasiet **Labi**.

    Ziņojums jūs informē, ka darbs tika pievienots pakešuzdevumu rindai.

1. Atlasiet **Noliktavas pārvaldība \> Vispārīgi \> Cikla inventarizācijas plānošana**. Plāns sākas nekavējoties un izveido inventarizācijas darbu. Tā kā inventarizācijas darbs nav pabeigts, lauks **Statuss** ir iestatīts uz *Procesā*. Pēc vienas minūtes vērtība kolonnā **Kopējā cikla inventarizācija** mainās uz *1*.

    > [!NOTE]
    > Cikla inventarizācijas darbs netiks izveidots, ja dienu skaits kopš pēdējās cikla inventarizācijas ir mazāks par vērtību, kas cikla inventarizācijas plānam iestatīts laukā **Dienu skaits starp cikla inventarizācijām**. Piemēram, ja lauks **Dienu skaits starp cikla inventarizācijām** ir iestatīts uz *5*, cikla inventarizācijas darbs tiks veidots ik pēc piecām dienām. Tomēr, ja cikla inventarizācijas darbs tiek apstrādāts 3. dienā, nākamais cikla inventarizācijas darbs tiks izveidots piecas dienas pēc tam, kad tika apstrādāta pēdējā cikla inventarizācija, t. i., 8. dienā.

1. Darbību rūtī atlasiet **Darbs**, lai skatītu izveidoto inventarizācijas darbu.
