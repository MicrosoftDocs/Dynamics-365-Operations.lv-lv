---
title: "Mazie kases Austrumeiropā"
description: "Šajā tēmā ir sniegta informācija par petty cash funkcionalitāte, kas ļauj lietotājiem ir Igaunija, Lietuva, Čehija, Ungārija, Latvija, Polija un Krievija atspoguļo naudas operāciju sistēmā."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268504
ms.assetid: ff2ea7b0-8de2-48c5-8f9f-5d95d9924925
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: e843abff91f74ff8c2c577f499fa829821fc56ee
ms.lasthandoff: 03/31/2017


---

# <a name="petty-cash-for-eastern-europe"></a>Mazie kases Austrumeiropā

Šajā tēmā ir sniegta informācija par petty cash funkcionalitāte, kas ļauj lietotājiem ir Igaunija, Lietuva, Čehija, Ungārija, Latvija, Polija un Krievija atspoguļo naudas operāciju sistēmā.

Mazie kases posteņi funkcionalitāti varat izmantot, lai automatizētu darbības ieņēmumi un izdevumi naudā, primāro dokumentu izveidi un drukāšanu saistītus pārskatus. Mazie kases posteņi funkcionalitāte ļauj veikt šādas darbības:

-   Saņemšanu un izdevumu pieejamo naudas līdzekļu konta.
-   Ģenerēt tipisku naudas formas: kases ieņēmumu orderi, kases izdevumu orderi un kases orderi reģistrācijas žurnālā.
-   Nosaka maksimālo naudas summu, kas ir atļauta operācijām ar klientiem, piegādātājiem un tā tālāk.
-   Parāda sistēmas kases operācijas dažādās valūtās.
-   Konvertēt skaidras naudas operācijas summas ārvalstu valūtā, grāmatvedības pārskatu sniegšanas noklusētajā valūtā.
-   Ģenerēt **kases grāmatā** un kases atskaiti.

## <a name="prerequisites"></a>Priekšnosacījumi
Pirms varat lietot petty cash funkcionalitāti, ir jāpabeidz šādus priekšnoteikumus:

-   Iestatiet naudas kontus.
-   Iestatītu grāmatošanas metodes naudas.
-   Iestatiet numuru sērijas kases dokumentu numerācijai.
-   Noklusējuma vērtības iestatīšana kases un bankas vadības parametrus.
-   Kases žurnālu nosaukumu iestatīšana vispārējā Virsgrāmatā.

### <a name="set-up-cash-accounts"></a>Kases konti

Lai iestatītu naudas, atveriet **naudas un bankas vadības**&gt;**bankas kontiem**&gt;**Likvīdie**, un ievadiet šādu informāciju.

| Lauks                 | apraksts                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| Kase                  | Ievadiet kodu, kas identificē kases konts (naudas).                                                                    |
| Vārds, uzvārds                  | Ievadiet naudas konta aprakstu.                                                                             |
| Valūta              | Atlasiet noklusētā valūtas koda, kas skaidras naudas darījumiem.                                                              |
| Numuru sēriju grupa | Ja kases dokumentu numerācija nedrīkst atšķirties no numerācijas, kas ir norādīti parametri, ievadiet kodu. |
| Dažādas valūtas       | Atzīmējiet šo izvēles rūtiņu, lai atļautu valūtās, kas atšķiras no uzskaites valūtā jāgrāmato.                     |
| Negatīvs atlikums kasē         | Atzīmējiet šo izvēles rūtiņu, lai atļautu negatīvu naudas atlikumu jebkurā valūtā.                                               |

