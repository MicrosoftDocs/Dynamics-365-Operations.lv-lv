---
title: Mazie kases posteņi Austrumeiropai un Krievijai
description: Šajā tēmā ir sniegta informācija par mazo kases posteņu funkcionalitāti, kas lietotājiem Igaunijā, Lietuvā, Čehijā, Ungārijā, Latvijā, Polijā un Krievijā ļauj sistēmā atainot kases operācijas.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.reviewer: kfend
ms.custom: 268504
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8d301cb7b16960d9f239719841516ca6354381c0011d0b2d8302f8b85012ed1e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733592"
---
# <a name="petty-cash-for-eastern-europe-and-russia"></a>Mazie kases posteņi Austrumeiropai un Krievijai

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par mazo kases posteņu funkcionalitāti, kas lietotājiem Igaunijā, Lietuvā, Čehijā, Ungārijā, Latvijā, Polijā un Krievijā ļauj sistēmā atainot kases operācijas.

Mazo kases posteņu funkcionalitāti varat izmantot, lai automatizētu kases operācijas ieņēmumiem un izdevumiem, primāro dokumentu veidošanai un saistīto pārskatu drukāšanai. Mazo kases posteņu funkcionalitāte jums ļauj veikt tālāk minētās operācijas.

-   Uzskaitīt pieejamo kases līdzekļu ieņēmumus un izdevumus.
-   Ģenerēt tipiskās kases formas: kases ieņēmumu orderus, kases izdevumu orderus un reģistrācijas žurnālu kases orderiem.
-   Kontrolēt maksimālo skaidras naudas summu, kas ir atļauta operācijām ar debitoriem, kreditoriem un tamlīdzīgi.
-   Sistēmā kases operācijas atainot dažādās valūtās.
-   Ārvalstu valūtā veikto kases operāciju summas konvertēt uz noklusējuma valūtu, lai varētu veidot uzskaites pārskatus.
-   Ģenerēt pārskatu **Kases grāmata** un kasiera pārskatu.

## <a name="prerequisites"></a>Priekšnosacījumi
Pirms sākat varat izmantot mazo kases posteņu funkcionalitāti, ir jāizpilda tālāk minētie priekšnosacījumi.

-   Iestatiet kases kontus.
-   Iestatiet kases grāmatošanas metodes.
-   Iestatiet numuru sērijas kases dokumentu numurēšanai.
-   Iestatiet noklusējuma vērtības kases un bankas vadības parametriem.
-   Iestatiet kases žurnālu nosaukumus virsgrāmatā.

### <a name="set-up-cash-accounts"></a>Iestatīt kases kontus

Lai iestatītu kontu Kase, atveriet sadaļu **Kases un bankas vadība** &gt; **Bankas konti** &gt; **Kases konti** un ievadiet tālāk norādīto informāciju.

| Lauks                 | Apraksts                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| Kase                  | Ievadiet kodu, ar ko identificēt šo kases kontu (kasi).                                                                    |
| Nosaukums                  | Ievadiet kases konta aprakstu.                                                                             |
| Valūta              | Atlasiet noklusējuma valūtas kodu kases transakcijām.                                                              |
| Numuru sēriju grupa | Ja kases dokumentu numerācijai ir jāatšķiras no parametros norādītās numerācijas, ievadiet kodu. |
| Dažādas valūtas       | Atzīmējiet šo izvēles rūtiņu, lai ļautu grāmatot valūtas, kas atšķiras no uzskaites valūtas.                     |
| Negatīvs atlikums kasē         | Atzīmējiet šo izvēles rūtiņu, lai ļautu izmantot negatīvas kases bilances jebkurā valūtā.                                               |

