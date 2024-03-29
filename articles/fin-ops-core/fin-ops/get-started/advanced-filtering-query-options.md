---
title: Papildu filtrēšanas un vaicājumu sintakse
description: Šajā rakstu ir aprakstītas filtrēšanas un vaicājumu opcijas papildu filtra/kārtošanas dialogam un atbilstības operators filtra rūtī vai režģa kolonnas virsraksta filtriem.
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89175763357f4309c4eb7874d0068586c5d9e726
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123954"
---
# <a name="advanced-filtering-and-query-syntax"></a>Papildu filtrēšanas un vaicājumu sintakse

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā tēmā ir aprakstītas filtrēšanas un vaicājumu opcijas, kas ir pieejamas, ja rūts Filtrēšana dialoglodziņā Detalizētā filtrēšana/kārtošana vai režģa kolonnas filtros izmantojat operatoru **atbilst**.

## <a name="advanced-query-syntax"></a>Papildu vaicājumu sintakse

<table>
<thead>
<tr>
<th>Sintakse</th>
<th>Simbolu apraksts</th>
<th>apraksts</th>
<th>Piemērs</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>vērtība</em></td>
<td>Vienāds ar ievadīto vērtību.</td>
<td>Ierakstiet meklējamo vērtību.</td>
<td><strong>Smits</strong> atrod &quot;Smits&quot;.</td>
</tr>
<tr>
<td>!<em>vērtība</em> (izsaukuma zīme)</td>
<td>Nav vienāds ar ievadīto vērtību.</td>
<td>Ierakstiet izsaukuma zīmi un tad vērtību, kas jāizslēdz.</td>
<td><strong>!Smits</strong> atrod visas vērtības, izņemot vērtību &quot;Smits&quot;.</td>
</tr>
<tr>
<td><em>vērtība no</em>..<em>vērtība līdz</em> (divpunkte)</td>
<td>Starp divām vērtībām, kas atdalītas ar divpunkti</td>
<td>Ierakstiet, no kuras vērtības, pēc tam divus punktus un līdz kurai vērtībai.</td>
<td><strong>1..10</strong> atrod visas vērtības no 1 līdz 10. Tomēr virknes laukā <strong>A..C</strong> atrod visas vērtības, kas sākas ar &quot;A&quot; un &quot;B&quot;, un vērtības, kas ir pilnīgi vienādas ar &quot;C&quot;. Piemēram, šis vaicājums neatradīs &quot;Ca&quot;. Lai atrastu visas vērtības no &quot;A<em>&quot; līdz &quot;C</em>&quot;, ierakstiet <strong>A..D</strong>.</td>
</tr>
<tr>
<td>..<em>vērtība</em> (divpunkte)</td>
<td>Mazāks vai vienāds ar ievadīto vērtību.</td>
<td>Ierakstiet divus punktus un pēc tam vērtību.</td>
<td><strong>..1000</strong> atrod visus skaitļus, kas ir mazāki par vai vienādi ar 1000, piemēram, &quot;100&quot;, &quot;999,95&quot; un &quot;1000&quot;.</td>
</tr>
<tr>
<td><em>vērtība</em>.. (divpunkte)</td>
<td>Lielāks vai vienāds ar ievadīto vērtību.</td>
<td>Ierakstiet vērtību un tad divus punktu.</td>
<td><strong>1000..</strong> atrod visus skaitļus, kas ir lielāki par vai vienādi ar 1000, piemēram, &quot;1000&quot;, &quot;1000,01&quot; un &quot;1 000 000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>vērtība</em> (zīme “lielāks par”)</td>
<td>Lielāka par ievadīto vērtību.</td>
<td>Ierakstiet zīmi “lielāks par” (<strong>&gt;</strong>) un pēc tam vērtību.</td>
<td><strong>&gt;1000</strong> atrod visus skaitļus, kas ir lielāki par 1000, piemēram, &quot;1000,01&quot;, &quot;20 000&quot; un &quot;1 000 000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>vērtība</em> (zīme “mazāks par”)</td>
<td>Mazāka par ievadīto vērtību.</td>
<td>Ierakstiet zīmi “mazāks par” (<strong>&lt;</strong>) un pēc tam vērtību.</td>
<td><strong>&lt;1000</strong> atrod visus skaitļus, kas ir mazāki 1000, piemēram, &quot;999,99&quot;, &quot;1&quot; un &quot;-200&quot;.</td>
</tr>
<tr>
<td><em>vērtība</em>* (zvaigznīte)</td>
<td>Sākot no ievadītas vērtības.</td>
<td>Ierakstiet sākuma vērtību un pēc tam zvaigznīti (<strong>*</strong>).</td>
<td><strong>S*</strong> atrod jebkuru virkni, kas sākas ar &quot;S&quot;, piemēram, &quot;Stokholma&quot;, &quot;Sidneja&quot; un &quot;Sanfrancisko&quot;.</td>
</tr>
<tr>
<td>*<em>vērtība</em> (zvaigznīte)</td>
<td>Beidzas ar ievadīto vērtību.</td>
<td>Ierakstiet zvaigznīti un pēc tam beidzamo vērtību.</td>
<td><strong>*austrumi</strong> atrod jebkuru virkni, kas beidzas ar &quot;austrumi&quot;, piemēram, &quot;ziemeļaustrumi&quot; un &quot;dienvidaustrumi&quot;.</td>
</tr>
<tr>
<td>*<em>vērtība</em>* (zvaigznīte)</td>
<td>Satur ievadīto vērtību.</td>
<td>Ierakstiet zvaigznīti, pēc tam vērtību un vēl vienu zvaigznīti.</td>
<td><strong>*au*</strong> atrod jebkādu virkni, kas ietver &quot;au&quot;, piemēram, &quot;ziemeļaustrumi&quot; un &quot;dienvidaustrumi&quot;.</td>
</tr>
<tr>
<td>? (jautājuma zīme)</td>
<td>Satur vienu vai vairākas nezināmas zīmes.</td>
<td>Ierakstiet jautājuma zīmi nezināmās zīmes vietā vērtībā.</td>
<td><strong>Sm?ts</strong> atrod &quot;Smits&quot; un &quot;Smats&quot;.</td>
</tr>
<tr>
<td><em>vērtība</em>,<em>vērtība</em> (komats)</td>
<td>Atbilst vērtībām, kas atdalītas ar komatiem.</td>
<td>Ierakstiet visus kritērijus un atdaliet tās ar komatiem.</td>
<td><strong>A, D, F, G</strong> atrod &quot;A&quot;, &quot;D&quot;, &quot;F&quot; un &quot;G&quot;. <strong>10, 20, 30, 100</strong> atrod &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr>
<td>"" (divas dubultpēdiņas)</td>
<td>Atbilst tukšai vērtībai</td>
<td>Ierakstiet divas secīgas dubultās pēdiņas, lai filtrētu tukšas vērtības šajā laukā.</td>
<td>Divas secīgas dubultās pēdiņas (<strong>""</strong>) atrod rindas, kurām pašreizējai kolonnai nav vērtības.</td>
</tr>
<tr>
<td>(<span class="code">Finanšu un operāciju vaicājums</span>) (finanšu un operāciju vaicājums iekavās)</td>
<td>Atbilst definētajam vaicājumam.</td>
<td>Ierakstiet vaicājumu kā SQL priekšrakstu iekavās, izmantojot finanšu un operāciju vaicājuma valodu.</td>
  <td><strong><span class="code">((AccountNum kā "US *") & & (DirPartyTable.Name piemēram, "* CONT"))</span></strong><br><br> 
       piemērs sintaksei filtra nosacījumam laukā no saknes datu avota, kā arī laukā no cita datu avota (visu klientu lapai)</td>
