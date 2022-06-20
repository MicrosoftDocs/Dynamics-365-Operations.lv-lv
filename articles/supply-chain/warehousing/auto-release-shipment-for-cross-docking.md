---
title: Automātisks sūtījums pārkraušanai sadales centrā
description: Šajā rakstā aprakstīta stratēģija pārkraušanai sadales centrā, kas ļauj automātiski izlaist pieprasījuma pasūtījumu nosūtīšanai uz noliktavu, kad ražošanas pasūtījums, kas nodrošina pieprasījuma daudzumu, ir ziņots kā pabeigts, tādējādi daudzums tiek pārvietots tieši no ražošanas izdošanas vietas uz nosūtīšanas vietu.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 34283422bafaeabef9ac454957b60db84eb5a9c7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903787"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Automātisks sūtījums pārkraušanai sadales centrā

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstīta stratēģija pārkraušanai sadales centrā, kas ļauj automātiski izlaist pieprasījuma pasūtījumu nosūtīšanai uz noliktavu, kad ražošanas pasūtījums, kas nodrošina pieprasījuma daudzumu, ir norādīts kā pabeigts. Tādējādi pieprasītā pasūtījuma izpildei nepieciešamais daudzums tiek pārvietots tieši no ražošanas izlaides novietojuma uz nosūtīšanas vietu.

Pārkraušana sadales centrā ir noliktavas apstrādes plūsma, kurā daudzums, kas nepieciešams izejošā pasūtījuma izpildei, tiek novirzīts uz pasūtījuma nosūtīšanas doku vai sagatavošanas zonu no vietas, kur saņemts ienākošais pasūtījums. (Ienākošais pasūtījums var būt pirkšanas pasūtījums, pārsūtīšanas pasūtījums vai ražošanas pasūtījums.) Tā kā uzlabotais pārkraušana sadales centrā līdzeklis atbalsta visus piedāvājuma un pieprasījuma pasūtījumus, un tam ir nepieciešams, lai izejošais pieprasījums tiktu izdots, pirms tiek identificēta pārkraušana sadales centrā iespēja, automātiskā sūtījuma līdzeklim ir tālāk minētās īpašības:

- Tas atbalsta tikai ražošanas pasūtījumus kā piegādi un tikai pārdošanas pasūtījumus un pārsūtīšanas pasūtījumus kā pieprasījumu.
- Pārkraušanas sadales centrā darbību var uzsākt pat tad, ja pieprasījuma pasūtījums nav izdots noliktavai pirms piegādes kvīts reģistrēšanas (proti, pirms ražošana tika norādīta kā pabeigta).

Šai pārkraušanas sadales centrā funkcijai ir divas priekšrocības:

- Noliktavas darbības var izlaist pabeigto preču daudzuma izvietošanu parastajā noliktavas uzglabāšanas zonā, ja šie daudzumi drīzumā atkal atlasīti, lai izpildītu izejošo pasūtījumu. Tā vietā daudzumus var pārvietot vienu reizi no izdošanas novietojuma uz iepakošanas/nosūtīšanas vietu. Šādā veidā funkcionalitāte palīdz minimizēt krājumu apstrādes reižu skaitu un galu galā palīdz maksimāli palielināt laika un vietas ietaupījumu noliktavas ražotnē.
- Noliktavas darbības var atlikt pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu izdošanu noliktavai, līdz pabeigto preču izlaide saistītam ražošanas pasūtījumam tiek norādīta kā pabeigta. Šī priekšrocība varētu būt īpaši svarīga pasūtījuma veikšanas ražošanas vidē, kur ražošanas izpildes laiks parasti ir ilgāks par izpildes laiku preču ražošanas krājumam vidē.

## <a name="prerequisites"></a>Priekšnosacījumi

