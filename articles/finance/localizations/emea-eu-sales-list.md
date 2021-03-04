---
title: ES pārdošanas saraksta pārskats
description: Šajā rakstā ir sniegta informācija par Eiropas Savienības (ES) pārdošanas saraksta atskaišu veidošanu.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EUSalesList
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68cbd8d3495f8c10c57fa0751fabb03a6946c7dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408272"
---
# <a name="eu-sales-list-reporting"></a>ES pārdošanas saraksta pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par Eiropas Savienības (ES) pārdošanas saraksta atskaišu veidošanu.

<a name="eu-sales-list-reporting"></a>ES pārdošanas saraksta pārskats
-----------------------

Kreditoram, kurš veic EK preču vai pakalpojumu piegādi uzņēmumiem, kas veic uzņēmējdarbību Eiropas Savienības (ES) ietvaros, ir jāiesniedz deklarācija par EK piegādēm (ES pārdošanas saraksts vai ESL). Parasti ESL ir jāiesniedz nodokļu iestādēm ne vēlāk kā ESL kalendārā perioda mēneša pēdējā dienā. Kreditoram ir jānorāda ESL tā pievienotās vērtības nodokļa maksātāja (PVN) reģistrācijas numuru, kā arī jānorāda, pēc debitora, šādu informāciju:

-   ES Debitora PVN maksātāja reģistrācijas numurs
-   EK preču un pakalpojumu piegādes kopējā vērtība, kas tiek veikta ES debitoriem šajā periodā. Kreditoram ir arī jāatdala vispārējā preču piegādes no triangulārās tirdzniecības piegādēm. Triangulārās tirdzniecība darbība ietver preču tiešo piegādi no kreditora piegādātāja savam klientam, ja abas puses ir reģistrētas citās Eiropas Savienības dalībvalstīs.

Izmantojot ESL, katras ES dalībvalsts nodokļu iestādes var pārbaudīt, vai PVN ir samaksāts katrai EK darbībai. Sarakstu un PVN deklarāciju kombinācija ļauj ES dalībvalstīm apmainīties ar informāciju par preču plūsmu visā ES.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Pārskats par ES tirdzniecības saraksta pārskata procesu
ES pārdošanas saraksta pārskatam var veikt šādus uzdevumus:

-   Apkopot informāciju par EK tirdzniecības darbībām. EK tirdzniecības darbība var būt pārdošanas rēķins, brīva teksta rēķins, projekta rēķins vai kreditora rēķins. Darbība ir identificēta, pamatojoties uz darījumu partnera valsti/reģionu. Dažādu veidu EK tirdzniecības darbības tiek apkopotas ES pārdošanas saraksta tabulā, kur tās tiek attēlotas kopējā formā. Katrs ieraksts ESL tabulā atspoguļo vienu darījumu un sastāv no darījumu partnera PVN maksātāja reģistrācijas numura, kā arī norādīto preču un pakalpojumu kopējā vērtība.
-   (Izvēles iespēja) Priekšskatīt **ES pārdošanas saraksta** pārskatu. Varat priekšskatīt un pārbaudīt pārskatu **ES pārdošanas saraksts** par norādīto periodu Microsoft Excel darbgrāmatas formātā.
-   Izveidot **ES pārdošanas saraksta** pārskatu. **ES pārdošanas saraksta** pārskats tiek izveidots elektronisko faila īpašā formātā, kas ir specifisks katrai ES dalībvalstij. Parasti **ES pārdošanas saraksta** pārskats satur pamatinformāciju par pārskatu sniedzošu pusi, un piegādāto preču un pakalpojumu vērtības. Informācija tiek grupēta pēc valsts un numuru darījumu partnera PVN maksātāja reģistrācijas numura.
-   Aizvērt ES pārdošanas saraksta pārskata periodu. Pēc tam, kad **ES pārdošanas saraksta** pārskats tiek izveidots un iesniegts iestādēm, jūs varat atzīmēt ESL tabulu kā **Slēgts**. Šīs darbības netiks iekļautas papildu pārskatos.