Izveidot kases atlikumu kontroles noteikumus par kases kontu, izvēlieties kases konts un pēc tam rūtī darbības uz **naudas konta** cilni, jo **atlikuma limitu** grupu, noklikšķiniet uz **atlikuma limitu**. Ievadiet tālāk aprakstīto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valūtas tips</td>
<td>Atlasiet valūtas veidu:
<ul>
<li><strong>Norēķinu valūtu</strong> – izmantot pamata uzņēmuma valūtas kods.</li>
<li><strong>Norādītās valūtas</strong> – lietojiet valūtas kodu, kas atšķiras no pamata uzņēmuma valūtas kods.</li>
</ul></td>
</tr>
<tr class="even">
<td>Valūta</td>
<td>Ja esat atlasījis <strong>norādītās valūtas</strong>, <strong>tipu Currency</strong> lauku, atlasiet valūtas kodu. Šis lauks nav pieejams, ja atlasīta <strong>norēķinu valūtu</strong>, <strong>tipu Currency</strong> lauks.</td>
</tr>
<tr class="odd">
<td>Atlikuma limita veids</td>
<td>Atlasiet vienu no vērtībām, kas ir pieejama:
<ul>
<li><strong>Maksimālais</strong> – naudas summa nedrīkstētu pārsniegt <strong>atlikuma limitu</strong> summu naudas kontā (augšējā robeža).</li>
<li><strong>Minimālais</strong> – naudas summa nedrīkstētu iet zem <strong>atlikuma limitu</strong> summu naudas kontā (apakšā saistīta).</li>
</ul></td>
</tr>
<tr class="even">
<td>Pārbaudīt atlikuma limitu</td>
<td>Izvēlieties, kas notiek naudas dokumentu apstiprināšanas procesa laikā, ja <strong>atlikuma limits</strong> summa naudas kontā ir pārsniegts:
<ul>
<li><strong>Pieņemt</strong> – ierobežojums var tikt pārsniegts.</li>
<li><strong>Brīdinājums</strong> -ierobežojums var tikt pārsniegts, bet lietotājs saņem brīdinājumu. Kases dokuments ir apstiprināts vai apstiprināta.</li>
<li><strong>Kļūda</strong> – nevar tikt pārsniegts. Lietotājs saņem kļūdas ziņojumu un kases dokumentu nav apstiprināt vai apstiprināt.</li>
</ul>
Papildinformāciju par naudas dokumentu apstiprināšanas procesu, skatiet &quot;skaidras naudas darījuma apstiprinājumu un grāmatošanas&quot; sadaļu šajā tēmā.</td>
</tr>
<tr class="odd">
<td>Atlikuma limits</td>
<td>Ievadiet ierobežojumu naudas konta atlikumu. Summa ir valūtā, kuru jūs norādījāt.</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a>Kases grāmatošanas profilu iestatīšana

Kases grāmatošanas metodes nosaka grāmatojumiem Virsgrāmatā. Lai iestatītu grāmatošanas metodes naudas, dodieties uz **naudas****un bankas vadības**&gt;**Setup**&gt;**kases grāmatošanas metodes**, un atlasiet vai izveidojiet grāmatošanas metodi. Ievadiet tālāk aprakstīto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Derīgs</td>
<td>Norādiet, vai grāmatošanas metode tiek pielietota īpaša naudas kontu vai visi konti:
<ul>
<li><strong>Galda</strong> – ja kases konts rindu grāmatošanas profilu, ka līnija tiek izmantots naudas transakciju grāmatošanai.</li>
<li><strong>Visas</strong> – nav naudas konta grāmatošanas profilu rindā ir.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kase</td>
<td>Ja esat atlasījis <strong>tabulas</strong>, <strong>derīgs</strong> lauku, norādiet naudas kontu. Šis lauks paliek tukšs, ja esat atlasījis <strong>visiem</strong>, <strong>derīgs</strong> lauks.</td>
</tr>
<tr class="odd">
<td>Virsgrāmatas konts</td>
<td>Ievadiet Virsgrāmatas kontu, lai izmantotu kā kopsavilkuma konts kases kontam skaitu.</td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a>Iestatiet numuru sērijas kases dokumenti

Iestatīt numuru sērijas kases dokumenti, dodieties uz **naudas un bankas vadības**&gt;**uzstādīšanas**&gt;**skaidras un bezskaidras naudas pārvaldības parametri**. Par **numuru sēriju** cilnes, norādiet numuru sērijas kodus **kases ieņēmumu orderi**, **kases izdevumu orderi**, **kases korekcijas dokuments**, un **valūtas pārrēķins** dokumentus, un par **kases atskaites numurs**.

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a>Noklusējuma vērtības iestatīšana kases un bankas vadības parametri