| Priekšnoteikumi | Apraksts |
|---|---|
| Objekts | Krājumam jābūt iespējotam noliktavas pārvaldības procesiem.<p>**Piezīme:** vienumus, kam iespējots pieļaujamais svars, nevar iekļaut pārkraušanas sadales centrā procesos.</p> |
| Noliktava | Noliktavai jābūt iespējotai noliktavas pārvaldības procesiem. |
| Veidnes pārkraušanai sadales centrā | Attiecīgajai noliktavai ir jābūt iestatītai vismaz vienai pārkraušanas sadales centrā veidnei, kas izmanto **Pēc piegādes kvīts** pieprasījuma apjoma izlaides politiku. |
| Darba klase | **Pārkraušanas sadales centrā** darba pasūtījuma veidam ir jāizveido pārkraušanas sadales centrā darba klases ID. |
| Darbu veidnes | Lai izveidotu pārkraušanas sadales centrā izdošanas un izvietošanas darbu, ir nepieciešamas **Pārkraušanas sadales centrā** darba pasūtījuma veida darba veidnes. |
| Vietas direktīvas | Lai vadītu izvietošanas darbu novietojumus, kuros pārdošanas pasūtījuma daudzumi tiks iepakoti un nosūtīti, ir nepieciešamas **Pārkraušanas sadales centrā** darba pasūtījuma veida novietojuma direktīvas. |
| Iezīmēšana starp pieprasījuma pasūtījumu un ražošanas pasūtījumu | Noliktavas sistēma var izraisīt automātisku izejošā pasūtījuma sūtījuma izlaišanu un izveidot pārkraušanas sadales centrā darbu no izvades novietojuma, veicot darbību, kas norādīta kā pabeigta, tikai tad, ja pārdošanas pasūtījumi un pārsūtīšanas pasūtījumi ir rezervēti un atzīmēti attiecībā pret ražošanas pasūtījumu. |

## <a name="example-cross-docking-flow"></a>Pārkraušanas sadales centrā plūsmas piemērs

Tipisku pārkraušanas sadales centrā plūsmu veido tālāk minētās galvenās darbības.

1. Pārdošanas pasūtījuma pieņēmējs izveido pārdošanas pasūtījumu preces izgatavošanas. Parasti pieprasītais daudzums nav pieejams, un tas vispirms ir jāsaražo.
2. Pārdošanas pasūtījuma ņēmējs izveido ražošanas pasūtījumu tieši no pārdošanas pasūtījuma rindas. Šādā veidā pārdošanas pasūtījuma pieņēmējs rezervē un atzīmē pārdošanas pasūtījuma daudzumu attiecībā pret ražošanas pasūtījuma daudzumu. 

    Vai arī ražošanas plānotājs norāda, ka iezīmēšana ir jāatjaunina, kad plānotie pasūtījumi tiek apstiprināti.

3. Ar ražošanas pasūtījumu tiek veiktas tālāk minētās darbības:

    1. Ražošanas plānotājs novērtē un izdod ražošanas pasūtījumu. (Novērtējums ietver izejmateriālu rezervēšanu, un izlaišana ietver nodošanu noliktavai.)
    2. Noliktavas darbinieks sāk un pabeidz izejmateriālu izdošanu no glabāšanas vietas uz ražošanas ievades vietu atbilstoši ražošanas saņemšanas darbam.
    3. Ražotnes operators sāk ražošanas pasūtījumu.
    4. Pēdējā darbībā iekārtu operators izmanto mobilo ierīci, lai ziņotu par ražošanas pasūtījumu kā pabeigtu.

4. Sistēma izmanto iestatījumus, lai identificētu pārkraušanas sadales centrā notikumu abiem saistītajiem pasūtījumiem un pēc tam izpilda tālāk minētos uzdevumus:

    1. Automātiski izdod saistīto pārdošanas pasūtījumu uz noliktavu, lai izveidotu sūtījumu.
    2. Automātiski izveido pārkraušanas sadales centrā darbu, kam ir instrukcijas izņemt pabeigtās preces no izvades vietas un pārvieto tās uz izejošo novietojumu, ko pārkraušanas sadales centrā vietas direktīvas ir piešķīrušas pārdošanas pasūtījumam.
    3. Palūdziet iekārtas operatoram pabeigt pārkraušanas sadales centrā darbu, tiklīdz tiek ziņots, ka ražošanas pasūtījums ir pabeigts.

