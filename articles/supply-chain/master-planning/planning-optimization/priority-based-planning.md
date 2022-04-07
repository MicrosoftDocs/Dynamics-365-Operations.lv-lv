---
title: Uz prioritāti balstīta plānošana
description: Šajā tēmā aprakstītas Uz prioritāti balstītas Microsoft plānošanas funkcijas Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: bdca7ef99716cebee5c4eb41d1e51793b9468dd4
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468305"
---
# <a name="priority-based-planning"></a>Uz prioritāti balstīta plānošana

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstītas Uz prioritāti balstītas Microsoft plānošanas funkcijas Dynamics 365 Supply Chain Management. Šī funkcija pievieno atbalstu uz pieprasījumu balstītai plānošanai, kas ir viens no demand Driven Material Requirements Planning (DDMRP) soļi. Uz prioritāti balstīta plānošana iespējo plānošanas optimizāciju, lai ģenerētu plānotos pasūtījumus, kurus nosaka plānošanas prioritātes, nevis pieprasījumu datumi.

Uz prioritāti balstīta plānošana ļauj piešķirt prioritāti papildināšanas pasūtījumiem, lai nodrošinātu steidzamu pieprasījumu pēc prioritātes tiek noteikt pēc mazāk svarīga pieprasījuma. Piemēram, krājumu papildināšanas pasūtījumam tiks prioritāte pār standarta uzpildīšanas papildināšanas pasūtījumu. Sistēma automātiski var sadalīt lielākus pasūtījumus atsevišķos mazākos pasūtījumos, kur pasūtījumu rindas tiek grupētas pēc prioritātes. Tad tas vispirms var apstrādāt visus augstas prioritātes pasūtījumus.