Lai iestatītu noklusētās vērtības, naudas un bankas vadības parametrus petty cash funkcionalitāti, dodieties uz **naudas un bankas vadības**&gt;**Setup**&gt;**naudas un bankas vadības parametrus**. Par **naudas** cilni, ievadiet tālāk minēto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kase</td>
<td>Atlasiet noklusēto kases konts žurnālos.</td>
</tr>
<tr class="even">
<td>Kases grāmatošana</td>
<td>Ievadiet grāmatošanas metodi, kas jālieto, ja nav citu grāmatošanas metodi, nav norādīts noklusējuma naudas.</td>
</tr>
<tr class="odd">
<td>Dokumentu numuru kontrole</td>
<td>Izvēlieties, kas notiek, ja dublikātu numuri atrodami kases dokumenta numurs pārbaudes laikā:
<ul>
<li>Neatļaut vienādus dokumentu numurus</li>
<li>Finanšu gada laikā noraidīt kopijas</li>
<li>Atļaut vienādus dokumentu numurus</li>
<li>Brīdināt dublēšanās gadījumā</li>
</ul></td>
</tr>
<tr class="even">
<td>Pārbaudīt operāciju limitu</td>
<td>Norādīt, kas notiek, ja tiek pārsniegts operācijas ar counteragents:
<ul>
<li><strong>Pieņemt</strong> – ierobežojums var tikt pārsniegts.</li>
<li><strong>Brīdinājums</strong> -ierobežojums var tikt pārsniegts, bet lietotājs saņem brīdinājumu. Šī operācija tiek grāmatota.</li>
<li><strong>Kļūda</strong> – nevar tikt pārsniegts. Lietotājs saņem kļūdas ziņojumu, un darbības nav grāmatotas.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pārbaudes metode</td>
<td>Atlasiet apstiprināšanas metode, ko lieto, lai kontroles pārsniedzis limitu summas operācijām:
<ul>
<li><strong>Operācija</strong> -apstiprināšana tiek veikta, vienai darbībai</li>
<li><strong>Līguma</strong> -validācija tiek darīts katrā darbībā, kas ir noteikts līgums ar Kontrahentu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Operāciju limits</td>
<td>Ievadiet maksimālo summu, kas ir atļauta operācijām ar counteragents skaidrā naudā.</td>
</tr>
<tr class="odd">
<td>Grāmatošana agrākā datumā</td>
<td>Atzīmējiet šo izvēles rūtiņu, lai iespējotu naudas darījumi jāiegrāmato pirms kases darbību pēdējo datumu.</td>
</tr>
<tr class="even">
<td>Dimensijas</td>
<td>Ievadiet dimensijas <strong>nodaļas kods</strong>, <strong>analītiskais kods</strong>, un <strong>mērķa kods</strong> laukus. Drukas formā kases dokumentiem atspoguļos šo informāciju.</td>
</tr>
<tr class="odd">
<td>Lietot akceptēšanas statusu</td>
<td>Atzīmējiet šo izvēles rūtiņu, lai lietotu papildu statusu, <strong>Confirmed</strong>, naudas dokumentu apstiprināšanas procesa laikā. (Lai iegūtu papildinformāciju, skatiet &quot;skaidras naudas darījuma apstiprinājumu un grāmatošanas&quot; sadaļu.)</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a>Kases žurnālu nosaukumu iestatīšana vispārējā Virsgrāmatā

Lai veidotu naudas transakcijas grāmatošanas žurnālu, dodieties uz **Virsgrāmatas**&gt;**žurnāla iestatījumu**&gt;**žurnālu nosaukumus**, un izveidot jaunu ierakstu. Šajā **žurnāla tipa** lauku, norādiet **naudas**. Citu noklusējuma žurnāla parametrus definēt, cik jums nepieciešams.

