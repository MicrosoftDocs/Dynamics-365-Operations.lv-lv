---
title: Vispārējā plānošana precēm ar ierobežotu glabāšanas laiku
description: Šajā rakstā ir aprakstīts, kā iestatīt un lietot plānošanas līdzekļus, kas ņem vērā iztuļķamo preču glabāšanas laiku.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 68a1ba2bfe90aaf0462917c405d483fa12bf8126
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428226"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Vispārējā plānošana precēm ar ierobežotu glabāšanas laiku

[!include [banner](../../includes/banner.md)]

Glabāšanas laiks ir laiks, kurā preci var uzglabāt, līdz to vairs nevar izmantot vai pārdot. Precēm, kam ir ierobežots glabāšanas laiks, iespējams, tiks izmantota noliktavas stratēģija pirmais derīguma termiņš, pirmais ārā (First-out — FEFO), kam ir prioritāte pār patērētajiem un pārdotajiem krājumiem, pamatojoties uz to atlikušo glabāšanas laiku. Šī noliktavas stratēģija ir būtiska pārtikas, arādiem un citām precēm, kas tiek raksturotas ar īsu glabāšanas laiku. Saskaņā ar FEFO metodi, noliktavas krājumi tiek glabāti kā preces lielveikala plauktā: preces, kam ir ilgs glabāšanas laiks, tiek novietotas plauktos tā, lai preces, kurām ir īsāks atlikušais glabāšanas laiks, tiek nosūtītas vispirms.

## <a name="using-shelf-life-in-master-planning"></a>Glabāšanas laika izmantošana vispārējā plānošanā

Šajā sadaļā skaidrots, kā vispārējā plānošana iesaka piegādi glabāšanas laika krājumiem.

Palaižot vispārējo plānu, tas ģenerē ieteiktos plānotos pasūtījumus (piegādi), kas izpildīs pieprasījumu un arī samazina aizkaves. Ja plāns ietver krājumus, kuriem ir ierobežots glabāšanas laiks, plānošanas aprēķini kļūst sarežģītāki, jo plāns nedrīkst tikai samazināt aizkavi, bet arī izmantot esošo piegādi pirms tā termiņa beigām. Plānam ir jāmēģina izmantot piegādes, kas ir vistuvākais tā beigu datumam pirms piegādes, kas beidzas vēlāk. Tāpēc vispārējā plānošana meklē, lai sasniegtu šādus mērķus šādā secībā:

1. Samaziniet aizkaves summu.
1. Maksimizēt FEFO piegādes summu.
1. Minimizēt krājumu papildināšanu.

Dažos gadījumos var būt konflikts starp pirmajiem diviem mērķiem, un ir jāveic izvēle: vai vēlaties aizkavēt nosūtīšanu vai vēlaties izmantot vēlāk izbeigtu piegādi, nevis piegādi, kas beidzas ātrāk? Lai atrisinātu šo konfliktu vispārējās plānošanas laikā, sistēma nodzēsīs to, ka izvairītos no kavēšanās, izmantojot piegādes, kuru termiņš drīz beigsies. Parasti šis konflikts rodas, ja var būt aizkave un segums pēc perioda. Tāpēc ir ieteicams lietot vajadzības periodu, kas ir īsāks par preces glabāšanas laiku. Citi vajadzību tipi (piemēram, prasības) maz ticami saskarsies ar šo konflikta tipu.

## <a name="set-up-shelf-life"></a>Iestatīt glabāšanas laiku

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Konfigurēt katru vispārējo plānu, lai apsvērtu glabāšanas laiku

Pēc noklusējuma vispārējā plānā nav ņemts vērā glabāšanas laiks. Izmantojiet šo procedūru, lai iespējotu glabāšanas laika aprēķinus katram vispārējaim plānam, kuram tie ir nepieciešami.