Lai saņemtu ātru šīs funkcijas apskatu, skatiet sekojošo video: [Plānošanas optimizācijas atbalsts uz prioritāti balstītai plānošanai Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Ieslēgt prioritātes balstīts plānojums jūsu sistēmā

Lai varētu izmantot šo līdzekli, sistēmā tas vispirms ir jāiespējo. Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Vispārējā plānošana*
- **Funkcionalitātes nosaukums:** *prioritātes vadīts MRP atbalsts optimizācijas plānošanai*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Kur un kā tiek piešķirtas plānošanas prioritātes

*Prioritātes informācijas* par piedāvājumu un pieprasījumu plānošana ir uz prioritāti balstītas plānošanas pamats. Plānošanas prioritāte nosaka pieprasījuma vai piedāvājuma rindas svarīgumu. Optimizācijas plānošana to izmanto, kad **vajadzību koda** laukam ir iestatīta *prioritāte*.

Plānošanas prioritāte parasti ir skaitlis no 0 (nulle) līdz 100, kur 0 apzīmē augstāko svarīgumu. Tas ir parādīts un iestatīts laukā **Plānošanas** prioritāte. Šo lauku var atrast šādās lapās: **pieprasījuma** apjoma prognozes rindas, pārdošanas pasūtījuma detaļas, **pirkšanas** pasūtījuma **detaļas,** **·** **detalizēta informācija par pārsūtīšanas pasūtījumu un detalizēta informācija par plānoto pasūtījumu**.

Ja atbilstošā krājuma vai vajadzības grupas vajadzības kods ir iestatīts uz Prioritāte, plānošanas optimizācijas bilances piedāvājums ar pieprasījumu, izmantojot uz pieprasījumu balstītas pieejas, kā tas aprēķina plānošanas prioritāti un katrai izlaistajai precei apsver vērtības, **kas** ir iestatītas lapas Krājumu vajadzība laukos Minimālais, *·* **·** **Pārkārtot** un Maksimālais.**·** **·**

> [!NOTE]
> Prioritātes *vērtība* ir pieejama tikai tad, **ja ir** iespējota plānošanas optimizācija.

Saistītie plānošanas prioritāšu *modeļi kontrolē plānošanas* prioritāti un sadala plānotos pasūtījumus pēc prioritāšu diapazona. Tie arī ļauj iestatīt noklusējuma plānošanas prioritāšu vērtības katram piedāvājumam vai pieprasījuma tipam un noteikt prioritātes aprēķināšanas metodi.

## <a name="types-of-priority-calculation-methods"></a>Prioritāšu aprēķina metožu tipi

Katram plānošanas prioritātes modelim ir prioritātes aprēķina **metodes iestatījums**, kas kontrolē, kā vispārējais plāns attiecas uz prioritāti plānotajiem pasūtījumiem. Pieejamās vērtības ir Maksimālā *krājumu daudzuma procenti un* *Prioritātes diapazoni*. *Prioritātes diapazoni* parāda metodes Procenti no maksimālā *krājumu daudzuma detalizētāku* versiju.

### <a name="percent-of-maximum-inventory-quantity"></a>Maksimālā krājumu daudzuma procentuālā vērtība

Maksimālā krājumu *daudzuma* aprēķināšanas metodē piegādes prioritātes aprēķins atrod pašreizējo kopējo pieejamo krājumu (neto plūsmu) *kā* procentus **no** maksimālā krājumu daudzuma vērtības, kas ir iestatīta krājumam. Pēc tam viens plānotais pasūtījums tiek izveidots katram krājumam un kreditoram (ja vien netiek izmantots maksimālais pasūtījuma daudzums sadalīšanai). Pasūtījuma plānošanas prioritāte tiek aprēķināta kā procenti no maksimālās vērtības.

Tiek izmantota šāda formula:

*Maksimālā procentuālā vērtība* = (*neto plūsmas pozīcija* × 100) ÷ *Maksimālā krājumu daudzuma vērtība no krājumu vajadzības*

Šajā formulā neto *plūsmas pozīciju* aprēķina šādi:

*Neto plūsmas pozīcijaOn-handOn-order* = *·* + *·* - Kvalificēts *pieprasījums*

- *Pasūtītais ir* paredzētā piegāde.
- *Kvalificēts* pieprasījums atspoguļo neto vajadzības, kurām ir vajadzības datums plānošanas periodā.

Vispārējās plānošanas laikā tiek veidoti jauni plānotie pasūtījumi, ja neto plūsmas pozīcija ir mazāka nekā krājuma atkārtota pasūtījuma punkta daudzums. Plānotais pasūtījuma daudzums ir starpība starp maksimālo **krājumu daudzuma vērtību**, kas iestatīta krājumu līmenī un neto plūsmas pozīcijā. Plānotā pasūtījuma prioritāte tiek aprēķināta kā neto *plūsmas pozīcijas procenti* no maksimālā **krājumu daudzuma** vērtības.

> [!NOTE]
> Aprēķinātā prioritāte nevar būt negatīva, pat ja pieprasījums pārsniedz kopējo piedāvājumu. Ja pieprasījums pārsniedz kopējo piedāvājumu, aprēķinātā prioritāte tiek iestatīta uz 0 (nulli).

### <a name="priority-ranges"></a>Prioritāšu diapazoni

Prioritātes *diapazonu aprēķināšanas* metode ir detalizētāka nekā *metode* Procenti no maksimālā krājumu daudzuma un tiek konfigurēta plānošanas prioritātes modeļa līmenī. Vairākus jaunus plānotos piegādes pasūtījumus var izveidot, lai izpildītu krājumu pieprasījumu. Plānotās piegādes prioritātes seko vērtībām, kas ir **definētas** **lapas Plānošanas prioritāšu modeļi režģī Plānošanas prioritāšu diapazoni.**

Ja prioritātes aprēķina metodes lauks ir iestatīts uz **Prioritāšu diapazoni**, stājas spēkā šādi *papildu noteikumi*:

- Ja opcija **Apsvērt pieprasījuma prioritāti** plānotajam *prioritātes modelim ir iestatīta uz Jā*, prioritāte, kas iestatīta katrā pieprasījuma rindā, ierobežos prioritātes diapazona intervālu. Jebkura jauna plānotā piedāvājuma pasūtījuma prioritāte nebūs zemāka par pieprasījuma prioritāti. Diapazona augšējā vērtība tiek uzskatīta par slieksni, ar kuru tiek salīdzināta pieprasījuma prioritātes vērtība. Ja pieprasījuma prioritāte ir tieši vidū starp divu diapazonu augšējām sliekšņa vērtībām, tiks atlasīts diapazons ar augstāko prioritāti (t.i., viszemākā prioritāte).
- Ja plānotās **prioritātes modeļa** *lauks* Plānotais pasūtījums ir iestatīts uz Viena piegāde ar svarīgāko prioritāti, tiks izveidota tikai viena piegāde, lai izpildītu visu veidu līdz maksimumam. Prioritāte tiek iestatīta uz pirmā diapazona prioritāti, kas izraisa piegādi.
- Ja nav rīcībā esošo krājumu, piegādes un pieprasījuma, rinda plānošanas prioritāšu diapazonu režģī, **kur lauks No daudzuma ir iestatīts** **·** *uz* Nulle, tiks izmantota.
- Ja ir pieprasījums, bet nav rīcībā esošo krājumu vai gaidāmas piegādes, **rinda režģī Plānošanas prioritāšu diapazoni, kur lauks No daudzuma ir iestatīts** **·** *uz Nulle vai mazāks* tiks izmantots.
- Ja tiek novērtēts diapazons, kurā ir daļa no pieprasījuma, opcijas **Apsvērt pieprasījuma prioritāti** iestatījums joprojām būs spēkā.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Atšķirības starp tradicionālajiem laika skalas aprēķiniem un prioritāšu plānošanu

Uz prioritāti balstīta plānošana atšķiras no tradicionālajiem laika skalas aprēķiniem šādos veidos:

- Visi regulārie pirmsplānošanas procesori joprojām ir spēkā. Šie pirmsapstrādes procesori ietver apstiprinātu plānoto pasūtījumu piesaisti pārdošanas pieprasījumam, pirkšanas pieprasījuma kartēšanai un rezervēšanas loģikai. Tiek apstrādāts tikai tas pieprasījums, kas nav izpildīts ar šiem pirmsapstrādes procesoriem.
- Piesaistes laikā tiek apsvērta visa piegāde, neskatoties uz tās prioritāti. Šī piegāde ietver rīcībā esošos krājumus, izdoto piegādi un neapstausto apstiprināto plānoto pasūtījumu daļu.
- Pieprasījumu "negatīvās dienas" nevar piesaistīt piegādei visu laiku.
- Kad piegāde tiek piesaistīta pieprasījumam, vispirms tiek izmantots piedāvājums ar augstāko prioritāti (t.i., ar zemāko prioritātes vērtību). Par rīcībā esošo piegādi tiek uzskatīts, ka tās prioritātes vērtība ir 0 (nulle). Tāpēc tas tiks patērēts kā ļoti pirmais avots.
- Jaunas plānotās piegādes rindas tiks izveidotas saskaņā ar regulārajiem noteikumiem par minimālā pasūtījuma izmēru, maksimālo pasūtījuma lielumu, daudzumu daudzkārtēji utt.

## <a name="planning-priority-models"></a>Prioritāšu modeļu plānošana

*Plānošanas prioritāšu modeļi* tiek piešķirti vajadzības grupām un kontrolē plānošanas prioritāti plānotajiem pasūtījumiem. Tie definē loģiku, kas nosaka, kā plānošanas prioritātes vērtība tiek aprēķināta katram plānotajam pasūtījumam, un kā prioritāte tiek piešķirta plānotajiem pasūtījumiem, piegādes rindām un pieprasījuma rindām.

Lai strādātu ar plānošanas prioritāšu modeļiem, pārejiet uz sadaļu Vispārējās **plānošanas iestatīšanas \>\> plānošanas prioritāšu modeļi**. Kā iepriekš apspriests, viens no modeļa vissvarīgākajiem iestatījumiem ir Prioritātes **aprēķināšanas metodes** vērtība. Šis iestatījums kontrolē aprēķināšanas metodi, kas tiek izmantota, kad vispārējais plāns piešķir prioritātes vērtību plānotajiem pasūtījumiem.

> [!NOTE]
> Plānošanas prioritāšu modeļi attiecas uz visu juridisko personu organizācijas ietvaros.

### <a name="coverage-group"></a>Vajadzības grupa

Iestatiet jaunu vajadzību grupu, kuru plānojat izmantot uz prioritāti balstītai plānošanai, kā aprakstīts krājumu [vajadzību kārtulu definēšanas sadaļā](../tasks/define-coverage-rules-items.md). Pēc vajadzības grupas izveides iestatiet sekojošos papildu laukus:

- **Vajadzības kods** – atlasiet *prioritāti*, ja vajadzību grupa izmantos uz prioritāti balstītu plānošanu.
- **Plānošanas prioritātes modelis** – atlasiet jebkuru organizācijas plānošanas prioritātes modeli.

### <a name="item-coverage"></a>Krājumu segums

Iestatiet krājumu vajadzības iestatījumus, kā tas ir aprakstīts Vajadzību [iestatījumos](../coverage-settings.md). Pēc noklusējuma vajadzības koda **vērtība**, kas atlasīta vajadzību grupai, tiek kopēta uz krājumu vajadzības iestatījumiem. Tomēr noklusēto vērtību pēc noklusējuma var ignorēt. Dažos gadījumos vajadzību koda lauks **krājuma** nodrošinājuma ierakstam ir *iestatīts uz Plānošana*, bet saistītai vajadzību grupai nav definēts plānošanas prioritātes modelis. Šajos gadījumos visi modeļi, **·** *·* **·** *kuros* Prioritātes aprēķināšanas metodes lauks ir iestatīts kā procenti no maksimālā krājumu daudzuma un lauks Plānotā pasūtījuma izveidošana ir iestatīts uz Viena piegāde ar svarīgāko prioritāti, tiks piemērots pēc noklusējuma.

Lai krājumu **vajadzību iestatījumos** būtu pieejams *lauks* Pārkārtot **punktu**, iestatiet lauku Vajadzības kods uz Prioritāte. Šajā laukā ievadiet atkārtota pasūtījuma punkta daudzumu, kas sistēmai jāizmanto, nosakot, kad veikt plānotos **pasūtījumus**, kuru vajadzības koda vērtība ir *Prioritāte*.

Atkārtota pasūtījuma punktu daudzums bieži tiek aprēķināts kā pieprasījums izpildes laikā plus minimālā vērtība (drošības rezerve). Tai ir jābūt vērtībai starp minimālo **un** maksimālo **vērtību**.

Piemēram, laukus var iestatīt šādā veidā:

- **Minimums:** *10*
- **Atkārtota pasūtījuma punkts:** *45*
- **Maksimums:** *60*

Piemēram, atkārtota pasūtījuma punkta daudzums tiek balstīts uz septiņu dienu izpildes laiku un vidējo 5 dienas lietojumu. Tādēļ pieprasījums izpildes laikā ir 35. Minimālā vērtība 10 (drošības rezerve) tiek pievienota, lai iegūtu 45. atkārtota pasūtījuma punktu. Ja tiek izmantoti šie iestatījumi, piegāde tiks ieteikta, ja plānotais rīcībā esošo krājumu līmenis ir zem 45. Pasūtījuma prioritāte tiks pamatota ar plānošanas prioritātes iestatījumu.

### <a name="manage-planning-priority-models"></a>Pārvaldīt plānošanas prioritāšu modeļus

Strādāt ar plānošanas prioritāšu modeļiem. Rīkojieties.

1. Pāriet uz vispārējās **plānošanas iestatīšanas \> plānošanas \> prioritāšu modeļiem**.
1. Atlasiet esošu modeli saraksta rūtī vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu modeli.
1. Ieraksta galvenē iestatiet tālāk norādītos laukus.

    - **Nosaukums** – ievadiet modeļa nosaukumu. Nosaukumam jābūt unikālam visās jūsu organizācijas juridiskajās personām.
    - **Apraksts** – ievadiet modeļa aprakstu.
    - **Prioritātes aprēķina metode** – atlasiet vienu no šīm vērtībām:

        - *Prioritāšu diapazoni* – atlasot šo vērtību, kļūst **pieejama plānošanas prioritāšu diapazonu** režģis. Lai definētu plānošanas prioritātes vērtību, ir jāizveido vairāki prioritāšu diapazoni.
        - *Maksimālā krājumu daudzuma procenti* – aprēķiniet plānošanas prioritātes vērtību kā procentus, pamatojoties uz prognozēto krājumu līmeni virs maksimālā krājumu daudzuma.

    - **Plānotā pasūtījuma izveide** – šis lauks ir pieejams, ja prioritātes **aprēķina metodes lauks** ir iestatīts uz *Prioritātes diapazoni*. Atlasiet vienu no šīm vērtībām:

        - *Viena piegāde ar svarīgāko prioritāti* – nesadalīt plānotos pasūtījumus, pamatojoties uz prioritātes diapazonu. Plānotā pasūtījuma plānošanas prioritāte ir balstīta uz vissvarīgāko prioritātes diapazonu (t.i., zemāko plānošanas prioritātes vērtību).
        - *Sadalīt pēc prioritātes diapazoniem* – sadalīt pieprasījumu vairākos plānotos pasūtījumos, pamatojoties uz plānošanas prioritāšu diapazoniem. Atsevišķu plānoto pasūtījumu plānošanas prioritāti nosaka ar saistītā plānošanas prioritāšu diapazona plānošanas prioritāti.

    - **Apsveriet pieprasījuma** prioritāti – iestatiet šo opciju kā *Jā*, lai ierobežotu piegādei izveidotā jaunā plānotā pasūtījuma prioritāti. (Prioritāte nav zemāka par saistītās pieprasījuma prioritāti.) Iestatot šo opciju kā *Nē*, pieprasījuma pasūtījuma prioritāte netiks izskatīta, kad tiek aprēķināta piegādes pasūtījuma prioritāte.

1. Ja **prioritātes** *aprēķināšanas* **metodes lauku iestatāt uz Prioritātes diapazoni,** **·** **izmantojiet** pogas Pievienot un noņemt kopsavilkuma cilnes Plānošanas prioritāšu diapazoni rīkjoslā, lai pievienotu vai noņemtu prioritāšu diapazona rindas pēc vajadzības. Ja eksistē vairākas rindas un jūs ievietosiet jaunu rindu, plānošanas prioritāte automātiski tiks iestatīta uz atlasītās rindas vidējo vērtību un virs tās kārtas rindu. Katrā rindā iestatiet tālāk norādītos laukus:

    - **Plānošanas prioritāte** – ievadiet jebkuru vērtību no 0,00 līdz 100,00. Šī vērtība norāda plānošanas prioritāti, kas tiek izmantota rindai. Viszemākā prioritātes vērtība norāda augstāko prioritāti. Tiek piešķirta noklusējuma vērtība, bet to var mainīt pēc jūsu pieprasītā. Vienu plānošanas **prioritātes** vērtību vienā plānošanas prioritāšu modelī nevar izmantot vairākiem plānošanas prioritāšu diapazoniem.
    - **Apraksts** – ievadiet plānošanas prioritātes diapazona aprakstu (piemēram, Pasūtījuma *punkts uz Maksimumu*).
    - **No daudzuma** – apakšējā plānošanas prioritātes diapazona robeža. Šī vērtība ir tikai lasāma **un** **pamatota** uz iepriekšējās plānošanas prioritāšu diapazona vērtībām Līdz daudzumam un Procentos no daudzuma.
    - **Līdz daudzumam** – atlasiet lauku no krājuma seguma, kas jāizmanto, lai definētu diapazona augšējo robežu. Šīs vērtības tiek atbalstītas un ietekmēs **nākamā** diapazona vērtību No daudzuma:

        - *Nulle* – šī vērtība attēlo negatīvu līdz nulles diapazonam (*nulle vai mazāka līdz* nullei *·*). Rindām, kurās atlasīta šī vērtība, lauks **No** daudzuma procentos ir tikai lasāms un vienmēr tiek iestatīts uz *100* procentiem.
        - *Minimālais krājumu daudzums* – šī vērtība **parāda** minimālo vērtību krājumam vienību **vajadzību** lapā. Rindām, kur atlasīta šī vērtība, **lauks "No daudzuma" ir rediģējams un tiek** **izmantots, lai iestatītu nākamā diapazona vērtību No daudzuma (piemēram,** 80% no minimālā krājumu daudzuma *).*
        - *Pārkārtot* punktu – šī vērtība **parāda krājuma Pārkārtot** punkta vērtību krājumu **vajadzības** lapā. Rindām, kur ir atlasīta šī vērtība, **·** **lauks** "No daudzuma" ir rediģējams un tiek izmantots, lai iestatītu vērtību No daudzuma nākamajam diapazonam (piemēram, *80% no pasūtījuma punkta).*
        - *Maksimālais krājumu daudzums* – šī vērtība **parāda** maksimālo vērtību krājumam vienību **vajadzību** lapā. Rindām, kur atlasīta šī vērtība, **lauks "No daudzuma" ir rediģējams un tiek** **izmantots, lai iestatītu nākamā diapazona daudzumu No (piemēram,** 80% no minimālā krājumu daudzuma *).*
        - *Neierobežots* – šī vērtība attēlo bezgalīgu diapazona augšējo līmeni (*Neierobežots vai mazāks* līdz *Neierobežots*). Rindām, kurās atlasīta šī vērtība, lauks **No** daudzuma procentos ir tikai lasāms un vienmēr tiek iestatīts uz *100* procentiem.

    - **Procenti no līdz** daudzumam – ievadiet procentu vērtību, kas tiek izmantota, lai aprēķinātu plānošanas prioritātes diapazona augšējo robežu, pamatojoties uz vērtību, **kas atlasīta laukā Līdz daudzumam**. Piemēram, **·** *·* **·** *ja lauks Līdz daudzumam ir iestatīts uz Minimālais krājumu daudzums un lauks No daudzuma procentos ir iestatīts uz 50, augšējā robeža būs 50* procenti no minimālā krājumu daudzuma no saistītās krājumu vajadzības.

1. Kopsavilkuma cilnē **Plānošanas prioritātes noklusētie iestatījumi iestatiet laukus pēc pieprasījuma definēt noklusējuma plānošanas prioritātes katram piedāvājuma vai pieprasījuma rindas tipam (pārdošanas pasūtījums, pirkšanas pasūtījums, pārsūtīšanas pasūtījums** vai pieprasījuma apjoma prognoze). Var ievadīt tikai pozitīvas vērtības.

## <a name="view-and-maintain-planning-priority"></a>Skatīt un uzturēt plānošanas prioritāti

Plānošanas prioritāte tiek parādīta un iestatīta laukā **Plānošanas** prioritāte. Šo lauku varat atrast lapās, kas uzskaitītas šajā tabulā. Prioritāte tiek iestatīta kā skaitlis no 0 (nulle) līdz 100, kur 0 apzīmē augstāko svarīgumu.

| Lapa | Lauka atrašanās vieta | Vērtības avots |
|---|---|---|
| Pieprasījuma apjoma prognozes rindas | <p>**Cilne** Prece</p><p>(Augšējā sadaļā atlasiet rindu un pēc tam atlasiet **rindu Cilne** Prece.)</p> | Noklusētā vērtība vai vērtība, kas ir iestatīta manuāli |
| Pārdošanas pasūtījumu informācija | <p>**Cilne** Detalizētas informācijas par **rindu** kopsavilkuma cilnē Piegāde</p><p>(Atlasīt rindu **Kopsavilkuma cilnē Pārdošanas** pasūtījuma rindas un pēc tam **kopsavilkuma** cilnē Rindas informācija atlasiet **cilni** Piegāde.)</p> | Noklusētā vērtība, starpuzņēmumu vērtība vai manuāli iestatīta vērtība |
| Pirkšanas pasūtījuma dati | <p>**Cilne** Detalizētas informācijas par **rindu** kopsavilkuma cilnē Piegāde</p><p>(Atlasīt rindu **Kopsavilkuma cilnē Pirkšanas** pasūtījuma rindas un pēc tam **kopsavilkuma** cilnē Rindas informācija atlasiet **cilni** Piegāde.)</p> | Vērtība, kas iestatīta no plānotajiem pasūtījumiem, starpuzņēmuma vērtības vai manuāli iestatītas vērtības |
| Pārsūtīšanas pasūtījuma detaļas | <p>**Cilne** Detalizētas informācijas par **rindu** kopsavilkuma cilnē Piegāde</p><p>(Atlasīt rindu **Kopsavilkuma cilnē Pārsūtīšanas** pasūtījuma rindas un pēc tam **kopsavilkuma** cilnē Rindas informācija atlasiet **cilni** Piegāde.)</p> | Vērtība, kas apstiprināšanas laikā iestatīta no plānotajiem pasūtījumiem vai no manuāli iestatītās vērtības |
| Plānoto pasūtījumu informācija | **Vispārīgā** kopsavilkuma cilne | Vērtība, kas tiek aprēķināta vispārējās plānošanas laikā vai manuāli iestatītās vērtības laikā |

### <a name="intercompany-trade"></a>Starpuzņēmumu tirdzniecība

Plānošanas **prioritātes vērtība** starpuzņēmumu piedāvājuma un pieprasījuma rindās tiek koplietota starp saistītajiem elementiem. Modifikācija abās pusēs tiks parādīta saistītajā pasūtījuma rindā.

Daži piemēri:

- Lietotājs maina starpuzņēmumu pārdošanas pasūtījuma rindas plānošanas prioritāti no 20 uz 30. Šīs izmaiņas tiek atspoguļotas saistītajā starpuzņēmumu pirkšanas pasūtījuma rindā.
- Lietotājs maina starpuzņēmumu pirkšanas pasūtījuma rindas plānošanas prioritāti no 40 uz 50. Šīs izmaiņas tiek atspoguļotas saistītajā starpuzņēmumu pārdošanas pasūtījuma rindā.
