---
title: GS1 svītrkodi un QR kodi
description: Šajā tēmā ir aprakstīts, kā iestatīt GS1 svītrkodus un QR kodus, lai etiķetes varētu skenēt noliktavā.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ef28fcaf308225a78bcbac42f591e6b24b21b1b1
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384541"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1 svītrkodi un QR kodi

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Lai reģistrētu krājuma, paletes vai konteinera pārvietošanu, izmantojot mobilās ierīces skeneri, noliktavas darbiniekiem bieži ir jāveic vairāki uzdevumi. Šie uzdevumi var ietvert gan svītrkodu skenēšanu, gan informācijas manuālu ievadi mobilajā ierīcē. Svītrkodiem tiek izmantots uzņēmuma formāts, kuru jūs definējat un pārvaldāt, izmantojot Microsoft Dynamics 365 Supply Chain Management.

GS1 svītrkodu un QR kodu formāti nosūtīšanas etiķetēm tika izstrādāti, lai nodrošinātu globālu standartu datu apmaiņai starp uzņēmumiem. GS1 formāti ne tikai kodē datus, bet arī ļauj izmantot iepriekš definētu *programmas identifikatoru* sarakstu, lai definētu datu nozīmi. GS1 standarts definē datu formātu un dažādus datu veidus, ko var izmantot, lai tos kodētu. Atšķirībā no vecākajiem svītrkodiem GS1 svītrkodiem var būt vairāki datu elementi. Tāpēc, veicot vienu svītrkoda skenēšanu, var iegūt vairāku veidu informāciju par produktu, piemēram, partiju un beigu datumu.

GS1 atbalsts programmatūrā Supply Chain Management ievērojami vienkāršo skenēšanas procesu noliktavās, kur paletes un konteineri tiek apzīmēti, izmantojot kodus GS1 formātā. Noliktavas darbinieki var izgūt visu nepieciešamo informāciju, veicot vienu GS1 svītrkoda skenēšanu. Novēršot nepieciešamību veikt vairākas skenēšanas un/vai manuāli ievadīt informāciju, GS1 svītrkodi palīdz samazināt uzdevumu veikšanai nepieciešamo laiku. Tajā pašā laikā tie arī palīdz uzlabot precizitāti.

Loģistikas pārvaldītājiem ir jāiestata nepieciešamais programmas identifikatoru saraksts un katrs no tiem jāsaista ar atbilstošajiem mobilās ierīces izvēlnes elementiem. Programmas identifikatorus pēc tam var izmantot visās noliktavās kā globālo iestatījumu pārvietošanas un iepakošanas nolūkiem. Tāpēc visām nosūtīšanas etiķetēm būs vienota forma.

Ja vien nav norādīts citādi, termins *svītrkods* šajā tēmā tiek izmantots, lai atsauktos gan uz svītrkodiem, gan uz QR kodiem.

## <a name="turn-on-the-gs1-feature"></a>GS1 līdzekļa iespējošana

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *GS1 svītrkodu skenēšana*

## <a name="set-up-global-gs1-options"></a>GS1 globālo opciju iestatīšana

Lapā **Noliktavas pārvaldības parametri** sniegti vairaki iestatījumi, kas veido globālās GS1 opcijas.

Lai iestatītu globālās GS1 opcijas, rīkojieties tālāk aprakstītajā veidā.

1. Doties uz **Noliktavas vadība \> Iestatīšana \> Noliktavas vadības parametri**.
1. Kopsavilkuma cilnē **Svītrkodi** iestatiet tālāk minētos laukus.

    - **FNC1 rakstzīme** — norādiet rakstzīmes, kas jāinterpretē kā prefikss, kad svītrkods tiek parsēts.
    - **Datu matricas rakstzīme** — norādiet rakstzīmes, kas jāinterpretē kā prefikss, kad datu matrica tiek parsēta.
    - **QR koda rakstzīme** — norādiet rakstzīmes, kas jāinterpretē kā prefikss, kad QR kods tiek parsēts.
    - **Grupu atdalītājs** — norādiet rakstzīmi, kas identificē atsevišķas svītrkoda vai QR koda daļas.
    - **Identifikatora maksimālais garums** — norādiet maksimālo rakstzīmju skaitu, kas atļauts programmas identifikatoram.