1. Dodieties uz **vispārējās plānošanas iestatījumu \> plāniem \> Vispārējās \> plānošanas plāni**.
1. Atlasiet esošu plānu saraksta rūtī vai izveidojiet jaunu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju Izmantot glabāšanas **laika datumus** uz *Jā*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Konfigurēt izsekošanas dimensiju grupas, lai izsekotu partijas dimensiju

Preces glabāšanas laiku var izsekot tikai tad, ja prece tiek izsekota partijas dimensijā. Citiem vārdiem sakot, partijas atsauce un pieprasītie datumi jāievada, saņemot vai ražojot, un caur katru krājuma uzskaites darbību. Lai pārvaldītu šo opciju, iestatiet vienu vai vairākas izsekošanas dimensiju grupas, lai veiciet nepieciešamo izsekošanu, un pēc tam piešķiriet šīm grupām atbilstošās preces pēc vajadzības.

Izmantojiet tālāk norādītās darbības, lai iestatītu izsekošanas dimensiju grupu partijas dimensijas izsekošanai.

1. Pārejiet uz **sadaļu Preču informācijas pārvaldības iestatīšanas \>\> dimensija un variantu grupas Izsekošanas \> dimensiju grupas**.
1. Izpildiet kādu no šīm darbībām:

    - Darbību rūtī atlasiet Jauns, lai **izveidotu** jaunu izsekošanas dimensiju grupu. Ievadiet nosaukumu un aprakstu un pēc tam **darbību** rūtī atlasiet Saglabāt.
    - Saraksta rūtī atlasiet esošo izsekošanas dimensiju grupu, kuru vēlaties iestatīt partijas dimensijas izsekošanai.

1. Kopsavilkuma cilnes **Izsekošanas** dimensija rindā Pakešu **skaits** atzīmējiet izvēles rūtiņas kolonnās Aktīvie **un** **fiziskie** krājumi.

### <a name="set-up-shelf-life-for-a-product"></a>Iestatīt preces glabāšanas laiku

Izmantojiet tālāk norādītās darbības, lai iestatītu preces glabāšanas laiku.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Izveidojiet vai atveriet preci, ko vēlaties iestatīt.
1. Lai izmantotu glabāšanas laika iestatījumus kopsavilkuma cilnē Vispārīgi, **iestatiet** izsekošanas dimensiju grupas lauku izsekošanas dimensiju grupai, **kas** ir iestatīta partijas dimensijas izsekošanai. Šo lauku var iestatīt tikai preces izveides laikā. Vērtību esošajiem produktiem nevar mainīt.
1. Kopsavilkuma cilnē **Pārvaldīt krājumus** iestatiet šādus laukus:

    - **Glabāšanas laika periods dienās** – norādiet periodu (dienās), ar kuru pārbaudīt šīs preces partiju, lai nodrošinātu, ka tā ir piemērota patēriņam vai tālākpārdošanai. Šī lauka vērtība tiek pievienota partijas ražošanas datumam, *lai noteiktu* tās glabāšanas laika *informācijas datumu*. Varat konfigurēt sistēmu, lai ģenerētu kvalitātes pasūtījumus, kad pakete sasniedz tās glabāšanas laika pārbaudes datumu.
    - **Glabāšanas laika periods dienās** – norādiet dienu skaitu pirms šīs preces paketes derīguma beigām. Šī vērtība tiek pievienota ražošanas *datumam,* lai noteiktu beigu *datumu*. Pēc šī datuma partija tiek uzskatīta par nepieejamu.
    - **Derīguma termiņa periods dienās** – norādiet periodu (dienās), pēc kura šī produkta pakete joprojām ir pārdodama, bet vairs nevar saglabāt dažus no tās oriģinālajiem rekvizītiem. Šī vērtība tiek pievienota ražošanas *datumam,* lai noteiktu *derīguma termiņa datumu*. Varat palaist pārskatus, lai identificētu krājumus, kas ir pagājusi pēc derīguma termiņa datuma. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Iestatīt pārdošanas dienu kārtulu katram debitoram

