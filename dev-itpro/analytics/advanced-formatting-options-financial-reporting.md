---
title: "Papildu formatēšanas opcijas finanšu pārskatos"
description: "Veidojot finanšu pārskatu, ir pieejamas papildu formatēšanas funkcijas, ieskaitot filtrus dimensijām, ierobežojumus kolonnām un pārskata vienībām, nedrukājamas rindas un IF/THEN/ELSE apgalvojumus aprēķinos."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cc22e564c68ab04c61f2a2fc9d0a70335dc05b06
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="advanced-formatting-options-in-financial-reporting"></a>Papildu formatēšanas opcijas finanšu pārskatos

[!include[banner](../includes/banner.md)]


Veidojot finanšu pārskatu, ir pieejamas papildu formatēšanas funkcijas, ieskaitot filtrus dimensijām, ierobežojumus kolonnām un pārskata vienībām, nedrukājamas rindas un IF/THEN/ELSE apgalvojumus aprēķinos. 

Tabula paskaidro papildu formatēšanas funkcijas, kas ir pieejamas, veidojot pārskatus.

| Funkcija                   | Apraksts                                                                                                                                                                                                                                                                                                                     |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensiju filtrs           | Lai piekļūtu noteiktām datu kopām, jūs varat izmantot rindas definīcijas un kolonnas definīcijas dimensijas. Daudzos pārskatos rindu formātā tiek izmantots tikai fiziskais segments. Tomēr rindas var būt modificētas tā, lai tās saturētu dimensijas vērtības. Dimensiju filtri kolonnas definīcijā tiek izmantoti, lai piekļūtu noteiktām dimensiju vērtībām. |
| Pārskata vienības ierobežojums | Pārskata rindu var iestatīt tā, lai tā parāda tikai informāciju, kas ir saistīta ar konkrētu pārskata vienību.                                                                                                                                                                                                                      |
| Nedrukājamas (NP) rindas     | Nedrukājamas rindas ir noderīgas daudzos pārskatos. Ja ir nepieciešami vairāki aprēķini, lai iegūtu vērtību, šie aprēķini var būt paslēpti drukātajā pārskatā. Nedrukājamās rindas tiek pielietotas arī problēmu novēršanas pārskatu dizainos, un papildu šūnu novietojumos.                                                    |
| Kolonnas ierobežojums         | Kolonnu ierobežojums rindas definīcijā ir noderīgs vērtību paslēpšanai, kas attiecas tikai uz dažām pārskata rindām. Kad rindā tiek veikti procentu vērtību aprēķini, kolonnas ierobežojums neļauj kopsummas kolonnas vai citu kolonnu drukāšanu, ja šie numuri nav piemērojami.                              |
| Kolonnas atkāpe               | Jūs varat pievienot kolonnu pārtraukumus rindas definīcijā, lai parādītu pārskata informāciju blakus. Jūs varat pievienot vairākus kolonnas pārtraukumus vienā rindas definīcijā, un kolonnas galvenes tiek atkārtotas katras kolonnas augšpusē pēc kolonnas pārtraukuma. Pārskata komentāri tiek rādīti starp kolonnu pārtraukumiem.                              |
| IF/THEN/ELSE apgalvojumi     | Var modificēt aprēķinus rindas definīcijā vai kolonnas definīcijā.                                                                                                                                                                                                                                                         |

## <a name="advanced-cell-placement"></a>Papildu šūnu novietojums
Papildu šūnu novietojums, vai *forsēšana*, ietver noteiktas vērtības novietojumu noteiktās šūnās. Piemēram, forsēšanu bieži lieto, lai pārvietotu pareizu līdzsvaru skaidras naudas plūsmas pārskatā. Jūs varat izmantot forsēšanu šādiem mērķiem:

-   Pārvietot vērtības no programmas Microsoft Excel uz konkrētām šūnām.
-   Stingri definēt noteiktas vērtības atskaitē.
-   Modificēt pazīmes, kopējot vērtību no iepriekšējās šūnas un šo vērtību reizinot ar -1.