</tr>
<tr>
<td>O</td>
<td>Šodienas datums</td>
<td><strong>T</strong> veida.</td>
<td><strong>T</strong> atbilst šodienas datumam.</td>
</tr>
<tr>
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metode iekavās)</td>
<td>Atbilstība metodes <strong>SysQueryRangeUtil</strong> parametru norādītajai vērtībai vai vērtību diapazonam</td>
<td>Ierakstiet metodi <strong>SysQueryRangeUtil</strong>, kurai ir parametri, kas norāda vērtību vai vērtību diapazonu.</td>
<td>
<ol>
<li>Noklikšķiniet uz <strong>Debitoru parādi</strong> &gt; <strong>Rēķini</strong> &gt; <strong>Atvērtie debitoru rēķini</strong>.</li>
<li>Nospiediet taustiņu kombināciju Ctrl+Shift+F3, lai atvērtu lapu <strong>Uzziņas</strong>.</li>
<li>Cilnē <strong>Diapazons</strong> noklikšķiniet uz <strong>Pievienot</strong>.</li>
<li>Laukā <strong>Tabula</strong> atlasiet <strong>Neapmaksātās debitora darbības</strong>.</li>
<li>Laukā <strong>Lauks</strong> atlasiet <strong>Izpildes datums</strong>.</li>
<li>Laukā <strong>Kritēriji</strong> ievadiet <strong>(yearRange(-2,0))</strong>.</li>
<li>Noklikšķiniet uz <strong>OK</strong>. Saraksta lapa tiek atjaunināta, un tajā ir uzskaitīti kritērijiem atbilstoši ievadītie rēķini. Šajā piemērā ir uzskaitīti rēķini, kas bija jāmaksā iepriekšējo divu gadu laikā.</li>
</ol>
Papildinformāciju, kā arī vairākus piemērus par <strong>SysQueryRangeUtil</strong> datuma metodēm skatiet tabulā nākamajā sadaļā.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Papildu datumu vaicājumi, kas lieto SysQueryRangeUtil metodes