> [!NOTE]
> Prefiksi norāda sistēmai, ka svītrkods ir šifrēts saskaņā ar GS1 standartu. Vienlaicīgi un dažādiem nolūkiem var izmantot līdz trim prefiksiem (**FNC1 rakstzīme**, **Datu matricas rakstzīme** un **QR koda rakstzīme**).

## <a name="gs1-application-identifiers"></a>GS1 lietojumprogrammas identifikatori

GS1 formāti ne tikai kodē datus, bet arī ļauj izmantot iepriekš definētu programmas identifikatoru sarakstu, lai definētu datu nozīmi. Loģistikas pārvaldītājiem ir jāiestata nepieciešamais programmas identifikatoru saraksts un katrs no tiem jāsaista ar atbilstošajiem mobilās ierīces izvēlnes elementiem. Identifikatorus pēc tam var izmantot visās noliktavās kā globālo iestatījumu pārvietošanas un iepakošanas nolūkiem. Tāpēc visām nosūtīšanas etiķetēm būs vienota forma.

Sistēma izmanto datus, it īpaši iepriekš definētos programmas identifikatorus, lai izveidotu noteikumus, kas jāpiemēro attiecīgajai skenētās informācijai daļai.

Katrs programmas identifikators norāda sistēmai, ka turpmākās rakstzīmes skenētajā svītrkodā jāuzskata par šifrētas informācijas bloku. Pietieikuma identifikatoru iestatījums nosaka, kā sistēmai būtu jāinterpretē svītrkods un jāsaglabā tas kā vērtība sistēmā.

Loģistikas pārvaldītāji var izmantot standarta starptautiskos programmas identifikatorus un/vai izveidot savus.

### <a name="load-the-standard-application-identifiers"></a>Standarta programmas identifikatoru ielāde

Lai ātri sāktu darbu, varat ielādēt kopējo starptautisko programmas identifikatoru sarakstu. Pēc tam sarakstu pēc nepieciešamības vēlāk var paplašināt vai rediģēt.

Lai ielādētu standarta programmas identifikatorus, veiciet tālāk minētās darbības.

1. Atveriet **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 programmas identifikatori**.
1. Darbību rūtī atlasiet **Izveidot noklusējuma iestatījumus**.

> [!WARNING]
> Ar komandu **Izveidot noklusējuma iestatījumus** tiek dzēsti visi pašlaik definētie programmas identifikatori un tie tiek aizstāti ar standarta sarakstu. Taču pēc noklusējuma iestatījumu ielādes varat pielāgot sarakstu pēc nepieciešamības.

### <a name="set-up-custom-application-identifiers"></a>Pielāgoto programmas identifikatoru iestatīšana

Ja daži vai visi jūsu uzņēmuma izmantotie programmas identifikatori atšķiras no standarta kopas, varat izveidot savus kodus no nulles vai pielāgot standarta kopu pēc nepieciešamības.

Lai iestatītu un pielāgotu savus GS1 programmas identifikatorus, veiciet tālāk minētās darbības.

1. Atveriet **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 programmas identifikatori**.
1. Izpildiet kādu no šīm darbībām:

    - Lai izveidotu jaunu isentifikatoru: darbību rūtī atlasiet **Jauns**.
    - Lai rediģētu esošu identifikatoru: atlasiet identifikatoru un pēc tam darbību rūtī atlasiet **Rediģēt**.

