---
title: Ar ko izveido darba komponenti
description: "Šajā tēmā ir aprakstīts, konceptuāli elementi, ka darbu var iekļaut un sniegti piemēri par to, kā jūs varat izmantot šos elementus savā uzņēmumā."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Ar ko izveido darba komponenti

Šajā tēmā ir aprakstīts, konceptuāli elementi, ka darbu var iekļaut un sniegti piemēri par to, kā jūs varat izmantot šos elementus savā uzņēmumā. 

Pirms varat izveidot darbavietas, ir jāiestata daži uzziņu informāciju. Jūs varat izveidot darbu, kuram ir tikai nosaukums. Tomēr, ietverot papildu informāciju, piemēram, amatu, jūs sniedzat noklusētās vērtības pozīcijām, kas ir piešķirts darbam. Turklāt daži no jūsu ievadītos datus var izmantot, lai filtrētu kompensācijas plāniem konkrētiem darbiem. Ja jūs vēlaties, lai iestatītu tiesības, ko var izmantot, lai filtrētu kompensācijas plāniem konkrētu darbu, ieteicams iestatīt darba funkcijas un darbu veidiem pirms uzstādīšanas darbus. Kam šīs noklusētās vērtības, kas ir pieejami, jūs ietaupīsiet laiku, pievienojot darba pozīcijām. 

Daži darba detaļas, piemēram, darba nosaukums, tips un funkciju, ir spēkā stāšanās datums. Ja izveidotu darbu šodien, bet ne pievienot šos datus tikai vēlāk, un tad paskatās uz darbu radīšanas dienā, šie dati netiks rādītas. Tāpēc ieteicams izveidot dažus no šīs atsauces informāciju pirms to prasa. Tādā veidā varat pievienot informāciju jaunu darbavietu tos veidojot.

## <a name="job-titles"></a>Amatu nosaukumi
Pirms darbu izveidošanas ir jāiestata šo darbu amata nosaukumi. Amatiem tiek piešķirti to darbu amatu nosaukumi, ar kuriem šie amati ir saistīti. 

Uzturēt amatu nosaukumus, kas izmantojot **virsraksti** lapa, kuru var atvērt, izmantojot meklēšanas funkciju. Par * nosaukumi * * lapu, ievadiet nosaukumu, kuru plānojat izmantot savus darbus.

## <a name="job-types"></a>Darba tipi
Darbu tipus izmanto, lai grupētu līdzīgus darbus kategorijās. Darbu veidi nav nepieciešami. Tomēr, ja plānojat izmantot darbu tipus, kad iestatāt atlīdzību pārvaldības piemērotības nosacījumus, pirms darbu iestatīšanas ir jāiestata darbu tipi. Daži darba tipu piemēri ir pilna laika un nepilna darba laika, vai algu un stundas samaksas. Saglabātu darbu veidi, izmantojot **darba tipus** lapā. Par **darba tipus** lapu, ievadiet nosaukumu un īsu aprakstu par darba tipu. Šajā **atbrīvot statusa** lauku, atlasiet vienu no šīm opcijām, lai norādītu Fair Labor Standards Act (FLSA) atbrīvotas statusu darbus, kas ir šī uzdevuma tips:

-   **Reģistrācijas** – darbi tiek atbrīvoti no virsstundām saskaņā FLSA.
-   **Nav atbrīvoti,** -darbi netiek atbrīvoti no virsstundām saskaņā FLSA.
-   **Neattiecas** -FLSA segums nav piemērojams.

## <a name="job-functions"></a>Darba funkcijas
Darbs krustojumos raksturo augsta līmeņa funkcionālās kategorijās un augsta līmeņa nodokļi ir saistīti. Darba funkcijas nav nepieciešami. Darba funkcijas, kā arī darba veidus, var izmantot, lai filtrētu kompensācijas plāniem konkrētiem darbiem. Jūs saista darba funkcijas un darbu veidiem ar kompensācijas plāniem, izveidojot atbilstīguma noteikumi par **noteikumi par attaisnotiem izdevumiem** lapā. Kompensācijas plānu, kas attiecas uz konkrētu kombināciju darba tipu un darba funkcijas, ko definējāt caur atbilstības kārtulu var pievienot pēc tam kopa līmeņus. (Šie līdzekļi tiek piemēroti gan fiksēta kompensācija un mainīgās atlīdzības plānus.) Tomēr, ja jūs plānojat izmantot darba funkcijas, uzstādot atbilstīguma noteikumi par kompensāciju vadību, ieteicams iestatīt darba funkcijas pirms uzstādīšanas darbus. Tabulā ir norādīti daži piemēri darba funkcijas.

| Darbs           | Darba funkcija         |
|---------------|----------------------|
| Pārdošanas daļas vadītājs | Vidēja līmeņa vadītājs    |
| Grāmatvedis    | Speciālisti        |

Darba funkciju uzturēšanai, izmantojot **darba funkciju** lapā. Par **darba funkciju** lapu, ievadiet identifikācijas kodu un īsu aprakstu par darba funkcijas.

## <a name="job-tasks"></a>Darba uzdevumi
Darba uzdevumus apraksta pamata uzdevumus, kas jāveic darba ņēmējam, kurš ir novietots uz darbu. To pašu darbu uzdevumu var pievienot vairākus darbus, kā arī pozīcijas attiecībā uz darbiem, kas izmanto šo darba uzdevumu. Tabulā ir norādīti daži piemēri darba uzdevumus.

<table>
<thead>
<tr class="header">
<th>Darbs</th>
<th>Darba uzdevums</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pārdošanas daļas vadītājs</td>
<td><ul>
<li><strong>Perf pārskatīšanu</strong> – pārskatīt katra pārdevēja darba izpildi.</li>
<li><strong>ABS pārskats</strong> – apstiprināt vai noraidīt katra pārdevēja kavējuma pieprasījumus vai reģistrāciju.</li>
</ul></td>
</tr>
<tr class="even">
<td>Grāmatvedis</td>
<td><strong>FIN-atskaites</strong> – iknedēļas finanšu pārskati jāiesniedz galvenais finansu amatpersona.</td>
</tr>
</tbody>
</table>

Jums saglabāt darba uzdevumus, izmantojot **darba uzdevumus** lapā. Par **darba uzdevumus** lapu, ievadiet vārdu un darbu uzdevuma aprakstu. Šajā **Note** laukā, ja vēlaties, varat ievadīt papildu informāciju. Piezīmes var atjaunināt konkrēts darbs, nemainot atzīmē, ka ievadījāt šeit.

## <a name="areas-of-responsibility"></a>Atbildības jomas
Atbildības jomas var izmantot, lai norādītu, darba lomas, procesus un produktus, kas atbildīgs ir darba ņēmējs, kurš atrodas darba stāvoklī. Piemēram, darbs, kas saucas "Grāmatvedis", viena atbildības joma varētu būt "Finanšu atskaišu produktu." Uzturat atbildības jomas, izmantojot **atbildības jomas** lapu, kurā jūs varat atrast, izmantojot meklēšanas funkciju. Par **atbildības jomas** lapu, ievadiet nosaukumu un aprakstu par atbildību. Šajā **Note** laukā, ja vēlaties, varat ievadīt papildu informāciju. Piezīmes var atjaunināt konkrēts darbs, nemainot atzīmē, ka ievadījāt šeit.