*Pārdošanas dienu funkcionalitāte* nodrošina, ka preces no paketes, kuras derīguma termiņš drīz beigsies, netiks nosūtītas debitoriem. Iestatot tā nodrošina, ka tad, kad preces tiek sūtītas debitoram, atbilstošais pārdošanas dienu skaits joprojām paliks pēc piegādes.

Lai izmantotu pārdošanas dienu funkcionalitāti, jānorāda pārdošanas dienu skaits, kas tiek piemērots katrai precei (vai preču grupai) katram debitoram. Šis process ir manuāli jāpabeidz, jo tam nav datu elementa.

Izmantojiet šo procedūru, lai iestatītu pārdošanas dienas katrai precei katram debitoram.

1. Dodieties uz **Pārdošana un mārketings \> Debitori \> Visi debitori**.
1. Atrodiet un atlasiet debitoru, ko vēlaties iestatīt.
1. Darbību rūts cilnē **Pārdošana**, kas atrodas iestatītajā **grupā**, atlasiet Pārdošanas **\> pārdošanas dienas**.
1. Debitora lapā **Pārdošanas dienas režģī tiek** uzskaitīti esošās pārdošanas dienu kārtulas katrai precei vai preču grupai. Izmantojiet pogas Darbību rūtī, lai pievienotu vai rediģētu rindas režģī pēc vajadzības. Filtrs **tiek** nodrošināts, lai palīdzētu atrast esošās rindas.
1. Katrā rindā iestatiet tālāk norādītos laukus:

    - **Krājuma kods** — atlasiet vienu no šīm vērtībām, lai norādītu ietekmēto krājumu diapazonu:

        - *Tabula* – rinda attiecas uz noteiktu krājumu.
        - *Grupa* – rinda attiecas uz noteiktu krājumu grupu.
        - *visi* – rinda attiecas uz visiem krājumiem.

    - **Krājumu saistība** – Ja krājuma koda **lauku iestatāt** uz *Tabula*, atlasiet noteiktu krājumu. Ja krājuma koda **lauku iestatāt** uz *Grupēt*, atlasiet krājumu grupu. Iestatot lauku Krājuma **kods** uz *Visi*, šis lauks nav pieejams.
    - **Pārdošanas dienas —** ievadiet minimālo dienu skaitu, kas debitoram ir jāpārdod atbilstošas preces pirms paketes termiņa beigām. Pārdošanas dienu vērtība tiek pamatota uz pieprasīto saņemšanas datumu (vai apstiprināto saņemšanas datumu, ja tas ir definēts) atbilstošām precēm pārdošanas pasūtījumā.
    - *(Citas preces dimensijas)* – lai ierobežotu rindas darbības jomu, pēc vajadzības norādiet citas dimensijas vērtības (**·** **piemēram**, Izmērs un Krāsa). Lai kontrolētu, kuras dimensijas tiek parādītas režģī, darbību **rūtī atlasiet** Rādīt dimensijas.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Iestatīt visas atbilstošās preces tā, lai tās būtu kontrolētas FEFO datumā

Lai varētu strādāt pārdošanas dienas, katram atbilstošajam krājumam jāpieder pie **krājumu modeļu grupas, kurā atzīmēta FEFO izvēles rūtiņa**, kas tiek kontrolēta ar datumu.

Izmantojiet šo procedūru, lai iestatītu krājuma modeļa grupu tā, lai tā atbalsta pārdošanas dienu funkcionalitāti.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Krājumi \> Krājumu modeļu grupas**.
1. Atlasiet eksistējošu grupu saraksta rūtī vai izveidojiet jaunu, darbību **rūtī** atlasot Jauns.
1. Kopsavilkuma cilnē **Krājumu politika** atzīmējiet izvēles rūtiņu **FEFO, kas tiek kontrolēta** ar datumu.
1. Iestatiet grupai citus laukus pēc vajadzības.

Izmantojiet šo procedūru, lai skatītu vai iestatītu krājumu modeļa grupu, kurai pieder prece.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atveriet preci, kuru vēlaties pārbaudīt vai labot.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet krājumu modeļu grupas **lauku** uz grupu **, kurā ir atzīmēta FEFO izvēles rūtiņa, kas** tiek kontrolēta ar datumu.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>1. piemērs: vienkāršs FEFO, 10 dienu periods, izpildes laika dienu nulle

