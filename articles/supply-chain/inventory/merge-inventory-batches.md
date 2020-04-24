---
title: Sapludināt krājumu partijas
description: Šajā rakstā ir sniegta informācija par to kā, konsolidēt divu vai vairāku krājumu partijas sapludinātā partijā.
author: pjacobse
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa571fb7392f6f7154f7f1bfd908e11e1bebd3a6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214186"
---
# <a name="merge-inventory-batches"></a>Sapludināt krājumu partijas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par to kā, konsolidēt divu vai vairāku krājumu partijas sapludinātā partijā.

Sapludinot partijas, aprēķini var palīdzēt optimizēt sapludinātās partijas raksturlielumus un partijas atribūtus. kad avota partijas ir atlasītas, sapludināto partiju pirms tās grāmatošanas var pārskatīt un mainīt. Partiju sapludināšanas datus var arī pārsūtīt uz krājumu žurnālu apstiprināšanai. Pēc tam krājumus var rezervēt vai grāmatot tieši no šī krājumu žurnāla. Grāmatojot sapludināto partiju, krājumi tiek pielāgoti avota partijām un sapludinātajai partijai.

## <a name="are-there-any-prerequisites"></a>Vai ir kādi priekšnosacījumi?
Jā, ir dažas lietas, kas ir jāiestata pirms varēs lietot partiju sapludināšanas rīkus. Tabulā ir sniegts šo priekšnosacījumu apraksts.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lapa</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Žurnālu nosaukumi, krājumi</td>
<td>Jums ir jāizveido žurnāla nosaukums ar tipu MK, kas tiek izmantots pēc noklusējuma, kad krājumu žurnālos grāmatojat partiju sapludināšanas. Papildu, bet ieteicama, darbība: var norādīt, ka rezervācijas jāveic automātiski, kad partiju sapludināšanas ieraksts tiek pārsūtīts uz krājumu žurnālu. Pretējā gadījumā pastāv risks, ka pēc partiju sapludināšanas datu iestatīšanas un iegrāmatošanas žurnālā tiek izmainīti rīcībā esošie krājumi. Lai žurnāla nosaukumam iespējotu automātiskās rezervācijas, laukā <strong><strong>Rezervācija</strong></strong> atlasiet opciju <strong>Automātiski</strong>.</td>
</tr>
<tr class="even">
<td>Krājumu un noliktavas vadības parametri</td>
<td>Ir jānorāda noklusētais krājumu žurnāla nosaukums.</td>
</tr>
<tr class="odd">
<td>Izlaistās preces</td>
<td>Tālāk ir norādīti krājuma ieteicamie iestatījumi.
<ul>
<li>Lai automātiski ģenerētu sapludināto partiju numurus, partiju numuru grupai ir jāpiešķir izlaistā prece. Partijas numuru var ievadīt manuāli, veidojot sapludinātu partiju vai atlasot esošo partijas numuru. Ja atlasāt esošu partijas numuru, pārliecinieties, vai atlasītā partija nav ietverta nevienā krājumu transakcijā.</li>
<li>Ja izlaistajai precei izmantojat glabāšanas laika vai derīguma termiņa datumus, sapludinātās partijas datumi tiek aprēķināti, pamatojoties uz laukā <strong>Partiju sapludināšanas datuma aprēķins</strong> atlasīto vērtību. Pieejamas šādas opcijas
<ul>
<li><strong>Tuvākais</strong> — aprēķini tiek veikti pēc partiju sapludināšanai atlasītajai avota partijai norādītā tuvākā datuma.</li>
<li><strong>Pēdējais</strong> — aprēķini tiek veikti pēc partiju sapludināšanai atlasītajai avota partijai norādītā pēdējā datuma.</li>
<li><strong>Manuāli</strong> — aprēķini netiek veikti. Ja visām avota partijām ir vienāds datums, datums tiek piedāvāts. Šo datumu var mainīt. Ja avota partiju datumi atšķiras, varat manuāli ievadīt datumu.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Partiju numuru grupa</td>
<td>Nav obligāti: lai ģenerētu partijas numuru, kad izveidojat sapludināto partiju, izlaistajai precei ir obligāti jāpiešķir partiju numuru grupa. Pretējā gadījumā partijas numuru var ievadīt manuāli.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Kad vajadzētu sapludināt krājumu partijas?
Tālāk kā piemēri ir aprakstīti daži scenāriji, kuros partiju sapludināšana varētu būt lietderīga.

