---
title: Laidiena veidnes
description: Šajā tēmā aprakstīts, kā iestatīt kritērijus, kas nosaka, vai kopumi tiek apstrādāti manuāli vai automātiski, un darbam, kas tiek ģenerēts noliktavai, apstrādājot kopumu.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a606f413bf3660a89270c0751b2656fab07cd80d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575996"
---
# <a name="wave-templates"></a>Laidiena veidnes

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā iestatīt kritērijus, kas nosaka, vai kopumi tiek apstrādāti manuāli vai automātiski, un darbam, kas tiek ģenerēts noliktavai, apstrādājot kopumu. Norādiet kritērijus, izveidojot kopuma veidnes un vaicājumus, kas sakrīt ar kopumu izsniegtajām rindām pārdošanas pasūtījumos, ražošanas pasūtījumos un Kanban.

## <a name="settings-for-wave-templates"></a>Kopuma veidņu iestatījumi

Iestatot kopuma veidni, varat norādīt tālāk minēto:

- **Novietojums** un **Noliktava**, kurai veidnei veidos darbu.
- Secība, kādā tiks novērtētas veidnes. Secība, kādā veidnes tiek saskaņotas ar izlaistajām rindām pārdošanas pasūtījumos, ražošanas pasūtījumos un Kanban. Kad rinda ir izlaista, sistēma lieto pirmā kopuma veidni, kuras kritērijiem rinda atbilst. Jo plašāki kritēriji, jo lielāka iespēja, ka līnija atbilst kritērijiem, tāpēc veidnes ar viskonkrētām kritērijiem ir jāievieš saraksta augšgalā. Izmantojiet darbību rūts pogas **Pārvietot uz augšu** un **Pārvietot uz leju**, lai pēc nepieciešamības kārtotu veidnes sarakstā.
- Katras veidnes veiktie pasākumi. Kopuma **Metodes** veic darbības, kuras veido veidne, piemēram, darba izveidi un sadalīšanu katram kopuma veidnes veidam.
- Kopuma atribūti (filtri), kas jālieto kopuma veidnei.

> [!NOTE]
> Ja nepieciešams, izstrādātājs var izveidot papildu metodes. Pilnu metožu sarakstu varat skatīt lapā **Kopuma apstrādes metodes**.

Daži iestatījumi pārstāv stratēģiskus lēmumus kopuma apstrādei, kā aprakstīts tālāk:

- Ja veidne tiek izmantota pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu krājumu piegādei vai krājumu pārvietošanai uz ražošanu, ražošanas pasūtījumiem vai Kanban.
- Ja kopums tiek apstrādāts manuāli vai automātiski, kā aprakstīts tālāk:

  - **Manuālā apstrāde** — rinda tiek pievienota kopumam un krājumi tiek rezervēti, tomēr jums ir jāatlasa **Apstrādāt** uz saraksta lapas **Visi kopumi**, lai pasūtījumam izveidotu izdošanas darbu.
  - **Automātiskā apstrāde** — varat pilnīgi vai daļēji automatizēt kopuma apstrādi. Ja jūs pilnīgi automatizējat kopuma apstrādi, tiek izveidots kopumu, kas ietver rindu no pārdošanas pasūtījuma, ražošanas pasūtījuma vai Kanban, ja ir izveidots pārdošanas pasūtījums, ražošanas pasūtījums vai Kanban. Krājumi tiek atskaitīti no rīcībā esošajiem krājumiem un tiek izveidots izdošanas darbs. Ja jūs daļēji automatizējat kopuma apstrādi, varat norādīt vērtības, kas aktivizēs kopuma apstrādi. Piemēram, varat norādīt maksimālo svaru sūtījumiem, kas aktivizēs kopuma apstrādi, kad kopuma rindu kopējais svars sasniedz šo vērtību.

