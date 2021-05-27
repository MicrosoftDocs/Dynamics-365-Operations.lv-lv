---
title: Kopējo izmaksu modulis
description: Kopējo izmaksu modulis palīdz uzņēmumiem racionalizēt ienākošās kravas nosūtīšanas darbības, sniedzot lietotājiem pilnīgu finanšu un nepilnu kontroli pār importēto kravu no ražotāja uz noliktavu.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccc6f0100582b9703b9755b50b7e8504aa153d15
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022136"
---
# <a name="landed-cost-module"></a>Kopējo izmaksu modulis

[!include [banner](../../includes/banner.md)]

**Kopējo izmaksu** modulis palīdz uzņēmumiem racionalizēt ienākošās kravas nosūtīšanas darbības, sniedzot lietotājiem pilnīgu finanšu un nepilnu kontroli pār importēto kravu no ražotāja uz noliktavu. Importētajām precēm kopējās izmaksas var būt 40 procenti vai vairāk no katras importētās preces kopējām izmaksām. Tāpēc ir jāsniedz precīzs kopējo izmaksu novērtējums.

Uzņēmumi var izmantot kopējās izmaksas, lai veiktu sekojošos uzdevumus:

- Novērtētās kopējās izmaksas reisa izveides laikā.
- Iedalītās kopējā izmaksas uz vairākiem krājumiem un pirkšanas pasūtījumiem vai pārsūtīšanas pasūtījumiem vienā reisā.
- Atbalstiet preču pārsūtīšanu starp fiziskām atrašanās vietām, atpazīstot kopējās izmaksas.
- Atpazīt uzkrājumus tranzīta precēm.

Kopējās izmaksas nodrošina precīzas un laicīgas pieskaitāmās zemes izmaksu tāmes. Tajā pašā laikā tā nodrošina palielinātu finanšu un elektronisku redzamību paplašinātā piegādes ķēdē. Tas arī palīdz samazināt izmaksu aprēķināšanas un izmaksu aprēķināšanas kļūdu administrēšanu.

## <a name="highlights"></a>Galvenie punkti

### <a name="voyages"></a>Reisi

Kopējās izmaksās reiss ir atšķirīga kustība no nosūtīšanas vietas, izmantojot noteiktu adresātu kopu noteiktā laika posmā uz norādītu saņemšanas noliktavas atrašanās vietu. Pirkšanas pasūtījumus un pasūtījumu rindas var pievienot vienam konteineram vai vairākiem reisa konteineriem, un izmaksas tiks pareizi sadalītas atpakaļ uz krājumu rindu. Pasūtījumus un pasūtījumu rindas var pievienot arī visām juridiskajām personām vienam reisam.

### <a name="item-ownership"></a>Krājuma īpašumtiesības

Sistēmā Microsoft Dynamics 365 Supply Chain Management preces parasti tiek saņemtas noliktavas galamērķī un pēc tam iekļautas rēķinā. Tomēr saskaņā ar vairumu starptautisko tirdzniecības līgumu uzņēmums uzņemsies atbildību par precēm no laika, kad tās atstāj oriģinālo ostu, pirms tās ir fiziski saņemtas. Kopējās izmaksas ļauj uzņēmumiem izrakstīt rēķinu par precēm pirms to fiziskās saņemšanas. Šī koncepcija ir pazīstama kā preces tranzīta pasūtījumā. Tas izveido jaunu pasūtījuma tipu, lai pārvaldītu preču saņemšanu pēc sākotnējā pirkšanas pasūtījuma saņemšanas.

### <a name="costs"></a>Izmaksas

Izveidojot reisu kopējās izmaksās, tam var automātiski pievienot izmaksas. Šīs izmaksas ir iestatītas Kopējās izmaksās un tām ir pieejamas dažādas izmaksu opcijas un izmaksu bāzes. Katras izmaksas var iestatīt dažādiem reisa līmeņiem un sadalīt uz krājuma līmeni, izmantojot sadalījuma noteikumus, kas atbalsta daudzumu, tilpumu, svaru, summu un noteiktus tilpuma dalītājus. Šīs novērtētās izmaksas sniedz precīzu visu reisa izmaksu novērtējumu.

Pēc tam Kopējās izmaksas veic prognozēto kopējo izmaksu iepriekšēju grāmatošanu/uzkrājumu, lai nodrošinātu, ka reisa izveides laikā tiek sniegtas precīzas aprēķinātās izmaksas. Kad šīs automātiskās izmaksas tiek iekļautas rēķinā, novērtētās izmaksas tiek apgrieztas un aizstātas ar faktiskajām izmaksām, pamatojoties uz izmaksu rēķiniem.