1. Iestatiet jaunajam vai atlasītajam identifikatoram tālāk norādītos laukus.

    - **Programmas identifikators** — ievadiet programmas identifikatora identifikācijas kodu. Parasti šis kods ir divciparu vesels skaitlis, bet tas var būt arī garāks. Decimālskaitļu vērtībām pēdējais cipars norāda decimāldaļu vietu skaitu. Papildinformāciju skatiet tālāk šī saraksta izvēles rūtiņas **Decimāldaļas** aprakstā.
    - **Apraksts** — ievadiet īsu identifikatora aprakstu.
    - **Fiksēts garums** — atlasiet šo izvēles rūtiņu, ja vērtībām, kas tiek skenētas, izmantojot šo programmas identifikatoru, ir fiksēts rakstzīmju skaits. Ja vērtību garums ir mainīgs, notīriet šo izvēles rūtiņu. Šajā gadījumā jānorāda vērtības beigas, izmantojot grupas atdalītāja rakstzīmi, ko norādījāt lapā **Noliktavas pārvaldības parametri**.
    - **Garums** — ievadiet maksimālo rakstzīmju skaitu, kas var tikt parādīts vērtībām, kas tiek skenētas, izmantojot šo programmas identifikatoru. Ja ir atlasīta izvēles rūtiņa **Fiksēts garums**, ir paredzēts tieši šis rakstzīmju skaits.
    - **Veids** — atlasiet to vērtības veidu, kas tiek skenēts, izmantojot šo programmas identifikatoru (*Skaitlisks*, *Burtciparu* vai *Datums*). Datumiem paredzētais formāts ir GGMMDD (bez atstarpēm vai defisēm).
    - **Decimāls** — atlasiet šo izvēles rūtiņu, ja vērtība ietver fiksētu decimālpunktvietu. Ja ir atzīmēta šī rūtiņa, sistēma izmantos programmas identifikatora pēdējo ciparu, lai noteiktu decimāldaļskaitļu skaitu. Piemēram, ja programmas identifikators ir *3205*, vērtības labās puses pieci cipari tiks interpretēti kā aiz decimālpunkta esoši.

> [!NOTE]
> Grupas atdalītājs, kas norādīts lapā **Noliktavas pārvaldības parametri**, nav obligāts, ja vērtībai, kurai seko programmas identifikators, ir fiksēts garums vai ja tās garums ir maksimizēts (t. i., ja garums ir vienāds ar programmas identifikatoram iestatīto vērtību **Garums**).

## <a name="establish-the-generic-gs1-setup"></a>Vispārīgo GS1 iestatījumu izveide

Vispārīgie GS1 iestatījumi izveido kopējo kartējumu kolekciju. Šie kartējumi atbilst katram atbilstošajam mobilās programmas ievades laukam ar programmas identifikatoru, kas nosaka, kā šajā laukā ir jāinterpretē un jāglabā skenēto svītrkodu vērtības. Pēc noklusējuma šie iestatījumi attiecas uz visu mobilās ierīces izvēlnes elementu skenēšanu. Tomēr tos var pārrakstīt vienam vai vairākiem konkrētiem laukiem ar GS1 politiku, kas piešķirta konkrētam izvēlnes elementam.

Vispārīgie GS1 iestatījumi ļauj vienlaikus skenēt tikai vienu vērtību. Tādēļ, ja vēlaties ielādēt vairākas lauku vērtības no vienas skenēšanas, atbilstošajiem izvēlnes elementiem ir jāiestata GS1 politika.

Plašāku informāciju par GS1 politikām skatiet nākamajā sadaļā.

### <a name="load-the-standard-generic-gs1-setup"></a>Standarta vispārīgo GS1 iestatījumu ielāde

Lapā **GS1 vispārīgie iestatījumi** varat ielādēt standarta kartējumu kopu starp mobilās ierīces laukiem un standarta programmas identifikatoriem, kas tiek izveidoti ar noklusējuma iestatījumu.

Lai izveidotu vispārīgus GS1 iestatījumus, atveriet sadaļu **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 vispārīgie iestatījumi**. Pēc tam atlasiet **Izveidot noklusējuma iestatījumus**, lai automātiski piešķirtu piemērotu programmas identifikatoru katram laukam, ko parasti izmanto mobilās ierīces izvēlnes elementi.