**Piezīme:** daudzos gadījumos, jums ir jākonfigurē pārskata definīcija tā, lai kolonnu aprēķini tiek paveikti pirms rindu aprēķiniem. Lai pabeigtu šo konfigurāciju, rīkojieties šādi.

1.  Pārskatu veidotājā atveriet pārskata definīciju.
2.  Cilnē **Iestatījumi**, sadaļā **Aprēķina prioritāte**, atlasiet **Vispirms veikt kolonnas aprēķinu, un tad rindas aprēķinu**.

## <a name="designing-the-report"></a>Pārskata izkārtošana
Veidojot pārskatu, jums vispirms vajadzētu izveidot visas detalizācijas rindas, lai pārliecinātos, ka vērtības tiek iegūtas kā paredzēts. Pēc tam pievienojiet **NP** (Nedrukājams) formātu, lai ignorētu detalizāciju, kas satur gala vērtības. **Svarīgi:**, izmantojot formāta kodu **CAL** rindas definīcijā, jūs nevarat apskatīt detaļās darbības detalizāciju. Forsēšanai formulas izmanto šādu formātu: &lt;mērķa kolonna&gt;=&lt;sākotnējā kolonna&gt;.&lt;rindas kods&gt; Visus rindas papildu izvietojumus atdaliet ar komatu un atstarpi. Piemērs: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Papildu formatēšanas opciju piemēri
Zemāk sniegtie piemēri parāda kā formatēt rindas definīciju un kolonnas definīciju, lai forsētu pamata naudas plūsmas pārskatu (piemērs 1) un statistikas pārskatu (piemērs 2).

### <a name="example-1-basic-forcing"></a>Piemērs 1: Pamata forsēšana

Šajā tabulā ir parādīts rindas definīcijas piemērs, kas izmanto pamata forsēšanu.

| Rindas kods | Apraksts                      | Formāta kods | Saistītās formulas/Rindas/Vienības | Formāta ignorēšana | Parastā bilance | Drukāšanas vadība | Kolonnas ierobežojumi | Rindu modifikators               | Saite uz finanšu dimensijām |
|----------|----------------------------------|-------------|-----------------------------|-----------------|----------------|---------------|--------------------|----------------------------|------------------------------|
| 100      | Skaidras naudas atlikums perioda sākumā |             |                             |                 |                |               |                    | Konta modifikators = \[/BB\] | +Segments2 = \[1100\]         |
| 130      | Skaidras naudas atlikums perioda sākumā      | CAL         | C=C.100,F=D.100             |                 |                |               |                    |                            |                              |
| 160      |                                  |             |                             |                 |                |               |                    |                            |                              |
| 190      |                                  |             |                             |                 |                |               |                    |                            |                              |

Šajā tabulā ir parādīts kolonnas definīcijas piemērs, kas kolonnā izmanto pamata forsēšanu.

|                              | A   | B    | C        | D      | E      | F    |
|------------------------------|-----|------|----------|--------|--------|------|
| Galvene 1                     |     |      |          |        |        |      |
| Galvene 2                     | A   | B    | C        | D      | E      | F    |
| Galvene 3                     |     |      |          |        |        |      |
| Kolonnas tips                  | RINDA | DESC | FD       | FD     | FD     | CALC |
| Grāmatas kods/Kategorijas atribūts |     |      | FAKTISKAIS   | FAKTISKAIS | FAKTISKAIS |      |
| Finanšu gads                  |     |      | PAMATA     | PAMATA   | PAMATA   |      |
| Periods                       |     |      | PAMATA     | PAMATA   | PAMATA   |      |
| Iekļautie periodi              |     |      | PERIODISKS | YTD/BB | YTD    |      |
| Formula                      |     |      |          |        |        | E-D  |
| Kolonnas platums                 | 5.   | 30   | 14.       | 14.     | 14.     | 14.   |

### <a name="example-2-statistical-reports"></a>Piemērs 2: Statistikas pārskati

