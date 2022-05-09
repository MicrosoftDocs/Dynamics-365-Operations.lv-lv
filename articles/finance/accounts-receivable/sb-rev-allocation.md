---
title: Ieņēmumu sadalījums
description: Šajā tēmā skaidrots, kā abonementa norēķinos izmantot ieņēmumu sadalījumu.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 2a1bdff364039c6bf0cdfbc11f0979398934c52c
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629709"
---
# <a name="revenue-allocation"></a>Ieņēmumu sadalījums

Šajā tēmā skaidrots, kā iestatīt rēķinu grafika ieņēmumu sadalījuma parametrus. Varat iestatīt vai rediģēt ieņēmumu sadalījumu, veidojot norēķinu grafiku. Kad atverat ieņēmumu **sadalījuma lapu aktīvam** vai pārtrauktam norēķinu grafikam, lauki ir tikai lasāmi.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Norādīt ieņēmumu sadalījumu norēķinu grafikam

Lai norādītu ieņēmumu sadalījumu norēķinu grafikam, sekojiet šiem soļiem.

1. Lapā Visi **/Aktīvie norēķinu grafiki** atlasiet norēķinu grafiku vai norēķinu grafika rindu.
2. **Cilnē Ieņēmumu** sadalījums, kas atrodas lapas augšpusē, atlasiet Ieņēmumu **sadalījums**.
3. Vairāku elementu **izkārtojuma tipa** laukā atlasiet vairāku elementu izkārtojuma tipu (MEA).
4. **Vairāku elementu izkārtojuma numura** laukā norādiet MEA numuru. Pēc tam **laukā Atliktā līguma ieņēmumi** norādiet atliktā līguma ieņēmumu kontu.

    Ja vairāku elementu izkārtojumā tipa lauku iestatāt **uz Viens**,**·** **katrai** rindai tiek lietotas tās pašas vairāku elementu izkārtojuma numurs un atliktā līguma ieņēmumu konta vērtības.**·** Ja vairāku elementu izkārtojuma **tipa lauks** **tiek iestatīts uz Vairāki**, **·** **katrai** rindai varat norādīt dažādas vairāku elementu izkārtojuma numura un atliktā līguma ieņēmumu konta vērtības.
    
    MEA numuru var piešķirt tikai diviem vai vairākiem krājumiem. Vienai rindai nevar būt savs MEA numurs.

5. Atlasiet **Saglabāt**.

### <a name="fields"></a>Lauki

Vairāku **elementu izkārtojumā** ir šādi lauki.