> [!WARNING]
> Ja jau pastāv kādi vispārīgi GS1 iestatījumi, komanda **Izveidot noklusējuma iestatījumus** tos pilnībā izdzēš un ielādē standarta iestatījumus.

### <a name="customize-the-standard-generic-gs1-setup"></a>Standarta vispārīgo GS1 iestatījumu pielāgošana

Lai pielāgotu vispārīgos GS1 iestatījumus, veiciet tālāk minētās darbības.

1. Atveriet sadaļu **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 vispārīgi iestatījumi**.
1. Izpildiet kādu no šīm darbībām:

    - Lai izveidotu jaunu kartējumu: darbību rūtī atlasiet **Jauns**.
    - Lai rediģētu esošu kartējumu: atlasiet kartējumu un pēc tam darbību rūtī atlasiet **Rediģēt**.

1. Iestatiet jaunajam vai atlasītajam kartējumam tālāk norādītos laukus.

    - **Lauks** — atlasiet vai ievadiet mobilās programmas ievades lauku, kam jāpiešķir ienākošā vērtība. Vērtība nav parādāmais nosaukums, ko redz darbinieki. Tā vietā tas ir atslēgas nosaukums, kas piešķirts pamatā esošā koda laukam. Noklusējuma iestatījumi nodrošina lauku, kas, iespējams, būs noderīgi, apkopojumu un ietver intuitīvus atslēgas nosaukumus katram laukam un atbilstošu programmētu funkcionalitāti. Tomēr, iespējams, jums būs jārunā ar saviem izstrādes partneriem, lai atrastu pareizo izvēli ieviešanai.
    - **Programmas identifikators** — atlasiet piemērojamo programmas identifikatoru, kā definēts lapā **GS1 programmas identifikatori**. Identifikators nosaka, kā svītrkods tiks interpretēts un saglabāts kā nosauktā lauka vērtība. Pēc programmas identifikatora atlases laukā **Apraksts** ir redzams tā apraksts.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>GS1 politiku, ko var piešķirt mobilās ierīces izvēlnes elementiem, iestatīšana

GS1 standarta mērķis ir ļaut darbiniekiem ielādēt vairākas vērtības, skenējot vienu svītrkodu vienu reizi. Lai sasniegtu šo mērķi, loģistikas vadītājiem ir jāiestata GS1 politikas, kas paziņo sistēmai, kā interpretēt vairāku vērtību svītrkodus. Vēlāk varat piešķirt politikas mobilās ierīces izvēlnes elementiem, lai kontrolētu, kā svītrkods tiek interpretēts, kad darbinieki to skenē, izmantojot noteiktu izvēlnes elementu.

Ja izvēlnes elementam nav piešķirta GS1 politika, sistēma var tvert tikai vienu vērtību. Šī vērtība tiek piemērota mobilās programmas ievadei, kas tiek atlasīta, kad darbinieks veic skenēšanu, kā norādīts vispārīgajos GS1 iestatījumos. Ja izvēlnes elementam ir piešķirta GS1 politika, sistēma joprojām izmanto vispārīgos GS1 iestatījumus, lai kartētu pirmo svītrkoda vērtību uz atlasīto lauku. Tomēr pēc tam tā var tvert papildu lauka vērtības, kā norādīts piemērojamajā politikā.

### <a name="load-the-standard-specific-gs1-policies"></a>Standarta specifisko GS1 politiku ielāde

Lai ātri sāktu darbu, varat ielādēt GS1 politiku kopu. Pēc tam politikas pēc nepieciešamības vēlāk varat paplašināt vai rediģēt.

Lai ielādētu standarta programmas identifikatorus, veiciet tālāk minētās darbības.

1. Dodieties uz sadaļu **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 politika**.
1. Darbību rūtī atlasiet **Izveidot noklusējuma iestatījumus**.