## <a name="prerequisites"></a>Priekšnosacījumi
Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorija</th>
<th>Priekšnosacījums</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Iestatīšana:</strong> Juridiska persona</td>
<td>Juridiskās personas primārajai adresei ir jāatrodas ES dalībvalstī. Lapā <strong>Juridiskas personas</strong> (noklikšķiniet uz <strong>Organizācijas administrēšana</strong> &gt; <strong>Organizācijas</strong> &gt; <strong>Juridiskas personas</strong>) atlasiet savu juridisko personu. Kopsavilkuma cilnē <strong>Adreses</strong>, izveidojiet adresi, atlasiet valsti/reģionu un citas adreses sastāvdaļas, un atzīmējiet adresi kā <strong>Primārā</strong>. Kopsavilkuma cilnē <strong>Nodokļa reģistrācija</strong>, laukā <strong>Nodokļa reģistrācijas numurs</strong> norādiet nodokļa reģistrācijas numuru jūsu uzņēmumam.</td>
</tr>
<tr class="even">
<td><strong>Iestatīšana:</strong> PVN reģistrācijas identifikācijas parametri</td>
<td>Iestatiet PVN reģistrācijas identifikācijas parametrus lapā <strong>Valsts/reģiona parametri</strong> (noklikšķiniet uz <strong>Nodokļi</strong> &gt; <strong>Iestatīšana</strong> &gt; <strong>PVN</strong> &gt; <strong>Valsts/reģiona parametri</strong>). Katrai valstij/reģionam, kur jums ir darījumu partneri, izveidojiet ierakstu lapā un norādiet šādu informāciju:
<ul>
<li><strong>Valsts/reģions</strong> – atlasiet valsti/reģionu, ko saistīt ar PVN reģistrācijas identifikāciju.</li>
<li><strong>PVN</strong> – ievadiet nodokļa reģistrācijas identifikācijas numuru (t.i., nodokļa reģistrācijas numura prefiksu) atlasītajai valstij/reģionam.</li>
<li><strong>Pārbaudīt PVN reģistrācijas numuru</strong> – atlasiet šo izvēles rūtiņu, lai apstiprinātu PVN reģistrācijas identifikāciju atlasītajai valstij/reģionam.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Iestatīšana:</strong> PVN reģistrācijas numuri</td>
<td>Izveidojiet PVN reģistrācijas numurus jūsu darījumu partneriem lapā <strong>PVN reģistrācijas numuri</strong> (noklikšķiniet uz <strong>Nodokļi</strong> &gt; <strong>Iestatīšana</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN reģistrācijas numuri</strong>). Katram PVN reģistrācijas numuram, izveidojiet ierakstu lapā un norādiet šādu informāciju:
<ul>
<li><strong>Valsts/reģions</strong> – atlasiet darījumu partnera PVN reģistrācijas valsti/reģionu.</li>
<li><strong>PVN reģistrācijas numurs</strong> – ievadiet darījuma partnera PVN reģistrācijas numuru.</li>
<li><strong>Uzņēmuma nosaukums</strong> – (Izvēles iespēja) ievadiet darījuma partnera nosaukumu.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Iestatīšana:</strong> darījuma partneru nodokļu reģistrācija</td>
<td>Iestatiet nodokļu reģistrācijas informāciju par jūsu darījumu partneriem lapā <strong>Visi debitori</strong> (noklikšķiniet uz <strong>Pārdošana un mārketings</strong> &gt; <strong>Debitori</strong> &gt; <strong>Visi debitori</strong>, atlasiet debitora ierakstu un pēc tam noklikšķiniet uz <strong>Opcijas</strong> &gt; <strong>Mainīt skatījumu</strong> &gt; <strong>Detalizētas informācijas skats</strong>) vai lapā <strong>Kreditori</strong> (noklikšķiniet uz <strong>Sagāde un avoti</strong> &gt; <strong>Kreditori</strong> &gt; <strong>Kreditori</strong>, atlasiet kreditora ierakstu un pēc tam noklikšķiniet uz <strong>Opcijas</strong> > &gt; <strong>Mainīt skatījumu</strong> &gt; <strong>Detalizētas informācijas skats</strong>). Kopsavilkuma cilnē <strong>Rēķins un piegāde</strong>, laukā <strong>PVN reģistrācijas numurs</strong>, atlasiet PVN reģistrācijas numuru.</td>
</tr>
<tr class="odd">
<td><strong>Iestatīšana:</strong> PVN</td>
<td>Iestatiet nodokļu kodus, lai pārskatu <strong>ES pārdošanas saraksts</strong> iekļautu lapā <strong>PVN kodi</strong> (noklikšķiniet uz <strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN kodi</strong>). Kopsavilkuma cilnē <strong>Pārskata iestatīšana</strong> katram PVN kodam, kas jāiekļauj pārskatā, notīriet izvēles rūtiņu <strong>Nav iekļauts</strong>. Iestatiet PVN parametrus krājumiem lapā <strong>Krājumu PVN grupas</strong> (noklikšķiniet uz <strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>Krājumu PVN grupas</strong>). Katrai PVN krājumu grupai, atlasiet vērtību laukā <strong>Pārskata veids</strong>. Vērtību, ko jūs atlasāt nosaka ESL summas kolonnu, kurā tiks iekļauta rindas summa.
<ul>
<li><strong>Tukšs</strong> – rindas summa tiek iekļauta kolonnā <strong>Nepiešķirta vērtība</strong>.</li>
<li><strong>Krājums</strong> – rindas summa tiek iekļauta kolonnā <strong>Krājuma vērtība</strong>.</li>
<li><strong>Pakalpojums</strong> – rindas summa tiek iekļauta kolonnā <strong>Pakalpojumu vērtība</strong>.</li>
<li><strong>Investīcija</strong> – rindas summa tiek iekļauta kolonnā <strong>Investīcijas vērtība</strong>. Šī kolonna attiecas tikai uz Beļģiju.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Iestatīšana:</strong> ESL pārskatu veidošanas konfigurācijas</td>
<td>ESL elektronisko pārskatu veidošanas konfigurācijas importēšana vai izveidošana Informāciju par to, kā izveidot un uzturēt elektroniskā pārskata konfigurācijas, skatiet elektroniskā pārskata dokumentācijā.</td>
</tr>
<tr class="odd">
<td><strong>Iestatīšana:</strong> Galvenie parametri</td>
<td>Iestatiet ESL pārskatu parametrus lapā <strong>Ārējās tirdzniecības parametri</strong> (noklikšķiniet uz <strong>Nodokļi</strong> &gt; <strong>Iestatīšana</strong> &gt; <strong>Ārējā tirdzniecība</strong> &gt; <strong>Ārējās tirdzniecības parametri</strong>). Norādiet šādus parametrus:
<ul>
<li>Cilne <strong>ES pārdošanas saraksts</strong>:
<ul>
<li><strong>Termiņatlaides pārskats</strong> — atzīmējiet šo izvēles rūtiņu, ja termiņatlaide ir jāiekļauj vērtībā, kad darbība ir iekļauta ESL.</li>
<li><strong>Pārsūtīšanas pirkumi</strong> – atlasiet šo izvēles rūtiņu, lai iekļautu pirkumus ESL.</li>
<li><strong>Failu formāta kartēšana</strong> – atlasiet elektroniskā pārskata formātu, ko lietot, kad elektroniskais fails tiek izveidots priekš ESL.</li>
<li><strong>Pārskata formāta kartēšana</strong> – atlasiet elektroniskā pārskata formātu, ko lietot, kad priekšskatījuma pārskats tiek izveidots priekš ESL.</li>
<li><strong>Noapaļošanas nosacījums</strong> – norādiet reāls skaitli, izmantošanai noapaļojot. ESL summas, kas bez atlikuma dalās ar šo skaitli, tiks noapaļotas.</li>
<li><strong>Noapaļošanas metode</strong> – atlasiet noapaļošanas metodi, ko izmantot, noapaļojot ESL summas (<strong>Parasta</strong>, <strong>Uz zemāku</strong>, vai <strong>Noapaļošana</strong>).</li>
<li><strong>Lietot minimālo vērtību</strong> – atlasiet šo izvēles rūtiņu, ja vēlaties, lai summas, kas ir mazākas par skaitli <strong>Noapaļošanas nosacījums</strong>, tiktu noapaļotas līdz skaitlim <strong>Noapaļošanas nosacījums</strong>.</li>
<li><strong>Decimāldaļu skaits</strong> – norādiet decimāldaļu vietu skaitu, ko rādīt ESL summās (gan elektroniskajos failos, gan <strong>ESL priekšskatījuma</strong> pārskatā).</li>
</ul></li>
<li>Cilne <strong>Valsts/reģiona parametri</strong>: identificējiet ES dalībvalstīs. Katrai ES dalībvalstij, izveidojiet ierakstu lapā un norādiet šādu informāciju:
<ul>
<li><strong>Valsts/reģions</strong> – atlasiet valsti/reģionu.</li>
<li><strong>Valsts/reģiona tips</strong> – ja vērtība <strong>Valsts/reģions</strong> ir valsts/reģions, kurā ir reģistrēts jūsu uzņēmums, atlasiet <strong>Iekšzemes</strong>. Ja vērtība <strong>Valsts/reģions</strong> ir cita ES dalībvalsts, nevis valsts/reģions, kurā ir reģistrēts jūsu uzņēmums, atlasiet <strong>ES</strong>. Ja lauka <strong>Valsts/reģions</strong> vērtība nav ES dalībvalsts, atlasiet vienumu <strong>Trešā valsts/reģions</strong>.</li>
</ul></li>
<li>Cilne <strong>Numuru sērijas</strong>: rindā, kur vērtība <strong>Atsauce</strong> vērtība ir <strong>ES pārdošanas saraksts</strong>, atlasiet numuru sērijas kodu.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Saistītās transakcijas</strong></td>
<td><ul>
<li>Reģistrējiet pārdošanu klientam citā ES valstī.</li>
<li>Reģistrējiet brīva teksta rēķinu klientam citā ES valstī.</li>
<li>Reģistrējiet projekta rēķinu klientam citā ES valstī.</li>
<li>Reģistrējiet rēķinu no kreditora klientam citā ES valstī.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>Darbs ar ESL
### <a name="collecting-information-about-intra-community-trade-transactions"></a>Apkopot informāciju par EK tirdzniecības darbībām

