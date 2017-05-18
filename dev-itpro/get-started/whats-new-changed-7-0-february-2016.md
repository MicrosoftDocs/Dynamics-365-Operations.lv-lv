---
title: "Jaunumi un izmaiņas programmatūrā Dynamics AX 7.0 (2016. gada februāra izlaidumā)"
description: "Šajā rakstā ir aprakstītas funkcijas, kas versijā Microsoft Dynamics AX 7.0 ir jaunas vai ir mainītas. Šī versija satur gan platformas, gan programmas līdzekļus, un tā tika izlaista 2016. gada februārī."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 36d4aec3936ef99b880f3affc75df1b952cb3133
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Jaunumi un izmaiņas programmatūrā Dynamics AX 7.0 (2016. gada februāra izlaidumā)

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstītas funkcijas, kas versijā Microsoft Dynamics AX 7.0 ir jaunas vai ir mainītas. Šī versija satur gan platformas, gan programmas līdzekļus, un tā tika izlaista 2016. gada februārī.

<a name="cost-management"></a>Izmaksu pārvaldība
---------------

<table>

<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Gūstiet ātru apskatu par krājumu bilanci, nepabeigto darbu (NP) krājumu bilanci un par to, kāda atlasītajam finanšu gadam ir bijusi krājumu ienākošā un izejošā plūsma.</td>
<td>Nav attiecināms</td>
<td>Darbvieta <strong>Izmaksu administrēšana</strong> ietver sadaļu, kur tiek sniegts inventarizācijas akts vai NP inventarizācijas akts par atlasīto finanšu periodu. Šis akts ir balstīts uz datu kopas kešatmiņu, kura pēc noklusējuma tiek atjaunināta ik pēc 24 stundām. Datu kopas kešatmiņu var konfigurēt tā, lai lietotāji varētu to manuāli atjaunināt reāllaika atskaitēm. <strong>Datu atsvaidzināšanas statusa karte</strong> darbvietā <strong>Izmaksu administrēšana</strong> rāda, kad kešatmiņa tika atjaunināta pēdējo reizi.</td>
<td>Izmaksu kontrolleriem interesē, vai inventarizācijas vai NP inventarizācijas akta bilance laika gaitā palielinās vai samazinās. Operāciju notikumus klasificējot izrakstā, izmaksu kontrolleris var gūt pārskatu par krājumu plūsmu. Ja krājumi vai NO krājumi tiek vērtēti pēc standarta izmaksām, tad ir redzama arī vispārējā reģistrētā novirze.</td>
</tr>
<tr class="odd">
<td>Izmantojiet moduli <strong>Izmaksu pārvaldība</strong>.</td>
<td>Nav attiecināms</td>
<td>Izmaksu pārvaldība ir ieviesta kā domēna apgabals. Ar izmaksām saistītā konfigurācija un ieskati bija izkaisīti pa sadaļām Krājumu vadība, Ražošanas kontrole un Kreditori.</td>
<td>Tā kā visi ar izmaksu pārvaldību saistītie uzdevumi ir centralizēti vienā modulī, izmaksu kontrolleriem sistēmas uzturēšana tagad būs ērtāka.</td>
</tr>
<tr class="even">
<td>Ir atjaunināti ar krājumu uzskaiti un ražošanas uzskaiti saistītie grāmatošanas tipi.</td>
<td>Etiķetes formās <strong>InventPosting</strong>, <strong>Resource</strong>, <strong>ResourceGroup</strong> un <strong>ProductionGroup</strong> ne vienmēr atbilst faktiski lietotajām etiķetēm <strong>LedgerPostingType</strong>. Etiķetēs izmantotā terminoloģija nav viegli saprotama.</td>
<td>Etiķetes ir atjauninātas tā, lai etiķetes lapās <strong>InventPosting</strong>, <strong>Resource</strong>, <strong>ResourceGroup</strong> un <strong>ProductionGroup</strong> atbilstu faktiskajām <strong>LedgerPostingType</strong> etiķetēm. Turklāt visas etiķetes ir pārdēvētas tā, ka etiķetes atbilstu operāciju notikumiem. Ņemiet vērā, ka faktiskā grāmatošanas loģika nav mainījusies.</td>
<td>Sistēmas konfigurēšana ir vienkāršāka, jo jaunās etiķetes ir saistītas operāciju notikumiem, kas lieto šo grāmatošanas tipu.</td>
</tr>
<tr class="odd">
<td>Pirkšanas cenu, izmaksas vai pārdošanas cenu no programmas Microsoft Excel importējiet/eksportējiet uz izmaksu versiju vai otrādi.</td>
<td>Cenas vai izmaksas nevar pareizi importēt izmaksu versijā, jo datu modelim ir nepieciešams InventDim ID.</td>
<td>Datu elementu ieviešana sniedz iespēju ieviest importēšanas/eksportēšanas līdzekli. Šis līdzeklis lietotājiem ļauj importēt/eksportēt cenas vai izmaksas uz izmaksu aprēķināšanas versiju.
<ul>
<li>Importējiet pilnu sarakstu ar nākamā gada pirkšanas cenām, kas iegūts no Pirkšanas struktūrvienības.</li>
<li>Izmaksas un standarta pārdošanas cenas no galvenās pārvaldes ar vienu operāciju lietojiet vienam vai vairākiem pārdošanas uzņēmumiem.</li>
</ul></td>
<td>Šī iespēja izmaksas kontrolleriem var ietaupīt būtisku daudzumu laika, kad viņi veic sistēmas uzturēšanu, it īpaši, ja ir nepieciešams uzturēt iepriekš noteiktas izmaksas nākamajam finanšu gadam.</td>
</tr>
<tr class="even">
<td>Iegūstiet ātru pārskatu par krājumu bilanci un izmaksu objekta vidējām vienības izmaksām.</td>
<td>Lietotājam ir jāatver rīcībā esošā forma un jāatlasa krājumu dimensijas, kas atspoguļo izmaksu objektu. Līdz ar to lietotājam ir jāzina, kuras krājumu dimensijas bija atzīmētas attiecīgās preces finanšu krājumam.</td>
<td>Ieviesta jauna lapa <strong>Izmaksu objekts</strong>. Pēc noklusējuma šajā lapā tiek rādīti visi ar preci saistītie izmaksu objekti. Šajā lapā ir redzams pašreizējais krājumu daudzums, vērtība un vidējās vienības izmaksas katram izmaksu objektam.</td>
<td>Šī iespēja likvidē daļu sarežģītības un atvieglo izmaksu kontrollera darbu.</td>
</tr>
<tr class="odd">
<td>Krājumu kontroles laikā izmantojiet jauno lapu <strong>Izmaksu ieraksti</strong>.</td>
<td>Var būt sarežģīti veikt krājumu kontroli reģistrētajām krājumu transakcijām un saistītajām nosegšanas darbībām, jo vienas un tās pašas transakcijas var būt fizisks vai finansiālas.</td>
<td>Lapa <strong>Izmaksu ieraksti</strong> piedāvā jaunu veidu, kā skatīt krājumu transakcijas.
<ul>
<li>Transakcijas tiek rādītas hronoloģiskā secībā.</li>
<li>Ir iekļautas tikai transakcijas, kas ietekmē izmaksas.</li>
<li>Nav nekādas norādes uz fiziskām izmaksām vai finanšu izmaksām.</li>
<li>Nav nekādas norādes uz fizisku daudzumu vai finanšu daudzumu.</li>
<li>Izmaksas tiek pievienotas pakāpeniski.</li>
</ul></td>
<td>Šī iespēja kontrolleriem var ietekmēt būtisku daudzumu laika, kad krājumu kontrole viņiem ir jāveic transakcijas līmenī.</td>
</tr>
<tr class="even">
<td>Izmantojiet jauno dialoglodziņu <strong>Ražošanas NP pārskats</strong>, lai redzētu apkopotu skatu par konkrētai precei uzkrātajām izmaksām.</td>
<td>Nav attiecināms</td>
<td>NP pārskats rāda attiecīgā ražošanas pasūtījuma apkopotu NP bilanci, sagrupētu atbilstošās izmaksu klasifikācijas. Diagrammā hronoloģiskā secībā ir parādīts, kā operāciju grāmatojumi ir ietekmējusi NP bilanci.</td>
<td>Šī iespēja izmaksu kontrolleriem var ietaupīt daudz laika, kad viņiem ir nepieciešams uzzināt, kāda ir pašreizējā NP bilance noteiktā ražošanas pasūtījumā vai cik daudz materiālu attiecīgajam pasūtījumam ir patērēts.</td>
</tr>
<tr class="odd">
<td>Izmantojiet līdzekli Skatīt izmaksu salīdzinājumu, kas ir ieviests ražošanas pasūtījumos. Šis līdzeklis atvieglo ar ražošanas pasūtījumu saistīto izmaksu salīdzināšanu.</td>
<td>Lietotājs var salīdzināt tikai novērtētās izmaksas un faktiskās izmaksas. Salīdzinājumu var veikt viszemākajā līmenī.</td>
<td>Izmaksu salīdzinājuma līdzeklis izmaksu kontrolleriem ļauj salīdzināt šādus datus:
<ul>
<li>Aktīvās izmaksas pret Plānotajām izmaksām = Plānošanas novirze</li>
<li>Novērtētās izmaksas pret Faktiskajām izmaksām = Ražošanas novirze</li>
<li>Plānošanas novirze + Ražošanas novirze = Kopējā novirze</li>
</ul>
Šis līdzeklis darbojas neatkarīgi no izmaksu aprēķināšanas metodēm, kuras ir piešķirtas ražotajam krājumam. Pēc noklusējuma diagrammā ir redzams izmaksu salīdzinājumu pēc izmaksu grupas tipa. Diagramma lietotājiem sniedz iespēju skatīt detalizētākus līmeņus.</td>
<td>Šī iespēja izmaksu kontrolleriem vai ražošanas vadītājiem ļauj analizēt, kur rodas ražošanas novirzes un kas tās izraisa.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Izstrādātājs
|                                                                                                              |                                                                                                                                                                                                    |                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                                                         | **Dynamics AX 2012**                                                                                                                                                                               | **Dynamics AX 7.0**                                                                                                                                                                                                            | **Kāpēc tas ir svarīgi?**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Mākonī izveidojiet tīmeklī pieejamus risinājumus, kam var piekļūt no daudzām ierīcēm.                                 | Nav pieejams                                                                                                                                                                                      | Dynamics AX pašreizējā versija ir balstīta uz jaunu tīmekļa klienta un klienta struktūru.                                                                                                                                    | Saviem lietotājiem varat sniegt nākamās paaudzes risinājumus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Savu risinājumu izstrādāšanai lietojiet Microsoft Visual Studio.                                                       | Microsoft MorphX ir galvenā izstrādes vide, bet noteikta izstrāde notiek programmā Visual Studio.                                                                                                | Visual Studio ir vienīgā izstrādes vide.                                                                                                                                                                             | Tā patur jau pazīstamās Dynamics AX 2012 koncepcijas un nemanāmi pielāgo tās Visual Studio struktūrai un paraugiem. Tas ļauj izmantot standarta savstarpējo savietojamību ar citām .NET valodām un projektiem.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Kopējo starpniekvalodu (Common Intermediate Language — CIL) kompilējiet visiem līdzekļiem.                                                 | Valoda X++ tiek kompilēta uz P kodu.                                                                                                                                                                         | Pilnīgi jaunais X++ kompilators ģenerē CIL visiem līdzekļiem. CIL ir tā pati starpniekvaloda, ko izmanto citas valodas ar .NET bāzi.                                                                                   | CIL ir ātrāka, spēj efektīvāk izmantot atsauces uz klasēm pārvaldītajās dinamisko saišu bibliotēkās (Dynamic-Link Library — DLL) un spēj darboties uz lielas .NET utilītu rīku bāzes.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Biznesa informācijas (BI) atskaites un vizualizācijas iegulstiet Microsoft Dynamics AX klientā.             | Nav pieejams                                                                                                                                                                                      | Izveidojiet ārkārtīgi intuitīvas un plūstošas vizualizācijas.                                                                                                                                                                              | Šī iespēja sniedz lēmumu pieņemšanai nepieciešamos uz BI balstītos ieskatus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Integrējiet programmatūrā Microsoft Office.                                                                             | Nav pieejams                                                                                                                                                                                      | Jauno iespēju klāstā ietilpst programma Excel datu savienotājs, lapa **Darbgrāmatas veidotājs**, Eksportēšanas API un Dokumentu pārvaldība.                                                                                                        | Saviem lietotājiem varat izveidot produktivitātes risinājumus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Automatizējiet būvēšanu, testēšanu un izvietošanu.                                                                            | Daļēji pieejams                                                                                                                                                                                | Izvietojiet izstrādātāja topoloģiju, izmantojot izstrādātāja un būvējuma VM. Automātiski konfigurējiet būvējuma VM, lai atklātu, būvētu moduļus no Visual Studio Online (VSO) un izpildītu testus. Tiek atbalstīta C\# un X++ moduļu kompilēšana un atsauces. | Šī iespēja palielina izstrādātāju produktivitāti, samazinot izmaksas un testēšanai un pārbaudēm nepieciešamo darbu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Pielāgojiet ar pārklājumiem un paplašinājumiem.                                                                  | Paplašinājumi nav pieejami.                                                                                                                                                                       | Dynamics AX pašreizējai versijai ir jauns pielāgošanas modelis.                                                                                                                                                              | Varat pielāgot Microsoft vai trešo pušu Microsoft partneru sniegto modeļu elementu pirmkodu un metadatus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Veidojiet jaunas vadīklas un lietotāja interfeisa elementus, izmantojot X++ un modernu tīmekļa struktūru.                                  | Pielāgotās vadīklas ir atkarīgas no ārējām struktūrām, piemēram, struktūrām Microsoft ActiveX un Windows prezentāciju pamats (Windows Presentation Foundation — WPF).                                                                                   | Pašreizējā versijā vadīklu būvēšana ir vienkāršāka. X++ struktūru var lietot programmu funkcionalitātei un biznesa loģikai, un klients uz HTML/JavaScript bāzes ļauj izmantot modernas vizualizācijas.                         | Jūsu vadīklas var izstrādāt tā, lai tās izskatītos un darbotos tāpat kā Dynamics AX standarta komplektācijā iekļautās (Out-of-box — OOB) vadīklas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Novērtējiet un pielāgojiet veiktspēju, izmantojot jaunus rīkus.                                                            | Nav pieejams PerfSDK, Datu paplašināšanas rīkkopa, Trace Parser tīmekļa programma un PerfTimer.                                                                                                             | Jauno līdzekļu klāstā ietilpst PerfSDK, Datu paplašināšanas rīkkopa, Trace Parser tīmekļa programma un PerfTimer.                                                                                                                                                  | Programmatūras izstrādes komplekts (Software Development Kit — SDK) jums ļauj testēt un pārbaudīt visu būtisko biznesa procesu darbību viena lietotāja un, ja piemērojams, vairāklietotāju testa režīmā. Datu paplašināšanas rīkkopa jums ļauj pareizi izvērst visus veiktspējas testus, kam ir nepieciešams pareizi izvērst pamatdatus un transakciju datus. Trace Parser jums ļauj izpildīt viena lietotāja vai vairāklietotāju veiktspējas testu. PerfTimer jums ļauj redzēt, vai kāds no vaicājumiem vai jebkurš specifiskas metodes izsaukums izraisa kādas veiktspējas problēmas. Tāpēc jums nav nepieciešams veikt izsekošanu un visu detalizēti analizēt. |
| Atklājiet atjaunināmu skatu, izmantojot OData.                                                                        | Nav pieejams                                                                                                                                                                                      | Dynamics AX pašreizējā versijā tiek ieviests publisks OData pakalpojuma galapunkts, kas saskanīgā veidā ļauj piekļūt Dynamics AX datiem plašā klientu klāstā.                                                     | Jūsu risinājumi var mijiedarboties ar RESTful pakalpojumiem, koplietot datus atklājamā veidā un iespējot plašu integrēšanu, izmantojot HTTP steka protokolu.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Izmantojiet biznesa savienotāja priekšrocības, lai autorētu biznesa loģiku un atbalstītu integrēšanas scenārijus.         | Ir pieejamas biznesa savienotājs, ko var izsaukt X++ koda no pārvaldītā koda. Ir ieteicams izmantot biznesa savienotāju tikai C\# biznesa loģikas autorēšanai, nevis integrācijas scenārijiem. | Biznesa savienotājs vairs netiek atbalstīts. Autorēšanas prasības tiek nodrošinātas ar to, ka X++ kods tiek kompilēts par pārvaldītu kodu. Līdz ar to interop veikšana ir vienkāršāka. Integrēšanas scenāriji tiek izpildīti, izmantojot OData.       | Turpmāk biznesa savienotāju vairs nevarat izmantot.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Izvēlieties mērogu (t.i., decimāldaļu skaitu) reālos datu bāzes laukos un paplašinātos datu tipos (EDT). | Mērogs 16 ir noklusējuma mērogs, un izstrādātājs to nevar mainīt.                                                                                                                               | EDT un laukiem tagad ir mēroga rekvizīts, ko var lietot atsevišķam laukam un EDT. Pēc noklusējuma ir iestatīta vērtība 6, nevis 16.                                                                                                | Lietojot mazāku mērogu, veiktspēja ar NCCI tabulām (atmiņas atbalsts ar SQL) ir daudzkārt ātrāka. Mainiet mērogu, kā nepieciešams atsevišķo lauku lietošanai.                                                                                                                                                                                                                                                                                                                                                                                                               |
## <a name="financial-management"></a>Finanšu pārvaldība
<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Kontu struktūras eksportējiet uz Microsoft Excel.</td>
<td>Nav pieejams</td>
<td>Tagad varat atlasīt kādu konta struktūru un eksportēt to uz Excel.</td>
<td>Daudzi klienti pieprasīja iespēju kontu struktūras eksportēt uz Excel, lai filtrēšana būtu vienkāršāka.</td>
</tr>
<tr class="odd">
<td>Ar konta struktūru saistītās virsgrāmatas un papildu kārtulu struktūras skatiet vienā lapā.</td>
<td> Lietotājam ir nepieciešams pāriet uz vairākām formām, lai redzētu izmantoto virsgrāmatu un kontu struktūru. </td>
<td>Kontu struktūras lapai ir pievienota papildinformācija.</td>
<td>Definējot un rediģējot kontu struktūras, ir vienkāršāk piekļūt svarīgai informācijai.</td>
</tr>
<tr class="even">
<td>Ar kontu plānu saistītās virsgrāmatas skatiet vienā lapā.</td>
<td>Lietotājam ir nepieciešams pāriet uz katru uzņēmumu un atvērt virsgrāmatas formu, lai apskatītu šai virsgrāmatai piešķirto kontu.</td>
<td>Lapai **Kontu plāns** ir pievienota papildinformācija.</td>
<td> Definējot un piešķirot kontu plānus, ir vienkāršāk piekļūt svarīgai informācijai.</td>
</tr>
<tr class="odd">
<td>Slēguma lapas korekcijas un slēgšanas transakcijas skatiet atsevišķās kolonnās saraksta lapā **Apgrozījuma bilance**. </td>
<td>Abu tipu transakcijas lietotājs redz vienā kolonnā.</td>
<td>Saraksta lapai **Apgrozījuma bilance** ir pievienots papildu parametrs.</td>
<td>Tas ļauj veikt precīzāku datu analīzi, un noteiktās valstīs/reģionos tas ir arī nepieciešams normatīvo atskaišu sniegšanai. </td>
</tr>
<tr class="even">
<td>Izmantojiet jauno lapu **Globālais vispārējais žurnāls**.</td>
<td>Nav pieejams </td>
<td>Jauna lapa **Globālais vispārējais žurnāls**, kur ievadīt vispārējus žurnālus. Privilēģijas attiecībā uz šo lapu ir pievienotas lomai **Grāmatvedis**.</td>
<td>Šādi kopēja pakalpojuma grāmatvedis var ievadīt vispārējos žurnālus dažādos uzņēmumos, bez nepieciešamības aizvērt formu vai pārslēgt uzņēmuma kontekstu.</td>
</tr> 
<tr class="odd">
<td>Izmantojiet jauno lapu **Uzskaites avota pārlūks**.</td>
<td>Pieejama no Dynamics AX 2012 R3 CU10.</td>
<td>Jaunā lapa **Uzskaites avota pārlūks** un darbības, lai uz to pārietu no saraksta lapas **Apgrozījuma bilance** un lapas **Dokumentu transakcijas**.</td>
<td>Sniedz iespējas skatīt visdetalizētāko informāciju par apgrozījuma bilances avotu vai virsgrāmatas uzskaites ierakstu, vai ekspromtanalīzi.</td>
</tr>
<tr class="even">
<td>Pievienojiet papildu grāmatošanas līmeņus.</td>
<td>Papildu grāmatošanas līmeņu pievienošana bija izstrādātāju uzdevums.</td>
<td>Tagad ir pieejami desmit grāmatošanas līmeņi.</td>
<td>Vairums klientu pievieno papildu grāmatošanas līmeņus.</td>
</tr>
<tr class="odd">
<td>Izmantojiet opciju Saistītie dokumenti.</td>
<td>Nav pieejams</td>
<td>Opcija Saistītie dokumenti lietotājiem ir pieejama, lai starpuzņēmumu transakciju grāmatošanas laikā attiecīgo dokumentu redzētu korespondējošā uzņēmumā. No saistītajiem dokumentiem lietotāji var noklikšķināt uz detalizētās informācijas un ātri pāriet uz korespondējošā uzņēmuma dokumentu.</td>
<td>Grāmatojot starpuzņēmumu transakcijas, lietotājiem nebija iespējas redzēt korespondējošā uzņēmumā grāmatoto dokumentu vai izsekot uz to.</td>
</tr>
<tr class="even">
<td>Masveida finanšu perioda slēgšana</td>
<td>Nav pieejams</td>
<td>Lietotāji var atjaunināt moduļa piekļuvi un mainīt perioda statusu vairākiem uzņēmumiem vienlaicīgi.</td>
<td>Pirms šī līdzekļa ieviešanas lietotājiem bija jāmaina uzņēmums, kurā viņi bija pieteikušies, jāpāriet uz virsgrāmatas kalendāru formu un manuāli jāatjaunina moduļa piekļuve un perioda statuss.</td>
</tr>
<tr class="odd">
<td>Izmantojiet Oanda nodrošinātus valūtas maiņas kursus.</td>
<td>Maiņas kursa nodrošinātāja konfigurēšana, lai importētu maiņas kursus no Oanda, bija izstrādātāju uzdevums. </td>
<td>Ja lietotājiem ir atslēga Oanda pakalpojumam, viņi to var ievadīt, kad konfigurē valūtas maiņas kursa nodrošinātāju.</td>
<td>Lietotāji var izmantot standarta komplektācijā iekļauto funkcionalitāti, plānoti importējot Oanda nodrošinātos valūtas maiņas kursus.</td>
</tr>
<tr class="even">
<td>Filtrējiet finanšu atskaites (Management Reporter), pamatojoties uz dimensijām, atribūtiem, datumiem un scenārijiem. </td>
<td> Visa pārvaldības atskaišu sastādītāja atskaišu filtrēšana tiek veikta, izmantojot atskaites dizainu. Piemēram, ja lietotājs, kuram ir skatīšanas privilēģijas, vēlas skatīt kādu atskaiti citam datumam, atskaišu noformētājam ir jāveic šī modifikācija. </td>
<td>Ir pievienotas pārskatu opcijas, lai lietotājs, skatot pārskatu, varētu lietot dažādus filtrus. Šādā gadījumā, pamatojoties uz šiem filtriem, tiek ģenerēts jauns pārskats.</td>
<td>Finanšu atskaišu patērētāji var lietot dažādus filtrus dimensijām, datumiem, atribūtiem un scenārijiem, neprasot atskaišu noformējumu atjauninājumus.</td>
</tr>
<tr class="odd">
<td>Skatiet finanšu atskaites (Management Reporter) Microsoft Dynamics AX klientā.</td>
<td>Lai skatītu pārvaldības atskaišu sastādītāja atskaites, tika izmantots atsevišķs tīmekļa klients.</td>
<td>Visām finanšu atskaitēm var piekļūt Dynamics AX klientā. Lietotājs atlasa atskaiti, kuru vēlas skatīt, un šī atskaite tiek parādīta klientā.</td>
<td>Tagad finanšu atskaites varat skatīt bez nepieciešamības piekļūt citam klientam/programmai.</td>
</tr>
<tr class="even">
<td>Drukājiet finanšu atskaites (Management Reporter) no Microsoft Dynamics AX klienta.</td>
<td>Atskaites drukāšanai tiktu izmantotas pārlūka drukas opcijas drukāšanai, un tiktu izdrukāts tikai tas, ko lietotājs var redzēt ekrānā. </td>
<td>Lietotājs var izvēlēties atskaites detalizētības līmeni un lapas iestatījumus, Dynamics AX klienta finanšu atskaitē izmantojot opciju Drukāt.</td>
<td>Izdrukātās atskaites tiek drukātas veidā, kādā lietotāji tās vēlas, nevis kā tīmekļa lapas.</td>
</tr><tr class="odd">
<td>Analizējiet finanšu datus, izmantojot Power BI satura pakotni Finanšu veiktspējas pārraudzība.</td>
<td>Nav pieejams</td>
<td>Vietnē PowerBI.com atlasiet vienumu **Iegūt datus** un pēc tam atlasiet satura pakotni **Dynamics AX — Finanšu veiktspēja**. Ievadiet sava Dynamics AX galapunkta vietrādi URL, lai redzētu, kā jūsu dati tiek atspoguļoti šajā informācijas panelī.</td>
<td>Ar trīs vai četriem klikšķiem organizācijas var izvietot Power BI informācijas paneli, kas ietver svarīgus finanšu datus. Saturu var personalizēt pēc organizācijas.</td>
</tr>
<tr class="even">
<td>Izsekojiet finanšu perioda slēgšanas procesus.</td>
<td>Nav pieejams </td>
<td>Slēgšanas veidnes un grafikus var izveidot, izmantojot Finanšu perioda slēgšanas konfigurāciju. Izmantojiet darbvietu **Finanšu perioda slēgšana**, lai izsekotu slēgšanas grafiku norisi vairākos uzņēmumos.</td>
<td>Šī darbvieta likvidē manuālās sistēmas aktivitāšu definēšanai, plānošanai un paziņošanai. Tādējādi tiek samazināts dienu skaits līdz aizvēršanai.</td>
</tr>
<tr class="odd">
<td>Pārraugiet budžeta datu salīdzinājumu ar faktiskajiem datiem, un izveidojiet virsgrāmatas prognozes, izmantojot darbvietu **Virsgrāmatas budžeti un prognozes** un papildu uzziņu formas.</td>
<td>Nav pieejams</td>
<td> Darbvietai var piekļūt, izmantojot Dynamics AX informācijas paneli. Tā ietver saites uz vairākām jaunām uzziņu lapām: **Kopsavilkums par faktiskajām pret budžeta vērtībām**, **Budžeta kontroles statistikas kopsavilkums**, **Budžeta reģistra ieraksti** un **Budžeta plāni**.</td>
<td>Jaunas uzziņu lapas ļauj ērti piekļūt budžeta informācijai. Šajā darbvietā visi budžeta uzturēšanas un uzraudzības uzdevumi ir apkopoti vienuviet, ko budžeta vadītāji vai grāmatvedības vadītāji var ērti izmantot.</td>
</tr>
<tr class="even">
<td>Izveidojiet izkārtojumus budžeta plāniem un prognozēm.</td>
<td>Dokuments **Budžeta plāns** tiek skatīts kā saraksts ar rindām, kurās ir finanšu dimensiju kombināciju spēkā stāšanās datumi un summas. Lai budžeta plāna datus skatītu tabulā PivotTable, lietotājam ir jāizveido un jālieto Excel veidnes.</td>
<td>Budžeta plāniem un prognozēm ir pieejams neierobežots skaits izkārtojumu. Izkārtojumā varat kombinēt atlasītas finanšu dimensijas, lietotāja definētas kolonnas un citus rindu atribūtus (piem., komentārus, projektus un aktīvus). Lietotāji jebkurā laikā var pārslēgt izkārtojumu budžeta plāna dokumentam un rediģēt datus, izmantojot atlasīto izkārtojumu. Budžeta plānošanas konfigurācija ir vienkāršota, novēršot scenāriju ierobežojumus un izmantojot izkārtojumus, lai noteiktu, kādus datus var apskatīt un rediģēt katrā budžeta plāna dokumenta posmā.</td>
<td>Šādi tiek sniegtas elastīgas iespējas veidot un labot budžeta plānus, izmantojot Excel un Dynamics AX klientu. Excel darbgrāmatām paredzētās veidnes var ģenerēt, izmantojot izkārtojuma iestatījumus Budžeta plāns.</td>
</tr>
<tr class="odd">
<td>Drukājiet atskaiti **Kreditora rēķina transakcijas**, izmantojot informāciju no atskaites **Detalizēts apmaksas dienu saraksts**, kurā ir ietvertas nokavētās dienas. </td>
<td>Nepieciešams drukāt divas dažādas atskaites: **Detalizēts apmaksas dienu saraksts** un **Kreditora rēķina transakcijas**.</td>
<td>Abu atskaišu informācija ir apvienota atskaitē **Kreditora rēķina transakcijas**. Atskaite **Detalizēts apmaksas dienu saraksts** ir novecojusi. </td>
<td>Šādi tiek izslēgta nepieciešamība drukāt divas atsevišķas, bet saistītas atskaites.</td>
</tr>
<tr class="even">
<td>Normatīvās atskaites ģenerējiet tieši PDF formātā.</td>
<td>Vispirms jums normatīvā atskaite ir jāizveido vienā formātā, un pēc tam tā jāeksportē PDF formātā.</td>
<td>PDF formāts ir normatīvo atskaišu noklusējuma formāts.</td>
<td>Tādējādi tiek sniegta vienota attēlošana gan datora monitorā, gan drukātā papīra kopijā.</td>
</tr>
<tr class="odd">
<td>Pārdošanas nodokļa apmaksas procesu palaidiet kā pakešuzdevumu. </td>
<td>Nav pieejams</td>
<td>Lapā **Pārdošanas nodokļa apmaksas periods** varat norādīt, ka segšanas process ir jādarbina pakešrežīmā.</td>
<td>Periodiem, kas ietver daudzas nodokļu transakcijas, nosegšanas process var būt laikietilpīgs, un var noderēt iespēja šo procesu darbināt fonā kā pakešuzdevumu.</td>
</tr>
</tbody>
</table>





