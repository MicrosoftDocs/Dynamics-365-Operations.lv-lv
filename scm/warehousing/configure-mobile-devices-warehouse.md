---
title: "Iestatīt mobilās ierīces darbam noliktavā"
description: "Šajā rakstā ir aprakstīts, kā konfigurēt izvēlnes vienumus, kurus noliktavas darbinieki izmanto, veicot darbu mobilajā ierīcē."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1ea74c0cb3abe6b8474842d8a7b0f431c8897aaf
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="set-up-mobile-devices-for-warehouse-work"></a>Iestatīt mobilās ierīces darbam noliktavā

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts, kā konfigurēt izvēlnes vienumus, kurus noliktavas darbinieki izmanto, veicot darbu mobilajā ierīcē.

**Piezīme.** Šis raksts attiecas uz moduļa Noliktavas pārvaldība līdzekļiem. Tas neattiecas uz moduļa Krājumu vadība līdzekļiem. Izvēlnes vienumus, kas tiek rādīti izvēlnēs noliktavas mobilajā ierīcē, var konfigurēt lapā **Mobilās ierīces izvēlnes vienumi**. Tā kā izvēlnes vienumus var ietvert dažādās izvēlnēs, var viegli konfigurēt izvēļņu struktūras tā, lai noteiktiem lietotājiem tiktu rādīti darba veidi. Varat konfigurēt izvēlnes vienumus tālāk norādīto uzdevumu veikšanai.

-   Apstrādāt pieprasījumu vai veikt aktivitāti, piemēram, izdrukāt etiķeti, ģenerēt unikālos noliktavas vienību identifikatorus, sākt ražošanas pasūtījumu vai ātri atrast uzmeklēt informāciju par krājumiem kādā novietojumā,
-   Izveidot darbu, kas tiks veikts, izmantojot citu procesu. Piemēram, saņemot pirkšanas pasūtījuma krājumu, var tikt izveidots izvietošanas darbs citam darbiniekam.
-   Veikt darbu, kas ir izveidots, izpildot citu procesu (esošu darbu), piemēram, izvietošanas darbu, kas ir izveidots, saņemot pirkšanas pasūtījuma krājumu.

Lai izveidotu izvēlnes vienumu kādai aktivitātei vai pieprasījumam, laukam **Režīms** norādiet vērtību **Netiešs**. Pēc tam kļūst pieejams lauka **Aktivitātes kods** opciju saraksts, kurā varat atlasīt to pieprasījuma vai aktivitātes tipu, kam šis izvēlnes vienums ir paredzēts. Lai izveidotu izvēlnes vienumu noliktavas darba ģenerēšanai, laukam **Režīms** iestatiet vērtību **Darbs**. Pēc tam kļūst pieejams lauka **Darba izveides process** opciju saraksts. Lai izveidotu izvēlnes vienumu esoša noliktavas darba apstrādei, iestatiet lauka **Režīms** vērtību **Darbs** un pēc tam norādiet opcijas **Izmantot esošo darbu** iestatījumu **Jā**. **Piezīme.** Atkarībā no izvēlnes vienumam atlasītā režīma un no tā, vai izvēlnes vienums tiek izmantots esoša darba veikšanai, izvēlnes vienumiem var būt pieejami papildu lauki. Informāciju par papildu lauku atlasi skatiet tālāk šī raksta sadaļā “Papildu izvēlnes vienumu opcijas”.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Aktivitāšu un pieprasījumu izvēlnes vienumu konfigurēšana
Ja ir izvēlnes vienumam ir iestatīta lauka **Režīms** vērtība **Netiešs**, varat izveidot izvēlnes vienumu tādas vispārējas aktivitātes vai pieprasījuma veikšanai, kas neizraisa darba izveidi. Piemēram, noliktavas vienību uzlīmju atkārtotai drukāšanai un pieprasījuma veikšanai par krājumiem noteiktā novietojumā. Tālāk esošajā tabulā ir norādītas pieejamās opcijas.

