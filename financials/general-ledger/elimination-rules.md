---
title: Korekcijas noteikumi
description: "Šajā tēmā ir sniegta informācija par likvidēšanas noteikumus un piedāvā dažādas iespējas ziņošanai par izslēgšanu."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Korekcijas noteikumi

Šajā tēmā ir sniegta informācija par likvidēšanas noteikumus un piedāvā dažādas iespējas ziņošanai par izslēgšanu.

Korekcijas darbības ir nepieciešamas, kad pamata juridiska persona darbojas ar vienu vai vairākām pakārtotām juridiskām personām un tiek izmantoti konsolidētie finanšu pārskati. Konsolidētajos finanšu pārskatos jābūt iekļautām tikai darbībām, kas veiktas starp konsolidēto organizāciju un citām personām ārpus šīs organizācijas. Tāpēc darījumos starp juridiskām personām, kas ir daļa no tās pašas organizācijas ir jānoņem, vai izslēgti no Virsgrāmatas, tāpēc tie neparādās finanšu pārskatos. Ir vairāki veidi, kā ziņot korekcijas:

-   Korekcijas noteikumu var izveidot un apstrādāt konsolidēšanas vai korekcijas uzņēmumā.
-   Var izmantot finanšu pārskatu, lai parādītu korekciju kontus un dimensijas noteiktā rindā vai kolonnā.
-   Var izmantot atsevišķu juridisku personu manuālo darbību ierakstu grāmatošanai, lai izsekotu korekcijas.

Šajā tēmā ir pievērsta uzmanība korekcijas noteikumiem, kas tiek apstrādāti konsolidēšanas vai korekcijas uzņēmumā. Var iestatīt korekcijas noteikumus korekcijas darbību izveidei juridiskā personā, kura ir norādīta kā korekcijas mērķa juridiska persona. Šī mērķa juridiska persona ir pazīstama arī kā koriģēta juridiska persona. Korekcijas žurnāli var tikt izveidoti konsolidācijas procesa laikā vai izmantojot korekcijas žurnāla priekšlikumu. Pirms likvidēšanas noteikumu iestatīšanas jums ir jāiepazīstas ar sekojošajiem terminiem:

-   **Avota juridiska persona** — juridiska persona, kurai koriģējamās summas ir iegrāmatotas.
-   **Mērķa juridiska persona** — juridiska persona, kurā tiek grāmatoti korekcijas noteikumi.
-   **Koriģēta juridiska persona** — juridiska persona, kura ir norādīta kā mērķa juridiska persona korekcijai.
-   **Konsolidēta juridiska persona** — juridiska persona, kura tika izveidota, lai juridisku personu grupai ziņotu par finanšu rezultātiem. Šajā juridiskajā personā ir konsolidēti juridisku personu finanšu dati, un finanšu pārskats tiek veidots no apvienotajiem datiem.