Šajā tabulā ir parādīts rindas definīcijas piemērs, kas izmanto pamata forsēšanu statistikas pārskatam.

| Rindas kods | Apraksts               | Formāta kods | Saistītās formulas/Rindas/Vienības     | Formāta ignorēšana      | Parastā bilance | Drukāšanas vadība | Kolonnas ierobežojumi | Rindu modifikators | Saite uz finanšu dimensijām               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|---------------|--------------------|--------------|--------------------------------------------|
| 50       | Statistiskā informācija   | REM         |                                 |                      |                |               |                    |              |                                            |
| 100      | Darbinieku skaits - ASV            | CAL         | 4.                               | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 115      | Darbinieku skaits - Starptautiskais | CAL         | 11.                              | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 130      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 190      | ASV tirdzniecība                  |             |                                 |                      | C              |               |                    |              | +Segments2 = \[41\*\], Segments3 = \[00\]    |
| 220      | Starptautiskā tirdzniecība       |             |                                 |                      | C              |               |                    |              | +Segments2 = \[41\*\], Segments3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 280      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 310      | ASV tirdzniecība                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |               |                    |              |                                            |
| 340      | Starptautiskā tirdzniecība       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |               |                    |              |                                            |

Šajā tabulā ir parādīts kolonnas definīcijas piemērs, kas izmanto pamata forsēšanu statistikas pārskatam.

|                              | A   | B    | C      | D            | E     | F            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Galvene 1                     | A   | B    | C      | D            | E     | F            |
| Galvene 2                     | -   | -    | YTD    | Ikgadēja tirdzniecība | Personāls | $ Vienai personai |
| Galvene 3                     |     |      |        |              |       |              |
| Kolonnas tips                  | RINDA | DESC | FD     | CALC         | CALC  | CALC         |
| Grāmatas kods/Kategorijas atribūts |     |      | FAKTISKAIS |              |       |              |
| Finanšu gads                  |     |      | PAMATA   |              |       |              |
| Periods                       |     |      | PAMATA   |              |       |              |
| Iekļautie periodi              |     |      | YTD    |              |       |              |
| Formula                      |     |      |        |              |       | E-D          |
| Kolonnas platums                 | 5.   | 30   | 14.     | 14.           | 14.    | 14.           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Ierobežot rindu, lai noteiktu pārskata mērvienību
Ja pārskata rinda ir ierobežota noteiktai pārskata vienībai, tajā rindā tiek parādīti saistītie dati tikai nosauktajai pārskata vienībai, un ignorēti dati citām pārskata vienībām pārskata kokā. Piemēram, jūs varat izveidot rindu, kas sniedz detalizāciju par kopējās darbības izdevumus un noteiktu nodaļu. Jūsu ziņojums var saturēt dublētus datus, ja pārskats satur gan pārskata koka, gan rindas definīciju, kas ir vairāk nekā tikai fizisks konts. Piemēram, jums ir pārskata koks, kurā ir uzskaitītas sešas nodaļas jūsu organizācijā, un jums ir arī rindas definīcija, kas uzskaita noteiktu kontu un nodaļu kombināciju rindā. Veidojot pārskatu, konta un nodaļas noteikta kombinācija tiek izdrukāta katrā pārskata koka līmenī pat, ja šī nodaļa var neatbilst tam, kas ir kokā. Tas notiek tāpēc, ka rinda ignorē to, kas parasti tiek filtrēts pārskata definīcijā. Viens veids, kā izvairīties no datu dublēšanas ir ierobežot rindu noteiktai pārskata vienībai. **Piezīme:** ja rinda satur dimensijas, un jūs ierobežojat šo rindu pārskata apakšvienībai, rindas summa tiek iekļauta apakšvienībā, un tās pamatvienībās, bet dublēšanās nenotiek.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Ierobežot rindu līdz pārskata vienībai

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atlasiet modificējamo rindas definīciju.
2.  Veiciet dubultklikšķi uz atbilstošās **Saistītās Formulas/Rindas/Vienības** šūnas.
3.  Dialoglodziņā **Pārskata vienību atlase**, laukā **Pārskata koks**, atlasiet koku, kas ir piešķirts pārskata definīcijā.
4.  Atlasiet pārskata vienību, un pēc tam noklikšķiniet uz **Labi**. Ierobežojums parādās rindas definīcijas šūnā.
5.  Veiciet dubultklikšķi uz ierobežotās rindas šūnas **Saite uz finanšu dimensijām** kolonnu, un pēc tam ievadiet saiti uz finanšu datu sistēmu.

