---
title: Pārskats par preču konfigurācijas modeļiem
description: Šajā rakstā ir definēti termini un koncepcijas, kas ir saistīti ar preču konfigurācijas modeļiem. Preču konfigurācijas modeļi sniedz iespēju veidot iekšējo preču struktūru, ko var izmantot, lai konfigurētu daudzus vienas preces variantus.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage, PCModalWaitDialog, PCTemplateConfigurationManager, PCConfigurationUIGrouping
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ee8d70e8d7c11513ff067847577285f10bb9bcb
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887220"
---
# <a name="product-configuration-models-overview"></a>Pārskats par preču konfigurācijas modeļiem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir definēti termini un koncepcijas, kas ir saistīti ar preču konfigurācijas modeļiem. Preču konfigurācijas modeļi sniedz iespēju veidot iekšējo preču struktūru, ko var izmantot, lai konfigurētu daudzus vienas preces variantus.

Preču konfigurācijas modeļi tiek veidoti, lai pārstāvētu vispārīgu preču struktūru. Kad ir iestatīts kāds preču konfigurācijas modelis, varat konfigurēt atšķirīgu preces variantu, kam ir unikāls materiālu komplekts (MK) un unikāls maršruts. Lai izpildītu relācijas un ierobežojumus starp dažādiem preces variantiem, preču konfigurācijas modeļiem tiek izmantoti gan deklaratīvie ierobežojumi, gan obligātie aprēķini. Jūs varat konfigurēt krājumus pārdošanas pasūtījumos, pārdošanas piedāvājumos, pirkšanas pasūtījumos un ražošanas pasūtījumos. Nākamajā tabulā ir aprakstīti tabulas ierobežojumu termini un jēdzieni.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Komponenti</td>
<td>Komponenti ir preču konfigurācijas modeļa galvenie veidošanas bloki. Komponenti tiek rādīti koka struktūrā, lapā <strong>Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli</strong>. Komponenti var ietvert šādus elementus:
<ul>
<li>Atribūti</li>
<li>Ierobežojumi</li>
<li>Aprēķini</li>
<li>Apakškomponenti</li>
<li>Lietotāju prasības</li>
<li>MK rindas</li>
<li>Maršruta operācijas</li>
</ul></td>
</tr>
<tr class="even">
<td>Atribūti</td>
<td>Atribūti apraksta visus preču konfigurācijas modeļa līdzekļus. Atribūtus var izmantot, lai norādītu līdzekļus, ko var atlasīt konfigurējot atšķirīgu preci. Atribūti tiek izmantoti, ievērojot ierobežojumus un nosacījumus. Ja atribūti tiek izveidoti un pievienoti preces konfigurācijas modelim, saistītie atribūtu veidi tiek norādīti ar atsaucēm. Atribūtam var iestatīt noklusējuma vērtību. Konfigurācijas lietotāja interfeisā (UI) tiek izmantota noklusējuma vērtība, konfigurējot preču konfigurācijas modeli. Varat norādīt, ka atribūts ir obligāts, tikai lasāms vai slēpts.
<ul>
<li><strong>Obligāts</strong> — konfigurējot preci, šim atribūtam ir jāiestata kāda vērtība.</li>
<li><strong>Tikai lasāms</strong> — atribūta vērtība tiek rādīta konfigurācijas sesijas laikā, taču to nevar mainīt.</li>
<li><strong>Paslēpts</strong> — atribūta vērtība ir iekļauta ierobežojumos un nosacījumos, taču netiek rādīta konfigurācijas sesijas laikā.</li>
</ul>
Varat norādīt arī atribūtu nosacījumu. Ja nosacījums tiek izpildīts, obligātajam atribūtam ir jāievada vērtība. Nosacījumi ir izteiksmes, kas jāievēro tajos atribūtos, MK rindās un maršruta operācijās, kas tiks iekļautas preču konfigurācijas modelī. Jebkurš atribūts, uz kuru ir izveidota atsauce nosacījumā, kļūst obligāts. Iesakām cilnē <strong>Atribūti</strong> atribūtus atlasīt kā obligātus. Tas var atvieglot obligāto atribūtu identificēšanu. Atribūtu vērtības ir atkārtoti izmantojamo konfigurāciju svarīga daļa. Sistēma izmanto atribūtu vērtības, lai noteiktu, vai pastāv konfigurācija, kas atbilst lietotāja veiktajai atlasei konfigurācijas sesijas laikā.</td>
</tr>
<tr class="odd">
<td>Atribūtu tipi</td>
<td>Atribūta tipi nosaka datu tipu kopu atribūtiem, kas tiek izmantoti preču konfigurācijas modelī. Tiek izmantoti šādi atribūtu veidi:
<ul>
<li><strong>Vesels skaitlis</strong> ar diapazonu vai bez tā</li>
<li><strong>Decimāls</strong></li>
<li><strong>Teksts</strong> ar fiksētu sarakstu vai bez tā</li>
<li><strong>Būla</strong></li>
</ul>
Ja atribūta tips ir <strong>Būla</strong>, <strong>Vesels skaitlis</strong> ar diapazonu vai <strong>Teksts</strong> ar fiksētu sarakstu, tad šī vērtību kopa ir pieejama, kad ir iestatīts preces konfigurācijas modelis. <strong>Piezīme.</strong> Preču konfigurācijas risinātājs atpazīst tikai šādus atribūtu tipus: <strong>Būla</strong>, <strong>Teksts</strong> ar fiksētu sarakstu un <strong>Vesels skaitlis</strong> ar diapazonu. Tāpēc tikai šos atribūtu veidus var izmantot izteiksmju ierobežojumos un nosacījumos.</td>
</tr>
<tr class="even">
<td>Ierobežojumi</td>
<td>Ierobežojumi apraksta preču modeļa konfigurācijas ierobežojumus. Ierobežojumi tiek izmantoti, lai garantētu, ka preces konfigurēšanas laikā tiek atlasītas tikai derīgas vērtības. Ierobežojumi var būt izteiksmes ierobežojumi vai tabulas ierobežojumi:
<ul>
<li>Izteiksmes ierobežojumus var izmantot tikai tam komponentam, kuram tie ir piesaistīti. Komponenta izteiksmes ierobežojumos var tikt izmantota atsauce uz komponenta apakškomponentu atribūtiem. Preču konfigurācijas risinātājs tiek izmantots, lai atrisinātu ierobežojumus, un ierobežojumu rakstīšanas laikā jums ir jālieto risinātāja sintakse. Plašāku informāciju skatiet tēmas vietnē par izteiksmes ierobežojumiem un tabulas ierobežojumiem.</li>
<li>Lai preces konfigurācijas modeļa komponentam varētu lieto tabulas ierobežojumus, tie vispirms ir jādefinē. Tabulas ierobežojumi var būt lietotāja definēti vai sistēmas definēti. Lietotāja definēts tabulas ierobežojums ir tādas matricas veids, ko var izmantot, lai aprakstītu tādu atribūtu vērtību kombināciju kopas, ko definē atribūtu veidi. Piemēram, ja tiek ražoti skaļruņi, tad lietotāja definēta tabulas ierobežojuma matricā var būt kolonnas skaļruņu apdarei un režģim.</li>
</ul>
<strong>Piemērs.</strong> Skaļruņi ir pieejami ar četrām apdarēm: Melns, Ozola, Rožkoka un Balts. Skaļruņiem var būt viens no trim priekšējiem režģiem: Melns, Metāla vai Balts. Melnā apdare ir pieejama visiem režģiem, bet pārējās apdares ir pieejamas tikai noteiktiem režģiem. Nākamajā tabulā ir parādīts piemērs, kāda informācija tiek rādīta cilnē <strong>Atļautās kombinācijas</strong>, lapā <strong>Rediģēt tabulas ierobežojumu</strong>.
<table>
<thead>
<tr class="header">
<th>Korpusa apdare</th>
<th>Priekšējais režģis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Melns</td>
<td>Melns</td>
</tr>
<tr class="even">
<td>Melns</td>
<td>Metāla</td>
</tr>
<tr class="odd">
<td>Melns</td>
<td>Balts</td>
</tr>
<tr class="even">
<td>Ozola</td>
<td>Melns</td>
</tr>
<tr class="odd">
<td>Rožkoka</td>
<td>Balts</td>
</tr>
<tr class="even">
<td>Balts</td>
<td>Melns</td>
</tr>
<tr class="odd">
<td>Balts</td>
<td>Balts</td>
</tr>
</tbody>
</table>
Sistēmas definēts tabulas ierobežojums norāda kartēšanu starp atribūta tipu un lauku Supply Chain Management tabulā. Sistēmas definēts tabulas ierobežojums dinamiski saista atribūta tipu un lauku. Šī saite sniedz iespēju ar preces konfigurācijas modeļa atribūtu atspoguļojot Supply Chain Management tabulas lauka datus.</td>
</tr>
<tr class="odd">
<td>Aprēķini</td>
<td>Aprēķini ir ierobežojumu papildinājums. Varat izmantot aprēķinu, lai veiktu aritmētiskas operācijas ar tipa <strong>Decimāldaļskaitlis</strong> un <strong>Vesels skaitlis</strong> atribūtiem vai loģiskas operācijas ar tipa <strong>Teksts</strong> (ar fiksētu sarakstu) un <strong>Būla</strong> atribūtiem. Aprēķinam ir mērķa atribūts, kurš ietvers aprēķina izteiksmes rezultātu. Aprēķina izteiksme tiek veidota, izmantojot izteiksmju redaktoru.</td>
</tr>
<tr class="even">
<td>Apakškomponenti</td>
<td>Apakškomponenti atspoguļo preču konfigurācijas modeļa koka struktūru. Apakškomponentus var izmantot, lai veidotu preču konfigurācijas modeļa struktūru. Apakškomponenti veido atsauces uz esošiem komponentiem. Tādēļ apakškomponentu lietošana veicina komponentu atkārtotu izmantošanu vairākos preces konfigurācijas modeļos. Apakškomponenta lapā <strong>Detalizēta informācija par MK rindu</strong> apakškomponentam varat atlasīt atšķirīgu vērtību. Alternatīvi varat atlasīt atribūtu, kuram vērtība ir atlasīta, iestatot preces konfigurācijas modeli. Lai preci iekļautu kā komponentu vai apakškomponentu, preces izveidošanas laikā lapā <strong>Izveidot preci</strong> ir jānorāda tālāk minētā informācija.
<ul>
<li>Laukā <strong>Preces tips</strong> atlasiet opciju <strong>Krājums</strong>.</li>
<li>Laukā <strong>Preces apakštips</strong> atlasiet opciju <strong>Preces šablons</strong>.</li>
<li>Laukā <strong>Konfigurēšanas tehnoloģija</strong> atlasiet opciju <strong>Konfigurācija atbilstoši ierobežojumam</strong>.</li>
</ul>
Cilnē <strong>Vispārīgi</strong>, lapā <strong>Detalizēta informācija par izlaistajām precēm</strong> varat apskatīt, vai izlaisto preci var izmantot kā komponentu vai apakškomponentu. Ja laukā <strong>Konfigurēšanas tehnoloģija</strong> ir atlasīta opcija <strong>Konfigurācija atbilstoši ierobežojumam</strong>, tad šo preci var lietot kā komponentu vai apakškomponentu. Varat paslēpt apakškomponentus, lai tie netiktu rādīti lietotājam konfigurācijas sesijas laikā. Atribūti, apakškomponenti un lietotāju prasības, kas saistītas ar apakškomponentu, arī ir paslēpti.</td>
</tr>
<tr class="odd">
<td>Lietotāju prasības</td>
<td>Lietotāju prasības norāda abstrakciju starp lietotāju prasībām, specifiskiem komponentiem un atribūtiem. Lietotāja prasību nevar kartēt ar krājumu. Piemēram, klients vēlas iegādāties mājas kinoteātra sistēmu. Tirdzniecības pārstāvis var jautāt par tās telpas lielumu, kur klients plāno uzstādīt sistēmu, lai noteiktu, cik vati ir nepieciešami. Šajā piemērā telpas lielums var būt lietotāja prasība, kas palīdz noteikt atbilstošo atribūta vērtību konkrētam komponentam. Varat paslēpt lietotāja prasības, lai tās netiktu rādītas lietotājam konfigurācijas sesijas laikā. Atribūti, apakškomponenti un lietotāju prasības, kas saistītas ar lietotāju prasību, arī ir paslēptas. Jūs varat rakstīt nosacījumu, lai kontrolētu, vai lietotāju prasību var paslēpt. Nosacījums ir jāraksta, izmantojot optimizācijas modelēšanas valodas (Optimization Modeling Language — OML) sintaksi.</td>
</tr>
<tr class="even">
<td>MK rindas</td>
<td>MK rindas norāda komponentu atsevišķus materiālus preču konfigurācijas modelī. Lapā <strong>Detalizēta informācija par MK rindu</strong> visi krājumi ir pieejami atlasei. MK rindai var pievienot nosacījumu, lai atšķirīgas preces variantam atlasītās MK rindas varētu atšķirties, pamatojoties uz lietotāja veikto atlasi preces konfigurācijas modeļa iestatīšanas laikā. Nosacījumi ir izteiksmes, kas jāievēro tajos atribūtos, MK rindās un maršruta operācijās, kas tiks iekļautas preču konfigurācijas modelī. Lapā <strong>Detalizēta informācija par MK rindu</strong> varat atlasīt atšķirīgu vērtību. Alternatīvi varat kartēt uz kādu atribūtu, kuram ir atlasīta vērtība, iestatot preces konfigurācijas modeli.</td>
</tr>
<tr class="odd">
<td>Maršruta operācijas</td>
<td>Lapā <strong>Detalizēta informācija par maršruta operāciju</strong> varat atlasīt atšķirīgu vērtību. Alternatīvi varat kartēt uz kādu atribūtu, kuram ir atlasīta vērtība, iestatot preces konfigurācijas modeli. Nosacījumi tiek rakstīti kā izteiksmju ierobežojumi. Nosacījumi ir izteiksmes, kas jāievēro tajos atribūtos, MK rindās un maršruta operācijās, kas tiks iekļautas preču konfigurācijas modelī.</td>
</tr>
</tbody>
</table>