-   Semijs iet pa noliktavu un pamana, ka noliktavā vairāku viena un tā paša krājuma partija ir nelielā daudzumā. Ir gaidāmas vairākas jaunas piegādes un viņš saprot, ka grīdas vietu var atbrīvot, sapludinot nesaistītus daudzumus jaunā partijā.
-   Semijs saņem krājumus un vēlas apvienot jaunu partiju ar citu jau saņemtu partiju, lai uzlabotu esošās partijas atribūta vērtību. Līdz ar to jūs izveidojat jaunu partiju.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Vai var sapludināt dažādās vietās esošas un dažādām juridiskām personām piederošas partijas?
Nē, sapludināt var tikai tās partijas, kuras atrodas vienā vietā, vienas noliktavas dimensijās un pieder vienai juridiskai personai. Tomēr sapludinātajai partijai var norādīt citu novietojumu un paletes ID.

## <a name="can-i-merge-partial-quantities"></a>Vai var sapludināt daļējus daudzumus?
Nē, sapludināt var tikai pilna daudzuma partijas. Partiju sapludināšanas funkcionalitāti ir paredzēts izmantot kā krājumu apstrādes līdzekli, nevis ražošanas līdzekli.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Ko darīt, ja partijām ir dažādas partijas atribūtu vērtības?
Kad atlasāt avota partijas, kuras vēlaties apvienot sapludinātajā partijā, programmatūra Supply Chain Management pārbauda, vai visām partijām ir raksturlielumi vai atribūtu vērtības. Ja atribūta vērtības ir vienādas, sapludinātajai partijai tiek piedāvāta vērtība. Šo vērtību var mainīt. To atribūtu vērtību lauki, kuras sapludinātajai partijai atšķiras, tiek atstāti neaizpildīti, un šīs vērtības var ievadīt manuāli. Ja partijas atribūta vērtības veids ir vesels skaitlis vai daļskaitlis un vērtības visās avota partijās atšķiras, vērtība tiek aprēķināta, izmantojot svērtā vidējā aprēķināšanu. Aprēķinātā vērtība tiek noapaļota uz augšu vai uz leju uz tuvāko soļa vērtību. Ja avota partijas vērtības lauks ir tukšs, partija un tās daudzums aprēķinā netiek iekļauts. **Piemērs.** Turpmākajā piemērā ir norādīta sapludinātās partijas svērtā vidējā aprēķināšana. Divām avota partijām nav norādīta partijas atribūta veida vērtība, kura ir vesels skaitlis. Šāds atribūts ir piešķirts avota partijām.

| Atribūts | Minimums | Solis | Maksimums |
|-----------|---------|-----------|---------|
| Līmenis     | 3       | 3         | 30      |

Avota partijām ir tālāk minētās partijas atribūta **Līmeņa partija** vērtības.

| Partija | Daudzums | Atribūts | Atribūta vērtība |
|-------|----------|-----------|-----------------|
| B1    | 10.       | Līmenis     | Tukšs           |
| B2    | 15.       | Līmenis     | 15.              |
| B3    | 20.       | Līmenis     | 20.              |
| B4    | 25       | Līmenis     | Tukšs           |
| B5    | 30       | Līmenis     | 25              |

Pievienojot šīs partijas kā avota partijas, sapludinātajai partijai tiek piešķirtas tālāk minētās vērtības.

| Partija | Daudzums | Atribūts | Atribūta vērtība |
|-------|----------|-----------|-----------------|
| B6    | 100      | Līmenis     | 21              |

Partijas B1 un B4 vērtības un daudzumi netiek iekļauti svērtā vidējā aprēķināšanā. Tāpēc sapludinātās partijas vērtība tiek aprēķināta tālāk norādītajā veidā.

| Vērtība | Daudzums (svars)                              | Relatīvais svars | Relatīvais svars x vērtība                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15.    | 15.                                             | 0,230769231     | 3,461538462                                                           |
| 20.    | 20.                                             | 0,307692308     | 6,153846154                                                           |
| 25    | 30                                             | 0,461538462     | 11,53846154                                                           |
|       | **Kopsumma:** 65, kas ir svaru summa |                 | **Kopsumma:** 21,5384615, kas tiek noapaļota līdz 21 (tuvākā soļa vērtība) |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Ko darīt, ja partijām ir dažādi partijas datumi?
Ja partijām ir atšķirīgi partijas datumi, daži datumi tiek aprēķināti pēc vērtībām lapas **Partiju sapludināšana** kopsavilkuma cilnes **Sapludināta partija** grupā **Partijas datums**. Sistēmā tiek aprēķinātas vērtības grupas **Partijas datums** laukiem. Šīs vērtības ietver ražošanas, beigu, glabāšanas laika pārbaudes un derīguma termiņa datumus. Datumi tiek aprēķināti atbilstoši krājuma iestatījumiem lapas **Detalizēta informācija par izlaistajām precēm** lauku grupā **Krājuma dati**. Vērtības var mainīt vai ievadīt manuāli. Nekādiem citiem datumiem aprēķini netiek veikti. Tāds pats princips tiek izmantots partijas atribūtu vērtībām. Ja visām avota partijām ir vienāds datums, šis datums tiek piedāvāts sapludinātajai partijai. Ja datums visām avota partijām atšķiras, sapludinātajai partijai datums netiek norādīts un to var ievadīt manuāli.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Ko darīt, ja partijām, kuras vēlos sapludināt, atšķiras dimensijas?
Ar preču, izsekošanas un noliktavas dimensijas apstrādā tālāk aprakstītajā veidā.