Šajā tabulā ir parādīti transakciju veidi, kurus var nākties koriģēt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Darījuma veids</th>
<th>Piemērs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pārdošanas pasūtījuma ievade un rēķinu nosūtīšana (centralizēta apstrāde)</td>
<td>Jūs pārdodat preci debitoram citas juridiskas personas jūsu organizācijā vārdā.</td>
</tr>
<tr class="even">
<td>Pārdošanas pasūtījuma ievade (starpuzņēmumu/uzņēmuma iekšienē) un rēķinu nosūtīšana</td>
<td>Jūs pārdodat preces starp juridiskām personām jūsu organizācijā.</td>
</tr>
<tr class="odd">
<td>Pirkšanas pasūtījumi (centralizēta apstrāde)</td>
<td>Jūs iegādājāties krājumus, izejvielas, pakalpojumus, pamatlīdzekļus un citas preces no kreditora citas juridiskas personas jūsu organizācijā vārdā.</td>
</tr>
<tr class="even">
<td>Krājumu vadība (starpuzņēmumu/uzņēmuma iekšienē)</td>
<td><ul>
<li>Jūs pārsūtat vienas juridiskas personas krājumus uz citas juridiskas personas jūsu organizācijā pamatlīdzekļiem.</li>
<li>Jūs pārsūtat vienas juridiskas personas krājumus uz citas juridiskas personas jūsu organizācijā krājumiem.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Inventāra tranzīta izsekošana</td>
<td>Jūs pārsūtat krājumus starp vienas juridiskas personas noliktavām, kuras atrodas dažādās ģeogrāfiskās vietās.</td>
</tr>
<tr class="even">
<td>Parādu kreditoriem centralizēta rēķinu apstrāde</td>
<td>Jūs reģistrējat rēķinu citas juridiskas personas jūsu organizācijā vārdā.</td>
</tr>
<tr class="odd">
<td>Parādu kreditoriem centralizēta maksājumu apstrāde</td>
<td>Jūs apmaksājat rēķinu citas juridiskas personas jūsu organizācijā vārdā.</td>
</tr>
<tr class="even">
<td>Kases pārvaldība un kase (centralizētā apstrāde)</td>
<td><ul>
<li>Jūs apstrādājat nodokļu maksājumus, nodokļu atmaksājumus, procentu maksājumus, aizdevumus, avansus, samaksātās dividendes un iepriekšapmaksātus honorārus vai komisijas.</li>
<li>Jūs apmaksājat izdevumus citas juridiskas personas jūsu organizācijā vārdā. Rēķins tiek ievadīts mērķa juridiskas personas grāmatās un jums ir jāsedz maksājumi juridisku personu starpā. Piemēram, viena juridiska persona apmaksā darbinieka izdevumu pārskatu citā juridiskajā personā. Šādā gadījumā darbinieka izdevumu pārskatā ir izdevumi, kuri ir saistīti ar citu juridisku personu.</li>
<li>Jūs pārvedat skaidru naudu no vienas juridiskas personas uz otru jūsu organizācijā.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Debitoru parādi (centralizēta apstrāde)</td>
<td>Jūs saņemat skaidru naudu par citas juridiskas personas debitora rēķinu un noguldāt čeku šīs juridiskas personas bankas kontā.</td>
</tr>
<tr class="even">
<td>Algas (centralizēta apstrāde, starpuzņēmumu/uzņēmumā)</td>
<td><ul>
<li>Jūs maksājat citas juridiskas personas algas. Piemēram, juridiska persona maksā algu saviem darbiniekiem, bet izdara atvilkumu par darbu, ko darbinieks paveicis citai juridiskai personai tā algu aprēķina izpildes posmā. Vai arī, darbinieks ir strādājis uz nepilnu slodzi gan juridiskajā personā A, gan juridiskajā personā B, un atalgojumu saņem no abiem uzņēmumiem. Šajos gadījumos darbinieka alga ietver maksājumus no abām juridiskām personām. Grāmatotas tiek ne tikai algas, bet arī to nodokļi, pabalsti, atvilkumi un uzkrājumi.</li>
<li>Jūs pārvedat darbaspēku no vienas struktūrvienības vai nodaļas uz otru.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pamatlīdzekļi (starpuzņēmumu/uzņēmuma)</td>
<td>Jūs pārsūtat pamatlīdzekļus uz citas juridiskas personas pamatlīdzekļiem vai krājumiem.</td>
</tr>
<tr class="even">
<td>Sadalījumi (starpuzņēmumu/uzņēmuma)</td>
<td>Jūs apstrādājat korporatīvos sadalījumus. Sadalījumi ir aktivitātes attiecībā uz jebkuru sadalīto kontu, neatkarīgi no izcelsmes moduļa.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Piemērs
Jūsu juridiska persona — juridiska persona A — pārdod logrīkus citai juridiskai personai jūsu organizācijā — juridiskai personai B. Šajā piemērā ir parādīts, kā var rasties nepieciešamība koriģēt transakcijas, kas notiek starp divām juridiskām personām:

-   Juridiska persona A pārdod logrīku, kas maksā 10,00 juridiskai personai B par 10,00.
-   Juridiska persona A pārdod logrīku, kas maksā 10,00 juridiskai personai B par 10,00 plus 2,00 par faktiskajām transporta izmaksām.
-   Juridiska persona A pārdod logrīku, kas maksā 10,00, juridiskai personai B par 15,00 un atzīst peļņu no šīs pārdošanas.
-   Juridiska persona A pārdod logrīku, kas maksā 10,00, juridiskai personai B par 15,00 un atzīst daļu no peļņas no šīs pārdošanas. Juridiska persona B atzīst otru daļu no peļņas par pārdošanu. Līdz ar to ieņēmumi tiek sadalīti. Ieņēmumu sadalīšana veicina pasūtīšanu no citas juridiskas personas organizācijā, nevis no ārējās organizācijas.