## <a name="foundation"></a>Fonds
<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Piekļūstiet klientam jebkurā laikā un jebkurā vietā. </td>
<td>AX 2012 darbvirsmas klients sniedz pilnīgu formu kopu, bet to var darbināt tikai datoros, kuros darbojas Microsoft Windows, un to ir nepieciešams instalēt. Bieži vien ar darbvirsmas klientu tiek lietots Termināļa serveris, lai iespējotu piekļuvi plašā apgabala tīklā (WAN). Uzņēmuma portāla tīmekļa klients nodrošina mazāku formu kopu.</td>
<td>Abi AX 2012 klienti ir aizstāti ar vienu, uz standartiem balstītu tīmekļa klientu, kas sniedz pilnīgu darbvirsmas klienta funkcionalitāti kopā ar uzņēmuma portāla klienta sasniedzamību.</td>
<td>Šādi tiek likvidēta izstrādes darbu sadalīšana starp abām UI platformām. Izmantojot standarta tīmekļa interfeisus, tiek izslēgta nepieciešamība pēc termināļa servera.</td>
</tr>
<tr class="odd">
<td>Produktīvi strādājiet, izmantojot jauno uzdevumu ierakstītāju.</td>
<td>AX 2012 uzdevumu ierakstītājam ir nepieciešama tieša piekļuve programmas objektu servera (Application Object Server — AOS) datoram un paaugstinātas privilēģijas, un tas nesniedz nekādas rediģēšanas opcijas.</td>
<td>Jauno uzdevumu ierakstītāju var izmantot tieši no tīmekļa klienta. Lai piekļūtu uzdevumu ierakstītājam, nav nepieciešamas administratora privilēģijas. Ierakstītās darbības var skatīt reālajā laikā, kad tās ierakstāt, ir ieviestas jaunas rediģēšanas opcijas, un Uzdevumu ierakstītājs atbalsta vairāk scenāriju, papildus jau esošajiem biznesa procesu modelētāja (BPM) scenārijiem.</td>
<td>Jaunais Uzdevumu ierakstītājs nodrošina racionalizētu funkcionalitāti un sniedz jaunas iespējas programmā Dynamics AX. Dažas no šīm iespējām ir pieejamas jau tagad, un turpmāk sekos vēl vairāk iespēju.</td>
</tr>
<tr class="even">
<td>Palīdziet lietotājiem labāk izprast viņu gaidāmo darbu ar darbvietām.</td>
<td>Lomu centri sniedz apskatu par informāciju, kas attiecas uz lietotāja darba funkciju uzņēmumā vai organizācijā.</td>
<td>Darbvietas ir jauns jēdziens programmatūrā Dynamics AX, un tām ir paredzēts aizstāt lomu centrus kā galveno veidu, kā pāriet uz uzdevumiem un konkrētām lapām. Tās nodrošina vienas lapas apskatu par biznesa aktivitāti un palīdz lietotājiem izprast pašreizējo statusu, gaidāmo noslodzi un procesa vai lietotāja veiktspēju. Darbvietas ir fragmentārākas nekā AX 2012 lomu centri, un lietotājam var būt piekļuve vairākām darbvietām.</td>
<td>Darbvietas ir paredzētas lietotāju produktivitātes palielināšanai. Izstrādātājiem būs nepieciešams izveidot darbvietu katrai nozīmīgajai produktā atbalstītajai “aktivitātei”. Mantojuma lomu centrs no versijas AX 2012 parasti tiks aizstāts ar vairākām darbvietām Dynamics AX pašreizējā versijā.</td>
</tr>
<tr class="odd">
<td>Lieciet formām reaģēt uz pārlūka skatvietas vai ierīces lielumu.</td>
<td>Versijā AX 2012 formas satura izvietojums bija stingri noteikts, izmantojot kolonnas, un kopējais formas augstums/platums lielā mērā bija noteikts, pamatojoties uz formā esošajam vadīklām.</td>
<td>Jaunākajā Dynamics AX versijā ir notikusi pāreja uz tīmekli, un tagad formas izmēri ir balstīti uz pārlūka skatvietas lielumu vai ierīci. Vadīklas un izkārtojuma parametri ir modificēti vai pievienoti, lai labāk reaģētu uz skatvietas lieluma izmaiņām.</td>
<td>Formas saturam ir jāspēj labāk reaģēt, lai optimāli izmantotu pieejamo pārlūka vai ierīces augstumu/platumu. Lai panāktu spēju reaģēt, var būt nepieciešamas izmaiņas formas modelēšanā.</td>
</tr>
<tr class="even">
<td>Izmantojiet modeļus, lai panāktu labāku formu izstrādes pieredzi.</td>
<td>Versijā AX 2012 formu veidnes bija pieejamas kā formu izstrādes sākumpunkts, pamatojoties uz formas stilu. Papildu pievienojumprogramma Formas stila pārbaudītājs sniedza informāciju par to, kā forma atšķīrās no tai atbilstošās veidnes.</td>
<td>Pašreizējā Dynamics AX versijā ir ieviesti formu modeļi. Formu modeļi ir formu veidņu un formas stila pārbaudītāja kombinācija, kas ir cieši integrēta izstrādātāja uzdevumos. Modeļi ir definēti formas līmenī (kā versijā AX 2012), un tagad ir pieejami apakšmodeļi grupas un cilnes lapas līmenī.</td>
<td>Formām, kas atbilst modeļiem, ir daudz priekšrocību, tostarp konsekventāks lietotāja interfeiss, vienkāršākā izstrādāšana, ērtāks formas jaunināšanas ceļš un lielāka uzticamība formas izkārtojuma reaģētspējai.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Palīdzība
<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Piekļūstiet strukturētai procedurālai palīdzībai (uzdevumu ceļvežiem) un konceptuālām tēmām, noklikšķinot uz **Palīdzība**.</td>
<td>AX 2012 palīdzības sistēma novirza uz HTML tēmām, kas tiek glabātas lokālajā tīmekļa serverī. Debitori un partneri var izveidot paši savu palīdzību.</td>
<td>Pašreizējā Dynamics AX versijā palīdzības sistēma rāda uzdevumu ceļvežus, kas tiek glabāti pakalpojumu Microsoft Dynamics Lifecycle Services (LCS) BPM. Palīdzības sistēma rāda arī tēmas no Microsoft dokumentu vietnes. Papildinformāciju skatiet tēmās [Dynamics AX palīdzība — darba sākšana](help-overview.md) un [Jaunie pieejamie uzdevumu ceļveži (2016. gada februāris)](new-task-guides-available-february-2016.md).</td>
<td>Uzdevumu ceļveži sniedz strukturētu, interaktīvu pieredzi, kas jūs vada caur uzdevuma vai biznesa procesa darbībām. Varat lejupielādēt un pielāgot uzdevumu ceļvežus, ko nodrošina Microsoft. Tēmā ir sniegts ātrāks un elastīgāks veids, kā izveidot, piegādāt un atjaunināt preces dokumentāciju. Tāpēc tā palīdz garantēt, ka jums ir pieeja visjaunākajai tehniskajai informācijai.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Cilvēkkapitāla pārvaldība
<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Prasmes un sertifikātus pēc kursu pabeigšanas pārsūtiet klases dalībniekiem.</td>
<td>Šis ir manuāls process.</td>
<td>Kad kurss ir pabeigts, kļūst pieejama jauna opcija dalībnieka ierakstus atjaunināt ar jaunajām prasmēm un sertifikātiem.</td>
<td>Tas nodrošina jaunu un efektīvu veidu, kā labot darbinieku ierakstus.</td>
</tr>
<tr class="odd">
<td>Ātri pārbaudiet nodarbinātību.</td>
<td>Šis ir manuāls process.</td>
<td>Jūsu personāldaļa var ātri pārbaudīt nodarbinātību, izmantojot darbvietu vai darbinieku lapu.</td>
<td>Personāldaļai vairs nav nepieciešams piekļūt vairākām lapām, lai pārbaudītu sākuma datumu, vadītāju, amatā pavadīto mēnešu skaitu un datus par atlīdzību.</td>
</tr>
<tr class="even">
<td>Ļaujiet darbiniekiem sistēmā skatīt, atjaunināt un dzēst informāciju.</td>
<td>Šī funkcija ir pieejama, bet ar ierobežotām skatīšanas un atjaunināšanas iespējām.</td>
<td>Šis līdzeklis ir iespējots, un darbiniekiem un darbuzņēmējiem ļauj skatīt dažādus personas datus. Ja vēlaties, var izmantot darbplūsmu, kad informācija tiek veidota, atjaunināta vai dzēsta.</td>
<td>Šādi darbiniekiem tiek ļauts kontrolēt savu informāciju — vai nu tas būtu saistībā ar adreses vai kontaktinformācijas atjaunināšanu, pieteikšanos darbā, anketas aizpildīšanu vai sava attēla atjaunināšanu. Kad ir iespējota kāda darbplūsma, informāciju var pārskatīt apstiprinātājs vai informāciju var apstiprināt automātiski, pamatojoties uz jūsu biznesa procedūrām.</td>
</tr>
<tr class="odd">
<td>Ļaujiet vadītājiem skatīt vai rediģēt informāciju par darbiniekiem.</td>
<td>Šī funkcija ir pieejama, bet ar ierobežotām skatīšanas un atjaunināšanas iespējām.</td>
<td>Atkarībā no konfigurācijas iestatījumiem un drošības vadītāji var skatīt vai rediģēt informāciju par darbiniekiem.</td>
<td>Tādējādi vadītāji var piekļūt svarīgiem datiem par darbinieku, lai varētu pieņemt labākus lēmumus par resursu sadalījumu, veiktspēju un darbinieku izaugsmi.</td>
</tr>
<tr class="even">
<td>Izmantojiet pārvaldnieka pašapkalpošanās funkcionalitāti.</td>
<td>Nav pieejams</td>
<td>Vadītāji tagad var iesniegt pieprasījumus pēc jaunas nolīgšanas (darbiniekiem un darbuzņēmējiem), pārcelšanas un izbeigšanas (darba attiecību pārtraukšanas). Tāpat vadītāji var pieprasīt jaunu amatu, paplašināt amatu ilgumu vai pieprasīt amatu izmaiņas.</td>
<td>Iepriekš šie scenāriji bija pieejami vienīgi personāla vadībai. Šo scenāriju iespējošana vadītājiem organizācijā sniedz jaudīgus rīkus. Varat iespējot papildu darbplūsmas, lai nodrošinātu atbilstošo pārskatīšanas un apstiprināšanas līmeni.</td>
</tr>
<tr class="odd">
<td>Piekļūstiet atlīdzību apstrādes rezultātiem.</td>
<td>Rezultāti ir pieejami tikai apstrādes laikā.</td>
<td>Kad process ir palaists, atlīdzības apstrādes rezultātiem tagad var piekļūt jebkurā laikā.</td>
<td>Šādi tiek nodrošināts lielisks procesa audits un procesa iznākums. Šādi tiek nodrošināts arī visaptverošs skats uz datiem, pirms tiek atjaunināti darbinieku ieraksti.</td>
</tr>
<tr class="even">
<td>Piekļūstiet atvieglojumu apstrādes rezultātiem.</td>
<td>Rezultāti ir pieejami tikai apstrādes laikā.</td>
<td>Kad process ir palaists, atvieglojumu apstrādes rezultātiem tagad var piekļūt jebkurā laikā.</td>
<td>Šādi tiek sniegts visaptverošs skats uz datiem, kas tiek atjaunināti ar atvieglojumu reģistrāciju un izmaksu izmaiņām.</td>
</tr>
<tr class="odd">
<td>Skatiet laika skalas “Spēkā stāšanās datums” izmaiņas.</td>
<td>Nav pieejams</td>
<td>Šis salīdzināšanas rīks ir pieejams darbiniekiem, amatiem un darbiem. Tas sniedz visaptverošu skatu uz izmaiņām dažādās ieraksta versijās.</td>
<td>Tādējādi jums tiek ietaupīts laiks, kad skatāt izmaiņas, kas laika gaitā ir notikušas darbinieku, amatu un darbu ierakstos. Šādi varat ātri salīdzināt divas ieraksta versijas vai visus ierakstus laika gaitā.</td>
</tr>
<tr class="even">
<td>Skatiet darbiniekus pēc uzņēmuma.</td>
<td>Šis ir manuāls process, kas tiek veikts, izmantojot filtrēšanu.</td>
<td>Darbinieku un darbuzņēmēju saraksti tiek automātiski filtrēti pēc uzņēmuma, kurā esat pieteikušies.</td>
<td>Šādi tiek sniegts filtrēts skats ar darbiniekiem, kas ir nodarbināti uzņēmumā, kurā esat pieteicies. Lai gūtu nefiltrētu skatu uz visiem darbiniekiem un darbuzņēmējiem, joprojām ir pieejams darbinieku saraksts. Dynamics AX pašreizējā versijā sistēma nemaina uzņēmumu, pamatojoties uz sarakstā atlasīto darbinieku.</td>
</tr>
<tr class="odd">
<td>Atjauniniet kursu dalībnieku sarakstu.</td>
<td>Nav pieejams</td>
<td>Kursu dalībniekus var noņemt no dalībnieku saraksta.</td>
<td>Šādi tiek nodrošināts vienkāršs veids, kā atjaunināt ierakstus par kursu dalībniekiem, kuri reģistrēti kļūdas dēļ.</td>
</tr>
<tr class="even">
<td>Pārvaldiet atlīdzību notikumus grupā.</td>
<td>Nav pieejams</td>
<td>Šis līdzeklis racionalizē darbinieku atlīdzību izmaiņu apstrādi.</td>
<td>Šādi tiek nodrošināta vienkārša, racionalizēta apstrāde darbinieka ierakstu atjaunināšanai, izmantojot atlīdzības darbvietu un saistītās lapas.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Krājumu vadība
Nav pievienoti jauni līdzekļi.

