---
title: Norēķinu grafika līdzekļi
description: Šī tēma skaidro norēķinu grafiku funkcijas, piemēram, cenu noteikšanas metodes, eskalācijas un atlaides, līdzinājuma datumus, prorāciju, apgrieztos norēķinus un dalītas krājumu grupas.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ce323565a94e8e70d90a65b7a3143e984a1c159
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696648"
---
# <a name="billing-schedule-features"></a>Norēķinu grafika līdzekļi

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidroti norēķinu grafiku un norēķinu grafika rindu līdzekļi. Tajā aprakstītas dažādas metodes, kas tiek izmantotas cenu noteikšanai, kā izmantot eskalācijas un atlaides un kā atsaukt norēķinu periodu. Tas ietver arī piemērus par prorāciju aprēķiniem un krājumu grupu sadalīšanu.

## <a name="pricing-methods"></a>Cenu noteikšanas metodes

Lai aprēķinātu krājuma vienības cenu, var izmantot vienu no šīm cenu noteikšanas metodēm:

* Izlīdzināts
* Standarts
* Pakāpe
* Fiksēts līmenis

### <a name="flat-pricing"></a>Vienotā cenu noteikšana

Izmantojot vienotās cenu noteikšanas metodi, **norēķinu** grafika rindas krājuma vienības cenu lapā Visi norēķinu grafiki var rediģēt uz jebkādu vērtību, kuru vēlaties. Cenas **vienības vērtība** vienmēr ir **1**. Tāpēc vienības **cenas un** neto **summas** vērtības krājumam ir vienādas.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standarta cenu noteikšana (bez tirdzniecības līguma)

Ja standarta cenu noteikšanas metode tiek izmantota bez tirdzniecības līguma, jūs iestatāt vienības cenu norēķinu grafika rindas krājumam, **·** **atlasot Preču informācijas pārvaldību lapā Nodoto preču papildinformāciju.** Vienības cena ir parādīta sadaļā Pamata **pārdošanas** cena. Tas tiek aprēķināts kā *cenas*&divide;*cenas daudzums.*

### <a name="standard-pricing-with-a-trade-agreement"></a>Standarta cenu noteikšana (ar tirdzniecības līgumu)

Sekojošos piemēros tiek rādīti standarta cenu aprēķini, ja pastāv tirdzniecības līgums. Tirdzniecības līgumus var izveidot lapā Detalizēta informācija par **izpildei nodotām produktiem**.

Abos piemēros tiek izmantots krājums ar šādām cenu iekavām.

| Daudzums no | Līdz daudzumam | U no M | Cena | Cenas vienība |
|---|---|---|---|---|
| 0 | 100 | Katrs | 1,50 | 1 |
| 100 | 200 | Katrs | 1.25 | 1 |
| 200 | 999999 | Katrs | 1.00 | 1 |

**1. piemērs**

Rēķina daudzums ir 250 un tiek izmantota standarta cenu noteikšanas metode. Tā kā daudzums ir 200–999 999 cenas daudzuma diapazonā, vienības cena ir 1,00. 

Neto summa tiek aprēķināta šādi:

*Neto summa* = (*Daudzuma*&times;*cena*) &divide;*Cenas vienība* = (250 &times; 1,00) &divide; 1 = 250

**2. piemērs**

Rēķina daudzums ir 100 un tiek izmantota standarta cenu noteikšanas metode. Tā kā rēķina daudzums ir 0–100 cenas daudzumu diapazonā, vienības cena ir 1,50.

> [!NOTE]
> Rēķina daudzums ir 0–100 diapazonā, nevis 100–200 diapazonā, jo standarta daudzuma atbilstības uzvedības *laikā* daudzums sakrīt, ja tas ir lielāks par vai vienāds ar daudzumu "no" *un mazāks par* daudzumu "līdz".

Neto summa tiek aprēķināta šādi:

*Neto summa* = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Pakāpju cenu noteikšana

Tālākajā piemērā krājumam ir šādas cenu iekavas.

| Daudzums no | Līdz daudzumam | U no M | Cena | Cenas vienība |
|---|---|---|---|---|
| 0 | 100 | Katrs | 1,50 | 10. |
| 100 | 200 | Katrs | 1.25 | 10. |
| 200 | 999999 | Katrs | 1.00 | 10. |

Ja rēķina daudzums ir 250 un tiek izmantota pakāpju cenu noteikšanas metode, krājumu cenas tiek aprēķinātas šādi, pamatojoties uz cenu noteikšanas iekavām:

- **Pirmās 100 vienības:** 100 &times; 1,50 = 150,00
- **Otrās 100 vienības:** 100 &times; 1,25 = 125,00
- **Atlikušie krājumi:** 50 &times; 1,00 = 50,00

Neto summa tiek aprēķināta šādi:

*Neto summa* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Pēc neto summas aprēķina, vienības cenu aprēķina, dalot neto summu ar daudzumu:

*Vienības cena* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Vienotās pakāpes cenu noteikšana

Tālākajā piemērā krājumam ir šādas cenu iekavas.

| Daudzums no | Līdz daudzumam | U no M | Fiksēta līmeņa summa | Cenas vienība |
|---|---|---|---|---|
| 0 | 50 | Katrs | 100.00 | 50 |
| 50 | 200 | Katrs | 150.00 | 200 |

Tabulā ir parādīti rēķini un vienības cenas dažādiem iegādātiem daudzumiem. Neto summa tiek aprēķināta vispirms, un tad tiek aprēķināta vienības cena.

| Rēķins | Nopirktais daudzums | Vienības cena | Neto summa |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Eskalācijas un atlaides

Eskalācija *ir* cenas pieaugums nākamā norēķinu periodā, kuram vēl nav izveidots rēķins. *Atlaide* ir cenas samazināšana turpmāko norēķinu periodam, kuram vēl nav izveidots rēķins.

Abonementa rēķinos eskalācijas un atlaides maksājumu grafikam nevar piemērot atkārtoti. Piemēram, rēķinu grafikam nevar lietot eskalāciju trīs mēnešus iepriekš un apstrādāt to. Citiem vārdiem sakot, nevar piemērot cenas pieaugumu, kas noticis pirms trim mēnešiem.

Jūs varat lietot eskalāciju vai atlaidi norēķinu grafikam vai norēķinu grafika rindai vienā no šīm vietām:

- Visu **/aktīvo norēķinu grafiku** saraksta lapa
- Noteikts norēķinu grafiks
- Noteikta norēķinu grafika rinda

### <a name="apply-an-escalation-or-discount"></a>Lietot eskalāciju vai atlaidi

Lai rēķina grafikam lietotu eskalāciju vai atlaidi, sekojiet šiem soļiem.

1. Atlasiet norēķinu grafiku vai norēķinu grafika rindu.
2. Atlasiet **Eskalāciju un** atlaidi cilnē **Eskalācija un** atlaide vai rēķinu grafika rindā.
3. Ja plaša patēriņa cenu indekss tiek lietots, lai aprēķinātu eskalāciju vai atlaidi, **atlasiet vērtību laukā Patērētāja cenu indeksa** aprēķins.
4. Atlasiet **Jauns,** lai pievienotu eskalāciju vai atlaides rindu.
5. Lai iegūtu atlaidi, atzīmējiet **izvēles** rūtiņu Atlaide. Eskalācijai atstājiet izvēles **rūtiņu** Atlaide notīrītu.
6. Iestatiet sākuma **datuma un** biežuma **laukus**.
7. Atlikto maksājumu krājumiem, kas izmanto nenosāpto ieņēmumu līdzekli, iestatiet **beigu datuma** lauku.
8. Iestatiet **procentus**, **summu** vai patērētāja **cenu indeksa grafika** lauku.
9. Iestatiet beigu **datuma** lauku.
10. Atlasiet **Labi**.
11. Atkārtojiet no 4. līdz 10. solim katrai papildu eskalācijai vai atlaides rindai, kas nepieciešama.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Lauki norēķinu grafika rindu lapā