## <a name="daily-cash-operations-via-a-slip-journal"></a>Ikdienas naudas operācijām, izmantojot pavadzīmes žurnāls
Izveidot kases dokumentu izmantojot pavadzīmes žurnāls, dodieties uz **naudas un bankas vadības**&gt;**naudas darījumiem**&gt;**žurnāla**, un izveidot jaunu žurnālu. Rūtī darbības noklikšķiniet uz **līnijas**. Pievienot jaunu rindu, un ievadiet tālāk minēto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Datums</td>
<td>Ievadiet darījuma datumu.</td>
</tr>
<tr class="even">
<td>Konts</td>
<td>Izvēlieties kases kontu. Pēc noklusējuma, kases konts ir norādīts kases un bankas vadības parametrus.</td>
</tr>
<tr class="odd">
<td>apraksts</td>
<td>Ievadiet paskaidrojošu tekstu darbībai.</td>
</tr>
<tr class="even">
<td>Debets Kredīts</td>
<td>Ievadiet naudas dokumenta summa kādā no šiem laukiem:
<ul>
<li><strong>Debeta</strong> -šo lauku izmanto, lai reģistrētu kases ieņēmumu un kases ieņēmumu orderis.</li>
<li><strong>Kredīta</strong> -šo lauku izmanto, lai reģistrētu kases izdevumu un kases izdevumu orderis.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Korespondējošā konta tipa korespondējošais konts</td>
<td>Atlasiet korespondējošā konta tipu un korespondējošā konta numuru.</td>
</tr>
<tr class="even">
<td>Valūta</td>
<td>Atlasiet darbības valūtas kods.</td>
</tr>
<tr class="odd">
<td>Dokuments</td>
<td>Šis lauks tiek aizpildīts automātiski, pamatojoties uz žurnāla iestatījumiem.</td>
</tr>
<tr class="even">
<td>Pasūtījuma numurs</td>
<td>Ja nav citu numuru sērija tiek iestatīta par kases kontu, šis lauks tiek aizpildīts automātiski, pamatojoties uz numuru sēriju, kas norādīta formā Parametri. Pasūtījuma numuru šajā laukā var ievadīt manuāli, cik jums nepieciešams. Lai novērstu inconsistence, naudas dokumentu numerācija, piemēro šādu vadīklu: kases dokumentu ar agrāku datumu operāciju skaits nevar būt lielāks nekā naudas dokumentu, kurā ir vēlāk operāciju skaits. Ja jums nav nepieciešama šo vadīklu, atlasiet <strong>norīkošanu uz agrāku datumu</strong> izvēles rūtiņu naudas un bankas vadības parametrus.</td>
</tr>
<tr class="odd">
<td>Apstiprināšanas statuss</td>
<td>Pirmās darbības statuss ir <strong>nav</strong>. Meklējiet informāciju par to, kā iestatīt darbības statusu, &quot;skaidras naudas darījuma apstiprinājumu un grāmatošanas&quot; sadaļu.</td>
</tr>
<tr class="even">
<td>Dokumenta tips </td>
<td>Šī lauka <strong>skaidras naudas pasūtījums</strong> tab tiek aizpildīts automātiski, pamatojoties uz kases dokumentu ievadīto summu:
<ul>
<li><strong>Kases ieņēmumu orderis</strong> – šī vērtība tiek izmantota, ja ievadītā summa <strong>debeta</strong> lauku kases kontam.</li>
<li><strong>Kases izdevumu orderis</strong> – šī vērtība tiek izmantota, ja ievadītā summa <strong>kredīta</strong> lauku kases konts</li>
<li><strong>Korekcijas</strong> – negatīva summa ievadītās <strong>debeta</strong> lauku vai <strong>kredīta</strong> lauku kases kontam.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PVN grupa</td>
<td>Norādiet PVN grupu, lai aprēķinātu nodokļus par darbību.</td>
</tr>
<tr class="even">
<td>Krājumu PVN grupa</td>
<td>Norāda krājuma PVN grupu, lai aprēķinātu nodokļus par darbību.</td>
</tr>
<tr class="odd">
<td>Iemesls</td>
<td>Par <strong>skaidras naudas pasūtījums</strong> cilni, ievadiet tekstu, kas apraksta darījuma priekšmets. Šis teksts tiks drukāta kases ordera ziņošanas forma.</td>
</tr>
<tr class="even">
<td>Dokumenta datums</td>
<td>Ievadiet aprakstu, numurs un datums, primārais dokuments, ko ir iemesls darbībai (piemēram, avansa atskaites, rēķina vai pasūtījuma).</td>
</tr>
<tr class="odd">
<td>Pārstāvja tips</td>
<td>Šim laukam var būt šādas vērtības:
<ul>
<li><strong>Darba ņēmējs</strong> - <strong>pārstāvis</strong> uzmeklēšanas satur darbinieku sarakstu, ja <strong>korespondējošais konts</strong> lauks ir iestatīts <strong>grāmatas</strong> vai <strong>bankas</strong>, vai kontrahenta sarakstu ar kontaktpersonām, ja <strong>korespondējošais konts</strong> lauks ir iestatīts <strong>klientu</strong> vai <strong>kreditoru</strong>. Lai iestatītu pārstāvjiem, dodieties uz <strong>pamata</strong>&gt;<strong>Setup</strong>&gt;<strong>kontaktus</strong>&gt;<strong>kontaktpersona</strong>.</li>
<li><strong>Citas</strong> - <strong>pārstāvis</strong> uzmeklēšanas satur sarakstu ar citiem klientiem. Lai iestatītu uztvērēji, kas neparādās <strong>klientiem</strong> vai <strong>kreditoriem</strong> tabulu, dodieties uz <strong>Virsgrāmatas</strong>&gt;<strong>uztvērēji</strong>. Šis veids ir pieejams tikai Latvija. ( <strong>CSELatvia</strong> konfigurācijas atslēga ir aktivizēta.)</li>
<li><strong>Piegādātāju</strong> - <strong>pārstāvis</strong> uzmeklēšanas satur sarakstu kreditoriem. Lai iestatītu kreditorus, dodieties uz <strong>kreditoru parādi</strong>&gt;<strong>kreditoriem</strong>.</li>
<li><strong>Klientu</strong> - <strong>pārstāvis</strong> uzmeklēšanas satur debitoru sarakstu. Lai iestatītu klientiem, dodieties uz <strong>Debitori</strong>&gt;<strong>klientiem</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Pārstāvis</td>
<td>Atlasiet tipu, kuru jūs norādījāt pārstāvis <strong>pārstāvības veidu</strong> lauks.</td>
</tr>
<tr class="odd">
<td>Darbinieka vārds</td>
<td>Šis lauks tiek aizpildīts automātiski, pamatojoties uz <strong>korespondējošais konts</strong> un <strong>pārstāvis</strong> laukus. Kases orderi iespiešanas formu atspoguļos šo informāciju.</td>
</tr>
<tr class="even">
<td>Personas apliecība</td>
<td>Šis lauks tiek aizpildīts automātiski, pamatojoties uz identitātes kartes dati šai kontaktpersonai (pārstāvis). Ja <strong>korespondējošā konta tips</strong> lauks ir iestatīts <strong>avansa turētāja</strong>, un <strong>korespondējošais konts</strong> ir iestatīts uz darbinieku skaitu, kases ieņēmumu vai izdevumu var izdarīt no vai darbiniekam. Šajā gadījumā <strong>apliecinošs dokuments</strong> lauks tiek aizpildīts automātiski, izmantojot datus par identitātes karti no <strong>darbinieku</strong> tabulu (<strong>personāla uzskaites</strong>&gt;<strong>darbinieku tabulā</strong>).</td>
</tr>
<tr class="odd">
<td>Nolūks</td>
<td>Šajā <strong>mērķim</strong> tabulu, noteikt vienu vai vairākus adresātu kodi darījuma summas. Atlasiet mērķa kods <strong>mērķim</strong> laukam un ievadiet paskaidrojums <strong>darbības tekstu</strong> lauks. Šajā <strong>summu</strong> laukā, ievadiet summu darījuma valūtā. <strong>%</strong> Lauks rāda, kā procentuāla attiecība mērķa summu ar kopējo darījumu summu.</td>
</tr>
<tr class="even">
<td>Atgādinājums</td>
<td>Atlikusī summa, kas aprēķināta. Ievērojiet, ka visa darījuma summa jāpiešķir adresāta kodus.</td>
</tr>
<tr class="odd">
<td>Amatpersonas</td>
<td>Par <strong>ierēdņu</strong> cilnes, norādiet atbildīgo personu vārdus un amatu nosaukumus: direktors, galvenais grāmatvedis un kasieris. <strong>Pozīciju</strong> vērtības nosaka ierēdņu uzstādīšanas <strong>vispārējās</strong> un <strong>grāmatas</strong> cilnēm <strong>amatpersonas</strong> lapas (<strong>pamata</strong>&gt;<strong>Setup</strong>&gt;<strong>kontaktus</strong>&gt;<strong>amatpersonas</strong>).</td>
</tr>
<tr class="even">
<td>Priekšapmaksa</td>
<td>Atzīmējiet šo izvēles rūtiņu, ja darbība ir priekšapmaksa.</td>
</tr>
<tr class="odd">
<td>Grāmatošanas metode</td>
<td>Kases konts ievadiet grāmatošanas metodi. Pēc noklusējuma izmanto grāmatošanas metode, kas ir norādīts kases un bankas vadības parametrus.</td>
</tr>
<tr class="even">
<td>Korespondējošo kontu grāmatošanas metode</td>
<td>Ievadiet atlasītā korespondējošā konta grāmatošanas metodi.</td>
</tr>
<tr class="odd">
<td>Kopējā summa</td>
<td>Šajā <strong>kopsumma</strong> lauku grupā lappuses apakšā, <strong>Reimb</strong> laukā redzama summa, kas aprēķināta par visu naudas atmaksāšanu potzari, kas ievadītas pašreizējā žurnālā, un <strong>Disb</strong> laukā ir norādīta kopējā visas kases izdevumu orderi.</td>
</tr>
</tbody>
</table>

