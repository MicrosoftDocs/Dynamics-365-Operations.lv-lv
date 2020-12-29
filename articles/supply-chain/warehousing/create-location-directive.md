---
title: Darbs ar novietojuma direktīvām
description: Šajā tēmā ir aprakstīts, kā strādāt ar atrašanās vietas direktīvām. Novietojuma direktīvas ir lietotāja definēti nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai.
author: Mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: f56257fd3f2f681bbd514843d8ddafa2395648d3
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517480"
---
# <a name="work-with-location-directives"></a>Darbs ar novietojuma direktīvām

[!include [banner](../includes/banner.md)]

Novietojuma direktīvas ir nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai. Piemēram, pārdošanas pasūtījuma transakcijā novietojuma direktīva nosaka, kur krājumi tiks izdoti un kur izdotie krājumi tiks izvietoti. Atrašanās vietas direktīvas ietver galveni un saistītās rindas. Tie tiek izveidoti noteiktiem *darba pasūtījuma veidiem*.

> [!NOTE]
> Šī tēma attiecas uz moduļa **Noliktavas pārvaldība** līdzekļiem. Tas neattiecas uz līdzekļiem modulī [Krājumu vadība](../inventory/inventory-home-page.md).

Varat izmantot novietojuma direktīvas, lai veiktu tālāk norādītos uzdevumus.

- Ienākošo krājumu izvietošanai.
- Izejošajām transakcijām paredzēto krājumu izdošanai un organizēšanai.
- Izejvielu izdošanai un nodošanai ražošanai.
- Novietojumu papildināšanai.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms jūs varat izveidot novietojumu direktīvu, jums ir jāveic šādas darbības, lai nodrošinātu, ka tiek ievēroti priekšnosacījumi.