- Ja piešķirat sūtījumus atvērtam kopumam. Piemēram, ja jūs apsolāt debitoriem, ka līdz 12.00 veiktais pasūtījums tiks nosūtīts 24 stundu laikā, varat iestatīt kopuma veidni, lai automātiski piešķirtu pasūtījuma rindas atvērtam kopums līdz 12.00. Šajā laikā kopums tiek automātiski apstrādāts.

Apstrādājot kopumu, izdošanas darbs, kas tiek izveidots, ir balstīts uz darba veidnes un novietojuma direktīvu, kas ir norādīta noliktavai. Darba veidne norāda, kā tiek izveidots izdošanas darbs, un novietojuma direktīva norāda izdošanas un izvietošanas vietas.

## <a name="create-a-wave-template"></a>Kopuma veidnes izveide

Lai iestatītu kopuma veidni, veiciet tālāk aprakstītās darbības:

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Kopumi** \> **Kopuma veidnes**.
1. Atlasiet **Jauns**, lai izveidotu jaunu kopuma veidni.
1. Laukā **KOpuma veidnes veids** atlasiet vienu no šīm opcijām:

    - *Nosūtīšana* - Izmantojiet kopuma veidni, lai nosūtītu krājumus pārdošanas pasūtījumiem un pārsūtītu pasūtījumus.
    - *Ražošanas pasūtījumi* - Lietojiet kopuma veidni, lai pārvietotu ražošanas pasūtījumu krājumus.
    - *Kanban* - Lietojiet kopuma veidni, lai pārvietotu Kanban pasūtījumu krājumus.

1. **Kopuma veidnes nosaukuma** un **Kopuma veidnes apraksta** laukos ievadiet kopuma veidnes nosaukumu un aprakstu.

    > [!NOTE]
    > Ja noliktavai tiek izveidota vairāk nekā viena veidne, numurs laukā **Kopuma veidņu secība** norāda veidnes pozīciju secībā, kurā veidnes tiek lietotas, ja tās atbilst kritērijiem. Ja nepieciešams, varat atlasīt **Pārvietot uz augšu** vai **Pārvietot uz leju**, lai mainītu veidņu secību.

1. Laukos **Novietojums** un **Noliktava** atlasiet vietu un noliktavu, kam kopuma veidne izveidos kopumus un izdošanas darbu.
1. Ja vēlaties automatizēt kopumu apstrādi, pēc vajadzības veiciet šādus iestatījumus:

    - **Automatizēt kopumu izveidi** - Iestatiet šo opciju uz *Jā*, lai automātiski izveidotu kopumu, kad pārdošanas pasūtījums, ražošanas pasūtījums vai Kanban tiek nodots izpildei noliktavā.
    - **Piešķirt atvērtiem kopumiem** – iestatiet to uz *Jā*, lai automātiski piešķirtu rindas atvērtam kopumam, kad rindas tiek izlaistas. Rindas tiek piešķirtas kopumiem, pamatojoties uz kopuma veidnes vaicājuma filtru.
    - **Kopuma apstrade izlaišanas laikā noliktavā** – iestatiet šo uz *Jā*, lai automātiski apstrādātu kopumu un izveidotu darbu, kad rinda tiek nodota noliktavai.
    - **Kopuma automātiska apstrādes uz sliekšņa** - iestatiet šo opciju uz *Jā*, lai automātiski apstrādātu kopumu, kad tā vērtības sasniedz svara, sūtījuma un lauku grupā **Kopuma robežvērtības** norādīto rindu robežvērtības. Šis iestatījums ir pieejams tikai tad, ja laukā **Kopuma veidnes tips** ir atlasīta opcija *Nosūtīšana*.
    - **Automatizēt kopuma izlaišanu** - iestatiet šo uz *Jā*, lai automātiski atbrīvotu vilni. Izdošanas darbs ir izveidots un pieejams mobilajās ierīcēs.
    - **Automatizēt papildinājuma darbu izlaišanu** - iestatiet šo opciju uz *Jā*, lai izveidotu uz pieprasījuma balstītu papildināšanas darbu un automātiski to izlaistu. Jums ir jāpievieno papildināšanas kopuma metode kopuma veidnei un jāizveido papildināšanas veidne *Kopuma pieprasījuma* tipam. Iestatiet papildināšanas veidni lapā **Papildināšanas veidnes**. Tādēļ nepieciešams, lai jūs kopuma veidnei pievienotu metodi papildināt.
    - **Turpināt kopuma apstrādi, ja neizdodas izveidot darbu** - Ja šī opcija ir iestatīta uz *Jā*, sistēma izmanto tukšu atrašanās vietu, ja tā nevar rezervēt krājumus novietojuma direktīvas piedāvātajā atrašanās vietā (piemēram, tāpēc, ka krājumi vairs nav pieejami). Ja šī opcija ir iestatīta uz *Nē*, kopums neizdosies, ja sistēma nevarēs rezervēt krājumus.