Lai pārbaudītu žurnāla ievadnes, darbību rūtī noklikšķiniet uz **validēt**.

## <a name="daily-cash-operations-via-a-general-journal"></a>Ikdienas naudas operācijām, izmantojot Virsgrāmatas žurnālā
Izveidot kases darbība, izmantojot Virsgrāmatas žurnālā, dodieties uz **Virsgrāmatas**&gt;**dienasgrāmatas ieraksti**&gt;**v/g žurnālos**, un izveidot jaunu žurnālu. Rūtī darbības noklikšķiniet uz **līnijas**. Pievienot jaunu rindu, un ievadiet tālāk minēto informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Datums</td>
<td>Ievadiet darījuma datumu.</td>
</tr>
<tr class="even">
<td>Konta veids</td>
<td>Atlasiet <strong>Petty cash</strong>.</td>
</tr>
<tr class="odd">
<td>Konts</td>
<td>Izvēlieties kases kontu numuru.</td>
</tr>
<tr class="even">
<td>Darbības teksts</td>
<td>Ievadiet paskaidrojošu tekstu darbībai.</td>
</tr>
<tr class="odd">
<td>Debets Kredīts</td>
<td>Ievadiet naudas dokumenta summa kādā no šiem laukiem:
<ul>
<li><strong>Debeta</strong> -šo lauku izmanto, lai reģistrētu kases ieņēmumu un kases ieņēmumu orderis.</li>
<li><strong>Kredīta</strong> -šo lauku izmanto, lai reģistrētu kases izdevumu un kases izdevumu orderis.</li>
</ul></td>
</tr>
<tr class="even">
<td>Korespondējošā konta tipa korespondējošais konts</td>
<td>Atlasiet korespondējošā konta tipu un korespondējošā konta numuru.</td>
</tr>
<tr class="odd">
<td>Valūta</td>
<td>Atlasiet darbības valūtas kods.</td>
</tr>
</tbody>
</table>