## <a name="selecting-print-control-in-a-row-definition"></a>Drukāšanas vadības atlasīšana rindas definīcijā
Drukāšanas vadības kodus katrai kolonnai var norādīt, izmantojot **Drukāšanas vadība** šūnu.

### <a name="add-print-control-codes-to-a-report-row"></a>Pievienot pārskata rindai drukāšanas vadības kodus

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Drukāšanas vadība**.
3.  Dialoglodziņā **Drukāšanas vadība**, atlasiet drukāšanas vadības kodu vai nospiediet un turiet taustiņu Ctrl, lai atlasītu vairākus kodus. Jūs varat arī ievadīt drukāšanas kodus pa tiešo šūnā **Drukāšanas vadība**. Izmantojiet komatu, lai atdalītu vairākus drukāšanas vadības kodus.
4.  Atlasiet nosacījuma drukāšanas opcijas.
5.  Noklikšķiniet uz **Labi**.

### <a name="regular-print-control-codes"></a>Parasti drukāšanas vadības kodi

Šajā tabulā ir aprakstītas rindas definīcijas parastas drukāšanas vadības kodi.

| Drukāšanas vadības kods | Drukāšanas vadības kodu atšifrējums         | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Nedrukājama rinda                                 | Nepieļauj, ka tiek drukātas summas rindā, un izslēdz summas no aprēķiniem. Lai aprēķinā iekļautu nedrukājamu kolonnu, veidojiet atsauci uz kolonnu tieši aprēķina formulā. Piemēram, nedrukājama rinda 240 ir iekļauta šādā aprēķinā: **230+240+250**. Tomēr, nedrukājama rinda 240 netiek iekļauta šādā aprēķinā: **230:250**. |
| CS                 | Valūtas simbols; lietot valūtas formātu šajā rindā | Iekļaut valūtas simbolu visās neprocentuālajās summās. Procentuālās vērtības nekad nesaņem valūtas simbolu.                                                                                                                                                                                                                                                                                                |
| XD                 | Likvidēt rindu kontu detalizācijas pārskatā            | Likvidēt kontu parādīšanu konta detalizācijas pārskatos un darbību detalizācijas pārskatos. Šī drukāšanas vadība ir noderīga, kad rindā tiek iekļauti vairāki konti, kas nav jāuzskaita konta detalizācijas pārskatā vai darbības detalizācijas pārskatā.                                                                                                                                                           |
| X0                 | Likvidēt rindu, ja visas vērtības ir nulle                        | Izslēdziet rindu no pārskata, ja visas šūnas rindā ir vai nu tukšas vai satur nulles. Šī drukāšanas vadība ir jēgpilna tikai tad, ja pārskata definīcijā nav atlasīta nulles bilances nerādīšanas opcija.                                                                                                                                                                                            |
| B0                 | Atstāt nulles kolonnas tukšas                         | Atstājiet kolonnas tukšas rindā, kas satur nulles vērtības.                                                                                                                                                                                                                                                                                                                                                      |
| XR                 | Likvidēt apkopojumu                                  | Likvidējiet apkopojumu. Ja pārskatā tiek izmantots pārskata veidošanas koks, summas šajā rindā netiek apkopotas turpmākos pamatmezglos.                                                                                                                                                                                                                                                                               |
| SR                 | Likvidēt noapaļošanu                                | Neļaut summu noapaļošanu šajā rindā.                                                                                                                                                                                                                                                                                                                                                          |
| XT                 | Likvidēt rindu darbības detalizācijas pārskatā        | Likvidēt darbību parādīšanu darbību detalizācijas pārskatos. Šī drukāšanas vadība ir noderīga, kad rindā tiek iekļauti vairāki konti, kas nav jāuzskaita darbības detalizācijas pārskatā.                                                                                                                                                                                                             |

