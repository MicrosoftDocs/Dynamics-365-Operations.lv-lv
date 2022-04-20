---
title: Krājumu budžets
description: Šajā tēmā aprakstīta piegādes un pieprasījuma apjoma prognozes funkcionalitāte, ko var izmantot, lai izveidotu krājumu budžetu programmā Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1446928c2f5fe606d1d0732764a2a4460643afcf
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/05/2022
ms.locfileid: "8548172"
---
# <a name="inventory-forecasts"></a>Krājumu budžets

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā skatīt un izveidot krājumu budžetu. Varat izveidot un skatīt piegādes un pieprasījuma apjoma prognozes rindas krājumiem, krājumu grupām, krājumu sadalījuma principiem, debitoru kontiem, debitoru grupām, kreditoru kontiem un kreditoru grupām.

Katrai budžeta rindai var atlasīt pielietojamo prognozes modeli. Pēc tam var norādīt krājumu vai krājumu grupu, pieskaitot daudzumu vai darbības summu. Varat iestatīt arī laika grafiku budžeta daudzuma sadalei.

Piegādes un pieprasījuma apjoma prognozes rindas veido krājumu budžetu tai pašai krājuma un modeļa kombinācijai. Šis krājumu budžets parāda bilanci starp piegādi un pieprasījumu, kas tika ievadīts tam pašam krājumam. To nevar rediģēt. Krājumu budžets palīdz krājumu pārvaldības grupai pārskatīt rīcībā esošo krājumu paredzamās izmaiņas krājumiem gaidāmajā periodā.

Pēc pieprasījuma un/vai piegādes ievadīšanas varat palaist budžeta plānošanu, lai aprēķinātu bruto vajadzības pēc materiāliem un noslodzes un izveidotu plānotos pasūtījumus.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Budžeta rindu skatīšana un manuāla ievade

Izmantojiet šo procedūru, lai manuāli izveidotu budžeta rindas precēm.

Pastāv arī citi veidi, kā izveidot budžeta rindas:

- [Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md).
- [Vēsturisko datu importēšana pieprasījuma apjoma prognozēm](import-historical-data.md).
- [Prognozes ģenerēšana izmantojot Microsoft Azure algoritmiskās mācīšanās tīmekļa pakalpojumus](demand-forecasting-setup.md).
- [Pieprasījuma vai piegādes apjoma prognozes rindas importēšana, izmantojot datu pārvaldības struktūru (ForecastDemandForecastEntryStaging un ForecastSupplyForecastEntryStaging datu elementus)](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).

1. darbībā esošajā tabulā redzmi dažādi veidi, kā piekļūt izmantotajām lapām.

1. Atkarībā no elementa veida, kuram vēlaties izveidot prognozi, un prognozes veida, ko vēlaties izveidot, atveriet piegādes, pieprasījuma vai krājumu prognozes lapu kā aprakstīts nākamajā tabulā.

    | Elements | Instrukcijas |
    |---|---|
    | Izlaistās preces | <ol><li>Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</li><li>Atlasiet preci, kurai veidot prognozi.</li><li>Darbību rūts cilnes **Plāns** grupā **Prognozes** atlasiet **Pieprasījuma apjoma prognoze**, **Piegādes apjoma prognoze** vai **Krājumu prognoze** atkarībā no prognozes veida, ar kuru vēlaties strādāt.</li></ol> |
    | Izlaistie preces varianti | <ol><li>Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistie preces varianti**.</li><li>Atlasiet variantu, kuram veidot prognozi.</li><li>Darbību rūts cilnes **Plāns** grupā **Prognozes** atlasiet **Pieprasījuma apjoma prognoze**, **Piegādes apjoma prognoze** vai **Krājumu prognoze** atkarībā no prognozes veida, ar kuru vēlaties strādāt.</li></ol> |
    | Krājumu grupas | <ol><li>Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Krājumi \> Inventarizācijas grupas**.</li><li>Atlasiet krājumu grupu, kurai veidot prognozi.</li><li>Darbību rūts cilnē atlasiet **Prognozēšana \> Pieprasījums**, **Prognozēšana \> Piegāde** vai **Prognozēšana \> Krājumu prognoze** atkarībā no prognozes veida, ar kuru vēlaties strādāt.</li></ol> |
    | Krājumu sadalījuma principi | <ol><li>Doties uz **Krājumu pārvaldība \> Iestatījumi \> Budžets**.</li><li>Atlasiet krājumu sadalījuma principu, kam veidot budžetu.</li><li>Darbību rūtī atlasiet **Pieprasījuma apjoma prognoze**.</li></ol> |
    | Debitori | <ol><li>Dodieties uz **Vispārējā plānošana \> Prognozēšana \> Manuāls prognozes ieraksts \> Debitori**.</li><li>Atlasiet debitoru, kuram veidot prognozi.</li><li>Darbību rūtī atlasiet **Pieprasījuma apjoma prognozes definēšana**.</li></ol> |
    | Debitoru grupas | <ol><li>Dodieties uz **Vispārējā plānošana \> Prognozēšana \> Manuāls prognozes ieraksts \> Debitoru grupas**.</li><li>Atlasiet debitoru grupu, kurai veidot prognozi.</li><li>Darbību rūtī atlasiet **Pieprasījuma apjoma prognozes definēšana**.</li></ol> |
    | Kreditori | <ol><li>Dodieties uz **Vispārējā plānošana \> Prognozēšana \> Manuāls prognozes ieraksts \> Kreditori**.</li><li>Atlasiet kreditoru, kuram veidot prognozi.</li><li>Lai atvērtu lapu **Piegādes apjoma prognoze**, darbību rūtī atlasiet **Ievade**.</li></ol> |
    | Kreditoru grupas | <ol><li>Dodieties uz **Vispārējā plānošana \> Prognozēšana \> Manuāls prognozes ieraksts \> Kreditoru grupas**.</li><li>Atlasiet kreditoru grupu, kurai veidot prognozi.</li><li>Lai atvērtu lapu **Piegādes apjoma prognoze**, darbību rūtī atlasiet **Ievade**.</li></ol> | 
    | Visas rindas | <ul><li>Dodieties uz **Vispārējā plānošana \> Prognozēšana \> Pieprasījuma apjoma prognozes rindas** vai **Vispārējā plānošana \> Prognozēšana \> Piegādes apjoma prognozes rindas**, atkarībā no prognozes veida, ar kuru vēlaties strādāt.</li></ul> |

    Atkarībā no šīs atlases tiek parādīta **Piegādes apjoma prognozes** vai **Pieprasījuma apjoma prognozes** lapa. Tā parāda jebkuras esošas budžeta rindas ierakstam, ko atlasījāt pirms lapas atvēršanas.

