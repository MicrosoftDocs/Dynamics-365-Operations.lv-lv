---
title: Darba komponentu iestatīšana
description: Šajā rakstā ir aprakstīti konceptuālie elementi, kas var būt iekļauti darbā, un sniegti piemēri par to, kā šos elementus varat lietot savā organizācijā.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace, HCMJobFamily
audience: Application User
ms.author: twheeloc
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: afe100879a4f83e4ef16048bc4b1acace19b679b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877719"
---
# <a name="set-up-the-components-of-a-job"></a>Darba komponentu iestatīšana


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīti konceptuālie elementi, kas var būt iekļauti darbā, un sniegti piemēri par to, kā šos elementus varat lietot savā organizācijā. 

Pirms izveidojat darbus, ir jāiestata noteikta atsauces informācija. Varat izveidot darbu, kam ir tikai nosaukums. Taču, ja iekļaujat papildinformāciju, piemēram, darba amatu, tad šim darbam piešķirtajiem amatiem varat nodrošināt noklusējuma vērtības. Turklāt noteiktu ievadīto informāciju var izmantot atlīdzības plānu filtrēšanai konkrētiem darbiem. Ja vēlaties iestatīt piemērotību, kuru varat lietot, lai atlīdzības plānus filtrētu konkrētam darbam, tad pirms darbu iestatīšanas ir jāiestata darbu funkcijas un darbu tipi. Ja ir pieejamas šīs noklusējuma vērtības, jūs ietaupāt laiku, kad darbam pievienojat amatus. 

Noteikta darba informācija, piemēram, darba amats, tips un funkcija, ir ar spēkā stāšanās datumu. Ja darbu izveidojat šodien, bet šo informāciju pievienojat tikai vēlāk, un pēc tam uz šo darbu skatāties tā izveidošanas datumā, šī informācija nav redzama. Tādēļ noteikta atsauces informācija ir jāizveido, vēl pirms tā ir nepieciešama. Šādi šo informāciju varat pievienot jauniem darbiem, kad tos izveidojat.

## <a name="job-titles"></a>Darbu amati
Pirms darbu izveidošanas ir jāiestata šo darbu amata nosaukumi. Amatiem tiek piešķirti to darbu amatu nosaukumi, ar kuriem šie amati ir saistīti. 

Darbu amati ir jāuztur, izmantojot lapu **Amati**, kuru varat atvērt, izmantojot funkciju Meklēt. Lapā **Amati** ievadiet amatus, kurus plānojat izmantot saviem darbiem.

## <a name="job-types"></a>Darba tipi
Darbu tipi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās. Darbu tipi nav obligāti. Tomēr, ja plānojat izmantot darbu tipus, kad iestatāt atlīdzību pārvaldības piemērotības nosacījumus, pirms darbu iestatīšanas ir jāiestata darbu tipi. Daži darbu tipu piemēri ir pilna laika un nepilna laika, vai algots un stundu apmaksa. Darbu tipi tiek uzturēti lapā **Darbu tipi**. Lapā **Darbu tipi** ievadiet darbu tipa nosaukumu un īsu aprakstu. Laukā **Atbrīvojuma statuss** atlasiet vienu no tālāk norādītajām opcijām, lai norādītu Godīga darba standartu akta (Fair Labor Standards Act — FLSA) atbrīvojuma statusu darbiem, kam ir tālāk norādītais darba tips.

-   **Atbrīvojums** — darbi ir atbrīvoti no virsstundām saskaņā ar FLSA.
-   **Bez atbrīvojuma** — darbi nav atbrīvoti no virsstundām saskaņā ar FLSA.
-   **Nav piemērojams** — FLSA segums nav piemērojams.

## <a name="job-family"></a>Amatu saime
Darba saime ir darbu grupa, kurā ir iesaistīts līdzīgs darbs un kam nepieciešama līdzīga apmācība, prasmes, zināšanas un kompetence. Darbu saime var būt saistīta ar darbu lapas **Darbi** kopsavilkuma cilnē **Darbu klasifikācija** un lapas **Visi amati** kopsavilkuma cilnē **Vispārīgi**. Darba saimes var būt plašas vai specifiskas, atkarībā no jūsu uzņēmējdarbības un pārskatu sniegšanas prasībām. Daži plašas darba saimes piemēri ir **Kvalificēts darbaspēks** un **Nekvalificēts darbaspēks**. Daži atsevišķas darba saimes piemēri ir **Grāmatvedība**, **Ražošana**  un **Pārdošana**.

Darbu saimes ir jāuztur, izmantojot lapu **Darba saime**, kuru varat atvērt, izmantojot meklēšanas funkciju. Lapā **Darbu saime** ievadiet unikālu ģimenes nosaukumu un ievadiet detalizētu aprakstu, ko plānojat izmantot darbiem.

## <a name="job-functions"></a>Darba funkcijas
Darba funkcijas apraksta augsta līmeņa funkcionālās kategorijas un attiecas uz augsta līmeņa pienākumiem. Darba funkcijas nav obligātas. Darba funkcijas varat lietot kopā ar darbu tipiem, lai filtrētu atlīdzību plānus noteiktiem darbiem. Darba funkcijas un darbu tipus varat saistīt ar atlīdzību plāniem, iestatot piemērotības kārtulas lapā **Piemērotības kārtulas**. Pēc tam varat pievienot līmeņu komplektu atlīdzību plānam, kurš attiecas uz noteiktu darba tipa un darba funkcijas kombināciju, kuru definējāt, izmantojot piemērotības kārtulu. (Šie līdzekļi attiecas gan uz fiksētās atlīdzības plāniem, gan uz mainīgās atlīdzības plāniem.) Taču, ja atlīdzību pārvaldības piemērotības kārtulu iestatīšanas laikā plānojat izmantot darba funkcijas, tad darba funkcijas ir jāiestata pirms darbu iestatīšanas. Nākamajā tabulā ir parādīti daži darba funkciju piemēri.

