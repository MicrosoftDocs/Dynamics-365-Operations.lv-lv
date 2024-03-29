---
title: Plānoto pasūtījumu apstiprināšana
description: Šajā rakstā skaidrots, kā apstiprināt plānotos pasūtījumus. Kad plānotie pasūtījumi ir apstiprināti, tie kļūst par faktiskajiem pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem vai ražošanas pasūtījumiem.
author: t-benebo
ms.date: 08/09/2022
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c2e4294cb54e9ba41467f505e361d5ee45f1f27d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740527"
---
# <a name="firm-planned-orders"></a>Plānoto pasūtījumu apstiprināšana

[!include [banner](../../includes/banner.md)]

Plānotie pasūtījumi *jāapstiprina* (t.i., jāizlaiž) kā daļa no vispārējās plānošanas procesa. Kad plānotie pasūtījumi ir apstiprināti, tie kļūst par faktiskajiem pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem vai ražošanas pasūtījumiem. Tie pasūtījumi ir zināmi arī kā *izlaistie pasūtījumi* vai *atvērtie pasūtījumi*.

Ir trīs plānoto pasūtījumu apstiprināšanas metodes:

- **Manuāla apstiprināšana** – atlasiet sarakstā noteiktus plānotos pasūtījumus un pēc tam manuāli sāciet procesu.
- **Automātiskā apstiprināšana** – nosakiet noklusēto apstiprināšanas periodu vajadzības grupām, atsevišķiem krājumiem un krājumu un vispārējo plānu kombinācijām. Pēc tam vispārējās plānošanas izpildes laikā plānotie pasūtījumi tiks automātiski apstiprināti, ja pasūtījuma datums ir norādītajā apstiprināšanas periodā.
- **Apstiprināšana, pamatojoties uz vaicājumu** – definējiet vaicājumu, lai atlasītu plānotos pasūtījumus, pamatojoties uz to rekvizītiem. Jūs variet iestatīt pakešuzdevumu, lai palaistu vaicājumu un apstiprinātu atbilstošus pasūtījumus regulārā grafikā.

Šajā rakstā ir sīkāk aprakstīta katra metode.

## <a name="enable-the-features-that-are-described-in-this-article"></a><a name="enable-features"></a> Iespējot šajā rakstā aprakstītos līdzekļus

Visplānotās pasūtījumu funkcijas ir pieejamas visās Microsoft standarta instalācijās Dynamics 365 Supply Chain Management. Tomēr dažas no šajā rakstā aprakstītajām funkcijām ir jāieslēdzas Līdzekļu pārvaldībā pirms to lietošanas.

### <a name="turn-parallelized-firming-of-planned-orders-on-or-off"></a>Ieslēgt vai izslēgt plānoto pasūtījumu paralēlo apstiprināšanas darbību

Paralēla apstiprināšana palīdz paātrināt apstiprināšanas procesu, to paralējot starp vairākiem pavedieniem. Šī pieeja var būt noderīga, kad daudzi plānotie pasūtījumi ir apstiprināti. Lai lietotu šo funkcionalitāti, *sistēmai jābūt* ieslēgtai plānoto pasūtījumu paralēlai apstiprināšanas funkcijai. 

No Piegādes ķēdes pārvaldības versijas 10.0.21 šī funkcija ir ieslēgta pēc noklusējuma. Tāpat kā Piegādes ķēdes pārvaldībai 10.0.25 šī funkcija ir obligāta un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.25, šo funkcionalitāti var ieslēgt vai izslēgt, [...](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)*dodoties* uz funkciju pārvaldību un meklējot līdzekli Plānoto pasūtījumu paralēla apstiprināšana.

### <a name="turn-planned-order-firming-with-filtering-on-or-off"></a>Ieslēgt vai izslēgt plānoto pasūtījumu apstiprināšana ar filtrēšanu

