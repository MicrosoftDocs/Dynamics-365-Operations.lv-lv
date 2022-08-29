---
title: Veiktspējas problēmu novēršana ER konfigurācijās
description: Šajā rakstā skaidrots, kā atrast un labot veiktspējas problēmas Elektronisko pārskatu (ER) konfigurācijās.
author: kfend
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
ms.openlocfilehash: 283577e70d4e5c4314776f7420857cf8e25e735f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278742"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>Veiktspējas problēmu novēršana ER konfigurācijās

Šajā rakstā skaidrots, kā atrast un atrisināt veiktspējas problēmas [Elektronisko pārskatu](general-electronic-reporting.md) (ER) konfigurācijās [...](general-electronic-reporting.md#Configuration).

Parasti veiktspējas izpēte sastāv no vairākām darbībām.

1. [Apkopot](#collecting-data) datus.
2. Analizēt apkopotos datus.
3. Pamatojoties uz analīzes rezultātiem, izmantojiet ER konfigurācijas, lai [veiktu izmaiņas](#making-changes), vai arī izlemtu apkopot vairāk datu.

## <a name="troubleshooting"></a>Problēmu novēršana

### <a name="analyze-execution-time"></a>Analizēt izpildes laiku

Izpildes laiks var būt atkarīgs no neprognozējamiem faktoriem, piemēram, citiem uzdevumiem, kas darbojas tajā pašā vidē, un kešdarbes, kas izmanto datus, kad tie tiek izsaukti pirmo reizi. Tādēļ izpilde un mērījums ir jāatkārto vairākas reizes.

Dažreiz veiktspējas problēmas nav saistītas ar ER formāta konfigurāciju, kas tiek izmantota pārskatiem. Tā vietā tās izraisa X++ kods, kas tiek izmantots, lai atvērtu šī ER formāta konfigurāciju.

1. Vai nu [darbību centrā](#infolog-time) vai [notikumu žurnālā](#event-log-time) skatiet pārskata izpildes laiku.
2. Salīdziniet pārskata izpildes laiku ar kopējo izpildes laiku scenārijā.
3. Ja pārskata izpildes laiks ir daudz mazāks nekā kopējais izpildes laiks, apsveriet datu apjomu, ko pārskats apstrādā:

    - Ja pārskats apstrādā mazu datu apjomu, problēma var ietvert konfigurācijas ielādes laiku.
    - Ja pārskats apstrādā lielu datu apjomu, problēma var ietvert koda X++ pirmapstrādi. Izmantojiet [Trace parsētāju](#analyze-trace-parser-trace), lai analizētu šo gadījumu.

    Pārējos gadījumos skatiet nākamās sadaļas.

4. Veiciet vairākus testus, kas ietver dažādus datu apjomus, lai noteiktu, kā izpildes laiks ir atkarīgs no datu apjoma.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Trace parsētāja darbību izsekošanas analīze

Sagatavojiet nelielu piemēru vai savāciet vairākas izsekotās darbības no pārskata ģenerēšanas nejaušām daļām.

Pēc tam [Trace parser](#trace-parser) veiciet standarta apakšpuses analīzi un atbildiet uz šādiem jautājumiem:

- Kādas ir galvenās metodes attiecībā uz laika patēriņu?
- Kādu daļu no kopējā laika šīs metodes izmanto?

Atbildiet uz tiem pašiem jautājumiem arī par vaicājumiem.

Ja redzat, ka metodes prefiksā ir “ER”, pārejiet uz nākamo sadaļu.

Ja redzat, ka metodes vai vaicājumi tiek veidoti programmas komplektā, apsveriet vispārēju optimizāciju (piemēram, izveidojot indeksus).

Analizējiet izsaukumu skaitu. Ja to skaits ir ievērojami augstāks nekā paredzēts, apsveriet atbilstošo konfigurācijas mezglu kešdarbi.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Datu bāzes izsaukumu analīze

Sagatavojiet piemēru, kas satur nelielu datu apjomu, lai varētu apkopot [ER izsekotās darbības](#electronic-reporting-traces).

Pēc tam atveriet izsekotās darbības ER modeļa kartēšanas noformētājā un apskatiet lapas apakšpusi. Atbildiet uz šādiem jautājumiem:

- Vai tiek veikta vaicājumu dublēšana? Ja tā ir, apsveriet vienu no šiem labojumiem:

    - [Izmantojiet kešdarbi](#use-caching), ja domājat, ka vienā pamatierakstā ir vairāki izsaukumi.
    - [Izmantojiet kešdarbes parametru aprēķinātu lauku](#cached-parameterized), ja domājat, ka dažādos ierakstos ir izsaukumi uz vienu un to pašu ierakstu.
    - [Izmantojiet **JOIN** datu avotu](#use-join-datasource), ja jums ir jālasa ļoti daudz dažādu datu bāzu ierakstu.

- Vai vaicājumu un ienesto ierakstu skaits atbilst vispārējam datu apjomam? Piemēram, ja dokumentam ir 10 rindas, vai statistika rāda, ka pārskats izgūs 10 rindas vai 1000 rindas? Ja jums ir liels skaits ienesto ierakstu, apsveriet vienu no šiem labojumiem:

    - [Lai pusē **apstrādātu** datus, **lietojiet funkciju** FILTER, nevis](#filter) funkciju WHERE Microsoft SQL Server.
    - Izmantojiet kešdarbi, lai izvairītos no to pašu datu ieneses.
    - [Izmantojiet apkopoto datu funkcijas](#collected-data), lai izvairītos no to pašu ienesto datu apkopošanas.

### <a name="analyze-perfview-traces"></a>PerfView darbību izsekošanas analīze

[PerfView](#perfview) ir pieredzējušu izstrādātāju rīks. Papildinformāciju par tālāk minētajām darbībām skatiet sadaļā [Pulksteņa laika izpētes pamati](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Apkopojiet izsekotās darbības, izmantojot pavediena laiku.
2. Ietveriet tikai stekus, kas izmanto **runUnattended**, lai filtrētu tikai pavedienu, kam ir konfigurācijas izpilde. (Pievienojiet **runUnattended** pie **IncPats** ievades lodziņa.)
3. Saīsiniet visu CPU, tīklu un bloķēto laiku.
4. Ielādējiet [ER priekšiestatījumus rīkam PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).
5. Atlasiet **ER** \> **Citi priekšiestatījumi**.
6. Apskatiet nosaukumus:

    - Iespējams, redzēsit platformas kodu, kas aizņem visvairāk laika.
    - Varat veikt dubultskārienu (vai dubultklikšķi) un doties uz **izsaukumiem**.

        Ja atradīsit klases ar prefiksu “ERExpression”, un ja tās ir funkcijas, kas saistītas ar formulām, tad funkciju nosaukumu iespējams atrast, balstoties uz klases nosaukuma, un varat apskatīt ER repositoriju, lai skatītu atribūtus.

### <a name="fixes"></a>Labojumi

- Ja redzams, ka vaicājumi patērē lielāko daļu no CPU laika, mēģiniet samazināt vaicājumu apjomu:

    - [Pārskatiet ER izsekotās darbības](#analyze-database-calls), meklējot vaicājumu dublējumus.
    - Apskatiet, cik ierakstu tiek ienesti, un novērtējiet, cik daudz datu teorētiski būtu jāienes.

- Ja redzat, ka lielāko daļu no CPU laika patērē funkcijas, mēģiniet atrast vietu konfigurācijā, kas patērē visvairāk resursu.
- Ja redzat, ka lielāko daļu no CPU laika patērē datu apkopošanas funkcijas, apsveriet iespēju tās aizstāt ar *SQL grupēšanu pēc* modeļa kartēšanas puses.

### <a name="collecting-data"></a><a name="collecting-data"></a>Datu apkopošana

Atkarībā no vides ir vairāki veidi, kā apkopot pieejamos datus:

- Iegūt kopējo palaišanas laiku no:

    - Darbību centra
    - Notikumu žurnāla

- Izpildes profilēšana izmantojot:

    - ER rīkus
    - Trace parsētāju
    - PerfView

#### <a name="collecting-data-in-a-production-environment"></a>Datu apkopošana ražošanas vidē

Dažreiz problēmas var pavairot tikai ražošanas vidē. Datus var apkopot, šādos veidos:

- Izmantojot [Trace parsētāja](../perf-test/trace-trace-tutorial.md) darbību izsekošanu
- Izmantojot [ER izpildes](trace-execution-er-troubleshoot-perf.md) darbību izsekošanu
- Izmantojot kopējo izpildes laiku

#### <a name="collecting-data-in-a-development-environment"></a>Datu apkopošana izstrādes vidē

Papildus tiem rīkiem, kurus var izmantot ražošanas vidē, ir vairāki rīki, ko var izmantot izstrādes vidē:

- Notikumu žurnāls (Microsoft-Dynamics-ElectronicReporting). Šis žurnāls var sniegt kopējo izpildes laiku.
- Vispārīgie .NET rīki, piemēram, PerfView.

Turklāt izstrādes vide sniedz lielāku elastību attiecībā uz eksperimentiem. Piemēram, varat izslēgt daļu pārskatu, lai redzētu, kā tiek ietekmēts izpildes laiks.

### <a name="tools"></a><a name="tools"></a>Rīki

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Izpildes laiks darbību centrā

ER var parādīt konfigurācijas izpildes laiku darbību centrā. Šī opcija darbojas tikai noteiktam lietotājam un noteiktam uzņēmumam, kā arī tikai interaktīvām sesijām. Lai padarītu šo līdzekli pieejamu, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Rādīt failu ģenerēšanas laiku** uz **Jā**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Izpildes laiks notikumu žurnālā

1. Atvērt Windows Notikumu skatītāju.
2. Sadaļā **Programmu un pakalpojumu žurnāli** atveriet **Microsoft-Dynamics-ElectronicReporting/Operational**.
3. Meklējiet **FormatMapingRun** notikumus, kur **EventID=2**, jo šie notikumi ietver informāciju par patērēto laiku.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Trace parsētāja darbību izsekošana 

Tā kā ER ir ieviests kodā X++, varat izmantot vispārējos X++ rīkus, veiktspējas analizēšanai. Papildinformāciju skatiet sadaļā [Darbību izsekošana, izmantojot Trace parsētāju](../perf-test/trace-trace-tutorial.md).

Šai pieejai ir daži ierobežojumi. Tā kā daļa no ER ir ieviesta C#, ne visa informācija būs pieejama. Tomēr, varat skatīt datu izmantošanas informāciju. Turklāt pārskata ilga izpilde var pārsniegt darbību izsekošanas krātuves ierobežojumus.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER darbību izsekošana

ER var apkopot savu darbību izsekošanas informāciju, un tam ir vizualizācijas un analīzes rīki, kas paredzēti šīm izsekotajām darbībām. Papildinformāciju skatiet [Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Tā kā gan X++, gan ER ir ieviesti papildus .NET platformai, varat izmantot vispārējos .NET rīkus. Piemēram, varat izmantot bezmaksas [PerfView](https://github.com/Microsoft/perfview) rīku.

Varat arī apkopot datus no komandrindas. Piemēram, tālāk redzamais Windows PowerShell skripts apkopo izpildes laiku, līdz datorā tiek apturēta jebkāda formāta izpilde.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Šai pieejai ir daži ierobežojumi. Jums ir nepieciešama administratora piekļuve šim datoram. Turklāt jums ir jābūt pieredzējušiem izstrādātājiem, jo eksistē grūtības apgūt šo pieredzi.

### <a name="making-changes"></a><a name="making-changes"></a>Izmaiņu veikšana

#### <a name="use-caching"></a><a name="use-caching"></a>Kešdarbes izmantošana

Lai gan kešdarbe samazina laiku, kas nepieciešams atkārtotai datu ienesei, tā aizņem lielu atmiņas krātuves vietu. Izmantojiet kešdarbi gadījumos, kad ienesto datu apjoms nav pārāk liels. Papildinformāciju un piemēru, kas parāda, kā izmantot kešdarbi, skatiet sadaļā [Modeļa kartēšanas uzlabošana, pamatojoties uz izpildes darbību izsekošanas informāciju](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="reduce-volume-of-data-fetched"></a><a name="reduce-fetched-data"></a> Samazināt ienesto datu apjomu

Atmiņas patēriņu kešatmiņai var samazināt, ierobežojot lauku skaitu programmas tabulas ieneses ieneses izpildlaikā. Šajā gadījumā tiks ienestas tikai tās programmas tabulas lauka vērtības, kas nepieciešamas ER modeļa kartēšanai. Citi šīs tabulas lauki netiks ienesti. Tāpēc atmiņas apjoms, kas ir nepieciešams ienesto ierakstu ierakstīšanai kešatmiņā, tiek samazināts. Papildinformāciju skatiet [ER risinājumu veiktspējas uzlabošanai, samazinot izpildlaikā ienesto tabulas lauku skaitu](er-reduce-fetched-fields-number.md).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Izmantot kešdarbes parametru aprēķināto lauku

Dažreiz vērtības ir nepieciešams izmantot atkārtoti. Piemēri ietver kontu nosaukumus un kontu numurus. Lai ietaupītu laiku, varat izveidot aprēķinātu lauku, kura parametri atrodas augstākajā līmenī, un pēc tam pievienot šo lauku kešatmiņai.

Šo pieeju ieteicams lietot tikai tad, ja kešatmiņā saglabāto datu lielums ir mazs. Papildinformāciju skatiet sadaļā [ER risinājumu veiktspējas uzlabošana, pievienojot APRĒĶINĀTĀ LAUKA datu avotu parametrus](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>SAVIENOJUMA datu avota izmantošana

Datu avots **SAVIENOJUMS** iespējo vairāku savienotu ierakstu ienešanu, izmantojot vienu vaicājumu. Nav nepieciešams izmantot atsevišķu vaicājumu, lai ienestu katru savienoto ierakstu. Piemēram, ja ir 1000 rindas un katras rindas krājumu dati tiek ienesti, izmantojot relāciju, tad sanāks 1001 vaicājums (= 1000 + 1). Izmantojot **SAVIENOJUMA** datu avotu, jūs izmantosit tikai vienu vaicājumu, lai ienestu tos pašus datus. Papildinformāciju skatiet sadaļā [Izmantojiet SAVIENOJUMA datu avotus ER modeļu kartējumos, lai iegūtu datus no vairākām programmas tabulām](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Funkcijas WHERE vietā izmantot funkciju FILTER

Funkcija **[FILTER](er-functions-list-filter.md)** platformā SQL Server izpilda nosacījumus, savukārt **WHERE** funkcija ienes visus datus no saraksta pa vienam ierakstam un piemēro nosacījumus katram ierakstam. Piemēram, jūs vēlaties atlasīt vienu ierakstu no 1000 ierakstiem. Ja izmantosit **WHERE**, tiks ienesti visi 1000 ieraksti. Tomēr, ja izmantosit **FILTER**, tiks ienests tieši viens ieraksts. **FILTER** var izmantot arī indeksus datu bāzes pusē.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Apkopoto datu funkciju vai uzkrāto datu avota izmantošana

Ja konfigurācijai ir *grupēt pēc* komponents, kas apkopo iepriekš ienestos datus pēc pārskata, tad komponents visus datus ienesīs atkārtoti. Izmantojot apkopotās datu funkcijas, jūs iespējojat ER uzkrāt datus pirmās ieneses laikā. Plašāku informāciju skatiet [ER formātu konfigurēšana, lai veiktu uzskaiti un summēšanu](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Konfigurācijas daļu pārrakstīšana kompilatorā X++

ER atbalsta tabulu un klašu izsaukšanas metodes, ieskaitot paplašinājumus. Apsveriet iespēju pārrakstīt modeļa kartēšanas daļas kompilatorā X++, lai palīdzētu uzlabot veiktspēju.

ER var patērēt datus no šādiem avotiem:

- Klases (**objekta** un **klases** datu avoti)
- Tabulas (**tabulas** un **tabulas ierakstu** datu avoti)

[ER programmas programmēšanas interfeiss (API)](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) nodrošina arī veidu, kā nosūtīt iepriekš aprēķinātos datus no izsaukšanas koda. Programmas komplekts satur daudzus šādas pieejas piemērus.