| Darbs           | Darba funkcija         |
|---------------|----------------------|
| Pārdošanas daļas vadītājs | Vidēja līmeņa vadītājs    |
| Grāmatvedis    | Speciālisti        |

Darba funkcijas tiek uzturētas lapā **Darba funkcijas**. Lapā **Darba funkcijas** ievadiet identifikācijas kodu un īsu aprakstu par attiecīgo darba funkciju.

## <a name="compensation"></a>Kompensācija
Lai piešķirtu fiksētās atlīdzības sistēmu darbiniekam, kuram ir amats darbā, jums darbam jāiestata atlīdzības līmeņi. Kompensācijas **līmenis tiek izmantots**, kad minimālās, vidējā darba un maksimālās summas ir iestatītas kompensācijas struktūrā (kompensācijas režģis). Kad tiek izveidots fiksētās atlīdzības plāns, tiek atlasīta kompensācijas struktūra. Kompensācijas struktūra ietver arī kompensācijas līmeni. Kad darbiniekam atlasāt fiksētās atlīdzības sistēmu, atlasei pieejamie atlīdzības līmeņi ir atkarīgi no darba, ar kuru ir saistīts darbinieka amats. Papildinformāciju par to, kā iestatit atlīdzību skatiet [Atlīdzības plāni](hr-compensation-overview.md).

## <a name="job-skills"></a>Darba prasmes
Darba prasmes apraksta prasmes, kas nepieciešamas darba veikšanai. Prasmju līmenis jāsaista ar visām darba prasmēm. Prasmju līmeņi ir lietotāja definēti. Tie norāda prasmju vai prasmes līmeni, kas nepieciešams prasmei. Piemēram, uzņēmumi var iestatīt skaitliskus līmeņus, piemēram, 1 līdz 5, kur **1** norāda darbību un **5** apzīmē ekspertu. Alternatīvi uzņēmumi var iestatīt līmeņus, kas atzīmēti kā **Iesācējs**, **Vidējais** vai **Eksperts**. Pēc prasmju līmeņa iestatīšanas var tikt iestatīts arī šīs prasmes svarīgums. Piemēram, ja grāmatvedim nepieciešamas stipras Microsoft Excel zināšanas, var tikt izveidotas prasmes ar nosaukumu **Excel zināšanas**. Pēc tam prasmju līmeni var iestatīt uz **Vidējais**, un svarīgumu var iestatīt uz **Vairums**.

Darbam izmantotās prasmes var izmantot prasmju kartēšanā. Prasmju kartēšana var salīdzināt prasmju kopu, kas nepieciešama darbam, un prasmes, kas saistītas ar darbinieku. Pēc tam tā var noteikt atbilstību procentos, pamatojoties uz prasmju pārklāšanos. Papildinformāciju par prasmju kartēšanu skatiet sadaļā [Prasmju konfigurēšana](hr-develop-skills.md). 

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
<li><strong>Izpildes novērtēšana</strong> — novērtēt katra pārdevēja&#39;darba izpildi.</li>
<li><strong>Kavējumu izskatīšana</strong> — apstiprināt vai noraidīt katra pārdevēja&#39;kavējumu pieprasījumus vai reģistrācijas.</li>
</ul></td>
</tr>
<tr class="even">
<td>Grāmatvedis</td>
<td><strong>Finanšu pārskata sniegšana</strong> — sniegt iknedēļas finanšu pārskatus finanšu direktoram.</td>
</tr>
</tbody>
</table>

Darba uzdevumi tiek uzturēti lapā **Darba uzdevumi**. Lapā **Darba uzdevumi** ievadiet darba uzdevuma nosaukumu un īsu aprakstu. Laukā **Piezīme** varat pievienot papildinformāciju, ja vēlaties. Konkrētam darbam piezīmes var atjaunināt, nemainot šeit ievadītās piezīmes.

## <a name="areas-of-responsibility"></a>Atbildības jomas
Atbildības jomas ir jāizmanto, lai norādītu darba lomas, procesus un preces, par ko ir atbildīgs darbinieks, kurš ieņem šo amatu. Piemēram, darbam ar nosaukumu “Grāmatvedis” viena atbildības joma varētu būt “Finanšu pārskatu izveide par preci A”. Atbildības jomas ir jāuztur, izmantojot lapu **Atbildības jomas**, kuru varat atrast, izmantojot funkciju Meklēt. Lapā **Atbildības jomas** ievadiet atbildības nosaukumu un aprakstu. Laukā **Piezīme** varat pievienot papildinformāciju, ja vēlaties. Konkrētam darbam piezīmes var atjaunināt, nemainot šeit ievadītās piezīmes.

## <a name="steps-for-creating-a-job"></a>Norādījumi par darba izveidi
Sīku jaunas darba izveides procedūras aprakstu skatiet rakstā [Jaunu darbu definēšana](./hr-personnel-define-jobs.md). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