Šāda veida darbības var uzskatīt par EK tirdzniecības darbībām:

-   Pārdošanas rēķini
-   Brīvā teksta rēķini
-   Projekta rēķini
-   Kreditora rēķini

Darbība tiek uzskatīta par EK tirdzniecības darbību, ja darbības piegādes adrese ir kādā no ES dalībvalstīm. Šādām valstīm/reģioniem, cilnē **Valsts/reģiona parametri** ir jābūt ierakstam lapā **Ārējās tirdzniecības parametri**, un **Valsts/reģiona tips** vērtībai ir jābūt iestatītam uz **ES**. EK tirdzniecības darbības tiek atzīmētas laukā **Saraksta kods** lauks. Izmantojot šo lauku, jūs varat arī atdalīt vispārējās EK tirdzniecības darbības no triangulārās tirdzniecības darījumiem. Informāciju par kopienas iekšējās tirdzniecības transakcijām varat apkopot lapā **ES pārdošanas saraksts** (noklikšķiniet uz **Nodokļi** &gt; **Deklarācijas** &gt; **Ārējā tirdzniecība** &gt; **ES pārdošanas saraksts**), izmantojot funkciju **Pārsūtīt**. Šī funkcija ļauj iekļaut darbības, kurām ir dažādu pārskatu veidu summas (t. i., krājumu vai pakalpojumu), saskaņā ar krājumu PVN grupām, kas norādītas darbību rindās. Jūs varat lietot arī citus filtrus, lai noteiktu darbības, kas jāiekļauj. Funkcija **Pārsūtīt** lapā **ES pārdošanas saraksts** izveido ierakstu katrai EK tirdzniecības darbībai, kas ir iekļauta, un norāda darījuma partnera konta numuru, valsti/reģionu, PVN reģistrācijas numuru, rēķina numuru un datumu, kā arī katra pārskata tipa rindu kopskaitu. Tas arī nokopē vērtību **Saraksta kods** no darbības. Saraksta kodu darbībai var manuāli mainīt lapā **ES pārdošanas saraksts**. Funkcija **Pārsūtīt** izveido ierakstus, kur vērtība **Pārskata statuss** ir iestatīta uz **Iekļauts**. Jūs varat pārbaudīt informāciju, kas tiek apkopota lapā **ES pārdošanas saraksts**, izmantojot funkciju **Apstiprināt**.