## <a name="localization"></a>Lokalizācija
<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Konfigurējiet un ģenerējiet elektroniskos dokumentus, lai ievērotu juridiskās prasības dažādās valstīs/reģionos.</td>
<td>Elektroniskie dokumenti ir iekodēti ar X++ vai kā paplašināmās stila lapas valodas transformācijas (XSLT). Lai veiktu jebkādas formāta korekcijas, ir jāveic izstrādes darbs. Piekļuve datiem un formatējumam nav izolēta. Pielāgotai formāta izvietošanai ir nepieciešama jauna Microsoft Dynamics AX labojumfailu pakotne, kas ignorē esošo formātu. Pielāgotas katra formāta modifikācijas ir nepieciešams manuāli portēt uz jaunas Microsoft Dynamics AX labojumfailu pakotnes pirmkodu.</td>
<td>Elektronisko atskaišu veidošana (Electronic Reporting — ER) ir jauns elektronisko dokumentu konfigurēšanas un veidošanas rīks, kura mērķauditorija ir biznesa lietotājs, nevis izstrādātājs. ER kā dokumentu formātu datu avotus ļauj iestatīt datu modeļus, kas ir atkarīgi no domēna, bet ir neatkarīgi no Microsoft Dynamics AX datu bāzes. Biznesa lietotājs var konfigurēt formātus, pamatojoties uz šiem no domēna atkarīgajiem datu modeļiem (piemēram, maksājumiem, Intrastat atskaitēm vai nodokļu atskaitēm). Lietotājs konfigurē formātus, izmantojot vienkāršus vizuālos rīkus, kas ir līdzīgi kā programmā Excel. Pašlaik ER atbalsta elektronisko dokumentu ģenerēšanu teksta, XML un Excel formātā. Šos dokumentus var ģenerēt vienlaicīgi un iepakot zip failos. Datu modeļiem un formātiem tiek atbalstīta versiju izveide. Formāta versijām var būt derīguma periodi. Katrs datu modelis vai formāta versija tiek glabāti atsevišķā konfigurācijā un izplatīti partneriem un debitoriem, izmantojot LCS. Partneri un debitori var pielāgot Microsoft datu modeļus un formātus vai izveidot paši savus. ER šādas partneru un debitoru veiktās konfigurācijas izmaiņas saglabā kā izmaiņas Microsoft konfigurācijās, tādējādi vienkāršojot jaunināšanu uz jaunām Microsoft konfigurāciju versijām. Izmantojot LCS, partneri savu datu modeli un formāta konfigurācijas var arī kopīgot ar citiem partneriem un debitoriem, kuri tos var pielāgot un kopīgot. Izmaiņu pielāgošana un vienkārša jaunināšana tiek atbalstītas visā pielāgošanas ķēdē.</td>
<td>ER vienkāršo elektronisko dokumentu formātu izveidošanu, uzturēšanu un jaunināšanu, lai ievērotu juridiskās prasības dažādās valstīs/reģionos. ER paātrina un vienkāršo elektronisko dokumentu formātu veidošanas un pārbaudīšanas procesu. Šīs izmaiņas var veikt biznesa lietotāji, nevis izstrādātāji. Partneriem un debitoriem ER ļauj ātrāk un vieglāk savus formāta pielāgojumus jaunināt uz jaunām formātu versijām, kuras izlaiž Microsoft vai citi partneri. ER sniedz vienotu veidu (izmantojot LCS), kā Microsoft un partneri elektronisko dokumentu konfigurācijas var izplatīt citiem partneriem un debitoriem. Turklāt ER partneriem un debitoriem vienkāršo elektronisko dokumentu formātu pielāgošanu, jaunināšanu un izplatīšanu savām specifiskajām biznesa vajadzībām.</td>
</tr>
<tr class="odd">
<td>(MEX) Ģenerējiet Meksikas pievienotās vērtības nodokļa (PVN) normatīvās atskaites.</td>
<td>Atskaites **Pārdošanas un pirkšanas PVN** ir jāģenerē, izmantojot nerealizētā PVN funkcionalitāti, lai lietotāji atkarībā no statusa varētu identificēt transakcijas, kas pieder realizētajai un nerealizētajai sadaļai.</td>
<td>Atskaites **Pārdošanas un pirkšanas PVN** tika mainītas, un tagad nosacījuma nodokļa līdzeklis tiek ņemts vērā, tikai izmantojot īpašus apmaksas periodus nerealizētā un realizētā pārdošanas nodokļa kodu definīcijai.</td>
<td>Lai lietotāji šīs atskaites varētu ģenerēt pareizi, ir nepieciešams mainīt pārdošanas nodokļa kodu konfigurāciju. Nosacījuma pārdošanas nodokļa līdzeklis ir nepieciešams, un lietotājam ir nepieciešams konfigurēt atsevišķus apmaksas periodus, nerealizētos un realizētos, lai identificētu transakcijas saistītajos sadaļu apgabalos.</td>
</tr>
<tr class="even">
<td>(JPN) Pārvaldiet Japānas pamatlīdzekļu paātrinātā nolietojuma deklarācijas dokumentu.</td>
<td>Nav pieejams</td>
<td>Svarīga deklarācijas informācija tiek centralizēti glabāta vienā dokumentā, lai uzturēšana notiktu labāk.</td>
<td>Dokumentu atbilstība un pārvaldības ērtums palīdz samazināt problēmas auditēšanas un citu pārskatu laikā.</td>
</tr>
<tr class="odd">
<td>(JPN) Pārbaudiet JBA rakstzīmes bankas kontā.</td>
<td>Nav pieejams</td>
<td>Varat pārbaudīt, vai ar kana rakstītie nosaukumu lauki ietver ir tikai tādas rakstzīmes, ko atļauj JBA bankas formāts.</td>
<td>Šādi lietotājiem maksājumu failu ģenerēšanas laikā tiek mazināti pārtraukumi, kas rodas nederīgu rakstzīmju dēļ.</td>
</tr>
<tr class="even">
<td>(JPN) Atgūstiet Japānas pamatlīdzekļu sīknaudas starpību finanšu gada beigās.</td>
<td>Nav pieejams</td>
<td>Lapā **Pamatlīdzekļu parametri** varat izvēlēties, vai atgūšanu veikt finanšu perioda vai finanšu gada beigās.</td>
<td>Šāda izvēle sniedz lielāku elastību, lai pieskaņotos vietējai praksei.</td>
</tr>
<tr class="odd">
<td>(JPN) Ģenerējiet Japānas korporatīvo nodokļu deklarācijas pievienotās tabulas nr. 16 ar kopsavilkuma summu pēc pamatlīdzekļu galvenā veida.</td>
<td>Nav pieejams</td>
<td>Pamatlīdzekļu vērtību modeļiem varat izvēlēties veikt kopsavilkumu pēc galvenā veida. Pēc noklusējuma šī funkcionalitāte tiek izmantota jaunizveidotiem pamatlīdzekļiem.</td>
<td>Lielām korporācijām, kurām ir tūkstošiem pamatlīdzekļu, kopsavilkuma atskaites ievērojami samazina ģenerējamās atskaites lielumu.</td>
</tr>
<tr class="even">
<td>(JPN) Japānas pamatlīdzekļiem speciālo nolietojuma rezervi sāciet piešķirt no nākamā finanšu gada.</td>
<td>Nav pieejams</td>
<td>Tādu pamatlīdzekļu vērtību modeļiem, kam ir atbilstoša ārkārtas nolietojuma tabula, varat izvēlēties sadalījumu sākt no nākamā finanšu perioda vai no nākamā finanšu gada.</td>
<td>Šāda izvēle sniedz lielāku elastību, lai pieskaņotos vietējai praksei.</td>
</tr>
<tr class="odd">
<td>(JPN) Ģenerējiet Japānas patēriņa nodokļu atskaiti, kas ietver pārskatītās nodokļu likmes.</td>
<td>Patēriņa nodokļu atskaite ir pieejama 5 procentu nodokļa likmei.</td>
<td>Patēriņa nodokļa atskaite ietver sadaļu pārskatītajai nodokļa likmei (piemēram, 8 procenti).</td>
<td>Valdība tikko izsludināja šo izkārtojumu.</td>
</tr>
<tr class="even">
<td>(ES) Konfigurējiet noapaļošanas iestatījumus ES pārdošanas sarakstā.</td>
<td>Noapaļošanas iestatījumi ES pārdošanas saraksta atskaišu veidošanai dažādām valstīm/reģioniem ir iekodēti ar X++ vai kā paplašināmās stila lapas valodas transformācijas (XSLT).</td>
<td>Noapaļošanas iestatījumi tiek pievienoti ārējās tirdzniecības parametriem. Varat konfigurēt noapaļošanas precizitāti, noapaļošanas metodi, izvades precizitāti un par noapaļošanas precizitāti mazāku summu darbību.</td>
<td>Šādi tiek apvienota un vienkāršota ES pārdošanas saraksta atskaišu veidošanas konfigurācija. Noapaļošanas iestatījumu koriģēšanai vairs nav nepieciešams izstrādes darbs.</td>
</tr>
<tr class="odd">
<td>(ES) Konfigurējiet apgrieztās maksāšanas piemērojamības kārtulas.</td>
<td>Apgrieztās maksāšanas piemērojamības kārtulas ir iestrādātas iekšzemes apgrieztās maksāšanas scenārijam. Piemērojamību slieksni var iestatīt krājumu grupai. Šī funkcionalitāte ir pieejama tikai Lielbritānijai.</td>
<td>Apgrieztās maksāšanas piemērojamības kārtulas varat konfigurēt pēc dokumenta tipa (pirkšanas/pārdošanas pasūtījums, kreditora rēķins, brīva teksta rēķins un citi) un apgrieztās maksāšanas grupa, kas apvieno krājumus, krājumu grupas un pirkšanas/pārdošanas kategorijas. Piemērojamības kārtulas ir ar spēkā stāšanās datumu. Varat arī pārdošanas nodokļu grupās atzīmēt atsevišķus pārdošanas nodokļu kodus kā piemērojamus apgrieztajai maksāšanai. Pārdošanas rēķina atskaite tiek koriģēta, lai parādītu apgrieztās maksāšanas informāciju. Šī funkcionalitāte ir pieejama visām Eiropas valstīm/reģioniem.</td>
<td>Ar šo izmaiņu tiek apvienota apgrieztās maksāšanas piemērojamības kārtulu konfigurācija un tiek atbalstīta Eiropas valstu/reģionu iekšzemes apgrieztās maksāšanas regulu pieņemšana.</td>
</tr>
<tr class="even">
<td>(DE) Ģenerējiet vācu audita failu — GDPdUGoBD</td>
<td>Lietotāji var iestatīt definīciju tabulām, kurās ir finanšu dati, ko ir paredzēts eksportēt Vācijas auditoru un iestāžu pieņemtajā formātā.</td>
<td>Šis līdzeklis ir ieviests kā elektronisko pārskatu konfigurācija. Šī funkcionalitāte ir pieejama Vācijai un Austrijai.</td>
<td>Šī izmaiņa lietotājam sniedz daudz plašākas datu formatēšanas un pārveidošanas iespējas, kā arī nodrošina visas priekšrocības, kas ir saistītas ar elektronisko atskaišu konfigurācijas darbības cikla pārvaldību, piemēram, vienkāršu konfigurācijas apmaiņu, versiju izmantošanu un citas priekšrocības.</td>
</tr>
<tr class="odd">
<td>(FR) Bilances saraksts ar grupu kopsummu kontiem (atskaite).</td>
<td>Atskaite Bilances saraksts ar grupu kopsummu kontiem ir ieviesta kā SSRS atskaite (LedgerAccountSum\_FR).</td>
<td>Atskaite Bilances saraksts ar grupu kopsummu kontiem ir ieviesta kā Management Reporter atskaite, un tā ir pieejama LCS līdzekļu bibliotēkas lokalizēto finanšu atskaišu mapē.</td>
<td>Tādējādi lietotāji no finanšu atskaišu lietošanas līdzeklī Management Reporter var gūt visas priekšrocības un brīvas pielāgošanas iespējas.</td>
</tr>
<tr class="even">
<td>(EU) Avizo, dalības piezīme un kontroles atskaites maksājumiem.</td>
<td>Visas šīs atskaites ir ieviestas, kā arī SSRS atskaites.</td>
<td>Šīs atskaites ir ieviestas kā Open XML veidnes, kuras paredzēts lietot programmā Microsoft Excel.</td>
<td>Elektronisko maksājumu konfigurācijas satur maksājuma failu formātu iestatījumus un veidnes. Tādējādi lietotāji no elektronisko atskaišu veidošanas var gūt visas priekšrocības un brīvas atskaišu pielāgošanas iespējas.</td>
</tr>
<tr class="odd">
<td>(EU) Konfigurējiet Intrastat noapaļošanas iestatījumus.</td>
<td>Noapaļošanas iestatījumi Intrastat atskaišu veidošanai dažādām valstīm/reģioniem ir iekodēti ar X++ vai kā paplašināmās stila lapas valodas transformācijas (XSLT).</td>
<td>Noapaļošanas iestatījumi tiek pievienoti ārējās tirdzniecības parametriem. Varat konfigurēt noapaļošanas precizitāti, noapaļošanas metodi, izvades precizitāti un par noapaļošanas precizitāti mazāku summu darbību.</td>
<td>Šādi tiek apvienota un vienkāršota Intrastat atskaišu veidošanas konfigurācija. Noapaļošanas iestatījumu koriģēšanai vairs nav nepieciešams izstrādes darbs.</td>
</tr>
<tr class="even">
<td>(EU) Intrastat preču kodus iestatiet kategoriju hierarhijās.</td>
<td>Intrastat preču kodi ir atsevišķs saraksts. Lai gan pastāv kategoriju hierarhija ar tipu Preces kods, taču Retail HQent un pārdošanas kategorijās šie preču kodi tiktu atiestatīti uz noklusējuma vērtībām.</td>
<td>Atsevišķs Intrastat preču kodu saraksts tiek sapludināts ar produktu hierarhiju, kuras veids ir Preču kods.</td>
<td>Šādi preču kodu piešķiršana izlaistajiem produktiem tiek apvienota ar kategorijām pārdošanas un iepirkuma dokumentos.</td>
</tr>
<tr class="odd">
<td>(EU) Ziņot par Intrastat daudzumu papildu vienībās, izmantojot vienības pārveidošanas iestatījumu.</td>
<td>Intrastat preču kodam ir teksta lauks papildu vienību norādīšanai, un kartē **Prece** ir lauks papildu vienību daudzuma norādīšanai kilogramos.</td>
<td>Papildu vienības Intrastat preču kodam tiek izvēlētas no saraksta Vienības. Papildu vienību daudzums tiek aprēķināts, izmantojot vienības pārveidošanas iestatījumus.</td>
<td>Tādējādi pārrēķināšana no transakcijas vienībām tiek apvienota ar papildu vienībām.</td>
</tr>
<tr class="even">
<td>(EU) Piegādes veidam piešķiriet noklusējuma transportēšanas metodi.</td>
<td>Nav pieejams</td>
<td>Piegādes veidam ir pievienots lauks noklusējuma transportēšanas metodei.</td>
<td>Līdz ar to tiek vienkāršota sagatavošanās Intrastat atskaišu veidošanai.</td>
</tr>
<tr class="odd">
<td>(EU) Atzīmējiet izlaistās preces, kuras nav paredzēts iekļaut Intrastat atskaitēs.</td>
<td>Nav pieejams</td>
<td>Izlaistajai precei ir pievienota opcija šo krājumu izslēgt no Intrastat atskaitēm.</td>
<td>Līdz ar to tiek vienkāršota sagatavošanās Intrastat atskaišu veidošanai.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Ražošana
|                                                                                                                                                      |                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                                                                                                 | **Dynamics AX 2012**                                                                                                             | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Kāpēc tas ir svarīgi?**                                                                                                                                                                                                                                            |
| Ražošanas pasūtījumiem izpildiet materiālu pieejamības pārbaudes atsevišķā lapā, kas tiek atvērta no darbvietas **Ražošanas stāva pārvaldība**. | Nav pieejams                                                                                                                    | Ražošanas supervizors var pārbaudīt, vai plānotajiem ražošanas pasūtījumiem nepieciešamajā datumā ir pieejami materiāli. Darbvietā ražošanas supervizors var redzēt, cik daudz ražošanas pasūtījumu ir plānotajā stāvoklī un gaida izlaišanu. Pamatojoties uz dinamisko vispārējo plānu, informācija par materiālu pieejamību tiek atjaunināta, ja rīcībā esošie krājumi atbilst šīm materiālu prasībām faktiskajiem vai plānotajiem pasūtījumiem. Pamatojoties uz informāciju par materiālu pieejamību, supervizors var izlaist pasūtījumus lapā **Materiālu pieejamība**.                                                                                                                                                                                                                                                                                                                        | Šādi ražošanas vadītāji var pieņemt pareizos lēmumus par materiālu sadalījumu pasūtījumiem, kad ražošanas pasūtījumi tiek izlaisti uz ražotni.                                                                                                       |
| Sāciet ražošanas darbus un ziņojiet par to norisi, izmantojot jauno lapu **Darbu kartes ierīce**.                                                              | Forma **Darba reģistrācija** galvenokārt tiek izmantota par mērķi lielos termināļa ekrānos, un UI elementiem parasti var piekļūt ar peles klikšķiem. | Lai gan jaunā lapa **Darbu kartes ierīce** ir ļoti vienkārša, tā ir paredzēta arī skārienvadībai. Šī lapa labi ietilpst mobilajās ierīcēs, piemēram, planšetdatoros un tālruņos. Ražotnes darbinieks konstatēs mazāku informācijas pārslodzi un intuitīvāku lietošanas ērtumu. Darbinieks var veikt tradicionālos uzdevumus, piemēram, darba sākšanu, beigšanu un ziņošanu par norisi. Papildus strādāšanai pie faktiskā darba vai atteikšanās un aiziešanas reģistrēšanai, darbinieks var skatīt pielikumus, paņemt pusdienu pārtraukumu un veikt citas darbības. Darbi darbiniekam tiek sarindoti plānotā secībā, bet darbinieks tos var arī izvēlēties. Šī lapa galvenokārt ir paredzēta atsevišķām ražošanas operācijām, kur materiāli tiek sagatavoti ražošanai. Scenārijiem, kas ir saistīti ar atskaitīšanos par līdzproduktiem un blakusproduktiem un ar materiālu izdošanu, izsekojot dimensijas, lietojiet lapu **Darba reģistrācija**. | Ieviešot alternatīvu UI, kas ir paredzēts pieskārieniem un kam var piekļūt no visu veidu ierīcēm, piemēram, termināļa ekrāniem un mobilajām ierīcēm, šis līdzeklis palīdzēs samazināt tradicionālās ražotnes reģistrāciju izlaides īstenošanas izmaksas. |