-   **Preces dimensijas** — visām atlasītā krājuma preces dimensijām jābūt vienādam. Nevar sapludināt partijas ar dažādām preces dimensijām.
-   **Izsekošanas dimensijas** — ja krājumam ir norādīta partiju numuru grupa, automātiski tiek ģenerēts jauns partijas numurs. Ja krājumam nav piešķirta partijas numura grupa, esošo partiju atlasīt vai numuru ievadīt var manuāli. Sērijas numuri tiek pārsūtīti no avota partijas uz sapludinātās partijas krājumu žurnāla rindām.
-   **Noliktavas dimensijas** — vietas un noliktavas dimensijām jābūt vienādām visām avota partijām un sapludinātajai partijai. Tomēr sapludinātajai partijai var norādīt jaunu novietojumu un paletes ID.

## <a name="how-does-posting-work"></a>Kā notiek grāmatošana?
Grāmatošana tiek veikta divējādi atkarībā no tā, vai tiek izmantots žurnāliem paredzēts apstiprināšanas process. Var izmantot darbību **Pārsūtīt uz žurnālu** un **Grāmatot partiju sapludināšanu**, lai pārsūtītu ierakstu par partiju sapludināšanu uz žurnālu, kur to var pārbaudīt un iegrāmatot, vai arī partiju sapludināšanu var iegrāmatot tieši. Galvenā atšķirība starp šīm divām darbībām ir tā, ka, veicot pārsūtīšanu uz žurnālu, partijas sapludināšana netiek iegrāmatota. Ar abām šīm darbībām tiek izveidota jauna partija, ja nav atlasīta esošā partija, tiek atjaunināta visa partijas informācija un atribūtu vērtības un tiek izveidots krājumu žurnāls.

-   **Pārsūtīt uz žurnālu** — pārsūtīt informāciju par partiju sapludināšanu uz jaunu krājumu žurnālu. Ja ir iestatīta automātisko rezervāciju opcija, avota partiju daudzumi tiek rezervēti. Partiju sapludināšanas datus nevar mainīt. Lai varētu mainīt partijas sapludināšanu, ir jāizdzēš žurnāls. Žurnālu var izmantot kā uzdevumu, ko citam darbiniekam jāizpilda vēlāk. Partijas daudzuma rezervēšana žurnāla rindā ir nodrošināta. Šis sadalījums ļauj kvalitātes plānotājam vai noliktavas pārvaldniekam izveidot uzdevumus saviem darbiniekiem.
-   **Grāmatot partiju sapludināšanu** — grāmatot partiju sapludināšanas tieši. Šo darbību var veikt, kad ir pabeigta fiziska sapludināšana.

Partiju sapludināšanas krājumu žurnālu var apstiprināt saraksta lapā **Visu partiju sapludināšanas**. Noklikšķiniet uz **Žurnāls** &gt; **Grāmatot**. Kad žurnāla dati ir iegrāmatoti, detalizēto informāciju par sapludināto partiju mainīt nevar. Pēc ieraksta par partiju sapludināšanu pārsūtīšanas uz krājumu žurnālu, informāciju var mainīt tikai, ja žurnāls tiek izdzēsts.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Kāpēc pēc krājuma ar pieļaujamo svaru sapludināšanas krājumu žurnālā netiek rādīta informāciju par pieļaujamo svaru?
Krājumus ar pieļaujamo svaru var sapludināt līdzīgi kā citus krājumus. Tomēr informācija par pieļaujamo svaru krājumu žurnālā nav redzama. Informāciju par pieļaujamo svaru ieteicams pārbaudīt pirms ieraksta par partiju sapludināšanu pārsūtīšanas uz krājumu žurnālu.