### <a name="conditional-print-control-codes"></a>Nosacījuma drukāšanas vadības kodi

Šajā tabulā ir aprakstītas rindas definīcijas nosacījuma drukāšanas vadības kodi.

| Drukāšanas vadības kods | Apraksts                                  |
|--------------------|----------------------------------------------|
| (nav)             | Notīriet nosacījuma drukāšanas atlasi.       |
| DR                 | Drukāt tikai debeta bilances šai rindai.  |
| CR                 | Drukāt tikai kredīta bilances šai rindai. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Kolonnu ierobežojumi rindas definīcijā
Šūnai **Kolonnas ierobežojums** rindas definīcijā ir vairāki mērķi. Atkarībā no rindas tipa, jūs varat izmantot šūnu **Kolonnas ierobežojums**, lai norādītu vienu no šim funkcijām:

-   Šūna var ierobežot rindu summu drukāšana noteiktai kolonnai. Šī funkcija ir noderīga, ja veidojat tabulveida bilanci.
-   Šūna var norādīt summu kolonnu kārtošanai.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Aprēķina formulas izmantošana rindas definīcijā
Aprēķina formula rindas definīcijā var saturēt operatorus **+**, **-**, **\*** un **/**, kā arī apgalvojumus **IF/THEN/ELSE**. Turklāt, aprēķins var ietvert atsevišķas šūnas un absolūtās summas (faktiskās vērtības, kas ir iekļautas formulā). Formula var ietvert ne vairāk kā 1024 rakstzīmes. Aprēķini nevar būt piemēroti rindām, kas satur **Saite uz finanšu dimensijām** (FD) tipa šūnas. Tomēr jūs varat ietvert aprēķinus secīgās rindās, likvidēt šo rindu drukāšanu, un pēc tam summēt aprēķina rindas.

### <a name="operators-in-a-calculation-formula"></a>Operatori aprēķina formulā

Aprēķina formula izmanto sarežģītākus operatorus nekā rindas summas formula. Taču operatorus **\*** un **/** varat izmantot kopā ar papildu operatoriem summu reizināšanai (\*) un dalīšanai (/). Lai izmantotu diapazonu vai summu aprēķina formulā, jums jāizmanto zīmi (@) pirms jebkura rindas koda, ja vien jūs neizmantojat kolonnu rindas definīcijā. Piemēram, lai summu rindā 100 pieskaitītu summai rindā 330, varat izmantot rindu kopsummas formulu **100+330** vai aprēķina formulu **@100+@330**. **Piezīme:** nepieciešams izmantot zīmi (@) pirms katra rindas koda, ko jūs izmantojat aprēķinu formulā. Pretējā gadījumā skaitlis ir lasāms kā absolūta summa. Piemēram, ar formulu **@100+330** summai rindā 100 tiek pieskaitīti USD 330. Norādot kolonnu aprēķināšanas formulā, zīme (@) nav nepieciešama.

### <a name="create-a-calculation-formula"></a>Izveidot aprēķina formulu

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Formāta kods**, un atlasiet **CAL**.
3.  Šūnā **Saistītās formulas/Rindas/Vienības** ievadiet aprēķina formulu.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Aprēķina formulas piemērs noteiktām rindām

Šajā piemērā aprēķina formula **@100+@330** nozīmē, ka summa rindā 100 tiek pieskaitīta summai rindā 330. Ar rindu kopsummas formulu **340+370** rindā 340 esošā summa tiek pieskaitīta summai rindā 370. (Rindā 370 esošā summa ir no aprēķina formulas iegūta summa.)