Norēķinu **grafika rindu lapā** ir šādi lauki.

| Lauks | Apraksts |
|---|---|
| Krājuma numurs | Norēķinu grafika rindas krājuma numurs. Šis lauks ir pieejams tikai tad, ja lapa ir atvērta no norēķinu grafika rindas vienuma. |
| Patēriņa cenu indeksa aprēķins | <p>Atlasiet metodi, kas tiek izmantota, lai aprēķinātu plaša patēriņa cenu indeksa eskalāciju:</p><ul><li>**Iepriekšējais patērētāja cenu indekss** – eskalācijas aprēķinam izmantojiet iepriekšējo plaša patēriņa cenu indeksa vērtību.</li><li>**Plaša patēriņa pamatcenas** indekss – eskalācijas aprēķinam izmantojiet patēriņa pamatcenas indeksa vērtību.</li></ul> |
| **Rindu** režģis | |
| Atlaide | <p>Atzīmējiet šo izvēles rūtiņu, lai norādītu, vai summas izmaiņa ir eskalācija vai atlaide:</p><ul><li>**Atlasīts** — izmaiņas attiecas uz atlaidi norēķinu grafikam vai norēķinu grafika rindai.</li><li>**Dzēsts** – izmaiņa attiecas uz eskalāciju norēķinu grafikam vai grafika rindai.</li></ul><p>Šīs izvēles rūtiņas iestatījumu nevar mainīt krājumiem, kas izmanto nenosūtāmo ieņēmumu līdzekli. Turklāt atlaides nevar lietot krājumiem, kas izmanto ieņēmumu sadali.</p> |
| Sākuma datums | Atlasiet eskalācijas vai atlaides sākuma datumu. |
| Biežums | Atlasiet eskalācijas vai atlaides biežumu: Nav **, Mēneša** **,** Ceturkšņa **,** Pusgads **vai Reizi** gadā **.** |
| Procentuālā vērtība | Norādiet eskalācijas vai atlaides procentus. |
| Summa | Norādiet eskalācijas vai atlaides summu. |
| Patēriņa cenu indeksa grafiks | Atlasiet patērētāja cenu indeksa grafiku, kas tiek izmantots aprēķiniem. |
| Beigu datums | <p>Atlasiet eskalācijas vai atlaides beigu datumu.</p><p>**Piezīme.** Šis lauks ir nepieciešams krājumiem, kas izmanto nenobīdāmo ieņēmumu līdzekli.</p> |
| Atlikšanas grafika numurs | <p>Atlikto maksājumu grafika numurs.</p><p>Šis lauks ir pieejams tikai tad, ja lapa ir atvērta no norēķinu grafika rindas.</p> |
| Žurnāla iedaļas numurs | <p>Žurnāla pakešuzdevuma numurs.</p><p>Šis lauks ir pieejams tikai tad, ja lapa ir atvērta no norēķinu grafika rindas.</p> |
| Beigu atlaides summa | <p>Atlaižu summu summa visām režģa rindām.</p><p>Šis lauks ir pieejams tikai tad, ja lapa ir atvērta no norēķinu grafika rindas.</p> |
| Pašreizējā īstermiņa nenosācīto ieņēmumu summa | <p>Pašreizējā īstermiņa nenosācāmo ieņēmumu summa.</p><p>Šī summa tiek **parādīta**, ja lapā Periodiskā līguma norēķinu parametri ir atlasīta īstermiņa atlikto maksājumu metode un **rindas krājuma konti ir iestatīti lapā Nenokārtoto ieņēmumu iestatījumi**.</p> |
| Pašreizējā ilgtermiņa nenosācīto ieņēmumu summa | <p>Pašreizējā ilgtermiņa nenosācāmo ieņēmumu summa.</p><p>Šī summa tiek **parādīta**, ja lapā Periodiskā līguma norēķinu parametri ir atlasīta īstermiņa atlikto maksājumu metode un **rindas krājuma konti ir iestatīti lapā Nenokārtoto ieņēmumu iestatījumi**.</p> |