Šajā piemērā parādīts glabāšanas laika pamat piemērs, kur piesaiste starp piegādes pasūtījumiem un pieprasījumu tiek veikta, lai sasniegtu šādus sistēmas mērķus:

- Samaziniet aizkaves summu.
- Maksimizēt FEFO piegādes summu.
- Minimizēt krājumu papildināšanu.

Sistēmai ir šādi krājumu un vispārējā plāna iestatījumi:

- **Vajadzības kods (papildināšanas stratēģija):** periods 
- **Vajadzības periods:** 10 dienas (vienādas ar glabāšanas laiku)
- **Glabāšanas laiks:** 10 dienas
- **Pārdošanas dienas:** 0 dienas
- **Izpildes laiks:** 0 dienas
- **Negatīvās dienas:** 0 dienas
- **Plānotā pasūtījuma tips (krājuma noklusējuma pasūtījuma iestatījumi): pirkšanas** pasūtījums

Sistēmā ir šādi krājuma pārdošanas pasūtījumi:

- **SO1:** daudzums (daudzums) = 2, pieprasītais piegādes datums = šodien + 1 diena
- **SO2:** daudzums = 1, pieprasītais piegādes datums = šodien + 4 dienas
- **SO3: daudzums** = 1, pieprasītais piegādes datums = šodien + 5 dienas

Visi šie pārdošanas pasūtījumi veido krājuma pieprasījumu.

Krājumam pastāv šādas piegādes:

- **Rīcībā esošie krājumi: daudzums** = 1, beigu datums = šodien + 5 dienas
- **1. pirkšanas pasūtījums (PO1):** saņemšanas datums = šodiena + 2 dienas, daudzums = 1, beigu datums = šodiena + 4 dienas

Sistēma izveido piegādes sarakstu, kas var segt šo pieprasījumu, un tā šķiro sarakstu pēc beigu datuma (izmantojot FEFO).

Vispārējā plānošana izveido nepieciešamo piesaisti starp piedāvājumu un pieprasījumu. Tas arī izveido jebkādu nepieciešamo pieprasījumu, pamatojoties uz piegādes sarakstu (izmantojot FEFO) un ņemot vērā pieejamības datumu.

- SO1 var tikt izpildīts ar rīcībā esošo daudzumu, bet to nevar izpildīt PO1, jo PO1 pieejamības datums ir vienu dienu vēlāks nekā TO pieprasa SO1. Tādējādi SO1 ģenerē pieprasījumu vienai preču vienībai.
- SO2 var segt ar PO1, jo PO1 saņems pieprasīto laiku, un beigu datums joprojām būs derīgs. Tāpēc SO2 prasība ir pilnībā nosegta ar PO1.
- SO3 nav iekļauts, jo resursi nav pieejami. Tādējādi SO3 ģenerē pieprasījumu vienai preču vienībai.

Lai nosegtu visas atlikušās prasības, sistēmai jāizveido šāds plānotais pirkšanas pasūtījums:

- **PPO1: saņemšanas** datums = šodiena, daudzums = 2, beigu datums = šodiena + 10 dienas

Tabulā ir apkopots rezultāts.

| Pieprasījums | Piesaiste |
|---|---|
| **SO1:** piegādes datums = šodiena + 1 diena, daudzums = 2 | <p>**Rīcībā esošie krājumi: daudzums** = 1, beigu datums = šodiena + 5 dienas</p><p>**PPO1: saņemšanas** datums = šodiena, daudzums = 1, beigu datums = šodiena + 10 dienas</p> |
| **SO2:** piegādes datums = šodiena + 4 dienas, daudzums = 1 | **PO1:** Saņemšanas datums = šodiena + 2 dienas, 1 daudzums, beigu datums = šodiena + 4 dienas |
| **SO3:** piegādes datums = šodiena + 5 dienas, daudzums = 1 | **PPO1: saņemšanas** datums = šodiena, daudzums = 2, beigu datums = šodiena + 10 dienas |