| Opcija                      | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nav                        | Šī noklusējuma vērtība neiespējo aktivitāti vai pieprasījumu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Par programmu                       | Skatiet informāciju par sistēmu, piemēram, versijas numuru, noliktavas ID un darbinieku, kurš pašlaik ir pieteicies.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Mainīt noliktavu            | Mainiet noliktavu, kurā darbinieks ir pieteicies.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Atrašanās vietas pieprasījums            | Skatiet informāciju par visiem novietojumā esošajiem krājumiem un daudzumiem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Numura zīmes pieprasījums       | Skatiet krājumu daudzumu noliktavas vienībā un noliktavas vienības novietojumu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Sākt ražošanas pasūtījumu      | Izveidojiet ražošanas pasūtījumu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Ražošanas brāķis            | Ievadiet ražošanas laikā izveidotā brāķa daudzumu katrai materiālu komplekta (MK) rindai.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Ražošanas pēdējā palete      | Norādiet, ka ir saražota ražošanas pasūtījuma pēdējā krājumu palete un ražošanas pasūtījuma statuss ir jāatjaunina uz **Ziņots kā pabeigts**. Ražošanas laikā neizmantoto izejmateriālu statuss tiek mainīts atpakaļ no **Izdots** uz **Pasūtīts**, un vienības var atgriezt krājumos.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Krājumu pieprasījums                | Skenējiet krājumu, lai noteiktu, kur tas atrodas noliktavā. Pieprasījums atgriež visus skenētā krājuma novietojumus un daudzumu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Atkārtoti drukāt etiķeti               | Atkārtoti izdrukājiet noliktavas vienības uzlīmi.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Numura zīmes būvējums         | Izveidojiet pamata noliktavas vienību, apvienojot vairākas noliktavas vienības vienā un tajā pašā novietojumā. Šī opcija ir noderīga, ja vienlaicīgi pārvietojat vairākas noliktavas vienības. Pēc tam, kad pamata noliktavas vienība ir pārvietota, ir jāveic noliktavas vienības pārtraukums, pirms varat atlasīt krājumus no katras noliktavas vienības. **Padoms.** Lai pārvietotu pamata noliktavas vienību, ir jāizmanto mobilā ierīce, kas ir konfigurēta kustības darba izveidei.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Numura zīmes pārtraukums         | Sadaliet noliktavas vienības būvējumu, lai varētu atlasīt vienumus no būvējumā ietvertajām noliktavas vienībām.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Autovadītāja reģistrēšanās norīkojuma izpildei             | Ja izmantojat moduli Transportēšanas pārvaldība, reģistrējiet vadītāja ierašanos, skenējot ieejošās kravas ID, norīkojuma ID vai sūtījuma ID. Lai izmantotu šo opciju, norīkojumam ir jāpiešķir krava un kravas statusam ir jābūt **Iekrauts**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Autovadītāja reģistrēšanās pēc norīkojuma pabeigšanas            | Reģistrējiet to, ka vadītājs ir pabeidzis savu norīkojumu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Notīrīt numuru sērijas kešatmiņu | Dzēsiet numuru sērijas numurus no numuru sērijas kešatmiņas. Šo aktivitāti parasti veic sistēmas administrators, lai novērstu kešdarbes problēmas, kad tiek izmantota mobilā ierīce.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Mainīt partijas atgriešanas metodi    | Atļaujiet darbiniekam norādīt krājuma un partijas atgriešanas metodes kodu. Veicot šo atlasi, tiek atjaunināts partijai norādītais atgriešanas metodes kods.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Parādīt atvērto darbu sarakstu      | Parādiet pieejamo darbu sarakstu noteiktam lietotājam. Pēc tam lietotājs var atlasīt veicamo darbu un saņem norādījumus tā veikšanai. Šo sarakstu ir paredzēts skatīt planšetdatoros, kuru ekrāna izmērs ir vismaz 7 collas. Kad atlasāt šo opciju, kļūst pieejami izvēlnes vienumi **Rediģēt vaicājumu** un **Lauku saraksts**. Lapā **Rediģēt vaicājumu** varat iestatīt sarakstā parādīto darbu kritērijus. Lapā **Lauku saraksts** varat atlasīt darbu sarakstā parādāmos laukus. Piemēram, varat samazināt parādīto lauku skaitu, lai lietotājs varētu ātrāk atlasīt piemērotāko darba vienumu. Kopsavilkuma cilnes **Vispārīgi** laukā **Ierakstu skaits lapā** varat arī atlasīt vienā lapā parādāmo darbu vienumu skaitu. Ja ir atlasīta opcija **Ļauj lietotājiem filtrēt pēc darba transakcijas veida**, darbu sarakstā tiek ietverta vadīkla **Filtrēt darbu**, ko lietotājs var izmantot filtrēšanai pēc transakcijas veida. Lietotājiem darbu sarakstā tiek rādīti tikai tie darbi, kuriem attiecīgajam lietotājam ir atļauja piekļūt. Jums ir jāpārliecinās, ka lietotājiem ir atļauja piekļūt vienu vai vairākiem lietotāja noteiktajiem izvēlnes vienumiem, kas atbalsta noteiktās darba klases tipus, kam šiem lietotājiem ir jāspēj piekļūt. Atļaujas tiek pārbaudītas, kad lietotājs mēģina izpildīt sarakstā iekļautu darbu. |

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Citam darbiniekam vai procesam paredzēta darba izveides izvēlnes vienumu konfigurēšana
Varat iestatīt izvēlnes vienumu, kas izveido darbu citam darbiniekam pēc tam, kad mobilajā ierīcē tiek veikta sākotnējā darbība. Piemēram, kad viens darbinieks izmanto mobilo ierīci, lai saņemtu krājumu, citam darbiniekam tiek izveidots izvietošanas darbs. Lai iestatītu izvēlnes vienumu, kas izraisa darba izveidi, lapā **Mobilās ierīces izvēlnes vienumi** atlasiet lauka **Režīms** vērtību **Darbs**. Tālāk esošajā tabulā ir norādītas lauka **Darba izveides process** opcijas, kas ir sakārtotas pēc darba pasūtījuma veida.