## <a name="proration-examples"></a>Prorācijas piemēri

Prorācijas aprēķini var balstīties uz dienu skaitu vai mēnešu skaitu. Metode, kas tiek izmantota prorācijas aprēķinam, ir iestatīta lapā **Periodisko līgumu rēķinu parametri**. Proration metode ietekmē to, kā summas tiek aprēķinātas norēķinu grafikam šādās situācijās:

- Sākotnējā izveide
- Eskalācijas vai atlaides pieteikums
- Izbeigšana
- Aizturēšanas novietojums vai noņemšana
- Atbalsta pievienošana vai atjaunošana

Prorācijas metode ietekmē arī aprēķinus mēneša periodisko ieņēmumu (MRR) pārskatā.

### <a name="example-1"></a>1. piemērs

Norēķinu grafika gada summa ir $5,000. Sākuma datums ir 2019. gada 12. augusts, un beigu datums ir 2019. gada 22. decembris. Norēķinu biežums ir ikgadēji. Atkarībā no tā, vai tiek izmantota ikdienas vai ikmēneša aprēķina metode, aprēķinātā summa tiek aprēķināta sekojošos veidos:

- **Katru dienu**

    - *DaysEnd datuma* = *skaits* – *sākuma datums* + 1 = 133 dienas
    - *Dienu skaits gadā* = 2020. gada 11. augusts – 2019. gada 12. augusts + 1 = 366 dienas
    - *Plus summa* = 5000 &times; (133 &divide; 366) = 1816,94

