---
title: Formulas veidotājs elektronisko pārskatu veidošanā (ER)
description: Šajā tēmā ir paskaidrots, kā elektronisko pārskatu veidošanā (Electronic reporting — ER) lietot formulas veidotāju.
author: NickSelin
manager: kfend
ms.date: 07/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e55ab83302cc75b1a9d9d3e4f06d2258697b31fc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771218"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formulas veidotājs elektronisko pārskatu veidošanā (ER)

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā elektronisko pārskatu veidošanā (Electronic reporting — ER) lietot formulas veidotāju. Kad veidojat formātu noteiktam ER elektroniskajam dokumentam, datu pārveidošanai varat lietot formulas, lai nodrošinātu atbilstību dokumenta izpildes un formatējuma prasībām. Šīs formulas līdzinās formulām programmā Microsoft Excel. Formulās tiek atbalstīti dažādi funkciju tipi — teksta, datuma un laika, matemātiskās, loģiskās, informācijas, datu tipu pārveidošanas un citas (biznesa jomai specifiskas funkcijas).

## <a name="formula-designer-overview"></a>Pārskats par formulas veidotāju

ER atbalsta formulas veidotāju. Tāpēc veidošanas laikā varat konfigurēt izteiksmes, kuras var izmantot tālāk norādīto uzdevumu izpildes laikā.

- To datu pārveidošana, kuri ir saņemti no programmas datu bāzes un ir jāievada ER datu modelī, kas ir paredzēts izmantošanai kā datu avots ER formātiem. (Šie pārveidojumi var iekļaut, piemēram, filtrēšanu, grupēšanu un datu tipa pārveidošanu.)
- Datu formatēšana tādiem datiem, kas ir jāsūta uz ģenerēto elektronisko dokumentu saskaņā ar noteikta ER formāta izkārtojumu un nosacījumiem. (Formatēšanu var veikt, piemēram, saskaņā ar pieprasīto valodu, kultūru vai kodējumu.)
- Elektronisko dokumentu izveides procesa kontrolēšana. (Piemēram, izteiksmes var iespējot vai atspējot noteiktu formāta elementu izvadi atkarībā no datu apstrādes. Tās var arī pārtraukt dokumenta izveides procesu vai sūtīt ziņojumus lietotājiem.)

Lapu **Formulas veidotājs** var atvērt, veicot kādu no tālāk norādītajām darbībām.

- Datu avota elementus saistīt ar datu modeļa komponentiem.
- Datu avota elementus saistīt ar formāta komponentiem.
- Pabeigt uzturēšanu aprēķinātajiem laukiem, kas ir daļa no datu avotiem.
- Definēt redzamības nosacījumus lietotāja ievades parametriem.
- Formatēt formāta transformācijas.
- Definēt formāta komponentu iespējošanas nosacījumus.
- Definēt failu nosaukumus formāta komponentiem FILE.
- Definēt nosacījumus procesa kontroles pārbaudēm.
- Definēt ziņojumu tekstu procesa kontroles pārbaudēm.

## <a name="designing-er-formulas"></a>ER formulu veidošana

### <a name="data-binding"></a>Datu saistīšana

ER formulas veidotāju var izmantot, lai definētu izteiksmi, kas pārveido no datu avotiem saņemtos datus, lai izpildes laikā šos datus varētu ievadīt datu patērētājā.

- No programmas datu avotiem un izpildes laika parametriem uz ER datu modeli
- No ER datu modeļa uz ER formātu
- No programmas datu avotiem un izpildes laika parametriem uz ER formatu

Nākamajā attēlā ir parādīts šī tipa izteiksmes noformējums. Šajā piemērā izteiksme noapaļo tabulas Intrastat lauka **Intrastat.AmountMST** vērtību līdz diviem cipariem aiz komata un pēc tam atgriež noapaļoto vērtību.