| Lauks | Apraksts |
|---|---| 
| Vairāku elementu izkārtojuma veids | <p>Izvēlieties MEA tipu darbībai:</p><ul><li>**Vairāki** – darbības rindas krājumi ir daļa no MEA vai arī eksistē vairāk nekā viens izkārtojums.</li><li>**Neviens** – darbība ir standarta darbība, kam nav ieņēmumu sadalījuma.</li><li>**Viens** – visi krājumi darbībā ir daļa no viena MEA.</li></ul> |
| Vairāku elementu izkārtojuma numurs | <p>Rindas MEA numurs. Šis lauks ir pieejams, ja vairāku **elementu izkārtojuma tipa lauks** ir iestatīts uz **Vairāki**.</p><p>Ja šis lauks ir tukšs un jūs piešķirat MEA numuru, **·** **·** **savrupas pārdošanas cenas izcelsmes un savrupas pārdošanas cenas lauki tiek automātiski atjaunināti, pamatojoties uz vērtībām no savrupas pārdošanas cenas** lapas. Ir pieejami tikai tie MEA numuri, kas piešķirti citām pārdošanas pasūtījuma rindām.</p> |
| Atliktā līguma ieņēmumu konts | Norādiet kontu, ko izmantot žurnāla ierakstiem, kad izveidots MEA līguma rēķins. Šis lauks ir pieejams tikai tad, ja tiek izmantoti periodiski līguma norēķini. |
| **Līnijas** | |
| Varianta numurs | Pārdošanas pasūtījuma varianta numurs. |
| Krājuma numurs | Krājuma kods no pārdošanas pasūtījuma. |
| Norēķinu biežums | Ieņēmumu sadalījuma biežums: ikdienas **, mēneša** **·**, ceturkšņa **·**, **pusgads** vai **gada.** |
| Daudzums | Pārdošanas pasūtījuma vērtība. |
| Līguma vērtība | Līguma vērtība |
| Vairāku elementu izkārtojuma numurs | <p>Rindas MEA numurs. Šis lauks ir pieejams, ja vairāku **elementu izkārtojuma tipa lauks** ir iestatīts uz **Vairāki**.</p><p>Ja šis lauks ir tukšs un jūs piešķirat MEA numuru, **·** **·** **savrupas pārdošanas cenas izcelsmes un savrupas pārdošanas cenas lauki tiek automātiski atjaunināti, pamatojoties uz vērtībām no savrupas pārdošanas cenas** lapas. Ir pieejami tikai tie MEA numuri, kas piešķirti citām pārdošanas pasūtījuma rindām. Ja šīs vērtības krājumam nav iestatītas, tiek izmantotas lapas Vairāku elementu **ieņēmumu sadalījuma parametri** vērtības.</p> | 
| Atsevišķās pārdošanas cenas izcelsme | <p>Savrupas pārdošanas cenas izcelsme:</p><ul><li>**Summa** – savrupa pārdošanas cena ir jūsu norādīta summa, kas ir lielāka par 0 (nulle). Summa pēc vajadzības tiek konvertēta starp funkcionālajām un izcelsmes valūtām.</li><li>**Pamatpārdošanas** cena – savrupa pārdošanas cena atbilst preces pamatpārdošanas cenai.</li><li>**Rēķina cena** – savrupa pārdošanas cena atbilst krājuma rēķina cenai.</li><li>**Krājuma procenti** – savrupā pārdošanas cena tiek norādīta kā procentuāla vērtība un aprēķināta, pamatojoties uz preces cenu. Ja ir atlasīta šī opcija, norādiet noklusēto procentuālo vērtību.</li><li>**Piešķirt atdalošo** summu – savrupas *pārdošanas* cenas izcelsme tiek aprēķināta kā pamatelementa līguma kopējā vērtība – *kopējā savrupā pakārtoto krājumu pārdošanas cena*:</p><ul><li>*Pamatelementa līguma vērtība ir* neto summa vai rēķinā izrakstītā summa.</li><li>*Kopējā pakārtoto krājumu savrupā pārdošanas* cena ir visu atvasināto krājumu paplašinātās vai līguma savrupās pārdošanas cenas summa, izņemot atvasināto krājumu, kam tiek izmantota šī savrupa pārdošanas cenas izcelsme.</li></ul><p>Ja aprēķinātā summa ir negatīva vērtība, summa tiek iestatīta uz 0 (nulle).</p><p>**Piezīme.** Šo opciju ieņēmumu sadalījušumā var atlasīt tikai vienam pakārtotam krājumam.</p></li><li>**Neviens** – savrupās pārdošanas cenas izcelsme ir balstīta uz pakārtotajiem krājumiem. Šī opcija attiecas uz krājumiem, kas ieņēmumu sadalīšanas veidnē ir definēti kā pamatelementi. **Ja izvēles rūtiņa Ieņēmumu** sadalīšana ir atzīmēta, šī opcija tiek automātiski atzīmēta un iestatījumu nevar mainīt.</li><li>**Rēķina pamatcenas** procenti – savrupas pārdošanas cenas izcelsme ir pamatelementa rēķina cenas procenti. Šī opcija ir pieejama tikai pakārtotajiem krājumiem ieņēmumu sadalīšanas veidnē.</li><li>**Standarta cenas procenti** – savrupas pārdošanas cenas izcelsme ir pamatelementa standarta cenas procenti. Šī opcija ir pieejama tikai pakārtotajiem krājumiem ieņēmumu sadalīšanas veidnē. Ja atvasinātā **krājuma** **·** **·** **opcija tiek mainīta no pamatcenas procentuālās vērtības uz pamatrēķina cenu procentos vai no pamata rēķina cenas procentiem uz pamatcenas procentuālo vērtību**, arī aprēķinātās vērtības tiek atjauninātas.</li></ul> |
| Atsevišķās pārdošanas cena | <p>Savrupā rindas pārdošanas cena darbības valūtā.</p><p>Vērtība laukā Summa **ir** ievadīta vai aprēķināta.</p> |
| Līguma atsevišķā pārdošanas cena | Līguma savrupa pārdošanas cena. |
| Atlikušie līguma ieņēmumi | Līguma atlikušo ieņēmumu summa. Šī summa ir visu to rindu summa, kurām vēl nav izveidoti rēķini. |
| Kopējie līguma ieņēmumi | Rindas līguma ieņēmumu kopsumma. Šī summa ir visu rindu summa neatkarīgi no tā, vai tām ir izveidoti rēķini. |
| Atliktā līguma ieņēmumu konts | <p>Norādiet kontu, ko izmantot žurnāla ierakstiem, kad izveidots MEA līguma rēķins.</p><p>Šis lauks ir pieejams tikai tad, ja tiek izmantoti periodiski līguma norēķini.</p> |
| Kļūda | Jebkādas kļūdas, kas radās ieņēmumu sadalījumā. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Izmantot ieņēmumu sadalījumu pārdošanas pasūtījumam

Lai pārdošanas pasūtījumā izmantotu ieņēmumu sadalījuma funkcionalitāti, sekojiet šiem soļiem.

1. Lapā Visi **pārdošanas pasūtījumi** izveidojiet pārdošanas pasūtījumu ar krājumiem.
2. Cilnes Rēķins **sadaļā** Ieņēmumu **sadalījums** atlasiet **Ieņēmumu sadalījums**.
3. **Vairāku elementu izkārtojuma tipa** laukā atlasiet MEA tipu.
4. **Vairāku elementu izkārtojuma numura** laukā norādiet MEA numuru.
5. Ja vairāku **elementu izkārtojuma tipa** lauks ir iestatīts uz **Vairāki**, atlasiet izvēlētās rindas un pēc tam atlasiet **Lietot atlasītajam**.
6. Atlasiet **Saglabāt**.

Izmantojot ieņēmumu un izdevumu atliktos maksājumus, atlikto maksājumu grafiks tiek izveidots automātiski. Jūs variet to aplūkot visu **atlikto maksājumu grafiku** lapā.