Šajā ilustrācijā parādīta šī piemēra laika skala.

![1. piemērs: vienkāršs FEFO, 10 dienu periods, izpildes laika dienu nulle.](media/fefo-example-1.png "1. piemērs: vienkāršs FEFO, 10 dienu periods, izpildes laika dienu nulle")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>2. piemērs: vienkāršs FEFO, prasība, trīs izpildes laika dienas

Šajā piemērā parādīts, kā sistēmas mēģinājums samazināt kavējumus reizēm var izraisīt pārs pasūtījumu rašanās.

Sistēmai ir šādi krājumu un vispārējā plāna iestatījumi:

- **Vajadzības kods (papildināšanas stratēģija):** prasība
- **Glabāšanas laiks:** 10 dienas
- **Pārdošanas dienas:** 0 dienas
- **Izpildes laiks:** Izveidots pēc šādiem kreditora tirdzniecības līgumiem:

    - **1. tirdzniecības līgums:** ja daudzums = 1, izpildes laiks = 4
    - **2. tirdzniecības līgums:** ja daudzums = 2, izpildes laiks = 3

- **Negatīvās dienas:** 0 dienas
- **Plānotā pasūtījuma tips (krājuma noklusējuma pasūtījuma iestatījumi): pirkšanas** pasūtījums

Sistēmā ir šāds pārdošanas pasūtījums:

- **SO1: daudzums** = 2, pieprasītais piegādes datums = šodien + 3 dienas

Šo pieprasījumu sedz esošais piedāvājums un apstiprinātais pirkšanas pasūtījums:

- **Rīcībā esošie krājumi: pieejami** = šodiena, daudzums = 1, beigu datums = šodiena + 2 dienas
- **PO1:** Saņemšanas datums = šodiena + 3 dienas, daudzums = 1, beigu datums = šodiena + 4 dienas

SO1 nevar izpildīt ar rīcībā esošiem krājumiem, jo krājumu beigu datums ir pirms nosūtīšanas datuma. PO1 var segt SO1 prasību ar daudzumu tikai 1. Tādējādi SO1 ģenerē pieprasījumu vienai preču vienībai. Lai nosegtu šo pieprasījumu, sistēma izveido plānoto pirkšanas pasūtījumu (PPO1).

Sistēmai ir divi tirdzniecības līgumi (viens daudzumam = 1, izpildes laiks = 4 dienas, un viens daudzumam = 2, izpildes laiks = 3 dienas). Tāpēc sistēma mēģina minimizēt aizkavēšanos, izveidojot plānotu pirkšanas pasūtījumu (PPO1), kas atbilst otrajam tirdzniecības līgumam. Rezultāts ir pārāk liela informācija (daudzums = 2, beigu datums = šodiena + 10 dienas).

Tabulā ir apkopots rezultāts.

| Pieprasījums | Piesaiste |
|---|---|
| **SO1:** piegādes datums = šodiena + 3 dienas, daudzums = 2 | <p>**PO1:** Saņemšanas datums = šodiena + 3 dienas, daudzums = 1, beigu datums = šodiena + 4 dienas</p><p>**PPO1: saņemšanas** datums = šodiena + 3 dienas, daudzums = 1, beigu datums = šodiena + 10 dienas</p> |

Šajā ilustrācijā parādīta šī piemēra laika skala.

![2. piemērs: vienkāršs FEFO, prasība, trīs izpildes laika dienas.](media/fefo-example-2.png "2. piemērs: vienkāršs FEFO, prasība, trīs izpildes laika dienas")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>3. piemērs: vienkāršs FEFO, prasība, trīs izpildes laika dienas, 5 pārdošanas dienas

Šajā piemērā ir parādīts, kā glabāšanas laiks darbojas, kad krājumam tiek pievienotas pārdošanas dienas.

Sistēmai ir šādi krājumu un vispārējā plāna iestatījumi:

- **Vajadzības kods (papildināšanas stratēģija):** prasība
- **Glabāšanas laiks:** 10 dienas
- **Pārdošanas dienas:** 5 dienas
- **Izpildes laiks:** 5 dienas
- **Negatīvās dienas:** 0 dienas
- **Plānotā pasūtījuma tips (krājuma noklusējuma pasūtījuma iestatījumi): pirkšanas** pasūtījums

Sistēmā ir šādi pārdošanas pasūtījumi:

- **SO1: daudzums** = 2, pieprasītais piegādes datums = šodien + 2 dienas
- **SO2:** daudzums = 1, pieprasītais piegādes datums = šodien + 3 dienas
- **SO3: daudzums** = 1, pieprasītais piegādes datums = šodien + 5 dienas

Šo pieprasījumu var segt ar pastāvošu piedāvājumu un apstiprinātu pirkšanas pasūtījumu:

- **Rīcībā esošie krājumi: pieejami** = šodiena, daudzums = 1, beigu datums = šodiena + 6 dienas
- **PO1:** Saņemšanas datums = šodiena + 2 dienas, daudzums = 3, beigu datums = šodiena + 10 dienas

Sistēma izveido piesaistes kandidātu sarakstu, pamatojoties uz piegādes (FEFO) sarakstu un pieejamības datumiem. Tāpēc so1 nevar izpildīt, izmantojot rīcībā esošos krājumus, jo šis krājums beidzas pirms pārdošanas dienu beigām, kuras pieprasa debitors (pieprasītais saņemšanas datums + 5 dienas). PP1 var segt SO1 prasību ar divām vienībām un SO2 prasību ar vienu vienību. Tāpēc tikai SO3 joprojām ir nenosegts vienas preču vienības pieprasījums. Lai nosegtu šo pieprasījumu, sistēma izveido sekojošo plānoto pirkšanas pasūtījumu:

- **PP01: saņemšanas** datums = šodiena + 5 dienas, daudzums = 1, beigu datums = šodiena + 10 dienas

Tabulā ir apkopots rezultāts.

| Pieprasījums | Piesaiste |
|---|---|
| **SO1:** piegādes datums = šodiena + 2 dienas, daudzums = 2 | **PO1:** Saņemšanas datums = šodiena + 2 dienas, daudzums = 2, beigu datums = šodiena + 10 dienas |
| **SO2:** piegādes datums = šodiena + 3 dienas, daudzums = 1 | **PO1:** Saņemšanas datums = šodiena + 2 dienas, daudzums = 1, beigu datums = šodiena + 10 dienas |
| **SO3:** piegādes datums = šodiena + 5 dienas, daudzums = 1 | **PPO1: saņemšanas** datums = šodiena + 5 dienas, daudzums = 1, beigu datums = šodiena + 10 dienas |

Šajā ilustrācijā parādīta šī piemēra laika skala.

![3. piemērs: vienkāršs FEFO, prasība, trīs izpildes laika dienas, 5 pārdošanas dienas.](media/fefo-example-3.png "3. piemērs: vienkāršs FEFO, prasība, trīs izpildes laika dienas, 5 pārdošanas dienas")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>4. piemērs: vienkāršs FEFO, periods, izpildes laiks ir atkarīgs no daudzuma

Šajā piemērā parādīts, kā sistēmas mēģinājums samazināt kavējumus reizēm var izraisīt pārs pasūtījumu rašanās.

Sistēmai ir šādi krājumu un vispārējā plāna iestatījumi:

- **Vajadzības kods (papildināšanas stratēģija):** periods
- **Vajadzības periods:** 10 dienas (vienādas ar glabāšanas laiku)
- **Glabāšanas laiks:** 10 dienas
- **Pārdošanas dienas:** 0 dienas
- **Izpildes laiks:** Izveidots pēc šādiem kreditora tirdzniecības līgumiem:

    - **1. tirdzniecības līgums:** ja daudzums = 1, izpildes laiks = 5
    - **2. tirdzniecības līgums:** ja daudzums = 2, izpildes laiks = 0