## <a name="master-planning-and-forecasting"></a>Vispārējā plānošana un prognozēšana
|                                                                                                                            |                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                                                                       | **Dynamics AX 2012**                                                                                                                                                                                                                                                                          | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                               | **Kāpēc tas ir svarīgi?**                                                                                                                              |
| Brīdiniet lietotāju, ja pārdošanas pasūtījums vai ražošanas pasūtījums nav gatavs piegādei līdz paredzētajam datumam.                         | Vispārējās plānošanas izveidotie brīdinājumi tiek saukti par *aizkavēšanās paziņojumiem*. *Aizkavēšanās* ir starp divām pusēm noslēgts līgums par kāda līdzekļa pirkšanu vai pārdošanu par cenu, par kuru puses ir vienojušās šodien (*aizkavēšanās cenu*), lai gan piegāde un maksājums tiks veikts vēlāk (*piegādes datumā*). | *Aizkavēšanās ziņojumi* un *aizkavēšanās datumi* ir pārdēvēti par attiecīgi *aprēķinātajām aizkavēm* un *aizkavēšanās datumiem*.                                                                                                                                                                                                                                                   | AX 2012 versijā lietotā terminoloģija bija neprecīza un izraisīja nepareizus tulkojumus.                                                               |
| Gūstiet ātru ieskatu par vispārējās plānošanas izpildes statusu, steidzami plānotajiem pasūtījumiem un plānotajiem pasūtījumiem, kas izraisa aizkaves. | Šī informācija ir pieejama, bet tā ir izkaisīta pa vairākām formām.                                                                                                                                                                                                                       | Darbvieta **Vispārējā plānošana** sniedz acumirklī uztveramu informāciju par laiku, kad tika izpildīta pēdējā vispārējā plānošana, vai radās kādas kļūdas, kādi ir steidzami plānotie pasūtījumi un kuri plānotie pasūtījumi izraisa aizkaves.                                                                                                                                   | Varat lietderīgi izmantot darbvietas sniegto apskatu. Saistītā informācija ir apkopota tā, lai vadītu vispārējo plānošanu un palīdzētu uzlabot produktivitāti. |
| Izmantojiet programmu Excel, lai atjauninātu pieprasījuma apjoma prognozes.                                                                                      | Nav pieejams                                                                                                                                                                                                                                                                                 | Kad ievadāt pieprasījuma apjoma prognozes, veicat atjauninājumus un dzēšat pieprasījuma apjoma prognozes, varat izmantot integrāciju ar Excel.                                                                                                                                                                                                                             | Tas palīdz uzlabot efektivitāti un produktivitāti.                                                                                                          |
| Prognozējiet turpmāko pieprasījumu un izveidojiet pieprasījuma apjoma prognozes, pamatojoties uz vēsturiskiem transakciju datiem.                                  | Versijā Microsoft Dynamics AX 2012 R3 prognožu modeļi Microsoft SQL Server analītiskajos pakalpojumos tiek izmantoti, lai izveidotu pieprasījuma apjoma prognozes.                                                                                                                                                | Novērtējiet nākotnes pieprasījumu, izmantojot Microsoft Azure mašīnmācīšanās mākoņa pakalpojuma jaudu un vērienu. Mašīnmācīšanās prognozēšanas modeļi ir vienkārši lietojami un paplašināmi, lai atbilstu debitoru vēlmēm. Pakalpojums veic visatbilstošāko modeļu atlasi un piedāvā galvenos veiktspējas rādītājus (Key Performance Indicators — KPI), ko var izmantot, lai aprēķinātu prognozes precizitāti. | Ģenerējiet precīzākas prognozes, izmantojot mašīnmācīšanās metodes.                                                                              |
| Optimizējiet pasūtījuma datumu un daudzumu, pamatojoties uz vispārējās plānošanas izpildes sniegto vizuālo apskatu pār saistītajām darbībām.          | Darbību diagrammas apskats ir pieejams, bet tajā tiek rādītas visas saistītās darbības. Kad darbības tiek lietotas, tās nekavējoties pazūd no šī skata.                                                                                                                                             | Darbību diagramma sniedz labāku apskatu. Tā ietver opcijas, kuras jums ļauj rādīt tikai lietotās darbības un tieši saistītās darbības. Kad darbības tiek lietotas, ir tiek pelēkotas, bet joprojām tiek rādītas. Tāpēc apskats tiek saglabāts. Darbību diagrammai ir pievienota papildinformācija, lai datus parādītu vienā lapā.                               | Jūsu produktivitāte uzlabojas, jo koncentrējaties tikai uz svarīgajām darbībām.                                                              |