<table>
<thead>
<tr>
<th>Metode</th>
<th>Apraksts</th>
<th>Piemērs</th>
</tr>
</thead>
<tbody>
<tr>
<td>Diena (_relativeDays=0)</td>
<td>Atrodiet datumu, kas atbilst sesijas datumam. Pozitīvās vērtības norāda turpmākos datumus, bet negatīvas vērtības norāda iepriekšējos datumus.</td>
<td>
<ul>
<li><strong>Rīt</strong> — ievadiet <strong>(Day(1))</strong>.</li>
<li><strong>Šodien</strong> — ievadiet <strong>(Day(0))</strong>.</li>
<li><strong>Vakar</strong> — ievadiet <strong>(Day(-1))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Atrodiet datumu diapazonu, kas atbilst sesijas datumam. Pozitīvās vērtības norāda turpmākos datumus, bet negatīvas vērtības norāda iepriekšējos datumus.</td>
<td>
<ul>
<li><strong>Pēdējās 30 dienas</strong> — ievadiet <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Iepriekšējās 30 dienas un nākamās 30 dienas</strong> — ievadiet <strong>(DayRange(-30,30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Atrast visus datumus pēc norādītā atbilstošā datuma.</td>
<td>
<ul>
<li><strong>Vairāk nekā 30 dienas no šodienas</strong> — ievadiet <strong>(GreaterThanDate(30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Atrodiet visus datumu/laika ierakstus pēc pašreizējā laika.</td>
<td>
<ul>
<li><strong>Visi turpmākie datumi/laiki</strong> — ievadiet <strong>(GreaterThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Atrodiet visus datumus pirms norādītā atbilstošā datuma.</td>
<td>
<ul>
<li><strong>Mazāk nekā septiņas dienas no šodienas</strong> — ievadiet <strong>(LessThanDate(7))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Atrodiet visus datumu/laika ierakstus pirms pašreizējā laika.</td>
<td>
<ul>
<li><strong>Vis iepriekšējie datumi/laiki</strong> — ievadiet <strong>(LessThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Atrodiet pašreizējo mēnesi datumu diapazonā, kurā norādīti mēneši.</td>
<td>
<ul>
<li><strong>Iepriekšējie divi mēneši</strong> — ievadiet <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Nākamie trīs mēneši</strong> — ievadiet <strong>(MonthRange(0,3))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Atrodiet pašreizējo gadu datumu diapazonā, kurā norādīti gadi.</td>
<td>
<ul>
<li><strong>Nākamais gads</strong> — ievadiet <strong>(YearRange(0, 1))</strong>.</li>
<li><strong>Iepriekšējais gads</strong> — ievadiet <strong>(YearRange(-1,0))</strong>.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