### <a name="generating-the-eu-sales-list-report"></a>ES pārdošanas saraksta pārskata izveide

Jūs varat izveidot pārskatu **ES pārdošanas saraksts**, izmantojot funkciju **Pārskatu veidošana**, lapā **ES pārdošanas saraksts**. Funkcija ļauj atlasīt pārskata periodu un lietot filtrus, lai definētu ESL ierakstus, kas jāiekļauj. Papildus var norādīt citus parametrus, kas ir specifiski katrai valstij/reģionam. Jūs varat arī izveidot priekšskatījuma pārskatu, elektronisko failu vai abus. Funkcija **Pārskatu veidošana** izmanto pārskatu un failu formāta iestatījumus, kas norādīti lapā **Ārējās tirdzniecības parametri**. Parasti, pārskats **ES pārdošanas saraksts** sastāv no atsevišķām rindām, kas uzskaita piegāžu kopsummas pēc darījuma partnera valsts/reģiona, PVN reģistrācijas numura un pārskata veida (tiek ietvertas triangulārās tirdzniecības darbības). Pēc tam, kad izveidojat pārskatu **ES pārdošanas saraksts** konkrētam periodam, jūs varat atzīmēt ESL ierakstus, kas tiek iekļauti, iestatot vērtību **Pārskata statuss** kā **Iekļauti pārskatā**. Lai iestatītu šo statusu, izmantojiet funkciju **Atzīmēt kā iekļauti pārskatā**, lapā **ES pārdošanas saraksts**.

### <a name="closing-the-eu-sales-list-reporting-period"></a>ES pārdošanas saraksta pārskata perioda aizvēršana

Kad esat pabeidzis pārskata sniegšanas procesu noteiktam laika periodam (piemēram, kad nodokļu iestādes ir pieņēmušas pārskatu **ES pārdošanas saraksts**), jūs varat atzīmēt ESL ierakstus, kas pārskatā tiek iekļauti periodam, iestatot vērtību **Pārskata statuss** kā **Slēgts**. Lai iestatītu šo statusu, izmantojiet funkciju **Atzīmēt kā slēgts**, lapā **ES pārdošanas saraksts**. Ja jūs atgriežat perioda slēgšanu, varat atzīmēt ESL ierakstus, iestatot vērtību **Pārskata statuss** kā **Iekļauts**. Šie ieraksti tad var vēlreiz tikt iekļauti pārskatā **ES pārdošanas saraksts**. Lai iestatītu šo statusu, izmantojiet funkciju **Atzīmēt kā** **iekļauti**, lapā **ES pārdošanas saraksts**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]