- **Negatīvās dienas:** 0 dienas
- **Plānotā pasūtījuma tips (krājuma noklusējuma pasūtījuma iestatījumi): pirkšanas** pasūtījums

Sistēmā ir šādi pārdošanas pasūtījumi:

- **SO1: daudzums** = 1, pieprasītais piegādes datums = šodien
- **SO2:** daudzums = 1, pieprasītais piegādes datums = šodien + 6 dienas

Šo pieprasījumu var daļēji segt esošā piegāde no šādiem apstiprinātajiem pirkšanas pasūtījumiem:

- **PO1:** Saņemšanas datums = šodiena + 1 dienas, daudzums = 1, beigu datums = šodiena + 2 dienas
- **PO2:** saņemšanas datums = šodiena + 3 dienas, daudzums = 1, beigu datums = šodiena + 7 dienas

Sistēmai ir divi tirdzniecības līgumi (viens daudzumam = 1, izpildes laiks = 5 dienas, un viens daudzumam = 2, izpildes laiks = 0 dienas). Tāpēc sistēma mēģina minimizēt aizkavēšanos, izveidojot šādu plānoto pirkšanas pasūtījumu, kas atbilst otrajam tirdzniecības līgumam:

- **PP01: saņemšanas** datums = šodiena, daudzums = 2, beigu datums = šodiena + 10 dienas

SO1 tiks segta ar vienu vienību no PPO1. SO2 tiks segti ar PO2, jo PO2 termiņš beidzas ātrāk nekā PPO1.

Tabulā ir apkopots rezultāts.

| Pieprasījums | Piesaiste |
|---|---|
| **SO1:** piegādes datums = šodiena, daudzums = 1 | **PPO1: saņemšanas** datums = šodiena, daudzums = 1, beigu datums = šodiena + 10 dienas |
| **SO2:** piegādes datums = šodiena + 6 dienas, daudzums = 1 | **PO2:** saņemšanas datums = šodiena + 3 dienas, daudzums = 1, beigu datums = šodiena + 7 dienas |

> [!NOTE]
> PP1 netiek izmantots, jo tiks nokavēts datums S01 un beigsies derīgums pirms S02 piegādes. Par PPO1 ir pārspīlēja viena vienība, lai iespējotu izpildes laiku līdz 0 (nulle) katram 2. tirdzniecības līgumam.

Šajā ilustrācijā parādīta šī piemēra laika skala.

![4. piemērs: vienkāršs FEFO, periods, izpildes laiks ir atkarīgs no daudzuma.](media/fefo-example-4.png "4. piemērs: vienkāršs FEFO, periods, izpildes laiks ir atkarīgs no daudzuma")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>5. piemērs: vienkārša FEFO, prasība, 10 negatīvas dienas

Šajā piemērā parādīts, kā glabāšanas laiks darbojas, ja krājumam tiek pievienots liels skaits negatīvu dienu. Negatīvas dienas ir dienu skaits, ko vēlaties gaidīt, pirms pasūtīt krājuma papildināšanu, kurā ir negatīvi krājumi. Sistēma neveidojiet piegādi, ja vien nav pārsniegts negatīvo dienu skaits.

Sistēmai ir šādi krājumu un vispārējā plāna iestatījumi:

- **Vajadzības kods (papildināšanas stratēģija):** prasība
- **Izpildes laiks:** 0 dienas
- **Negatīvās dienas:** 10 dienas
- **Plānotā pasūtījuma tips (krājuma noklusējuma pasūtījuma iestatījumi): pirkšanas** pasūtījums

Sistēmā ir šāds pārdošanas pasūtījums:

- **SO1: daudzums** = 1, pieprasītais piegādes datums = šodien

Šo pieprasījumu var segt ar pastāvošu piegādi no šāda apstiprināta pirkšanas pasūtījuma:

- **PO1:** Saņemšanas datums = šodiena + 3 dienas, daudzums = 1, beigu datums = šodiena + 5 dienas