| Rindas kods | Apraksts                 | Formāta kods | Saistītās formulas/Rindas/Vienības | Drukāšanas vadība | Rindu modifikators | Saite uz finanšu dimensijām |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Skaidras naudas atlikums perioda sākumā |             |                            | NP            | BB           | +Konts=\[1100:1110\]       |
| 370      | Skaidras naudas atlikums gada sākumā   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Skaidras naudas atlikums perioda sākumā | TOT         | 340+370                    |               |              |                              |

Ja rindas definīcijā rindai ir formāta kods **CAL**, un jūs ievadāt matemātisko aprēķinu šūnā **Saistītās Formulas/Rindas/Vienības**, pārskatā nepieciešams ievadīt arī saistītās kolonnas un rindas burtu. Piemēram, ievadiet **A.120**, lai apzīmētu kolonnu A, rindu 120. Ja vēlaties, visu kolonnu norādīšanai varat izmantot zīmi @. Piemēram, ievadiet **@120**, lai apzīmētu visas kolonnas rindā 120. Jebkurš matemātiskais aprēķins, kurā nav kolonnas burta vai zīmes @, tiek uzskatīts par reālu skaitli. **Piezīme.** Ja atsaucei uz rindu izmantojat etiķetes rindas kodu, kā atdalītājs starp kolonnas burtu un etiķeti ir jālieto punkts (.) (piemēram, **A.GROSS\_MARGIN/A.SALES**). Ja izmantojat zīmi @, tad atdalītājs nav nepieciešams (piemēram, **@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Aprēķina formulas piemērs noteiktai kolonnai

Šajā piemērā aprēķina formula **E=C.340** nozīmē, ka šūnā, kas atrodas kolonnā C, rindā 340 tiek veikts aprēķins tikai kolonnai E. **Piezīme:** kad jūs norādāt kolonnu aprēķināšanas formulā, zīme (@) nav nepieciešama.

| Rindas kods | Apraksts                 | Formāta kods | Saistītās formulas/Rindas/Vienības | Drukāšanas vadība | Rindu modifikators | Saite uz finanšu dimensijām |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Skaidras naudas atlikums perioda sākumā |             |                            | NP            | BB           | +Konts=\[1100:1110\]       |
| 370      | Skaidras naudas atlikums gada sākumā   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Skaidras naudas atlikums perioda sākumā | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Skaitļa modificēšana atlasītajās kolonnās

Ja jūs modificējat skaitli vai aprēķinu vienā noteiktas rindas kolonnā, bet nevēlaties ietekmēt citas kolonnas pārskatā, jūs varat norādīt **CAL** (aprēķins), rindas definīcijas kolonnā **Formāta kods**.

-   Lai veiktu aprēķinu visās pārskata kolonnās (**FD**), neievadiet kolonnas piešķīrumu.
-   Lai formulu ierobežotu uz noteiktām kolonnām, ievadiet kolonnas burtu, vienādības zīmi (**=**) un pēc tam formulu.
-   Jūs varat norādīt vairākas kolonnas. Ja izmantojat zīmi (@) ar īpašu kolonnas izvietojumu, zīme (@) ir saistīta ar rindu.
-   Vienā rindā jūs varat ievadīt vairākas kolonnas formulas. Atdaliet formulas ar komatiem.

### <a name="calculation-examples"></a>Aprēķina piemēri

| Aprēķins            | Darbība, kas tiek izveidota                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Katrā kolonnas rindā vērtība 130 tiek reizināta ar 0,75. Rezultāts tiek ievietots katras kolonnas pašreizējā rindā. |
| B=@130\*.75            | Tas pats aprēķins tiek veikts kolonnā B.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF/THEN/ELSE apgalvojumi rindas definīcijā

**IF/THEN/ELSE** apgalvojumus var pievienot jebkuram derīgam aprēķinam, un izmantot ar **CAL** formātu. Jūs ievadāt **IF/THEN/ELSE** aprēķina formulas šūnā **Saistītās Formulas/Rindas/Vienības** kolonnā. **IF/THEN/ELSE** aprēķina formulas izmanto šādu formātu: IF &lt;patiess/aplams apgalvojums&gt; THEN &lt;formula&gt; ELSE &lt;formula&gt; Apgalvojuma daļa **ELSE &lt;formula&gt;** nav obligāta.

#### <a name="if-statements"></a>IF apgalvojumi

Apgalvojums, kas seko **IF** apgalvojumam, var būt jebkurš apgalvojums, kuru var novērtēt kā patiesu vai nepatiesu. Apgalvojums, kas seko **IF** apgalvojumam var ietvert vienkāršu novērtējumu, vai arī tas var būt sarežģīts apgalvojums, kas var saturēt vairākas izteiksmes. Daži piemēri:

-   **IF A.200&gt;0** (Vienkāršs apgalvojums)
-   **IF A.200&gt;0 AND A.200&lt;10,000** (Komplekss apgalvojums)
-   **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (Komplekss apgalvojums, kas satur vairākas izteiksmes)

Nosacījums **Periodi**, apgalvojumā **IF** parāda pārskata periodu skaitu. Šis nosacījums parasti tiek izmantots, lai aprēķinātu līdzšinējā gada vidējo. Piemēram, kad tiek veikta atskaite periodam 7 šī gada, nosacījums **B.150/Periods** nozīmē, ka vērtība, kas atrodas kolonnā B, rindā 150 tiek dalīta ar 7.

#### <a name="then-and-else-formulas"></a>THEN un ELSE formulas

Formulas **THEN** un **ELSE** var būt jebkurš derīgs aprēķins, no ļoti vienkāršiem vērtību piešķīrumiem līdz sarežģītām formulām. Piemēram, apgalvojums **IF A.200&gt;0 THEN A=B.200** nozīmē: “ja vērtība šūnā, kas atrodas kolonnā A, rindā 200, ir lielāka par 0 (nulle), tad vērtību no šūnas, kas atrodas kolonnā B, rindā 200, ir jāievieto pašreizējās rindas kolonnas A šūnā”. Iepriekšējais **IF/THEN** apgalvojums ievieto vērtību pašreizējās rindas vienā kolonnā. Tomēr, jūs varat lietot arī zīmi (@) kādā no formulas patiess/aplams novērtējumiem, lai parādītu visas kolonnas. Šeit ir daži piemēri, kas aprakstīti turpmākajās sadaļās:

-   **IF A.200 &gt;0 THEN B.200**: ja šūnas A.200 vērtība ir pozitīva, tad vērtība no šūnas B.200 tiek ievietota katrā pašreizējās rindas kolonnā.
-   **IF A.200 &gt;0 THEN @200**: ja šūnas A.200 vērtība ir pozitīva, tad vērtība no katras kolonnas rindā 200 tiek ievietota pašreizējās rindas atbilstošajā kolonnā.
-   **IF @200 &gt;0 THEN @200**: ja pašreizējā kolonnā rindas 200 vērtība ir pozitīva, tad vērtība no rindas 200 tiek ievietota pašreizējās rindas tajā pašā kolonnā.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Aprēķina ierobežošana līdz pārskata vienībai rindas definīcijā

Lai pārskatu kokā kādu aprēķinu ierobežotu uz atsevišķu pārskatu vienību tā, lai iegūtā summa netiek apkopota uz augstāka līmeņa vienību, rindas definīcijas šūnā **Saistītās formulas/rindas/vienības** varat izmantot kodu **@Unit**. Kods **@Unit** ir uzskaitīts pārskatu koka struktūras kolonnā B, **Vienības nosaukums**. Ja izmantojat kodu **@Unit**, vērtības netiek apkopotas uz augstāku līmeni, bet aprēķins tiek novērtēts katrā pārskatu koka līmenī. **Piezīme:** lai lietotu šo funkciju, pārskata kokam jābūt saistītām ar rindas definīciju. Aprēķinu rinda var atsaukties uz aprēķinu rindu vai finanšu datu rindu. Aprēķins tiek ierakstīts rindas definīcijas un finanšu datu – tipa ierobežojuma šūnā **Saistītās Formulas/Rindas/Vienības**. Aprēķinā ir jāizmanto nosacījuma aprēķins, kas sākas ar konstrukciju **IF @Unit**. Piemērs: IF @Unit(SALES) THEN @100 ELSE 0 Šajā aprēķinā ir iekļauta summa no katras pārskatā esošās kolonnas rindas 100, bet tikai Pārdošanas vienībai. Ja vairākām vienībām ir nosaukums Pārdošana, summa tiek parādīta katrā no šīm vienībām. Turklāt rinda 100 var būt finanšu datu rinda, un var būt definēta kā nedrukājama. Šajā gadījumā summa netiek parāda visās vienībās kokā. Jūs varat arī ierobežot summu vienam kolonnas pārskatam, piemēram, kolonnai H, izmantojot kolonnu ierobežojumu, lai drukātu vērtību tikai šajā pārskata kolonnā. Jūs varat iekļaut **OR** kombinācijas apgalvojumā **IF**. Piemērs: IF @Unit(SALES) OR @Unit(SALESWEST) THEN 5 ELSE @100 Aprēķina tipa ierobežojumā vienību varat norādīt vienā no tālāk aprakstītajiem veidiem.

-   Ievadiet vienības nosaukumu, lai iekļautu atbilstošas vienības. Piemēram, **IF @Unit(SALES)** iespējo aprēķinu jebkurai vienībai, kuras nosaukums ir Pārdošana, pat ja pārskatu kokā pastāv vairākas Pārdošanas vienības.
-   Ievadiet uzņēmuma un vienības nosaukumu, lai ierobežotu aprēķinu līdz noteiktām vienībām noteiktā uzņēmumā. Piemēram, ievadiet **IF @Unit(ACME:SALES**), lai aprēķinu ierobežotu uz Pārdošanas vienībām ACME uzņēmumā.
-   Ievadiet pilnu hierarhijas kodu no pārskata koka, lai ierobežot aprēķinu līdz noteiktai mērvienībai. Piemēram, ievadiet **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)**. **Piezīme:** Lai atrastu pilnu hierarhijas kodu, ar peles labo pogu noklikšķiniet pārskata koka definīcijā, un pēc tam atlasiet **Kopēt pārskata vienības identifikatoru (H kods)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Ierobežot aprēķinu līdz pārskata vienībai

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Formāta kods**, un atlasiet **CAL**.
3.  Noklikšķiniet uz šūnas **Saistītās formulas/rindas/vienības**, un pēc tam ievadiet nosacījuma aprēķinu, kas sākas ar konstrukciju **IF @Unit**.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF/THEN/ELSE apgalvojumi kolonnas definīcijā