1. Darbību rūtī atlasiet **Jauns**, lai režģim pievienotu budžeta rindu augšējā lapas daļā.
1. Jaunās rindas laukā **Modelis** atlasiet pielietojamo prognozes modeli. Pēc tam pēc vajadzības ievadiet citu informāciju, piemēram, krājumu, krājumu grupu, debitora vai kreditora kontu vai grupu, krājumu daudzumu vai kopējo darbību summu. Pilnīgu informāciju par laukiem, kas ir pieejami **Piedāvājuma apjoma prognozes** un **Pieprasījuma apjoma prognozes** lapās, skatiet tālāk šīs tēmas sadaļās.
1. Lai sadalītu budžetu visam periodam, cilnes **Apskats** rīkjoslā atlasiet **Piešķirt budžetu**.
1. Režģī **Sadalījums** pārskatiet laika diapazonu un laika intervālus, kas tiks izmantoti budžeta daudzumu sadalei.

## <a name="supply-forecast-lines"></a>Piegādes apjoma prognozes rindas

Piegādes apjoma prognoze ļauj izveidot plānu krājumu iegādei. Tas paziņo sagādes un avotu darbiniekiem, ko vajadzētu pasūtīt.

Varat ievadīt piegādes apjoma prognozi pēc krājuma, krājumu grupas, krājumu sadalījuma principa, kreditora un kreditoru grupas. Informāciju par visiem **Piegādes apjoma prognozes** lapas atvēršanas veidiem dažādiem elementiem un ierakstiem, skatiet iepriekš šīs tēmas sadaļā [Budžeta rindu skatīšana un manuāla ievade](#manual-entry).

Lapas **Piegādes apjoma prognozes** augšējā daļa nodrošina režģi ar piegādes apjoma prognozes rindām un ciļņu kopu, ko varat izmantot, lai skatītu un iestatītu papildu informāciju par atlasīto budžeta rindu. Lapas apakšējā daļā ir sniegts **Sadalījuma** režģis.

Tālāk redzamās apakšsadaļas apraksta visus laukus, kas ir pieejami katrā cilnē, un visas komandas, kas ir pieejamas lapas darbību rūtī un rīkjoslā, cilnē **Apskats**.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Darbību rūts komandas piegādes apjoma prognozes lapā

Šajā tabulā ir aprakstītas komandas, kas ir pieejamas **Piegādes apjoma prognozes** lapas darbību rūtī.

| Komanda | Apraksts |
|---|---|
| Saglabāt | Saglabā pašreizējos iestatījumus. |
| Labot | Iespējo lapas iestatījumu rediģēšanu. |
| Jauna | Pievieno budžeta rindu augšējam režģim. |
| Delete | Noņem atlasīto budžeta rindu no augšējā režģa. |
| Budžeta bilances | Skatiet paredzamās bilances, kas aprēķinātas atlasītā rindas modeļa ID pašreizējam finanšu gadam. Bilances tiek sadalītas pēc perioda (mēneša). |
| Naudas plūsmas prognozes | Skatiet paredzamās darbības, kas piešķirtas Virsgrāmatai. Papildinformāciju skatiet sadaļā [Naudas plūsmas prognozes](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Krājums \> Dimensiju rādīšana | Atlasiet krājumu dimensijas, kas jāparāda režģa cilnē **Apskats**. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Rīkjoslas komandas piegādes apjoma prognozes lapas cilnē Apskats

Šajā tabulā ir aprakstītas komandas, kas ir pieejamas **Piegādes apjoma prognozes** lapas **Apskats** cilnes rīkjoslā.

| Komanda | Apraksts |
|---|---|
| Piešķirt budžetu | Ja izmantojat sadalījuma metodi, izveidojiet atsevišķas grafika rindas budžeta darbībām. Pēc tam rindu daudzums tiek sadalīts pēc datuma (atbilstoši atlasītajiem laika intervāliem), daudzuma un summas visā laika diapazonā. (Skatiet sadaļu [Iedalīt prognozi](#allocate-forecast) tālāk Šajā tēmā.) |
| Lielapjoma atjaunināšana | Atveriet lapu **Budžeta darbību rediģēšana**. (Skatiet sadaļu [Budžeta darbību lielapjoma atjaunināšana](#bulk-update) tālāk šajā tēmā.) |
| Krājumu budžets | Atveriet **Krājumu budžeta** lapas skatu, kas ir filtrēts atlasītajai krājumu/modeļu kombinācijai. (Skatiet sadaļu [Krājumu budžets](#inventory-forecast) tālāk šajā tēmā.) |
| Izveidot krājuma vajadzības | Atveriet dialoglodziņu, kurā var izveidot krājumu vajadzības un pārdošanas pasūtījumu vai krājumu žurnāla rindas ar projektu saistītajām budžeta darbībām. Lai gan šī komanda ir pieejama gan piegādes apjoma prognozes rindām, gan pieprasījuma apjoma prognozes rindām, to nevar izmantot **Piegādes apjoma prognozes** lapā. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Piegādes apjoma prognozes lapas cilne Apskats

Nākamajā tabulā ir aprakstīti lapas **Piegādes apjoma prognozes** lauki cilnē **Apskats**.

| Lauks | Apraksts |
|---|---|
| **Modelis** | Budžeta modelis, ar kuru saistīta darbība. |
| **Datums** | Darbības sākuma datums. |
| **Kreditora konts** | Kreditora konts ar ko ir saistīta darbība. |
| **Kreditoru grupa** | Kreditoru grupa ar ko ir saistīta darbība. |
| **Krājuma numurs** | Krājuma identifikators. |
| **Krājuma grupa** | Krājuma grupa, ar ko ir saistīta darbība. |
| **Krājumu sadalījuma princips** | Krājumu sadalījuma princips, kas ir saistīts ar prognozi. |
| **Pieļaujamā svara daudzums** | Prognozētais daudzums norādītajās pieļaujamā svara vienībās. |
| **Pieļaujamā svara vienība** | Pieļaujamā svara vienība, kurā krājums ir iegādāts. Vērtība tiek automātiski izgūta no krājuma iestatījuma. |
| **Daudzums** | Prognozētais daudzums norādītajā pirkšanas vienībā. |
| **Vienība** | Krājuma pirkšanas vienība. Vērtība tiek automātiski izgūta no krājuma iestatījuma. Tomēr, to var modificēt, ja ir iestatīta vienību pārveidošana. |
| **Summa** | Bruto summa bez atlaidēm, kuru budžeta darbība pievieno prognozei. |
| **Valūta** | Budžeta darbībā izmantotā valūta. Noklusējuma valūta tiek ievadīta automātiski, bet var atlasīt arī citu valūtu. |
| (Citas dimensijas) | Papildu dimensijas var parādīt režģī kā kolonnas. Lai atlasītu parādītās papildu dimensijas, darbību rūtī atlasiet **Parādīt dimensijas**. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Piegādes apjoma prognozes lapas cilne Vispārīgi

Cilne **Vispārīgi** parāda papildu informāciju par rindu, kas pašreiz atlasīta cilnē **Apskats**. Daļa šīs informācijas ir atkārtojums no cilnes **Apskats**. Nākamajā tabulā ir aprakstīti lauki, kas ir unikāli cilnei **Vispārīgi**.

| Lauks | Apraksts |
|---|---|
| Sniegt pārskatu | Iestatiet šo opciju uz *Jā*, lai ietvertu darbību pārskatā. |
| Komentāri | Ievadiet jebkādus komentārus par budžeta darbību. |
| Aktīvie | Atzīmējiet šo izvēles rūtiņu, lai ietvertu darbību budžeta pārskatā. |
| Iekļaut naudas plūsmas prognozēs | Atzīmējiet šo izvēles rūtiņu, lai budžeta darbību iekļautu Virsgrāmatā. Šīs izvēles rūtiņas iestatījumu nevar modificēt pārskata darbībām. |
| PVN grupa | Nodokļu grupa, kuru izmanto, lai norādītu nodokli budžeta darbībai. |
| Krājumu PVN grupa | Krājumu nodokļu grupa, kuru izmanto, lai norādītu nodokli budžeta darbībai. |
| Metode | <p>Atlasiet metodi, kuru izmantot budžeta darbības sadalījumam:</p><ul><li>**Nav** — sadalījums netiek veikts.</li><li>**Periods** — prognozēt to pašu daudzumu katram periodam. Atlasot šo vērtību, norādiet daudzumu laukā **Uz** un laika vienību laukā **Vienība**.</li><li>**Princips** — budžeta sadalījums atbilstoši perioda sadalījuma principam, ko norāda laukā **Perioda princips**. Šo metodi var izmantot, ja ir jāņem vērā sezonālās novirzes.</li></ol>|
| Uz | <p>Ievadiet laika intervālu skaitu nākotnei, uz kuru attieksies budžets. Šis lauks ir pieejams tikai tad, ja atlasāt *Periodu* laukā **Metode**.</p><p>Piemēram, atlasot *Periods* laukā **Metode**, ievadot *1* laukā **Uz** un atlasot *Mēneši* laukā **Vienība**. Norādiet beigu datumu laukā **Beigas**, kas attieksies uz vienu gadu nākotnē. Šajā gadījumā tiek izveidota viena budžeta rinda katram nākamā gada mēnesim, pamatojoties uz krājumu un daudzumu, kāds norādīts virsraksta rindā.</p> |
| Vienība | Atlasiet laika intervāla vienību: *Dienas*, *Mēneši* vai *Gadi*. Sadalījums pēcāk atbilst dienu, mēnešu vai gadu skaitam, kādu norādījāt laukā **Uz**.|
| Perioda princips | Norādiet perioda sadalījuma principu. |
| Beigt | Norādiet beigu datumu, izmantojot laukus **Uz** un **Vienība**. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Piegādes apjoma prognozes lapas cilne Krājums

Cilne **Krājums** parāda papildinformāciju par rindu, kas pašreiz atlasīta cilnē **Apskats**.

Cilnes **Krājums** augšpusē esošais režģis atkārto krājuma informāciju, kas tiek rādīta arī cilnē **Apskats**. Turklāt tajā ir iekļauts lauks **Vienības cena**, kas parāda pirkšanas cenu vienību skaitam, kas norādīts laukā **Vienība**. Vienības cena tiek automātiski izgūta no krājuma iestatījuma, bet to var mainīt.

Laukos zem režģa ir sniegta papildinformācija par krājumu. Daļa šīs informācijas ir atkārtojums no cilnes **Apskats**. Nākamajā tabulā ir aprakstīti lauki, kas ir unikāli cilnei **Krājums**.

| Lauks | Apraksts |
|---|---|
| Cenas vienība | Vienību skaits, uz kuru attiecas pirkšanas cena. Vērtība tiek automātiski izgūta no krājumu tabulas, bet to var mainīt. |
| Pirkšanas papildmaksas | Fiksētās izmaksas pirkšanas cenai. Papildmaksas nav atkarīgas no daudzuma. |
| Atlaides procenti | Atlaide procentos. |
| Atlaides summa | Atlaide kā summa uz pārdošanas vienību. |
| Bruto summa | Summa, ja nav piemērota atlaide. |
| Daudzums | Darbību daudzums krājumu uzskaites vienībā. |
| MK apakškomplekts | Materiālu komplekta (MK) numurs noteiktam MK apakškomplektam. |
| Pakārtotais maršruts | Īpaša pakārtotā maršruta numurs. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Piegādes apjoma prognozes lapas cilne Finanšu dimensijas

Cilne **Finanšu dimensijas** parāda visas finanšu dimensijas vērtības rindai, kas pašreiz atlasīta cilnē **Apskats**.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Piegādes apjoma prognozes lapas cilne Krājumu dimensijas

Cilne **Krājumu dimensijas** parāda visas krājumu dimensijas vērtības rindai, kas pašreiz atlasīta cilnē **Apskats**.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Sadalījuma režģis piegādes apjoma prognozes lapā

Ja izmantojat krājumu sadalījuma principu vai arī ievadāt krājumu budžetu vienam vai vairākiem turpmākiem periodiem, prognozi var piešķirt, atlasot **Piešķirt budžetu** rīkjoslas cilnē **Apskats**. Daudzums tiek sadalīts tādā veidā, kā norādīts **Sadalījuma** režģa rindās.

## <a name="demand-forecast-lines"></a>Pieprasījuma apjoma prognozes rindas

Pieprasījuma apjoma prognoze ļauj ievadīt vai izveidot pieprasījumu debitoram. Tas palīdz pārdošanas un mārketinga darbiniekiem informēt vispārējās plānošanas pārdevējus par gaidāmo pieprasījumu prognozes periodā.

Varat ievadīt pieprasījuma apjoma prognozi pēc krājuma, krājumu grupas, krājumu sadalījuma principa, debitora un debitoru grupas. Informāciju par visiem **Pieprasījuma apjoma prognozes** lapas atvēršanas veidiem dažādiem elementiem un ierakstiem, skatiet iepriekš šīs tēmas sadaļā [Budžeta rindu skatīšana un manuāla ievade](#manual-entry).

Lapas **Pieprasījuma apjoma prognozes** augšējā daļa nodrošina režģi ar pieprasījuma apjoma prognozes rindām un ciļņu kopu, ko varat izmantot, lai skatītu un iestatītu papildu informāciju par atlasīto budžeta rindu. Lapas apakšējā daļā ir sniegts **Sadalījuma** režģis.

Tālāk redzamās apakšsadaļas apraksta visus laukus, kas ir pieejami katrā cilnē, un visas komandas, kas ir pieejamas lapas darbību rūtī un rīkjoslā, cilnē **Apskats**.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Darbību rūts komandas pieprasījuma apjoma prognozes lapā

Šajā tabulā ir aprakstītas komandas, kas ir pieejamas **Pieprasījuma apjoma prognozes** lapas darbību rūtī.

| Komanda | Apraksts |
|---|---|
| Saglabāt | Saglabā pašreizējos iestatījumus. |
| Labot | Iespējo lapas iestatījumu rediģēšanu. |
| Jauna | Pievieno budžeta rindu augšējam režģim. |
| Delete | Noņem atlasīto budžeta rindu no augšējā režģa. |
| Budžeta bilances | Skatiet paredzamās bilances, kas aprēķinātas atlasītā rindas modeļa ID pašreizējam finanšu gadam. Bilances tiek sadalītas pēc perioda (mēneša). |
| Naudas plūsmas prognoze | Skatiet paredzamās darbības, kas ir jāpiešķir Virsgrāmatai. Papildinformāciju skatiet sadaļā [Naudas plūsmas prognozes](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Parādīt dimensijas | Atlasiet preces, noliktavas un izsekošanas dimensijas, kas jāparāda režģa cilnē **Apskats**. |
| Virsgrāmatas priekšskatījums | Skatiet atlasītās darbības Virsgrāmatas ierakstus. |
| Pārsūtīt piedāvājuma rindas | Pārsūtiet piedāvājuma rindas uz atlasīto projektu. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Rīkjoslas komandas pieprasījuma apjoma prognozes lapas cilnē Apskats

Šajā tabulā ir aprakstītas komandas, kas ir pieejamas **Pieprasījuma apjoma prognozes** lapas **Apskats** cilnes rīkjoslā.

| Komanda | Apraksts |
|---|---|
| Piešķirt budžetu | Ja izmantojat sadalījuma metodi, izveidojiet atsevišķas grafika rindas budžeta darbībām. Pēc tam rindu daudzums tiek sadalīts pēc datuma (atbilstoši atlasītajiem laika intervāliem), daudzuma un summas visā laika diapazonā. (Skatiet sadaļu [Iedalīt prognozi](#allocate-forecast) tālāk Šajā tēmā.)|
| Lielapjoma atjaunināšana | Atveriet lapu **Budžeta darbību rediģēšana**. (Skatiet sadaļu [Budžeta darbību lielapjoma atjaunināšana](#bulk-update) tālāk šajā tēmā.) |
| Krājumu budžets | Atveriet **Krājumu budžeta** lapas skatu, kas ir filtrēts atlasītajai krājumu/modeļu kombinācijai. (Skatiet sadaļu [Krājumu budžets](#inventory-forecast) tālāk šajā tēmā.) |
| Izveidot krājuma vajadzības | Atveriet dialoglodziņu, kurā var izveidot krājumu vajadzības un pārdošanas pasūtījumu vai krājumu žurnāla rindas ar projektu saistītajām budžeta darbībām. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Pieprasījuma apjoma prognozes lapas cilne Apskats

Nākamajā tabulā ir aprakstīti lapas **Pieprasījuma apjoma prognozes** lauki cilnē **Apskats**.

| Lauks | Apraksts |
|---|---|
| **Uzdevuma nosaukums** | Pakešuzdevuma daļas nosaukums, kas tiek izmantots budžeta rindas izveidē. |
| **Modelis** | Budžeta modelis, ar kuru saistīta darbība. |
| **Datums** | Darbības sākuma datums. |
| **Debitora konts** | Debitora konts ar kuru ir saistīta darbība. |
| **Debitoru grupa** | Debitoru grupa ar kuru ir saistīta darbība. |
| **Krājuma numurs** | Krājuma identifikators. |
| **Preces nosaukums** | Krājuma apraksts. |
| **Krājumu sadalījuma princips** | Krājumu sadalījuma princips, kuru izmanto krājumu budžeta sadalījumā. |
| **Pārdošanas daudzums** | Darbību daudzums norādītajā pārdošanas vienībā. |
| **Vienība** | Krājuma pārdošanas mērvienības. |
| **Daudzums** | Bruto summa bez atlaidēm, kuru budžeta darbība pievieno prognozei. |
| **Pārdošanas cena** | Pārdošanas cena vienību skaitam, kas norādīts laukā **Cenas vienība**. Vērtība tiek izgūta no krājuma iestatījuma, bet to var mainīt. |
| **Pārdošanas valūta** | Budžeta darbībā izmantotā valūta. Noklusējuma valūta tiek ievadīta automātiski, bet var atlasīt arī citu valūtu. |
| **Pieļaujamā svara daudzums** | Prognozētais daudzums norādītajās pieļaujamā svara vienībās. |
| **Pieļaujamā svara vienība** | Pieļaujamā svara vienība, kurā krājums tiek pārdots. Vērtība tiek automātiski izgūta no krājuma iestatījuma. |
| (Citas dimensijas) | Papildu preces, noliktavas un izsekošanas dimensijas var parādīt režģī kā kolonnas. Lai atlasītu parādītās papildu dimensijas, darbību rūtī atlasiet **Parādīt dimensijas**. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Pieprasījuma apjoma prognozes lapas cilne Vispārīgi

Cilne **Vispārīgi** parāda papildu informāciju par rindu, kas pašreiz atlasīta cilnē **Apskats**. Daļa šīs informācijas ir atkārtojums no cilnes **Apskats**. Nākamajā tabulā ir aprakstīti lauki, kas ir unikāli cilnei **Vispārīgi**.

| Lauks | Apraksts |
|---|---|
| Pieprasījuma apjoma prognozes sērijas numurs | Pieprasījuma apjoma prognozes rindas unikālais numurs. Šis numurs tiek ģenerēts, izmantojot numuru sēriju, kas ir atlasīta pieprasījuma apjoma prognozēm **Vispārējās plānošanas parametru** lapā. |
| Krājumu grupa | Krājuma grupa, ar ko ir saistīta darbība. |
| Sniegt pārskatu | Iestatiet šo opciju uz *Jā*, lai ietvertu darbību pārskatā. |
| Komentāri | Ievadiet jebkādus komentārus par budžeta darbību. |
| Aktīvie | Atzīmējiet šo izvēles rūtiņu, lai ietvertu darbību budžeta pārskatā. Šīs izvēles rūtiņas iestatījumu nevar modificēt pārskata darbībām. |
| Iekļaut naudas plūsmas prognozēs | Atzīmējiet šo izvēles rūtiņu, lai budžeta darbību iekļautu Virsgrāmatā. Šīs izvēles rūtiņas iestatījumu nevar modificēt pārskata darbībām. Papildinformāciju skatiet sadaļā [Naudas plūsmas prognozes](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| PVN grupa | Nodokļu grupa, kuru izmanto, lai norādītu nodokli budžeta darbībai. |
| Krājumu PVN grupa | Krājumu nodokļu grupa, kuru izmanto, lai norādītu nodokli budžeta darbībai. |
| Metode | <p>Atlasiet metodi, kuru izmantot budžeta darbības sadalījumam:</p><ul><li>**Nav** — sadalījums netiek veikts.</li><li>**Periods** — prognozēt to pašu daudzumu katram periodam. Atlasot šo vērtību, norādiet daudzumu laukā **Uz** un laika vienību laukā **Vienība**.</li><li>**Princips** — budžeta sadalījums atbilstoši perioda sadalījuma principam, ko norāda laukā **Perioda princips**. Šo metodi var izmantot, ja ir jāņem vērā sezonālās novirzes.</li><ul>|
| Uz | <p>Ievadiet laika intervālu skaitu nākotnei, uz kuru attieksies budžets. Šis lauks ir pieejams tikai tad, ja atlasāt *Periodu* laukā **Metode**.</p><p>Piemēram, atlasot *Periods* laukā **Metode**, ievadot *1* laukā **Uz** un atlasot *Mēneši* laukā **Vienība**. Norādiet beigu datumu laukā **Beigas**, kas attieksies uz vienu gadu nākotnē. Šajā gadījumā tiek izveidota viena budžeta rinda katram nākamā gada mēnesim, pamatojoties uz krājumu un daudzumu, kāds norādīts virsraksta rindā. |
| Vienība | Atlasiet laika intervāla vienību: *Dienas*, *Mēneši* vai *Gadi*. Sadalījums pēcāk atbilst dienu, mēnešu vai gadu skaitam, kādu norādījāt laukā **Uz**.|
| Perioda princips | Norādiet perioda sadalījuma principu, ko izmanto budžeta sadalījumam. Papildinformāciju skatiet sadaļā [Budžeta plānošanas datu sadalījums](../../finance/budgeting/budget-planning-data-allocation.md). |
| Beigt | Norādiet beigu datumu, izmantojot laukus **Uz** un **Vienība**. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Pieprasījuma apjoma prognozes lapas cilne Krājums

Cilne **Krājums** parāda papildu informāciju par krājumu, kas pašreiz atlasīts cilnē **Apskats**. Daļa šīs informācijas ir atkārtojums no cilnes **Apskats**. Nākamajā tabulā ir aprakstīti lauki, kas ir unikāli cilnei **Krājums**.

| Lauks | Apraksts |
|---|---|
| Cenas vienība | Pārdošanas vienību skaits, uz kuru attiecas pārdošanas cena. Vērtība tiek automātiski izgūta no krājumu tabulas, bet to var mainīt. |
| Pārdošanas papildmaksas | Fiksētās izmaksas pārdošanas cenai. Papildmaksas nav atkarīgas no daudzuma. |
| Izmaksu cena | Pašreizējās budžeta darbības izmaksas uz krājuma vienību. Vērtība tiek izgūta no tabulas Krājumi, bet to var mainīt. |
| Atlaides procenti | Atlaide procentos. |
| Atlaides summa | Atlaide kā summa uz pārdošanas vienību. |
| Bruto summa | Summa, ja nav piemērota atlaide. |
| Krājumu daudzums | Darbību daudzums krājumu uzskaites vienībā. |
| Izmantot noteiktu MK | Noteikta MK numurs. |
| Izmantot specifisku maršrutu | Īpaša pakārtotā maršruta numurs. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Pieprasījuma apjoma prognozes lapas cilne Projekts

Cilne **Projekts** parāda papildu informāciju par projektu, kas pašreiz atlasīts cilnē **Apskats**. Daļa šīs informācijas ir atkārtojums no cilnēm **Apskats**, **Vispārīgi** vai **Krājums**. Nākamajā tabulā ir aprakstīti lauki, kas ir unikāli cilnei **Projekts**.

| Lauks | Apraksts |
|---|---|
| Projekta datums | Pieprasījuma apjoma prognozes darbības datums. |
| Projekta ID | Identifikators projektam, uz kuru attiecas pašreizējā darbība. |
| Finansējuma avots | Ar pieprasījuma apjoma prognozi saistītais finansējuma avots. |
| Aktivitātes numurs | Ar pieprasījuma apjoma prognozes darbību saistītā aktivitāte. |
| Kategorija | Pašreizējās darbības izmaksu kategorija. |
| Rindas rekvizīts | Statuss, kas ir piesaistīts darbībai. |
| Darbības ID | Sistēmas ģenerēts identifikators pieprasījuma apjoma prognozes darbībai. |
| Izmaksu summa | Pieprasījuma apjoma prognozes darbības summa. |
| Vienības cena | Cena par vienību. |
| Modificēja | Identifikators darbiniekam, kurš pēdējais modificējis atlasīto darbību. |
| Rēķina datums | Ievadiet paredzēto rēķina datumu. |
| Korekcijas datums | Skatiet vai mainiet korekcijas datumu. Kad budžets ir izveidots, korekcijas datums tiek iestatīts uz projekta beigu datumu. Ja projektam nav beigu datuma, tiek piemērots projekta datums. Šis lauks attiecas uz fiksētas cenas projektiem un investīciju projektiem. |
| Izmaksu apmaksas datums | Ievadiet pirkuma maksājuma paredzamo datumu. |
| Pārdošanas pasūtījuma apmaksas datums | Ievadiet pārdošanas pasūtījuma maksājuma paredzamo datumu. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Pieprasījuma apjoma prognozes lapas cilne Finanšu dimensijas

Cilne **Finanšu dimensijas** parāda visas finanšu dimensijas vērtības rindai, kas pašreiz atlasīta cilnē **Apskats**.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Pieprasījuma apjoma prognozes lapas cilne Krājumu dimensijas

Cilne **Krājumu dimensijas** parāda visas krājumu dimensijas vērtības rindai, kas pašreiz atlasīta cilnē **Apskats**.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Sadalījuma režģis pieprasījuma apjoma prognozes lapā

Ja izmantojat krājumu sadalījuma principu vai arī ievadāt krājumu budžetu vienam vai vairākiem turpmākiem periodiem, prognozi var piešķirt, atlasot **Piešķirt budžetu** rīkjoslas cilnē **Apskats**. Daudzums tiek sadalīts tādā veidā, kā norādīts **Sadalījuma** režģa rindās. (Skatiet sadaļu [Iedalīt prognozi](#allocate-forecast) tālāk Šajā tēmā.)

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Krājumu prognoze

Piegādes un pieprasījuma apjoma prognozes rindu lapās ir poga **Krājumu budžets**, kas atver tā paša krājuma/modeļa kombinācijas filtrētās lapas **Krājumu budžets** skatu. Krājumu budžets parāda bilanci starp piegādi un pieprasījumu, kas tika ievadīts tam pašam krājumam. To nevar rediģēt. Krājumu budžets palīdz krājumu pārvaldības grupai pārskatīt rīcībā esošo krājumu paredzamās izmaiņas krājumiem gaidāmajā periodā.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Darbību rūts lapā Krājumu prognoze

Šajā tabulā ir aprakstītas komandas, kas ir pieejamas **Krājumu prognozes** lapas darbību rūtī.

| Darbība | Apraksts |
|---|---|
| Piegādes apjoma prognoze | Atveriet **Piegādes apjoma prognozes** lapas skatu, kas ir filtrēts tai pašai krājumu/modeļu/datumu kombinācijai. |
| Pieprasījuma apjoma prognoze | Atveriet **Pieprasījuma apjoma prognozes** lapas skatu, kas ir filtrēts tai pašai krājumu/modeļu/datumu kombinācijai. |
| Krājums \> Dimensiju rādīšana | Atlasiet preces, noliktavas un izsekošanas dimensijas, kas jāparāda **Apskata** režģī. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Režģis lapā Krājumu prognoze

Tabulā ir aprakstīti lauki, kas atrodami **Krājumu prognozes** lapas režģī.

| Lauks | Apraksts |
|---|---|
| **Modelis** | Budžeta modelis, ar kuru saistīta darbība. |
| **Krājuma numurs** | Krājuma identifikators. |
| **Budžeta datums** | Budžeta darbības datums. |
| **Budžeta tips** | Darbības avots (*Pieprasījuma apjoma prognoze* vai *Piegādes apjoma prognoze*). |
| **Pieļaujamā svara daudzums** | Prognozētais daudzums pieļaujamā svara vienībās. |
| **Daudzums** | Prognozētais daudzums krājumu uzskaites vienībās. |
| **Uzkrātais pieļaujamais svars** | Uzkrātais prognozējamais daudzums pieļaujamā svara vienībā, ja tam pašam krājumam ir uzkrātas vairākas budžeta rindas. |
| **MK apakškomplekts** | Noteikta MK apakškomplekta numurs. |
| **Pakārtotais maršruts** | Īpaša pakārtotā maršruta numurs. |
| (Citas dimensijas) | Papildu dimensijas var parādīt režģī kā kolonnas. Lai atlasītu parādītās papildu dimensijas, darbību rūtī atlasiet **Krājumi \> Parādīt dimensijas**. |

## <a name="allocate-forecast"></a><a name="allocate-forecast"></a>Piešķirt prognozi

Izmantojiet šo procedūru, lai apstrādātu atlasītas prognozes transakciju rindas. Piešķirot prognozi, daudzums tiek sadalīts kā norādīts rindās režģī **Sadalījums**.

1. Atkarībā no entitījas tipa, kurai izveidojat prognozi, un no veidojamās prognozes tipa, atveriet piegādes vai pieprasījuma prognozes lapu, kā aprakstīts rakstā [Prognozes rindu skatīšana un manuāla ievade](#manual-entry).
1. Piegādes vai pieprasījuma prognozes rindu lapā atlasiet prognozes rindu un cilnē **Pārskats** rīkjoslā atlasiet **Piešķirt prognozi**.
1. Dialoglodziņā **Piešķirt prognozi** iestatiet Šajā tabulā aprakstītos laukus. (Vērtība, kuru atlasāt laukā **Metode** nosaka, ka pārējie lauki ir pieejami.)

    | Lauks | Apraksts |
    |---|---|
    | Metode | <p>Atlasiet metodi, kuru izmantot budžeta darbības sadalījumam:</p><ul><li>**Nav** — sadalījums netiek veikts.</li><li>**Periods** — prognozēt to pašu daudzumu katram periodam. Atlasot šo vērtību, norādiet daudzumu laukā **Uz** un laika vienību laukā **Vienība**.</li><li>**Princips** — budžeta sadalījums atbilstoši perioda sadalījuma principam, ko norāda laukā **Perioda princips**. Šo metodi varat lietot, ja vēlaties iekļaut sezonālas variācijas.</li><ul>|
    | Kam | <p>Ievadiet laika intervālu skaitu nākotnei, uz kuru attieksies budžets. Šis lauks ir pieejams tikai tad, ja atlasāt *Periodu* laukā **Metode**.</p><p>Piemēram, atlasot *Periods* laukā **Metode**, ievadot *1* laukā **Uz** un atlasot *Mēneši* laukā **Vienība**. Pēc tam laukā **Beigas** norādiet beigu datumu pēc viena gada. Šajā gadījumā tiek izveidota viena budžeta rinda katram nākamā gada mēnesim, pamatojoties uz krājumu un daudzumu, kāds norādīts virsraksta rindā. |
    | Vienība | Atlasiet laika intervāla vienību: *Dienas*, *Mēneši* vai *Gadi*. Sadalījums pēcāk atbilst dienu, mēnešu vai gadu skaitam, kādu norādījāt laukā **Uz**.|
    | Perioda princips | Norādiet perioda sadalījuma principu, ko izmanto budžeta sadalījumam. Papildinformāciju skatiet sadaļā [Budžeta plānošanas datu sadalījums](../../finance/budgeting/budget-planning-data-allocation.md). |
    | Beigt | Norādiet beigu datumu, kuri attiecas uz jūsu iestatījumiem laukos **Uz** un **Vienība**. |

1. Atlasiet **Labi**, lai apstiprinātu iestatījumus.
1. Rezultātus varat pārskatīt tas pašas rindas cilnē **Sadalījums**.

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Budžeta darbību lielapjoma atjaunināšanu

Izmantojiet šo procedūru, lai apstrādātu esošās prognozes darbību rindas. Prognozes darījuma rindas var kopēt, rediģēt un dzēst.

1. Piegādes vai pieprasījuma apjoma prognozes rindu lapā atlasiet **Lielapjoma atjaunināšana**.
1. Dialoglodziņā atlasiet **Filtrs**.
1. Cilnē **Diapazons** atlasiet kritērijus, kas identificē prognozes datu avotu, ko vēlaties kopēt, rediģēt vai dzēst. Šie dati var ietvert prognozes modeli, krājuma numuru un debitora kontu.
1. Atlasiet **Labi**, lai apstiprinātu atlasi.

    Pēc datu atlases, varat izmantot dialoglodziņu **Budžeta darbību rediģēšana**, lai definētu, kā tos kopēt, rediģēt vai dzēst.

    > [!NOTE]
    > Filtrēšanas darbība ir priekšnosacījums **Lielapjoma rediģēšanas** funkcionalitātes izmantošanai. Ja šo darbību izlaiž, programma atlasa un atjaunina **visas** prognožu rindas. Tādā veidā jūs varat netīši izraisīt darbību dublēšanu vai noņemšanu.

1. Sadaļā **Pārvaldība** atlasiet, vai vēlaties kopēt, atjaunināt vai dzēst atlasītās budžeta darbības.
1. Izmantojiet sadaļu **Lauka modifikācijas**, lai mainītu budžeta parametrus. Atzīmējiet parametra izvēles rūtiņu un pēc tam atlasiet kādu no pieejamajām opcijām. Piemēram, atzīmējiet izvēles rūtiņu **Modelis** un pēc tam atlasiet budžeta modeļa numuru. Esošās prognozes rindas tiek kopētas atlasītajā budžeta modelī.
1. Izmantojiet sadaļu **Perioda maiņa**, lai pārvietotu prognozes sākuma un beigu datumus uz priekšu vai atpakaļ. Atzīmējiet izvēles rūtiņu un pēc tam izmantojiet daudzuma un perioda laukus, lai definētu, kā jāpārvieto prognozes datumi. Varat ievadīt negatīvu daudzumu, lai pārvietotu sākuma datumu uz priekšu (t.i., pārlikt to ātrāk).

    Piemēram, lai atliktu prognozes darbības sākuma datumu par sešiem mēnešiem, atzīmējiet izvēles rūtiņu, kā daudzumu ievadiet *6* un kā periodu atlasiet *Mēneši*.

1. Izmantojiet sadaļu **Labot lauku**, lai atjauninātu faktiskos prognozes datus. Laukā **Lauks** atlasiet kritēriju, kuru vēlaties mainīt. Laukā **Koeficients** ievadiet reizināšanas koeficientu, ko lietot atlasītajam kritērijam, vai arī ievadiet pastāvīgo pieskaitīšanas vai atņemšanas lielumu. Piemēram, atlasiet *Daudzumu* kā kritēriju un ievadiet koeficientu *1,5*, lai reizinātu krājuma daudzumu ar 1,5. Vai arī ievadiet pastāvīgo lielumu *-25*, lai samazinātu krājuma apjomu par 25 vienībām.
1. Izmantojiet sadaļu **Finanšu dimensijas**, lai atjauninātu budžeta rindu finanšu dimensijas. Atlasiet finanšu dimensijas, kuras vēlaties mainīt, un pēc tam ievadiet vērtību, ko piemērot atlasītajām dimensijām.
1. Atlasiet **Labi**, lai piemērotu izmaiņas.

## <a name="use-forecasts-with-master-planning"></a>Izmantot prognozes ar vispārējo plānošanu

Kad ievadāt pieprasījuma apjoma prognozi un/vai piegādes apjoma prognozi, vispārējās plānošanas laikā varat ietvert prognozes, lai vispārējās plānošanas darbības laikā atstātu prognozēto pieprasījumu un/vai piedāvājumu. Kad prognoze ir iekļauta vispārējā plānošanā, tiek aprēķinātas bruto vajadzības materiāliem un noslodzei un tiek ģenerēti plānotie pasūtījumi.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Iestatīt vispārējo plānu, lai iekļautu krājumu apjoma prognozi

Lai iestatītu vispārējo plānu tā, lai tas ietvertu krājumu apjoma prognozi, sekojiet šīm darbībām.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet esošu plānu vai izveidojiet jaunu plānu.
1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:

    - **Budžeta modelis** - atlasiet lietojamo budžeta modeli. Šis modelis tiks ņemts vērā, kad pašreizējam vispārējam plānam tiek ģenerēts piegādes ieteikums.
    - **Iekļaut piegādes apjoma prognozi** - Iestatiet šo opciju kā *Jā*, lai piegādes apjoma prognozi iekļautu pašreizējā vispārējā plānā. Ja to iestatāt uz *Nē*, piegādes apjoma prognozes darījumi netiks iekļauti vispārējā plānā.
    - **Iekļaut pieprasījuma apjoma prognozi** - Iestatiet šo opciju kā *Jā*, lai pieprasījuma apjoma prognozi iekļautu pašreizējā vispārējā plānā. Ja to iestatāt uz *Nē*, pieprasījuma apjoma prognozes darījumi netiks iekļauti vispārējā plānā.
    - **Budžeta vajadzību samazināšanai izmantotā metode** — Atlasiet metodi, kas jāizmanto, lai samazinātu budžeta vajadzības. Plašāku informāciju skatiet [Prognozes samazināšanas principi](planning-optimization/demand-forecast.md#reduction-keys).

1. Kopsavilkuma cilnē **Laika periodi dienās** varat iestatīt sekojošos laukus, lai noteiktu periodu, kurā tiek iekļauta prognoze:

    - **Budžeta plāns** — iestatiet šo opciju kā *Jā*, lai ignorētu budžeta plāna laika ierobežojumu, kas izveidots no atsevišķām vajadzību grupām. Iestatiet to uz *Nē*, lai pašreizējam vispārējam plānam izmantotu vērtības no atsevišķām vajadzību grupām.
    - **Budžeta laika periods** — Ja iestatāt opciju **Budžeta plāns** kā *Jā*, norādiet dienu skaitu (no šodienas datuma), kurā jāpiemēro pieprasījuma apjoma prognoze.

    > [!IMPORTANT]
    > Ar plānošanas optimizāciju netiek atbalstīta opcija **Budžeta plāns**.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Palaist vispārējo plānu, kas iekļauj krājumu apjoma prognozi

Lai palaistu vispārējo plānu, kas ietver krājumu apjoma prognozi, sekojiet šīm darbībām.

1. Atvēriet **Vispārējā plānošana \> Darbvietas \> Vispārējā plānošana**.
1. Laukā **Vispārējais plāns** ievadiet vai atlasiet vispārējo plānu, kas iestatīts iepriekšējā procedūrā.
1. Elementā **Vispārējā plānošana** atlasiet **Palaist**.
1. Dialoglodziņā **Vispārējā plānošana** iestatiet opciju **Atsekot apstrādes laiku** uz *Jā*.
1. Laukā **Pavedienu skaits** ievadiet skaitli.
1. Kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrs**.
1. Parādās standarta vaicājumu redaktora dialoglodziņš. Cilnē **Diapazons** atlasiet rindu, kur **Lauks** ir iestatīts uz *Krājuma kods*.
1. Laukā **Kritēriji** atlasiet krājuma kodu, kas jāiekļauj plānā.
1. Atlasiet **Labi**.

Lai apskatītu aprēķinātās vajadzības, atveriet lapu **Bruto vajadzības**. Piemēram, lapas **Izlaistās preces** darbību rūtī, cilnē **Plāns** grupā **Prasības** atlasiet **Bruto vajadzības**.

Lai skatītu izveidotos plānotos pasūtījumus, dodieties uz **Vispārējā plānošana \> Vispārēji \> Plānotie pasūtījumi** un atlasiet atbilstošo budžeta plānu.

## <a name="additional-resources"></a>Papildu resursi

- [Pieprasījuma prognozes apskats](introduction-demand-forecasting.md)
- [Pieprasījuma prognozēšanas iestatīšana](demand-forecasting-setup.md)
- [Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)
- [Manuāla bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)
- [Vispārējā plānošana ar pieprasījuma apjoma prognozēm](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]