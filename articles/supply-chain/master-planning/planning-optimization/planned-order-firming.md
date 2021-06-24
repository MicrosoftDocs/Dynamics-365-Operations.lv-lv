---
title: Plānoto pasūtījumu apstiprināšana
description: Šajā tēmā skaidrots, kā apstiprināt plānotos pasūtījumus. Kad plānotie pasūtījumi ir apstiprināti, tie kļūst par faktiskajiem pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem vai ražošanas pasūtījumiem.
author: ChristianRytt
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e2fc40e3e9874d47dd51e773628ba1ce75b8ebab
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193885"
---
# <a name="firm-planned-orders"></a>Plānoto pasūtījumu apstiprināšana

[!include [banner](../../includes/banner.md)]

Plānotie pasūtījumi *jāapstiprina* (t.i., jāizlaiž) kā daļa no vispārējās plānošanas procesa. Kad plānotie pasūtījumi ir apstiprināti, tie kļūst par faktiskajiem pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem vai ražošanas pasūtījumiem. Tie pasūtījumi ir zināmi arī kā *izlaistie pasūtījumi* vai *atvērtie pasūtījumi*.

Ir trīs plānoto pasūtījumu apstiprināšanas metodes:

- **Manuāla apstiprināšana** – atlasiet sarakstā noteiktus plānotos pasūtījumus un pēc tam manuāli sāciet procesu.
- **Automātiskā apstiprināšana** – nosakiet noklusēto apstiprināšanas periodu vajadzības grupām, atsevišķiem krājumiem un krājumu un vispārējo plānu kombinācijām. Pēc tam vispārējās plānošanas izpildes laikā plānotie pasūtījumi tiks automātiski apstiprināti, ja pasūtījuma datums ir norādītajā apstiprināšanas periodā.
- **Apstiprināšana, pamatojoties uz vaicājumu** – definējiet vaicājumu, lai atlasītu plānotos pasūtījumus, pamatojoties uz to rekvizītiem. Jūs variet iestatīt pakešuzdevumu, lai palaistu vaicājumu un apstiprinātu atbilstošus pasūtījumus regulārā grafikā.

Šajā tēmā ir sīkāk aprakstīta katra metode.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Iespējot šajā tēmā aprakstītos līdzekļus

Visplānoto pasūtījumu līdzekļi ir pieejami visās standarta Microsoft Dynamics 365 Supply Chain Management instalācijās, kas izmanto plānošanas optimizāciju. Tomēr daži no šajā tēmā aprakstītajiem līdzekļiem pirms to izmantošanas ir jāieslēdz līdzekļu pārvaldībā.

### <a name="enable-parallelized-firming-of-planned-orders"></a>Plānoto pasūtījumu paralēlas apstiprināšanas iespējošana

Paralēla apstiprināšana palīdz paātrināt apstiprināšanas procesu, to paralējot starp vairākiem pavedieniem. Šī pieeja var būt noderīga, kad daudzi plānotie pasūtījumi ir apstiprināti.