Lai kādam kases kontam iestatītu kases bilances kontroles kārtulas, atlasiet kases kontu un pēc tam darbību rūtī, cilnē **Kases konts**, grupā **Atlikuma limits** noklikšķiniet uz **Atlikuma limits**. Ievadiet tālāk aprakstīto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valūtas tips</td>
<td>Atlasiet valūtas tipu no tālāk uzskaitītajiem.
<ul>
<li><strong>Uzskaites valūta</strong> — izmantot uzņēmuma pamata valūtas kodu.</li>
<li><strong>Norādītā valūta</strong> — izmantot valūtas kodu, kas atšķiras no uzņēmuma pamata valūtas koda.</li>
</ul></td>
</tr>
<tr class="even">
<td>Valūta</td>
<td>Ja laukā <strong>Valūtas tips</strong> atlasījāt vērtību <strong>Norādītā valūta</strong>, tad atlasiet kādu valūtas kodu. Šis lauks ir nepieejams, ja laukā <strong>Valūtas tips</strong> atlasījāt vērtību <strong>Uzskaites valūta</strong>.</td>
</tr>
<tr class="odd">
<td>Atlikuma limita veids</td>
<td>Atlasiet vienu no tālāk aprakstītajām pieejamajām vērtībām.
<ul>
<li><strong>Maksimums</strong> — šim kases kontam kases atlikums nedrīkst pārsniegt summu <strong>Atlikuma limits</strong> (augstākā vērtība).</li>
<li><strong>Minimums</strong> — šim kases kontam kases atlikums nedrīkst būt zemāks par summu <strong>Atlikuma limits</strong> (zemākā vērtība).</li>
</ul></td>
</tr>
<tr class="even">
<td>Pārbaudīt atlikuma limitu</td>
<td>No nākamajām opcijām atlasiet, kas kases dokumentiem notiek apstiprināšanas procesa laikā, ja šim kases kontam tiek pārsniegta summa <strong>Atlikuma limits</strong>.
<ul>
<li><strong>Pieņemt</strong> — limits var tikt pārsniegts.</li>
<li><strong>Brīdinājums</strong> — limits var tikt pārsniegts, bet lietotājam tiek parādīts brīdinājuma ziņojums. Kases dokuments tiek ratificēts vai apstiprināts.</li>
<li><strong>Kļūda</strong> — nedrīkst&#39;pārsniegt ierobežojumu. Lietotājs saņem kļūdas ziņojumu, un kases dokuments netiek&#39;ratificēts vai apstiprināts.</li>
</ul>
Papildinformāciju par kases dokumentu apstiprināšanas procesu skatiet tālāk šīs tēmas sadaļā &quot;Kases transakciju apstiprināšana un grāmatošana&quot;.</td>
</tr>
<tr class="odd">
<td>Atlikuma limits</td>
<td>Ievadiet limitu kases kontu atlikumam. Šai summai ir jābūt jūsu norādītajā valūtā.</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a>Iestatīt kases grāmatošanas metodes

Kases grāmatošanas metodes definē grāmatojumus virsgrāmatā. Lai iestatītu kases grāmatošanas metodi, dodieties uz **Kases** **un bankas pārvaldība** &gt; **Iestatīšana** &gt; **Kases grāmatošanas metodes** un atlasiet vai izveidojiet grāmatošanas metodi. Ievadiet tālāk aprakstīto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Derīgs</td>
<td>Atlasiet, vai grāmatošanas metode attiecas uz konkrētu kases kontu vai uz visiem kases kontiem.
<ul>
<li><strong>Tabula</strong> — ja kases kontam pastāv kāda grāmatošanas metodes rinda, tad kases transakciju grāmatošanai tiek lietota šī rinda.</li>
<li><strong>Visi</strong> — šim kases kontam nav grāmatošanas metodes rindas.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kase</td>
<td>Ja laukā <strong>Derīgs</strong> atlasījāt vērtību <strong>Tabula</strong>, norādiet kases kontu. Šis lauks paliek tukšs, ja laukā <strong>Derīgs</strong> atlasījāt vērtību <strong>Visi</strong>.</td>
</tr>
<tr class="odd">
<td>Virsgrāmatas konts</td>
<td>Ievadiet numuru virsgrāmatai, kuru šim kases kontam lietot ka summas kontu.</td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a>Iestatīt numuru sērijas kases dokumentiem

Lai iestatītu numuru sērijas kases dokumentiem, dodieties uz **Kases un bankas vadība** &gt; **Iestatīšana** &gt; **Kases un bankas vadības parametri**. Cilnē **Numuru sērija** norādiet numuru sēriju kodus dokumentiem **Kases ieņēmumu orderi**, **Kases izdevumu orderi**, **Kases storno dokuments** un **Valūtas pārrēķins**, un vienumam **Kases pārskata numurs**.

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a>Iestatīt noklusējuma vērtības kases un bankas vadības parametriem