<table>
<tbody>
<tr>
<th>Darba pasūtījuma veids</th>
<th>Opcija</th>
<th>Apraksts</th>
</tr>
<tr>
<td rowspan="8">Pirkšanas pasūtījums</td>
<td>Pirkšanas pasūtījuma rindas saņemšana</td>
<td>Reģistrējiet noteikta krājuma daudzuma ieejas plūsmu, izmantojot pirkšanas pasūtījuma numuru un pirkšanas pasūtījuma rindas numuru, un izvietojiet izvietošanas darbu citam darbiniekam.</td>
</tr>
<tr>
<td>Pirkšanas pasūtījuma rindas saņemšana un izvietošana</td>
<td>Reģistrējiet noteikta krājumu daudzuma saņemšanu, izmantojot pirkšanas pasūtījuma numuru un pirkšanas pasūtījuma rindas numuru, un izvietojiet krājumus. Tas pats darbinieks veic abas darbības.</td>
</tr>
<tr>
<td>Pirkšanas pasūtījuma krājuma saņemšana</td>
<td>Reģistrējiet noteikta krājuma daudzuma ieejas plūsmu pirkšanas pasūtījumam, reģistrējot pirkšanas pasūtījuma numuru un krājuma numuru, un izvietojiet izvietošanas darbu citam darbiniekam.</td>
</tr>
<tr>
<td>Pirkšanas pasūtījuma krājuma saņemšana un izvietošana</td>
<td>Reģistrējiet noteikta krājumu daudzuma saņemšanu pirkšanas pasūtījumam, reģistrējot pirkšanas pasūtījuma numuru, un izvietojiet krājumus. Tas pats darbinieks veic abas darbības.</td>
</tr>
<tr>
<td>Noliktavas vienības saņemšana</td>
<td>Saņemiet ienākošo kravu, izmantojot noliktavas vienības ID.</td>
</tr>
<tr>
<td>Numura zīmes saņemšana un izvietošana</td>
<td>Saņemiet un izvietojiet ienākošo kravu, izmantojot noliktavas vienības ID.</td>
</tr>
<tr>
<td>Kravas krājuma saņemšana</td>
<td>Reģistrējiet noteikta kravas daudzuma saņemšanu, izmantojot kravas ID, un izveidojiet izvietošanas darbu citam darbiniekam. Krājuma numurs un preču dimensijas izveido saņemšanas atbilstību pirkšanas pasūtījuma rindām.</td>
</tr>
<tr>
<td>Kravas krājuma saņemšana un izvietošana</td>
<td>Reģistrējiet noteikta kravas daudzuma saņemšanu, izmantojot kravas ID, un izvietojiet krājumus. Krājuma numurs un preču dimensijas izveido saņemšanas atbilstību pirkšanas pasūtījuma rindām. Tas pats darbinieks veic abas darbības.</td>
</tr>
<tr>
<td>Atgriezt pasūtījumu</td>
<td>Atgriešanas pasūtījuma saņemšana</td>
<td>Reģistrējiet noteikta krājuma daudzuma saņemšanu, reģistrējot AKA kodu, un izveidojiet izvietošanas darbu citam darbiniekam.</td>
</tr>
<tr>
<td>Atgriešanas pasūtījuma saņemšana un izvietošana</td>
<td>Reģistrējiet noteikta krājumu daudzuma saņemšanu, reģistrējot AKA kodu, un izvietojiet krājumus. Tas pats darbinieks veic abas darbības.</td>
</tr>
<tr>
<td>Pārsūtīšanas pasūtījums</td>
<td>Pārsūtīšanas pasūtījuma krājumu saņemšana</td>
<td>Reģistrējiet noteikta krājuma daudzuma saņemšanu un izveidojiet izvietošanas darbu citam darbiniekam.

<strong>Piezīme.</strong> Lietojiet šo opciju tikai tad, ja krājumi ir nosūtīti no noliktavas, kurai nav iespējoti noliktavas pārvaldības procesi.</td>
</tr>
<tr>
<td>Pārsūtīšanas pasūtījuma krājumu saņemšana un izvietošana</td>
<td>Reģistrējiet noteikta krājumu daudzuma saņemšanu un izvietojiet krājumus. Tas pats darbinieks veic abas darbības.

<strong>Piezīme.</strong> Lietojiet šo opciju tikai tad, ja krājumi ir nosūtīti no noliktavas, kurai nav iespējoti noliktavas pārvaldības procesi.</td>
</tr>
<tr>
<td>Pārsūtīšanas pasūtījuma rindas saņemšana</td>
<td>Reģistrējiet noteikta krājuma daudzuma saņemšanu un izveidojiet izvietošanas darbu citam darbiniekam.</td>
</tr>
<tr>
<td>Pārsūtīt pasūtījuma rindas saņemšanu un izvietošanu</td>
<td>Reģistrējiet noteikta krājumu daudzuma saņemšanu un izvietojiet krājumus. Tas pats darbinieks veic abas darbības.</td>
</tr>
<tr>
<td>Ražošana</td>
<td>Reģistrēt pabeigšanu</td>
<td>Reģistrējiet noteiktu saražotā krājuma daudzumu, kura ražošana ir pabeigta, un izvietojiet izvietošanas darbu citam darbiniekam. Šis daudzums varētu būt daļa vai viss ražošanai paredzētais daudzums.</td>
</tr>
<tr>
<td>Reģistrēt pabeigšanu un izvietot</td>
<td>Reģistrējiet noteiktu ražošanā pabeigtu krājumu daudzumu, un izvietojiet krājumus. Šis daudzums varētu būt daļa vai viss ražošanai paredzētais daudzums. Tas pats darbinieks veic abas darbības.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Norādiet, ka Kanban ir pabeigts, un izveidojiet izvietošanu darbu citam darbiniekam.</td>
</tr>
<tr>
<td>Kanban izvietošana</td>
<td>Norādiet, ka Kanban ir pabeigts, un izvietojiet krājumus. Tas pats darbinieks veic abas darbības.</td>
</tr>
<tr>
<td>Krājumi</td>
<td>Kustība</td>
<td>Reģistrējiet krājumu pārvietošanu no vien novietojuma uz citu. Darbinieks norāda novietojumu, no kuras krājumi tiek pārvietoti, kā arī novietojumu, uz kuru tie tiek pārvietoti.</td>
</tr>
<tr>
<td>Karantīna</td>
<td>Mainiet rīcībā esošo krājumu statusu noliktavas vienībai vai novietojumam, lai padarītu bojātas vai trūkstošas krājumu vienības nepieejamas.</td>
</tr>
<tr>
<td>Kustība pēc veidnes</td>
<td>Pārvietojiet krājumus no viena novietojuma uz citu daļēji automatizētā veidā. Darbinieks atlasa novietojumu, no kura ir jāpārvieto krājumi, un programmatūra Dynamics 365 for Finance and Operations izmanto šī novietojuma direktīvu, lai noteiktu, uz kurieni krājumi ir jāpārvieto.</td>
</tr>
<tr>
<td>Starpnoliktavu pārsūtīšana</td>
<td>Reģistrējiet krājumu pārvietošanu no vienas noliktavas uz citu. Lai izmantotu šo opciju, darbiniekam ir jābūt atļaujai veikt darbus abās noliktavās.