## <a name="procurement-and-sourcing"></a>Sagāde un avoti
|                                                                                                                                                         |                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                                                                                                    | **Dynamics AX 2012** | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | **Kāpēc tas ir svarīgi?**                                                                                                                                                                                                               |
| Izmantojiet darbvietu **Pirkšanas pasūtījumu sagatavošana**, lai gūtu ātru ieskatu par sagatavošanā esošo pirkšanas pasūtījumu statusu.                      | Netiek atbalstīts        | Darbvieta **Pirkšanas pasūtījumu sagatavošana** sniedz apskatu par pasūtījumiem no brīža, kad tie tiek izveidoti kā melnraksts, un darbplūsmā seko līdzi to apstiprināšanas stāvokļiem un tālāk uz ratificēšanu.                                                                                                                                                                                                                                                                                                                      | Jūsu pirkšanas struktūrvienībai vairs nav nepieciešams meklēt informāciju no vairākām lapām — tagad struktūrvienība var izmantot darbvietas sniegto apskatu.                                                                                         |
| Izmantojiet darbvietu **Pirkšanas pasūtījuma ieejas plūsma un papilddati**, lai gūtu ātru ieskatu par pirkšanas pasūtījumiem, kas gaida ieejas plūsmu, lai palīdzētu ar turpmākajiem datiem un darbībām. | Netiek atbalstīts        | Darbvieta **Pirkšanas pasūtījuma ieejas plūsma un papilddati** sniedz apskatu par ratificētajiem pirkšanas pasūtījumiem, kuri gaida ieejas plūsmu vai sūtījumus. Šī darbvieta ietver sarakstus ar nokavētajām ieejas plūsmām un gaidošajām ieejas plūsmām, lai palīdzētu ar proaktīvo pārskatīšanu un piegādātāja turpmākajiem datiem un darbībām. Šajā darbvietā ir arī uzskaitīti pirkšanas pasūtījumi, kuriem noliktavā ir notikusi saņemšanas reģistrācija, lai palīdzētu garantēt, ka ieejas plūsma tiek grāmatota. Pārskatīšanai ir pieejamas pirkšanas pasūtījumu atgriešanas, kas vēl nav nosūtītas. | Jūsu pirkšanas struktūrvienība var izmantot šīs darbvietas sniegto apskatu. Saistītā informācija ir apkopota tā, lai vadītu turpmāko datu un darbību procedūras un palīdzētu uzlabot produktivitāti.                                                                |
| Pirkšanas pasūtījumus sūtiet ratificēšanai uz kreditoru portālu, kurš tiek viesots Dynamics AX klientā. Ļaujiet kreditoram apstiprināt vai noraidīt.                            | Netiek atbalstīts        | Kreditoru portāla interfeiss kreditoriem ļauj saņemt pirkšanas pasūtījumus, ko nepieciešams apstiprināt vai noraidīt. Tas kreditoram ļauj arī gūt pārskatu par visiem ratificētajiem pirkšanas pasūtījumiem attiecībā uz kādu kontu. Pirkšanas aģents var sūtīt pirkšanas pasūtījumu, pieprasot ratificēšanu no kreditora. Kreditoram ir jābūt reģistrētam Microsoft Azure Active Directory (Azure AD) lietotājam pakalpojumā Dynamics AX, attiecīgā kreditora kontaktpersonai, un šim kreditoram ir nepieciešama īpaša drošības loma.                                                     | Jūsu pirkšanas struktūrvienība var izmantot mazināto dokumentācijas apjomu un manuāli sekot līdzi atbildēm par pirkšanas pasūtījumiem, tām ieplūstot tieši sistēmā. Izmantojot vienu patiesības avotu, mazinās iespējamība, ka debitoram un kreditoram radīsies pārpratumi. |