1. Iestatiet **Kopuma sliekšņu** lauku grupu pēc vajadzības:
    - **Kopuma svara slieksnis** — ievadiet maksimālo svaru, ko var saturēt kopums.
    - **Nosūtīšanas slieksnis** – ievadiet maksimālo sūtījumu skaitu, ko var iekļaut kopumā.
    - **Rindas slieksnis** – ievadiet maksimālo rindu skaitu, ko var iekļaut kopumā.

1. Lauku grupā **Noklusējuma vērtības** atlasiet kopuma atribūtus, ko izmantot kā papildu kritērijus kopuma veidnei. Kopuma atribūti ir noderīgi, lai piešķirtu papildu kritērijus, piemēram, konkrētu debitora nosaukumu vai kopuma veidni. Izveidojiet atribūtu tipus lapā **Konteineru atribūti**. 

1. Iestatiet **Kopuma paziņojumu politiku** politikai, kuru vēlaties izmantot paziņojumu ģenerēšanai saistībā ar kopumiem, kas izmanto šo veidni. Kopuma paziņojumu politikas piemēru skatiet [Kopuma izpildes paziņojumos](wave-execution-notifications.md).

1. Kopsavilkuma cilnes **Metodes** rūtī **Atlasītās metodes** tiek uzskaitītas atlasītā kopuma veidnes veida metodes. Kopuma metodes veic darbības, kuras veido veidne, piemēram, darba izveidi un sadalīšanu katram kopuma veidnes veidam. Šīs darbības tiek sauktas arī par kopuma darbībām. Kopuma metodes ir iepriekš definētas katram kopuma veidnes tipam. Iepriekš definētas kopuma metodes nevar noņemt, tomēr jūs varat pārkārtot metožu secību un pievienot papildu metodes. Piemēram, ja veidojat kopuma veidni piegādei, varat pievienot metodes papildināšanai un konteinerizēšanai. Kopuma konteinerizēšanu var pievienot kopuma metožu sērijai, lai definētu kopuma veidnē apstrādāto rindu konteinerizēšanu. Lai pievienotu papildu metodi, izpildiet tālākos norādījumus:

    - Rūtī **Atlikušie projekti** atlasiet kādu metodi un pēc tam atlasiet bultiņas pogu **Pa kreisi**, lai to pievienotu rūtī **Atlasītās metodes**.
    - Lai mainītu secību, atlasiet metodi un pēc tam noklikšķiniet uz bultiņas **Uz augšu** vai **Uz leju**.

    > [!NOTE]
    > Pievienojot metodi, tā automātiski tiek uzskaitīta atbilstošajā atrašanās vietā darbību secībā.

1. Lai iestatītu vaicājumu, kas atbildīs izlaistajām rindām ar atbilstošu kopumu, darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Lai pārbaudītu, vai kopuma veidnes iestatījumi ir derīgi, noklikšķiniet uz **Pārbaudīt veidni**.