<strong>Piezīme.</strong> Lai izmantotu šo izvēlnes vienumu, ir nepieciešams noklusējuma krājumu pārsūtīšanas žurnāls, kurā ir iestatīta lauka <strong>Dokumenta izrakstīšana</strong> vērtība <strong>Grāmatošana</strong>.</td>
</tr>
<tr>
<td>Numura zīmes ielāde</td>
<td>Izmantojiet šo opciju, kad iestatāt noliktavu pirmo reizi. Skenējiet visas noliktavas vienības visos noliktavas novietojumos. Novietojumiem ir jābūt atkarīgiem no noliktavas vienības. šo opciju nevar izmantot, ja krājumu rezervēšanas hierarhijā vienums <strong>Sērijas numurs</strong> vai <strong>Partijas numurs</strong> ir novietots virs vienuma <strong>Novietojums</strong>.</td>
</tr>
<tr>
<td>Cikla inventarizācija</td>
<td>Ienākošā korekcija</td>
<td>Palieliniet krājumos esošo vienību daudzumu. Norādiet atrašanās vietu, noliktavas vienību, vienību, daudzumu, mērvienību un statusu.</td>
</tr>
<tr>
<td>Izejošā korekcija</td>
<td>Samaziniet krājumos esošo vienību daudzumu. Norādiet krājuma atrašanās vietu, noliktavas vienību, vienību, daudzumu, mērvienību un statusu.</td>
</tr>
<tr>
<td>Cikla inventarizācija uz vietas</td>
<td>Sāciet inventarizāciju novietojumam. Darbiniekam ir jāinventarizē visi novietojumā esošie krājumi. Ja inventarizācijas rezultātā tiek iegūts daudzums, kas ir mazāks par paredzēto daudzumu, trūkstošais daudzums tiek uzskatīts par zaudējumu.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Esoša darba apstrādes izvēlnes vienumu konfigurēšana
Varat iestatīt ne tikai noliktavas darbu izveides izvēlnes vienumus, bet arī jau izveidotu darbu apstrādes izvēlnes vienumus. Iestatiet lauka **Režīms** vērtību **Darbs** un atlasiet opciju **Izmantot esošo darbu**. Pēc tam cilnē **Vispārīgi** kļūst pieejamas dažas papildu opcijas. Varat kontrolēt piekļuvi izvēlnes vienumam, kopsavilkuma cilnē **Darba klase** piešķirot vienu vai vairākas darba klases. Darba klases definē darbu, ko var apstrādāt ar izvēlnes vienumu. Darba klasi var arī izmantot, lai piešķirtu piekļuves tiesības noteiktām lietotāju lomām vai nošķirtu dažādu operāciju veidu apstrādi. Tālāk esošajā tabulā ir aprakstītas pieejamās opcijas.

<table>