Lai iestatītu noklusējuma vērtības kases un bankas vadības parametriem mazo kases posteņu funkcionalitātei, dodieties uz **Kases un bankas vadība** &gt; **Iestatīšana** &gt; **Kases un bankas vadības parametri**. Cilnē **Kase** ievadiet tālāk norādīto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kase</td>
<td>Atlasiet noklusējuma kases kontu žurnālos.</td>
</tr>
<tr class="even">
<td>Kases grāmatošana</td>
<td>Ievadiet noklusējuma kases grāmatošanas metodi, kas tiek lietota, ja nav norādīta neviena cita grāmatošanas metode.</td>
</tr>
<tr class="odd">
<td>Dokumentu numuru kontrole</td>
<td>Atlasiet, kas notiek, ja kases dokumenta pārbaudes laika tiek konstatēti numuru dublikāti.
<ul>
<li>Neatļaut vienādus dokumentu numurus</li>
<li>Neatļaut kopijas finanšu gada ietvaros</li>
<li>Atļaut vienādus dokumentu numurus</li>
<li>Brīdināt dublēšanās gadījumā</li>
</ul></td>
</tr>
<tr class="even">
<td>Pārbaudīt operāciju limitu</td>
<td>Norādiet, kas notiek, ja tiek pārsniegts operācijām ar kontrahentiem noteiktais limits.
<ul>
<li><strong>Pieņemt</strong> — limits var tikt pārsniegts.</li>
<li><strong>Brīdinājums</strong> — limits var tikt pārsniegts, bet lietotājam tiek parādīts brīdinājuma ziņojums. Šī operācija tiek grāmatota.</li>
<li><strong>Kļūda</strong> — nedrīkst&#39;pārsniegt ierobežojumu. Lietotājs saņem kļūdas ziņojumu, un operācija netiek&#39;grāmatota.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pārbaudes metode</td>
<td>Atlasiet pārbaudes metodi, kas tiek lietota, lai operācijām kontrolētu pārsniegšanas limitu summas.
<ul>
<li><strong>Operācija</strong> — pārbaude tiek veikta katrai transakcijai</li>
<li><strong>Līgums</strong> — pārbaude tiek veikta katrai transakcijai, kam ir norādīts līgums ar kontrahentu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Operāciju limits</td>
<td>Ievadiet maksimālo summu, kas kasē ir atļauta operācijām ar kontrahentiem.</td>
</tr>
<tr class="odd">
<td>Grāmatošana agrākā datumā</td>
<td>Atzīmējiet šo izvēles rūtiņu, lai iespējotu kases transakciju grāmatošanu pirms kases transakcijas pēdējā datuma.</td>
</tr>
<tr class="even">
<td>Dimensijas</td>
<td>Ievadiet dimensijas laukos <strong>Nodaļas kods</strong>, <strong>Analītiskais kods</strong> un <strong>Mērķa kods</strong>. Kases dokumentu drukāšanas forma atainos šo informāciju.</td>
</tr>
<tr class="odd">
<td>Lietot ratifikācijas statusu</td>
<td>Atzīmējiet šo izvēles rūtiņu, lai kases dokumentiem apstiprināšanas procesa laikā lietotu papildu statusu <strong>Ratificēts</strong>. (Papildinformāciju skatiet sadaļā &quot;Kases transakciju apstiprināšana un grāmatošana&quot;.)</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a>Iestatīt kases žurnālu nosaukumus virsgrāmatā

Lai izveidotu žurnālu kases transakciju grāmatošanai, dodieties uz **Virsgrāmata** &gt; **Žurnāla iestatīšana** &gt; **Žurnālu nosaukumi** un izveidojiet jaunu ierakstu. Laukā **Žurnāla tips** norādiet **Kase**. Definējiet citus nepieciešamos noklusējuma žurnāla parametrus.

