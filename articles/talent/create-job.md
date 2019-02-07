---
title: "Darba komponentu iestatīšana"
description: "Šajā tēmā ir aprakstīti konceptuālie elementi, kas var būt iekļauti darbā, un sniegti piemēri par to, kā šos elementus varat lietot savā organizācijā."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: b40b81fc24086e73b54cfe0cb5e6a81ec5838ab5
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="set-up-the-components-of-a-job"></a>Darba komponentu iestatīšana

[!include [banner](includes/banner.md)]


Šajā tēmā ir aprakstīti konceptuālie elementi, kas var būt iekļauti darbā, un sniegti piemēri par to, kā šos elementus varat lietot savā organizācijā. 

Pirms izveidojat darbus, ir jāiestata noteikta atsauces informācija. Varat izveidot darbu, kam ir tikai nosaukums. Taču, ja iekļaujat papildinformāciju, piemēram, darba amatu, tad šim darbam piešķirtajiem amatiem varat nodrošināt noklusējuma vērtības. Turklāt noteiktu ievadīto informāciju var izmantot atlīdzības plānu filtrēšanai konkrētiem darbiem. Ja vēlaties iestatīt piemērotību, kuru varat lietot, lai atlīdzības plānus filtrētu konkrētam darbam, tad pirms darbu iestatīšanas ir jāiestata darbu funkcijas un darbu tipi. Ja ir pieejamas šīs noklusējuma vērtības, jūs ietaupāt laiku, kad darbam pievienojat amatus. 

Noteikta darba informācija, piemēram, darba amats, tips un funkcija, ir ar spēkā stāšanās datumu. Ja darbu izveidojat šodien, bet šo informāciju pievienojat tikai vēlāk, un pēc tam uz šo darbu skatāties tā izveidošanas datumā, šī informācija nav redzama. Tādēļ noteikta atsauces informācija ir jāizveido, vēl pirms tā ir nepieciešama. Šādi šo informāciju varat pievienot jauniem darbiem, kad tos izveidojat.

## <a name="job-titles"></a>Darbu amati
Pirms darbu izveidošanas ir jāiestata šo darbu amata nosaukumi. Amatiem tiek piešķirti to darbu amatu nosaukumi, ar kuriem šie amati ir saistīti. 

Darbu amati ir jāuztur, izmantojot lapu **Amati**, kuru varat atvērt, izmantojot funkciju Meklēt. Lapā **Amati** ievadiet amatus, kurus plānojat izmantot saviem darbiem.

## <a name="job-types"></a>Darbu tipi
Darbu tipi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās. Darbu tipi nav obligāti. Tomēr, ja plānojat izmantot darbu tipus, kad iestatāt atlīdzību pārvaldības piemērotības nosacījumus, pirms darbu iestatīšanas ir jāiestata darbu tipi. Daži darbu tipu piemēri ir pilna laika un nepilna laika, vai algots un stundu apmaksa. Darbu tipi tiek uzturēti lapā **Darbu tipi**. Lapā **Darbu tipi** ievadiet darbu tipa nosaukumu un īsu aprakstu. Laukā **Atbrīvojuma statuss** atlasiet vienu no tālāk norādītajām opcijām, lai norādītu Godīga darba standartu akta (Fair Labor Standards Act — FLSA) atbrīvojuma statusu darbiem, kam ir tālāk norādītais darba tips.

-   **Atbrīvojums** — darbi ir atbrīvoti no virsstundām saskaņā ar FLSA.
-   **Bez atbrīvojuma** — darbi nav atbrīvoti no virsstundām saskaņā ar FLSA.
-   **Nav piemērojams** — FLSA segums nav piemērojams.

## <a name="job-functions"></a>Darba funkcijas
Darba funkcijas apraksta augsta līmeņa funkcionālās kategorijas un attiecas uz augsta līmeņa pienākumiem. Darba funkcijas nav obligātas. Darba funkcijas varat lietot kopā ar darbu tipiem, lai filtrētu atlīdzību plānus noteiktiem darbiem. Darba funkcijas un darbu tipus varat saistīt ar atlīdzību plāniem, iestatot piemērotības kārtulas lapā **Piemērotības kārtulas**. Pēc tam varat pievienot līmeņu komplektu atlīdzību plānam, kurš attiecas uz noteiktu darba tipa un darba funkcijas kombināciju, kuru definējāt, izmantojot piemērotības kārtulu. (Šie līdzekļi attiecas gan uz fiksētās atlīdzības plāniem, gan uz mainīgās atlīdzības plāniem.) Taču, ja atlīdzību pārvaldības piemērotības kārtulu iestatīšanas laikā plānojat izmantot darba funkcijas, tad darba funkcijas ir jāiestata pirms darbu iestatīšanas. Nākamajā tabulā ir parādīti daži darba funkciju piemēri.

| Darbs           | Darba funkcija         |
|---------------|----------------------|
| Pārdošanas daļas vadītājs | Vidēja līmeņa vadītājs    |
| Grāmatvedis    | Speciālisti        |

Darba funkcijas tiek uzturētas lapā **Darba funkcijas**. Lapā **Darba funkcijas** ievadiet identifikācijas kodu un īsu aprakstu par attiecīgo darba funkciju.

## <a name="job-tasks"></a>Darba uzdevumi
Darba uzdevumi apraksta pamata uzdevumus, kuri ir jāveic darbiniekam, kas ieņem šo amatu. Vienu un to pašu darba uzdevumu var pievienot vairākiem darbiem, kā arī tādiem darbu amatiem, kas izmanto šos darba uzdevumus. Nākamajā tabulā ir parādīti daži darba uzdevumu piemēri.

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
<li><strong>Izpildes novērtēšana</strong> — novērtēt katra pārdevēja darba izpildi.</li>
<li><strong>Kavējumu izskatīšana</strong> — apstiprināt vai noraidīt katra pārdevēja kavējumu pieprasījumus vai reģistrācijas.</li>
</ul></td>
</tr>
<tr class="even">
<td>Grāmatvedis</td>
<td><strong>Finanšu pārskata sniegšana</strong> — sniegt iknedēļas finanšu pārskatus finanšu direktoram.</td>
</tr>
</tbody>
</table>

Darba uzdevumi tiek uzturēti lapā **Darba uzdevumi**. Lapā **Darba uzdevumi** ievadiet darba uzdevuma nosaukumu un īsu aprakstu. Laukā **Piezīme** varat pievienot papildinformāciju, ja vēlaties. Konkrētam darbam piezīmes var atjaunināt, nemainot šeit ievadītās piezīmes.

## <a name="areas-of-responsibility"></a>Atbildības jomas
Atbildības jomas ir jāizmanto, lai norādītu darba lomas, procesus un preces, par ko ir atbildīgs darbinieks, kurš ieņem šo amatu. Piemēram, darbam ar nosaukumu “Grāmatvedis” viena atbildības joma varētu būt “Finanšu pārskatu izveide par preci A”. Atbildības jomas ir jāuztur, izmantojot lapu **Atbildības jomas**, kuru varat atrast, izmantojot funkciju Meklēt. Lapā **Atbildības jomas** ievadiet atbildības nosaukumu un aprakstu. Laukā **Piezīme** varat pievienot papildinformāciju, ja vēlaties. Konkrētam darbam piezīmes var atjaunināt, nemainot šeit ievadītās piezīmes.

## <a name="steps-for-creating-a-job"></a>Norādījumi par darba izveidi
Sīku jaunas darba izveides procedūras aprakstu skatiet tēmā [Jaunu darbu definēšana](../fin-and-ops/hr/tasks/define-new-jobs.md). 