<thead>
<tr class="header">
<th>Opcija</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nav</td>
<td>Šī noklusējuma vērtība neizraisa darba apstrādi.</td>
</tr>
<tr class="even">
<td>Sistēmas noteikts</td>
<td>Programmatūra Microsoft Dynamics 365 for Finance and Operations kontrolē darbiniekam piešķirtā darba tipu un secību, kādā darbinieks veic šo darbu. Kad atlasāt šo opciju, darbību rūtī varat noklikšķināt uz <strong>Sistēmā noteikts darbs</strong>, lai atvērtu lapu <strong>Sistēmā noteikta kārtošanas secība</strong>, kur varat iestatīt darba kārtošanas kritērijus. Kārtošanas kritēriji kontrolē kārtību, kādā darbinieks šo darbu veid. Varat pievienot tik daudz kritēriju, cik nepieciešams.</td>
</tr>
<tr class="odd">
<td>Lietotāja noteikts</td>
<td>Darbinieks izvēlas veicamo darbu un secību, kādā to veikt.</td>
</tr>
<tr class="even">
<td>Lietotāju grupēšana</td>
<td>Darbinieks manuāli grupē darbu. Šī opcija ir noderīga, piemēram, kad darbinieks kādā novietojumā var vienlaicīgi izdot vairākus krājumus. Pēc tam, kad darbinieks ir izdevis visi vajadzīgos krājumus, viņš var izvietot krājumus.</td>
</tr>
<tr class="odd">
<td>Sistēmas grupēšana</td>
<td>Programmatūra Microsoft Dynamics 365 for Finance and Operations grupē darbiniekam paredzēto darbu, pamatojoties uz norādīto lauku. Piemēram, izdošanas darbs tiek grupēts, kad darbinieks skenē sūtījuma ID, kravas ID vai jebkuru vērtību, ar kuru var saistīt katru darba vienību. Ja atlasāt šo opciju, ir nepieciešams aizpildīt tālāk norādītos laukus.
<ul>
<li><strong>Sistēmas grupēšanas lauks</strong> — atlasiet lauku, ko darbinieks skenē, lai grupētu darbu.</li>
<li><strong>Sistēmas grupēšanas etiķete</strong> — ievadiet tekstu, lai norādītu darbiniekam, kas ir jāskenē, lai grupētu darbu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Validēts, lietotāja noteikts</td>
<td>Darbinieks atlasa veicamo darbu, kad darbs ir saistīts ar lielāku elementu, piemēram, kravu vai sūtījumu. Darbinieks nosaka secību, kādā krājumi tiek izdoti. Ja atlasāt šo opciju, ir nepieciešams aizpildīt tālāk norādītos laukus.
<ul>
<li><strong>Validēts, lietotāja noteikts lauks</strong> — atlasiet lauku, ko darbinieks skenē, lai grupētu darbu.</li>
<li><strong>Validēta, lietotāja noteikta etiķete</strong> — ievadiet tekstu, lai norādītu darbiniekam, kas ir jāskenē, kad izdošanas darbu grupē sistēma.</li>
</ul>
Šī opcija ir noderīga, piemēram, ja ir paredzēts iekraut vairākas paletes. Ja atlasāt lauka <strong>Validēts, lietotāja noteikts</strong> vērtību <strong>LoadId</strong>, darbinieks var izdot jebkuru ar kravu saistīto paleti Ja darbinieks skenē krājumu, kas nav saistīts ar kravu, viņš saņem kļūdas ziņojumu.</td>
</tr>
<tr class="odd">
<td>Klastera izdošana</td>
<td>Darbinieks grupē darbu klasteros. Izmantojot klasterus, darbinieki var no viena novietojuma vienlaicīgi izdot krājumus vairākiem darba pasūtījumiem.</td>
</tr>
<tr class="even">
<td>Cikla inventarizācijas grupēšana</td>
<td>Darbinieks atlasa zonu, darba pūlu vai novietojumu, un programmatūra Microsoft Dynamics 365 for Finance and Operations piešķir darbu, pamatojoties uz atlasi. Ja atlasāt šo opciju, varat darbību rūtī noklikšķināt uz <strong>Cikla inventarizācija</strong>, lai norādītu papildu parādāmo informāciju, kā arī varat norādīt, cik reižu darbiniekam ir jāatkārto inventarizācija, ja tiek konstatēta atšķirība.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Papildus izvēlnes vienumu opcijas
Lapā **Mobilās ierīces izvēlnes vienumi** ir pieejamas papildu izvēlnes vienumu opcijas. Opcijas atšķiras atkarībā no procesa, kam konfigurējat izvēlnes vienumu. 

Tabulā ir sniegts šo opciju apraksts.

<table>