## <a name="daily-cash-operations-via-a-slip-journal"></a>Ikdienas kases operācijas, izmantojot orderu žurnālu
Lai izveidotu kases dokumentu, izmantojot orderu žurnālu, dodieties uz **Kases un bankas vadība** &gt; **Kases transakcijas** &gt; **Orderu žurnāls** un izveidojiet jaunu žurnālu. Darbību rūtī noklikšķiniet uz **Rindas**. Pievienojiet jaunu rindu un ievadiet tālāk norādīto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Datums</td>
<td>Ievadiet darījuma datumu.</td>
</tr>
<tr class="even">
<td>Konts</td>
<td>Atlasiet kases kontu. Pēc noklusējuma kases konts ir norādīts sadaļā Kases un bankas vadības parametri.</td>
</tr>
<tr class="odd">
<td>Apraksts</td>
<td>Ievadiet skaidrojošu tekstu par transakciju.</td>
</tr>
<tr class="even">
<td>Debetkarte</td>
<td>Ievadiet kases dokumenta summu vienā no tālāk norādītajiem laukiem.
<ul>
<li><strong>Debets</strong> — izmantojiet šo lauku, lai reģistrētu kases ieņēmumus un kases ieņēmumu orderi.</li>
<li><strong>Kredīts</strong> — izmantojiet šo lauku, lai reģistrētu kases izdevumus un kases izdevumu orderi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Korespondējošā konta tipa korespondējošais konts</td>
<td>Atlasiet korespondējošā konta tipu un korespondējošā konta numuru.</td>
</tr>
<tr class="even">
<td>Valūta</td>
<td>Atlasiet transakcijas valūtas kodu.</td>
</tr>
<tr class="odd">
<td>Dokuments</td>
<td>Šis lauks tiek aizpildīts automātiski, pamatojoties uz žurnāla iestatīšanu.</td>
</tr>
<tr class="even">
<td>Pasūtījuma numurs</td>
<td>Ja šim kases kontam nav norādīta neviena cita numuru sērija, šis lauks tiek aizpildīts automātiski, pamatojoties uz parametros norādīto numuru sēriju. Ja nepieciešams, šajā lauka pasūtījuma numuru varat ievadīt manuāli. Lai nepieļautu kases dokumentu numerācijas nesakritības, tiek lietots šāds kontroles kritērijs: tāda kases dokumenta numurs, kura operācijas datums ir agrāks, nedrīkst&#39;būt lielāks par tāda kases dokumenta numuru, kura operācijas datums ir vēlāks. Ja šis kontroles kritērijs nav&#39;nepieciešams, tad kases un bankas vadības parametru sadaļā atzīmējiet izvēles rūtiņu <strong>Grāmatošana agrākā datumā</strong>.</td>
</tr>
<tr class="odd">
<td>Apstiprināšanas statuss</td>
<td>Pirmās transakcijas statuss ir <strong>Nav</strong>. Papildinformāciju par transakcijas statusa iestatīšanu skatiet sadaļā &quot;Kases transakciju apstiprināšana un grāmatošana&quot;.</td>
</tr>
<tr class="even">
<td>Dokumenta tips</td>
<td>Lauks cilnē <strong>Kases orderis</strong> tiek automātiski aizpildīts tālāk aprakstītajā veidā, pamatojoties uz summu, kuru ievadījāt šim kases dokumentam.
<ul>
<li><strong>Kases ieņēmumu orderis</strong> — šī vērtība tiek lietota, ja kases kontam summu ievadījāt laukā <strong>Debets</strong>.</li>
<li><strong>Kases izdevumu orderis</strong> — šī vērtība tiek lietota, ja kases kontam summu ievadījāt laukā <strong>Kredīts</strong>.</li>
<li><strong>Labojums</strong> — kases kontam ievadījāt negatīvu summu laukā <strong>Debets</strong> vai laukā <strong>Kredīts</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PVN grupa</td>
<td>Norādiet PVN kodu grupu, ko izmantot operācijas nodokļu aprēķināšanai.</td>
</tr>
<tr class="even">
<td>Krājumu PVN grupa</td>
<td>Norādiet krājumu PVN grupu, ko izmantot operācijas nodokļu aprēķināšanai.</td>
</tr>
<tr class="odd">
<td>Iemesls</td>
<td>Cilnē <strong>Kases orderis</strong> ievadiet tekstu, kas apraksta transakcijas priekšmetu. Šis teksts tiks drukāts kases ordera pārskata formā.</td>
</tr>
<tr class="even">
<td>Dokumenta datums</td>
<td>Ievadiet aprakstu, numuru un datumu primārajam dokumentam, kurš ir transakcijas iemesls (piemēram, avansa pārskati, rēķins vai pasūtījums).</td>
</tr>
<tr class="odd">
<td>Pārstāvja tips</td>
<td>Šim laukam var būt tālāk aprakstītās vērtības.
<ul>
<li><strong>Nodarbinātais</strong> — uzmeklēšanas sadaļā <strong>Pārstāvis</strong> ir ietverts darbinieku&#39;saraksts, ja ir iestatīta lauka <strong>Korespondējošais konts</strong> vērtība <strong>Virsgrāmata</strong> vai <strong>Banka</strong>, vai kontrahenta kontaktpersonu saraksts, ja ir iestatīta lauka <strong>Korespondējošais konts</strong> vērtība <strong>Debitors</strong> vai <strong>Kreditors</strong>. Lai iestatītu pārstāvjus, dodieties uz <strong>Pamata</strong> &gt; <strong>Iestatīšana</strong> &gt; <strong>Kontaktpersonas</strong> &gt; <strong>Kontaktpersona</strong>.</li>
<li><strong>Cits</strong> — uzmeklēšanā <strong>Pārstāvis</strong> ir saraksts ar citiem debitoriem. Lai iestatītu saņēmējus, kas netiek&#39;rādīti tabulā <strong>Debitori</strong> vai <strong>Kreditori</strong> , pārejiet uz sadaļu uz <strong>Virsgrāmata</strong> &gt; <strong>Saņēmēji</strong>. Šis tips ir pieejams tikai Latvijai. (Ir jābūt iespējotai konfigurācijas atslēgai <strong>CSELatvia</strong>.)</li>
<li><strong>Kreditors</strong> — uzmeklēšanā <strong>Pārstāvis</strong> ir saraksts ar kreditoriem. Lai iestatītu kreditorus, dodieties uz <strong>Parādi kreditoriem</strong> &gt; <strong>Kreditori</strong>.</li>
<li><strong>Debitors</strong> — uzmeklēšanā <strong>Pārstāvis</strong> ir saraksts ar debitoriem. Lai iestatītu debitorus, dodieties uz <strong>Debitoru parādi</strong> &gt; <strong>Debitori</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Pārstāvis</td>
<td>Atlasiet pārstāvi, kura tips atbilst laukā <strong>Pārstāvja tips</strong> norādītajam tipam.</td>
</tr>
<tr class="odd">
<td>Personas vārds</td>
<td>Šis lauks tiek aizpildīts automātiski, pamatojoties uz laukiem <strong>Korespondējošais konts</strong> un <strong>Pārstāvis</strong>. Kases orderu drukāšanas forma atainos šo informāciju.</td>
</tr>
<tr class="even">
<td>Personas apliecība</td>
<td>Šis lauks tiek aizpildīts automātiski, pamatojoties uz attiecīgās kontaktpersonas (pārstāvja) personas apliecības datiem. Ja laukam <strong>Korespondējošā konta tips</strong> ir iestatīta vērtība <strong>Avansa turētājs</strong> un laukam <strong>Korespondējošais konts</strong> ir iestatīts darbinieka numurs, tad kases ieņēmumus vai izdevumus var veikt no darbinieka vai uz darbinieku. Tādā gadījumā lauks <strong>Personas apliecība</strong> tiek aizpildīts automātiski, izmantojot datus personas apliecībai no tabulas <strong>Darbinieks</strong> (<strong>Darbinieku uzskaite</strong> &gt; <strong>Darbinieku tabula</strong>).</td>
</tr>
<tr class="odd">
<td>Nolūks</td>
<td>Tabulā <strong>Nolūks</strong> attiecīgajai transakcijas summai definējiet vienu vai vairākus mērķa kodus. Atlasiet mērķa kodu laukā <strong>Nolūks</strong> un ievadiet skaidrojumu laukā <strong>Transakcijas teksts</strong>. Laukā <strong>Summa</strong> ievadiet summu transakcijas valūtā. Laukā <strong>Procenti</strong> tiek rādīta mērķa summas attiecība pret kopējo transakcijas summu, izteikta procentu veidā.</td>
</tr>
<tr class="even">
<td>Atgādinājums</td>
<td>Atlikusī summa, kas ir aprēķināta. Ņemiet vērā, ka kopējā transakcijas summa ir jāpiešķir mērķa kodiem.</td>
</tr>
<tr class="odd">
<td>Amatpersonas</td>
<td>Cilnē <strong>Amatpersonas</strong> norādiet atbildīgo personu vārdus, uzvārdus un amatus: Direktors, Galvenais grāmatvedis un Kasieris. Vērtības <strong>Amats</strong> tiek noteiktas pēc amatpersonu iestatīšanas lapas <strong>Amatpersonas</strong> cilnēs <strong>Vispārīgi</strong> un <strong>Virsgrāmata</strong> (<strong>Pamata</strong> &gt; <strong>Iestatīšana</strong> &gt; <strong>Kontaktpersonas</strong> &gt; <strong>Amatpersonas</strong>).</td>
</tr>
<tr class="even">
<td>Priekšapmaksa</td>
<td>Atzīmējiet šo izvēles rūtiņu, ja transakcija ir priekšapmaksa.</td>
</tr>
<tr class="odd">
<td>Grāmatošanas metode</td>
<td>Ievadiet grāmatošanas metodi attiecīgajam kases kontam. Pēc noklusējuma tiek lietota grāmatošanas metode, kas ir norādīta sadaļā Kases un bankas vadības parametri.</td>
</tr>
<tr class="even">
<td>Korespondējošo kontu grāmatošanas metode</td>
<td>Ievadiet grāmatošanas metodi atlasītajam korespondējošajam kontam.</td>
</tr>
<tr class="odd">
<td>Kopējā summa</td>
<td>Lapas apakšā esošajā lauku grupā <strong>Kopējā summa</strong> laukā <strong>Ieņēmumu</strong> tiek rādīta kopsumma, kas ir aprēķināta visiem pašreizējā žurnālā ievadītajiem kases ieņēmumu orderiem, un laukā <strong>Izdevumu</strong> tiek rādīta kopsumma visiem kases izdevumu orderiem.</td>
</tr>
</tbody>
</table>