Faktiskās izmaksas tiek atgrieztas prognozētās izmaksas, kas tiek grāmatotas izmaksu rēķinu izrakstīšanas laikā, izmantojot klīringa kontus, kas iestatīti katram izmaksu tipam (piemēram, nodoklis, kravas pārvadāšana un apdrošināšana). Šie grāmatojumi seko grāmatošanas uzvedībai, kas saistīta ar noteiktu krājumu. Tie automātiski atjaunina krājumu grāmatošanu, neņemot vērā to, vai grāmatošanas tips ir pirmais in, pirmais ārā (FIFO), pēdējais atrodas, pirmais ārā (LIFO), pārvieto svērto vidējo vai pārvieto vidējo. Visi krājumu modeļu grupu grāmatošanas tipi tiek atbalstīti. Lai pārvietotu vidējo un standarta izmaksu grāmatošanu, pirkšanas cenas novirzes konti ir pieejami, lai grāmatotu atšķirības starp prognozētajām izmaksām un faktiskajām izmaksām.

### <a name="item-and-order-tracking"></a>Krājumu un pasūtījumu izsekošana

Kad reiss pārvietojas no sākotnējās nosūtīšanas vietas uz beigu mērķa noliktavu, lietotāji var pēc vajadzības atjaunināt katru kravu vai *kāju*, vai ceļojumu. Katrai kājai tiek identificēts izpildes laiks un kravas statuss. Tiek identificēti arī apstiprinātie piegādes datumi kustībai uz nākošo ceļojuma daļu. Kopā šie piegādes datumi nodrošina paredzamo preču piegādes datumu saņemšanas noliktavā. Lietotāji var mainīt šos piegādes datumus. Šādā gadījumā preču plānotais piegādes datums pēc tam tiek automātiski atjaunināts, pamatojoties uz ceļojuma izpildes laikiem un sadaļām. Redzamība tranzītā, izmantojot reisu un kuģi, ir pieejama uz konteinera pamata pirms preču saņemšanas. Ņemot vērā to, ka datumi tiek atjaunināti katrā pirkšanas pasūtījuma rindā, uzņēmumiem ir lielāka kontrole pār loģistiku un noliktavas plānošanu.

## <a name="landed-cost-concepts"></a>Kopējo izmaksu koncepcijas

Tabulā ir apkopotas dažas galvenās Kopējo izmaksu koncepcijas.

| Koncepcija | Apraksts |
|---|---|
| Reiss | Parasti reiss ir viens kuģis. Tomēr atkarībā no jūsu prakses un procedūrām, tas var būt viens kreditors vai viens pirkšanas pasūtījums. Nav ierobežojumu šīs koncepcijas izmantošanai. |
| Folio | Folio bieži nosaka muitas noteikumi. Tas var ietvert viena kreditora preces vienam elementam/uzņēmumam vienā sūtījumā. Folio preces var būt vienā konteinerā vai izplatītas starp vairākiem konteineriem. |
| Nosūtīšanas konteiners | Sūtījumu konteineru veikala pirkšanas pasūtījuma rindas. Šo līmeņu līmenis ir zem nosūtīšanas līmeņa. Parasti tās tiek izmantotas, ja preces tiek segtas pa konteineriem vai ja saņemšana ir veikta uz konteineru. |
| Nosūtīšanas konteinera veids | Pārvadāšanas konteinera veidi var noteikt izmaksu tipa cenu (piemēram, kravas pārvadāšana). Tās sniedz arī noderīgu nosūtīšanas informāciju. |
| Izmaksu tips | Izmaksu tipi identificē izmaksas, kas saistītas ar importu, piemēram, nodeva, kravas pārvadāšana un apdrošināšana. |
| Automātiskās izmaksas | Automātiskās izmaksas darbojas kā tirdzniecības līgumi. Automātiskās izmaksas ir saistītas ar reisa līmeni. |
| Osta | Ostas ir apgabali, no kurienes preces tiek saņemtas un no tām pārsūtītas. |
| Kuģis | Kuģis ir līdzeklis, ko izmanto preču transportēšanai, piemēram, kuģis vai lidmašīna. |
| Tranzītpreces | Atkarībā no iestatījumiem preces tiek novietotas tranzīta noliktavā pēc rēķina atjaunināšanas. |
| Aktivitāte | Aktivitātes var izmantot, lai uzglabātu katru nozīmīgu ceļojuma soli starp divām ostām. Tos var izmantot datumu atjaunināšanai. |
| Maršruta veidne | Ceļojuma veidnes ir maršruti, ko preces izmanto starp divām ostām. |

**Kopējo izmaksu** un **Transportēšanas pārvaldības (TMS)** moduļu terminoloģijas un funkciju salīdzināšanai skatiet sadaļu [Kopējās izmaksas pret Transportēšanas pārvaldību](landed-cost-vs-tms.md).