Par **rēķina** tab, varat norādīt grāmatošanas profilu atlasītajam kontam un korespondējošo kontu. Ja reģistrētais darījums ir priekšapmaksa, atlasiet **priekšapmaksas** izvēles rūtiņu **maksājumu** tab. Šajā **pārstāvis** lauka grupa, aizpildiet laukus, kā jūs to darījāt Slip žurnāla rindām, kas jādrukā uz **naudas** atskaite. Lai pārbaudītu žurnāla ievadnes, darbību rūtī noklikšķiniet uz **validēt**.

## <a name="cash-transaction-approval-and-posting"></a>Skaidras naudas darījuma apstiprinājumu un grāmatošanas
Skaidras naudas darījumiem, var piemērot šādus statusus: **neviens**, **Confirmed**, **Approved**, un **noraidīts**. A **izmantot apstiprinātu statusu** parametru par **apstiprinājuma** FastTab no **naudas** cilnē pie **naudas un bankas vadības**&gt;**Setup**&gt;**naudas un bankas vadības parametrus** ļauj aktivizēt divus papildu statusus: **Confirmed** un **noraidīts**. Apstiprinājums ir lietderīgi, ja naudas dokumentus izsniedz un naudas ieņēmumi vai izdevumi tiek sadalīti starp diviem darbiniekiem: grāmatvedis un kasieris. **Atiestatīt statusu** funkcija maina pašreizējās darbības statuss. **Apstiprinātas** kļūst **Confirmed**, un **Confirmed** kļūst **nav**. Kases žurnāla ierakstus var labot tikai tad, ja statuss ir **nav**. Skaidras naudas darījumiem var noraidīt tikai tad, ja darbības statuss ir **Confirmed**. Noraidīja kases dokumenti ir iekļauti **kases dokumentu reģistrācijas žurnālā** atskaiti, bet tie nav atspoguļoti **kases grāmatā** atskaite. Lai apstiprinātu darbību, atlasiet atbilstošo Slip žurnāla rindas un pēc tam noklikšķiniet uz **apstiprinājuma dokumentus**&gt;**Confirm**. Pasūtījuma numurs tiek ģenerēts, pamatojoties uz norādīto numuru sēriju. Darbības statuss tiek mainīts uz **Confirmed**, un var vairs labot žurnāla rindas. Kases konta atlikums paliek nemainīgs. Lai atteiktu kases dokumentu, noklikšķiniet uz **apstiprinājuma dokumentus**&gt;**noraidīt**. Šī opcija ir pieejama tikai dokumentiem, kuros ir **Confirmed** statusu. Lai apstiprinātu darbību, atlasiet atbilstošo Slip žurnāla rindas un pēc tam noklikšķiniet uz **apstiprinājuma dokumentus**&gt;**apstiprināt**. **Approved** statuss norāda, ka naudas līdzekļi tiek saņemti vai iztērējuši. Naudas summa tiek mainīta. Kases darbība var grāmatot. Lai atceltu **apstiprināts** statusu un atiestatīšanas statusa līdz **neviens**, noklikšķiniet uz **dokumentus apstiprinājuma**&gt;**Atiestatīt statusu**. Tikai apstiprināti kases darbības var grāmatot. Lai grāmatotu žurnālu, noklikšķiniet uz **pēc**&gt;**pēc**.