## <a name="projects"></a>Projekti
|                                        |                                                                                         |                                                                                                                                              |                                                          |
|----------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Ko iespējams izdarīt?**                   | **Dynamics AX 2012**                                                                    | **Dynamics AX 7.0**                                                                                                                          | **Kāpēc tas ir svarīgi?**                               |
| Rezervējiet darbiniekus projektos kā resursus. | Līdzīgi kā resursi, arī darbinieki projektos tiek tieši rezervēti papildus resursiem. | Tabulu Resurss, kur tiek glabāti resursi ražošanai un izgatavošanai, tagad var izmantot, lai projektam kā resursus rezervētu darbiniekus. | Kad rezervējat projektus, jums ir nepieciešams rezervēt tikai resursus. |

## <a name="retail-sales-marketing-and-customer-service"></a>Mazumtirdzniecības pārdošana, mārketings un debitoru apkalpošana
### <a name="retail-hq"></a>Retail HQ

Microsoft Azure viesotais līdzeklis Retail HQ piedāvā visu komerciālo operāciju aspektu centralizētu pārvaldību un pilnīgu pārskatāmību, izmantojot tīmekļa klientu.

<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Veiciet tirgū virzīšanas operācijas.</td>
<td>Lietotājiem ir jāpiekļūst vairākām formām, lai pārvaldītu šādus informāciju:
<ul>
<li>Kategoriju pārvaldība</li>
<li>Preču pārvaldība</li>
<li>Kanāla preces īpašības</li>
<li>Preču klāsts</li>
<li>Katalogu pārvaldība</li>
<li>Komplekti</li>
<li>Cenas un atlaides</li>
</ul></td>
<td>Darbvieta <strong>Kategorijas un preču pārvaldība</strong> sniedz šādu funkcionalitāti:
<ul>
<li>Preču klāsta pārvaldība.</li>
<li>Preču klāsta cikla izsekošana.</li>
<li>Izlaisto preču pārvaldība.</li>
</ul>
Darbvieta <strong>Cenu un atlaižu pārvaldība</strong> sniedz šādu funkcionalitāti:
<ul>
<li>Cenu un atlaižu pārvaldība noteiktam kanālam un kategorijai.</li>
<li>Kategorijas cenu kārtulu pārvaldība.</li>
<li>Cenu un atlaižu prioritātes, kas jums ļauj piešķirt prioritātes cenu grupām un atlaidēm, lai varētu kontrolēt to lietošanas secību.</li>
<li>Piederības un kataloga atlaižu pārvaldība.</li>
</ul>
Darbvieta <strong>Katalogu pārvaldība</strong> sniedz šādu funkcionalitāti:
<ul>
<li>Aktīvo katalogu kopsavilkums.</li>
<li>Kataloga cikla izsekošana vienuviet.</li>
</ul></td>
<td><ul>
<li>Darbvietas uzlabo darbinieku efektivitāti un produktivitāti, darbiniekiem ļaujot centralizēti pārvaldīt savus uzdevumus un darbības, kas ir saistīti ar tirgū virzīšanas lomu.</li>
<li>Cenu un atlaižu prioritātes līdzeklis debitoriem sniedz lielāku kontroli pār to, kā tiek lietotas cenas un atlaides. Šis līdzeklis ļauj izmantot arī jaunus scenārijus, kur augstākas veikala cenas uzvar pār standarta cenām.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pārvaldiet mazumtirdzniecības kanālu izvietojumus un operācijas.</td>
<td>Lietotājam ir jāpiekļūst vairākām formām, lai veiktu šādus uzdevumus:
<ul>
<li>Izveidojiet un konfigurējiet jaunus kanālus un saistītos elementus.</li>
<li>Pārvaldiet ikdienas veikala darbības.</li>
<li>Apstrādājiet mazumtirdzniecības transakcijas ar Microsoft Dynamics AX, ģenerējiet mazumtirdzniecības izrakstus un atjauniniet Microsoft Dynamics AX krājumus un finanses.</li>
</ul>
 </td>
<td>Darbvieta <strong>Kanāla izvietošana</strong> ļauj veikt šādus uzdevumus:
<ul>
<li>Izveidojiet jaunus kanālus un saistītos elementus.</li>
<li>Sekojiet līdzi mazumtirdzniecības veikala konfigurācijas progresam.</li>
<li>Veiciet uzdevuma pabeigšanai nepieciešamās darbības vai sniedziet uzdevuma pabeigšanai nepieciešamo informāciju.</li>
<li>Sekojiet līdzi ierīču statusam, kā arī veikalos tieši pārbaudiet un lejupielādējiet Retail Modern POS (MPOS) programmas instalāciju.</li>
<li>Piekļūstiet visām saistītajām lapām.</li>
</ul>Darbvieta
<strong>Mazumtirdzniecības veikala pārvaldība</strong> jums ļauj veikt šādus uzdevumus:
<ul>
<li>Pārvaldiet darbiniekus un darbinieku pārdošanas punkta (point of sale — POS) atļaujas.</li>
<li>Sekojiet līdzi maiņu statusam attiecībā uz konkrētu veikalu vai veikalu grupu.</li>
<li>Veikalos tieši pārbaudiet un lejupielādējiet MPOS programmas instalāciju.</li>
<li>Drukājiet atskaites un piekļūstiet saistītajām lapām.</li>
</ul>Darbvieta 
<strong>Mazumtirdzniecības veikala finanses</strong> jums ļauj veikt šādus uzdevumus:
<ul>
<li>Izveidojiet, aprēķiniet un grāmatojiet izrakstus konkrētam kanālam.</li>
<li>Plānojiet pakešuzdevumus, lai atjauninātu krājumus, un aprēķiniet un grāmatojiet izrakstus.</li>
<li>Sekojiet līdzi atvērtajiem izrakstiem.</li>
<li>Sekojiet līdzi maiņu statusam attiecībā uz konkrētu veikalu vai veikalu grupu.</li>
<li>Drukājiet atskaites un ātri piekļūstiet visām saistītajām lapām.</li>
</ul></td>
<td>Darbvietas uzlabo darbinieku efektivitāti un produktivitāti, darbiniekiem ļaujot centralizēti pārvaldīt lielāko daļu savu uzdevumu un darbību, kas ir saistīti kanāla izvietošanu, veikala pārvaldību un finansēm.</td>
</tr>
<tr class="even">
<td>Pārvaldiet mazumtirdzniecības IT operācijas.</td>
<td>Lietotājam ir nepieciešams iekļūt vairākām formām.</td>
<td>Darbvieta <strong>Mazumtirdzniecības IT</strong> noteiktam kanālam Commerce Data Exchange vaicājumus ļauj veikt vienuviet, lai jūs varētu izpildīt šādus uzdevumus:
<ul>
<li>Lejupielādējiet sesijas.</li>
<li>Augšupielādējiet sesijas.</li>
<li>Sekojiet līdzi nesekmīgām sesijām, uzsāciet un palaidiet tās atkārtoti.</li>
<li>Skatiet vai palaidiet gaidāmos darbus.</li>
</ul></td>
<td>Darbvietas uzlabo darbinieku efektivitāti un produktivitāti, darbiniekiem ļaujot centralizēti pārvaldīt savus uzdevumus un darbības, kas ir saistīti ar mazumtirdzniecības IT operācijām.</td>
</tr>
<tr class="odd">
<td>Importējiet/eksportējiet datus, izmantojot datu elementus.</td>
<td>AX 2012 atbalsta standarta Microsoft Dynamics Retail Management System (RMS) migrāciju, izmantojot datu importēšanas/eksportēšanas struktūru.</td>
<td>Mazumtirdzniecības datu elementi ir paplašināti, lai atbalstītu visus ar mazumtirdzniecību saistītos vispārējos un atsauces datus. Ir uzlabots arī datu elementu atbalsts visā Dynamics AX risinājumā.</td>
<td>Datu elementi debitoriem ļauj veikt metadatu vadītu datu importēšanu un eksportēšanu. Turklāt OData elementi programmu Dynamics AX debitoriem ļauj integrēt trešās puses programmās.</td>
</tr>
<tr class="even">
<td>Veiciet viedo analīzi, izmantojot BI atskaites no Microsoft Dynamics AX un POS klienta.</td>
<td>Ir pieejamas vairāk nekā 25 iekšējai lietošanai paredzētās atskaites un 5 kanāla puses atskaites.</td>
<td>Ir pieejamas vairāk nekā 30 iekšējai lietošanai paredzētās atskaites un 10 kanāla puses atskaites.</td>
<td>Šīs atskaites debitoriem ļauj izmantot vairāk BI, lai prognozētu tendences, atklātu ieskatus un pastāvīgi strādātu ar maksimālu veiktspēju.</td>
</tr>
<tr class="odd">
<td>Analizējiet mazumtirdzniecības kanāla pārdošanas datus, izmantojot Power BI satura pakotni Mazumtirdzniecības kanāla veiktspējas pārraudzība.</td>
<td>Nav pieejams</td>
<td>Vietnē PowerBI.com atlasiet <strong>Iegūt datus</strong> un pēc tam atlasiet satura pakotni <strong>Dynamics AX — Mazumtirdzniecības kanāla veiktspēja</strong>. Ievadiet sava Dynamics AX galapunkta vietrādi URL, lai redzētu, kā jūsu dati tiek atspoguļoti šajā informācijas panelī.</td>
<td>Ar trīs vai četriem klikšķiem organizācijas var izvietot Power BI informācijas paneli, kas ietver svarīgus finanšu datus. Saturu var personalizēt pēc organizācijas. Turklāt Power BI informācijas paneļa elementus lietotāji var iegult savās personalizētajās darbvietās programmā Dynamics AX, lai uzreiz redzētu analītisko informāciju.</td>
</tr>
<tr class="even">
<td>Konfigurējiet patērētāju atļaujas.</td>
<td>Nav pieejams</td>
<td>Debitori var izvēlēties, vai POS operācijas var būt pieejamas patērētājiem. Mazumtirdzniecības serveris izmanto atļaujas attiecībā uz lietojumprogrammu programmēšanas interfeisu (API) izsaukumiem.</td>
<td>Tas sniedz iespēju konfigurēt patēriņa līmeņa atļaujas.</td>
</tr>
<tr class="odd">
<td>Pārvaldiet un pārbaudiet elementu konfigurācijas.</td>
<td>Nav pieejams</td>
<td>Līdzeklis Konfigurācijas pārvaldnieks un validators sniedz šādu funkcionalitāti:
<ul>
<li>Lielapjoma konfigurācijas datu augšupielāde</li>
<li>Biznesa elementa validēšana</li>
</ul></td>
<td>Tā sniedz iespēju jau iepriekš sagatavot konfigurāciju un pārbaudīt šīs konfigurācijas statusu un pabeigtību attiecībā uz dažādiem konfigurācijas elementiem.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Retail aparatūras stacija