- **Mēnesis**

    - *Sākuma mēneša daļa* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Vidējie mēneši* = 3
    - *Beigu mēneša daļa* = 22 &divide; 31
    - Prorated amount = 5000 &divide; 12 (20 &times;\[&divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>2. piemērs

Norēķinu grafika gada summa ir $12,000. Sākuma datums ir 2019. gada 1. augusts, un beigu datums ir 2019. gada 31. decembris. Norēķinu biežums ir ikgadēji. Atkarībā no aprēķina metodes, aprēķinātā summa tiek aprēķināta sekojošos veidos:

- **Katru dienu**

    - *DaysEnd datums* = *–* sākuma *datums* + 1 = 153 dienas
    - *Gada dienu skaits* = 2020. gada 31. jūlijs – 2019. gada 1. augusts + 1 = 366 dienas
    - *Plus summa* = 12 000 &times; (153 &divide; 366) = 5016,39

- **Mēnesis (pilns mēnesis)**

    - *Mēnešu skaits* = 5
    - *Kopējie mēneši* = 12
    - *Prorated amount* = (12 000 &times; 5) &divide; 12 = 5000

## <a name="reversing-a-period-billing"></a>Perioda norēķinu atsaukšana

Piemēram, norēķinu grafikam ir tikai viena rinda:

- Rēķini tiek veikti katru mēnesi 12 mēnešu laikā no janvāra līdz decembrim.
- Rēķini ir izveidoti visiem periodiem līdz aprīlim.

Jūs vēlaties anulēt rēķinu par aprīlī izrakstīto rēķinu periodu.

Ja pārdošanas rēķins vēl nav izveidots norēķinu periodam aprīlī, pārdošanas pasūtījumu var dzēst. Šajā gadījumā detalizētas informācijas **statuss** Rēķinā tiks noņemts. Tomēr, tā kā rēķins ir izveidots norēķinu periodam, **detalizētās** informācijas statuss Rēķinā nevar tikt dzēsts. Tāpēc, lai atsauktu rēķinus aprīlī, rindai jāizveido korespondējošā kredīta nota.

1. **Lapā Visi norēķinu grafiki** izveidojiet grafika rindu tam pašam krājumam.
2. Mainiet **krājuma** daudzuma vērtību uz sākotnējā daudzuma negatīvu vērtību.
3. Lauku Norēķinu **biežums** iestatiet uz **Vienreizējs**.
4. Atjauniniet sākuma un beigu datumus, lai tie atbilstu norēķinu informācijas rindas datumiem, kuriem vēlaties izveidot kredīta notu. Šim piemēram iestatiet sākuma datumu uz 2019. gada 1. aprīli un beigu datumu uz 2019. gada 30. aprīli.
5. Saglabājiet izmaiņas.
6. Atveriet lapu **Ģenerēt rēķinu** un izveidojiet pārdošanas pasūtījumu, kam ir kredīta nota norādītajam periodam.
7. Nav obligāti: grāmatot rēķinu.

Pārskatot rēķinu grafika rindas, jūs ievērojat, ka jaunajai rindai ir saite uz kredīta notu. Sākotnējai rindai joprojām būs saite uz sākotnējo aprīlī izrakstīto rēķinu.

## <a name="split-item-group-examples"></a>Sadalīt krājumu grupu piemērus

Šajā piemērā ir spēkā šāds iestatījums:

- Lapā Periodiskie **līguma norēķinu parametri ir** atlasīti vienumi **Sadalīt** pēc krājumu grupas un **lauks Unikāls grafika veids** tiek iestatīts uz **Debitors**.
- Ir izveidotas trīs krājumu grupas: PREFIKSS **·**, **DATAHUB** un **SPP**.
- Debitoram US-001 vairāki norēķinu grafiki, kur krājumu grupa ir PREFIX vai DATAHUB.
- Debitoram US-002 vairāki norēķinu grafiki, kur krājumu grupai ir PREFIKSS vai SPP.

| Norēķinu grafika numurs | Debitors | Krājumu grupa |
|---|---|---|
| <A1/&< | US-001 | PREFIKSU |
| <A002/ & PARALĒLĀS | US-001 | DATUHUB |
| <A003/&B; | US-002 | PREFIKSU |
| <A004/&B; | US-002 | SPP |

Debitors US-001 iegādājas atjaunošanas krājumu, kas pieder krājumu prefiksa grupai. Šī darbība ir jauns pārdošanas pasūtījums.

| Pārdošanas pasūtījums # | Debitors | Galvenais krājums | Atjaunošanas krājums | Atjaunošanas krājumu grupa | Norēķinu grafika numurs |
|---|---|---|---|---|---|
| SO0001 (<a0/&) | US-001 | D0001 | D0002 | PREFIKSU | <A1/&< |

Kad pārdošanas pasūtījuma rēķins ir iegrāmatots, atjaunošanas krājums tiek pievienots debitora esošajam norēķinu grafikam (PLĀNO001). Šajā norēķinu grafikā tiek izmantota krājumu PREFIKSA grupa. Visi atjaunošanas krājumi, kas pieder vienai krājumu grupai, tiek ievietoti vienā norēķinu grafikā.

**Galvene**
 
| Norēķinu grafika numurs | Debitors | Krājumu grupa |
|---|---|---| 
| <A1/&< | US-001 | PREFIKSU |

**Rinda**

| Norēķinu grafika numurs | Debitors | Krājumu grupa |
|---|---|---|
| <A1/&< | US-001 | D0002 |

Debitors US-001 tagad iegādājas atjaunošanas krājumu, kas pieder SPP krājumu grupai. Šī darbība ir jauns pārdošanas pasūtījums.

| Pārdošanas pasūtījums # | Debitors | Galvenais krājums | Atjaunošanas krājums | Atjaunošanas krājumu grupa | Norēķinu grafika numurs |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004(s) | SPP | |

Pašlaik debitora US-001 nav rēķinu grafika, kas izmanto SPP krājumu grupu. Tāpēc tiek izveidots jauns norēķinu grafiks.

**Galvene**

| Norēķinu grafika numurs| Debitors | Krājumu grupa |
|---|---|---|
| <A1/& | US-001 | SPP |

**Rinda**

| Norēķinu grafika numurs | Debitors | Krājumu grupa |
|---|---|---|
| <A1/& | US-001 | D0004(s) |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Vairāki norēķinu grafiki tam pašam gala lietotājam un debitoram

Šajā piemērā ir spēkā šāds iestatījums:

- Lapā Periodiskie **līguma norēķinu parametri ir** atlasīts **Sadalījums pēc** krājumu grupas, un **lauks Unikāls grafika veids** ir iestatīts uz **Gala lietotājs**.
- Gala lietotāju **lapā ir** iestatītas šādas debitora un gala lietotāju attiecības.

    | Debitora konts | Lietotāja konts |
    |---|---|
    | US-001 | US-221 |

Debitoram un gala lietotāja kombinācijai tiek izveidoti vairāki norēķinu grafiki. Tā **kā lapā Periodiskie** līguma norēķinu parametri ir **atlasīts** Sadalījums pēc krājumu grupas, tam pašam debitora un gala lietotāja relācijai var izveidot vairākus norēķinu grafikus.

| Norēķinu grafika numurs | Debitors | Lietotāja konts | Virsraksta krājumu grupa |
|---|---|---|---|
| <A1/& | US-001 | US-221 | IG1 (IG1) |
| <A006/&B; | US-001 | US-221 | IG2 (IG2) |
| <A007/ & PARALĒLĀS | US-001 | US-221 | IG3 (IG3) |

Lapā Krājumu **iestatīšana jūs** izveidojat atbalsta un atjaunošanas krājumu attiecības.

| Krājuma kods | Krājumu saistība | Atbalsta krājums | Atjaunošanas krājums | Atjaunošanas krājumu grupa |
|---|---|---|---|---|
| Tabula | D001 (datu) | KRĀJUMS27 | D007(s) | IG1 (IG1) |
| Tabula | D002 (datu) | 28. KRĀJUMS | D005 (datu) | IG2 (IG2) |
| Tabula | D003 (datu) | KRĀJUMS29 | D006(S) | IG3 (IG3) |

Tagad izveidojiet pārdošanas pasūtījumu debitoram US-001. Šim pārdošanas pasūtījumam ir preces no Krājumu **iestatīšanas** lapas. Kad izveidojat pārdošanas pasūtījumu, atveriet **lapu** Atbalsts un atjaunošana un **iestatiet** beigu lietotāja konta lauku un jebkuru citu nepieciešamo informāciju atjaunošanas krājumam.

Kad darbībai ir izveidots un grāmatots rēķins, debitora/gala lietotājam un krājumu grupas kombinācijai tiek izveidoti dažādi norēķinu grafiki. Vienam norēķinu grafikam var piešķirt vairāk nekā vienu rindu vienā un tajā pašā pārdošanas pasūtījumā.

| Pārdošanas pasūtījums # | Debitors | Lietotāja konts | Galvenais krājums | Atbalsta krājums | Atjaunošanas krājums | Norēķinu grafika numurs |
|---|---|---|---|---|---|---|
| SO0001 (<a0/&) | US-001 | US-221 | D001 (datu) | KRĀJUMS27 | D007(s) | <A1/& |
| SO0001 (<a0/&) | US-001 | US-221 | D002 (datu) | 28. KRĀJUMS | D005 (datu) | <A006/&B; |
| SO0001 (<a0/&) | US-001 | US-221 | D003 (datu) | KRĀJUMS29 | D006(S) | <A1/& |
