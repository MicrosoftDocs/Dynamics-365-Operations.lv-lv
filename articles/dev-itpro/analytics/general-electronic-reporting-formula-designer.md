---
title: "Formulas veidotājs elektronisko atskaišu veidošanā"
description: "Šajā tēmā ir paskaidrots, kā elektronisko pārskatu veidošanā (Electronic reporting — ER) lietot formulas veidotāju."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 946584d8afa8937afc7a26835e05b0eecebaad35
ms.openlocfilehash: 67558889dea03738a665d8f1e2f30833b96c4656
ms.contentlocale: lv-lv
ms.lasthandoff: 12/23/2017

---

# <a name="formula-designer-in-electronic-reporting"></a>Formulas veidotājs elektronisko atskaišu veidošanā

[!include[banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā elektronisko pārskatu veidošanā (Electronic reporting — ER) lietot formulas veidotāju. Kad veidojat formātu noteiktam ER elektroniskajam dokumentam, datu pārveidošanai varat lietot formulas, lai nodrošinātu atbilstību dokumenta izpildes un formatējuma prasībām. Šīs formulas līdzinās Microsoft Excel formulām. Formulās tiek atbalstīti dažādi funkciju tipi — teksta, datuma un laika, matemātiskās, loģiskās, informācijas, datu tipu pārveidošanas un citas (biznesa jomai specifiskas funkcijas).

## <a name="formula-designer-overview"></a>Pārskats par formulas veidotāju

ER atbalsta formulas veidotāju. Tāpēc veidošanas laikā varat konfigurēt izteiksmes, kuras var izmantot tālāk norādīto uzdevumu izpildes laikā.

- Datu pārveidošana tādiem datiem, kas ir saņemti no Microsoft Dynamics 365 for Finance and Operations Enterprise Edition datu bāzes un kas ir jāievada ER datu modelī, kuru ir paredzēts lietot kā datu avotu ER formātiem. (Šie pārveidojumi var iekļaut, piemēram, filtrēšanu, grupēšanu un datu tipa pārveidošanu.)
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

- No Finance and Operations datu avotiem un izpildlaika parametriem uz ER datu modeli
- No ER datu modeļa uz ER formātu
- No Finance and Operations datu avotiem un izpildlaika parametriem uz ER formātu

Nākamajā attēlā ir parādīts šī tipa izteiksmes noformējums. Šajā piemērā izteiksme noapaļo Finance and Operations tabulas Intrastat lauka **Intrastat.AmountMST** vērtību līdz diviem cipariem aiz komata un pēc tam atgriež noapaļoto vērtību.

[![Datu saistīšana](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Tālāk esošajā attēlā ir parādīts, kā var lietot šī tipa izteiksmi. Šajā piemērā izveidotās izteiksmes rezultāts tiek ievadīts datu modeļa **Nodokļu pārskatu veidošanas modelis** komponentā **Transaction.InvoicedAmount**.

[![Tiek izmantota datu saistīšana](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Izpildes laikā izveidotā formula **ROUND (Intrastat.AmountMST, 2)** katra tabulas Instrastat ieraksta lauka **AmountMST** vērtību noapaļo līdz diviem cipariem aiz komata. Pēc tam tā noapaļoto vērtību ievada datu modeļa **Nodokļu pārskatu veidošana** komponentā **Transaction.InvoicedAmount**.

### <a name="data-formatting"></a>Datu formatēšana

ER formulas veidotāju var izmantot, lai definētu izteiksmi, kas formatē no datu avotiem saņemtos datus, lai šos datus varētu nosūtīt kā daļu no ģenerētā elektroniskā dokumenta. Iespējams, jums ir formatējums, kas jālieto kā tipiska kārtula, kuru nepieciešams atkārtoti izmantot kādam formātam. Šajā gadījumā formāta konfigurācijā šo formatēšanu varat vienu reizi ieviest kā nosauktu pārveidošanu, kurai ir formatēšanas izteiksme. Pēc tam šo nosaukto pārveidošanu var saistīt ar daudziem formāta komponentiem, kuriem ir nepieciešams formatēt izvadi atbilstoši jūsu izveidotajai formatēšanas izteiksmei.

Nākamajā attēlā ir parādīts šī tipa transformēšanas noformējums. Šajā piemērā pārveidošana **TrimmedString** aprauj ienākošos datus ar datu tipu **String**, noņemot sākuma un beigu atstarpes. Pēc tam tā atgriež aprauto virknes vērtību.

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
- Pārbaude atgriež kļūdas ziņojumu, kas ietver Finance and Operations etiķetes SYS70894 tekstu lietotāja vēlamajā valodā.

[![Apstiprināšana](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER formulas veidotāju var izmantot arī, lai ģenerētu faila nosaukumu ģenerētajam elektroniskajam dokumentam un kontrolētu faila izveides procesu. Nākamajā attēlā ir parādīts šī tipa procesa plūsmas kontroles noformējums. Šeit ir šajā piemērā lietotās konfigurācijas skaidrojums:

- Ierakstu saraksts no datu avota **model.Intrastat** tiek sadalīts partijās. Katrā no partijām ietverts līdz 1000 ierakstiem.
- Izvade izveido zip failu, kas katrai izveidotajai partijai satur vienu failu XML formātā.
- Izteiksme atgriež faila nosaukumu ģenerētajiem elektroniskajiem dokumentiem, savienojot faila nosaukumu un faila nosaukuma paplašinājumu. Otrajai partijai un visām turpmākajām partijām faila nosaukums kā sufiksu ietver partijas ID.
- Izteiksme iespējo (atgriežot vērtību **TRUE**) faila izveides procesu partijām, kas ietver vismaz vienu ierakstu.

[![Faila vadība](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Pamata sintakse

ER izteiksmes var saturēt jebkuru vai visus no šādiem elementiem:

- Konstantes
- Operatori
- Atsauces
- Ceļi
- Funkcijas

#### <a name="constants"></a>Konstantes

Kad veidojat izteiksmes, varat lietot teksta un skaitļu konstantes (t.i., vērtības, kas netiek aprēķinātas). Piemēram, izteiksme **VALUE ("100") + 20** lieto skaitļu konstanti **20** un virknes konstanti **"100"**, un atgriež skaitlisku vērtību **120**. ER formulas veidotājs atbalsta atsoļa sekvences. Tādējādi varat norādīt, kura izteiksmes virkne ir jāapstrādā citādi. Piemēram, izteiksme **"Ļevs Tolstojs ""Karš un miers"" 1. sējums"** atgriež šādu teksta virkni: **Ļevs Tolstojs "Karš un miers" 1. sējums**.

#### <a name="operators"></a>Operatori

Tālāk esošajā tabulā ir parādīti aritmētiskie operatori, ko varat izmantot, lai veiktu pamata matemātiskās darbības, piemēram, saskaitīšanu, atņemšanu, reizināšanu un dalīšanu.

| Operators | Nozīme               | Paraugs |
|----------|-----------------------|---------|
| +        | Papildinājums              | 1+2     |
| -        | Atņemšana, negācija | 5-2, -1 |
| \*       | Reizināšana        | 7\*8    |
| /        | Nodaļa              | 9/3     |

Tālāk esošajā tabulā parādīti atbalstītie salīdzināšanas operatori. Šos operatorus varat izmantot, lai salīdzinātu divas vērtības.

| Operators | Nozīme                  | Paraugs    |
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
| 7.          | Grupēšana       | ( … )                                                                   |
| 6.          | Piekļuve elementam  | … . …                                                                   |
| 5.          | Funkcijas izsaukums  | … ( … )                                                                 |
| 4.          | Reizināšana un dalīšana | … \* …<br>… / …                                                         |
| 3.          | Piedeva       | … + …<br>… - …                                                          |
| 2          | Salīdzinājums     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Atdalīšana     | … , …                                                                   |

Ja izteiksmē ir vairāki secīgi operatori ar vienādu prioritātes vērtību, šie operatori tiek vērtēti no kreisās uz labo pusi. Piemēram, izteiksme **1 + 6 / 2 \* 3 &gt; 5** atgriež vērtību **patiess**. Ieteicams izmantot iekavas, lai skaidri norādītu vēlamo operāciju secību izteiksmēs, lai izteiksmes būtu vieglāk lasāmas un uzturamas.

#### <a name="references"></a>Atsauces

Visus pašreizējā ER komponenta datu avotus, kas ir pieejami izteiksmes veidošanas laikā, var izmantot kā nosauktas atsauces. (Pašreizējais ER komponents var būt modelis vai formāts.) Piemēram, pašreizējais ER datu modelis ietver datu avotu **ReportingDate**, un šis datu avots atgriež datu tipa **DATETIME** vērtību. Lai pareizi formatētu šo vērtību ģenerēšanas dokumentā, izteiksmē uz datu avotu varat atsaukties šādi: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**.

Pirms visām ar atsauci norādītā datu avota nosaukumā esošajām rakstzīmēm, kas nav alfabēta burti, ir jāievieto vienpēdiņa ('). Ja ar atsauci norādītā datu avota nosaukumā ir vismaz viens simbols, kas nav alfabēta burts, nosaukums ir jāietver vienpēdiņās. (Šie simboli, kas nav alfabēta burti, var būt, piemēram, pieturzīmes vai citi rakstveida simboli.) Tālāk sniegti daži piemēri.

- Uz datu avotu **Today's date & time** ER izteiksmē ir jāatsaucas šādi: **'Today''s date & time'**.
- Uz datu avota **Customers** metodi **name()** ER izteiksmē ir jāatsaucas šādi: **Customers.'name()'**.

Ja Finance and Operations datu avotu metodēm ir parametri, šo metožu izsaukšanai tiek izmantota tālāk norādītā sintakse.

- Ja datu avota **System** metodei **isLanguageRTL** ir parametrs **EN-US** ar datu tipu **String**, ER izteiksmē uz šo metodi ir jāatsaucas šādi: **System.'isLanguageRTL'("EN-US")**.
- Pēdiņas nav obligātas, ja metodes nosaukums ietver tikai burtu un ciparu simbolus. Taču tās ir obligātas tabulas metodei, ja nosaukums ietver iekavas.

Kad datu avots **System** tiek pievienots ER kartēšanai, kas atsaucas uz Finance and Operations programmas klasi **Global**, izteiksme atgriež Būla vērtību **FALSE**. Modificētā izteiksme **System.' isLanguageRTL'("AR")** atgriež Būla vērtību **TRUE**.

Varat ierobežot veidu, kādā vērtības tiek nodotas šī tipa metodes parametriem.

- Šī tipa metodēm var nodot tikai konstantes. Konstanšu vērtības tiek definētas veidošanas laikā.
- Šī tipa parametriem tiek atbalstīti tikai primitīvi (pamata) datu tipi. (Primitīvie datu tipi ir vesels skaitlis, reāls skaitlis, Būla vērtība, virkne utt.).

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
| NOW () | Pašreizējo Finance and Operations programmas servera datumu un laiku atgrieziet kā datuma/laika vērtību. | |
| TODAY () | Pašreizējo Finance and Operations programmas servera datumu atgrieziet kā datuma vērtību. | |
| NULLDATE () | Atgrieziet datuma vērtību **null**. | |
| NULLDATETIME () | Atgrieziet datuma/laika vērtību **null**. | |
| DATETIMEFORMAT (datums un laiks, formāts) | Norādīto datuma/laika vērtību pārveidojiet par virkni norādītajā formātā. (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** pašreizējās Finance and Operations programmas servera datumu, 2015. gada 24. decembri, atgriež kā **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam. |
| DATETIMEFORMAT (datums un laiks, formāts, kultūra) | Norādīto datuma/laika vērtību pārveidojiet par virkni norādītajā formātā un atbilstoši norādītajai [kultūrai](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** pašreizējo Finance and Operations programmas servera datumu, 2015. gada 24. decembri, atgriež kā **"24.12.2015"** atbilstoši atlasītajai vācu kultūrai. |
| SESSIONTODAY () | Pašreizējo Finance and Operations sesijas datumu atgrieziet kā datuma vērtību. | |
| SESSIONNOW () | Pašreizējo Finance and Operations sesijas datumu un laiku atgrieziet kā datuma/laika vērtību. | |
| DATEFORMAT (datums, formāts) | Norādītā datuma virknes attēlojumu atgrieziet norādītajā formātā. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** pašreizējās Finance and Operations sesijas datumu, 2015. gada 24. decembri, atgriež kā **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam. |
| DATEFORMAT (datums, formāts, kultūra) | Norādīto datuma vērtību pārveidojiet par virkni norādītajā formātā un atbilstoši norādītajai [kultūrai](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** pašreizējo Finance and Operations sesijas datumu, 2015. gada 24. decembri, atgriež kā **"24.12.2015"** atbilstoši atlasītajai vācu kultūrai. |
| DAYOFYEAR (datums) | Atgrieziet veselu skaitļu attēlojumu dienu skaitam no 1. janvāra līdz norādītajam datumam. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** atgriež **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** atgriež **1**. |
| DAYS (1. datums, 2. datums) | Atgrieziet dienu skaitu starp pirmo norādīto datumu un otro norādīto datumu. Ja pirmais datums ir lielāks par otro datumu, tiek atgriezta pozitīva vērtība; ja pirmais datums ir vienāds ar otro datumu, tiek atgriezta **0** (nulle); citos gadījumos tiek atgriezta negatīva vērtība. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** atgriež **-1**. |

### <a name="data-conversion-functions"></a>Datu konvertēšanas funkcijas

| Funkcija | apraksts | Paraugs |
|----------|-------------|---------|
| DATETODATETIME (datums) | Norādīto datuma vērtību pārveidojiet par datuma/laika vērtību. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** pašreizējās Finance and Operations sesijas datumu, 2015. gada 24. decembri, atgriež izteiktu kā **12/24/2015 12:00:00 AM**. Šajā piemērā **CompInfo** ir ER datu avots ar tipu **Finance and Operations/Table**, un tas atsaucas uz tabulu CompanyInfo. |
| DATEVALUE (virkne, formāts) | Norādītās virknes datuma attēlojumu atgrieziet norādītajā formātā. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** atgriež datumu 2016. gada 21. decembris atbilstoši norādītajam pielāgotajam formātam un programmas noklusējuma kultūrai **EN-US**. |
| DATEVALUE (virkne, formāts, kultūra) | Norādītās virknes datuma attēlojumu atgrieziet norādītajā formātā un atbilstoši norādītajai kultūrai. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** atgriež datumu 2016. gada 21. janvāris atbilstoši norādītajam pielāgotajam formātam un kultūrai. Taču **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** parādīs izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīgs datums. |
| DATETIMEVALUE (virkne, formāts) | Norādītās virknes datuma/laika attēlojumu atgrieziet norādītajā formātā. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** atgriež 2016. gada 21. decembra plkst. 2.55.00 atbilstoši norādītajam pielāgotajam formātam un programmas noklusējuma kultūrai **EN-US**. |
| DATETIMEVALUE (virkne, formāts, kultūra) | Norādītās virknes datuma/laika attēlojumu atgrieziet norādītajā formātā un atbilstoši norādītajai kultūrai. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** atgriež 2016. gada 21. decembra plkst. 2.55.00 atbilstoši norādītajam pielāgotajam formātam un kultūrai. Taču **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** parādīs izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīgs datums/laiks. |

### <a name="list-functions"></a>Saraksta funkcijas

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkcija</th>
<th>apraksts</th>
<th>Paraugs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (ievade, garums)</td>
<td>Norādīto ievades virkni sadalīt apakšvirknēs, katrai no kurām ir norādīts garums. Atgriezt rezultātu kā jaunu sarakstu.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> atgriež jaunu sarakstu, kas sastāv no diviem ierakstiem ar tipa <strong>STRING</strong> lauku. Pirmā ieraksta laukā ir teksts <strong>&quot;abc&quot;</strong>, bet otrā ieraksta laukā ir teksts <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (saraksts, skaits)</td>
<td>Norādīto sarakstu sadalīt partijās, katrā no kurām ir iekļauts norādītais ierakstu skaits. Atgriezt rezultātu kā jaunu partiju sarakstu, kas satur šādus elementus:
<ul>
<li>Partijas kā parasti saraksti (komponents <strong>Value</strong>)</li>
<li>Skaits pašreizējā partijā (komponents <strong>BatchNumber</strong>)</li>
</ul></td>
<td>Tālāk esošajā attēlā redzamais datu avots <strong>Lines</strong> tiek izveidots kā ierakstu saraksts, kurš sastāv no trīs ierakstiem. Šis saraksts tiek sadalīts divās partijās — katrā no partijām ir līdz diviem ierakstiem.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Tālāk esošajā attēlā parādīts izveidotā formāta izkārtojums. Šajā formāta izkārtojumā saistījumi ar datu avotu <strong>Lines</strong> tiek izveidoti, lai ģenerētu izvadi XML formātā Šajā izvadē ietverti atsevišķi mezgli katrai partijai un tajā esošajiem ierakstiem.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (1. ieraksts [, 2. ieraksts, …])</td>
<td>Atgriezt jaunu sarakstu, kas tiek izveidots no norādītajiem argumentiem.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> atgriež tukšu ierakstu, kur lauku saraksts satur visus laukus no ierakstu sarakstiem <strong>MainData</strong> un <strong>OtherData</strong>.</td>
</tr>
<tr class="even">
<td>LISTJOIN (1. saraksts, 2. saraksts, …)</td>
<td>Atgriezt savienotu sarakstu, kas tiek izveidots no norādīto argumentu sarakstiem.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> atgriež sešu ierakstu sarakstu, kurā viens datu tipa <strong>STRING</strong> lauks satur atsevišķus burtus.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (saraksts)</td>
<td>Atgrieziet vērtību <strong>TRUE</strong>, ja norādītajā sarakstā nav neviena elementa. Pretējā gadījumā atgriezt vērtību <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (saraksts)</td>
<td>Atgriezt tukšu sarakstu, šī saraksta struktūrai kā avotu izmantojot norādīto sarakstu.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> atgriež jaunu tukšu sarakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež funkcija <strong>SPLIT</strong>.</td>
</tr>
<tr class="odd">
<td>FIRST (saraksts)</td>
<td>Atgriezt pirmo ierakstu no norādītā saraksta, ja šis ieraksts nav tukšs. Pretējā gadījumā parādīt izņēmumu.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (saraksts)</td>
<td>Atgriezt pirmo ierakstu no norādītā saraksta, ja šis ieraksts nav tukšs. Pretējā gadījumā atgriezt ierakstu <strong>null</strong>.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (saraksts)</td>
<td>Atgriezt sarakstu, kas satur tikai pirmo norādītā saraksta elementu.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (ceļš)</td>
<td>Atgriezt jaunu izplātu sarakstu, kas atspoguļo visus elementus, kuri atbilst norādītajam ceļam. Šis ceļš ir jādefinē kā derīgs datu avota ceļš datu avota elementam ar ierakstu saraksta datu tipu. Tādiem datu elementiem kā ceļa virkne un datums ER izteiksmju veidotājā veidošanas laikā ir jāizraisa kļūda.</td>
<td>Ja kā satura avotu (DS) ievadāt <strong>SPLIT(&quot;abcdef&quot; , 2)</strong>, funkcija <strong>COUNT( ALLITEMS (DS.Value))</strong> atgriež vērtību <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (saraksts [, 1. izteiksme, 2. izteiksme, …])</td>
<td>Atgrieziet norādīto sarakstu, kas ir sakārtots atbilstoši norādītajiem argumentiem. Šos argumentus var definēt kā izteiksmes.</td>
<td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, <strong>ORDERBY (Vendors, Vendors.'name()')</strong> atgriež sarakstu ar kreditoriem, kuri ir sakārtoti augošā secībā pēc nosaukuma.</td>
</tr>
<tr class="even">
<td>REVERSE (saraksts)</td>
<td>Atgriezt norādīto sarakstu apgrieztā kārtošanas secībā.</td>
<td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> atgriež sarakstu ar kreditoriem, kuri ir sakārtoti dilstošā secībā pēc nosaukuma.</td>
</tr>
<tr class="odd">
<td>WHERE (saraksts, nosacījums)</td>
<td>Atgrieziet norādīto sarakstu, kas ir filtrēts atbilstoši norādītajam nosacījumam. Norādītais nosacījums tiek lietots attiecībā uz atmiņā esošu sarakstu. Šādi funkcija <strong>WHERE</strong> atšķiras no funkcijas <strong>FILTER</strong>.</td>
<td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu.</td>
</tr>
<tr class="even">
<td>ENUMERATE (saraksts)</td>
<td>Atgriezt jaunu sarakstu, kas sastāv no norādītā saraksta uzskaitījuma ierakstiem un parāda šādus elementus:
<ul>
<li>Norādītā saraksta ieraksti kā parasti saraksti (komponents <strong>Value</strong>)</li>
<li>Pašreizējā ieraksta indekss (komponents <strong>Number</strong>)</li>
</ul></td>
<td>Tālāk esošajā attēlā datu avots <strong>Enumerated</strong> tiek izveidots kā uzskaitījuma kreditoru ierakstu saraksts no datu avota <strong>Vendors</strong>, kas atsaucas uz tabulu VendTable.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Tālāk esošajā attēlā ir parādīts formāts. Šajā formātā tiek izveidoti saistījumi, lai ģenerētu izvadi XML formātā Šajā izvadē atsevišķi kreditori attēloti kā uzskaitījuma mezgli.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (saraksts)</td>
<td>Atgriezt ierakstu skaitu norādītajā sarakstā, ja šis saraksts nav tukšs. Pretējā gadījumā atgriezt vērtību <strong>0</strong> (nulle).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> atgriež vērtību <strong>2</strong>, jo funkcija <strong>SPLIT</strong> izveido sarakstu, kas sastāv no diviem ierakstiem.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (ceļš)</td>
<td>Atgrieziet ierakstu sarakstu, kas izveidots no argumenta ar vienu no tālāk uzskaitītajiem tipiem.
<ul>
<li>Modeļa uzskaitījums</li>
<li>Formāta uzskaitījums</li>
<li>Konteiners</li>
</ul>
<p>Izveidotajā sarakstā ietverti ieraksti ar tālāk norādītajiem laukiem.</p>
<ul>
<li>Vārds, uzvārds</li>
<li>Iezīme</li>
<li>apraksts</li>
</ul>
Izpildes laikā lauki <strong>Etiķete</strong> un <strong>Apraksts</strong> atgriež vērtības atbilstoši formāta valodas iestatījumiem.</td>
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
<blockquote>[!NOTE]<br>
Atbilstoši formāta vecākelementu FILE un FOLDER valodas iestatījumiem etiķešu un aprakstu tulkotais teksts tiek ievadīts ER formāta izvadē.</blockquote></td>
</tr>
<tr class="odd">
<td>LISTOFFIELDS (ceļš, valoda)</td>
<td>Atgrieziet ierakstu sarakstu, kas izveidots no argumenta, piemēram, modeļu uzskaitījuma, formātu uzskaitījuma vai konteinera. Izveidotajā sarakstā ietverti ieraksti ar tālāk norādītajiem laukiem.
<ul>
<li>Vārds, uzvārds</li>
<li>Iezīme</li>
<li>apraksts</li>
<li>Tulkots</li>
</ul>
<p>Izpildes laikā lauki <strong>Etiķete</strong> un <strong>Apraksts</strong> atgriež vērtības atbilstoši formāta valodas iestatījumiem un norādītajai valodai. Lauks <strong>Tulkots</strong> norāda, ka lauks <strong>Etiķete</strong> ir iztulkots norādītajā valodā.</td>
<td>Piemēram, varat izmantot datu avota tipu <strong>Aprēķinātais lauks</strong>, lai konfigurētu datu modeļu uzskaitījuma <strong>enumType</strong> datu avotus <strong>enumType_de</strong> un <strong>enumType_deCH</strong>.
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
Šajā gadījumā varat izmantot tālāk norādīto izteiksmi, lai iegūtu uzskaitījuma vērtības etiķeti Šveices vācu valodā, ja šāds tulkojums ir pieejams. Ja tulkojums Šveices vācu valodā nav pieejams, etiķete ir vācu valodā: <strong>IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)</strong>.</td>
</tr>
<tr class="even">
<td>STRINGJOIN (saraksts, lauka nosaukums, norobežotājs)</td>
<td>Atgrieziet virkni, kas sastāv no norādītā saraksta norādītā lauka savirknētajām vērtībām. Vērtības tiek atdalītas ar norādīto norobežotāju.</td>
<td>Ja kā datu avotu (DS) ievadāt <strong>SPLIT(&quot;abc&quot; , 1)</strong>, izteiksme <strong>STRINGJOIN (DS, DS.Value, &quot;:&quot;)</strong> atgriež <strong>&quot;a:b:c&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>SPLITLISTBYLIMIT (saraksts, robežvērtība, ierobežojumu avots)</td>
<td>Norādīto sarakstu sadaliet jaunā apakšsarakstu sarakstā un atgrieziet rezultātu ierakstu saraksta saturā. Robežvērtības parametrs definē ierobežojuma vērtību sākotnējā saraksta sadalīšanai. Ierobežojuma avota parametrs definē soli, par kādu kopsumma tiek palielināta. Ierobežojums netiek lietots atsevišķam vienumam attiecīgajā sarakstā, ja ierobežojuma avots pārsniedz definēto ierobežojumu.</td>
<td>Tālāk esošajos attēlos parādīts formāts un tam izmantotie datu avoti. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc formāta palaišanas. Šajā gadījumā izvade ir nekārtots preču saraksts.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>Tālāk esošajos attēlos redzams, ka tas pats formāts ir pielāgots tā, lai preču sarakstu rādītu pa partijām, vienā partijā ietverot preces un nepārsniedzot kopējā svara ierobežojumu 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Tālāk esošajā attēlā parādīts rezultāts pēc pielāgotā formāta palaišanas.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE]<br>
Ierobežojums netiek lietots pēdējam sākotnējā saraksta vienumam, jo ierobežojuma avota (svara) vērtība (11) pārsniedz noteikto ierobežojumu (9). Lai pārskata ģenerēšanas laikā ignorētu (izlaistu) apakšsarakstus (ja nepieciešams), izmantojiet funkciju <strong>WHERE</strong> vai atbilstošā formāta elementa izteiksmi <strong>Enabled</strong>.</blockquote></td>
</tr>
<tr class="even">
<td>FILTER (saraksts, nosacījums)</td>
<td>Atgrieziet norādīto sarakstu, kad vaicājums ir modificēts filtrēšanai atbilstoši norādītajam nosacījumam. Šī funkcija atšķiras no funkcijas <strong>WHERE</strong>, jo norādītais nosacījums tiek lietots datu bāzes līmenī visiem ER datu avotiem ar tipu <strong>Tabulas ieraksti</strong>. Sarakstu un nosacījumu var definēt, izmantojot tabulas un relācijas.</td>
  <td>Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, <strong>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu. Ja parametrs <strong>Vendor</strong> ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu <strong>VendTable</strong>, un parametrs <strong>parmVendorBankGroup</strong>, kas ir konfigurēts kā ER datu avots, atgriež vērtību ar virknes datu tipu, <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> atgriež tikai noteiktā banku grupā ietverto kreditoru kontu sarakstu.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loģiskas funkcijas

| Funkcija | apraksts | Paraugs |
|----------|-------------|---------|
| CASE (izteiksme, 1. opcija, 1. rezultāts \[, 2. opcija, 2. rezultāts\] … \[, noklusējuma rezultāts\]) | Norādītās izteiksmes vērtību novērtēt pret norādītajām alternatīvajām opcijām. Atgrieziet tās opcijas rezultātu, kas ir vienāda ar izteiksmes vērtību. Pretējā gadījumā atgrieziet pēc izvēles ievadīto noklusējuma rezultātu, ja noklusējuma rezultāts ir norādīts. (Noklusējuma rezultāts ir pēdējais parametrs, kura priekšā neatrodas opcija.) | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** atgriež virkni **"WINTER"**, ja pašreizējās Finance and Operations sesijas datums ir diapazonā no oktobra līdz decembrim. Pretējā gadījumā šī izteiksme atgriež tukšu virkni. |
| IF (nosacījums, 1. vērtība, 2. vērtība) | Atgrieziet pirmo norādīto vērtību, ja norādītais nosacījums tiek izpildīts. Pretējā atgrieziet otro norādīto vērtību. Ja 1. vērtība un 2. vērtība ir ieraksti vai ierakstu saraksti, rezultātā ir ietverti tikai tie lauki, kas ir iekļauti abos sarakstos. | **IF (1=2, "nosacījums tiek izpildīts", "nosacījums netiek izpildīts")** atgriež virkni **"nosacījums netiek izpildīts"**. |
| NOT (nosacījums) | Atgriezt norādītā nosacījuma pretējo loģisko vērtību. | **NOT (TRUE)** atgriež **FALSE**. |
| AND (1. nosacījums\[, 2. nosacījums, …\]) | Atgriež **TRUE**, ja *visi* norādītie nosacījumi ir patiesi. Pretējā gadījumā atgriezt vērtību **FALSE**. | **AND (1=1, "a"="a")** atgriež **TRUE**. **AND (1=2, "a"="a")** atgriež **FALSE**. |
| OR (1. nosacījums\[, 2. nosacījums, …\]) | Atgriež **FALSE**, ja *visi* norādītie nosacījumi ir aplami. Atgriež **TRUE**, ja *kāds* no norādītajiem nosacījumiem ir patiess. | **OR (1=2, "a"="a")** atgriež **TRUE**. |

### <a name="mathematical-functions"></a>Matemātiskās funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| ABS (skaitlis) | Atgrieziet norādītā skaitļa absolūto vērtību. (Tas ir, atgrieziet skaitli bez tā zīmes.) | **ABS (-1)** atgriež **1**. |
| POWER (skaitlis, pakāpe) | Atgriezt rezultātu norādītā pozitīvā skaitļa kāpināšanai norādītajā pakāpē. | **POWER (10, 2)** atgriež **100**. |
| NUMBERVALUE (virkne, decimāldaļu atdalītājs, ciparu grupēšanas atdalītājs) | Norādīto virkni pārveidot par skaitli. Norādītais decimāldaļu atdalītājs tiek lietots starp decimāldaļskaitļa veselo skaitli un daļskaitļiem. Norādītais ciparu grupēšanas atdalītājs tiek izmantots kā tūkstošu atdalītājs. | **NUMBERVALUE("1 234,56", ",", " ")** atgriež vērtību **1234.56**. |
| VALUE (vērtība) | Norādīto virkni pārveidot par skaitli. Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme. Parādiet izņēmumu, ja norādītajā virknē ir ietvertas citas rakstzīmes, kas nav skaitļi. | **VALUE ("1 234,56")** parāda izņēmumu. |
| ROUND (skaitlis, cipari aiz komata) | Atgrieziet norādīto skaitli, kas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.<ul><li>Ja decimāldaļskaitļa parametra vērtība ir lielāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz attiecīgajam ciparu skaitam aiz komata.</li><li>Ja decimāldaļskaitļa parametra vērtība ir **0** (nulle), norādītais skaitlis tiek noapaļots tuvākajam veselajam skaitlim.</li><li>Ja decimāldaļskaitļa parametra vērtība ir mazāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz cipariem, kas atrodas pa kreisi no komata.</li></ul> | **ROUND (1200.767, 2)** noapaļo līdz diviem cipariem aiz komata un atgriež **1200.77**. **ROUND (1200.767, -3)** noapaļo līdz tuvākajam 1,000 reizinājumam un atgriež **1000**. |
| ROUNDDOWN (skaitlis, cipari aiz komata) | Atgrieziet norādīto skaitli, kas ir noapaļots uz leju līdz norādītajam ciparu skaitam aiz komata.<blockquote>[!NOTE]<br>Šī funkcija darbojas līdzīgi funkcijai <strong>ROUND</strong>, bet norādīto skaitli tā vienmēr noapaļo uz leju (nulles virzienā).</blockquote> | **ROUNDDOWN (1200.767, 2)** noapaļo uz leju līdz diviem cipariem aiz komata un atgriež **1200.76**. **ROUNDDOWN (1700.767, -3)** noapaļo uz leju līdz tuvākajam 1,000 reizinājumam un atgriež **1000**. |
| ROUNDUP (skaitlis, cipari aiz komata) | Atgrieziet norādīto skaitli, kas ir noapaļots uz augšu līdz norādītajam ciparu skaitam aiz komata.<blockquote>[!NOTE]<br>Šī funkcija darbojas līdzīgi funkcijai <strong>ROUND</strong>, bet norādīto skaitli tā vienmēr noapaļo uz augšu (prom no nulles).</blockquote> | **ROUNDUP (1200.763, 2)** noapaļo uz augšu līdz diviem cipariem aiz komata un atgriež **1200.77**. **ROUNDUP (1200.767, -3)** noapaļo uz augšu līdz tuvākajam 1,000 reizinājumam un atgriež **2000**. |

### <a name="data-conversion-functions"></a>Datu konvertēšanas funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| VALUE (vērtība) | Norādīto virkni pārveidot par skaitli. Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme. Parādiet izņēmumu, ja norādītajā virknē ir ietvertas citas rakstzīmes, kas nav skaitļi. | **VALUE ("1 234,56")** parāda izņēmumu. |
| NUMBERVALUE (virkne, decimāldaļu atdalītājs, ciparu grupēšanas atdalītājs) | Norādīto virkni pārveidot par skaitli. Norādītais decimāldaļu atdalītājs tiek lietots starp decimāldaļskaitļa veselo skaitli un daļskaitļiem. Norādītais ciparu grupēšanas atdalītājs tiek izmantots kā tūkstošu atdalītājs. | **NUMBERVALUE("1 234,56", ",", " ")** atgriež **1234.56**. |
| INTVALUE (virkne) | Atgrieziet veselu skaitļu attēlojumu norādītajai virknei. Tiek aprautas visas decimāldaļas. | **INTVALUE ("100.77")** atgriež **100**. |
| INTVALUE (skaitlis) | Atgrieziet veselu skaitļu attēlojumu norādītajam skaitlim. Tiek aprautas visas decimāldaļas. | **INTVALUE (-100.77)** atgriež **-100**. |
| INT64VALUE (virkne) | Atgrieziet int64 attēlojumu norādītajai virknei. Tiek aprautas visas decimāldaļas. | **INT64VALUE ("22565422744")** atgriež **22565422744**. |
| INT64VALUE (skaitlis) | Atgrieziet int64 attēlojumu norādītajam skaitlim. Tiek aprautas visas decimāldaļas. | **INT64VALUE (22565422744.00)** atgriež **22565422744**. |

### <a name="record-functions"></a>Ieraksta funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| NULLCONTAINER (saraksts) | Atgriezt ierakstu **null**, kam ir tāda pati struktūra kā norādītajam ierakstu sarakstam vai ierakstam.<blockquote>[!NOTE]<br>Šī funkcija ir novecojusi. Tās vietā lietojiet <strong>EMPTYRECORD</strong>.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** atgriež jaunu tukšu ierakstu, kam ir tāda pati struktūra kā sarakstam, ko atgrieza funkcija **SPLIT**. |
| EMPTYRECORD (ieraksts) | Atgriezt ierakstu **null**, kam ir tāda pati struktūra kā norādītajam ierakstu sarakstam vai ierakstam.<blockquote>[!NOTE]<br>Ieraksts <strong>null</strong> ir ieraksts, kurā visos laukos ir tukšas vērtības. Tukša vērtība skaitļiem ir <strong>0</strong> (nulle), virknēm tā ir tukša virkne utt.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** atgriež jaunu tukšu ierakstu, kam ir tāda pati struktūra kā sarakstam, ko atgrieza funkcija **SPLIT**. |

### <a name="text-functions"></a>Teksta funkcijas

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkcija</th>
<th>apraksts</th>
<th>Paraugs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (virkne)</td>
<td>Atgrieziet norādīto virkni, kas ir pārveidota par lielajiem burtiem.</td>
<td><strong>UPPER(&quot;Piemērs&quot;)</strong> atgriež <strong>&quot;PIEMĒRS&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (virkne)</td>
<td>Atgrieziet norādīto virkni, kas ir pārveidota par mazajiem burtiem.</td>
<td><strong>LOWER (&quot;Piemērs&quot;)</strong> atgriež <strong>&quot;piemērs&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (virkne, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes sākuma.</td>
<td><strong>LEFT (&quot;Piemērs&quot;, 3)</strong> atgriež <strong>&quot;Pie&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (virkne, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes beigām.</td>
<td><strong>RIGHT (&quot;Piemērs&quot;, 3)</strong> atgriež <strong>&quot;ērs&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (virkne, sākuma pozīcija, rakstzīmju skaits)</td>
<td>Atgriezt noteikto rakstzīmju skaitu no norādītās virknes, sākot norādītajā pozīcijā.</td>
<td><strong>MID (&quot;Piemērs&quot;, 2, 3)</strong> atgriež <strong>&quot;mēr&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (virkne)</td>
<td>Atgriezt norādītajā virknē esošo rakstzīmju skaitu.</td>
<td><strong>LEN (&quot;Piemērs&quot;)</strong> atgriež <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (skaitlis)</td>
<td>Atgriezt rakstzīmju virkni, uz ko atsaucas norādītais unikoda skaitlis.</td>
<td><strong>CHAR (255)</strong> atgriež <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE]<br>
Šīs funkcijas atgrieztā virkne ir atkarīga kodējuma, kas ir atlasīts vecākelementa formāta elementā FILE. Atbalstīto kodējumu sarakstu skatiet tēmā <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodējuma klase</a>.</blockquote>
</td>
</tr>
<tr class="even">
<td>CONCATENATE (1. virkne [, 2. virkne, …])</td>
<td>Atgrieziet visas norādītās teksta virknes, kas ir savienotas vienā virknē.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> atgriež <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE]<br>
Arī izteiksme <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> atgriež <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr class="odd">
<td>TRANSLATE (virkne, raksts, aizstājējs)</td>
<td>Atgrieziet norādīto virkni, kurā visi norādītajā raksta virknē esošie rakstzīmju gadījumi ir aizstāti ar rakstzīmēm, kas atrodas norādītās aizstāšanas virknes atbilstošajā pozīcijā.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> aizstāj burtus <strong>&quot;cd&quot;</strong> ar virkni <strong>&quot;GH&quot;</strong> un atgriež <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (virkne, raksts, aizstājējs, parastas izteiksmes karodziņš)</td>
<td>Ja norādītās parastās izteiksmes karodziņš ir <strong>true</strong>, atgrieziet norādīto virkni, kas ir modificēta, lietojot šai funkcijai kā raksta argumentu norādīto parasto izteiksmi. Šī izteiksme tiek izmantota, lai atrastu rakstzīmes, kas ir jāaizstāj. Norādītā aizstāšanas argumenta rakstzīmes tiek izmantotas, lai aizstātu atrastās rakstzīmes. Ja norādītās parastās izteiksmes karogs ir <strong>false</strong>, šī funkcija darbojas kā <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> lieto parastu izteiksmi, kas noņem visus simbolus, kuri nav skaitļi, un atgriež <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> aizstāj burtus <strong>&quot;cd&quot;</strong> ar virkni <strong>&quot;GH&quot;</strong> un atgriež <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (ievade)</td>
<td>Atgrieziet norādīto ievadi, kas ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās Finance and Operations instances servera lokalizācijas iestatījumiem. Vērtībām ar tipu <strong>real</strong> šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.</td>
<td>Ja Finance and Operations instances servera lokalizācija ir definēta kā <strong>EN-US</strong>, <strong>TEXT (NOW ())</strong> pašreizējo Finance and Operations sesijas datumu, 2015. gada 17. decembri, atgriež kā teksta virkni <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> atgriež <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (1. virkne, 2. virkne[, 3. virkne, …])</td>
<td>Atgrieziet norādīto virkni, kas ir formatēta, visus <strong>%N</strong> gadījumus aizstājot ar <em>n</em>-to argumentu. Argumenti ir virknes. Ja nav norādīts parametra arguments, šis parametrs virknē tiek atgriezts kā <strong>&quot;%N&quot;</strong>. Vērtībām ar tipu <strong>real</strong> šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.</td>
<td>Tālāk esošajā attēlā redzamais datu avots <strong>PaymentModel</strong> atgriež sarakstu ar debitoru ierakstiem, izmantojot komponentu <strong>Customer</strong>, un apstrādāšanas datuma vērtību, izmantojot lauku <strong>ProcessingDate</strong>.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>ER formātā, kas ir izveidots tā, lai ģenerētu elektronisku failu noteiktiem debitoriem, vienums <strong>PaymentModel</strong> ir atlasīts kā datu avots, un tas kontrolē procesa plūsmu. Lietotājiem tiek parādīts izņēmums, lai viņus informētu par to, kad atlasītais debitors tiek apturēts datumam, kad atskaite tiek apstrādāta. Šāda tipa apstrādes kontrolei izveidotā formulā var izmantot šādus resursus:</p>
<ul>
<li>Finance and Operations etiķete SYS70894, kurā ir šāds teksts:
<ul>
<li><strong>Valodai EN-US:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Valodai DE:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Finance and Operations etiķete SYS18389, kurā ir šāds teksts:
<ul>
<li><strong>Valodai EN-US:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>Valodai DE:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Lūk, kādu formulu varat izveidot:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Ja pārskats debitoram <strong>Litware Retail</strong> tiek apstrādāts 2015. gada 17. decembrī kultūrā <strong>EN-US</strong> un valodā <strong>EN-US</strong>, šī formula atgriež tālāk norādīto tekstu, kuru lietotājam var parādīt kā izņēmuma ziņojumu.</p>
<p>&quot;Nothing to print. Customer Litware Retail is stopped for 12/17/2015.&quot;</p>
<p>Ja tas pats pārskats debitoram <strong>Litware Retail</strong> tiek apstrādāts 2015. gada 17. decembrī kultūrā <strong>DE</strong> un valodā <strong>DE</strong>, šī formula atgriež tālāk norādīto tekstu, kurā izmantots cits datuma formāts.</p>
<p>&quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE]<br>
ER formulās etiķetēm tiek lietota tālāk norādītā sintakse.
<ul>
<li><strong>Etiķetēm no Finance and Operations resursiem:</strong> <strong>@&quot;X&quot;</strong>, kur X ir etiķetes ID lietojumprogrammas objektu kokā (AOT)</li>
<li><strong>Etiķetēm, kas ir ietvertas ER konfigurācijās:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, kur X ir etiķetes ID ER konfigurācijā</li>
</ul></blockquote></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (skaitlis, formāts)</td>
<td>Atgrieziet norādītā skaitļa virknes attēlojumu norādītajā formātā. (Informāciju par atbalstītajiem formātiem skatiet šeit: <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standarta</a> un <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">pielāgotie</a>.) Formāta numuriem izmantotā kultūra ir atkarīga no šīs funkcijas izpildes konteksta.</td>
<td>Kultūrai EN-US <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> atgriež <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> atgriež <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (skaitlis, valoda, valūta, drukas valūtas nosaukuma karogs, cipari aiz komata)</td>
<td>Atgrieziet norādīto skaitli, kas ir izteikts vārdos (pārvērsts) teksta virknēs norādītajā valodā. Valodas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek izmantots izpildes konteksta valodas kods. (Izpildes konteksta valodas kods tiek definēts ģenerēšanas mapei vai failam.) Arī valūtas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek izmantota uzņēmuma valūta.
<blockquote>[!NOTE]<br>
Valūtas nosaukuma drukāšanas karodziņa un ciparu aiz komata parametri tiek analizēti tikai šiem valodu kodiem: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> un <strong>RU</strong>. Turklāt valūtas nosaukuma drukāšanas karodziņa parametrs tiek analizēts tikai tiem Finance and Operations uzņēmumiem, kuru valsts vai reģiona konteksts atbalsta valūtu nosaukumu locījumus.</blockquote></td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> atgriež <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> atgriež <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> atgriež <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>PADLEFT (virkne, garums, papildināšanas rakstzīmes)</td>
<td>Atgrieziet norādītā garuma virkni, kurā norādītās virknes sākumā ir ievadītas norādītās rakstzīmes.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> atgriež teksta virkni <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr class="even">
<td>TRIM (virkne)</td>
<td>Atgrieziet norādīto teksta virkni, kam ir aprautas sākuma un beigu atstarpes un noņemtas vairākas atstarpes starp vārdiem.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sample&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> atgriež <strong>&quot;Sample text&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>GETENUMVALUEBYNAME (uzskaitījuma datu avota ceļš, uzskaitījuma vērtības etiķetes teksts)</td>
<td>Atgrieziet norādītā uzskaitījuma datu avota vērtību atbilstoši uzskaitījuma etiķetes norādītajam tekstam.</td>
<td>Tālāk esošajā attēlā ir parādīts datu modelī ieviests uzskaitījums <strong>ReportDirection</strong>. Ņemiet vērā, ka etiķetes ir definētas uzskaitījumu vērtībām.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.</p>
<ul>
<li>Modeļu uzskaitījums <strong>ReportDirection</strong> ir ievietots pārskatā kā datu avots <strong>$Direction</strong>.</li>
<li>ER izteiksme <strong>$IsArrivals</strong> ir izveidota ar mērķi lietot modeļu uzskaitījumu kā šīs funkcijas parametru. Šīs izteiksmes vērtība ir <strong>TRUE</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Datu konvertēšanas funkcijas

| Funkcija | apraksts | Paraugs |
|----------|-------------|---------|
| TEXT (ievade) | Atgrieziet norādīto ievadi, kas ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās Finance and Operations instances servera lokalizācijas iestatījumiem. Vērtībām ar tipu **real** šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata. | Ja Finance and Operations instances servera lokalizācija ir definēta kā **EN-US**, **TEXT (NOW ())** pašreizējo Finance and Operations sesijas datumu, 2015. gada 17. decembri, atgriež kā teksta virkni **"12/17/2015 07:59:23 AM"**. **TEXT (1/3)** atgriež **"0.33"**. |
| QRCODE (virkne) | Atgrieziet QR koda attēlu base64 binārajā formātā norādītajai virknei. | **QRCODE ("Sample text")** atgriež **U2FtcGxlIHRleHQ=**. |

### <a name="data-collection-functions"></a>Datu apkopošanas funkcijas

| Funkcija | apraksts | Paraugs |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Atgrieziet pašreizējā formāta elementa nosaukumu. Atgrieziet tukšu virkni, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi **ER Lietot formāta izvades datus uzskaitei un summēšanai**, kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**. |
| SUMIFS (galvenā virkne summēšanai, kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\]) | Atgrieziet XML mezglu vērtību summu (ar nosaukumu, kas definēts kā atslēga), kas ir savākts formāta izpildes laikā un nodrošina atbilstību norādītajiem nosacījumiem (diapazonu un vērtību pāriem). Atgrieziet **0** (nulles) vērtību, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |
| SUMIF (atslēgu virkne summēšanai, kritēriju diapazona virkne, kritēriju vērtību virkne) | Atgrieziet XML mezglu vērtību summu (ar nosaukumu, kas definēts kā atslēga), kas ir savākts formāta izpildes laikā un nodrošina atbilstību norādītajam nosacījumam (diapazonam un vērtībai). Atgrieziet **0** (nulles) vērtību, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |
| COUNTIFS (kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\]) | Atgrieziet XML mezglu skaitu, kas ir savākts formāta izpildes laikā un nodrošina atbilstību norādītajiem nosacījumiem (diapazonu un vērtību pāriem). Atgrieziet **0** (nulles) vērtību, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |
| COUNTIF (kritēriju diapazona virkne, kritēriju vērtību virkne) | Atgrieziet XML mezglu skaitu, kas ir savākts formāta izpildes laikā un nodrošina atbilstību norādītajam nosacījumam (diapazonam un vērtībai). Atgrieziet **0** (nulles) vērtību, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |
| COLLECTEDLIST (kritēriju 1. diapazona virkne, kritēriju 1. vērtības virkne \[, kritēriju 2. diapazona virkne, kritēriju 2. vērtības virkne, …\]) | Atgrieziet XML mezglu vērtību sarakstu, kas ir savākts formāta izpildes laikā un nodrošina atbilstību ievadītajiem nosacījumiem (diapazonam un vērtībai). Atgrieziet tukšu sarakstu, ja pašreizējo failu karodziņš **Apkopot izvades informāciju** ir izslēgts. | |

### <a name="other-business-domainspecific-functions"></a>Citas (biznesa jomai specifiskas) funkcijas

| Funkcija | Apraksts | Piemērs |
|----------|-------------|---------|
| CONVERTCURRENCY (summa, avota valūta, mērķa valūta, datums, uzņēmums) | Norādīto naudas summu no norādītās avota valūtas konvertējiet norādītajā mērķa valūtā, izmantojot norādītā Finance and Operations uzņēmuma iestatījumus norādītajā datumā. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** atgriež viena eiro ekvivalentu ASV dolāros pašreizējās sesijas datumā, balstoties uz uzņēmuma DEMF iestatījumiem. |
| ROUNDAMOUNT (skaitlis, cipari aiz komata, noapaļošanas kārtula) | Norādīto summu noapaļojiet līdz norādītajam ciparu skaitam aiz komata saskaņā ar norādīto noapaļošanas kārtulu.<blockquote>[!NOTE]<br>Noapaļošanas kārtula ir jānorāda kā Finance and Operations uzskaitījuma <strong>RoundOffType</strong> vērtība.</blockquote> | Ja ir iestatīta parametra **model.RoundOff** vērtība **Downward**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** atgriež vērtību **1000.78**. Ja parametrs **model.RoundOff** ir iestatīts uz **Normal** vai uz **Rounding-up**, tad **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** atgriež vērtību **1000.79**. |
| CURCredRef (cipari) | Atgriezt kreditora atsauci, pamatojoties uz norādītā rēķina numura cipariem. | **CURCredRef ("VEND-200002")** atgriež **"2200002"**. |
| MOD\_97 (cipari) | Atgriezt kreditora atsauci kā MOD97 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem. | **MOD\_97 ("VEND-200002")** atgriež **"20000285"**. |
| ISOCredRef (cipari) | Atgrieziet Starptautiskās Standartizācijas organizācijas (ISO) kreditora atsauci atbilstoši norādītā rēķina numura cipariem un burtiem.<blockquote>[!NOTE]<br>Lai izslēgtu alfabētu simbolus, kas nav saderīgi ar ISO, šis ievades parametrs pirms nodošanas šai funkcijai ir jātulko.</blockquote> | **ISOCredRef ("VEND-200002")** atgriež **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (virkne, skaitlis) | Iegūt papildu finanšu dimensijas ID. Dimensijas šajā virknē tiek attēlotas kā ar komatiem atdalīti ID. Skaitļi šajā virknē definē pieprasītās dimensijas sērijas kodu. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** atgriež **"CC"**. |
| GetCurrentCompany () | Atgrieziet tās juridiskās personas (uzņēmuma) koda teksta attēlojumu, kurā lietotājs ir pašlaik pierakstījies. | **GETCURRENTCOMPANY ()** atgriež **USMF** lietotājam, kurš ir pierakstījies programmā Finance and Operations uzņēmumā **Contoso Entertainment System USA**. |
| CH\_BANK\_MOD\_10 (cipari) | Atgrieziet kreditora atsauci kā MOD10 izteiksmi atbilstoši norādītā rēķina numura cipariem. | **CH\_BANK\_MOD\_10 ("VEND-200002")** atgriež **3**. |
| FA\_SUM (pamatlīdzekļa kods, vērtības modeļa kods, sākuma datums, beigu datums) | Atgrieziet sagatavoto norādītā perioda pamatlīdzekļu summas datu konteineru. | **FA\_SUM ("COMP-000001", "Current", Date1, Date2)** atgriež sagatavoto datu konteineru pamatlīdzeklim **"COMP-000001"** ar vērtības modeli **"Current"** par periodu no **Date1** līdz **Date2**. |
| FA\_BALANCE (pamatlīdzekļa kods, vērtības modeļa kods, pārskata gads, pārskata datums) | Atgrieziet sagatavoto pamatlīdzekļu bilances datu konteineru. Pārskata gads ir jānorāda kā Finance and Operations uzskaitījuma **AssetYear** vērtība. | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** atgriež sagatavoto datu konteineru no bilancēm pamatlīdzeklim **"COMP-000001"** ar vērtības modeli **"Current"** pašreizējā Finance and Operations sesijas datumā. |
| TABLENAME2ID (virkne) | Atgrieziet tabulas ID veselu skaitļu attēlojumu norādītajam tabulas nosaukumam. | **TABLENAME2ID ("Intrastat")** atgriež **1510**. |
| ISVALIDCHARACTERISO7064 (virkne) | Atgrieziet Būla vērtību **TRUE**, ja norādītā virkne attēlo derīgu starptautisko bankas konta numuru (IBAN). Pretējā gadījumā tiks atgriezta Būla vērtība **FALSE**. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** atgriež **TRUE**. **ISVALIDCHARACTERISO7064 ("AT61")** atgriež **FALSE**. |

### <a name="functions-list-extension"></a>Funkciju saraksta paplašināšana

ER jums ļauj paplašināt funkciju sarakstu, kuras tiek lietotas ER izteiksmēs. Ir jāveic noteiktas tehniskas darbības. Papildinformāciju skatiet rakstā [Elektronisko atskaišu veidošanas funkciju saraksta paplašināšana](general-electronic-reporting-formulas-list-extension.md).

## <a name="see-also"></a>Skatiet arī

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Paplašināt elektronisko pārskatu veidošanas (ER) funkciju sarakstu](general-electronic-reporting-formulas-list-extension.md)