Apgalvojums **IF/THEN/ELSE** ļauj jebkuram aprēķinam būt atkarīgam no citas kolonnas rezultātiem. Jūs varat atsaukties uz citām kolonnām, bet jūs nevarat atsaukties uz pārskata šūnu apgalvojumā **IF**. Jebkurš aprēķins jāpielieto visai kolonnai. Piemēram, apgalvojums **IF B&gt;100 THEN B ELSE C\*1.25** nozīmē: “Ja summa kolonnā B ir lielāka par 100, tad vērtība no kolonnas B ir jāievieto kolonnā **CALC**. Ja summa kolonnā B nav lielāka par 100, tad vērtība kolonnā C ir jāreizina ar 1,25 un rezultāts ir jāievieto kolonnā **CALC**.” Vienmēr turpiniet apgalvojumu **IF** ar loģisku apgalvojumu, kuru var novērtēt kā patiesu vai nepatiesu. Formulas, kuras tiek izmantotas gan apgalvojumā **THEN**, gan apgalvojumā **ELSE** var saturēt atsauces uz kolonnu skaitu, un šīs formulas var būt tik sarežģītas, cik jums nepieciešams. **Piezīme:** Jūs nevarat ievietot aprēķina rezultātu nevienā citā kolonnā. Rezultātiem jābūt kolonnā, kas satur formulu.




