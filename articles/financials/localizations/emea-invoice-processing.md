---
title: "Rēķina apstrāde"
description: "Šajā tēmā ir sniegta informācija par rēķinu apstrādāšanu Austrumeiropas valstīm."
author: v-kikozl
manager: AnnBe
ms.date: 07/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-kikozl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 07d09512ef612b41bf527b74496fa440f23851fc
ms.openlocfilehash: d1fca30eb6de22c2d2fb2c4d6bfdfd21fd4bbd6e
ms.contentlocale: lv-lv
ms.lasthandoff: 02/14/2018

---

# <a name="invoice-processing"></a>Rēķina apstrāde

[!include[banner](../includes/banner.md)]

Šajā tēmā ir īsi aprakstīti daži valstij specifiskie scenāriji, piemēram, Eiropas Kopienas iekšējais pievienotās vērtības nodoklis (PVN) un atliktais nodoklis. Rēķinu izrakstīšanas procesu ietekmē dažās Eiropas valstīs pastāvošās juridiskās prasības. Šajā tēmā ir sniegta arī informācija par to, kā šīm valstīm tiek apstrādāti debitoru un kreditoru rēķini. 
<table>
<thead>
<tr>
<th>Scenārijs</th>
<th>Valstis</th>
<th>Funkcionalitātes izmaiņu apraksts</th>
</tr>
</thead>
<tbody>
<tr>
<td>Debitoru un kreditoru PVN datumi</td>
<td>Čehija, Polija</td>
<td>
<p>Kad preces tiek iegādātas no Eiropas Savienības (ES) valstīm, ir pienākums veikt PVN pašnovērtējumu:</p>
<ul>
<li>Pārdošanas PVN ir jāmaksā tajā PVN periodā, kad rēķins tika izrakstīts (dokumenta datumā).</li>
<li>Pirkšanas PVN nevar atskaitīt pirms dokumenta saņemšanas (PVN reģistra datuma).</li>
</ul>
<p>Lai atbalstītu šo scenāriju, ir jābūt konfigurētiem tālāk norādītajiem iestatījumiem.</p>
<ul>
<li>Lapā <strong>Kreditoru parādu parametri</strong> iespējojiet parametru <strong>EK iekšējais PVN</strong> un <strong>EK iekšējā PVN dokumenta datums</strong>.</li>
<li>Iestatiet divus PVN kodus — vienu, kam ir pozitīva PVN likme, un vienu, kam ir negatīva PVN likme.</li>
<li>Iestatiet PVN grupu, kas ietver gan pozitīvo, gan negatīvo PVN kodu. Negatīvajam PVN kodam parametru <strong>EK iekšējais PVN</strong> iestatiet uz <strong>Jā</strong>.</li>
</ul>
<p>Pēc sekmīgas iestatīšanas pirkumiem būs divas grāmatotās PVN transakcijas:</p>
<ul>
<li>Pozitīva transakcija, kuras virziens ir <strong>saņemamais PVN</strong> un kuras PVN reģistra datums ir vienāds ar datumu no rēķina grāmatošanas lapas.</li>
<li>Negatīva transakcija, kuras virziens ir <strong>maksājamais PVN</strong> un kuras PVN reģistra datums ir vienāds ar dokumenta datumu.</li>
</ul>
</td>
</tr>
<tr>
<td>Modificējiet pārdošanas dokumenta datumu.</td>
<td>Visas Austrumeiropas valstis</td>
<td><p>Projekta rēķinā varat modificēt lauku <strong>Dokumenta datums</strong>. Šis datums ir redzams izdrukātajā rēķinā.</p>
<p>Lauks <strong>Dokumenta datums</strong> ir arī lapā <strong>Rēķina grāmatošana</strong> un <strong>Brīva teksta rēķins</strong>. Pēc rēķina grāmatošanas dokumenta datums ir redzams rēķina virsrakstā.</p>
</td>
</tr>
<tr>
<td>Dokumenta datums valūtas maiņas kursiem</td>
<td>Polija, Ungārija, Čehija</td>
<td>
<p>Likumdošana paredz atšķirīgus noteikumus komercdarbības transakciju derīgu valūtas maiņas kursu atlasīšanai. Laukā <strong>Maiņas kursa datums</strong> lapā <strong>Debitoru parādu parametri</strong> un <strong>Parādu kreditoriem parametri</strong> varat atlasīt datumu, kas pirkumu un pārdošanas dokumentiem ir jāizmanto summām uzskaites valūtas aprēķinā. Datu ievadīšanas laikā sistēma izgūst transakcijas valūtas maiņas kursu, pamatojoties uz šo parametru.</p>
<blockquote>[!NOTE]<br>Ja lauku <strong>Maiņas kursa datums</strong> iestatāt uz <strong>Dokumenta datums (tikai ES tirdzniecība)</strong>, tad sistēma izmanto PVN grupu. PVN grupai cilnē <strong>Vispārīgi</strong> pastāv parametrs <strong>ES tirdzniecība</strong>. Ja opcija <strong>ES tirdzniecība</strong> PVN grupai ir pārslēgta uz <strong>Jā</strong> un ja šī PVN grupa pastāv dokumenta virsrakstā, tad valūtas maiņas kursu sistēma izgūst, pamatojoties uz dokumenta datumu. Ja opcija <strong>ES tirdzniecība</strong> šai PVN grupai ir iestatīta uz <strong>Nē</strong>, tad valūtas maiņas kursu sistēma izgūst, pamatojoties uz dokumenta grāmatošanas datumu.</blockquote>
</td>
</tr>
<tr>
<td>Darījumu veikšanas datumi, PVN reģistra datumi un dokumentu un PVN datuma kontrole</td>
<td>Polija, Ungārija, Čehija</td>
<td>
<p>Pārdošanas datums un dokumenta saņemšanas datums PVN pārskatiem ir jānorāda obligāti.</p>
<ul>
<li>Pārdošanas datums ir transakcijas izpildes datums debitoru parādos.</li>
<li>Dokumentu saņemšanas datums ir datums, kas apliecina tiesības pieprasīt PVN samazinājumu debitoru parādos. Katram saņemtajam dokumentam ir datums, kuru izmantot auditēšanas nolūkos.</li>
</ul>
<p>Ungārijas funkcionalitāte datumu termiņiem, Čehijas funkcionalitāte izpildes datumiem un Polijas funkcionalitāte PVN reģistra datumam ietver prasību par nodokļu informācijas ziņošanu, kas ir balstīta uz datumu, kurš atšķiras no grāmatošanas datuma.</p>
<p>Lauks <strong>PVN reģistra datums</strong> atbalsta šo prasību, un tas ir redzams vairāk nekā 20 lapās. Šīs lapas ietver žurnālus, pārdošanas pasūtījumus, pirkšanas pasūtījumus, brīva teksta rēķinus, kreditoru rēķinu žurnālus un projektu rēķinus. Atjauninot vai grāmatojot dokumentus, visi nodokļi tiek grāmatoti, izmantojot atbilstošo PVN reģistra datumu, un datums tiek ietverts tādās lapās kā, piemēram, debitoru un kreditoru rēķinu žurnālu lapas.</p>
<p>Čehijai lauks <strong>PVN reģistra datums</strong> grāmatošanas laikā var būt tukšs, ja tiek grāmatots atliktais PVN. Pretējā gadījumā šis lauks ir obligāts, un tas ir jāaizpilda.</p>
<p>Datuma validēšanas parametrus var iestatīt lapā <strong>PVN grupas</strong>.</p>
<ul>
<li>Parametrs <strong>PVN reģistra aizpildīšanas datums</strong> un <strong>Pārdošanas datuma aizpildīšana</strong> tiek izmantots kā noklusējuma aizpildīšanas metode atbilstošajiem datumiem. Ir pieejama arī manuāla ievade un vairākas automatizētas ievades metodes.</li>
<li>Lauks <strong>Obligātais pārdošanas datums</strong> norāda, vai pārdošanas datums ir jāievada pirms pārdošanas rēķina grāmatošanas.</li>
</ul>
<p>Lapā <strong>PVN reģistra transakcijas</strong> varat aizpildīt tukšos datumus, kas PVN reģistram paredzēti grāmatotajām nodokļu transakcijām.</p>
</td>
</tr>
<tr>
<td>PVN reģistra datumi, kas ietver atlikto nodokli</td>
<td>Ungārija</td>
<td>
<p>Ungārijas nodokļu noteikumi paredz, ka rēķini ir jāizveido vai nu izpildes laikā, vai ne vēlāk kā 15 dienas pēc izpildes.</p>
<p>Izpildes datums ir datums, kad tika sniegti pasūtītie pakalpojumi, vai datums, kad tika piegādāti pasūtītie krājumi. Kad atjaunināt vai grāmatojat dokumentus, visi nodokļi tiek grāmatoti, izmantojot atbilstošo PVN reģistra datumu, un šis datums tiek rādīts saistītajās lapās. Turklāt noteikumi pieprasa, lai PVN par pastāvīgi piegādātajiem pakalpojumiem, piemēram, īri, nomu, konsultācijām un apkuri, atbilstu tālāk norādītajiem kritērijiem.</p>
<ul>
<li>PVN ir jāgrāmato speciālā virsgrāmatas kontā un rēķina datumā.</li>
<li>PVN no speciālajiem kontiem ir jāpārsūta uz saņemamā PVN kontu vai uz maksājamā PVN kontu, un apmaksas datumā tas ir jāietver PVN pārskatā.</li>
</ul>
<p>Lai atbalstītu šīs prasības, virsgrāmatas grāmatojumus varat pārsūtīt uz atliktā ienākošā nodokļa kontu un atliktā izejošā nodokļa kontu. Taču vispirms ir jāizpilda tālāk norādītie priekšnosacījumi.</p>
<ul>
<li>Virsgrāmatas grāmatošanas grupās iestatiet virsgrāmatas kontu Atliktais maksājamais PVN un Atliktais saņemamais PVN.</li>
<li>Iespējojiet parametru <strong>Atliktais PVN</strong> attiecībā uz krājumu PVN grupām.</li>
</ul>
</td>
</tr>
<tr>
<td>Obligātais PVN datums</td>
<td>Polija</td>
<td>
<p>Varat pieprasīt, lai PVN reģistra datums tiktu ietverts pirkšanas un pārdošanas transakciju ierakstos. Tāpēc PVN reģistra datumu var iegūt pirms transakcijas grāmatošanas. Šī funkcionalitāte jums palīdz izvairīties no vairāku transakciju apstrādes perioda beigās.</p>
<p>Lauku <strong>PVN reģistra datums</strong> varat padarīt par obligātu, kad tiek grāmatotas debitoru vai kreditoru transakcijas. Lai šo lauku padarītu par obligātu, saistītajam debitora vai kreditora kontam aktivizējiet opciju <strong>Nepieciešams PVN datums</strong>.</p>
</td>
</tr>
</tbody>
</table>