Lai pārbaudītu žurnālu ierakstus, darbību rūtī noklikšķiniet uz **Validēt**.

## <a name="daily-cash-operations-via-a-general-journal"></a>Ikdienas kases operācijas, izmantojot virsgrāmatas žurnālu
Lai izveidotu kases transakciju, izmantojot virsgrāmatas žurnālu, dodieties uz **Virsgrāmata** &gt; **Žurnāla ieraksti** &gt; **Virsgrāmatas žurnāli** un izveidojiet jaunu žurnālu. Darbību rūtī noklikšķiniet uz **Rindas**. Pievienojiet jaunu rindu un ievadiet tālāk norādīto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Datums</td>
<td>Ievadiet darījuma datumu.</td>
</tr>
<tr class="even">
<td>Konta veids</td>
<td>Atlasiet vienumu <strong>Mazie kases posteņi</strong>.</td>
</tr>
<tr class="odd">
<td>Konts</td>
<td>Atlasiet kases konta numuru.</td>
</tr>
<tr class="even">
<td>Darbības teksts</td>
<td>Ievadiet skaidrojošu tekstu par transakciju.</td>
</tr>
<tr class="odd">
<td>Debetkarte</td>
<td>Ievadiet kases dokumenta summu vienā no tālāk norādītajiem laukiem.
<ul>
<li><strong>Debets</strong> — izmantojiet šo lauku, lai reģistrētu kases ieņēmumus un kases ieņēmumu orderi.</li>
<li><strong>Kredīts</strong> — izmantojiet šo lauku, lai reģistrētu kases izdevumus un kases izdevumu orderi.</li>
</ul></td>
</tr>
<tr class="even">
<td>Korespondējošā konta tipa korespondējošais konts</td>
<td>Atlasiet korespondējošā konta tipu un korespondējošā konta numuru.</td>
</tr>
<tr class="odd">
<td>Valūta</td>
<td>Atlasiet transakcijas valūtas kodu.</td>
</tr>
</tbody>
</table>

