---
title: Korekciju kārtulas
description: Šajā tēmā ir sniegta informācija par korekciju kārtulām un dažādām korekciju ziņošanas iespējām.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e062e7541871d77803cbed475d715621b19537f1
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722638"
---
# <a name="elimination-rules"></a>Korekciju kārtulas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par korekciju kārtulām un dažādām korekciju ziņošanas iespējām.

Korekcijas darbības ir nepieciešamas, kad pamata juridiska persona darbojas ar vienu vai vairākām pakārtotām juridiskām personām un tiek izmantoti konsolidētie finanšu pārskati. Konsolidētajos finanšu pārskatos jābūt iekļautām tikai darbībām, kas veiktas starp konsolidēto organizāciju un citām personām ārpus šīs organizācijas. Tāpēc transakcijas starp juridiskajām personām, kas pieder vienai un tai pašai organizācijai, ir jānoņem no virsgrāmatas vai jākoriģē virsgrāmatā tā, lai tās netiktu rādītas finanšu pārskatos. Ir vairāki veidi, kā ziņot korekcijas:

-   Korekciju kārtulu var izveidot un apstrādāt konsolidēšanas vai korekcijas uzņēmumā.
-   Var izmantot finanšu pārskatu, lai parādītu korekciju kontus un dimensijas noteiktā rindā vai kolonnā.
-   Var izmantot atsevišķu juridisku personu manuālo darbību ierakstu grāmatošanai, lai izsekotu korekcijas.

Šajā tēmā ir pievērsta uzmanība korekciju kārtulām, kas tiek apstrādātas konsolidēšanas vai korekcijas uzņēmumā. Korekciju kārtulas varat iestatīt, lai izveidotu korekciju transakcijas juridiskajā personā, kura ir norādīta kā korekcijas mērķa juridiskā persona. Šī mērķa juridiska persona ir pazīstama arī kā koriģēta juridiska persona. Korekcijas žurnāli var tikt izveidoti konsolidācijas procesa laikā vai izmantojot korekcijas žurnāla priekšlikumu. Pirms likvidēšanas noteikumu iestatīšanas jums ir jāiepazīstas ar sekojošajiem terminiem:

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
Iestatot korekciju kārtulas, ir ieteicams izveidot finanšu dimensiju, kas ir īpaši paredzēta korekcijas nolūkiem. Vairums klientu tai piešķir nosaukumu Darījumu partneris vai tamlīdzīgu. Ja izlemjat kādu finanšu dimensiju nelietot, jums noteikti ir nepieciešami galvenie konti, kas ir raksturīgi tikai starpuzņēmumu transakcijām. 

Korekciju iestatījumi atrodamas moduļa Konsolidācijas apgabalā Iestatīšana. Kad esat ievadījis kārtulas aprakstu, ir jāizvēlas uzņēmums, uz kuru šis korekciju žurnāls tiks grāmatots. Tam ir jābūt uzņēmumam, kuram juridiskās personas iestatījumos ir atlasīta opcija **Lietot finanšu korekciju procesā**. 

Ja nepieciešams, varat iestatīt datumu, kurā šī korekciju kārtula kļūst aktīva un kurā tās darbība beidzas. Ja vēlaties, lai tā būtu pieejama korekcijas priekšlikuma procesā, tad opcija **Aktīvs** ir jāiestata uz **Jā**. Atlasiet žurnāla nosaukumu, kura tips ir **Korekcija**.

Kad pamatinformācija ir definēta, varat definēt faktiskās apstrādes kārtulas, noklikšķinot uz **Rindas**. Korekcijām ir divas opcijas — neto izmaiņas summas koriģēšana vai fiksētas summas definēšana. 

Atlasiet savu pakalpojuma kontu. Varat izmantot zvaigznīti (\*) kā aizstājzīmi. Piemēram, 1\* kā sadalījuma datu avotu atlasītu visus kontus, kas sākas ar 1. 

Kad ir atlasīti jūsu avota konti, opcija **Konta specifikācijas** nosaka kontu no izmantotā mērķa uzņēmuma. Atlasiet vērtību **Avots**, ja vēlaties lietot to pašu galveno kontu, kurš definēts kontā **Avots**. Ja atlasāt vērtību **Lietotāja definēts**, tad jums ir jānorāda galamērķa konts. 

Dimensiju specifikācija darbojas tāpat. Ja atlasāt vērtību **Avots**, tad mērķa uzņēmumā tiks lietotas tādas pašas dimensijas kā avota uzņēmumā. Ja atlasāt vērtību **Lietotāja definēts**, tad jums ir jānorāda dimensijas mērķa uzņēmumā, noklikšķinot uz izvēlnes vienuma **Mērķa dimensijas**. 

Atlasiet avota dimensijas un finanšu dimensijas un vērtības, kuras tiek lietotas kā korekcijas avots.

## <a name="process-elimination-transactions"></a>Korekcijas transakciju apstrāde
Korekciju transakcijas var apstrādāt divos veidos — kamēr notiek konsolidēšana tiešsaistē vai izveidojot korekciju žurnālu un izpildot korekciju priekšlikuma procesu. Šajā sadaļā galvenā uzmanība ir vērsta uz žurnāla izveidošanu un korekcijas procesa izpildi. 

Ja kāds uzņēmums ir definēts kā korekcijas uzņēmums, tad modulī Konsolidācijas atlasiet vienumu **Korekciju žurnāls**. Pēc žurnāla nosaukuma atlasīšanas noklikšķiniet uz **Rindas**. Priekšlikumu varat palaist, atlasot izvēlni **Priekšlikumi** un pēc tam atlasot vienumu **Korekcijas priekšlikums**.

Atlasiet uzņēmumu, kurš ir konsolidēto datu avots, un pēc tam izvēlieties kārtulu, kuru vēlaties apstrādāt. Ievadiet sākuma datumu, kad sākt meklēt korekcijas summas, un beigu datumu, kad beigt meklēt korekcijas summas. Lauks **VG grāmatošanas datums** ir datums, kurš tiek izmantots žurnāla grāmatošanai virsgrāmatā. Kad noklikšķināt uz **Labi**, varat pārskatīt summas un grāmatot šo žurnālu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