Lai padarītu šo funkcionalitāti pieejamu jūsu sistēmā, dodieties uz sadaļu [Līdzekļu pārvaldība](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet līdzekli *Paralēlā plānoto pasūtījumu apstiprināšana*.

### <a name="enable-planned-order-firming-with-filtering"></a>Iespējot plānoto pasūtījumu apstiprināšanas ar filtrēšanu

Plānotā pasūtījumu apstiprināšana ar filtrēšanu ļauj definēt loģiskos kritērijus, lai atlasītu, kurus plānotos pasūtījumus apstiprināt. Var arī priekšskatīt, kuri plānotie pasūtījumi tika atlasīti, palaist procesu fonā un/vai plānot kā pakešuzdevumu.

Lai padarītu šo funkcionalitāti pieejamu jūsu sistēmā, dodieties uz sadaļu [Līdzekļu pārvaldība](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet līdzekli *Plānoto pasūtījumu apstiprināšana ar filtrešanu*.

### <a name="enable-auto-firming-for-planning-optimization"></a>Iespējot automātisko apstiprināšanu plānošanas optimizācijai

Automātiskā apstiprināšana ļauj apstiprināt plānotos pasūtījumus kā daļu no vispārējās plānošanas procesa, laika periodā apstiprināšanai. Plānošanas programmā, kas ir veidota Supply Chain Management, vienmēr tiek atbalstīta automātiskā apstiprināšana. Tomēr, lai izmantotu to arī ar plānošanas optimizāciju, ir jāieslēdz līdzeklis.

Lai padarītu šo funkcionalitāti pieejamu jūsu sistēmā, dodieties uz sadaļu [Līdzekļu pārvaldība](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet līdzekli *Automatiskā apstiprināšana plānošanas optimizācijai*.

## <a name="manually-firm-planned-orders"></a>Manuāli apstiprināt plānotos pasūtījumus

Lai manuāli apstiprinātu plānotos pasūtījumus, atrodiet un atlasiet plānotos pasūtījumus, ko vēlaties apstiprināt, un pēc tam apstiprināšanas procesu sāciet manuāli.

1. [Atveriet jebkuru plānoto pasūtījumu saraksta lapu](approved-planned-order.md#view-planned-orders).
1. Izmantojiet lauku **Filtrs**, lauku **Plāns** un kolonnu virsrakstus, lai filtrētu un kārtotu sarakstu, lai varētu atrast meklētos plānotos pasūtījumus.
1. Atzīmējiet katram apstiprinātām plānotām pasūtījumam izvēles rūtiņu. Ja vēlaties apstiprināt visus plānotos pasūtījumus, kas pašlaik uzskaitīti lapā (pamatojoties uz pielietotajiem filtriem), izlaidiet šo darbību.
1. Darbību rūtī atlasiet vienu no šīm pogām:

    - **Apstiprināšana** – apstiprināt tikai atlasītos plānotos pasūtījumus.
    - **Apstiprināt visu** – apstiprināt visus plānotos pasūtījumus, kas pašlaik uzskaitīti lapā (pamatojoties uz lietotajiem filtriem), neatkarīgi no atlasītās izvēles rūtiņas. Šī opcija var būt noderīga, ja jūs apstiprinājiet daudz plānoto pasūtījumu.

1. Kopsavilkuma cilnes **Parametri** dialoglodziņā **Apstiprināšana** iestatiet šādus laukus. (Daudzi no šiem laukiem ņem noklusētās vērtības no **Standarta atjaunināšana** lapas cilnes **Vispārējā plānošana**.)

    - **Atjaunināt iezīmēšanu** - Atlasiet krājuma iezīmēšanas politiku, lai to izmantotu plānoto pasūtījumu apstiprināšanas laikā.
    - **Pārtraukt apstiprināšanu, ja rodas kļūda** – iestatiet šo opciju uz *Jā*, lai pārtrauktu visu atlasīto plānoto pasūtījumu apstiprināšanu, ja kādā no tiem rodas kļūda. Šī opcija jāiestata uz *Nē*, ja opcija **Paralelizēt apstiprināšanu** ir iestatīta uz *Jā*.
    - **Paralēla apstiprināšana** – šī opcija ir pieejama tikai tad, ja jūsu sistēmā ir ieslēgta [*Plānoto pasūtījumu paralēlā apstiprināšana* līdzeklis](#enable-features) un ja esat atlasījis divus vai vairākus plānotos pasūtījumus apstiprināšanas laikā. Iestatiet to uz *Jā*, lai apstiprināšanas procesus palaistu paralēli. Paralēla apstiprināšana var palīdzēt uzlabot veiktspēju.
    - **Pavedienu skaits** - šī opcija ir pieejama tikai tad, ja jūsu sistēmā ir ieslēgts [*Plānoto pasūtījumu paralēlā apstiprināšana* līdzeklis](#enable-features) un ja esat iestatījis opciju **Paralelizēt apstiprināšanu** uz *Jā*. Ievadiet pavedienu skaitu, ko izmantot apstiprināšanas procesa paralēlošanai. Papildinformāciju par to, kā izmantot šo opciju vispārējā plānošanā, skatiet sadaļā [Vispārējās plānošanas veiktspējas uzlabošanai](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > Lauka **Pavedienu skaits** vērtība *0* (nulle) palielina vispārējās plānošanas izpildes laiku. Tādēļ ieteicams vienmēr iestatīt šo lauku uz vērtību, kas ir lielāka par 0.

    - **Grupēt pēc kreditora** – iestatiet šo opciju kā *Jā*, lai grupētu plānotos pirkšanas pasūtījumus un apstiprināšanas laikā izveidotu vienu pirkšanas pasūtījumu kreditoram. Var arī izveidot vienu pirkšanas pasūtījumu ar vienu rindu katram plānotajam pasūtījumam.
    - **Grupēt pēc pircēja grupas** - iestatiet šo opciju uz *Jā*, lai sagrupētu plānotos pirkšanas pasūtījumus un izveidotu vienu pirkšanas pasūtījumu, kas apvieno kreditoru un pircēju grupu. Lai izmantotu šo opciju, iestatiet opciju **Grupēt pēc kreditora** uz *Jā*.
    - **Grupēt pēc pirkšanas līguma** – iestatiet šo opciju uz *Jā*, lai grupētu plānotos pirkšanas pasūtījumus, kuriem ir tāds pats kreditors kā esošiem pirkšanas līgumiem, un izveidotu vienu pirkšanas pasūtījumu katram pirkšanas līgumam. Ja ir aktivizēta opcija **Grupēt pēc kreditora**, šī opcija tiek aktivizēta automātiski. Lai izmantotu **Grupēt pēc pirkšanas līguma**, **Atrast pirkšanas līgumu** ir jāiestata uz *Jā* lapā **Vispārējās plānošanas parametri**.
    - **Grupēt pēc perioda** (sadaļā **Pirkšanas pasūtījums** ) – atlasiet periodu, pēc kā grupēt plānotos pirkšanas pasūtījumus. Lai izmantotu šo opciju, atlasiet opciju **Grupēt pēc kreditora**.
    - **Grupēt pēc perioda** (sadaļā **Transferi** ) – atlasiet periodu, pēc kā grupēt plānotos transfera pasūtījumus. Pasūtījumi tiks grupēti, pamatojoties uz vērtībām **No noliktavas** un **Uz noliktavu**.

    ![Dialoglodziņš Parametri dialoglodziņā Apstiprināšana](./media/manual-firming.png "Dialoglodziņš Parametri dialoglodziņā Apstiprināšana")

1. Kopsavilkuma cilnē **Palaist fonā** iestatiet darbu tā, lai tas darbotos pakešuzdevumu režīmā. Tomēr nav nozīmes iestatīt periodisku grafiku, ja veicat manuālu apstiprināšanas darbu. Lauki darbojas tāpat, kā citi [fona darbu](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management. Tomēr manuālai apstiprināšanai pakešuzdevums apstrādās tikai pašlaik atlasītos plānotos pasūtījumus. Netiks apstrādāts neviens pasūtījums, kas atbilst lapā pašreiz lietotajiem filtriem.
1. Atlasiet **Labi**, lai lietotu iestatījumus un ģenerētu apstiprinātos pasūtījumus.

## <a name="auto-firm-planned-orders"></a>Plānoto pasūtījumu automatiskā apstiprināšana

Automātiskā apstiprināšana ļauj apstiprināt plānotos pasūtījumus kā daļu no vispārējās plānošanas procesa. Var definēt apstiprināšanas periodu vajadzības grupām, atsevišķiem krājumiem un krājumu un vispārējo plānu kombinācijām. Pēc tam vispārējās plānošanas izpildes laikā plānotie pasūtījumi tiks automātiski apstiprināti, ja pasūtījuma datums ir norādītajā apstiprināšanas periodā. Plānotie pasūtījumi, kas tiek ģenerēti, veicot plānošanas optimizāciju, un iebūvētā vispārējās plānošanas operācija apstrādā pasūtījuma datumu (t.i., sākuma datumu) atšķirīgi.

> [!NOTE]
> Plānoto pirkšanas pasūtījumu automātisko apstiprināšanu var veikt tikai krājumiem, kas saistītie ar kreditoru.
> 
> Atvasinātiem pasūtījumiem (t.i. pakārtotie pirkšanas pasūtījumi), kas ir apstiprināti, būs statuss *Pārskatīšanā*, ja ir ieslēgta gadījuma izmaiņu izsekošana.

> [!IMPORTANT]
> Pirms šajā sadaļā aprakstīto līdzekli var izmantot kopā ar plānošanas optimizāciju, sistēmā ir jābūt ieslēgtam [*Plānošanas optimizācijas automātiskas apstiprināšanas* līdzeklim](#enable-features), kā aprakstīts šīs tēmas sākumā. Automātisko apstiprināšanas procesu vienmēr var izmantot ar iebūvēto vispārējās plānošanas programmu.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automātiskā apstiprināšana ar plānošanas optimizāciju pret iebūvēto plānošanas programmu

Plānošanas optimizāciju un iebūvēto plānošanas programmu, var izmantot, lai automātiski apstiprinātu plānotos pasūtījumus. Taču pastāv dažas svarīgas atšķirības. Piemēram, Plānošanas optimizācija izmanto pasūtījuma datumu (t.i., sākuma datumu), lai noteiktu, kurus plānotos pasūtījumus apstiprināt, tā kā iebūvētā plānošanas programma izmanto prasības datumu (t.i., beigu datumu). Sekojošajā tabulā ir apkopotas atšķirības.

| Funkcija | Plānošanas optimizācija | Iebūvēta plānošanas programma |
|---|---|---|
| **Bāzes datums** | Automātiskā apstiprināšana ir balstīta uz pasūtījuma datumu (sākuma datumu). | Automātiskā apstiprināšana ir balstīta uz prasības datumu (beigu datuma). |
| **Piegādes/izpildes laiks** | Tā kā pasūtījuma datums (sākuma datums) aktivizē apstiprināšanu, jums nav jāapsver izpildes laiks kā daļa no apstiprināšanas laika ierobežojuma. | Lai palīdzētu nodrošināt, ka pasūtījumi ir apstiprināti savlaicīgi, apstiprināšanas laika periodam jābūt ilgākam par izpildes laiku. |
| **Pasūtījumi šajā nedēļā** | Lai apstiprinātu visus pasūtījumus, kam jāsākas pašreizējās nedēļas laikā, apstiprināšanas laika periodam jābūt vienai nedēļai. | Lai apstiprinātu visus pasūtījumus, kam jāsākas pašreizējās nedēļas laikā, apstiprināšanas laika periodam jābūt izpildes laikam plus viena nedēļa. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Iestatiet automātisko apstiprināšanu un apstiprināšanas periodu

Automātiskā apstiprināšana tiek ieslēgta, piešķirot automatizētu apstiprināšanas periodu atbilstošajiem vajadzības iestatījumiem, kā aprakstīts tālāk šajā sadaļā. Ja automātiskā apstiprināšana nav ieslēgta visiem vajadzības iestatījumiem vai plānošana tiek sākta no noteiktas lapas, piemēram, no izlaistas preces lapas **Neto vajadzības**, automātiskās apstiprināšanas process tiek izlaists.

Automātiskās apstiprināšanas opciju grupēšana un atzīmēšana paņem vērtības no cilnes **Standarta atjauninājums** lapā **Vispārējās plānošanas parametri**.

Automātiskās apstiprināšanas periods tiek definēts pēc dienu skaita, kas tiek ievadīts atbilstošam vajadzības iestatījumam. Automatisko apstiprināšanu var ieslēgt un kontrolēt laika ierobežojumu šādos veidos:

- Lai definētu noklusējuma apstiprināšanas laika ierobežojumu nodrošinājuma grupai, dodieties uz **Vispārējā plānošana \> Iestatījumi \> Nodrošinājums \> Nodrošinājuma grupas** un atlasiet nodrošinājuma grupu. Pēc tam no kopsavilkuma cilnes **Citi** laukā **Automātisks apstiprināšanas periods (dienas)** ievadiet dienu skaitu.
- Lai pārrakstītu apstiprināšanas laika periodu, kas ir definēts konkrēta krājuma vajadzību grupai, pārejiet uz sadaļu **Preces informācijas pārvaldība \> Izlaistās preces**. Darbības rūtī atlasiet **Plāns** un pēc tam atlasiet **Krājuma nodrošinājums**. Cilnē **Vispārīgi** atlasiet **Ignorēt laika periodu** un pēc tam laukā **Automātisks apstiprināšanas periods (dienas)** ievadiet dienu skaitu.
- Lai pārrakstītu apstiprināšanas laika periodu, kas ir definēts nodrošinājuma grupai un krājumu nodrošinājumam noteiktam vispārējam plānam, dodieties uz **Vispārējā plānošana \> Iestatījumi \> Vispārējie plāni** un atlasiet vispārējo plānu. Pēc tam kopsavilkuma cilnē **Periods dienās** opciju **Apstiprināt** uzstādiet uz *Jā* un ievadiet dienu skaitu.

Ja visi iepriekš minētie laika periodi tiek iestatīti uz *0* (nulle), automātiskā apstiprināšana tiek efektīvi deaktivizēta atbilstošajiem segtajiem krājumiem.

## <a name="firm-planned-orders-by-using-a-query"></a>Plānoto pasūtījumu apstiprināšana, izmantojot vaicājumu

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

Uz vaicājumiem balstīta apstiprināšana ļauj plānot apstiprināšanu, pamatojoties uz iepriekš definētiem kritērijiem. Atšķirībā no automātiskās apstiprināšanas uz vaicājumiem balstīta apstiprināšana ļauj automātiski apstiprināt dažādas pasūtījumu apakškopas dažādos laika punktos. Turklāt, lai apstiprinātu dažādus plānoto pasūtījumu tipus, var izmantot gan manuālas, gan automatizētas operācijas. Varat arī priekšskatīt, kuri apstiprinātie pasūtījumi ir atlasīti, pamatojoties uz jūsu iestatījumiem. Tāpēc varat apstiprināt, ka atlase atbilst jūsu prognozēm.

Automātisko apstiprināšanu var apvienot ar vaicājumu apstiprināšanu. Piemēram, uz vaicājumu balstītam apstiprināšanas darbam ir nākotnes periods, kas ir garāks nekā laika periods atbilstošai automātiskās apstiprināšanas seguma konfigurācijai. Tādēļ uz vaicājumu balstīts apstiprināšanas darbs apstrādās tā plānotos pasūtījumus pirms automātiskās apstiprināšanas aktivizēšanas. Šo darbību var izmantot, lai plānotu pasūtījumus noteiktiem kreditoriem citādi nekā līdzīgu produktu pasūtījumus no citiem kreditoriem.

> [!IMPORTANT]
> Pirms šajā sadaļā aprakstīto līdzekli var izmantot, sistēmā ir jābūt ieslēgtam [*Plānotā pasūtījuma apstiprināšana ar filtrešanu* līdzeklim](#enable-features), kā aprakstīts šīs tēmas sākumā.

Lai apstiprinātu plānoto pasūtījumu, izmantojot apstiprināšanas procesu, kas balstīts uz vaicājumiem, veiciet šīs darbības.

1. Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Palaist \> Plānoto pasūtījumu apstiprināšana**.
1. Dialoglodziņā **Plānotā pasūtījuma apstiprināšana** kopsavilkuma cilnē **Parametri** iestatiet pamata apstrādes, atzīmēšanas un grupēšanas opcijas. Šīs opcijas darbojas tāpat, kā dialoglodziņā **Apstiprināšana**. (Skatiet iepriekšējo sadaļu aprakstiem.) Pēc tam sadaļā **Plāns** iestatiet šādus laukus, kas ir unikāli dialoglodziņam **Plānotā pasūtījuma apstiprināšana**:

    - **Plāns** – atlasiet vispārējo plānu, kas jālieto plānoto pasūtījumu apstiprināšanas laikā, kas atrodami šajā vaicājumā.
    - **Laika perioda dienas uz priekšu apstiprināšana** - var izvēlēties, cik tālu nākotnē ir jāaprēķina dažādas prasības un citi apsvērumi, izmantojot vispārējo plānošanu.
    - **Laika perioda dienas atpakaļ apstiprināšana** - var izvēlēties, cik tālu pagatnē ir jāaprēķina dažādas prasības un citi apsvērumi, izmantojot vispārējo plānošanu.

    ![Dialoglodziņš Parametri dialoglodziņā Plānoto pasūtījumu apstiprināšana](./media/planned-order-firming-main-1.png "Dialoglodziņš Parametri dialoglodziņā Plānoto pasūtījumu apstiprināšana")

1. Lai norādītu, kuri ieraksti ir jāiekļauj pasūtījumā, atlasiet pogu **Filtrs** kopsavilkuma cilnē **Iekļaujamie ieraksti**. Tiek atvērts standarta vaicājuma dialoglodziņš, kur varat definēt atlases kritērijus, kārtošanas kritērijus un savienojumus. Lauki darbojas tāpat, kā citi vaicājumu veidi pakalpojumā Supply Chain Management. Lauki šeit ir tikai lasāmi un parāda vērtības, kas saistītas ar jūsu vaicājumu.

    ![Dialoglodziņš Iekļaujamie ieraksti dialoglodziņā Plānoto pasūtījumu apstiprināšana](./media/planned-order-firming-main-2.png "Dialoglodziņš Iekļaujamie ieraksti dialoglodziņā Plānoto pasūtījumu apstiprināšana")

1. Atlasiet **Priekšskatījums**, lai priekšskatītu jūsu apstiprinātā pasūtījuma saturu, pamatojoties uz līdz šim veiktajiem iestatījumiem. Apstiprināmo plānoto pasūtījumu saraksts tiek parādīts kā ziņojums. Tad ir iespējams pielāgot savus iestatījumus pēc vajadzības, līdz priekšskatījums rāda apstiprināto pasūtījumu pēc jūsu nolūka.

    ![Apstiprinātā pasūtījuma priekšskatījuma piemērs](./media/planned-order-firming-preview.png "Apstiprinātā pasūtījuma priekšskatījuma piemērs")

    > [!WARNING]
    > Šis līdzeklis apstiprinās visus plānotos pasūtījumus, kas atbilst filtra kritērijiem. Nekritiska plānoto pasūtījumu apstiprināšana var radīt nevēlamu pirkšanas, pārsūtīšanas un ražošanas pasūtījumu skaitu. Pirms turpināt, vienmēr izmantojiet pogu **Priekšskatījums**, lai pārbaudītu iekļaujamos ierakstus.

1. Kopsavilkuma cilnē **Palaist fonā** iestatiet darbu tā, lai tas darbotos pakešuzdevumu režīmā un/vai iestatiet periodisku grafiku. Lauki darbojas tāpat, kā citi [fona darbu](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.
1. Atlasiet **Labi**, lai lietotu iestatījumus un ģenerētu apstiprinātos pasūtījumus.

## <a name="track-firmed-orders"></a>Atsekot apstiprinātos pasūtījumus

Lai izsekotu apstiprināto plānoto pasūtījumu, veiciet šīs darbības.

1. [Atveriet jebkuru plānoto pasūtījumu saraksta lapu](approved-planned-order.md#view-planned-orders).
1. Atveriet vai atlasiet plānoto pasūtījumu, kuru vēlaties izsekot.
1. Darbību rūtī cilnē **Skatīt** grupā **Skatīt** atlasiet **Apstiprināšanas vēsture**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