[![Datu saistīšana](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Tālāk esošajā attēlā ir parādīts, kā var lietot šī tipa izteiksmi. Šajā piemērā izveidotās izteiksmes rezultāts tiek ievadīts datu modeļa **Nodokļu pārskatu veidošanas modelis** komponentā **Transaction.InvoicedAmount**.

[![Tiek izmantota datu saistīšana](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Izpildes laikā izveidotā formula **ROUND (Intrastat.AmountMST, 2)** katra tabulas Instrastat ieraksta lauka **AmountMST** vērtību noapaļo līdz diviem cipariem aiz komata. Pēc tam tā noapaļoto vērtību ievada datu modeļa **Nodokļu pārskatu veidošana** komponentā **Transaction.InvoicedAmount**.

### <a name="data-formatting"></a>Datu formatēšana

ER formulas veidotāju var izmantot, lai definētu izteiksmi, kas formatē no datu avotiem saņemtos datus, lai šos datus varētu nosūtīt kā daļu no ģenerētā elektroniskā dokumenta. Iespējams, jums ir formatējums, kas jālieto kā tipiska kārtula, kuru nepieciešams atkārtoti izmantot kādam formātam. Šajā gadījumā formāta konfigurācijā šo formatēšanu varat vienu reizi ieviest kā nosauktu pārveidošanu, kurai ir formatēšanas izteiksme. Pēc tam šo nosaukto pārveidošanu var saistīt ar daudziem formāta komponentiem, kuriem ir nepieciešams formatēt izvadi atbilstoši jūsu izveidotajai formatēšanas izteiksmei.

Nākamajā attēlā ir parādīts šī tipa transformēšanas noformējums. Šajā piemērā pārveidošana **TrimmedString** apcērt ienākošos datus ar datu tipu **String**, noņemot sākuma un beigu atstarpes. Pēc tam tā atgriež apcirstu virknes vērtību.

[![Pārveidošana](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Nākamajā attēlā ir parādīts, kā var lietot šī tipa transformēšanu. Šajā piemērā vairāki formāta komponenti izpildes laikā kā izvadi uz ģenerēto elektronisko dokumentu sūta tekstu. Visi šie formāta komponenti atsaucas uz pārveidošanu **TrimmedString** pēc nosaukuma.

[![Tiek izmantota pārveidošana](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kad formāta komponenti, piemēram, iepriekšējā attēlā norādītais komponents **partyName**, atsaucas uz pārveidošanu **TrimmedString**, pārveidošana uz ģenerēto elektronisko dokumentu kā izvadi sūta tekstu. Šis teksts neietver sākuma un beigu atstarpes.

Ja jums ir formatējums, kas ir jālieto atsevišķi, šo formatējumu varat ieviest kā noteikta formāta komponenta saistīšanas atsevišķu izteiksmi. Nākamajā attēlā ir parādīta šī tipa izteiksme. Šajā piemērā formāta komponents **partyType** tiek saistīts ar datu avotu, izmantojot izteiksmi, kas ienākošos datus no lauka **Model.Company.RegistrationType** datu avotā pārveido par tekstu, kurš rakstīts ar lielajiem burtiem. Pēc tam izteiksme šo tekstu kā izvadi sūta uz elektronisko dokumentu.

[![Formatējuma lietošana atsevišķam komponentam](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Apstrādes plūsmas kontrole

ER formulas veidotāju var izmantot, lai definētu izteiksmes, kas kontrolē elektronisko dokumentu ģenerēšanas procesa plūsmu. Jūs varat veikt tālāk norādītos uzdevumus.

- Definējiet nosacījumus, kas nosaka, kad ir jāaptur dokumenta veidošanas process.
- Norādiet izteiksmes, kas izveido ziņojumus lietotājam par apturētiem procesiem vai parāda izpildes žurnāla ziņojumus par pārskata ģenerēšanas procesa turpināšanu.
- Norādiet ģenerēto elektronisko dokumentu failu nosaukumus un kontrolējiet to izveidošanas nosacījumus.

Katrs apstrādes plūsmas kontroles noteikums ir paredzēts kā atsevišķa pārbaude. Nākamajā attēlā ir parādīta šī tipa pārbaude. Šeit ir šajā piemērā lietotās konfigurācijas skaidrojums:

- Pārbaude tiek novērtēta, kad XML faila ģenerēšanas laikā tiek izveidots mezgls **INSTAT**.
- Ja transakciju saraksts ir tukšs, pārbaude aptur izpildes procesu un atgriež uzrakstu **FALSE**.
- Pārbaude atgriež kļūdas ziņojumu, kas ietver etiķetes SYS70894 tekstu lietotāja vēlamajā valodā.

[![Validēšana](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER formulas veidotāju var izmantot arī, lai ģenerētu faila nosaukumu ģenerētajam elektroniskajam dokumentam un kontrolētu faila izveides procesu. Nākamajā attēlā ir parādīts šī tipa procesa plūsmas kontroles noformējums. Šeit ir šajā piemērā lietotās konfigurācijas skaidrojums:

- Ierakstu saraksts no datu avota **model.Intrastat** tiek sadalīts partijās. Katrā no partijām ietverts līdz 1000 ierakstiem.
- Izvade izveido zip failu, kas katrai izveidotajai partijai satur vienu failu XML formātā.
- Izteiksme atgriež faila nosaukumu ģenerētajiem elektroniskajiem dokumentiem, savienojot faila nosaukumu un faila nosaukuma paplašinājumu. Otrajai partijai un visām turpmākajām partijām faila nosaukums kā sufiksu ietver partijas ID.
- Izteiksme iespējo (atgriežot vērtību **TRUE**) faila izveides procesu partijām, kas ietver vismaz vienu ierakstu.

[![Faila vadība](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="documents-content-control"></a>Dokumentu satura kontrole

ER formulu noformētāju var izmantot, lai konfigurētu izteiksmes, kuras kontrolē to, kādi dati tiks ievietoti ģenerētajos elektroniskajos dokumentos izpildlaikā. Izteiksmes var iespējot vai atspējot konkrētu formāta elementu izvadi atkarībā no apstrādes datiem un konfigurētās loģikas. Šo izteiksmi var ievadīt viena formāta elementam cilnes **Kartēšana** laukā **Iespējots** lapā **Operāciju noformētājs** kā loģikas nosacījums, kas atgriež **Būla** vērtību:

-   Ja tiek atgriezta vērtība **Patiess**, pašreizējais formāta elements ir izpildīts.
-   Ja tiek atgriezta vērtība **Nepatiess**, pašreizējais formāta elements ir izlaists.

Šajā ilustrācijā parādītas šāda veida izteiksmes ( **ISO20022 Kredīta pārnese (NO)** formāta konfigurācijas versija **11.12.11**, kuru nodrošina Microsoft, ir piemērs). Formāta komponents **XMLHeader** ir konfigurēts, lai aprakstītu kredīta pārnes ziņojuma struktūru, ievērojot ISO 20022 XML ziņojumu standartus. Formāta komponents **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** ir konfigurēts, lai ģenerētajam ziņojumam pievienotu **Ustrd** XML elementu un ievietotu pārveduma formātu kā šādu XML elementu tekstu:

-   Komponents **PaymentNotes** tiek izmantots, lai izvadītu tekstu no maksājuma piezīmēm.
-   Komponents **DelimitedSequence** izvada ar komatu atdalītus rēķina numurus, kuri tiek izmantoti, lai veiktu doto kredīta pārnesi.

[![Operāciju noformētājs](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Komponenti **PaymentNotes** un **DelimitedSequence** tiek marķēti, izmantojot jautājumzīmi. Tas nozīmē, ka abu komponentu izmantojums ir nosacījuma, pamatojoties uz šādiem kritērijiem:

-   Izteiksme **@.PaymentsNotes<>""**, kas definēta komponentam **PaymentNote**, iespējo populāciju (atgriežot **TRUE**) uz XML elementu **Ustrd**, maksājuma piezīmju tekstu, kad šis teksts dotajam kredīta pārvedumam nav tukšs.

[![Operāciju noformētājs](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)

-   Izteiksme **@.PaymentsNotes=""**, kas definēta komponentam **DelimitedSequence**, iespējo populāciju (atgriežot **TRUE**) uz XML elementu **Ustrd**, atdalīti ar komatu ir tie rēķina skaitļi, kas ir izmantoti, lai veiktu doto kredīta pārvedumu, kad maksājuma piezīmju teksts šim kredīta pārvedumam ir tukšs.

[![Operāciju noformētājs](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)

Pamatojoties uz šo iestatījumu, ģenerētais ziņojums par katru debitora maksājumu — XML elements **Ustrd**— saturēs vai nu maksājuma piezīmju tekstu, vai, ja šis teksts ir tukšs, tekstu, kurā ar komatiem atdalīti rēķina numuri, kas izmantoti, lai veiktu šo maksājumu.

### <a name="basic-syntax"></a>Pamata sintakse

ER izteiksmes var saturēt jebkuru vai visus no šādiem elementiem:

- Konstantes
- Operatori
- Atsauces
- Ceļi
- Funkcijas

#### <a name="constants"></a>Konstantes

Kad veidojat izteiksmes, varat lietot teksta un skaitļu konstantes (t.i., vērtības, kas netiek aprēķinātas). Piemēram, izteiksme **VALUE ("100") + 20** lieto skaitļu konstanti **20** un virknes konstanti **"100"**, un atgriež skaitlisku vērtību **120**. ER formulas veidotājs atbalsta atsoļa sekvences. Tādējādi varat norādīt, kura izteiksmes virkne ir jāapstrādā citādi. Piemēram, izteiksme **"Ļevs Tolstojs ""Karš un miers"" 1. sējums"** atgriež šādu teksta virkni: **Ļevs Tolstojs "Karš un miers" 1. sējums**.

#### <a name="operators"></a>Operatori

Tālāk esošajā tabulā ir parādīti aritmētiskie operatori, ko varat izmantot, lai veiktu pamata matemātiskās darbības, piemēram, saskaitīšanu, atņemšanu, reizināšanu un dalīšanu.

| Operators | Nozīme               | Piemērs |
|----------|-----------------------|---------|
| +        | Saskaitīšana              | 1+2     |
| -        | Atņemšana, negācija | 5-2, -1 |
| \*       | Reizināšana        | 7\*8    |
| /        | Dalīšana              | 9/3     |

Tālāk esošajā tabulā parādīti atbalstītie salīdzināšanas operatori. Šos operatorus varat izmantot, lai salīdzinātu divas vērtības.

| Operators | Nozīme                  | Piemērs    |
|----------|--------------------------|------------|
| =        | Vienāds                    | X=Y        |
| &gt;     | Lielāks nekā             | X&gt;Y     |
| &lt;     | Mazāks nekā                | X&lt;Y     |
| &gt;=    | Lielāks vai vienāds ar | X&gt;=Y    |
| &lt;=    | Mazāks vai vienāds ar    | X&lt;=Y    |
| &lt;&gt; | Nav vienāds ar             | X&lt;&gt;Y |

Turklāt rakstzīmi & varat izmantot kā teksta savienošanas operatoru. Šādi vienu vai vairākas teksta virknes varat savirknēt jeb savienot vienā teksta daļā.

| Operators | Nozīme     | Piemērs                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Savienot | "Nav ko drukāt" & ":&nbsp;" & "nav atrasts neviens ieraksts" |

##### <a name="operator-precedence"></a>Operatoru prioritātes

Ir svarīgi, kādā secībā tiek vērtētas saliktas izteiksmes daļas. Piemēram, izteiksmes **1 + 4 / 2** rezultāts atšķiras atkarībā no tā, vai pirmā tiek izpildīta saskaitīšanas vai dalīšanas operācija. Varat izmantot iekavas, lai skaidri definētu, kā izteiksme tiek novērtēta. Piemēram, lai norādītu, ka vispirms ir jāveic saskaitīšanas operācija, iepriekšējo izteiksmi varat mainīt uz **(1 + 4) / 2**. Ja skaidri nenorādāt operāciju secību izteiksmē, secība ir atkarīga no atbalstītajiem operatoriem piešķirtās noklusējuma prioritātes. Tālāk esošajā tabulā ir parādīta katram operatoram piešķirtā prioritāte. Operatori, kuru prioritāte ir augstāka (piemēram, 7), tiek vērtēti pirms operatoriem, kuriem ir zemāka prioritāte (piemēram, 1).

| Prioritāšu secība | Operatori      | Sintakse                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Grupēšana       | ( … )                                                                   |
| 6          | Piekļuve elementam  | … . …                                                                   |
| 5          | Funkcijas izsaukums  | … ( … )                                                                 |
| 4          | Reizināšana un dalīšana | … \* …<br>… / …                                                         |
| 3          | Saskaitīšana un atņemšana       | … + …<br>… - …                                                          |
| 2          | Salīdzinājums     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Atdalīšana     | … , …                                                                   |

Ja izteiksmē ir vairāki secīgi operatori ar vienādu prioritātes vērtību, šie operatori tiek vērtēti no kreisās uz labo pusi. Piemēram, izteiksme **1 + 6 / 2 \* 3 &gt; 5** atgriež vērtību **patiess**. Ieteicams izmantot iekavas, lai skaidri norādītu vēlamo operāciju secību izteiksmēs, lai izteiksmes būtu vieglāk lasāmas un uzturamas.

#### <a name="references"></a>Atsauces

Visus pašreizējā ER komponenta datu avotus, kas ir pieejami izteiksmes veidošanas laikā, var izmantot kā nosauktas atsauces. (Pašreizējais ER komponents var būt modelis vai formāts.) Piemēram, pašreizējais ER datu modelis ietver datu avotu **ReportingDate**, un šis datu avots atgriež datu tipa **DATETIME** vērtību. Lai pareizi formatētu šo vērtību ģenerēšanas dokumentā, izteiksmē uz datu avotu varat atsaukties šādi: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**.

Pirms visām ar atsauci norādītā datu avota nosaukumā esošajām rakstzīmēm, kas nav alfabēta burti, ir jāievieto vienpēdiņa ('). Ja ar atsauci norādītā datu avota nosaukumā ir vismaz viens simbols, kas nav alfabēta burts, nosaukums ir jāietver vienpēdiņās. (Šie simboli, kas nav alfabēta burti, var būt, piemēram, pieturzīmes vai citi rakstveida simboli.) Tālāk sniegti daži piemēri.

- Uz datu avotu **Today's date & time** ER izteiksmē ir jāatsaucas šādi: **'Today''s date & time'**.
- Uz datu avota **Customers** metodi **name()** ER izteiksmē ir jāatsaucas šādi: **Customers.'name()'**.

Ja programmas datu avotu metodēm ir parametri, šo metožu izsaukšanai tiek izmantota tālāk norādītā sintakse.

- Ja datu avota **System** metodei **isLanguageRTL** ir parametrs **EN-US** ar datu tipu **String**, ER izteiksmē uz šo metodi ir jāatsaucas šādi: **System.'isLanguageRTL'("EN-US")**.
- Pēdiņas nav obligātas, ja metodes nosaukums ietver tikai burtu un ciparu simbolus. Taču tās ir obligātas tabulas metodei, ja nosaukums ietver iekavas.

Kad datu avots **System** tiek pievienots ER kartēšanai, kas atsaucas uz programmas klasi **Global**, izteiksme atgriež Būla vērtību **FALSE**. Modificētā izteiksme **System.' isLanguageRTL'("AR")** atgriež Būla vērtību **TRUE**.

Varat ierobežot veidu, kādā vērtības tiek nodotas šī tipa metodes parametriem.

- Šī tipa metodēm var nodot tikai konstantes. Konstanšu vērtības tiek definētas veidošanas laikā.
- Šī tipa parametriem tiek atbalstīti tikai primitīvi (pamata) datu tipi. (Primitīvie datu tipi ir vesels skaitlis, reāls skaitlis, Būla vērtība, virkne utt.)

#### <a name="paths"></a>Ceļi

Ja izteiksme atsaucas uz kādu strukturētu datu avotu, ceļa definīciju varat izmantot, lai atlasītu konkrētu šī datu avota primitīvo elementu. Punkta rakstzīme (.) tiek lietota, lai atdalītu atsevišķus strukturēta datu avota elementus. Piemēram, pašreizējais ER datu modelis ietver datu avotu **InvoiceTransactions**, un šis datu avots atgriež ierakstu sarakstu. Ieraksta **InvoiceTransactions** struktūra ietver laukus **AmountDebit** un **AmountCredit**, un šie abi lauki atgriež skaitliskas vērtības. Tādējādi varat izveidot šādu izteiksmi, lai aprēķinātu rēķinā iekļauto summu: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Funkcijas

Nākamajā sadaļā ir aprakstītas funkcijas, kuras var izmantot ER izteiksmēs. Visus izteiksmes konteksta datu avotus (pašreizējo ER datu modeli vai ER formātu) var izmantot kā parametrus funkciju izsaukšanai saskaņā ar funkciju izsaukšanas argumentu sarakstu. Kā funkciju izsaukšanas parametrus var izmantot arī konstantes. Piemēram, pašreizējais ER datu modelis ietver datu avotu **InvoiceTransactions**, un šis datu avots atgriež ierakstu sarakstu. Ieraksta **InvoiceTransactions** struktūra ietver laukus **AmountDebit** un **AmountCredit**, un šie abi lauki atgriež skaitliskas vērtības. Tāpēc, lai aprēķinātu rēķinā iekļauto sumu, varat izveidot šādu izteiksmi, kas lieto iebūvēto ER noapaļošanas funkciju: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Atbalstītās funkcijas

Nākamajās tabulās ir aprakstītas datu manipulācijas funkcijas, kuras var izmantot, lai izveidotu ER datu modeļus un ER atskaites. Šis funkciju saraksts nav fiksēts. Izstrādātāji to var pagarināt. Lai redzētu sarakstu ar funkcijām, kuras varat izmantot, atveriet funkciju rūti ER formulas veidotājā.

### <a name="date-and-time-functions"></a>Datuma un laika funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| ADDDAYS (datums un laiks, dienas) | Norādītajai datuma/laika vērtībai pieskaitiet norādīto dienu skaitu. | **ADDDAYS (NOW(), 7)** atgriež datumu un laiku septiņas dienas uz priekšu. |
| DATETODATETIME (datums) | Norādīto datuma vērtību pārveidojiet par datuma/laika vērtību. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** pašreizējās Finance and Operations sesijas datumu, 2015. gada 24. decembri, atgriež izteiktu kā **12/24/2015 12:00:00 AM**. Šajā piemērā **CompInfo** ir ER datu avots ar tipu **Finance and Operations/Table**, un tas atsaucas uz tabulu CompanyInfo. |
| NOW () | Atgriezt pašreizējo programmas servera datumu un laiku kā datuma/laika vērtību. | |
| TODAY () | Atgriezt pašreizējo programmas servera datumu kā datuma vērtību. | |
| NULLDATE () | Atgriezt datuma vērtību **null**. | |
| NULLDATETIME () | Atgriezt datuma/laika vērtību **null**. | |
| DATETIMEFORMAT (datums un laiks, formāts) | Norādīto datuma/laika vērtību pārveidojiet par virkni norādītajā formātā. (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** pašreizējās programmas servera datumu, 2015. gada 24. decembri, atgriež kā **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam. |
| DATETIMEFORMAT (datums un laiks, formāts, kultūra) | Norādīto datuma/laika vērtību pārveidojiet par virkni norādītajā formātā un atbilstoši norādītajai [kultūrai](https://msdn.microsoft.com/goglobal/bb896001.aspx). (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** pašreizējo programmas servera datumu, 2015. gada 24. decembri, atgriež kā **"24.12.2015"** atbilstoši atlasītajai vācu kultūrai. |
| SESSIONTODAY () | Atgriezt pašreizējo programmas sesijas datumu kā datuma vērtību. | |
| SESSIONNOW () | Atgriezt pašreizējo programmas sesijas datumu un laiku kā datuma/laika vērtību. | |
| DATEFORMAT (datums, formāts) | Norādītā datuma virknes attēlojumu atgriezt norādītajā formātā. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** pašreizējās programmas sesijas datumu, 2015. gada 24. decembri, atgriež kā **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam. |
| DATEFORMAT (datums, formāts, kultūra) | Norādīto datuma vērtību pārveidojiet par virkni norādītajā formātā un atbilstoši norādītajai [kultūrai](https://msdn.microsoft.com/goglobal/bb896001.aspx). (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** pašreizējo programmas sesijas datumu, 2015. gada 24. decembri, atgriež kā **"24.12.2015"** atbilstoši atlasītajai vācu kultūrai. |
| DAYOFYEAR (datums) | Atgriezt veselu skaitļu attēlojumu dienu skaitam no 1. janvāra līdz norādītajam datumam. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** atgriež **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** atgriež **1**. |
| DAYS (1. datums, 2. datums) | Atgriezt dienu skaitu starp pirmo norādīto datumu un otro norādīto datumu. Ja pirmais datums ir vēlāks par otro datumu, tiek atgriezta pozitīva vērtība; ja pirmais datums ir vienāds ar otro datumu, tiek atgriezta **0** (nulle); vai tiek atgriezta negatīva vērtība, ja pirmais datums ir agrāks par otro datumu. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** atgriež **-1**. |

### <a name="data-conversion-functions"></a>Datu konvertēšanas funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| DATETODATETIME (datums) | Norādīto datuma vērtību pārveidojiet par datuma/laika vērtību. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** pašreizējās Finance and Operations sesijas datumu, 2015. gada 24. decembri, atgriež izteiktu kā **12/24/2015 12:00:00 AM**. Šajā piemērā **CompInfo** ir ER datu avots ar tipu **Finance and Operations/Table**, un tas atsaucas uz tabulu CompanyInfo. |
| DATEVALUE (virkne, formāts) | Norādītās virknes datuma attēlojumu atgriezt norādītajā formātā. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** atgriež datumu 2016. gada 21. decembris atbilstoši norādītajam pielāgotajam formātam un programmas noklusējuma kultūrai **EN-US**. |
| DATEVALUE (virkne, formāts, kultūra) | Norādītās virknes datuma attēlojumu atgriezt norādītajā formātā un atbilstoši norādītajai kultūrai. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** atgriež datumu 2016. gada 21. janvāris atbilstoši norādītajam pielāgotajam formātam un kultūrai. Taču **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** parāda izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīgs datums. |
| DATETIMEVALUE (virkne, formāts) | Norādītās virknes datuma/laika attēlojumu atgriezt norādītajā formātā. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** atgriež 2016. gada 21. decembra plkst. 2.55.00 atbilstoši norādītajam pielāgotajam formātam un programmas noklusējuma kultūrai **EN-US**. |
| DATETIMEVALUE (virkne, formāts, kultūra) | Norādītās virknes datuma/laika attēlojumu atgriezt norādītajā formātā un atbilstoši norādītajai kultūrai. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** atgriež 2016. gada 21. decembra plkst. 2.55.00 atbilstoši norādītajam pielāgotajam formātam un kultūrai. Taču **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** parāda izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīgs datums/laiks. |

### <a name="list-functions"></a>Saraksta funkcijas

<table>
<thead>
<tr>
<th>Funkcija</th>
<th>Apraksts</th>
<th>Piemērs</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (ievade, garums)</td>
<td>Norādīto ievades virkni sadalīt apakšvirknēs, katrai no kurām ir norādīts garums. Atgriezt rezultātu kā jaunu sarakstu.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> atgriež jaunu sarakstu, kas sastāv no diviem ierakstiem ar tipa <strong>STRING</strong> lauku. Pirmā ieraksta laukā ir teksts <strong>&quot;abc&quot;</strong>, bet otrā ieraksta laukā ir teksts <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr>
<td>SPLIT (ievade, norobežotājs)</td>
<td>Norādīto ievades virkni sadalīt apakšvirknēs, pamatojoties uz norādīto norobežotāju.</td>
<td><strong>SPLIT (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> atgriež jaunu sarakstu, kas sastāv no trīs ierakstiem, kuriem ir lauks <strong>STRING</strong>. Laukam pirmajā ierakstā ir teksts <strong>&quot;X&quot;</strong>, laukam otrajā ierakstā ir teksts &quot;&nbsp;&quot;, un laukam trešajā ierakstā ir teksts <strong>&quot;y&quot;</strong>. Ja norobežotājs ir tukšs, tiek atgriezts jauns saraksts, kas sastāv no viena ieraksta, kurā ir lauks <strong>STRING</strong> ar ievades tekstu. Ja ievade ir tukša, tiek atgriezts jauns tukšs saraksts.
Ja ievade vai norobežotājs nav norādīts (null), tiek parādīts programmas izņēmums.</td>
</tr>
<tr>
<td>SPLITLIST (saraksts, skaits)</td>
<td>Norādīto sarakstu sadalīt partijās, katrā no kurām ir iekļauts norādītais ierakstu skaits. Atgriezt rezultātu kā jaunu partiju sarakstu, kas satur šādus elementus:
<ul>
<li>Partijas kā parasti saraksti (komponents<strong>Value</strong> )</li>
<li>Skaits pašreizējā partijā (komponents<strong>BatchNumber</strong> )</li>
</ul>
</td>
<td>Tālāk esošajā attēlā redzamais datu avots <strong>Lines</strong> tiek izveidots kā ierakstu saraksts, kurš sastāv no trīs ierakstiem. Šis saraksts tiek sadalīts divās partijās — katrā no partijām ir līdz diviem ierakstiem.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Tālāk esošajā attēlā parādīts izveidotā formāta izkārtojums. Šajā formāta izkārtojumā saistījumi ar datu avotu <strong>Lines</strong> tiek izveidoti, lai ģenerētu izvadi XML formātā Šajā izvadē ietverti atsevišķi mezgli katrai partijai un tajā esošajiem ierakstiem.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (1. ieraksts [, 2. ieraksts, …])</td>
<td>Atgriezt jaunu sarakstu, kas tiek izveidots no norādītajiem argumentiem.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> atgriež tukšu ierakstu, kur lauku saraksts satur visus laukus no ierakstu sarakstiem <strong>MainData</strong> un <strong>OtherData</strong>.</td>
</tr>
<tr>
<td>LISTJOIN (1. saraksts, 2. saraksts, …)</td>
<td>Atgriezt savienotu sarakstu, kas tiek izveidots no norādīto argumentu sarakstiem.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> atgriež sešu ierakstu sarakstu, kurā viens datu tipa <strong>STRING</strong> lauks satur atsevišķus burtus.</td>
</tr>
<tr>
<td>ISEMPTY (saraksts)</td>
<td>Atgriezt vērtību <strong>TRUE</strong>, ja norādītajā sarakstā nav neviena elementa. Pretējā gadījumā atgriezt vērtību <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (saraksts)</td>
<td>Atgriezt tukšu sarakstu, šī saraksta struktūrai kā avotu izmantojot norādīto sarakstu.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> atgriež jaunu tukšu sarakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež funkcija <strong>SPLIT</strong>.</td>
</tr>
<tr>
<td>FIRST (saraksts)</td>
<td>Atgriezt pirmo ierakstu no norādītā saraksta, ja šis ieraksts nav tukšs. Pretējā gadījumā parādīt izņēmumu.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (saraksts)</td>
<td>Atgriezt pirmo ierakstu no norādītā saraksta, ja šis ieraksts nav tukšs. Pretējā gadījumā atgriezt ierakstu <strong>null</strong>.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (saraksts)</td>
<td>Atgriezt sarakstu, kas satur tikai pirmo norādītā saraksta elementu.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (ceļš)</td>
<td>Šī funkcija darbojas kā atmiņā esoša atlase. Tā atgriež jaunu izplātu sarakstu, kas atspoguļo visus elementus, kuri atbilst norādītajam ceļam. Šis ceļš ir jādefinē kā derīgs datu avota ceļš datu avota elementam ar ierakstu saraksta datu tipu. Tādiem datu elementiem kā ceļa virkne un datums ER izteiksmju veidotājā veidošanas laikā ir jāizraisa kļūda.</td>
<td>Ja kā satura avotu (DS) ievadāt <strong>SPLIT(&quot;abcdef&quot; , 2)</strong>, funkcija <strong>COUNT( ALLITEMS (DS.Value))</strong> atgriež vērtību <strong>3</strong>.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (ceļš)</td>
<td>Šī funkcija darbojas kā apvienots SQL vaicājums. Tā atgriež jaunu izplātu sarakstu, kas atspoguļo visus elementus, kuri atbilst norādītajam ceļam. Norādītajam ceļam ir jābūt definētam kā derīgam datu avota ceļam datu avota elementam ar ierakstu saraksta datu tipu, un tajā ir jābūt vismaz vienām attiecībām. Tādiem datu elementiem kā ceļa virkne un datums ER izteiksmju veidotājā veidošanas laikā ir jāizraisa kļūda.</td>
<td>Savā modeļa kartēšanā definējiet tālāk norādītos datu avotus.
<ul>
<li><strong>CustInv</strong> (tips<strong>Tabulas ieraksti</strong> ), kas atsaucas uz tabulu CustInvoiceTable</li> 
<li><strong>FilteredInv</strong> (tips<strong>Aprēķinātais lauks</strong> ), kurā ir izteiksme <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong></li>
<li><strong>JourLines</strong> (tips<strong>Aprēķinātais lauks</strong> ), kurā ir izteiksme <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong></li>
</ul>
<p>Kad palaižat sava modeļa kartēšanu, lai izsauktu datu avotu <strong>JourLines</strong>, tiek izpildīts tālāk norādītais SQL priekšraksts.</p>
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3 WHERE...
</td>
</tr>
<tr>
<td>ORDERBY (saraksts [, 1. izteiksme, 2. izteiksme, …])</td>
<td>Atgriezt norādīto sarakstu, kas ir sakārtots atbilstoši norādītajiem argumentiem. Šos argumentus var definēt kā izteiksmes.</td>
<td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, <strong>ORDERBY (Vendors, Vendors.'name()')</strong> atgriež sarakstu ar kreditoriem, kuri ir sakārtoti augošā secībā pēc nosaukuma.</td>
</tr>
<tr>
<td>REVERSE (saraksts)</td>
<td>Atgriezt norādīto sarakstu apgrieztā kārtošanas secībā.</td>
<td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> atgriež sarakstu ar kreditoriem, kuri ir sakārtoti dilstošā secībā pēc nosaukuma.</td>
</tr>
<tr>
<td>WHERE (saraksts, nosacījums)</td>
<td>Atgriezt norādīto sarakstu, kas ir filtrēts atbilstoši norādītajam nosacījumam. Norādītais nosacījums tiek lietots attiecībā uz atmiņā esošu sarakstu. Šādi funkcija <strong>WHERE</strong> atšķiras no funkcijas <strong>FILTER</strong>.</td>
<td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu.</td>
</tr>
<tr>
<td>ENUMERATE (saraksts)</td>
<td>Atgriezt jaunu sarakstu, kas sastāv no norādītā saraksta uzskaitījuma ierakstiem un parāda šādus elementus:
<ul>
<li>Norādītā saraksta ieraksti kā parasti saraksti (komponents<strong>Value</strong> )</li>
<li>Pašreizējā ieraksta indekss (komponents<strong>Number</strong> )</li>
</ul>
</td>
<td>Tālāk esošajā attēlā datu avots <strong>Enumerated</strong> tiek izveidots kā uzskaitījuma kreditoru ierakstu saraksts no datu avota <strong>Vendors</strong>, kas atsaucas uz tabulu VendTable.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Tālāk esošajā attēlā ir parādīts formāts. Šajā formātā tiek izveidoti saistījumi, lai ģenerētu izvadi XML formātā Šajā izvadē atsevišķi kreditori attēloti kā uzskaitījuma mezgli.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (saraksts)</td>
<td>Atgriezt ierakstu skaitu norādītajā sarakstā, ja šis saraksts nav tukšs. Pretējā gadījumā atgriezt vērtību <strong>0</strong> (nulle).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> atgriež vērtību <strong>2</strong>, jo funkcija <strong>SPLIT</strong> izveido sarakstu, kas sastāv no diviem ierakstiem.</td>
</tr>
<tr>
<td>LISTOFFIELDS (ceļš)</td>
<td>Atgriezt ierakstu sarakstu, kas izveidots no argumenta ar vienu no tālāk uzskaitītajiem tipiem.
<ul>
<li>Modeļa uzskaitījums</li>
<li>Formāta uzskaitījums</li>
<li>Konteiners</li>
</ul>
<p>Izveidotajā sarakstā ietverti ieraksti ar tālāk norādītajiem laukiem.</p>
<ul>
<li>Nosaukums</li>
<li>Etiķete</li>
<li>Apraksts</li>
</ul>
Izpildes laikā lauki <strong>Etiķete</strong> un <strong>Apraksts</strong> atgriež vērtības atbilstoši formāta valodas iestatījumiem.
</td>
<td>Tālāk esošajā attēlā ir parādīts datu modelī ieviests uzskaitījums.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.</p>
<ul>
<li>Modeļu uzskaitījums ir ievietots pārskatā kā datu avots.</li>
<li>ER izteiksme modeļu uzskaitījumu izmanto kā funkcijas <strong>LISTOFFIELDS</strong> parametru.</li>
<li>Ierakstu saraksta tipa datu avots tiek ievietots pārskatā, izmantojot izveidoto ER izteiksmi.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Tālāk esošajā piemērā parādīti ER formāta elementi, kas ir piesaistīti datu avotam ar ierakstu saraksta tipu, kas tika izveidots, izmantojot funkciju <strong>LISTOFFIELDS</strong>.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Atbilstoši formāta vecākelementu FILE un FOLDER valodas iestatījumiem etiķešu un aprakstu tulkotais teksts tiek ievadīts ER formāta izvadē.</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (ceļš, valoda)</td>
<td>Atgriezt ierakstu sarakstu, kas izveidots no argumenta, piemēram, modeļu uzskaitījuma, formātu uzskaitījuma vai konteinera. Izveidotajā sarakstā ietverti ieraksti ar tālāk norādītajiem laukiem.
<ul>
<li>Nosaukums</li>
<li>Etiķete</li>
<li>Apraksts</li>
<li>Tulkots</li>
</ul>
Izpildes laikā lauki <strong>Etiķete</strong> un <strong>Apraksts</strong> atgriež vērtības atbilstoši formāta valodas iestatījumiem un norādītajai valodai. Lauks <strong>Tulkots</strong> norāda, ka lauks <strong>Etiķete</strong> ir iztulkots norādītajā valodā.
</td>
<td>Piemēram, varat izmantot datu avota tipu <strong>Aprēķinātais lauks</strong>, lai konfigurētu datu modeļu uzskaitījuma <strong>enumType</strong> datu avotus <strong>enumType_de</strong> un <strong>enumType_deCH</strong>.
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>Šajā gadījumā varat izmantot tālāk norādīto izteiksmi, lai iegūtu uzskaitījuma vērtības etiķeti Šveices vācu valodā, ja šāds tulkojums ir pieejams. Ja Šveices vācu valodas tulkojums nav pieejams, etiķete ir Vācu.</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (saraksts, lauka nosaukums, norobežotājs)</td>
<td>Atgriezt virkni, kas sastāv no norādītā saraksta norādītā lauka savirknētajām vērtībām. Vērtības tiek atdalītas ar norādīto norobežotāju.</td>
<td>Ja kā datu avotu (Data Source — DS) ievadāt <strong>SPLIT(&quot;abc&quot; , 1)</strong>, funkcija <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> atgriež <strong>&quot;a-b-c&quot;</strong>.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (saraksts, robežvērtība, ierobežojumu avots)</td>
<td>Norādīto sarakstu sadalīt jaunā apakšsarakstu sarakstā un atgriezt rezultātu ierakstu saraksta saturā. Parametrs <strong>robežvērtība</strong> definē ierobežojuma vērtību sākotnējā saraksta sadalīšanai. Parametrs <strong>ierobežojuma avots</strong> definē soli, par kādu kopsumma tiek palielināta. Ierobežojums netiek lietots atsevišķam vienumam attiecīgajā sarakstā, ja ierobežojuma avots pārsniedz definēto ierobežojumu.</td>
<td>Nākamajā attēlā ir parādīts kāds formāts. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>Nākamajā attēlā ir parādīti datu avoti, kas tiek izmantoti šim formātam.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc formāta palaišanas. Šajā gadījumā izvade ir nekārtots preču saraksts.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>Nākamajos attēlos tas pats formāts ir pielāgots tā, lai preču sarakstu rādītu pa partijām, vienā partijā ietverot preces un nepārsniedzot kopējā svara ierobežojumu 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc pielāgotā formāta palaišanas.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] Ierobežojums netiek lietots pēdējam sākotnējā saraksta vienumam, jo ierobežojuma avota (svara) vērtība (11) pārsniedz noteikto ierobežojumu (9). Lai pārskata ģenerēšanas laikā ignorētu (izlaistu) apakšsarakstus (ja nepieciešams), izmantojiet funkciju <strong>WHERE</strong> vai atbilstošā formāta elementa izteiksmi <strong>Enabled</strong>.</blockquote>
</td>
</tr>
<tr>
<td>FILTER (saraksts, nosacījums)</td>
<td>Atgriezt norādīto sarakstu, kad vaicājums ir modificēts filtrēšanai atbilstoši norādītajam nosacījumam. Šī funkcija atšķiras no funkcijas <strong>WHERE</strong>, jo norādītais nosacījums tiek lietots datu bāzes līmenī visiem ER datu avotiem ar tipu <strong>Tabulas ieraksti</strong>. Sarakstu un nosacījumu var definēt, izmantojot tabulas un relācijas.</td>
<td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, <strong>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu. Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, un ja parametrs <strong>parmVendorBankGroup</strong> ir konfigurēts kā ER datu avots, kurš atgriež vērtību ar datu tipu <strong>String</strong>, funkcija <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> atgriež sarakstu, kurā ir tikai to kreditoru konti, kas pieder noteiktai banku grupai.</td>
</tr>
<tr>
<td>INDEX (saraksts, indekss)</td>
<td>Šī funkcija atgriež ierakstu, ko sarakstā atlasa noteikts skaitliskais indekss. Tiek parādīts izņēmums, ja indekss neietilpst sarakstā esošo ierakstu diapazonā.</td>
<td>Ja ievadāt datu avotu <strong>DS</strong> tipam <strong>Aprēķinātais lauks</strong> un tajā ir izteiksme <strong>SPLIT ("A|B|C", “|”), 2</strong>, izteiksme <strong>DS.Value</strong> atgriež teksta vērtību “B”. Arī izteiksme <strong>INDEX (SPLIT ("A|B|C", “|”), 2).Value</strong> atgriež “B” teksta vērtību.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loģiskas funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| CASE (izteiksme, 1. opcija, 1. rezultāts \[, 2. opcija, 2. rezultāts\] … \[, noklusējuma rezultāts\]) | Norādītās izteiksmes vērtību novērtēt pret norādītajām alternatīvajām opcijām. Atgriezt tās opcijas rezultātu, kas ir vienāda ar izteiksmes vērtību. Pretējā gadījumā atgriezt pēc izvēles ievadīto noklusējuma rezultātu, ja noklusējuma rezultāts ir norādīts. (Noklusējuma rezultāts ir pēdējais parametrs, kura priekšā neatrodas opcija.) | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** atgriež virkni **"WINTER"**, ja pašreizējās prorgammas sesijas datums ir diapazonā no oktobra līdz decembrim. Pretējā gadījumā šī izteiksme atgriež tukšu virkni. |
| IF (nosacījums, 1. vērtība, 2. vērtība) | Atgriezt pirmo norādīto vērtību, ja norādītais nosacījums tiek izpildīts. Pretējā atgriezt otro norādīto vērtību. Ja 1. vērtība un 2. vērtība ir ieraksti vai ierakstu saraksti, rezultātā ir ietverti tikai tie lauki, kas ir iekļauti abos sarakstos. | **IF (1=2, "nosacījums tiek izpildīts", "nosacījums netiek izpildīts")** atgriež virkni **"nosacījums netiek izpildīts"**. |
| NOT (nosacījums) | Atgriezt norādītā nosacījuma pretējo loģisko vērtību. | **NOT (TRUE)** atgriež **FALSE**. |
| AND (1. nosacījums\[, 2. nosacījums, …\]) | Atgriež **TRUE**, ja *visi* norādītie nosacījumi ir patiesi. Pretējā gadījumā atgriezt vērtību **FALSE**. | **AND (1=1, "a"="a")** atgriež **TRUE**. **AND (1=2, "a"="a")** atgriež **FALSE**. |
| OR (1. nosacījums\[, 2. nosacījums, …\]) | Atgriež **FALSE**, ja *visi* norādītie nosacījumi ir aplami. Atgriež **TRUE**, ja *kāds* no norādītajiem nosacījumiem ir patiess. | **OR (1=2, "a"="a")** atgriež **TRUE**. |
| VALUEIN (ievade, saraksts, saraksta elementu izteiksme) | Noteikt, vai norādītā ievade atbilst kāda norādītā saraksta elementa vērtībai. Atgriež **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes izpildes rezultātam attiecībā uz vismaz vienu ierakstu. Pretējā gadījumā atgriezt vērtību **FALSE**. Parametrs **ievade** apzīmē datu avota elementa ceļu. Šī elementa vērtībai tiks noteikta atbilstība. Parametrs **saraksts** apzīmē datu avota elementa ceļu ierakstu saraksta tipam kā sarakstam ar ierakstiem, kuros ir kāda izteiksme. Šī elementa vērtība tiks salīdzināta ar norādīto ievadi. Arguments **saraksta elementu izteiksme** apzīmē izteiksmi, kas norāda uz vai satur vienu norādītā saraksta lauku, kurš ir jāizmanto atbilstības noteikšanai. | Piemērus skatiet nākamajā sadaļā [Piemēri: VALUEIN (ievade, saraksts, saraksta elementu izteiksme)](#examples-valuein-input-list-list-item-expression). |

#### <a name="examples-valuein-input-list-list-item-expression"></a>Piemēri: VALUEIN (ievade, saraksts, saraksta elementu izteiksme)
Parasti funkcija **VALUEIN** tiek tulkota uz **OR** nosacījumu kopu:

(input = list.item1.value) OR (input = list.item2.value) OR …

##### <a name="example-1"></a>1. piemērs
Savā modeļu kartējumā jūs definējat šādus datu avotus: **Saraksts** (ar tipu**Aprēķinātais lauks** ). Šajā datu avotā ir izteiksme **SPLIT ("a,b,c", ",")**.

Kad tiek izsaukts datu avots, kas ir konfigurēts kā izteiksme **VALUEIN ("B", List, List.Value)**, tas atgriež **TRUE**. Šajā gadījumā funkcija **VALUEIN** tiek tulkota uz šādu nosacījumu kopu:

**(("B" = "a") or ("B" = "b") or ("B" = "c"))**, where **("B" = "b")** is equal to **TRUE**

Kad tiek izsaukts datu avots, kas ir konfigurēts kā izteiksme **VALUEIN ("B", List, LEFT(List.Value, 0))**, tas atgriež **FALSE**. Šajā gadījumā funkcija **VALUEIN** tiek tulkota uz šādu nosacījumu:

**("B" = "")**, which isn't equal to **TRUE**

Ņemiet vērā, ka šāda nosacījuma tekstā rakstzīmju skaita augšējā robeža ir 32 768 rakstzīmes. Tādēļ nevajadzētu veidot datu avotus, kas izpildlaikā varētu pārsniegt šo ierobežojumu. Ja ierobežojums tiek pārsniegts, programmas darbība tiek pārtraukta un tiek parādīts izņēmums. Piemēram, šāda situācija var rasties, ja datu avots ir konfigurēts kā **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)** un sarakstā **List1** un **List2** ir daudz ierakstu.

Noteiktos gadījumos funkcija **VALUEIN** tiek tulkota uz datu bāzes priekšrakstu, izmantojot operatoru **EXISTS JOIN**. Šāda uzvedība it spēkā, kad tiek izmantota funkcija **FILTER** un tiek ievēroti šādi nosacījumi:

- Opcija **ASK FOR QUERY** ir izslēgta funkcijas **VALUEIN** datu avotam tādai funkcijai, kas atsaucas uz ierakstu sarakstu. (Šim datu avotam izpildlaikā netiks lietoti nekādi papildu nosacījumi.)
- Funkcijas **VALUEIN** datu avotam tādai funkcijai, kas atsaucas uz ierakstu sarakstu, nav konfigurētas ligzdotās izteiksmes.
- Funkcijas **VALUEIN** saraksta elements atsaucas uz kādu norādītā datu avota lauku (nevis izteiksmi vai metodi).

Apsveriet iespēju izmantot šo opciju, nevis funkciju **WHERE**, kā iepriekš aprakstīts šajā piemērā.

##### <a name="example-2"></a>2. piemērs

Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.

- **In** (tips**Tabulas ieraksti** ), kas atsaucas uz Intrastat tabulu
- **Port** (tips**Tabulas ieraksti** ), kas atsaucas uz IntrastatPort tabulu

Kad tiek izsaukts datu avots, kas ir konfigurēts kā izteiksme **FILTER (In, VALUEIN(In.Port, Port, Port.PortId)**, tiek ģenerēts šāds SQL priekšraksts, lai atgrieztu filtrētos ierakstus Intrastat tabulā:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Laukiem **dataAreaId** gala SQL priekšraksts tiek ģenerēts, izmantojot operatoru **IN**.

##### <a name="example-3"></a>3. piemērs

Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.

- **Le** (tips**Aprēķinātais lauks** ), kurā ir izteiksme **SPLIT ("DEMF,GBSI,USMF", ",")**
- **In** (tips**Tabulas ieraksti** ), kas atsaucas uz Intrastat tabulu un kam ir ieslēgta **Starpuzņēmumu** opcija

Kad tiek izsaukts datu avots, kas ir konfigurēts kā izteiksme **FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)**, gala SQL priekšrakstā ir šāds nosacījums:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>Matemātiskās funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| ABS (skaitlis) | Atgriezt norādītā skaitļa absolūto vērtību. (Tas ir, atgriezt skaitli bez tā zīmes.) | **ABS (-1)** atgriež **1**. |
| POWER (skaitlis, pakāpe) | Atgriezt rezultātu norādītā pozitīvā skaitļa kāpināšanai norādītajā pakāpē. | **POWER (10, 2)** atgriež **100**. |
| NUMBERVALUE (virkne, decimāldaļu atdalītājs, ciparu grupēšanas atdalītājs) | Norādīto virkni pārveidot par skaitli. Norādītais decimāldaļu atdalītājs tiek lietots starp decimāldaļskaitļa veselo skaitli un daļskaitļiem. Norādītais ciparu grupēšanas atdalītājs tiek izmantots kā tūkstošu atdalītājs. | **NUMBERVALUE("1 234,56", ",", " ")** atgriež vērtību **1234.56**. |
| VALUE (virkne) | Norādīto virkni pārveidot par skaitli. Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme. Parādiet izņēmumu, ja norādītajā virknē ir ietvertas citas rakstzīmes, kas nav skaitļi. | **VALUE ("1 234,56")** parāda izņēmumu. |
| ROUND (skaitlis, cipari aiz komata) | Atgriezt norādīto skaitli, kas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.<ul><li>Ja parametra **cipari aiz komata** vērtība ir lielāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz attiecīgajam ciparu skaitam aiz komata.</li><li>Ja parametra **cipari aiz komata** vērtība ir **0** (nulle), norādītais skaitlis tiek noapaļots līdz tuvākajam veselajam skaitlim.</li><li>Ja parametra **cipari aiz komata** vērtība ir mazāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz skaitlim, kas atrodas pa kreisi no komata.</li></ul> | **ROUND (1200.767, 2)** noapaļo līdz diviem cipariem aiz komata un atgriež **1200.77**. **ROUND (1200.767, -3)** noapaļo līdz tuvākajam 1,000 reizinājumam un atgriež **1000**. |
| ROUNDDOWN (skaitlis, cipari aiz komata) | Atgriezt norādīto skaitli, kas ir noapaļots uz leju līdz norādītajam ciparu skaitam aiz komata.<blockquote>[!NOTE] Šī funkcija darbojas līdzīgi funkcijai **ROUND**, bet norādīto skaitli tā vienmēr noapaļo uz leju (nulles virzienā).</blockquote> | **ROUNDDOWN (1200.767, 2)** noapaļo uz leju līdz diviem cipariem aiz komata un atgriež **1200.76**. **ROUNDDOWN (1700.767, -3)** noapaļo uz leju līdz tuvākajam 1,000 reizinājumam un atgriež **1000**. |
| ROUNDUP (skaitlis, cipari aiz komata) | Atgriezt norādīto skaitli, kas ir noapaļots uz augšu līdz norādītajam ciparu skaitam aiz komata.<blockquote>[!NOTE] Šī funkcija darbojas līdzīgi funkcijai **ROUND**, bet norādīto skaitli tā vienmēr noapaļo uz augšu (prom no nulles).</blockquote> | **ROUNDUP (1200.763, 2)** noapaļo uz augšu līdz diviem cipariem aiz komata un atgriež **1200.77**. **ROUNDUP (1200.767, -3)** noapaļo uz augšu līdz tuvākajam 1,000 reizinājumam un atgriež **2000**. |

### <a name="data-conversion-functions"></a>Datu konvertēšanas funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| VALUE (virkne) | Norādīto virkni pārveidot par skaitli. Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme. Parādiet izņēmumu, ja norādītajā virknē ir ietvertas citas rakstzīmes, kas nav skaitļi. | **VALUE ("1 234,56")** parāda izņēmumu. |
| NUMBERVALUE (virkne, decimāldaļu atdalītājs, ciparu grupēšanas atdalītājs) | Norādīto virkni pārveidot par skaitli. Norādītais decimāldaļu atdalītājs tiek lietots starp decimāldaļskaitļa veselo skaitli un daļskaitļiem. Norādītais ciparu grupēšanas atdalītājs tiek izmantots kā tūkstošu atdalītājs. | **NUMBERVALUE("1 234,56", ",", " ")** atgriež **1234.56**. |
| INTVALUE (virkne) | Atgriezt veselu skaitļu attēlojumu norādītajai virknei. Tiek aprautas visas decimāldaļas. | **INTVALUE ("100.77")** atgriež **100**. |
| INTVALUE (skaitlis) | Atgriezt veselu skaitļu attēlojumu norādītajam skaitlim. Tiek aprautas visas decimāldaļas. | **INTVALUE (-100.77)** atgriež **-100**. |
| INT64VALUE (virkne) | Atgriezt int64 attēlojumu norādītajai virknei. Tiek aprautas visas decimāldaļas. | **INT64VALUE ("22565422744")** atgriež **22565422744**. |
| INT64VALUE (skaitlis) | Atgriezt int64 attēlojumu norādītajam skaitlim. Tiek aprautas visas decimāldaļas. | **INT64VALUE (22565422744.00)** atgriež **22565422744**. |

### <a name="record-functions"></a>Ieraksta funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| NULLCONTAINER (saraksts) | Atgriezt ierakstu **null**, kam ir tāda pati struktūra kā norādītajam ierakstu sarakstam vai ierakstam.<blockquote>[!NOTE] Šī funkcija ir novecojusi. Tās vietā lietojiet **EMPTYRECORD**.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** atgriež jaunu tukšu ierakstu, kam ir tāda pati struktūra kā sarakstam, ko atgrieza funkcija **SPLIT**. |
| EMPTYRECORD (ieraksts) | Atgriezt ierakstu **null**, kam ir tāda pati struktūra kā norādītajam ierakstu sarakstam vai ierakstam.<blockquote>[!NOTE] Ieraksts **null** ir ieraksts, kurā visos laukos ir tukšas vērtības. Tukša vērtība skaitļiem ir **0** (nulle), virknēm tā ir tukša virkne utt.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** atgriež jaunu tukšu ierakstu, kam ir tāda pati struktūra kā sarakstam, ko atgrieza funkcija **SPLIT**. |

### <a name="text-functions"></a>Teksta funkcijas

<table>
<thead>
<tr>
<th>Funkcija</th>
<th>Apraksts</th>
<th>Piemērs</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (virkne)</td>
<td>Atgriezt norādīto virkni, kas ir pārveidota par lielajiem burtiem.</td>
<td><strong>UPPER(&quot;Piemērs&quot;)</strong> atgriež <strong>&quot;PIEMĒRS&quot;</strong>.</td>
</tr>
<tr>
<td>LOWER (virkne)</td>
<td>Atgriezt norādīto virkni, kas ir pārveidota par mazajiem burtiem.</td>
<td><strong>LOWER (&quot;Piemērs&quot;)</strong> atgriež <strong>&quot;piemērs&quot;</strong>.</td>
</tr>
<tr>
<td>LEFT (virkne, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes sākuma.</td>
<td><strong>LEFT (&quot;Piemērs&quot;, 3)</strong> atgriež <strong>&quot;Pie&quot;</strong>.</td>
</tr>
<tr>
<td>RIGHT (virkne, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes beigām.</td>
<td><strong>RIGHT (&quot;Piemērs&quot;, 3)</strong> atgriež <strong>&quot;ērs&quot;</strong>.</td>
</tr>
<tr>
<td>MID (virkne, sākuma pozīcija, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes, sākot norādītajā pozīcijā.</td>
<td><strong>MID (&quot;Piemērs&quot;, 2, 3)</strong> atgriež <strong>&quot;mēr&quot;</strong>.</td>
</tr>
<tr>
<td>LEN (virkne)</td>
<td>Atgriezt norādītajā virknē esošo rakstzīmju skaitu.</td>
<td><strong>LEN (&quot;Piemērs&quot;)</strong> atgriež <strong>6</strong>.</td>
</tr>
<tr>
<td>CHAR (skaitlis)</td>
<td>Atgriezt rakstzīmju virkni, uz ko atsaucas norādītais unikoda skaitlis.</td>
<td><strong>CHAR (255)</strong> atgriež <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE] Šīs funkcijas atgrieztā virkne ir atkarīga kodējuma, kas ir atlasīts vecākelementa formāta elementā FILE. Atbalstīto kodējumu sarakstu skatiet tēmā <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodējuma klase</a>.</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (1. virkne [, 2. virkne, …])</td>
<td>Atgriezt visas norādītās teksta virknes, kas ir savienotas vienā virknē.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> atgriež <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE] Arī izteiksme <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> atgriež <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (virkne, raksts, aizstājējs)</td>
<td>Atgriezt norādīto virkni, kurā visi norādītajā raksta virknē esošie rakstzīmju gadījumi ir aizstāti ar rakstzīmēm, kas atrodas norādītās aizstāšanas virknes atbilstošajā pozīcijā.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> aizstāj burtus <strong>&quot;cd&quot;</strong> ar virkni <strong>&quot;GH&quot;</strong> un atgriež <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>REPLACE (virkne, raksts, aizstājējs, regulāras izteiksmes karodziņš)</td>
<td>Ja norādītais parametrs <strong>regulāras izteiksmes karodziņš</strong> ir <strong>true</strong>, atgriezt norādīto virkni pēc tās modificēšanas, šai funkcijai kā argumentu <strong>raksts</strong> lietojot norādīto regulāro izteiksmi. Šī izteiksme tiek izmantota, lai atrastu rakstzīmes, kas ir jāaizstāj. Norādītā argumenta <strong>aizstājējs</strong> rakstzīmes tiek izmantotas, lai aizstātu atrastās rakstzīmes. Ja norādītā parametra <strong>regulārās izteiksmes karodziņš</strong> ir <strong>false</strong>, šī funkcija uzvedas kā funkcija <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> lieto regulāru izteiksmi, kas noņem visus simbolus, kuri nav skaitļi, un atgriež <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> aizstāj burtus <strong>&quot;cd&quot;</strong> ar virkni <strong>&quot;GH&quot;</strong> un atgriež <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>TEXT (ievade)</td>
<td>Atgriezt norādīto ievadi, kas ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās prorgammas instances servera lokalizācijas iestatījumiem. Vērtībām ar tipu <strong>real</strong> šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.</td>
<td>Ja Finance and Operations instances servera lokalizācija ir definēta kā <strong>EN-US</strong>, funkcija <strong>TEXT (NOW ())</strong> pašreizējo prorgammas sesijas datumu, 2015. gada 17. decembri, atgriež kā teksta virkni <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> atgriež <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr>
<td>FORMAT (1. virkne, 2. virkne[, 3. virkne, …])</td>
<td>Atgrieziet norādīto virkni, kas ir formatēta, aizstājot argumentu <strong>%N</strong> ar argumentu <em>n</em>. Argumenti ir virknes. Ja nav norādīts parametra arguments, šis parametrs virknē tiek atgriezts kā <strong>&quot;%N&quot;</strong>. Vērtībām ar tipu <strong>real</strong> šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.</td>
<td>Tālāk esošajā attēlā redzamais datu avots <strong>PaymentModel</strong> atgriež sarakstu ar debitoru ierakstiem, izmantojot komponentu <strong>Customer</strong>, un apstrādāšanas datuma vērtību, izmantojot lauku <strong>ProcessingDate</strong>.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>ER formātā, kas ir izveidots tā, lai ģenerētu elektronisku failu noteiktiem debitoriem, vienums <strong>PaymentModel</strong> ir atlasīts kā datu avots, un tas kontrolē procesa plūsmu. Lietotājiem tiek parādīts izņēmums, lai viņus informētu par to, kad atlasītais debitors tiek apturēts datumam, kad atskaite tiek apstrādāta. Šāda tipa apstrādes kontrolei izveidotā formulā var izmantot šādus resursus:</p>
<ul>
<li>Etiķete SYS70894, kurā ir šāds teksts:
<ul>
<li><strong>Valodai EN-US:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Valodai DE:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Etiķete SYS18389, kurā ir šāds teksts:
<ul>
<li><strong>Valodai EN-US:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>Valodai DE:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Lūk, kādu formulu varat izveidot:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Ja pārskats debitoram <strong>Litware Retail</strong> tiek apstrādāts 2015. gada 17. decembrī kultūrā <strong>EN-US</strong> un valodā <strong>EN-US</strong>, šī formula atgriež tālāk norādīto tekstu, kurš lietotājam var tikt rādīts kā izņēmuma ziņojums.</p>
<p>&quot;Nothing to print. Customer Litware Retail is stopped for 12/17/2015.&quot;</p>
<p>Ja tas pats pārskats debitoram <strong>Litware Retail</strong> tiek apstrādāts 2015. gada 17. decembrī kultūrā <strong>DE</strong> un valodā <strong>DE</strong>, šī formula atgriež tālāk norādīto tekstu, kurā tiek izmantots cits datuma formāts.</p>
<p>&quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE] ER formulās etiķetēm tiek lietota tālāk norādītā sintakse.
<ul>
<li><strong>Etiķetēm no Finance and Operations programmu resursiem:</strong> <strong>@&quot;X&quot;</strong>, kur <strong>X</strong> ir etiķetes ID programmas objektu kokā (AOT)</li>
<li><strong>Etiķetēm, kas ir ietvertas ER konfigurācijās:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, kur <strong>X</strong> ir etiķetes ID ER konfigurācijā</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (skaitlis, formāts)</td>
<td>Atgriezt norādītā skaitļa virknes attēlojumu norādītajā formātā. (Informāciju par atbalstītajiem formātiem skatiet šeit: <a href="https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx">standarta</a> un <a href="https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx">pielāgotie</a>.) Formāta numuriem izmantotā kultūra ir atkarīga no šīs funkcijas izpildes konteksta.</td>
<td>Kultūrai EN-US <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> atgriež <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> atgriež <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr>
<td>NUMBERFORMAT (skaitlis, formāts, kultūra)</td>
<td>Norādītā skaitļa virknes attēlojumu atgriezt norādītajā formātā un atbilstoši norādītajai kultūrai. (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās <a href="https://docs.microsoft.com/dotnet/standard/base-types/standard-numeric-format-strings">standarta</a> un <a href="https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings">pielāgots</a>.)</td>
<td><strong>NUMBERFORMAT (10/3, “F2”, “de”)</strong> atgriež <strong>3,33</strong>, savukārt <strong>NUMBERFORMAT (10/3, “F2”, “en-us”)</strong> atgriež <strong>3,33</strong>.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (skaitlis, valoda, valūta, drukas valūtas nosaukuma karogs, cipari aiz komata)</td>
<td>Atgriezt norādīto skaitli pēc tam, kad tas ir izteikts vārdos (konvertēts par teksta virknēm) norādītajā valodā. Valodas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek izmantots izpildes konteksta valodas kods. (Valodas kods izpildes kontekstam tiek definēts ģenerēšanas mapei vai failam.) Arī valūtas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek izmantota uzņēmuma valūta.
<blockquote>[!NOTE] Parametri <strong>drukas valūtas nosaukuma karogs</strong> un <strong>cipari aiz komata</strong> tiek analizēti tikai šādiem valodu kodiem: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> un <strong>RU</strong>. Turklāt parametrs <strong>drukas valūtas nosaukuma karogs</strong> tiek analizēts tikai tiem uzņēmumiem, kuru valsts vai reģiona konteksts atbalsta valūtu nosaukumu locījumus.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> atgriež <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> atgriež <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> atgriež <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr>
<td>PADLEFT (virkne, garums, papildināšanas rakstzīmes)</td>
<td>Atgriezt norādītā garuma virkni, kurā norādītās virknes sākumā ir ievadītas norādītās rakstzīmes.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> atgriež teksta virkni <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr>
<td>TRIM (virkne)</td>
<td>Atgriezt norādīto teksta virkni, kam ir aprautas sākuma un beigu atstarpes un noņemtas vairākas atstarpes starp vārdiem.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sample&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> atgriež <strong>&quot;Sample text&quot;</strong>.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (uzskaitījuma datu avota ceļš, uzskaitījuma vērtības etiķetes teksts)</td>
<td>Atgriezt norādītā uzskaitījuma datu avota vērtību atbilstoši uzskaitījuma etiķetes norādītajam tekstam.</td>
<td>Tālāk esošajā attēlā ir parādīts datu modelī ieviests uzskaitījums <strong>ReportDirection</strong>. Ņemiet vērā, ka etiķetes ir definētas uzskaitījumu vērtībām.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.</p>
<ul>
<li>Modeļu uzskaitījums <strong>ReportDirection</strong> ir ievietots pārskatā kā datu avots <strong>$Direction</strong>.</li>
<li>ER izteiksme <strong>$IsArrivals</strong> ir izveidota ar mērķi lietot modeļu uzskaitījumu kā šīs funkcijas parametru. Šīs izteiksmes vērtība ir <strong>TRUE</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (ievade)</td>
<td>Norādīto ievadi ar tipu <strong>Virkne</strong> konvertēt uz datu elementu ar datu tipu <strong>GUID</strong>.<blockquote>[!NOTE] Lai veiktu konvertēšanu pretējā virzienā (tas ir, lai norādīto ievadi ar datu tipu <strong>GUID</strong> konvertētu uz datu elementu ar datu tipu <strong>Virkne</strong> ), varat izmantot funkciju <strong>TEXT()</strong>.</blockquote></td>
<td>Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.
<ul>
<li><strong>myID</strong> (tips<strong>Aprēķinātais lauks</strong> ), kurā ir izteiksme <strong>GUIDVALUE(&quot;AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0&quot;)</strong></li>
<li><strong>Users</strong> (tips<strong>Tabulas ieraksti</strong> ), kas atsaucas uz tabulu UserInfo</li>
</ul>
Kad šie datu avoti ir definēti, varat izmantot tādu izteiksmi kā <strong>FILTER (Users, Users.objectId = myID)</strong>, lai filtrētu tabulu UserInfo pēc lauka <strong>objectId</strong> ar datu tipu <strong>GUID</strong>.
</td>
</tr>
<tr>
<td>JSONVALUE (identifikators, ceļš)</td>
<td>Parsēt datus formātā JavaScript Object Notation (JSON), kuriem piekļūst ar norādīto ceļu, lai izgūtu skalāru vērtību, kas ir balstīta uz norādīto ID.</td>
<td>Datu avotā <strong>$JsonField</strong> ir ietverti tālāk norādītie dati JSON formātā: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. Šim datu avotam funkcija </strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong> atgriež vērtību <strong>7.3.1234.1</strong> ar datu tipu <strong>String</strong>.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Datu konvertēšanas funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| TEXT (ievade) | Atgriezt norādīto ievadi, kas ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās prorgammas instances servera lokalizācijas iestatījumiem. Vērtībām ar tipu **real** šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata. | Ja Finance and Operations instances servera lokalizācija ir definēta kā **EN-US**, funkcija **TEXT (NOW ())** pašreizējo Finance and Operations sesijas datumu, 2015. gada 17. decembri, atgriež kā teksta virkni **"12/17/2015 07:59:23 AM"**. **TEXT (1/3)** atgriež **"0.33"**. |
| QRCODE (virkne) | Norādītajai virknei atgriezt kvadrātkoda (Quick Response Code — QR koda) attēlu base64 binārajā formātā. | **QRCODE ("Sample text")** atgriež **U2FtcGxlIHRleHQ=**. |

### <a name="data-collection-functions"></a>Datu apkopošanas funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Atgriezt pašreizējā formāta elementa nosaukumu. Atgriezt tukšu virkni, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi **ER Lietot formāta izvades datus uzskaitei un summēšanai**, kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**. |
| SUMIFS (galvenā virkne summēšanai, kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\]) | Atgriezt summu no vērtībām, kas tika savāktas XML mezgliem (kur nosaukums ir definēts kā atslēga) formāta palaišanas laikā un kas nodrošina atbilstību norādītajiem nosacījumiem (diapazonu un vērtību pāriem). Atgriezt **0** (nulles) vērtību, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |
| SUMIF (atslēgu virkne summēšanai, kritēriju diapazona virkne, kritēriju vērtību virkne) | Atgriezt summu no vērtībām, kas tika savāktas XML mezgliem (kur nosaukums ir definēts kā atslēga) formāta palaišanas laikā un kas nodrošina atbilstību norādītajam nosacījumam (diapazonam un vērtībai). Atgriezt **0** (nulles) vērtību, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |
| COUNTIFS (kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\]) | Atgriezt XML mezglu skaitu, kas tika savākts, izpildot formātu, un kas nodrošina atbilstību norādītajiem nosacījumiem (diapazonu un vērtību pāriem). Atgriezt **0** (nulles) vērtību, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |
| COUNTIF (kritēriju diapazona virkne, kritēriju vērtību virkne) | Atgriezt XML mezglu skaitu, kas tika savākts, izpildot formātu, un kas nodrošina atbilstību norādītajam nosacījumam (diapazonam un vērtībai). Atgriezt **0** (nulles) vērtību, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |
| COLLECTEDLIST (kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\]) | Atgriezt sarakstu ar vērtībām, kas tika savāktas XML mezgliem, izpildot formātu, un kas nodrošina atbilstību norādītajiem nosacījumiem (diapazonam un vērtībai). Atgriezt tukšu sarakstu, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |

### <a name="other-business-domainspecific-functions"></a>Citas (biznesa jomai specifiskas) funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| CONVERTCURRENCY (summa, avota valūta, mērķa valūta, datums, uzņēmums) | Norādīto naudas summu no norādītā avota valūtas konvertēt norādītajā mērķa valūtā, izmantojot norādītā uzņēmuma iestatījumus norādītajā datumā. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** atgriež viena eiro ekvivalentu ASV dolāros pašreizējās sesijas datumā, balstoties uz uzņēmuma DEMF iestatījumiem. |
| ROUNDAMOUNT (skaitlis, cipari aiz komata, noapaļošanas kārtula) | Norādīto summu noapaļojiet līdz norādītajam ciparu skaitam aiz komata saskaņā ar norādīto noapaļošanas kārtulu.<blockquote>[!NOTE] Noapaļošanas kārtula ir jānorāda kā uzskaitījuma **RoundOffType** vērtība.</blockquote> | Ja ir iestatīta parametra **model.RoundOff** vērtība **Downward**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** atgriež vērtību **1000.78**. Ja parametrs **model.RoundOff** ir iestatīts uz **Normal** vai uz **Rounding-up**, tad **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** atgriež vērtību **1000.79**. |
| CURCredRef (cipari) | Atgriezt kreditora atsauci, pamatojoties uz norādītā rēķina numura cipariem. | **CURCredRef ("VEND-200002")** atgriež **"2200002"**. |
| MOD\_97 (cipari) | Atgriezt kreditora atsauci kā MOD97 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem. | **MOD\_97 ("VEND-200002")** atgriež **"20000285"**. |
| ISOCredRef (cipari) | Atgriezt Starptautiskās Standartizācijas organizācijas (ISO) kreditora atsauci atbilstoši norādītā rēķina numura cipariem un burtiem.<blockquote>[!NOTE] Lai izslēgtu alfabētu simbolus, kas nav saderīgi ar ISO, šis ievades parametrs pirms nodošanas šai funkcijai ir jātulko.</blockquote> | **ISOCredRef ("VEND-200002")** atgriež **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (virkne, skaitlis) | Iegūt norādīto papildu finanšu dimensijas ID. Parametrā **virkne** dimensijas tiek attēlotas kā ar komatiem atdalīti identifikatori. Parametrs **skaitlis** definē pieprasītās dimensijas sērijas kodu šajā virknē. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** atgriež **"CC"**. |
| GetCurrentCompany () | Atgriezt tās juridiskās personas (uzņēmuma) koda teksta attēlojumu, kurā lietotājs ir pašlaik pierakstījies. | **GETCURRENTCOMPANY ()** atgriež **USMF** lietotājam, kurš ir pierakstījies uzņēmumā **Contoso Entertainment System USA**. |
| CH\_BANK\_MOD\_10 (cipari) | Atgriezt kreditora atsauci kā MOD10 izteiksmi atbilstoši norādītā rēķina numura cipariem. | **CH\_BANK\_MOD\_10 ("VEND-200002")** atgriež **3**. |
| FA\_SUM (pamatlīdzekļa kods, vērtības modeļa kods, sākuma datums, beigu datums) | Atgriezt sagatavoto norādītā perioda pamatlīdzekļu summas datu konteineru. | **FA\_SUM ("COMP-000001", "Current", Date1, Date2)** atgriež sagatavoto datu konteineru pamatlīdzeklim **"COMP-000001"** ar vērtības modeli **"Current"** par periodu no **Date1** līdz **Date2**. |
| FA\_BALANCE (pamatlīdzekļa kods, vērtības modeļa kods, pārskata gads, pārskata datums) | Atgriezt sagatavoto pamatlīdzekļu bilances datu konteineru. Šis pārskata gads ir jānorāda kā uzskaitījuma **AssetYear** vērtība. | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** atgriež sagatavoto datu konteineru no bilancēm pamatlīdzeklim **"COMP-000001"** ar vērtības modeli **"Current"** pašreizējā programmas sesijas datumā. |
| TABLENAME2ID (virkne) | Atgriezt tabulas ID veselu skaitļu attēlojumu norādītajam tabulas nosaukumam. | **TABLENAME2ID ("Intrastat")** atgriež **1510**. |
| ISVALIDCHARACTERISO7064 (virkne) | Atgriezt Būla vērtību **TRUE**, ja norādītā virkne attēlo derīgu starptautisko bankas konta numuru (IBAN). Pretējā gadījumā atgriezt Būla vērtību **FALSE**. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** atgriež **TRUE**. **ISVALIDCHARACTERISO7064 ("AT61")** atgriež **FALSE**. |
| NUMSEQVALUE (numuru sērijas kods, tvērums, tvēruma ID) | Atgriezt numuru sērijas jauno ģenerēto vērtību, pamatojoties uz norādīto numuru sērijas kodu, tvērumu un tvēruma ID. Tvērumam ir jābūt noradītam ka uzskaitījuma **ERExpressionNumberSequenceScopeType** vērtībai (**Koplietots**, **Juridiskā persona** vai **Uzņēmums**). Tvērumam **Koplietots** kā tvēruma ID ir jānorāda tukša virkne. Tvērumam **Uzņēmums** un **Juridiskā persona** kā tvēruma ID ir jānorāda uzņēmuma kods. Ja tvērumam **Uzņēmums** un **Juridiskā persona** ka tvēruma ID norādāt tukšu virkni, tiek izmantots pašreizējais uzņēmuma kods. | Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.<ul><li>**enumScope** (tips**Dynamics 365 for Operations uzskaitījums** ), kas atsaucas uz **ERExpressionNumberSequenceScopeType** uzskaitījumu</li><li>**NumSeq** (tips**Aprēķinātais lauks** ), kurā ir izteiksme **NUMSEQVALUE ("Gene\_1", enumScope.Company, "")**</li></ul>Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jauno vērtību, kas ir ģenerēta ar numuru sēriju **Gene\_1**, kura ir konfigurēta uzņēmumam, kas nodrošina kontekstu, kurā tiek darbināts ER formāts. |
| NUMSEQVALUE (numuru sērijas kods) | Atgriezt numuru sērijas jauno ģenerēto vērtību, pamatojoties uz norādīto numuru sēriju, tvērumu **Uzņēmums**, un (kā tvēruma ID) tā uzņēmuma tvērumu, kas nodrošina kontekstu, saskaņā ar kuru tiek darbināts ER formāts. | Savā modeļu kartējumā jūs definējat šādus datu avotus: **NumSeq** (ar tipu**Aprēķinātais lauks** ). Šajā datu avotā ir izteiksme **NUMSEQVALUE ("Gene\_1")**. Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jauno vērtību, kas ir ģenerēta ar numuru sēriju **Gene\_1**, kura ir konfigurēta uzņēmumam, kas nodrošina kontekstu, kurā tiek darbināts ER formāts. |
| NUMSEQVALUE (numuru sērijas ieraksta ID) | Atgriezt numuru sērijas jauno ģenerēto vērtību, pamatojoties uz norādīto numuru sērijas ieraksta ID. | Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.<ul><li>**LedgerParms** (tips**Tabula** ), kas atsaucas uz LedgerParameters tabulu</li><li>**NumSeq** (tips**Aprēķinātais lauks** ), kurā ir izteiksme **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)**</li></ul>Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jauno vērtību, kas ir ģenerēta ar numuru sēriju, kura ir konfigurēta virsgrāmatas parametros tam uzņēmumam, kas nodrošina kontekstu, kurā tiek darbināts ER formāts. Šī numuru sērija unikāli identificē žurnālus un darbojas kā partijas numurs, kas sasaista transakcijas. |

### <a name="functions-list-extension"></a>Funkciju saraksta paplašināšana

ER jums ļauj paplašināt funkciju sarakstu, kuras tiek lietotas ER izteiksmēs. Ir jāveic noteiktas tehniskas darbības. Papildinformāciju skatiet rakstā [Elektronisko pārskatu (EP) veidošanas funkciju saraksta paplašināšana](general-electronic-reporting-formulas-list-extension.md).

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko ziņojumu (ER) pārskats](general-electronic-reporting.md)
- [Paplašināt elektronisko pārskatu veidošanas (ER) funkciju sarakstu](general-electronic-reporting-formulas-list-extension.md)