Cilnē **Rēķins** varat norādīt grāmatošanas metodes atlasītajam kontam un korespondējošajam kontam. Ja reģistrētā transakcija ir priekšapmaksa, tad cilnē **Maksājums** atzīmējiet izvēles rūtiņu **Priekšapmaksa**. Lauku grupā **Pārstāvis** aizpildiet laukus tāpat, kā to izdarījāt orderu žurnāla rindās, lai izdrukātu pārskatā **Kase**. Lai pārbaudītu žurnālu ierakstus, darbību rūtī noklikšķiniet uz **Validēt**.

## <a name="cash-transaction-approval-and-posting"></a>Kases transakciju apstiprināšana un grāmatošana
Kases transakcijām var lietot šādus statusus: **Nav**, **Ratificēts**, **Apstiprināts** un **Noraidīts**. Parametrs **Lietot ratifikācijas statusu** cilnes **Kase** kopsavilkuma cilnē **Apstiprinājums**, kurš atrodas sadaļā **Kases un bankas vadība** &gt; **Iestatīšana** &gt; **Kases un bankas vadības parametri**, jums ļauj aktivizēt divus papildu statusus: **Ratificēts** un **Noraidīts**. Ratifikācija ir piemērota, kad tiek izdoti kases dokumenti un kad kases ieņēmumus vai izdevumus koplieto divi darbinieki: grāmatvedis un kasieris. Funkcija **Atiestatīt statusu** maina pašreizējās transakcijas statusu. **Apstiprināts** kļūst par **Ratificēts**, un **Ratificēts** kļūst par **Nav**. Kases žurnāla ierakstus var rediģēt tikai tad, kad to statuss ir **Nav**. Kases transakcijas var noraidīt tikai tad, kad to transakcijas statuss ir **Ratificēts**. Noraidītie kases dokumenti ir iekļauti pārskatā **Kases dokumentu reģistrācijas žurnāls**, bet tie netiek atspoguļoti pārskatā **Kases grāmata**. Lai ratificētu kādu transakciju, atlasiet atbilstošo orderu žurnāla rindu un pēc tam noklikšķiniet uz **Dokumentu apstiprinājums** &gt; **Ratificēt**. Tiek ģenerēts kārtas numurs, pamatojoties uz norādīto numuru sēriju. Transakcijas statuss mainās uz **Ratificēts**, un jūs vairs nevarat rediģēt šo žurnāla rindu. Kases konta atlikums nemainās. Lai noraidītu kādu kases dokumentu, noklikšķiniet uz **Dokumentu apstiprinājums** &gt; **Noraidīt**. Šī opcija ir pieejama tikai dokumentiem, kuru statuss ir **Ratificēts**. Lai apstiprinātu kādu transakciju, atlasiet atbilstošo orderu žurnāla rindu un pēc tam noklikšķiniet uz **Dokumentu apstiprinājums** &gt; **Apstiprināt**. Statuss **Apstiprināts** norāda, ka kases līdzekļi ir saņemti vai iztērēti. Kases atlikums ir mainījies. Kases transakciju var grāmatot. Lai atceltu statusu **Apstiprināts** un atiestatītu uz statusu **Nav**, noklikšķiniet uz **Dokumentu apstiprinājums** &gt; **Atiestatīt statusu**. Grāmatot var tikai apstiprinātas kases transakcijas. Lai grāmatotu žurnālu, noklikšķiniet uz **Grāmatot** &gt; **Grāmatot**.