|                                                                                                  |                                                                         |                                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                                             | **Dynamics AX 2012**                                                    | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                           | **Kāpēc tas ir svarīgi?**                                                                                                        |
| Iespējojiet POS ierīces, lai veidotu savienojumu ar perifērijas ierīcēm, piemēram, printeriem, kases aparātiem vai maksājumu ierīcēm. | Lai norādītu izmantojamās ierīces, tiek lietots MPOS aparatūras profils. | Pievienotas aparatūras profils atbalsta daudzveidīgāku aparatūru no vienas stacijas uz nākamo. Jauns Aparatūras stacijas profils atbalsta unikālu termināļa ID katrai aparatūras stacijai, kad tiek apstrādātas elektronisko līdzekļu pārskaitījumu (EFT) transakcijas. EFT atbalsts ir sapludināts ar aparatūras staciju, lai mazinātu MPOS līdzdalību EFT maksājumu apstrādē. | Šādi implementācijām tiek nodrošināta lielāka elastība. Tas arī sniedz uzlabotu drošību un samazina pakļaušanu kredītkartes datiem. |

### <a name="retail-server-and-data-management"></a>Mazumtirdzniecības servera un datu pārvaldība

Mazumtirdzniecības servera un datu pārvaldība patērētājiem un uzņēmumiem ļauj radīt visaptverošu iepirkšanās pieredzi visos kanālos — gan tiešsaistes, gan veikala, gan zvanu centra kanālos.