5. Pēc tam, kad pārkraušanas sadales centrā darbs ir pabeigts, un daudzumi tiek iekrauti transportlīdzeklī, nosūtīšanas noliktavas plānotājs apstiprina pārdošanas sūtījumu.

## <a name="example-scenario"></a>Piemēra situācija

Šim scenārijam ir jābūt instalētiem demo datiem, un jums ir jāizmanto **USMF** demo datu uzņēmums.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Pārkraušanas sadales centrā, kas izmanto automātiskā sūtījuma līdzekli, iestatīšana

#### <a name="cross-docking-template"></a>Veidne pārkraušanai sadales centrā

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Darbs** \> **Pārkraušanas sadales centrā veidnes**.
2. Atlasiet **Jauns**.
3. Laukā **Secības numurs** ievadiet **1**.
4. Laukā **Pārkraušanas sadales centrā veidnes ID** ievadiet nosaukumu, piemēram, **XDock\_RAF**.
5. Laukā **Pieprasījuma izlaišanas politika** atlasiet **Pēc piegādes kvīts**.
6. Laukā **Noliktava** ievadiet tās noliktavas numuru, kurā vēlaties iestatīt pārkraušanas sadales centrā procesu. Šajā piemērā atlasiet vērtību **51**.

    > [!NOTE]
    > Tiklīdz tiek atlasīta **Pēc piegādes kvīts** kā veidnes pieprasījuma nodošanas politika, visi pārējie lauki lapā vairs nav pieejami. Tāpat nevarat definēt nekādus piegādes avotus. Šī problēma rodas tāpēc, ka pārkraušana sadales centrā, kas izmanto automātiskā sūtījuma līdzekli, atbalsta tikai ražošanas pasūtījumus kā piegādes avotus, un ir nepieciešams, lai starp pārdošanas pasūtījumiem un ražošanas pasūtījumiem tiktu veikta iezīmēšana. Ja kā pieprasījuma izlaišanas politiku atlasāt **Pirms piegādes kvīts**, lauki cilnēs **Plānošana** un **Piegādes avoti** ir pieejami un tos var rediģēt.

#### <a name="work-classes"></a>Darba klases

1. Dodieties uz **Noliktavas vadība** \> **Iestatīšana** \> **Darbs** \> **Darba klases**.
2. Atlasiet **Jauns**.
3. Laukā **Darba klases ID** ievadiet nosaukumu, piemēram, **CrossDock.**
4. Laukā **Darba pasūtījuma veids** atlasiet **Pārkraušana sadales centrā**.

Lai ierobežotu vietu veidus, kuros var novietot bez pārkraušanas sadales centrā pabeigtās preces, varat norādīt vienu vai vairākus derīgus vietas veidus.

#### <a name="work-templates"></a>Darbu veidnes

1. Dodieties uz **Noliktavas vadība** \> **Iestatīšana** \> **Darbs** \> **Darbu veidnes**.
2. Laukā **Darba pasūtījuma veids** atlasiet **Pārkraušana sadales centrā**.
3. Atlasiet **Jauns**.
4. Laukā **Secības numurs** ievadiet **1**.
5. Laukā **Darba veidne** ievadiet nosaukumu, piemēram, **CrossDock\_51**.
6. Atlasiet **Saglabāt**.
7. Sadaļā **Darba veidnes detalizētas informācija** atlasiet **Jauns**.
8. Jaunajai rindai laukā **Darba veids** atlasiet **Izdot**. Laukā **Darba klases ID** atlasiet **CrossDock**.
9. Atlasiet **Jauns**.
10. Jaunajai rindai laukā **Darba veids** atlasiet **Izvietot**. Laukā **Darba klases ID** atlasiet **CrossDock**.