## <a name="print-a-cash-order"></a>Drukāt kases orderi
Lai drukātu kases orderi, atlasiet orderu žurnāla rindu un pēc tam darbību rūtī noklikšķiniet uz **Drukāt** &gt; **Kases ordera pārskats**. Sistēma ģenerē drukāšanas formu kases ieņēmumu orderim vai kases izdevumu orderim, ņemot vērā to, vai atlasītajai rindai summa tika ievadīta laukā **Debets** vai laukā **Kredīts**.

-   Ja summa ir norādīta laukā **Debets**: Kases ieņēmumu orderis
-   Ja summa ir norādīta laukā **Kredīts**: Kases izdevumu orderis

Drukāt var orderu žurnāla rindas, kuru statuss ir **Ratificēts**, **Apstiprināts** vai **Noraidīts**. Kases orderu dokumentus varat drukāt arī sadaļā **Kases un bankas vadība** &gt; **Pieprasījumi un pārskati** &gt; **Kases orderis**.

## <a name="periodic-tasks"></a>Periodiskie uzdevumi
Tālāk norādītos uzdevumus var izpildīt šeit: **Kases un bankas vadība** &gt; **Periodiskie uzdevumi**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Periodiskais uzdevums</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pārbaudīt atlikuma limitu</td>
<td>Pārbaudiet atlikumu atlasītajam kases kontam noteiktajā datumā un parādiet rezultātu informatīvā ziņojumā. Atlikuma aprēķina var skaitīt tikai apstiprinātās transakcijas. Netiek&#39;ņemtas vērā transakcijas, kas ir atzīmētas ar statusu <strong>Algām</strong>.</td>
</tr>
<tr class="even">
<td>Skaidras naudas atlikuma pārrēķins</td>
<td>Izmantojiet šo uzdevumu, lai pārliecinātos, ka virsgrāmatas bilances kases kontiem atbilst kases atlikumam.</td>
</tr>
<tr class="odd">
<td>Kases pārskata izveidošana (tikai Polijai)</td>
<td>Izveidojiet pārskatu <strong>Kase</strong>. Pārskata <strong>Kase</strong> numurs tiek ģenerēts, pamatojoties uz numuru sēriju, ko iestatījāt vienumam <strong>Pārskata numurs</strong>. Uzdevumam paredzētajā dialoglodziņā vienumam <strong>Beigu datums</strong> norādiet pēdējo datumu, kurā kases transakcijas ir jāskaita pārskatam <strong>Kase</strong>. Izmantojiet funkciju <strong>Filtrēt</strong> cilnē <strong>Iekļaujamie ieraksti</strong>, lai norādītu papildu kritērijus kases transakciju atlases ierobežošanai. Šie kritēriji var iekļaut kases kontu numurus un valūtu kodus. Laukā <strong>Izveidoja</strong> atlasiet lietotāju, kurs ir atbildīgs par pārskata izveidošanu. Lai skatītu izveidoto pārskatu <strong>Kase</strong>, izmantojiet pogu <strong>Kases pārskati</strong> lapā <strong>Kases konti</strong>.</td>
</tr>
<tr class="even">
<td>Kase — Valūtas pārrēķins FIFO un LIFO (tikai Polijai)</td>
<td>Aprēķiniet valūtas pārrēķinu pēc Polijas standartiem. Izmantojiet funkciju <strong>Filtrēt</strong> cilnē <strong>Iekļaujamie ieraksti</strong>, lai norādītu kases kontu, kuram izpildīt šo uzdevumu. Atzīmējiet izvēles rūtiņu <strong>Pārrēķins</strong>, lai izpildītu pilnu valūtas maiņas starpības pārrēķinu visiem atvērtajiem periodiem. Tālāk ir aprakstīts, kā notiek valūtas pārrēķināšana, ja tiek izmantota metode “pirmais iekšā, pirmais ārā” (first in, first out – FIFO) un metode “pēdējais iekšā, pirmais ārā” (last in, first out — LIFO).
<ul>
<li><strong>FIFO metode</strong> — sistēma meklē izdevumu transakciju, kurai ir agrāks transakcijas datums (mazāks kārtas numurs), un to nosedz ar ieejas plūsmas transakciju, kurai ir agrāks transakcijas datums (mazāks kārtas numurs).</li>
<li><strong>LIFO metode</strong> — sistēma meklē izdevumu transakciju, kurai ir vēlāks transakcijas datums (lielāks kārtas numurs), un to nosedz ar ieejas plūsmas transakciju, kurai ir vēlāks transakcijas datums (lielāks kārtas numurs).</li>
</ul>
Nosegtā summa tiek rādīta laukā <strong>Nosegts valūtā</strong>, lapā <strong>Kases transakcija</strong>. Ja pastāv valūtas pārrēķina starpība, šī summa tiek rādīta laukā <strong>Valūtas pārrēķina summa</strong>, un tabulā <strong>Kases transakcija</strong> tiek ģenerēta transakcija ar dokumenta tipu <strong>Valūtas kursu starpība</strong>. Virsgrāmatas konti peļņas/zaudējumu transakcijām ir iestatīti tabulā <strong>Valūta</strong> (<strong>Peļņa no valūtas kursa svārstībām</strong> un <strong>Zaudējumi no valūtas kursa svārstībām</strong>).</td>
</tr>
<tr class="odd">
<td>Ārvalstu valūtas pārvērtēšana — Kase</td>
<td>Izmantojiet šo uzdevumu, lai izmantotu atbilstošu bilanci noklusējuma valūtā pārskata datumā, kad operācijas tiek ievadītas ārvalstu valūtās. Izmantojiet funkciju <strong>Filtrēt</strong> cilnē <strong>Iekļaujamie ieraksti</strong>, lai norādītu kases kontu, kuram izpildīt šo uzdevumu. Šim uzdevumam paredzētajā dialoglodziņā izmantojiet laukus <strong>No valūtas</strong> un <strong>Uz valūtu</strong>, lai norādītu transakciju valūtas. Summu konvertētajā valūtā sistēma salīdzina ar summu noklusējuma valūtā, izmantojot maiņas kursu atlasītajā datumā. Šo abu summu starpība (izņemot iepriekšējo valūtas pārrēķinu) ir aprēķinātais valūtas pārrēķins. Šis uzdevums izveido apstiprinātu kases transakciju ar tipu <strong>Valūtas pārrēķins</strong>. Virsgrāmatas transakcija tiek veidota, izmantojot virsgrāmatas kontu kasei un virsgrāmatas kontu, kurš ir norādīts tabulas <strong>Valūta</strong> vienumā <strong>Nerealizētā peļņa</strong> vai <strong>Nerealizētie zaudējumi</strong>.</td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a>Pieprasījumi un pārskati

| Pieprasījums vai pārskats                             | Apraksts                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kases transakciju skats                        | Orderu žurnāla rindai darbību rūtī izmantojiet pogu **Pieprasījumi**, lai skatītu virsgrāmatas transakcijas, kases atlikumu un citu informāciju                                                                                  |
| Kases transakcija                              | Lai skatītu kases transakcijas, dodieties uz **Kases un bankas vadība** &gt; **Pieprasījumi un pārskati** &gt; **Kases transakcijas**. Izmantojiet funkciju **Filtrēt**, lai norādītu papildu kritērijus kases transakciju atlases ierobežošanai. |
| Reģistrācijas žurnāls (Igaunijai, Krievijai) | Pārskats sadaļā **Kases un bankas vadība** &gt; **Pieprasījumi un pārskati** &gt; **Reģistrācijas žurnāls** ataino visus izdotos kases ienākumu un kases izdevumu orderus.                                   |
| Kases grāmata (Latvijai, Lietuvai, Krievijai)     | Pārskats sadaļā **Kases un bankas vadība** &gt; **Pieprasījumi un pārskati** &gt; **Kases grāmatas žurnāls** ataino faktiskās kases līdzekļu kustības (ieņēmumus un izdevumus).                                                            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]