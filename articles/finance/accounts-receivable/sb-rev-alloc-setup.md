---
title: Iestatīt vairāku elementu ieņēmumu sadalījumu
description: Šajā tēmā ir aprakstīts, kā abonementa norēķinos iestatīt parametrus vairāku elementu ieņēmumu sadalījumam.
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
ms.openlocfilehash: e422b16d1c4505b2837bb282918ecada902b806e
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566566"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Iestatīt vairāku elementu ieņēmumu sadalījumu

Vairāku elementu ieņēmumu sadalījums ļauj iestatīt dažādas veidnes, kas tiek izmantotas, lai aprēķinātu un sadalītu ieņēmumus vairākiem krājumiem. Šī funkcionalitāte var palīdzēt nodrošināt atbilstību grāmatvedības standartu codification tēmai 606 (ASC 606) un/vai 15. starptautiskajam finanšu pārskatu standartam (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Vairāku elementu ieņēmumu sadalījuma parametri

Izmantojiet lapu **Vairāku elementu ieņēmumu sadalījuma parametri**, lai iestatītu parametrus vairāku elementu ieņēmumu sadalījumam.

### <a name="standalone-selling-price-origin"></a>Atsevišķās pārdošanas cenas izcelsme

Savrupas **pārdošanas cenas izcelsmes lauks** nosaka, no kurienes nāk savrupa pārdošanas cena. Varat atjaunināt vērtību krājumu savrupās **pārdošanas cenas lapā** un darbībā. Ir pieejamas tālāk minētās opcijas.

| Opcija | Apraksts |
|--------|-------------|
| Summa | Savrupā pārdošanas cena ir norādīta summa, kas ir lielāka par 0 (nulle). Summa pēc vajadzības tiek konvertēta starp funkcionālajām un izcelsmes valūtām. |
| Pārdošanas pamatcena | Savrupā pārdošanas cena atbilst krājuma pamatpārdošanas cenai. |
| Rēķina cena | Savrupā pārdošanas cena sakrīt ar krājuma rēķina cenu. |
| Krājuma procenti | Savrupā pārdošanas cena tiek norādīta kā procentuālā vērtība un tiek aprēķināta, pamatojoties uz preces cenu. Ja atlasāt šo opciju, norādiet noklusēto procentu likmi. |
| Piešķirt atlikušo summu | <p>Savrupas pārdošanas cenas izcelsme *tiek* aprēķināta kā pamatelementa līguma kopējā vērtība — *kopējā pakārtoto krājumu savrupā pārdošanas cena*:</p><ul><li>*Pamatelementa līguma vērtība ir* neto summa vai rēķinā izrakstītā summa.</li><li>*Kopējā pakārtoto krājumu savrupā pārdošanas* cena ir visu atvasināto krājumu paplašinātās vai līguma savrupās pārdošanas cenas summa, izņemot atvasināto krājumu, kam tiek izmantota šī savrupa pārdošanas cenas izcelsme.</li></ul><p>Ja aprēķinātā summa ir negatīva vērtība, summa tiek iestatīta uz 0 (nulle).</p><p>**Piezīme.** Šo opciju ieņēmumu sadalījušumā var atlasīt tikai vienam pakārtotam krājumam.</p> |
| Nav | Savrupās pārdošanas cenas izcelsme ir balstīta uz pakārtotajiem krājumiem. Šī opcija attiecas uz krājumiem, kas ieņēmumu sadalīšanas veidnē ir definēti kā pamatelementi. **Ja izvēles rūtiņa Ieņēmumu** sadalīšana ir atzīmēta, šī opcija tiek automātiski atzīmēta un iestatījumu nevar mainīt. |
| Procenti no pamatrēķina cenas | Savrupās pārdošanas cenas izcelsme ir pamatelementa rēķina cenas procenti. Noklusēto vērtību var mainīt. Šī opcija ir pieejama tikai pakārtotajiem krājumiem ieņēmumu sadalīšanas veidnē. |
| Procenti no pamata standarta cenas | Savrupās pārdošanas cenas izcelsme ir pamatelementa standarta cenas procenti. Noklusēto vērtību var mainīt. Šī opcija ir pieejama tikai pakārtotajiem krājumiem ieņēmumu sadalīšanas veidnē. Tā ir noklusējuma opcija pakārtotajiem krājumiem. Ja atvasinātā **krājuma** **·** **·** **opcija tiek mainīta no pamatcenas procentuālās vērtības uz pamatrēķina cenu procentos vai no pamata rēķina cenas procentiem uz pamatcenas procentuālo vērtību**, arī aprēķinātās vērtības tiek atjauninātas. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Ņemt vērā ieņēmumu sadalījuma noapaļošanas atšķirības

Konts **ieņēmumu sadalījuma noapaļošanas starpību** laukam norāda kontu, ko izmanto, lai ierakstītu visas noapaļošanas korekcijas līguma ieņēmumu summā. Tas ir pieejams, ja tiek izmantoti periodiski līguma norēķini.

## <a name="item-standalone-selling-price"></a>Krājuma atsevišķās pārdošanas cena

Izmantojiet lapu **Krājuma savrupa pārdošanas cena**, lai norādītu krājuma izcelsmes un savrupu pārdošanas cenu. Šajā lapā norādītās vērtības tiek **izmantotas** kā noklusējuma vērtības lapā Ieņēmumu sadalījums vairākos elementos ieņēmumu sadalījumā un periodiskos līguma rēķinos.

### <a name="specify-item-standalone-selling-price"></a>Norādīt krājuma savrupu pārdošanas cenu

Lai norādītu krājuma savrupu cenu, veiciet šādas darbības.

1. Savrupas **pārdošanas cenas lapas** **savrupas** pārdošanas cenas izcelsmes laukā atlasiet savrupas pārdošanas cenas izcelsmi.
2. Veiciet vienu no tālāk minētajām darbībām atkarībā no vērtības, ko izvēlējāties laukā **Savrupā pārdošanas cenas** izcelsme:

    * Ja atlasījāt **Krājuma procenti**, norādiet procentu **laukā Procentus**.
    * Ja atlasījāt **Summa**, norādiet summu laukā **Savrupā pārdošanas** cena.

2. Katrai precei, ko vēlaties pievienot sarakstam, atlasiet **Pievienot**.
3. Laukā **Krājuma** kods atlasiet krājuma kodu. Laukā **Krājumu** saistība atlasiet krājumu saistību. Krājumiem, kuru izvēles **rūtiņa Ieņēmumu** sadalīšana ir notīrīta, atlasītās krājuma koda un krājumu saistības kombinācijai jābūt unikālai.
4. Ja nepieciešams, **mainiet** **savrupas pārdošanas cenas** izcelsmes, **savrupas pārdošanas** cenas vai procentuālās vērtības lauka noklusējuma vērtību.
5. Katram pamatelementam, ko vēlaties pievienot sarakstam, atlasiet **Pievienot**.
6. Laukā **Krājuma** kods atlasiet krājuma kodu. Laukā **Krājumu** saistība atlasiet krājumu saistību.
7. Atzīmējiet **izvēles rūtiņu Ieņēmumu** sadalīšana.
8. Laukā **Krājumu** saistība atlasiet krājumu saistību. Saraksts tiek atjaunināts ar pamatvienību un visiem pakārtotajiem krājumiem.
9. Pakārtotajam krājumam mainiet savrupas pārdošanas cenas izcelsmes noklusējuma vērtību, **pamatcenas** procentus, **·** **pamatrēķina** cenas procentus vai pēc pieprasīšanas piešķiriet summas lauku.**·**
10. Lai pievienotu vairākus krājumus vienlaicīgi, atlasiet Pievienot **krājumus**.
11. Atjauniniet vaicājumu, lai atlasītu pievienojamo krājumu diapazonu.
12. Atlasiet **Labi**, pārskatiet pievienoto krājumu sarakstu un atlasiet **Labi**.

### <a name="fields"></a>Lauki

Krājuma **savrupā pārdošanas cenas lapā** ir ietverti tālāk norādīti lauki.

| Lauks | Apraksts |
|-------|-------------|
| Atsevišķās pārdošanas cenas izcelsme | <p>Atlasiet savrupas pārdošanas cenas izcelsmi:</p><ul><li>**Summa** – savrupa pārdošanas cena ir jūsu norādīta summa, kas ir lielāka par 0 (nulle). Summa pēc vajadzības tiek konvertēta starp funkcionālajām un izcelsmes valūtām.</li><li>**Pamatpārdošanas** cena – savrupa pārdošanas cena atbilst preces pamatpārdošanas cenai.</li><li>**Rēķina cena** – savrupa pārdošanas cena atbilst krājuma rēķina cenai.</li><li>**Krājuma procenti** – savrupā pārdošanas cena tiek norādīta kā procentuāla vērtība un aprēķināta, pamatojoties uz preces cenu. Ja atlasāt šo opciju, norādiet noklusēto procentu likmi.</li></ul>**Piešķirt atdalošo** summu – savrupas *pārdošanas* cenas izcelsme tiek aprēķināta kā pamatelementa līguma kopējā vērtība – *kopējā savrupā pakārtoto krājumu pārdošanas cena*:</p><ul><li>*Pamatelementa līguma vērtība ir* neto summa vai rēķinā izrakstītā summa.</li><li>*Kopējā pakārtoto krājumu savrupā pārdošanas* cena ir visu atvasināto krājumu paplašinātās vai līguma savrupās pārdošanas cenas summa, izņemot atvasināto krājumu, kam tiek izmantota šī savrupa pārdošanas cenas izcelsme.</li></ul><p>Ja aprēķinātā summa ir negatīva vērtība, summa tiek iestatīta uz 0 (nulle).</p><p>**Piezīme.** Šo opciju ieņēmumu sadalījušumā var atlasīt tikai vienam pakārtotam krājumam.</p></li><li>**Neviens** – savrupās pārdošanas cenas izcelsme ir balstīta uz pakārtotajiem krājumiem. Šī opcija attiecas uz krājumiem, kas ieņēmumu sadalīšanas veidnē ir definēti kā pamatelementi. **Ja izvēles rūtiņa Ieņēmumu** sadalīšana ir atzīmēta, šī opcija tiek automātiski atzīmēta un iestatījumu nevar mainīt.</li><li>**Rēķina pamatcenas** procenti – savrupas pārdošanas cenas izcelsme ir pamatelementa rēķina cenas procenti. Noklusēto vērtību var mainīt. Šī opcija ir pieejama tikai pakārtotajiem krājumiem ieņēmumu sadalīšanas veidnē.</li><li>**Standarta cenas procenti** – savrupas pārdošanas cenas izcelsme ir pamatelementa standarta cenas procenti. Noklusēto vērtību var mainīt. Šī opcija ir pieejama tikai pakārtotajiem krājumiem ieņēmumu sadalīšanas veidnē. Tā ir noklusējuma opcija pakārtotajiem krājumiem. Ja atvasinātā **krājuma** **·** **·** **opcija tiek mainīta no pamatcenas procentuālās vērtības uz pamatrēķina cenu procentos vai no pamata rēķina cenas procentiem uz pamatcenas procentuālo vērtību**, arī aprēķinātās vērtības tiek atjauninātas.</li></ul> |
| Atsevišķās pārdošanas cena | Norādiet krājuma savrupo pārdošanas cenu. Šis lauks ir pieejams, ja savrupas **pārdošanas cenas izcelsmes lauks** ir iestatīts uz **Summa**. |
| Procenti | Norādiet savrupās pārdošanas cenas procentuālo vērtību. Šis lauks ir pieejams, **kad savrupas** **pārdošanas** cenas izcelsmes lauks ir iestatīts uz Preces procenti, **Pamatrēķinā** iekļautās cenas procenti vai **pamatcenas procenti.** |
| Ieņēmumu sadale | <p>Norādīt, vai rindā tiek izmantota ieņēmumu sadalīšana:</p><ul><li>**Atlasīts** – laukā Krājumu saistība var atlasīt tikai tos krājumus, kuriem iestatīta ieņēmumu **sadalīšanas** veidne. Šo izvēles rūtiņu var atzīmēt tikai ieņēmumu sadalīšanas veidnes pamatelementiem.</li><li>**Dzēsts** - krājums ir standarta prece, kas neizmanto ieņēmumu sadalījumu.</li></ul> |
| Saistība | Simbols norāda, vai ieņēmumu sadalījumā krājums ir pamatobjekts vai pakārtotais krājums. |
| Krājuma kods | <p>Atlasiet krājuma kodu: **Tabula** vai **Grupa**.</p><p>Ja izvēles **rūtiņa Ieņēmumu** sadalīšana ir atzīmēta, šis lauks ir iestatīts **uz** Tabula un vērtību nevar mainīt.</p> |
| Krājumu saistība | <p>Atlasiet krājuma kodu.</p><p>Ja izvēles rūtiņa **Ieņēmumu sadalīšana** ir atzīmēta, atlasei ir pieejami tikai krājumi, kas ir pamatelementi, kuriem ir iestatīta ieņēmumu sadalīšanas veidne. Kad pamatelements ir atlasīts, saraksts tiek automātiski atjaunināts ar šī pamatelementa pakārtotajiem krājumiem.</p> |
| Pamatkrājums | Pamatelementam šis lauks rāda krājuma kodu. Pakārtotajiem krājumiem ieņēmumu sadalījumā tas rāda pamatelementa krājuma numuru. |

## <a name="mea-templates"></a>MEA veidnes

**Izmantojiet MEA veidņu lapu**, lai izveidotu un rediģētu vairāku elementu izkārtojumu (MEA) veidņu ID. Šie i tiek izmantoti ieņēmumu sadalījuma **lapā,** lai grupētu krājumus kopā.

### <a name="create-a-template"></a>Izveidot veidni

Lai iestatītu MEA veidni, sekojiet šiem soļiem.

1. **MEA veidņu** lapā atlasiet **Jauns**.
1. Laukā **MEA veidnes ID** ievadiet unikālo ID.
1. Ievadiet aprakstu laukā **Apraksts**.
1. Laukā **Atlikto maksājumu līguma** ieņēmumi atlasiet kontu, ko vēlaties lietot žurnāla ierakstiem, kad tiek izveidots MEA līguma rēķins. Šis lauks ir pieejams, ja periodiskie līguma norēķini ir iespējoti un tiek izmantoti.
1. Atlasiet **Saglabāt**.