Plānotā pasūtījumu apstiprināšana ar filtrēšanu ļauj definēt loģiskos kritērijus, lai atlasītu, kurus plānotos pasūtījumus apstiprināt. Var arī priekšskatīt, kuri plānotie pasūtījumi tika atlasīti, palaist procesu fonā un/vai plānot kā pakešuzdevumu.

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.25, funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.29 versiju, administratori šo funkcionalitāti var ieslēgt vai izslēgt, *·*[meklējot](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Plānoto pasūtījumu apstiprināšanas ar filtrēšanas līdzekli līdzekļu pārvaldības darbvietā.

### <a name="turn-auto-firming-for-planning-optimization-on-or-off"></a>Ieslēgt vai izslēgt automātisko apstiprināšanas iestatījumu optimizācijas plānošanai

Automātiskā apstiprināšana ļauj apstiprināt plānotos pasūtījumus kā daļu no vispārējās plānošanas procesa, laika periodā apstiprināšanai. Plānošanas programmā, kas ir veidota Supply Chain Management, vienmēr tiek atbalstīta automātiskā apstiprināšana. Tomēr, lai izmantotu to arī ar plānošanas optimizāciju, ir jāieslēdz līdzeklis.

No Piegādes ķēdes pārvaldības versijas 10.0.21 šī funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldību 10.0.29 šī funkcija ir obligāta, un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.29 versiju, varat ieslēgt vai izslēgt šo funkcionalitāti, [...](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)*dodoties* uz līdzekļu pārvaldību un meklējot automātiskās apstiprināšanas plānošanas optimizācijas līdzeklim.

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
    - **Paralēla apstiprināšana** – [*·*](#enable-features) šī opcija ir pieejama tikai tad, ja jūsu sistēmai ir ieslēgta plānoto pasūtījumu paralēlā apstiprināšana un ja esat atlasījis divus vai vairākus plānotos pasūtījumus apstiprināšanas laikā. Iestatiet to uz *Jā*, lai apstiprināšanas procesus palaistu paralēli. Paralēla apstiprināšana var palīdzēt uzlabot veiktspēju.
    - **Pavedienu skaits –**[*šī* opcija ir pieejama tikai tad,](#enable-features)**ja** jūsu sistēmai ir ieslēgta plānoto pasūtījumu paralēlā apstiprināšana un ja paralēlās *apstiprināšanas opcija ir iestatīta uz Jā.* Ievadiet pavedienu skaitu, ko izmantot apstiprināšanas procesa paralēlošanai. Papildinformāciju par to, kā izmantot šo opciju vispārējā plānošanā, skatiet sadaļā [Vispārējās plānošanas veiktspējas uzlabošanai](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > Lauka **Pavedienu skaits** vērtība *0* (nulle) palielina vispārējās plānošanas izpildes laiku. Tādēļ ieteicams vienmēr iestatīt šo lauku uz vērtību, kas ir lielāka par 0.

    - **Grupēt pēc kreditora** – iestatiet šo opciju kā *Jā*, lai grupētu plānotos pirkšanas pasūtījumus un apstiprināšanas laikā izveidotu vienu pirkšanas pasūtījumu kreditoram. Var arī izveidot vienu pirkšanas pasūtījumu ar vienu rindu katram plānotajam pasūtījumam.
    - **Grupēt pēc pircēja grupas** - iestatiet šo opciju uz *Jā*, lai sagrupētu plānotos pirkšanas pasūtījumus un izveidotu vienu pirkšanas pasūtījumu, kas apvieno kreditoru un pircēju grupu. Lai izmantotu šo opciju, iestatiet opciju **Grupēt pēc kreditora** uz *Jā*.
    - **Grupēt pēc pirkšanas līguma** – iestatiet šo opciju uz *Jā*, lai grupētu plānotos pirkšanas pasūtījumus, kuriem ir tāds pats kreditors kā esošiem pirkšanas līgumiem, un izveidotu vienu pirkšanas pasūtījumu katram pirkšanas līgumam. Ja ir aktivizēta opcija **Grupēt pēc kreditora**, šī opcija tiek aktivizēta automātiski. Lai izmantotu **Grupēt pēc pirkšanas līguma**, **Atrast pirkšanas līgumu** ir jāiestata uz *Jā* lapā **Vispārējās plānošanas parametri**.
    - **Grupēt pēc perioda** (sadaļā **Pirkšanas pasūtījums** ) – atlasiet periodu, pēc kā grupēt plānotos pirkšanas pasūtījumus. Lai izmantotu šo opciju, atlasiet opciju **Grupēt pēc kreditora**.
    - **Grupēt pēc perioda** (sadaļā **Transferi** ) – atlasiet periodu, pēc kā grupēt plānotos transfera pasūtījumus. Pasūtījumi tiks grupēti, pamatojoties uz vērtībām **No noliktavas** un **Uz noliktavu**.

    > [!NOTE]
    > Katra no opcijām "Grupēt pēc" liek sistēmai konvertēt katru plānoto pasūtījumu uz rindu vienā pirkšanas pasūtījumā, kas rodas no grupēšanas.

    ![Dialoglodziņš Parametri dialoglodziņā Apstiprināšana.](./media/manual-firming.png "Dialoglodziņš Parametri dialoglodziņā Apstiprināšana")

1. Kopsavilkuma cilnē **Palaist fonā** iestatiet darbu tā, lai tas darbotos pakešuzdevumu režīmā. Tomēr nav nozīmes iestatīt periodisku grafiku, ja veicat manuālu apstiprināšanas darbu. Lauki darbojas tāpat, kā citi [fona darbu](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management. Tomēr manuālai apstiprināšanai pakešuzdevums apstrādās tikai pašlaik atlasītos plānotos pasūtījumus. Netiks apstrādāts neviens pasūtījums, kas atbilst lapā pašreiz lietotajiem filtriem.
1. Atlasiet **Labi**, lai lietotu iestatījumus un ģenerētu apstiprinātos pasūtījumus.

## <a name="auto-firm-planned-orders"></a>Plānoto pasūtījumu automatiskā apstiprināšana

Automātiskā apstiprināšana ļauj apstiprināt plānotos pasūtījumus kā daļu no vispārējās plānošanas procesa. Var definēt apstiprināšanas periodu vajadzības grupām, atsevišķiem krājumiem un krājumu un vispārējo plānu kombinācijām. Pēc tam vispārējās plānošanas izpildes laikā plānotie pasūtījumi tiks automātiski apstiprināti, ja pasūtījuma datums ir norādītajā apstiprināšanas periodā. Plānotie pasūtījumi, kas tiek ģenerēti, plānojot optimizāciju un novecojušu vispārējās plānošanas programmu, apstrādā pasūtījuma datumu (t.i., sākuma datumu) atšķirīgi.

> [!NOTE]
> Plānoto pirkšanas pasūtījumu automātisko apstiprināšanu var veikt tikai krājumiem, kas saistītie ar kreditoru.
> 
> Atvasinātiem pasūtījumiem (t.i. pakārtotie pirkšanas pasūtījumi), kas ir apstiprināti, būs statuss *Pārskatīšanā*, ja ir ieslēgta gadījuma izmaiņu izsekošana.

> [!IMPORTANT]
> Pirms šajā sadaļā aprakstīto līdzekli var izmantot ar plānošanas optimizāciju, [*·*](#enable-features) jūsu sistēmai ir jābūt ieslēgtai līdzeklim Automātiskās apstiprināšanas optimizācijai saskaņā ar aprakstu šī raksta sākumā. Automātisko apstiprināšanas procesu vienmēr var izmantot ar novecojušu vispārējās plānošanas programmu.

### <a name="auto-firming-with-planning-optimization-vs-the-deprecated-master-planning-engine"></a>Automātiskā apstiprināšana ar plānošanas optimizāciju pret novecojušu vispārējās plānošanas programmu

Plānoto pasūtījumu automātiskai apstiprināšanai var izmantot gan plānošanas optimizāciju, gan novecojušu vispārējās plānošanas programmu. Taču pastāv dažas svarīgas atšķirības. Piemēram, plānošanas optimizācijā tiek izmantots pasūtījuma datums (tas ir, sākuma datums), lai noteiktu, kurus plānotos pasūtījumus apstiprināt, bet novecojusi vispārējās plānošanas programma izmanto pieprasījuma datumu (t.i., beigu datumu). Sekojošajā tabulā ir apkopotas atšķirības.

| Līdzeklis | Plānošanas optimizācija | Novecojusi vispārējās plānošanas programma |
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

Uz vaicājumiem balstīta apstiprināšana ļauj plānot apstiprināšanu, pamatojoties uz iepriekš definētiem kritērijiem. Atšķirībā no automātiskās apstiprināšanas uz vaicājumiem balstīta apstiprināšana ļauj automātiski apstiprināt dažādas pasūtījumu apakškopas dažādos laika punktos. Turklāt, lai apstiprinātu dažādus plānoto pasūtījumu tipus, var izmantot gan manuālas, gan automatizētas operācijas. Varat arī priekšskatīt, kuri apstiprinātie pasūtījumi ir atlasīti, pamatojoties uz jūsu iestatījumiem. Tāpēc varat apstiprināt, ka atlase atbilst jūsu prognozēm.

Automātisko apstiprināšanu var apvienot ar vaicājumu apstiprināšanu. Piemēram, uz vaicājumu balstītam apstiprināšanas darbam ir nākotnes periods, kas ir garāks nekā laika periods atbilstošai automātiskās apstiprināšanas seguma konfigurācijai. Tādēļ uz vaicājumu balstīts apstiprināšanas darbs apstrādās tā plānotos pasūtījumus pirms automātiskās apstiprināšanas aktivizēšanas. Šo darbību var izmantot, lai plānotu pasūtījumus noteiktiem kreditoriem citādi nekā līdzīgu produktu pasūtījumus no citiem kreditoriem.

> [!IMPORTANT]
> Pirms šajā sadaļā aprakstītās funkcijas lietošanas sistēmai [*·*](#enable-features) ir jābūt ieslēgtai plānoto pasūtījumu apstiprināšanas ar filtrēšanas funkciju, kā aprakstīts šī raksta sākumā.

Lai apstiprinātu plānoto pasūtījumu, izmantojot apstiprināšanas procesu, kas balstīts uz vaicājumiem, veiciet šīs darbības.

1. Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Palaist \> Plānoto pasūtījumu apstiprināšana**.
1. Dialoglodziņā **Plānotā pasūtījuma apstiprināšana** kopsavilkuma cilnē **Parametri** iestatiet pamata apstrādes, atzīmēšanas un grupēšanas opcijas. Šīs opcijas darbojas tāpat, kā dialoglodziņā **Apstiprināšana**. (Skatiet iepriekšējo sadaļu aprakstiem.) Pēc tam sadaļā **Plāns** iestatiet šādus laukus, kas ir unikāli dialoglodziņam **Plānotā pasūtījuma apstiprināšana**:

    - **Plāns** – atlasiet vispārējo plānu, kas jālieto plānoto pasūtījumu apstiprināšanas laikā, kas atrodami šajā vaicājumā.
    - **Laika perioda dienas uz priekšu apstiprināšana** - var izvēlēties, cik tālu nākotnē ir jāaprēķina dažādas prasības un citi apsvērumi, izmantojot vispārējo plānošanu.
    - **Laika perioda dienas atpakaļ apstiprināšana** - var izvēlēties, cik tālu pagatnē ir jāaprēķina dažādas prasības un citi apsvērumi, izmantojot vispārējo plānošanu.

    ![Dialoglodziņš Parametri dialoglodziņā Plānoto pasūtījumu apstiprināšana.](./media/planned-order-firming-main-1.png "Dialoglodziņš Parametri dialoglodziņā Plānoto pasūtījumu apstiprināšana")

1. Lai norādītu, kuri ieraksti ir jāiekļauj pasūtījumā, atlasiet pogu **Filtrs** kopsavilkuma cilnē **Iekļaujamie ieraksti**. Tiek atvērts standarta vaicājuma dialoglodziņš, kur varat definēt atlases kritērijus, kārtošanas kritērijus un savienojumus. Lauki darbojas tāpat, kā citi vaicājumu veidi pakalpojumā Supply Chain Management. Lauki šeit ir tikai lasāmi un parāda vērtības, kas saistītas ar jūsu vaicājumu.

    ![Dialoglodziņš Iekļaujamie ieraksti dialoglodziņā Plānoto pasūtījumu apstiprināšana.](./media/planned-order-firming-main-2.png "Dialoglodziņš Iekļaujamie ieraksti dialoglodziņā Plānoto pasūtījumu apstiprināšana")

1. Atlasiet **Priekšskatījums**, lai priekšskatītu jūsu apstiprinātā pasūtījuma saturu, pamatojoties uz līdz šim veiktajiem iestatījumiem. Apstiprināmo plānoto pasūtījumu saraksts tiek parādīts kā ziņojums. Tad ir iespējams pielāgot savus iestatījumus pēc vajadzības, līdz priekšskatījums rāda apstiprināto pasūtījumu pēc jūsu nolūka.

    ![Apstiprinātā pasūtījuma priekšskatījuma piemērs.](./media/planned-order-firming-preview.png "Apstiprinātā pasūtījuma priekšskatījuma piemērs")

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