1. Pārliecinieties, vai ir ieslēgta vajadzīgā licences atslēga. Dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Licences konfigurācija**, izvērsiet licences atslēgu **Tirdzniecība** un pēc tam atlasiet konfigurācijas atslēgu **Noliktavas un transportēšanas pārvaldība**. Ievērojiet, ka šai darbībai nepieciešama administratora piekļuve.
1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Noliktavas**.
1. Izveidojiet noliktavu.
1. Kopsavilkuma cilnē **Noliktava** iestatiet **Izmantot noliktavas pārvaldības procesus** opciju uz *Jā*.
1. Izveidojiet novietojumus, novietojumu veidus, novietojumu profilus un novietojumu formātus. Lai iegūtu papildu informāciju, skatiet [Konfigurēt novietojumus WMS iespējotā noliktavā](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Izveidojiet vietas, zonas un zonu grupas. Lai iegūtu papildu informāciju, skatiet [Noliktavu iestatīšana](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) un [Konfigurēt novietojumus WMS iespējotā noliktavā](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="work-order-types-for-location-directives"></a>Darba pasūtījumu veidi novietojuma direktīvām

Daudzi lauki, ko var iestatīt novietojuma direktīvām, ir kopēji visiem darba pasūtījuma veidiem. Tomēr citi lauki ir specifiski noteiktiem darba pasūtījumu veidiem.

![Atrašanās vietas direktīvu darba pasūtījumu veidi](media/Location_Directives_Work_Order_Types.png "Atrašanās vietas direktīvu darba pasūtījumu veidi")

> [!NOTE]
> Divi darba pasūtījumu veidi *Atceltie darbi* un *Cikla inventarizācija* tiek izmantoti tikai sistēmā. Šim darba pasūtījumu veidiem nevar izveidot novietojuma direktīvas.

Tabulās turpmākajās apakšsadaļās ir uzskaitīti kopējie un darbinieku pasūtījumu veida lauki, kas ir pieejami, iestatot novietojuma direktīvu.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Lauki, kas ir kopēji visiem darba pasūtījumu veidiem

Sekojošajā tabulā ir uzskaitīti lauki, kas ir kopīgi visiem darbu pasūtījumu veidiem.

| Kopsavilkuma cilne | Lauks |
|---|---|
| Vietas direktīvas | Darba veids |
| Vietas direktīvas | Vieta |
| Vietas direktīvas | Noliktava |
| Vietas direktīvas | Direktīvas kods |
| Vietas direktīvas | Vairākas NV |
| Līnijas | Sērijas numurs |
| Līnijas | No daudzuma |
| Līnijas | Līdz daudzumam |
| Līnijas | Vienība |
| Līnijas | Novietot daudzumu |
| Līnijas | Ierobežot atbilstoši vienībai |
| Līnijas | Noapaļot uz augšu līdz vienībai |
| Līnijas | Meklēt iepakojuma daudzumu |
| Līnijas | Atļaut sadalījumu |
| Novietojuma direktīvas darbības | Sērijas numurs |
| Novietojuma direktīvas darbības | Vārds, uzvārds |
| Novietojuma direktīvas darbības | Fiksētā novietojuma lietojums |
| Novietojuma direktīvas darbības | Atļaut negatīvu krājumu daudzumu |
| Novietojuma direktīvas darbības | Partija iespējota. |
| Novietojuma direktīvas darbības | Stratēģija |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Lauki, kas ir specifiski darba pasūtījumu veidiem

Sekojošajā tabulā ir uzskaitīti lauki, kas ir specifiski noteiktiem darbu pasūtījumu veidiem.

| Kopsavilkuma cilne | Lauks | Darba pasūtījuma veids |
|---|---|---|
| Vietas direktīvas | Novietot pēc | Pirkšanas pasūtījumi |
| Vietas direktīvas | Piemērojamais atgriešanas metodes kods | Pirkšanas pasūtījumi |
| Vietas direktīvas | Atgriešanas metodes kods | Pirkšanas pasūtījumi |
| Vietas direktīvas | Piemērojamais atgriešanas metodes kods | Pabeigto preču izvietošana |
| Vietas direktīvas | Atgriešanas metodes kods | Pabeigto preču izvietošana |
| Vietas direktīvas | Piemērojamais atgriešanas metodes kods | Atgrieztie pasūtījumi |
| Vietas direktīvas | Atgriešanas metodes kods | Atgrieztie pasūtījumi |
| Vietas direktīvas | Piemērojamais atgriešanas metodes kods | Kanban izvietošana |
| Vietas direktīvas | Piemērojamais atgriešanas metodes kods | Kanban izdošana |
| Līnijas | Tūlītējas papildināšanas veidne | Pārdošanas pasūtījumi |
| Līnijas | Tūlītējas papildināšanas veidne | Izejmateriālu izdošana |
| Līnijas | Tūlītējas papildināšanas veidne | Pārsūtīt izejas plūsmu |
| Līnijas | Tūlītējas papildināšanas veidne | Kanban izdošana |

## <a name="open-the-location-directives-page"></a>Atvērt atrašanās vietas direktīvu lapu

Lai atvertu lapu **Novietojuma direktīvas**, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Novietojuma direktīvas**.

No turienes varat apskatīt, izveidot un rediģēt savas atrašanās vietas direktīvas, izmantojot darbības rūts komandas. Informāciju par to, kā izmantot visus lapā pieejamos laukus, skatīt pārējās šīs tēmas sadaļās.

## <a name="action-pane"></a>Darbības rūts

Darbību rūtī **Novietojuma direktīvas** ir iekļautas pogas, ko varat izmantot, lai izveidotu, rediģētu un dzēstu direktīvas (**Rediģēt**, **Izveidot** un **Dzēst**). Tajā ir arī šādas pogas, kas ļauj pielāgot secību, kādā atrašanās vietas direktīva tiek apstrādāta, un konfigurēt vaicājumu, kas nosaka novietojuma direktīvas piemērošanas kritērijus:

- **Pārvietot uz augšu** — Pārvietojiet atlasīto atrašanās vietas direktīvu uz augšu secībā. Piemēram, varat pārvietot to no sērijas 4. numura uz sērijas 3. numuru.
- **Pārvietot uz leju** — pārvietojiet atlasīto atrašanās vietas direktīvu uz leju secībā. Piemēram, varat pārvietot to no sērijas 4. numura uz sērijas 5. numuru.
- **Rediģēt vaicājumu** — atveriet dialoglodziņu, kur varat definēt nosacījumus, pēc kuriem ir jāapstrādā atlasītā novietojuma direktīva. Piemēram, iespējams, vēlēsieties to piemērot tikai noteiktai noliktavai.

## <a name="location-directives-header"></a>Atrašanās vietas direktīvu virsraksts

Novietojuma direktīvas virsrakstā ir ietverti šādi lauki, kas attiecas uz secības numuru un aprakstošu atrašanās vietas direktīvas nosaukumu:

- **Sērijas numurs** — Šis lauks norāda secību, kādā sistēma mēģina piemērot katru novietojuma direktīvu atlasītajam darba pasūtījuma veidam. Vispirms piemēro zemus numurus. Varat mainīt secību, izmantojot pogas **Pārvietot uz augšu** un **Pārvietot uz leju** darbības rūtī.
- **Nosaukums** - Ievadiet atrašanās vietas direktīvas aprakstošu nosaukumu. Šim nosaukumam būtu jāpalīdz noteikt direktīvas vispārīgo mērķi. Piemēram, ievadiet *Pārdošanas pasūtījuma saņemšana noliktavā 24*.

## <a name="location-directives-fasttab"></a>Atrašanās vietas direktīvu kopsavilkuma cilne

Kopsavilkuma cilnes **Novietojuma direktīvas** lauki ir specifiski darba pasūtījuma veidam, kas ir atlasīts saraksta rūts laukā **Darba pasūtījuma veids**.

- **Darba veids** - Atlasiet veicamā darba veidu. Pieejamās vērtības ir atkarīgas no laukā **Darba pasūtījuma tips** atlasītā krājumu transakcijas veidu. Atlasiet vienu no šīm vērtībām:

    - **Izdošana** – novietojuma direktīva mēģinās atrast ideālāko vietu, lai izvietotu vai atrastu krājumu, kas nonāk sistēmā, izmantojot saņemšanas, ražošanas vai krājumu korekcijas. To var izmantot, lai definētu izvietošanu sagatavošanas vietā vai pie galīgās nosūtīšanas vietas angāra durvīm.
    - **Saņemt** – atrašanās vietas direktīva mēģinās atrast ideālākās vietas, no kurienes fiziski rezervēt krājumus (tas ir, izveidot darbu). Saņemšanu var pabeigt (tas ir, izdošanas darba rindu var slēgt) arī tad, ja darbs nav pabeigts. Lietotājs var veikt fizisku izdošanu. Sistēmā šī darbība ir izdošanas solis. Lietotājs pēc tam var atcelt darbību, izmantojot mobilo ierīci, un pabeigt darbu vēlāk. Tomēr, pabeidzot galīgo izdošanu, pirmais darba virsraksts tiek slēgts.

    > [!IMPORTANT]
    > Citas vērtības laukā **Darba veids** nav saistītas ar novietojuma direktīvām. Tās parādās tikai tāpēc, ka lauks nav filtrēts, lai atbilstu atlasītajam darba pasūtījuma veidam.

- **Vieta** - Šis lauks ir obligāts, jo atrašanās vietas direktīvai ir jābūt iespējai noteikt derīgu vietu un noliktavu.
- **Noliktava** - Šis lauks ir obligāts, jo atrašanās vietas direktīvai ir jābūt iespējai noteikt derīgu vietu un noliktavu.
- **Deriktīvas kods** - Atlasiet direktīvas kodu, ko saistīt ar darba veidni vai papildināšanas veidni. Lapā **Direktīvas kods** varat izveidot jaunus kodus, ko var izmantot darba veidņu vai papildināšanas veidņu savienošanai ar atrašanās vietas direktīvām. Direktīvas kodus var izmantot arī, lai izveidotu saikni starp jebkuru darba veidnes rindu un atrašanās vietas direktīvu (piemēram, angāra durvis vai sagatavošanas vietas).

    > [!TIP]
    > Ja ir iestatīts direktīvas kods, sistēma nemeklēs atrašanās vietas direktīvas pēc kārtas numura, kad darbs ir jāveido. Tā vietā tas meklēs pēc direktīvas koda. Šādā veidā varat precīzāk norādīt, kāda vietas veidne darba veidnē tiek izmantota noteiktai darbībai, piemēram, materiālu sagatavošana.

- **Vairāki SKU** - Iestatiet šo opciju uz *Jā*, lai atrašanās vietā varētu izmantot vairākas noliktavas vienības (SKU). Piemēram, ir jāiespējo vairākas SKU angāra durvju novietojumam. Ja iespējojat vairākas SKU, jūsu novietojums tiks norādīts darbā, kā paredzēts. Tomēr izvietošanas novietojums varēs apstrādāt tikai vairāku krājumu izvietošanu (ja darbs ietver dažādas SKU, kas ir jāsaņem un jānovieto). Tas nevarēs apstrādāt vienu SKU izvietošanu. Ja šī opcija ir iestatīta uz *Nē*, jūsu novietojums tiks norādīts tikai tad, ja jūsu izvietošanai ir tikai viena veida SKU.

    > [!IMPORTANT]
    > Lai varētu veikt gan vairāku vienumu, gan vienas SKU izvietošanu, ir jānorāda divas rindas ar vienādu struktūru un iestatījumiem, bet vienai rindai ir jāiestata opcija **Vairākas SKU** uz *Jā* vienai rindai un *Nē* citai. Tāpēc, lai veiktu izvietošanas operācijas, jums ir jābūt divām identiskām atrašanās vietas direktīvām, pat ja jums nav jāatšķir atsevišķas SKU un vairāki SKU uz darba ID. Bieži, ja nav iestatītas abas šīs atrašanās vietas direktīvas, neparedzētas biznesa procesu atrašanās vietas tiks iegūtas no izmantotās atrašanās vietas direktīvas. Ja nepieciešams apstrādāt pasūtījumus, kas ietver vairākas noliktavas vienības, ir jāizmanto līdzīgi iestatījumi novietojuma direktīvām, kurām ir *saņemt* no **Darba tips**.

    Lietojiet opciju **Vairākas SKU** darba rindām, kas apstrādā vairāk nekā vienu krājuma numuru. (Krājuma kods darba informācijā būs tukšs, un tas tiks attēlots kā **Vairākas** noliktavas programmas apstrādes lapās.)

    Tipiskā piemērā darba veidne ir iestatīta tā, lai tai būtu vairāk nekā viens saņemšanas/izvietošanas pāris. Šādā gadījumā, iespējams, vēlēsities meklēt noteiktu izstādīšanas atrašanās vietu, ko izmantot rindām ar *Izvietošana* no **Darba veids**.

    > [!NOTE]
    > Ja opcija **Vairākas SKU** ir iestatīta uz *Jā*, nevar atlasīt **Rediģēšanas vaicājumu** darbības rūtī, jo vaicājumu nevar novērtēt krājumu līmenī, ja ir vairāki krājumi. Lai nodrošinātu, ka ir atlasīta vēlamā novietojuma direktīva, izmantojiet lauku **Direktīvas kods**, lai vadītu novietojuma direktīvas atlasi, kas saistīta ar izvietošanas rindām, kur šis direktīvas kods tiek piešķirts darba veidnē.

    Ja jūs vienmēr strādājat ar vienas vienības vai jaukta krājuma operācijām, ir svarīgi definēt divas novietojuma direktīvas *Izvietošanas* darba veidam: viens, kur opcija **Vairākas SKU** ir iestatīta uz *Jā* un, kur tā ir iestatīta uz *Nē*.

- **Piemērojamais izvietojuma kods** - Norādiet, vai atrašanās vietas direktīvas atgriešanas metodes kodam ir jāatbilst atgriešanas metodes kodam, kas tiek lietots, kad krājums ir saņemts, vai arī atrašanās vietas direktīvu var atlasīt, pamatojoties uz jebkuru atgriešanas metodes kodu. Ja atlasīsiet *Precīza atbilstība*, bet lauks **Atgriešanas metodes kods** ir tukšs, šai atrašanās vietas direktīvai tiks izmantot tikai tukši atgriešanas metodes kodi.

    > [!NOTE]
    > Šis lauks ir pieejams tikai atlasītajiem darba pasūtījumu veidiem, kur ir atļauta papildināšana. Pilnīgu sarakstu skatiet sadaļā [Lauki, kas ir raksturīgi darbu pasūtījumu veidiem](#fields-specific-types) iepriekš šajā tēmā.

- **Atrast pēc** – Norādiet, vai saņemtam daudzumam jābūt visam numura zīmes daudzumam, vai arī tam jābūt krājumam pēc krājuma. Lietojiet šo lauku, lai nodrošinātu, ka viss numura zīmes saturs tiek novietots vienā vietā un ka sistēma nepiedāvā sadalīt saturu vairākās vietās **IPPN** (numura zīmes saņemšanas), **Jauktas numura zīmes** saņemšanas un **Klasteru** saņemšanas procesiem. ( **Klasteru** saņemšanas procesam nepieciešams, lai būtu ieslēgts līdzeklis *Kastera saņemšanas līdzeklis* .) Atrašanās vietas direktīvas vaicājuma, rindu un novietojuma direktīvas darbības var atšķirties atkarībā no atlasītās vērtības. Kopsavilkuma cilne **Rindas** izmanto tikai tad, ja **Atrast** pēc ir iestatīts uz *Krājums*.

    > [!NOTE]
    > Šis lauks ir pieejams tikai atlasītajiem darba pasūtījumu veidiem, kur ir atļauta papildināšana. Pilnīgu sarakstu skatiet sadaļā [Lauki, kas ir raksturīgi darbu pasūtījumu veidiem](#fields-specific-types).

- **Izvietojuma kods** — Šis lauks tiek izmantots novietojuma direktīvās, kurām ir darba pasūtījuma veidi *Pirkšanas pasūtījumi*, *Pabeigto produktu saņemšana* vai *Atgriešanas pasūtījumi* un darba veids *Izvietošana*. Izmantojiet to, lai vadītu plūsmu, izmantojot noteiktu novietojuma direktīvu, atkarībā no izvietojuma koda, ko darbinieks atlasīja noliktavas programmā. Piemēram, var nosūtīt atpakaļ atgrieztos produktus uz pārbaudes atrašanās vietu, pirms tie tiek atgriezti krājumos. Izvietojuma kodu var saistīt ar krājumu statusu. Šādā veidā to var izmantot, lai mainītu krājuma statusu kā saņemšanas procesa daļu. Piemēram, jums ir izvietojuma kods, *QA*, kas iestata krājuma statusu uz *QA*. Pēc tam varat izmantot atsevišķu atrašanās vietas direktīvu, lai pārvietotu šo krājumu uz karantīnas novietojumu.

    > [!NOTE]
    > Šis lauks ir pieejams tikai atlasītajiem darba pasūtījumu veidiem, kur ir atļauta papildināšana. Pilnīgu sarakstu skatiet sadaļā [Lauki, kas ir raksturīgi darbu pasūtījumu veidiem](#fields-specific-types).

## <a name="lines-fasttab"></a>Rindas kopsavilkuma cilne

Izmantojiet kopsavilkuma cilni **Rindas**, lai izveidotu nosacījumus saistīto darbību piemērošanai, kas ir norādītas kopsavilkuma cilnē **Novietojuma direktīvas darbības**. Katrai rindai var norādīt minimālo daudzumu un maksimālo daudzumu, uz kuru darbības jāattiecina. Var arī norādīt, ka darbības ir jāizmanto specifiskai krājuma vienībai.

- **Sērijas numurs** - Ievadiet secību, kādā atlasītajam darba tipam jāapstrādā katra novietojuma direktīvas rinda. Varat mainīt secību, izmantojot pogas **Pārvietot uz augšu** un **Pārvietot uz leju** rīkjoslā.
- **No daudzuma** – Norādiet to daudzumu diapazona sākumu, uz kuriem attiecas rinda. Laukā **Vienība** norādiet šim daudzumam izmantojamo mērvienību.
- **Līdz daudzumam** – Norādiet to daudzumu diapazona beigas, uz kuriem attiecas rinda. Laukā **Vienība** norādiet šim daudzumam izmantojamo mērvienību.
- **Vienība** - Atlasiet krājumu mērvienību. Varat norādīt minimālo daudzumu un maksimālo daudzumu, kuram direktīva jāpiemēro, kā arī varat norādīt, ka direktīvai jābūt paredzētai noteiktai krājuma vienībai. Lauks **Vienība** tiek izmantots *tikai* daudzuma novērtēšanai. Lai noteiktu, vai ir spēkā novietojuma direktīvas rinda, sistēma izmanto daudzumu vienībā, kas norādīta šajā rindā. Katru reizi, kad tā sasniedz atrašanās vietas direktīvas rindu, sistēma mēģina pārveidot pieprasījuma vienību uz rindu norādīto vienību. Ja mērvienību pārvēršana nepastāv, sistēma pārvietojas uz nākamo rindu.
- **Daudzuma atrašana** — Šis lauks tiek izmantots tikai laikā, kad notiek mēģinājumi ievietot vai atrast krājumus noliktavā. (Tādēļ to piemēro tikai tad, ja **Darba tipa** lauks ir iestatīts uz *Izdot*). Atlasiet vienu no šīm vērtībām, lai norādītu daudzumu, kas tiek izmantots, lai novērtētu, vai daudzums ir **No daudzuma** **Līdz daudzumam** diapazonā:

    - **Numura zīmju daudzums** — Izmantojiet saņemto numura zīmju daudzumu.
    - **Izmantotais daudzums** — Izmantojiet darbības laikā izmantoto daudzumu. Piemēram, jūs saņēmāt daudzumu 1 000 noliktavā un sadalāt to 10 numura zīmēs, no kurām katrai ir daudzums 100. Šādā gadījumā varat izmantot daudzumu 1 000 krājumu, nevis numura zīmes daudzumu 100.
    - **Atlikušais daudzums** — Izmantojiet daudzumu, kas joprojām ir jāsaņem pirkšanas pasūtījuma rindā, kas tiek apstrādāta.
    - **Plānotais daudzums** — Izmantojiet pirkšanas pasūtījuma rindas kopējo daudzumu neatkarīgi no tā, kas jau ir saņemts.

- **Ierobežot pēc vienības** — Šī izvēles rūtiņa ļauj izveidot novietojuma direktīvas rindu, kas ir raksturīga mērvienībai vai vairākām mērvienībām. Atzīmējiet to, lai ierobežotu mērvienības, kas tiek uzskatītas par derīgiem novietojuma direktīvas rindu atlases kritērijiem. Šī funkcionalitāte darbojas tikai atrašanās vietas direktīvām, kur lauks **Darba veids** ir iestatīts uz *Saņemt*.

    Piemēram, rezervējot daudzumus, vēlaties rezervēt paletes tikai no noteiktas atrašanās vietu kopas. Šādā gadījumā rindas ierobežos šo secību paletes, tādā veidā, lai jebkurš daudzums, kas ir mazāks par paleti, netiks izvēlēts novietojuma direktīvai.

    Ievērojiet, ka izvēles rūtiņa **Ierobežot pēc vienības** nekontrolē vienību vai vienības, kas tiek pielietotas darba rindās. Vienības ierobežojums attiecas tikai uz vienībām, kas padarītas pieejamas, izmantojot vienību secību grupu. Piemēram, vienība ir saistīta ar vienību secību grupu, kas ietver gan vienību *paletes*, gan vienību *gabali*. Mērvienības ir definētas, kad 1 palete = 100 gabali, un novietojuma direktīvā tiek izmantota funkcionalitāte **Ierobežot pēc vienības** tikai paletēm. Turklāt ir definēta darba veidne, kas ierobežo darba virsraksta izveidi uz 50 gab. Šādā gadījumā tiks izveidotas darba rindas no 50 gabaliem. Lai norādītu ierobežojuma mērvienību, veiciet tālāk norādītās darbības:

    1. Kopsavilkuma cilnē **Rindas** rīkjoslā atlasiet **Ierobežot pēc vienības**. (Šī poga kļūst pieejama tikai pēc tam, kad rindā esat atlasījis izvēles rūtiņu **Ierobežot pēc vienības** un pēc tam atlasījis **Saglabāt**.)
    1. Lapā **Ierobežot pēc vienībām** laukā **Vienība** atlasiet mērvienību, ar kuru vēlaties ierobežot saņemšanas un izvietošanas procesus.

- **Noapaļot līdz vienībai** — Šis lauks darbojas kopā ar izvēles rūtiņu **Ierobežot pēc vienības**. Piemēram, ja opcijas  **Ierobežot pēc vienības** un **Noapaļot līdz vienībai** tiek atlasīti atrašanās vietas direktīvas rindā, darbs, kas ģenerēts no direktīvas izejmateriāla saņemšanai ir jānoapaļo ar precizitāti līdz vienai apstrādes vienībai, kas ir norādīts lapā **Ierobežot pēc vienības**.

    > [!NOTE]
    > Šis **Noapaļot līdz vienībai** iestatījums darbojas tikai darba pasūtījuma veidam *Izejmateriāla saņemšana*, un tikai novietojuma direktīvās, kur lauks **Darba veids** ir iestatīts uz *Saņemt*.

- **Atrast iepakojuma daudzumu** — Ja pārdošanas pasūtījumā, pārsūtīšanas pasūtījumā vai ražošanas pasūtījumā tiek norādīts iepakojuma daudzums, šī izvēles rūtiņa ļauj ierobežot sistēmu, lai varētu atlasīt tikai tās atrašanās vietas, kurās ir vismaz tāds iepakošanas daudzums.

    > [!NOTE]
    > Šī funkcionalitāte darbojas tikai ar *Saņemt* veida vietas direktīvām.

- **Atļaut sadalīšanu** - Norāda, vai vietas direktīva var sadalīt saņemto daudzumu vai daudzumu, kas ir rezervēts vairāku noliktavu vietās, vai arī visam daudzumam jāatrodas vienā vietā vai tas ir jārezervē no vienas vietas, lai varētu izveidot darbu.
- **Tūlītēja papildināšanas veidne** - Izmantojiet šo lauku, lai izveidotu savienojumu ar papildināšanas veidni, lai nekavējoties sāktu papildināšanu, ja krājumi nav piešķirti. Ja atstājat šo lauku tukšu, krājumu papildināšana netiks sākta, līdz visas atrašanās vietas direktīvas rindas nebūs apstrādātas.

    > [!NOTE]
    > Šis lauks ir pieejams tikai atlasītajiem darba pasūtījumu veidiem, kur ir atļauta papildināšana. Pilnīgu sarakstu skatiet sadaļā [Lauki, kas ir raksturīgi darbu pasūtījumu veidiem](#fields-specific-types).

## <a name="location-directive-actions-fasttab"></a>Atrašanās vietas direktīvas darbību kopsavilkuma cilne

Var definēt vairākas novietojuma direktīvas darbības katrai rindai. Un atkal — kārtas numurs tiek izmantots, lai noteiktu secību, kādā darbības tiek novērtētas. Šajā līmenī varat iestatīt vaicājumu, lai definētu, kā var atrast vislabāko novietojumu noliktavā. Varat arī izmantot iepriekš definētas **Stratēģijas** vērtības, lai atrastu optimālu novietojumu.

- **Sērijas numura** - Šis lauks parāda secību, kādā darbības ir apstrādātas atlasītajam darba tipam. Varat mainīt secību, izmantojot pogas **Pārvietot uz augšu** un **Pārvietot uz leju** rīkjoslā.
- **Nosaukums** - Ievadiet novietojuma direktīvas darbības nosaukumu. Esiet precīzi, lai darbība, kas tiek veikta, būtu skaidri saprotama no nosaukuma.
- **Fiksētā novietojuma lietojums** — Norādiet atrašanās vietas, kas jāņem vērā atrašanās vietas direktīvā. Atlasiet vienu no šīm vērtībām:

    - **Fiksētas un nefiksētas vietas** - vietas direktīva ņem vēra visas vietas.
    - **Tikai fiksētas vietas precei** - vietas direktīva ņem vērā precēm tikai fiksētas vietas.
    - **Tikai fiksētas vietas preces variantam** - vietas direktīva ņem vērā preces variantiem tikai fiksētas vietas.

- **Atļaut negatīvus krājumus** - Atzīmējiet šo izvēles rūtiņu, lai vietas direktīvās atļautu negatīvus krājumus norādītajā noliktavas vietā.
- **Partija iespējota** - Atzīmējiet šo izvēles rūtiņu, lai lietotu partijas stratēģijas krājumiem, kam ir iespējotas partijas. Ir svarīgi atzīmēt šo izvēles rūtiņu procesiem, kuri izmanto novietojuma direktīvas, lai atrastu atrašanās vietas, no kurām saņemt partijas numura izsekotos krājumus. Šādā veidā tiek iekļauta atrašanās vietu meklēšana, kas ietver partijas numura izsekotos krājumus. Ja ir atzīmēta šī izvēles rūtiņa, un **Stratēģijas** lauks ir iestatīts uz *Nav*, sistēma pārvietosies uz nākamo darbības rindu.
- **Stratēģija** - Lai varētu vieglāk un ātrāk definēt darbības, kas ir saistītas ar katru novietojuma direktīvas rindu, varat izvēlēties kādu no šiem iepriekš definētajām stratēģijām:

    - **Nav** – neviena stratēģija netiks izmantota.
    - **Saskaņo iepakojuma daudzumu** - šī stratēģija pārbauda, vai saņemšanas vietā ir norādītais iepakojuma daudzums. Šī stratēģija ir derīga tikai tad, ja **Darba tipa** lauks ir iestatīts uz *Saņemt*.
    - **Konsolidēt** - šī stratēģija konsolidē krājumus noteiktā vietā, ja jau ir pieejami līdzīgi krājumi. Šī stratēģija ir derīga tikai tad, ja **Darba tipa** lauks ir iestatīts uz *Izdot*. Parastas izdošanas iestatīšanas sistēma mēģina konsolidēt pirmajā darbības rindā un pēc tam otrajā rindā to mēģina izveidot bez konsolidācijas. Preču konsolidēšana padara efektīvāku vēlāku izdošanu.
    - **FEFO partijas rezervēšana** — Šī stratēģija izmanto pirmo beigu termiņu, pirmās izejas (FEFO) partijas rezervāciju. Izmantojiet to, ja krājumi tiek novietoti, izmantojot partijas beigu datumu, un tiek piešķirti partijas rezervācijai. Šo stratēģiju var izmantot tikai krājumiem, kuriem iespējotas partijas. Tā ir derīga tikai tad, ja **Darba tipa** lauks ir iestatīts uz *Saņemt*.
    - **Noapaļot līdz pilnai LP un FEFO partijai** — Šī stratēģija apvieno stratēģijas elementus *FEFO partijas rezervācija* un *Noapaļot līdz pilnam LP*. Tas ir derīgs tikai partijas iespējotiem krājumiem un novietojuma direktīvām, kurām ir *Saņemt* darba tips. Lai izmantotu stratēģiju *FEFO partijas rezervēšana*, rindai jābūt partijas iespējotai, un stratēģiju *Noapaļot līdz pilnam LP* var izmantot tikai papildināšanai. Ja šī stratēģija ir konfigurēta kopā ar atrašanās vietas uzkrājumu limitu, tas var izraisīt atlasītās ievietošanas darba vietas pārslogošanu un krājumu veidošanas ierobežojumu ignorēšanu.
    - **Noapaļot uz augšu līdz pilnai NV** - šī stratēģija tiek izmantota, lai noapaļotu krājumu daudzumu, lai tas atbilstu noliktavas vienību daudzumam, kas ir piešķirts izdodamajiem krājumiem. Šo stratēģiju var izmantot tikai *Saņemt* veida papildināšanas novietojuma direktīvām. Ja šī stratēģija ir konfigurēta kopā ar atrašanās vietas uzkrājumu limitu, tas var izraisīt atlasītās ievietošanas darba vietas pārslogošanu un krājumu veidošanas ierobežojumu ignorēšanu.
    - **Numura zīmes vadīšana** - Izmantojiet šo stratēģiju, izlaižot pasūtījumu nosūtīšanai uz noliktavu, lai izveidotu izdošanas un izvietošanas darbu, atrašanās vietas direktīvā tiek izmantota stratēģija. Šo pieeju var izmantot vairākām numura zīmēm. Šī stratēģija mēģinās rezervēt un izveidot izdošanas darbu novietojumos, kur tiek glabātas pieprasītās noliktavas vienības, kas ir saistītas ar pārsūtīšanas pasūtījuma rindām. Tomēr, ja šīs darbības nevar pabeigt, bet joprojām vēlaties izveidot izdošanas darbu, jums vajadzētu atgriezties pie citas atrašanās vietas direktīvas darbību stratēģijas. Atkarībā no jūsu biznesa procesu prasībām, iespējams, vēlēsities meklēt arī citā noliktavas apgabalā.
    - **Tukša vieta bez ienākoša darba** - Izmantojiet šo stratēģiju, lai atrastu tukšas vietas. Novietojums tiek uzskatīts par tukšu, ja tam nav fizisku krājumu un nav gaidāms ienākošais darbs. Šo stratēģiju var izmantot tikai *Saņemt* darba veida novietojuma direktīvām.
    - **Atrašanās vietas vecumstruktūras FIFO** - Izmantot FIFO (first in, first out) stratēģiju, lai nosūtītu gan partijas izsekotos krājumus, gan partijas neizsekotos krājumus, pamatojoties uz datumu, kad krājumi ievadīti noliktavā. Šī iespēja var būt īpaši noderīga partijas neizsekotajiem krājumiem, kuru beigu datums nav pieejams kārtošanai. FIFO stratēģija atrod novietojumu, kas ietver vecāko vecumstruktūras datumu, un tad piešķir izdošanu, pamatojoties uz šo vecumstruktūras datumu.
    - **Atrašanās vietas vecumstruktūras LIFO** - Izmantot LIFO (last in, last out) stratēģiju, lai nosūtītu gan partijas izsekotos krājumus, gan partijas neizsekotos krājumus, pamatojoties uz datumu, kad krājumi ievadīti noliktavā. Šī iespēja var būt īpaši noderīga partijas neizsekotajiem krājumiem, kuru beigu datums nav pieejams kārtošanai. LIFO stratēģija atrod novietojumu, kas ietver jaunāko vecumstruktūras datumu, un tad piešķir izdošanu, pamatojoties uz šo vecumstruktūras datumu.

## <a name="example-using-location-directives"></a>Piemērs: atrašanās vietas direktīvu izmantošana

Šajā piemērā ir aprakstīts pirkšanas pasūtījuma process, kur vietas direktīvai ir jāatrod brīva vieta noliktavā krājuma vienībām, kas ir tikko reģistrētas saņemšanas dokā. Vispirms ir jāatrod brīva vieta noliktavā, konsolidējot rīcībā esošos krājumus. Ja konsolidācija nav iespējama, tad ir jāatrod tukša vieta.

Šādā gadījumā ir jādefinē divas vietas direktīvas darbības. Pirmajai darbībai secībā ir jāizmanto stratēģija *Konsolidēt* un otrajai vajadzētu izmantot stratēģiju *Tukšs novietojums bez ienākoša darba*. Ja tiek definēta trešā darbība pārpildes scenārija apstrādei, iespējami divi galarezultāti, kurā noliktavā vairs nav vietas: darbu var izveidot arī tad, ja nav definētas vietas, vai darba izveides process var neizdoties. Rezultātu nosaka iestatījumi lapā **Novietojuma direktīvas kļūmes**, kur varat izlemt, vai atlasīt opciju **Pārtraukt darbu, ja rodas ar novietojuma direktīvu saistīta kļūme** katram darba pasūtījuma tipam.

## <a name="next-step"></a>Nākošais solis

Pēc novietojuma direktīvu izveides katru direktīvas kodu var saistīt ar darba izveides darba veidnes kodu. Papildinformāciju skatiet šeit: [Noliktavas darba kontrolēšana, izmantojot darbu veidnes un novietojuma direktīvas](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="additional-resources"></a>Papildu resursi

- Video: [Noliktavas pārvaldības konfigurācija Deep Dive](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Palīdzības tēma: [Kontrolēt noliktavas darbu, izmantojot darbu veidnes un novietojuma direktīvas](control-warehouse-location-directives.md)
