---
title: "Atlīdzības plāni"
description: "Atlīdzību un atvieglojumu vadītāji atlīdzību pārvaldību var izmantot, lai organizācijas darbiniekiem uzturētu un apstrādātu fiksētās un mainīgās atlīdzības sistēmas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 1809a6679685e483694a53b7742d80f02ade2cd5
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-plans"></a>Atlīdzības plāni

[!include[banner](includes/banner.md)]


Atlīdzību un atvieglojumu vadītāji atlīdzību pārvaldību var izmantot, lai organizācijas darbiniekiem uzturētu un apstrādātu fiksētās un mainīgās atlīdzības sistēmas.

### <a name="introduction"></a>Ievads

Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu. Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus. Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem. 

Darbinieki var būt reģistrēti vienā vai vairākos abu veidu plānos. Lai būtu piemērots reģistrācijai kādā atlīdzības plānā, darbiniekam ir jāatbilst tālāk norādītajām prasībām.
-   Darbiniekam ir nepieciešama aktīva amata piešķire.
-   Darbiniekam ir nepieciešams atbilst kritērijiem, kas atlīdzības plānam ir definēti ar piemērotības nosacījumiem.

## <a name="compensation-setup"></a>Atlīdzības iestatīšana
Nākamajā tabulā ir uzskaitīti atlīdzības procesa komponenti, kas var būt būtiski jūsu uzņēmuma atlīdzības plānu iestatīšanai.