## <a name="print-a-cash-order"></a>Drukāt kases orderi
Drukāt kases orderi, atlasiet Slip žurnāla rindas un pēc tam rūtī darbības noklikšķiniet uz **drukāt**&gt;**naudas pasūtījumu pārskats**. Sistēma ģenerē iespiešanas formu kases ieņēmumu orderis vai kases izdevumu orderis, atkarībā no tā, vai summa ir ievadīta **debeta** lauka vai **kredīta** laukā atlasītajai rindai:

-   Ja tur ir summa **debeta** lauks: kases ieņēmumu orderis
-   Ja tur ir summa **kredīta** lauks: kases izdevumu orderis

Žurnāla rindām, kam ir slīdēšanas **Confirmed**, **apstiprināts**, vai **noraidīts** statusu var izdrukāt. Var arī drukāt naudas pasūtījumu dokumentus pie **kases un bankas vadības**&gt;**Inquires un atskaites**&gt;**skaidras naudas pasūtījums**.

## <a name="periodic-tasks"></a>Periodiskie uzdevumi
Šādus uzdevumus var veikt **naudas un bankas vadības**&gt;**periodiskos uzdevumus**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Periodisks uzdevums</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pārbaudīt atlikuma limitu</td>
<td>Pārbaudiet atlasīto naudas konta bilanci, norādītajā datumā un parāda rezultātu informāciju ziņojumā. Bilances aprēķināšanai var saskaitīt tikai apstiprinātas darbības. Darbības, kas atzīmētas kā <strong>Payroll</strong> netiek uzskatīts.</td>
</tr>
<tr class="even">
<td>Skaidras naudas atlikuma pārrēķins</td>
<td>Izmantojiet šo uzdevumu, lai pārliecinātos, vai kases kontiem Virsgrāmatas bilanci atbilstoši kases atlikumu.</td>
</tr>
<tr class="odd">
<td>Kases atskaites izveidi (Polija)</td>
<td>Izveidot <strong>naudas</strong> atskaite. <strong>Naudas</strong> atskaites numurs tiek ģenerēts, pamatojoties uz numuru sēriju, kas iestatīta <strong>protokola numurs</strong>. Dialoga lodziņā uzdevuma veikšanai, jo <strong>līdz</strong>, norādīt pēdējo datumu, kurā naudas darījumos jāuzskata par <strong>naudas</strong> atskaite. Izmantojiet <strong>filtra</strong> darboties <strong>iekļaujamos ierakstus</strong> cilni, lai norādītu papildu kritērijus, lai ierobežotu atlasi, skaidras naudas darījumu. Šajos kritērijos var ietvert naudas kontu numuri un valūtu kodi. Šajā <strong>veido</strong> lauku, atlasiet lietotāju, kurš ir atbildīgs par atskaites sastādīšanā. Skatīt <strong>naudas</strong> atskaiti, kas izveidota, izmantojiet <strong>kases atskaites</strong> pogu <strong>Likvīdie</strong> lapā.</td>
</tr>
<tr class="even">
<td>Kase - valūtas korekcijas FIFO, LIFO (Polija)</td>
<td>Aprēķinātu valūtas pārrēķinu par poļu standarti. Lietošanas <strong>filtra</strong> darboties <strong>iekļaujamos ierakstus</strong> cilni, lai precizētu kases kontu par uzdevuma palaišanai. Atlasiet <strong>pārrēķinu</strong> izvēles rūtiņu darīt pilnu pārrēķināšanas korekcijas valūtas kursa starpību par visiem atvērtiem periodiem. Lūk, kā valūtas pārrēķins tiek aprēķināta kad pirmais iekšā, pirmais ārā (FIFO) un pēdējais iekšā, pirmais ārā (LIFO) metodes tiek izmantotas:
<ul>
<li><strong>FIFO metodi</strong> – sistēma meklē izdevumu darbību, kas ir iepriekšējās darbības datums (mazāku pasūtījuma numurs) un norēķinās ar ieejas plūsmas darbība, kas ir iepriekšējās darbības datums (mazāku pasūtījuma numurs).</li>
<li><strong>LIFO metodi</strong> – sistēma meklē izdevumu darbību, kas ir vēlāk darbību (lielāks kārtas numuru) un norēķinās ar ieejas plūsmas darbība, kas ir vēlāk darbību (lielāks kārtas numuru).</li>
</ul>
Nosegtā summa tiek atspoguļots <strong>norēķinās valūtā</strong> lauku <strong>naudas darījumu</strong> lapā. Ja korekcijas valūtas kursa starpību summa tiek atspoguļots <strong>valūtas pārrēķina summa</strong> laukā un darbībā, kuras <strong>valūtas kursa starpība</strong> dokumenta tipam tiek izveidots <strong>naudas darījumu</strong> tabulā. Iestata Virsgrāmatas kontus darbībām, peļņa/zaudējumi <strong>valūtas</strong> tabulu (<strong>kurss finansiālu peļņu</strong> un <strong>kurss finansiālus zaudējumus</strong>).</td>
</tr>
<tr class="odd">
<td>Ārvalstu valūtas pārvērtēšana — Kase</td>
<td>Izmantojiet šo uzdevumu ir pietiekama bilance noklusētajā valūtā pārskata datumā, kad ir ievadīti operācijas ārvalstu valūtās. Lietošanas <strong>filtra</strong> darboties <strong>iekļaujamos ierakstus</strong> cilni, lai precizētu kases kontu par uzdevuma palaišanai. Dialoglodziņā uzdevuma veikšanai izmantot <strong>no valūtas</strong> un <strong>uz valūtas</strong> laukus, lai norādītu darījuma valūtā. Sistēma tiek salīdzinātas summa valūtā, kas tika pārveidots, izmantojot valūtas maiņas kursu atlasītajā datumā ar summu sistēmas pamatvalūtā. Starpība starp abām summām (izņemot iepriekšējās valūtas pārrēķins) tiek aprēķināts valūtas pārrēķins. Šis uzdevums izveido apstiprinātā kases darbība no <strong>valūtas pārrēķins</strong> tips. Virsgrāmatas darbībai ir izveidots, izmantojot Virsgrāmatas konta par naudas un Virsgrāmatas kontā, kas norādīts <strong>nerealizētā peļņa</strong> vai <strong>Nerealizētie zaudējumi</strong>, <strong>valūtas</strong> tabulā.</td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a>Pieprasījumi un pārskati
| Aptauju vai pārskatu                             | apraksts                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kases darbību skatīt                        | Slip žurnāla rindas, izmantojiet **izziņas** pogu darbību rūtī skatiet Virsgrāmatas darbības, kases atlikumu un citu informāciju.                                                                                  |
| Kases darbība                              | Dodieties uz **naudas un bankas vadības**&gt;**uzziņās un pārskatos**&gt;**naudas darījumiem** lasiet skaidrās naudas darījumos. Izmantojiet **filtra** funkciju, lai norādītu papildu kritērijus, lai ierobežotu atlasi, skaidras naudas darījumu. |
| (Igaunija, Krievija) reģistrācijas žurnāls | Ziņojums pie **naudas un bankas vadības**&gt;**uzziņās un pārskatos**&gt;**reģistrācijas žurnāla** atspoguļo visas naudas atmaksu un kases izdevumu orderi, kas ir izsniegtas.                                   |
| Kases grāmata (lai Latvija, Lietuva, Krievija)     | Ziņojums pie **naudas un bankas vadības**&gt;**uzziņās un pārskatos**&gt;**kases grāmatas pārskats** atspoguļo faktisko naudas fondu pārvietošanu (ieņēmumi un izdevumi).                                                            |