<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Atļaut darba sadali</td>
<td>Atlasiet šo opciju, lai ļautu lietotājiem ievietot darba pasūtījumam paredzētos krājumus vairāk nekā vienā mērķa noliktavas vienībā. Šī opcija ir noderīga, piemēram, ja mērķa noliktavas vienība ir pilna un darbiniekam jāpievieno atlikušie krājumi citā noliktavas vienībā. Darbinieks var noklikšķināt uz <strong>Pilns</strong>, lai norādītu, ka noliktavas vienība ir pilna, un pārtraukt ar to saistītu izdošanas darbu saņemšanu. Pēc tam izdotajiem krājumiem tiek parādīts izvietošanas novietojums, un pabeigtais izdošanas darbs tiek pārvietots uz jaunu darba pasūtījumu. Atlikušais mērķa noliktavas vienības izdošanas darbs paliek sākotnējā darba pasūtījumā.</td>
</tr>
<tr class="even">
<td>Noenkurošana</td>
<td>Atlasiet šo opciju, lai ļautu darbiniekiem norādīt novietojumu, ar kuru tiks aizstāts ieteiktais sagatavošanas posma vai iekraušanas novietojums. Viss atlikušais izvietošanas darbs tiek novirzīts uz jauno novietojumu. Šī opcija ir noderīga, piemēram, ja darbiniekam ir jānovieto 1. pasūtījuma krājumi sagatavošanas posma novietojumā pie 1. doka, taču to nevar izdarīt, jo no novietojuma vēl nav paņemta iepriekšējā krava. Tā vietā, lai gaidītu, kamēr kļūs pieejams 1. doka sagatavošanas posma novietojums, darbinieks var izlemt izmantot 2. doka sagatavošanas posma novietojumu. Šādā gadījumā darbinieks ignorē ieteikto sagatavošanas posma novietojumu. Pēc tam tiek atjaunināts visu darba pasūtījuma atlikušo krājumu izvietošanas novietojums, mainot to uz 2. doka sagatavošanas posma novietojumu. Ja atlasāt šo opciju, ir jāiestata lauks <strong>Noenkuroja pēc</strong>.</td>
</tr>
<tr class="odd">
<td>Noenkuroja pēc</td>
<td>Ja izmantojat noenkurošanu, ir jānorāda, vai vēlaties noenkurot pēc sūtījuma vai kravas.</td>
</tr>
<tr class="even">
<td>Audita veidnes ID</td>
<td>Atlasiet darba audita veidni, ar kuru tiks pārtraukts darba process šim izvēles vienumam, lai var veikt citu operāciju. Piemēram, ja šis izvēlnes vienums ir paredzēts ienākošajam darbam, audita veidnē var tikt pieprasīts, lai darbinieks pārbaudītu temperatūru piegādes konteinerā. Procesa pārtraukšanas brīdis ir norādīts audita veidnē. Šis brīdis var būt, piemēram, darba sākšanas vai pabeigšanas brīdis vai tā statusa maiņas brīdis.</td>
</tr>
<tr class="odd">
<td>Klastera profila ID</td>
<td>Atlasiet klastera profilu, kuru lietot klastera izdošanai. Klastera profilā ir ietverti tādi iestatījumi kā klasteru automātiskas izveides iestatījums, pozīciju nosaukumi, klasteriem piešķiramo darba vienību skaits, iestatījums klasteru sadalīšanai atsevišķās vienībās un pārbaudes nepieciešamības iestatījums. Šis lauks ir pieejamas tikai tad, ja ir atlasīta lauka <strong>Novirzītājs</strong> vērtība <strong>Klastera izdošana</strong>.</td>
</tr>
<tr class="even">
<td>Vispirms saskaitīt krājumu kopējo daudzumu</td>
<td>Atlasiet šo opciju, lai noteiktu, ka darbiniekam skaitīšanas laikā vispirms ir jāsaskaita kopējais daudzums. Ja tiek konstatēta atšķirība, darbiniekam ir jāsniedz papildinformācija, piemēram, unikālais noliktavas vienības identifikators, partijas numurs un sērijas numuri.</td>
</tr>
<tr class="odd">
<td>Izveidot kustību</td>
<td>Atlasiet šo opciju, lai ļautu darbiniekam izveidot kustības darbu, ko nav nepieciešams veikt nekavējoties. Šī opcija ir noderīga, piemēram, ja ir pabeigta kvalitātes pārbaude un pārbaudes veicējs vēlas, lai krājums tiktu pārvietots prom no kvalitātes pārbaudes zonas.</td>
</tr>
<tr class="even">
<td>Direktīvas kods</td>
<td>Lai izmantotu konkrētu novietojuma direktīvu, atlasiet direktīvas kodu, kurš ir saistīts ar novietojuma direktīvu. Šis lauks ir pieejams, ja izveidojat darbu un darba izveides process ir <strong>Kustība pēc veidnes</strong>.</td>
</tr>
<tr class="odd">
<td>Atspējot cikla inventarizācijas robežvērtības</td>
<td>Atlasiet šo opciju, lai ignorētu cikla inventarizācijas robežvērtības. Ja atlasāt šo opciju, cikla inventarizācijas darbs netiek izveidots, ja tiek pārsniegtas robežvērtības.</td>
</tr>
<tr class="even">
<td>Parādīt partijas metodes kodu</td>
<td>Atlasiet šo opciju, lai attēlotu partijas atgriešanas metodes kodus. Piemēram, var tikt rādīti partijas atgriešanas metodes kodi, kad tiks saņemta atgriezta partija. Pēc tam darbinieki var novērtēt partijas statusu vai kvalitāti un atlasīt atbilstošo kodu. Partijas atgriešanas metodes kodā ietvertie noteikumi nosaka, vai partija būs pieejama citiem noliktavas procesiem. Ja neatlasāt šo opciju, tiek izmantots kāds no tālāk norādītajiem partijas atgriešanas metodes kodiem.
<ul>
<li>Ja saņemat jaunu partijas numuru, tiek izmantots noklusējuma partijas atgriešanas metodes kods, kas ir norādīts krājumu modeļu grupai</li>
<li>Tiek izmantots tas partijas atgriešanas metodes kods, kas jau ir piešķirts partijai</li>
</ul></td>
</tr>
<tr class="odd">
<td>Parādīt metodes kodu</td>
<td>Atlasiet šo opciju, lai parādītu atgriešanas metodes kodus. Piemēram, varat parādīt partijas atgriešanas metodes kodus, kad saņemat atgrieztos krājumus. Pēc tam darbinieki var novērtēt krājumu statusu vai kvalitāti un atlasīt atbilstošo kodu. Atgriešanas metodes kodā ietvertie noteikumi nosaka, vai krājums būs pieejams citiem noliktavas procesiem.</td>
</tr>
<tr class="even">
<td>Rādīt krājumu statusu</td>
<td>Atlasiet šo opciju, lai parādītu krājumu vienību statusu. Šī opcija ir pieejama visiem izvēlnes vienumiem, kuriem tiek izmantots esošais darbs, izņemot cikla inventarizāciju.</td>
</tr>
<tr class="odd">
<td>Rādīt izdošanas ekrāna kopsavilkumu</td>
<td>Atlasiet šo opciju, lai parādītu kopsavilkumu par atlasītā darba pasūtījuma izdošanas darbu. Kopsavilkums tiek rādīts līdz darba pasūtījumā tiek apstrādāta pirmā darba rinda.</td>
</tr>
<tr class="even">
<td>Ģenerēt numura zīmi</td>
<td>Atlasiet šo opciju, lai ģenerētu unikālu noliktavas vienības identifikatoru, pamatojoties uz numuru sērijas atlasi. Piemēram, varat ģenerēt unikālo noliktavas vienības identifikatoru tiem krājumiem, kas ir saņemti atbilstoši pirkšanas pasūtījumiem.</td>
</tr>
<tr class="odd">
<td>Grupēt izvietošanu</td>
<td>Atlasiet šo opciju, lai grupētu izvietošanas darbu. Šī opcija ir pieejama tad, ja darbu ir grupējis darbinieks vai programmatūra Microsoft Dynamics 365 for Finance and Operations. Kad darbinieks ir pabeidzis visu izdošanas darbu grupā, tai pašai grupai tiek izveidots izvietošanas darbs.</td>
</tr>
<tr class="even">
<td>Krājumu korekciju veidi</td>
<td>Atlasiet krājumu korekcijas veidu, kas nosaka korekcijas grāmatošanai izmantoto krājumu inventarizācijas žurnālu un to, vai noņemt rezervācijas. Šis lauks ir pieejams tikai darba izveides procesam <strong>Ienākošā korekcija</strong> vai <strong>Izejošā korekcija</strong></td>
</tr>
<tr class="odd">
<td>Ignorēt partijas numuru</td>
<td>Atlasiet šo opciju, lai ļautu tiem darbiniekiem, kuri atzīmē kādam ražošanas pasūtījumam paredzēto daudzumu kā pabeigtu, ievadīt partijas numuru, kas atšķiras no ražošanas pasūtījumam piešķirtā partijas numura.</td>
</tr>
<tr class="even">
<td>Ignorēt mērķa noliktavas vienību</td>
<td>Atlasiet šo opciju, lai ļautu darbiniekiem norādīt mērķa unikālo noliktavas vienības identifikatoru, kas atšķiras no ieteiktās mērķa noliktavas vienības. Izmantojiet šo opciju, ja darba pasūtījuma pirmā izdošana ir visam krājuma daudzumam noliktavas vienībā. Šī opcija ir noderīga, piemēram, ja tiek atkārtoti lietota kāda palete.</td>
</tr>
<tr class="odd">
<td>Izdot un iepakot</td>
<td>Atlasiet šo opciju, lai ļautu darbiniekiem apvienot pārdošanas pasūtījuma vai kravas darbu vienā darba vienībā. Darbinieks var veikt tikai ar pārdošanas pasūtījumu vai kravu saistītu darbu. Šī opcija ir noderīga, piemēram, ja ir jāpalielina pārdošanas pasūtījuma daudzums pēc tam, kad pārdošanas pasūtījumam ir izveidota krava, sūtījums un darbs. Šī opcija ir pieejama, ja izvēlnes vienumā tiek izmantots esošais darbs un šo darbu vada lietotājs vai sistēma.</td>
</tr>
<tr class="even">
<td>Nav</td>
<td>Norādiet, vai darbiniekam novietojumā vispirms ir jāizdod vecākā partija. Pieejamas šādas opcijas
<ul>
<li><strong>Nav</strong> — darbinieks var izdot jebkuru novietojumā esošo partiju. Darbinieks nesaņem nekādu ziņojumu.</li>
<li><strong>Brīdināt</strong> — darbinieks var izdot jebkuru novietojumā esošo partiju, taču, ja tā nav vecākā partija, tiek parādīts brīdinājuma ziņojums.</li>
<li><strong>Uzspiest</strong> — darbiniekam novietojumā vispirms ir jāizdod vecākā partija. Ja izdotā partija nav vecākā partija, darbinieks saņem kļūdas ziņojumu. <strong>Piezīme.</strong> Šī opcija darbojas tikai tad, ja krājumam piešķirtajā rezervēšanas hierarhijā vienums <strong>Partijas numurs</strong> atrodas zem vienuma <strong>Novietojums</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Drukāt etiķeti</td>
<td>Atlasiet šo opciju, lai ļautu darbiniekiem drukāt noliktavas vienību etiķetes.</td>
</tr>
<tr class="even">
<td>Sistēmas grupēšanas lauks</td>
<td>Atlasiet lauku, kas nosaka, kā programmatūra Microsoft Dynamics 365 for Finance and Operations grupēs darbinieku veikto izdošanas darbu. Piemēram, ja atlasīsiet lauku <strong>ShipmentId</strong>, darbinieks skenēs sūtījuma ID, lai grupētu izdošanas darbu. Pēc tam viss ar sūtījumu saistītais darbs tiks piešķirts darbiniekam. Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai. Ir arī jāievada teksts laukā <strong>Sistēmas grupēšanas etiķete</strong>, lai norādītu darbiniekam, kas ir jāskenē.</td>
</tr>
<tr class="odd">
<td>Sistēmas grupēšanas etiķete</td>
<td>Ievadiet tekstu, tiek rādīts darbiniekam, lai norādītu, kas ir jāskenē, ja programmatūra Microsoft Dynamics 365 for Finance and Operations grupē izdošanas darbu. Piemēram, ja izmantojat lauku <strong>ShipmentId</strong>, lai grupētu izdošanas darbu pēc sūtījuma, varat šajā laukā ievadīt vērtību <strong>Sūtījuma ID</strong>. Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai. Turklāt laikā <strong>Sistēmas grupēšanas lauks</strong> ir jāatlasa lauks, pēc kura grupēt.</td>
</tr>
<tr class="even">
<td>Lietot noklusējuma datus</td>
<td>Atlasiet šo opciju, lai darbību rūtī iespējotu pogu <strong>Noklusējuma dati</strong>, kas ļauj atlasīt laukus, lai parādītu datus, kuri darbiniekam parasti ir nepieciešami ikdienas darba veikšanai. Šī opcija ir noderīga, piemēram, ja darbinieks bieži izdod krājumus no viena un tā paša novietojuma. Varat atlasīt lauku <strong>Avota atrašanās vieta</strong>, lai novietojums tiktu rādīts pēc noklusējuma.</td>
</tr>
<tr class="odd">
<td>Validēts, lietotāja noteikts lauks</td>
<td>Atlasiet lauku, kuru darbinieks skenēs, lai grupētu darbu. Piemēram, ja atlasīsiet <strong>LoadId</strong>, darbinieks var izdot jebkādu darbu, kas ir saistīts ar atlasīto kravu. Ir arī jāievada teksts laukā <strong>Validēta, lietotāja noteikta etiķete</strong>, lai norādītu darbiniekam, kas ir jāskenē.</td>
</tr>
<tr class="even">
<td>Validēta, lietotāja noteikta etiķete</td>
<td>Ievadiet tekstu, lai norādītu lietotājam, kas ir jāskenē, ja izdošanas darbs tiek grupēts, izmantojot validētu, lietotāja noteiktu lauku. Piemēram, ja izmantojat lauku <strong>LoadId</strong>, lai grupētu izdošanas darbu kravai, varat ievadīt laukā <strong>kravas ID</strong>.</td>
</tr>
<tr class="odd">
<td>Darba veidnes kods</td>
<td>Atlasiet darba veidni, kurā procesam tiks izveidots darbs. Piemēram, ja saņemat krājumu kādam pirkšanas pasūtījumam, izvietošanas darbs tiks ģenerēts, pamatojoties uz darba veidni. Ja neatlasāt darba veidni, programmatūra Microsoft Dynamics 365 for Finance and Operations piešķir veidni, pamatojoties uz vaicājuma kritērijiem. Plašāku informāciju par darbu veidnēm skatiet sadaļā <a href="control-warehouse-location-directives.md">Noliktavas darbu kontrolēšana ar darba veidnēm un novietojuma direktīvām</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Pieprasīšana, lai darbinieki, izdodot krājumus, apstiprinātu preci, novietojumu vai daudzumu
Varat iestatīt darba apstiprinājumus, kas nosaka, ka darbiniekam, strādājot noliktavā, ir jāreģistrē novietojums vai daudzums, izmantojot mobilo ierīci. Darba apstiprinājumi palīdz nodrošināt, ka darbinieks atrodas pareizajā novietojumā un strādā ar pareizo krājumu daudzumu. Varat arī programmatūrā Microsoft Dynamics 365 for Finance and Operations iespējot automātisku darbinieka veiktās reģistrācijas apstiprināšanu. Ja iespējojat automātisko apstiprināšanu, nevarat pieprasīt arī novietojuma vai daudzuma apstiprinājumus. Darba apstiprinājumos tiek ietvertas arī preces un preču varianti. Turklāt varat arī reģistrēt apstiprinājumus, skenējot svītrkodu. Lai apstiprinātu preces un preču variantus, jums jāievada preces vai preces varianta ID. Šis ID var būt preces ID, preces meklēšanas ID, ārējais ID, GTIN vai svītrkods. Pēc tam, kad ievadīsiet ID vai noskenēsiet svītrkodu, mobilajā ierīcē tiks parādītas preces varianta dimensijas. 

