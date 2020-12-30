---
title: Elektronisko atskaišu veidošanas formulas valoda
description: Šajā tēmā ir sniegta informācija pat to, kā izmantot formulu valodu elektronisko atskaišu (ER) veidošanā.
author: NickSelin
manager: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3f11e91d06f20d1c384c3c2c5cf9326214331ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686273"
---
# <a name="electronic-reporting-formula-language"></a>Elektronisko atskaišu veidošanas formulas valoda

[!include [banner](../includes/banner.md)]

Elektroniskie pārskati (ER) nodrošina spēcīgu datu transformācijas pieredzi. Valoda, kas tiek izmantota, lai izteiktu nepieciešamos datus manipulācijām [ER formulas noformētājā](general-electronic-reporting-formula-designer.md), līdzinās Microsoft Excel formulas valodai .

## <a name="basic-syntax"></a>Pamata sintakse

ER izteiksmes var saturēt jebkuru vai visus no šādiem elementiem:

- [Konstantes](#Constants)
- [Operatori](#Operators)
- [Atsauces](#References)
- [Ceļi](#Paths)
- [Funkcijas](#Functions)

## <a name=""></a><a name="Constants">Konstantes</a>

Kad veidojat izteiksmes, varat lietot teksta un skaitļu konstantes (t.i., vērtības, kas netiek aprēķinātas). Piemēram, izteiksme `VALUE ("100") + 20` lieto skaitļu konstanti **20** un virknes konstanti **"100"**, un atgriež skaitlisku vērtību **120**.

ER formulas veidotājs atbalsta atsoļa sekvences. Tādējādi varat norādīt, kura izteiksmes virkne ir jāapstrādā citādi. Piemēram, izteiksme `"Leo Tolstoy ""War and Peace"" Volume 1"`atgriež teksta virkni **Leo Tolstoy "War and Peace" Volume 1**.

## <a name=""></a><a name="Operators">Operatori</a>

Tālāk esošajā tabulā ir parādīti aritmētiskie operatori, ko varat izmantot, lai veiktu pamata matemātiskās darbības, piemēram, saskaitīšanu, atņemšanu, reizināšanu un dalīšanu.

| Operators | Nozīme               | Paraugs     |
|----------|-----------------------|-------------|
| +        | Papildinājums              | `1+2`       |
| -        | Atņemšana, negācija | `5-2` - `-1` |
| \*       | Reizināšana        | `7\*8`      |
| /        | Nodaļa              | `9/3`       |

Tālāk esošajā tabulā parādīti atbalstītie salīdzināšanas operatori. Šos operatorus varat izmantot, lai salīdzinātu divas vērtības.

| Operators | Nozīme                  | Paraugs      |
|----------|--------------------------|--------------|
| =        | Vienādi                    | `X=Y`        |
| &gt;     | Lielāks nekā             | `X>Y`        |
| &lt;     | Mazāks nekā                | `X<Y`        |
| &gt;=    | Lielāks vai vienāds ar | `X>=Y`       |
| &lt;=    | Mazāks vai vienāds ar    | `X<=Y`       |
| &lt;&gt; | Nav vienāds ar             | `X<>Y`       |

Turklāt rakstzīmi & varat izmantot kā teksta savienošanas operatoru. Šādi vienu vai vairākas teksta virknes varat savirknēt jeb savienot vienā teksta daļā.

| Operators | Nozīme     | Paraugs                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Savienot | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Operatoru prioritātes

Ir svarīgi, kādā secībā tiek vērtētas saliktas izteiksmes daļas. Piemēram, izteiksmes `1 + 4 / 2` rezultāts atšķiras atkarībā no tā, vai pirmā tiek izpildīta saskaitīšanas vai dalīšanas operācija. Varat izmantot iekavas, lai skaidri definētu, kā izteiksme tiek novērtēta. Piemēram, lai norādītu, ka vispirms ir jāveic saskaitīšanas operācija, iepriekšējo izteiksmi varat mainīt uz `(1 + 4) / 2`. Ja skaidri nenorādāt operāciju secību izteiksmē, secība ir atkarīga no atbalstītajiem operatoriem piešķirtās noklusējuma prioritātes. Tālāk esošajā tabulā ir parādīta katram operatoram piešķirtā prioritāte. Operatori, kuru prioritāte ir augstāka (piemēram, 7), tiek vērtēti pirms operatoriem, kuriem ir zemāka prioritāte (piemēram, 1).

| Prioritāšu secība | Operatori      | Sintakse                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Grupēšana       | ( … )                                                                   |
| 6          | Piekļuve elementam  | … . …                                                                   |
| 5          | Funkcijas izsaukums  | … ( … )                                                                 |
| 4          | Reizināšana un dalīšana | … \* …<br>… / …                                                         |
| 3          | Saskaitīšana un atņemšana       | … + …<br>… - …                                                          |
| 2          | Salīdzinājums     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Atdalīšana     | … , …                                                                   |

Ja izteiksmē ir vairāki secīgi operatori ar vienādu prioritātes vērtību, šie operatori tiek vērtēti no kreisās uz labo pusi. Piemēram, izteiksme  `1 + 6 / 2 \* 3 > 5` atgriež vērtību **true**. Ieteicams izmantot iekavas, lai skaidri norādītu vēlamo operāciju secību izteiksmēs, lai izteiksmes būtu vieglāk lasāmas un uzturamas.

## <a name=""></a><a name="References">Atsauces</a>

Visus pašreizējā ER komponenta datu avotus, kas ir pieejami izteiksmes veidošanas laikā, var izmantot kā nosauktas atsauces. Pašreizējais ER komponents var būt vai nu modeļa kartēšana, vai formāts. Piemēram, pašreizējā ER datu modeļa kartēšana ietver datu avotu **ReportingDate**, kurš atgriež vērtību ar datu tipu *DateTime*. Lai pareizi formatētu šo vērtību ģenerēšanas dokumentā, izteiksmē uz datu avotu varat atsaukties šādi: `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Pirms visām ar atsauci norādītā datu avota nosaukumā esošajām rakstzīmēm, kas nav alfabēta burti, ir jāievieto vienpēdiņa ('). Ja ar atsauci norādītā datu avota nosaukumā ir vismaz viens simbols, kas nav alfabēta burts, nosaukums ir jāietver vienpēdiņās. Šie simboli, kas nav alfabēta burti, var būt, piemēram, pieturzīmes vai citi rakstveida simboli. Daži piemēri:

- Uz datu avotu **Today's date & time** ER izteiksmē ir jāatsaucas šādi: `'Today''s date & time'`.
- Uz datu avota **Customers** metodi **name()** ER izteiksmē ir jāatsaucas šādi: `Customers.'name()'`.

Ja programmas datu avotu metodēm ir parametri, šo metožu izsaukšanai tiek izmantota tālāk norādītā sintakse.

- Ja datu avota System metodei **isLanguageRTL** ir **System** parametrs **EN-US** ar datu tipu *String*, ER izteiksmē uz šo metodi ir jāatsaucas šādi: `System.isLanguageRTL("EN-US")`.
- Pēdiņas nav obligātas, ja metodes nosaukums ietver tikai burtu un ciparu simbolus. Taču tās ir obligātas tabulas metodei, ja nosaukums ietver iekavas.

Kad datu avots **System** tiek pievienots ER kartēšanai, kas atsaucas uz programmas klasi **Global**, izteiksme `System.isLanguageRTL("EN-US ")` atgriež *Būla* vērtību **FALSE**. Modificētā izteiksme `System.isLanguageRTL("AR")` atgriež *Būla* vērtību **TRUE**.

Varat ierobežot veidu, kādā vērtības tiek nodotas šī tipa metodes parametriem.

- Šī tipa metodēm var nodot tikai konstantes. Konstanšu vērtības tiek definētas veidošanas laikā.
- Šī tipa parametriem tiek atbalstīti tikai primitīvi (pamata) datu tipi. Primitīvie datu tipi ir *vesels skaitlis*, *reāls skaitlis*, *Būla vērtība* un *virkne*.

## <a name=""></a><a name="Paths">Ceļi</a>

Ja izteiksme atsaucas uz kādu strukturētu datu avotu, ceļa definīciju varat izmantot, lai atlasītu konkrētu šī datu avota primitīvo elementu. Punkta rakstzīme (.) tiek lietota, lai atdalītu atsevišķus strukturēta datu avota elementus. Piemēram, pašreizējā ER datu modeļa kartēšana ietver datu avotu **InvoiceTransactions**, un šis datu avots atgriež ierakstu sarakstu. Ieraksta **InvoiceTransactions** struktūra ietver laukus **AmountDebit** un **AmountCredit**, un šie abi lauki atgriež skaitliskas vērtības. Tāpēc, lai aprēķinātu rēķinā iekļauto summu, var noformēt šādu izteiksmi: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Šīs `InvoiceTransactions.AmountDebit`izteiksmes konstrukcija ir ceļš, kas tiek izmantots, lai piekļūtu veida **Record List** datu avota **InvoiceTransactions** laukam *AmountDebit*.

### <a name="relative-path"></a>Relatīvais ceļš

Ja strukturētā datu avota ceļš sākas ar zīmi "at" (@), tas ir relatīvs ceļš. "At" zīme tiek rādīta atlikušās izmantotās hierarhiskā koka absolūtā ceļa daļas vietā. Tālāk redzamajā attēlā parādīts piemērs. Šeit absolūtais ceļš `Ledger.'accountingCurrency()'`norāda, ka **Virsgrāmatas** datu avota uzskaites valūtas vērtība tiek ievadīta datu modeļa laukā **AccountingCurrency**.

![Absolūtā ceļa piemērs ER modeļa kartēšanas noformētāja lapā](./media/ER-FormulaLanguage-AbsolutePath.png)

Šajā ilustrācijā ir parādīts piemērs tam, kā tiek izmantots relatīvais ceļš. Relatīvais ceļš `@.AccountNum` norāda, ka lauks **AccountNum** datu avotā **Intrastat** (kas datu modeļa hierarhiskajā kokā tiek parādīts vienu līmeni virs lauka **AccountNum**) tiek izmantots, lai datu modeļa laukā **AccountNum** ievadītu debitora vai kreditora kodu.

![Relatīvā ceļa piemērs ER modeļa kartēšanas noformētāja lapā](./media/ER-FormulaLanguage-RelativePath1.png)

Atlikusī absolūtā ceļa daļa tiek rādīta arī [ER formulas redaktorā.](general-electronic-reporting-formula-designer.md).

![Atlikusī absolūtā ceļa daļa ER formulas noformētāja lapā](./media/ER-FormulaLanguage-RelativePath2.png)

Papildinformācijai skatiet [Relatīva ceļa lietošana ER modeļu un formātu datu saistījumiem](relative-path-data-bindings-er-models-format.md).

## <a name=""></a><a name="Functions">Funkcijas</a>

ER iebūvētās funkcijas var izmantot ER izteiksmēs. Visus izteiksmes konteksta datu avotus (respektīvi, pašreizējo ER datu kartēšanu vai ER formātu) var izmantot kā parametrus funkciju izsaukšanai saskaņā ar funkciju izsaukšanas argumentu sarakstu. Kā funkciju izsaukšanas parametrus var izmantot arī konstantes. Piemēram, pašreizējā ER datu modeļa kartēšana ietver datu avotu **InvoiceTransactions**, un šis datu avots atgriež ierakstu sarakstu. Ieraksta **InvoiceTransactions** struktūra ietver laukus **AmountDebit** un **AmountCredit**, un šie abi lauki atgriež skaitliskas vērtības. Tāpēc, lai aprēķinātu rēķinā iekļauto sumu, varat izveidot šādu izteiksmi, kas lieto iebūvēto ER noapaļošanas funkciju: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Noformējot ER modeļu kartējumus un ER pārskatus, varat izmantot ER funkcijas no šādām kategorijām:

- [Datuma un laika funkcijas](er-functions-category-datetime.md)
- [Saraksta funkcijas](er-functions-category-list.md)
- [Loģiskas funkcijas](er-functions-category-logical.md)
- [Matemātiskās funkcijas](er-functions-category-mathematical.md)
- [Ieraksta funkcijas](er-functions-category-record.md)
- [Teksta funkcijas](er-functions-category-text.md)
- [Datu apkopošanas funkcijas](er-functions-category-data-collection.md)
- [Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)
- [Tipa pārveidošanas funkcijas](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Funkciju saraksta paplašināšana

ER jums ļauj paplašināt funkciju sarakstu, kuras tiek lietotas ER izteiksmēs. Ir jāveic noteiktas tehniskas darbības. Papildinformāciju skatiet rakstā [Elektronisko pārskatu (EP) veidošanas funkciju saraksta paplašināšana](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Saliktās izteiksmes

Var izveidot saliktas izteiksmes, kas izmanto dažādu kategoriju funkcijas, ar nosacījumu, ka datu tipi sakrīt. Ja izmantojat funkcijas kopā, saskaņojiet vienas funkcijas izvades datu veidu ar ievades datu veidu, kas ir nepieciešams citai funkcijai. Piemēram, lai izvairītos no iespējamas kļūdas "saraksts ir tukšs" lauka saistīšanā ar ER formāta elementu, apvienojiet funkcijas no kategorijas [Saraksts](er-functions-category-list.md) ar funkciju no kategorijas [Loģikas](er-functions-category-logical.md), kā redzams šajā piemērā. Šeit formula izmanto funkciju [IF](er-functions-logical-if.md), lai pārbaudītu, vai saraksts **IntrastatTotals** ir tukšs, pirms tiek atgriezta vajadzīgā apkopojuma vērtība no šī saraksta. Ja saraksts **IntrastatTotals** ir tukšs, formula atgriež **0** (nulle).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Vairāki risinājumi

Bieži vien jūs varat iegūt vienu un to pašu datu transformācijas rezultātu vairākos veidos, izmantojot dažādu kategoriju funkcijas vai dažādas funkcijas no tās pašas kategorijas. Piemēram, iepriekšējo izteiksmi var arī konfigurēt, izmantojot funkciju [COUNT](er-functions-list-count.md) no kategorijas [Saraksts](er-functions-category-list.md) kategorijas.

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Paplašināt elektronisko pārskatu veidošanas funkciju sarakstu](general-electronic-reporting-formulas-list-extension.md)