Visas šīs transakcijas ir starpuzņēmumu transakcijas, kuras tiek grāmatotas abu pušu kontos. Turklāt šajās transakcijās var tikt iekļautas uzcenojuma un nocenošanas summas, kad starpuzņēmumu pārdošanas summa nav vienāda ar preču vērtību.

## <a name="set-up-elimination-rules"></a>Korekcijas noteikumu iestatīšana
Iestatot novēršanas noteikumu dinamika 365 operācijām, ieteicams izveidot finanšu dimensiju, jo īpaši novēršanas nolūkos. Lielākā daļa klientu nosaukt to tirdzniecības partneris vai kaut ko tamlīdzīgu. Ja nolemjat nelietot finanšu dimensijai, tad pārliecinieties, ka ir galvenā uzskaite, kas ir raksturīgas tikai starpuzņēmumu transakcijas. 

Korekcijas iestatīšanas atrodas konsolidācijas modulis uzstādīšanas jomā. Pēc tam, kad jūs ievadiet kārtulas aprakstu, ir izvēlēties uzņēmumu, kas post korekcijas žurnālu. Tas būtu uzņēmums, kas ir **finanšu likvidēšanas procesu izmantošanai** atlasīts iestatījuma juridiska persona. 

Var uzstādīt datumu kas novēršanas likums stājas spēkā, un, kad tas ir beidzies, ja nepieciešams. Ir jāiestata **aktīvā** uz **Jā** ja jūs vēlaties, lai tie būtu pieejami likvidēšanu priekšlikuma procesā. Žurnāla nosaukumu, kuru tips ir atlasiet **likvidēšanu**.

Pēc tam, kad esat definējis pamati, faktisko apstrādes kārtulas var definēt, noklikšķinot uz **līnijas**. Ir divas iespējas saīsināšanai, novēršot neto apgrozījuma summu vai noteikt fiksētu summu. 

Atlasiet avotu kontā. Var izmantot zvaigznīti (\*) kā savvaļas karti. Piemēram, 1\* varētu atlasīt visus kontus, kas sākas ar 1 kā avota datu sadalījumu. 

Pēc tam, kad esat atlasījis avota konti, **konta specifikācija** nosaka no galamērķa uzņēmumā, kas izmanto kontu. Atlasiet **avots** ja jūs vēlaties izmantot vienu un to pašu galveno kontu, kas definēts **avots** kontu. Ja atlasāt **lietotāja definēts**, tad ir jānorāda uz galamērķa kontu. 

Dimensijas specifikācija darbojas tādā pašā veidā. Ja atlasāt **avots**, tā izmantos tās pašas dimensijas adresāta uzņēmumā kā avota uzņēmumā. Ja atlasāt **lietotāja definēts**, jums vajadzēs norādīt dimensijas galamērķa uzņēmumā, noklikšķinot uz **mērķa dimensiju** izvēlnes elementu. 

Atlasiet avota izmērus un finanšu dimensijas un vērtības, kas tiek izmantotas kā avotu likvidēšanu.

## <a name="process-elimination-transactions"></a>Korekcijas transakciju apstrāde
Ir divi veidi, kā procesa novēršanas darbības konsolidācija tiešsaistē procesa laikā vai likvidēšanas žurnālā izveidojot un palaižot likvidēšanas priekšlikumu procesu. Šajā sadaļā ir vērsta uz žurnālu izveide un palaišana likvidēšanas procesu. 

Sabiedrība definē kā uzņēmuma likvidēšanu, atlasiet **likvidēšanu žurnāla** konsolidācijas modulī. Pēc tam, kad ir atlasīti žurnāla nosaukumu, noklikšķiniet uz **līnijas**. Priekšlikums var palaist, izvēloties **priekšlikumus** izvēlni, un pēc tam atlasot **likvidēšanas priekšlikumu**.

Atlasiet uzņēmumu, kas ir konsolidēto datu avotu un pēc tam izvēlieties kārtulas, kuru vēlaties apstrādāt. Ievadiet sākuma datumu, lai sāktu meklēt korekcijas summas un beigu datumu, lai meklēšanas termiņš korekcijas summas. **VG grāmatojuma datumu** lauks ir izmantots, grāmatojot žurnālu Virsgrāmatā datums. Pēc noklikšķināšanas uz **OK**, var pārskatīt summas un Grāmatojiet žurnālu.