#### <a name="location-directives"></a>Vietas direktīvas

Lai vadītu izdoto ražošanas daudzumu pārvietošanu uz parasto glabāšanas vietu, pabeigto preču standarta izvietošanas procesam ir nepieciešama **Izvietot** novietojuma direktīva. Tāpat ir jāiestata pārkraušanas sadales centrā **Izvietot** novietojuma direktīva, lai uzdotu darbu izvietot pabeigto daudzumu izvietošanai norādītajā nosūtīšanas vietā, kas apkalpo saistītā pārdošanas pasūtījuma sūtījumu.

Lai varētu veikt pārkraušanu sadales centrā, piemēram, regulārai pabeigto preču izvietošanai, nav jāizveido novietojuma direktīva izdošanas darba darbībai, jo izvades vieta ir norādīta. Turklāt ir paredzams, ka šī izvades vieta tiks iestatīta kā noklusējuma izvades novietojums vienā no ar resursiem saistītajiem ierakstiem (tas ir, resursi, resursu grupas saistība vai resursu grupa) vai kā noklusējuma ražošanas pabeigto preču atrašanās vieta noliktavai.

1. Dodieties uz **Noliktavas vadība** \> **Iestatīšana** \> **Novietojuma direktīvas**.
2. Laukā **Darba pasūtījuma veids** atlasiet **Pārkraušana sadales centrā**.
3. Atlasiet **Jauns**.
4. Laukā **Secības numurs** ievadiet **1**.
5. Laukā **Nosaukums** ievadiet nosaukumu, piemēram, **Angāra durvis**.
6. Laukā **Darba veids** atlasiet **Ievietot**.
7. Laukā **Vieta** atlasiet **5**.
8. Laukā **Noliktava** atlasiet **51**.
9. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**.
10. Laukā **Līdz daudzumam** ievadiet maksimālo diapazona daudzumu, piemēram, **1000000**.
11. Atlasiet **Saglabāt**.
12. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**.
13. Laukā **Nosaukums** ievadiet nosaukumu, piemēram, **Angāra durvis**.
14. Atlasiet **Saglabāt**.
15. Varat izmantot standarta vaicājuma iespēju, lai ierobežotu izvietošanas vietas līdz vienai vai vairākām konkrētām vietām. Atlasiet **Rediģēt vaicājumu** un atlasiet **51** kā kritēriju laukam **Noliktava** tabulā **Vietas**.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Pārkraut sadales centrā pabeigtās preces uz nosūtīšanas vietu

Lai pārkrautu pabeigto preču daudzumu uz saistītā pārdošanas pasūtījuma nosūtīšanas vietu, veiciet tālāk minētās darbības.

1. Dodieties uz **Pārdošana un mārketings** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**.
3. Pārdošanas pasūtījuma virsrakstā atlasiet debitora kontu **ASV-001** un noliktavu, kura ir iestatīta pārkraušanai sadales centrā, kas izmanto automātiskā sūtījuma līdzekli.
4. Pievienojiet rindu pabeigtajai precei un kā daudzumu ievadiet **10**.
5. Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Preces un piegādes** \> **Ražošanas pasūtījums**.
6. Dialoglodziņā **Izveidot ražošanas pasūtījumu** pārskatiet noklusējuma vērtības un pēc tam atlasiet **Izveidot**. Tiek izveidots jauns ražošanas pasūtījums, un tas ir saistīts ar pārdošanas pasūtījumu (t.i., tas ir rezervēts un atzīmēts).
7. Nav obligāti: mainiet lauka **Daudzums** vērtību, lai tā būtu lielāka par vērtību, kas nepieciešama, lai izpildītu pārdošanas pasūtījumu. Kad ražošanas daudzums ir reģistrēts kā pabeigts, sistēma izveidos pārkraušanas sadales centrā darbu, kas paredzēts norādītajam daudzumam un izvietošanas darbam atlikušajam daudzumam atbilstoši parastajai procedūrai pabeigto preču izvietošanas apstrādei.

    Kā jau tika minēts iepriekš, starp pārdošanas pasūtījumu un ražošanas pasūtījumu ir jābūt iezīmei. Pretējā gadījumā pārkraušana sadales centrā nedarbosies. Iezīmēšanu var izveidot vairākos veidos, kā norādīts tālāk:

    - Sistēma var automātiski izveidot iezīmēšanu tālāk minētajās situācijās:

        - Ražošanas pasūtījums tiek manuāli izveidots tieši no pārdošanas pasūtījuma rindas (skatīt 6. darbību).
        - Plānotie ražošanas pasūtījumi ir apstiprināti, un lauks **Atjaunināt iezīmēšanu** tiek iestatīts uz **Standarts**.

    - Lietotājs var manuāli izveidot iezīmēšanu, atverot lapu **Iezīmēšana** no pieprasījuma pasūtījuma rindas.

    > [!NOTE]
    > Iezīmēšanu nevar manuāli izveidot vienībām, kas iestatītas standarta un svērtās vidējās vērtības izmantošanai krājumu modeļos.