> [!WARNING]
> Ar komandu **Izveidot noklusējuma iestatījumus** tiek dzēstas visas pašlaik definētās politikas un tās tiek aizstātas ar standarta politiku kopu. Taču pēc noklusējuma iestatījumu ielādes varat pielāgot politikas pēc saviem ieskatiem.

### <a name="set-up-custom-specific-gs1-policies"></a>Pielāgotu GS1 politiku iestatīšana

Lai iestatītu un pielāgotu GS1 politikas, izpildiet tālāk norādītās darbības.

1. Dodieties uz sadaļu **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 politika**.
1. Izpildiet kādu no šīm darbībām:

    - Lai izveidotu jaunu politiku: darbību rūtī atlasiet **Jauns**.
    - Lai rediģētu esošu politiku: atlasiet politiku saraksta rūtī.

1. Jaunās vai atlasītās politikas galvenē iestatiet tālāk norādītos laukus.

    - **Politikas nosaukums** — ievadiet politikas nosaukumu.
    - **Apraksts** — ievadiet politikas īsu aprakstu.

1. Kopsavilkuma cilnē zem galvenes kartējiet lauku nosaukumus uz programmas identifikatoriem, kā tas nepieciešams pašreizējai politikai. Izmantojiet pogas rīkjoslā, lai pēc nepieciešamības pievienotu vai noņemtu rindas. Katrā rindā iestatiet tālāk norādītos laukus:

    - **Lauks** — atlasiet vai ievadiet mobilās programmas ievades lauku, kam jāpiešķir ienākošā vērtība. Vērtība nav parādāmais nosaukums, ko redz darbinieki. Tā vietā tas ir atslēgas nosaukums, kas piešķirts pamatā esošā koda laukam. Noklusējuma iestatījumi nodrošina lauku, kas, iespējams, būs noderīgi, apkopojumu un ietver intuitīvus atslēgas nosaukumus katram laukam un atbilstošu programmētu funkcionalitāti. Tomēr, iespējams, jums būs jārunā ar saviem izstrādes partneriem, lai atrastu pareizo izvēli ieviešanai.
    - **Programmas identifikators** — atlasiet piemērojamo programmas identifikatoru, kā definēts lapā **GS1 programmas identifikatori**. Identifikators nosaka, kā svītrkods tiks interpretēts un saglabāts kā nosauktā lauka vērtība. Pēc programmas identifikatora atlases laukā **Apraksts** ir redzams tā apraksts.
    - **Kārtošana** — katrs vairāku vērtību svītrkods ietver programmas identifikatoru sērijas, un katram no tiem seko vērtība. Piemērojamā GS1 politika identificē, kurš programmas identifikators tiek kartēts uz katru datu bāzes lauku. Tomēr, ja svītrkods izmanto vienu un to pašu programmas identifikatoru vairāk nekā vienu reizi, sistēma izmanto secību, kādā programmas identifikatori tiek parādīti kodā, lai tos kartētu uz laukiem. Rindām, kurām ir kopīgs programmas identifikators ar vienu vai vairākām citām rindām, izmantojiet šo lauku, lai izveidotu secību, kādā tiek apstrādātas atbilstošās rindas. Vispirms tiks apstrādāta rinda ar zemāko kārtošanas vērtību.

> [!NOTE]
> Svītrkodiem, kas ietver vairāk nekā vienu identisku programmas identifikatoru, lai izveidotu lauku secību *obligāti* jāizmanto lauks **Kārtošana**.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1 politiku piešķire mobilās ierīces izvēlnes elementiem

Pēc noklusējuma visi mobilās ierīces izvēlnes elementi nodrošina ievades laukus, kur darbinieki var skenēt vienu vērtību atbilstoši vispārīgajiem GS1 iestatījumiem. Ja vēlaties, lai darbinieki varētu skenēt vairākas lauka vērtības vienā skenēšanā jebkuram mobilās ierīces izvēlnes elementam, ir jāpiešķir GS1 politika, veicot tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Izveidojiet vai atveriet izvēlnes elementu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **GS1 politika** uz politiku, kas attiecas uz izvēlnes elementu.