Tālāk esošajā tabulā ir aprakstīti dažādi darba veidi, kam var izmantot darba apstiprinājumus.

| Opcija                 | Apraksts                                                                |
|------------------------|----------------------------------------------------------------------------|
| Atlasīt                   | Pieprasiet apstiprinājumu, kad tiek izdoti krājumi.                                |
| Izvietot                    | Pieprasiet apstiprinājumu, kad krājumi tiek ievietoti novietojumā.                     |
| Uzskaite               | Pieprasiet apstiprinājumu cikla inventarizācijas laikā.                                |
| Korekcijas            | Pieprasiet apstiprinājumu, kad tiek koriģēts krājumu daudzums.               |
| Pielāgots                 | Pieprasiet apstiprinājumu pielāgotiem darbiem.                                      |
| Karantīna             | Pieprasiet apstiprinājumu, kad krājumi tiek pārvietoti uz karantīnu.                   |
| Numura zīmes būvējums | Pieprasiet apstiprinājumu, kad krājumi tiek apvienoti, lai izveidotu noliktavas vienību. |
| Drukāt                  | Pieprasiet apstiprinājumu, kad tiek drukātas noliktavas vienību etiķetes.                |
| Statusa maiņa          | Pieprasiet apstiprinājumu, kad tiek mainīts krājumu statuss.              |

**Piezīme.** Preces apstiprinājumu varat pieprasīt tikai izdošanas un izvietošanas darbu veidiem.

<a name="see-also"></a>Skatiet arī
--------

[Noliktavas mobilo ierīču displeja iestatījumi](change-warehouse-mobile-device-displays.md)

[Mobilās ierīces izvēlnes vienuma iestatīšana pirkšanas pasūtījuma darba veikšanai (uzdevuma ceļvedis)](/dynamics365/unified-operations/supply-chain/warehousing/tasks/set-up-mobile-device-menu)

[Mobilās ierīces izvēlnes vienuma iestatīšana saņemto krājumu reģistrēšanai (uzdevuma ceļvedis)](/dynamics365/unified-operations/supply-chain/warehousing/tasks/set-up-mobile-device-menu-item-register-received-items)
[Krājumu statusu lietošanas priekšrocības](../inventory/inventory-statuses.md)