<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Izveidojiet savienojumu ar Commerce Runtime (CRT) datu bāzi, kurā glabājas attiecīgā kanāla biznesa dati, izmantojot CRT pakalpojumus.</td>
<td>Tiek atbalstīta versija OData V3.</td>
<td>Tiek atbalstīta versija OData V4.</td>
<td>Tas palīdz debitoram vienmēr būt informētam par aktuālajiem OData standartiem. Turklāt tas izveido robustu un visaptverošu kanālu pieredzi, integrējot pārdošanu veikala, mobilajos un tiešsaistes kanālos.</td>
</tr>
<tr class="odd">
<td>Atbalstiet mazumtirdzniecības pakalpojumus kā viesojamu pakalpojumu kopu.</td>
<td>Mazumtirdzniecības serverī netiek atbalstīts e-komercijas API.</td>
<td>E-komercijas API tagad ir pieejams, izmantojot mazumtirdzniecības serveri, lai atbalstītu tiešsaistes scenārijus.</td>
<td>Tas nodrošina viesotus un mērogojamus e-komercijas pakalpojumus, ko var izmantot ar trešās puses tiešsaistes veikaliem.</td>
</tr>
<tr class="even">
<td>Pārvietojiet datus starp Microsoft Dynamics AX iekšējo biroju un kanāliem, izmantojot Commerce Data Exchange.</td>
<td>Commerce Data Exchange ir sistēma, kas pārsūta datus starp Microsoft Dynamics AX un mazumtirdzniecības kanāliem, piemēram, tiešsaistes veikaliem vai fiziskajiem veikaliem. Plašāku informāciju skatiet tēmā <a href="https://technet.microsoft.com/en-us/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Pastāv funkcionāla paritāte ar Microsoft Dynamics AX 2012 CU8. Taču ņemiet vērā šādu informāciju:
<ul>
<li>Sistēma Commerce Data Exchange ir pārstrādāta lietošanai mākonī.</li>
<li>Async pakalpojums izmanto tiešu datu bāzes piekļuvi uz kanāla datu bāzi.</li>
<li>Commerce Data Exchange: Real-Time Service tiek viesots kā Microsoft Dynamics AX pielāgots pakalpojums.</li>
<li>MPOS pārvalda sinhronizēšanu starp bezsaistes datu bāzēm un mazumtirdzniecības serveri.</li>
</ul></td>
<td>Sistēma Commerce Data Exchange ir pārstrādāta lietošanai mākoņa platformā. Tā turpina pārvaldīt datu pārsūtīšanu starp Microsoft Dynamics AX un mazumtirdzniecības kanāliem, piemēram, tiešsaistes veikaliem vai fiziskajiem veikaliem.</td>
</tr>
<tr class="odd">
<td>Atbalstiet Plug and Play, daļēji integrētu starpkanālu maksājumu apstrādi, izmantojot maksājumu SDK.</td>
<td>AX 2012 sniedz šādu funkcionalitāti:
<ul>
<li>Atbalsts visiem kanāliem: POS, e-komercija un zvanu centrs.</li>
<li>Atbalsts gan klātesošām, gan neesošām kartēm.</li>
<li>Lapa maksājuma pieņemšanai.</li>
<li>Perifērais atbalsts attiecībā uz LS5300 un MX925 kā parauga kodu spraudnī Retail SDK.</li>
</ul></td>
<td>Dynamics AX pašreizējā versija atbalsta visus esošos Microsoft Dynamics AX for Retail 2012 kredītkaršu/debetkaršu līdzekļus un četrus jaunus uzlabojumus.</td>
<td>Tā debitoram ļauj apstrādāt kredītkartes/debetkartes transakcijas maksājumiem.</td>
</tr>
<tr class="even">
<td>Aktivizējiet ierīces, izmantojot Microsoft kontu (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Nav pieejams</td>
<td>Tiek nodrošināta šāda funkcionalitāte:
<ul>
<li>Uzlabota drošība, ko sniedz Azure AD balstīta aktivizēšana mākonim.</li>
<li>Uzlabota drošība marķieru pārvaldībai.</li>
<li>Uzlabota uzticamība, problēmu novēršana un kļūdu ziņošana aktivizēšanas laikā</li>
<li>Vienkāršoti ar aktivizēšanu saistītie IT administrēšanas uzdevumi.</li>
<li>Pārskatīts draudu modelis un izlabotas drošības problēmas.</li>
</ul></td>
<td>Tas nodrošina šādas priekšrocības:
<ul>
<li>Drošība ir uzlabota, izmantojot Azure AD un ierīces marķieri/ID (RS izsaukumi, kas izmanto marķieri, lietotājam raksturīga programmas krātuve).</li>
<li>Tas aptur neatļautu MPOS attālo lietošanu (ierīces lietojamības bloķēšanu).</li>
<li>Tas izseko MPOS ierīces PCI atbilstības nolūkos.</li>
<li>Tas kartē fiziskās ierīces ar biznesa elementu (reģistru), izmantojot ierīces marķieri.</li>
<li>Tas inicializē iestatījumus gludai MPOS funkcionalitātei (numuru sērijas un aparatūras profili) kā MPOS pirmo saskares punktu.</li>
<li>Tas ziņo informāciju par ierīci no galvenās pārvaldes.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pārvaldiet bagātinātas multivides saturu autorēšanai un pasniegšanai caur līdzekli Multivides galerija.</td>
<td>Nav pieejams</td>
<td><ul>
<li>Atbalstiet attēlu augšupielādi, kā arī skatīšanu, pārvaldīšanu un dzēšanu no līdzekļa Multivides galerija gan ārēji viesotiem, gan mazumtirdzniecības viesotiem attēliem.</li>
<li>Atbalstiet attēlu augšupielādi un skatīšanu no elementu lapām (<strong>Preces</strong>, <strong>Katalogi</strong> un citām), piesaistot attēlu no galerijas un augšupielādējot kādu attēlu no darbvirsmas.</li>
<li>Optimizējiet attēlus sīktēliem, pielāgotam izmēram un oriģinālam.</li>
<li>Izpildiet entītiju lielapjoma saistīšanu, lietojot veidni un fona darbus lielapjoma saistīšanai.</li>
<li>Integrācija ar Microsoft Excel pārraksta atribūtu grupu nosaukumdošanas metožu ierobežojumu un iepriekš definētos ceļus.</li>
<li>Atbalstiet bezsaistes attēlus un drošus attēlus personu identificējošas informācijas (PII) saturam, piemēram, mazumtirdzniecības viesotiem darbinieku un debitoru attēliem.</li>
</ul></td>
<td><ul>
<li>Tas ir vērsts uz galvenajiem punktiem ap ārēji viesotiem attēliem, jums likvidējot nepieciešamību pārvietoties šurpu turpu, tā vietā nepieciešamo varat izdarīt vienuviet.</li>
<li>Tas nodrošina jaudīgu satura pārvaldību, izmantojot līdzekli Multivides galerija augšupielādētiem un ārēji viesotiem attēliem, kā arī sniedz filtrēšanu, lai jums palīdzētu atrast attēlus.</li>
<li>Tas jums ļauj ērti izveidot lielapjoma saistības starp ārēji viesotiem attēliem un elementiem, piemēram, precēm un katalogiem.</li>
<li>Tas atbalsta mazumtirdzniecības viesotu krātuvi attēliem un integrāciju ar Excel vienkāršiem atjauninājumiem.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Bagātīga klientu pieredze

Mazumtirdzniecība sniedz pilnīgu mobilo pieredzi jebkurā vietā un jebkurā laikā, un ar jebkuru ierīci. Šī funkcionalitāte sniedz uzlabotu iepirkšanos un veikala pieredzi visos kanālos.

<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Meklējiet, pārlūkojiet, uzmeklējiet vai skenējiet preces, pievienojiet preces iepirkumu grozam, pieņemiet maksājumu un veiciet izsniegšanu, izmantojot intuitīvu, skāriendraudzīgu, bagātīgu un visaptverošu lietotāja pieredzi ar MPOS.</td>
<td>AX 2012 nodrošina šādus līdzekļus:
<ul>
<li>Veiciet pārdošanu, atgriešanu un anulēšanu.</li>
<li>Veidojiet, modificējiet un saņemiet debitoru pasūtījumus.</li>
<li>Veiciet maiņas un naudas kastes operācijas.</li>
<li>Izdodiet un saņemiet pasūtījumus un veiciet krājumu uzskaiti.</li>
<li>Skatiet veikala iekšējās atskaites.</li>
</ul></td>
<td>Tiek nodrošināta funkcionālā paritāte ar AX 2012 MPOS. Tas ietver šādu funkcionalitāti:
<ul>
<li>Debitoru uzmeklēšana dažādos veikalos/kanālos.</li>
<li>Iespēja veidot debitoru pasūtījumu, nepiekļūstot reāllaika pakalpojumam.</li>
<li>Uzlabotas ierīču aktivizēšanas darbplūsmas, statusa un kļūdu ziņojumi.</li>
<li>Paplašināmības uzlabojumi, piemēram, trigeri pirms grāmatošanas un aktivitāšu atbalsts, lai uzlabotu pielāgošanu.</li>
</ul></td>
<td>Pārdošanas darbinieki var apstrādāt pārdošanas transakcijas un debitoru pasūtījumus, un veikt ikdienas operācijas un krājumu vadību, jebkurā veikala vietā izmantojot mobilās ierīces.</td>
</tr>
<tr class="odd">
<td>Palaidiet POS kā tīmekļa programmu, izmantojot Mākoņa POS.</td>
<td>Nav pieejams</td>
<td>Tiek nodrošināta funkcionālā paritāte ar MPOS. Tas ietver šādu funkcionalitāti:
<ul>
<li>Ierīces aktivizēšana, izmantojot AAD</li>
<li>Interaktīvs izkārtojuma dizains</li>
<li>Atbalsts pārlūkiem Edge, Internet Explorer un Chrome.</li>
</ul></td>
<td>Tas nodrošina tīmekļa programmu POS, kuras funkcionalitāte ir savietojama ar MPOS un kuru var izmantot dažādās platformās un pārlūkprogrammās bez izvietošanas maksas.</td>
</tr>
<tr class="even">
<td>Integrējiet ar satura pārvaldības sistēmām, lai izveidotu visaptverošu kanālu e-komercijas vietni.</td>
<td>Tiek atbalstīts Microsoft SharePoint un trešās puses veikali.</td>
<td>Tiek nodrošināta e-komercijas platforma, kas atbalsta trešo pušu veikalus. Šī platforma ietver šādus līdzekļus:
<ul>
<li>Bagātīgs patērētāju API.</li>
<li>Autentifikācijas integrācija ar jebkuriem trešās puses atvērtā ID nodrošinātājiem.</li>
<li>Maksājumu integrācija.</li>
</ul></td>
<td>Tagad debitori var elastīgi izmantot sev vēlamo satura pārvaldības sistēmu.</td>
</tr>
<tr class="odd">
<td>Vērsieties pie debitoriem, izmantojot pasta pasūtījumu katalogus, un racionalizējiet operācijas, izmantojot ātru pasūtījumu izveidi, asistēto pārdošanu un izpildi, izmantojot zvanu centru.</td>
<td><ul>
<li>Zvanu centra kanāls</li>
<li>Pasta pasūtījumu katalogi</li>
<li>Ātra pasūtījuma izveide un asistētā pārdošana</li>
<li>Uzlabota pasūtījumu izpilde</li>
<li>Klientu apkalpošana</li>
<li>Integrēta cenu noteikšana un akcijas/atlaides</li>
</ul></td>
<td>Ir pieejama līdzekļu paritāte ar AX 2012 zvanu centra risinājumu, izņemot cenu ignorēšanu.</td>
<td>Zvanu centri ir mazumtirdzniecības kanāla veids, kas darbiniekiem pa tālruni ļauj pieņemt pasūtījumus no debitoriem un izveidot pārdošanas pasūtījumus.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Komercijas rekvizīti

Uz mazumtirdzniecību un komerciju koncentrēta konfigurēšanas opcija palīdz racionalizēt mazumtirdzniecībai raksturīgos izvietojumus.

|                                               |                                                                                                             |                                                                                                                                                                               |                                                                                                                                                         |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                          | **Dynamics AX 2012**                                                                                        | **Dynamics AX 7.0**                                                                                                                                                           | **Kāpēc tas ir svarīgi?**                                                                                                                              |
| Lietojiet informācijas paneli Komercijas rekvizīti.        | Ir pieejama apgabala lapa ar saitēm uz izvēlnes vienumiem.                                                         | Informācijas panelis Komercijas rekvizīti sniedz saites uz bieži izmantotajiem uzdevumiem, tostarp saites uz darbvietām, Power BI tīmekļa vadību, izlasi, nesenajām lapām un pašreizējiem darba elementiem. | Uzlabotais informācijas panelis darbiniekiem sniedz lielākas iespējas, padarot viņu darbu efektīvāku un nodrošinot elastīgu sākumpunktu jebkuram mazumtirdzniecībai raksturīgam uzdevumam.             |
| Lietojiet datu elementus, lai piekļūtu konta izmaiņām.  | Konta izmaiņas tiek eksportētas uz mapi failu sistēmā.                                                | Konta izmaiņām var piekļūt, izmantojot datu elementus.                                                                                                                         | Šis līdzeklis sniedz lielāku elastību, kad datus pārvietojat starp dažādām sistēmām. Turklāt šo līdzekli var uzlabot ar OData programmām. |
| Lietojiet Mākoņa POS un MPOS.                       | Standarta komplektācijā tiek atbalstīts tikai Uzņēmuma POS (Enterprise POS — EPOS).                                                     | MPOS un Mākoņa POS aizstāj EPOS klientu. Komercijas rekvizītiem pēc noklusējuma ir pievienots arī e-komercijas kanāls.                                                     | Šis līdzeklis sniedz lielāku standarta komplektācijas kanālu atbalstu ar ātri izvietojamiem pārdošanas punkta klientiem.                                                  |
| Ieviesiet un uzturiet divu līmeņu arhitektūru. | Datu importēšanas/eksportēšanas struktūra sniedz iespēju pārvietot datus starp AX 2012 un trešo pušu sistēmām. | Ir izveidoti datu elementi, lai uzlabotu divu līmeņu arhitektūras struktūru.                                                                                                           | Datu elementi un OData programmas sniedz nošķiršanas līmeni, lai divu līmeņu scenāriju ieviešana un uzturēšana būtu vienkāršāka.                          |
| Vienkāršojiet formas.                               | Lai vienkāršotu UI,ir nepieciešams pielāgots kods.                                                                 | Formu un izvēlņu paplašinājumi nodrošina standartizētā UI vienkāršošanu.                                                                                                              | Šis līdzeklis nodrošina ātrāku un vienkāršāku veidu, kā smalki pielāgot formas, pamatojoties uz mazumtirgotāja vajadzībām.                                                             |

### <a name="pos-task-recorder"></a>POS uzdevumu ierakstītājs

<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Izveidojiet un kopīgojiet uzdevumu ceļvežus un dokumentus, kas paredzēti Modern POS.</td>
<td>Nav pieejams</td>
<td>MPOS uzdevumu ierakstītājs atbalsta šādus līdzekļus:
<ul>
<li>Izveidojiet uzdevumu ierakstus dažādiem uzdevumiem, kas tiek veikti ar MPOS.</li>
<li>Ģenerējiet dokumentu, kas ietver darbības un ekrānuzņēmumus, un saistiet to ar zaru biznesa procesa modelī.</li>
</ul></td>
<td>Partneri un neatkarīgi programmatūras piegādātāji (Independent Software Vendor — ISV) var pielāgot MPOS un sniegt atbalsta dokumentus, lai apmācītu savus lietotājus.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Paplašināmība

<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Atbalstiet paplašināmus un ērti izvietojamus mazumtirdzniecības komponentus HQ, zvanu centrā, e-komercijā un POS.</td>
<td>Komponentus var paplašināt, izmantojot Retail SDK. Netiek atbalstītas nekādas iepakošanas un izvietošanas iespējas.</td>
<td>Paplašināmības āķi ir uzlaboti izmantošanai dažādos komponentos, lai labāk atbalstītu koda izolēšanu un apkalpojamību. Lūk, daži no iekļautajiem līdzekļiem:
<ul>
<li>Darbplūsma, aktivitāte un operācija.</li>
<li>Trigeri pirms un pēc darbībām, kas jums ļauj ērti paplašināt darbplūsmu.</li>
<li>Programmu un operāciju trigeri.</li>
</ul>
Turklāt ir pieejama struktūra, kas jums ļauj veidot un iepakot šos komponentus, izmantojot MSBuild, un pēc tam efektīvi izvietot savus pielāgojumus, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</td>
<td>Mazumtirgotājiem ir ļoti specifiskas prasības, kas ir atkarīgas no operācijas vertikālajām un ģeogrāfiskajām īpašībām. Sniedzot ērti paplašināmu platformu, mēs iespējojam lietojumu dažādās vertikālēs un tirgos. Tā kā arī mazumtirdzniecībai ir ļoti izplatīta arhitektūra, spēja efektīvi izvietot ievērojami uzlabo produktivitāti.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Cikla pārvaldība

Lifecycle Services (LCS) sniedz pakalpojumu kopu, ko debitori un partneri var izmantot, lai pārvaldītu sistēmas ciklu no reģistrēšanās līdz ikdienas operācijām.

<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Pārvaldiet programmu, izmantojot mākoņa izvietošanas pakalpojumus.</td>
<td>Nav pieejams</td>
<td>Mākonī var izvietot šādas topoloģijas:
<ul>
<li>Mazumtirdzniecības viena lodziņa izmēģinājuma topoloģija.</li>
<li>Mazumtirdzniecības daudzlodziņu augstas pieejamības topoloģija.</li>
<li>Izstrādātāja topoloģija ar Retail SDK.</li>
</ul>
Pastāv uzlabota “zema pieskāriena” klienta komponenta instalācija, izmantojot pašapkalpošanās instalāciju:
<ul>
<li>Retail Modern POS.</li>
<li>Retail Hardware Station.</li>
<li>Atbalsts pielāgotu pakotņu augšupielādei un izplatīšanai, izmantojot pašapkalpošanās instalāciju.</li>
</ul></td>
<td>Mākoņa izvietošanas pakalpojumi sniedz šādas priekšrocības:
<ul>
<li>Retail HQ komponentiem ievērojami mazināts izvietošanas darbs un sarežģītība.</li>
<li>Vietējā izvietošana Microsoft Azure publiskajā mākonī.</li>
<li>Uzlabota veikala iekšējo komponentu pašapkalpošanās instalācija, lai konfigurēšanu padarītu vienkāršāku un intuitīvāku</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pārraugiet sistēmas darbspēju un atrodiet kļūdas un problēmas.</td>
<td>Šai funkcionalitātei ir nepieciešama pakotne <a href="http://www.microsoft.com/en-us/download/details.aspx?id=42636">System Center 2012 Management Pack for Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</td>
<td>Pārraudzība un diagnostika mazumtirdzniecības komponentiem tagad ir pieejama, izmantojot LCS informācijas paneli <strong>Darbības ieskati</strong>.</td>
<td>Informācijas panelis <strong>Darbības ieskati</strong> ir mākoņa pārraudzības portāls, kas aizstāj nepieciešamību instalēt System Center Operations Manager (SCOM) infrastruktūru.</td>
</tr>
<tr class="even">
<td>Izveidojiet, konfigurējiet, lejupielādējiet un instalējiet Retail aparatūras staciju un ierīces, izmantojot pašapkalpošanos.</td>
<td>Izmantojot instalācijas pakotāju un uzņēmuma portālu, lietotājs var izpildīt automatizētu instalēšanu un konfigurēšanu visiem komponentiem, kas ir nepieciešami konkrētā datorā, pamatojoties uz definēto topoloģiju.</td>
<td>Tā kā ir tikai divas instalācijas pakotnes, viena — MPOS klientam un otra — Retail aparatūras stacijas komponentam, tad pašapkalpošanās ir samazinājusi šo klienta komponentu instalēšanai katrā līmenī nepieciešamā darba apjomu.</td>
<td>Pašapkalpošanās mērķis ir minimizēt prasības un lietotājam vienkāršot instalēšanas izpildi.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Pārdošana
<table>






<tbody>
<tr class="odd">
<td><strong>Ko iespējams izdarīt?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Kāpēc tas ir svarīgi?</strong></td>
</tr>
<tr class="even">
<td>Gūstiet ātru pārskatu par piegādes alternatīvām, kad debitoriem apsolāt pasūtījumus.</td>
<td>Ja pastāv preču pieejamības ierobežojumi un debitora pieprasīto piegādes datumu attiecībā uz vienu vai vairākām precēm pasūtījumā nevar izpildīt, tad pasūtījumu solīšanas uzdevums kļūst par problēmu. Lai atrastu alternatīvas, kas var kompensēt pieejamības un piegādes laika jautājumus, un tādējādi varētu ievērot debitora pieprasīto datumu, vai lai debitoriem piedāvātu piegādes risinājumu, ko viņi var pieņemt un kam var uzticēties, pasūtījumu apstrādātājam, iespējams, ir jāatver vairākas formas, un katra no tām piedāvā tikai nepieciešamās informācijas apakškopu. Precīzāk — vienā formā tiek rādīts rīcībā esošais daudzums dažādās vietās, citā formā tiek rādīts rīcībā esošais daudzums starpuzņēmumu iestatījumā, bet trešajā formā lietotājam tiek ļauts aprēķināt agrāko pieejamo datumu vienlaicīgi tikai vienai vietai/variantam, un ceturtajā formā tiek rādīti piedāvājuma pasūtījumi. Tāpēc lietotājiem nav pārliecības, ka viņi ir apskatījuši visas saistītās iespējas, nevis vienkārši izvēlējušies tūlītēju, bet ne optimālu risinājumu. Lietotājiem arī nav sajūtas, ka viņu darbs notiek efektīvi, jo pasūtījuma apsolīšanas darbplūsmas laikā notiek daudzi traucējumi, viņiem atverot un aizverot vairākas lapas un kombinējot ieskatus un opcijas.</td>
<td>Pamatojoties uz pastāvošajiem algoritmiem attiecībā uz piegādes datumu aprēķināšanu, lapā <strong>Piegādes alternatīvas </strong>tiek sniegta jauna lietotāja pieredze pasūtījumu solīšanai:
<ul>
<li>Tā apvieno svarīgo informāciju no vairākām formām vienuviet.</li>
<li>Tā nodrošina gatavas alternatīvās piegādes pakotnes, piemēram, kombinējot vietu, noliktavu, variantu un transporta režīmu, pamatojoties uz ātrākās piegādes (agrākā pieejamā datuma) kritēriju, ko var izvēlēties lietotājs.</li>
<li>Tā lietotājam ļauj atlasīt opcijas no simulācijas interfeisa un pārsūtīt tās uz pārdošanas pasūtījuma rindu.</li>
</ul></td>
<td>Uzņēmumiem, kas vēlas nodrošināt augstu klientu apkalpošanas līmeni, vienlaikus veltot pūles krājumu optimizēšanas stratēģijai, ir jāspēj apsolīt uzticamus un konkurētspējīgus pasūtījumus. Galu galā, viņu klientu pašu uzņēmumiem ir nepieciešams, lai preces būtu pieejamas laikā. Uzdevuma lapa <strong>Piegādes alternatīvas</strong> pasūtījuma solīšanas uzdevumu padara ātrāku, vienkāršāku un sistemātiskāku, identificējot un iesakot vislabākos alternatīvos pasūtījuma piegādes datumus vienā interaktīvā vietā.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Pakalpojumu pārvaldība
Nav pievienoti jauni līdzekļi.

## <a name="transportation-management"></a>Transportēšanas pārvaldība
Nav pievienoti jauni līdzekļi.

## <a name="travel-and-expense"></a>Ceļošana un izdevumi
Nav pievienoti jauni līdzekļi.

## <a name="warehouse-management"></a>Noliktavas pārvaldība
|                                                                       |                                                                                                                                                                                                              |                                                                                                                                                               |                                                                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ko iespējams izdarīt?**                                                  | **Dynamics AX 2012**                                                                                                                                                                                         | **Dynamics AX 7.0**                                                                                                                                           | **Kāpēc tas ir svarīgi?**                                                                                                                                                           |
| Lejupielādējiet, instalējiet un konfigurējiet noliktavas mobilo ierīču portālu. | Šo portālu varat lejupielādēt, instalēt un konfigurēt Microsoft Dynamics AX instalēšanas procesa laikā, izmantojot standarta iestatījumu. Tas ir izstrādāts automātiskai lokālajai izvietošanai un konfigurēšanai. | Varat lejupielādēt savrupu instalētāju, izmantojot izvēlnes vienumu līdzeklī Noliktavas vadība. Tas ir izstrādāts automātiskai lokālajai izvietošanai un konfigurēšanai. | Kad iestatāt mobilās ierīces funkcionalitāti, noliktavas mobilo ierīču portāls ir jāinstalē un jākonfigurē lokāli, un ir jāiegūst savienojums ar Dynamics AX mākonī. |



<a name="see-also"></a>Skatiet arī
--------

[Jaunumi un izmaiņas](whats-new-changed.md)

[Pieejami jauni uzdevumu ceļveži (2016. gada februāris)](new-task-guides-available-february-2016.md)