## <a name="gs1-setup-example"></a>GS1 iestatījumu piemērs

Šis piemērs attiecas uz sistēmu, kur GS1 opcijas ir iestatītas tālāk norādītajā veidā.

- Lapā **Noliktavas pārvaldības parametri** ir noteikti tālāk norādītie globālie iestatījumi.

  - **FNC1 rakstzīme:** *\]C1*
  - **Grupu atdalītājs:** *\~*

- Lapā **GS1 programmas identifikatori** uz šo piemēru attiecas tālāk norādītie programmas identifikatori.

    | Pieteikuma identifikators | Apraksts | Fiksētais garums | Ilgums | tips | Decimāldaļskaitlis |
    |---|---|---|---|---|---|
    | 01 | GTIN | Atlasītās | 14. | Skaitlisks | Nodzēsts |
    | 10. | Paketes numurs | Nodzēsts | 20 | Burtciparu | Nodzēsts |
    | 17 | Derīguma beigu datums | Atlasītās | 6 | Datums | Nodzēsts |
    | 30 | Daudzuma saņemšana | Nodzēsts | 8 | Skaitlisks | Nodzēsts |

- Lapā **GS1 vispārīgie iestatījumi** uz šo piemēru attiecas tālāk norādītie vispārīgās GS1 politikas iestatījumi.

    | Lauks | Pieteikuma identifikators | Apraksts |
    |---|---|---|
    | ItemId | 01 | GTIN |

- Lapā **GS1 politika** ir politika, kur lauks **Politikas nosaukums** ir iestatīts uz *Pirkuma saņemšana*. Šajā politikā ir ietvertas tālāk norādītās rindas.

    | Lauks | Pieteikuma identifikators | Apraksts | Kārtošana |
    |---|---|---|---|
    | ExpDate | 17 | Derīguma beigu datums | 0 |
    | InventBatchId | 10. | Paketes numurs | 0 |
    | Daudz. | 30 | Daudzuma saņemšana | 0 |

- Lapā **Mobilās ierīces izvēlnes elementi** ir izvēlnes elements ar nosaukumu *Pirkuma saņemšana*. Tā lauks **GS1 politika** ir iestatīts uz *Pirkuma saņemšana*.

Kad pirkšanas pasūtījuma preces tiek piegādātas noliktavā, darbinieks veic tālāk norādītās darbības.

1. Mibilajā ierīcē atlasiet izvēlnes elementu **Pirkuma saņemšana**.
1. Ievadiet pirkšanas pasūtījuma numuru.
1. Atlasiet lauku **Krājums** un skenējiet šādu svītrkodu: *\]C10100000012345678\~3030\~10b1\~17220215*.

Ņemot vērā šim piemēram izveidotos iestatījumus, sistēma parsē skenēto svītrkodu tālāk aprakstītajā veidā.

| Lauka atslēga | Lietojumprogrammas ID | Vērtība | Piezīme |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Tā kā darbinieks veica skenēšanu uz lauku **Krājums**, pirmā svītrkoda vērtība tiek kartēta uz šo lauku. Kartēšana tiek ņemta no GS1 vispārīgajiem iestatījumiem. |
| Daudz. | 30 | 30 | Tā kā vienā skenēšanā tiek tvertas vairākas lauka vērtības, šis kartējums un visi atlikušie kartējumi tiek ņemti no GS1 politikas, kas piešķirta izvēlnes elementam **Pirkumu saņemšana**. Šī vērtība ir saņemtais daudzums. |
| InventBatchId | 10. | b1 | Šī vērtība ir partijas ID. |
| ExpDate | 17 | 220215 | Datuma formāts ir GGMMDD. Tāpēc termiņa beigu datums ir 2022. gada 15. februāris. |

Pēc tam kvīts tiek reģistrēta, un attiecīgās datu bāzes vērtības tiek ievadītas pēc vienas skenēšanas.