8. Lapas **Ražošanas pasūtījums** darbību rūtī cilnes **Ražošanas pasūtījums** grupā **Process** atlasiet **Novērtējums** un pēc tam atlasiet **Labi**. Pasūtījums tiek novērtēts, un izejmateriāla daudzums tiek rezervēts ražošanai.
9. Cilnes **Ražošanas pasūtījums** darbību rūtī grupā **Process** atlasiet **Nodot izpildei** un pēc tam atlasiet **Labi**. Izejmateriāliem tiek izveidots noliktavas izdošanas darbs.
10. Atveriet un pārskatiet darbu. Darbību rūtī cilnē **Noliktavas** grupā **Vispārīgi** atlasiet **Detalizēta informācija par darbu**. Pierakstiet darba ID.
11. Pierakstieties Warehouse Management mobile lietotnē, lai palaistu darbu 51. noliktavā.
12. Dodieties uz **Ražošana** \> **Ražošanas izdošana**.
13. Ievadiet darba ID, lai sāktu un pabeigtu izejmateriālu izdošanu. 

    Kad darbs ir norādīts kā pabeigts, izejmateriālu daudzums ir pieejams ražošanas ievades vietā (**005** USMF demo datos), un var sākt ražošanas pasūtījuma izpildi.

14. Lapas **Ražošanas pasūtījums** darbību rūtī cilnes **Ražošanas pasūtījums** grupā **Process** atlasiet **Sākt** un pēc tam atlasiet **Labi**.
15. Programmā atveriet **Ražošana** \> **RAF un izvietošana**.
16. Laukā **Preces ID** ievadiet ražošanas pasūtījuma numuru un citu obligāto informāciju, un pēc tam atlasiet **Labi**.

Ņemiet vērā, ka tiek izpildīti tālāk aprakstītie notikumi:

- Saistītajam pārdošanas pasūtījumam tiek sākta izlaišana uz noliktavu.
- Pamatojoties uz izlaišanu, tiek izveidots nosūtīšanas un pārkraušanas sadales centrā darbs. Šis darbs uzdod noliktavas operatoram izvēlēties daudzumus, kas ir nepieciešami, lai izpildītu pārdošanas pasūtījuma rindu, un izvietot tos nosūtīšanas vietā, kas norādīta pārkraušanas sadales centrā novietojuma direktīvā.
- Ja ražošanas pasūtījuma daudzums ir lielāks par daudzumu, kāds pieprasīts pārdošanas pasūtījumā, tiek izveidots regulārs izvietošanas darbs. Šis darbs uzdod noliktavas operatoram izvēlēties pabeigto preču daudzumu, kas paliek pēc pārkraušanas sadales centrā, un pārvietot to uz parasto uzglabāšanu saskaņā ar novietojuma direktīvu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]