Tā kā sistēma ir konfigurēta atļaut 10 negatīvas dienas, tā sedz SO1 pieprasījumu, izmantojot PO1, kaut arī rezultāts būs trīs dienu aizkave, jo SO1 izveido negatīvu krājumu, līdz tiek saņemts PO1. Plānotais pirkšanas pasūtījums netiek izveidots, kaut arī izpildes laiks ir 0 (nulle) un plānotā pirkšanas pasūtījuma izveide samazinās kavēšanās.

Tabulā ir apkopots rezultāts.

| Pieprasījums | Piesaiste |
|---|---|
| **SO1:** piegādes datums = šodiena, daudzums = 1 | **PO1:** Saņemšanas datums = šodiena + 3 dienas, daudzums = 1, beigu datums = šodiena + 5 dienas |

Šajā ilustrācijā parādīta šī piemēra laika skala.

![5. piemērs: vienkārša FEFO, prasība, 10 negatīvas dienas.](media/fefo-example-5.png "5. piemērs: vienkārša FEFO, prasība, 10 negatīvas dienas")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>6. piemērs: vienkārša FEFO, prasība, piecas negatīvas dienas

Šajā piemērā parādīts, kā darbojas glabāšanas laiks, ja krājuma negatīvo dienu skaits ir mazāks par preces glabāšanas laika periodu.

Sistēmai ir šādi krājumu un vispārējā plāna iestatījumi:

- **Vajadzības kods (papildināšanas stratēģija):** prasība
- **Pārdošanas dienas:** 0 dienas
- **Izpildes laiks:** 0 dienas
- **Negatīvās dienas:** 5 dienas
- **Plānotā pasūtījuma tips (krājuma noklusējuma pasūtījuma iestatījumi): pirkšanas** pasūtījums

Sistēmā ir šāds pārdošanas pasūtījums:

- **SO1: daudzums** = 2, pieprasītais piegādes datums = šodien

Šo pieprasījumu var segt ar pastāvošu piegādi no šādiem apstiprinātiem pirkšanas pasūtījumiem:

- **PO1:** Saņemšanas datums = šodiena, daudzums = 1, beigu datums = šodiena + 1 diena
- **PO2:** saņemšanas datums = šodiena + 2 dienas, daudzums = 1, beigu datums = šodiena + 3 dienas

Tomēr sistēmai ir jāņem vērā ierobežojums, ka nosūtīto preču derīguma termiņš nosūtīšanas laikā nevar būt beidzies. Tāpēc gan PO2, gan PO1 nevar izmantot so1, jo PP1 beidzas pirms PO2 saņemšanas. Sistēma izveido šādu plānoto pirkšanas pasūtījumu, lai pabeigtu SO1 pieprasījuma nosegšanu:

- **PPO1: saņemšanas** datums = šodiena, daudzums = 1, beigu datums = šodiena + 10 dienas

Sistēma var izmantot piecu negatīvo dienu priekšrocības un izmantot PO2 un PPO1, lai nosegtu SO1. Tomēr šī pieeja izraisīs piegādes aizkavēšanos līdz PO2 saņemšanas brīdim, un PP1 pa to laiku beigsies. Tāpēc sistēma sedz SO1, izmantojot PPO1 un PO1.

Tabulā ir apkopots rezultāts.

| Pieprasījums | Piesaiste |
|---|---|
| **SO1:** piegādes datums = šodiena, daudzums = 2 | <p>**PO1:** Saņemšanas datums = šodiena, daudzums = 1, beigu datums = šodiena + 1 diena</p><p>**PPO1: saņemšanas** datums = šodiena, daudzums = 1, beigu datums = šodiena + 10 dienas</p> |

Šajā ilustrācijā parādīta šī piemēra laika skala.

![6. piemērs: vienkāršs FEFO, vajadzība, piecas negatīvas dienas.](media/fefo-example-6.png "6. piemērs: vienkārša FEFO, prasība, piecas negatīvas dienas")