<table>
<thead>
<tr class="header">
<th>Komponents</th>
<th>Papildinformācija...</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Fiksētās atlīdzības darbības</td>
<td>Ar fiksētājām atlīdzības darbībām tiek sasniegti divi mērķi:
<ul>
<li>Darbības var norādīt, kāda informācija ir jāreģistrē, kad mainās darbinieka atlīdzība. Piemēram, varat pieprasīt, lai tiktu reģistrēts izmaiņu iemesls, piemēram, paaugstināšana vai pazemināšana amatā.</li>
<li>Darbības var nodrošināt, ka fiksētās atlīdzības plānu apstrādāšanas laikā tiek lietots kāds aprēķins.  Piemēram, darbības ar tipu Kapitāls darbinieku algas salīdzinās ar minimālo atsauces punktu darbinieka līmenim un nodrošinās, ka darbiniekam tiek izmaksāts vismaz minimums.</li>
</ul></td>
</tr>
<tr class="even">
<td>Līmeņi</td>
<td>Līmeņi ir saistīti ar darbiem un jebkuriem amatiem, kas ir saistīti ar darba atsauci. Varat izveidot atsevišķus līmeņus trīs atlīdzības plānu tipiem: Kategorija, Josla un Pakāpe.</td>
</tr>
<tr class="odd">
<td>Diapazona lietojuma matrica</td>
<td>Diapazona lietojuma matrica jums palīdz pārcelt darbiniekus uz kontrolpunktu viņu darbiem. Diapazona lietojumu varat arī izmantot, lai uzņēmumā kontrolētu apmaksas likmes kapitālu, neņemot vērā atsevišķa darbinieka veiktspēju vai uzņēmuma vispārējo veiktspēju. Piemēram, darbinieki, kas savā diapazonā ir zemāk apmaksāti, saņem lielāku procentuālo pieaugumu nekā darbinieki, kas savā diapazonā ir augstāk apmaksāti. Šādi varat sistemātiski nobīdīt kapitāla atšķirības. Diapazona lietojums tiek aprēķināts šādi: (Fiksēta apmaksas likme - Diapazona minimums) ÷ (Diapazona maksimums - Diapazona minimums).</td>
</tr>
<tr class="even">
<td>Atsauces punkta iestatījumi</td>
<td>Atsauces punkta iestatījumi ietver atsauces punktu kopu, kuri veido matricas diapazonus. Katru diapazonu var saistīt ar kādu apmaksas likmi. Piemēram, kategoriju plāniem bieži vien ir atsauces punkti Minimums, Viduspunkts un Maksimums.</td>
</tr>
<tr class="odd">
<td>Atlīdzības matrica</td>
<td>Atlīdzības matrica ir atsauces punktu un līmeņu kopa, ko izmantojat, lai veidotu atlīdzību struktūru.</td>
</tr>
<tr class="even">
<td>Atlīdzības struktūra</td>
<td>Atlīdzības struktūra ir atlīdzības matrica, kurā apmaksas likmes katram līmenim ir saistītas ar atsauces punktiem.</td>
</tr>
<tr class="odd">
<td>Piemērotības nosacījumi</td>
<td>Piemērotības nosacījumi tiek izmantoti, lai identificētu darbiniekus konkrētos darbos, darbu funkcijās, darbu tipos, departamentos, arodbiedrībās vai atlīdzību reģionos, uz kuriem attiecas noteikti atlīdzību plāni. Lai darbiniekus reģistrētu plānā, jums ir jāizveido piemērotības nosacījumi gan mainīgās, gan fiksētās atlīdzības plāniem. Kad atlīdzības plānam ir norādīti piemērotības nosacījumi, varat definēt līmeņus, kas ir jālieto attiecībā uz šajā plāna ietvertajiem darbiem.</td>
</tr>
<tr class="even">
<td>Algas izmaksas biežums</td>
<td>Algas izmaksas biežums tiek lietots, lai definētu laika periodu, kādam ir norādīta atlīdzība.  Algas izmaksas biežums jums palīdz saprast, piemēram, vai atlīdzības summa ir norādīta kā gada alga vai kā stundas apmaksas likme. Algas izmaksas biežums tiek arī lietots, lai iestatītu pārveidošanas koeficientus un atlīdzības summu no algas izmaksas biežuma reizi mēnesī, reizi nedēļā, divreiz nedēļā un reizi stundā varētu konvertēt uz gada algas izmaksas biežumu.</td>
</tr>
<tr class="odd">
<td>Atlīdzības reģioni</td>
<td>Atlīdzības reģioni tiek lietoti, lai darbinieka atlīdzību norādītu, pamatojoties uz darbvietas atrašanās vietu.</td>
</tr>
<tr class="even">
<td>Kontrolpunkts</td>
<td>Kontrolpunkts nosaka, ko jūs uzskatāt par ideālu apmaksas likmi visiem darbiniekiem kādā atlīdzības līmenī. Kategoriju plāna struktūrām kontrolpunkti parasti ir diapazona viduspunkts. Joslu struktūrās kontrolpunkti tiek izmantoti reti. Fiksētas atlīdzības plānam kontrolpunktu varat norādīt formā Fiksētas atlīdzības plāni.</td>
</tr>
<tr class="odd">
<td>Darba funkcijas</td>
<td>Darba funkcijas tiek izmantotas, lai atlīdzību plānus klasificētu un filtrētu specifiskiem darbiem.</td>
</tr>
<tr class="even">
<td>Darba tipi</td>
<td>Darba tipi tiek izmantoti, lai atlīdzību plānus klasificētu un filtrētu specifiskiem darbiem.</td>
</tr>
<tr class="odd">
<td>Mainīgas atlīdzības tipi</td>
<td>Mainīgas atlīdzības plānos tiek iestatīti mainīgas atlīdzības tipi, piemēram, akciju prēmijas vai skaidras naudas prēmijas.</td>
</tr>
<tr class="even">
<td>Atlīdzību režģi</td>
<td>Atlīdzību režģi ietver atlīdzību struktūru.  Atlīdzību režģus var izmantot ar vienu vai vairākiem atlīdzības plāniem.</td>
</tr>
<tr class="odd">
<td>Veiktspējas plāni</td>
<td>Veiktspējas plāni tiek lietoti, lai veiktspēju saistītu ar sadalījumu matricu, tādējādi plānu varētu izmantot stratēģijai Samaksa par rezultātu.</td>
</tr>
<tr class="even">
<td>Veiktspējas vērtējumi</td>
<td>Veiktspējas vērtējumi tiek izmantoti veiktspējas plānos, lai noteiktu nopelnu piemaksas vai veiktspējas piemaksas apjomu.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Apstrādes notikumi
Procesa notikums aprēķina atlīdzības informāciju noteiktam periodam visiem darbiniekiem, kas ir reģistrēti vienā vai vairākos fiksētās vai mainīgās atlīdzības plānos. Procesa notikumu varat palaist atkārtoti, lai pārbaudītu vai atjauninātu aprēķinātos atlīdzības rezultātus.

<a name="compensation-events"></a>Atlīdzības notikumi
-------------------

Katru reizi, kad tiek palaists procesa notikums, tiek izveidots atlīdzības notikums.  Atlīdzības notikumi ietver atlīdzības procesa rezultātus katram darbiniekam, kas ir iekļauts attiecīgajā procesa notikumā.  Kad šie aprēķini ir pareizi, varat ielādēt atlīdzības notikumu, lai atjauninātu atlīdzības ierakstus tiem darbiniekiem, kurus šis procesa notikums ietekmē.

## <a name="recommendations"></a>Ieteikumi
Pēc procesa notikuma palaišanas varat ieteikt korekcijas darbinieka nopelnu palielinājumam vai piemaksas summai, pamatojoties uz procesa notikuma aprēķinātajām vadlīnijām. Lai darbiniekiem sniegtu ieteikumus, ieteikumi ir jāiespējo, kad iestatāt atlīdzību plānus vai kad iestatāt procesa notikumu.




